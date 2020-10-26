---
title: Siuntų konsolidacija, kai jos išleidžiamos į sandėlį naudojant automatinį pardavimo užsakymų išleidimą
description: Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai naudojant tą pačią periodinę automatizuotą išleidimo į sandėlį procedūrą.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f4d095456435a3401daa173d79b80b81176a3c17
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987123"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="4a964-103">Siuntų konsolidacija, kai jos išleidžiamos į sandėlį naudojant automatinį pardavimo užsakymų išleidimą</span><span class="sxs-lookup"><span data-stu-id="4a964-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a964-104">Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai naudojant tą pačią periodinę automatizuotą išleidimo į sandėlį procedūrą.</span><span class="sxs-lookup"><span data-stu-id="4a964-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="4a964-105">Užsakymai bus automatiškai konsoliduoti į siuntas pagal taisykles, apibrėžiamas kaip siuntos konsolidacijos strategijos.</span><span class="sxs-lookup"><span data-stu-id="4a964-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="4a964-106">Scenarijaus metu sukursite pardavimo užsakymų rinkinius ir kiekvieną rinkinį išleisite į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4a964-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="4a964-107">Tada galėsite peržiūrėti siuntas, sukurtas arba atnaujintas siuntos konsolidacijos metu pagal sukonfigūruotas strategijas.</span><span class="sxs-lookup"><span data-stu-id="4a964-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="4a964-108">Leidimas naudoti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="4a964-108">Make demo data available</span></span>

<span data-ttu-id="4a964-109">Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="4a964-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4a964-110">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="4a964-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="4a964-111">Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="4a964-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="4a964-112">Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus.</span><span class="sxs-lookup"><span data-stu-id="4a964-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="4a964-113">Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.</span><span class="sxs-lookup"><span data-stu-id="4a964-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="4a964-114">Šio scenarijaus pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="4a964-115">Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="4a964-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="4a964-116">Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose.</span><span class="sxs-lookup"><span data-stu-id="4a964-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="4a964-117">Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4a964-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="4a964-118">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="4a964-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="4a964-119">1 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="4a964-120">1-1 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="4a964-120">Sales order 1-1</span></span>

1. <span data-ttu-id="4a964-121">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="4a964-122">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4a964-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4a964-123">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="4a964-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="4a964-124">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-125">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-126">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="4a964-127">1-2 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="4a964-127">Sales order 1-2</span></span>

1. <span data-ttu-id="4a964-128">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="4a964-129">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4a964-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4a964-130">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="4a964-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="4a964-131">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-132">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-133">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="4a964-134">1-3 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="4a964-134">Sales order 1-3</span></span>

1. <span data-ttu-id="4a964-135">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="4a964-136">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4a964-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4a964-137">**Pristatymo būdas:** *10*</span><span class="sxs-lookup"><span data-stu-id="4a964-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="4a964-138">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-139">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-140">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="4a964-141">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-142">**Prekės numeris:** *A0002* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-143">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="4a964-144">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="4a964-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="4a964-145">2 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="4a964-146">2-1 ir 2-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a964-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="4a964-147">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="4a964-148">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="4a964-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="4a964-149">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-150">**Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus*)</span><span class="sxs-lookup"><span data-stu-id="4a964-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="4a964-151">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="4a964-152">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-153">**Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus*)</span><span class="sxs-lookup"><span data-stu-id="4a964-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="4a964-154">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="4a964-155">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="4a964-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="4a964-156">3 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="4a964-157">3-1 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="4a964-157">Sales order 3-1</span></span>

1. <span data-ttu-id="4a964-158">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="4a964-159">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="4a964-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="4a964-160">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-161">**Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus*)</span><span class="sxs-lookup"><span data-stu-id="4a964-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="4a964-162">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="4a964-163">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-164">**Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus*)</span><span class="sxs-lookup"><span data-stu-id="4a964-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="4a964-165">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="4a964-166">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="4a964-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="4a964-167">Šis užsakymas yra toks pat kaip du 2 užsakymų rinkinio užsakymai, kuriuos sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="4a964-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="4a964-168">Tačiau jis nurodytas kaip jo pačio užsakymų rinkinys, nes vėliau šiame scenarijuje jį išleisite atskirai.</span><span class="sxs-lookup"><span data-stu-id="4a964-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="4a964-169">4 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="4a964-170">4-1 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="4a964-170">Sales order 4-1</span></span>

1. <span data-ttu-id="4a964-171">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="4a964-172">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4a964-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4a964-173">**Kliento paraiška:** *1*</span><span class="sxs-lookup"><span data-stu-id="4a964-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="4a964-174">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-175">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-176">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="4a964-177">5 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="4a964-178">5-1 ir 5-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a964-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="4a964-179">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="4a964-180">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4a964-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4a964-181">**Kliento paraiška:** *2*</span><span class="sxs-lookup"><span data-stu-id="4a964-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="4a964-182">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-183">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-184">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="4a964-185">5-3 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="4a964-185">Sales order 5-3</span></span>

1. <span data-ttu-id="4a964-186">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="4a964-187">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4a964-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4a964-188">**Kliento paraiška:** *1*</span><span class="sxs-lookup"><span data-stu-id="4a964-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="4a964-189">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-190">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-191">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="4a964-192">6 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="4a964-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="4a964-193">6-1 ir 6-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a964-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="4a964-194">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="4a964-195">**Kliento sąskaita:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="4a964-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="4a964-196">**Kliento paraiška:** *2*</span><span class="sxs-lookup"><span data-stu-id="4a964-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="4a964-197">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-198">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-199">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="4a964-200">6-3 ir 6-4 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a964-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="4a964-201">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="4a964-202">**Kliento sąskaita:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="4a964-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="4a964-203">**Kliento paraiška:** *1*</span><span class="sxs-lookup"><span data-stu-id="4a964-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="4a964-204">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-205">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-206">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="4a964-207">6-5 ir 6-6 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a964-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="4a964-208">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="4a964-209">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="4a964-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="4a964-210">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="4a964-210">**Site:** *6*</span></span>
    - <span data-ttu-id="4a964-211">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="4a964-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="4a964-212">**Telkinys:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="4a964-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="4a964-213">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-214">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-215">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="4a964-216">6-7 ir 6-8 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a964-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="4a964-217">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="4a964-218">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="4a964-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="4a964-219">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="4a964-219">**Site:** *6*</span></span>
    - <span data-ttu-id="4a964-220">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="4a964-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="4a964-221">**Telkinys:** šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="4a964-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="4a964-222">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="4a964-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="4a964-223">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="4a964-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="4a964-224">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="4a964-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="4a964-225">Automatinis pardavimo užsakymų išleidimas į sandėlį</span><span class="sxs-lookup"><span data-stu-id="4a964-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="4a964-226">Kiekvienam anksčiau sukurtam pardavimo užsakymų rinkiniui atliksite automatinio išleidimo į sandėlį procedūrą.</span><span class="sxs-lookup"><span data-stu-id="4a964-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="4a964-227">Kiekvienu atveju dirbsite pagal čia pateiktą [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="4a964-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="4a964-228">Pagrindinė išleidimo į sandėlį procedūra</span><span class="sxs-lookup"><span data-stu-id="4a964-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="4a964-229">Kiekvienam anksčiau sukurtam pardavimo užsakymų rinkiniui atliksite tris procedūras, aprašytas tolesniuose poskirsniuose.</span><span class="sxs-lookup"><span data-stu-id="4a964-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="4a964-230">Bangos šablono, kuris bus naudojamas išleidimo metu, naujinimas</span><span class="sxs-lookup"><span data-stu-id="4a964-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="4a964-231">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4a964-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="4a964-232">Nustatykite lauką **Bangos šablono tipas** į *Siuntimo*.</span><span class="sxs-lookup"><span data-stu-id="4a964-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="4a964-233">Raskite ir pasirinkite bangos šabloną, susietą su sandėliu, kurį naudojote šio scenarijaus užsakymų rinkiniuose, kuriuos sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="4a964-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="4a964-234">Pavyzdžiui, jei naudojote *24* sandėlį, pasirinkite bangos šabloną **24 numatytoji siunta**.</span><span class="sxs-lookup"><span data-stu-id="4a964-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="4a964-235">Jei naudojote *61* sandėlį, pasirinkite bangos šabloną **61 siunta**.</span><span class="sxs-lookup"><span data-stu-id="4a964-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="4a964-236">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="4a964-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4a964-237">Parinktį **Apdoroti bangą išleidžiant ją į sandėlį** nustatykite į *Ne*.</span><span class="sxs-lookup"><span data-stu-id="4a964-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="4a964-238">Išleidimas į sandėlį</span><span class="sxs-lookup"><span data-stu-id="4a964-238">Release to the warehouse</span></span>

1. <span data-ttu-id="4a964-239">Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Automatinis pardavimo užsakymų išleidimas**.</span><span class="sxs-lookup"><span data-stu-id="4a964-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="4a964-240">Nustatykite lauką **Išleistinas kiekis** į *Visi*.</span><span class="sxs-lookup"><span data-stu-id="4a964-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="4a964-241">„FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti**, kad būtų atidarytas užklausos dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="4a964-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="4a964-242">Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę, kuriai nustatyti tolesni parametrai, į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="4a964-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="4a964-243">**Lentelė:** *pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="4a964-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="4a964-244">**Išvestinė lentelė:** *pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="4a964-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="4a964-245">**Laukas:** *pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="4a964-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="4a964-246">**Kriterijai:** įveskite kableliais atskirtų norimo užsakymo rinkinio pardavimo užsakymų numerių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="4a964-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="4a964-247">Pasirinkite **Gerai**, kad užklausa būtų įrašyta.</span><span class="sxs-lookup"><span data-stu-id="4a964-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="4a964-248">Pasirinkite **Gerai**, kad pradėtumėte procedūrą *Automatinis išleidimas į sandėlį*.</span><span class="sxs-lookup"><span data-stu-id="4a964-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="4a964-249">Sukurtos arba atnaujintos siuntos peržiūra</span><span class="sxs-lookup"><span data-stu-id="4a964-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="4a964-250">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="4a964-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="4a964-251">Raskite ir pasirinkite reikiamą siuntą.</span><span class="sxs-lookup"><span data-stu-id="4a964-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="4a964-252">Jei kuriant ar naujinant siuntą buvo naudojama konsolidacijos strategija, turėtumėte ją matyti lauke **Siuntos konsolidacijos strategija**.</span><span class="sxs-lookup"><span data-stu-id="4a964-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="4a964-253">1 užsakymų rinkinio pardavimo užsakymų išleidimas</span><span class="sxs-lookup"><span data-stu-id="4a964-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="4a964-254">Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 1 užsakymų rinkinio pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a964-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="4a964-255">Baigę turėtumėte matyti, kad buvo sukurtos dvi siuntos.</span><span class="sxs-lookup"><span data-stu-id="4a964-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="4a964-256">Pirmoje siuntoje yra trys eilutės ir ji buvo sukurta naudojant *CustomerMode* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="4a964-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="4a964-257">Antroji siunta, nenaudojanti pristatymo transportavimo būdo *Oro keliai*, buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="4a964-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="4a964-258">2 užsakymų rinkinio pardavimo užsakymų išleidimas</span><span class="sxs-lookup"><span data-stu-id="4a964-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="4a964-259">Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 2 užsakymų rinkinio pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a964-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="4a964-260">Baigę turėtumėte matyti, kad buvo sukurtos trys siuntos.</span><span class="sxs-lookup"><span data-stu-id="4a964-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="4a964-261">Pirmojoje siuntoje yra *degių* prekių.</span><span class="sxs-lookup"><span data-stu-id="4a964-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="4a964-262">Kiekvienoje iš kitų dviejų siuntų yra viena eilutė, turinti *sprogią* prekę.</span><span class="sxs-lookup"><span data-stu-id="4a964-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="4a964-263">3 užsakymų rinkinio pardavimo užsakymų išleidimas</span><span class="sxs-lookup"><span data-stu-id="4a964-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="4a964-264">Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 3 užsakymų rinkinio pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a964-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="4a964-265">Baigę turėtumėte matyti, kad įvyko tolesni veiksmai.</span><span class="sxs-lookup"><span data-stu-id="4a964-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="4a964-266">Buvo atnaujinta viena esama siunta (siunta, sukurta, kai 2 užsakymų rinkinys buvo išleistas į sandėlį).</span><span class="sxs-lookup"><span data-stu-id="4a964-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="4a964-267">Buvo įtraukta eilutė, kurioje yra *degi* prekė.</span><span class="sxs-lookup"><span data-stu-id="4a964-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="4a964-268">Buvo sukurta viena nauja siunta, kurioje yra *sprogi* prekė.</span><span class="sxs-lookup"><span data-stu-id="4a964-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="4a964-269">4 užsakymų rinkinio pardavimo užsakymų išleidimas</span><span class="sxs-lookup"><span data-stu-id="4a964-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="4a964-270">Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 4 užsakymų rinkinio pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a964-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="4a964-271">Baigę turėtumėte matyti, kad buvo atnaujinta viena esama siunta (kurioje laukas **Kliento paraiška** nustatytas į *1*).</span><span class="sxs-lookup"><span data-stu-id="4a964-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="4a964-272">Į ją buvo įtraukta viena nauja eilutė.</span><span class="sxs-lookup"><span data-stu-id="4a964-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="4a964-273">5 užsakymų rinkinio pardavimo užsakymų išleidimas</span><span class="sxs-lookup"><span data-stu-id="4a964-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="4a964-274">Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 5 užsakymų rinkinio pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a964-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="4a964-275">Baigę turėtumėte matyti, kad įvyko tolesni veiksmai.</span><span class="sxs-lookup"><span data-stu-id="4a964-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="4a964-276">Buvo atnaujinta viena esama siunta (kurioje laukas **Kliento paraiška** nustatytas į *1*).</span><span class="sxs-lookup"><span data-stu-id="4a964-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="4a964-277">Į ją buvo įtraukta 5-3 pardavimo užsakymo (kuriame laukas **Kliento paraiška** nustatytas į *1*) eilutė.</span><span class="sxs-lookup"><span data-stu-id="4a964-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="4a964-278">Buvo sukurta viena nauja siunta, kurioje 5-1 ir 5-2 pardavimo užsakymų eilutės sugrupuojamos į vieną siuntą.</span><span class="sxs-lookup"><span data-stu-id="4a964-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="4a964-279">6 užsakymų rinkinio pardavimo užsakymų išleidimas</span><span class="sxs-lookup"><span data-stu-id="4a964-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="4a964-280">Sekite [pagrindinę išleidimo į sandėlį procedūrą](#release-procedure), kad išleistumėte 6 užsakymų rinkinio pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a964-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="4a964-281">Baigę turėtumėte matyti, kad buvo sukurtos keturios siuntos.</span><span class="sxs-lookup"><span data-stu-id="4a964-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="4a964-282">Dviejų kliento *US-003* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="4a964-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="4a964-283">Dviejų kliento *US-004* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="4a964-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="4a964-284">Kliento *US-007* 6-5 ir 6-6 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="4a964-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="4a964-285">Kliento *US-007* 6-7 ir 6-8 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant *CrossOrder* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="4a964-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a964-286">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4a964-286">Additional resources</span></span>

- [<span data-ttu-id="4a964-287">Siuntos konsolidacijos strategijos</span><span class="sxs-lookup"><span data-stu-id="4a964-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="4a964-288">Siuntos konsolidacijos strategijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="4a964-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
