---
title: Faktinis likęs kiekis, nurodytas vienetais, negali būti lygus nuliui
description: Kai generuojate važtaraštį, į jį pateikiami duomenys turi ne nulinį atsargų kiekį, bet nulinį pardavimų kiekį.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248794"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="06b74-103">Faktinis likęs kiekis, nurodytas vienetais, negali būti lygus nuliui</span><span class="sxs-lookup"><span data-stu-id="06b74-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="06b74-104">Klaidos kodas: SYS19591</span><span class="sxs-lookup"><span data-stu-id="06b74-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="06b74-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="06b74-105">Symptoms</span></span>

<span data-ttu-id="06b74-106">Kai generuojate važtaraštį, į jį pateikiami duomenys turi ne nulinį atsargų kiekį, bet nulinį pardavimų kiekį.</span><span class="sxs-lookup"><span data-stu-id="06b74-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="06b74-107">Kai bandote sugeneruoti važtaraštį, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="06b74-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="06b74-108">Faktinis likęs kiekis, išreikštas vienetu %1, negali būti lygus nuliui.</span><span class="sxs-lookup"><span data-stu-id="06b74-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="06b74-109">Todėl negalite sugeneruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="06b74-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="06b74-110">Priežastis</span><span class="sxs-lookup"><span data-stu-id="06b74-110">Cause</span></span>

<span data-ttu-id="06b74-111">Sistema įvertina faktiškai likusį kiekį atsargų vienetu ir faktiškai likusį kiekį siuntimo vienetu.</span><span class="sxs-lookup"><span data-stu-id="06b74-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="06b74-112">Jei sistema nustato, kad faktinis likęs kiekis siuntimo vienetu yra 0 (nulis), bet faktinis likęs kiekis atsargų vienetu nėra 0, negalite sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="06b74-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="06b74-113">Pavyzdžiui, ši problema gali kilti, jei prekės pardavimo ir atsargų vienetai skiriasi, o konvertavimas tarp vienetų nėra tikslus.</span><span class="sxs-lookup"><span data-stu-id="06b74-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="06b74-114">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="06b74-114">Resolution</span></span>

<span data-ttu-id="06b74-115">Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas.</span><span class="sxs-lookup"><span data-stu-id="06b74-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="06b74-116">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="06b74-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="06b74-117">Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="06b74-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="06b74-118">Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be apvalinimo problemų.</span><span class="sxs-lookup"><span data-stu-id="06b74-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="06b74-119">Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.</span><span class="sxs-lookup"><span data-stu-id="06b74-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="06b74-120">Įsitikinkite, kad atsargų matavimo vienetas yra mažesnis nei pardavimų matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="06b74-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="06b74-121">Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka</span><span class="sxs-lookup"><span data-stu-id="06b74-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="06b74-122">Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="06b74-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="06b74-123">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="06b74-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="06b74-124">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="06b74-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="06b74-125">„FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="06b74-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="06b74-126">Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.</span><span class="sxs-lookup"><span data-stu-id="06b74-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="06b74-127">Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="06b74-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="06b74-128">Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.</span><span class="sxs-lookup"><span data-stu-id="06b74-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="06b74-129">Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="06b74-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="06b74-130">Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be apvalinimo problemų</span><span class="sxs-lookup"><span data-stu-id="06b74-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="06b74-131">Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte savo krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be apvalinimo problemų.</span><span class="sxs-lookup"><span data-stu-id="06b74-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="06b74-132">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="06b74-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="06b74-133">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="06b74-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="06b74-134">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="06b74-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="06b74-135">Skirtuke  **Krovinio eilutės** pasirinkite prekės, viršijančios pristatymo perviršį, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="06b74-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="06b74-136">Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="06b74-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="06b74-137">Skirtuke  **Eilutės informacija** pasirinkite **Užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="06b74-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="06b74-138">Nustatykite **Kiekio** lauką į paimtą kiekį (tai yra, į lauko **Darbo sukurto kiekio** reikšmę), kad būtų galima atlikti važtaraščio generavimą.</span><span class="sxs-lookup"><span data-stu-id="06b74-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="06b74-139">Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu</span><span class="sxs-lookup"><span data-stu-id="06b74-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="06b74-140">Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.</span><span class="sxs-lookup"><span data-stu-id="06b74-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="06b74-141">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="06b74-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="06b74-142">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="06b74-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="06b74-143">„FastTab” **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="06b74-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="06b74-144">Pasižymėkite laukų **Kiekis** ir **Vienetas** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="06b74-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="06b74-145">Eikite į **Organizacijos administravimas \> Vienetai \> Vienetai**.</span><span class="sxs-lookup"><span data-stu-id="06b74-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="06b74-146">Pasirinkite vienetą, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="06b74-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="06b74-147">Pakoreguokite lauko **Dešimtainis tikslumas** reikšmę, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="06b74-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="06b74-148">Įsitikinkite, kad atsargų matavimo vienetas yra mažesnis nei pardavimų matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="06b74-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="06b74-149">Įsitikinkite, kad atsargų matavimo vienetas yra mažesnis nei pardavimų matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="06b74-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="06b74-150">Jei reikia, apsvarstykite galimybę iš naujo sukonfigūruoti prekės matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="06b74-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
