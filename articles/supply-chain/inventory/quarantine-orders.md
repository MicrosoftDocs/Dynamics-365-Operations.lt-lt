---
title: Sulaikymo užsakymai
description: Šioje temoje aprašoma, kaip, naudojant sulaikymo užsakymus, galima blokuoti atsargas.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570477"
---
# <a name="quarantine-orders"></a><span data-ttu-id="2505b-103">Sulaikymo užsakymai</span><span class="sxs-lookup"><span data-stu-id="2505b-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2505b-104">Šioje temoje aprašoma, kaip, naudojant sulaikymo užsakymus, galima blokuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="2505b-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="2505b-105">Naudojant sulaikymo užsakymus galima blokuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="2505b-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="2505b-106">Pavyzdžiui, galbūt sulaikyti prekes norėsite kokybės kontrolės tikslais.</span><span class="sxs-lookup"><span data-stu-id="2505b-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="2505b-107">Sulaikytos atsargos perkeliamos į sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="2505b-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="2505b-108">**Pastaba.** Jei naudojate patobulinto sandėlio valdymo procesus (modulyje Sandėlio valdymas), sulaikymo užsakymų apdorojimo funkcija naudojama tik su grąžinimo pardavimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="2505b-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="2505b-109">Turimų atsargų prekių sulaikymas</span><span class="sxs-lookup"><span data-stu-id="2505b-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="2505b-110">Kai sulaikote prekes, galite sulaikymo užsakymus kurti patys arba nustatyti sistemą, kad ji automatiškai kurtų sulaikymo užsakymus vykdant gavimo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="2505b-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="2505b-111">Norėdami sulaikymo užsakymus kurti automatiškai, puslapio **Prekių modelių grupės** skirtuke **Atsargų strategijos** pasirinkite parinktį **Sulaikymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="2505b-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="2505b-112">Taip pat gavimo sandėlių lauke **Sulaikymo sandėlis** reikia nurodyti numatytąjį sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="2505b-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="2505b-113">Kai faktiškai turimos atsargos įrašomos pirkimo užsakyme arba gamybos užsakyme, programoje „Microsoft Dynamics 365 for Finance and Operations“ sulaikytos prekės automatiškai perkeliamos į sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="2505b-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2505b-114">Perkeliama, nes sulaikymo užsakymo būsena pakeičiama į **Pradėtas**.</span><span class="sxs-lookup"><span data-stu-id="2505b-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="2505b-115">Kai patys kuriate sulaikymo užsakymus, nėra būtina nustatyti dabartinės prekės sulaikymo valdymo susietoje prekių modelių grupėje.</span><span class="sxs-lookup"><span data-stu-id="2505b-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="2505b-116">Norėdami vykdyti šį procesą, turite nurodyti sulaikytinas turimas atsargas ir naudotiną sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="2505b-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="2505b-117">Planuoti šį procesą jums padės sulaikymo užsakymų būsenos.</span><span class="sxs-lookup"><span data-stu-id="2505b-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="2505b-118">Sulaikymo užsakymų būsenos</span><span class="sxs-lookup"><span data-stu-id="2505b-118">Quarantine order statuses</span></span>
<span data-ttu-id="2505b-119">Sulaikymo užsakymų būsenos gali būti tokios:</span><span class="sxs-lookup"><span data-stu-id="2505b-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="2505b-120">Sukurta</span><span class="sxs-lookup"><span data-stu-id="2505b-120">Created</span></span>
-   <span data-ttu-id="2505b-121">Pradėta</span><span class="sxs-lookup"><span data-stu-id="2505b-121">Started</span></span>
-   <span data-ttu-id="2505b-122">Paskelbta baigtu</span><span class="sxs-lookup"><span data-stu-id="2505b-122">Reported as finished</span></span>
-   <span data-ttu-id="2505b-123">Baigta</span><span class="sxs-lookup"><span data-stu-id="2505b-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="2505b-124">Sukurta</span><span class="sxs-lookup"><span data-stu-id="2505b-124">Created</span></span>

<span data-ttu-id="2505b-125">Kai sulaikymo užsakymas sukurtas neautomatiniu būdu, bet prekė dar neperkelta į sulaikymo sandėlį, sulaikymo užsakymo būsena yra **Sukurtas**.</span><span class="sxs-lookup"><span data-stu-id="2505b-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="2505b-126">Sugeneruojamos dvi atsargų operacijos.</span><span class="sxs-lookup"><span data-stu-id="2505b-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="2505b-127">Viena operacija – tai išdavimo operacija, kurios būsena gali būti **Užsakyta**, **Rezervuota faktiškai** arba **Paimta**.</span><span class="sxs-lookup"><span data-stu-id="2505b-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="2505b-128">Kita operacija – tai gavimo operacija, kurios būsena sulaikymo sandėlyje gali būti **Užsakyta** arba **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="2505b-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="2505b-129">Galite rezervuoti, pasirinkti ir registruoti atsargų naujinimus naudodami įprastus procesus.</span><span class="sxs-lookup"><span data-stu-id="2505b-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="2505b-130">Pradėta</span><span class="sxs-lookup"><span data-stu-id="2505b-130">Started</span></span>

<span data-ttu-id="2505b-131">Kai sulaikymo užsakymo būsena yra **Pradėtas**, atsargos perkeliamos iš įprasto sandėlio į sulaikymo sandėlį ir sugeneruojamos dvi atsargų operacijos.</span><span class="sxs-lookup"><span data-stu-id="2505b-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="2505b-132">Vienos operacijos būsena yra **Išskaičiuota**, o kitos operacijos būsena yra **Gauta**.</span><span class="sxs-lookup"><span data-stu-id="2505b-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="2505b-133">Tuo pat metu sukuriamos dvi atsargų operacijos, tvarkančios grįžtamąjį perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="2505b-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="2505b-134">Šių operacijų datos nenurodytos.</span><span class="sxs-lookup"><span data-stu-id="2505b-134">These transactions aren't dated.</span></span> <span data-ttu-id="2505b-135">Vienos operacijos būsena yra **Rezervuota faktiškai**, o kitos operacijos būsena yra **Užsakyta**.</span><span class="sxs-lookup"><span data-stu-id="2505b-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="2505b-136">Paskelbta baigtu</span><span class="sxs-lookup"><span data-stu-id="2505b-136">Reported as finished</span></span>

<span data-ttu-id="2505b-137">Spustelėdami **Paskelbti baigtu**, galite paskelbti, kad pradėtas sulaikymo užsakymas baigtas.</span><span class="sxs-lookup"><span data-stu-id="2505b-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="2505b-138">Prekė nebėra sulaikoma, tačiau dar nėra perkeliama atgal į įprastą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="2505b-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="2505b-139">Perkėlimą atgal į įprastą sandėlį galima apdoroti naudojant žurnalą Prekių gavimas, kurį galima inicijuoti proceso Skelbti baigtu metu.</span><span class="sxs-lookup"><span data-stu-id="2505b-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="2505b-140">Baigta</span><span class="sxs-lookup"><span data-stu-id="2505b-140">Ended</span></span>

<span data-ttu-id="2505b-141">Pasibaigus sulaikymo užsakymui, prekė iš sulaikymo sandėlio perkeliama atgal į įprastą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="2505b-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="2505b-142">Prekės operacijos būsena sulaikymo sandėlyje nustatoma kaip **Parduota**, o įprastame sandėlyje – kaip **Nupirkta**.</span><span class="sxs-lookup"><span data-stu-id="2505b-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="2505b-143">Sulaikymo užsakymo nurašytas kiekis</span><span class="sxs-lookup"><span data-stu-id="2505b-143">Quarantine order scrap</span></span>
<span data-ttu-id="2505b-144">Sulaikymo užsakymo proceso metu galite nurašyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="2505b-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="2505b-145">Apdorojant nurašymą atsargų būsena bus nustatyta į **Parduotos** iš sulaikymo sandėlio naudojant išdavimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="2505b-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="2505b-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2505b-146">Additional resources</span></span>
--------

[<span data-ttu-id="2505b-147">Atsargų blokavimas</span><span class="sxs-lookup"><span data-stu-id="2505b-147">Inventory blocking</span></span>](inventory-blocking.md)
