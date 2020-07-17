---
title: Pakoreguokite ER formatą, kad sugeneruotumėte pasirinktinį elektroninį dokumentą
description: Šioje temoje paaiškinama, kaip pakoreguoti „Microsoft” pateiktą elektroninės ataskaitos (angl. „Electronic reporting“ (ER) formatą, kad jis sugeneruotų pasirinktinį elektroninį dokumentą.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67763b29744c4262249ef1ec04e7df490b31fe5b
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498107"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="9486a-103">Pakoreguokite ER formatą, kad sugeneruotumėte pasirinktinį elektroninį dokumentą</span><span class="sxs-lookup"><span data-stu-id="9486a-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9486a-104">Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų funkcinio konsultanto vaidmens vartotojas gali atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="9486a-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="9486a-105">[Elektroninių ataskaitų (ER) sistemos](general-electronic-reporting.md) konfigūracijos parametrai.</span><span class="sxs-lookup"><span data-stu-id="9486a-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="9486a-106">Importuokite „Microsoft” pateiktas ER konfigūracijas, naudojamas generuojant [tiekėjo apmokėjimo](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) failą.</span><span class="sxs-lookup"><span data-stu-id="9486a-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="9486a-107">Sukurkite standartinės „Microsoft” pateiktos ER formato konfigūracijos pasirinktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="9486a-108">Modifikuokite pasirinktinę ER formato konfigūraciją, kad ji sugeneruotų mokėjimo failus, atitinkančius atitinkamo banko reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9486a-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="9486a-109">Patvirtinkite atliktus standartinės ER formato konfigūracijos pakeitimus pasirinktinėje ER formato konfigūracijoje.</span><span class="sxs-lookup"><span data-stu-id="9486a-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="9486a-110">Visos šios procedūros gali būti atliktos **GBSI** įmonėje.</span><span class="sxs-lookup"><span data-stu-id="9486a-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="9486a-111">Kodavimas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="9486a-111">No coding is required.</span></span>

- [<span data-ttu-id="9486a-112">ER sistemos konfigūracija</span><span class="sxs-lookup"><span data-stu-id="9486a-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="9486a-113">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9486a-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="9486a-114">Aktyvuokite ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="9486a-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="9486a-115">Peržiūrėkite ER konfigūracijos teikėjų sąrašą</span><span class="sxs-lookup"><span data-stu-id="9486a-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="9486a-116">Pridėkite naują ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="9486a-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="9486a-117">Aktyvuokite ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="9486a-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="9486a-118">Importuokite standartinio ER formato konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="9486a-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="9486a-119">Importuokite standartinio ER formato konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="9486a-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="9486a-120">Peržiūrėkite importuotas ER konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="9486a-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="9486a-121">Tiekėjo mokėjimą apdorojimui paruošimas</span><span class="sxs-lookup"><span data-stu-id="9486a-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="9486a-122">Pridėkite tiekėjo paskyros banko informaciją</span><span class="sxs-lookup"><span data-stu-id="9486a-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="9486a-123">Įveskite tiekėjo mokėjimą</span><span class="sxs-lookup"><span data-stu-id="9486a-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="9486a-124">Apdorokite tiekėjo apmokėjimą naudojant standartinį ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="9486a-125">Nustatykite elektroninį mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="9486a-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="9486a-126">Apdorokite tiekėjo mokėjimą</span><span class="sxs-lookup"><span data-stu-id="9486a-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="9486a-127">Pritaikykite standartinį ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="9486a-128">Sukurkite pritaikytą formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="9486a-129">Redaguokite pritaikytą formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="9486a-130">Pažymėkite pritaikytą formatą kaip leistiną</span><span class="sxs-lookup"><span data-stu-id="9486a-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="9486a-131">Apdorokite tiekėjo apmokėjimą naudodami pritaikytą ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="9486a-132">Nustatykite elektroninį mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="9486a-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="9486a-133">Apdorokite tiekėjo mokėjimą</span><span class="sxs-lookup"><span data-stu-id="9486a-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="9486a-134">Importuokite standartinio ER formato konfigūracijų naujas versijas</span><span class="sxs-lookup"><span data-stu-id="9486a-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="9486a-135">Importuokite standartinio ER formato konfigūracijų naujas versijas</span><span class="sxs-lookup"><span data-stu-id="9486a-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="9486a-136">Peržiūrėkite importuotas ER formato konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="9486a-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="9486a-137">Patvirtinkite importuoto formato naujos versijos pakeitimus pasirinktiniame formate </span><span class="sxs-lookup"><span data-stu-id="9486a-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="9486a-138">Užbaikite pasirinktinio formato esamą juodraštinę versiją</span><span class="sxs-lookup"><span data-stu-id="9486a-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="9486a-139">Iš naujo pritaikykite pasirinktinį formatą pagal naują pagrindinę versiją</span><span class="sxs-lookup"><span data-stu-id="9486a-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="9486a-140">Apdorokite tiekėjo apmokėjimą naudodami iš naujo pritaikytą ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="9486a-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9486a-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="9486a-142">ER sistemos konfigūracija</span><span class="sxs-lookup"><span data-stu-id="9486a-142">Configure the ER framework</span></span>

<span data-ttu-id="9486a-143">Kaip elektroninių ataskaitų funkcinio konsultanto vartotojas, turite sukonfigūruoti minimalų ER parametrų rinkinį, kad galėtumėte naudoti ER sistemą standartinio ER formato pasirinktinės versijos kūrimui.</span><span class="sxs-lookup"><span data-stu-id="9486a-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="9486a-144">ER parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9486a-144">Configure ER parameters</span></span>

1. <span data-ttu-id="9486a-145">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-146">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9486a-147">**Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9486a-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="9486a-148">**Priedai** skirtuke nustatykite tolesnius parametrus:</span><span class="sxs-lookup"><span data-stu-id="9486a-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="9486a-149">**Konfigūracijos** lauke pasirinkite **Failas** tipą, skirtą **USMF** įmonei.</span><span class="sxs-lookup"><span data-stu-id="9486a-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="9486a-150"> **Užduoties archyvas**, **Laikini**, **Bazinė linija** ir **Kiti** laukuose pasirinkite **Failas** tipą.</span><span class="sxs-lookup"><span data-stu-id="9486a-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="9486a-151">Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9486a-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="9486a-152">ER konfigūracijos tiekėjo aktyvavimas</span><span class="sxs-lookup"><span data-stu-id="9486a-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="9486a-153">Kiekviena pridėta ER konfigūracija pažymėta kaip priklausanti ER konfigūracijos teikėjui.</span><span class="sxs-lookup"><span data-stu-id="9486a-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="9486a-154">ER konfigūracijos tiekėjas, kuris aktyvuojamas **Elektroninė ataskaita** darbo srityje naudojamas šiam tikslui.</span><span class="sxs-lookup"><span data-stu-id="9486a-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="9486a-155">Todėl turite aktyvuoti ER konfigūracijos tiekėją **Elektroninė ataskaita** darbo srityje prieš pridėdami ar redaguodami ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="9486a-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="9486a-156">Tik ER konfigūracijos savininkas gali redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9486a-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="9486a-157">Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="9486a-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="9486a-158">ER konfigūracijos teikėjų sąrašo peržiūra</span><span class="sxs-lookup"><span data-stu-id="9486a-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="9486a-159">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-160">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9486a-161">**Konfigūracijos teikėjo lentelė** puslapyje kiekvienas teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="9486a-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="9486a-162">Peržiūrėkite šio puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="9486a-162">Review the contents of this page.</span></span> <span data-ttu-id="9486a-163">Jei įrašas, skirtas **Litware, Inc.** ( `https://www.litware.com`) jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="9486a-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="9486a-164">Pridėkite naują ER konfigūracijos tiekėją</span><span class="sxs-lookup"><span data-stu-id="9486a-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="9486a-165">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-166">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="9486a-167">**Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="9486a-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="9486a-168">Lauke **Pavadinimas** įveskite **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="9486a-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="9486a-169">**Internetinis adresas** lauke įveskite `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="9486a-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="9486a-170">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="9486a-171">ER konfigūracijos tiekėjo aktyvavimas</span><span class="sxs-lookup"><span data-stu-id="9486a-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="9486a-172">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-173">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Litware, Inc.”** plytelę ir pasirinkite **Nustatyti kaip aktyvų**.</span><span class="sxs-lookup"><span data-stu-id="9486a-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="9486a-174">Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="9486a-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="9486a-175">Standartinio ER formato konfigūracijų importavimas</span><span class="sxs-lookup"><span data-stu-id="9486a-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="9486a-176">Standartinio ER konfigūracijų importavimas</span><span class="sxs-lookup"><span data-stu-id="9486a-176">Import the standard ER configurations</span></span>

<span data-ttu-id="9486a-177">Norėdami pridėti standartines ER konfigūracijas prie dabartinės „Microsoft Dynamics 365 Finance” programos, importuokite iš ER [saugyklos, ](general-electronic-reporting.md#Repository), sukonfigūruotos tam programos egzemplioriui.</span><span class="sxs-lookup"><span data-stu-id="9486a-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="9486a-178">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-179">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Microsoft”** plytelę ir pasirinkite **Saugyklos**, kad peržiūrėtumėte „Microsoft” tiekėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9486a-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="9486a-180">Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="9486a-181">Jei esate raginami autorizuoti, kad prisijungtumėte prie „Regulatory Configuration Service”, vadovaukitės autorizavimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="9486a-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="9486a-182">**Konfigūracijos saugykla** puslapyje kairėje konfigūracijos medyje pasirinkite **BACS (JK)** formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9486a-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="9486a-183">**Versijos** „FastTab” skirtuke pasirinkite pasirinktos ER formato konfigūracijos **1.1** versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="9486a-184">Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš Bendrosios saugyklos į dabartinę „Finance“ programą.</span><span class="sxs-lookup"><span data-stu-id="9486a-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigūracijos saugyklos puslapis](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="9486a-186">Jei kyla problemų prisijungiant prie [Bendrosios saugyklos ](er-download-configurations-global-repo.md), vietoj to galite [atsisiųsti konfigūracijas](download-electronic-reporting-configuration-lcs.md) iš „Microsoft Dynamics Lifecycle Services (LCS)”.</span><span class="sxs-lookup"><span data-stu-id="9486a-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="9486a-187">Importuotų ER konfigūracijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="9486a-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="9486a-188">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-189">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="9486a-190">**Konfigūracijos** puslapyje konfigūracijos medyje kairėje pusėje išplėskite **Mokėjimo būdas**.</span><span class="sxs-lookup"><span data-stu-id="9486a-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="9486a-191">Atkreipkite dėmesį, kad be pasirinkto **BACS (JK)** ER formato, buvo importuotos kitos būtinos ER konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9486a-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="9486a-192">Įsitikinkite, kad sekančios ER konfigūracijos yra prieinamos konfigūracijos medyje:</span><span class="sxs-lookup"><span data-stu-id="9486a-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="9486a-193">**Mokėjimo būdas** – šioje konfigūracijoje yra [duomenų modelio](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentas, rodantis mokėjimo verslo domeno duomenų struktūrą.</span><span class="sxs-lookup"><span data-stu-id="9486a-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="9486a-194">**Apmokėjimo modelio susiejimas 1611** – šioje konfigūracijoje yra [modelio susiejimo ](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentas, aprašantis, kaip duomenų modelis užpildomas programos duomenimis vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="9486a-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="9486a-195">**BACS (JK)** – šioje konfigūracijoje yra [formato](general-electronic-reporting.md#FormatComponentOutbound) ir formato susiejimo ER komponentai.</span><span class="sxs-lookup"><span data-stu-id="9486a-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="9486a-196">Formato komponentas nurodo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="9486a-196">The format component specifies the report layout.</span></span> <span data-ttu-id="9486a-197">Formato susiejimo komponente yra modelio duomenų šaltinis ir nurodo, kaip ataskaitos maketas yra užpildomas naudojant šį duomenų šaltinį vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="9486a-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Konfigūracijų puslapis](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="9486a-199">Paruoškite tiekėjo mokėjimą apdorojimui</span><span class="sxs-lookup"><span data-stu-id="9486a-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="9486a-200">Pridėkite tiekėjo paskyros banko informaciją</span><span class="sxs-lookup"><span data-stu-id="9486a-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="9486a-201">Turite pridėti tiekėjo paskyros banko informaciją, kuri bus paminėta vėliau registruotame mokėjime.</span><span class="sxs-lookup"><span data-stu-id="9486a-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="9486a-202">Eikite į **Mokėtinos sumos** \> **Tiekėjai** \> **Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="9486a-203">**Visi tiekėjai** puslapyje pasirinkite **GB_SI_000001** tiekėjo paskyrą, tada Veiksmų srityje **Tiekėjas** skirtuke **Nustatyti** grupę, pasirinkite **Banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="9486a-204">**Tiekėjo banko sąskaitos** puslapyje pasirinkite **Nauja** ir įveskite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="9486a-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="9486a-205">**Banko sąskaita**  lauke įveskite **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="9486a-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="9486a-206">**Banko grupė** lauke pasirinkite **BankoGBP**.</span><span class="sxs-lookup"><span data-stu-id="9486a-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="9486a-207">**Banko sąskaitos numeris** lauke įveskite **202015**.</span><span class="sxs-lookup"><span data-stu-id="9486a-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="9486a-208">**SWIFT kodas** lauke įveskite <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="9486a-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="9486a-209">**IBAN** lauke įveskite **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="9486a-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="9486a-210">**Banko kodas** lauke palikite numatytąją vertę, <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="9486a-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Tiekėjų bankų paskyrų puslapis](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="9486a-212">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-212">Select **Save**.</span></span>
5. <span data-ttu-id="9486a-213">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9486a-213">Close the page.</span></span>
6. <span data-ttu-id="9486a-214">**Visi tiekėjai** puslapyje atidarykite **GB_SI_000001** tiekėjo paskyrą.</span><span class="sxs-lookup"><span data-stu-id="9486a-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="9486a-215">Jei reikia, tiekėjo informacijos puslapyje pasirinkite **Redaguoti**, kad puslapis būtų redaguojamas.</span><span class="sxs-lookup"><span data-stu-id="9486a-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="9486a-216">**Mokėjimas** „FastTab” skirtuke **Banko paskyra** lauke pasirinkite **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="9486a-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Tiekėjo išsamios informacijos puslapis](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="9486a-218">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-218">Select **Save**.</span></span>
10. <span data-ttu-id="9486a-219">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9486a-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="9486a-220">Įveskite tiekėjo mokėjimą</span><span class="sxs-lookup"><span data-stu-id="9486a-220">Enter a vendor payment</span></span>

<span data-ttu-id="9486a-221">Turite sukurti naują tiekėjo mokėjimą naudodami [mokėjimo pasiūlymą](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="9486a-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="9486a-222">Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9486a-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9486a-223">**Tiekėjo mokėjimo žurnalas** puslapyje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="9486a-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="9486a-224">Lauke **Pavadinimas** pasirinkite **Tiek.Mok.**</span><span class="sxs-lookup"><span data-stu-id="9486a-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="9486a-225">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="9486a-225">Select **Lines**.</span></span>
5. <span data-ttu-id="9486a-226">Pasirinkite **Mokėjimo pasiūlymas** \> **Sukurti mokėjimo pasiūlymą**.</span><span class="sxs-lookup"><span data-stu-id="9486a-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="9486a-227">Dialogo lange **Tiekėjo mokėjimo pasiūlymas** konfigūruokite sąlygas įrašams, skirtiems tik **GB_SI_000001** tiekėjo paskyrai, filtruoti ir tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="9486a-228">Pasirinkite **00000007_SF** sąskaitos faktūros eilutę ir pasirinkite **Kurti mokėjimą**.</span><span class="sxs-lookup"><span data-stu-id="9486a-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Tiekėjo mokėjimo pasiūlymo dialogo langas](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="9486a-230">Patikrinkite, ar įvestas apmokėjimas sukonfigūruotas naudoti **Elektroninis** mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="9486a-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Puslapis Tiekėjo mokėjimai](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="9486a-232">Apdorokite tiekėjo mokėjimą naudodami standartinį ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="9486a-233">Nustatykite elektroninį mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="9486a-233">Set up the electronic payment method</span></span>

<span data-ttu-id="9486a-234">Turite sukonfigūruoti elektroninio mokėjimo metodą, kad jis naudotų importuoto ER formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9486a-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="9486a-235">Eikite į **Mokėtinos sumos** \> **Mokėjimo nustatymas** \> **Mokėjimo būdai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="9486a-236">**Mokėjimo būdai – tiekėjai** puslapyje pasirinkite **Elektroninis** mokėjimo būdą kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="9486a-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="9486a-237">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-237">Select **Edit**.</span></span>
4. <span data-ttu-id="9486a-238">**Failo formatai** „FastTab“ skirtuke nustatykite **Bendras elektroninis eksportavimo formatas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9486a-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="9486a-239">Lauke **Eksportuoti formato konfigūraciją** pasirinkite **BACS (JK)** formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9486a-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Mokėjimo metodai – tiekėjų puslapis](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="9486a-241">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="9486a-242">Apdorokite mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="9486a-242">Process a vendor payment</span></span>

1. <span data-ttu-id="9486a-243">Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9486a-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9486a-244">Puslapyje **Tiekėjo mokėjimų žurnalas** pasirinkite anksčiau pridėtą mokėjimų žurnalą tada pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="9486a-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="9486a-245">**Tiekėjo mokėjimai** puslapyje pasirinkite **Generuoti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="9486a-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="9486a-246">Dialogo lange **Generuoti mokėjimus** įveskite tolesnę informaciją:</span><span class="sxs-lookup"><span data-stu-id="9486a-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9486a-247">Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="9486a-248">Lauke **Banko sąskaita** įveskite **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="9486a-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="9486a-249">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-249">Select **OK**.</span></span>
6. <span data-ttu-id="9486a-250">**Elektroninės ataskaitos parametrai** dialogo lange nustatykite **Spausdinti kontrolės ataskaitą** pasirinktį į **Taip**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Elektroninių ataskaitų parametrų dialogo puslapis](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="9486a-252">Be mokėjimo failo, taip pat galite generuoti kontrolės ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9486a-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="9486a-253">Atsisiųskite suarchyvuotą failą, tada iš jo išskleiskite šiuos failus:</span><span class="sxs-lookup"><span data-stu-id="9486a-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="9486a-254">Kontrolės ataskaita „Excel” formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-254">The control report in Excel format</span></span>
    - <span data-ttu-id="9486a-255">Mokėjimo failas TXT formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-255">The payment file in TXT format</span></span>

        <span data-ttu-id="9486a-256">Atkreipkite dėmesį, kad pagal pateikto ER formato [struktūrą](#PositionRoutingNumber), sugeneruotame faile mokėjimo eilutės failas  prasideda banko kodu, kuris buvo [nurodytas](#DefineRoutingNumber) sukonfigūruotai banko paskyrai.</span><span class="sxs-lookup"><span data-stu-id="9486a-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Mokėjimo failas TXT formatu](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="9486a-258">Pritaikykite standartinį ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-258">Customize the standard ER format</span></span>

<span data-ttu-id="9486a-259">Pavyzdžiui, šiame skyriuje rodomas pavyzdys, kurį norite naudoti su „Microsoft” teikiamomis ER konfigūracijomis, kad būtų sugeneruoti tiekėjų mokėjimo failai BACS formatu, bet turite atitinkamai pritaikyti, kad atitiktų konkretaus banko reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9486a-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="9486a-260">Jums taip pat reikia atnaujinti pasirinktinį formatą, kai naujos ER konfigūracijų versijos taps prieinamomis.</span><span class="sxs-lookup"><span data-stu-id="9486a-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="9486a-261">Tačiau siekiate atnaujinti be didesnių išlaidų.</span><span class="sxs-lookup"><span data-stu-id="9486a-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="9486a-262">Šiuo atveju, būdami „Litware, Inc.” atstovu turite sukurti (išvesti) naują ER formato konfigūraciją naudodami „Microsoft” pateiktą konfigūraciją **BACS (JK)** kaip pagrindą.</span><span class="sxs-lookup"><span data-stu-id="9486a-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="9486a-263">Sukurkite pritaikytą formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-263">Create a custom format</span></span>

1. <span data-ttu-id="9486a-264">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9486a-265">**Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="9486a-266">„Litware, Inc.” naudos ER formato konfigūracijos 1.1 versiją kaip pasirinktinės versijos pagrindą.</span><span class="sxs-lookup"><span data-stu-id="9486a-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="9486a-267">Pasirinkite **Kurti konfigūraciją**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9486a-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="9486a-268">Galite naudoti dialogo langą, kad sukurtumėte naują pasirinktinio mokėjimo formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9486a-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="9486a-269">**Nauja** lauko grupėje pasirinkite **Išvesti iš Pavadinimo: BACS (UK), „Microsoft”** parinktį.</span><span class="sxs-lookup"><span data-stu-id="9486a-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="9486a-270">**Pavadinimas** lauke įveskite **BACS (JK pritaikytas)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Konfigūracijos išplečiamojo dialogo lango kūrimas](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="9486a-272">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="9486a-272">Select **Create configuration**.</span></span>

<span data-ttu-id="9486a-273">**BACS (pritaikyta JK)** sukuriama ER formato konfigūracijos versija 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="9486a-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="9486a-274">Ši versija turi [būseną](general-electronic-reporting.md#component-versioning) **Juodraštis** ir ji gali būti redaguojama.</span><span class="sxs-lookup"><span data-stu-id="9486a-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="9486a-275">Jūsų pritaikyto ER formato dabartinis turinys atitinka „Microsoft” pateikto formato turinį.</span><span class="sxs-lookup"><span data-stu-id="9486a-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Konfigūracijų puslapis](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="9486a-277">Redaguoti pritaikytą formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-277">Edit a custom format</span></span>

<span data-ttu-id="9486a-278">Turite sukonfigūruoti savo pritaikytą formatą, kad jis atitiktų banko konkrečius reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9486a-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="9486a-279">Pavyzdžiui, bankas gali reikalauti, kad sugeneruotuose apmokėjimų failuose turi būti nurodytas Tarptautinių tarpbankinių finansinių atsiskaitymų organizacijos (angl. „Society for Worldwide Interbank Financial Telecommunication“ (SWIFT) kodas, kuriam priskirtas agento vaidmuo apdorojant tiekėjo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="9486a-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="9486a-280">SWIFT kodai yra tarptautiniai banko kodai, kurie nurodo tam tikrus bankus visame pasaulyje.</span><span class="sxs-lookup"><span data-stu-id="9486a-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="9486a-281">Jie taip pat vadinami Banko identifikaciniais kodais (BIC).</span><span class="sxs-lookup"><span data-stu-id="9486a-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="9486a-282">SWIFT kodas susideda iš 11 simbolių ir turi būti įvestas sugeneruoto apmokėjimo kiekvieno mokėjimo eilučių pradžioje.</span><span class="sxs-lookup"><span data-stu-id="9486a-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="9486a-283">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9486a-284">**Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (pritaikyta JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="9486a-285">**Versijos** „FastTab” skirtuke pasirinkite pasirinktos konfigūracijos **1.1.1** versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="9486a-286">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-286">Select **Designer**.</span></span>
5. <span data-ttu-id="9486a-287">**Formato kūrimo įrankis** puslapyje pasirinkite **Rodyti išsamią informaciją**, kad peržiūrėtumėte daugiau informacijos apie formatavimo elementus.</span><span class="sxs-lookup"><span data-stu-id="9486a-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="9486a-288">Išplėskite ir peržiūrėkite šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="9486a-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="9486a-289">**BACSAtaskaitųAplankas** **Aplankas** tipo elementas.</span><span class="sxs-lookup"><span data-stu-id="9486a-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="9486a-290">Šis elementas naudojamas generuoti išvestį suskleistu formatu.</span><span class="sxs-lookup"><span data-stu-id="9486a-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="9486a-291">**Failas** **Failo** tipo elementas.</span><span class="sxs-lookup"><span data-stu-id="9486a-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="9486a-292">Šis elementas naudojamas generuoti mokėjimo failą TXT formatu.</span><span class="sxs-lookup"><span data-stu-id="9486a-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="9486a-293">**Operacijos** **Seka** tipo elementas.</span><span class="sxs-lookup"><span data-stu-id="9486a-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="9486a-294">Šis elementas naudojamas generuoti vieną mokėjimo eilutę mokėjimo faile.</span><span class="sxs-lookup"><span data-stu-id="9486a-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="9486a-295">**Operacija** **Seka** tipo elementas.</span><span class="sxs-lookup"><span data-stu-id="9486a-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="9486a-296">Šis elementas naudojamas generuoti atskirus vienos mokėjimo eilutės laukus.</span><span class="sxs-lookup"><span data-stu-id="9486a-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="9486a-297">Pasirinkite **opearcija** elementą.</span><span class="sxs-lookup"><span data-stu-id="9486a-297">Select the **transaction** element.</span></span>

    ![Operacijos elementas, esantis ER operacijų kūrimo įrankyje](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="9486a-299">Pateikta ataskaita sukonfigūruota taip, kad <a id="PositionRoutingNumber"></a>kiekviena mokėjimo eilutė prasideda banko kodu.</span><span class="sxs-lookup"><span data-stu-id="9486a-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="9486a-300">**tiek.BankoKodas** formato elementas naudojamas šiam tikslui.</span><span class="sxs-lookup"><span data-stu-id="9486a-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="9486a-301">Pasirinkite **Pridėti** ir pasirinkite **Tekstas \\Eilutė** pridedamo elemento formato tipą:</span><span class="sxs-lookup"><span data-stu-id="9486a-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="9486a-302">**Pavadinimas** lauke įveskite **tiek.BankoSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="9486a-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="9486a-303">**Mažiausias ilgis** lauke įveskite **11**.</span><span class="sxs-lookup"><span data-stu-id="9486a-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="9486a-304">**Didžiausias ilgis** lauke įveskite **11**.</span><span class="sxs-lookup"><span data-stu-id="9486a-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="9486a-305">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9486a-306">**tiek.BankoSWIFT**elementas bus naudojamas įvesti tiekėjo banko SWIFT kodą sugeneruotuose failuose.</span><span class="sxs-lookup"><span data-stu-id="9486a-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="9486a-307">Formato struktūros medyje pasirinkite **tiek.BankoSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="9486a-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="9486a-308">Pasirinkite **Perkelti aukštyn**, kad perkeltumėte pasirinkto formato elementą aukštyn vienu lygiu.</span><span class="sxs-lookup"><span data-stu-id="9486a-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="9486a-309">Kartokite šį veiksmą, kol **tiek.BankoSWIFT** elementas taps <a id="PositionSWIFTCode"></a>pirmu elementu, esančiu pirminiame **operacija** elemente.</span><span class="sxs-lookup"><span data-stu-id="9486a-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![Tiek.BankoSWIFT kaip pirmas elementas, esantis ER operacijų kūrimo įrankio operacijoje](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="9486a-311">Kol **tiek.BankoSWIFT** vis dar yra pasirinkta formato struktūros medyje, pasirinkite **Susiejimas** skirtuke ir tada išplėskite **modelis** duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="9486a-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="9486a-312">Išplėskite **modelis.Mokėjimas** \> **modelis.Mokėjimas.KreditoriausAgentas** ir pasirinkite **modelis.Mokėjimas. KreditoriausAgentas.BICFI** duomenų šaltinio lauką.</span><span class="sxs-lookup"><span data-stu-id="9486a-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="9486a-313">Šio duomenų šaltinio lauke rodomas tiekėjo banko SWIFT kodas, kuriam priskirtas agento vaidmuo apdorojant tiekėjo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="9486a-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="9486a-314">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-314">Select **Bind**.</span></span> <span data-ttu-id="9486a-315">**tiek.BankoSWIFT** formato elementas dabar yra susietas su **modelis.Mokėjimas.KreditoriausAgentas.BICFI** duomenų šaltinio lauku, kad SWIFT kodai būtų įvesti sugeneruotuose mokėjimo failuose.</span><span class="sxs-lookup"><span data-stu-id="9486a-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![tiek.BankoSWIFT formato elementas, susietas su modelis.Mokėjimas.KreditoriausAgentas.BICFI duomenų šaltinio lauku ER operacijų kūrimo įrankyje](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="9486a-317">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-317">Select **Save**.</span></span>
15. <span data-ttu-id="9486a-318">Uždarykite kūrimo įrankio puslapį.</span><span class="sxs-lookup"><span data-stu-id="9486a-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="9486a-319">Pažymėkite pritaikytą formatą kaip leistiną</span><span class="sxs-lookup"><span data-stu-id="9486a-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="9486a-320">Dabar, kai sukurta pirmoji jūsų pritaikyto formato versija, kurios būsena **Juodraštis**, ją galite paleisti testavimui.</span><span class="sxs-lookup"><span data-stu-id="9486a-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="9486a-321">Norėdami paleisti ataskaitą, turite apdoroti tiekėjo mokėjimą naudodami mokėjimo būdą, nurodantį jūsų pritaikytą ER formatą.</span><span class="sxs-lookup"><span data-stu-id="9486a-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="9486a-322">Pagal numatytuosius nustatymus jums iškvietus ER formatą programoje tik būseną\` **Baigta** ar **Bendrinta** turinčios versijos [bus svarstomos](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="9486a-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="9486a-323">Toks veikimas užtikrina, kad nebaigto dizaino ER formatai nebūtų naudojami.</span><span class="sxs-lookup"><span data-stu-id="9486a-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="9486a-324">Tačiau, atliekant bandomuosius vykdymus, galite priversti programą naudoti ER formato **Juodraštis** būsenos versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="9486a-325">Tokiu būdu galite koreguoti dabartinio formato versiją, jei reikia atlikti pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="9486a-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="9486a-326">Daugiau informacijos žr. [Taikomumas](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="9486a-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="9486a-327">Norėdami naudoti ER formato juodraščio versiją, turite aiškiai pažymėti ER formatą.</span><span class="sxs-lookup"><span data-stu-id="9486a-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="9486a-328">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9486a-329">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="9486a-330">**Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="9486a-331">Pasirinkite **Redaguoti**, kad pagal poreikį galėtumėte redaguoti esamą puslapį.</span><span class="sxs-lookup"><span data-stu-id="9486a-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="9486a-332">Kairiojoje srityje esančiame konfigūracijos medyje pasirinkite **BACS (pritaikyta JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="9486a-333">Nustatykite **Leist juodraštį** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9486a-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Paleiskite juodraštinę pasirinktį Konfigūracijų puslapyje](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="9486a-335">Apdorokite tiekėjo mokėjimą naudodami pritaikytą ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="9486a-336">Nustatykite elektroninį mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="9486a-336">Set up the electronic payment method</span></span>

<span data-ttu-id="9486a-337">Turite sukonfigūruoti elektroninį mokėjimo būdą, kad jūsų pritaikyto ER formatas būtų naudojamas tiekėjo mokėjimams apdoroti.</span><span class="sxs-lookup"><span data-stu-id="9486a-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="9486a-338">Eikite į **Mokėtinos sumos** \> **Mokėjimo nustatymas** \> **Mokėjimo būdai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="9486a-339">**Mokėjimo būdai – tiekėjai** puslapyje pasirinkite **Elektroninis** mokėjimo būdą kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="9486a-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="9486a-340">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-340">Select **Edit**.</span></span>
4. <span data-ttu-id="9486a-341">**Failo formatas** „FastTab“ skirtuke nustatykite **Bendras elektroninis eksportavimo formatas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9486a-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="9486a-342">**Eksportuoti formato konfigūraciją** lauke pasirinkite **BACS (pritaikyta JK)** formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9486a-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Mokėjimo metodai – tiekėjų puslapis](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="9486a-344">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="9486a-345">Apdorokite mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="9486a-345">Process a vendor payment</span></span>

1. <span data-ttu-id="9486a-346">Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9486a-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9486a-347">**Tiekėjo mokėjimo žurnalas** puslapyje pasirinkite jūsų anksčiau sukurtą mokėjimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="9486a-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="9486a-348">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="9486a-348">Select **Lines**.</span></span>
4. <span data-ttu-id="9486a-349">**Tiekėjo mokėjimai** puslapyje, virš tinklelio, pasirinkite **Mokėjimo būsena** \>**Nėra**.</span><span class="sxs-lookup"><span data-stu-id="9486a-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="9486a-350">Pasirinkite **Generuoti mokėjimą**.</span><span class="sxs-lookup"><span data-stu-id="9486a-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="9486a-351">Dialogo lange **Generuoti mokėjimus** įveskite tolesnę informaciją:</span><span class="sxs-lookup"><span data-stu-id="9486a-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9486a-352">Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="9486a-353">Lauke **Banko sąskaita** įveskite **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="9486a-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="9486a-354">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-354">Select **OK**.</span></span>
8. <span data-ttu-id="9486a-355">**Elektroninės ataskaitos parametrai** dialogo lange nustatykite **Spausdinti kontrolės ataskaitą** pasirinktį į **Taip**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9486a-356">Be mokėjimo failo, galite generuoti tik kontrolės ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9486a-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="9486a-357">Atsisiųskite suarchyvuotą failą, tada iš jo išskleiskite šiuos failus:</span><span class="sxs-lookup"><span data-stu-id="9486a-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="9486a-358">Kontrolės ataskaita „Excel” formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-358">The control report in Excel format</span></span>
    - <span data-ttu-id="9486a-359">Mokėjimo failas TXT formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-359">The payment file in TXT format</span></span>

        <span data-ttu-id="9486a-360">Atkreipkite dėmesį, kad pagal jūsų pritaikyto ER formato struktūrą, sugeneruoto failo mokėjimo eilutė dabar [prasideda](#PositionSWIFTCode) SWIFT kodu,  [įvestu](#DefineSWIFTCode) tiekėjo, kurio apmokėjimas buvo apdorotas, banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="9486a-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Mokėjimo failas TXT formatu](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="9486a-362">Importuokite standartinio ER formato konfigūracijų naujas versijas</span><span class="sxs-lookup"><span data-stu-id="9486a-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="9486a-363">Pavyzdžiui, šiame skyriuje rodomas pavyzdys, kai gaunate pranešimą apie Žinių bazės straipsnį [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="9486a-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="9486a-364">Šis pranešimas informuoja jus apie naują **BACS (JK)** „Microsoft” paskelbtą ER formato versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="9486a-365">Be kontrolės ataskaitos ši nauja versija leidžia vartotojams generuoti mokėjimo pažymų ataskaitą ir lydinčios pažymos ataskaitą, kol tiekėjo mokėjimas apdorojamas.</span><span class="sxs-lookup"><span data-stu-id="9486a-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="9486a-366">Jums ši funkcija pravers.</span><span class="sxs-lookup"><span data-stu-id="9486a-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="9486a-367">Importuokite standartinio ER formato konfigūracijų naujas versijas</span><span class="sxs-lookup"><span data-stu-id="9486a-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="9486a-368">Norėdami pridėti standartinių ER konfigūracijų naujas versijas prie dabartinės „Finance” programos, importuokite jas iš jūsų sukonfigūruotos ER [saugyklos](general-electronic-reporting.md#Repository).</span><span class="sxs-lookup"><span data-stu-id="9486a-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="9486a-369">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-370">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Microsoft”** plytelę ir pasirinkite **Saugyklos**, kad peržiūrėtumėte „Microsoft” tiekėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9486a-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="9486a-371">Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="9486a-372">Jei esate raginami autorizuoti, kad prisijungtumėte prie „Regulatory Configuration Service”, vadovaukitės autorizavimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="9486a-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="9486a-373">**Konfigūracijos saugykla** puslapyje kairėje konfigūracijos medyje pasirinkite **BACS (JK)** formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9486a-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="9486a-374">**Versijos** „FastTab” skirtuke pasirinkite pasirinktos ER formato konfigūracijos **3.3** versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="9486a-375">Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš Bendrosios saugyklos į dabartinę „Finance“ programą.</span><span class="sxs-lookup"><span data-stu-id="9486a-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigūracijos saugyklos puslapis](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="9486a-377">Jei kyla problemų prisijungiant prie [Bendrosios saugyklos](er-download-configurations-global-repo.md), vietoj to galite [atsisiųsti konfigūracijas](download-electronic-reporting-configuration-lcs.md) iš LCS.</span><span class="sxs-lookup"><span data-stu-id="9486a-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="9486a-378">Peržiūrėkite importuotas ER formato konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="9486a-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="9486a-379">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-380">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="9486a-381">**Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="9486a-382">Sparčiajame skirtuke **Versijos** paspauskite **3.3**.</span><span class="sxs-lookup"><span data-stu-id="9486a-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="9486a-383">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-383">Select **Designer**.</span></span>
6. <span data-ttu-id="9486a-384">**Formato kūrimo įrankis** puslapyje išplėskite **BACSAtaskaitosAplankas** formato elementą.</span><span class="sxs-lookup"><span data-stu-id="9486a-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="9486a-385">Atkreipkite dėmesį, kad versijoje 3.3 yra **MokėjimoPažymosAtaskaita** formato elementas, kuris naudojamas mokėjimo pažymos ataskaitai generuoti, kai apdorojamas tiekėjo mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="9486a-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![MokėjimoPažymosAtaskaitos formato elementas ER operacijų kūrimo įrankyje](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="9486a-387">Uždarykite kūrimo įrankio puslapį.</span><span class="sxs-lookup"><span data-stu-id="9486a-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="9486a-388">Patvirtinkite importuoto formato naujos versijos pakeitimus pritaikytame formate </span><span class="sxs-lookup"><span data-stu-id="9486a-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="9486a-389">Užbaikite pritaikyto formato esamą juodraštinę versiją</span><span class="sxs-lookup"><span data-stu-id="9486a-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="9486a-390">Jei norite, kad dabartinė jūsų pritaikyto formato būsena būtų baigta, užbaikite juodraštinę versiją 1.1.1, pakeisdami jos būseną iš **Juodraštis** į **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="9486a-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="9486a-391">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="9486a-392">**Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="9486a-393">**Konfigūracijos** puslapyje kairėje esančiame konfigūracijų medyje išskleiskite **Mokėjimo modelis**, išplėskite **BACS (JK)** ir tada pasirinkite **BACS (pritaikyta JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="9486a-394">**Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="9486a-395">Versijos 1.1.1 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="9486a-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="9486a-396">Nauja redaguotina versija, 1.1.2, buvo pridėta ir jos būsena yra **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="9486a-397">Šią versiją galite naudoti norėdami atlikti tolesnius keitimus savo pritaikytame ER formate.</span><span class="sxs-lookup"><span data-stu-id="9486a-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="9486a-398">Iš naujo pritaikykite pritaikytą formatą pagal naują pagrindinę versiją</span><span class="sxs-lookup"><span data-stu-id="9486a-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="9486a-399">Norėdami naudoti naujas **BACS (JK)** formato 3.3 versijos funkcijas jūsų tinkinime, turite pakeisti pagrindinės konfigūracijos versiją, skirtą pritaikytam tinkinimui **BACS (pritaikyta JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="9486a-400">Šis procesas vadinamas [pritaikymu kitoje vietoje](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="9486a-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="9486a-401">Vietoj **BACS (JK)** 1.1 versijos naudokite 3.3 versiją.</span><span class="sxs-lookup"><span data-stu-id="9486a-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="9486a-402">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="9486a-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="9486a-403">**Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (pritaikyta JK)**.</span><span class="sxs-lookup"><span data-stu-id="9486a-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="9486a-404">**Versijos** „FastTab” skirtuke pasirinkite versiją **1.1.2** ir pasirinkite **Pritaikyti kitoje vietoje**.</span><span class="sxs-lookup"><span data-stu-id="9486a-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="9486a-405">**Pritaikyti kitoje vietoje** dialogo lange **Tikslinė versija** lauke pasirinkite pagrindinės konfigūracijos **3.3** versiją pritaikyti ją kaip naują pagrindinę versiją ir naudoti ją konfigūracijai atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="9486a-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Pritaikymo kitoje vietoje dialogo langas](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="9486a-407">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-407">Select **OK**.</span></span>
6. <span data-ttu-id="9486a-408">Atkreipkite dėmesį, kad juodraštinės versijos numeris pakeistas iš **1.1.2** į **3.3.2**, kad parodytų pagrindinės versijos pasikeitimą.</span><span class="sxs-lookup"><span data-stu-id="9486a-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="9486a-409">Kai pritaikyta versija ir naujoji versija suliejamos, gali atsirasti konfliktų dėl formatų, kurie negali būti automatiškai sulieti, pasikeitimų.</span><span class="sxs-lookup"><span data-stu-id="9486a-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Pritaikykite konfigūraciją su konfliktais kitoje vietoje Konfigūracijų puslapyje](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="9486a-411">Jei atsirado konfliktų, jie turi būti išspręsti neautomatiniu būdu formato kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="9486a-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="9486a-412">Sparčiajame skirtuke **Versijos** paspauskite **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="9486a-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="9486a-413">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-413">Select **Designer**.</span></span>
9. <span data-ttu-id="9486a-414">**Formato kūrimo įrankis** puslapyje **Išsami informacija** „FastTab” pasirinkite pritaikyto kitoje vietoje konflikto įrašą ir pasirinkite **Taikyti pagrindinę vertę**.</span><span class="sxs-lookup"><span data-stu-id="9486a-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Pritaikykite konflikto įrašą kitoje vietoje ER operacijų kūrimo įrankyje](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="9486a-416">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9486a-416">Select **Save**.</span></span>

    <span data-ttu-id="9486a-417">Pritaikyto kitoje vietoje konflikto įrašas nebeatsiras **Išsami informacija** „FastTab”.</span><span class="sxs-lookup"><span data-stu-id="9486a-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konfliktas išspręstas ER operacijų kūrimo įrankyje](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="9486a-419">Jūs išsprendėte konfliktą patvirtinę, kad šioje pagrindinio modelio versijoje Nr.3 turi būti naudojama šiame ER formate.</span><span class="sxs-lookup"><span data-stu-id="9486a-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="9486a-420">Išplėskite **BACSAtaskaitųAplankas** \> **failas** \>**operacijos** \> **operacija**.</span><span class="sxs-lookup"><span data-stu-id="9486a-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="9486a-421">**Susiejimas** skirtuke atkreipkite dėmesį, kad jūsų pritaikyto ER formato versijoje 3.3.2 yra tiek jūsų tinkinimas (**tiek.BankoSWIFT** formato elementas ir jo susiejimas) ir nauja „Microsoft” pateikta pagrindinio ER formato versijos 3.3 versijos funkcija ( **MokėjimoPažymosAtaskaita** formato elemento kartu su jo įdėtais elementais ir sukonfigūruotais susiejimais).</span><span class="sxs-lookup"><span data-stu-id="9486a-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="9486a-422">Tik keliais pelės spustelėjimais patvirtinote naujos pagrindinės versijos pakeitimus suliedami juos su jūsų tinkinimu.</span><span class="sxs-lookup"><span data-stu-id="9486a-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Sulietas formatas ER operacijų kūrimo įrankyje](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="9486a-424">Uždarykite kūrimo įrankio puslapį.</span><span class="sxs-lookup"><span data-stu-id="9486a-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="9486a-425">Pritaikymo kitoje vietoje veiksmas nėra grįžtamas.</span><span class="sxs-lookup"><span data-stu-id="9486a-425">The rebase action is reversible.</span></span> <span data-ttu-id="9486a-426">Norėdami atšaukti šį pritaikymą kitoje vietoje, pasirinkite **1.1.1** **BACS (pritaikyta JK)** formato versiją **Versijos** „FastTab” skirtuke ir pasirinkite **Gauti šią versiją**.</span><span class="sxs-lookup"><span data-stu-id="9486a-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="9486a-427">Tada 3.3.2 versija bus pernumeruota į 1.1.2, o juodraštinės versijos 1.1.2 turinys atitiks 1.1.1 versijos turinį.</span><span class="sxs-lookup"><span data-stu-id="9486a-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="9486a-428">Apdorokite tiekėjo mokėjimą naudodami iš pritaikytą kitoje vietoje ER formatą</span><span class="sxs-lookup"><span data-stu-id="9486a-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="9486a-429">Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9486a-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="9486a-430">**Tiekėjo mokėjimo žurnalas** puslapyje pasirinkite jūsų anksčiau sukurtą mokėjimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="9486a-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="9486a-431">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="9486a-431">Select **Lines**.</span></span>
4. <span data-ttu-id="9486a-432">**Tiekėjo mokėjimai** puslapyje, virš tinklelio, pasirinkite **Mokėjimo būsena** \>**Nėra**.</span><span class="sxs-lookup"><span data-stu-id="9486a-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="9486a-433">Pasirinkite **Generuoti mokėjimą**.</span><span class="sxs-lookup"><span data-stu-id="9486a-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="9486a-434">Dialogo lange **Generuoti mokėjimus** įveskite tolesnę informaciją:</span><span class="sxs-lookup"><span data-stu-id="9486a-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9486a-435">Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.</span><span class="sxs-lookup"><span data-stu-id="9486a-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="9486a-436">Lauke **Banko sąskaita** įveskite **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="9486a-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="9486a-437">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-437">Select **OK**.</span></span>
8. <span data-ttu-id="9486a-438">Dialogo lange **Elektroninių ataskaitų parametrai** įveskite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="9486a-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="9486a-439">Nustatykite parinktį **Spausdinti kontrolės ataskaitą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9486a-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="9486a-440">Nustatykite **Spausdinti mokėjimo pažymą** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9486a-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Elektroninių ataskaitų parametrų dialogo langas](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="9486a-442">Be mokėjimo failo galite generuoti tiek kontrolės ataskaita, tiek mokėjimo pažymos ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9486a-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="9486a-443">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9486a-443">Select **OK**.</span></span>
10. <span data-ttu-id="9486a-444">Atsisiųskite suarchyvuotą failą, tada iš jo išskleiskite šiuos failus:</span><span class="sxs-lookup"><span data-stu-id="9486a-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="9486a-445">Kontrolės ataskaita „Excel” formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-445">The control report in Excel format</span></span>
    - <span data-ttu-id="9486a-446">Mokėjimo pažymos ataskaita „Excel” formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-446">The payment advice report in Excel format</span></span>

        ![Mokėjimo pažymos ataskaita „Excel” formatu](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="9486a-448">Mokėjimo failas TXT formatu</span><span class="sxs-lookup"><span data-stu-id="9486a-448">The payment file in TXT format</span></span>

        <span data-ttu-id="9486a-449">Atkreipkite dėmesį į sugeneruoto failo, prasidedančio SWIFT kodu, kuris buvo įvestas tiekėjo, kurio apmokėjimas apdorojamas, banko sąskaitai, mokėjimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="9486a-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Mokėjimo failas TXT formatu](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="9486a-451">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9486a-451">Additional resources</span></span>

- [<span data-ttu-id="9486a-452">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9486a-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9486a-453">ER konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="9486a-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="9486a-454">ER konfigūracijų atsisiuntimas iš „Configuration service” Bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="9486a-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
