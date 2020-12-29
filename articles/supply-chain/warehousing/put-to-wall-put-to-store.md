---
title: Dėjimas prie sienos - dėjimas į parduotuvę
description: Šioje temoje pateikta informacija apie dėjimo prie sienos - dėjimo į parduotuvę funkcijas. Funkcijos leidžia jums tvarkyti scenarijus, kuriuose privalote konsoliduoti produktą į išankstinio pakavimo sritį pagal konfigūruojamus kriterijus. Jis padeda sumažinti pakavimo laiką, nes leidžia paimti vieną paskirties licencijos numerį ir gali naudoti daugiau padėjimo padėčių klasterinio paėmimo metu.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433928"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="fa598-105">Dėjimas prie sienos - dėjimas į parduotuvę</span><span class="sxs-lookup"><span data-stu-id="fa598-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa598-106">*Dėjimo prie sienos - dėjimo į parduotuvę* funkcija eidžia jums tvarkyti scenarijus, kuriuose privalote konsoliduoti produktą į išankstinio pakavimo sritį pagal konfigūruojamus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="fa598-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="fa598-107">Kadangi ši funkcija leidžia paimti vieną paskirties licencijos numerį ir gali naudoti daugiau padėjimo padėčių klasterinio paėmimo metu, bendrovės siunčiančios į parduotuves ar tvarkančios mažus elementus gauna naudos iš sutrumpinto pakavimo laiko.</span><span class="sxs-lookup"><span data-stu-id="fa598-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="fa598-108">Darbo srautas šiai funkcija valdo paimtą produktą į rūšiavimo vietos distribuciją įvairiuose talpyklų tipuose.</span><span class="sxs-lookup"><span data-stu-id="fa598-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="fa598-109">Bendrai, visos rūšiavimo vietos apima daugelį rūšiavimo padėčių.</span><span class="sxs-lookup"><span data-stu-id="fa598-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="fa598-110">Kiekviena rūšiavimo padėtis yra priskirta pagal kriterijus nustatytus verslo procese.</span><span class="sxs-lookup"><span data-stu-id="fa598-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="fa598-111">Dažniausi kriterijai yra galutinė paskirties vieta, siuntimas ar krovimas.</span><span class="sxs-lookup"><span data-stu-id="fa598-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="fa598-112">Po to, kai gaminys atvyksta, jis paskirstoams visoms rūšiavimo vietoms pagal kiekį susietą su užsakymu, paskirties vieta, siuntimo ar kroviniu.</span><span class="sxs-lookup"><span data-stu-id="fa598-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="fa598-113">Kai talpykla yra pilna ar užbaigta, ji patraukiama į stacionarią vietą ar siunčiama į vietą tolesniam tvarkymui, priklausomai nuo verslo proceso.</span><span class="sxs-lookup"><span data-stu-id="fa598-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="fa598-114">Ši sandėlio savybė taip pat rodoma kitais pavadinimais, tokiais kaip dėjimas į šviesą ar tarpo atidarymas.</span><span class="sxs-lookup"><span data-stu-id="fa598-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="fa598-115">Įjunkite Siunčiamo rūšiavimo funkciją</span><span class="sxs-lookup"><span data-stu-id="fa598-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="fa598-116">Prieš jums pradedant naudoti *Dėjimo prie sienos - dėjimo į parduotuvę* funkciją, *Siunčiamo rūšiavimo* savybė jūsų sistemoje turi būti įjungta.</span><span class="sxs-lookup"><span data-stu-id="fa598-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="fa598-117">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="fa598-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="fa598-118">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="fa598-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fa598-119">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="fa598-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="fa598-120">**Funkcijos pavadinimas:** *Siunčiamas rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="fa598-121">*Siunčiamo rūšiavimo* savybė gali būti naudojama kartu su *Plačios bangos žingsnio kodo organizavimo* funkcija, jei ji yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="fa598-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="fa598-122">Privalote taip pat įjungti šią funkciją, jei naudosite iš anksto nustaytus kodus, nurodytus bangos žingsni koduose.</span><span class="sxs-lookup"><span data-stu-id="fa598-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="fa598-123">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="fa598-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="fa598-124">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="fa598-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="fa598-125">**Funkcijos pavadinimas:** *Organizacijos bangos žingsnio kodas*</span><span class="sxs-lookup"><span data-stu-id="fa598-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="fa598-126">Sąranka</span><span class="sxs-lookup"><span data-stu-id="fa598-126">Setup</span></span>

<span data-ttu-id="fa598-127">Šiai demonstracijai, standartiniai „Contoso“ duomenys ir sandėlis *62* yra naudojamas.</span><span class="sxs-lookup"><span data-stu-id="fa598-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="fa598-128">Keletas vėliau išvardytų priedų yra taip pat naudojami.</span><span class="sxs-lookup"><span data-stu-id="fa598-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="fa598-129">Vietos tipas</span><span class="sxs-lookup"><span data-stu-id="fa598-129">Location type</span></span>

1. <span data-ttu-id="fa598-130">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos tipai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="fa598-131">Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte vietos tipo rūšiavimą.</span><span class="sxs-lookup"><span data-stu-id="fa598-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="fa598-132">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="fa598-132">Set the following values:</span></span>

    - <span data-ttu-id="fa598-133">**Vietos tipas:** *RŪŠIUOTI*</span><span class="sxs-lookup"><span data-stu-id="fa598-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="fa598-134">**Aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="fa598-135">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="fa598-136">Sandėlio valdymo parametrai</span><span class="sxs-lookup"><span data-stu-id="fa598-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="fa598-137">Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="fa598-138">**Pagrindiniame** skirtuke **Vietos tipai** „FastTab“ nustatykite **Vietos tipo rūšiavimo** lauklį, įveskite *RŪŠIUOTI*.</span><span class="sxs-lookup"><span data-stu-id="fa598-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="fa598-139">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="fa598-140">Vietos profilis</span><span class="sxs-lookup"><span data-stu-id="fa598-140">Location profile</span></span>

1. <span data-ttu-id="fa598-141">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="fa598-142">Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte profilį rūšiavimo vietai.</span><span class="sxs-lookup"><span data-stu-id="fa598-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="fa598-143">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="fa598-144">**Vietos profilio identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="fa598-145">**Pavadinimas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="fa598-146">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="fa598-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fa598-147">**Vietos formatas:** *PAKUOTĖ*</span><span class="sxs-lookup"><span data-stu-id="fa598-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="fa598-148">**Vietos tipas:** *RŪŠIUOTI*</span><span class="sxs-lookup"><span data-stu-id="fa598-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="fa598-149">**Naudoti licencijos numerio sekimą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="fa598-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="fa598-150">**Leiskite maišytus elementus:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="fa598-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="fa598-151">**Leiskite maišytas inventoriaus būsenas:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="fa598-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="fa598-152">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="fa598-153">Vietos</span><span class="sxs-lookup"><span data-stu-id="fa598-153">Locations</span></span>

1. <span data-ttu-id="fa598-154">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**.</span><span class="sxs-lookup"><span data-stu-id="fa598-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="fa598-155">Išvalykite **Kurti patikrinimo skaičius vietai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="fa598-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="fa598-156">Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="fa598-157">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="fa598-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="fa598-158">**Vieta:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="fa598-159">**Vietos profilio identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="fa598-160">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="fa598-161">Pakavimo šablonai</span><span class="sxs-lookup"><span data-stu-id="fa598-161">Packing profiles</span></span>

1. <span data-ttu-id="fa598-162">Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="fa598-163">Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="fa598-164">**Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="fa598-165">**Aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="fa598-166">**Talpyklos pakavimo politika** Palikite šį laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="fa598-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="fa598-167">**Talpyklos identifikavimo numerio režimas:** *Automatinis*</span><span class="sxs-lookup"><span data-stu-id="fa598-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="fa598-168">**Talpyklos tipas:** *PADĖKLAS 48x48*</span><span class="sxs-lookup"><span data-stu-id="fa598-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="fa598-169">**Automatinis talpyklos sukūrimas jam esant uždarytam:** Palikite šį laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="fa598-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="fa598-170">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="fa598-171">Bangos veiksmo kodai</span><span class="sxs-lookup"><span data-stu-id="fa598-171">Wave step codes</span></span>

<span data-ttu-id="fa598-172">Jei įjungėte *Plačios bangos žingsnio kodo organizavimo* funkciją, nustatykite šiuos kodus.</span><span class="sxs-lookup"><span data-stu-id="fa598-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="fa598-173">Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos žingsnio kodai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="fa598-174">Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="fa598-175">**Bangos žingsnio kodas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="fa598-176">**Bangos žingsnio aprašas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="fa598-177">**Bangos žingsnio tipas:** *Rūšiavimo šablonas*</span><span class="sxs-lookup"><span data-stu-id="fa598-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="fa598-178">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="fa598-179">Siuntimo rūšiavimo šablonas</span><span class="sxs-lookup"><span data-stu-id="fa598-179">Outbound sorting template</span></span>

<span data-ttu-id="fa598-180">Rūšiavimo pavyzdys kontroliuoja, ar rūšiavimo padėtys yra sukurtos, kokie kriterijai yra naudojami ir kitas rūšiavimo proceso savybes.</span><span class="sxs-lookup"><span data-stu-id="fa598-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="fa598-181">Eikite į **Sandėlio valdymas \> Sąranka \> Pakavimas \> Siunčiamo rūšiavimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="fa598-182">Veiksmų juostoje pasirinkite **Naujas** tam, kad rūšiuotumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="fa598-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="fa598-183">Naujojo šablono antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="fa598-184">**Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Bangos rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="fa598-185">**Aprašas:** *Bangos rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="fa598-186">**BRūšiuoti šablono tipą:** *Bangos poreikis*</span><span class="sxs-lookup"><span data-stu-id="fa598-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="fa598-187">Šis laukelis nulemia procesą, kuriam naudojamas rūšiavimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="fa598-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="fa598-188">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="fa598-188">The following values are available:</span></span>

        - <span data-ttu-id="fa598-189">**Bangos poreikis** – Rūšiavimo šablonas naudojamas *Pridėti prie sienos* procesui.</span><span class="sxs-lookup"><span data-stu-id="fa598-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="fa598-190">Šio šablono tipas yra naudojamas pakavimo stočiai apeiti ir apdoroti inventorių tiesiogiai ne bangoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="fa598-191">Galite naudoti šį tipą tik jei **rūšiavimo** bangos proceso metodas yra įtrauktas į bangos šabloną.</span><span class="sxs-lookup"><span data-stu-id="fa598-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="fa598-192">**Talpykla** – Rūšiavimo šablonas yra naudojamas *Padėklo statymui po paėmimo* proceso metu.</span><span class="sxs-lookup"><span data-stu-id="fa598-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="fa598-193">Šis šablono tipas yra naudojamas apdoroti talpyklas, kurios yra uždarytos pakavimo stotyje ir turi būti surūšiuotos ant padėklų.</span><span class="sxs-lookup"><span data-stu-id="fa598-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="fa598-194">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="fa598-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="fa598-195">**Vieta:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="fa598-196">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="fa598-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fa598-197">**Rūšiavimo patvirtinimas:** *Padėties nuskaitymas*</span><span class="sxs-lookup"><span data-stu-id="fa598-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="fa598-198">Šis laukelis nulemia patvirtinimą, kurio reikia rūšiavimo metu.</span><span class="sxs-lookup"><span data-stu-id="fa598-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="fa598-199">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="fa598-199">The following values are available:</span></span>

        - <span data-ttu-id="fa598-200">Jokia</span><span class="sxs-lookup"><span data-stu-id="fa598-200">None</span></span>
        - <span data-ttu-id="fa598-201">Numerio lentelės nuskaitymas</span><span class="sxs-lookup"><span data-stu-id="fa598-201">License plate scan</span></span>
        - <span data-ttu-id="fa598-202">Padėties nuskaitymas</span><span class="sxs-lookup"><span data-stu-id="fa598-202">Position scan</span></span>

    - <span data-ttu-id="fa598-203">**Sukurkite veiksmą vietos uždaryme:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="fa598-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="fa598-204">Jei ši parinktis nustatyta *Taip*, vietos uždarymo metu, veiksmas bus sukuriamas inventoriaus nugabenimui į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="fa598-205">Jei ši parinktis nustatyta *Ne*, inventorius bus nedelsiant paimtas į užsakymą, kai padėtis bus uždaryta.</span><span class="sxs-lookup"><span data-stu-id="fa598-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="fa598-206">**Padėties priskyrimas:** *Rankinis*</span><span class="sxs-lookup"><span data-stu-id="fa598-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="fa598-207">Šis laukelis nulemia priskyrimo padėties tipą.</span><span class="sxs-lookup"><span data-stu-id="fa598-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="fa598-208">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="fa598-208">The following values are available:</span></span>

        - <span data-ttu-id="fa598-209">**Rankinis** – Vartotojas privalo visuomet nurodyti padėtį, kurioje inventorius turi būti rūšiuojamas.</span><span class="sxs-lookup"><span data-stu-id="fa598-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="fa598-210">**Automatinis** – Sistema automatiškai ves inventorių į bet kurią padėtį pagal rūšiavimo šablono tarpus.</span><span class="sxs-lookup"><span data-stu-id="fa598-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="fa598-211">**Priskirti rūšiavimo vietos kriterijus:** *Naudoti tik tuščias padėtis*</span><span class="sxs-lookup"><span data-stu-id="fa598-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="fa598-212">Šis laukelis kontroliuoja, ar jau rūšiavimo padėtyse esantis inventorius yra įtraukiamas, kai padėtis priskiriama poreikiui.</span><span class="sxs-lookup"><span data-stu-id="fa598-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="fa598-213">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="fa598-213">The following values are available:</span></span>

        - <span data-ttu-id="fa598-214">**Naudoti tik tuščią padėtį** – Inventorių jau turinčios ir su juo susietos padėtys bus priimtos domėn</span><span class="sxs-lookup"><span data-stu-id="fa598-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="fa598-215">**Tuščios padėties priėmimas** – Į visą jau padėtyje esantį inventorių priskyrimo metu atsižvelgta nebus.</span><span class="sxs-lookup"><span data-stu-id="fa598-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="fa598-216">Visos naudojamos esamos padėtys.</span><span class="sxs-lookup"><span data-stu-id="fa598-216">All available positions will be used.</span></span>

    - <span data-ttu-id="fa598-217">**Bangos žingsnio kodas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="fa598-218">Jei *Plačios bangos žingsnio kodo organizavimo* funkcija yra įjungta, *Rūšiavimo* bangos žingsnio kodas turi taip pat būti nustatytas bangos žingsnio koduose.</span><span class="sxs-lookup"><span data-stu-id="fa598-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="fa598-219">**Automatinio uždarymo rūšiavimo padėtis:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="fa598-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="fa598-220">Jei ši parinktis nustatyta *Taip*, vietos rūšiavimas bus automatiškai uždaromas, kai visi darbai ateinantys į padėtį bus užbaigti.</span><span class="sxs-lookup"><span data-stu-id="fa598-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="fa598-221">**Rūšiuotų padėčių skaičius:** *3*</span><span class="sxs-lookup"><span data-stu-id="fa598-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="fa598-222">Šis laukelis nulemia didžiausią rūšiuojamų padėčių skaičių, kurį sistema sukurs.</span><span class="sxs-lookup"><span data-stu-id="fa598-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="fa598-223">**Rūšiavimo padėties priešdėlis:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="fa598-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="fa598-224">Šis laukelis nulemia priešdėlį, kurį sistema priskiria prieš padėties numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="fa598-225">**Automatinio pakavimo rūšiavimo padėtis:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="fa598-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="fa598-226">Jei ši parinktis nustatyta *Taip*, inventorius rūšiavimo padėtyje bus supakuotas į talpyklą, kai padėtis bus uždaroma.</span><span class="sxs-lookup"><span data-stu-id="fa598-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="fa598-227">**Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="fa598-228">Šis laukelis nulemia pakavimo profilį, kuris bus naudojamas rūšiuojant padėtį supakuotą į talpyklą.</span><span class="sxs-lookup"><span data-stu-id="fa598-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="fa598-229">Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad nurodytumėte kriterijus naudojamus šiam rūšiavimo šablonui.</span><span class="sxs-lookup"><span data-stu-id="fa598-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="fa598-230">Užklausos teksto laukelyje, **Rūšiavimo** skirtuke, pasirinkite **Naujas** eilutės įtraukimui ir tuomet nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="fa598-231">**Lentelė:** *Krovinio išsami informacija*</span><span class="sxs-lookup"><span data-stu-id="fa598-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="fa598-232">**Išvestinė lentelė:** *Krovinio išsami informacija*</span><span class="sxs-lookup"><span data-stu-id="fa598-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="fa598-233">**Laukas:** *Siuntos ID*</span><span class="sxs-lookup"><span data-stu-id="fa598-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="fa598-234">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="fa598-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="fa598-235">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-235">Select **OK**.</span></span>
1. <span data-ttu-id="fa598-236">Galite gauti šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“</span><span class="sxs-lookup"><span data-stu-id="fa598-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="fa598-237">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fa598-237">Select **Yes**.</span></span>

    <span data-ttu-id="fa598-238">**Siunčiamo rūšiavimo šablono pertrūkio** mygtukas pasirodo veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="fa598-239">Veiksmų juostoje pasirinkite **Siunčiamo rūšiavimo šablono pertrūkiai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="fa598-240">Pasirinkite **Grupavimas laukeliais:** žymimą laukelį tam, kad sugrupuotumėte pagal siuntimo identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="fa598-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="fa598-241">Šis nustatymas sukurs vieną padėtį siuntimui, kuris yra talpykla bangoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="fa598-242">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="fa598-243">Bangos apdorojimo metodai</span><span class="sxs-lookup"><span data-stu-id="fa598-243">Wave process methods</span></span>

1. <span data-ttu-id="fa598-244">Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="fa598-245">Veiksmų srityje spustelėkite **Pakartotinai generuoti metodus**.</span><span class="sxs-lookup"><span data-stu-id="fa598-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="fa598-246">**Rūšiavimo** metodas yra įtraukiamas į esamų metodų sąrašą, o *Siuntimo* bangos šablono tipas jam yra pasirenkamas.</span><span class="sxs-lookup"><span data-stu-id="fa598-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="fa598-247">Bangos šablonai</span><span class="sxs-lookup"><span data-stu-id="fa598-247">Wave templates</span></span>

<span data-ttu-id="fa598-248">Redaguokite bangos šabloną, naudojamą bangos poreikio rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="fa598-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="fa598-249">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="fa598-250">**Bangos šablono itpo** laukelyje, pasirinkite *Siuntimas*.</span><span class="sxs-lookup"><span data-stu-id="fa598-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="fa598-251">Pasirinkite esantį **62 siuntimo nustatytąjį** šabloną.</span><span class="sxs-lookup"><span data-stu-id="fa598-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="fa598-252">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fa598-253">**Bendri** „FastTab“, atlikite šiuos pakeitimus:</span><span class="sxs-lookup"><span data-stu-id="fa598-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="fa598-254">Parinktį **Apdoroti bangą išleidžiant ją į sandėlį** nustatykite į *Ne*.</span><span class="sxs-lookup"><span data-stu-id="fa598-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="fa598-255">Nustatykite **Priskirti atviroms bangoms** parinktį į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="fa598-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="fa598-256">**Metodai** „FastTab“, nustatykite **rūšiavimo** metodą:</span><span class="sxs-lookup"><span data-stu-id="fa598-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="fa598-257">**Likę metodai** tinklelyje, pasirinkite **rūšiavimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="fa598-258">Pasirinkite dešinės rodyklės mygtuką **rūšiavimas** perkėlimui į **Pasirinkti metodai** tinklelį.</span><span class="sxs-lookup"><span data-stu-id="fa598-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="fa598-259">**Pasirnkti metodai** tinklelyje, pasirinkite **rūšiavimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="fa598-260">Nustatykite **Bangos žingsnio kodo** laukelį į *Rūšiuoti*.</span><span class="sxs-lookup"><span data-stu-id="fa598-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="fa598-261">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="fa598-262">Mobiliojo įrenginio meniu elementai</span><span class="sxs-lookup"><span data-stu-id="fa598-262">Mobile device menu items</span></span>

1. <span data-ttu-id="fa598-263">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="fa598-264">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="fa598-265">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="fa598-266">**Meniu elemento pavadinimas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="fa598-267">**Pavadinimas:** *Rūšiuoti*</span><span class="sxs-lookup"><span data-stu-id="fa598-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="fa598-268">**Režimas:** *Netiesioginis*</span><span class="sxs-lookup"><span data-stu-id="fa598-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="fa598-269">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="fa598-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="fa598-270">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="fa598-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fa598-271">**Veiksmo kodas:** *Siunčiamas rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="fa598-272">**Naudoti proceso gidą:** *Taip* (nustatytoji vertė)</span><span class="sxs-lookup"><span data-stu-id="fa598-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="fa598-273">**Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Bangos rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="fa598-274">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="fa598-275">Mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="fa598-275">Mobile device menu</span></span>

1. <span data-ttu-id="fa598-276">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="fa598-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="fa598-277">Meniu sąraše pasirinkite **Siuntimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="fa598-278">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fa598-279">**Esančiuose meniu ir meniu elementų** tinklelyje suraskite ir pasirinkite **Rūšiavimo** meniu elementą, kurį kątik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="fa598-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="fa598-280">Pasirinkite dešinės rodyklės mygtuką **Rūšiavimas** perkėlimui į **Meniu struktūros** tinklelį.</span><span class="sxs-lookup"><span data-stu-id="fa598-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="fa598-281">Šiuo būdu, galėsite įtraukite naują meniu elementą **Siuntimai** meniu.</span><span class="sxs-lookup"><span data-stu-id="fa598-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="fa598-282">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="fa598-283">Vietos nurodymai</span><span class="sxs-lookup"><span data-stu-id="fa598-283">Location directives</span></span>

<span data-ttu-id="fa598-284">Privalote sukurti vietos direktyvas, kurios vestų sukurtą darbą po to, kai rūšiavimas yra užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="fa598-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="fa598-285">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="fa598-286">**Darbo tvarkos tipo** laukelyje pasirinkite *Rūšiuoto inventoriaus paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="fa598-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="fa598-287">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="fa598-288">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="fa598-289">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="fa598-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="fa598-290">**Pavadinimas:** *Dėti į „Baydoor“*</span><span class="sxs-lookup"><span data-stu-id="fa598-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="fa598-291">**Padėties direktyvos** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fa598-292">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="fa598-293">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="fa598-293">**Site:** *6*</span></span>
    - <span data-ttu-id="fa598-294">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="fa598-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="fa598-295">**Nurodymo kodas:** Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="fa598-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="fa598-296">**Keletas SKU:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="fa598-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="fa598-297">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="fa598-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="fa598-298">**Linijų** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes.</span><span class="sxs-lookup"><span data-stu-id="fa598-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="fa598-299">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="fa598-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="fa598-300">**SEekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="fa598-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="fa598-301">**Pradinis kiekis:** *0*</span><span class="sxs-lookup"><span data-stu-id="fa598-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="fa598-302">**Galutinis kiekis:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="fa598-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="fa598-303">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="fa598-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="fa598-304">**Vietos direktyvos veiksmai** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="fa598-305">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="fa598-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="fa598-306">**SEekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="fa598-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="fa598-307">**Pavadinimas:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="fa598-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="fa598-308">Pasirinkite **Įrašyti** tam, kad atliktumėte **Siūlymo redagavimo** mygtuką **Vietos direktyvos veiksmai** „FastTab“ prieinamą.</span><span class="sxs-lookup"><span data-stu-id="fa598-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="fa598-309">„FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="fa598-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="fa598-310">Užklausos teksto laukelyje, **Intervalas** skirtuke, suraskite eilutę, kurioje **Laukelis** laukelis yra nustatytas į *Vieta*.</span><span class="sxs-lookup"><span data-stu-id="fa598-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="fa598-311">Nustatykite **Kriterijų** laukelį šiai eilutei į *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="fa598-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="fa598-312">Pasirinkite **OK** redagavimo patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="fa598-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="fa598-313">Darbo klasės</span><span class="sxs-lookup"><span data-stu-id="fa598-313">Work classes</span></span>

1. <span data-ttu-id="fa598-314">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="fa598-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="fa598-315">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="fa598-316">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="fa598-317">**Darbo klasės identifikavimo numeris:** *Rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="fa598-318">**Aprašas:** *Rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="fa598-319">**Darbo tvarkos tipas:** *Rūšiuoto inventoriaus paėmimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="fa598-320">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="fa598-321">Darbo šablonai</span><span class="sxs-lookup"><span data-stu-id="fa598-321">Work templates</span></span>

1. <span data-ttu-id="fa598-322">Eikite į **Sandėlio valdymas \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="fa598-323">Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="fa598-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="fa598-324">Tinklelyje, pasirinkite **62 pasirinkite pakuoti** darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="fa598-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="fa598-325">Veiksmų juostoje pasirinkite **Darbo antraštės tarpai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="fa598-326">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fa598-327">Linijoje, kurioje **Laukelio pavadinimas** laukelė nustatykite *Siuntimo identifikavimo kodas*, ištrinkite **Grupuoti pagal šį laukelį** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="fa598-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="fa598-328">Pasirinkite **Įrašyti** ir tuomet uždarykite **Darbo antraštės tarpai** teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="fa598-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="fa598-329">**Darbo tvarkos tipo** laukelyje pasirinkite *Rūšiuoto inventoriaus paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="fa598-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="fa598-330">Pasirinkite **Naujas** tam, kad sukurtumėte darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="fa598-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="fa598-331">**Peržiūros** skyriuje, nustatykite šias vertes.</span><span class="sxs-lookup"><span data-stu-id="fa598-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="fa598-332">Priimkite nustatytąsias vertes visiems kitiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="fa598-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="fa598-333">**Darbo šablonas:** *Rūšiuotas paėmimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="fa598-334">**Darbo šablono aprašas:** *Rūšiuotas paėmimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="fa598-335">Pasirinkite **Įrašyti** tam, kad padarytumėte **Darbo šablono informacijos** skyrių prieinamą.</span><span class="sxs-lookup"><span data-stu-id="fa598-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="fa598-336">**Darbo šablono informacijos** skyriuje sukursti dvi eilutes.</span><span class="sxs-lookup"><span data-stu-id="fa598-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="fa598-337">Pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes eilutei 1:</span><span class="sxs-lookup"><span data-stu-id="fa598-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="fa598-338">**Darbo tipas:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="fa598-339">**Privaloma:** Pasirinkite (= *Taip*)</span><span class="sxs-lookup"><span data-stu-id="fa598-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="fa598-340">**Darbo klasės identifikavimo numeris:** *Rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="fa598-341">Pasirinkite **Naujas** dar kartą ir tuomet nustatykite tolesnes vertes eilutei 2:</span><span class="sxs-lookup"><span data-stu-id="fa598-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="fa598-342">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="fa598-343">**Privaloma:** Pasirinkite (= *Taip*)</span><span class="sxs-lookup"><span data-stu-id="fa598-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="fa598-344">**Darbo klasės identifikavimo numeris:** *Rūšiavimas*</span><span class="sxs-lookup"><span data-stu-id="fa598-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="fa598-345">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="fa598-346">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="fa598-346">Example scenario</span></span>

<span data-ttu-id="fa598-347">Šis scenarijus simuliuoja situaciją, kuomet sandėlis talpina mažus objektus vietose ir turi pakuoti juos į dėžės prieš siuntimą bei kai pakavimo stoties veikimas nėra labai tinkamas.</span><span class="sxs-lookup"><span data-stu-id="fa598-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="fa598-348">Darbuotojai paima užsakymus daugeliui klientų ir skirtingais adresais tuo pačiu metu taip padidindami paėmimo greitį.</span><span class="sxs-lookup"><span data-stu-id="fa598-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="fa598-349">Po paėmimo, darbuotojais atvyksta į rūšiavimo vietą, kurioje paimti objektai gali būti surūšiuoti į tinkamas dėžės pagal būtinus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="fa598-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="fa598-350">Šiame pavyzdyje siuntimo identifikavimo kodas bus naudojamas nulemti tinkamą dėžę, nes visi siuntimai turi skirtingus adresus.</span><span class="sxs-lookup"><span data-stu-id="fa598-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="fa598-351">Po to, kai visi objektai iš krovimo yra supakuoti ir rūšiuoti pagal siuntimus, dėžės bus patraukiamos į paruošimo vietą ir vėliau pakraunamo į sunkvežimį.</span><span class="sxs-lookup"><span data-stu-id="fa598-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="fa598-352">Prieš šio scenarijaus pradžią, įsitikinkite, kad visos standartinės sandėlio funkcijos jūsų sandėlyje yra nustatytos tinkamai.</span><span class="sxs-lookup"><span data-stu-id="fa598-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="fa598-353">Standartinis „Contoso“ sandėlis *62* yra naudojamas šiuo tikslu.</span><span class="sxs-lookup"><span data-stu-id="fa598-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="fa598-354">Standartinės konfigūracijos nebuvo pakeistos, taip pat nepakeista informacija nustatymuose.</span><span class="sxs-lookup"><span data-stu-id="fa598-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="fa598-355">Kurti paklausą</span><span class="sxs-lookup"><span data-stu-id="fa598-355">Create demand</span></span>

<span data-ttu-id="fa598-356">Prieš funkcijų rodymą, privalote sukurti šiek tiek poreikio.</span><span class="sxs-lookup"><span data-stu-id="fa598-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="fa598-357">Šiame scenarijui, sukursti tris prekybos užsakymus trims skirtingiems klientams tam, kad simuliuotumėte skirtingus pristatymo adresus,</span><span class="sxs-lookup"><span data-stu-id="fa598-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="fa598-358">Tokiu būdu, sukursite tris skirtingus siuntimus.</span><span class="sxs-lookup"><span data-stu-id="fa598-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="fa598-359">Prieš sukuriant prekybos užsakymus ir siuntimus, įsitikinkite, kad paėmimo vietos turi pakankamai inventoriaus visiems objektams užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="fa598-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="fa598-360">Peržiūrėkite vietos direktyvos nustatymus, kad patvirtintumėte paėmimo vietas naudojamas prekybos užsakymo paėmime.</span><span class="sxs-lookup"><span data-stu-id="fa598-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="fa598-361">Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba bet kokį kitą srautą.</span><span class="sxs-lookup"><span data-stu-id="fa598-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="fa598-362">Tuomet rezervuokite inventorių.</span><span class="sxs-lookup"><span data-stu-id="fa598-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="fa598-363">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="fa598-364">Pasirinkite **Naujas** prekybos užsakymo sukūrimui užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="fa598-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="fa598-365">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="fa598-366">**Klientas:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="fa598-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="fa598-367">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="fa598-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="fa598-368">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-368">Select **OK**.</span></span>
1. <span data-ttu-id="fa598-369">Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="fa598-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="fa598-370">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="fa598-370">Set the following values:</span></span>

    - <span data-ttu-id="fa598-371">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="fa598-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="fa598-372">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="fa598-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="fa598-373">Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="fa598-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="fa598-374">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="fa598-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="fa598-375">**Kiekis:** *10*</span><span class="sxs-lookup"><span data-stu-id="fa598-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="fa598-376">Pakartokite tolesnius žingsnius kiekvienai prekybos eilutei užsakyme tam, kad rezervuotumėte jam inventorių:</span><span class="sxs-lookup"><span data-stu-id="fa598-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="fa598-377">„FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="fa598-378">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fa598-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="fa598-379">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-379">Select **Save**.</span></span>

1. <span data-ttu-id="fa598-380">Pasirinkite **Naujas** prekybos užsakymo sukūrimui užsakymui 2.</span><span class="sxs-lookup"><span data-stu-id="fa598-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="fa598-381">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="fa598-382">**Klientas:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="fa598-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="fa598-383">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="fa598-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="fa598-384">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-384">Select **OK**.</span></span>
1. <span data-ttu-id="fa598-385">Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="fa598-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="fa598-386">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="fa598-386">Set the following values:</span></span>

    - <span data-ttu-id="fa598-387">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="fa598-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="fa598-388">**Kiekis:** *7*</span><span class="sxs-lookup"><span data-stu-id="fa598-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="fa598-389">Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="fa598-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="fa598-390">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="fa598-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="fa598-391">**Kiekis:** *3*</span><span class="sxs-lookup"><span data-stu-id="fa598-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="fa598-392">Pakartokite tolesnius žingsnius kiekvienai prekybos eilutei užsakyme tam, kad rezervuotumėte jam inventorių:</span><span class="sxs-lookup"><span data-stu-id="fa598-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="fa598-393">„FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="fa598-394">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fa598-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="fa598-395">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-395">Select **Save**.</span></span>

1. <span data-ttu-id="fa598-396">Pasirinkite **Naujas** prekybos užsakymo sukūrimui užsakymui 3.</span><span class="sxs-lookup"><span data-stu-id="fa598-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="fa598-397">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="fa598-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="fa598-398">**Klientas:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="fa598-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="fa598-399">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="fa598-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="fa598-400">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-400">Select **OK**.</span></span>
1. <span data-ttu-id="fa598-401">Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="fa598-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="fa598-402">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="fa598-402">Set the following values:</span></span>

    - <span data-ttu-id="fa598-403">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="fa598-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="fa598-404">**Kiekis:** *8*</span><span class="sxs-lookup"><span data-stu-id="fa598-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="fa598-405">Pakartokite šiuos žingsnius tam, kad rezervuotumėte inventorių prekybos eilutei:</span><span class="sxs-lookup"><span data-stu-id="fa598-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="fa598-406">„FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="fa598-407">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fa598-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="fa598-408">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-408">Select **Save**.</span></span>

<span data-ttu-id="fa598-409">Pabaikite tolesnias procedūras tam, kad paleistumėte visus prekybos užsakymus sandėliui.</span><span class="sxs-lookup"><span data-stu-id="fa598-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="fa598-410">Bus sukurti trys skirtingi siuntimai.</span><span class="sxs-lookup"><span data-stu-id="fa598-410">Three different shipments will be created.</span></span> <span data-ttu-id="fa598-411">Tuomet galėsite įtraukti tris skirtingus siuntimus vienai bangai.</span><span class="sxs-lookup"><span data-stu-id="fa598-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="fa598-412">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="fa598-413">Tinklelyje pasirinkite pirmą savo sukurtą prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="fa598-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="fa598-414">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="fa598-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="fa598-415">Gausite informacinį pranešimą, kuris rodys sukurtą bangos identifikavimo kodą ir siuntimo identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="fa598-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="fa598-416">Pakartokite ankstesnius žingsnius prekybos užsakymų 2 ir 3 išleidimui į sandelį.</span><span class="sxs-lookup"><span data-stu-id="fa598-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="fa598-417">Atkreipkite dėmesį, kad jūsų gautas informacinis pranešimas nurodo, kad siuntimas buvo įtrauktas į bangą sukurtą jūsų išleistam prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="fa598-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="fa598-418">Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.</span><span class="sxs-lookup"><span data-stu-id="fa598-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="fa598-419">Pasirinkite bangos identifikavimo kodą, kuris buvo sukurtas iš prekybos užsakymui tam, kad atidarytumėte **Bangų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="fa598-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="fa598-420">Puslapis rodo bangos informaciją.</span><span class="sxs-lookup"><span data-stu-id="fa598-420">This page shows the wave details.</span></span> <span data-ttu-id="fa598-421">**Bangos eilučių**„FastTab“ rodo sukurtus siuntimus.</span><span class="sxs-lookup"><span data-stu-id="fa598-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="fa598-422">Privalote dabar sukurti darbą objektų nusiuntimui į paėmimo vietas rūšiavimo vietoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="fa598-423">Veiksmų juostoje pasirinkite **Apdoroti**.</span><span class="sxs-lookup"><span data-stu-id="fa598-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="fa598-424">Bangos apdorojimo metu, rūšiavimo metodas naudos rūšiavimo šabloną priskirdamas inventorių rūšiavimo padėtims.</span><span class="sxs-lookup"><span data-stu-id="fa598-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="fa598-425">Kai banga yra apdorota, gausite informacinį pranešimą sakantį, kad banga buvo publikuota ir darbas buvo sukurtas.</span><span class="sxs-lookup"><span data-stu-id="fa598-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="fa598-426">Veiksmų juostoje, **Bangos** skirtuke, **Susijusios informacijos** grupėje, pasirinkite **Darbas** tam, kad peržiūrėtumėte šiai bangą sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="fa598-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="fa598-427">Pasižymėkite darbo ID.</span><span class="sxs-lookup"><span data-stu-id="fa598-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="fa598-428">Eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į konteinerius \> Siunčiamo rūšiavimo padėties priskyrimai**.</span><span class="sxs-lookup"><span data-stu-id="fa598-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="fa598-429">Kairiame stulpelyje galite peržiūrėti siunčiamą rūšiavimo padėtį sukurtą visiems siuntimams.</span><span class="sxs-lookup"><span data-stu-id="fa598-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="fa598-430">**Rūšiavimo padėties kriterijų** „FastTab“, galite peržiūrėti siuntimo identifikavimo kodą tai padėčiai.</span><span class="sxs-lookup"><span data-stu-id="fa598-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="fa598-431">Buvo sukurtas vienas darbo identifikavimo kodas tam, kad nusiųstų inventorių iš paėmimo vietų į rūšiavimo vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="fa598-432">Darbo užbaigimui jums reikės darbo identifikavimo kodo, kuris buvo sukurtas bangos apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="fa598-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="fa598-433">Prekybos užsakymo paėmimas rūšiavimo vietai</span><span class="sxs-lookup"><span data-stu-id="fa598-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="fa598-434">Prisijunkite prie mobilios programos kaip darbuotojas sandėlyje *62*.</span><span class="sxs-lookup"><span data-stu-id="fa598-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="fa598-435">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="fa598-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="fa598-436">**Siunčiama** meniu pasirinkite **Prekybos paėmimas**.</span><span class="sxs-lookup"><span data-stu-id="fa598-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="fa598-437">Pasirinkite **identifikavimo kodo** laukelį ir tuomet įveskite darbo identifikavimo kodą iš bangos apdorojimo.</span><span class="sxs-lookup"><span data-stu-id="fa598-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="fa598-438">Patvirtinkite savo įrašą.</span><span class="sxs-lookup"><span data-stu-id="fa598-438">Confirm your entry.</span></span>

    <span data-ttu-id="fa598-439">Po to, būsite paskatinti įvesti galutinį licencijos numerį (LP).</span><span class="sxs-lookup"><span data-stu-id="fa598-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="fa598-440">Atkreipkite dėmesį, kad eilutė 1 iš prekybos užsakymo 1, kuris turi būti paimtas ir įtrauktas į galutinį licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="fa598-441">Rodomas objekto numeris, kiekis, aprašas ir paėmimo vieta.</span><span class="sxs-lookup"><span data-stu-id="fa598-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="fa598-442">**Galutinio LP** laukelyje įveskite licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="fa598-443">Paimsite visas eilutes, kurios buvo sukurtos bangos apdorojimo metu į tą patį galutinį licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="fa598-444">Patvirtinkite savo įrašą.</span><span class="sxs-lookup"><span data-stu-id="fa598-444">Confirm your entry.</span></span>

    <span data-ttu-id="fa598-445">Mobili programa dabar rodo **Paėmimo** puslapio serijas, kurios rodo jums paėmimo vietas ir objektą bei būtiną paimti kiekį.</span><span class="sxs-lookup"><span data-stu-id="fa598-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="fa598-446">Po to, kai objektas yra įtrauktas į licencijos numerį, patvirtinsite paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="fa598-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="fa598-447">Paskutinis puslapis bus darbas, kuris paėmė objektus į rūšiavimo vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="fa598-448">Patvirtinkite pirmą paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="fa598-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="fa598-449">Rodomas kitas paėmimo darbas.</span><span class="sxs-lookup"><span data-stu-id="fa598-449">The next pick work is shown.</span></span> <span data-ttu-id="fa598-450">Patvirtinkite paėmimą.</span><span class="sxs-lookup"><span data-stu-id="fa598-450">Confirm the pick.</span></span>
1. <span data-ttu-id="fa598-451">Tęskite tvirtindami likusį paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="fa598-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="fa598-452">Paskutinis žingsnis yra pabaigti padėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="fa598-452">The last step is to complete the put work.</span></span> <span data-ttu-id="fa598-453">Patvirtinkite padėjimą šalin į rūšiavimo vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="fa598-454">Matysite „Darbas baigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="fa598-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="fa598-455">Išeikite iš **Prekybos paėmimo** mobilioje programoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="fa598-456">Rūšiavimas/dėjimas prie sienos</span><span class="sxs-lookup"><span data-stu-id="fa598-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="fa598-457">Dabar, kai visas inventorius buvo įdėtas į rūšiavimo vietą, jis turi būti surūšiuotas į teisingą rūšiavimo vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="fa598-458">Prisijungimas prie mobilios programos.</span><span class="sxs-lookup"><span data-stu-id="fa598-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="fa598-459">Pagrindiniame meniu pasirinkite **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="fa598-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="fa598-460">**Siuntimo** meniu pasirinkite **Rūšiuoti** objektų rūšiavimo pradžiai.</span><span class="sxs-lookup"><span data-stu-id="fa598-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="fa598-461">**LP/CON** laukelyje įveskite paimto prekybos užsakymo darbo paskirties licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="fa598-462">Patvirtinkite savo įrašą.</span><span class="sxs-lookup"><span data-stu-id="fa598-462">Confirm your entry.</span></span>
1. <span data-ttu-id="fa598-463">Įveskite objekto numerį, kurį reikia rūšiuoti pirma.</span><span class="sxs-lookup"><span data-stu-id="fa598-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="fa598-464">Sistema nusprendža, jurią rūšiavimo vietą reikia rodyti pirmiausiai.</span><span class="sxs-lookup"><span data-stu-id="fa598-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="fa598-465">Patvirtinkite rūšiavimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="fa598-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="fa598-466">Būsite paskatinti priskirti licencijos numerį rūšiavimo vietai.</span><span class="sxs-lookup"><span data-stu-id="fa598-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="fa598-467">Pasirinkite **LP** laukelį ir įveskite licencijos numerį ir tuomet patvirtinkite savo įrašą.</span><span class="sxs-lookup"><span data-stu-id="fa598-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="fa598-468">Kadangi rūšiavimo padėtis yra susieta su siuntimo identifikavimo kodu, jūs rūšiuosite paimtus objektus į licencijos numerį, nurodytą siunčiamame siuntime ir prekybos užsakyme.</span><span class="sxs-lookup"><span data-stu-id="fa598-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="fa598-469">Kitas puslapis rodo objekto identifikavimo numerį, kokybę, rūšiavimo padėties identifikavimo numerį ir iš kur (paėmimas) į kur (rūšiavimas) licencijos numerio identifikavimo kodus.</span><span class="sxs-lookup"><span data-stu-id="fa598-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="fa598-470">Informacija šiame puslapyje aiškina jums, kaip rūšiuoti konkrečius objektus ir kiekius iš paėmimo licencijos numerio į rūšiavimo licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="fa598-471">Patvirtinkite rūšiavimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="fa598-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="fa598-472">Rūšiuokite objektus į pirmą rūšiavimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="fa598-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="fa598-473">Kai pabaigėte, sistema nukreips jus į kitą rūšiavimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="fa598-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="fa598-474">Pakartokite šią procedūrą visoms paimtoms eilutėms darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="fa598-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="fa598-475">Taip pat turėtumėte naudoti šį procesą, kai esama kelių paėmimo eilučių, kurios turi tą patį objekto numerį.</span><span class="sxs-lookup"><span data-stu-id="fa598-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="fa598-476">Kartojant šį procesą su visais objektais, sistema vertina kriterijus iš nuskaityto kito objekto (darbo linijos) ir nusprendžia, kuris rūšiavimo padėtis turi būti padėta.</span><span class="sxs-lookup"><span data-stu-id="fa598-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="fa598-477">Jūs automatiškai nukreipiami tam, kad padėtumėte objektą į tinkamą rūšiavimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="fa598-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="fa598-478">Priklausomai nuo patvirtinimo nustatymų, esate nukreiptas patvirtinti šį veiksmą įvedant padėties numerį ar licencijos numerio identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="fa598-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa598-479">Jei įjungtas automatinis rūšiavimas, rankinis pakeitimas nėra galimas.</span><span class="sxs-lookup"><span data-stu-id="fa598-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="fa598-480">Kai baigėte, „Microsoft Dynamics 365 Supply Chain Management“, atidarykite **Siuntimo rūšiavimo padėties priskyrimo** puslapį, kad peržiūrėtumėte padėčių būseną.</span><span class="sxs-lookup"><span data-stu-id="fa598-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="fa598-481">Jei padėtys yra uždaromos automatiškai, pasirinkite **Rodyti uždarytas** tam, kad rodytumėte uždarytas padėtis.</span><span class="sxs-lookup"><span data-stu-id="fa598-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="fa598-482">Atkreipkite dėmesį, kad yra rodomi rūšiavimo padėties pervedimai.</span><span class="sxs-lookup"><span data-stu-id="fa598-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="fa598-483">Apdorotas objektas ir kiekis yra apdorojami per rodomas padėtis.</span><span class="sxs-lookup"><span data-stu-id="fa598-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="fa598-484">Kai nustatote siunčiamo rūšiavimo šabloną, nustatote **Automatinio uždarymo rūšiavimo padėties** parinktį į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="fa598-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="fa598-485">Dėl to, padėtis yra automatiškai uždaroma po to, kai paskutinis tikėtinas intventorius yra patalpintas.</span><span class="sxs-lookup"><span data-stu-id="fa598-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="fa598-486">Rūšiavimo padėtyes yra **Uždarytos** būsenoje ir darbas buvo sukurtas tam, kad perkeltų rūšiuotą inventorių į *Baydoor* vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="fa598-487">Pabaikite rūšiuoto inventoriaus paėmimo darbą tam, kad perkeltumėte inventorių į siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="fa598-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="fa598-488">Kai inventorius yra paruoštas, patvirtinkite jo siuntimą.</span><span class="sxs-lookup"><span data-stu-id="fa598-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="fa598-489">Rūšiuoto inventoriaus paėmimo darbo tinkamam apdorojimui, mobilaus prietaiso meniu objektas turi darbo klasės identifikavimo kodą, kuriame **Darbo tvarkos tipo** laukelis yra nustatytas *Rūšiuoto inventoriaus paėmimas* ir turi būti naudojamas judėjimo ir krovimo procedūroms.</span><span class="sxs-lookup"><span data-stu-id="fa598-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="fa598-490">Rankiniu būdu uždarykite padėtį (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="fa598-490">Manually close a position (optional)</span></span>

<span data-ttu-id="fa598-491">Jei rūšiavimo padėtys turi būti uždarytos rankiniu būdu, **Automatinio uždarymo rūšiavimo padėties** parinktis siunčiamo rūšiavimo šablonui turi būti nustatyta į *Ne* ir uždarymas turi būti atliktas prieš inventoriaus judėjimą į „bay door“ sritį.</span><span class="sxs-lookup"><span data-stu-id="fa598-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="fa598-492">Padėtys gali būti uždaromos įvariais būdais:</span><span class="sxs-lookup"><span data-stu-id="fa598-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="fa598-493">Per sandėlio programą:</span><span class="sxs-lookup"><span data-stu-id="fa598-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="fa598-494">Vartotojai gali nuskaityti vieną iš objektų, kurie jau yra padėtyje ir tuomet pasirinkti **Uždaryti** padėties uždarymui.</span><span class="sxs-lookup"><span data-stu-id="fa598-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="fa598-495">Jei vartotojas nuskaito talpyklą, kuri jau buvo rūšiuota talpykloje, rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="fa598-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="fa598-496">Nepaisant to, vartotojas gali ir toliau tęsti padėties uždarymą.</span><span class="sxs-lookup"><span data-stu-id="fa598-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="fa598-497">„Microsoft Dynamics 365 Supply Chain Management“ **Siunčiamo rūšiavimo padėties priskyrimuose** puslapyje:</span><span class="sxs-lookup"><span data-stu-id="fa598-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="fa598-498">Vartotojai gali pasirinkti siunčiamo rūšiavimo padėties įrašą ir tuomet pasirinkti **Uždaryti padėtį** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="fa598-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="fa598-499">Patarimai</span><span class="sxs-lookup"><span data-stu-id="fa598-499">Tips</span></span>

- <span data-ttu-id="fa598-500">Objektus galima judinti tarp padėčių po to, kai jie buvo vienai priskirti.</span><span class="sxs-lookup"><span data-stu-id="fa598-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="fa598-501">Sistema įvertina, kiek kiekvieno objekto vienetų turėtų eiti į konkrečią padėtį.</span><span class="sxs-lookup"><span data-stu-id="fa598-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="fa598-502">Rūšiavimo šablonas gali būti kofigūruojamas automatiškai sukurti talpyklas, kai padėtys yra uždarytos.</span><span class="sxs-lookup"><span data-stu-id="fa598-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="fa598-503">Šis požiūris sukurs standartinės talpyklos identifikavimo kodo strukūtrą, kuri paremta konkrečiu pakavim profiliu.</span><span class="sxs-lookup"><span data-stu-id="fa598-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa598-504">Po to, kai judėjimo darbas yra sukurti pagal rūšiavimo vietą, privalote neatšaukti darbo.</span><span class="sxs-lookup"><span data-stu-id="fa598-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="fa598-505">Kitu atveju, pozicija ir talpyklos jame bus pašalintos iš sistemos ir neprieinamos tolesniam apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="fa598-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="fa598-506">Inventorius taip pat bus pašalintas.</span><span class="sxs-lookup"><span data-stu-id="fa598-506">The inventory will also be removed.</span></span>
