---
title: Siuntų konsolidacija, kai siuntos konsolidacijos strategijos nepaisoma puslapyje Išleisti į sandėlį
description: Šioje temoje pateikiamas scenarijus, kai viena ar daugiau pardavimo eilučių turi būti rankiniu būdu išleistos į sandėlį iš puslapio Išleisti į sandėlį, o sistemos nustatyta siuntos konsolidacijos strategija turi būti perrašyta prieš išleidimą.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: be573f3a137fbd74ba2f5d8bb346e4bb9f9116c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237112"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="0ebb1-103">Siuntų konsolidacija, kai siuntos konsolidacijos strategijos nepaisoma puslapyje Išleisti į sandėlį</span><span class="sxs-lookup"><span data-stu-id="0ebb1-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ebb1-104">Šioje temoje pateikiamas scenarijus, kai viena ar daugiau pardavimo eilučių turi būti rankiniu būdu išleistos į sandėlį iš puslapio **Išleisti į sandėlį**, o sistemos nustatyta siuntos konsolidacijos strategija turi būti perrašyta prieš išleidimą.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="0ebb1-105">Gali reikėti perrašyti siuntos konsolidacijos strategiją, jei, pvz., užsakymas, kuris paprastai nėra konsoliduojamas su atviromis siuntomis, turi būti konsoliduojamas su atviromis siuntomis.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="0ebb1-106">Scenarijaus metu sukursite pardavimo užsakymų rinkinį, o tada perrašysite numatytąją siuntos konsolidacijos strategiją prieš užsakymų išleidimą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="0ebb1-107">Leidimas naudoti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="0ebb1-107">Make demo data available</span></span>

<span data-ttu-id="0ebb1-108">Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0ebb1-109">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="0ebb1-110">Siuntos konsolidacijos strategijų ir produktų filtrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0ebb1-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="0ebb1-111">Čia aprašytame scenarijuje laikoma, kad jūs jau įjungėte funkciją, atlikote pratimus, esančius [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md), ir sukūrėte ten aprašytas strategijas ir kitus įrašus.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="0ebb1-112">Nepamirškite atlikti šių pratimų prieš tęsdami darbą su šiuo scenarijumi.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="0ebb1-113">Šio scenarijaus pardavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="0ebb1-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="0ebb1-114">Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai** ir sukurkite tris vienodus pardavimo užsakymus, kuriuose nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0ebb1-115">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="0ebb1-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="0ebb1-116">Įtraukite pardavimo užsakymo eilutę, kuriai nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0ebb1-117">**Prekės numeris:** *A0001* (prekė, kuriai nepriskirtas filtras **4 kodas**)</span><span class="sxs-lookup"><span data-stu-id="0ebb1-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0ebb1-118">**Kiekis:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0ebb1-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0ebb1-119">Pasirinkite **Atsargos \> Rezervavimas**, tada veiksmų srityje pasirinkite **Rezervuoti partiją**, kad užsakymo eilutė būtų rezervuota.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="0ebb1-120">Pardavimo užsakymų išleidimas iš puslapio Išleisti į sandėlį</span><span class="sxs-lookup"><span data-stu-id="0ebb1-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="0ebb1-121">Atlikite tolesnius veiksmus, norėdami perrašyti siuntos konsolidacijos strategiją išleidimo į sandėlį metu.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="0ebb1-122">Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Išleidimas į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="0ebb1-123">Viršutinėje srityje pasirinkite pirmąjį šiame scenarijuje sukurtą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="0ebb1-124">Pasirinkite **Įtraukti**, kad įtrauktumėte eilutę į išleidimą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="0ebb1-125">Atkreipkite dėmesį, kad *numatytoji* siuntos konsolidacijos strategija taikoma apatinėje srityje.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="0ebb1-126">Apatinėje srityje pasirinkite **Pasirinkti naują siuntos konsolidacijos strategiją**.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="0ebb1-127">Pasirinkite strategiją, leidžiančią konsoliduoti su kitomis tos pačios strategijos atidarytomis siuntomis.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="0ebb1-128">Pavyzdžiui, pasirinkite strategiją *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="0ebb1-129">Pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="0ebb1-130">Pasirinkite antrąjį ir trečiąjį šiame scenarijuje sukurtus pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="0ebb1-131">Pasirinkite **Įtraukti**, kad įtrauktumėte eilutes į išleidimą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="0ebb1-132">Atkreipkite dėmesį, kad *numatytoji* strategija taikoma apatinėje srityje.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="0ebb1-133">Pasirinkite antrą eilutę, tada lauke **Pasirinkti naują siuntos konsolidacijos strategiją** pasirinkite strategiją *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="0ebb1-134">Abiejose eilutėse pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="0ebb1-135">Siuntų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="0ebb1-135">Verify the shipments</span></span>

<span data-ttu-id="0ebb1-136">Turėtų būti sukurtos dvi siuntos.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="0ebb1-137">Pirmoje siuntoje yra dvi eilutės ir ji buvo sukurta naudojant *CustomerOrderNo* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="0ebb1-138">Antroje siuntoje yra viena eilutė ir siunta buvo sukurta naudojant *numatytąją* siuntos konsolidacijos strategiją.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="0ebb1-139">Atlikite tolesnius veiksmus, norėdami peržiūrėti sukurtas siuntas.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="0ebb1-140">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="0ebb1-141">Raskite ir pasirinkite reikiamą siuntą.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="0ebb1-142">Lauke **Siuntos konsolidacijos strategija** peržiūrėkite konsolidacijos strategiją, kuri buvo naudojama kuriant siuntą.</span><span class="sxs-lookup"><span data-stu-id="0ebb1-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ebb1-143">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0ebb1-143">Additional resources</span></span>

- [<span data-ttu-id="0ebb1-144">Siuntos konsolidacijos strategijos</span><span class="sxs-lookup"><span data-stu-id="0ebb1-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="0ebb1-145">Siuntos konsolidacijos strategijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0ebb1-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]