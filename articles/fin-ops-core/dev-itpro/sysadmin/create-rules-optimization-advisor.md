---
title: Optimizavimo patariamojo įrankio taisyklių kūrimas
description: Šioje temoje aptariama, kaip į optimizavimo patariamąjį įrankį įtraukti naujų taisyklių.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e14949b871534868c42d2b26a116e10ff9f05179
ms.sourcegitcommit: 8ff2413b6cb504d2b36fce2bb50441b2e690330e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/24/2020
ms.locfileid: "3082001"
---
# <a name="create-rules-for-optimization-advisor"></a>Optimizavimo patariamojo įrankio taisyklių kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukurti naujų **optimizavimo patariamojo įrankio** taisyklių. Pavyzdžiui, galite sukurti naują taisyklę, nustatančią, kurių pasiūlymų patvirtinimų (RFQ) atvejų pavadinimai yra tušti. Naudojant atvejų pavadinimus, juos lengva nustatyti ir jų ieškoti. Nors šis pavyzdys gana paprastas, juo parodoma, ko galima pasiekti optimizavimo taisyklėmis. 

*Taisyklė* yra programos duomenų patikra. Jei išpildoma sąlyga, kurią vertina taisyklė, sukuriama galimybių optimizuoti procesus ar patobulinti duomenis. Dėl galimybių galima imtis veiksmų ir (pasirenkama) galima matuoti veiksmų poveikį. 

Norėdami sukurti naują **optimizavimo patariamojo įrankio** taisyklę, įtraukite naują klasę, išplečiančią abstrakčią klasę **SelfHealingRule**, įdiegiančią **IDiagnosticsRule** sąsają ir kurią įformina atributas **DiagnosticRule**. Klasėje taip pat turi būti metodas, kurį įformina atributas **DiagnosticsRuleSubscription**. Paprastai tai daroma naudojant metodą **opportunityTitle**, kuris bus aptartas vėliau. Šią naująją klasę galima įtraukti į pasirinktinį modelį su priklausomybe modelyje **SelfHealingRules**. Tolesniame pavyzdyje įdiegiama taisyklė vadinama **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Abstrakčioje klasėje **SelfHealingRule** yra abstrakčių metodų, kuriuos reikia įdiegti paveldinčiose klasėse. Pagrindas yra metodas **įvertinti**, kuris pateikia taisyklės nustatytų galimybių sąrašą. Galimybės gali būti taikomos vienam juridiniam subjektui arba visai sistemai.

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

Aukščiau parodytas metodas analizuoja įmones ir pasirenka RFQ atvejus su tuščiais pavadinimais metode **findRFQCasesWithEmptyTitle**. Jei randamas bent vienas toks atvejis, naudojant metodą **getOpportunityForCompany** sukuriama konkrečios įmonės galimybė. Atkreipkite dėmesį, kad lentelės **SelfHealingOpportunity** lauko **Duomenys** tipas yra **Konteineris**, todėl jame gali būti duomenų, susijusių su šiai taisyklei būdinga logika. Elemente **OpportunityDate** nustačius dabartinę laiko žymą, užregistruojamas vėliausio galimybės įvertinimo laikas.  

Galimybės taip pat gali būti taikomos visoje įmonėje. Tokiu atveju įmonių analizė nebūtina ir galimybę reikia kurti naudojant metodą **getOpportunityAcrossCompanies**. 

Tolesniame kode rodomas metodas **findRFQCasesWithEmptyTitle**, pateikiantis RFQ atvejų tuščiais pavadinimais ID.

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

Dar du įdiegtini metodai yra **opportunityTitle** ir **opportunityDetails**. Pirmasis pateikia trumpą galimybės pavadinimą, pastarasis pateikia išsamų galimybės aprašą, kuriame taip pat gali būti duomenų.

Pavadinimas, kurį pateikia **opportunityTitle**, rodomas darbo srities **Optimizavimo patariamasis įrankis** stulpelyje **Optimizavimo galimybė**. Jis taip pat rodomas kaip šoninės srities, kurioje apie galimybę rodoma daugiau informacijos, antraštė. Paprastai šį metodą įformina atributas **DiagnosticRuleSubscription**, su kuriuo galima naudoti tolesnius argumentus. 

* **Diagnostikos sritis** – tipo **DiagnosticArea** išvardijimas, apibrėžiantis, kuriai programos sričiai priklauso taisyklė, pvz., **DiagnosticArea::SCM**. 

* **Taisyklės pavadinimas** – eilutė su taisyklės pavadinimu. Ji bus rodoma formos **Diagnostikos tikrinimo taisyklė** stulpelyje **Taisyklės pavadinimas** (**DiagnosticsValidationRuleMaintain**). 

* **Vykdymo dažnis** – tipo **DiagnosticRunFrequency** išvardijimas, aprašantis, kaip dažnai taisyklę reikėtų vykdyti, pvz., **DiagnosticRunFrequency::Daily**. 

* **Taisyklės aprašas** – eilutė su išsamesniu taisyklės aprašu. Ji bus rodoma formos **Diagnostikos tikrinimo taisyklė** stulpelyje **Taisyklės aprašas** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Kad taisyklė veiktų, reikalingas atributas **DiagnosticRuleSubscription**. Paprastai jis naudojamas su **opportunityTitle**, tačiau gali įforminti bet kurį klasės metodą.

Toliau pateikiamas diegimo pavyzdys. Kad būtų paprasčiau, naudojamos neapdorotos eilutės, tačiau, norint diegti tinkamai, reikia naudoti žymas. 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

Aprašas, kurį pateikia **opportunityDetails**, rodomas šoninėje srityje, kurioje apie galimybę rodoma daugiau informacijos. Su juo galima naudoti argumentą **SelfHealingOpportunity**, kuris yra laukas **Duomenys** ir kurį naudojant apie galimybę galima pateikti daugiau informacijos. Pavyzdyje metodas pateikia RFQ atvejų tuščiu pavadinimu ID. 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

Du likę įgyvendinti abstraktūs metodai yra **provideHealingAction** ir **securityMenuItem**. 

Jei nurodomas atkūrimo veiksmas, **provideHealingAction** pateikia true, kitu atveju pateikiama false. Jei pateikiama true, turi būti įdiegtas metodas **performAction**, kitaip bus pateikta klaida. Su metodu **performAction** galima naudoti argumentą **SelfHealingOpportunity**, kuriame su veiksmu galima naudoti duomenis. Pavyzdyje veiksmas atidaro **PurchRFQCaseTableListPage**, kad būtų galima koreguoti rankiniu būdu. 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

Gali būti įmanoma naudojant galimybės duomenis imtis automatinių veiksmų – tai priklauso nuo konkrečių taisyklės duomenų. Šiame pavyzdyje sistema galėtų automatiškai generuoti RFQ atvejų pavadinimus. 

**securityMenuItem** pateikia veiksmų meniu elemento pavadinimą, kad taisyklę galėtų matyti tik veiksmų meniu elementą galintys pasiekti vartotojai. Saugos sumetimais gali būti reikalaujama, kad konkrečias taisykles ir galimybes galėtų pasiekti tik įgaliotieji vartotojai. Pavyzdyje peržiūrėti galimybę gali tik prieigą prie **PurchRFQCaseTitleAction** turintys vartotojai. Atkreipkite dėmesį, kad šis veiksmų meniu elementas buvo sukurtas šiam pavyzdžiui ir buvo įtrauktas kaip saugos teisės **PurchRFQCaseTableMaintain** įvesties taškas. 

> [!NOTE]
> Meniu elementas turi būti veiksmų meniu elementas, kad sauga veiktų tinkamai. Kiti meniu elementų tipai, pvz., **Rodymo meniu elementai** veiks netinkamai.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Sukompiliavę taisyklę, vykdykite tolesnę užduotį, kad ji būtų rodoma vartotojo sąsajoje (UI).

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

Taisyklė bus rodoma formoje **Diagnostikos tikrinimo taisyklė**, kurią galima rasti dalyje **Sistemos administravimas** > **Periodinės užduotys** > **Tvarkyti diagnostikos tikrinimo taisyklę**. Norėdami ją įvertinti, eikite į **Sistemos administravimas** > **Periodinės užduotys** > **Planuoti diagnostikos tikrinimo taisyklę**, pasirinkite taisyklės dažnį, pvz., **Kasdien**. Spustelėkite **Gerai**. Norėdami peržiūrėti naująją galimybę, eikite į **Sistemos administravimas** > **Optimizavimo patariamasis įrankis**. 

Toliau pateiktas pavyzdys yra kodo fragmentas su taisyklės griaučiais, apimančiais visus reikiamus metodus ir atributus. Tai jums padės pradėti rašyti naujas taisykles.Pavyzdyje pateiktos etiketės ir veiksmų meniu elementai naudojami tik demonstraciniais tikslais.

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

Norėdami gauti daugiau informacijos, peržiūrėkite trumpą „YouTube“ vaizdo įrašą: [Optimizavimo patarėjas naudojant „Dynamics 365 for Finance and Operations“](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
