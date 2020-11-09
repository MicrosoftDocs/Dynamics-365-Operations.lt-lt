---
title: Sandėlio intervalas
description: Šioje temoje pateikiama informacija apie sandėlio intervalą. Sandėlio intervalas leidžia konsoliduoti poreikį pagal prekę ir matavimo vienetą iš užsakymų, kurių būsena yra Užsakytas, Rezervuotas arba Išleistas. Jis padeda sandėlio vadovams sumaniai planuoti paėmimų vietas dar prieš tai, kai jos išleidžia užsakymus į sandėlį ir sukuria paėmimų darbą.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017419"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="1590c-105">Sandėlio intervalas</span><span class="sxs-lookup"><span data-stu-id="1590c-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1590c-106">Sandėlio intervalas leidžia konsoliduoti poreikį pagal prekę ir matavimo vienetą iš užsakymų, kurių būsena yra *Užsakytas* , *Rezervuotas* arba *Išleistas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="1590c-107">Sugeneruota paklausa gali būti taikoma vietoms, kurios bus naudojamos paėmimui, atsižvelgiant į kiekį, vienetą, faktines dimensijas, fiksuotas vietas ir kita.</span><span class="sxs-lookup"><span data-stu-id="1590c-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="1590c-108">Po to, kai buvo sukurtas intervalo planas, papildymo darbas gali būti sukurtas tam, kad būtų galima pasiekti reikiamą atsargų kiekį kiekvienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="1590c-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="1590c-109">Ši funkcija padeda sandėlio vadovams sumaniai planuoti paėmimų vietas dar prieš tai, kai jos išleidžia užsakymus į sandėlį ir sukuria paėmimų darbą.</span><span class="sxs-lookup"><span data-stu-id="1590c-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="1590c-110">Sandėlio intervalo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="1590c-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="1590c-111">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1590c-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1590c-112">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="1590c-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1590c-113">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="1590c-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1590c-114">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="1590c-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1590c-115">**Funkcijos pavadinimas** *Sandėlio intervalo funkcija*</span><span class="sxs-lookup"><span data-stu-id="1590c-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="1590c-116">Sandėlio intervalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1590c-116">Set up warehouse slotting</span></span>

<span data-ttu-id="1590c-117">Norėdami naudoti šią funkciją, turite nustatyti šiuos elementus sistemoje:</span><span class="sxs-lookup"><span data-stu-id="1590c-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="1590c-118">Kurti matavimo vieneto pakopas intervalui</span><span class="sxs-lookup"><span data-stu-id="1590c-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="1590c-119">Matavimo vienetų pakopos įgalina sugrupuoti kelis matavimo vienetus, kad juos būtų galima nustatyti.</span><span class="sxs-lookup"><span data-stu-id="1590c-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="1590c-120">Pavyzdžiui, jei kelių dydžių dėžės paimamos iš tos pačios dėžių paėmimo srities, visiems dydžiams galima sukurti vieną pakopą.</span><span class="sxs-lookup"><span data-stu-id="1590c-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="1590c-121">**Turi būti sukurta kiekvieno matavimo vieneto eilutė, kuri turėtų būti pakopos dalis.**</span><span class="sxs-lookup"><span data-stu-id="1590c-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="1590c-122">Eikite į **Sandėlio valdymas \>Nustatymas \>Papildymas \> Matavimo vienetų pakopų intervalas**.</span><span class="sxs-lookup"><span data-stu-id="1590c-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="1590c-123">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1590c-123">Select **New**.</span></span>
1. <span data-ttu-id="1590c-124">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="1590c-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="1590c-125">**Matavimo vieneto pakopa:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="1590c-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="1590c-126">**Aprašymas:** *Kiekviena dėžės paletė*</span><span class="sxs-lookup"><span data-stu-id="1590c-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="1590c-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1590c-127">Select **Save**.</span></span>
1. <span data-ttu-id="1590c-128">„FastTab“ skirtuke **Matavimo vienetai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="1590c-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1590c-129">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-130">**Vienetas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="1590c-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="1590c-131">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="1590c-132">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="1590c-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="1590c-133">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="1590c-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="1590c-134">Pasirinkite **Nauja** , kad įtrauktumėte antrą eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="1590c-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="1590c-135">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-136">**Vienetas:** *ea*</span><span class="sxs-lookup"><span data-stu-id="1590c-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="1590c-137">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="1590c-138">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="1590c-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="1590c-139">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="1590c-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="1590c-140">Pasirinkite **Nauja** , kad įtrauktumėte trečią eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="1590c-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="1590c-141">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-142">**Vienetas:** *PL*</span><span class="sxs-lookup"><span data-stu-id="1590c-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="1590c-143">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="1590c-144">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="1590c-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="1590c-145">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="1590c-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="1590c-146">Pasirinkite **Įrašyti** , kad įrašytumėte pakopą.</span><span class="sxs-lookup"><span data-stu-id="1590c-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="1590c-147">Kurti nurodymo kodą, skirtą intervalui</span><span class="sxs-lookup"><span data-stu-id="1590c-147">Create a directive code for slotting</span></span>

<span data-ttu-id="1590c-148">Turite pasirinkti nurodymo kodą, kuris turi būti susietas su šablonu.</span><span class="sxs-lookup"><span data-stu-id="1590c-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="1590c-149">Eikite į **Sandėlio valdymas \> Nustatymas \> Nurodymų kodai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="1590c-150">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1590c-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1590c-151">**Nurodymo kodas** lauke įveskite *Intervalas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="1590c-152">**Nurodymo aprašymas** lauke įveskite *Intervalas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="1590c-153">Intervalo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1590c-153">Set up slotting templates</span></span>

<span data-ttu-id="1590c-154">Kiekvienas intervalo šablonas kontroliuoja atsargų priskyrimui tam tikroms sandėlio vietoms.</span><span class="sxs-lookup"><span data-stu-id="1590c-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="1590c-155">Kiekviename šablone turi būti eilutė kiekvieno intervalo specifikacijai.</span><span class="sxs-lookup"><span data-stu-id="1590c-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="1590c-156">Norėdami nustatyti intervalo šablonus, naudokite šiame skyriuje nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="1590c-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="1590c-157">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Papildymas \> Intervalo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="1590c-158">Pasirinkite **Naujas** , kad sukurtumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="1590c-158">Select **New** to create a template.</span></span>

<span data-ttu-id="1590c-159">Toliau turite nustatyti šablono antraštę, intervalo specifikacijas ir vietos nurodymus, kaip paaiškinta šiuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="1590c-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="1590c-160">Intervalo šablono antraštės Nustatymas</span><span class="sxs-lookup"><span data-stu-id="1590c-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="1590c-161">Šablono antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="1590c-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="1590c-162">**Intervalo šablonas:** _61_</span><span class="sxs-lookup"><span data-stu-id="1590c-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="1590c-163">**Aprašas:** _61_</span><span class="sxs-lookup"><span data-stu-id="1590c-163">**Description:** _61_</span></span>
    - <span data-ttu-id="1590c-164">**Reikalaujamas tipas:** *Pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="1590c-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="1590c-165">Šiuo metu palaikomas tik vienas reikalaujamas tipas *Pardavimo užsakymas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="1590c-166">**Reikalaujama strategija:** _Užsakyta_</span><span class="sxs-lookup"><span data-stu-id="1590c-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="1590c-167">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="1590c-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="1590c-168">**Užsakyta** – Pardavimo užsakyme visas užsakytas kiekis turi būti laikomas paklausa.</span><span class="sxs-lookup"><span data-stu-id="1590c-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="1590c-169">**Rezervuota** – Rezervuoti (faktiniai ir užsakyti) pardavimo užsakymo eilutės kiekiai yra laikomi paklausa.</span><span class="sxs-lookup"><span data-stu-id="1590c-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="1590c-170">**Sandėlis:** _61_</span><span class="sxs-lookup"><span data-stu-id="1590c-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="1590c-171">**Leisti bangai reikalauti naudoti nerezervuotus kiekius:** _Taip_</span><span class="sxs-lookup"><span data-stu-id="1590c-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="1590c-172">Taip pat galite nurodyti užklausą, kuri susiaurina vertinamą paklausą.</span><span class="sxs-lookup"><span data-stu-id="1590c-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="1590c-173">Intervalo specifikacijų kiekvienam darbo šablonui nustatymas</span><span class="sxs-lookup"><span data-stu-id="1590c-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="1590c-174">Kiekvienam sukurtam šablonui atlikite šiuos veiksmus, kad pridėtumėte eilutę kiekvienai intervalo specifikacijai.</span><span class="sxs-lookup"><span data-stu-id="1590c-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="1590c-175">Norėdami sukurti naują šablono eilutę, „FastTab” skirtuke **Nauja** pasirinkite **Išsami intervalo šablono informacija**.</span><span class="sxs-lookup"><span data-stu-id="1590c-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="1590c-176">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-177">**Seka:** _1_</span><span class="sxs-lookup"><span data-stu-id="1590c-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="1590c-178">**Aprašymas:** _Fiksuota vieta_</span><span class="sxs-lookup"><span data-stu-id="1590c-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="1590c-179">**Mažiausias kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="1590c-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="1590c-180">Šis laukas nurodo minimalų paklausos kiekį, kurio reikia eilutei.</span><span class="sxs-lookup"><span data-stu-id="1590c-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="1590c-181">**Maksimalus kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="1590c-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="1590c-182">Šis laukas nurodo maksimalų paklausos kiekį, kuris galioja eilutei.</span><span class="sxs-lookup"><span data-stu-id="1590c-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="1590c-183">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="1590c-184">Šiame lauke apibrėžiamas matavimo vienetas, kurį nurodo minimalus ir maksimalus kiekis.</span><span class="sxs-lookup"><span data-stu-id="1590c-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="1590c-185">**Matavimo vieneto pakopa:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="1590c-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="1590c-186">Šis laukas nurodo paklausos matavimo vienetus, kurie galioja eilutei.</span><span class="sxs-lookup"><span data-stu-id="1590c-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="1590c-187">(Norėdami gauti daugiau informacijos, žr. šios temos skyrių [Matavimo vienetų pakopos intervalui](#unit-tiers).)</span><span class="sxs-lookup"><span data-stu-id="1590c-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="1590c-188">**Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_</span><span class="sxs-lookup"><span data-stu-id="1590c-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="1590c-189">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="1590c-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="1590c-190">**Tarkime, kad tuščia** – Šioje sistemoje daroma prielaida, kad visos vietos iš paėmimo srities, yra tuščios ir nereiktų patikrinti šių vietų dėl atsargų.</span><span class="sxs-lookup"><span data-stu-id="1590c-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="1590c-191">**Atsižvelgti į kiekį** – Ši sistema patikrina visas vietas iš paėmimo srities dėl atsargų, ir turėtų praleisti visas vietas, kurios nėra tuščios.</span><span class="sxs-lookup"><span data-stu-id="1590c-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="1590c-192">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="1590c-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="1590c-193">Šiame lauke apibrėžiama vietos nurodymas, kuri naudojamas papildymo darbo paėmimų vietai rasti.</span><span class="sxs-lookup"><span data-stu-id="1590c-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="1590c-194">**Perpildos vieta:** palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="1590c-195">Šis laukas nurodo vietą, į kurią yra įtrauktas atsargų kiekis, jei vietos negalima rasti, kai eilutė yra apdorojama.</span><span class="sxs-lookup"><span data-stu-id="1590c-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="1590c-196">**Leisti** _taip_</span><span class="sxs-lookup"><span data-stu-id="1590c-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="1590c-197">Jei ši parinktis nustatyta kaip *Taip* , jei bet koks reikalavimas negali būti įvykdytas, perkėlimo darbas bus sukurtas, kad būtų galima paimti atsargas iš vietų, kuriose yra atsargų, tačiau kur niekas nebuvo paimta.</span><span class="sxs-lookup"><span data-stu-id="1590c-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="1590c-198">Tada šablonas paleidžiamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="1590c-198">The template is then run again.</span></span> <span data-ttu-id="1590c-199">Šiuo metu nepaisoma vietų atsargų.</span><span class="sxs-lookup"><span data-stu-id="1590c-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="1590c-200">Ši funkcija veikia geriausiai, kai laukas **Priskirti intervalo kriterijų** nustatomas į _Atsižvelgti į kiekį_.</span><span class="sxs-lookup"><span data-stu-id="1590c-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="1590c-201">**Fiksuotos vietos naudojimas:** _Galima naudoti tik fiksuotas produkto vietas_</span><span class="sxs-lookup"><span data-stu-id="1590c-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="1590c-202">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="1590c-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="1590c-203">**Fiksuotos ir nefiksuotos vietos** – Sistema neapribojama naudoti tik fiksuotas vietas.</span><span class="sxs-lookup"><span data-stu-id="1590c-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="1590c-204">**Tik fiksuotos produkto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto vietos.</span><span class="sxs-lookup"><span data-stu-id="1590c-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="1590c-205">**Tik fiksuotos produkto varianto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto varianto vietos.</span><span class="sxs-lookup"><span data-stu-id="1590c-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="1590c-206">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1590c-206">Select **Save**.</span></span>
1. <span data-ttu-id="1590c-207">Pasirinkite **Naujas** , kad sukurtumėte antrą šablono eilutę.</span><span class="sxs-lookup"><span data-stu-id="1590c-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="1590c-208">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-209">**Seka:** _2_</span><span class="sxs-lookup"><span data-stu-id="1590c-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="1590c-210">**Aprašymas:** _Kita_</span><span class="sxs-lookup"><span data-stu-id="1590c-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="1590c-211">**Minimalus kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="1590c-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="1590c-212">**Maksimalus kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="1590c-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="1590c-213">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="1590c-214">**Matavimo vieneto pakopa:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="1590c-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="1590c-215">**Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_</span><span class="sxs-lookup"><span data-stu-id="1590c-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="1590c-216">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="1590c-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="1590c-217">**Perpildos vieta:** palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1590c-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="1590c-218">**Leisti** _taip_</span><span class="sxs-lookup"><span data-stu-id="1590c-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="1590c-219">**Fiksuotos vietos naudojimas:** _Fiksuotos ir nefiksuotos vietos_</span><span class="sxs-lookup"><span data-stu-id="1590c-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="1590c-220">Antrojoje eilutėje,dabar bus nurodyti kriterijai, naudojami nustatyti, kokiose vietose gali būti padarytos tos eilutės paklausa.</span><span class="sxs-lookup"><span data-stu-id="1590c-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="1590c-221">Pasirinktie eilutę, kurios **Seka** yra nustatyta į *2*.</span><span class="sxs-lookup"><span data-stu-id="1590c-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="1590c-222">Pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="1590c-223">Skirtuke **Diapazonas** pasirinkite **Pridėti** , kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="1590c-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="1590c-224">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-225">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="1590c-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="1590c-226">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="1590c-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="1590c-227">**Laukas:** *Vietos profilio ID*</span><span class="sxs-lookup"><span data-stu-id="1590c-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="1590c-228">**Kriterijai:** lauke *Pick-06* (pasirinkite dvigubą pliuso ženklą \[**++**\], kad išplėstumėte sąrašą, tada pasirinkite *Pick-06* - *Paėmimo vieta 6*.)</span><span class="sxs-lookup"><span data-stu-id="1590c-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="1590c-229">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="1590c-230">Nustatyti vietos nurodymus</span><span class="sxs-lookup"><span data-stu-id="1590c-230">Set up location directives</span></span>

<span data-ttu-id="1590c-231">Reikia nustatyti bent vieną vietos nurodymą, kad būtų palaikomi intervalo paėmimai.</span><span class="sxs-lookup"><span data-stu-id="1590c-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="1590c-232">Naudokite šiame skyriuje nurodytas procedūras, kad nustatytumėte naują *papildymo vietos nurodymą* , skirtą paėmimams.</span><span class="sxs-lookup"><span data-stu-id="1590c-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="1590c-233">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1590c-234">Kairinės srities lauke **Darbo užsakymo tipas** pasirinkite *Papildymas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="1590c-235">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1590c-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1590c-236">Naujo vietos nurodymo antraštės lauke **Pavadinimas** , įveskite *61 intervalo paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="1590c-237">Konfigūruokite vietų nurodymus „FastTab“ skirtuke</span><span class="sxs-lookup"><span data-stu-id="1590c-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="1590c-238">„FastTab“ skirtuke **Vietų nurodymai** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="1590c-239">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="1590c-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1590c-240">**Darbo tipas:** _Paėmimas_</span><span class="sxs-lookup"><span data-stu-id="1590c-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="1590c-241">**Vieta:** _6_</span><span class="sxs-lookup"><span data-stu-id="1590c-241">**Site:** _6_</span></span>
    - <span data-ttu-id="1590c-242">**Sandėlis:** _61_</span><span class="sxs-lookup"><span data-stu-id="1590c-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="1590c-243">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="1590c-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="1590c-244">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="1590c-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="1590c-245">Konfigūruoti „FastTab“ skirtuką Eilutės</span><span class="sxs-lookup"><span data-stu-id="1590c-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="1590c-246">„FastTab“ skirtuke **Eilutės** spustelėję **Nauja** sukursite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="1590c-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="1590c-247">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-247">On the new line, set the following values.</span></span> <span data-ttu-id="1590c-248">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="1590c-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1590c-249">**Pradinis kiekis:** _0_</span><span class="sxs-lookup"><span data-stu-id="1590c-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="1590c-250">**Galutinis kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="1590c-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="1590c-251">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="1590c-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="1590c-252">Konfigūruokite vietų nurodymų veiksmus „FastTab“ skirtuke</span><span class="sxs-lookup"><span data-stu-id="1590c-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="1590c-253">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="1590c-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="1590c-254">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-254">On the new line, set the following values.</span></span> <span data-ttu-id="1590c-255">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="1590c-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1590c-256">**Pavadinimas:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="1590c-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="1590c-257">**Strategija:** _Nėra_</span><span class="sxs-lookup"><span data-stu-id="1590c-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="1590c-258">Pasirinkite **Įrašyti** , kad būtų galima naudoti mygtuką **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="1590c-259">Redaguoti užklausą</span><span class="sxs-lookup"><span data-stu-id="1590c-259">Edit the query</span></span>

1. <span data-ttu-id="1590c-260">„FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="1590c-261">Skirtuke **Diapazonas** pasirinkite **Pridėti** , kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="1590c-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="1590c-262">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1590c-263">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="1590c-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="1590c-264">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="1590c-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="1590c-265">**Laukas:** *Zonos ID*</span><span class="sxs-lookup"><span data-stu-id="1590c-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="1590c-266">**Kriterijai:** *Bulk* (pasirinkite dvigubą pliuso ženklą \[**++**\] , kad išplėstumėte sąrašą, tada pasirinkite *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="1590c-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="1590c-267">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="1590c-268">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="1590c-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="1590c-269">Scenarijaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="1590c-269">Set up the scenario</span></span>

<span data-ttu-id="1590c-270">Šiame scenarijuje naudokite įtaisytuosius pavyzdžio duomenis ir kurkite šiame skyriuje aprašytus įrašus.</span><span class="sxs-lookup"><span data-stu-id="1590c-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="1590c-271">Naudoti USMF pavyzdinius duomenis</span><span class="sxs-lookup"><span data-stu-id="1590c-271">Use the USMF sample data</span></span>

<span data-ttu-id="1590c-272">Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1590c-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="1590c-273">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="1590c-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="1590c-274">Kurti paklausą</span><span class="sxs-lookup"><span data-stu-id="1590c-274">Create demand</span></span>

<span data-ttu-id="1590c-275">Atlikite šiuos veiksmus, kad sukurtumėte paklausą, kuriai taikysite intervalą.</span><span class="sxs-lookup"><span data-stu-id="1590c-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="1590c-276">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="1590c-277">Pasirinkite **Naujas** , kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1590c-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="1590c-278">Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-007_.</span><span class="sxs-lookup"><span data-stu-id="1590c-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="1590c-279">Lauke **Sandėlis** pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="1590c-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="1590c-280">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1590c-280">Select **OK**.</span></span>
1. <span data-ttu-id="1590c-281">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="1590c-281">The new sales order is opened.</span></span> <span data-ttu-id="1590c-282">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="1590c-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1590c-283">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="1590c-284">**Prekė:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="1590c-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="1590c-285">**Kiekis:** _20_</span><span class="sxs-lookup"><span data-stu-id="1590c-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="1590c-286">Pasirinkite **Įtraukti eilutę** naujai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="1590c-287">**Prekė:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="1590c-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="1590c-288">**Kiekis:** _8_</span><span class="sxs-lookup"><span data-stu-id="1590c-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="1590c-289">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1590c-289">Select **Save**.</span></span>
1. <span data-ttu-id="1590c-290">Pasirinkite **Naujas** , kad antrą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1590c-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="1590c-291">Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-008_.</span><span class="sxs-lookup"><span data-stu-id="1590c-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="1590c-292">Lauke **Sandėlis** pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="1590c-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="1590c-293">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="1590c-293">The new sales order is opened.</span></span> <span data-ttu-id="1590c-294">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="1590c-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1590c-295">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1590c-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="1590c-296">**Prekė:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="1590c-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="1590c-297">**Kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="1590c-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="1590c-298">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1590c-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="1590c-299">Naudokite įprastą intervalo scenarijų</span><span class="sxs-lookup"><span data-stu-id="1590c-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="1590c-300">Po to, kai yra visi būtini elementai, kaip aprašyta ankstesniame skyriuje, jūs esate pasirengę išbandyti šią funkciją dirbdami per kiekvieną šiame skyriuje esantį pratimą.</span><span class="sxs-lookup"><span data-stu-id="1590c-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="1590c-301">Generuoti paklausą</span><span class="sxs-lookup"><span data-stu-id="1590c-301">Generate demand</span></span>

1. <span data-ttu-id="1590c-302">Eikite į **Sandėlio valdymas \>Sąranka \> Papildymas \> Intervalo šablonai** ir pasirinkite norimą naudoti intervalo šabloną.</span><span class="sxs-lookup"><span data-stu-id="1590c-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="1590c-303">Veiksmų srityje spustelėkite **Generuoti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="1590c-304">Ši komanda įvertina visas paklausas, kurios yra sistemoje ir kurios atitinka intervalo šablono užklausą.</span><span class="sxs-lookup"><span data-stu-id="1590c-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="1590c-305">Bendra visų užsakymų paklausa yra konsoliduojama po vieną kiekvieno kiekio/matavimo vieneto eilutę.</span><span class="sxs-lookup"><span data-stu-id="1590c-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="1590c-306">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="1590c-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="1590c-307">Intervalo paklausa</span><span class="sxs-lookup"><span data-stu-id="1590c-307">Slotting demand</span></span>

<span data-ttu-id="1590c-308">Dėl to, kad yra intervalo šablono nustatymu, *Intervalo paklausa* parodo paklausos generavimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="1590c-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="1590c-309">Veiksmų srityje pasirinkite **Intervalo paklausa** norėdami peržiūrėti rezultatus iš komandos **Generuoti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="1590c-310">Intervalo paklausos eilutės gali būti redaguojamas.</span><span class="sxs-lookup"><span data-stu-id="1590c-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="1590c-311">Galite panaikinti eilutę, pridėti naują eilutę arba redaguoti eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="1590c-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="1590c-312">Galite redaguoti paklausą neautomatiniu būdu arba galite ją importuoti iš išorinės sistemos naudodami duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="1590c-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="1590c-313">Neatsižvelgiant į tai, iš kur intervalo paklausa yra, ji bus naudojamas atliekant tolesnį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="1590c-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="1590c-314">Surasti paklausą</span><span class="sxs-lookup"><span data-stu-id="1590c-314">Locate demand</span></span>

<span data-ttu-id="1590c-315">Kai paklausa sugeneruojama, turite naudoti komandą **Surasti paklausą,** kad būtų sugeneruotas *Intervalo planas*.</span><span class="sxs-lookup"><span data-stu-id="1590c-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="1590c-316">Veiksmų srityje spustelėkite **Surasti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="1590c-317">Paleidžiamas intervalo procesas.</span><span class="sxs-lookup"><span data-stu-id="1590c-317">The slotting process runs.</span></span> <span data-ttu-id="1590c-318">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="1590c-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="1590c-319">Intervalo planas</span><span class="sxs-lookup"><span data-stu-id="1590c-319">Slotting plan</span></span>

<span data-ttu-id="1590c-320">Intervalo planas nurodo vietą, kurioje buvo priskirta kiekviena prekė/kiekis, buvo panaudota perpilda, buvo sukurtas padėjimo darbas ar naudota šablono eilutė.</span><span class="sxs-lookup"><span data-stu-id="1590c-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="1590c-321">**Bet kokia paklausa, kurios negalima įvykdyti yra paryškintas raudonai.**</span><span class="sxs-lookup"><span data-stu-id="1590c-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="1590c-322">Veiksmų srityje pasirinkite **Intervalo planas,** norėdami peržiūrėti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="1590c-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="1590c-323">Sukurkite papildymą</span><span class="sxs-lookup"><span data-stu-id="1590c-323">Create replenishment</span></span>

<span data-ttu-id="1590c-324">Sukūrę planą, turite sukurti *Papildymo darbą* , pagrįstą planu.</span><span class="sxs-lookup"><span data-stu-id="1590c-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="1590c-325">Veiksmų srityje pasirinkite **Vykdyti papildymą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="1590c-326">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="1590c-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="1590c-327">Šis pranešimas nurodo antraščių, sukurtų darbo kūrimo ID, skaičių.</span><span class="sxs-lookup"><span data-stu-id="1590c-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="1590c-328">Vietos nurodymai, kurie bus naudojami, yra identifikuojami pagal nurodymo kodą, pateiktą kiekvienoje šablono eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1590c-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="1590c-329">Patarimai</span><span class="sxs-lookup"><span data-stu-id="1590c-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="1590c-330">Intervalo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1590c-330">Set up automatic slotting</span></span>

<span data-ttu-id="1590c-331">Po to, kai visi reikiami elementai yra, galite nustatyti automatinį valdymą, atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1590c-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="1590c-332">Eikite į **Sandėlio valdymas \> Papildymas \> Atlikti intervalą**.</span><span class="sxs-lookup"><span data-stu-id="1590c-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="1590c-333">Nurodykite paleidžiančius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1590c-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="1590c-334">Pasirinkite vieną ar daugiau iš šių intervalo veiksmų:</span><span class="sxs-lookup"><span data-stu-id="1590c-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="1590c-335">Generuoti paklausą</span><span class="sxs-lookup"><span data-stu-id="1590c-335">Generate demand</span></span>
    - <span data-ttu-id="1590c-336">Surasti paklausą</span><span class="sxs-lookup"><span data-stu-id="1590c-336">Locate demand</span></span>
    - <span data-ttu-id="1590c-337">Kurti papildymo darbą</span><span class="sxs-lookup"><span data-stu-id="1590c-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="1590c-338">Intervalo veiksmai yra progresyvūs.</span><span class="sxs-lookup"><span data-stu-id="1590c-338">The slotting steps are progressive.</span></span> <span data-ttu-id="1590c-339">Jei norite pasirinkti *Surasti paklausą* , pirmiausia turite pasirinkti *Generuoti paklausą*.</span><span class="sxs-lookup"><span data-stu-id="1590c-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="1590c-340">Nurodyti naudotiną šabloną.</span><span class="sxs-lookup"><span data-stu-id="1590c-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="1590c-341">Jei norėsite, pakartojimas paleidžiamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="1590c-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="1590c-342">Norėdami atlikti scenarijų pratimus, **ne** nustatykite automatinio intervalo.</span><span class="sxs-lookup"><span data-stu-id="1590c-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
