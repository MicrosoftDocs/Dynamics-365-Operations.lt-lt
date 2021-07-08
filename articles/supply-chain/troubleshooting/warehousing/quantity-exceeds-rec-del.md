---
title: Kiekis, kurį bandote atnaujinti, viršija gautą/pristatytą kiekį.
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija darbo kiekį, kuris buvo paimtas ir rezervuotas pardavimo užsakymui.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249145"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="bde07-103">Kiekis, kurį bandote atnaujinti, viršija gautą/pristatytą kiekį</span><span class="sxs-lookup"><span data-stu-id="bde07-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="bde07-104">Klaidos kodas: SYS7676</span><span class="sxs-lookup"><span data-stu-id="bde07-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="bde07-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="bde07-105">Symptoms</span></span>

<span data-ttu-id="bde07-106">Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija darbo kiekį, kuris buvo paimtas ir rezervuotas pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="bde07-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="bde07-107">Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="bde07-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="bde07-108">Kiekis, kurį bandote atnaujinti, viršija gautą / pristatytą kiekį.</span><span class="sxs-lookup"><span data-stu-id="bde07-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="bde07-109">Todėl negalite sugeneruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="bde07-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="bde07-110">Priežastis</span><span class="sxs-lookup"><span data-stu-id="bde07-110">Cause</span></span>

<span data-ttu-id="bde07-111">Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bde07-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="bde07-112">Pavyzdžiui, ši problema gali kilti, jei krovinio eilutės kiekis, sukurto darbo kiekis arba paimtas kiekis nėra tikslus.</span><span class="sxs-lookup"><span data-stu-id="bde07-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="bde07-113">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="bde07-113">Resolution</span></span>

<span data-ttu-id="bde07-114">Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas.</span><span class="sxs-lookup"><span data-stu-id="bde07-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="bde07-115">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="bde07-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="bde07-116">Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="bde07-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="bde07-117">Pakoreguokite krovinio eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="bde07-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="bde07-118">Atšaukite visas paėmimo registracijas ir perdarykite paėmimą.</span><span class="sxs-lookup"><span data-stu-id="bde07-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="bde07-119">Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka</span><span class="sxs-lookup"><span data-stu-id="bde07-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="bde07-120">Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="bde07-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="bde07-121">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="bde07-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bde07-122">Pasirinkite krovinį, kuriam nepavyksta sugeneruoti siuntimo.</span><span class="sxs-lookup"><span data-stu-id="bde07-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="bde07-123">„FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="bde07-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="bde07-124">Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.</span><span class="sxs-lookup"><span data-stu-id="bde07-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="bde07-125">Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="bde07-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="bde07-126">Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.</span><span class="sxs-lookup"><span data-stu-id="bde07-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="bde07-127">Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="bde07-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="bde07-128">Krovinio eilutės kiekio koregavimas</span><span class="sxs-lookup"><span data-stu-id="bde07-128">Adjust the load line quantity</span></span>

<span data-ttu-id="bde07-129">Norėdami pakoreguoti krovinio eilutės kiekį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="bde07-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="bde07-130">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="bde07-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bde07-131">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="bde07-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="bde07-132">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="bde07-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="bde07-133">Skirtuke  **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="bde07-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="bde07-134">Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="bde07-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="bde07-135">Nustatykite **Sumažinti krovinio eilutę** lauką, kad koregavimai atsispindėtų krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bde07-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="bde07-136">Atšaukite visas paėmimo registracijas ir perdarykite paėmimą</span><span class="sxs-lookup"><span data-stu-id="bde07-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="bde07-137">Jei kas nors panaudojo paėmimo registraciją krovinio eilutei uždaryti be darbo, gali atsirasti neatitikimas tarp krovinio eilutės kiekio ir paimto kiekio.</span><span class="sxs-lookup"><span data-stu-id="bde07-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="bde07-138">Tokiu atveju rankinio paėmimo registravimas turi būti atšauktas, o paėmimas turi būti baigtas naudojant „Warehouse Management Mobile App”.</span><span class="sxs-lookup"><span data-stu-id="bde07-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="bde07-139">Norėdami atšaukti paėmimo registravimą, naudokite toliau pateiktą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="bde07-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="bde07-140">Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="bde07-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="bde07-141">Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="bde07-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="bde07-142">Skirtuke  **Pardavimo užsakymo eilutės** pasirinkite pardavimo užsakymo eilutę, kuriai buvo atliktas paėmimo registravimas.</span><span class="sxs-lookup"><span data-stu-id="bde07-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="bde07-143">Pasirinkite **Atnaujinti eilutę \> Paėmimas**, jei norite atsisakyti prekių paėmimo.</span><span class="sxs-lookup"><span data-stu-id="bde07-143">Select **Update line \> Pick** to unpick the items.</span></span>
