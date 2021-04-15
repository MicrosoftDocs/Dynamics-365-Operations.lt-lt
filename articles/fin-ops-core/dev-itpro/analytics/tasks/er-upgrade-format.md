---
title: 'ER: formato atnaujinimas pritaikant naują pagrindinę to formato versiją'
description: Šioje temoje aprašoma, kaip išlaikyti elektroninių ataskaitų (ER) formato konfigūraciją.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05f8562bcab50a303b58174d177c6058f9417294
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744944"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="9cc4d-103">ER: formato atnaujinimas pritaikant naują pagrindinę to formato versiją</span><span class="sxs-lookup"><span data-stu-id="9cc4d-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cc4d-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali prižiūrėti elektroninių ataskaitų (ER) formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="9cc4d-105">Šia procedūra paaiškinama, kaip pasirinktinę formato versiją galima sukurti pagal iš konfigūracijų teikėjo (KT) gautą formatą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="9cc4d-106">Ja taip pat paaiškinama, kaip pritaikyti naują, pagrindinę to formato versiją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="9cc4d-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūrų „Konfigūracijų teikėjo sukūrimas ir jo pažymėjimas kaip aktyvaus‟ ir „Sukurto formato naudojimas generuoti elektroniniams mokėjimų dokumentams‟ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="9cc4d-108">Šiuos veiksmus galima atlikti GBSI įmonėje.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="9cc4d-109">Formato konfigūracijos pasirinkimas tinkinti</span><span class="sxs-lookup"><span data-stu-id="9cc4d-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="9cc4d-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="9cc4d-111">Šiame pavyzdyje pavyzdinė įmonė „Litware, Inc.“ (https://www.litware.com) veiks kaip konfigūracijų teikėjas, kuris palaiko konkrečios šalies elektroninių mokėjimų formato konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="9cc4d-112">Pavyzdinė įmonė „Proseware, Inc.‟ (http://www.proseware.com) veiks kaip formato konfigūracija, kurią pateikė „Litware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="9cc4d-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="9cc4d-113">„Proseware, Inc.“ naudoja formatus tam tikruose tos šalies regionuose.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="9cc4d-114">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9cc4d-115">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-115">Click Show filters.</span></span>
4. <span data-ttu-id="9cc4d-116">Taikykite šiuos filtrus: lauke „Pavadinimas” įveskite filtro reikšmę „BACS (JK fiktyvus)” naudodami filtro operatorių „prasideda“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="9cc4d-117">Pasirinkta BACS (JK fiktyvus) formato konfigūracija priklauso teikėjui „Litware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="9cc4d-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="9cc4d-118">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-118">Click Show filters.</span></span>
6. <span data-ttu-id="9cc4d-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9cc4d-120">Tinkinti „Proseware, Inc.‟ naudos formato versiją, kurios būsena – Baigta.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="9cc4d-121">Naujos savo pasirinktinio elektroninio dokumento formato konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="9cc4d-122">„Proseware, Inc.“ gavo 1.1 BACS (JK fiktyvus) konfigūracijos versiją, kurioje yra pradinis formatas, skirtas generuoti elektroninio mokėjimo dokumentams iš „Litware, Inc.‟ pagal jų aptarnavimo abonementą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="9cc4d-123">„Proseware, Inc.“ nori pradėti ją naudoti kaip standartą savo šalyje, tačiau, norint atitikti konkretaus regiono reikalavimus, ją reikia šiek tiek pritaikyti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="9cc4d-124">„Proseware, Inc.“ taip pat nori pasilikti galimybę atnaujinti pasirinktinį formatą, kai tik „Litware, Inc.‟ pateiks naują jo versiją (su pakeitimais, atitinkančiais naujus konkrečios šalies reikalavimus), ir ji atnaujinti nori patirdama kuo mažesnes išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="9cc4d-125">Norėdami tai padaryti, „Proseware, Inc.‟ turi sukurti konfigūraciją, kaip pagrindą naudodama „Litware, Inc.‟ BACS (JK fiktyvus) konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="9cc4d-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-126">Close the page.</span></span>
2. <span data-ttu-id="9cc4d-127">Pasirinkite „Proseware, Inc.‟ kaip aktyvų teikėją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="9cc4d-128">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-128">Click Set active.</span></span>
4. <span data-ttu-id="9cc4d-129">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9cc4d-130">Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9cc4d-131">Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="9cc4d-132">Iš „Litware, Inc.” pasirinkite BACS (JK fiktyvus) konfigūraciją. „Proseware, Inc.” kaip pasirinktinės versijos pagrindą naudos 1.1 versiją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="9cc4d-133">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="9cc4d-134">Taip galite sukurti naują pasirinktinio mokėjimo formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="9cc4d-135">Lauke Naujas įveskite „Kildinti iš pavadinimo: BACS (JK fiktyvus), „Litware, Inc.‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="9cc4d-136">Norėdami patvirtinti, kad kaip pasirinktinės versijos kūrimo pagrindas bus naudojamas BACS (JK fiktyvus), pasirinkite parinktį Kildinti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="9cc4d-137">Lauke Pavadinimas įveskite „BACS (JK fiktyvus pasirinktinis)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="9cc4d-138">Lauke „Aprašas“ įveskite „BACS tiekėjo mokėjimas (JK fiktyvus pasirinktinis)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="9cc4d-139">Čia automatiškai įvedamas aktyvus konfigūracijų teikėjas („Proseware, Inc.‟).</span><span class="sxs-lookup"><span data-stu-id="9cc4d-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="9cc4d-140">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9cc4d-141">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="9cc4d-142">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="9cc4d-143">Savo elektroninio dokumento formato tinkinimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="9cc4d-144">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-144">Click Designer.</span></span>
2. <span data-ttu-id="9cc4d-145">Spustelėkite Išplėsti / sutraukti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="9cc4d-146">Spustelėkite Išplėsti / sutraukti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="9cc4d-147">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="9cc4d-148">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="9cc4d-149">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="9cc4d-150">Lauke „Pavadinimas“, įveskite „IBAN“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="9cc4d-151">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-151">Click OK.</span></span>
9. <span data-ttu-id="9cc4d-152">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ IBAN“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="9cc4d-153">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="9cc4d-154">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="9cc4d-155">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-155">Click OK.</span></span>
13. <span data-ttu-id="9cc4d-156">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="9cc4d-157">Lauke Didžiausias ilgis įveskite „60‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="9cc4d-158">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="9cc4d-159">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="9cc4d-160">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="9cc4d-161">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="9cc4d-162">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="9cc4d-163">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita \ IBAN“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="9cc4d-164">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė = model.Payments \ Tiekėjas \ Bankas \ IBAN \ Eilutė”.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="9cc4d-165">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-165">Click Bind.</span></span>
23. <span data-ttu-id="9cc4d-166">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="9cc4d-167">Pritaikyto formato tikrinimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-167">Validate the customized format</span></span>
1. <span data-ttu-id="9cc4d-168">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-168">Click Validate.</span></span>

    <span data-ttu-id="9cc4d-169">Patikrinkite pritaikytą formato maketą ir duomenų susiejimo pakeitimus ir įsitikinkite, kad visi susiejimai veikia gerai.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="9cc4d-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="9cc4d-171">Pasirinktinės formato konfigūracijos dabartinės versijos būsenos keitimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="9cc4d-172">Pakeiskite sukurtos formato konfigūracijos būseną iš Juodraštis į Baigta, kad ją būtų galima naudoti generuojant mokėjimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="9cc4d-173">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-173">Click Change status.</span></span>

    <span data-ttu-id="9cc4d-174">Atkreipkite dėmesį, kad dabartinės pasirinktos konfigūracijos versijos būsena yra Juodraštis.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9cc4d-175">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-175">Click Complete.</span></span>
3. <span data-ttu-id="9cc4d-176">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9cc4d-177">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-177">Click OK.</span></span>
5. <span data-ttu-id="9cc4d-178">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9cc4d-179">Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1.1.1 baigta versija.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="9cc4d-180">Tai reiškia, kad tai yra 1-oji pasirinktinio BACS (JK fiktyvus pasirinktinis) formato versija, kuri paremta 1-ąja BACS (JK fiktyvus) formato versija, kuri paremta 1-ąja mokėjimų (suprastintasis modelis) duomenų modelio versija.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="9cc4d-181">Pritaikyto formato tikrinimas generuojant mokėjimo failus</span><span class="sxs-lookup"><span data-stu-id="9cc4d-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="9cc4d-182">Lygiagrečiame „Finance and Operations” seanse atlikite procedūros „Sukurto formato naudojimas generuoti elektroniniams mokėjimų dokumentams‟ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="9cc4d-183">Elektroninio mokėjimo būdo parametruose pasirinkite BACS (JK fiktyvus pasirinktinis) formatą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="9cc4d-184">Įsitikinkite, kad sukurtame mokėjimo faile yra neseniai įdiegtas XML mazgas, pagal regiono reikalavimus pateikiantis IBAN kodą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="9cc4d-185">Esamos konkrečios šalies konfigūracijos naujinimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="9cc4d-186">„Litware, Inc.“ turi atnaujinti BACS (JK fiktyvus) konfigūraciją ir įgyvendinti naujus šalies reikalavimus dėl elektroninio dokumento formato valdymo.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="9cc4d-187">Vėliau tai bus įtraukta į naują šios konfigūracijos versiją, kuri bus teikiama aptarnavimo abonentams, įskaitant „Proseware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="9cc4d-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="9cc4d-188">Tikrų su paslaugų teikimu susijusių procesų metu kiekvieną naują BACS (JK fiktyvus) versiją „Proseware, Inc.‟ galima importuoti iš „Litware, Inc.‟ konfigūracijų LCS saugyklos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="9cc4d-189">Atlikdami šią procedūrą tai imituosime BACS (JK fiktyvus) atnaujindami paslaugų teikėjo vardu.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="9cc4d-190">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-190">Close the page.</span></span>
2. <span data-ttu-id="9cc4d-191">Pasirinkite teikėją „Litware, inc.“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="9cc4d-192">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-192">Click Set active.</span></span>
4. <span data-ttu-id="9cc4d-193">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9cc4d-194">Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9cc4d-195">Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="9cc4d-196">Pasirenkama teikėjui „Litware, Inc.‟ priklausanti BACS (JK fiktyvus) juodraščio versija, siekiant įdiegti keitimus, atitinkančius naujus konkrečios šalies reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="9cc4d-197">Elektroninio dokumento pagrindinio formato lokalizavimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="9cc4d-198">Tarkime, kad yra naujų šalies reikalavimų, kuriuos turi palaikyti „Litware, Inc.“:</span><span class="sxs-lookup"><span data-stu-id="9cc4d-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="9cc4d-199">Kreditoriaus banko SWIFT kodo reikšmė kiekvienoje mokėjimo operacijoje.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="9cc4d-200">Tiekėjo pavadinimo teksto generuojamame faile yra 100 simbolių ilgio riba.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="9cc4d-201">Nauji konkrečių šalių reikalavimai</span><span class="sxs-lookup"><span data-stu-id="9cc4d-201">New country-specific requirements</span></span>  
- <span data-ttu-id="9cc4d-202">Pasirinkite norimos konfigūracijos juodraščio versiją, kad įdiegtumėte reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="9cc4d-203">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-203">Click Designer.</span></span>
2. <span data-ttu-id="9cc4d-204">Spustelėkite Išplėsti / sutraukti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="9cc4d-205">Spustelėkite Išplėsti / sutraukti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="9cc4d-206">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="9cc4d-207">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="9cc4d-208">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="9cc4d-209">Lauke „Pavadinimas“ įveskite „SWIFT“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="9cc4d-210">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-210">Click OK.</span></span>
9. <span data-ttu-id="9cc4d-211">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ SWIFT“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="9cc4d-212">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="9cc4d-213">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="9cc4d-214">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-214">Click OK.</span></span>
13. <span data-ttu-id="9cc4d-215">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="9cc4d-216">Lauke Didžiausias ilgis įveskite „100‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="9cc4d-217">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="9cc4d-218">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="9cc4d-219">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="9cc4d-220">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="9cc4d-221">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Agentas‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="9cc4d-222">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Agentas \ SWIFT“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="9cc4d-223">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė = model.Payments \ Tiekėjas \ Bankas \ SWIFT \ Eilutė”.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="9cc4d-224">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-224">Click Bind.</span></span>
23. <span data-ttu-id="9cc4d-225">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="9cc4d-226">Lokalizuoto formato tikrinimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-226">Validate the localized format</span></span>
1. <span data-ttu-id="9cc4d-227">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-227">Click Validate.</span></span>
2. <span data-ttu-id="9cc4d-228">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="9cc4d-229">Pagrindinės formato konfigūracijos dabartinės versijos būsenos keitimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="9cc4d-230">Atnaujintos pagrindinės formato konfigūracijos būseną iš Juodraštis pakeiskite į Baigta, kad ją būtų galima naudoti generuojant mokėjimo dokumentus ir atnaujinant iš jos gautas formato konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="9cc4d-231">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-231">Click Change status.</span></span>

    <span data-ttu-id="9cc4d-232">Atkreipkite dėmesį, kad dabartinės pasirinktos konfigūracijos versijos būsena yra Juodraštis.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9cc4d-233">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-233">Click Complete.</span></span>
3. <span data-ttu-id="9cc4d-234">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9cc4d-235">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-235">Click OK.</span></span>
5. <span data-ttu-id="9cc4d-236">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="9cc4d-237">Pasirinktinės formato konfigūracijos pagrindinės versijos keitimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="9cc4d-238">„Proseware, Inc.“ informuota, kad yra nauja 1.2 BACS (JK fiktyvus) konfigūracija, kurią galima naudoti generuojant elektroninio mokėjimo dokumentus pagal neseniai paskelbtus konkrečių šalių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="9cc4d-239">„Proseware, Inc.“ nori pradėti ją naudoti kaip tos šalies standartą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="9cc4d-240">Norėdami tai padaryti, „Proseware, Inc.‟ turi pakeisti pagrindinę pasirinktinės BACS (JK fiktyvus pasirinktinis) konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="9cc4d-241">Vietoj 1.1 BACS (JK fiktyvus) versijos naudoti naują 1.2 versiją.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="9cc4d-242">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9cc4d-243">Pasirinkite teikėją „Proseware, Inc.” ir pažymėkite jį kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="9cc4d-244">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-244">Click Set active.</span></span>
4. <span data-ttu-id="9cc4d-245">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="9cc4d-246">Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="9cc4d-247">Medyje išskleiskite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="9cc4d-248">Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus) \ BACS (JK fiktyvus pasirinktinis)“.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="9cc4d-249">Pasirinkite BACS (JK fiktyvus pasirinktinis) konfigūraciją, kuri priklauso įmonei „Proseware, Inc.‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="9cc4d-250">Naudokite pasirinktos konfigūracijos juodraščio versiją, kad įdiegtumėte reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="9cc4d-251">Spustelėkite Pritaikyti kitoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-251">Click Rebase.</span></span>

    <span data-ttu-id="9cc4d-252">Pasirinkite naująją 1.2 pagrindinės konfigūracijos versiją, kuri bus taikoma kaip naujas konfigūracijos naujinimo pagrindas.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="9cc4d-253">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-253">Click OK.</span></span>

    <span data-ttu-id="9cc4d-254">Atkreipkite dėmesį, kad, suliejant pasirinktinę versiją ir naują pagrindinę versiją, rasta konfliktų, susijusių su tam tikrais formato pakeitimais, kurių automatiškai sulieti negalima.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="9cc4d-255">Pritaikymo kitoje vietoje konfliktų sprendimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="9cc4d-256">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-256">Click Designer.</span></span>
    
    <span data-ttu-id="9cc4d-257">Atkreipkite dėmesį, kad nepavyko automatiškai išspręsti tiekėjo pavadinimo teksto ilgio limito.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="9cc4d-258">Todėl tai pateikiama konfliktų sąraše.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="9cc4d-259">Su kiekvienu tipo Naujinimas konfliktu galima naudoti tolesnes parinktis. – Taikyti ankstesnę pagrindinę reikšmę (mygtukas tinklelio viršuje), kad būtų pasirinkta ankstesnė pagrindinės versijos reikšmė (mūsų atveju – 0).</span><span class="sxs-lookup"><span data-stu-id="9cc4d-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="9cc4d-260">- Taikyti pagrindinę reikšmę (mygtukas tinklelio viršuje), kad būtų pasirinkta nauja pagrindinės versijos reikšmė (mūsų atveju – 100).</span><span class="sxs-lookup"><span data-stu-id="9cc4d-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="9cc4d-261">- pasilikti savo (pasirinktinę) reikšmę (mūsų atveju – 60).</span><span class="sxs-lookup"><span data-stu-id="9cc4d-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="9cc4d-262">Spustelėkite Taikyti pagrindinę reikšmę, kad pritaikytumėte konkrečių šalių 100 simbolių limitą tiekėjo pavadinimo teksto ilgiui.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="9cc4d-263">Atkreipkite dėmesį, kad „Proseware, Inc.‟ ir „Litware, Inc.‟ turi pasirinktinių ir vietinių šio formato versijų, naudojančių IBAN ir SWIFT kodus su susijusiais komponentais, kurie automatiškai suliejami valdomame formate.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="9cc4d-264">Spustelėkite Taikyti pagrindinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-264">Click Apply base value.</span></span>

    <span data-ttu-id="9cc4d-265">Spustelėkite Taikyti pagrindinę reikšmę, kad pritaikytumėte konkrečių šalių 100 simbolių limitą tiekėjų pavadinimams.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="9cc4d-266">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-266">Click Save.</span></span>

    <span data-ttu-id="9cc4d-267">Įrašius formatą iš konfliktų sąrašo bus pašalinti išspręsti konfliktai.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="9cc4d-268">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="9cc4d-269">Pasirinktinės formato konfigūracijos naujos versijos būsenos keitimas</span><span class="sxs-lookup"><span data-stu-id="9cc4d-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="9cc4d-270">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-270">Click Change status.</span></span>

    <span data-ttu-id="9cc4d-271">Atnaujintos, pasirinktinės formato konfigūracijos būseną pakeiskite iš Juodraštis į Baigta.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="9cc4d-272">Taip formato konfigūraciją bus galima naudoti generuojant mokėjimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="9cc4d-273">Atkreipkite dėmesį, kad dabartinės pasirinktos konfigūracijos versijos būsena yra Juodraštis.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="9cc4d-274">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-274">Click Complete.</span></span>
3. <span data-ttu-id="9cc4d-275">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9cc4d-276">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-276">Click OK.</span></span>

    <span data-ttu-id="9cc4d-277">Atkreipkite dėmesį, kad sukurtoji konfigūracija įrašoma kaip baigta 1.2.2 versija: 2-oji pagrindinio BACS (JK fiktyvus pasirinktinis) formato versija, paremta 2-ąja pagrindinio BACS (JK fiktyvus) formato versija, kuri paremta 1-ąja mokėjimų (suprastintasis modelis) duomenų modelio versija.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="9cc4d-278">Pritaikyto formato tikrinimas generuojant mokėjimo failus</span><span class="sxs-lookup"><span data-stu-id="9cc4d-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="9cc4d-279">Lygiagrečiame „Finance and Operations” seanse atlikite procedūros „Sukurto formato naudojimas generuoti elektroniniams mokėjimų dokumentams‟ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="9cc4d-280">Elektroninio mokėjimo būdo parametruose pasirinkite sukurtąjį formatą „BACS (JK fiktyvus pasirinktinis)‟.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="9cc4d-281">Įsitikinkite, kad sukurtame mokėjimo faile yra neseniai „Proseware, Inc.“ įdiegtas XML mazgas, pagal regiono reikalavimus pateikiantis IBAN sąskaitos kodą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="9cc4d-282">Faile taip pat turėtų būti neseniai įmonės „Litware, Inc.‟ įdiegtas XML mazgas, pagal šalies reikalavimus pateikiantis SWIFT banko kodą.</span><span class="sxs-lookup"><span data-stu-id="9cc4d-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]