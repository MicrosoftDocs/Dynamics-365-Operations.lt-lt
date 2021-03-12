---
title: Siuntimo proceso apžvalga
description: Šioje temoje apžvelgiamas modulio Atsargų valdymas siuntimo procesas.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27596bf260c069af4a7457c0eb8d02c45e5202b9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000239"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="3c42d-103">Siuntimo proceso apžvalga</span><span class="sxs-lookup"><span data-stu-id="3c42d-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c42d-104">Šioje temoje apžvelgiamas modulio Atsargų valdymas siuntimo procesas.</span><span class="sxs-lookup"><span data-stu-id="3c42d-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="3c42d-105">Išeigos užsakymai</span><span class="sxs-lookup"><span data-stu-id="3c42d-105">Output orders</span></span>

<span data-ttu-id="3c42d-106">Išeigos užsakymai naudojami pardavimo užsakymų eilutėms ir perkėlimo užsakymų eilutėms susieti su siuntimo paėmimo procesais, naudojančiais išrinkimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="3c42d-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="3c42d-107">Iš pardavimo užsakymų ar perkėlimo užsakymų generuojant išrinkimo dokumentus, automatiškai sukuriami išeigos užsakymai ir siuntos.</span><span class="sxs-lookup"><span data-stu-id="3c42d-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="3c42d-108">Išrinkimo dokumentas yra tiesiogiai susijęs su siunta.</span><span class="sxs-lookup"><span data-stu-id="3c42d-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="3c42d-109">Siuntoje galima apdoroti perkėlimo užsakymo siuntą arba pardavimo užsakymo važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="3c42d-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="3c42d-110">Tolesnėje diagramoje apžvelgiamas siunčiamų užsakymų procesas.</span><span class="sxs-lookup"><span data-stu-id="3c42d-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="3c42d-111">[![Siunčiamų užsakymų proceso apžvalga](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="3c42d-112">Galite nustatyti siuntimo taisykles, kad apibrėžtumėte, kaip programa turi apdoroti siuntimo procesą.</span><span class="sxs-lookup"><span data-stu-id="3c42d-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="3c42d-113">Naudodami šias taisykles galite valdyti siuntimo procesą.</span><span class="sxs-lookup"><span data-stu-id="3c42d-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="3c42d-114">Konkrečiai, naudodami šias taisykles galite valdyti, kuriuo proceso etapu galima siųsti siuntą.</span><span class="sxs-lookup"><span data-stu-id="3c42d-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="3c42d-115">Tolesniais parametrais apibrėžiama, kaip tvarkomi siuntimo procesai.</span><span class="sxs-lookup"><span data-stu-id="3c42d-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="3c42d-116">Pardavimo ir perkėlimo užsakymų išrinkimo maršruto būsena</span><span class="sxs-lookup"><span data-stu-id="3c42d-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="3c42d-117">Eikite į **Gautinos sumos** \> **Sąranka** \> **Gautinų sumų parametrai**, tada skirtuko **Naujinimai** lauke **Išrinkimo maršruto būsena** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3c42d-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="3c42d-118">[![Pardavimo užsakymų laukas Išrinkimo maršruto būsena](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="3c42d-119">Jei laukas **Išrinkimo maršruto būsena** nustatytas kaip **Baigtas**, išrinkimo procesas įvyksta automatiškai, vykstant išrinkimo dokumentų generavimo procesui.</span><span class="sxs-lookup"><span data-stu-id="3c42d-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="3c42d-120">Jei laukas nustatytas kaip **Suaktyvintas**, išrinkimo dokumentų eilutes reikia atnaujinti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3c42d-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="3c42d-121">Ta pati sąranka taikoma perkėlimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="3c42d-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="3c42d-122">Eikite į **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai**, tada skirtuko **Transportavimas** lauke **Išrinkimo maršruto būsena** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3c42d-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="3c42d-123">[![Perkėlimo užsakymų laukas Išrinkimo maršruto būsena](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="3c42d-124">Išeigos atsargų užsakymų baigimas</span><span class="sxs-lookup"><span data-stu-id="3c42d-124">End output inventory orders</span></span>

<span data-ttu-id="3c42d-125">Eikite į **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai**, tada skirtuke **Bendra** nustatykite parinktį **Baigti išeigos atsargų užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="3c42d-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="3c42d-126">[![Parinktis Baigti išeigos atsargų užsakymą](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="3c42d-127">Sandėlio darbuotojui sumažinus išrinkimo dokumentų kiekį, iš siuntos bus pašalintas atitinkamas atsargų užsakymo kiekis.</span><span class="sxs-lookup"><span data-stu-id="3c42d-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="3c42d-128">Tam tikru laiku atnaujinus išrinkimo dokumentą, apie likusį kiekį pranešama užsakyme, jei parinktis **Baigti išeigos atsargų užsakymą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c42d-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="3c42d-129">Jei parinktis **Baigti išeigos atsargų užsakymą** nustatyta į **Ne**, likęs kiekis saugomas kaip atviro išeigos užsakymo kiekis ir turi būti įtrauktas į naują išrinkimo dokumentą kaip **Atviri išeigos užsakymai** funkcijos dalis.</span><span class="sxs-lookup"><span data-stu-id="3c42d-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="3c42d-130">[![Meniu Funkcijos komanda Atviri išeigos užsakymai](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="3c42d-131">[![Puslapio Atviri išeigos užsakymai meniu Funkcijos](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="3c42d-132">Mažinti kiekį</span><span class="sxs-lookup"><span data-stu-id="3c42d-132">Reduce quantity</span></span>

<span data-ttu-id="3c42d-133">Trečiasis parametras, kurį galite naudoti išrinkimo dokumentų generavimo proceso metu, yra parametras **Mažinti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="3c42d-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="3c42d-134">Nustačius šį parametrą, jis veikia kartu su parametru **Rezervavimas**, kuris išleidimo į sandėlį metu paleidžia rezervavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="3c42d-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="3c42d-135">[![Parametras Mažinti kiekį](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="3c42d-136">Pardavimo užsakymo siuntimo proceso pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3c42d-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="3c42d-137">Šiame pavyzdyje naudojamas pardavimo užsakymas su dviem prekėmis.</span><span class="sxs-lookup"><span data-stu-id="3c42d-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="3c42d-138">Generuodami išrinkimo dokumentą, pasirenkate parametrą **Mažinti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="3c42d-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="3c42d-139">Todėl išleidžiate ir sukuriate tik turimų atsargų paėmimo eilutes.</span><span class="sxs-lookup"><span data-stu-id="3c42d-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="3c42d-140">Apie paėmimą reikia pranešti naudojant išrinkimo dokumentų registravimo procesą (**Išrinkimo maršruto būsena** = **Suaktyvintas**).</span><span class="sxs-lookup"><span data-stu-id="3c42d-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="3c42d-141">Generuojant išrinkimo dokumentus rezervuojamos dar nerezervuotos atsargos.</span><span class="sxs-lookup"><span data-stu-id="3c42d-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="3c42d-142">Neturimas atsargas galima pašalinti iš pardavimo užsakymo arba išleisti į sandėlį, kad siuntimą būtų galima apdoroti vėliau, kai atsargas bus galima paimti.</span><span class="sxs-lookup"><span data-stu-id="3c42d-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="3c42d-143">[![Išrinkimo dokumento naujinimas](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="3c42d-144">Kai tik paimamos visos puslapio **Išrinkimo dokumento registravimas** paėmimo eilutės, susietoji siunta baigiama.</span><span class="sxs-lookup"><span data-stu-id="3c42d-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="3c42d-145">Tada pagal paimtas atsargas galima inicijuoti pardavimo užsakymo važtaraščių procesą.</span><span class="sxs-lookup"><span data-stu-id="3c42d-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="3c42d-146">[![Siunčiamų siuntų naujinimas](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="3c42d-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
