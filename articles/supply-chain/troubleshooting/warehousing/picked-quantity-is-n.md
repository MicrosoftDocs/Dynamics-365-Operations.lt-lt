---
title: Paimtas kiekis yra nepakankamas važtaraščio generavimo metu
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra paimtas kiekis, neatitinkantis sukurto darbo kiekio krovinio eilutėje.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249144"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="01ab0-103">Paimtas kiekis yra nepakankamas važtaraščio generavimo metu</span><span class="sxs-lookup"><span data-stu-id="01ab0-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="01ab0-104">Klaidos kodas: SYS54073</span><span class="sxs-lookup"><span data-stu-id="01ab0-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="01ab0-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="01ab0-105">Symptoms</span></span>

<span data-ttu-id="01ab0-106">Kai generuojate važtaraštį, siunčiamame krovinyje yra paimtas kiekis, neatitinkantis sukurto darbo kiekio krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="01ab0-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="01ab0-107">Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="01ab0-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="01ab0-108">Kadangi %1 yra paimta, nepakanka atnaujinti %2, kai vėliau likutis turi būti %3.</span><span class="sxs-lookup"><span data-stu-id="01ab0-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="01ab0-109">Todėl negalite sugeneruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="01ab0-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="01ab0-110">Priežastis</span><span class="sxs-lookup"><span data-stu-id="01ab0-110">Cause</span></span>

<span data-ttu-id="01ab0-111">Važtaraščio negalima sugeneruoti dabartinėje būsenoje, nes gali egzistuoti viena iš šių sąlygų:</span><span class="sxs-lookup"><span data-stu-id="01ab0-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="01ab0-112">Susijęs darbas dar neparinktas ir perkeltas į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="01ab0-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="01ab0-113">Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="01ab0-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="01ab0-114">Krovinio eilutės kiekis, sukurto darbo kiekis ir paimtas kiekis nesutampa.</span><span class="sxs-lookup"><span data-stu-id="01ab0-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="01ab0-115">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="01ab0-115">Resolution</span></span>

<span data-ttu-id="01ab0-116">Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas.</span><span class="sxs-lookup"><span data-stu-id="01ab0-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="01ab0-117">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="01ab0-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="01ab0-118">Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="01ab0-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="01ab0-119">Pakoreguokite krovinio eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="01ab0-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="01ab0-120">Atšaukite visas paėmimo registracijas ir perdarykite paėmimą.</span><span class="sxs-lookup"><span data-stu-id="01ab0-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="01ab0-121">Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka</span><span class="sxs-lookup"><span data-stu-id="01ab0-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="01ab0-122">Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="01ab0-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="01ab0-123">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="01ab0-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="01ab0-124">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="01ab0-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="01ab0-125">„FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="01ab0-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="01ab0-126">Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.</span><span class="sxs-lookup"><span data-stu-id="01ab0-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="01ab0-127">Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="01ab0-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="01ab0-128">Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.</span><span class="sxs-lookup"><span data-stu-id="01ab0-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="01ab0-129">Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="01ab0-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="01ab0-130">Krovinio eilutės kiekio koregavimas</span><span class="sxs-lookup"><span data-stu-id="01ab0-130">Adjust the load line quantity</span></span>

<span data-ttu-id="01ab0-131">Norėdami pakoreguoti krovinio eilutės kiekį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="01ab0-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="01ab0-132">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="01ab0-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="01ab0-133">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="01ab0-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="01ab0-134">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="01ab0-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="01ab0-135">Skirtuke  **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="01ab0-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="01ab0-136">Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="01ab0-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="01ab0-137">Nustatykite **Sumažinti krovinio eilutę** lauką, kad koregavimai atsispindėtų krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="01ab0-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="01ab0-138">Atšaukite visas paėmimo registracijas ir perdarykite paėmimą</span><span class="sxs-lookup"><span data-stu-id="01ab0-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="01ab0-139">Problema gali kilti dėl to, kad kažkas panaudojo paėmimo registraciją uždaryti krovinio eilutei be darbo.</span><span class="sxs-lookup"><span data-stu-id="01ab0-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="01ab0-140">Tokiu atveju rankinio paėmimo registravimas turi būti atšauktas, o paėmimas turi būti baigtas naudojant „Warehouse Management Mobile App”.</span><span class="sxs-lookup"><span data-stu-id="01ab0-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="01ab0-141">Norėdami atšaukti paėmimo registravimą, naudokite toliau pateiktą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="01ab0-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="01ab0-142">Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="01ab0-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="01ab0-143">Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="01ab0-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="01ab0-144">Skirtuke  **Pardavimo užsakymo eilutės** pasirinkite pardavimo užsakymo eilutę, kuriai buvo atliktas paėmimo registravimas.</span><span class="sxs-lookup"><span data-stu-id="01ab0-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="01ab0-145">Pasirinkite **Atnaujinti eilutę \> Paėmimas**, jei norite atsisakyti prekių paėmimo.</span><span class="sxs-lookup"><span data-stu-id="01ab0-145">Select **Update line \> Pick** to unpick the items.</span></span>
