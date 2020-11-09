---
title: Siuntų konsolidacija naudojant siuntų konsolidacijos darbo sritį
description: Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami į siuntas naudojant siuntos konsolidacijos darbo sritį.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1eec1a8e3a9a2a0f95302e1d6ea68eb90b9a3b93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016821"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="b71f1-103">Siuntų konsolidacija naudojant siuntų konsolidacijos darbo sritį</span><span class="sxs-lookup"><span data-stu-id="b71f1-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b71f1-104">Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami į siuntas naudojant siuntos konsolidacijos darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="b71f1-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="b71f1-105">Leidimas naudoti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="b71f1-105">Make demo data available</span></span>

<span data-ttu-id="b71f1-106">Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="b71f1-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b71f1-107">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="b71f1-108">Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b71f1-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="b71f1-109">Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus.</span><span class="sxs-lookup"><span data-stu-id="b71f1-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="b71f1-110">Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.</span><span class="sxs-lookup"><span data-stu-id="b71f1-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="b71f1-111">Neautomatinės siuntos konsolidacijos funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="b71f1-112">Kad galėtumėte naudoti funkciją *Neautomatinė siuntos konsolidacija* , turite ją įjungti jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="b71f1-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="b71f1-113">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="b71f1-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b71f1-114">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="b71f1-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b71f1-115">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="b71f1-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b71f1-116">**Funkcijos pavadinimas:** *Neautomatinė siuntos konsolidacija*</span><span class="sxs-lookup"><span data-stu-id="b71f1-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="b71f1-117">Kaip buvo minėta temoje [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), prieš kurdami strategijas, taip pat turite įjungti funkciją *Konsoliduoti siuntą*.</span><span class="sxs-lookup"><span data-stu-id="b71f1-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="b71f1-118">Tačiau jau turėjote atlikti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="b71f1-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="b71f1-119">Šio scenarijaus pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="b71f1-120">Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="b71f1-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="b71f1-121">Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose.</span><span class="sxs-lookup"><span data-stu-id="b71f1-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="b71f1-122">Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="b71f1-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="b71f1-123">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="b71f1-123">Go to **Accounts receivable \> Orders \> All sales orders** , and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="b71f1-124">1 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="b71f1-125">1-1 ir 1-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="b71f1-126">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-127">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b71f1-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b71f1-128">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b71f1-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b71f1-129">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-130">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-131">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-132">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-132">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="b71f1-133">1-3 pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="b71f1-133">Sales order 1-3</span></span>

1. <span data-ttu-id="b71f1-134">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-135">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b71f1-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b71f1-136">**Pristatymo būdas:** *10*</span><span class="sxs-lookup"><span data-stu-id="b71f1-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="b71f1-137">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-138">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-139">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-140">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-140">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="b71f1-141">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-142">**Prekės numeris:** *A0002* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-143">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b71f1-144">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b71f1-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b71f1-145">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad būtų rezervuota antroji užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="b71f1-145">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="b71f1-146">2 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="b71f1-147">2-1 ir 2-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="b71f1-148">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-149">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b71f1-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="b71f1-150">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b71f1-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b71f1-151">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-152">**Prekės numeris:** *M9200* (prekė, kurios filtras **4 kodas** nustatytas į *Degus* )</span><span class="sxs-lookup"><span data-stu-id="b71f1-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable* )</span></span>
    - <span data-ttu-id="b71f1-153">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-154">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-154">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="b71f1-155">Įtraukite antrą pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-156">**Prekės numeris:** *M9201* (prekė, kurios filtras **4 kodas** nustatytas į *Sprogus* )</span><span class="sxs-lookup"><span data-stu-id="b71f1-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive* )</span></span>
    - <span data-ttu-id="b71f1-157">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b71f1-158">**Pristatymo būdas:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b71f1-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b71f1-159">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad būtų rezervuota antroji užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="b71f1-159">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="b71f1-160">3 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="b71f1-161">3-1 ir 3-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="b71f1-162">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-163">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b71f1-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b71f1-164">**Kliento paraiška:** *1*</span><span class="sxs-lookup"><span data-stu-id="b71f1-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b71f1-165">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-166">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-167">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-168">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-168">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="b71f1-169">3-3 ir 3-4 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="b71f1-170">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-171">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b71f1-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b71f1-172">**Kliento paraiška:** *2*</span><span class="sxs-lookup"><span data-stu-id="b71f1-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b71f1-173">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-174">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-175">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-176">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-176">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="b71f1-177">4 užsakymų rinkinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="b71f1-178">4-1 ir 4-2 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="b71f1-179">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-180">**Kliento sąskaita:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="b71f1-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="b71f1-181">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-182">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-183">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-184">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-184">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="b71f1-185">4-3 ir 4-4 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="b71f1-186">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-187">**Kliento sąskaita:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b71f1-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="b71f1-188">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-189">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-190">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-191">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-191">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="b71f1-192">4-5 ir 4-6 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="b71f1-193">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-194">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b71f1-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b71f1-195">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="b71f1-195">**Site:** *6*</span></span>
    - <span data-ttu-id="b71f1-196">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="b71f1-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b71f1-197">**Telkinys:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="b71f1-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="b71f1-198">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-199">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-200">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-201">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-201">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="b71f1-202">4-7 ir 4-8 pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b71f1-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="b71f1-203">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b71f1-204">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b71f1-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b71f1-205">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="b71f1-205">**Site:** *6*</span></span>
    - <span data-ttu-id="b71f1-206">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="b71f1-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b71f1-207">**Telkinys:** šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="b71f1-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="b71f1-208">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71f1-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b71f1-209">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas** )</span><span class="sxs-lookup"><span data-stu-id="b71f1-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b71f1-210">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b71f1-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b71f1-211">Pasirinkite **Atsargos \> Rezervavimas** , tada veiksmų srityje pasirinkite **Rezervuoti partiją** , kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="b71f1-211">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="b71f1-212">Užsakymų išleidimas į sandėlį</span><span class="sxs-lookup"><span data-stu-id="b71f1-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="b71f1-213">Atlikite tolesnius veiksmus, kad išleistumėte kiekvieną šiame scenarijuje sukurtą pardavimo užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="b71f1-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="b71f1-214">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b71f1-215">Raskite ir pasirinkite pardavimo užsakymą, kurį norite išleisti.</span><span class="sxs-lookup"><span data-stu-id="b71f1-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="b71f1-216">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Veiksmai \> Išleisti į sandėlį** , kad būtų išleistas pasirinktas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b71f1-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="b71f1-217">Kartokite šią procedūrą kiekvienam kitam šiame scenarijuje sukurtam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="b71f1-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="b71f1-218">Siuntų konsolidacija naudojant siuntų konsolidacijos darbo sritį</span><span class="sxs-lookup"><span data-stu-id="b71f1-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="b71f1-219">Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Siuntos konsolidacijos darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="b71f1-220">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b71f1-221">Užklausos rengyklės dialogo lango skirtuke **Diapazonas** pasirinkite **Įtraukti** , kad įtrauktumėte eilutę, kuriai nustatyti tolesni parametrai, į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="b71f1-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="b71f1-222">**Lentelė:** *pardavimo užsakymai*</span><span class="sxs-lookup"><span data-stu-id="b71f1-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="b71f1-223">**Laukas:** *pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="b71f1-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="b71f1-224">**Kriterijai:** įveskite kableliais atskirtų pardavimo užsakymų numerių sąrašą kiekvienam užsakymų rinkiniui, sukurtam šiam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="b71f1-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="b71f1-225">Pasirinkite **Gerai** , kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b71f1-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b71f1-226">Veiksmų srityje pasirinkite **Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="b71f1-227">Pasirinkite visas siuntas, tada veiksmų srityje pasirinkite **Konsoliduoti**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="b71f1-228">Siuntų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-228">Verify the shipments</span></span>

<span data-ttu-id="b71f1-229">Tolesnė procedūra leidžia tikrinti siuntas, sukurtas arba atnaujintas dėl siuntos konsolidacijos.</span><span class="sxs-lookup"><span data-stu-id="b71f1-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="b71f1-230">Naudokite ją, norėdami peržiūrėti kiekvieną užsakymą, kurį sukūrėte šiam scenarijui, ir tada peržiūrėkite tolesnius poskyrius, kad įsitikintumėte, jog gavote numatytus rezultatus.</span><span class="sxs-lookup"><span data-stu-id="b71f1-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="b71f1-231">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="b71f1-232">Raskite ir pasirinkite reikiamą siuntą.</span><span class="sxs-lookup"><span data-stu-id="b71f1-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="b71f1-233">Jei kuriant ar naujinant siuntą buvo naudojama konsolidacijos strategija, turėtumėte ją matyti lauke **Siuntos konsolidacijos strategija**.</span><span class="sxs-lookup"><span data-stu-id="b71f1-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="b71f1-234">1 užsakymų rinkinio susijusios siuntos</span><span class="sxs-lookup"><span data-stu-id="b71f1-234">Related shipments for order set 1</span></span>

<span data-ttu-id="b71f1-235">Turėtų būti sukurtos dvi siuntos.</span><span class="sxs-lookup"><span data-stu-id="b71f1-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="b71f1-236">Pirmoje siuntoje yra trys eilutės ir ji buvo sukurta naudojant *CustomerMode* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="b71f1-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="b71f1-237">Antroji siunta, nenaudojanti pristatymo transportavimo būdo *Oro keliai* , buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="b71f1-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="b71f1-238">2 užsakymo rinkinio susijusios siuntos</span><span class="sxs-lookup"><span data-stu-id="b71f1-238">Related shipments for order set 2</span></span>

<span data-ttu-id="b71f1-239">Turėtų būti sukurtos trys siuntos.</span><span class="sxs-lookup"><span data-stu-id="b71f1-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="b71f1-240">Pirmojoje siuntoje yra *degių* prekių.</span><span class="sxs-lookup"><span data-stu-id="b71f1-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="b71f1-241">Kiekvienoje iš kitų dviejų siuntų yra viena eilutė, turinti *sprogią* prekę.</span><span class="sxs-lookup"><span data-stu-id="b71f1-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="b71f1-242">3 užsakymo rinkinio susijusios siuntos</span><span class="sxs-lookup"><span data-stu-id="b71f1-242">Related shipments for order set 3</span></span>

<span data-ttu-id="b71f1-243">Turėtų būti sukurtos dvi siuntos.</span><span class="sxs-lookup"><span data-stu-id="b71f1-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="b71f1-244">Pirmoje siuntoje yra pardavimo užsakymo eilučių, kuriose laukas **Kliento paraiška** nustatytas į *1*.</span><span class="sxs-lookup"><span data-stu-id="b71f1-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="b71f1-245">Antroje siuntoje yra pardavimo užsakymo eilučių, kuriose laukas **Kliento paraiška** nustatytas į *2*.</span><span class="sxs-lookup"><span data-stu-id="b71f1-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="b71f1-246">4 užsakymo rinkinio susijusios siuntos</span><span class="sxs-lookup"><span data-stu-id="b71f1-246">Related shipments for order set 4</span></span>

<span data-ttu-id="b71f1-247">Turėtų būti sukurtos keturios siuntos.</span><span class="sxs-lookup"><span data-stu-id="b71f1-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="b71f1-248">Dviejų kliento *US-003* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="b71f1-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b71f1-249">Dviejų kliento *US-004* užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="b71f1-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b71f1-250">Kliento *US-007* 4-5 ir 4-6 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant siuntos konsolidacijos strategiją *Užsakymų telkinys*.</span><span class="sxs-lookup"><span data-stu-id="b71f1-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b71f1-251">Kliento *US-007* 4-7 ir 4-8 pardavimų užsakymų eilutės buvo sugrupuotos į vieną siuntą naudojant *CrossOrder* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="b71f1-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b71f1-252">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b71f1-252">Additional resources</span></span>

- [<span data-ttu-id="b71f1-253">Siuntos konsolidacijos strategijos</span><span class="sxs-lookup"><span data-stu-id="b71f1-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="b71f1-254">Siuntos konsolidacijos strategijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b71f1-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
