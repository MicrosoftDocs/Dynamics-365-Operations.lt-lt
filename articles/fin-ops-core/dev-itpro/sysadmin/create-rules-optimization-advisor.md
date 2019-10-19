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
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180995"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="d70dd-103">Optimizavimo patariamojo įrankio taisyklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="d70dd-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d70dd-104">Šioje temoje paaiškinama, kaip sukurti naujų **optimizavimo patariamojo įrankio** taisyklių.</span><span class="sxs-lookup"><span data-stu-id="d70dd-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="d70dd-105">Pavyzdžiui, galite sukurti naują taisyklę, nustatančią, kurių pasiūlymų patvirtinimų (RFQ) atvejų pavadinimai yra tušti.</span><span class="sxs-lookup"><span data-stu-id="d70dd-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="d70dd-106">Naudojant atvejų pavadinimus, juos lengva nustatyti ir jų ieškoti.</span><span class="sxs-lookup"><span data-stu-id="d70dd-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="d70dd-107">Nors šis pavyzdys gana paprastas, juo parodoma, ko galima pasiekti optimizavimo taisyklėmis.</span><span class="sxs-lookup"><span data-stu-id="d70dd-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="d70dd-108">*Taisyklė* yra programos duomenų patikra.</span><span class="sxs-lookup"><span data-stu-id="d70dd-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="d70dd-109">Jei išpildoma sąlyga, kurią vertina taisyklė, sukuriama galimybių optimizuoti procesus ar patobulinti duomenis.</span><span class="sxs-lookup"><span data-stu-id="d70dd-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="d70dd-110">Dėl galimybių galima imtis veiksmų ir (pasirenkama) galima matuoti veiksmų poveikį.</span><span class="sxs-lookup"><span data-stu-id="d70dd-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="d70dd-111">Norėdami sukurti naują **optimizavimo patariamojo įrankio** taisyklę, įtraukite naują klasę, išplečiančią abstrakčią klasę **SelfHealingRule**, įdiegiančią **IDiagnosticsRule** sąsają ir kurią įformina atributas **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="d70dd-112">Klasėje taip pat turi būti metodas, kurį įformina atributas **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="d70dd-113">Paprastai tai daroma naudojant metodą **opportunityTitle**, kuris bus aptartas vėliau.</span><span class="sxs-lookup"><span data-stu-id="d70dd-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="d70dd-114">Šią naująją klasę galima įtraukti į pasirinktinį modelį su priklausomybe modelyje **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="d70dd-115">Tolesniame pavyzdyje įdiegiama taisyklė vadinama **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="d70dd-116">Abstrakčioje klasėje **SelfHealingRule** yra abstrakčių metodų, kuriuos reikia įdiegti paveldinčiose klasėse.</span><span class="sxs-lookup"><span data-stu-id="d70dd-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="d70dd-117">Pagrindas yra metodas **įvertinti**, kuris pateikia taisyklės nustatytų galimybių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d70dd-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="d70dd-118">Galimybės gali būti taikomos vienam juridiniam subjektui arba visai sistemai.</span><span class="sxs-lookup"><span data-stu-id="d70dd-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
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

<span data-ttu-id="d70dd-119">Aukščiau parodytas metodas analizuoja įmones ir pasirenka RFQ atvejus su tuščiais pavadinimais metode **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="d70dd-120">Jei randamas bent vienas toks atvejis, naudojant metodą **getOpportunityForCompany** sukuriama konkrečios įmonės galimybė.</span><span class="sxs-lookup"><span data-stu-id="d70dd-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="d70dd-121">Atkreipkite dėmesį, kad lentelės **SelfHealingOpportunity** lauko **Duomenys** tipas yra **Konteineris**, todėl jame gali būti duomenų, susijusių su šiai taisyklei būdinga logika.</span><span class="sxs-lookup"><span data-stu-id="d70dd-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="d70dd-122">Elemente **OpportunityDate** nustačius dabartinę laiko žymą, užregistruojamas vėliausio galimybės įvertinimo laikas.</span><span class="sxs-lookup"><span data-stu-id="d70dd-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="d70dd-123">Galimybės taip pat gali būti taikomos visoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="d70dd-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="d70dd-124">Tokiu atveju įmonių analizė nebūtina ir galimybę reikia kurti naudojant metodą **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="d70dd-125">Tolesniame kode rodomas metodas **findRFQCasesWithEmptyTitle**, pateikiantis RFQ atvejų tuščiais pavadinimais ID.</span><span class="sxs-lookup"><span data-stu-id="d70dd-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
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

<span data-ttu-id="d70dd-126">Dar du įdiegtini metodai yra **opportunityTitle** ir **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="d70dd-127">Pirmasis pateikia trumpą galimybės pavadinimą, pastarasis pateikia išsamų galimybės aprašą, kuriame taip pat gali būti duomenų.</span><span class="sxs-lookup"><span data-stu-id="d70dd-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="d70dd-128">Pavadinimas, kurį pateikia **opportunityTitle**, rodomas darbo srities **Optimizavimo patariamasis įrankis** stulpelyje **Optimizavimo galimybė**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="d70dd-129">Jis taip pat rodomas kaip šoninės srities, kurioje apie galimybę rodoma daugiau informacijos, antraštė.</span><span class="sxs-lookup"><span data-stu-id="d70dd-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="d70dd-130">Paprastai šį metodą įformina atributas **DiagnosticRuleSubscription**, su kuriuo galima naudoti tolesnius argumentus.</span><span class="sxs-lookup"><span data-stu-id="d70dd-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="d70dd-131">**Diagnostikos sritis** – tipo **DiagnosticArea** išvardijimas, apibrėžiantis, kuriai programos sričiai priklauso taisyklė, pvz., **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="d70dd-132">**Taisyklės pavadinimas** – eilutė su taisyklės pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="d70dd-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="d70dd-133">Ji bus rodoma formos **Diagnostikos tikrinimo taisyklė** stulpelyje **Taisyklės pavadinimas** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="d70dd-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="d70dd-134">**Vykdymo dažnis** – tipo **DiagnosticRunFrequency** išvardijimas, aprašantis, kaip dažnai taisyklę reikėtų vykdyti, pvz., **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="d70dd-135">**Taisyklės aprašas** – eilutė su išsamesniu taisyklės aprašu.</span><span class="sxs-lookup"><span data-stu-id="d70dd-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="d70dd-136">Ji bus rodoma formos **Diagnostikos tikrinimo taisyklė** stulpelyje **Taisyklės aprašas** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="d70dd-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="d70dd-137">Kad taisyklė veiktų, reikalingas atributas **DiagnosticRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="d70dd-138">Paprastai jis naudojamas su **opportunityTitle**, tačiau gali įforminti bet kurį klasės metodą.</span><span class="sxs-lookup"><span data-stu-id="d70dd-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="d70dd-139">Toliau pateikiamas diegimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="d70dd-139">The following is an example implementation.</span></span> <span data-ttu-id="d70dd-140">Kad būtų paprasčiau, naudojamos neapdorotos eilutės, tačiau, norint diegti tinkamai, reikia naudoti žymas.</span><span class="sxs-lookup"><span data-stu-id="d70dd-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="d70dd-141">Aprašas, kurį pateikia **opportunityDetails**, rodomas šoninėje srityje, kurioje apie galimybę rodoma daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="d70dd-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="d70dd-142">Su juo galima naudoti argumentą **SelfHealingOpportunity**, kuris yra laukas **Duomenys** ir kurį naudojant apie galimybę galima pateikti daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="d70dd-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="d70dd-143">Pavyzdyje metodas pateikia RFQ atvejų tuščiu pavadinimu ID.</span><span class="sxs-lookup"><span data-stu-id="d70dd-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
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

<span data-ttu-id="d70dd-144">Du likę įgyvendinti abstraktūs metodai yra **provideHealingAction** ir **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="d70dd-145">Jei nurodomas atkūrimo veiksmas, **provideHealingAction** pateikia true, kitu atveju pateikiama false.</span><span class="sxs-lookup"><span data-stu-id="d70dd-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="d70dd-146">Jei pateikiama true, turi būti įdiegtas metodas **performAction**, kitaip bus pateikta klaida.</span><span class="sxs-lookup"><span data-stu-id="d70dd-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="d70dd-147">Su metodu **performAction** galima naudoti argumentą **SelfHealingOpportunity**, kuriame su veiksmu galima naudoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="d70dd-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="d70dd-148">Pavyzdyje veiksmas atidaro **PurchRFQCaseTableListPage**, kad būtų galima koreguoti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="d70dd-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="d70dd-149">Gali būti įmanoma naudojant galimybės duomenis imtis automatinių veiksmų – tai priklauso nuo konkrečių taisyklės duomenų.</span><span class="sxs-lookup"><span data-stu-id="d70dd-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="d70dd-150">Šiame pavyzdyje sistema galėtų automatiškai generuoti RFQ atvejų pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="d70dd-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="d70dd-151">**securityMenuItem** pateikia veiksmų meniu elemento pavadinimą, kad taisyklę galėtų matyti tik veiksmų meniu elementą galintys pasiekti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="d70dd-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="d70dd-152">Saugos sumetimais gali būti reikalaujama, kad konkrečias taisykles ir galimybes galėtų pasiekti tik įgaliotieji vartotojai.</span><span class="sxs-lookup"><span data-stu-id="d70dd-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="d70dd-153">Pavyzdyje peržiūrėti galimybę gali tik prieigą prie **PurchRFQCaseTitleAction** turintys vartotojai.</span><span class="sxs-lookup"><span data-stu-id="d70dd-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="d70dd-154">Atkreipkite dėmesį, kad šis veiksmų meniu elementas buvo sukurtas šiam pavyzdžiui ir buvo įtrauktas kaip saugos teisės **PurchRFQCaseTableMaintain** įvesties taškas.</span><span class="sxs-lookup"><span data-stu-id="d70dd-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="d70dd-155">Meniu elementas turi būti veiksmų meniu elementas, kad sauga veiktų tinkamai.</span><span class="sxs-lookup"><span data-stu-id="d70dd-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="d70dd-156">Kiti meniu elementų tipai, pvz., **Rodymo meniu elementai** veiks netinkamai.</span><span class="sxs-lookup"><span data-stu-id="d70dd-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="d70dd-157">Sukompiliavę taisyklę, vykdykite tolesnę užduotį, kad ji būtų rodoma vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="d70dd-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
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

<span data-ttu-id="d70dd-158">Taisyklė bus rodoma formoje **Diagnostikos tikrinimo taisyklė**, kurią galima rasti dalyje **Sistemos administravimas** > **Periodinės užduotys** > **Tvarkyti diagnostikos tikrinimo taisyklę**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="d70dd-159">Norėdami ją įvertinti, eikite į **Sistemos administravimas** > **Periodinės užduotys** > **Planuoti diagnostikos tikrinimo taisyklę**, pasirinkite taisyklės dažnį, pvz., **Kasdien**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="d70dd-160">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-160">Click **OK**.</span></span> <span data-ttu-id="d70dd-161">Norėdami peržiūrėti naująją galimybę, eikite į **Sistemos administravimas** > **Optimizavimo patariamasis įrankis**.</span><span class="sxs-lookup"><span data-stu-id="d70dd-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="d70dd-162">Toliau pateiktas pavyzdys yra kodo fragmentas su taisyklės griaučiais, apimančiais visus reikiamus metodus ir atributus.</span><span class="sxs-lookup"><span data-stu-id="d70dd-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="d70dd-163">Tai jums padės pradėti rašyti naujas taisykles.</span><span class="sxs-lookup"><span data-stu-id="d70dd-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="d70dd-164">Pavyzdyje pateiktos etiketės ir veiksmų meniu elementai naudojami tik demonstraciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="d70dd-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
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

<span data-ttu-id="d70dd-165">Norėdami gauti daugiau informacijos, peržiūrėkite trumpą „YouTube“ vaizdo įrašą: [Optimizavimo patarėjas naudojant „Dynamics 365 for Finance and Operations“](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="d70dd-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
