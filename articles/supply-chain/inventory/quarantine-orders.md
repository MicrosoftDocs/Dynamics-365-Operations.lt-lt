---
title: Sulaikymo užsakymai
description: Šioje temoje aprašoma, kaip, siekiant naudoti sulaikymo užsakymus, galima blokuoti atsargas.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956187"
---
# <a name="quarantine-orders"></a><span data-ttu-id="9ccc5-103">Sulaikymo užsakymai</span><span class="sxs-lookup"><span data-stu-id="9ccc5-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ccc5-104">Šioje temoje aprašoma, kaip, siekiant naudoti sulaikymo užsakymus, galima blokuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="9ccc5-105">Sulaikymo užsakymai leidžia užblokuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="9ccc5-106">Pavyzdžiui, galbūt sulaikyti prekes norėsite kokybės kontrolės tikslais.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="9ccc5-107">Sulaikytos atsargos perkeliamos į sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="9ccc5-108">Pastaba. Jei naudojate patobulinto sandėlio valdymo procesus (modulyje Sandėlio valdymas), sulaikymo užsakymų apdorojimo funkcija naudojama tik su grąžinimo pardavimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="9ccc5-109">Turimų atsargų prekių sulaikymas</span><span class="sxs-lookup"><span data-stu-id="9ccc5-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="9ccc5-110">Kai sulaikote prekes, galite sulaikymo užsakymus kurti rankiniu būdu arba nustatyti sistemą, kad ji automatiškai kurtų sulaikymo užsakymus vykdant gavimo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="9ccc5-111">Norėdami nustatyti sistemą automatiškai generuoti sulaikymo užsakymus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="9ccc5-112">Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių modelių grupės**.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="9ccc5-113">Pasirinkite atitinkamą modelio grupę iš juostos arba sukurkite naują modelio grupę.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="9ccc5-114">„FastTab” **Atsargų strategijos** pasirinkite **Karantino valdymo** žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="9ccc5-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-115">Close the page.</span></span>
1. <span data-ttu-id="9ccc5-116">Taip pat gavimo sandėlių lauke **Sulaikymo sandėlis** reikia nurodyti numatytą karantino sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="9ccc5-117">Kai prekė, užregistruota kaip gauta sandėlyje, priklauso modelių grupei, kurioje pažymėtas sulaikymo valdymo žymės langelis, sistema sugeneruoja jai **sulaikymo** užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="9ccc5-118">Sulaikymo užsakymas nurodo darbuotojams perkelti prekę į sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="9ccc5-119">Kai rankiniu būdu kuriate karantino užsakymus **Karantino užsakymai** puslapyje, nėra būtina nustatyti dabartinės prekės sulaikymo valdymo susietoje prekių modelių grupėje.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="9ccc5-120">Norėdami vykdyti šį procesą, turite nurodyti sulaikytinas turimas atsargas ir naudotiną sulaikymo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="9ccc5-121">Planuoti šį procesą jums padės sulaikymo užsakymų būsenos.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="9ccc5-122">Sulaikymo užsakymų būsenos</span><span class="sxs-lookup"><span data-stu-id="9ccc5-122">Quarantine order statuses</span></span>

<span data-ttu-id="9ccc5-123">Sulaikymo užsakymų būsenos gali būti tokios:</span><span class="sxs-lookup"><span data-stu-id="9ccc5-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="9ccc5-124">Sukurta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-124">Created</span></span>
- <span data-ttu-id="9ccc5-125">Pradėta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-125">Started</span></span>
- <span data-ttu-id="9ccc5-126">Paskelbta baigtu</span><span class="sxs-lookup"><span data-stu-id="9ccc5-126">Reported as finished</span></span>
- <span data-ttu-id="9ccc5-127">Baigta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="9ccc5-128">Sukurta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-128">Created</span></span>

<span data-ttu-id="9ccc5-129">Kai sulaikymo užsakymas sukurtas neautomatiniu būdu, bet prekė dar neperkelta į sulaikymo sandėlį, sulaikymo užsakymo būsena yra **Sukurtas**.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="9ccc5-130">Sugeneruojamos dvi atsargų operacijos.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="9ccc5-131">Viena operacija – tai išdavimo operacija, kurios būsena gali būti **Užsakyta**, **Rezervuota faktiškai** arba **Paimta**.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="9ccc5-132">Kita operacija – tai gavimo operacija, kurios būsena sulaikymo sandėlyje gali būti **Užsakyta** arba **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="9ccc5-133">Galite rezervuoti, pasirinkti ir registruoti atsargų naujinimus naudodami įprastus procesus.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="9ccc5-134">Pradėta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-134">Started</span></span>

<span data-ttu-id="9ccc5-135">Kai sulaikymo užsakymo būsena yra **Pradėtas**, atsargos perkeliamos iš įprasto sandėlio į sulaikymo sandėlį ir sugeneruojamos dvi atsargų operacijos.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="9ccc5-136">Vienos operacijos būsena yra **Išskaičiuota**, o kitos operacijos būsena yra **Gauta**.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="9ccc5-137">Tuo pat metu sukuriamos dvi atsargų operacijos, tvarkančios grįžtamąjį perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="9ccc5-138">Šių operacijų datos nenurodytos.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-138">These transactions aren't dated.</span></span> <span data-ttu-id="9ccc5-139">Vienos operacijos būsena yra **Rezervuota faktiškai**, o kitos operacijos būsena yra **Užsakyta**.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="9ccc5-140">Paskelbta baigtu</span><span class="sxs-lookup"><span data-stu-id="9ccc5-140">Reported as finished</span></span>

<span data-ttu-id="9ccc5-141">Norėdami pradėti sulaikymo užsakymą pranešti baigtu, atidarykite užsakymą ir veiksmų srityje **pasirinkite** Pranešti apie baigtą.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="9ccc5-142">Prekė nebėra sulaikoma, tačiau dar nėra perkeliama atgal į įprastą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="9ccc5-143">Perkėlimą atgal į įprastą sandėlį galima apdoroti naudojant žurnalą Prekių gavimas, kurį galima inicijuoti proceso Skelbti baigtu metu.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="9ccc5-144">Baigta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-144">Ended</span></span>

<span data-ttu-id="9ccc5-145">Pasibaigus sulaikymo užsakymui, prekė iš sulaikymo sandėlio perkeliama atgal į įprastą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="9ccc5-146">Prekės operacijos būsena sulaikymo sandėlyje nustatoma kaip *Parduota*, o įprastame sandėlyje – kaip *Nupirkta*.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="9ccc5-147">Sulaikymo užsakymo nurašytas kiekis</span><span class="sxs-lookup"><span data-stu-id="9ccc5-147">Quarantine order scrap</span></span>

<span data-ttu-id="9ccc5-148">Sulaikymo užsakymo proceso metu galite nurašyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="9ccc5-149">Apdorojant nurašymą atsargų būsena bus nustatyta į *Parduotos* iš sulaikymo sandėlio naudojant išdavimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ccc5-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9ccc5-150">Additional resources</span></span>

- [<span data-ttu-id="9ccc5-151">Atsargų blokavimas</span><span class="sxs-lookup"><span data-stu-id="9ccc5-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
