---
title: Įrašyti prekių gavimą pirkimo užsakyme
description: Šioje procedūroje parodoma, kaip prekių gavimą registruoti tiesiogiai pirkimo užsakyme.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "343218"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="9eecb-103">Įrašyti prekių gavimą pirkimo užsakyme</span><span class="sxs-lookup"><span data-stu-id="9eecb-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9eecb-104">Šioje procedūroje parodoma, kaip prekių gavimą registruoti tiesiogiai pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="9eecb-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="9eecb-105">Taip pat produktų gavimą galima registruoti sandėlyje ir vėliau tai įrašyti pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="9eecb-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="9eecb-106">Šią užduotį paprastai atlieka pirkimo agentas arba mokėtinų sumų koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="9eecb-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="9eecb-107">Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="9eecb-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="9eecb-108">Pavyzdys apima veiksmus, skirtus paprastam pirkimo užsakymui kurti, kad procedūrą būtų galima paleisti kaip užduočių vedlį.</span><span class="sxs-lookup"><span data-stu-id="9eecb-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="9eecb-109">Jei atlikdami procedūrą naudojote savo duomenis, pradėkite nuo antrinės užduoties Įrašyti prekių gavimą.</span><span class="sxs-lookup"><span data-stu-id="9eecb-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="9eecb-110">Naujo prekių gavimo pirkimo užsakymo ruošimas</span><span class="sxs-lookup"><span data-stu-id="9eecb-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="9eecb-111">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="9eecb-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9eecb-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9eecb-112">Click New.</span></span>
3. <span data-ttu-id="9eecb-113">Lauke Tiekėjo kodas įveskite US-101.</span><span class="sxs-lookup"><span data-stu-id="9eecb-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="9eecb-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9eecb-114">Click OK.</span></span>
5. <span data-ttu-id="9eecb-115">Lauke Prekės numeris įveskite M0001.</span><span class="sxs-lookup"><span data-stu-id="9eecb-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="9eecb-116">Lauke Kiekis įveskite 5.</span><span class="sxs-lookup"><span data-stu-id="9eecb-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="9eecb-117">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="9eecb-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="9eecb-118">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="9eecb-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="9eecb-119">Įrašyti prekių gavimą</span><span class="sxs-lookup"><span data-stu-id="9eecb-119">Record receipt of goods</span></span>
1. <span data-ttu-id="9eecb-120">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="9eecb-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="9eecb-121">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="9eecb-121">Click Product receipt.</span></span>
    * <span data-ttu-id="9eecb-122">Lauke Kiekis galima pasirinkti skirtingas kiekio, kurį norite gauti, parinktis.</span><span class="sxs-lookup"><span data-stu-id="9eecb-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="9eecb-123">Pavyzdžiui, jei kiekis buvo anksčiau užregistruotas sandėlyje, galite pasirinkti Užregistruotas kiekis.</span><span class="sxs-lookup"><span data-stu-id="9eecb-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="9eecb-124">Pavyzdžiui, naudokite reikšmę Užsakytas kiekis.</span><span class="sxs-lookup"><span data-stu-id="9eecb-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="9eecb-125">Lauke Produkto gavimo kvitas įveskite bet kokią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9eecb-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="9eecb-126">Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.</span><span class="sxs-lookup"><span data-stu-id="9eecb-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="9eecb-127">Išplėskite dalį Eilutės.</span><span class="sxs-lookup"><span data-stu-id="9eecb-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="9eecb-128">Nustatykite kiekį – 4.</span><span class="sxs-lookup"><span data-stu-id="9eecb-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="9eecb-129">Čia galite patys nurodyti kiekvienos užsakymo eilutės gaunamą kiekį.</span><span class="sxs-lookup"><span data-stu-id="9eecb-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="9eecb-130">Sutraukite sekciją Eilutės.</span><span class="sxs-lookup"><span data-stu-id="9eecb-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="9eecb-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9eecb-131">Click OK.</span></span>
    * <span data-ttu-id="9eecb-132">Dabar pirkimo užsakyme prekės užregistruotos kaip gautos, o tai atsispindi sukurtame produktų gavimo kvitų žurnale.</span><span class="sxs-lookup"><span data-stu-id="9eecb-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="9eecb-133">Galite naudoti veiksmą Produkto gavimo kvitas, norėdami peržiūrėti žurnalus, sukurtus su pirkimo užsakymu, ir sužinoti, kas ir kada buvo gauta.</span><span class="sxs-lookup"><span data-stu-id="9eecb-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

