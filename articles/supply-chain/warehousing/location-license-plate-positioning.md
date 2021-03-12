---
title: Vietos numerio lentelės padėtis
description: Numerio lentelės vietos nustatymas leidžia matyti, kur numerio lentelė yra kelių padėklų vietoje, pvz., vietoje, kurioje naudojamas dvigubai gilių padėklų išdėstymas.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6d94d37368b8fc3ff7dbe4c1845acd52bf2a64ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004682"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="221c5-103">Vietos numerio lentelės padėtis</span><span class="sxs-lookup"><span data-stu-id="221c5-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="221c5-104">Numerio lentelės vietos nustatymas leidžia matyti, kur numerio lentelė yra kelių padėklų vietoje, pvz., vietoje, kurioje naudojamas dvigubai gilių padėklų išdėstymas.</span><span class="sxs-lookup"><span data-stu-id="221c5-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="221c5-105">Funkcija prideda eilės numerį prie kiekvienos numerio lentelės, padėtos į saugojimo vietą.</span><span class="sxs-lookup"><span data-stu-id="221c5-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="221c5-106">Šis eilės numeris naudojamas, kad būtų galima užsakyti numerių lenteles saugojimo vietoje.</span><span class="sxs-lookup"><span data-stu-id="221c5-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="221c5-107">Todėl funkcija sumaniai palaiko scenarijus, kuriuose klientai naudoja gravitacinę išdėstymo sistemą ir turi žinoti, kad pasirenkant, kuriai numerio lentelė yra priekyje.</span><span class="sxs-lookup"><span data-stu-id="221c5-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="221c5-108">Šioje temoje parodytas scenarijus, kaip nustatyti ir naudoti funkciją.</span><span class="sxs-lookup"><span data-stu-id="221c5-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="221c5-109">Įjunkite Vietos numerio lentelės vietos nustatymo funkciją</span><span class="sxs-lookup"><span data-stu-id="221c5-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="221c5-110">Prieš naudojanti numerio lentelės vietos išdėstymą, funkcija turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="221c5-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="221c5-111">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="221c5-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="221c5-112">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="221c5-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="221c5-113">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="221c5-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="221c5-114">**Funkcijos pavadinimas:** *Vietos numerio lentelės išdėstymas*</span><span class="sxs-lookup"><span data-stu-id="221c5-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="221c5-115">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="221c5-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="221c5-116">Įgalinkite duomenų pavyzdį</span><span class="sxs-lookup"><span data-stu-id="221c5-116">Make sample data available</span></span>

<span data-ttu-id="221c5-117">Norėdami dirbti su šiuo scenarijumi naudojant čia rekomenduojamas vertes, turite dirbti su sistema, kurioje įdiegti duomenų pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="221c5-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="221c5-118">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="221c5-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="221c5-119">Nustatykite funkciją šiam scenarijui</span><span class="sxs-lookup"><span data-stu-id="221c5-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="221c5-120">Užbaikite šias procedūras, kad nustatytumėte *Vietos numerio lentelės nustatymas* funkciją šioje temoje pristatytam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="221c5-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="221c5-121">Vietos šablonai</span><span class="sxs-lookup"><span data-stu-id="221c5-121">Location profiles</span></span>

<span data-ttu-id="221c5-122">Funkcija turi būti įjungta kiekviename vietos, kurioje ji bus naudojama, profilyje.</span><span class="sxs-lookup"><span data-stu-id="221c5-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="221c5-123">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="221c5-124">Vietų profilių sąraše, kairėje, pasirinkite **MASINIS-06**.</span><span class="sxs-lookup"><span data-stu-id="221c5-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="221c5-125">**Bendra** „FastTab” skirtuke dvi funkciją papildė dvi naujos parinktys.</span><span class="sxs-lookup"><span data-stu-id="221c5-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="221c5-126">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="221c5-126">Set the following values:</span></span>

    - <span data-ttu-id="221c5-127">**Įjungti numerio lentelės padėtį:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="221c5-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="221c5-128">Kai ši parinktis nustatyta į *Taip*, numerio lentelės pozicija bus išlaikyta vietos numerių lentelėse.</span><span class="sxs-lookup"><span data-stu-id="221c5-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="221c5-129">**Rodyti mobiliojo įrenginio LP padėtį:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="221c5-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="221c5-130">Kai parinktis nustatyta į *Taip*, numerio lentelės pozicija bus rodoma mobiliojo įrenginio vartotojams koreguojant ir skaičiuojant.</span><span class="sxs-lookup"><span data-stu-id="221c5-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="221c5-131">Šią pasirinktį galima pakeisti tik tada, kai funkcija įjungta.</span><span class="sxs-lookup"><span data-stu-id="221c5-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="221c5-132">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="221c5-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="221c5-133">Vietos nurodymai</span><span class="sxs-lookup"><span data-stu-id="221c5-133">Location directives</span></span>

1. <span data-ttu-id="221c5-134">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="221c5-135">Kairiojoje srityje įsitikinkite, kad **Darbo užsakymo tipas** laukas nustatytas į *Pardavimų užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="221c5-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="221c5-136">Vietų nurodymų sąraše pasirinkite **61 SO paimti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="221c5-137">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="221c5-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="221c5-138">**Eilutės** „FastTab” pasirinkite eilutę, kuri turi **Eilės numeris** *2* vertę.</span><span class="sxs-lookup"><span data-stu-id="221c5-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="221c5-139">**Vietos nurodymų veiksmai** „FastTab” skirtuke pasirinkite eilutę, kurios **Pavadinimas** vertė *Pasirinkti mažiau nei padėklą* (turi būti tik vienintelė eilutė), ir pakeiskite jos **Eilės numeris** vertę į *2*.</span><span class="sxs-lookup"><span data-stu-id="221c5-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="221c5-140">Pasirinkite į **Nauja** virš tinklelio pridėti eilutę naujam vietos nurodymo veiksmui.</span><span class="sxs-lookup"><span data-stu-id="221c5-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="221c5-141">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="221c5-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="221c5-142">**Eilės numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="221c5-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="221c5-143">**Pavadinimas:** *Paėmimo pozicija 1*</span><span class="sxs-lookup"><span data-stu-id="221c5-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="221c5-144">Kol renkamasi nauja eilutė, virš tinklelio pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="221c5-145">Užklausų rengyklėje pasirinkite **Sujungimai** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="221c5-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="221c5-146">Išplėskite **Vietos** lentelę sujungimą, kad parodytų sujungimą prie **Atsargų dimensijos** lentelės.</span><span class="sxs-lookup"><span data-stu-id="221c5-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="221c5-147">Išplėskite **Atsargų dimensijos** lentelę sujungimą, kad parodytų sujungimą prie **Turimos atsargos** lentelės.</span><span class="sxs-lookup"><span data-stu-id="221c5-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="221c5-148">Pasirinkite **Atsargų dimensijos** ir pasirinkite **Pridėti lentelės sujungimą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="221c5-149">Pasirodančiame lentelių sąraše **Ryšys** stulpelyje pasirinkite **Numerio lentelė (numerio lentelė)**.</span><span class="sxs-lookup"><span data-stu-id="221c5-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="221c5-150">Tada pasirinkite **Pasirinkti**, kad į **Numerio lentelė** pridėtumėte **Atsargų dimensijos** lentelės sujungimą.</span><span class="sxs-lookup"><span data-stu-id="221c5-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="221c5-151">Kol **Numerio lentelė** vis dar pasirinkta, pasirinkite **Pridėti lentelės sujungimą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="221c5-152">Pasirodančiame lentelių sąraše **Ryšys** stulpelyje pasirinkite **Vietos numerio lentelės nustatymas (numerio lentelė)**.</span><span class="sxs-lookup"><span data-stu-id="221c5-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="221c5-153">Tada pasirinkite **Pasirinkti**, kad į **Vietos numerio lentelės nustatymas** pridėtumėte **Atsargų dimensijos** lentelės sujungimą.</span><span class="sxs-lookup"><span data-stu-id="221c5-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="221c5-154">![Lentelių sujungimai](media/LpTableJoin.png "Lentelių sujungimai")</span><span class="sxs-lookup"><span data-stu-id="221c5-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="221c5-155">Pasirinkite **Gerai**, kad patvirtintumėte atnaujintus sujungtas lenteles ir uždarytumėte užklausos rengyklę.</span><span class="sxs-lookup"><span data-stu-id="221c5-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="221c5-156">„FastTab“ skirtuke **Vietos nurodymų veiksmai** vėl pasirinkite **Redaguoti užklausą**, kad iš naujo atidarytumėte užklausos rengyklę.</span><span class="sxs-lookup"><span data-stu-id="221c5-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="221c5-157">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="221c5-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="221c5-158">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="221c5-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="221c5-159">**Lentelė:** *Vietos numerio lentelės nustatymas*</span><span class="sxs-lookup"><span data-stu-id="221c5-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="221c5-160">**Išvestinė lentelė:** *Vietos numerio lentelės nustatymas*</span><span class="sxs-lookup"><span data-stu-id="221c5-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="221c5-161">**Laukas:** *LP pozicija*</span><span class="sxs-lookup"><span data-stu-id="221c5-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="221c5-162">**Kriterijai:** *1*</span><span class="sxs-lookup"><span data-stu-id="221c5-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="221c5-163">![Naujas diapazonas](media/LpPositionCriteria.png "Naujas diapazonas")</span><span class="sxs-lookup"><span data-stu-id="221c5-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="221c5-164">Pasirinkite **Gerai**, kad patvirtintumėte pakeitimus ir uždarytumėte užklausų rengyklę.</span><span class="sxs-lookup"><span data-stu-id="221c5-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="221c5-165">Nustatykite duomenų pavyzdį šiam scenarijui</span><span class="sxs-lookup"><span data-stu-id="221c5-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="221c5-166">Šiam scenarijui vartotojas turi prisijungti prie sandėliavimo mobiliosios programėlės naudodamas darbuotoją, nustatytą sandėliui *61*, kad atliktų darbą.</span><span class="sxs-lookup"><span data-stu-id="221c5-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="221c5-167">Vartotojas taip pat turi atlikti operacijas.</span><span class="sxs-lookup"><span data-stu-id="221c5-167">The user must also complete transactions.</span></span>

<span data-ttu-id="221c5-168">Kadangi *Vietos numerio lentelės nustatymas* funkcija prideda naują identifikatorių, skirtą numerių lentelių pozicijoms, vietoje, iš pradžių turite sukurti duomenų, kad šis scenarijus veiktų.</span><span class="sxs-lookup"><span data-stu-id="221c5-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="221c5-169">Vietoje skaičiavimo pirmoji vieta</span><span class="sxs-lookup"><span data-stu-id="221c5-169">Spot-count the first location</span></span>

1. <span data-ttu-id="221c5-170">Atverkite sandėliavimo mobiliąją programėlę, kad prisijungtumėte prie sandėlio *61*.</span><span class="sxs-lookup"><span data-stu-id="221c5-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="221c5-171">Eikite į **Atsargos \>Vietoje skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="221c5-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="221c5-172">**Vietoje skaičiavimas** puslapyje nustatykite **Vietos** lauką į *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="221c5-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="221c5-173">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-173">Select **OK**.</span></span>

    <span data-ttu-id="221c5-174">Puslapyje rodoma jūsų įvesta vieta.</span><span class="sxs-lookup"><span data-stu-id="221c5-174">The page shows the location that you entered.</span></span> <span data-ttu-id="221c5-175">Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”</span><span class="sxs-lookup"><span data-stu-id="221c5-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="221c5-176">Pasirinkite **Atnaujinti**, kad pridėtumėte vietą.</span><span class="sxs-lookup"><span data-stu-id="221c5-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="221c5-177">**Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **Prekė** lauką ir įveskite vertę *A0001*.</span><span class="sxs-lookup"><span data-stu-id="221c5-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="221c5-178">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-178">Select **OK**.</span></span>
1. <span data-ttu-id="221c5-179">**Ciklo skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **LP** lauką ir įveskite vertę *LP1001* (arba kitą jūsų pasirinktą numerio lentelės numerį).</span><span class="sxs-lookup"><span data-stu-id="221c5-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="221c5-180">**Ciklų skaičius: pridėti naują LP arba prekę** puslapis rodo **Numerio lentelės pozicija 1**.</span><span class="sxs-lookup"><span data-stu-id="221c5-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="221c5-181">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-181">Select **OK**.</span></span>

    <span data-ttu-id="221c5-182">Dabar turite nurodyti prekės kiekį, suskaičiuotą numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="221c5-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="221c5-183">Nustatykite **Kiek.** lauką į *10*.</span><span class="sxs-lookup"><span data-stu-id="221c5-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="221c5-184">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-184">Select **OK**.</span></span>

    <span data-ttu-id="221c5-185">Puslapyje rodoma jūsų įvesta vieta.</span><span class="sxs-lookup"><span data-stu-id="221c5-185">The page shows the location that you entered.</span></span> <span data-ttu-id="221c5-186">Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”</span><span class="sxs-lookup"><span data-stu-id="221c5-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="221c5-187">Pasirinkite **Atnaujinti**, kad pridėtumėte dar vieną skaičių vietoje.</span><span class="sxs-lookup"><span data-stu-id="221c5-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="221c5-188">**Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **Prekė** lauką ir įveskite vertę *A0002*.</span><span class="sxs-lookup"><span data-stu-id="221c5-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="221c5-189">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-189">Select **OK**.</span></span>
1. <span data-ttu-id="221c5-190">**Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **LP** lauką ir įveskite vertę *LP1002* (arba bet kokį kitą savo pasirinktą numerio lentelės numerį, tik jei jis skiriasi nuo anksčiau nurodyto numerio lentelės numerio).</span><span class="sxs-lookup"><span data-stu-id="221c5-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="221c5-191">Pakeiskite numerio lentelės padėtį nustatydami **LP pozicija** lauką į *2*.</span><span class="sxs-lookup"><span data-stu-id="221c5-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="221c5-192">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-192">Select **OK**.</span></span>
1. <span data-ttu-id="221c5-193">Nurodykite prekės kiekį, suskaičiuotą numerio lentelėje, nustatydami **Kiek.** lauką į *10*.</span><span class="sxs-lookup"><span data-stu-id="221c5-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="221c5-194">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-194">Select **OK**.</span></span>

    <span data-ttu-id="221c5-195">Puslapyje rodoma jūsų įvesta vieta.</span><span class="sxs-lookup"><span data-stu-id="221c5-195">The page shows the location that you entered.</span></span> <span data-ttu-id="221c5-196">Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”</span><span class="sxs-lookup"><span data-stu-id="221c5-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="221c5-197">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-197">Select **OK**.</span></span>

<span data-ttu-id="221c5-198">Dabar darbas baigtas.</span><span class="sxs-lookup"><span data-stu-id="221c5-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="221c5-199">Vietoje skaičiavimo antroji vieta</span><span class="sxs-lookup"><span data-stu-id="221c5-199">Spot-count the second location</span></span>

1. <span data-ttu-id="221c5-200">**Vietoje skaičiavimas** puslapyje nustatykite **Vieta** lauką į *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="221c5-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="221c5-201">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-201">Select **OK**.</span></span>

    <span data-ttu-id="221c5-202">Puslapyje rodoma jūsų įvesta vieta.</span><span class="sxs-lookup"><span data-stu-id="221c5-202">The page shows the location that you entered.</span></span> <span data-ttu-id="221c5-203">Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”</span><span class="sxs-lookup"><span data-stu-id="221c5-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="221c5-204">Pasirinkite **Atnaujinti**, kad pridėtumėte vietą.</span><span class="sxs-lookup"><span data-stu-id="221c5-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="221c5-205">**Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **Prekė** lauką ir įveskite vertę *A0002*.</span><span class="sxs-lookup"><span data-stu-id="221c5-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="221c5-206">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-206">Select **OK**.</span></span>
1. <span data-ttu-id="221c5-207">**Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **LP** lauką ir įveskite vertę *LP1003* (arba bet kokį kitą savo pasirinktą numerio lentelės numerį, tik jei jis skiriasi nuo numerio lentelių numerių, anksčiau nurodytų ankstesnėje procedūroje).</span><span class="sxs-lookup"><span data-stu-id="221c5-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="221c5-208">**Ciklų skaičius: pridėti naują LP arba prekę** puslapis rodo **Numerio lentelės pozicija 1**.</span><span class="sxs-lookup"><span data-stu-id="221c5-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="221c5-209">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-209">Select **OK**.</span></span>
1. <span data-ttu-id="221c5-210">Nurodykite prekės kiekį, suskaičiuotą numerio lentelėje, nustatydami **Kiek.** lauką į *10*.</span><span class="sxs-lookup"><span data-stu-id="221c5-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="221c5-211">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-211">Select **OK**.</span></span>

    <span data-ttu-id="221c5-212">Puslapyje rodoma jūsų įvesta vieta.</span><span class="sxs-lookup"><span data-stu-id="221c5-212">The page shows the location that you entered.</span></span> <span data-ttu-id="221c5-213">Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”</span><span class="sxs-lookup"><span data-stu-id="221c5-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="221c5-214">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-214">Select **OK**.</span></span>

<span data-ttu-id="221c5-215">Dabar darbas baigtas.</span><span class="sxs-lookup"><span data-stu-id="221c5-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="221c5-216">Darbo informacija</span><span class="sxs-lookup"><span data-stu-id="221c5-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="221c5-217">Vietų skaičiavimai iš mobiliosios programėlės sukuria ciklo skaičiavimo darbą „Microsoft Dynamics 365”.</span><span class="sxs-lookup"><span data-stu-id="221c5-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="221c5-218">Darbui atlikti reikia, kad skaičiavimai būtų priimti prieš juos registruojant į atsargas.</span><span class="sxs-lookup"><span data-stu-id="221c5-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="221c5-219">Prisijunkite prie „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="221c5-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="221c5-220">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="221c5-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="221c5-221">**Apžvalga** skirtuke ieškokite eilučių, turinčių šias vertes:</span><span class="sxs-lookup"><span data-stu-id="221c5-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="221c5-222">**Darbo užsakymo tipas:** *Ciklo skaičiavimas*</span><span class="sxs-lookup"><span data-stu-id="221c5-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="221c5-223">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="221c5-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="221c5-224">**Darbo būsena:** *Laukiama peržiūra*</span><span class="sxs-lookup"><span data-stu-id="221c5-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="221c5-225">Šioms eilutėms buvo sukurti du darbo ID.</span><span class="sxs-lookup"><span data-stu-id="221c5-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="221c5-226">Reikia priimti abiejų šių darbų ID skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="221c5-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="221c5-227">Tinklelyje pasirinkite pirmo darbo ID, skirtą *Ciklo skaičiavimas* darbo užsakymo tipui.</span><span class="sxs-lookup"><span data-stu-id="221c5-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="221c5-228">Veiksmų srityje skirtuke **Darbas**, **Bendra** grupėje, pasirinkite **Ciklo skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="221c5-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="221c5-229">Rodomos dvi eilutės, po vieną kiekvienai prekei ir numerio lentelei.</span><span class="sxs-lookup"><span data-stu-id="221c5-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="221c5-230">**Suskaičiuotas kiekis** vertės **Vieta**, **Numerio lentelė** ir **Prekė** laukų vertės turi sutapti su jūsų mobiliajame įrenginyje sukurtais skaičiavimų įrašais.</span><span class="sxs-lookup"><span data-stu-id="221c5-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="221c5-231">Jei kuris nors iš šių laukų nematomas, pasirinkite **Rodyti dimensijas** Veiksmų srityje, kad pridėtumėte į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="221c5-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="221c5-232">Pasirinkite abi eilutes.</span><span class="sxs-lookup"><span data-stu-id="221c5-232">Select both lines.</span></span>
1. <span data-ttu-id="221c5-233">Veiksmų srityje spustelėkite **Pridėti skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="221c5-234">Gaunate pranešimą „Registravimas – žurnalas”.</span><span class="sxs-lookup"><span data-stu-id="221c5-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="221c5-235">Pasirinkite **Pranešimo išsami informacija**, kad peržiūrėtumėte užregistruotą žurnalo numerį.</span><span class="sxs-lookup"><span data-stu-id="221c5-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="221c5-236">Uždarykite pranešimo išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="221c5-236">Close the message details.</span></span>
1. <span data-ttu-id="221c5-237">Atnaujinkite **Darbas** puslapį.</span><span class="sxs-lookup"><span data-stu-id="221c5-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="221c5-238">Pirmas darbo ID buvo uždarytas ir nebebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="221c5-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="221c5-239">Norėdami peržiūrėti uždarytą darbą pasirinkite **Rodyti uždarytą** žymės langelį virš tinklelio.</span><span class="sxs-lookup"><span data-stu-id="221c5-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="221c5-240">Dabar priimsite darbą, skirtą numerio lentelei, esantį *01A01R1S2B* vietoje.</span><span class="sxs-lookup"><span data-stu-id="221c5-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="221c5-241">**Apžvalga** skirtuke pasirinkite antrojo darbo ID, skirto *Ciklo skaičiavimas* darbo užsakymo tipui.</span><span class="sxs-lookup"><span data-stu-id="221c5-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="221c5-242">Veiksmų srityje skirtuke **Darbas**, **Bendra** grupėje, pasirinkite **Ciklo skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="221c5-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="221c5-243">Rodoma prekės ir numerio lentelės viena eilutė.</span><span class="sxs-lookup"><span data-stu-id="221c5-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="221c5-244">**Suskaičiuotas kiekis** vertės **Vieta**, **Numerio lentelė** ir **Prekė** laukų vertės turi sutapti su jūsų mobiliajame įrenginyje sukurtais skaičiavimų įrašais.</span><span class="sxs-lookup"><span data-stu-id="221c5-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="221c5-245">Pasirinkite eilutę.</span><span class="sxs-lookup"><span data-stu-id="221c5-245">Select the line.</span></span>
1. <span data-ttu-id="221c5-246">Veiksmų srityje spustelėkite **Pridėti skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="221c5-247">Gaunate pranešimą „Registravimas – žurnalas”.</span><span class="sxs-lookup"><span data-stu-id="221c5-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="221c5-248">Pasirinkite **Pranešimo išsami informacija**, kad peržiūrėtumėte užregistruotą žurnalo numerį.</span><span class="sxs-lookup"><span data-stu-id="221c5-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="221c5-249">Uždarykite pranešimo išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="221c5-249">Close the message details.</span></span>
1. <span data-ttu-id="221c5-250">Atnaujinkite **Darbas** puslapį.</span><span class="sxs-lookup"><span data-stu-id="221c5-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="221c5-251">Antras darbo ID buvo uždarytas ir nebebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="221c5-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="221c5-252">Norėdami peržiūrėti uždarytą darbą pasirinkite **Rodyti uždarytą** žymės langelį virš tinklelio.</span><span class="sxs-lookup"><span data-stu-id="221c5-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="221c5-253">Turimos atsargos pagal vietą</span><span class="sxs-lookup"><span data-stu-id="221c5-253">On-hand by location</span></span>

1. <span data-ttu-id="221c5-254">Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Turima pagal vietą**.</span><span class="sxs-lookup"><span data-stu-id="221c5-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="221c5-255">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="221c5-255">Set the following values:</span></span>

    - <span data-ttu-id="221c5-256">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="221c5-256">**Site:** *6*</span></span>
    - <span data-ttu-id="221c5-257">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="221c5-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="221c5-258">**Atnaujinti keliose vietose:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="221c5-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="221c5-259">Atkreipkite dėmesį, kad vieta *01A01R1S1B* turi dvi numerio lenteles:</span><span class="sxs-lookup"><span data-stu-id="221c5-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="221c5-260">**A0001**, kur **LP pozicija** laukas nustatytas į *1*</span><span class="sxs-lookup"><span data-stu-id="221c5-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="221c5-261">**A0002**, kur **LP pozicija** laukas nustatytas į *2*</span><span class="sxs-lookup"><span data-stu-id="221c5-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="221c5-262">Atkreipkite dėmesį, kad vieta *01A01R1S2B* turi vieną numerio lentelę:</span><span class="sxs-lookup"><span data-stu-id="221c5-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="221c5-263">**A0002**, kur **LP pozicija** laukas nustatytas į *1*</span><span class="sxs-lookup"><span data-stu-id="221c5-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="221c5-264">Pardavimo užsakymo scenarijus</span><span class="sxs-lookup"><span data-stu-id="221c5-264">Sales order scenario</span></span>

<span data-ttu-id="221c5-265">Dabar, kai *Vietos numerio lentelės nustatymas* funkcija nustatyta, o atsargos buvo parengtos, turite sukurti pardavimo užsakymą, kad būtų sugeneruotas paėmimo darbas, nukreipsiantis sandėlio darbuotoją paimti prekę *A0002* iš atsargų vietos, kurioje padėklo ID yra *1* pozicijoje.</span><span class="sxs-lookup"><span data-stu-id="221c5-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="221c5-266">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="221c5-267">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="221c5-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="221c5-268">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="221c5-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="221c5-269">**Kliento sąskaita:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="221c5-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="221c5-270">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="221c5-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="221c5-271">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="221c5-271">Select **OK**.</span></span>
1. <span data-ttu-id="221c5-272">Nauja eilutė pridėta į tinklelį, esantį **Pardavimo užsakymo eilutės** „FastTab”.</span><span class="sxs-lookup"><span data-stu-id="221c5-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="221c5-273">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="221c5-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="221c5-274">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="221c5-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="221c5-275">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="221c5-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="221c5-276">Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="221c5-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="221c5-277">**Rezervavimas** puslapyje, Veiksmų srityje, pasirinkite **Rezervuoti partiją**, kad užrezervuotumėte atsargas užsakymų eilutei.</span><span class="sxs-lookup"><span data-stu-id="221c5-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="221c5-278">Uždarykite **Rezervavimas** puslapį.</span><span class="sxs-lookup"><span data-stu-id="221c5-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="221c5-279">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="221c5-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="221c5-280">Gausite informacinį pranešimą, nurodantį bangos ID ir siuntos ID, sukurtus šiam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="221c5-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="221c5-281">**Pardavimo užsakymo eilutės** „FastTab” skirtuke, virš tinklelio esančiame meniu **Sandėlis**, pasirinkite **Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="221c5-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="221c5-282">**Darbas** puslapis pasirodo ir parodo pardavimų eilutei sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="221c5-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="221c5-283">Pasižymėkite rodomo darbo ID.</span><span class="sxs-lookup"><span data-stu-id="221c5-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="221c5-284">Pardavimo paėmimo scenarijus</span><span class="sxs-lookup"><span data-stu-id="221c5-284">Sales picking scenario</span></span>

1. <span data-ttu-id="221c5-285">Atverkite sandėliavimo mobiliąją programėlę ir prisijunkite prie sandėlio *61*.</span><span class="sxs-lookup"><span data-stu-id="221c5-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="221c5-286">Eikite į **Išsiųsti \> Pardavimų paėmimas**.</span><span class="sxs-lookup"><span data-stu-id="221c5-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="221c5-287">**Nuskaityti darbo ID / numerio lentelės ID** puslapyje pasirinkite **ID** lauką ir įveskite darbo ID iš pardavimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="221c5-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="221c5-288">Atkreipkite dėmesį, kad paėmimo darbas nurodo jums paimti prekę *A0002* iš vietos *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="221c5-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="221c5-289">Gaunate šią instrukciją, nes prekė *A0002* yra numerio lentelėje, esančioje *1* padėtyje toje vietoje.</span><span class="sxs-lookup"><span data-stu-id="221c5-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="221c5-290">![1 pozicijos vieta](media/LocationLicensePlatePositioning.png "1 pozicijos vieta")</span><span class="sxs-lookup"><span data-stu-id="221c5-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="221c5-291">Įveskite vietai sukurtos numerio lentelės ID, tada vadovaukitės raginimais ir pasirinkite pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="221c5-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
