---
title: Sulaikymo užsakymai
description: Šioje temoje aprašoma, kaip, naudojant sulaikymo užsakymus, galima blokuoti atsargas.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03a9004aae563959dd19276268b9f81aca4b0735
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011702"
---
# <a name="quarantine-orders"></a><span data-ttu-id="22313-103">Sulaikymo užsakymai</span><span class="sxs-lookup"><span data-stu-id="22313-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22313-104">Šioje temoje aprašoma, kaip, naudojant sulaikymo užsakymus, galima blokuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="22313-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="22313-105">Naudojant sulaikymo užsakymus galima blokuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="22313-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="22313-106">Pavyzdžiui, galbūt sulaikyti prekes norėsite kokybės kontrolės tikslais.</span><span class="sxs-lookup"><span data-stu-id="22313-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="22313-107">Sulaikytos atsargos perkeliamos į sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="22313-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="22313-108">**Pastaba.** Jei naudojate patobulinto sandėlio valdymo procesus (modulyje Sandėlio valdymas), sulaikymo užsakymų apdorojimo funkcija naudojama tik su grąžinimo pardavimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="22313-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="22313-109">Turimų atsargų prekių sulaikymas</span><span class="sxs-lookup"><span data-stu-id="22313-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="22313-110">Kai sulaikote prekes, galite sulaikymo užsakymus kurti patys arba nustatyti sistemą, kad ji automatiškai kurtų sulaikymo užsakymus vykdant gavimo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="22313-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="22313-111">Norėdami sulaikymo užsakymus kurti automatiškai, puslapio **Prekių modelių grupės** skirtuke **Atsargų strategijos** pasirinkite parinktį **Sulaikymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="22313-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="22313-112">Taip pat gavimo sandėlių lauke **Sulaikymo sandėlis** reikia nurodyti numatytąjį sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="22313-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="22313-113">Kai faktiškai turimos atsargos įrašomos pirkimo užsakyme arba gamybos užsakyme, Tiekimo grandinės valdyme sulaikytos prekės automatiškai perkeliamos į sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="22313-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Supply Chain Management.</span></span> <span data-ttu-id="22313-114">Perkeliama, nes sulaikymo užsakymo būsena pakeičiama į **Pradėtas**.</span><span class="sxs-lookup"><span data-stu-id="22313-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="22313-115">Kai patys kuriate sulaikymo užsakymus, nėra būtina nustatyti dabartinės prekės sulaikymo valdymo susietoje prekių modelių grupėje.</span><span class="sxs-lookup"><span data-stu-id="22313-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="22313-116">Norėdami vykdyti šį procesą, turite nurodyti sulaikytinas turimas atsargas ir naudotiną sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="22313-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="22313-117">Planuoti šį procesą jums padės sulaikymo užsakymų būsenos.</span><span class="sxs-lookup"><span data-stu-id="22313-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="22313-118">Sulaikymo užsakymų būsenos</span><span class="sxs-lookup"><span data-stu-id="22313-118">Quarantine order statuses</span></span>
<span data-ttu-id="22313-119">Sulaikymo užsakymų būsenos gali būti tokios:</span><span class="sxs-lookup"><span data-stu-id="22313-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="22313-120">Sukurta</span><span class="sxs-lookup"><span data-stu-id="22313-120">Created</span></span>
-   <span data-ttu-id="22313-121">Pradėta</span><span class="sxs-lookup"><span data-stu-id="22313-121">Started</span></span>
-   <span data-ttu-id="22313-122">Paskelbta baigtu</span><span class="sxs-lookup"><span data-stu-id="22313-122">Reported as finished</span></span>
-   <span data-ttu-id="22313-123">Baigta</span><span class="sxs-lookup"><span data-stu-id="22313-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="22313-124">Sukurta</span><span class="sxs-lookup"><span data-stu-id="22313-124">Created</span></span>

<span data-ttu-id="22313-125">Kai sulaikymo užsakymas sukurtas neautomatiniu būdu, bet prekė dar neperkelta į sulaikymo sandėlį, sulaikymo užsakymo būsena yra **Sukurtas**.</span><span class="sxs-lookup"><span data-stu-id="22313-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="22313-126">Sugeneruojamos dvi atsargų operacijos.</span><span class="sxs-lookup"><span data-stu-id="22313-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="22313-127">Viena operacija – tai išdavimo operacija, kurios būsena gali būti **Užsakyta**, **Rezervuota faktiškai** arba **Paimta**.</span><span class="sxs-lookup"><span data-stu-id="22313-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="22313-128">Kita operacija – tai gavimo operacija, kurios būsena sulaikymo sandėlyje gali būti **Užsakyta** arba **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="22313-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="22313-129">Galite rezervuoti, pasirinkti ir registruoti atsargų naujinimus naudodami įprastus procesus.</span><span class="sxs-lookup"><span data-stu-id="22313-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="22313-130">Pradėta</span><span class="sxs-lookup"><span data-stu-id="22313-130">Started</span></span>

<span data-ttu-id="22313-131">Kai sulaikymo užsakymo būsena yra **Pradėtas**, atsargos perkeliamos iš įprasto sandėlio į sulaikymo sandėlį ir sugeneruojamos dvi atsargų operacijos.</span><span class="sxs-lookup"><span data-stu-id="22313-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="22313-132">Vienos operacijos būsena yra **Išskaičiuota**, o kitos operacijos būsena yra **Gauta**.</span><span class="sxs-lookup"><span data-stu-id="22313-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="22313-133">Tuo pat metu sukuriamos dvi atsargų operacijos, tvarkančios grįžtamąjį perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="22313-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="22313-134">Šių operacijų datos nenurodytos.</span><span class="sxs-lookup"><span data-stu-id="22313-134">These transactions aren't dated.</span></span> <span data-ttu-id="22313-135">Vienos operacijos būsena yra **Rezervuota faktiškai**, o kitos operacijos būsena yra **Užsakyta**.</span><span class="sxs-lookup"><span data-stu-id="22313-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="22313-136">Paskelbta baigtu</span><span class="sxs-lookup"><span data-stu-id="22313-136">Reported as finished</span></span>

<span data-ttu-id="22313-137">Spustelėdami **Paskelbti baigtu**, galite paskelbti, kad pradėtas sulaikymo užsakymas baigtas.</span><span class="sxs-lookup"><span data-stu-id="22313-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="22313-138">Prekė nebėra sulaikoma, tačiau dar nėra perkeliama atgal į įprastą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="22313-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="22313-139">Perkėlimą atgal į įprastą sandėlį galima apdoroti naudojant žurnalą Prekių gavimas, kurį galima inicijuoti proceso Skelbti baigtu metu.</span><span class="sxs-lookup"><span data-stu-id="22313-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="22313-140">Baigta</span><span class="sxs-lookup"><span data-stu-id="22313-140">Ended</span></span>

<span data-ttu-id="22313-141">Pasibaigus sulaikymo užsakymui, prekė iš sulaikymo sandėlio perkeliama atgal į įprastą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="22313-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="22313-142">Prekės operacijos būsena sulaikymo sandėlyje nustatoma kaip **Parduota**, o įprastame sandėlyje – kaip **Nupirkta**.</span><span class="sxs-lookup"><span data-stu-id="22313-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="22313-143">Sulaikymo užsakymo nurašytas kiekis</span><span class="sxs-lookup"><span data-stu-id="22313-143">Quarantine order scrap</span></span>
<span data-ttu-id="22313-144">Sulaikymo užsakymo proceso metu galite nurašyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="22313-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="22313-145">Apdorojant nurašymą atsargų būsena bus nustatyta į **Parduotos** iš sulaikymo sandėlio naudojant išdavimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="22313-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="22313-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="22313-146">Additional resources</span></span>
--------

[<span data-ttu-id="22313-147">Atsargų blokavimas</span><span class="sxs-lookup"><span data-stu-id="22313-147">Inventory blocking</span></span>](inventory-blocking.md)
