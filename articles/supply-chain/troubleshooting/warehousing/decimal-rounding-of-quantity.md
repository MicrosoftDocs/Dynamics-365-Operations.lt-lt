---
title: Faktiškai atnaujinamo kiekio dešimtainis apvalinimas yra neteisingas
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, neatitinkantis vienete apibrėžto dešimtainio tikslumo.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248795"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="1e2e6-103">Faktiškai atnaujinamo kiekio dešimtainis apvalinimas yra neteisingas</span><span class="sxs-lookup"><span data-stu-id="1e2e6-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="1e2e6-104">Klaidos kodas: SYS19589</span><span class="sxs-lookup"><span data-stu-id="1e2e6-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="1e2e6-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="1e2e6-105">Symptoms</span></span>

<span data-ttu-id="1e2e6-106">Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, neatitinkantis vienete apibrėžto dešimtainio tikslumo.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="1e2e6-107">Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="1e2e6-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="1e2e6-108">Neteisingas faktiškai atnaujinamo kiekio, išreikšto vienetu %1, dešimtainis apvalinimas.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="1e2e6-109">Todėl negalite sugeneruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="1e2e6-110">Priežastis</span><span class="sxs-lookup"><span data-stu-id="1e2e6-110">Cause</span></span>

<span data-ttu-id="1e2e6-111">Sistema įvertina, ar siuntimo kiekio dešimtainis apvalinimas atitinka dešimtainį tikslumą, apibrėžtą siuntimo vienetui.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="1e2e6-112">Kai sistema suapvalina siuntimo kiekį iki nurodyto dešimtainio kablelio skaičiaus, jeigu ji nustato, kad suapvalintas siuntimo kiekis neatitinka faktinio siuntimo kiekio, važtaraščio sugeneruoti negalite.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="1e2e6-113">Pavyzdžiui, ši problema gali kilti, jei pardavimo kiekis yra 1,75 kilogramo (kg), bet dešimtainis tikslumas nustatytas į *1*.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="1e2e6-114">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="1e2e6-114">Resolution</span></span>

<span data-ttu-id="1e2e6-115">Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="1e2e6-116">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="1e2e6-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="1e2e6-117">Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be dešimtainių skaičių ir kitų apvalinimo problemų.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="1e2e6-118">Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="1e2e6-119">Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be dešimtainių skaičių ir kitų apvalinimo problemų</span><span class="sxs-lookup"><span data-stu-id="1e2e6-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="1e2e6-120">Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte savo krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be dešimtainių skaičių ir kitų apvalinimo problemų.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="1e2e6-121">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1e2e6-122">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1e2e6-123">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="1e2e6-124">Skirtuke  **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="1e2e6-125">Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="1e2e6-126">Skirtuke  **Eilutės informacija** pasirinkite **Užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="1e2e6-127">Nustatykite **Kiekio** lauką į paimtą kiekį (tai yra, į lauko **Darbo sukurto kiekio** reikšmę), kad būtų galima atlikti važtaraščio generavimą.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="1e2e6-128">Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu</span><span class="sxs-lookup"><span data-stu-id="1e2e6-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="1e2e6-129">Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="1e2e6-130">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1e2e6-131">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1e2e6-132">„FastTab” **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="1e2e6-133">Pasižymėkite laukų **Kiekis** ir **Vienetas** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="1e2e6-134">Eikite į **Organizacijos administravimas \> Vienetai \> Vienetai**.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="1e2e6-135">Pasirinkite vienetą, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1e2e6-136">Pakoreguokite lauko **Dešimtainis tikslumas** reikšmę, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="1e2e6-136">Adjust the value of the **Decimal precision** field as required.</span></span>
