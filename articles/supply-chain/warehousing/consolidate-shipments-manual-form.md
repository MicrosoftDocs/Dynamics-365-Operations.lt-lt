---
title: Siuntų konsolidacija rankiniu būdu naudojant siuntų konsolidavimo puslapį
description: Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami naudojant puslapį Konsoliduoti siuntas.
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
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383822"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="89795-103">Siuntų konsolidacija rankiniu būdu naudojant siuntų konsolidavimo puslapį</span><span class="sxs-lookup"><span data-stu-id="89795-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89795-104">Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami naudojant puslapį **Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="89795-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="89795-105">Leidimas naudoti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="89795-105">Make demo data available</span></span>

<span data-ttu-id="89795-106">Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="89795-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="89795-107">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="89795-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="89795-108">Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="89795-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="89795-109">Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus.</span><span class="sxs-lookup"><span data-stu-id="89795-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="89795-110">Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.</span><span class="sxs-lookup"><span data-stu-id="89795-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="89795-111">Šio scenarijaus pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="89795-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="89795-112">Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="89795-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="89795-113">Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose.</span><span class="sxs-lookup"><span data-stu-id="89795-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="89795-114">Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="89795-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="89795-115">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="89795-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="89795-116">1 ir 2 pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="89795-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="89795-117">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="89795-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="89795-118">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="89795-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="89795-119">**Telkinys:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="89795-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="89795-120">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="89795-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="89795-121">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="89795-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="89795-122">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="89795-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="89795-123">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="89795-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="89795-124">3 ir 4 pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="89795-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="89795-125">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="89795-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="89795-126">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="89795-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="89795-127">**Telkinys:** šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="89795-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="89795-128">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="89795-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="89795-129">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="89795-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="89795-130">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="89795-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="89795-131">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="89795-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="89795-132">Užsakymų išleidimas į sandėlį</span><span class="sxs-lookup"><span data-stu-id="89795-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="89795-133">Atlikite tolesnius veiksmus, kad išleistumėte kiekvieną šiame scenarijuje sukurtą pardavimo užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="89795-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="89795-134">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="89795-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="89795-135">Raskite ir pasirinkite pardavimo užsakymą, kurį norite išleisti.</span><span class="sxs-lookup"><span data-stu-id="89795-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="89795-136">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Veiksmai \> Išleisti į sandėlį**, kad būtų išleistas pasirinktas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="89795-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="89795-137">Kartokite šią procedūrą kiekvienam kitam šiame scenarijuje sukurtam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="89795-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="89795-138">Konsoliduoti siuntas</span><span class="sxs-lookup"><span data-stu-id="89795-138">Consolidate shipments</span></span>

1. <span data-ttu-id="89795-139">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="89795-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="89795-140">Raskite ir pasirinkite siuntą, sukurtą, kai į sandėlį buvo išleistas 1 pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="89795-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="89795-141">(Jos laukas **Siuntos konsolidacijos strategija** turėtų būti nustatytas į *Užsakymų telkinys*.)</span><span class="sxs-lookup"><span data-stu-id="89795-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="89795-142">Veiksmų srities skirtuke **Siuntos** pasirinkite **Siuntos \> Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="89795-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="89795-143">Patikrinkite siuntas, kurias siūloma konsoliduoti.</span><span class="sxs-lookup"><span data-stu-id="89795-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="89795-144">Konsolidavimui turi būti siūloma tik viena siunta, turinti tą pačią strategiją.</span><span class="sxs-lookup"><span data-stu-id="89795-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="89795-145">Puslapį **Siuntos konsolidacija** uždarykite.</span><span class="sxs-lookup"><span data-stu-id="89795-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="89795-146">Raskite ir pasirinkite siuntą, sukurtą, kai į sandėlį buvo išleistas 3 pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="89795-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="89795-147">(Jos laukas **Siuntos konsolidacijos strategija** turėtų būti nustatytas į *Numatytoji*.)</span><span class="sxs-lookup"><span data-stu-id="89795-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="89795-148">Veiksmų srities skirtuke **Siuntos** pasirinkite **Siuntos \> Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="89795-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="89795-149">Patikrinkite, ar nėra siūlomų konsoliduoti siuntų.</span><span class="sxs-lookup"><span data-stu-id="89795-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="89795-150">Pasirinkite **Rodyti filtrus**.</span><span class="sxs-lookup"><span data-stu-id="89795-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="89795-151">Srityje **Filtrai** pašalinkite filtrą **Užsakymo numeris** ir pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="89795-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="89795-152">Patikrinkite siuntas, kurias siūloma konsoliduoti.</span><span class="sxs-lookup"><span data-stu-id="89795-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="89795-153">Konsolidavimui turi būti siūloma tik viena siunta, turinti tą pačią strategiją.</span><span class="sxs-lookup"><span data-stu-id="89795-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89795-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="89795-154">Additional resources</span></span>

- [<span data-ttu-id="89795-155">Siuntos konsolidacijos strategijos</span><span class="sxs-lookup"><span data-stu-id="89795-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="89795-156">Siuntos konsolidacijos strategijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="89795-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)