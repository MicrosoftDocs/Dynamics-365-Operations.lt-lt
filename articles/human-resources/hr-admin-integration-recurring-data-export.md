---
title: Pasikartojančių duomenų eksportavimo programos kūrimas
description: Šiame straipsnyje nurodoma, kaip sukurti „Microsoft Azure“ loginę programą, kuria eksportuojami duomenys iš „Microsoft Dynamics 365 Human Resources“ pasikartojančiu grafiku.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b117f408b8ac8baabf7e8af3b383526f404441a4
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889865"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="1bd75-103">Pasikartojančių duomenų eksportavimo programos kūrimas</span><span class="sxs-lookup"><span data-stu-id="1bd75-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1bd75-104">Šiame straipsnyje nurodoma, kaip sukurti „Microsoft Azure“ loginę programą, kuria eksportuojami duomenys iš „Microsoft Dynamics 365 Human Resources“ pasikartojančiu grafiku.</span><span class="sxs-lookup"><span data-stu-id="1bd75-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="1bd75-105">Mokymo priemonėms naudojama „Human Resources“ programos DMF paketo REST taikomojo programavimo sąsaja (API) eksportuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="1bd75-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="1bd75-106">Kai duomenys eksportuoti, loginė programa išsaugo eksportuotų duomenų paketą „Microsoft OneDrive“ verslui aplanke.</span><span class="sxs-lookup"><span data-stu-id="1bd75-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="1bd75-107">Verslo scenarijus</span><span class="sxs-lookup"><span data-stu-id="1bd75-107">Business scenario</span></span>

<span data-ttu-id="1bd75-108">Viename įprastame verslo scenarijuje, skirtame „Microsoft Dynamics 365“ integravimams, duomenys turi būti eksportuojami į pasikartojančio grafiko atsiuntimo srauto sistemas.</span><span class="sxs-lookup"><span data-stu-id="1bd75-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="1bd75-109">Šios mokymo priemonės nurodo, kaip eksportuoti visus darbuotojo įrašus iš „Microsoft Dynamics 365 Human Resources“ ir įrašyti darbuotojų sąrašą „OneDrive“ verslui aplanke.</span><span class="sxs-lookup"><span data-stu-id="1bd75-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="1bd75-110">Konkretūs duomenys, kurie eksportuojami šiose mokymo priemonėse ir eksportuotų duomenų paskirties vieta, yra tik pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="1bd75-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="1bd75-111">Galite lengvai juos pakeisti, kad patenkintumėte savo verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="1bd75-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="1bd75-112">Naudojamos technologijos</span><span class="sxs-lookup"><span data-stu-id="1bd75-112">Technologies used</span></span>

<span data-ttu-id="1bd75-113">Šiose mokymo priemonėse naudojamos šios technologijos:</span><span class="sxs-lookup"><span data-stu-id="1bd75-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="1bd75-114">**[„Dynamics 365 Human Resources“](https://dynamics.microsoft.com/talent/overview/)**– bendrųjų duomenų šaltinis, skirtas darbuotojams, kurie bus eksportuojami.</span><span class="sxs-lookup"><span data-stu-id="1bd75-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="1bd75-115">**[„Azure Logic Apps“](https://azure.microsoft.com/services/logic-apps/)** – technologija, kuria galima organizuoti ir planuoti pasikartojantį eksportavimą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="1bd75-116">**[Jungtys](/azure/connectors/apis-list)** – technologija, naudojama prijungti loginę programą prie reikiamų galinių punktų.</span><span class="sxs-lookup"><span data-stu-id="1bd75-116">**[Connectors](/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="1bd75-117">[HTTP naudojant „Azure AD“](/connectors/webcontents/) jungtį</span><span class="sxs-lookup"><span data-stu-id="1bd75-117">[HTTP with Azure AD](/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="1bd75-118">[„OneDrive“ verslui](/azure/connectors/connectors-create-api-onedriveforbusiness) jungtis</span><span class="sxs-lookup"><span data-stu-id="1bd75-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="1bd75-119">**[DMF paketo REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – technologija, naudojama paleisti eksportavimą ir stebėti jo eigą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-119">**[DMF package REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="1bd75-120">**[„OneDrive“ verslui](https://onedrive.live.com/about/business/)** – eksportuojamų darbuotojų paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="1bd75-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1bd75-121">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1bd75-121">Prerequisites</span></span>

<span data-ttu-id="1bd75-122">Prieš pradėdami pratimą, nurodytą šiose mokymo priemonėse, turite turėti šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="1bd75-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="1bd75-123">„Human Resources“ aplinką, turinčią administravimo lygio teises aplinkoje</span><span class="sxs-lookup"><span data-stu-id="1bd75-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="1bd75-124">[„Azure“ prenumeratą](https://azure.microsoft.com/free/) laikyti loginę programą</span><span class="sxs-lookup"><span data-stu-id="1bd75-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="1bd75-125">Pratimas</span><span class="sxs-lookup"><span data-stu-id="1bd75-125">The exercise</span></span>

<span data-ttu-id="1bd75-126">Šio pratimo pabaigoje turėsite loginę programą, kuri bus prijungta prie jūsų „Human Resources“ ir „OneDrive“ verslui paskyros.</span><span class="sxs-lookup"><span data-stu-id="1bd75-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="1bd75-127">Loginė programa eksportuos duomenų paketą iš „Human Resources“, palaukite, kol bus baigta eksportuoti, atsisiųskite eksportuotų duomenų paketą ir įrašysite duomenų paketą į savo „OneDrive“ verslui nurodytą aplanką.</span><span class="sxs-lookup"><span data-stu-id="1bd75-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="1bd75-128">Baigta loginė programa bus panaši į šią iliustraciją.</span><span class="sxs-lookup"><span data-stu-id="1bd75-128">The completed logic app will resemble the following illustration.</span></span>

![Loginės programos apžvalga](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="1bd75-130">1 veiksmas: sukurti duomenų eksportavimo projektą programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="1bd75-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="1bd75-131">Programoje „Human Resources“ sukurkite duomenų eksportavimo projektą, kuriuo eksportuojami darbininkai.</span><span class="sxs-lookup"><span data-stu-id="1bd75-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="1bd75-132">Pavadinkite projektą **Eksportuoti darbininkus** ir įsitikinkite, kad parinktis **Generuoti duomenų paketus** yra nustatyta kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="1bd75-133">Įtraukite į projektą vieną objektą (**Darbininkas**) ir pasirinkite formatą, kuriuo norite eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="1bd75-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="1bd75-134">(Šiose mokymo priemonėse naudojamas „Microsoft Excel“ formatas.)</span><span class="sxs-lookup"><span data-stu-id="1bd75-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Darbininkų duomenų projekto eksportavimas](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="1bd75-136">Įsiminkite duomenų eksportavimo projekto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-136">Remember the name of the data export project.</span></span> <span data-ttu-id="1bd75-137">Jums jo reikės, kai kitame veiksme kursite loginę programą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="1bd75-138">2 veiksmas: sukurti loginę programą</span><span class="sxs-lookup"><span data-stu-id="1bd75-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="1bd75-139">Didžioji dalis pratimo susijusi su loginės programos kūrimu.</span><span class="sxs-lookup"><span data-stu-id="1bd75-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="1bd75-140">„Azure“ portale sukurkite loginę programą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-140">In the Azure portal, create a logic app.</span></span>

    ![Loginės programos kūrimo puslapis](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="1bd75-142">Įrankyje „Logic Apps Designer“ pradėkite nuo tuščios loginės programos.</span><span class="sxs-lookup"><span data-stu-id="1bd75-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="1bd75-143">Įtraukite [pasikartojančio grafiko paleidiklį](/azure/connectors/connectors-native-recurrence), kad galėtumėte paleisti loginę programą kas 24 valandas (arba pagal pasirinktą grafiką).</span><span class="sxs-lookup"><span data-stu-id="1bd75-143">Add a [Recurrence Schedule trigger](/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Pasikartojimo dialogo langas](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="1bd75-145">Iškvieskite [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API ir suplanuokite savo duomenų paketo eksportavimą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-145">Call the [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="1bd75-146">Naudokite veiksmą **Iškviesti HTTP užklausą** iš HTTP su „Azure AD“ jungtimi.</span><span class="sxs-lookup"><span data-stu-id="1bd75-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="1bd75-147">**Pagrindinis išteklių URL:** jūsų „Human Resources“ aplinkos URL (neįtraukite maršruto / vardų srities informacijos.)</span><span class="sxs-lookup"><span data-stu-id="1bd75-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="1bd75-148">**„Azure AD“ išteklių URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="1bd75-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="1bd75-149">„Human Resources“ tarnyboje dar nepateikiama jungtis, kuriuo būtų išstatomos visos API, kurios sudaro DMF paketų REST API, pvz., **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="1bd75-150">Užuot turite iškviesti API naudodami neapdorotas HTTPS užklausas per HTTP su „Azure AD“ jungtimi.</span><span class="sxs-lookup"><span data-stu-id="1bd75-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="1bd75-151">Ši jungtis naudoja „Azure Active Directory“ („Azure AD“) autentifikavimui ir įgaliojimui į „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="1bd75-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP naudojant „Azure AD“ jungtį](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="1bd75-153">Prisijunkite prie savo „Human Resources“ aplinkos per HTTP su „Azure AD“ jungtimi.</span><span class="sxs-lookup"><span data-stu-id="1bd75-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="1bd75-154">Nustatykite HTTP **SKELBTI** užklausą, kad būtų iškviesta **ExportToPackage** DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="1bd75-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="1bd75-155">**Metodas:** SKELBTI</span><span class="sxs-lookup"><span data-stu-id="1bd75-155">**Method:** POST</span></span>
        - <span data-ttu-id="1bd75-156">**Prašymo Url:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="1bd75-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="1bd75-157">**Užklausos tekstas:**</span><span class="sxs-lookup"><span data-stu-id="1bd75-157">**Body of the request:**</span></span>

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
    > <span data-ttu-id="1bd75-159">Galbūt norėsite pervardyti kiekvieną veiksmą taip, kad jis būtų prasmingesnis nei numatytasis pavadinimas, **iškviesti HTTP užklausą**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="1bd75-160">Pavyzdžiui, galite pervardyti šį veiksmą kaip **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="1bd75-161">[Inicijuokite kintamąjį](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable), skirtą užklausos **ExportToPackage** vykdymo būsenai saugoti.</span><span class="sxs-lookup"><span data-stu-id="1bd75-161">[Initialize a variable](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Kintamojo veiksmo inicijavimas](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="1bd75-163">Palaukite, kol duomenų eksportavimo vykdymo būsena taps **Pavyko**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="1bd75-164">Pridėkite [ciklą Iki](/azure/logic-apps/logic-apps-control-flow-loops#until-loop), kuris kartojamas, kol kintamojo **ExecutionStatus** reikšmė tampa **Pavyko**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-164">Add an [Until loop](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="1bd75-165">Pridėkite veiksmą **Delsa**, kuris laukia penkias sekundes prieš tikrindamas dabartinę eksportavimo vykdymo būseną.</span><span class="sxs-lookup"><span data-stu-id="1bd75-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Iki ciklo konteinerio](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="1bd75-167">Nustatykite ribinį skaičių į **15**, kad lauktumėte, kol eksportavimas pasibaigs ne daugiau nei 75 sekundes (15 iteracijų × 5 sek.).</span><span class="sxs-lookup"><span data-stu-id="1bd75-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="1bd75-168">Jei eksportavimas užtrunka ilgiau, atitinkamai pakoreguokite ribinį skaičių.</span><span class="sxs-lookup"><span data-stu-id="1bd75-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="1bd75-169">Įtraukite veiksmą **Iškviesti HTTP užklausą**, kad iškviestumėte [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API ir nustatykite kintamąjį **ExecutionStatus** į **GetExecutionSummaryStatus** atsako rezultatą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="1bd75-170">Šis pavyzdys neatlieka klaidų tikrinimo.</span><span class="sxs-lookup"><span data-stu-id="1bd75-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="1bd75-171">**GetExecutionSummaryStatus** API gali grąžinti nepavykusias terminalo būsenas (t. y., kitas nei **Pavyko** būsenas).</span><span class="sxs-lookup"><span data-stu-id="1bd75-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="1bd75-172">Daugiau informacijos ieškokite [API dokumentacijoje](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="1bd75-172">For more information, see the [API documentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="1bd75-173">**Metodas:** SKELBTI</span><span class="sxs-lookup"><span data-stu-id="1bd75-173">**Method:** POST</span></span>
        - <span data-ttu-id="1bd75-174">**Prašymo Url:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="1bd75-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="1bd75-175">**Užklausos turinys** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="1bd75-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="1bd75-176">Jums gali tekti įvesti vertę **Užklausos turinys** kūrimo įrankyje arba kodo rodinyje, arba funkcijos rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="1bd75-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP užklausos 2 veiksmo iškvietimas](media/integration-logic-app-get-execution-status-step.png)

        ![Kintamojo veiksmo nustatymas](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="1bd75-179">Reikšmė **Nustatyti kintamąjį**, priklausanti veiksmui (**body('Invoke\_an\_HTTP\_request\_2')?['value']**), skiriasi nuo reikšmės, skirtos turinio reikšmei **Iškviesti HTTP užklausą 2**, net jei kūrimo įrankyje tuo pačiu būdu bus rodomos vertės.</span><span class="sxs-lookup"><span data-stu-id="1bd75-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="1bd75-180">Gaukite eksportuoto paketo atsisiuntimo URL.</span><span class="sxs-lookup"><span data-stu-id="1bd75-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="1bd75-181">Įtraukite veiksmą **Iškviesti HTTP užklausą**, kad iškviestumėte [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="1bd75-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="1bd75-182">**Metodas:** SKELBTI</span><span class="sxs-lookup"><span data-stu-id="1bd75-182">**Method:** POST</span></span>
        - <span data-ttu-id="1bd75-183">**Prašymo Url:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="1bd75-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="1bd75-184">**Užklausos turinys:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="1bd75-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL veiksmas](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="1bd75-186">Atsisiųskite eksportuotą paketą.</span><span class="sxs-lookup"><span data-stu-id="1bd75-186">Download the exported package.</span></span>

    - <span data-ttu-id="1bd75-187">Pridėkite HTTP užklausą **GAUTI** (įtaisytasis [HTTP jungties veiksmas](/azure/connectors/connectors-native-http)), kad atsisiųstumėte paketą iš ankstesniame veiksme grąžinto URL.</span><span class="sxs-lookup"><span data-stu-id="1bd75-187">Add an HTTP **GET** request (a built-in [HTTP connector action](/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="1bd75-188">**Metodas:** GAUTI</span><span class="sxs-lookup"><span data-stu-id="1bd75-188">**Method:** GET</span></span>
        - <span data-ttu-id="1bd75-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="1bd75-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="1bd75-190">Jums gali tekti įvesti užklausos **URI** vertę kūrimo įrankyje arba kodo rodinyje, arba funkcijos rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="1bd75-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GAUTI veiksmas](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="1bd75-192">Šiai užklausai nereikia jokio papildomo autentifikavimo, nes URL, kurio **GetExportedPackageUrl** API grįžtys apima bendrai naudojamą prieigos parašų atpažinimo ženklą, kuris suteikia prieigą prie failo atsisiuntimo.</span><span class="sxs-lookup"><span data-stu-id="1bd75-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="1bd75-193">Įrašykite atsisiųstą paketą naudodami jungtį [„OneDrive“ verslui](/azure/connectors/connectors-create-api-onedriveforbusiness).</span><span class="sxs-lookup"><span data-stu-id="1bd75-193">Save the downloaded package by using the [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="1bd75-194">Įtraukite „OneDrive“ verslui veiksmą [Sukurti failą](/connectors/onedriveforbusinessconnector/#create-file).</span><span class="sxs-lookup"><span data-stu-id="1bd75-194">Add a OneDrive for Business [Create File](/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="1bd75-195">Jei reikia, prisijunkite prie savo „OneDrive“ verslui paskyros.</span><span class="sxs-lookup"><span data-stu-id="1bd75-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="1bd75-196">**Aplanko kelias:** pasirinktas aplankas</span><span class="sxs-lookup"><span data-stu-id="1bd75-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="1bd75-197">**Failo pavadinimas:** darbininko\_paketas.zip</span><span class="sxs-lookup"><span data-stu-id="1bd75-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="1bd75-198">**Failo turinys:** ankstesnio veiksmo tekstas (dinaminis turinys)</span><span class="sxs-lookup"><span data-stu-id="1bd75-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Failo veiksmo kūrimas](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="1bd75-200">3 veiksmas: tikrinti loginę programą</span><span class="sxs-lookup"><span data-stu-id="1bd75-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="1bd75-201">Norėdami tikrinti loginę programą, pasirinkite kūrimo įrankyje mygtuką **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="1bd75-202">Matysite, kad pradedami vykdyti loginės programos veiksmai.</span><span class="sxs-lookup"><span data-stu-id="1bd75-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="1bd75-203">Po 30–40 sekundžių, loginė programa turėtų būti baigta vykdyti, o jūsų „OneDrive“ verslui aplanke turėtų būti naujas paketo failas, kuriame yra eksportuoti darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="1bd75-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="1bd75-204">Jei pranešama apie bet kurio veiksmo triktį, kūrimo įrankyje pasirinkite nepavykusį veiksmą ir patikrinkite dėl jos laukus **Įvestys** ir **Išvestys**.</span><span class="sxs-lookup"><span data-stu-id="1bd75-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="1bd75-205">Derinkite ir koreguokite veiksmą taip, kaip reikia, kad ištaisytumėte klaidas.</span><span class="sxs-lookup"><span data-stu-id="1bd75-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="1bd75-206">Toliau pateiktoje iliustracijoje parodyta, kaip atrodo įrankis „Logic Apps Designer“, kai visi loginės programos veiksmai sėkmingai vykdomi.</span><span class="sxs-lookup"><span data-stu-id="1bd75-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Sėkmingas loginės programos vykdymas](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="1bd75-208">Suvestinė</span><span class="sxs-lookup"><span data-stu-id="1bd75-208">Summary</span></span>

<span data-ttu-id="1bd75-209">Šiose mokymo priemonės jūs sužinojote, kaip naudoti loginę programą eksportuoti duomenis iš „Human Resources“ ir įrašyti eksportuotus duomenis į „OneDrive“ verslo aplanką.</span><span class="sxs-lookup"><span data-stu-id="1bd75-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="1bd75-210">Galite modifikuoti šių mokymo priemonių veiksmus, reikalingus patenkinti jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="1bd75-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]