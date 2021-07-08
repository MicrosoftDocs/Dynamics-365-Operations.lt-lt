---
title: Kiekis viršija pristatymo perviršio procentą važtaraščio kūrimo metu
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo perviršio procentą.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249142"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="e7337-103">Kiekis viršija pristatymo perviršio procentą važtaraščio kūrimo metu</span><span class="sxs-lookup"><span data-stu-id="e7337-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="e7337-104">Klaidos kodas: SYS24920</span><span class="sxs-lookup"><span data-stu-id="e7337-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="e7337-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="e7337-105">Symptoms</span></span>

<span data-ttu-id="e7337-106">Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo perviršio procentą.</span><span class="sxs-lookup"><span data-stu-id="e7337-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="e7337-107">Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="e7337-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="e7337-108">Eilutės pristatymo perteklius yra %1 procentai, o leistinas pristatymo perteklius yra tik %2 procentai.</span><span class="sxs-lookup"><span data-stu-id="e7337-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="e7337-109">Todėl negalite sugeneruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="e7337-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e7337-110">Priežastis</span><span class="sxs-lookup"><span data-stu-id="e7337-110">Cause</span></span>

<span data-ttu-id="e7337-111">Paimtas krovinio arba siuntos kiekis yra didesnis nei užsakytas kiekis ir nėra pristatymo perviršio procento diapazone.</span><span class="sxs-lookup"><span data-stu-id="e7337-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="e7337-112">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="e7337-112">Resolution</span></span>

<span data-ttu-id="e7337-113">Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas.</span><span class="sxs-lookup"><span data-stu-id="e7337-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="e7337-114">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="e7337-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="e7337-115">Pakoreguokite krovinio eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="e7337-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="e7337-116">Pakoreguokite pristatymo perviršio procentą.</span><span class="sxs-lookup"><span data-stu-id="e7337-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="e7337-117">Atšaukite ir atlikite koregavimus.</span><span class="sxs-lookup"><span data-stu-id="e7337-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="e7337-118">Krovinio eilutės kiekio koregavimas</span><span class="sxs-lookup"><span data-stu-id="e7337-118">Adjust the load line quantity</span></span>

<span data-ttu-id="e7337-119">Norėdami pakoreguoti krovinio eilutės kiekį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="e7337-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="e7337-120">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="e7337-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e7337-121">Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="e7337-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="e7337-122">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="e7337-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="e7337-123">Skirtuke  **Krovinio eilutės** pasirinkite prekės, viršijančios pristatymo perviršio procentą, krovinio eilutę.</span><span class="sxs-lookup"><span data-stu-id="e7337-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="e7337-124">Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="e7337-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="e7337-125">Skirtuke  **Eilutės informacija** pasirinkite **Užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="e7337-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="e7337-126">Nustatykite **Kiekio** lauką į paimtą kiekį (tai yra, į lauko **Darbo sukurto kiekio** reikšmę), kad būtų galima atlikti važtaraščio generavimą.</span><span class="sxs-lookup"><span data-stu-id="e7337-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="e7337-127">Pristatymo perviršio procento koregavimas</span><span class="sxs-lookup"><span data-stu-id="e7337-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="e7337-128">Norėdami pakoreguoti pristatymo perviršio procentą, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="e7337-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="e7337-129">Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="e7337-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="e7337-130">Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="e7337-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="e7337-131">Skirtuke  **Pardavimo užsakymo eilutės** pasirinkite prekės, viršijančios pristatymo perviršio procentą, pardavimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="e7337-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="e7337-132">Skirtuke  **Eilutės informacija** pasirinkite **Pristatymas**.</span><span class="sxs-lookup"><span data-stu-id="e7337-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="e7337-133">Nustatykite lauką **Perviršis** į didesnį procentą, sutalpinantį pagal krovinio kiekį paimtą kiekį, kad būtų galima atlikti važtaraščio generavimą.</span><span class="sxs-lookup"><span data-stu-id="e7337-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="e7337-134">Atšaukimas ir koregavimų atlikimas</span><span class="sxs-lookup"><span data-stu-id="e7337-134">Reverse and make adjustments</span></span>

<span data-ttu-id="e7337-135">Atšaukite viską, kas buvo užregistruota kroviniui (pavyzdžiui, važtaraštį, siuntos patvirtinimą ir darbą), atlikite pardavimo užsakymo koregavimus, iš naujo paleiskite užsakymą į sandėlį ir pabaikite siuntimo procedūrą.</span><span class="sxs-lookup"><span data-stu-id="e7337-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="e7337-136">Norėdami atšaukti važtaraštį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="e7337-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="e7337-137">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="e7337-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e7337-138">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti važtaraščius**.</span><span class="sxs-lookup"><span data-stu-id="e7337-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="e7337-139">Naudokite šią procedūrą norėdami atšaukti siuntos patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="e7337-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="e7337-140">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="e7337-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e7337-141">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="e7337-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="e7337-142">Norėdami atšaukti darbą naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="e7337-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="e7337-143">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="e7337-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e7337-144">Veiksmų juostos skirtuke  **Kroviniai**, grupėje  **Darbas** pasirinkite  **Atšaukti darbą**.</span><span class="sxs-lookup"><span data-stu-id="e7337-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
