---
title: "Analizės įtraukimas į darbo sritis naudojant „Power BI Embedded“"
description: "Šioje temoje rodoma, kaip įterpti „Power BI“ ataskaitą darbo srities skirtuke Analizė."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 3f6b83166ba942e40e5e1f7c0ef9df40a44bfbc5
ms.contentlocale: lt-lt
ms.lasthandoff: 08/13/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Analizės įtraukimas į darbo sritis naudojant „Power BI Embedded“

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šią funkcija palaiko 7.2 arba vėlesnės versijos „Dynamics 365 for Finance and Operations“.

## <a name="introduction"></a>Įvadas
Šioje temoje rodoma, kaip įterpti „Microsoft Power BI“ ataskaitą darbo srities skirtuke **Analizė**. Čia pateiktame pavyzdyje išplėsime Transporto parko valdymo programos darbo sritį **Rezervacijų valdymas**, kad skirtuke **Analizė** galėtume įterpti analizės darbo sritį.

## <a name="prerequisites"></a>Būtinieji komponentai
+ Prieiga prie projektuotojo terpės, kurioje veikia 8-asis ar naujesnis platformos atnaujinimas.
+ Naudojant „Microsoft Power BI Dekstop“ programą sukurta analizės ataskaita (.pbix failas), kurioje yra iš objekto parduotuvės duomenų bazės gaunamas duomenų modelis.

## <a name="overview"></a>Apžvalga
Nesvarbu, ar išplečiate esamą, ar sukuriate naują asmeninę programos darbo sritį, informatyviems ir interaktyviems verslo duomenų rodiniams pristatyti galite naudoti įdėtuosius analizės rodinius. Analizės darbo srities įtraukimo procesą sudaro keturi veiksmai.

1. Įtraukite .pbix failą kaip „Dynamics 365“ išteklių.
2. Apibrėžkite analizės darbo srities skirtuką.
3. Įterpkite .pbix išteklių darbo srities skirtuke.
4. Pasirinktina: įtraukite plėtinius, kad tinkintumėte rodinį.

> [!NOTE]
> Daugiau informacijos apie tai, kaip kurti analizės ataskaitas, ieškokite [Darbo su „Power BI Dekstop“ pradžia](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/). Šis puslapis – puikus įžvalgų, galinčių padėti kurti patrauklius sprendimus analizės ataskaitoms, šaltinis.

## <a name="add-a-pbix-file-as-a-resource"></a>Įtraukite .pbix failą kaip išteklių.
Prieš pradėdami, turite sukurti arba gauti „Power BI“ ataskaitą, kurią įdėsite į darbo sritį. Daugiau informacijos apie tai, kaip kurti analizės ataskaitas, ieškokite [Darbo su „Power BI Dekstop“ pradžia](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).

Atlikite šiuos veiksmus, norėdami įtraukti .pbix failą kaip „Visual Studio“ projekto artefaktą.

1. Naujo projekto atitinkamame modelyje kūrimas.
2. Sprendimų naršyklėje pasirinkite projektą, spustelėkite dešiniuoju klavišu ir pasirinkite **Įtraukti** \> **Nauja prekė**.
3. Dialogo lange **Naujo elemento įtraukimas**, esančio parinktyje **Operacijų artefaktai**, pasirinkite šabloną **Išteklius**.
4. Įveskite pavadinimą, kuris bus naudojamas nurodant ataskaitą X++ metaduomenyse, tada spustelėkite **Įtraukti**.

    ![Naujos prekės dialogo lango įtraukimas](media/analytical-workspace-add.png)

5. Raskite .pbix failą, kuriame yra analizės ataskaitos apibrėžimas, tada spustelėkite **Atidaryti**.

    ![Pasirinkite ištekliaus failo dialogo langą](media/analytical-workspace-select-resource.png)

Įtraukę .pbix failą kaip „Dynamics 365“ išteklių, ataskaitas galite įdėti į darbo sritis ir, naudodami meniu elementus, įtraukti tiesioginių saitų.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Skirtuko valdiklio įtraukimas į programos darbo sritį
Šiame pavyzdyje išplėsime Transporto parko valdymo modelio darbo sritį **Rezervacijų valdymas** į formos **FMClerkWorkspace** apibrėžimą įtraukdami skirtuką **Analizė**.

Toliau pavaizduota, kaip forma **FMClerkWorkspace** atrodo „Microsoft Visual Studio“ dizaineryje.

![Forma FMClerkWorkspace prieš pakeitimus](media/analytical-workspace-definition-before.png)

Atlikite šiuos veiksmus, norėdami išplėsti darbo srities **Rezervacijų valdymas** formos apibrėžimą.

1. Norėdami išplėsti dizaino apibrėžimą, atidarykite formų dizainerį.
2. Dizaino apraše pasirinkite viršutinį elementą, pažymėtą **Dizainas | Šablonas: darbo srities veikimas**.
3. Norėdami įtraukti naują valdiklį pavadinimu **FormTabControl1**, spustelėkite dešiniuoju mygtuku ir pasirinkite **Naujas** \> **Skirtukas**.
4. Formų dizaineryje pasirinkite **FormTabControl1**.
5. Spustelėkite dešiniuoju mygtuku ir pasirinkite **Naujo skirtuko puslapis**, kad įtrauktumėte naujo skirtuko puslapį.
6. Pervadinkite skirtuko puslapį suteikdami prasmingesnį pavadinimą, pvz, **Darbo sritis**.
7. Formų dizaineryje pasirinkite **FormTabControl1**.
8. Spustelėkite dešiniuoju mygtuku ir pasirinkite **Naujo skirtuko puslapis**.
9. Pervadinkite skirtuko puslapį suteikdami prasmingesnį pavadinimą, pvz, **Analizė**.
10. Formų dizaineryje pasirinkite **Analizė (skirtuko puslapis)**.
11. Ypatybę **Antraštė** nustatykite į **Analizė**.
12. Dešiniuoju pelės mygtuku spustelėkite valdiklį, tada pasirinkite **Naujas** \> **Grupė** ir įtraukite naują formos grupės valdiklį.
13. Pervadinkite formos grupę suteikdami prasmingesnį pavadinimą, pvz, **powerBIReportGroup**.
14. Formų dizaineryje pasirinkite **PanoramaBody (skirtukas)**, tada vilkite valdiklį į skirtuką **Darbo sritis**.
15. Dizaino apraše pasirinkite viršutinį elementą, pažymėtą **Dizainas | Šablonas: darbo srities veikimas**.
16. Spustelėkite dešiniuoju mygtuku ir pasirinkite **Pašalinti šabloną**.
17. Dešiniuoju pelės mygtuku spustelėkite dar kartą, tada pasirinkite **Pridėti šabloną** \> **Darbo sritis su skirtukais**.
18. Pradėkite kurti, kad patvirtintumėte pakeitimus.

Toliau pavaizduota, kaip atrodo dizainas pritaikius šiuos pakeitimus.

![FMClerkWorkspace po pakeitimų](media/analytical-workspace-definition-after.png)

Pridėję formų valdiklių, kurie bus naudojami darbo srities ataskaitai įdėti, turite apibrėžti, kokio dydžio turi būti pagrindinis valdiklis, kad tilptų į maketą. Pagal numatytuosius nustatymus puslapiai **Filtrų sritis** ir **Skirtukas** bus rodomi ataskaitoje. Tačiau šių valdiklių matomumą galite keisti atitinkamai pagal tikslinį ataskaitos vartotoją.

> [!NOTE]
> Norint išlaikyti nuoseklumą, įdėtoms darbo sritims rekomenduojame naudoti plėtinius, kurie paslėptų puslapius **Filtrų sritis** ir **Skirtukas**.

Užbaigėte prašymo formos apibrėžimo išplėtimo užduotį. Daugiau informacijos apie tai, kaip naudoti plėtinius tinkinimams atlikti, ieškokite [Tinkinimas: perdengimas ir plėtiniai](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>X ++ verslo logikos įtraukimas norint įdėti peržiūros programos valdiklį
Atlikite šiuos veiksmus, norėdami įtraukti verslo logiką, inicijuojančią į darbo sritį **Rezervacijų valdymas** įdėtą peržiūros programos valdiklį.

1. Norėdami išplėsti dizaino apibrėžimą, atidarykite **FMClerkWorkspace** formų dizainerį.
2. Paspauskite F7, kad pasiektumėte kodo aprašo kodą.
3. Įtraukite toliau nurodytą X++ kodą.

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Pradėkite kurti, kad patvirtintumėte pakeitimus.

Užbaigėte verslo logikos įtraukimo užduotį, skirtą įdėtam ataskaitų peržiūros programos valdikliui inicijuoti. Toliau pavaizduota, kaip atrodo darbo sritis pritaikius šiuos pakeitimus.

![Į darbo sritį įdėta ataskaita](media/analytical-workspace-final.png)

> [!NOTE]
> Esamą operacijų rodinį galite pasiekti naudodami virš puslapio pavadinimo esančius darbo srities skirtukus.

## <a name="reference"></a>Nuoroda

### <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl metodas
Šiame skyriuje pateikiama informacija apie pagelbiklio klasę, naudojamą „Power BI“ ataskaitai (.pbix išteklius) į formos grupės valdiklį įdėti.

#### <a name="syntax"></a>Sintaksė
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parametrai

| Vardas             | aprašymas                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | .pbix ištekliaus pavadinimas.                                                                              |
| formGroupControl | Formos grupės valdiklis, kuriam bus taikomas „Power BI“ ataskaitos valdiklis.                                              |
| defaultPageName  | Numatytasis puslapio pavadinimas.                                                                                       |
| showFilterPane   | Būlio logikos vertė, kuria nurodoma, ar filtro sritis turi būti rodoma (**true**), ar paslėpta (**klaidinga**).     |
| showNavPane      | Būlio logikos vertė, kuria nurodoma, ar naršymo sritis turi būti rodoma (**true**), ar paslėpta (**klaidinga**). |
| defaultFilters   | Numatytieji „Power BI“ ataskaitos filtrai.                                                                 |

