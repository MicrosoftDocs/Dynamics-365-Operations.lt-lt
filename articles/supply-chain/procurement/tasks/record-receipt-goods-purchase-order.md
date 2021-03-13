---
title: Prekių gavimo įrašymas pirkimo užsakyme
description: Šioje temoje aprašoma, kaip įrašyti prekių gavimą tiesiogiai pirkimo užsakyme.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d016df08850c75858c50b7f9a97b11b566d26cb0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022663"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="071a5-103">Prekių gavimo įrašymas pirkimo užsakyme</span><span class="sxs-lookup"><span data-stu-id="071a5-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="071a5-104">Šioje temoje aprašoma, kaip įrašyti prekių gavimą tiesiogiai pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="071a5-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="071a5-105">Taip pat produktų gavimą galima registruoti sandėlyje ir vėliau tai įrašyti pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="071a5-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="071a5-106">Šią užduotį paprastai atlieka pirkimo agentas arba mokėtinų sumų koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="071a5-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="071a5-107">Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="071a5-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="071a5-108">Pavyzdys apima veiksmus, skirtus paprastam pirkimo užsakymui kurti, kad procedūrą būtų galima paleisti kaip užduočių vedlį.</span><span class="sxs-lookup"><span data-stu-id="071a5-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="071a5-109">Jei atlikdami procedūrą naudojote savo duomenis, pradėkite nuo antrinės užduoties **Įrašyti prekių gavimą**.</span><span class="sxs-lookup"><span data-stu-id="071a5-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="071a5-110">Naujo prekių gavimo pirkimo užsakymo ruošimas</span><span class="sxs-lookup"><span data-stu-id="071a5-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="071a5-111">Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="071a5-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="071a5-112">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="071a5-112">Select **New**.</span></span>
3. <span data-ttu-id="071a5-113">Lauke **„Tiekėjo paskyra“** įveskite „`US-101`“.</span><span class="sxs-lookup"><span data-stu-id="071a5-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="071a5-114">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="071a5-114">Select **OK**.</span></span>
5. <span data-ttu-id="071a5-115">Lauke **„Prekės numeris“** įveskite „`M0001`“.</span><span class="sxs-lookup"><span data-stu-id="071a5-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="071a5-116">Lauke **„Kiekis“** įveskite „`5`“.</span><span class="sxs-lookup"><span data-stu-id="071a5-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="071a5-117">Veiksmų srityje pasirinkite **Pirkimas**.</span><span class="sxs-lookup"><span data-stu-id="071a5-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="071a5-118">Pasirinkite **„Patvirtinti“**.</span><span class="sxs-lookup"><span data-stu-id="071a5-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="071a5-119">Įrašyti prekių gavimą</span><span class="sxs-lookup"><span data-stu-id="071a5-119">Record receipt of goods</span></span>
1. <span data-ttu-id="071a5-120">Veiksmų srityje pasirinkite **„Gauti“**.</span><span class="sxs-lookup"><span data-stu-id="071a5-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="071a5-121">Pasirinkite **„Produkto gavimo kvitas“**.</span><span class="sxs-lookup"><span data-stu-id="071a5-121">Select **Product receipt**.</span></span> <span data-ttu-id="071a5-122">Lauke **Kiekis** galima pasirinkti skirtingas kiekio, kurį norite gauti, parinktis.</span><span class="sxs-lookup"><span data-stu-id="071a5-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="071a5-123">Pavyzdžiui, jei kiekis buvo anksčiau užregistruotas sandėlyje, galite pasirinkti **Užregistruotas kiekis**.</span><span class="sxs-lookup"><span data-stu-id="071a5-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="071a5-124">Pavyzdžiui, naudokite reikšmę **Užsakytas kiekis**.</span><span class="sxs-lookup"><span data-stu-id="071a5-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="071a5-125">Išplėskite **Peržiūra** skyrių.</span><span class="sxs-lookup"><span data-stu-id="071a5-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="071a5-126">Lauke **Produkto gavimo kvitas** įveskite bet kurią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a5-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="071a5-127">Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.</span><span class="sxs-lookup"><span data-stu-id="071a5-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="071a5-128">Išplėskite skyrių **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="071a5-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="071a5-129">Nustatykite **Kiekis** lauke „4“.</span><span class="sxs-lookup"><span data-stu-id="071a5-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="071a5-130">Čia galite patys nurodyti kiekvienos užsakymo eilutės gaunamą kiekį.</span><span class="sxs-lookup"><span data-stu-id="071a5-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="071a5-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="071a5-131">Select **OK**.</span></span> <span data-ttu-id="071a5-132">Dabar pirkimo užsakyme prekės užregistruotos kaip gautos, o tai atsispindi sukurtame produktų gavimo kvitų žurnale.</span><span class="sxs-lookup"><span data-stu-id="071a5-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="071a5-133">Galite naudoti veiksmą Produkto gavimo kvitas, norėdami peržiūrėti žurnalus, sukurtus su pirkimo užsakymu, ir sužinoti, kas ir kada buvo gauta.</span><span class="sxs-lookup"><span data-stu-id="071a5-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

