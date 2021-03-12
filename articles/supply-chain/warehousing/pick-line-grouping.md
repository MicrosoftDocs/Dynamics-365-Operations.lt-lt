---
title: Paėmimo eilutės grupavimas
description: Šioje temoje pateikiama paėmimo eilutės grupavimo apžvalga.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989723"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="01c53-103">Paėmimo eilutės grupavimas</span><span class="sxs-lookup"><span data-stu-id="01c53-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01c53-104">Paėmimo eilutės grupavimas leidžia sujungti keletą darbo eilučių, turinčias ta pačią prekę ir vietą, į vieną paėmimą, kuris pateikiamas vartotojui mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="01c53-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="01c53-105">Todėl sandėlio darbuotojai gali gauti pačias naudingiausias instrukcijas, tačiau būtinas darbo eilučių atskyrimas (pavyzdžiui, skirtingiems konteineriams, užsakymams ir kita) sistemoje.</span><span class="sxs-lookup"><span data-stu-id="01c53-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="01c53-106">Paėmimo eilutės funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="01c53-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="01c53-107">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="01c53-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="01c53-108">Administratoriai gali naudoti [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo erdvę tam, kad patikrintų funkcijos būseną, ir jei būtina, ją įjungtų.</span><span class="sxs-lookup"><span data-stu-id="01c53-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="01c53-109">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="01c53-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="01c53-110">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="01c53-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="01c53-111">**Funkcijos pavadinimas:** *Paėmimo eilutės grupavimas*</span><span class="sxs-lookup"><span data-stu-id="01c53-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="01c53-112">Paėmimo eilutės grupavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="01c53-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="01c53-113">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="01c53-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="01c53-114">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="01c53-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="01c53-115">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="01c53-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="01c53-116">Lauke **Meniu elemento pavadinimas** įveskite *Pardavimo grupės eilutės paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="01c53-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="01c53-117">Lauke **Pavadinimas** įveskite *Pardavimo grupės eilutės paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="01c53-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="01c53-118">Šis pavadinimas bus rodomas mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="01c53-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="01c53-119">Lauke **Režimas** pasirinkite *Darbas*.</span><span class="sxs-lookup"><span data-stu-id="01c53-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="01c53-120">Nustatykite pasirinkties **Naudoti esamą darbą** padėtį *Taip*.</span><span class="sxs-lookup"><span data-stu-id="01c53-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="01c53-121">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="01c53-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="01c53-122">Lauke **Nukreipė** pasirinkite *Vartotojo nurodyta*.</span><span class="sxs-lookup"><span data-stu-id="01c53-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="01c53-123">Nustatykite parinkties **Generuoti numerio lentelę** vertę *Taip*.</span><span class="sxs-lookup"><span data-stu-id="01c53-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="01c53-124">Nustatykite parinkties **Grupinis paėmimas** vertę *Taip*.</span><span class="sxs-lookup"><span data-stu-id="01c53-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="01c53-125">Priimkite numatytąsias vertes likusioms parinktims.</span><span class="sxs-lookup"><span data-stu-id="01c53-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="01c53-126">Atlikite toliau pateikiamus veiksmus, kad sukonfigūruotumėte mobiliojo įrenginio meniu elemento tinkamas darbo klases.</span><span class="sxs-lookup"><span data-stu-id="01c53-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="01c53-127">„FastTab” **Darbo klasės** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="01c53-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="01c53-128">Lauke **Darbo klasės ID** galite pasirinkti arba *Pardavimas* arba *PrdU paėmimas*, atsižvelgiant į sandėlį, kurį naudosite.</span><span class="sxs-lookup"><span data-stu-id="01c53-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="01c53-129">Šiame scenarijuje pasirinkite *PrdU Paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="01c53-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="01c53-130">Laukas **Darbo užsakymo tipas** yra automatiškai nustatomas į *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="01c53-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="01c53-131">Mobiliojo įrenginio meniu nustatymas</span><span class="sxs-lookup"><span data-stu-id="01c53-131">Set up a mobile device menu</span></span>

<span data-ttu-id="01c53-132">Atlikite šiuos veiksmus norėdami įtraukti meniu elementą, kurį ką tik sukūrėte **Siunčiama** meniu.</span><span class="sxs-lookup"><span data-stu-id="01c53-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="01c53-133">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="01c53-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="01c53-134">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="01c53-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="01c53-135">Sąrašo srityje rodomi visi esami mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="01c53-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="01c53-136">Pasirinkite *Siunčiama* iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="01c53-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="01c53-137">Sąraše **Prieinami meniu ir meniu elementai** suraskite ir pasirinkite jūsų sukurtą *Pardavimo grupės eilutės paėmimas* meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="01c53-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="01c53-138">Pasirinkite dešiniosios rodyklės mygtuką *Pardavimo grupės eilutės paėmimas* meniu elementui perkelti į **Meniu struktūra** sąrašą.</span><span class="sxs-lookup"><span data-stu-id="01c53-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="01c53-139">Naudokite rodyklės aukštyn ir žemyn mygtukus perkelti meniu prekei į norimą meniu struktūros padėtį.</span><span class="sxs-lookup"><span data-stu-id="01c53-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="01c53-140">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="01c53-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="01c53-141">Darbo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="01c53-141">Set up a work template</span></span>

1. <span data-ttu-id="01c53-142">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="01c53-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="01c53-143">Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="01c53-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="01c53-144">Tinklelyje **Peržiūra** raskite ir pasirinkite darbo šabloną, kuris turėtų būti naudojamas su šia funkcija.</span><span class="sxs-lookup"><span data-stu-id="01c53-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="01c53-145">Šiame scenarijuje pasirinkite *51 paėmimo iki etapo* šabloną.</span><span class="sxs-lookup"><span data-stu-id="01c53-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="01c53-146">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="01c53-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="01c53-147">Užklausos redaktoriaus teksto laukelio skirtuke **Rūšiavimas** pasirinkite **Įtraukti**, o tada nustatykite šias naujos eilutės vertes:</span><span class="sxs-lookup"><span data-stu-id="01c53-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="01c53-148">Stulpelyje **Lentelė** pasirinkite *Laikino darbo operacijos*.</span><span class="sxs-lookup"><span data-stu-id="01c53-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="01c53-149">Stulpelyje **Išvestinė lentelė** pasirinkite *Laikino darbo operacijos*.</span><span class="sxs-lookup"><span data-stu-id="01c53-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="01c53-150">Stulpelyje **Laukas** pasirinkite *Prekės numeris*.</span><span class="sxs-lookup"><span data-stu-id="01c53-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="01c53-151">Stulpelyje **Ieškos kryptis** pasirinkite *Didėjimo tvarka*.</span><span class="sxs-lookup"><span data-stu-id="01c53-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="01c53-152">Pasirinkite **Gerai** dialogo lango uždarymui ir jūsų pasirinkimo įrašymui.</span><span class="sxs-lookup"><span data-stu-id="01c53-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="01c53-153">Jūs gaunate šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“</span><span class="sxs-lookup"><span data-stu-id="01c53-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="01c53-154">Pasirinkite **Taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="01c53-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01c53-155">Norint, kad paėmimo eilutės grupavimo funkcija veiktų, darbo eilutės turi būti surūšiuotos pagal prekės ID.</span><span class="sxs-lookup"><span data-stu-id="01c53-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="01c53-156">Jei eilutės, kuriose yra tos pačios prekės, nepateikiamos viena po kitos, jos nebus grupuojamos.</span><span class="sxs-lookup"><span data-stu-id="01c53-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="01c53-157">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="01c53-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="01c53-158">Paėmimo darbo kūrimas</span><span class="sxs-lookup"><span data-stu-id="01c53-158">Create picking work</span></span>

<span data-ttu-id="01c53-159">Kad galėtumėte nustatyti paėmimo eilutės grupavimą, turite sukurti tinkamą siuntimo darbą.</span><span class="sxs-lookup"><span data-stu-id="01c53-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="01c53-160">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="01c53-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="01c53-161">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="01c53-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="01c53-162">Lauke **Kliento kodas** pasirinkite *„US-004”*.</span><span class="sxs-lookup"><span data-stu-id="01c53-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="01c53-163">„FastTab“ **Bendra** lauke **Sandėlis** pasirinkite *51*.</span><span class="sxs-lookup"><span data-stu-id="01c53-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="01c53-164">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="01c53-164">Select **OK**.</span></span>
1. <span data-ttu-id="01c53-165">„FastTab” **Pardavimo užsakymo eilutės** įtraukite toliau pateikiamas šešias eilutes:</span><span class="sxs-lookup"><span data-stu-id="01c53-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="01c53-166">**1 eilutė.** Lauke **Prekės numeris** pasirinkite *M9200*.</span><span class="sxs-lookup"><span data-stu-id="01c53-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="01c53-167">Lauke **Kiekis** įveskite *3*.</span><span class="sxs-lookup"><span data-stu-id="01c53-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="01c53-168">**2 eilutė.** Lauke **Prekės numeris** pasirinkite *M9201*.</span><span class="sxs-lookup"><span data-stu-id="01c53-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="01c53-169">Lauke **Kiekis** įveskite *3*.</span><span class="sxs-lookup"><span data-stu-id="01c53-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="01c53-170">**3 eilutė.** Lauke **Prekės numeris** pasirinkite *M9202*.</span><span class="sxs-lookup"><span data-stu-id="01c53-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="01c53-171">Lauke **Kiekis** įveskite *2*.</span><span class="sxs-lookup"><span data-stu-id="01c53-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="01c53-172">**4 eilutė.** Lauke **Prekės numeris** pasirinkite *M9200*.</span><span class="sxs-lookup"><span data-stu-id="01c53-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="01c53-173">Lauke **Kiekis** įveskite *1*.</span><span class="sxs-lookup"><span data-stu-id="01c53-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="01c53-174">**5 eilutė.** Lauke **Prekės numeris** pasirinkite *M9200*.</span><span class="sxs-lookup"><span data-stu-id="01c53-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="01c53-175">Lauke **Kiekis** įveskite *3*.</span><span class="sxs-lookup"><span data-stu-id="01c53-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="01c53-176">**6 eilutė.** Lauke **Prekės numeris** pasirinkite *M9202*.</span><span class="sxs-lookup"><span data-stu-id="01c53-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="01c53-177">Lauke **Kiekis** įveskite *7*.</span><span class="sxs-lookup"><span data-stu-id="01c53-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="01c53-178">Toliau pateikiama kiekvienos prekės bendro kiekio suvestinė.</span><span class="sxs-lookup"><span data-stu-id="01c53-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="01c53-179">**Prekė M9200:** *7* vienetai</span><span class="sxs-lookup"><span data-stu-id="01c53-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="01c53-180">**Prekė M9201:** *3* vienetai</span><span class="sxs-lookup"><span data-stu-id="01c53-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="01c53-181">**Prekė M9202:** *9* vienetai</span><span class="sxs-lookup"><span data-stu-id="01c53-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="01c53-182">Prieš perduodami užsakymus į sandėlį, turite įsitikinti, kad paėmimo vietose pakanka atsargų visoms prekėms visuose užsakymuose pateikti.</span><span class="sxs-lookup"><span data-stu-id="01c53-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="01c53-183">Patikrinkite parametrą **Vietos nurodymas**, kad nustatytumėte paėmimo vietas, naudojamas pardavimo užsakymo paėmimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="01c53-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="01c53-184">Jei naudojate „Contoso” demonstracinių duomenų aplinką *„51”* sandėliui, patvirtinkite, kad yra galimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="01c53-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="01c53-185">Dabar turite rezervuoti atsargas kiekvienai eilutei.</span><span class="sxs-lookup"><span data-stu-id="01c53-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="01c53-186">„FastTab” **Pardavimo užsakymo eilutės** pasirinkite vieną iš eilučių, kurias reikia rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="01c53-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="01c53-187">Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="01c53-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="01c53-188">Puslapio **Rezervavimas** veiksmų srityje pasirinkite **Rezervuoti partiją** rezervavimo taikymui.</span><span class="sxs-lookup"><span data-stu-id="01c53-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="01c53-189">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="01c53-189">Then close the page.</span></span>
1. <span data-ttu-id="01c53-190">Pakartokite 8‑10 veiksmus eilutėms, kurias reikia rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="01c53-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="01c53-191">Dabar privalote išleisti pardavimo užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="01c53-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="01c53-192">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="01c53-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="01c53-193">Gausite pranešimą, kad siunta ir banga buvo sukurtos ir, kad banga buvo pateikta vykdyti pakete.</span><span class="sxs-lookup"><span data-stu-id="01c53-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="01c53-194">Kai banga ir visos proceso pabaigos užduotys yra baigtos, sukuriamas darbo, kuriame yra šešios eilutės, ID.</span><span class="sxs-lookup"><span data-stu-id="01c53-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="01c53-195">Eilutės rūšiuojamos pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="01c53-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="01c53-196">Eikite į **Sandėlio valdymas \> Darbas \> Visas darbas** sukurtam darbui peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="01c53-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="01c53-197">Pasižymėkite **Darbo ID** reikšmę, nes ji bus reikalinga kitoje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="01c53-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="01c53-198">Paėmimo inicijavimas iš mobiliojo įrenginio</span><span class="sxs-lookup"><span data-stu-id="01c53-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="01c53-199">Prisijunkite prie mobilaus prietaiso kaip vartotojas nustatytas sandėliui *51*.</span><span class="sxs-lookup"><span data-stu-id="01c53-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="01c53-200">Mobiliajame įrenginyje pasirinkite meniu, kuriame yra naujas mobiliojo įrenginio meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="01c53-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="01c53-201">Šiame scenarijuje pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="01c53-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="01c53-202">Pasirinkite meniu elementą **Pardavimo grupės eilutės paėmimas** paėmimo inicijavimui.</span><span class="sxs-lookup"><span data-stu-id="01c53-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="01c53-203">Įveskite **Darbo ID** vertę, kurią pasižymėjote ankstesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="01c53-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="01c53-204">Turėtumėte matyti paėmimo veiksmą, kuriame sugrupuotos visos prekės *„M9200”* paėmimo eilutės, ir turėtumėte gauti instrukcijas, kaip paimti *7'* prekės *„M9200”* vienetus.</span><span class="sxs-lookup"><span data-stu-id="01c53-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="01c53-205">Mobiliajame įrenginyje trijų paėmimo darbo eilučių paėmimo darbas buvo sujungtas į vieną paėmimo veiksmą vartotojui.</span><span class="sxs-lookup"><span data-stu-id="01c53-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="01c53-206">Patvirtinkite paėmimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="01c53-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="01c53-207">Perėję į darbo ID darbo puslapį pastebėsite, kad visos trys prekės *„M9200”* paėmimo eilutės buvo uždarytos vienu metu.</span><span class="sxs-lookup"><span data-stu-id="01c53-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="01c53-208">Grįžkite į mobilųjį įrenginį ir toliau atlikite paėmimą.</span><span class="sxs-lookup"><span data-stu-id="01c53-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="01c53-209">Turi būti pristatyta 4‑a prekės *„M9201”* darbo eilutė.</span><span class="sxs-lookup"><span data-stu-id="01c53-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="01c53-210">Kadangi užsakyme buvo tik viena darbo eilutė, nieko negalima sujungti.</span><span class="sxs-lookup"><span data-stu-id="01c53-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="01c53-211">Patvirtinkite paėmimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="01c53-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="01c53-212">Per paskutinį paėmimo veiksmą mobiliajame įrenginyje sujungiamos dvi paskutinės darbo užsakymo paėmimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="01c53-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="01c53-213">Atlikite paėmimo veiksmą *9'* prekės *„M9202”* vienetams.</span><span class="sxs-lookup"><span data-stu-id="01c53-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="01c53-214">Patvirtinkite padėjimo veiksmą ir visas papildomas paėmimo / padėjimo poras, kad užbaigtumėte darbą.</span><span class="sxs-lookup"><span data-stu-id="01c53-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="01c53-215">Darbo eilutes galima grupuoti tik tuo atveju, jei jos pateikiamos iš eilės.</span><span class="sxs-lookup"><span data-stu-id="01c53-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="01c53-216">Toliau nurodytos funkcijos nepalaikomos.</span><span class="sxs-lookup"><span data-stu-id="01c53-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="01c53-217">Esamo svorio prekės</span><span class="sxs-lookup"><span data-stu-id="01c53-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="01c53-218">Jei darbe yra esamo svorio prekių, prieš pradėdami paėmimą matote klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="01c53-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="01c53-219">Vienetų paėmimas</span><span class="sxs-lookup"><span data-stu-id="01c53-219">Piece picking</span></span>
>   - <span data-ttu-id="01c53-220">Darbo eilutės, kuriose nebaigtas papildymo darbas</span><span class="sxs-lookup"><span data-stu-id="01c53-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="01c53-221">Viršytas paėmimo kiekis</span><span class="sxs-lookup"><span data-stu-id="01c53-221">Over-picking</span></span>
>   - <span data-ttu-id="01c53-222">Nevisiškas paėmimas ir prekių perskirstymas</span><span class="sxs-lookup"><span data-stu-id="01c53-222">Short picking with item reallocation</span></span>
