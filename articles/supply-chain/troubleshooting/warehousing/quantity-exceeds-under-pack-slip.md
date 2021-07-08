---
title: Kiekis viršija pristatymo trūkumo procentą važtaraščio kūrimo metu
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo trūkumo procentą.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249140"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="a50df-103">Kiekis viršija pristatymo trūkumo procentą važtaraščio kūrimo metu</span><span class="sxs-lookup"><span data-stu-id="a50df-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="a50df-104">Klaidos kodas: SYS24921</span><span class="sxs-lookup"><span data-stu-id="a50df-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="a50df-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="a50df-105">Symptoms</span></span>

<span data-ttu-id="a50df-106">Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo trūkumo procentą.</span><span class="sxs-lookup"><span data-stu-id="a50df-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="a50df-107">Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="a50df-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="a50df-108">Eilutės pristatymo trūkumas yra %1 procentai, o leistinas pristatymo trūkumas yra tik %2 procentai.</span><span class="sxs-lookup"><span data-stu-id="a50df-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="a50df-109">Todėl negalite sugeneruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="a50df-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a50df-110">Priežastis</span><span class="sxs-lookup"><span data-stu-id="a50df-110">Cause</span></span>

<span data-ttu-id="a50df-111">Paimtas krovinio arba siuntos kiekis yra mažesnis nei užsakytas kiekis ir nėra pristatymo trūkumo procento diapazone.</span><span class="sxs-lookup"><span data-stu-id="a50df-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="a50df-112">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="a50df-112">Resolution</span></span>

<span data-ttu-id="a50df-113">Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas.</span><span class="sxs-lookup"><span data-stu-id="a50df-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="a50df-114">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="a50df-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="a50df-115">Pakoreguokite perviršio trūkumo procentą.</span><span class="sxs-lookup"><span data-stu-id="a50df-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="a50df-116">Atšaukite ir atlikite koregavimus.</span><span class="sxs-lookup"><span data-stu-id="a50df-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="a50df-117">Perviršio trūkumo procento koregavimas</span><span class="sxs-lookup"><span data-stu-id="a50df-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="a50df-118">Norėdami pakoreguoti pristatymo trūkumo procentą, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="a50df-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="a50df-119">Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a50df-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="a50df-120">Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="a50df-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="a50df-121">Skirtuke  **Pardavimo užsakymo eilutės** pasirinkite prekės, viršijančios pristatymo trūkumo procentą, pardavimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="a50df-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="a50df-122">Skirtuke  **Eilutės informacija** pasirinkite **Pristatymas**.</span><span class="sxs-lookup"><span data-stu-id="a50df-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="a50df-123">Nustatykite lauką **Pristatymo trūkumas** į didesnį procentą, sutalpinantį pagal krovinio kiekį paimtą kiekį, kad būtų galima atlikti važtaraščio generavimą.</span><span class="sxs-lookup"><span data-stu-id="a50df-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="a50df-124">Atšaukimas ir koregavimų atlikimas</span><span class="sxs-lookup"><span data-stu-id="a50df-124">Reverse and make adjustments</span></span>

<span data-ttu-id="a50df-125">Atšaukite viską, kas buvo užregistruota kroviniui (pavyzdžiui, važtaraštį, siuntos patvirtinimą ir darbą), atlikite pardavimo užsakymo koregavimus, iš naujo paleiskite užsakymą į sandėlį ir pabaikite siuntimo procedūrą.</span><span class="sxs-lookup"><span data-stu-id="a50df-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="a50df-126">Norėdami atšaukti važtaraštį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="a50df-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="a50df-127">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="a50df-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a50df-128">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti važtaraščius**.</span><span class="sxs-lookup"><span data-stu-id="a50df-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="a50df-129">Naudokite šią procedūrą norėdami atšaukti siuntos patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="a50df-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="a50df-130">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="a50df-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a50df-131">Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="a50df-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="a50df-132">Norėdami atšaukti darbą naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="a50df-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="a50df-133">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="a50df-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a50df-134">Veiksmų juostos skirtuke  **Kroviniai**, grupėje  **Darbas** pasirinkite  **Atšaukti darbą**.</span><span class="sxs-lookup"><span data-stu-id="a50df-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
