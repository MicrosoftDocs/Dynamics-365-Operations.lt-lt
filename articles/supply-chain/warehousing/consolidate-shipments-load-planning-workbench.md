---
title: Siuntų konsolidacija naudojant išleidimo į sandėlį funkciją krovinio planavimo darbo srityje
description: Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli to paties krovinio užsakymai, o tada jie automatiškai konsoliduojami į siuntas.
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
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 396a038dbf2f4b6835ecbb5fd8cb39a3a3608af7
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383826"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="f044a-103">Siuntų konsolidacija naudojant išleidimo į sandėlį funkciją krovinio planavimo darbo srityje</span><span class="sxs-lookup"><span data-stu-id="f044a-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f044a-104">Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli to paties krovinio užsakymai, o tada jie automatiškai konsoliduojami į siuntas.</span><span class="sxs-lookup"><span data-stu-id="f044a-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="f044a-105">Leidimas naudoti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="f044a-105">Make demo data available</span></span>

<span data-ttu-id="f044a-106">Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="f044a-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f044a-107">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f044a-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="f044a-108">Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f044a-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="f044a-109">Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus.</span><span class="sxs-lookup"><span data-stu-id="f044a-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="f044a-110">Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.</span><span class="sxs-lookup"><span data-stu-id="f044a-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="f044a-111">Šio scenarijaus pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f044a-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="f044a-112">Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f044a-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="f044a-113">Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose.</span><span class="sxs-lookup"><span data-stu-id="f044a-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="f044a-114">Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f044a-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="f044a-115">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f044a-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="f044a-116">1 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="f044a-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="f044a-117">1-1 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="f044a-117">Sales order 1-1</span></span>

1. <span data-ttu-id="f044a-118">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f044a-119">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f044a-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f044a-120">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f044a-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f044a-121">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-122">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-123">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-124">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="f044a-125">1-2 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="f044a-125">Sales order 1-2</span></span>

1. <span data-ttu-id="f044a-126">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f044a-127">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f044a-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f044a-128">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f044a-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f044a-129">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-130">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-131">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-132">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="f044a-133">1-3 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="f044a-133">Sales order 1-3</span></span>

1. <span data-ttu-id="f044a-134">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f044a-135">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f044a-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f044a-136">**Pristatymo būdas:** *10*</span><span class="sxs-lookup"><span data-stu-id="f044a-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="f044a-137">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-138">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-139">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-140">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="f044a-141">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-142">**Prekės numeris:** *A0002* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-143">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="f044a-144">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f044a-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f044a-145">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad būtų rezervuota antroji užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="f044a-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="f044a-146">2 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="f044a-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="f044a-147">2-1 ir 2-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="f044a-148">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-149">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="f044a-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="f044a-150">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-151">**Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus*)</span><span class="sxs-lookup"><span data-stu-id="f044a-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="f044a-152">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-153">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="f044a-154">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-155">**Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus*)</span><span class="sxs-lookup"><span data-stu-id="f044a-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="f044a-156">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="f044a-157">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f044a-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f044a-158">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad būtų rezervuota antroji užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="f044a-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="f044a-159">3 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="f044a-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="f044a-160">3-1 ir 3-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="f044a-161">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-162">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f044a-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f044a-163">**Kliento paraiška:** *1*</span><span class="sxs-lookup"><span data-stu-id="f044a-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="f044a-164">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-165">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-166">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-167">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="f044a-168">3-3 ir 3-4 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="f044a-169">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-170">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f044a-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f044a-171">**Kliento paraiška:** *2*</span><span class="sxs-lookup"><span data-stu-id="f044a-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="f044a-172">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-173">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-174">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-175">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="f044a-176">4 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="f044a-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="f044a-177">4-1 ir 4-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="f044a-178">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-179">**Kliento sąskaita:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="f044a-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="f044a-180">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-181">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-182">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-183">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="f044a-184">4-3 ir 4-4 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="f044a-185">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-186">**Kliento sąskaita:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="f044a-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="f044a-187">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-188">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-189">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-190">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="f044a-191">4-5 ir 4-6 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="f044a-192">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-193">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f044a-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f044a-194">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="f044a-194">**Site:** *6*</span></span>
    - <span data-ttu-id="f044a-195">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="f044a-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f044a-196">**Telkinys:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="f044a-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="f044a-197">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-198">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-199">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-200">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="f044a-201">4-7 ir 4-8 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="f044a-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="f044a-202">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f044a-203">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f044a-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f044a-204">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="f044a-204">**Site:** *6*</span></span>
    - <span data-ttu-id="f044a-205">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="f044a-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f044a-206">**Telkinys:** šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="f044a-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="f044a-207">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f044a-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f044a-208">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f044a-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f044a-209">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f044a-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f044a-210">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f044a-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="f044a-211">Krovinio planavimo darbo srities naudojimas kroviniams kurti ir paleisti į sandėlį</span><span class="sxs-lookup"><span data-stu-id="f044a-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="f044a-212">Atlikite tolesnius veiksmus, kad sukurtumėte krovinį kiekvienam šiame scenarijuje sukurtam užsakymų rinkiniui ir išleistumėte į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f044a-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="f044a-213">Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="f044a-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="f044a-214">Skirtuke **Pardavimo eilutės** raskite ir pasirinkite visas vieno iš sukurtų užsakymų rinkinių, sukurtų šiame scenarijuje, pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="f044a-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="f044a-215">Veiksmų srities skirtuke **Pasiūla ir paklausa** pasirinkite **Įtraukti \> Į naują krovinį**, kad įtrauktumėte pasirinktas užsakymo eilutes į naują krovinį.</span><span class="sxs-lookup"><span data-stu-id="f044a-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="f044a-216">Dialogo lango **Krovinio šablono priskyrimas** lauke **Krovinio šablono ID** pasirinkite krovinio šabloną, pvz., *Stnd krovinio šablonas*.</span><span class="sxs-lookup"><span data-stu-id="f044a-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="f044a-217">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f044a-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="f044a-218">Dalyje **Kroviniai** raskite ir pasirinkite ką tik sukurtą krovinį.</span><span class="sxs-lookup"><span data-stu-id="f044a-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="f044a-219">Pasirinkite **Išleidimas \> Išleidimas į sandėlį**, kad išleistumėte pasirinktą krovinį į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f044a-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="f044a-220">Kartokite šią procedūrą trims kitiems šiame scenarijuje sukurtiems užsakymų rinkiniams.</span><span class="sxs-lookup"><span data-stu-id="f044a-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="f044a-221">Siuntų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="f044a-221">Verify the shipments</span></span>

<span data-ttu-id="f044a-222">Tolesnė procedūra leidžia tikrinti siuntas, sukurtas arba atnaujintas dėl siuntos konsolidacijos.</span><span class="sxs-lookup"><span data-stu-id="f044a-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="f044a-223">Naudokite ją, norėdami peržiūrėti kiekvieną užsakymą, kurį sukūrėte šiam scenarijui, ir tada peržiūrėkite tolesnius poskyrius, kad įsitikintumėte, jog gavote numatytus rezultatus.</span><span class="sxs-lookup"><span data-stu-id="f044a-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="f044a-224">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="f044a-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="f044a-225">Raskite ir pasirinkite reikiamą siuntą.</span><span class="sxs-lookup"><span data-stu-id="f044a-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="f044a-226">Jei kuriant ar naujinant siuntą buvo naudojama konsolidacijos strategija, turėtumėte ją matyti lauke **Siuntos konsolidacijos strategija**.</span><span class="sxs-lookup"><span data-stu-id="f044a-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="f044a-227">1 užsakymų rinkinio išleidimas viename krovinyje</span><span class="sxs-lookup"><span data-stu-id="f044a-227">Release order set 1 in one load</span></span>

<span data-ttu-id="f044a-228">Turėtų būti sukurtos dvi siuntos.</span><span class="sxs-lookup"><span data-stu-id="f044a-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="f044a-229">Pirmoje siuntoje yra trys eilutės ir ji buvo sukurta naudojant *CustomerMode* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="f044a-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="f044a-230">Antroji siunta, nenaudojanti pristatymo transportavimo būdo *Oro keliai*, buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="f044a-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="f044a-231">2 užsakymų rinkinio išleidimas viename krovinyje</span><span class="sxs-lookup"><span data-stu-id="f044a-231">Release order set 2 in one load</span></span>

<span data-ttu-id="f044a-232">Turėtų būti sukurtos trys siuntos.</span><span class="sxs-lookup"><span data-stu-id="f044a-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="f044a-233">Pirmojoje siuntoje yra *degių* prekių.</span><span class="sxs-lookup"><span data-stu-id="f044a-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="f044a-234">Kiekvienoje iš kitų dviejų siuntų yra viena eilutė, turinti *sprogią* prekę.</span><span class="sxs-lookup"><span data-stu-id="f044a-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="f044a-235">3 užsakymų rinkinio išleidimas viename krovinyje</span><span class="sxs-lookup"><span data-stu-id="f044a-235">Release order set 3 in one load</span></span>

<span data-ttu-id="f044a-236">Turėtų būti sukurtos dvi siuntos.</span><span class="sxs-lookup"><span data-stu-id="f044a-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="f044a-237">Pirmoje siuntoje yra pardavimo užsakymo eilučių, kuriose laukas **Kliento paraiška** nustatytas į *1*.</span><span class="sxs-lookup"><span data-stu-id="f044a-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="f044a-238">Antroje siuntoje yra pardavimo užsakymo eilučių, kuriose laukas **Kliento paraiška** nustatytas į *2*.</span><span class="sxs-lookup"><span data-stu-id="f044a-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="f044a-239">4 užsakymų rinkinio išleidimas viename krovinyje</span><span class="sxs-lookup"><span data-stu-id="f044a-239">Release order set 4 in one load</span></span>

<span data-ttu-id="f044a-240">Turėtų būti sukurtos keturios siuntos.</span><span class="sxs-lookup"><span data-stu-id="f044a-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="f044a-241">Dviejų kliento sąskaitos *US-003* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="f044a-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f044a-242">Dviejų kliento sąskaitos *US-004* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="f044a-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f044a-243">Kliento sąskaitos *US-007* 4-5 ir 4-6 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="f044a-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f044a-244">Kliento sąskaitos *US-007* 4-7 ir 4-8 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant *CrossOrder* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="f044a-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f044a-245">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f044a-245">Additional resources</span></span>

- [<span data-ttu-id="f044a-246">Siuntos konsolidacijos strategijos</span><span class="sxs-lookup"><span data-stu-id="f044a-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="f044a-247">Siuntos konsolidacijos strategijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f044a-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
