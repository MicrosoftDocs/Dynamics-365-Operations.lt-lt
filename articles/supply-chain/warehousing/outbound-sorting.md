---
title: Siunčiamas rūšiavimas
description: Šiame skyriuje pateikta informacija apie siunčiamą rūšiavimą. Ši funkcija padeda paprasčiau tvarkyti mažas talpyklas ir sandėlio darbuotojams geriau susiplanuoti ir suorganizuoti padėklų talpą sunkvežimyje.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3c576209a86f776ac424f7fb9f2b606bea774a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828399"
---
# <a name="outbound-sorting"></a><span data-ttu-id="67974-104">Siunčiamas rūšiavimas</span><span class="sxs-lookup"><span data-stu-id="67974-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67974-105">Ši funkcija padeda paprasčiau tvarkyti mažas talpyklas ir sandėlio darbuotojams geriau susiplanuoti ir suorganizuoti padėklų talpą sunkvežimyje.</span><span class="sxs-lookup"><span data-stu-id="67974-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="67974-106">Naudodami siunčiamą rūšiavimą galite rūšiuoti supakuotas talpyklas ant tinkamo padėklo po to, kai jie palieka pakavimo stotį.</span><span class="sxs-lookup"><span data-stu-id="67974-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="67974-107">Taip pat galite pastatyti pakavimo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="67974-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="67974-108">Ši funkcija leidžia sustatyti padėklus iš talpyklių, kurie yra supakuoti naudojant pakavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="67974-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="67974-109">Talpykla nėra siunčiama į galutinę siuntimo vietą taip kaip tai daroma originaliame pakavimo sraute.</span><span class="sxs-lookup"><span data-stu-id="67974-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="67974-110">Šiuo atveju darbuotojai gali uždaryti talpyklą ir patraukti ją į rūšiavimo tipo vietą.</span><span class="sxs-lookup"><span data-stu-id="67974-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="67974-111">Jie gali rūšiuoti talpyklas į padėtis, kurių kiekviena turi licencijos numerį (LP).</span><span class="sxs-lookup"><span data-stu-id="67974-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="67974-112">Po talpyklų rūšiavimo, galima sukurti užduotį, kuri bus siunčiama visą LP į galutinį siuntimo uostą ar tarpinę vietą pagal vietos instrukcijas ar jūsų pačių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="67974-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="67974-113">Taip pat, rūšiavimo vietos uždarymo veiksmas gali nedelsiant pergabenti inventorių į galutinę siuntimo vietą ir paimti jį į užsakymą.</span><span class="sxs-lookup"><span data-stu-id="67974-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="67974-114">Įjunkite Siunčiamo rūšiavimo funkciją</span><span class="sxs-lookup"><span data-stu-id="67974-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="67974-115">Prieš naudodami šią funkciją, turite ją įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="67974-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="67974-116">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="67974-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="67974-117">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="67974-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="67974-118">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="67974-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="67974-119">**Funkcijos pavadinimas:** *Siunčiamas rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="67974-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="67974-120">Sąranka</span><span class="sxs-lookup"><span data-stu-id="67974-120">Setup</span></span>

<span data-ttu-id="67974-121">Dėl šio scenarijaus, privalote naudoti standartinius **USMF** demo duomenis ir *62* sandėlį.</span><span class="sxs-lookup"><span data-stu-id="67974-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="67974-122">Taip pat privalote užbaigti sąranką, kuri aprašyta tolesniuose skirsniuose.</span><span class="sxs-lookup"><span data-stu-id="67974-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="67974-123">Bangos šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="67974-123">Set up a wave template</span></span>

<span data-ttu-id="67974-124">Ši sąranka automatiškai apdoroja bangą ir sukuria darbą, kai sandėliui yra išduodama linija.</span><span class="sxs-lookup"><span data-stu-id="67974-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="67974-125">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="67974-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="67974-126">Šabloniniame sąraše pasirinkite **Sandėlis 62**.</span><span class="sxs-lookup"><span data-stu-id="67974-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="67974-127">„FastTab“ **Bendra** įsitikinkite, kad **Bangos apdorojimas išleidžiant į sandėlį** parinktis yra nustatyta ties *Taip* padėtimi.</span><span class="sxs-lookup"><span data-stu-id="67974-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="67974-128">Nustatykite darbuotoją</span><span class="sxs-lookup"><span data-stu-id="67974-128">Set up a worker</span></span>

<span data-ttu-id="67974-129">Pakavimo stotis yra laikoma vieta.</span><span class="sxs-lookup"><span data-stu-id="67974-129">The packing station is considered a location.</span></span> <span data-ttu-id="67974-130">Sandėlio darbuotojai, pasirašantys pakavimo stotyje, mato ir dirba tik su siuntimais ir talpyklomis suplanuotomis specifinėje pakavimo vietoje.</span><span class="sxs-lookup"><span data-stu-id="67974-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="67974-131">Vartotojas prisijungęs prie „Microsoft Dynamics 365“ turi būti nustatytas kaip Sandėlio tvarkymo darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="67974-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="67974-132">Jei vartotojo vardas nepasirodo užduoties vartotojų sąraše, laikykitės šios procedūros jo pridėjimui.</span><span class="sxs-lookup"><span data-stu-id="67974-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="67974-133">Šiais žingsniais laikoma, kad vartotojas jau yra sistemoje ir buvo susietas kaip darbuotojas ar darbininkas **Žmogiškųjų išteklių** modulyje.</span><span class="sxs-lookup"><span data-stu-id="67974-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="67974-134">Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="67974-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="67974-135">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-135">Select **New**.</span></span>
1. <span data-ttu-id="67974-136">**Darbuotojo** laukelyje pasirinkite paskirties vartotoją darbuotojų sąraše.</span><span class="sxs-lookup"><span data-stu-id="67974-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="67974-137">Pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="67974-137">Select **Select**.</span></span>
1. <span data-ttu-id="67974-138">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="67974-139">**Vartotojų** „FastTab” skirtuke pasirinkite **Naujas** tam, kad sukurtumėte mobilaus prietaiso paskyrą ir nustatykite jai šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="67974-140">**Vartotojo identifikavimo numeris** Įveskite unikalų identifikavimo numerį.</span><span class="sxs-lookup"><span data-stu-id="67974-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="67974-141">**Vartotojo vardas:** Įveskite vardą identifikavimo numeriui.</span><span class="sxs-lookup"><span data-stu-id="67974-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="67974-142">**Nustatytasis sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-143">**Meniu pavadinimas:** *Pagrindinis*</span><span class="sxs-lookup"><span data-stu-id="67974-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="67974-144">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="67974-145">Pasirodo **Slaptažodžio nustatymas** teksto laukelis, kuriame galit sukurti paprastą slaptažodį, kurį vartotojas galės naudoti prisijungdamas prie mobilios programos.</span><span class="sxs-lookup"><span data-stu-id="67974-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="67974-146">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="67974-146">Set the following values:</span></span>

    - <span data-ttu-id="67974-147">**Slaptažodis:** Įveskite paprastą slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="67974-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="67974-148">**Patvirtinti slaptažodį:** Įveskite tą patį slaptažodį dar kartą.</span><span class="sxs-lookup"><span data-stu-id="67974-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="67974-149">Pasirinkite **Nustatyti slaptažodį**.</span><span class="sxs-lookup"><span data-stu-id="67974-149">Select **Set password**.</span></span>

    <span data-ttu-id="67974-150">Pranešimas Veiksmų centre jus informuos, kad slaptažodis buvo nustatytas jūsų sukurtam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="67974-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="67974-151">Sukurkite vietos tipą</span><span class="sxs-lookup"><span data-stu-id="67974-151">Create a location type</span></span>

1. <span data-ttu-id="67974-152">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos tipai**.</span><span class="sxs-lookup"><span data-stu-id="67974-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="67974-153">Veiksmų juostoje pasirinkite **Naujas** vietos tipo sukūrimui ir nustatykite jam šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="67974-154">**Vietos tipas:** *RŪŠIUOTI*</span><span class="sxs-lookup"><span data-stu-id="67974-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="67974-155">**Aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="67974-156">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="67974-157">Nustatykite Sandėlio tvarkymo parametrus</span><span class="sxs-lookup"><span data-stu-id="67974-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="67974-158">Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="67974-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="67974-159">**Pagrindiniame** skirtuke **Vietos tipai** „FastTab“ nustatykite **Vietos tipo rūšiavimo** laukelį į *RŪŠIUOTI* padėtį.</span><span class="sxs-lookup"><span data-stu-id="67974-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="67974-160">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="67974-161">Nustatykite vietos profilį</span><span class="sxs-lookup"><span data-stu-id="67974-161">Set up a location profile</span></span>

1. <span data-ttu-id="67974-162">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="67974-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="67974-163">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-164">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="67974-165">**Vietos profilio identifikavimo numeris:** *Rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="67974-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="67974-166">**Pavadinimas:** *Rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="67974-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="67974-167">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="67974-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-168">**Vietos formatas:** *ASRB* (Aisle-Rack-Shelf-Bin)</span><span class="sxs-lookup"><span data-stu-id="67974-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="67974-169">**Vietos tipas:** *RŪŠIUOTI*</span><span class="sxs-lookup"><span data-stu-id="67974-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="67974-170">**Naudoti licencijos numerio sekimą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="67974-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="67974-171">**Leisti maišytus elementus:** *Taip* (Kai nustatote šią parinktį į *Taip* padėtį, **Leisti maišyto inventoriaus paketus** parinktis automatiškai nustatoma į *Taip* padėtį ir nebegali būti keičiama nepriklausomai.)</span><span class="sxs-lookup"><span data-stu-id="67974-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="67974-172">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="67974-173">Nustatykite vietą</span><span class="sxs-lookup"><span data-stu-id="67974-173">Set up a location</span></span>

1. <span data-ttu-id="67974-174">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**.</span><span class="sxs-lookup"><span data-stu-id="67974-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="67974-175">Antraštėje išvalykite **Kurti patikrinimo skaičius vietai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="67974-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="67974-176">Veiksmų juostoje pasirinkite **Naujas** vietos tipo sukūrimui ir nustatykite jam šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="67974-177">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-178">**Vieta:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="67974-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="67974-179">**Vietos profilio identifikavimo numeris:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="67974-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="67974-180">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="67974-181">Nustatykite siunčiamo rūšiavimo šabloną</span><span class="sxs-lookup"><span data-stu-id="67974-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="67974-182">Siunčiamo rūšiavimo šablonas nustato, ar veiksmas yra sukuriamas vietos rūšiavimu sukurtas, ar rūšiavimas atliekamas rankiniu būdu, ar automatiškai.</span><span class="sxs-lookup"><span data-stu-id="67974-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="67974-183">Esant šiam scenarijui, sukursite siunčiamo rūšiavimo šabloną tam, kad sukurtumėte padėklus po pakavimo stoties.</span><span class="sxs-lookup"><span data-stu-id="67974-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="67974-184">Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Siunčiamo rūšiavimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="67974-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="67974-185">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-186">Naujojo šablono antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="67974-187">**Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Automatinis veiksmas*</span><span class="sxs-lookup"><span data-stu-id="67974-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="67974-188">**Aprašas:** *Automatinio veiksmo sukūrimas*</span><span class="sxs-lookup"><span data-stu-id="67974-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="67974-189">**Siunčiamo rūšiavimo šablono identifikavimo tipas:** *Talpykla*</span><span class="sxs-lookup"><span data-stu-id="67974-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="67974-190">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-191">**Vieta:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="67974-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="67974-192">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="67974-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-193">**Rūšiavimo patvirtinimas:** *Padėties nuskaitymas*</span><span class="sxs-lookup"><span data-stu-id="67974-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="67974-194">**Sukurkite veiksmą vietos uždaryme:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="67974-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="67974-195">Jei ši parinktis nustatyta *Taip*, vietos uždarymo metu, veiksmas bus sukuriamas inventoriaus nugabenimui į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="67974-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="67974-196">Jei ši parinktis nustatyta *Ne*, inventorius bus nedelsiant paimtas į užsakymą, kai padėtis bus uždaryta.</span><span class="sxs-lookup"><span data-stu-id="67974-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="67974-197">**Padėties priskyrimas:** *Automatinis*</span><span class="sxs-lookup"><span data-stu-id="67974-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="67974-198">Jei šis laukelis nustatytas į *Rankinį*, vartotojas privalo visuomet nurodyti padėtį, kurioje inventorius turi būti rūšiuojamas.</span><span class="sxs-lookup"><span data-stu-id="67974-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="67974-199">Jei jis nustatytas į *Automatinį*, sistema automatiškai ves inventorių į bet kurią jai prieinamą padėtį pagal rūšiavimo šablono pertrūkius.</span><span class="sxs-lookup"><span data-stu-id="67974-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="67974-200">Pasirinkite **Išsaugoti** tam, kad **Redaguoti užklausą** mygtuką pastatytumėte į Veiksmų juostą.</span><span class="sxs-lookup"><span data-stu-id="67974-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="67974-201">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="67974-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="67974-202">Užklausos tvarkyklės **Rūšiavimas** skirtuke įtraukite liniją su šiomis vertėmis:</span><span class="sxs-lookup"><span data-stu-id="67974-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="67974-203">**Lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="67974-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="67974-204">**Išvestinė lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="67974-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="67974-205">**Laukas:** *Vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="67974-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="67974-206">Kai pasirenkate šią vertę, galite gauti šį pranešimą: „Laukelio vežėjo paslaugos nėra indekso laukelis.</span><span class="sxs-lookup"><span data-stu-id="67974-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="67974-207">Ar norite įtraukti rūšiavimą?“</span><span class="sxs-lookup"><span data-stu-id="67974-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="67974-208">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="67974-208">Select **Yes**.</span></span>

    - <span data-ttu-id="67974-209">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="67974-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="67974-210">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-210">Select **OK**.</span></span>
1. <span data-ttu-id="67974-211">Galite gauti šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“</span><span class="sxs-lookup"><span data-stu-id="67974-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="67974-212">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="67974-212">Select **Yes**.</span></span>

    <span data-ttu-id="67974-213">**Siunčiamo rūšiavimo šablono pertrūkio** mygtukas pasirodo veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="67974-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="67974-214">Veiksmų juostoje pasirinkite **Siunčiamo rūšiavimo šablono pertrūkiai**.</span><span class="sxs-lookup"><span data-stu-id="67974-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="67974-215">**Siunčiamo rūšiavimo kriterijų** teksto laukelyje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="67974-216">**Referencinės lentelės pavadinimas:** *Siuntimai*</span><span class="sxs-lookup"><span data-stu-id="67974-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="67974-217">**Referencinis laukelio pavadinimas:** *Vežėjo paslaugos*</span><span class="sxs-lookup"><span data-stu-id="67974-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="67974-218">**Grupavimas laukeliais:** Pasirinkite šį žymimą laukelį tam, kad sugrupuotumėte siuntimo pagal vežėjo paslaugas.</span><span class="sxs-lookup"><span data-stu-id="67974-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="67974-219">Norėdami įrašyti parametrus ir uždaryti dialogo langą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="67974-220">Nustatykite konteinerio pakavimo politiką</span><span class="sxs-lookup"><span data-stu-id="67974-220">Set up container packing policies</span></span>

1. <span data-ttu-id="67974-221">Eikite į **Sandėlio tvarkymas \> Sąranka \> Talpyklos \> Talpyklos rūšiavimo politika**.</span><span class="sxs-lookup"><span data-stu-id="67974-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="67974-222">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-223">Naujosios politikos antraštėje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="67974-224">**Konteinerio pakavimo politika:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="67974-225">**Aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="67974-226">**Peržiūros** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-227">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-228">**Nustatytoji vieta rūšiavimui:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="67974-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="67974-229">**Svorio vienetas:** *kg*</span><span class="sxs-lookup"><span data-stu-id="67974-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="67974-230">**Talpyklos uždarymo politika:** *Automatinis išleidimas*</span><span class="sxs-lookup"><span data-stu-id="67974-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="67974-231">**Talpyklos išleidimo politika:** *Priskirti talpyklą prie siunčiamo rūšiavimo padėties*</span><span class="sxs-lookup"><span data-stu-id="67974-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="67974-232">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="67974-233">Pakavimo profilių nustatymas</span><span class="sxs-lookup"><span data-stu-id="67974-233">Set up packing profiles</span></span>

<span data-ttu-id="67974-234">Sukurkite naują pakavimo profilį, kuris bus naudojamas kartu su rūšiavimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="67974-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="67974-235">Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="67974-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="67974-236">Veiksmų juostoje pasirinkite **Naujas** linijos sukūrimui ir nustatykite jam šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="67974-237">**Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="67974-238">**Aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="67974-239">**Konteinerio pakavimo politika:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="67974-240">**Talpyklos identifikavimo numerio režimas:** *Automatinis*</span><span class="sxs-lookup"><span data-stu-id="67974-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="67974-241">**Talpyklos tipas:** *Plati dėžė*</span><span class="sxs-lookup"><span data-stu-id="67974-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="67974-242">**Automatinis talpyklos sukūrimas jam esant uždarytam:** Išvalyta (= *Ne*)</span><span class="sxs-lookup"><span data-stu-id="67974-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="67974-243">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="67974-244">Darbo klasių nustatymas</span><span class="sxs-lookup"><span data-stu-id="67974-244">Set up work classes</span></span>

<span data-ttu-id="67974-245">Nustatykite darbo klasę, kuri bus naudojama kartu su rūšiavimu.</span><span class="sxs-lookup"><span data-stu-id="67974-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="67974-246">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="67974-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="67974-247">Veiksmų juostoje pasirinkite **Naujas** rūšiavimo darbo klasės sukūrimui ir nustatykite jam šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="67974-248">**Darbo klasės identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="67974-249">**Aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="67974-250">**Darbo tvarkos tipas:** *Rūšiuoto inventoriaus paėmimas*</span><span class="sxs-lookup"><span data-stu-id="67974-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="67974-251">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="67974-252">Nustatykite mobilaus prietaiso meniu elementus</span><span class="sxs-lookup"><span data-stu-id="67974-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="67974-253">Nustatykite naujo padėklo meniu elementus</span><span class="sxs-lookup"><span data-stu-id="67974-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="67974-254">Sukurkite mobilaus prietaiso meniu elementus padėklų rūšiavimo metu sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="67974-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="67974-255">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="67974-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="67974-256">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-257">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="67974-258">**Meniu elemento pavadinimas:** *Padėklo sukūrimas*</span><span class="sxs-lookup"><span data-stu-id="67974-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="67974-259">**Pavadinimas:** *Padėklo sukūrimas*</span><span class="sxs-lookup"><span data-stu-id="67974-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="67974-260">**Režimas:** *Netiesioginis*</span><span class="sxs-lookup"><span data-stu-id="67974-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="67974-261">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="67974-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="67974-262">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="67974-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-263">**Veiksmo kodas:** *Siunčiamas rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="67974-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="67974-264">Kai laukelis nustatytas į *Siunčiamą rūšiavimą*, rodomas **Siunčiamo rūšiavimo šablono identifikavimo kodo** laukelis.</span><span class="sxs-lookup"><span data-stu-id="67974-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="67974-265">**Naudoti proceso gidą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="67974-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="67974-266">Kai **Veiksmo kodo** laukelis yra nustatytas į *Siunčiamą rūšiavimą*, ši parinktis automatiškai nustatoma į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="67974-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="67974-267">**Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Automatinis veiksmas*</span><span class="sxs-lookup"><span data-stu-id="67974-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="67974-268">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="67974-269">Nustatykite naujo krovimo meniu elementus</span><span class="sxs-lookup"><span data-stu-id="67974-269">Set up a new loading menu item</span></span>

<span data-ttu-id="67974-270">Po to, sukurkite meniu elementą leidžiantį vartotojams judinti rūšiuotus inventoriaus elementus į gabenimo vietą.</span><span class="sxs-lookup"><span data-stu-id="67974-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="67974-271">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="67974-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="67974-272">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-273">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="67974-274">**Meniu elemento pavadinimas:** *Krauti iš Rūšiavimo*</span><span class="sxs-lookup"><span data-stu-id="67974-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="67974-275">**Pavadinimas:** *Krauti iš Rūšiavimo*</span><span class="sxs-lookup"><span data-stu-id="67974-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="67974-276">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="67974-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="67974-277">**Naudoti esantį darbą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="67974-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="67974-278">**Bendra** „FastTab“, nustatykite **Valdoma** laukelį į *Valdoma vartotojo*.</span><span class="sxs-lookup"><span data-stu-id="67974-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="67974-279">**Darbo klasių** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="67974-280">**Darbo klasės identifikavimo numeris:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="67974-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="67974-281">**Darbo tvarkos tipas:** *Rūšiuoto inventoriaus paėmimas*</span><span class="sxs-lookup"><span data-stu-id="67974-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="67974-282">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="67974-283">Nustatykite mobilaus prietaiso meniu</span><span class="sxs-lookup"><span data-stu-id="67974-283">Set up the mobile device menu</span></span>

<span data-ttu-id="67974-284">Privalote dabar pridėti naujus meniu elementus į mobilaus prietaiso meniu.</span><span class="sxs-lookup"><span data-stu-id="67974-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="67974-285">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="67974-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="67974-286">Pasirinkite **Siunčiama** meniu.</span><span class="sxs-lookup"><span data-stu-id="67974-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="67974-287">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="67974-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="67974-288">**Esančiuose meniu ir meniu elementų** stulpelyje, suraskite ir pasirinkite **Padėklo kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="67974-289">Pasirinkite dešinės rodyklės mygtuką **Padėklo kūrimo** judinimui į **Meniu struktūros** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="67974-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="67974-290">Naudokite viršutinės ir apatinės rodyklės mygtukus **Padėklo kūrimo** meniu elementui padėti į norimą padėtį mobilaus prietaiso meniu.</span><span class="sxs-lookup"><span data-stu-id="67974-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="67974-291">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-291">Select **Save**.</span></span>
1. <span data-ttu-id="67974-292">Pakartokite šią procedūrą **Krauti iš rūšiavimo** meniu elemento įtraukimui į **Siuntimo** meniu.</span><span class="sxs-lookup"><span data-stu-id="67974-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="67974-293">Nustatyti vietos nurodymus</span><span class="sxs-lookup"><span data-stu-id="67974-293">Set up location directives</span></span>

<span data-ttu-id="67974-294">*Vietos direktyvos* yra taisyklės padedančios identifikuoti paėmimo ir padėjimo vietas inventoriaus judėjime.</span><span class="sxs-lookup"><span data-stu-id="67974-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="67974-295">Dabar privalote sukurti taisyklę rūšiavimo veiksmo valdymui.</span><span class="sxs-lookup"><span data-stu-id="67974-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="67974-296">Nustatykite vieną SKU direktyvą</span><span class="sxs-lookup"><span data-stu-id="67974-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="67974-297">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="67974-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="67974-298">Kairėje juostoje pakeiskite **Darbo tvarkos tipo** laukelio vertę į *Rūšiuoto inventoriaus paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="67974-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="67974-299">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-300">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="67974-301">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="67974-302">**Pavadinimas:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="67974-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="67974-303">**Padėties direktyvos** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-304">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="67974-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="67974-305">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="67974-305">**Site:** *6*</span></span>
    - <span data-ttu-id="67974-306">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-307">**Keletas SKU:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="67974-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="67974-308">Pasirinkite **Įrašyti** įrankių juostai padėti į **Linijos** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="67974-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="67974-309">**Linijos** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje.</span><span class="sxs-lookup"><span data-stu-id="67974-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="67974-310">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="67974-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="67974-311">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="67974-312">**Iš:** *0*</span><span class="sxs-lookup"><span data-stu-id="67974-312">**From:** *0*</span></span>
    - <span data-ttu-id="67974-313">**Į:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="67974-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="67974-314">Pasirinkite **Įrašyti** įrankių juostai padėti į **Vietos direktyvos veiksmai** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="67974-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="67974-315">**Vietos direktyvos veiksmai** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje.</span><span class="sxs-lookup"><span data-stu-id="67974-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="67974-316">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="67974-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="67974-317">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="67974-318">**Pavadinimas:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="67974-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="67974-319">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-319">Select **Save**.</span></span>
1. <span data-ttu-id="67974-320">„FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="67974-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="67974-321">Užklausos tvarkyklėje, **Intervalas** skirtuke, suraskite eilutę, kurioje **Laukelis** laukelis yra nustatytas į *Vieta*.</span><span class="sxs-lookup"><span data-stu-id="67974-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="67974-322">Nustatykite **Kriterijų** laukelį šiai eilutei į *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="67974-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="67974-323">Pasirinkite **OK** tam, kad įrašytumėte savo nustatymus uždarytumėte užklausos tvarkyklę.</span><span class="sxs-lookup"><span data-stu-id="67974-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="67974-324">Nustatykite kelių SKU direktyvų</span><span class="sxs-lookup"><span data-stu-id="67974-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="67974-325">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="67974-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="67974-326">Kairėje juostoje pakeiskite **Darbo tvarkos tipo** laukelio vertę į *Rūšiuoto inventoriaus paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="67974-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="67974-327">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-328">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="67974-329">**Seka:** *2*</span><span class="sxs-lookup"><span data-stu-id="67974-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="67974-330">**Pavadinimas:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="67974-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="67974-331">**Padėties direktyvos** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-332">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="67974-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="67974-333">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="67974-333">**Site:** *6*</span></span>
    - <span data-ttu-id="67974-334">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-335">**Keletas SKU:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="67974-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="67974-336">Pasirinkite **Įrašyti** įrankių juostai padėti į **Linijos** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="67974-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="67974-337">**Linijos** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje.</span><span class="sxs-lookup"><span data-stu-id="67974-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="67974-338">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="67974-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="67974-339">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="67974-340">**Iš:** *0*</span><span class="sxs-lookup"><span data-stu-id="67974-340">**From:** *0*</span></span>
    - <span data-ttu-id="67974-341">**Į:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="67974-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="67974-342">Pasirinkite **Įrašyti** įrankių juostai padėti į **Vietos direktyvos veiksmai** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="67974-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="67974-343">**Vietos direktyvos veiksmai** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje.</span><span class="sxs-lookup"><span data-stu-id="67974-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="67974-344">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="67974-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="67974-345">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="67974-346">**Pavadinimas:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="67974-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="67974-347">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-347">Select **Save**.</span></span>
1. <span data-ttu-id="67974-348">„FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="67974-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="67974-349">Užklausos tvarkyklėje, **Intervalas** skirtuke, suraskite eilutę, kurioje **Laukelis** laukelis yra nustatytas į *Vieta*.</span><span class="sxs-lookup"><span data-stu-id="67974-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="67974-350">Nustatykite **Kriterijų** laukelį šiai eilutei į *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="67974-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="67974-351">Pasirinkite **OK** tam, kad įrašytumėte savo nustatymus uždarytumėte užklausos tvarkyklę.</span><span class="sxs-lookup"><span data-stu-id="67974-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="67974-352">Nustatyti darbo šablonus</span><span class="sxs-lookup"><span data-stu-id="67974-352">Set up work templates</span></span>

1. <span data-ttu-id="67974-353">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="67974-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="67974-354">Pakeiskite **Darbo tvarkos tipo** laukelio vertę į *Rūšiuoto inventoriaus paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="67974-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="67974-355">Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="67974-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="67974-356">**Peržiūros** skirtuke, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="67974-357">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="67974-358">**Darbo šablonas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="67974-359">**Darbo šablono aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="67974-360">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Darbo šablono išsami informacija** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="67974-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="67974-361">**Darbo šablono informacija** „FastTab“ pasirinkite **Naujas** tam, kad pridėtumėte liniją ir tuomet nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="67974-362">**Darbo tipas:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="67974-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="67974-363">**Darbo klasės identifikavimo numeris:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="67974-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="67974-364">Pasirinkite **Naujas** dar kartą, kad pridėtumėte antrą liniją ir tuomet nustatykite jai šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="67974-365">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="67974-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="67974-366">**Darbo klasės identifikavimo numeris:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="67974-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="67974-367">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="67974-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="67974-368">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="67974-368">Scenario</span></span>

<span data-ttu-id="67974-369">Scenarijus simuliuoja situaciją, kai paimtos talpyklos turėtų automatiškai būti rūšiuojamos į skirtingas padėtis (padėklus) po pakavimo stoties priklausomai nuo siuntimo vežėjo paslaugos.</span><span class="sxs-lookup"><span data-stu-id="67974-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="67974-370">Po to, kai visi elementai iš pakrovimo yra supakuoti ir rūšiuoti pagal adresą, padėklai bus patraukti į „bay door“.</span><span class="sxs-lookup"><span data-stu-id="67974-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="67974-371">Sukurkite prekybos užsakymus ir paėmimo tvarką</span><span class="sxs-lookup"><span data-stu-id="67974-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="67974-372">Pardavimo užsakymo 1 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="67974-372">Create sales order 1</span></span>

1. <span data-ttu-id="67974-373">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="67974-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="67974-374">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-375">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="67974-376">**Kliento sąskaita:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="67974-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="67974-377">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="67974-378">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="67974-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="67974-379">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="67974-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="67974-380">Perjunkite **Antraštės** rodinį.</span><span class="sxs-lookup"><span data-stu-id="67974-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="67974-381">„FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="67974-382">**Siuntos vežėjas:** *Oro transportas*</span><span class="sxs-lookup"><span data-stu-id="67974-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="67974-383">**Vežėjo paslauga:** *oro*</span><span class="sxs-lookup"><span data-stu-id="67974-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="67974-384">Perjunkite į **Linijų** peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="67974-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="67974-385">Jei nauja, tuščia linija nėra automatiškai įtraukta į tinklelį **Prekybos užsakymo linijų** „FastTab“, vienos linijos įtraukimui pasirinkite **Įtraukti liniją**.</span><span class="sxs-lookup"><span data-stu-id="67974-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="67974-386">Naujo užsakymo linijoje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="67974-387">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="67974-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="67974-388">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="67974-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="67974-389">Kai naujo užsakymo linija dar yra pasirinkta **Prekybos užsakymo linijoje** „FastTab“, **Inventoriaus** meniu virš tinklelio, pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="67974-390">**Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** viso pasirinktos linijos sandėlyje kiekio rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="67974-391">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="67974-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="67974-392">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="67974-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="67974-393">Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą.</span><span class="sxs-lookup"><span data-stu-id="67974-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="67974-394">Užrašykite bangos identifikavimo kodo pastabą ir siuntimo identifikavimo numerius.</span><span class="sxs-lookup"><span data-stu-id="67974-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="67974-395">Pardavimo užsakymas 2</span><span class="sxs-lookup"><span data-stu-id="67974-395">Sales order 2</span></span>

1. <span data-ttu-id="67974-396">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="67974-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="67974-397">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="67974-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="67974-398">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="67974-399">**Kliento sąskaita:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="67974-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="67974-400">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="67974-401">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="67974-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="67974-402">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="67974-402">The new sales order is opened.</span></span> <span data-ttu-id="67974-403">Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="67974-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="67974-404">Nustatykite šias vertes užsakymo linijoje:</span><span class="sxs-lookup"><span data-stu-id="67974-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="67974-405">**Prekė:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="67974-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="67974-406">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="67974-407">**Linijos informacijoje** „FastTab“, **Pristatymo** skirtuke, nustatykite **Pristatymo būdo** laukelį į *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="67974-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="67974-408">**Prekybos užsakymo linijos** „FastTab“, pasirinkite **Įtraukti liniją** ir tuomet nustatykite tolesnes vertes antrojo užsakymo linijoje:</span><span class="sxs-lookup"><span data-stu-id="67974-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="67974-409">**Prekė:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="67974-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="67974-410">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="67974-411">**Linijos informacijoje** „FastTab“, **Pristatymo** skirtuke, pakeiskite **Pristatymo būdo** laukelio vertę į *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="67974-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="67974-412">**Prekybos užsakymo linijos** „FastTab“, pasirinkite pirmojo užsakymo liniją.</span><span class="sxs-lookup"><span data-stu-id="67974-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="67974-413">Vėliau,**Inventorius** meniu virš tinklelio, pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="67974-414">**Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** viso pasirinktos linijos sandėlyje kiekio rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="67974-415">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="67974-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="67974-416">**Prekybos užsakymo linijos** „FastTab“, pasirinkite antrojo užsakymo liniją.</span><span class="sxs-lookup"><span data-stu-id="67974-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="67974-417">Vėliau,**Inventorius** meniu virš tinklelio, pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="67974-418">**Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** viso pasirinktos linijos sandėlyje kiekio rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="67974-419">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="67974-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="67974-420">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="67974-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="67974-421">Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą.</span><span class="sxs-lookup"><span data-stu-id="67974-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="67974-422">Atkreipkite dėmesį, kad dviejų bangų identifikavimo numeriai ir du siuntimo identifikavimo numeriai buvo sukurti, kiekvienas iš jų teko pristatymo būdui prekybos užsakymo linijose.</span><span class="sxs-lookup"><span data-stu-id="67974-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="67974-423">Gaukite darbo identifikavimo numerį iš darbo informacijos</span><span class="sxs-lookup"><span data-stu-id="67974-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="67974-424">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="67974-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="67974-425">Puslapis rodo darbo identifikavimo numerį, kuris buvo sukurtas iš prekybos užsakymų.</span><span class="sxs-lookup"><span data-stu-id="67974-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="67974-426">Naudokite bangos ir siuntimo identifikavimo numerius prekybos užsakymams, kuriuos kursite tam, kad surastumėte darbo identifikavimo numerį kiekvienai bangai ir siuntimui.</span><span class="sxs-lookup"><span data-stu-id="67974-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="67974-427">Pažymėkite šiuos darbo identifikavimo numerius, nes jums jų reikės kituose žingsniuose.</span><span class="sxs-lookup"><span data-stu-id="67974-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="67974-428">Atkreipkite dėmesį, kad du darbo identifikavimo numeriai buvo sukurti antrajam prekybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="67974-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="67974-429">Jei paimami skirtingi elementai iš skirtingų vietų, sukuriamas atskiras žodžių identifikavimo numeris.</span><span class="sxs-lookup"><span data-stu-id="67974-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="67974-430">Paėmimo elementai prekybos užsakymui</span><span class="sxs-lookup"><span data-stu-id="67974-430">Pick items for the sales orders</span></span>

<span data-ttu-id="67974-431">Užbaikite sukurtą darbą naudodami mobilų įrenginį, kuriuo perkelsite elementus į pakavimo stotį.</span><span class="sxs-lookup"><span data-stu-id="67974-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="67974-432">Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).</span><span class="sxs-lookup"><span data-stu-id="67974-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="67974-433">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="67974-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="67974-434">**Siunčiama** meniu pasirinkite **Prekybos paėmimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="67974-435">**identifikavimo kodo** laukelyje įveskite darbo identifikavimo kodą, kuris buvo sukurtas prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="67974-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="67974-436">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-436">Select **OK**.</span></span>
1. <span data-ttu-id="67974-437">**Prekybos užsakymai - Paėmimas** puslapyje įveskite paskirties LP, kuris buvo sukurtas prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="67974-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="67974-438">Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*bulk-001*), elementas (*A0001*) ir kokybė (*2 vnt.*).</span><span class="sxs-lookup"><span data-stu-id="67974-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="67974-439">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-439">Select **OK**.</span></span>
1. <span data-ttu-id="67974-440">Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="67974-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="67974-441">**Loc** laukelis turi rodyti, kad paimti elementai bus *Pakavimo* vietoje.</span><span class="sxs-lookup"><span data-stu-id="67974-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="67974-442">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-442">Select **OK**.</span></span>

    <span data-ttu-id="67974-443">**Nuskaityti darbo / licencijos numerio identifikavimo kodą** puslapyje gausite „Darbas baigtas“ pranešimą, kuris rodo, jog darbo identifikavimo kodas ir prekybos užsakymas 1 buvo užbaigti.</span><span class="sxs-lookup"><span data-stu-id="67974-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="67974-444">Dabar paimsite prekybos užsakymą 2.</span><span class="sxs-lookup"><span data-stu-id="67974-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="67974-445">**identifikavimo kodo** laukelyje įveskite darbo identifikavimo kodą, kuris buvo sukurtas prekybos užsakymui 2, kuriame linija 1 turi elementą *A0001*.</span><span class="sxs-lookup"><span data-stu-id="67974-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="67974-446">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-446">Select **OK**.</span></span>
1. <span data-ttu-id="67974-447">**Prekybos užsakymai - Paėmimas** puslapyje įveskite paskirties LP.</span><span class="sxs-lookup"><span data-stu-id="67974-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="67974-448">Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*bulk-001*), elementas (*A0001*) ir kokybė (*1 vnt.*).</span><span class="sxs-lookup"><span data-stu-id="67974-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="67974-449">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-449">Select **OK**.</span></span>
1. <span data-ttu-id="67974-450">Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="67974-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="67974-451">**Loc** laukelis turi rodyti, kad paimti elementai bus *Pakavimo* vietoje.</span><span class="sxs-lookup"><span data-stu-id="67974-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="67974-452">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-452">Select **OK**.</span></span>

    <span data-ttu-id="67974-453">**Darbo / licencijos numerio identifikavimo kodo nuskaitymo** puslapyje jums bus parodytas pranešimas „Darbas baigtas“.</span><span class="sxs-lookup"><span data-stu-id="67974-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="67974-454">Šis pranešimas rodo, kad darbo identifikavimo kodas 2 prekybos užsakymo 1 linijoje buvo užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="67974-455">**identifikavimo kodo** laukelyje įveskite darbo identifikavimo kodą, kuris buvo sukurtas prekybos užsakymui 2, kuriame linija 2 turi elementą *A0002*.</span><span class="sxs-lookup"><span data-stu-id="67974-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="67974-456">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-456">Select **OK**.</span></span>
1. <span data-ttu-id="67974-457">**Prekybos užsakymai - Paėmimas** puslapyje įveskite paskirties LP.</span><span class="sxs-lookup"><span data-stu-id="67974-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="67974-458">Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*bulk-002*), elementas (*A0001*) ir kokybė (*1 vnt.*).</span><span class="sxs-lookup"><span data-stu-id="67974-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="67974-459">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-459">Select **OK**.</span></span>
1. <span data-ttu-id="67974-460">Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="67974-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="67974-461">**Loc** laukelis turi rodyti, kad paimti elementai bus *Pakavimo* vietoje.</span><span class="sxs-lookup"><span data-stu-id="67974-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="67974-462">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-462">Select **OK**.</span></span>

    <span data-ttu-id="67974-463">**Darbo / licencijos numerio identifikavimo kodo nuskaitymo** puslapyje jums bus parodytas pranešimas „Darbas baigtas“.</span><span class="sxs-lookup"><span data-stu-id="67974-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="67974-464">Šis pranešimas rodo, kad darbo identifikavimo kodas 2 prekybos užsakymo 2 linijoje buvo užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="67974-465">Prekybos užsakymų pakavimas į talpyklas</span><span class="sxs-lookup"><span data-stu-id="67974-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="67974-466">Prekybos užsakymo 1 pakavimas į talpyklas</span><span class="sxs-lookup"><span data-stu-id="67974-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="67974-467">Eikite į **Sandėlio tvarkymas \> Pakavimas ir dėjimas į talpyklas \> Pakavimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="67974-468">Pasirodo **Pasirinkit pakavimo stotį** teksto laukelis.</span><span class="sxs-lookup"><span data-stu-id="67974-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="67974-469">Pagal nutylėjimą, **Darbuotojo** laukelis turi būti nustatytas į darbuotojo vardą, kurį nustatėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="67974-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="67974-470">Nustatykite tolesnes vertes tam, kad peržiūrėtumėte ir dirbtumėte su siuntimais ir talpyklomis, kuriuos yra planuojamos konkrečioje pakavimo vietoje:</span><span class="sxs-lookup"><span data-stu-id="67974-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="67974-471">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="67974-471">**Site:** *6*</span></span>
    - <span data-ttu-id="67974-472">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="67974-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="67974-473">**Vieta:** *Pakavimas*</span><span class="sxs-lookup"><span data-stu-id="67974-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="67974-474">**Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="67974-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="67974-475">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="67974-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="67974-476">**Pakavimo** puslapyje, **Licencijos numeris ar siuntimas** laukelyje įveskite paskirties LP prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="67974-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="67974-477">Tuomet pasirinkite **Skirtuką** ar **Įvesties** raktą savo klaviatūroje, kad išeitumėte iš laukelio.</span><span class="sxs-lookup"><span data-stu-id="67974-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="67974-478">Veiksmų juostoje pasirinkite **Naujas talpykla**.</span><span class="sxs-lookup"><span data-stu-id="67974-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="67974-479">Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="67974-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="67974-480">Užsirašykite talpyklos identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="67974-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="67974-481">**Elemento pakavimo** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-482">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="67974-483">**Identifikavimo kodo:** Elementas *A0001*</span><span class="sxs-lookup"><span data-stu-id="67974-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="67974-484">Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.</span><span class="sxs-lookup"><span data-stu-id="67974-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="67974-485">**Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį** tam, kad sistema atnaujintų **Bendro svorio** laukelį.</span><span class="sxs-lookup"><span data-stu-id="67974-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="67974-486">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-486">Select **OK**.</span></span> <span data-ttu-id="67974-487">Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="67974-488">Sukurkite antrą talpyklą tam, kad įtrauktumėte antrą elementą iš LP prekybos užsakymo 1 į naują talpyklą.</span><span class="sxs-lookup"><span data-stu-id="67974-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="67974-489">Veiksmų juostoje pasirinkite **Naujas talpykla**.</span><span class="sxs-lookup"><span data-stu-id="67974-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="67974-490">Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="67974-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="67974-491">Užsirašykite talpyklos identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="67974-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="67974-492">**Elemento pakavimo** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-493">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="67974-494">**Identifikavimo kodo:** Elementas *A0001*</span><span class="sxs-lookup"><span data-stu-id="67974-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="67974-495">Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.</span><span class="sxs-lookup"><span data-stu-id="67974-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="67974-496">**Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį** tam, kad sistema atnaujintų **Bendro svorio** laukelį.</span><span class="sxs-lookup"><span data-stu-id="67974-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="67974-497">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-497">Select **OK**.</span></span> <span data-ttu-id="67974-498">Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="67974-499">Prekybos užsakymo 2 pakavimas į talpyklas</span><span class="sxs-lookup"><span data-stu-id="67974-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="67974-500">**Pakavimo** puslapyje, **Licencijos numeris ar siuntimas** laukelyje įveskite paskirties LP prekybos užsakymui 2.</span><span class="sxs-lookup"><span data-stu-id="67974-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="67974-501">Tuomet pasirinkite **Skirtuką** ar **Įvesties** raktą savo klaviatūroje, kad išeitumėte iš laukelio.</span><span class="sxs-lookup"><span data-stu-id="67974-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="67974-502">Veiksmų juostoje pasirinkite **Naujas talpykla**.</span><span class="sxs-lookup"><span data-stu-id="67974-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="67974-503">Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="67974-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="67974-504">Užsirašykite talpyklos identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="67974-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="67974-505">**Elemento pakavimo** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-506">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="67974-507">**Identifikavimo kodo:** Elementas *A0001*</span><span class="sxs-lookup"><span data-stu-id="67974-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="67974-508">Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.</span><span class="sxs-lookup"><span data-stu-id="67974-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="67974-509">**Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį** tam, kad sistema atnaujintų **Bendro svorio** laukelį.</span><span class="sxs-lookup"><span data-stu-id="67974-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="67974-510">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-510">Select **OK**.</span></span> <span data-ttu-id="67974-511">Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="67974-512">**Licencijos numeris ar siuntimas** laukelyje įveskite paskirties LP prekybos užsakymui 2.</span><span class="sxs-lookup"><span data-stu-id="67974-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="67974-513">Tuomet pasirinkite **Skirtuką** ar **Įvesties** raktą savo klaviatūroje, kad išeitumėte iš laukelio.</span><span class="sxs-lookup"><span data-stu-id="67974-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="67974-514">Veiksmų juostoje pasirinkite **Naujas talpykla**.</span><span class="sxs-lookup"><span data-stu-id="67974-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="67974-515">Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="67974-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="67974-516">Užsirašykite talpyklos identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="67974-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="67974-517">**Elemento pakavimo** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="67974-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="67974-518">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="67974-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="67974-519">**Identifikavimo laukelis:** Elementas *A0002*</span><span class="sxs-lookup"><span data-stu-id="67974-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="67974-520">Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.</span><span class="sxs-lookup"><span data-stu-id="67974-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="67974-521">**Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį** tam, kad sistema atnaujintų **Bendro svorio** laukelį.</span><span class="sxs-lookup"><span data-stu-id="67974-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="67974-522">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-522">Select **OK**.</span></span> <span data-ttu-id="67974-523">Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="67974-524">Talpyklos informacijos peržiūrai, eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į talpyklas \> Talpyklos** ir ieškokite talpyklos identifikavimo kodo, kuris buvo sukurtas pakavimo metu.</span><span class="sxs-lookup"><span data-stu-id="67974-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="67974-525">Rūšiuokite talpyklas</span><span class="sxs-lookup"><span data-stu-id="67974-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67974-526">Patekę į **Padėklo kūrimo** meniu elementą mobiliame prietaise rūšiavimo siuntimui, matysite mygtuką pavadinimu **Pilnas**.</span><span class="sxs-lookup"><span data-stu-id="67974-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="67974-527">*Nenaudokite **Pilnas** mygtuko padėties rūšiavimui ir uždarymui.*</span><span class="sxs-lookup"><span data-stu-id="67974-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="67974-528">**Pilnas** mygtukas yra pateikiamas pagal nutylėjimą ir negali būti išjungtas ar pašalintas iš puslapio.</span><span class="sxs-lookup"><span data-stu-id="67974-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="67974-529">Jis nėra naudojamas *Siunčiamo rūšiavimo* funkcijai.</span><span class="sxs-lookup"><span data-stu-id="67974-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="67974-530">Rūšiuokite pirmą talpyklą</span><span class="sxs-lookup"><span data-stu-id="67974-530">Sort the first container</span></span>

1. <span data-ttu-id="67974-531">Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).</span><span class="sxs-lookup"><span data-stu-id="67974-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="67974-532">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="67974-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="67974-533">**Siunčiama** meniu pasirinkite **Padėklo sukūrimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="67974-534">**LP/Con** laukelyje įveskite pirmosios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 1.</span><span class="sxs-lookup"><span data-stu-id="67974-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="67974-535">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-535">Select **OK**.</span></span>
1. <span data-ttu-id="67974-536">Kadangi šiuo metu nėra jokių rūšiavimo padėčių, turite bent vieną nurodyti.</span><span class="sxs-lookup"><span data-stu-id="67974-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="67974-537">**Rūšiavimo padėties identifikavimo kodo** laukelyje įveskite *SP01*.</span><span class="sxs-lookup"><span data-stu-id="67974-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="67974-538">Kadangi šiuo metu nėra susieto jokio LP su esama padėtimi *SP01*, turite bent vieną nurodyti.</span><span class="sxs-lookup"><span data-stu-id="67974-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="67974-539">**LP** laukelyje įveskite *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="67974-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="67974-540">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-540">Select **OK**.</span></span>
1. <span data-ttu-id="67974-541">Kadangi rūšiavimo padėties patvirtinimas yra įjungtas, privalo įvesti rūšiavimo padėties identifikavimo kodą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="67974-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="67974-542">**Rūšiavimo padėties identifikavimo kodo** laukelyje įveskite *SP01*.</span><span class="sxs-lookup"><span data-stu-id="67974-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="67974-543">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-543">Select **OK**.</span></span>

    <span data-ttu-id="67974-544">Matysite „Darbas baigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="67974-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="67974-545">Rūšiuotos padėties peržiūrai ir LP joje peržiūrai, eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į konteinerius \> Siunčiamo rūšiavimo padėties priskyrimai**.</span><span class="sxs-lookup"><span data-stu-id="67974-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="67974-546">**Siunčiamo rūšiavimo padėties priskyrimai** langas rodo visas rūšiavimo padėtis, kurios šiuo metu yra įjungtos.</span><span class="sxs-lookup"><span data-stu-id="67974-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="67974-547">**Rūšiavimo padėties pervedimai** laukelis rodo LP, kuris yra susietas su kiekviena rūšiavimo padėtimi ir rūšiavimo padėtyje nesančiomis talpyklomis.</span><span class="sxs-lookup"><span data-stu-id="67974-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="67974-548">Atkreipkite dėmesį, kad viena rūšiavimo padėtis šiuo metu egzistuoja ir **Padėties rūšiavimo kriterijų** „FastTab“ rodo **Siuntimo – Vežėjo paslaugų - Oro** kriterijų.</span><span class="sxs-lookup"><span data-stu-id="67974-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="67974-549">Rūšiuokite likusias talpyklas</span><span class="sxs-lookup"><span data-stu-id="67974-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="67974-550">Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).</span><span class="sxs-lookup"><span data-stu-id="67974-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="67974-551">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="67974-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="67974-552">**Siunčiama** meniu pasirinkite **Padėklo sukūrimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="67974-553">**LP/Con** laukelyje įveskite antrosios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 1.</span><span class="sxs-lookup"><span data-stu-id="67974-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="67974-554">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-554">Select **OK**.</span></span> <span data-ttu-id="67974-555">Kadangi rūšiavimo šablonas yra nustatytas automatiniam rūšiavimui ir kriterijus atitinkantis padėties rūšiavimas jau egzistuoja, esate automatiškai nukreipiami į tinkamą rūšiavimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="67974-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="67974-556">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-556">Select **OK**.</span></span>
1. <span data-ttu-id="67974-557">Patvirtinkite rūšiavimo padėties identifikavimo kodą tam, kad nurodytumėte, jog inventorius yra tinkamoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="67974-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="67974-558">**Rūšiavimo padėties identifikavimo kodo** laukelyje įveskite *SP01*.</span><span class="sxs-lookup"><span data-stu-id="67974-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="67974-559">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-559">Select **OK**.</span></span>

    <span data-ttu-id="67974-560">Darbas yra baigtas antrojoje talpykloje iš prekybos užsakymo 1.</span><span class="sxs-lookup"><span data-stu-id="67974-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="67974-561">Dabar rūšiuosite likusias talpyklas iš prekybos užsakymo 2.</span><span class="sxs-lookup"><span data-stu-id="67974-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="67974-562">**LP/Con** laukelyje įveskite antrosios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 2 *A0001*.</span><span class="sxs-lookup"><span data-stu-id="67974-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="67974-563">Kadangi vežėjo paslaugos skiriasi, jums siūloma įvesti naują rūšiavimo padėtį ir priskirti LP tai padėčiai.</span><span class="sxs-lookup"><span data-stu-id="67974-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="67974-564">Naudokite padėties rūšiavimą *SP02* ir LP *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="67974-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="67974-565">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-565">Select **OK**.</span></span>
1. <span data-ttu-id="67974-566">Patikrinkite rūšiavimo padėtį įvesdami *SP02* **Padėties rūšiavimo identifikavimo kodo** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="67974-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="67974-567">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-567">Select **OK**.</span></span>

    <span data-ttu-id="67974-568">Darbas talpykloje baigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="67974-569">**LP/Con** laukelyje įveskite likusios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 2 *A0002*.</span><span class="sxs-lookup"><span data-stu-id="67974-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="67974-570">Kadangi vežėjo paslaugos sutampa su prekybos užsakymo 1 vežėjo paslaugomis, sistema rodo esančią rūšiavimo padėtį, kuri atitinka kriterijus.</span><span class="sxs-lookup"><span data-stu-id="67974-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="67974-571">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-571">Select **OK**.</span></span>
1. <span data-ttu-id="67974-572">Patikrinkite rūšiavimo padėtį įvesdami *SP02* **Padėties rūšiavimo identifikavimo kodo** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="67974-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="67974-573">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-573">Select **OK**.</span></span>

    <span data-ttu-id="67974-574">Darbas talpykloje baigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="67974-575">Uždarykite siunčiamo rūšiavimo padėtis</span><span class="sxs-lookup"><span data-stu-id="67974-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="67974-576">Kai inventorius yra rūšiuotas, padėtis turi būti uždaryti prieš darbo sukūrimą.</span><span class="sxs-lookup"><span data-stu-id="67974-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="67974-577">Rūšiuoto inventoriaus paėmimo darbas bus sukuriamas tam, kad inventorius būtų paimtas į „bay door“.</span><span class="sxs-lookup"><span data-stu-id="67974-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="67974-578">Uždarykite padėtį mobiliame prietaise</span><span class="sxs-lookup"><span data-stu-id="67974-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="67974-579">Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).</span><span class="sxs-lookup"><span data-stu-id="67974-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="67974-580">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="67974-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="67974-581">**Siunčiama** meniu pasirinkite **Padėklo sukūrimas**.</span><span class="sxs-lookup"><span data-stu-id="67974-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="67974-582">**LP/Con** laukelyje įveskite talpyklos identifikavimo numerį, kuris buvo rūšiuotas padėties *SP01* rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="67974-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="67974-583">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-583">Select **OK**.</span></span>
1. <span data-ttu-id="67974-584">Matysite šį pranešimą: „Talpykla jau rūšiuota padėčiai SP01.</span><span class="sxs-lookup"><span data-stu-id="67974-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="67974-585">Uždaryti padėtį?“</span><span class="sxs-lookup"><span data-stu-id="67974-585">Close the position?"</span></span> <span data-ttu-id="67974-586">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="67974-586">Select **Close**.</span></span>

    <span data-ttu-id="67974-587">Darbas užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="67974-588">Uždaryti padėtį iš siunčiamo rūšiavimo padėties priskyrimo</span><span class="sxs-lookup"><span data-stu-id="67974-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="67974-589">Eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į konteinerius \> Siunčiamo rūšiavimo padėties priskyrimai**.</span><span class="sxs-lookup"><span data-stu-id="67974-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="67974-590">Kairiame stulpelyje pasirinkite **SP02**.</span><span class="sxs-lookup"><span data-stu-id="67974-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="67974-591">Ši siunčiamo rūšiavimo padėties eilutė yra ta, kurią uždarėte.</span><span class="sxs-lookup"><span data-stu-id="67974-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="67974-592">Veiksmų juostoje pasirinkite **Uždaryti padėtį**.</span><span class="sxs-lookup"><span data-stu-id="67974-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="67974-593">Rūšiavimo padėties įrašas yra uždarytas ir neberodomas.</span><span class="sxs-lookup"><span data-stu-id="67974-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="67974-594">Visų uždarytų padėčių įrašų rodymui, pasirinkite **Rodyti uždarytus** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="67974-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="67974-595">Surūšiuotų atsargų paėmimas</span><span class="sxs-lookup"><span data-stu-id="67974-595">Sorted inventory picking</span></span>

<span data-ttu-id="67974-596">Privalote pabaigti rūšiuoto inventoriaus paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="67974-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="67974-597">Kai jis pabaigtas, inventorius bus paimamas į prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="67974-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="67974-598">Dabar, visi kiti sandėlio procesai yra pritaikyti.</span><span class="sxs-lookup"><span data-stu-id="67974-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="67974-599">Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).</span><span class="sxs-lookup"><span data-stu-id="67974-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="67974-600">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="67974-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="67974-601">**Siunčiama** meniu pasirinkite **Pakrovimas iš rūšiavimo**.</span><span class="sxs-lookup"><span data-stu-id="67974-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="67974-602">Įveskite paskirties LP identifikavimo kodą iš pirmosios rūšiavimo padėties, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="67974-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="67974-603">Nustatykite **identifikavimo kodo** lauką į *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="67974-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="67974-604">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-604">Select **OK**.</span></span>
1. <span data-ttu-id="67974-605">**Rūšiuoto inventoriaus paėmimas: Paimti** puslapis rodo būtiną atlikti paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="67974-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="67974-606">Paimkite iš *SORT* vietos ir paskirties LP *PLP01* turės daugelį elementų ir *3* kiekį.</span><span class="sxs-lookup"><span data-stu-id="67974-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="67974-607">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-607">Select **OK**.</span></span>
1. <span data-ttu-id="67974-608">**Rūšiuoto inventoriaus paėmimas: Padėti** puslapis rodo būtiną atlikti padėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="67974-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="67974-609">Padėkite į *Baydoor* vietą ir paskirties LP *PLP01* turės daugelį elementų ir *3* kiekį.</span><span class="sxs-lookup"><span data-stu-id="67974-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="67974-610">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-610">Select **OK**.</span></span>

    <span data-ttu-id="67974-611">Darbas užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-611">Work is completed.</span></span>

1. <span data-ttu-id="67974-612">Įveskite paskirties licencijos numerio identifikavimo kodą iš antrosios rūšiavimo padėties, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="67974-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="67974-613">Nustatykite **identifikavimo kodo** lauką į *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="67974-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="67974-614">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-614">Select **OK**.</span></span>
1. <span data-ttu-id="67974-615">**Rūšiuoto inventoriaus paėmimas: Paimti** puslapis rodo būtiną atlikti paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="67974-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="67974-616">Paimkite iš *SORT* vietos ir paskirties LP *PLP02* turės daugelį elementų ir *1* kiekį.</span><span class="sxs-lookup"><span data-stu-id="67974-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="67974-617">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-617">Select **OK**.</span></span>
1. <span data-ttu-id="67974-618">**Rūšiuoto inventoriaus paėmimas: Padėti** puslapis rodo būtiną atlikti padėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="67974-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="67974-619">Padėkite į *Baydoor* vietą ir paskirties LP *PLP02* turės daugelį elementų ir *1* kiekį.</span><span class="sxs-lookup"><span data-stu-id="67974-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="67974-620">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="67974-620">Select **OK**.</span></span>

    <span data-ttu-id="67974-621">Darbas užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="67974-621">Work is completed.</span></span>

<span data-ttu-id="67974-622">Nuo dabar, visi kiti sandėlio procesai yra pritaikyti.</span><span class="sxs-lookup"><span data-stu-id="67974-622">From this point forward, all other warehouse processes apply.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]