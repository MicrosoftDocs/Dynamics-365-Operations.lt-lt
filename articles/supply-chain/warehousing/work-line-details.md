---
title: Darbo eilutės informacija
description: Šioje temoje pateikiama informacija apie puslapį Darbo eilutės informacija, pateikiantį išsamų, rūšiuojamą ir filtruojamą atskirų sistemos darbo eilučių sąrašą.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245111"
---
# <a name="work-line-details"></a><span data-ttu-id="2aca5-103">Darbo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="2aca5-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2aca5-104">Puslapis **Darbo eilutės informacija** pateikia išsamų, rūšiuojamą ir filtruojamą atskirų sistemos darbo eilučių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="2aca5-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="2aca5-105">Jame pateikiama išsami planuojamų ir vykdomų sandėlio darbų peržiūra.</span><span class="sxs-lookup"><span data-stu-id="2aca5-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="2aca5-106">Galite lengvai perjungti peržiūrą tarp visų ir tik atvirų darbo eilučių.</span><span class="sxs-lookup"><span data-stu-id="2aca5-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="2aca5-107">Išsami informacija, pateikiama kiekvienai eilutei, apima darbo būseną, prekės numerį, vietą, darbo kiekį, krovinio ID ir siuntos ID.</span><span class="sxs-lookup"><span data-stu-id="2aca5-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="2aca5-108">Darbo eilutės informacijos funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="2aca5-108">Turn on the work line details feature</span></span>

<span data-ttu-id="2aca5-109">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2aca5-110">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="2aca5-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2aca5-111">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="2aca5-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2aca5-112">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="2aca5-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2aca5-113">**Funkcijos pavadinimas:** *Darbo eilutės informacija*</span><span class="sxs-lookup"><span data-stu-id="2aca5-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="2aca5-114">Darbo eilutės informacijos puslapio atidarymas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="2aca5-114">Open and use the Work line details page</span></span>

<span data-ttu-id="2aca5-115">Norėdami peržiūrėti darbo eilutės informacijos sąrašą, eikite į **Sandėlio valdymas \> Darbas \> Eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="2aca5-116">Dabar galite atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="2aca5-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="2aca5-117">Naudoti lauką **Filtruoti** eilučių, turinčių konkrečią bet kurio galimo parametro vertę, paieškai.</span><span class="sxs-lookup"><span data-stu-id="2aca5-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="2aca5-118">(Galimi parametrai apima daug parametrų, kurie tinklelyje nerodomi kaip stulpeliai.)</span><span class="sxs-lookup"><span data-stu-id="2aca5-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="2aca5-119">Naudoti žymės langelį **Rodyti uždarytus** uždarytų eilučių rodymui arba paslėpimui.</span><span class="sxs-lookup"><span data-stu-id="2aca5-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="2aca5-120">Pasirinkti **Rodyti dimensijas** dialogo langui **Dimensijų rodymas** atidaryti, kuriame galėsite pasirinkti rodyti arba slėpti skirtingus dimensijos stulpelius tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="2aca5-121">Pasirinkite bet kurią stulpelio antraštę meniu atidaryti, kuriame galėsite pasirinkti sąrašą rūšiavimą arba filtravimą pagal to stulpelio vertes.</span><span class="sxs-lookup"><span data-stu-id="2aca5-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="2aca5-122">Pasirinkite darbo eilutę ir tada **Keisti vietą** dialogo langui atidaryti, kuriame galėsite keisti tos darbo eilutės vietą.</span><span class="sxs-lookup"><span data-stu-id="2aca5-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="2aca5-123">Jūsų nurodyta vieta nepaisys vietos nurodymo nustatymo.</span><span class="sxs-lookup"><span data-stu-id="2aca5-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="2aca5-124">Pasirinkite darbo eilutę ir **Atšaukti darbo eilutę** dialogo langui atidaryti, kuriame galėsite iš dalies arba visiškai sumažinti tos darbo eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="2aca5-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="2aca5-125">Koreguoti kiekius.</span><span class="sxs-lookup"><span data-stu-id="2aca5-125">Adjust quantities.</span></span>
- <span data-ttu-id="2aca5-126">Peržiūrėti bet kurios darbo eilutės operacijas.</span><span class="sxs-lookup"><span data-stu-id="2aca5-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="2aca5-127">Funkcijos išbandymas</span><span class="sxs-lookup"><span data-stu-id="2aca5-127">Try out the feature</span></span>

<span data-ttu-id="2aca5-128">Šiame skyriuje pateikiama trijų dalių parodomoji versija, kaip dirbti su darbo eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="2aca5-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="2aca5-129">Įgalinkite duomenų pavyzdį</span><span class="sxs-lookup"><span data-stu-id="2aca5-129">Make sample data available</span></span>

<span data-ttu-id="2aca5-130">Norėdami dirbti su parodomąja versija, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="2aca5-131">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="2aca5-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="2aca5-132">Taip pat galite naudoti šią parodomąją versiją kaip vedlį darbui gamybos sistemoje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="2aca5-133">Tačiau Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="2aca5-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="2aca5-134">Patikrinkite ar scenarijaus nustatyme yra pakankamai pasiekiamų atsargų</span><span class="sxs-lookup"><span data-stu-id="2aca5-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="2aca5-135">Jei dirbate su **USMF** demonstraciniais duomenimis, pirmiausia turite įsitikinti, kad sistema nustatyta taip, kad kiekvienoje atitinkamoje vietoje yra pakankamai pasiekiamų atsargų.</span><span class="sxs-lookup"><span data-stu-id="2aca5-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="2aca5-136">Šia parodomąja versija numanoma, kad toliau pateiktos atsargos yra pasiekiamos:</span><span class="sxs-lookup"><span data-stu-id="2aca5-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="2aca5-137">**Prekė M9200:** 45 EA</span><span class="sxs-lookup"><span data-stu-id="2aca5-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="2aca5-138">(ar daugiau)</span><span class="sxs-lookup"><span data-stu-id="2aca5-138">(or more)</span></span>
- <span data-ttu-id="2aca5-139">**Prekė M9202:** 10 EA</span><span class="sxs-lookup"><span data-stu-id="2aca5-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="2aca5-140">(ar daugiau)</span><span class="sxs-lookup"><span data-stu-id="2aca5-140">(or more)</span></span>

<span data-ttu-id="2aca5-141">Atlikite šiuos veiksmus, norėdami patikrinti, ar yra pakankamai pasiekiamų atsargų ir visi reikalingi koregavimai yra atlikti.</span><span class="sxs-lookup"><span data-stu-id="2aca5-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="2aca5-142">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Vietos nurodymai**, sužinoti, kurios prekių paėmimų vietos yra naudojamos pardavimo užsakymo paėmimui 51 sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="2aca5-143">(Daugiau informacijos rasite [Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="2aca5-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="2aca5-144">Tikrinti atsargų lygius atitinkamose vietose.</span><span class="sxs-lookup"><span data-stu-id="2aca5-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="2aca5-145">Koreguoti atsargas kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="2aca5-145">Adjust inventory as required.</span></span> <span data-ttu-id="2aca5-146">Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba pritaikyti bet kurį kitą srautą.</span><span class="sxs-lookup"><span data-stu-id="2aca5-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="2aca5-147">1 dalis: Paėmimo darbo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="2aca5-147">Part 1: Create picking work</span></span>

<span data-ttu-id="2aca5-148">Prieš pradėdami kurti darbo užduotį, įsitikinkite, kad sandėlis nustatytas taip, kad būtų galima atsakyti į darbo užklausas numatytu būdu.</span><span class="sxs-lookup"><span data-stu-id="2aca5-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="2aca5-149">Norėdami sukurti paėmimo darbo užduotį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2aca5-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="2aca5-150">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2aca5-151">Pasirinkite **Nauja** dialogo langui **Sukurti pardavimų užsakymą** atidaryti.</span><span class="sxs-lookup"><span data-stu-id="2aca5-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="2aca5-152">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="2aca5-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2aca5-153">„FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į _US–001_.</span><span class="sxs-lookup"><span data-stu-id="2aca5-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="2aca5-154">„FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į _51_.</span><span class="sxs-lookup"><span data-stu-id="2aca5-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="2aca5-155">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="2aca5-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="2aca5-156">Jūsų naujas pirkimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="2aca5-156">Your new sales order is opened.</span></span> <span data-ttu-id="2aca5-157">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="2aca5-158">Nustatykite tokias šios užsakymo eilutės reikšmes:</span><span class="sxs-lookup"><span data-stu-id="2aca5-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="2aca5-159">**Prekės numeris:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="2aca5-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="2aca5-160">**Kiekis:** _20_</span><span class="sxs-lookup"><span data-stu-id="2aca5-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="2aca5-161">**Vienetas:** _ea_</span><span class="sxs-lookup"><span data-stu-id="2aca5-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="2aca5-162">Pasirinkite naują užsakymo eilutę ir meniu **Atsargos** pasirinkite **Rezervavimas** puslapiui **Rezervavimas** atidaryti.</span><span class="sxs-lookup"><span data-stu-id="2aca5-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="2aca5-163">Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="2aca5-164">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="2aca5-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="2aca5-165">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="2aca5-166">Sistema sukuria siuntą, įtraukia ją į naują krovinį ir sukuria reikiamą darbo užduotį.</span><span class="sxs-lookup"><span data-stu-id="2aca5-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="2aca5-167">Sukurkite antrą pardavimo užsakymą, skirtą tai pačiai kliento sąskaitai ir sandėliui, kurį naudojote pirmajam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="2aca5-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="2aca5-168">Įtraukite šias dvi užsakymo eilutes į šį užsakymą:</span><span class="sxs-lookup"><span data-stu-id="2aca5-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="2aca5-169">**1 eilutė:** Nustatykite lauką **Prekės numeris** į _M9200_, lauką **Kiekis** į _25_ ir lauką **Vienetas** į _EA_.</span><span class="sxs-lookup"><span data-stu-id="2aca5-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="2aca5-170">**2 eilutė:** Nustatykite lauką **Prekės numeris** į _M9202_, lauką **Kiekis** į _10_ ir **Vienetas** lauką į _EA_.</span><span class="sxs-lookup"><span data-stu-id="2aca5-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="2aca5-171">Pakartokite 6-8 veiksmus norėdami rezervuoti atsargas kiekvienai užsakymo eilutei (po vieną), tada pakartokite 9 veiksmą, užsakymui į sandėlį paleisti.</span><span class="sxs-lookup"><span data-stu-id="2aca5-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="2aca5-172">2 dalis: Darbo eilutės vietos pakeitimas</span><span class="sxs-lookup"><span data-stu-id="2aca5-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="2aca5-173">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="2aca5-174">Suraskite ir pasirinkite vieną iš darbo eilučių, kurias sukūrėte šiai parodomajai versijai.</span><span class="sxs-lookup"><span data-stu-id="2aca5-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="2aca5-175">Pasirinkite **Keisti vietą** dialogo langui **Pasirinkti naują vietą** atidaryti.</span><span class="sxs-lookup"><span data-stu-id="2aca5-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="2aca5-176">Dialogo lango **Pasirinkti naują vietą** lauke **Vieta** pasirinkite naują darbo eilutės vietą.</span><span class="sxs-lookup"><span data-stu-id="2aca5-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="2aca5-177">Norėdami pritaikyti pakeitimus ir uždaryti dialogo langą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aca5-178">Galite pateikti vietos keitimus tik tuo atveju, jei naujoje vietoje yra pakankamai prieinamų atsargų (paėmimui), arba jei ji praeina vietos tipo tikrinimą (dėl padėjimo).</span><span class="sxs-lookup"><span data-stu-id="2aca5-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="2aca5-179">3 dalis: keisti darbo eilutės kiekį arba atšaukti darbo eilutę</span><span class="sxs-lookup"><span data-stu-id="2aca5-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="2aca5-180">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="2aca5-181">Suraskite ir pasirinkite vieną iš darbo eilučių, kurias sukūrėte šiai parodomajai versijai.</span><span class="sxs-lookup"><span data-stu-id="2aca5-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="2aca5-182">Atkreipkite dėmesį, kad galite atšaukti arba pakeisti tik tas darbo eilutes, kurių darbo tipas yra _paėmimas_.</span><span class="sxs-lookup"><span data-stu-id="2aca5-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="2aca5-183">Pasirinkite **Atšaukti darbo eilutę**, kad būtų atidarytas dialogo langas **Atšaukti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="2aca5-184">Dialogo lango **Atšaukiamas kiekis** lauke **Kiekis** nurodykite kiekį, kuris turi būti *atimamas iš* kiekio, šiuo metu nurodyto eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2aca5-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="2aca5-185">Pagal numatytuosius nustatymus lauke **Kiekis** rodomas visas kiekis.</span><span class="sxs-lookup"><span data-stu-id="2aca5-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="2aca5-186">Jei atšaukiate visą kiekį, **Darbo būsenos** vertė bus pakeista į _Atšaukta_, tačiau lauke **Darbo kiekis** vis tiek bus rodoma pradinė vertė.</span><span class="sxs-lookup"><span data-stu-id="2aca5-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="2aca5-187">Jei atšaukiate tik dalį kiekio, laukas **Darbo kiekis** bus rodoma atnaujinta reikšmė,, tačiau laukas **Darbo statusas** nepasikeis.</span><span class="sxs-lookup"><span data-stu-id="2aca5-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="2aca5-188">Norėdami pritaikyti pakeitimus ir uždaryti dialogo langą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2aca5-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aca5-189">Jei atšaukiate tik dalį kiekio darbo eilutėje, taip pat turite pašalinti pasenusius kiekius iš krovinio eilutės.</span><span class="sxs-lookup"><span data-stu-id="2aca5-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="2aca5-190">Kitu atveju, nebent tinkamai nustatytas pristatymo trūkumas, nebus galima patvirtinti krovinio išsiuntimo.</span><span class="sxs-lookup"><span data-stu-id="2aca5-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]