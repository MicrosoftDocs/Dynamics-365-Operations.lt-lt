---
title: Sistemos nurodyta darbo seka
description: Šioje temoje pateikiama informacija apie sistemos nurodytą darbo seką. Ši funkcija leidžia rūšiuoti ir filtruoti darbo užsakymus, kuriuos sistema pateikia vartotojams vykdyti. Tai naudinga scenarijuose, kuomet reikia nurodyti papildomus kriterijus prekių paėmimo proceso vykdymui.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7db884a5cd62e1f44a2a86316fde6bf2d11a3376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239139"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="875d0-105">Sistemos nurodyta darbo seka</span><span class="sxs-lookup"><span data-stu-id="875d0-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="875d0-106">Sistemos nurodyta darbo seka leidžia rūšiuoti ir filtruoti darbo užsakymus, kuriuos sistema pateikia vartotojams vykdyti.</span><span class="sxs-lookup"><span data-stu-id="875d0-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="875d0-107">Tai naudinga scenarijuose, kai prekių paėmimo proceso vykdymui reikia nurodyti papildomus kriterijus, pvz., siuntimo laiką, prekių paėmimo zoną, vietos profilį arba įvairių kriterijų derinį.</span><span class="sxs-lookup"><span data-stu-id="875d0-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="875d0-108">Ši funkcija išplečia dabartinę sistemos nurodyto paėmimo funkciją įtraukdama sistemos nurodytą užklausos užsakymą, kuriame vartotojai gali nustatyti seką ir vieną ar daugiau užklausų, įvertinančių visus sukurtus darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="875d0-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="875d0-109">Užfiksuoti ir pristatyti bus tik tie darbo užsakymai, kurie atitinka kriterijus, nurodytus mobiliojo įrenginio meniu elemento nustatyme.</span><span class="sxs-lookup"><span data-stu-id="875d0-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="875d0-110">Todėl ši funkcija leidžia tolimesnį prekių paėmimo procesų optimizavimą, kadangi identifikuoja darbo užsakymus, atitinkančius nurodytus kriterijus, priskiria juos tinkamam mobiliojo įrenginio meniu elementui ir pateikia juos darbuotojui, atsižvelgiant į įgūdžius, surinkimo įrangą ar kitą reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="875d0-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="875d0-111">Jei reikalingi įvairūs kriterijai, turi būti naudojami keli mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="875d0-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="875d0-112">Organizacijoje naudojamos sistemos nurodytos darbo eigos funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="875d0-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="875d0-113">Norėdami naudoti sistemos nurodytos darbo eigos funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="875d0-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="875d0-114">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="875d0-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="875d0-115">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="875d0-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="875d0-116">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="875d0-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="875d0-117">**Funkcijos pavadinimas:** *Organizacijoje naudojama sistemos nurodyta darbo seka*</span><span class="sxs-lookup"><span data-stu-id="875d0-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="875d0-118">Sąranka</span><span class="sxs-lookup"><span data-stu-id="875d0-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="875d0-119">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="875d0-119">Make demo data available</span></span>

<span data-ttu-id="875d0-120">Norėdami dirbti su scenarijumi naudojant šioje temoje pristatytas reikšmes, turite naudoti sistemą, kurioje įdiegti standartiniai demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="875d0-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="875d0-121">Taip pat, turite pasirinkti **USMF** juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="875d0-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="875d0-122">Scenarijus naudoja *51* sandėlio demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="875d0-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="875d0-123">Prieš išleisdami užsakymus į sandėlį, įsitikinkite, kad prekių paėmimo vietose pakanka atsargų visiems užsakymams.</span><span class="sxs-lookup"><span data-stu-id="875d0-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="875d0-124">Numatytieji USMF duomenys turi palaikyti šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="875d0-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="875d0-125">Jeigu nenaudojate demonstracinių duomenų, patikrinkite parametrą **Vietos nurodymas** sužinoti kurios prekių paėmimo vietos yra naudojamos pardavimo užsakymo prekių paėmimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="875d0-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="875d0-126">Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba bet kokį kitą srautą.</span><span class="sxs-lookup"><span data-stu-id="875d0-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="875d0-127">Mobiliojo įrenginio meniu nustatymas</span><span class="sxs-lookup"><span data-stu-id="875d0-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="875d0-128">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="875d0-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="875d0-129">Mobiliojo įrenginio meniu elementų sąraše pasirinkite **Prekių paėmimas – Sistema**.</span><span class="sxs-lookup"><span data-stu-id="875d0-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="875d0-130">Reikalingas meniu elementas jau turi būti.</span><span class="sxs-lookup"><span data-stu-id="875d0-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="875d0-131">Patikrinkite šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="875d0-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="875d0-132">„FastTab“ skirtuke **Bendra** laukas **Nurodoma** turi būti nustatytas į *Sistemos nurodoma*.</span><span class="sxs-lookup"><span data-stu-id="875d0-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="875d0-133">„FastTab“ skirtukas **Darbo klasės** turi rodyti šiuos parametrus.</span><span class="sxs-lookup"><span data-stu-id="875d0-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="875d0-134">Darbo klasės ID</span><span class="sxs-lookup"><span data-stu-id="875d0-134">Work class ID</span></span> | <span data-ttu-id="875d0-135">Darbo užsakymo tipas</span><span class="sxs-lookup"><span data-stu-id="875d0-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="875d0-136">Pardavimai</span><span class="sxs-lookup"><span data-stu-id="875d0-136">Sales</span></span> | <span data-ttu-id="875d0-137">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="875d0-137">Sales orders</span></span> |
        | <span data-ttu-id="875d0-138">Pardavimo užsakymų paėmimas</span><span class="sxs-lookup"><span data-stu-id="875d0-138">SO Pick</span></span> | <span data-ttu-id="875d0-139">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="875d0-139">Sales orders</span></span> |

1. <span data-ttu-id="875d0-140">Veiksmų srityje pasirinkite **Sistemos nurodytos darbo sekos užklausos**.</span><span class="sxs-lookup"><span data-stu-id="875d0-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="875d0-141">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="875d0-141">Select **Edit**.</span></span>
1. <span data-ttu-id="875d0-142">Panaikinkite esamą eilutę ir patvirtinkite veiksmą pasirinkdami **Taip**.</span><span class="sxs-lookup"><span data-stu-id="875d0-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="875d0-143">Veiksmų srityje pasirinkite **Nauja** eilutei sukurti.</span><span class="sxs-lookup"><span data-stu-id="875d0-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="875d0-144">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="875d0-145">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="875d0-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="875d0-146">**Aprašymo laukas:** *Darbo kiekis yra mažesnis nei 20 ir Mažėjimo tvarka*</span><span class="sxs-lookup"><span data-stu-id="875d0-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="875d0-147">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="875d0-147">Select **Save**.</span></span>
1. <span data-ttu-id="875d0-148">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="875d0-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="875d0-149">Skirtuke **Sujungimas** išplėskite jungties hierarchiją lentelei **Darbo eilutės** rodyti.</span><span class="sxs-lookup"><span data-stu-id="875d0-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="875d0-150">Pasirinkite **Darbo eilučių** lentelės sujungimą.</span><span class="sxs-lookup"><span data-stu-id="875d0-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="875d0-151">Pasirinkite **Pridėti lentelės sujungimą**.</span><span class="sxs-lookup"><span data-stu-id="875d0-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="875d0-152">Atsiradusiame sąraše suraskite ir pasirinkite eilutę su šiais parametrais:</span><span class="sxs-lookup"><span data-stu-id="875d0-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="875d0-153">**Sujungimo režimas:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="875d0-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="875d0-154">**Ryšys:** *Vietos (Vieta)*</span><span class="sxs-lookup"><span data-stu-id="875d0-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="875d0-155">Pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="875d0-155">Select **Select**.</span></span>

    <span data-ttu-id="875d0-156">Vietos pridedamos į lentelės sujungimą.</span><span class="sxs-lookup"><span data-stu-id="875d0-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="875d0-157">Skirtuke **Rūšiavimas** pasirinkite **Pridėti** naujai eilutei pridėti.</span><span class="sxs-lookup"><span data-stu-id="875d0-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="875d0-158">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="875d0-159">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="875d0-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="875d0-160">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="875d0-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="875d0-161">**Laukas:** *Darbo kiekis* (atsiradusiame pranešimo lauke pasirinkite **Taip** rūšiavimui į šį lauką įtraukti.)</span><span class="sxs-lookup"><span data-stu-id="875d0-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="875d0-162">**Ieškos kryptis:** *Mažėjanti*</span><span class="sxs-lookup"><span data-stu-id="875d0-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="875d0-163">Pasirinkite skirtuką **Diapazonas**.</span><span class="sxs-lookup"><span data-stu-id="875d0-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="875d0-164">Jei į seką reikia įtraukti tik specifinius darbo kriterijus, juos galima nurodyti skirtuke **Diapazonas**. Šiame pavyzdyje jūs norite įterpti tik tą darbą, kurio kiekis yra mažesnis nei 20 EA (mažiausias matavimo vienetas).</span><span class="sxs-lookup"><span data-stu-id="875d0-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="875d0-165">Atkreipkite dėmesį, kad kai kurios eilutės jau įtrauktos.</span><span class="sxs-lookup"><span data-stu-id="875d0-165">Notice that some lines are already included.</span></span> <span data-ttu-id="875d0-166">Nepašalinkite šių eilučių.</span><span class="sxs-lookup"><span data-stu-id="875d0-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="875d0-167">Pasirinkite **Įtraukti** eilutei įtraukti.</span><span class="sxs-lookup"><span data-stu-id="875d0-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="875d0-168">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="875d0-169">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="875d0-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="875d0-170">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="875d0-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="875d0-171">**Laukas:** *Atsargų darbo kiekis*</span><span class="sxs-lookup"><span data-stu-id="875d0-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="875d0-172">**Kriterijai:** *\<20* (mažiau nei 20)</span><span class="sxs-lookup"><span data-stu-id="875d0-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="875d0-173">Pasirinkite **Įtraukti** dar vienai eilutei įtraukti.</span><span class="sxs-lookup"><span data-stu-id="875d0-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="875d0-174">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="875d0-175">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="875d0-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="875d0-176">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="875d0-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="875d0-177">**Laukas:** *Darbo tipas*</span><span class="sxs-lookup"><span data-stu-id="875d0-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="875d0-178">**Kriterijai:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="875d0-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="875d0-179">Pasirinkite **Įtraukti** dar vienai eilutei įtraukti.</span><span class="sxs-lookup"><span data-stu-id="875d0-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="875d0-180">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="875d0-181">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="875d0-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="875d0-182">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="875d0-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="875d0-183">**Laukas:** *Vietos profilio ID*</span><span class="sxs-lookup"><span data-stu-id="875d0-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="875d0-184">**Kriterijai:** *!ETAPAS*</span><span class="sxs-lookup"><span data-stu-id="875d0-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="875d0-185">Įsitikinkite, kad šauktukas (*!*) yra prieš *ETAPĄ*.</span><span class="sxs-lookup"><span data-stu-id="875d0-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="875d0-186">Pasirinkite **Gerai** norėdami išsaugoti ir uždaryti užklausą.</span><span class="sxs-lookup"><span data-stu-id="875d0-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="875d0-187">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="875d0-187">Select **Save**.</span></span>
1. <span data-ttu-id="875d0-188">Uždarykite puslapį, kad sugrįžtumėte į **Mobiliojo įrenginio meniu elementų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="875d0-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="875d0-189">Šis nustatymas nurodo kriterijus, kurie bus naudojami norint pateikti tinkamus darbus mobiliojo įrenginio meniu elementui.</span><span class="sxs-lookup"><span data-stu-id="875d0-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="875d0-190">Jei prie užklausos pridėsite daugiau kriterijų eilučių, pirmiausia sistema naudos užklausos eilutę, kurios sekos numeris yra mažiausias.</span><span class="sxs-lookup"><span data-stu-id="875d0-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="875d0-191">Kitaip tariant, visi tinkami darbai, kurių sekos numeris yra 1, bus pristatyti vartotojui pirmiausia, o tada pristatyti visi 2 sekos numerio darbai.</span><span class="sxs-lookup"><span data-stu-id="875d0-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="875d0-192">Todėl, jei tam tikrą diapazoną ir rūšiavimą reikia naudoti kartu, jie turi būti nurodyti toje pačioje sistemos nurodytos darbo sekos užklausoje.</span><span class="sxs-lookup"><span data-stu-id="875d0-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="875d0-193">Atliekant šį nustatymą bus užfiksuojamas bet koks darbas, kurio bent vienoje eilutėje yra kiekis mažesnis nei 20 EA.</span><span class="sxs-lookup"><span data-stu-id="875d0-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="875d0-194">Todėl, jei darbas turi eilutę, kurioje kiekis yra lygus 20 EA arba didesnis, jis bus tinkamas, jei jame yra bent viena eilutė, kurioje kiekis yra mažesnis nei 20 AE.</span><span class="sxs-lookup"><span data-stu-id="875d0-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="875d0-195">Vietos nurodymai</span><span class="sxs-lookup"><span data-stu-id="875d0-195">Location directives</span></span>

<span data-ttu-id="875d0-196">Jei naudojate numatytuosius „Contoso“ duomenis, vietos nurodymų užklausos veiksmui nereikalingi pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="875d0-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="875d0-197">Tačiau, siekiant užtikrinti, kad vietos nurodymuose bus užfiksuotos pardavimų užsakymų prekės, taikydami priemonę ne „Contoso“ aplinkoje, sukurkite naują vietos nurodymą.</span><span class="sxs-lookup"><span data-stu-id="875d0-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="875d0-198">Norėdami patikrinti parodomosios aplinkos nustatymus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="875d0-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="875d0-199">Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Vietos direktyvos**.</span><span class="sxs-lookup"><span data-stu-id="875d0-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="875d0-200">Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="875d0-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="875d0-201">Pasirinkite vietos nurodymą pavadinimu *51 paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="875d0-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="875d0-202">„FastTab“ skirtuke **Vietos direktyvos veiksmai** pasirinkite eilutę **Paėmimo** veiksmui.</span><span class="sxs-lookup"><span data-stu-id="875d0-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="875d0-203">Pasirinkite **Redaguoti užklausą** virš tinklelio.</span><span class="sxs-lookup"><span data-stu-id="875d0-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="875d0-204">Peržiūrėti **Diapazono** užklausą.</span><span class="sxs-lookup"><span data-stu-id="875d0-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="875d0-205">Suraskite eilutę, kurioje **Laukas** yra nustatytas *Vieta*.</span><span class="sxs-lookup"><span data-stu-id="875d0-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="875d0-206">Įsitikinkite, kad laukas **Kriterijai** yra tuščias, t. y., nėra apribojimų.</span><span class="sxs-lookup"><span data-stu-id="875d0-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="875d0-207">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="875d0-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="875d0-208">Pardavimo užsakymo paėmimo darbo užduoties sukūrimas</span><span class="sxs-lookup"><span data-stu-id="875d0-208">Create sales order picking work</span></span>

<span data-ttu-id="875d0-209">Prieš vykdant sistemos nurodytą paėmimą, reikia sukurti kai kuriuos siuntimo darbus.</span><span class="sxs-lookup"><span data-stu-id="875d0-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="875d0-210">Šiame scenarijuje sukursite keturis pardavimo užsakymus, pagrįstus nurodytomis sistemos nurodytos darbo sekos užklausomis.</span><span class="sxs-lookup"><span data-stu-id="875d0-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="875d0-211">Jūs rezervuosite atsargų kiekį kiekvienam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="875d0-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="875d0-212">Todėl kitiems užsakymams rezervuotų atsargų iš sandėlio paimti negalima, jei atsargų rezervavimas arba dalis atsargų rezervavimo nėra atšaukti.</span><span class="sxs-lookup"><span data-stu-id="875d0-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="875d0-213">Tada išleisite kiekvieną pardavimo užsakymą į sandėlį siuntimo darbui sukurti.</span><span class="sxs-lookup"><span data-stu-id="875d0-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="875d0-214">Pardavimo užsakymas 1</span><span class="sxs-lookup"><span data-stu-id="875d0-214">Sales order 1</span></span>

1. <span data-ttu-id="875d0-215">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="875d0-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="875d0-216">Veiksmų srityje pasirinkite **Nauja** sukurti pardavimo užsakymą 1.</span><span class="sxs-lookup"><span data-stu-id="875d0-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="875d0-217">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="875d0-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="875d0-218">„FastTab” skirtuke **Klientas** lauką **Kliento paskyra** nustatykite į *US–004*.</span><span class="sxs-lookup"><span data-stu-id="875d0-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="875d0-219">Skirtuke **Bendra** lauką **Sandėlis** nustatykite į *51*.</span><span class="sxs-lookup"><span data-stu-id="875d0-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="875d0-220">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="875d0-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="875d0-221">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="875d0-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="875d0-222">Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="875d0-223">**Prekės numeris:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="875d0-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="875d0-224">**Kiekis:** *20*</span><span class="sxs-lookup"><span data-stu-id="875d0-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="875d0-225">Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="875d0-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="875d0-226">Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** atsargų rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="875d0-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="875d0-227">Uždarykite **Rezervavimas** puslapį.</span><span class="sxs-lookup"><span data-stu-id="875d0-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="875d0-228">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį** sandėlio darbo užduočiai sukurti.</span><span class="sxs-lookup"><span data-stu-id="875d0-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="875d0-229">Gausite informacinius pranešimus apie sandėlio bangos ID ir siuntos ID, sukurtus šiam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="875d0-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="875d0-230">Pardavimo užsakymas 2</span><span class="sxs-lookup"><span data-stu-id="875d0-230">Sales order 2</span></span>

1. <span data-ttu-id="875d0-231">Veiksmų srityje pasirinkite **Nauja** pardavimo užsakymui 2 sukurti.</span><span class="sxs-lookup"><span data-stu-id="875d0-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="875d0-232">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="875d0-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="875d0-233">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="875d0-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="875d0-234">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="875d0-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="875d0-235">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="875d0-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="875d0-236">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="875d0-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="875d0-237">Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="875d0-238">**Prekės numeris:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="875d0-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="875d0-239">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="875d0-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="875d0-240">Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="875d0-241">**Prekės numeris:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="875d0-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="875d0-242">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="875d0-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="875d0-243">Rezervuoti abiejų eilučių atsargas.</span><span class="sxs-lookup"><span data-stu-id="875d0-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="875d0-244">Išleisti pardavimo užsakymus i sandėlį.</span><span class="sxs-lookup"><span data-stu-id="875d0-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="875d0-245">Pardavimo užsakymas 3</span><span class="sxs-lookup"><span data-stu-id="875d0-245">Sales order 3</span></span>

1. <span data-ttu-id="875d0-246">Veiksmų srityje pasirinkite **Nauja** sukurti pardavimo užsakymą 3.</span><span class="sxs-lookup"><span data-stu-id="875d0-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="875d0-247">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="875d0-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="875d0-248">**Kliento sąskaita:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="875d0-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="875d0-249">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="875d0-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="875d0-250">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="875d0-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="875d0-251">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="875d0-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="875d0-252">Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="875d0-253">**Prekės numeris:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="875d0-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="875d0-254">**Kiekis:** *7*</span><span class="sxs-lookup"><span data-stu-id="875d0-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="875d0-255">Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="875d0-256">**Prekės numeris:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="875d0-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="875d0-257">**Kiekis:** *8*</span><span class="sxs-lookup"><span data-stu-id="875d0-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="875d0-258">Rezervuoti abiejų eilučių atsargas.</span><span class="sxs-lookup"><span data-stu-id="875d0-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="875d0-259">Išleisti pardavimo užsakymus i sandėlį.</span><span class="sxs-lookup"><span data-stu-id="875d0-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="875d0-260">Pardavimo užsakymas 4</span><span class="sxs-lookup"><span data-stu-id="875d0-260">Sales order 4</span></span>

1. <span data-ttu-id="875d0-261">Veiksmų srityje pasirinkite **Nauja** 4 pardavimo užsakymui sukurti.</span><span class="sxs-lookup"><span data-stu-id="875d0-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="875d0-262">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="875d0-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="875d0-263">**Kliento sąskaita:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="875d0-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="875d0-264">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="875d0-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="875d0-265">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="875d0-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="875d0-266">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="875d0-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="875d0-267">Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="875d0-268">**Prekės numeris:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="875d0-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="875d0-269">**Kiekis:** *25*</span><span class="sxs-lookup"><span data-stu-id="875d0-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="875d0-270">Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="875d0-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="875d0-271">**Prekės numeris:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="875d0-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="875d0-272">**Kiekis:** *10*</span><span class="sxs-lookup"><span data-stu-id="875d0-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="875d0-273">Rezervuoti abiejų eilučių atsargas.</span><span class="sxs-lookup"><span data-stu-id="875d0-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="875d0-274">Išleisti pardavimo užsakymus i sandėlį.</span><span class="sxs-lookup"><span data-stu-id="875d0-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="875d0-275">Gauti darbo ID sukurtiems darbams</span><span class="sxs-lookup"><span data-stu-id="875d0-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="875d0-276">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="875d0-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="875d0-277">Filtruokite lauką **Sandėlis,** kad būtų rodomas tik *51* sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="875d0-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="875d0-278">Turėtų būti sukurti keturi darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-278">Four work IDs should have been created.</span></span> <span data-ttu-id="875d0-279">Pasižymėkite kiekvieno pardavimo užsakymo darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="875d0-280">Pardavimo užsakymo ID</span><span class="sxs-lookup"><span data-stu-id="875d0-280">Sales order ID</span></span> | <span data-ttu-id="875d0-281">Darbo ID</span><span class="sxs-lookup"><span data-stu-id="875d0-281">Work ID</span></span> | <span data-ttu-id="875d0-282">Darbo kiekis</span><span class="sxs-lookup"><span data-stu-id="875d0-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="875d0-283">Pardavimo užsakymas 1</span><span class="sxs-lookup"><span data-stu-id="875d0-283">Sales Order 1</span></span> | <span data-ttu-id="875d0-284">Darbo ID 1</span><span class="sxs-lookup"><span data-stu-id="875d0-284">Work ID 1</span></span> | <span data-ttu-id="875d0-285">20 EA</span><span class="sxs-lookup"><span data-stu-id="875d0-285">20 ea</span></span> |
    | <span data-ttu-id="875d0-286">Pardavimo užsakymas 2</span><span class="sxs-lookup"><span data-stu-id="875d0-286">Sales Order 2</span></span> | <span data-ttu-id="875d0-287">Darbo ID 2</span><span class="sxs-lookup"><span data-stu-id="875d0-287">Work ID 2</span></span> | <span data-ttu-id="875d0-288">6 EA (abiejų eilučių suma)</span><span class="sxs-lookup"><span data-stu-id="875d0-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="875d0-289">Pardavimo užsakymas 3</span><span class="sxs-lookup"><span data-stu-id="875d0-289">Sales Order 3</span></span> | <span data-ttu-id="875d0-290">Darbo ID 3</span><span class="sxs-lookup"><span data-stu-id="875d0-290">Work ID 3</span></span> | <span data-ttu-id="875d0-291">15 EA (abiejų eilučių suma)</span><span class="sxs-lookup"><span data-stu-id="875d0-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="875d0-292">Pardavimo užsakymas 4</span><span class="sxs-lookup"><span data-stu-id="875d0-292">Sales Order 4</span></span> | <span data-ttu-id="875d0-293">Darbo ID 4</span><span class="sxs-lookup"><span data-stu-id="875d0-293">Work ID 4</span></span> | <span data-ttu-id="875d0-294">35 EA (abiejų eilučių suma)</span><span class="sxs-lookup"><span data-stu-id="875d0-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="875d0-295">Prieš paleisdami mobiliojo įrenginio srautą, įsitikinkite, kad sukurtas darbo statusas yra *Atviras* *51* sandėliui ir *Pardavimo užsakymo* darbo užsakymo tipui.</span><span class="sxs-lookup"><span data-stu-id="875d0-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="875d0-296">Kitu atveju tikrinimo rezultatai gali skirtis, nes sistemos nurodytas paėmimas apims visą tinkamą darbą.</span><span class="sxs-lookup"><span data-stu-id="875d0-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="875d0-297">Eikite į **Sandėlio valdymas \>Darbas \> Siunčiama \> Atviri pardavimo darbai**.</span><span class="sxs-lookup"><span data-stu-id="875d0-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="875d0-298">Filtruokite tinklelio **Atviri pardavimo darbai** lauką **Sandėlis,** kad būtų rodomas tik *51* sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="875d0-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="875d0-299">Patikrinkite, ar rodomi tik keturi anksčiau sukurti darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="875d0-300">Uždarykite puslapį **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="875d0-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="875d0-301">Mobiliojo įrenginio srauto vykdymas</span><span class="sxs-lookup"><span data-stu-id="875d0-301">Mobile device flow execution</span></span>

<span data-ttu-id="875d0-302">Atsižvelgiant į nustatymą, sistema naudos vartotojo darbą, kuris yra surūšiuotas iš didžiausio darbo eilutės kiekio į žemiausią.</span><span class="sxs-lookup"><span data-stu-id="875d0-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="875d0-303">Kiekis kiekvienoje eilutėje bus mažesnis nei 20 AE.</span><span class="sxs-lookup"><span data-stu-id="875d0-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="875d0-304">Atminkite, kad atliekant ši nustatymą bus užfiksuojamas bet koks darbas, kurio bent vienoje eilutėje kiekis yra mažesnis nei 20 EA.</span><span class="sxs-lookup"><span data-stu-id="875d0-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="875d0-305">Todėl, jei darbas turi kitą eilutę, kurioje kiekis yra lygus 20 EA ar daugiau kaip 20 EA, jis taip pat bus galiojantis.</span><span class="sxs-lookup"><span data-stu-id="875d0-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="875d0-306">Mobilioji programa</span><span class="sxs-lookup"><span data-stu-id="875d0-306">Mobile app</span></span>

1. <span data-ttu-id="875d0-307">Prisijunkite prie „Warehouse“ programėlės kaip vartotojas sandėlyje *51*.</span><span class="sxs-lookup"><span data-stu-id="875d0-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="875d0-308">Eikite į **Išsiųsti \> Pardavimų išrinkimo sistema**.</span><span class="sxs-lookup"><span data-stu-id="875d0-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="875d0-309">Pateiktas darbo ID *4* išrinkimo veiksmas.</span><span class="sxs-lookup"><span data-stu-id="875d0-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="875d0-310">Šis darbo ID yra pateikiamas pirmiausia dėl sistemos nurodytos užklausų sekos nustatymo, kuriame nurodėte, kad darbas turi būti nustatytas pagal darbo eilutės kiekį mažėjimo tvarka.</span><span class="sxs-lookup"><span data-stu-id="875d0-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="875d0-311">Užpildykite reikiamą išrinkimą ir uždarykite darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="875d0-312">Tada pristatomas *3* darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="875d0-313">Viena iš darbo eilučių yra sekoje, kuri pagrįsta darbo eilutės kiekiu.</span><span class="sxs-lookup"><span data-stu-id="875d0-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="875d0-314">Užpildykite išrinkimą ir uždarykite darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="875d0-315">Tada pristatomas *2* darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="875d0-316">Ši darbo išrinkimo eilutė yra sekoje.</span><span class="sxs-lookup"><span data-stu-id="875d0-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="875d0-317">Užpildykite išrinkimą ir uždarykite darbo ID.</span><span class="sxs-lookup"><span data-stu-id="875d0-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="875d0-318">Jums nereikia pateikti jokio tolesnio darbo.</span><span class="sxs-lookup"><span data-stu-id="875d0-318">No further work should be presented to you.</span></span> <span data-ttu-id="875d0-319">Darbo ID *1* neatitinka šio mobiliojo įrenginio meniu elemento, nes užklausa nurodo, kad darbo antraštės bus nagrinėjamos tik tuo atveju, jei darbo eilutėse esantis kiekis yra mažesnis nei 20 AE.</span><span class="sxs-lookup"><span data-stu-id="875d0-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="875d0-320">Patarimai</span><span class="sxs-lookup"><span data-stu-id="875d0-320">Tips</span></span>

<span data-ttu-id="875d0-321">Sistemos nukreiptos darbo sekos užklausos yra *imtinai*.</span><span class="sxs-lookup"><span data-stu-id="875d0-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="875d0-322">Svarbu, kad atsimintumėte šį faktą kai kuriems nustatymams.</span><span class="sxs-lookup"><span data-stu-id="875d0-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="875d0-323">Pavyzdžiui, jūs norite, kad tam tikras meniu elementas būtų vykdomas tik tada, kai darbo vienetas yra *EA* ir užklausoje nurodote, kad apribojimas būtų taikomas tik skirtuke **Diapazonas**.</span><span class="sxs-lookup"><span data-stu-id="875d0-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="875d0-324">Tokiu atveju visas darbas, kurio bent viena darbo eilutė turi darbo vienetą, nustatytą *EA,* bus perduodamas darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="875d0-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="875d0-325">Todėl šis darbas taip pat gali apimti darbą, kurio darbo eilučių darbo vienetas nėra *EA* (pvz., *dėžė* arba *padėklas)*.</span><span class="sxs-lookup"><span data-stu-id="875d0-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="875d0-326">Užklausa neįtrauks tik darbo, kurio eilutė neturi darbo vieneto, nustatyto *EA*.</span><span class="sxs-lookup"><span data-stu-id="875d0-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="875d0-327">Todėl, šio scenarijaus pavyzdyje, darbo ID *4* taip pat buvo užfiksuotas naudojant užklausą.</span><span class="sxs-lookup"><span data-stu-id="875d0-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="875d0-328">Sukūrus užklausą, buvo pridėtos dvi eilutės: viena 25 EA ir kita 10 EA.</span><span class="sxs-lookup"><span data-stu-id="875d0-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="875d0-329">Šis darbas vis dar pateikiamas vartotojui, nes bent vienoje darbo eilutėje yra mažiau nei 20 EA.</span><span class="sxs-lookup"><span data-stu-id="875d0-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="875d0-330">Atsižvelgiant į scenarijų, šios problemos galima išvengti naudojant darbo pertraukas.</span><span class="sxs-lookup"><span data-stu-id="875d0-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]