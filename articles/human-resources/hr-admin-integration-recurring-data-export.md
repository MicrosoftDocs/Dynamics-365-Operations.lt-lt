---
title: Pasikartojančių duomenų eksportavimo programos kūrimas
description: Šiame straipsnyje nurodoma, kaip sukurti „Microsoft Azure“ loginę programą, kuria eksportuojami duomenys iš „Microsoft Dynamics 365 Human Resources“ pasikartojančiu grafiku.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bc9b5c97f855f1d8eb44765c98473b69f96adec
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466982"
---
# <a name="create-a-recurring-data-export-app"></a>Pasikartojančių duomenų eksportavimo programos kūrimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje nurodoma, kaip sukurti „Microsoft Azure“ loginę programą, kuria eksportuojami duomenys iš „Microsoft Dynamics 365 Human Resources“ pasikartojančiu grafiku. Mokymo priemonėms naudojama „Human Resources“ programos DMF paketo REST taikomojo programavimo sąsaja (API) eksportuoti duomenis. Kai duomenys eksportuoti, loginė programa išsaugo eksportuotų duomenų paketą „Microsoft OneDrive“ verslui aplanke.

## <a name="business-scenario"></a>Verslo scenarijus

Viename įprastame verslo scenarijuje, skirtame „Microsoft Dynamics 365“ integravimams, duomenys turi būti eksportuojami į pasikatojančio grafiko atsiuntimo srauto sistemas. Šios mokymo priemonės nurodo, kaip eksportuoti visus darbuotojo įrašus iš „Microsoft Dynamics 365 Human Resources“ ir įrašyti darbuotojų sąrašą „OneDrive“ verslui aplanke.

> [!TIP]
> Konkretūs duomenys, kurie eksportuojami šiose mokymo priemonėse ir eksportuotų duomenų paskirties vieta, yra tik pavyzdžiai. Galite lengvai juos pakeisti, kad patenkintumėte savo verslo poreikius.

## <a name="technologies-used"></a>Naudojamos technologijos

Šiose mokymo priemonėse naudojamos šios technologijos:

- **[„Dynamics 365 Human Resources“](https://dynamics.microsoft.com/talent/overview/)**– bendrųjų duomenų šaltinis, skirtas darbuotojams, kurie bus eksportuojami.
- **[„Azure Logic Apps“](https://azure.microsoft.com/services/logic-apps/)** – technologija, kuria galima organizuoti ir planuoti pasikartojantį eksportavimą.

    - **[Jungtys](https://docs.microsoft.com/azure/connectors/apis-list)** – technologija, naudojama prijungti loginę programą prie reikiamų galinių punktų.

        - [HTTP naudojant „Azure AD“](https://docs.microsoft.com/connectors/webcontents/) jungtį
        - [„OneDrive“ verslui](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) jungtis

- **[DMF paketo REST API](../dev-itpro/data-entities/data-management-api.md)** – technologija, naudojama paleisti eksportavimą ir stebėti jo eigą.
- **[„OneDrive“ verslui](https://onedrive.live.com/about/business/)** – eksportuojamų darbuotojų paskirties vieta.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami pratimą, nurodytą šiose mokymo priemonėse, turite turėti šiuos elementus:

- „Human Resources“ aplinką, turinčią administravimo lygio teises aplinkoje
- [„Azure“ prenumeratą](https://azure.microsoft.com/free/) laikyti loginę programą

## <a name="the-exercise"></a>Pratimas

Šio pratimo pabaigoje turėsite loginę programą, kuri bus prijungta prie jūsų „Human Resources“ ir „OneDrive“ verslui paskyros. Loginė programa eksportuos duomenų paketą iš „Human Resources“, palaukite, kol bus baigta eksportuoti, atsisiųskite eksportuotų duomenų paketą ir įrašysite duomenų paketą į savo „OneDrive“ verslui nurodytą aplanką.

Baigta loginė programa bus panaši į šią iliustraciją.

![Loginės programos apžvalga](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>1 veiksmas: sukurti duomenų eksportavimo projektą programoje „Human Resources“

Programoje „Human Resources“ sukurkite duomenų eksportavimo projektą, kuriuo eksportuojami darbininkai. Pavadinkite projektą **Eksportuoti darbininkus** ir įsitikinkite, kad parinktis **Generuoti duomenų paketus** yra nustatyta kaip **Taip**. Įtraukite į projektą vieną objektą (**Darbininkas**) ir pasirinkite formatą, kuriuo norite eksportuoti. (Šiose mokymo priemonėse naudojamas „Microsoft Excel“ formatas.)

![Darbininkų duomenų projekto eksportavimas](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Įsiminkite duomenų eksportavimo projekto pavadinimą. Jums jo reikės, kai kitame veiksme kursite loginę programą.

### <a name="step-2-create-the-logic-app"></a>2 veiksmas: sukurti loginę programą

Didžioji dalis pratimo susijusi su loginės programos kūrimu.

1. „Azure“ portale sukurkite loginę programą.

    ![Loginės programos kūrimo puslapis](media/integration-logic-app-creation-1.png)

2. Įrankyje „Logic Apps Designer“ pradėkite nuo tuščios loginės programos.
3. Įtraukite [pasikartojančio grafiko paleidiklį](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence), kad galėtumėte paleisti loginę programą kas 24 valandas (arba pagal pasirinktą grafiką).

    ![Pasikartojimo dialogo langas](media/integration-logic-app-recurrence-step.png)

4. Iškvieskite [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API ir suplanuokite savo duomenų paketo eksportavimą.

    1. Naudokite veiksmą **Iškviesti HTTP užklausą** iš HTTP su „Azure AD“ jungtimi.

        - **Pagrindinis išteklių URL:** jūsų „Human Resources“ aplinkos URL (neįtraukite maršruto / vardų srities informacijos.)
        - **„Azure AD“ ištelių URI:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > „Human Resources“ tarnyboje dar nepateikiama jungtis, kuriuo būtų išstatomos visos API, kurios sudaro DMF paketų REST API, pvz., **ExportToPackage**. Užuot turite iškviesti API naudodami neapdorotas HTTPS užklausas per HTTP su „Azure AD“ jungtimi. Ši jungtis naudoja „Azure Active Directory“ („Azure AD“) autentifikavimui ir įgaliojimui į „Human Resources“.

        ![HTTP naudojant „Azure AD“ jungtį](media/integration-logic-app-http-aad-connector-step.png)

    2. Prisijunkite prie savo „Human Resources“ aplinkos per HTTP su „Azure AD“ jungtimi.
    3. Nustatykite HTTP **SKELBTI** užklausą, kad būtų iškviesta **ExportToPackage** DMF REST API.

        - **Metodas:** SKELBTI
        - **Prašymo Url:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Užklausos tekstas:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![HTTP užklausos veiksmo iškvietimas](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Galbūt norėsite pervardyti kiekvieną veiksmą taip, kad jis būtų prasmingesnis nei numatytasis pavadinimas, **iškviesti HTTP užklausą**. Pavyzdžiui, galite pervardyti šį veiksmą kaip **ExportToPackage**.

5. [Inicijuokite kintamąjį](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable), skirtą užklausos **ExportToPackage** vykdymo būsenai saugoti.

    ![Kintamojo veiksmo inicijavimas](media/integration-logic-app-initialize-variable-step.png)

6. Palaukite, kol duomenų eksportavimo vykdymo būsena taps **Pavyko**.

    1. Pridėkite [ciklą Iki](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), kuris kartojamas, kol kintamojo **ExecutionStatus** reikšmė tampa **Pavyko**.
    2. Pridėkite veiksmą **Delsa**, kuris laukia penkes sekundes prieš tikrindamas dabartinę eksportavimo vykdymo būseną.

        ![Iki ciklo konteinerio](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Nustatykite ribinį skaičių į **15**, kad lauktumėte, kol eksportavimas pasibaigs ne daugiau nei 75 sekundes (15 iteracijų × 5 sek.). Jei eksportavimas užtrunka ilgiau, atitinkamai pakoreguokite ribinį skaičių.        

    3. Įtraukite veiksmą **Iškviesti HTTP užklausą**, kad iškvietumėte [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API ir nustatykite kintamąjį **ExecutionStatus** į **GetExecutionSummaryStatuss** atsako rezultatą.

        > Šis pavyzdys neatlieka klaidų tikrinimo. **GetExecutionSummaryStatus** API gali grąžinti nepavykusias terminalo būsenas (t. y., kitas nei **Pavyko** būsenas). Daugiau informacijos ieškokite [API dokumentacijoje](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Metodas:** SKELBTI
        - **Prašymo Url:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Užklausos turinys** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Jums gali tekti įvesti vertę **Užklausos turinys** kūrimo įrankyje arba kodo rodinyje, arba funkcijos rengyklėje.

        ![HTTP užklausos 2 veiksmo iškvietimas](media/integration-logic-app-get-execution-status-step.png)

        ![Kintamojo veiksmo nustatymas](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Reikšmė **Nustatyti kintamąjį**, priklausanti veiksmui (**body('Invoke\_an\_HTTP\_request\_2')?['value']**), skiriasi nuo reikšmės, skirtos turinio reikšmei **Iškviesti HTTP užklausą 2**, net jei kųrimo įrankyje tuo pačiu būdu bus rodomos vertės.

7. Gaukite eksportuoto paketo atsisiuntimo URL.

    - Įtraukite veiksmą **Iškviesti HTTP užklausą**, kad iškviestumėte [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.

        - **Metodas:** SKELBTI
        - **Prašymo Url:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Užklausos turinys:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL veiksmas](media/integration-logic-app-get-exported-package-step.png)

8. Atsisiųskite eksportuotą paketą.

    - Pridėkite HTTP užklausą **GAUTI** (įtaisytasis [HTTP jungties veiksmas](https://docs.microsoft.com/azure/connectors/connectors-native-http)), kad atsisiųstumėte paketą iš ankstesniame veiksme grąžinto URL.

        - **Metodas:** GAUTI
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Jums gali tekti įvesti užklausos **URI** vertę kūrimo įrankyje arba kodo rodinyje, arba funkcijos rengyklėje.

        ![HTTP GAUTI veiksmas](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Šiai užklausai nereikia jokio papildomo autentifikavimo, nes URL, kurio **GetExportedPackageUrl** API grįžtys apima bendrai naudojamą prieigos parašų atpažinimo ženklą, kuris suteikia prieigą prie failo atsisiuntimo.

9. Įrašykite atsisiųstą paketą naudodami jungtį [„OneDrive“ verslui](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).

    - Įtraukite „OneDrive“ verslui veiksmą [Sukurti failą](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).
    - Jei reikia, prisijunkite prie savo „OneDrive“ verslui paskyros.

        - **Aplanko kelias:** pasirinktas aplankas
        - **Failo pavadinimas:** darbininko\_paketas.zip
        - **Failo turinys:** ankstesnio veiksmo tekstas (dinaminis turinys)

        ![Failo veiksmo kūrimas](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>3 veiksmas: tikrinti loginę programą

Norėdami tikrinti loginę programą, pasirinkite kūrimo įrankyje mygtuką **Vykdyti**. Matysite, kad pradedami vykdyti loginės programos veiksmai. Po 30–40 sekundžių, loginė programa turėtų būti baigta vykdyti, o jūsų „OneDrive“ verslui aplanke turėtų būti naujas paketo failas, kuriame yra eksportuoti darbuotojai.

Jei pranešama apie bet kurio veiksmo triktį, kūrimo įrankyje pasirinkite nepavykusį veiksmą ir patikrinkite dėl jos laukus **Įvestys** ir **Išvestys**. Derinkite ir koreguokite veiksmą taip, kaip reikia, kad ištaisytumėte klaidas.

Toliau pateiktoje iliustracijoje parodyta, kaip atrodo įrankis „Logic Apps Designer“, kai visi loginės programos veiksmai sėkmingai vykdomi.

![Sėkmingas loginės programos vykdymas](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Suvestinė

Šiose mokymo priemonės jūs sužinojote, kaip naudoti loginę programą eksportuoti duomenis iš „Human Resources“ ir įrašyti eksportuotus duomenis į „OneDrive“ verslo aplanką. Galite modifikuoti šių mokymo priemonių veiksmus, reikalingus patenkinti jūsų verslo poreikius.




[!INCLUDE[footer-include](../includes/footer-banner.md)]