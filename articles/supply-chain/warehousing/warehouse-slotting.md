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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f6764f8bc082962af37d4775b6fe53d8704658eb
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597463"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="d3f03-105">Sandėlio intervalas</span><span class="sxs-lookup"><span data-stu-id="d3f03-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3f03-106">Sandėlio intervalas leidžia konsoliduoti poreikį pagal prekę ir matavimo vienetą iš užsakymų, kurių būsena yra *Užsakytas*, *Rezervuotas* arba *Išleistas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="d3f03-107">Sugeneruota paklausa gali būti taikoma vietoms, kurios bus naudojamos paėmimui, atsižvelgiant į kiekį, vienetą, faktines dimensijas, fiksuotas vietas ir kita.</span><span class="sxs-lookup"><span data-stu-id="d3f03-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="d3f03-108">Po to, kai buvo sukurtas intervalo planas, papildymo darbas gali būti sukurtas tam, kad būtų galima pasiekti reikiamą atsargų kiekį kiekvienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="d3f03-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="d3f03-109">Ši funkcija padeda sandėlio vadovams sumaniai planuoti paėmimų vietas dar prieš tai, kai jos išleidžia užsakymus į sandėlį ir sukuria paėmimų darbą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="d3f03-110">Sandėlio intervalo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="d3f03-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="d3f03-111">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="d3f03-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d3f03-112">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="d3f03-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d3f03-113">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="d3f03-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d3f03-114">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="d3f03-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d3f03-115">**Funkcijos pavadinimas** *Sandėlio intervalo funkcija*</span><span class="sxs-lookup"><span data-stu-id="d3f03-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="d3f03-116">Sandėlio intervalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3f03-116">Set up warehouse slotting</span></span>

<span data-ttu-id="d3f03-117">Norėdami naudoti šią funkciją, turite nustatyti šiuos elementus sistemoje:</span><span class="sxs-lookup"><span data-stu-id="d3f03-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="d3f03-118">Kurti matavimo vieneto pakopas intervalui</span><span class="sxs-lookup"><span data-stu-id="d3f03-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="d3f03-119">Matavimo vienetų pakopos įgalina sugrupuoti kelis matavimo vienetus, kad juos būtų galima nustatyti.</span><span class="sxs-lookup"><span data-stu-id="d3f03-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="d3f03-120">Pavyzdžiui, jei kelių dydžių dėžės paimamos iš tos pačios dėžių paėmimo srities, visiems dydžiams galima sukurti vieną pakopą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="d3f03-121">**Turi būti sukurta kiekvieno matavimo vieneto eilutė, kuri turėtų būti pakopos dalis.**</span><span class="sxs-lookup"><span data-stu-id="d3f03-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="d3f03-122">Eikite į **Sandėlio valdymas \>Nustatymas \>Papildymas \> Matavimo vienetų pakopų intervalas**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="d3f03-123">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-123">Select **New**.</span></span>
1. <span data-ttu-id="d3f03-124">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="d3f03-125">**Matavimo vieneto pakopa:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="d3f03-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="d3f03-126">**Aprašymas:** *Kiekviena dėžės paletė*</span><span class="sxs-lookup"><span data-stu-id="d3f03-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="d3f03-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-127">Select **Save**.</span></span>
1. <span data-ttu-id="d3f03-128">„FastTab“ skirtuke **Matavimo vienetai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="d3f03-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f03-129">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-130">**Vienetas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="d3f03-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="d3f03-131">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d3f03-132">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d3f03-133">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="d3f03-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d3f03-134">Pasirinkite **Nauja**, kad įtrauktumėte antrą eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="d3f03-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="d3f03-135">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-136">**Vienetas:** *ea*</span><span class="sxs-lookup"><span data-stu-id="d3f03-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="d3f03-137">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d3f03-138">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d3f03-139">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="d3f03-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d3f03-140">Pasirinkite **Nauja**, kad įtrauktumėte trečią eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="d3f03-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="d3f03-141">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-142">**Vienetas:** *PL*</span><span class="sxs-lookup"><span data-stu-id="d3f03-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="d3f03-143">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d3f03-144">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d3f03-145">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="d3f03-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d3f03-146">Pasirinkite **Įrašyti**, kad įrašytumėte pakopą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="d3f03-147">Kurti nurodymo kodą, skirtą intervalui</span><span class="sxs-lookup"><span data-stu-id="d3f03-147">Create a directive code for slotting</span></span>

<span data-ttu-id="d3f03-148">Turite pasirinkti nurodymo kodą, kuris turi būti susietas su šablonu.</span><span class="sxs-lookup"><span data-stu-id="d3f03-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="d3f03-149">Eikite į **Sandėlio valdymas \> Nustatymas \> Nurodymų kodai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="d3f03-150">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d3f03-151">**Nurodymo kodas** lauke įveskite *Intervalas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="d3f03-152">**Nurodymo aprašymas** lauke įveskite *Intervalas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="d3f03-153">Intervalo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3f03-153">Set up slotting templates</span></span>

<span data-ttu-id="d3f03-154">Kiekvienas intervalo šablonas kontroliuoja atsargų priskyrimui tam tikroms sandėlio vietoms.</span><span class="sxs-lookup"><span data-stu-id="d3f03-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="d3f03-155">Kiekviename šablone turi būti eilutė kiekvieno intervalo specifikacijai.</span><span class="sxs-lookup"><span data-stu-id="d3f03-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="d3f03-156">Norėdami nustatyti intervalo šablonus, naudokite šiame skyriuje nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="d3f03-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="d3f03-157">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Papildymas \> Intervalo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="d3f03-158">Pasirinkite **Naujas**, kad sukurtumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="d3f03-158">Select **New** to create a template.</span></span>

<span data-ttu-id="d3f03-159">Toliau turite nustatyti šablono antraštę, intervalo specifikacijas ir vietos nurodymus, kaip paaiškinta šiuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="d3f03-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="d3f03-160">Intervalo šablono antraštės Nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3f03-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="d3f03-161">Šablono antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="d3f03-162">**Intervalo šablonas:** _61_</span><span class="sxs-lookup"><span data-stu-id="d3f03-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="d3f03-163">**Aprašas:** _61_</span><span class="sxs-lookup"><span data-stu-id="d3f03-163">**Description:** _61_</span></span>
    - <span data-ttu-id="d3f03-164">**Reikalaujamas tipas:** *Pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="d3f03-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="d3f03-165">Šiuo metu palaikomas tik vienas reikalaujamas tipas *Pardavimo užsakymas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="d3f03-166">**Reikalaujama strategija:** _Užsakyta_</span><span class="sxs-lookup"><span data-stu-id="d3f03-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="d3f03-167">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="d3f03-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="d3f03-168">**Užsakyta** – Pardavimo užsakyme visas užsakytas kiekis turi būti laikomas paklausa.</span><span class="sxs-lookup"><span data-stu-id="d3f03-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="d3f03-169">**Rezervuota** – Rezervuoti (faktiniai ir užsakyti) pardavimo užsakymo eilutės kiekiai yra laikomi paklausa.</span><span class="sxs-lookup"><span data-stu-id="d3f03-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="d3f03-170">**Sandėlis:** _61_</span><span class="sxs-lookup"><span data-stu-id="d3f03-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d3f03-171">**Leisti bangai reikalauti naudoti nerezervuotus kiekius:** _Taip_</span><span class="sxs-lookup"><span data-stu-id="d3f03-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="d3f03-172">Taip pat galite nurodyti užklausą, kuri susiaurina vertinamą paklausą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="d3f03-173">Intervalo specifikacijų kiekvienam darbo šablonui nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3f03-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="d3f03-174">Kiekvienam sukurtam šablonui atlikite šiuos veiksmus, kad pridėtumėte eilutę kiekvienai intervalo specifikacijai.</span><span class="sxs-lookup"><span data-stu-id="d3f03-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="d3f03-175">Norėdami sukurti naują šablono eilutę, „FastTab” skirtuke **Nauja** pasirinkite **Išsami intervalo šablono informacija**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="d3f03-176">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-177">**Seka:** _1_</span><span class="sxs-lookup"><span data-stu-id="d3f03-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="d3f03-178">**Aprašymas:** _Fiksuota vieta_</span><span class="sxs-lookup"><span data-stu-id="d3f03-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="d3f03-179">**Mažiausias kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="d3f03-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="d3f03-180">Šis laukas nurodo minimalų paklausos kiekį, kurio reikia eilutei.</span><span class="sxs-lookup"><span data-stu-id="d3f03-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="d3f03-181">**Maksimalus kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d3f03-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="d3f03-182">Šis laukas nurodo maksimalų paklausos kiekį, kuris galioja eilutei.</span><span class="sxs-lookup"><span data-stu-id="d3f03-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="d3f03-183">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="d3f03-184">Šiame lauke apibrėžiamas matavimo vienetas, kurį nurodo minimalus ir maksimalus kiekis.</span><span class="sxs-lookup"><span data-stu-id="d3f03-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="d3f03-185">**Matavimo vieneto pakopa:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d3f03-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="d3f03-186">Šis laukas nurodo paklausos matavimo vienetus, kurie galioja eilutei.</span><span class="sxs-lookup"><span data-stu-id="d3f03-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="d3f03-187">(Norėdami gauti daugiau informacijos, žr. šios temos skyrių [Matavimo vienetų pakopos intervalui](#unit-tiers).)</span><span class="sxs-lookup"><span data-stu-id="d3f03-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="d3f03-188">**Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_</span><span class="sxs-lookup"><span data-stu-id="d3f03-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="d3f03-189">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="d3f03-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="d3f03-190">**Tarkime, kad tuščia** – Šioje sistemoje daroma prielaida, kad visos vietos iš paėmimo srities, yra tuščios ir nereiktų patikrinti šių vietų dėl atsargų.</span><span class="sxs-lookup"><span data-stu-id="d3f03-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="d3f03-191">**Atsižvelgti į kiekį** – Ši sistema patikrina visas vietas iš paėmimo srities dėl atsargų, ir turėtų praleisti visas vietas, kurios nėra tuščios.</span><span class="sxs-lookup"><span data-stu-id="d3f03-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="d3f03-192">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="d3f03-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="d3f03-193">Šiame lauke apibrėžiama vietos nurodymas, kuri naudojamas papildymo darbo paėmimų vietai rasti.</span><span class="sxs-lookup"><span data-stu-id="d3f03-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="d3f03-194">**Perpildos vieta:** palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="d3f03-195">Šis laukas nurodo vietą, į kurią yra įtrauktas atsargų kiekis, jei vietos negalima rasti, kai eilutė yra apdorojama.</span><span class="sxs-lookup"><span data-stu-id="d3f03-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="d3f03-196">**Leisti** _taip_</span><span class="sxs-lookup"><span data-stu-id="d3f03-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="d3f03-197">Jei ši parinktis nustatyta kaip *Taip*, jei bet koks reikalavimas negali būti įvykdytas, perkėlimo darbas bus sukurtas, kad būtų galima paimti atsargas iš vietų, kuriose yra atsargų, tačiau kur niekas nebuvo paimta.</span><span class="sxs-lookup"><span data-stu-id="d3f03-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="d3f03-198">Tada šablonas paleidžiamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="d3f03-198">The template is then run again.</span></span> <span data-ttu-id="d3f03-199">Šiuo metu nepaisoma vietų atsargų.</span><span class="sxs-lookup"><span data-stu-id="d3f03-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="d3f03-200">Ši funkcija veikia geriausiai, kai laukas **Priskirti intervalo kriterijų** nustatomas į _Atsižvelgti į kiekį_.</span><span class="sxs-lookup"><span data-stu-id="d3f03-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="d3f03-201">**Fiksuotos vietos naudojimas:** _Galima naudoti tik fiksuotas produkto vietas_</span><span class="sxs-lookup"><span data-stu-id="d3f03-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="d3f03-202">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="d3f03-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="d3f03-203">**Fiksuotos ir nefiksuotos vietos** – Sistema neapribojama naudoti tik fiksuotas vietas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="d3f03-204">**Tik fiksuotos produkto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto vietos.</span><span class="sxs-lookup"><span data-stu-id="d3f03-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="d3f03-205">**Tik fiksuotos produkto varianto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto varianto vietos.</span><span class="sxs-lookup"><span data-stu-id="d3f03-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="d3f03-206">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-206">Select **Save**.</span></span>
1. <span data-ttu-id="d3f03-207">Pasirinkite **Naujas**, kad sukurtumėte antrą šablono eilutę.</span><span class="sxs-lookup"><span data-stu-id="d3f03-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="d3f03-208">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-209">**Seka:** _2_</span><span class="sxs-lookup"><span data-stu-id="d3f03-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="d3f03-210">**Aprašymas:** _Kita_</span><span class="sxs-lookup"><span data-stu-id="d3f03-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="d3f03-211">**Minimalus kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="d3f03-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="d3f03-212">**Maksimalus kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d3f03-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="d3f03-213">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="d3f03-214">**Matavimo vieneto pakopa:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d3f03-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="d3f03-215">**Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_</span><span class="sxs-lookup"><span data-stu-id="d3f03-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="d3f03-216">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="d3f03-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="d3f03-217">**Perpildos vieta:** palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="d3f03-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="d3f03-218">**Leisti** _taip_</span><span class="sxs-lookup"><span data-stu-id="d3f03-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="d3f03-219">**Fiksuotos vietos naudojimas:** _Fiksuotos ir nefiksuotos vietos_</span><span class="sxs-lookup"><span data-stu-id="d3f03-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="d3f03-220">Antrojoje eilutėje,dabar bus nurodyti kriterijai, naudojami nustatyti, kokiose vietose gali būti padarytos tos eilutės paklausa.</span><span class="sxs-lookup"><span data-stu-id="d3f03-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="d3f03-221">Pasirinktie eilutę, kurios **Seka** yra nustatyta į *2*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="d3f03-222">Pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="d3f03-223">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="d3f03-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f03-224">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-225">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="d3f03-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d3f03-226">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="d3f03-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d3f03-227">**Laukas:** *Vietos profilio ID*</span><span class="sxs-lookup"><span data-stu-id="d3f03-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="d3f03-228">**Kriterijai:** lauke *Pick-06* (pasirinkite dvigubą pliuso ženklą \[**++**\], kad išplėstumėte sąrašą, tada pasirinkite *Pick-06* - *Paėmimo vieta 6*.)</span><span class="sxs-lookup"><span data-stu-id="d3f03-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="d3f03-229">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="d3f03-230">Nustatyti vietos nurodymus</span><span class="sxs-lookup"><span data-stu-id="d3f03-230">Set up location directives</span></span>

<span data-ttu-id="d3f03-231">Reikia nustatyti bent vieną vietos nurodymą, kad būtų palaikomi intervalo paėmimai.</span><span class="sxs-lookup"><span data-stu-id="d3f03-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="d3f03-232">Naudokite šiame skyriuje nurodytas procedūras, kad nustatytumėte naują *papildymo vietos nurodymą*, skirtą paėmimams.</span><span class="sxs-lookup"><span data-stu-id="d3f03-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="d3f03-233">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d3f03-234">Kairinės srities lauke **Darbo užsakymo tipas** pasirinkite *Papildymas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="d3f03-235">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d3f03-236">Naujo vietos nurodymo antraštės lauke **Pavadinimas**, įveskite *61 intervalo paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="d3f03-237">Konfigūruokite vietų nurodymus „FastTab“ skirtuke</span><span class="sxs-lookup"><span data-stu-id="d3f03-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="d3f03-238">„FastTab“ skirtuke **Vietų nurodymai** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="d3f03-239">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="d3f03-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d3f03-240">**Darbo tipas:** _Paėmimas_</span><span class="sxs-lookup"><span data-stu-id="d3f03-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="d3f03-241">**Vieta:** _6_</span><span class="sxs-lookup"><span data-stu-id="d3f03-241">**Site:** _6_</span></span>
    - <span data-ttu-id="d3f03-242">**Sandėlis:** _61_</span><span class="sxs-lookup"><span data-stu-id="d3f03-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d3f03-243">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="d3f03-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="d3f03-244">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="d3f03-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="d3f03-245">Konfigūruoti „FastTab“ skirtuką Eilutės</span><span class="sxs-lookup"><span data-stu-id="d3f03-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="d3f03-246">„FastTab“ skirtuke **Eilutės** spustelėję **Nauja** sukursite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="d3f03-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d3f03-247">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-247">On the new line, set the following values.</span></span> <span data-ttu-id="d3f03-248">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="d3f03-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d3f03-249">**Pradinis kiekis:** _0_</span><span class="sxs-lookup"><span data-stu-id="d3f03-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="d3f03-250">**Galutinis kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d3f03-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="d3f03-251">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="d3f03-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="d3f03-252">Konfigūruokite vietų nurodymų veiksmus „FastTab“ skirtuke</span><span class="sxs-lookup"><span data-stu-id="d3f03-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="d3f03-253">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="d3f03-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d3f03-254">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-254">On the new line, set the following values.</span></span> <span data-ttu-id="d3f03-255">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="d3f03-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d3f03-256">**Pavadinimas:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="d3f03-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="d3f03-257">**Strategija:** _Nėra_</span><span class="sxs-lookup"><span data-stu-id="d3f03-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="d3f03-258">Pasirinkite **Įrašyti**, kad būtų galima naudoti mygtuką **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="d3f03-259">Redaguoti užklausą</span><span class="sxs-lookup"><span data-stu-id="d3f03-259">Edit the query</span></span>

1. <span data-ttu-id="d3f03-260">„FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d3f03-261">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="d3f03-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d3f03-262">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-263">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="d3f03-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d3f03-264">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="d3f03-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d3f03-265">**Laukas:** *Zonos ID*</span><span class="sxs-lookup"><span data-stu-id="d3f03-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="d3f03-266">**Kriterijai:** *Bulk* (pasirinkite dvigubą pliuso ženklą \[**++**\] , kad išplėstumėte sąrašą, tada pasirinkite *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="d3f03-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="d3f03-267">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d3f03-268">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="d3f03-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d3f03-269">Scenarijaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3f03-269">Set up the scenario</span></span>

<span data-ttu-id="d3f03-270">Šiame scenarijuje naudokite įtaisytuosius pavyzdžio duomenis ir kurkite šiame skyriuje aprašytus įrašus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="d3f03-271">Naudoti USMF pavyzdinius duomenis</span><span class="sxs-lookup"><span data-stu-id="d3f03-271">Use the USMF sample data</span></span>

<span data-ttu-id="d3f03-272">Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="d3f03-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d3f03-273">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="d3f03-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="d3f03-274">Kurti paklausą</span><span class="sxs-lookup"><span data-stu-id="d3f03-274">Create demand</span></span>

<span data-ttu-id="d3f03-275">Atlikite šiuos veiksmus, kad sukurtumėte paklausą, kuriai taikysite intervalą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="d3f03-276">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="d3f03-277">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="d3f03-278">Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-007_.</span><span class="sxs-lookup"><span data-stu-id="d3f03-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="d3f03-279">Lauke **Sandėlis** pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="d3f03-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d3f03-280">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-280">Select **OK**.</span></span>
1. <span data-ttu-id="d3f03-281">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-281">The new sales order is opened.</span></span> <span data-ttu-id="d3f03-282">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="d3f03-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d3f03-283">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-284">**Prekė:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="d3f03-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="d3f03-285">**Kiekis:** _20_</span><span class="sxs-lookup"><span data-stu-id="d3f03-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="d3f03-286">Pasirinkite **Įtraukti eilutę** naujai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="d3f03-287">**Prekė:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d3f03-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d3f03-288">**Kiekis:** _8_</span><span class="sxs-lookup"><span data-stu-id="d3f03-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="d3f03-289">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-289">Select **Save**.</span></span>
1. <span data-ttu-id="d3f03-290">Pasirinkite **Naujas**, kad antrą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="d3f03-291">Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-008_.</span><span class="sxs-lookup"><span data-stu-id="d3f03-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="d3f03-292">Lauke **Sandėlis** pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="d3f03-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d3f03-293">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-293">The new sales order is opened.</span></span> <span data-ttu-id="d3f03-294">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="d3f03-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d3f03-295">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="d3f03-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="d3f03-296">**Prekė:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d3f03-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d3f03-297">**Kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="d3f03-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="d3f03-298">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="d3f03-299">Naudokite įprastą intervalo scenarijų</span><span class="sxs-lookup"><span data-stu-id="d3f03-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="d3f03-300">Po to, kai yra visi būtini elementai, kaip aprašyta ankstesniame skyriuje, jūs esate pasirengę išbandyti šią funkciją dirbdami per kiekvieną šiame skyriuje esantį pratimą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="d3f03-301">Generuoti paklausą</span><span class="sxs-lookup"><span data-stu-id="d3f03-301">Generate demand</span></span>

1. <span data-ttu-id="d3f03-302">Eikite į **Sandėlio valdymas \>Sąranka \> Papildymas \> Intervalo šablonai** ir pasirinkite norimą naudoti intervalo šabloną.</span><span class="sxs-lookup"><span data-stu-id="d3f03-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="d3f03-303">Veiksmų srityje spustelėkite **Generuoti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="d3f03-304">Ši komanda įvertina visas paklausas, kurios yra sistemoje ir kurios atitinka intervalo šablono užklausą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="d3f03-305">Bendra visų užsakymų paklausa yra konsoliduojama po vieną kiekvieno kiekio/matavimo vieneto eilutę.</span><span class="sxs-lookup"><span data-stu-id="d3f03-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="d3f03-306">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="d3f03-307">Intervalo paklausa</span><span class="sxs-lookup"><span data-stu-id="d3f03-307">Slotting demand</span></span>

<span data-ttu-id="d3f03-308">Dėl to, kad yra intervalo šablono nustatymu, *Intervalo paklausa* parodo paklausos generavimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="d3f03-309">Veiksmų srityje pasirinkite **Intervalo paklausa** norėdami peržiūrėti rezultatus iš komandos **Generuoti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="d3f03-310">Intervalo paklausos eilutės gali būti redaguojamas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="d3f03-311">Galite panaikinti eilutę, pridėti naują eilutę arba redaguoti eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="d3f03-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="d3f03-312">Galite redaguoti paklausą neautomatiniu būdu arba galite ją importuoti iš išorinės sistemos naudodami duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="d3f03-313">Neatsižvelgiant į tai, iš kur intervalo paklausa yra, ji bus naudojamas atliekant tolesnį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="d3f03-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="d3f03-314">Surasti paklausą</span><span class="sxs-lookup"><span data-stu-id="d3f03-314">Locate demand</span></span>

<span data-ttu-id="d3f03-315">Kai paklausa sugeneruojama, turite naudoti komandą **Surasti paklausą,** kad būtų sugeneruotas *Intervalo planas*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="d3f03-316">Veiksmų srityje spustelėkite **Surasti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="d3f03-317">Paleidžiamas intervalo procesas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-317">The slotting process runs.</span></span> <span data-ttu-id="d3f03-318">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="d3f03-319">Intervalo planas</span><span class="sxs-lookup"><span data-stu-id="d3f03-319">Slotting plan</span></span>

<span data-ttu-id="d3f03-320">Intervalo planas nurodo vietą, kurioje buvo priskirta kiekviena prekė/kiekis, buvo panaudota perpilda, buvo sukurtas padėjimo darbas ar naudota šablono eilutė.</span><span class="sxs-lookup"><span data-stu-id="d3f03-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="d3f03-321">**Bet kokia paklausa, kurios negalima įvykdyti yra paryškintas raudonai.**</span><span class="sxs-lookup"><span data-stu-id="d3f03-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="d3f03-322">Veiksmų srityje pasirinkite **Intervalo planas,** norėdami peržiūrėti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="d3f03-323">Sukurkite papildymą</span><span class="sxs-lookup"><span data-stu-id="d3f03-323">Create replenishment</span></span>

<span data-ttu-id="d3f03-324">Sukūrę planą, turite sukurti *Papildymo darbą*, pagrįstą planu.</span><span class="sxs-lookup"><span data-stu-id="d3f03-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="d3f03-325">Veiksmų srityje pasirinkite **Vykdyti papildymą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="d3f03-326">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="d3f03-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="d3f03-327">Šis pranešimas nurodo antraščių, sukurtų darbo kūrimo ID, skaičių.</span><span class="sxs-lookup"><span data-stu-id="d3f03-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="d3f03-328">Vietos nurodymai, kurie bus naudojami, yra identifikuojami pagal nurodymo kodą, pateiktą kiekvienoje šablono eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d3f03-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="d3f03-329">Patarimai</span><span class="sxs-lookup"><span data-stu-id="d3f03-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="d3f03-330">Intervalo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d3f03-330">Set up automatic slotting</span></span>

<span data-ttu-id="d3f03-331">Po to, kai visi reikiami elementai yra, galite nustatyti automatinį valdymą, atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="d3f03-332">Eikite į **Sandėlio valdymas \> Papildymas \> Atlikti intervalą**.</span><span class="sxs-lookup"><span data-stu-id="d3f03-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="d3f03-333">Nurodykite paleidžiančius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d3f03-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="d3f03-334">Pasirinkite vieną ar daugiau iš šių intervalo veiksmų:</span><span class="sxs-lookup"><span data-stu-id="d3f03-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="d3f03-335">Generuoti paklausą</span><span class="sxs-lookup"><span data-stu-id="d3f03-335">Generate demand</span></span>
    - <span data-ttu-id="d3f03-336">Surasti paklausą</span><span class="sxs-lookup"><span data-stu-id="d3f03-336">Locate demand</span></span>
    - <span data-ttu-id="d3f03-337">Kurti papildymo darbą</span><span class="sxs-lookup"><span data-stu-id="d3f03-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3f03-338">Intervalo veiksmai yra progresyvūs.</span><span class="sxs-lookup"><span data-stu-id="d3f03-338">The slotting steps are progressive.</span></span> <span data-ttu-id="d3f03-339">Jei norite pasirinkti *Surasti paklausą*, pirmiausia turite pasirinkti *Generuoti paklausą*.</span><span class="sxs-lookup"><span data-stu-id="d3f03-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="d3f03-340">Nurodyti naudotiną šabloną.</span><span class="sxs-lookup"><span data-stu-id="d3f03-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="d3f03-341">Jei norėsite, pakartojimas paleidžiamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="d3f03-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="d3f03-342">Norėdami atlikti scenarijų pratimus, **ne**nustatykite automatinio intervalo.</span><span class="sxs-lookup"><span data-stu-id="d3f03-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
