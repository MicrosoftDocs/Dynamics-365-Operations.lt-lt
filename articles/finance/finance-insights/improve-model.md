---
title: Prognozės modelio tobulinimas (peržiūros versija)
description: Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646084"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="930b2-103">Prognozės modelio tobulinimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="930b2-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="930b2-104">Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="930b2-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="930b2-105">Paleidžiate savo modelį programos „Microsoft Dynamics 365 Finance“ darbo srityje **Klientų mokėjimo prognozės**.</span><span class="sxs-lookup"><span data-stu-id="930b2-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="930b2-106">Tada tobulinimo veiksmai atliekami naudojant „AI Builder“.</span><span class="sxs-lookup"><span data-stu-id="930b2-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="930b2-107">Pasirinkite retrospektyvinius rezultatus</span><span class="sxs-lookup"><span data-stu-id="930b2-107">Select historical outcomes</span></span>

<span data-ttu-id="930b2-108">Pirmiausia turite pasirinkti vieną ar daugiau iš trijų galimų SF rezultatų: **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.</span><span class="sxs-lookup"><span data-stu-id="930b2-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="930b2-109">Turi būti parenkami visi trys rezultatai.</span><span class="sxs-lookup"><span data-stu-id="930b2-109">All three outcomes should be selected.</span></span> <span data-ttu-id="930b2-110">Jei išvalysite bet kurio iš rezultatų žymėjimą, SF bus išfiltruota iš mokymo proceso ir bus sumažintas prognozavimas.</span><span class="sxs-lookup"><span data-stu-id="930b2-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="930b2-111">[![Rezultatų patvirtinimas](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="930b2-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="930b2-112">Jei jūsų organizacijai reikalingi tik du rezultatai, pakeiskite **Vėlavimas** ir **Žymus vėlavimas** ribines vertes į 0 (nulį) dienų.</span><span class="sxs-lookup"><span data-stu-id="930b2-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="930b2-113">Tokiu būdu galite efektyviai sutraukti prognozavimą į dvejetainę būseną **Laiku** arba **Vėlavimas**.</span><span class="sxs-lookup"><span data-stu-id="930b2-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="930b2-114">Pasirinkti laukus</span><span class="sxs-lookup"><span data-stu-id="930b2-114">Select fields</span></span>

<span data-ttu-id="930b2-115">Pasirinkus laukus, kuriuos reikia įtraukti į modelį, reikia žinoti, kad sąraše yra visi galimi „Common Data Service“ objekto laukai, kurie susieti su duomenimis, kurie yra „Azure“ duomenų telkinyje.</span><span class="sxs-lookup"><span data-stu-id="930b2-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Common Data Service entity that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="930b2-116">Kai kurie šių laukų **neturėtų** būti pasirenkami.</span><span class="sxs-lookup"><span data-stu-id="930b2-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="930b2-117">Laukai, kurie neturėtų būti parenkami, patenka į vieną iš trijų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="930b2-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="930b2-118">Laukas reikalingas „Common Data Service“ objektui, tačiau duomenų telkinyje nėra atsarginių duomenų.</span><span class="sxs-lookup"><span data-stu-id="930b2-118">The field is required for the Common Data Service entity, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="930b2-119">Šis laukas yra ID, todėl jo mašininio mokymo funkcija nesupranta.</span><span class="sxs-lookup"><span data-stu-id="930b2-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="930b2-120">Lauke yra informacijos, kuri bus nepasiekiama prognozuojant.</span><span class="sxs-lookup"><span data-stu-id="930b2-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="930b2-121">Toliau esančiuose skyriuose pateikiami laukai, kurie galimi SF ir kliento objektams, ir nurodomi laukai, kurie **neturėtų** būti parenkami mokymui.</span><span class="sxs-lookup"><span data-stu-id="930b2-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="930b2-122">Kiekvienam iš šių laukų nurodyta kategorija nurodo ankstesnio sąrašo kategorijas.</span><span class="sxs-lookup"><span data-stu-id="930b2-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-common-data-model-entity"></a><span data-ttu-id="930b2-123">SF „Common Data Model“ objektas</span><span class="sxs-lookup"><span data-stu-id="930b2-123">Invoice Common Data Model entity</span></span>

<span data-ttu-id="930b2-124">Tolesnėje iliustracijoje parodyti SF objekto laukai.</span><span class="sxs-lookup"><span data-stu-id="930b2-124">The following illustration shows the fields that are available for the invoice entity.</span></span>

<span data-ttu-id="930b2-125">[![Galimi SF objekto laukai](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="930b2-125">[![Available fields for the invoice entity](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="930b2-126">Šie laukai neturėtų būti parenkami mokymui.</span><span class="sxs-lookup"><span data-stu-id="930b2-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="930b2-127">**SF sąskaita** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="930b2-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="930b2-128">**Uždaryta** (3 kategorija) – šis laukas naudojamas, norint filtruoti (uždarytas) ir prognozuoti (neuždarytas) SF.</span><span class="sxs-lookup"><span data-stu-id="930b2-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="930b2-129">**Pavadinimas** (1 kategorija)</span><span class="sxs-lookup"><span data-stu-id="930b2-129">**Name** (category 1)</span></span>
- <span data-ttu-id="930b2-130">**Šaltinio ID** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="930b2-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="930b2-131">**Šaltinio įrašas** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="930b2-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="930b2-132">**Šaltinio lentelė** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="930b2-132">**Source table** (category 2)</span></span>

### <a name="customer-common-data-model-entity"></a><span data-ttu-id="930b2-133">Kliento „Common Data Model“ objektas</span><span class="sxs-lookup"><span data-stu-id="930b2-133">Customer Common Data Model entity</span></span>

<span data-ttu-id="930b2-134">Tolesnėje iliustracijoje parodyti kliento objekto laukai.</span><span class="sxs-lookup"><span data-stu-id="930b2-134">The following illustration shows the fields that are available for the customer entity.</span></span>

<span data-ttu-id="930b2-135">[![Galimi kliento objekto laukai](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="930b2-135">[![Available fields for the customer entity](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="930b2-136">Šis laukas neturėtų būti parenkamas mokymui.</span><span class="sxs-lookup"><span data-stu-id="930b2-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="930b2-137">**Eilučių unikalusis raktas** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="930b2-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="930b2-138">Filtrai</span><span class="sxs-lookup"><span data-stu-id="930b2-138">Filters</span></span>

<span data-ttu-id="930b2-139">Šiuo metu filtrai nepalaiko kliento mokėjimo prognozavimo scenarijaus.</span><span class="sxs-lookup"><span data-stu-id="930b2-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="930b2-140">Todėl pasirinkite **Praleisti šį veiksmą** ir pereikite prie suvestinės puslapio.</span><span class="sxs-lookup"><span data-stu-id="930b2-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="930b2-141">[![Fokusavimo režimas su filtrais](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="930b2-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="930b2-142">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="930b2-142">Privacy notice</span></span>
<span data-ttu-id="930b2-143">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="930b2-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
