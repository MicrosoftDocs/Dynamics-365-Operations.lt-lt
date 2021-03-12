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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983020"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="f7d55-103">Siuntų konsolidacija rankiniu būdu naudojant siuntų konsolidavimo puslapį</span><span class="sxs-lookup"><span data-stu-id="f7d55-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7d55-104">Šioje temoje pateikiamas scenarijus, kai į sandėlį išleidžiami keli užsakymai, o vėliau jie konsoliduojami naudojant puslapį **Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="f7d55-105">Leidimas naudoti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="f7d55-105">Make demo data available</span></span>

<span data-ttu-id="f7d55-106">Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="f7d55-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f7d55-107">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="f7d55-108">Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f7d55-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="f7d55-109">Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus.</span><span class="sxs-lookup"><span data-stu-id="f7d55-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="f7d55-110">Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.</span><span class="sxs-lookup"><span data-stu-id="f7d55-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="f7d55-111">Šio scenarijaus pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7d55-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="f7d55-112">Pirmiausia sukurkite pardavimo užsakymų, su kuriais galite dirbti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f7d55-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="f7d55-113">Turite dirbti su sandėliu, kuris parengtas naudoti išplėstiniuose sandėlio (WMS) procesuose.</span><span class="sxs-lookup"><span data-stu-id="f7d55-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="f7d55-114">Jeigu nėra aiškiai nurodyto kito sandėlio, kiekviename iš tolesnių užsakymų rinkinių reikia naudoti tą patį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f7d55-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="f7d55-115">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymų, kuriuose nustatyti tolesniuose poskirsniuose aprašyti parametrai, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f7d55-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="f7d55-116">1 ir 2 pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7d55-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="f7d55-117">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f7d55-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f7d55-118">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f7d55-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f7d55-119">**Telkinys:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="f7d55-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="f7d55-120">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f7d55-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f7d55-121">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f7d55-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f7d55-122">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f7d55-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f7d55-123">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f7d55-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="f7d55-124">3 ir 4 pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7d55-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="f7d55-125">Sukurkite du vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f7d55-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f7d55-126">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f7d55-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f7d55-127">**Telkinys:** šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="f7d55-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="f7d55-128">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="f7d55-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f7d55-129">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="f7d55-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f7d55-130">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f7d55-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f7d55-131">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="f7d55-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="f7d55-132">Užsakymų išleidimas į sandėlį</span><span class="sxs-lookup"><span data-stu-id="f7d55-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="f7d55-133">Atlikite tolesnius veiksmus, kad išleistumėte kiekvieną šiame scenarijuje sukurtą pardavimo užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f7d55-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="f7d55-134">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f7d55-135">Raskite ir pasirinkite pardavimo užsakymą, kurį norite išleisti.</span><span class="sxs-lookup"><span data-stu-id="f7d55-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="f7d55-136">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Veiksmai \> Išleisti į sandėlį**, kad būtų išleistas pasirinktas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="f7d55-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="f7d55-137">Kartokite šią procedūrą kiekvienam kitam šiame scenarijuje sukurtam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="f7d55-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="f7d55-138">Konsoliduoti siuntas</span><span class="sxs-lookup"><span data-stu-id="f7d55-138">Consolidate shipments</span></span>

1. <span data-ttu-id="f7d55-139">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="f7d55-140">Raskite ir pasirinkite siuntą, sukurtą, kai į sandėlį buvo išleistas 1 pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="f7d55-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="f7d55-141">(Jos laukas **Siuntos konsolidacijos strategija** turėtų būti nustatytas į *Užsakymų telkinys*.)</span><span class="sxs-lookup"><span data-stu-id="f7d55-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="f7d55-142">Veiksmų srities skirtuke **Siuntos** pasirinkite **Siuntos \> Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="f7d55-143">Patikrinkite siuntas, kurias siūloma konsoliduoti.</span><span class="sxs-lookup"><span data-stu-id="f7d55-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="f7d55-144">Konsolidavimui turi būti siūloma tik viena siunta, turinti tą pačią strategiją.</span><span class="sxs-lookup"><span data-stu-id="f7d55-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="f7d55-145">Puslapį **Siuntos konsolidacija** uždarykite.</span><span class="sxs-lookup"><span data-stu-id="f7d55-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="f7d55-146">Raskite ir pasirinkite siuntą, sukurtą, kai į sandėlį buvo išleistas 3 pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="f7d55-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="f7d55-147">(Jos laukas **Siuntos konsolidacijos strategija** turėtų būti nustatytas į *Numatytoji*.)</span><span class="sxs-lookup"><span data-stu-id="f7d55-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="f7d55-148">Veiksmų srities skirtuke **Siuntos** pasirinkite **Siuntos \> Konsoliduoti siuntas**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="f7d55-149">Patikrinkite, ar nėra siūlomų konsoliduoti siuntų.</span><span class="sxs-lookup"><span data-stu-id="f7d55-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="f7d55-150">Pasirinkite **Rodyti filtrus**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="f7d55-151">Srityje **Filtrai** pašalinkite filtrą **Užsakymo numeris** ir pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="f7d55-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="f7d55-152">Patikrinkite siuntas, kurias siūloma konsoliduoti.</span><span class="sxs-lookup"><span data-stu-id="f7d55-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="f7d55-153">Konsolidavimui turi būti siūloma tik viena siunta, turinti tą pačią strategiją.</span><span class="sxs-lookup"><span data-stu-id="f7d55-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7d55-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f7d55-154">Additional resources</span></span>

- [<span data-ttu-id="f7d55-155">Siuntos konsolidacijos strategijos</span><span class="sxs-lookup"><span data-stu-id="f7d55-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="f7d55-156">Siuntos konsolidacijos strategijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f7d55-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)