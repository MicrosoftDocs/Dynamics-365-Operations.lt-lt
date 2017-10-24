---
title: Siuntimo procesas
description: "Šioje temoje apžvelgiamas modulio Atsargų valdymas siuntimo procesas."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: lt-lt
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="924ea-103">Siuntimo procesas</span><span class="sxs-lookup"><span data-stu-id="924ea-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="924ea-104">Šioje temoje apžvelgiamas modulio Atsargų valdymas siuntimo procesas.</span><span class="sxs-lookup"><span data-stu-id="924ea-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="924ea-105">Išeigos užsakymai</span><span class="sxs-lookup"><span data-stu-id="924ea-105">Output orders</span></span>

<span data-ttu-id="924ea-106">Išeigos užsakymai naudojami pardavimo užsakymų eilutėms ir perkėlimo užsakymų eilutėms susieti su siuntimo paėmimo procesais, naudojančiais išrinkimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="924ea-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="924ea-107">Iš pardavimo užsakymų ar perkėlimo užsakymų generuojant išrinkimo dokumentus, automatiškai sukuriami išeigos užsakymai ir siuntos.</span><span class="sxs-lookup"><span data-stu-id="924ea-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="924ea-108">Išrinkimo dokumentas yra tiesiogiai susijęs su siunta.</span><span class="sxs-lookup"><span data-stu-id="924ea-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="924ea-109">Siuntoje galima apdoroti perkėlimo užsakymo siuntą arba pardavimo užsakymo važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="924ea-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="924ea-110">Tolesnėje diagramoje apžvelgiamas siunčiamų užsakymų procesas.</span><span class="sxs-lookup"><span data-stu-id="924ea-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="924ea-111">[![Siunčiamų užsakymų proceso apžvalga](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="924ea-112">Galite nustatyti siuntimo taisykles, kad apibrėžtumėte, kaip programa turi apdoroti siuntimo procesą.</span><span class="sxs-lookup"><span data-stu-id="924ea-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="924ea-113">Naudodami šias taisykles galite valdyti siuntimo procesą.</span><span class="sxs-lookup"><span data-stu-id="924ea-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="924ea-114">Konkrečiai, naudodami šias taisykles galite valdyti, kuriuo proceso etapu galima siųsti siuntą.</span><span class="sxs-lookup"><span data-stu-id="924ea-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="924ea-115">Tolesniais parametrais apibrėžiama, kaip tvarkomi siuntimo procesai.</span><span class="sxs-lookup"><span data-stu-id="924ea-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="924ea-116">Pardavimo ir perkėlimo užsakymų išrinkimo maršruto būsena</span><span class="sxs-lookup"><span data-stu-id="924ea-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="924ea-117">Eikite į **Gautinos sumos** \> **Sąranka** \> **Gautinų sumų parametrai**, tada skirtuko **Naujinimai** lauke **Išrinkimo maršruto būsena** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="924ea-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="924ea-118">[![Pardavimo užsakymų laukas Išrinkimo maršruto būsena](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="924ea-119">Jei laukas **Išrinkimo maršruto būsena** nustatytas kaip **Baigtas**, išrinkimo procesas įvyksta automatiškai, vykstant išrinkimo dokumentų generavimo procesui.</span><span class="sxs-lookup"><span data-stu-id="924ea-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="924ea-120">Jei laukas nustatytas kaip **Suaktyvintas**, išrinkimo dokumentų eilutes reikia atnaujinti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="924ea-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="924ea-121">Ta pati sąranka taikoma perkėlimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="924ea-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="924ea-122">Eikite į **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai**, tada skirtuko **Transportavimas** lauke **Išrinkimo maršruto būsena** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="924ea-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="924ea-123">[![Perkėlimo užsakymų laukas Išrinkimo maršruto būsena](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="924ea-124">Išeigos atsargų užsakymų baigimas</span><span class="sxs-lookup"><span data-stu-id="924ea-124">End output inventory orders</span></span>

<span data-ttu-id="924ea-125">Eikite į **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai**, tada skirtuke **Bendra** nustatykite parinktį **Baigti išeigos atsargų užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="924ea-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="924ea-126">[![Parinktis Baigti išeigos atsargų užsakymą](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="924ea-127">Kartais, vykdant išrinkimo dokumento procesą, kai kurių atsargose esančių prekių paimti negalima.</span><span class="sxs-lookup"><span data-stu-id="924ea-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="924ea-128">Pavyzdžiui, tokia situacija gali kilti, jei sandėlio darbininkas sumažina paėmimo eilučių kiekius ir apdoroja išrinkimo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="924ea-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="924ea-129">Jei parinktis **Baigti išeigos atsargų užsakymą** nustatyta kaip **Taip**, likę nepaimti kiekiai grąžinami į užsakymo lygį.</span><span class="sxs-lookup"><span data-stu-id="924ea-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="924ea-130">Jei parinktis nustatyta kaip **Ne**, likę nepaimti kiekiai saugomi kaip atviro išeigos užsakymo kiekis.</span><span class="sxs-lookup"><span data-stu-id="924ea-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="924ea-131">Tokiu atveju kiekiai lieka išleisti į sandėlį ir juos reikia įtraukti į naują išrinkimo dokumentą naudojant funkciją **Atviri išeigos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="924ea-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="924ea-132">[![Meniu Funkcijos komanda Atviri išeigos užsakymai](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="924ea-133">[![Puslapio Atviri išeigos užsakymai meniu Funkcijos](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="924ea-134">Mažinti kiekį</span><span class="sxs-lookup"><span data-stu-id="924ea-134">Reduce quantity</span></span>

<span data-ttu-id="924ea-135">Trečiasis parametras, kurį galite naudoti išrinkimo dokumentų generavimo proceso metu, yra parametras **Mažinti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="924ea-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="924ea-136">Nustačius šį parametrą, jis veikia kartu su parametru **Rezervavimas**, kuris išleidimo į sandėlį metu paleidžia rezervavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="924ea-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="924ea-137">[![Parametras Mažinti kiekį](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="924ea-138">Pardavimo užsakymo siuntimo proceso pavyzdys</span><span class="sxs-lookup"><span data-stu-id="924ea-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="924ea-139">Šiame pavyzdyje naudojamas pardavimo užsakymas su dviem prekėmis.</span><span class="sxs-lookup"><span data-stu-id="924ea-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="924ea-140">Generuodami išrinkimo dokumentą, pasirenkate parametrą **Mažinti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="924ea-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="924ea-141">Todėl išleidžiate ir sukuriate tik turimų atsargų paėmimo eilutes.</span><span class="sxs-lookup"><span data-stu-id="924ea-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="924ea-142">Apie paėmimą reikia pranešti naudojant išrinkimo dokumentų registravimo procesą (**Išrinkimo maršruto būsena** = **Suaktyvintas**).</span><span class="sxs-lookup"><span data-stu-id="924ea-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="924ea-143">Generuojant išrinkimo dokumentus rezervuojamos dar nerezervuotos atsargos.</span><span class="sxs-lookup"><span data-stu-id="924ea-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="924ea-144">Neturimas atsargas galima pašalinti iš pardavimo užsakymo arba išleisti į sandėlį, kad siuntimą būtų galima apdoroti vėliau, kai atsargas bus galima paimti.</span><span class="sxs-lookup"><span data-stu-id="924ea-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="924ea-145">[![Išrinkimo dokumento naujinimas](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="924ea-146">Kai tik paimamos visos puslapio **Išrinkimo dokumento registravimas** paėmimo eilutės, susietoji siunta baigiama.</span><span class="sxs-lookup"><span data-stu-id="924ea-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="924ea-147">Tada pagal paimtas atsargas galima inicijuoti pardavimo užsakymo važtaraščių procesą.</span><span class="sxs-lookup"><span data-stu-id="924ea-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="924ea-148">[![Siunčiamų siuntų naujinimas](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="924ea-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

