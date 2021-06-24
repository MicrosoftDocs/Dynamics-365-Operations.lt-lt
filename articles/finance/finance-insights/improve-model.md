---
title: Prognozės modelio tobulinimas (peržiūros versija)
description: Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186647"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="7f6f2-103">Prognozės modelio tobulinimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7f6f2-104">Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="7f6f2-105">Paleidžiate savo modelį programos „Microsoft Dynamics 365 Finance“ darbo srityje **Klientų mokėjimo prognozės**.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="7f6f2-106">Tada tobulinimo veiksmai atliekami naudojant „AI Builder“.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="7f6f2-107">Pasirinkite retrospektyvinius rezultatus</span><span class="sxs-lookup"><span data-stu-id="7f6f2-107">Select historical outcomes</span></span>

<span data-ttu-id="7f6f2-108">Pirmiausia turite pasirinkti vieną ar daugiau iš trijų galimų SF rezultatų: **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="7f6f2-109">Turi būti parenkami visi trys rezultatai.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-109">All three outcomes should be selected.</span></span> <span data-ttu-id="7f6f2-110">Jei išvalysite bet kurio iš rezultatų žymėjimą, SF bus išfiltruota iš mokymo proceso ir bus sumažintas prognozavimas.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="7f6f2-111">[![Rezultatų patvirtinimas](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="7f6f2-112">Jei jūsų organizacijai reikalingi tik du rezultatai, pakeiskite **Vėlavimas** ir **Žymus vėlavimas** ribines vertes į 0 (nulį) dienų.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="7f6f2-113">Tokiu būdu galite efektyviai sutraukti prognozavimą į dvejetainę būseną **Laiku** arba **Vėlavimas**.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="7f6f2-114">Pasirinkti laukus</span><span class="sxs-lookup"><span data-stu-id="7f6f2-114">Select fields</span></span>

<span data-ttu-id="7f6f2-115">Jums renkantis laukelius, kuriuo reikia įtraukti į modelį, įsitikinkite, kad sąraše yra visi prieinami laukeliai „Microsoft Dataverse“ lentelėje, kuri yra žemėlapyje duomenyse „Azure“ duomenų ežere.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="7f6f2-116">Kai kurie šių laukų **neturėtų** būti pasirenkami.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="7f6f2-117">Laukai, kurie neturėtų būti parenkami, patenka į vieną iš trijų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="7f6f2-118">Laukelis turi būti „Dataverse“ lentelei, tačiau nėra jokių atsarginės kopijos duomenų jam duomenų ežere.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="7f6f2-119">Šis laukas yra ID, todėl jo mašininio mokymo funkcija nesupranta.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="7f6f2-120">Lauke yra informacijos, kuri bus nepasiekiama prognozuojant.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="7f6f2-121">Toliau esančiuose skyriuose pateikiami laukai, kurie galimi SF ir kliento objektams, ir nurodomi laukai, kurie **neturėtų** būti parenkami mokymui.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="7f6f2-122">Kiekvienam iš šių laukų nurodyta kategorija nurodo ankstesnio sąrašo kategorijas.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="7f6f2-123">Sąskaitos „Dataverse“ lentelė</span><span class="sxs-lookup"><span data-stu-id="7f6f2-123">Invoice Dataverse table</span></span>

<span data-ttu-id="7f6f2-124">Šiame paveiksle parodyti laukeliai, kurie yra prieinami sąskaitos lentelei.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="7f6f2-125">[![Prieinami laukeliai sąskaitos lentelei](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="7f6f2-126">Šie laukai neturėtų būti parenkami mokymui.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="7f6f2-127">**SF sąskaita** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="7f6f2-128">**Uždaryta** (3 kategorija) – šis laukas naudojamas, norint filtruoti (uždarytas) ir prognozuoti (neuždarytas) SF.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="7f6f2-129">**Pavadinimas** (1 kategorija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-129">**Name** (category 1)</span></span>
- <span data-ttu-id="7f6f2-130">**Šaltinio ID** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="7f6f2-131">**Šaltinio įrašas** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="7f6f2-132">**Šaltinio lentelė** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="7f6f2-133">Kliento „Dataverse“ lentelė</span><span class="sxs-lookup"><span data-stu-id="7f6f2-133">Customer Dataverse table</span></span>

<span data-ttu-id="7f6f2-134">Šiame paveiksle parodyti laukeliai, kurie yra prieinami kliento lentelei.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="7f6f2-135">[![Prieinami laukeliai kliento lentelei](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="7f6f2-136">Šis laukas neturėtų būti parenkamas mokymui.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="7f6f2-137">**Eilučių unikalusis raktas** (2 kategorija)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="7f6f2-138">Filtrai</span><span class="sxs-lookup"><span data-stu-id="7f6f2-138">Filters</span></span>

<span data-ttu-id="7f6f2-139">Šiuo metu filtrai nepalaiko kliento mokėjimo prognozavimo scenarijaus.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="7f6f2-140">Todėl pasirinkite **Praleisti šį veiksmą** ir pereikite prie suvestinės puslapio.</span><span class="sxs-lookup"><span data-stu-id="7f6f2-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="7f6f2-141">[![Fokusavimo režimas su filtrais](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="7f6f2-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
