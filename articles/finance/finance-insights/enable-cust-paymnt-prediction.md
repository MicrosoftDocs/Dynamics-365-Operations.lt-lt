---
title: Kliento mokėjimo prognozių įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti ir konfigūruoti modulio Finansinės įžvalgos funkciją Kliento mokėjimo prognozės.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644998"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="a0251-103">Kliento mokėjimo prognozių įjungimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="a0251-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a0251-104">Šioje temoje paaiškinama, kaip įjungti ir konfigūruoti modulio Finansinės įžvalgos funkciją Kliento mokėjimo prognozės.</span><span class="sxs-lookup"><span data-stu-id="a0251-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="a0251-105">Galite įjungti funkciją darbo srityje **Funkcijų valdymas**, o konfigūracijos parametrus įvesti puslapyje **Modulio Finansinės įžvalgos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a0251-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="a0251-106">Šioje temoje taip pat pateikiama informacija, kuri gali padėti veiksmingai naudoti funkciją.</span><span class="sxs-lookup"><span data-stu-id="a0251-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="a0251-107">Prieš atlikdami šiuos veiksmus, būtinai atlikite būtinuosius veiksmus, aprašytus temoje [Konfigūravimas moduliui Finansinės įžvalgos](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="a0251-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="a0251-108">Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="a0251-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="a0251-109">Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą.</span><span class="sxs-lookup"><span data-stu-id="a0251-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="a0251-110">(Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="a0251-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="a0251-111">Jei jūsų „Microsoft Dynamics 365 Finance“ įdiegtis yra „Service Fabric“ įdiegtis, galite praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="a0251-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="a0251-112">Modulio Finansinės įžvalgos komanda jums jau turėjo įjungti testą.</span><span class="sxs-lookup"><span data-stu-id="a0251-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="a0251-113">Jei nematote funkcijos darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant ją įjungti, kreipkitės adresu <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="a0251-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="a0251-114">Funkcijos Kliento mokėjimo įžvalgos įjungimas</span><span class="sxs-lookup"><span data-stu-id="a0251-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="a0251-115">Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="a0251-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="a0251-116">Rasti funkciją, pavadintą **Kliento mokėjimo įžvalgos (peržiūros versija)**.</span><span class="sxs-lookup"><span data-stu-id="a0251-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="a0251-117">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="a0251-117">Select **Enable now**.</span></span>

    <span data-ttu-id="a0251-118">Funkcija Kliento mokėjimo įžvalgos dabar yra įjungta ir parengta konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="a0251-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="a0251-119">Funkcijos Kliento mokėjimo įžvalgos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a0251-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="a0251-120">Nueikite į **Kreditas ir surinkimas \> Sąranka \> Finansinės įžvalgos \> Modulio Finansinės įžvalgos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a0251-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="a0251-121">[![Puslapis Modulio Finansinės įžvalgos parametrai prieš funkciją konfigūruojant](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="a0251-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="a0251-122">Puslapio **Modulio Finansinės įžvalgos parametrai** skirtuke **Kliento mokėjimo įžvalgos** pasirinkite saitą **Peržiūrėti duomenų laukus, naudojamus prognozavimo modelyje**, kad atidarytumėte puslapį **Prognozavimo modelio duomenų laukai**.</span><span class="sxs-lookup"><span data-stu-id="a0251-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="a0251-123">Čia galite peržiūrėti numatytąjį laukų, kurie naudojami kuriant kliento mokėjimo prognozių dirbtinio intelekto (DI) prognozavimo modelį, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="a0251-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="a0251-124">Norėdami naudoti numatytąjį laukų sąrašą, kad būtų galima sukurti prognozavimo modelį, uždarykite puslapį **Prognozavimo modelio duomenų laukai**, tada puslapyje **Modulio Finansinės įžvalgos parametrai** nustatykite parinktį **Įjungti funkciją** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a0251-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="a0251-125">Nurodykite „labai pavėluotą“ operacijos laikotarpį, kad nustatytumėte, ką jūsų įmonei reiškia prognozavimo talpykla **Labai vėluoja**.</span><span class="sxs-lookup"><span data-stu-id="a0251-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="a0251-126">Kiekvienoje atidarytoje SF sistema prognozuoja mokėjimo tikimybę pagal tris talpyklas: **Laiku**, **Vėluoja** ir **Labai vėluoja**.</span><span class="sxs-lookup"><span data-stu-id="a0251-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="a0251-127">**Laiku** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti operacijos termino dieną arba anksčiau.</span><span class="sxs-lookup"><span data-stu-id="a0251-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="a0251-128">**Vėluoja** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti po operacijos termino dienos, bet prieš „labai vėluojančio“ operacijos laikotarpio pradžią.</span><span class="sxs-lookup"><span data-stu-id="a0251-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="a0251-129">**Labai vėluoja** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti prasidėjus „labai vėluojančiam“ operacijos laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="a0251-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a0251-130">Pakeitus „labai vėluojantį“ operacijos laikotarpį ir pasirinkus **Pakeisti vėlavimo ribinę reikšmę** po to, kai buvo sukurtas kliento mokėjimų DI prognozavimo modelis, esamas prognozavimo modelis panaikinamas ir sukuriamas naujas modelis.</span><span class="sxs-lookup"><span data-stu-id="a0251-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="a0251-131">Naujas prognozavimo modelis perkels operacijas į „labai vėluojantį“ laikotarpį, atsižvelgdamas į parametrus, įvestus jam nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a0251-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="a0251-132">Kai baigsite apibrėžti „labai vėluojantį“ operacijos laikotarpį, pasirinkite **Kurti prognozavimo modelį**, kad sukurtumėte prognozavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="a0251-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="a0251-133">Puslapio **Modulio Finansinės įžvalgos parametrai** skyriuje **Prognozavimo modelis** rodoma prognozavimo modelio būsena.</span><span class="sxs-lookup"><span data-stu-id="a0251-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a0251-134">Bet kuriuo metu kurdami prognozavimo modelį, galite pasirinkti **Iš naujo nustatyti modelio kūrimą**, kad procesas būtų paleistas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="a0251-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="a0251-135">Funkcija jau sukonfigūruota ir yra parengta naudoti.</span><span class="sxs-lookup"><span data-stu-id="a0251-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="a0251-136">Kai funkcija įjungta ir sukonfigūruota, o prognozavimo modelis sukurtas ir veikia, puslapio **Modulio Finansinės įžvalgos parametrai** skyriuje **Prognozavimo modelis** rodomas modelio tikslumas, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="a0251-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="a0251-137">[![Prognozavimo modelio tikslumas puslapyje Modulio Finansinės įžvalgos parametrai](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="a0251-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="a0251-138">Išleidimo informacija</span><span class="sxs-lookup"><span data-stu-id="a0251-138">Release details</span></span>

<span data-ttu-id="a0251-139">Bandomąją modulio Finansinės įžvalgos viešosios peržiūros versiją galima įdiegti Jungtinėse Amerikos Valstijose, Europoje ir Jungtinėje Karalystėje.</span><span class="sxs-lookup"><span data-stu-id="a0251-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="a0251-140">„Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų.</span><span class="sxs-lookup"><span data-stu-id="a0251-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="a0251-141">Viešosios peržiūros versijos funkcijos gali ir turi būti įjungtos tik 2 pakopos smėlio dėžės aplinkose.</span><span class="sxs-lookup"><span data-stu-id="a0251-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="a0251-142">Sąrankos ir DI modelių, sukurtų smėlio dėžės aplinkoje, negalima perkelti į gamybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="a0251-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="a0251-143">Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365“ peržiūros versijų papildomos naudojimo sąlygos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="a0251-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a0251-144">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="a0251-144">Privacy notice</span></span>

<span data-ttu-id="a0251-145">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="a0251-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>