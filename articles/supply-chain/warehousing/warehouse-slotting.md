---
title: Sandėlio intervalas
description: Šioje temoje pateikiama informacija apie sandėlio intervalą. Sandėlio intervalas leidžia konsoliduoti poreikį pagal prekę ir matavimo vienetą iš užsakymų, kurių būsena yra Užsakytas, Rezervuotas arba Išleistas. Jis padeda sandėlio vadovams sumaniai planuoti paėmimų vietas dar prieš tai, kai jos išleidžia užsakymus į sandėlį ir sukuria paėmimų darbą.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993758"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="0bc36-105">Sandėlio intervalas</span><span class="sxs-lookup"><span data-stu-id="0bc36-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bc36-106">Keletas sandėlio vietų funkcijų yra prieinamos siekiant padėti sandėlio vadovams protingai planuoti paėmimo vietas prieš jiems paleidžiant užsakymus į sandėlį ir sukuriant paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="0bc36-107">*Sandėlio vietų funkija* leidžia jums kosoliduoti poreikį pagal elementą ir matavimo vienetą iš užsakymų, kurie turi *Užsakyta*, *Rezervuota* ar *Išleista* būseną.</span><span class="sxs-lookup"><span data-stu-id="0bc36-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="0bc36-108">Sugeneruota paklausa gali būti taikoma vietoms, kurios bus naudojamos paėmimui, atsižvelgiant į kiekį, vienetą, faktines dimensijas, fiksuotas vietas ir kita.</span><span class="sxs-lookup"><span data-stu-id="0bc36-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="0bc36-109">Po to, kai buvo sukurtas intervalo planas, papildymo darbas gali būti sukurtas tam, kad būtų galima pasiekti reikiamą atsargų kiekį kiekvienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="0bc36-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="0bc36-110">*Sandėlio vietos užsakymų perdavimui* funkcija leidžia sandėlio vadovams papildyti paėmimo vietas prisklausomai nuo poreikio perkelti užsakymus, kurie dar nėra paleisti į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="0bc36-111">Tai užtikrina, kad paėmimo vietos apims visus vienetus, kurių reika perduotiems užsakymams po jų paleidimo į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="0bc36-112">Šiai funkcijai turite taip pat įjungti *Sandėlio vietų funkcijos* funkciją.</span><span class="sxs-lookup"><span data-stu-id="0bc36-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="0bc36-113">*Sandėlio vietų priskyrimo papildymo* funkcija įtraukia parinktį šablono eilutėms, kurios yra naudojamos *Sandėlio vietų funkcijos* funkcijos.</span><span class="sxs-lookup"><span data-stu-id="0bc36-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="0bc36-114">Ši parinktis leidžia sistemai apgalvoti esamą turimą inventorių pagal tikslinę vietą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="0bc36-115">Dėl to, mažiau papildymų gali būti sukurta vienai vietai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="0bc36-116">*Sandėlio vietų priskyrimo papildymo* funkcijai turite taip pat įjungti *Sandėlio vietų funkcijos* funkciją.</span><span class="sxs-lookup"><span data-stu-id="0bc36-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="0bc36-117">Ji gali būti pasirinktinai naudojama kartu su *Sandėlio vietų perduotiems užsakymams* funkcija.</span><span class="sxs-lookup"><span data-stu-id="0bc36-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="0bc36-118">Įjunkite sandėlio vietų funkcijas</span><span class="sxs-lookup"><span data-stu-id="0bc36-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="0bc36-119">Prieš tai, kai galėsite jas naudoti, jos turi būti įjungtos jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="0bc36-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="0bc36-120">Administratoriai gali naudoti [funkcijos valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus tam, kad patikrintų funkcijų būsentą ir įjungtų jas, jei to reikia.</span><span class="sxs-lookup"><span data-stu-id="0bc36-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="0bc36-121">Įjunkite tolesnes funkcijas, kaip būtina:</span><span class="sxs-lookup"><span data-stu-id="0bc36-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="0bc36-122">Sandėlio intervalo funkcija</span><span class="sxs-lookup"><span data-stu-id="0bc36-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="0bc36-123">Sandėlio vietos perduotiems užsakymams</span><span class="sxs-lookup"><span data-stu-id="0bc36-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0bc36-124">Taigi *Sandėlio vietų funkcijos* funkcija turi būti įjungta prieš šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="0bc36-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="0bc36-125">Sandėlio vietų priskyrimo papipldymai</span><span class="sxs-lookup"><span data-stu-id="0bc36-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0bc36-126">Taigi *Sandėlio vietų funkcijos* funkcija turi būti įjungta prieš šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="0bc36-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="0bc36-127">Sandėlio intervalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bc36-127">Set up warehouse slotting</span></span>

<span data-ttu-id="0bc36-128">Norėdami naudoti sandėlio vietas, turite nustatyti tolesnius elementus savo sistemoje:</span><span class="sxs-lookup"><span data-stu-id="0bc36-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="0bc36-129">Intervalo kūrimo matavimo vieneto pakopos</span><span class="sxs-lookup"><span data-stu-id="0bc36-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="0bc36-130">Krypčių kodai</span><span class="sxs-lookup"><span data-stu-id="0bc36-130">Directive codes</span></span>
- <span data-ttu-id="0bc36-131">Intervalo šablonai</span><span class="sxs-lookup"><span data-stu-id="0bc36-131">Slotting templates</span></span>
- <span data-ttu-id="0bc36-132">Vietos nurodymai</span><span class="sxs-lookup"><span data-stu-id="0bc36-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="0bc36-133">Kurti matavimo vieneto pakopas intervalui</span><span class="sxs-lookup"><span data-stu-id="0bc36-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="0bc36-134">Matavimo vienetų pakopos įgalina sugrupuoti kelis matavimo vienetus, kad juos būtų galima nustatyti.</span><span class="sxs-lookup"><span data-stu-id="0bc36-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="0bc36-135">Pavyzdžiui, jei kelių dydžių dėžės paimamos iš tos pačios dėžių paėmimo srities, visiems dydžiams galima sukurti vieną pakopą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="0bc36-136">**Turi būti sukurta kiekvieno matavimo vieneto eilutė, kuri turėtų būti pakopos dalis.**</span><span class="sxs-lookup"><span data-stu-id="0bc36-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="0bc36-137">Eikite į **Sandėlio valdymas \>Nustatymas \>Papildymas \> Matavimo vienetų pakopų intervalas**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="0bc36-138">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-138">Select **New**.</span></span>
1. <span data-ttu-id="0bc36-139">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="0bc36-140">**Matavimo vieneto pakopa:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="0bc36-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="0bc36-141">**Aprašymas:** *Kiekviena dėžės paletė*</span><span class="sxs-lookup"><span data-stu-id="0bc36-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="0bc36-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-142">Select **Save**.</span></span>
1. <span data-ttu-id="0bc36-143">„FastTab“ skirtuke **Matavimo vienetai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="0bc36-144">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-145">**Vienetas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="0bc36-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="0bc36-146">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0bc36-147">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0bc36-148">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="0bc36-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0bc36-149">Pasirinkite **Nauja**, kad įtrauktumėte antrą eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="0bc36-150">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-151">**Vienetas:** *ea*</span><span class="sxs-lookup"><span data-stu-id="0bc36-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="0bc36-152">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0bc36-153">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0bc36-154">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="0bc36-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0bc36-155">Pasirinkite **Nauja**, kad įtrauktumėte trečią eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="0bc36-156">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-157">**Vienetas:** *PL*</span><span class="sxs-lookup"><span data-stu-id="0bc36-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="0bc36-158">**Aprašymas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0bc36-159">Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0bc36-160">**Vieneto klasė:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="0bc36-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0bc36-161">Pasirinkite **Įrašyti**, kad įrašytumėte pakopą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="0bc36-162">Kurti nurodymo kodą, skirtą intervalui</span><span class="sxs-lookup"><span data-stu-id="0bc36-162">Create a directive code for slotting</span></span>

<span data-ttu-id="0bc36-163">Turite pasirinkti nurodymo kodą, kuris turi būti susietas su šablonu.</span><span class="sxs-lookup"><span data-stu-id="0bc36-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="0bc36-164">Eikite į **Sandėlio valdymas \> Nustatymas \> Nurodymų kodai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="0bc36-165">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0bc36-166">**Nurodymo kodas** lauke įveskite *Intervalas*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="0bc36-167">**Nurodymo aprašymas** lauke įveskite *Intervalas*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="0bc36-168">Intervalo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bc36-168">Set up slotting templates</span></span>

<span data-ttu-id="0bc36-169">Kiekvienas intervalo šablonas kontroliuoja atsargų priskyrimui tam tikroms sandėlio vietoms.</span><span class="sxs-lookup"><span data-stu-id="0bc36-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="0bc36-170">Kiekviename šablone turi būti eilutė kiekvieno intervalo specifikacijai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="0bc36-171">Norėdami nustatyti intervalo šablonus, naudokite šiame skyriuje nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="0bc36-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="0bc36-172">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Papildymas \> Intervalo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="0bc36-173">Pasirinkite **Naujas**, kad sukurtumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="0bc36-173">Select **New** to create a template.</span></span>

<span data-ttu-id="0bc36-174">Toliau turite nustatyti šablono antraštę, intervalo specifikacijas ir vietos nurodymus, kaip paaiškinta šiuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="0bc36-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="0bc36-175">Vietos nustatymo perduotiems užsakymams atspindi nustatymą vietoms pardavimų užsakymusoe, bet **Paklausos tipo** laukelis yra nustatytas *Perduoti užsakymus*, o ne *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="0bc36-176">Nustatykite antraštę pardavimo užsakymo vietos šablonui</span><span class="sxs-lookup"><span data-stu-id="0bc36-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="0bc36-177">Šablono antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="0bc36-178">**Intervalo šablonas:** _61_</span><span class="sxs-lookup"><span data-stu-id="0bc36-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="0bc36-179">**Aprašas:** _61_</span><span class="sxs-lookup"><span data-stu-id="0bc36-179">**Description:** _61_</span></span>
    - <span data-ttu-id="0bc36-180">**Reikalaujamas tipas:** *Pardavimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="0bc36-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="0bc36-181">Šiuo metu *Pardavimo užsakymai* ir *Perdavimo užsakymai* yra tik palaikomi paklausos tipai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="0bc36-182">Galite pasirinkti *Perduoti užsakymus* tik jei *Sandėlio vietos perdavimo užsakymams* funkcija įjungta.</span><span class="sxs-lookup"><span data-stu-id="0bc36-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="0bc36-183">**Reikalaujama strategija:** _Užsakyta_</span><span class="sxs-lookup"><span data-stu-id="0bc36-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="0bc36-184">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="0bc36-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="0bc36-185">**Užsakyta** – Pardavimo užsakyme visas užsakytas kiekis turi būti laikomas paklausa.</span><span class="sxs-lookup"><span data-stu-id="0bc36-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="0bc36-186">**Rezervuota** – Rezervuoti (faktiniai ir užsakyti) pardavimo užsakymo eilutės kiekiai yra laikomi paklausa.</span><span class="sxs-lookup"><span data-stu-id="0bc36-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="0bc36-187">**Paleisti** – Paleistas kiekis turi būti nulemtas paklausos.</span><span class="sxs-lookup"><span data-stu-id="0bc36-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="0bc36-188">**Sandėlis:** _61_</span><span class="sxs-lookup"><span data-stu-id="0bc36-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="0bc36-189">**Leisti bangai reikalauti naudoti nerezervuotus kiekius:** _Taip_</span><span class="sxs-lookup"><span data-stu-id="0bc36-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="0bc36-190">Taip pat galite nurodyti užklausą, kuri susiaurina vertinamą paklausą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="0bc36-191">Intervalo specifikacijų kiekvienam darbo šablonui nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bc36-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="0bc36-192">Kiekvienam pardavimo užsakymo šablonui, kurį sukūrėte, atlikite šiuos žingsnius tam, kad įtrauktumėte eilutę kiekvienai vietos specifikacijai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="0bc36-193">Norėdami sukurti naują šablono eilutę, „FastTab” skirtuke **Nauja** pasirinkite **Išsami intervalo šablono informacija**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="0bc36-194">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-195">**Seka:** _1_</span><span class="sxs-lookup"><span data-stu-id="0bc36-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="0bc36-196">**Aprašymas:** _Fiksuota vieta_</span><span class="sxs-lookup"><span data-stu-id="0bc36-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="0bc36-197">**Mažiausias kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="0bc36-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="0bc36-198">Šis laukas nurodo minimalų paklausos kiekį, kurio reikia eilutei.</span><span class="sxs-lookup"><span data-stu-id="0bc36-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="0bc36-199">**Maksimalus kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0bc36-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="0bc36-200">Šis laukas nurodo maksimalų paklausos kiekį, kuris galioja eilutei.</span><span class="sxs-lookup"><span data-stu-id="0bc36-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="0bc36-201">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="0bc36-202">Šiame lauke apibrėžiamas matavimo vienetas, kurį nurodo minimalus ir maksimalus kiekis.</span><span class="sxs-lookup"><span data-stu-id="0bc36-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="0bc36-203">**Matavimo vieneto pakopa:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="0bc36-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="0bc36-204">Šis laukas nurodo paklausos matavimo vienetus, kurie galioja eilutei.</span><span class="sxs-lookup"><span data-stu-id="0bc36-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="0bc36-205">(Norėdami gauti daugiau informacijos, žr. šios temos skyrių [Matavimo vienetų pakopos intervalui](#unit-tiers).)</span><span class="sxs-lookup"><span data-stu-id="0bc36-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="0bc36-206">**Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_</span><span class="sxs-lookup"><span data-stu-id="0bc36-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="0bc36-207">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="0bc36-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="0bc36-208">**Tarkime, kad tuščia** – Šioje sistemoje daroma prielaida, kad visos vietos iš paėmimo srities, yra tuščios ir nereiktų patikrinti šių vietų dėl atsargų.</span><span class="sxs-lookup"><span data-stu-id="0bc36-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="0bc36-209">**Atsižvelgti į kiekį** – Ši sistema patikrina visas vietas iš paėmimo srities dėl atsargų, ir turėtų praleisti visas vietas, kurios nėra tuščios.</span><span class="sxs-lookup"><span data-stu-id="0bc36-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="0bc36-210">**Apgalvota turimas** – Sistema turi tikrinti, ar bet kuri paskirties vieta turi neužrezervuotą kiekį vienetui pagal paklausos eilutę.</span><span class="sxs-lookup"><span data-stu-id="0bc36-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="0bc36-211">Jei kiekis yra pakankamai didelis, kad atitiktų mažiausiai viena paklausos eilutės vienetą, sukurtas vietų plano įrašas yra sumažinamas esamu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="0bc36-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="0bc36-212">Pavyzdžiui, jei paklausa yra 10 atvejų ir vienas yra turimas, nustatyta paklausa bus devyni atvejai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="0bc36-213">Jei paklausa yra 10 atvejų ir vienas yra turimas, nustatyta paklausa bus 10 atvejų.</span><span class="sxs-lookup"><span data-stu-id="0bc36-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="0bc36-214">Ši vertė yra prieinama tik, jei *Sandėlio vietų priskyrimo papildymų* funkcija įjungta.</span><span class="sxs-lookup"><span data-stu-id="0bc36-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="0bc36-215">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="0bc36-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="0bc36-216">Šiame lauke apibrėžiama vietos nurodymas, kuri naudojamas papildymo darbo paėmimų vietai rasti.</span><span class="sxs-lookup"><span data-stu-id="0bc36-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="0bc36-217">**Perpildos vieta:** palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="0bc36-218">Šis laukas nurodo vietą, į kurią yra įtrauktas atsargų kiekis, jei vietos negalima rasti, kai eilutė yra apdorojama.</span><span class="sxs-lookup"><span data-stu-id="0bc36-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="0bc36-219">**Leisti** _taip_</span><span class="sxs-lookup"><span data-stu-id="0bc36-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="0bc36-220">Jei ši parinktis nustatyta kaip *Taip*, jei bet koks reikalavimas negali būti įvykdytas, perkėlimo darbas bus sukurtas, kad būtų galima paimti atsargas iš vietų, kuriose yra atsargų, tačiau kur niekas nebuvo paimta.</span><span class="sxs-lookup"><span data-stu-id="0bc36-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="0bc36-221">Tada šablonas paleidžiamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="0bc36-221">The template is then run again.</span></span> <span data-ttu-id="0bc36-222">Šiuo metu nepaisoma vietų atsargų.</span><span class="sxs-lookup"><span data-stu-id="0bc36-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="0bc36-223">Ši funkcija veikia geriausiai, kai laukas **Priskirti intervalo kriterijų** nustatomas į _Atsižvelgti į kiekį_.</span><span class="sxs-lookup"><span data-stu-id="0bc36-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="0bc36-224">**Fiksuotos vietos naudojimas:** _Galima naudoti tik fiksuotas produkto vietas_</span><span class="sxs-lookup"><span data-stu-id="0bc36-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="0bc36-225">Šiame lauke galimos vertės:</span><span class="sxs-lookup"><span data-stu-id="0bc36-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="0bc36-226">**Fiksuotos ir nefiksuotos vietos** – Sistema neapribojama naudoti tik fiksuotas vietas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="0bc36-227">**Tik fiksuotos produkto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto vietos.</span><span class="sxs-lookup"><span data-stu-id="0bc36-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="0bc36-228">**Tik fiksuotos produkto varianto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto varianto vietos.</span><span class="sxs-lookup"><span data-stu-id="0bc36-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="0bc36-229">Jei vietos šablonas turi mažiausiai vieną eilutę, kurioje **Priskyrimo vietos kriterjaus** laukelis nustatytas į *Laikomas turimu*, leidimai nebėra leidžiami jokiai eilutei šablone.</span><span class="sxs-lookup"><span data-stu-id="0bc36-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="0bc36-230">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-230">Select **Save**.</span></span>
1. <span data-ttu-id="0bc36-231">Pasirinkite **Naujas**, kad sukurtumėte antrą šablono eilutę.</span><span class="sxs-lookup"><span data-stu-id="0bc36-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="0bc36-232">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-233">**Seka:** _2_</span><span class="sxs-lookup"><span data-stu-id="0bc36-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="0bc36-234">**Aprašymas:** _Kita_</span><span class="sxs-lookup"><span data-stu-id="0bc36-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="0bc36-235">**Minimalus kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="0bc36-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="0bc36-236">**Maksimalus kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0bc36-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="0bc36-237">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="0bc36-238">**Matavimo vieneto pakopa:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="0bc36-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="0bc36-239">**Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_</span><span class="sxs-lookup"><span data-stu-id="0bc36-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="0bc36-240">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="0bc36-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="0bc36-241">**Perpildos vieta:** palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="0bc36-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="0bc36-242">**Leisti** _taip_</span><span class="sxs-lookup"><span data-stu-id="0bc36-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="0bc36-243">**Fiksuotos vietos naudojimas:** _Fiksuotos ir nefiksuotos vietos_</span><span class="sxs-lookup"><span data-stu-id="0bc36-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="0bc36-244">Antrojoje eilutėje,dabar bus nurodyti kriterijai, naudojami nustatyti, kokiose vietose gali būti padarytos tos eilutės paklausa.</span><span class="sxs-lookup"><span data-stu-id="0bc36-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="0bc36-245">Pasirinktie eilutę, kurios **Seka** yra nustatyta į *2*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="0bc36-246">Pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="0bc36-247">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="0bc36-248">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-249">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="0bc36-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="0bc36-250">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="0bc36-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="0bc36-251">**Laukas:** *Vietos profilio ID*</span><span class="sxs-lookup"><span data-stu-id="0bc36-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="0bc36-252">**Kriterijai:** lauke *Pick-06* (pasirinkite dvigubą pliuso ženklą \[**++**\], kad išplėstumėte sąrašą, tada pasirinkite *Pick-06* - *Paėmimo vieta 6*.)</span><span class="sxs-lookup"><span data-stu-id="0bc36-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="0bc36-253">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="0bc36-254">Nustatyti vietos nurodymus</span><span class="sxs-lookup"><span data-stu-id="0bc36-254">Set up location directives</span></span>

<span data-ttu-id="0bc36-255">Reikia nustatyti bent vieną vietos nurodymą, kad būtų palaikomi intervalo paėmimai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="0bc36-256">Naudokite šiame skyriuje nurodytas procedūras, kad nustatytumėte naują *papildymo vietos nurodymą*, skirtą paėmimams.</span><span class="sxs-lookup"><span data-stu-id="0bc36-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="0bc36-257">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="0bc36-258">Kairinės srities lauke **Darbo užsakymo tipas** pasirinkite *Papildymas*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="0bc36-259">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0bc36-260">Naujo vietos nurodymo antraštės lauke **Pavadinimas**, įveskite *61 intervalo paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="0bc36-261">Laujelyje **Sekos numeris**, priimkite nustatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="0bc36-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="0bc36-262">Konfigūruokite vietų nurodymus „FastTab“ skirtuke</span><span class="sxs-lookup"><span data-stu-id="0bc36-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="0bc36-263">„FastTab“ skirtuke **Vietų nurodymai** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="0bc36-264">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="0bc36-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0bc36-265">**Darbo tipas:** _Paėmimas_</span><span class="sxs-lookup"><span data-stu-id="0bc36-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="0bc36-266">**Vieta:** _6_</span><span class="sxs-lookup"><span data-stu-id="0bc36-266">**Site:** _6_</span></span>
    - <span data-ttu-id="0bc36-267">**Sandėlis:** _61_</span><span class="sxs-lookup"><span data-stu-id="0bc36-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="0bc36-268">**Nurodymo kodas:** _Intervalas_</span><span class="sxs-lookup"><span data-stu-id="0bc36-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="0bc36-269">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="0bc36-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="0bc36-270">Konfigūruoti „FastTab“ skirtuką Eilutės</span><span class="sxs-lookup"><span data-stu-id="0bc36-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="0bc36-271">„FastTab“ skirtuke **Eilutės** spustelėję **Nauja** sukursite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="0bc36-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="0bc36-272">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="0bc36-273">**Pradinis kiekis:** _0_</span><span class="sxs-lookup"><span data-stu-id="0bc36-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="0bc36-274">**Galutinis kiekis:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0bc36-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="0bc36-275">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="0bc36-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="0bc36-276">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="0bc36-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="0bc36-277">Konfigūruokite vietų nurodymų veiksmus „FastTab“ skirtuke</span><span class="sxs-lookup"><span data-stu-id="0bc36-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="0bc36-278">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="0bc36-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="0bc36-279">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-279">On the new line, set the following values.</span></span> <span data-ttu-id="0bc36-280">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="0bc36-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0bc36-281">**Sekos numeris:** Priimkite numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="0bc36-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="0bc36-282">**Pavadinimas:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="0bc36-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="0bc36-283">**Strategija:** _Nėra_</span><span class="sxs-lookup"><span data-stu-id="0bc36-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="0bc36-284">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="0bc36-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="0bc36-285">Pasirinkite **Įrašyti**, kad būtų galima naudoti mygtuką **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="0bc36-286">Redaguoti užklausą</span><span class="sxs-lookup"><span data-stu-id="0bc36-286">Edit the query</span></span>

1. <span data-ttu-id="0bc36-287">„FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="0bc36-288">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="0bc36-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="0bc36-289">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-290">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="0bc36-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="0bc36-291">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="0bc36-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="0bc36-292">**Laukas:** *Zonos ID*</span><span class="sxs-lookup"><span data-stu-id="0bc36-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="0bc36-293">**Kriterijai:** *Bulk* (pasirinkite dvigubą pliuso ženklą \[**++**\] , kad išplėstumėte sąrašą, tada pasirinkite *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="0bc36-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="0bc36-294">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="0bc36-295">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="0bc36-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="0bc36-296">Scenarijaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bc36-296">Set up the scenario</span></span>

<span data-ttu-id="0bc36-297">Šiame scenarijuje naudokite įtaisytuosius pavyzdžio duomenis ir kurkite šiame skyriuje aprašytus įrašus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="0bc36-298">Naudoti USMF pavyzdinius duomenis</span><span class="sxs-lookup"><span data-stu-id="0bc36-298">Use the USMF sample data</span></span>

<span data-ttu-id="0bc36-299">Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="0bc36-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="0bc36-300">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="0bc36-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="0bc36-301">Kurti paklausą</span><span class="sxs-lookup"><span data-stu-id="0bc36-301">Create demand</span></span>

<span data-ttu-id="0bc36-302">Atlikite šiuos veiksmus, kad sukurtumėte paklausą, kuriai taikysite intervalą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="0bc36-303">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="0bc36-304">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="0bc36-305">Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-007_.</span><span class="sxs-lookup"><span data-stu-id="0bc36-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="0bc36-306">Lauke **Sandėlis** pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="0bc36-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="0bc36-307">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-307">Select **OK**.</span></span>
1. <span data-ttu-id="0bc36-308">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-308">The new sales order is opened.</span></span> <span data-ttu-id="0bc36-309">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="0bc36-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0bc36-310">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-311">**Prekė:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="0bc36-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="0bc36-312">**Kiekis:** _20_</span><span class="sxs-lookup"><span data-stu-id="0bc36-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="0bc36-313">Pasirinkite **Įtraukti eilutę** naujai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="0bc36-314">**Prekė:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="0bc36-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="0bc36-315">**Kiekis:** _8_</span><span class="sxs-lookup"><span data-stu-id="0bc36-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="0bc36-316">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-316">Select **Save**.</span></span>
1. <span data-ttu-id="0bc36-317">Pasirinkite **Naujas**, kad antrą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="0bc36-318">Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-008_.</span><span class="sxs-lookup"><span data-stu-id="0bc36-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="0bc36-319">Lauke **Sandėlis** pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="0bc36-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="0bc36-320">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-320">The new sales order is opened.</span></span> <span data-ttu-id="0bc36-321">Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="0bc36-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0bc36-322">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0bc36-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="0bc36-323">**Prekė:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="0bc36-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="0bc36-324">**Kiekis:** _1_</span><span class="sxs-lookup"><span data-stu-id="0bc36-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="0bc36-325">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="0bc36-326">Naudokite įprastą intervalo scenarijų</span><span class="sxs-lookup"><span data-stu-id="0bc36-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="0bc36-327">Po to, kai yra visi būtini elementai, kaip aprašyta ankstesniame skyriuje, jūs esate pasirengę išbandyti šią funkciją dirbdami per kiekvieną šiame skyriuje esantį pratimą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="0bc36-328">Generuoti paklausą</span><span class="sxs-lookup"><span data-stu-id="0bc36-328">Generate demand</span></span>

1. <span data-ttu-id="0bc36-329">Eikite į **Sandėlio valdymas \>Sąranka \> Papildymas \> Intervalo šablonai** ir pasirinkite norimą naudoti intervalo šabloną.</span><span class="sxs-lookup"><span data-stu-id="0bc36-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="0bc36-330">Veiksmų srityje spustelėkite **Generuoti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="0bc36-331">Ši komanda įvertina visas paklausas, kurios yra sistemoje ir kurios atitinka intervalo šablono užklausą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="0bc36-332">Bendra visų užsakymų paklausa yra konsoliduojama po vieną kiekvieno kiekio/matavimo vieneto eilutę.</span><span class="sxs-lookup"><span data-stu-id="0bc36-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="0bc36-333">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="0bc36-334">Intervalo paklausa</span><span class="sxs-lookup"><span data-stu-id="0bc36-334">Slotting demand</span></span>

<span data-ttu-id="0bc36-335">Dėl to, kad yra intervalo šablono nustatymu, *Intervalo paklausa* parodo paklausos generavimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="0bc36-336">Veiksmų srityje pasirinkite **Intervalo paklausa** norėdami peržiūrėti rezultatus iš komandos **Generuoti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="0bc36-337">Intervalo paklausos eilutės gali būti redaguojamas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="0bc36-338">Galite panaikinti eilutę, pridėti naują eilutę arba redaguoti eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="0bc36-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="0bc36-339">Galite redaguoti paklausą neautomatiniu būdu arba galite ją importuoti iš išorinės sistemos naudodami duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="0bc36-340">Neatsižvelgiant į tai, iš kur intervalo paklausa yra, ji bus naudojamas atliekant tolesnį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="0bc36-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="0bc36-341">Surasti paklausą</span><span class="sxs-lookup"><span data-stu-id="0bc36-341">Locate demand</span></span>

<span data-ttu-id="0bc36-342">Kai paklausa sugeneruojama, turite naudoti komandą **Surasti paklausą,** kad būtų sugeneruotas *Intervalo planas*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="0bc36-343">Veiksmų srityje spustelėkite **Surasti paklausą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="0bc36-344">Paleidžiamas intervalo procesas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-344">The slotting process runs.</span></span> <span data-ttu-id="0bc36-345">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="0bc36-346">Intervalo planas</span><span class="sxs-lookup"><span data-stu-id="0bc36-346">Slotting plan</span></span>

<span data-ttu-id="0bc36-347">Intervalo planas nurodo vietą, kurioje buvo priskirta kiekviena prekė/kiekis, buvo panaudota perpilda, buvo sukurtas padėjimo darbas ar naudota šablono eilutė.</span><span class="sxs-lookup"><span data-stu-id="0bc36-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="0bc36-348">*Bet kokia paklausa, kurios negalima įvykdyti yra paryškintas raudonai.*</span><span class="sxs-lookup"><span data-stu-id="0bc36-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="0bc36-349">Veiksmų srityje pasirinkite **Intervalo planas,** norėdami peržiūrėti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="0bc36-350">**Sukurta paklausa**, **Nustatyti paklausą** ir **Vykdyti papildymą** procesai yra dabar vykdomi smėlio dėžėje.</span><span class="sxs-lookup"><span data-stu-id="0bc36-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="0bc36-351">(Šie procesai yra prieinami iš veiksmų juostos **Vietų šablono** puslapyje.)</span><span class="sxs-lookup"><span data-stu-id="0bc36-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="0bc36-352">**Sukurta paklausa**, **Nustatyta paklausą** ir **Vykdyti papildymą** procesai turi užraktą siekiant užtikrinti, kad jie nebus paleisti vienu metu.</span><span class="sxs-lookup"><span data-stu-id="0bc36-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="0bc36-353">Kitu atveju, naudojami duomenys gali būti panaikinti.</span><span class="sxs-lookup"><span data-stu-id="0bc36-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="0bc36-354">**Sukurta paklausa** ir **Nustatyta paklausai** procesai rodo įspėjimą, jei vykdymas nesukūrė įrašų arba jei įrašuose trūksta informacijos.</span><span class="sxs-lookup"><span data-stu-id="0bc36-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="0bc36-355">Jums pasirinkus **Vietų planas**, puslapis neturi **Naujas**, **Redaguoti** ar **Panaikinti** mygtukus veiksmų juostoje, nes duomenų šaltinio redaguoti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="0bc36-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="0bc36-356">Jums pasirinkus **Vykdyti papildymą**, sistema įjungia pasirinktą vietos šabloną ir procesus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="0bc36-357">Sukurkite papildymą</span><span class="sxs-lookup"><span data-stu-id="0bc36-357">Create replenishment</span></span>

<span data-ttu-id="0bc36-358">Sukūrę planą, turite sukurti *Papildymo darbą*, pagrįstą planu.</span><span class="sxs-lookup"><span data-stu-id="0bc36-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="0bc36-359">Veiksmų srityje pasirinkite **Vykdyti papildymą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="0bc36-360">Kai procesas baigiamas, atsiranda informacinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="0bc36-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="0bc36-361">Šis pranešimas nurodo antraščių, sukurtų darbo kūrimo ID, skaičių.</span><span class="sxs-lookup"><span data-stu-id="0bc36-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="0bc36-362">Vietos nurodymai, kurie bus naudojami, yra identifikuojami pagal nurodymo kodą, pateiktą kiekvienoje šablono eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0bc36-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="0bc36-363">Patarimai</span><span class="sxs-lookup"><span data-stu-id="0bc36-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="0bc36-364">Intervalo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bc36-364">Set up automatic slotting</span></span>

<span data-ttu-id="0bc36-365">Po to, kai visi reikiami elementai yra, galite nustatyti automatinį valdymą, atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="0bc36-366">Eikite į **Sandėlio valdymas \> Papildymas \> Atlikti intervalą**.</span><span class="sxs-lookup"><span data-stu-id="0bc36-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="0bc36-367">Nurodykite paleidžiančius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0bc36-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="0bc36-368">Pasirinkite vieną ar daugiau iš šių intervalo veiksmų:</span><span class="sxs-lookup"><span data-stu-id="0bc36-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="0bc36-369">Generuoti paklausą</span><span class="sxs-lookup"><span data-stu-id="0bc36-369">Generate demand</span></span>
    - <span data-ttu-id="0bc36-370">Surasti paklausą</span><span class="sxs-lookup"><span data-stu-id="0bc36-370">Locate demand</span></span>
    - <span data-ttu-id="0bc36-371">Kurti papildymo darbą</span><span class="sxs-lookup"><span data-stu-id="0bc36-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bc36-372">Intervalo veiksmai yra progresyvūs.</span><span class="sxs-lookup"><span data-stu-id="0bc36-372">The slotting steps are progressive.</span></span> <span data-ttu-id="0bc36-373">Jei norite pasirinkti *Surasti paklausą*, pirmiausia turite pasirinkti *Generuoti paklausą*.</span><span class="sxs-lookup"><span data-stu-id="0bc36-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="0bc36-374">Nurodyti naudotiną šabloną.</span><span class="sxs-lookup"><span data-stu-id="0bc36-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="0bc36-375">Jei norėsite, pakartojimas paleidžiamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="0bc36-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="0bc36-376">Norėdami atlikti scenarijų pratimus, **ne** nustatykite automatinio intervalo.</span><span class="sxs-lookup"><span data-stu-id="0bc36-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
