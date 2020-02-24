---
title: El. pašto ER paskirties vietos tipas
description: Šioje temoje pateikiama informacija apie tai, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento el. pašto paskirties vietą.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019906"
---
# <span data-ttu-id="bef64-103"><a name="EmailDestinationType">El. pašto paskirties vieta</a></span><span class="sxs-lookup"><span data-stu-id="bef64-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bef64-104">Galite sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento el. pašto paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="bef64-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="bef64-105">Remiantis paskirties vietos nustatymu, sugeneruotas dokumentas pristatomas kaip el. laiško priedas.</span><span class="sxs-lookup"><span data-stu-id="bef64-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="bef64-106">Nustatykite parinktį **Įgalinta** į **Taip**, norėdami siųsti išvesties failą el. paštu.</span><span class="sxs-lookup"><span data-stu-id="bef64-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="bef64-107">Įgalinę šią parinktį, galite nurodyti el. laiško gavėjus ir redaguoti el. laiško temą bei tekstą.</span><span class="sxs-lookup"><span data-stu-id="bef64-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="bef64-108">Galite nustatyti nuolatinį el. laiško temos ir teksto tekstą arba galite naudoti ER [formules](er-formula-language.md), norėdami el. laiškų tekstą kurti dinamiškai.</span><span class="sxs-lookup"><span data-stu-id="bef64-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="bef64-109">ER el. pašto adresus galite konfigūruoti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="bef64-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="bef64-110">Konfigūravimą galima baigti taip pat, kaip jį baigia spausdinimo valdymo funkcija, arba galima nustatyti el. pašto adresą, naudojant tiesioginę nuorodą į ER konfigūraciją per formulę.</span><span class="sxs-lookup"><span data-stu-id="bef64-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="bef64-111">[![El. pašto paskirties vietos įgalinimas](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="bef64-112">El. pašto adresų tipai</span><span class="sxs-lookup"><span data-stu-id="bef64-112">Email address types</span></span>

<span data-ttu-id="bef64-113">Pasirinkus laukų **Kam** arba **Kopija** parinktį **Redaguoti**, rodomas dialogo langas **Siųsti el. laišką**.</span><span class="sxs-lookup"><span data-stu-id="bef64-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="bef64-114">Tada galite pasirinkti norimą naudoti el. pašto adreso tipą.</span><span class="sxs-lookup"><span data-stu-id="bef64-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="bef64-115">Šiuo metu palaikomi el. pašto tipai **Konfigūravimo el. laiškas** ir **Spausdinimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="bef64-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="bef64-116">[![El. laiško tipo pasirinkimas](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="bef64-117">Spausdinimo valdymas</span><span class="sxs-lookup"><span data-stu-id="bef64-117">Print management</span></span>

<span data-ttu-id="bef64-118">Jei pasirinksite el. laiško tipą **Spausdinimo valdymas**, galite įvesti fiksuotus el. pašto adresus lauke **Kam**.</span><span class="sxs-lookup"><span data-stu-id="bef64-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="bef64-119">[![Fiksuotų el. pašto adresų konfigūravimas](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="bef64-120">Norėdami naudoti nefiksuotus el. pašto adresus, turite pasirinkti failo paskirties vietos el. pašto šaltinio tipą.</span><span class="sxs-lookup"><span data-stu-id="bef64-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="bef64-121">Palaikomos šios vertės: **Klientas**, **Tiekėjas**, **Potencialus klientas**, **Kontaktas**, **Konkurentas**, **Darbuotojas**, **Pretendentas**, **Galimas tiekėjas** ir **Neleidžiamas tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="bef64-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="bef64-122">Pasirinkę el. pašto šaltinio tipą, naudokite šalia lauko **El. pašto šaltinio sąskaita** esantį mygtuką, kad atidarytumėte formą **Formulės dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bef64-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="bef64-123">Šią formą galite naudoti norėdami pridėti formulę, kuri vykdymo metu pateikia pasirinkto šaltinio tipo **šalies sąskaitą** iš apdoroto dokumento į el. pašto paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="bef64-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="bef64-124">[![El. pašto šaltinio sąskaitos konfigūravimas](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="bef64-125">Formulės būdingos ER konfigūracijai.</span><span class="sxs-lookup"><span data-stu-id="bef64-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="bef64-126">Srityje **Formulė** įveskite konkretaus dokumento nuorodą į kliento arba tiekėjo šalies tipą.</span><span class="sxs-lookup"><span data-stu-id="bef64-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="bef64-127">Užuot rinkę tekstą, galite surasti duomenų šaltinio mazgą, atitinkantį kliento ar tiekėjo sąskaitą, ir tada pasirinkti **Įtraukti duomenų šaltinį**, kad atnaujintumėte formulę.</span><span class="sxs-lookup"><span data-stu-id="bef64-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="bef64-128">Pavyzdžiui, jei naudojate **ISO 20022 kredito perkėlimo** konfigūraciją, tiekėjo sąskaitą atitinkantis mazgas yra `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="bef64-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="bef64-129">Jei įvesite eilutės vertę, pvz., `"DE-001"`, ir įrašysite formulę, el. laiškas bus išsiųstas tiekėjo kontaktiniam asmeniui, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="bef64-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="bef64-130">[![ER formulių dizaino įrankio puslapis](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="bef64-131">[![El. pašto šaltinio sąskaitos konfigūravimas](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="bef64-132">Konfigūravimo el. laiškas</span><span class="sxs-lookup"><span data-stu-id="bef64-132">Configuration email</span></span>

<span data-ttu-id="bef64-133">Naudokite šį el. pašto tipą, jei jūsų naudojamos konfigūracijos duomenų šaltiniuose yra mazgas, pateikiantis **el. pašto adresą**.</span><span class="sxs-lookup"><span data-stu-id="bef64-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="bef64-134">Galite naudoti duomenų šaltinius ir funkcijas formulės dizaino įrankyje, kad gautumėte teisingai suformatuotą el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="bef64-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="bef64-135">Pavyzdžiui, jei naudojate **ISO 20022 kredito perkėlimo** konfigūraciją, tiekėjo kontaktinio asmens el. pašto adresą atitinkantis mazgas yra `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="bef64-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="bef64-136">[![El. pašto adreso šaltinio konfigūravimas](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="bef64-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bef64-137">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bef64-137">Additional resources</span></span>

- [<span data-ttu-id="bef64-138">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="bef64-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="bef64-139">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="bef64-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="bef64-140">Elektroninių ataskaitų (ER) formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="bef64-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
