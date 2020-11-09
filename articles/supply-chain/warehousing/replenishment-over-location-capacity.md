---
title: Papildymas pagal vietos erdvę
description: Šioje temoje pateikiama informacija apie vietos pajėgumo papildymo funkciją. Ši funkcija įjungia visus papildymo darbus, kurių bus reikalaujama kūrimo dieną ir valdo papildymo darbo prieinamumą siekiant užtikrinti, kad paėmimo vieta neišeis iš atsargų ir neviršys pajėgumo.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016613"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="ef20d-104">Papildymas pagal vietos erdvę</span><span class="sxs-lookup"><span data-stu-id="ef20d-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef20d-105">Kai kurie didelės apimties ar erdvėje apriboti sandėliai privalo išsiųsti daugiau elemento kiekio per dieną nei telpa paėmimo vietoje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="ef20d-106">*Vietos pajėgumo papildymo* funkcija įjungia visus papildymo darbus, kurių bus reikalaujama kūrimo dieną ir valdo papildymo darbo prieinamumą siekiant užtikrinti, kad paėmimo vieta neišeis iš atsargų ir neviršys pajėgumo.</span><span class="sxs-lookup"><span data-stu-id="ef20d-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="ef20d-107">Ši funkcija įjungia daugiau papildymo darbo, kuris bus sukuriamas nei telpa vietoje ir užblokuoja papildymo darbą nuo jo pabaigos, kai vieta yra pilna.</span><span class="sxs-lookup"><span data-stu-id="ef20d-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="ef20d-108">Kadangi atsargos paėmimo vietoje nukrenta žemiau konfigūruojamo slenksčio, didesnis papildymo darbas yra prieinamas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="ef20d-109">Įjungti vietos pajėgumo papildymo darbo funkciją</span><span class="sxs-lookup"><span data-stu-id="ef20d-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="ef20d-110">Tam, kad šioje temoje aprašyta funkcija būtų prieinama jūsų sistemoje, įjunkite tolesnes funkcijas [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)(tokia tvarka):</span><span class="sxs-lookup"><span data-stu-id="ef20d-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="ef20d-111">Darbo blokavimas organizacijos mastu</span><span class="sxs-lookup"><span data-stu-id="ef20d-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="ef20d-112">Papildymas pagal vietos erdvę</span><span class="sxs-lookup"><span data-stu-id="ef20d-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="ef20d-113">Nustatykite funkciją pavyzdiniam scenarijui</span><span class="sxs-lookup"><span data-stu-id="ef20d-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="ef20d-114">Šis skyrius aprašo gaires ir pavyzdį, kuris rodo, kaip nustatyti šią funkciją ir paruošti pavyzdinius duomenis pavyzdiniam scenarijui, kuris pateiktas vėliau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="ef20d-115">Duomenų pavyzdžių įgalinimas</span><span class="sxs-lookup"><span data-stu-id="ef20d-115">Enable sample data</span></span>

<span data-ttu-id="ef20d-116">Tam, kad dirbtumėte su [pavyzdiniu scenarijumi](#example-scenario) naudodami pavyzdinius įrašus ir vertes nurodytas čia, turite būti sistemoje, kurioje standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yra įdiegti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ef20d-117">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="ef20d-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="ef20d-118">Vietos profilis</span><span class="sxs-lookup"><span data-stu-id="ef20d-118">Location profile</span></span>

<span data-ttu-id="ef20d-119">Įjungti vietos pajėgumo papildymo funkciją vietos profilyje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="ef20d-120">Eikite į **Sandėlio valdymą \> Nustatymai \> Sandėlis \> Vietos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="ef20d-121">Kairėje juostoje, pasirinkite **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="ef20d-122">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef20d-123">Skirtuke **Papildymas** „FastTab“, nustatykite tolesnes reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ef20d-124">**Viršytas vietos pajėgumas:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ef20d-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="ef20d-125">Įjungus papildymo darbui leidžiama viršyti maksimalius vietos pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="ef20d-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="ef20d-126">Tai taip pat įjungia kitus laukelius **Papildymo** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="ef20d-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="ef20d-127">**Darbo prieinamumo slenksčio tipas:** *Kiekis*</span><span class="sxs-lookup"><span data-stu-id="ef20d-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="ef20d-128">Šis laukelis nustato metodą, kuris naudojamas nustatyti, kai daugiau darbo turi būti paleidžiama.</span><span class="sxs-lookup"><span data-stu-id="ef20d-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="ef20d-129">Galite paleisti bet kurį kiekį ar procentą:</span><span class="sxs-lookup"><span data-stu-id="ef20d-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="ef20d-130">*Procentas* – Pasirinkite šią parinktį tam, kad naudotumėte procentų pajėgumą pagrįstą atsargų limitais ir apimtimis.</span><span class="sxs-lookup"><span data-stu-id="ef20d-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="ef20d-131">Pasirenkant šią parinktį įjungiamas **Per didelio srauto procentai** laukelis ir išjungiami du su kiekiai susiję laukeliai  **Per didelio srauto kiekis** ir **Per didelio srauto padalinys**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="ef20d-132">Galite naudoti šią parinktį, jei paėmimo vietos naudoja apimtis.</span><span class="sxs-lookup"><span data-stu-id="ef20d-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="ef20d-133">Jei ši parinktis yra pasirinkta, nustatykite **Per didelio srauto procento** laukelį į procentą, kuriame daugiau papildomo darbo yra prieinama.</span><span class="sxs-lookup"><span data-stu-id="ef20d-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="ef20d-134">*Kokybė* – Pasirinkite šią parinktį, kad naudotumėte konkrečią kiekio vertę.</span><span class="sxs-lookup"><span data-stu-id="ef20d-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="ef20d-135">Pasirenkant šią parinktį išjungiamas **Per didelio srauto procentai** laukelis ir įjungiami **Per didelis  kiekis** ir **Per didelio srauto padalinys** laukeliai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="ef20d-136">Naudokite šią parinktį, kai nenaudojate tūrio vietose, kurios yra papildomos arba kai turite nuolatinius kiekius, kuriuose norite, kad daugiau atsargų būtų atvesta į vietą. </span><span class="sxs-lookup"><span data-stu-id="ef20d-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="ef20d-137">Jei ši parinktis pasirinkta, nustatykite **Per didelio srauto kiekį** ir **Per didelio srauto padalinio** laukelius ir padalinį, kuriame daugiau papildomo darbo yra prieinama.</span><span class="sxs-lookup"><span data-stu-id="ef20d-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="ef20d-138">**Perpildos kiekis:** *0.65*</span><span class="sxs-lookup"><span data-stu-id="ef20d-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="ef20d-139">Šis laukelis nustato kiekį, kuriuo vieta yra perpildyta.</span><span class="sxs-lookup"><span data-stu-id="ef20d-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="ef20d-140">Darbas bus prieinamas bet kada, kai turimo kiekio suma vietoje ir darbo kiekis yra žemesnis nei ši vertė.</span><span class="sxs-lookup"><span data-stu-id="ef20d-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="ef20d-141">Visi darbo papildymai viršijantys šią vertę bus blokuojami ir turės būti atblokuojami rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="ef20d-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="ef20d-142">Vietos laikymo limitai yra vertinami, kai darbo kiekis yra apskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="ef20d-143">**Perpildos padalinys:** *PL*</span><span class="sxs-lookup"><span data-stu-id="ef20d-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="ef20d-144">Šis laukelis nustato padalinį, kuris yra susietas su perpildos kiekiu.</span><span class="sxs-lookup"><span data-stu-id="ef20d-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="ef20d-145">Tokiu atveju, daugiau papildomo darbo bus prieinama, kai vieta sumažėja iki 0,65 padėklo (PL).</span><span class="sxs-lookup"><span data-stu-id="ef20d-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="ef20d-146">**Perpildos procentas**</span><span class="sxs-lookup"><span data-stu-id="ef20d-146">**Overflow percentage**</span></span>

        <span data-ttu-id="ef20d-147">Šis laukelis nustato procentą, kuriuo vieta yra perpildyta.</span><span class="sxs-lookup"><span data-stu-id="ef20d-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="ef20d-148">Darbas bus prieinamas bet kada, kai turimo kiekio suma vietoje ir darbo kiekis yra žemesnis nei šis procentas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="ef20d-149">Visi darbo kiekio procento papildymai viršijantys šią vertę bus blokuojami ir turės būti atblokuojami rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="ef20d-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="ef20d-150">Vietos laikymo limitai yra vertinami, kai darbo kiekio procentas yra apskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="ef20d-151">Jei nėra nustatytų jokių vietos talpinimo limitų, darbo kiekio procentas bus skaičiuojamas pagal pajėgumą, jei pajėgumo apribojimai yra nustatyti vietos profilyje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef20d-152">Jei naudojate demonstracinius duomenis **USMF** teisinis subjektas ir anksčiau įjungta *Vietos licencijos ženklo padėties* funkcija, turite būti išjungę **Įjungto licencijos ženklo vietos** nustatymus **BULK-06** vietos profiliui tam, kad būtų užbaigti mobilūs žingsniai šiame pavyzdiniame scenarijuje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="ef20d-153">Bangos veiksmo kodas</span><span class="sxs-lookup"><span data-stu-id="ef20d-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="ef20d-154">Tam, kad nustatytumėte čia aprašytą bangos žingsnio kodą, pirmiausia jums reikia naudoti [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte funkciją pavadintą *Organizacijos pločio bangos žingsnio kodas*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="ef20d-155">Eikite į **Sandėlio valdymą \> Nustatymai \> Bangos \> Bangos žingsnio kodas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="ef20d-156">Pasirinkite **Naujas** ir nustatykite tolesnes reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-156">Select **New** , and set the following values:</span></span>

    - <span data-ttu-id="ef20d-157">**Bangos veiksmo kodai:** *Papildyti*</span><span class="sxs-lookup"><span data-stu-id="ef20d-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="ef20d-158">**Bangos žingsnio aprašas:** *Papildymas*</span><span class="sxs-lookup"><span data-stu-id="ef20d-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="ef20d-159">**Bangos žingsnio tipas:** *Papildymas*</span><span class="sxs-lookup"><span data-stu-id="ef20d-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="ef20d-160">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="ef20d-161">Papildymo šablonas</span><span class="sxs-lookup"><span data-stu-id="ef20d-161">Replenishment template</span></span>

<span data-ttu-id="ef20d-162">Papildymo šablonai yra taisyklių rinkiniai, valdantys kada ir kaip vieta yra papildoma.</span><span class="sxs-lookup"><span data-stu-id="ef20d-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="ef20d-163">Eikite į **Sandėlio valdymas \> Nustatymas \> Papildymas \> Papildymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="ef20d-164">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef20d-165">**Peržiūros** skyriuje pasirinkite eilutę, kurioje **Papildymo šablono** laukelis yra nustatytas į *Papildymo poreikis*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="ef20d-166">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ef20d-166">Set the following values:</span></span>

    - <span data-ttu-id="ef20d-167">**Bangos veiksmo kodai:** *Papildyti*</span><span class="sxs-lookup"><span data-stu-id="ef20d-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="ef20d-168">**Leisti bangai reikalauti naudoti nerezervuotus kiekius:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ef20d-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="ef20d-169">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="ef20d-170">Bangos šablonas</span><span class="sxs-lookup"><span data-stu-id="ef20d-170">Wave template</span></span>

1. <span data-ttu-id="ef20d-171">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="ef20d-172">Kairiojoje juostoje nustatykite **Bangos šablono tipo** laukelį į *Siuntimas*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="ef20d-173">Pasirinkite šabloną **61 siuntimas** sąraše.</span><span class="sxs-lookup"><span data-stu-id="ef20d-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="ef20d-174">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef20d-175">**Bendras** „FastTab“, nustatykite **Automatizuoti papildymo darbo leidimo** parinktį į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="ef20d-176">Nustatykite šią parinktį į *Taip* tam, kad sukurtumėte užklausa pagrįstą papildymo darbą ir automatiškai jį išleistumėte.</span><span class="sxs-lookup"><span data-stu-id="ef20d-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="ef20d-177">Privalote įtraukti papildymo bangos metodą į bangos šabloną ir sukurti **Bangos poreikio** papildymo šablono tipą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="ef20d-178">Nustatykite papildymo šabloną **Papildymo šablonų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="ef20d-179">Tam, kad nustatytumėte papildymo šabloną, privalote įtraukti papildymo metodą į bangos šabloną.</span><span class="sxs-lookup"><span data-stu-id="ef20d-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="ef20d-180">**Metodai** „FastTab“ **Pasirinkti metodai** stulpelyje suraskite šią eilutę:</span><span class="sxs-lookup"><span data-stu-id="ef20d-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="ef20d-181">**Metodo pavadinimas** *papildymas*</span><span class="sxs-lookup"><span data-stu-id="ef20d-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="ef20d-182">**Pavadinimas** *Papildymas*</span><span class="sxs-lookup"><span data-stu-id="ef20d-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="ef20d-183">Nustatykite **Bangos žingsnio kodo** laukelį šiai linijai į *Pildyti*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="ef20d-184">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ef20d-185">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="ef20d-185">Example scenario</span></span>

<span data-ttu-id="ef20d-186">Po to, kai atliksite visus anksčiau aprašytus pavyzdžio duomenis esančius ir nustatytus, galite dirbti su šiuo scenarijumis tam, kad bandytumėte *Vietos pajėgumo papildymo* funkciją.</span><span class="sxs-lookup"><span data-stu-id="ef20d-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="ef20d-187">Šiame scenarijuje rodomos vertės apima tai, kad jūs dirbate su standartiniais demonstraciniais duomenimis, kuriuos pasirinkote **USMF** teisiniame subjekte ir tai, kad rengiate pavyzdžio įrašus, kurie yra aprašyti anksčiau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="ef20d-188">Scenarijus taip pat naudingas kaip pavyzdys rodantis, kaip funkcija gali būti naudojama gamybos parametruose.</span><span class="sxs-lookup"><span data-stu-id="ef20d-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="ef20d-189">Kurti papildymo darbą</span><span class="sxs-lookup"><span data-stu-id="ef20d-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="ef20d-190">Pardavimo užsakymo 1 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="ef20d-190">Create sales order 1</span></span>

1. <span data-ttu-id="ef20d-191">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ef20d-192">Veiksmų juostoje pasirinkite **Naujas** tam, kad atidarytumėte teksto laukelį naujo prekybos užsakymo sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="ef20d-193">Dialogo lange nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="ef20d-194">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="ef20d-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="ef20d-195">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="ef20d-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ef20d-196">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ef20d-197">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-197">The new sales order is opened.</span></span> <span data-ttu-id="ef20d-198">Jis apima naują, tuščią liniją **Prekybos užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="ef20d-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ef20d-199">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="ef20d-200">**Prekės numeris:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="ef20d-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="ef20d-201">**Kiekis:** *40*</span><span class="sxs-lookup"><span data-stu-id="ef20d-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="ef20d-202">**Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ef20d-203">**Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="ef20d-204">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ef20d-204">Close the page.</span></span>
1. <span data-ttu-id="ef20d-205">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ef20d-206">Gausite informacinį pranešimą, kuris rodo, kad bangos ir siuntimo ID buvo sukurti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="ef20d-207">Sukuriama ir papildymo banga.</span><span class="sxs-lookup"><span data-stu-id="ef20d-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="ef20d-208">Taip pat gausite įspėjimą, kuris sako „Darbo ID XXX negali būti atblokuotas, nes nepabaigtas papildymo darbas.“</span><span class="sxs-lookup"><span data-stu-id="ef20d-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="ef20d-209">Pardavimo užsakymo 2 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="ef20d-209">Create sales order 2</span></span>

1. <span data-ttu-id="ef20d-210">**Visų prekybos užsakymų** lange, veiksmų juostoje pasirinkite **Naujas** tam, kad atidarytumėte teksto laukelį naujo prekybos užsakymo sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-210">On the **All sales orders** , page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="ef20d-211">Teksto laukelyje nustatykite šią vertę:</span><span class="sxs-lookup"><span data-stu-id="ef20d-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="ef20d-212">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ef20d-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ef20d-213">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="ef20d-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ef20d-214">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ef20d-215">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-215">The new sales order is opened.</span></span> <span data-ttu-id="ef20d-216">Jis apima naują, tuščią liniją **Prekybos užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="ef20d-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ef20d-217">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="ef20d-218">**Prekės numeris:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="ef20d-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="ef20d-219">**Kiekis:** *60*</span><span class="sxs-lookup"><span data-stu-id="ef20d-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="ef20d-220">**Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ef20d-221">**Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="ef20d-222">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ef20d-222">Close the page.</span></span>
1. <span data-ttu-id="ef20d-223">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ef20d-224">Gausite informacinį pranešimą, kuris rodo, kad bangos ir siuntimo ID buvo sukurti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="ef20d-225">Sukuriama ir papildymo banga.</span><span class="sxs-lookup"><span data-stu-id="ef20d-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="ef20d-226">Taip pat gausite įspėjimą, kuris sako „Darbo ID XXX negali būti atblokuotas, nes nepabaigtas papildymo darbas.“</span><span class="sxs-lookup"><span data-stu-id="ef20d-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="ef20d-227">Pardavimo užsakymo 3 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="ef20d-227">Create sales order 3</span></span>

1. <span data-ttu-id="ef20d-228">**Visų prekybos užsakymų** puslapyje, veiksmų juostoje pasirinkite **Naujas** tam, kad atidarytumėte teksto laukelį naujo prekybos užsakymo sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="ef20d-229">Dialogo lange nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="ef20d-230">**Kliento sąskaita:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="ef20d-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="ef20d-231">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="ef20d-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ef20d-232">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ef20d-233">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-233">The new sales order is opened.</span></span> <span data-ttu-id="ef20d-234">Jis apima naują, tuščią liniją **Prekybos užsakymo eilučių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="ef20d-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ef20d-235">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ef20d-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="ef20d-236">**Prekės numeris:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="ef20d-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="ef20d-237">**Kiekis:** *30*</span><span class="sxs-lookup"><span data-stu-id="ef20d-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="ef20d-238">**Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ef20d-239">**Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="ef20d-240">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ef20d-240">Close the page.</span></span>
1. <span data-ttu-id="ef20d-241">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ef20d-242">Gausite informacinį pranešimą, kuris rodo, kad bangos ir siuntimo ID buvo sukurti.</span><span class="sxs-lookup"><span data-stu-id="ef20d-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="ef20d-243">Sukuriama ir papildymo banga.</span><span class="sxs-lookup"><span data-stu-id="ef20d-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="ef20d-244">Taip pat gausite įspėjimą, kuris sako „Darbo ID XXX negali būti atblokuotas, nes nepabaigtas papildymo darbas.“</span><span class="sxs-lookup"><span data-stu-id="ef20d-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="ef20d-245">Peržiūrėti išsamią darbo informaciją</span><span class="sxs-lookup"><span data-stu-id="ef20d-245">View work details</span></span>

1. <span data-ttu-id="ef20d-246">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ef20d-247">**Peržiūros** skyriuje filtruokite **Sandėlio** stulpelį sandėliui *61*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="ef20d-248">Turėtumėte matyti, kad septynių darbų ID buvo sukurti trims prekybos užsakymų reikalavimams.</span><span class="sxs-lookup"><span data-stu-id="ef20d-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="ef20d-249">Tris iš septynių darbo ID turi **Darbo užsakymo tipo** vertę *Papildymas* , o keturi turi **Darbo užsakymo tipo** vertę *Prekybos užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-249">Three of the seven work IDs have a **Work order type** value of *Replenishment* , and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="ef20d-250">Visi trys darbo ID turintys **Darbo užsakymo tipo** vertę *Papildymas* turi tas pačias *Paėmimo* ir *Padėjimo* vietas **Eilučių** skyriuje:</span><span class="sxs-lookup"><span data-stu-id="ef20d-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="ef20d-251">**Paimti:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="ef20d-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="ef20d-252">**Padėti:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="ef20d-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="ef20d-253">Du darbo ID buso sukurti prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="ef20d-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="ef20d-254">Atkreipkite dėmesį į darbo ID prekybos užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="ef20d-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="ef20d-255">Priklausomai nuo turimų kiekių, sukurti darbo kiekiai gali nežymiai skiris.</span><span class="sxs-lookup"><span data-stu-id="ef20d-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="ef20d-256">Nepaisant to, bendros sukurtos darbo antraštės turėtų atitikti šį scenarijaus pavyzdį. </span><span class="sxs-lookup"><span data-stu-id="ef20d-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="ef20d-257">Turimų atsargų licencijos numerio ID</span><span class="sxs-lookup"><span data-stu-id="ef20d-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="ef20d-258">Vėliau šiame scenarijuje naudosite sandėlio programą (ar emuliatorių), kuriame turėsite nustatyti licencijos numerį tam, kad pabaigtumėte paėmimą ir papildymo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="ef20d-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="ef20d-259">Tam, kad rastumėte vėliau jums reikalingų licencijos numerių ID, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ef20d-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="ef20d-260">Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="ef20d-261">Pasirinkite **Rodyti filtrus** mygtuką, kad atidarytumėte filtro juostą,</span><span class="sxs-lookup"><span data-stu-id="ef20d-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="ef20d-262">Įveskite tolesnius filtravimo kriterijus, kad gautumėte licencijos numerius šiam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="ef20d-263">Naudokite *pradžias su* filtru.</span><span class="sxs-lookup"><span data-stu-id="ef20d-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="ef20d-264">**Prekės numeris:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="ef20d-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="ef20d-265">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="ef20d-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ef20d-266">Pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-266">Select **Apply**.</span></span>
1. <span data-ttu-id="ef20d-267">Veiksmų juostoje, pasirinkite **Dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="ef20d-268"> **Dimensijos rodymo** teksto laukelyje, **Dimensijų talpinimas** skyriuje pasirinkite visas vertes.</span><span class="sxs-lookup"><span data-stu-id="ef20d-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="ef20d-269">**Perlaidos** skyriuje pasirinkite **Elemento numerį** ir **Kiekį \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="ef20d-270">Kai pabaigsite pasirinkite **Gerai** tam, kad uždarytumėte teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="ef20d-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ef20d-271">**Turimas** tinklelis rodo licencijos numerio numerius elementui *T0100* kiekvienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="ef20d-272">Atkreipkite dėmesį į licencijos numerį esantį kiekvienoje vietoje, nes jums šios informacijos reikės vėliau.</span><span class="sxs-lookup"><span data-stu-id="ef20d-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="ef20d-273">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ef20d-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="ef20d-274">Proceso veiksmai</span><span class="sxs-lookup"><span data-stu-id="ef20d-274">Process steps</span></span>

<span data-ttu-id="ef20d-275">Atliksite sandėlio vietos papildymą pirmiems dviems darbo ID.</span><span class="sxs-lookup"><span data-stu-id="ef20d-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="ef20d-276">Dirbas su trečiuoju papildymo darbu bus užblokuotas, kol atsargų lygis paėmimo vietoje nukris žemiau slenksčio.</span><span class="sxs-lookup"><span data-stu-id="ef20d-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="ef20d-277">Papildymas</span><span class="sxs-lookup"><span data-stu-id="ef20d-277">Replenishment</span></span>

1. <span data-ttu-id="ef20d-278">Prisijungti prie sandėlio programos kaip naudotojas sandėlyje *61*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="ef20d-279">(Įveskite *61* kaip vartotojo ID ir *1* slaptažodį.)</span><span class="sxs-lookup"><span data-stu-id="ef20d-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ef20d-280">Eikite į **Atsargos \> Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="ef20d-281">Esate paskatintas pabaigti pirmąjį papildymo darbą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="ef20d-282">Rodomi elemento numeris, kiekis ir paėmimo vieta.</span><span class="sxs-lookup"><span data-stu-id="ef20d-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="ef20d-283">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="ef20d-284">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="ef20d-285">Sistema sukuria licencijos numerio numerį paimto elemento naujam licencijos numeriui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="ef20d-286">Pasirinkite **Gerai** vertės patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="ef20d-287">Rodomas paėmimo darbas, kuris naudotojui rodo padėti galutinį licencijos numerį į papildymo vietą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="ef20d-288">*Padėjimo* vieta turi būti **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="ef20d-289">Patvirtinkite padėjimo informaciją ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="ef20d-290">Gausite „Darbas baigtas“ pranešimą ir yra rodoma informacija apie kitą paėmimo papildymo darbą: elemento numeris, kiekis ir vieta, iš kurios paimama.</span><span class="sxs-lookup"><span data-stu-id="ef20d-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="ef20d-291">Paėmimo vieta bus ta pati, kaip pirmoji papildymo vieta.</span><span class="sxs-lookup"><span data-stu-id="ef20d-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="ef20d-292">Dėl to, licencijos numeris turės tą patį licencijos numerio ID, kuris buvo naudojamas pirmajai papildymo darbo užduočiai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="ef20d-293">Pakartokite ankstesnius žingsnius tam, kad užbaigtumėte papildymo darbą antrajai darbo užduočiai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="ef20d-294">Kiekio ir gaultinis licencijos numeris skirsis nuo kiekio ir galutinio licencijos numerio pirmajai darbo užduočiai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="ef20d-295">Pabaigus antrąjį papildymo darbą, gausite „Darbas baigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="ef20d-296">Mobilus prietaisas taip pat informuos, kad nėra jokio prieinamo darbo, nors keletas papildomų darbų išliks.</span><span class="sxs-lookup"><span data-stu-id="ef20d-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="ef20d-297">Tokia seka atsitinka, nes papildymo darbas turi prieinamumo *Sulaikymo* statusą ir yra pažymėtas kaip **Blokuojamas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="ef20d-298">*Laikomas* statusas buvo paleistas, nes vietos profilis paėmimo vietoje, kurioje darbas buvo priskirtas, turi **Kiekio perviršio** vertę *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="ef20d-299">Dvi ankstesnės papildymo darbo užduotys užpildytos vietoje beveiki iki perviršio limito elementui *T0100*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="ef20d-300">(Padalinio pavertimas elementui *1 PL = 100 ea*.) Dėl to, likęs papildymo darbas viršys vietos perviršio limitą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="ef20d-301">Kol pakankamai atsargų yra paimta iš vietos tam, kad būtų pristatytas tolesnis darbo paleidimo slenkstis mobilaus prietaiso meniu elemente, šis papildymo darbas liks užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="ef20d-302">Prekybos užsakymo paėmimas</span><span class="sxs-lookup"><span data-stu-id="ef20d-302">Sales order pick</span></span>

<span data-ttu-id="ef20d-303">Prieš likusios papildymo darbo užduoties užbaigimą, paėmimo vieta turi būti atsargoms priskirta lygmeniu, kuriame likęs papildymo darbas gali būti atblokuotas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="ef20d-304">Kitaip tariant, turimų atsargų suma vietoje ir papildymo kiekis negali viršyti **Perviršio kiekio** vertės.</span><span class="sxs-lookup"><span data-stu-id="ef20d-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="ef20d-305">Kai suma yra mažesnė nei perviršio kiekis, likęs papildymo darbas bus atblokuotas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="ef20d-306">Prisijungti prie sandėlio programos kaip naudotojas sandėlyje *61*.</span><span class="sxs-lookup"><span data-stu-id="ef20d-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="ef20d-307">(Įveskite *61* kaip vartotojo ID ir *1* slaptažodį.)</span><span class="sxs-lookup"><span data-stu-id="ef20d-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ef20d-308">Eikite į **Išorė \> Prekybos paėmimas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="ef20d-309">Įveskite pirmojo darbo ID prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="ef20d-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="ef20d-310">Žiūrėkite darbo ID prekybos užsakymuose, kuriuos anksčiau užsirašėte **Darbo informacijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ef20d-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="ef20d-311">Darbo ID, kurį įvedėte čia, sukurs 10 ea kiekio paėmimo darbą iš dviejų atskirų vietų.</span><span class="sxs-lookup"><span data-stu-id="ef20d-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="ef20d-312">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-312">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-313">**Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą pirmajai vietai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="ef20d-314">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="ef20d-315">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="ef20d-316">**Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="ef20d-317">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="ef20d-318">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="ef20d-319">**Prekybos užsakymai: Padėjimas** puslapis rodo jums, kad turite atidėti abu pabaigtus paėmimo darbus į išorės etapo vietą. </span><span class="sxs-lookup"><span data-stu-id="ef20d-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="ef20d-320">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-320">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-321">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="ef20d-322">Įveskite antrojo darbo ID prekybos užsakymui 1.</span><span class="sxs-lookup"><span data-stu-id="ef20d-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="ef20d-323">Yra tik viena paėmimo užduotis šio darbo ID.</span><span class="sxs-lookup"><span data-stu-id="ef20d-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="ef20d-324">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-324">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-325">**Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="ef20d-326">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="ef20d-327">Licencijos numeris, kurį nurodėte bus sistemos sukurtas licencijos numeris iš papildymo darbo užduočių.</span><span class="sxs-lookup"><span data-stu-id="ef20d-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="ef20d-328">Tam, kad įsitikintumėte, jog apėmėte tinkamą licencijos numerio ID, patikrinkite inventorių **Turimo sąrašo** puslapyje elementui, vietai ir kiekiui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="ef20d-329">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="ef20d-330">Patvirtinkite instrukcija dėl padėjimo užduoties į išorės etapo vietą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="ef20d-331">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-331">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-332">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="ef20d-333">Prekybos užsakymas 2 yra užblokuotas dėl paėmimo, nes su juo susieta papildymo užduotis nėra baigta. </span><span class="sxs-lookup"><span data-stu-id="ef20d-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="ef20d-334">Šiuo metu dar nėra 30 ea kiekio paėmimo vietoje ir papildymo kiekis prekybos užsakymui 2 yra 60 ea.</span><span class="sxs-lookup"><span data-stu-id="ef20d-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="ef20d-335">Turimų atsargų suma ir papildymo atsargos (90 ea) viršija perviršio kiekį 0,65 PL (arba 65 ea).</span><span class="sxs-lookup"><span data-stu-id="ef20d-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="ef20d-336">Prieš tai, kai papildymo darbas bus užbaigtas, prekybos užsakymas 3 turi būti paimtas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="ef20d-337">Įveskite pirmojo darbo ID prekybos užsakymui 3.</span><span class="sxs-lookup"><span data-stu-id="ef20d-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="ef20d-338">Yra tik viena paėmimo užduotis šio darbo ID.</span><span class="sxs-lookup"><span data-stu-id="ef20d-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="ef20d-339">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-339">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-340">**Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="ef20d-341">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="ef20d-342">Licencijos numeris, kurį nurodėte bus sistemos sukurtas licencijos numeris iš papildymo darbo užduočių.</span><span class="sxs-lookup"><span data-stu-id="ef20d-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="ef20d-343">Tam, kad įsitikintumėte, jog apėmėte tinkamą licencijos numerio ID, patikrinkite inventorių **Turimo sąrašo** puslapyje elementui, vietai ir kiekiui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="ef20d-344">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="ef20d-345">Patvirtinkite instrukcija dėl padėjimo užduoties į išorės etapo vietą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="ef20d-346">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-346">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-347">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="ef20d-348">Kai tik turimų atsargų kiekio paėmimo vietoje ir papildymo suma yra žemiau slenksčio, jūs galėsite apdoroti likusį papildymo darbą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="ef20d-349">Grįžkite į **Darbo išsamios informacijos** puslapį ir atkreipkite dėmesį, kad papildymo darbo prieinamumas galutinei papildymo daliai (prekybos užsakymui 2) yra *Atviras* , nes dabar yra pakankamai vietos vietoje, kad ji priimtų papildymą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open* , because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="ef20d-350">Galite apdoroti šį papildymo darbą per mobilųjį įrenginį.</span><span class="sxs-lookup"><span data-stu-id="ef20d-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="ef20d-351">Eikite į **Atsargos \> Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="ef20d-352">Esate paskatintas pabaigti likusį papildymo darbą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="ef20d-353">Rodomi elemento numeris, kiekis ir paėmimo vieta.</span><span class="sxs-lookup"><span data-stu-id="ef20d-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="ef20d-354">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="ef20d-355">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="ef20d-356">Sistema sukuria licencijos numerio numerį paimto elemento naujam licencijos numeriui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="ef20d-357">Pasirinkite **Gerai** vertės patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="ef20d-358">Rodomas paėmimo darbas, kuris naudotojui rodo padėti galutinį licencijos numerį į papildymo vietą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="ef20d-359">*Padėjimo* vieta turi būti **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="ef20d-360">Patvirtinkite padėjimo informaciją ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="ef20d-361">Gausite „Darbas baigtas“ ir „Nėra esamo darbo“ pranešimus.</span><span class="sxs-lookup"><span data-stu-id="ef20d-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="ef20d-362">Dabar galite paimti prekybos užsakymą 2.</span><span class="sxs-lookup"><span data-stu-id="ef20d-362">You can now pick sales order 2.</span></span> <span data-ttu-id="ef20d-363">Jis taps atblokuotas, kai papildymo darbas bus susietas su pabaigtu prekybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="ef20d-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="ef20d-364">Įveskite pirmojo darbo ID prekybos užsakymui 2.</span><span class="sxs-lookup"><span data-stu-id="ef20d-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="ef20d-365">Yra tik viena paėmimo užduotis šio darbo ID.</span><span class="sxs-lookup"><span data-stu-id="ef20d-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="ef20d-366">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-366">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-367">**Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.</span><span class="sxs-lookup"><span data-stu-id="ef20d-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="ef20d-368">**LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ef20d-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="ef20d-369">Licencijos numeris, kurį nurodėte bus sistemos sukurtas licencijos numeris iš papildymo darbo užduoties.</span><span class="sxs-lookup"><span data-stu-id="ef20d-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="ef20d-370">Tam, kad įsitikintumėte, jog apėmėte tinkamą licencijos numerio ID, patikrinkite inventorių **Turimo sąrašo** puslapyje elementui, vietai ir kiekiui.</span><span class="sxs-lookup"><span data-stu-id="ef20d-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="ef20d-371">Pasirinkite **Gerai** mygtuką (pažymint simbolį).</span><span class="sxs-lookup"><span data-stu-id="ef20d-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="ef20d-372">Patvirtinkite instrukcija dėl padėjimo užduoties į išorės etapo vietą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="ef20d-373">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef20d-373">Select **OK**.</span></span>

    <span data-ttu-id="ef20d-374">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ef20d-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="ef20d-375">Pastabos ir patarimai</span><span class="sxs-lookup"><span data-stu-id="ef20d-375">Notes and tips</span></span>

- <span data-ttu-id="ef20d-376">Ši funkcija veikia su visais papildymo tipais: bangos poreikiu, min./maks., apkrovos poreikiu ir vietos priskyrimu.</span><span class="sxs-lookup"><span data-stu-id="ef20d-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="ef20d-377">Galite rankiniu būdu viršyti papildymo darbo prieinamumą kiekvienai darbo antraštei iš norimo **Darbo informacijos** puslapio.</span><span class="sxs-lookup"><span data-stu-id="ef20d-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="ef20d-378">Kai sistema nustato papildymo darbo prieinamumą, ji svarsto visas atsargas, kurios jau yra vietoje prieš pabaigiant darbą</span><span class="sxs-lookup"><span data-stu-id="ef20d-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="ef20d-379">Kiekvienas prekybos užsakymo elementas yra susiejamas su konkrečiu papildymo darbu.</span><span class="sxs-lookup"><span data-stu-id="ef20d-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="ef20d-380">Nėra jokių atitinkamų prekybos užsakymo darbo prieinamumo funkcijų.</span><span class="sxs-lookup"><span data-stu-id="ef20d-380">There is no corresponding sales work availability functionality.</span></span>
