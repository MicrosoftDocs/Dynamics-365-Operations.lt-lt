---
title: Elemento konsolidavimas - vietos naudojimas
description: Šiame temoje pateikta informacija apie funkcijas, kurios palengvina sandėlio vadovų vietų kiekio naudojimo peržiūrą ir filtravimą sandėlyje. Vadovai gali pasirinkti vietas ir sukurti inventoriaus judėjimo darbą tiesiai iš elemento konsolidavimo puslapio į konsoliduotus elementus ir taip pagerinti sandėlio vietos naudojimą.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004657"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="2e739-104">Elemento konsolidavimas - vietos naudojimas</span><span class="sxs-lookup"><span data-stu-id="2e739-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e739-105">Šiame temoje pateikta informacija apie funkcijas, kurios palengvina sandėlio vadovų vietų kiekio naudojimo peržiūrą ir filtravimą sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="2e739-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="2e739-106">Vadovai gali pasirinkti vietas ir sukurti inventoriaus judėjimo darbą tiesiai iš elemento **Elemento konsolidavimo** puslapio į konsoliduotus elementus ir taip pagerinti sandėlio vietos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="2e739-107">Savybių įjungimas</span><span class="sxs-lookup"><span data-stu-id="2e739-107">Turn on the features</span></span>

<span data-ttu-id="2e739-108">Prieš pradedant naudoti šiame skyriuje aprašytas savybes, privalote įjungti jas savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="2e739-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="2e739-109">Administratoriai gali naudoti [Savybių valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje tam, kad patikrintų savybių būseną ir jas įjungtų, jei jos būtinos.</span><span class="sxs-lookup"><span data-stu-id="2e739-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="2e739-110">Įjunkite toliau pateiktas savybes jų išvardijimo tvarka.</span><span class="sxs-lookup"><span data-stu-id="2e739-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="2e739-111">(Abi savybės yra skirtos **Sandėlio valdymo** moduliui.)</span><span class="sxs-lookup"><span data-stu-id="2e739-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="2e739-112">Sandėlio vietos būsena</span><span class="sxs-lookup"><span data-stu-id="2e739-112">Warehouse location status</span></span>
2. <span data-ttu-id="2e739-113">Prekės konsolidacijos vietos naudojimas</span><span class="sxs-lookup"><span data-stu-id="2e739-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="2e739-114">Sandėlio vietos būsena</span><span class="sxs-lookup"><span data-stu-id="2e739-114">Warehouse location status</span></span>

<span data-ttu-id="2e739-115">*Sandėlio vietos būsenos* savybė įtraukia keturis naujus laukelius į **Vietos** puslapį tam, kad būtų sekama papildoma informacija apie esamą vietos būseną:</span><span class="sxs-lookup"><span data-stu-id="2e739-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="2e739-116">**Prekės numeris** – Prekė, kuri šiuo metu yra vietoje.</span><span class="sxs-lookup"><span data-stu-id="2e739-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="2e739-117">Jei vieta turi keletą elementų, šis laukelis bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="2e739-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="2e739-118">**Paskutinė veiklos data ir laikas** – Paskutinės sandėlio operacijos, atliktos su vieta, laiko žyma.</span><span class="sxs-lookup"><span data-stu-id="2e739-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="2e739-119">**Skirstymo pagal terminus data** – Vietos atsargų įvežimo į sandėlį data.</span><span class="sxs-lookup"><span data-stu-id="2e739-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="2e739-120">Šie duomenys apskaičiuojami pagal licencijos numerio amžiaus duomenis.</span><span class="sxs-lookup"><span data-stu-id="2e739-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="2e739-121">Nepaisant to, kad šie duomenys yra tikslųs licencijos numerio sekimo vietoms, jie gali būti netikslūs vietoms, kurių licencijos numeris neseka.</span><span class="sxs-lookup"><span data-stu-id="2e739-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="2e739-122">**Vietos būsena** – Vietos būsena.</span><span class="sxs-lookup"><span data-stu-id="2e739-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="2e739-123">Dėl prieinamų verčių:</span><span class="sxs-lookup"><span data-stu-id="2e739-123">Four values are available:</span></span>

    - <span data-ttu-id="2e739-124">**Nenustatyta** – Vietos profilis neseka būsenos.</span><span class="sxs-lookup"><span data-stu-id="2e739-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="2e739-125">Todėl dabartinė būsena yra nežinoma.</span><span class="sxs-lookup"><span data-stu-id="2e739-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="2e739-126">**Tuščia** – Vietoje šiuo metu nėra jokio inventoriaus.</span><span class="sxs-lookup"><span data-stu-id="2e739-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="2e739-127">**Paėmimas** – Siunčiami pervedimai buvo pradėti pagal vietą, kuri galiausiai buvo tuščia.</span><span class="sxs-lookup"><span data-stu-id="2e739-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="2e739-128">**Laikymas** – Tik įeinantys pervedimai buvo atlikti, nes vieta buvo tuščia.</span><span class="sxs-lookup"><span data-stu-id="2e739-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="2e739-129">Šie laukeliai leidžia sandėlio vadovams geriau matyti vietų sandėlyje būseną.</span><span class="sxs-lookup"><span data-stu-id="2e739-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="2e739-130">Jie taip pat leidžia pateikti geresnes ataskaitas ir pritaikyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="2e739-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="2e739-131">Nustatyto elemento konsolidavimas ir vietos naudojimas</span><span class="sxs-lookup"><span data-stu-id="2e739-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="2e739-132">Šis skyrius aprašo instrukcijas, kaip parengti sistemą, kuri naudoja konsoliduotą elementą ir vietos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="2e739-133">Procedūros naudoja paprastas vertes iš standartinių demonstracijos duomenų.</span><span class="sxs-lookup"><span data-stu-id="2e739-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="2e739-134">Jei planuojate dirbti per visą pavyzdžio scenarijų, kuris pateiktas tolesėje temoje, pasirinkite **USMF** juridinį subjektą (kuriame yra standartiniai demonstracijos duomenys) ir sukurkite visus įrašus aprašytus šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="2e739-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="2e739-135">Jei neplanuojate dirbti su visu pavyzdiniu scenarijumi, čia pateiktos vertės gali būti laikomos nustatymų tipų pavyzdžiais, kuriuos privalote pabaigti tam, kad naudotumėte savybes.</span><span class="sxs-lookup"><span data-stu-id="2e739-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="2e739-136">Patvirtintas produktas</span><span class="sxs-lookup"><span data-stu-id="2e739-136">Released product</span></span>

1. <span data-ttu-id="2e739-137">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="2e739-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2e739-138">**Elemento skaičiaus** laukelyje, pasirinkite *M9201* ir atidarykite informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="2e739-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="2e739-139">Veiksmų juostoje, **Inventoriaus valdymo** skirtuke, **Sandėlio** grupėje, pasirinkite **Fiziniai matmenys**.</span><span class="sxs-lookup"><span data-stu-id="2e739-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="2e739-140">**Fiziniai matmenys** lange, veiksmų juostoje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2e739-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="2e739-141">Nauja eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="2e739-141">A new line is added to the grid.</span></span> <span data-ttu-id="2e739-142">**Elemento skaičiaus** laukelis nustatomas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="2e739-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="2e739-143">**Padalinio** laukelyje pasirinkite *ea*.</span><span class="sxs-lookup"><span data-stu-id="2e739-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="2e739-144">Likę laukeliai linijoje yra nustatomi automatiškai.</span><span class="sxs-lookup"><span data-stu-id="2e739-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="2e739-145">Pasirinkite **Išsaugoti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2e739-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="2e739-146">Vietos profilis</span><span class="sxs-lookup"><span data-stu-id="2e739-146">Location profile</span></span>

1. <span data-ttu-id="2e739-147">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="2e739-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="2e739-148">Vietų profilių sąraše, pasirinkite **FLOOR-05**.</span><span class="sxs-lookup"><span data-stu-id="2e739-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="2e739-149">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2e739-150">**Bendri** „FastTab“, įsitikinkite, kad abi toliau pateiktos parinktys yra nustatytos į *Taip*:</span><span class="sxs-lookup"><span data-stu-id="2e739-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="2e739-151">Įgalinti prekę vietoje</span><span class="sxs-lookup"><span data-stu-id="2e739-151">Enable item in location</span></span>
    - <span data-ttu-id="2e739-152">Įgalinti vietos būseną</span><span class="sxs-lookup"><span data-stu-id="2e739-152">Enable location status</span></span>

1. <span data-ttu-id="2e739-153">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2e739-154">Jei **Įjungti elementą vietoje** ir **Įjungti vietos būseną** parinktys jau buvo nustatytos į *Taip*, praleiskite laukiančias instrukcijas **Matmenų** nustatymui „FastTab“ 10 žingsnyje.</span><span class="sxs-lookup"><span data-stu-id="2e739-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="2e739-155">Jei parinktys dar nėra nustatytos į *Taip*, turite vykdyti nuolatinį **Sandėlio valdymo** modulio tikrinimą po rankinio jų nustatymo.</span><span class="sxs-lookup"><span data-stu-id="2e739-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="2e739-156">Šiuo atveju, atlikite kitą žingsnį.</span><span class="sxs-lookup"><span data-stu-id="2e739-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="2e739-157">Nuolatinio tikrinimo vykdymui, eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenš bazę \> Periodinis tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="2e739-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="2e739-158">**Nuolatinio tikrinimo** teksto laukelyje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="2e739-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2e739-159">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="2e739-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="2e739-160">**Tikrinti/Taisyti** *Tikrinti*</span><span class="sxs-lookup"><span data-stu-id="2e739-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="2e739-161">**Nuo datos:** Palikite šį laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="2e739-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="2e739-162">**Sandėlio vietos būsenos nuolatinis tikrinimas:** Pasirinkite šį žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="2e739-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="2e739-163">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2e739-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="2e739-164">Kai nuolatinis tikrinimas yra užbaigtas, gausite pranešimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="2e739-165">Atidarykite [Veiksmų centrą](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) žinutės peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="2e739-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="2e739-166">Pasirinkite **Žinutės informacija** informacijos peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="2e739-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="2e739-167">Jei žinutė dėl nuolatinio tikrinimo sako „Netinkamas vietos būsenos informacija rasta XXXX vietai XX sandėlyje“, privalote vykdyti nuolatinį tikrinimą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="2e739-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="2e739-168">Šįkart, nustatykite **Tikrinti/Taisyti** laukelį į *Taisyti klaidą*.</span><span class="sxs-lookup"><span data-stu-id="2e739-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="2e739-169">Peržiūrėkite žinutes, kad įsitikintumėte, jog nebuvo rasta jokių klaidų.</span><span class="sxs-lookup"><span data-stu-id="2e739-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="2e739-170">Dabar galite užbaigti profilio vietos nustatymą.</span><span class="sxs-lookup"><span data-stu-id="2e739-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="2e739-171">Eikite atgal į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Vietos profiliai**, pasirinkite vietos profilį **FLOOR-05** ir tuomet veiksmų juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2e739-172">**Matmenys** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="2e739-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2e739-173">**Tūrio panaudojimo procentas:** *100*</span><span class="sxs-lookup"><span data-stu-id="2e739-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="2e739-174">**Tūrio matavimo metodas naudojamas inventoriaus vietoms:** *Naudoti vietos tūrį*</span><span class="sxs-lookup"><span data-stu-id="2e739-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="2e739-175">**Esamas vietos aukštis:** *10*</span><span class="sxs-lookup"><span data-stu-id="2e739-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="2e739-176">**Esamas vietos plotis:** *10*</span><span class="sxs-lookup"><span data-stu-id="2e739-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="2e739-177">**Esamas vietos gylis:** *10*</span><span class="sxs-lookup"><span data-stu-id="2e739-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="2e739-178">**Maksimalus svoris:** *100*</span><span class="sxs-lookup"><span data-stu-id="2e739-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="2e739-179">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="2e739-180">Mobiliojo įrenginio meniu elementai</span><span class="sxs-lookup"><span data-stu-id="2e739-180">Mobile device menu items</span></span>

1. <span data-ttu-id="2e739-181">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="2e739-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2e739-182">Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte meniu elementą rūšiavimui.</span><span class="sxs-lookup"><span data-stu-id="2e739-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="2e739-183">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="2e739-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="2e739-184">**Meniu elemento pavadinimas:** *Reguliuoti viduje*</span><span class="sxs-lookup"><span data-stu-id="2e739-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="2e739-185">**Pavadinimas:** *Reguliuoti viduje*</span><span class="sxs-lookup"><span data-stu-id="2e739-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="2e739-186">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="2e739-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="2e739-187">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="2e739-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="2e739-188">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="2e739-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2e739-189">**Darbo kūrimo procesas:** *Reguliavimas viduje*</span><span class="sxs-lookup"><span data-stu-id="2e739-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="2e739-190">**Inventoriaus reguliavimo tipai:** *Reguliuoti viduje*</span><span class="sxs-lookup"><span data-stu-id="2e739-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="2e739-191">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="2e739-192">Mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="2e739-192">Mobile device menu</span></span>

1. <span data-ttu-id="2e739-193">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="2e739-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="2e739-194">Meniu sąraše pasirinkite **Inventorius**.</span><span class="sxs-lookup"><span data-stu-id="2e739-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="2e739-195">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2e739-196">**Esančiuose meniu ir meniu elementų** sąraše suraskite ir pasirinkite **Reguliavimas viduje** meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="2e739-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="2e739-197">Pasirinkite dešinės rodyklės mygtuką **Reguliavimas viduje** perkėlimui į **Meniu struktūros** sąrašą.</span><span class="sxs-lookup"><span data-stu-id="2e739-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="2e739-198">Šiuo būdu, galėsite įtraukite naują meniu elementą į pasirinktą meniu.</span><span class="sxs-lookup"><span data-stu-id="2e739-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="2e739-199">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="2e739-200">Perkėlimo tipai</span><span class="sxs-lookup"><span data-stu-id="2e739-200">Movement types</span></span>

1. <span data-ttu-id="2e739-201">Eikite į **Sandėlio tvarkymas \> Sąranka \> Inventorius \> Judėjimo tipai**.</span><span class="sxs-lookup"><span data-stu-id="2e739-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="2e739-202">Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="2e739-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2e739-203">**Judėjimo tipo kodas:** *KONSOLIDUOTI*</span><span class="sxs-lookup"><span data-stu-id="2e739-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="2e739-204">**Aprašas:** *Konsoliduoti vietas*</span><span class="sxs-lookup"><span data-stu-id="2e739-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="2e739-205">**Darbo klasės identifikavimo numeris:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="2e739-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="2e739-206">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e739-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2e739-207">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="2e739-207">Example scenario</span></span>

<span data-ttu-id="2e739-208">Tolesnis scenarijus naudoja sandėlio programą mobiliame prietaise tam, kad sukurtų inventorių *reguliavimą viduje* dvejose sandėlio vietose.</span><span class="sxs-lookup"><span data-stu-id="2e739-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="2e739-209">Įtraukti inventorių į vietas</span><span class="sxs-lookup"><span data-stu-id="2e739-209">Add inventory to locations</span></span>

1. <span data-ttu-id="2e739-210">Prisijunkite prie mobilaus prietaiso kaip vartotojas nustatytas sandėliui *51*.</span><span class="sxs-lookup"><span data-stu-id="2e739-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="2e739-211">Eikite į **Inventorius \> Reguliavimas viduje**.</span><span class="sxs-lookup"><span data-stu-id="2e739-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="2e739-212">Dabar įvesite pirmą vietos reguliavimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="2e739-213">**Reguliavimas viduje** užduotyje, pasirinkite vietą tam, kad sukurtumėte inventoriaus reguliavimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="2e739-214">**LOC** laukelyje pasirinkite *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="2e739-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="2e739-215">Patvirtinkite vietą.</span><span class="sxs-lookup"><span data-stu-id="2e739-215">Confirm the location.</span></span>
1. <span data-ttu-id="2e739-216">Sukurkite licencijos numerio identifikavimo kodą elementui, kuris bus įtrauktas į vietą.</span><span class="sxs-lookup"><span data-stu-id="2e739-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="2e739-217">**LP** laukelyje įveskite *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="2e739-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="2e739-218">Patvirtinkte licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="2e739-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="2e739-219">Įveskite elementą, kuris bus įtrauktas į licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="2e739-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="2e739-220">**ITEM** lauke įveskite *M9201*.</span><span class="sxs-lookup"><span data-stu-id="2e739-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="2e739-221">Patvirtinkite elementą.</span><span class="sxs-lookup"><span data-stu-id="2e739-221">Confirm the item.</span></span>
1. <span data-ttu-id="2e739-222">Įveskite elemento kiekį, kuris bus įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="2e739-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="2e739-223">**QTY** laukelyje įveskite *10*.</span><span class="sxs-lookup"><span data-stu-id="2e739-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="2e739-224">Patvirtinkite kiekį.</span><span class="sxs-lookup"><span data-stu-id="2e739-224">Confirm the quantity.</span></span>

    <span data-ttu-id="2e739-225">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="2e739-226">Dabar įveskite antrą vietos reguliavimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="2e739-227">**Reguliavimas viduje** užduotyje, pasirinkite vietą tam, kad sukurtumėte inventoriaus reguliavimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="2e739-228">**LOC** laukelyje pasirinkite *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="2e739-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="2e739-229">Patvirtinkite vietą.</span><span class="sxs-lookup"><span data-stu-id="2e739-229">Confirm the location.</span></span>
1. <span data-ttu-id="2e739-230">Sukurkite licencijos numerio identifikavimo kodą elementui, kuris bus įtrauktas į vietą.</span><span class="sxs-lookup"><span data-stu-id="2e739-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="2e739-231">**LP** laukelyje įveskite *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="2e739-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="2e739-232">Patvirtinkte licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="2e739-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="2e739-233">Įveskite elementą, kuris bus įtrauktas į licencijos numerį.</span><span class="sxs-lookup"><span data-stu-id="2e739-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="2e739-234">**ITEM** lauke įveskite *M9201*.</span><span class="sxs-lookup"><span data-stu-id="2e739-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="2e739-235">Patvirtinkite elementą.</span><span class="sxs-lookup"><span data-stu-id="2e739-235">Confirm the item.</span></span>
1. <span data-ttu-id="2e739-236">Įveskite elemento kiekį, kuris bus įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="2e739-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="2e739-237">**QTY** laukelyje įveskite *15*.</span><span class="sxs-lookup"><span data-stu-id="2e739-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="2e739-238">Patvirtinkite kiekį.</span><span class="sxs-lookup"><span data-stu-id="2e739-238">Confirm the quantity.</span></span>

    <span data-ttu-id="2e739-239">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2e739-240">Pasirinkite meniu mygtuką (kartais vadinamas mėsainiu ar mėsainio mygtuku) ir tuomet pasirinkite **Atšaukit** tam, kad išeitumėte iš **Rguliavimo viduje** užduoties.</span><span class="sxs-lookup"><span data-stu-id="2e739-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="2e739-241">Vietų konsolidavimas</span><span class="sxs-lookup"><span data-stu-id="2e739-241">Consolidate locations</span></span>

1. <span data-ttu-id="2e739-242">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Elemento konsolidavimas**.</span><span class="sxs-lookup"><span data-stu-id="2e739-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="2e739-243">Antraštėje pasirinkite sandėlė, kuriame atliksite konsolidavimą.</span><span class="sxs-lookup"><span data-stu-id="2e739-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="2e739-244">**Sandėlio** laukelyje įveskite *51*.</span><span class="sxs-lookup"><span data-stu-id="2e739-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="2e739-245">Įrašas rodomas visose vietose, kuriose elementas *M9201* buvo reguliuotas.</span><span class="sxs-lookup"><span data-stu-id="2e739-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="2e739-246">**Utilizavimo procento** stulpelis rodo naudojamą tūrį visose vietose.</span><span class="sxs-lookup"><span data-stu-id="2e739-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="2e739-247">Inventoriaus konsilidavimui, pasirinkite visas konsoliduoti būtinas vietas ir tuomet veiksmų juostoje pasirinkite **Konsoliduoti inventorių**.</span><span class="sxs-lookup"><span data-stu-id="2e739-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="2e739-248">**Konsoliduoti inventorių** teksto laukelyje nurodykite vietą ir judėjimo tipą, kuris turi būti naudojamas inventoriaus judėjimo darbo sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="2e739-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="2e739-249">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="2e739-249">Set the following values:</span></span>

    - <span data-ttu-id="2e739-250">**Vieta:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="2e739-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="2e739-251">**Judėjimo tipo kodas:** *KONSOLIDUOTI*</span><span class="sxs-lookup"><span data-stu-id="2e739-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="2e739-252">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2e739-252">Select **OK**.</span></span>
1. <span data-ttu-id="2e739-253">Gausite informacinį pranešimą, kuriame bus rodomas sukurto darbo judėjimas.</span><span class="sxs-lookup"><span data-stu-id="2e739-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="2e739-254">Užsirašykite darbo judėjimo identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="2e739-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="2e739-255">Darbo judėjimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="2e739-255">View movement work</span></span>

1. <span data-ttu-id="2e739-256">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="2e739-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="2e739-257">Peržiūrėkite sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="2e739-257">View the work that was created.</span></span> <span data-ttu-id="2e739-258">Naudokite darbo identifikavimo kodą inventoriaus konsolidavimo filtravimui ar paieškai darbo tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="2e739-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="2e739-259">Šiame scenarijuje, esama vieta turėjusi inventorių buvo naudojama kaip inventoriaus konsolidavimo vieta.</span><span class="sxs-lookup"><span data-stu-id="2e739-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="2e739-260">Dėl to, buvo sukurtas tik vienas dabo identifikavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="2e739-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="2e739-261">Sistema sukuria vieną darbo identifikavimo kodą vienam judėjimui, kuris turi būti atliktas.</span><span class="sxs-lookup"><span data-stu-id="2e739-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="2e739-262">Jei nurodote vietą, kuri jau turi inventorių, yra sukuriamas tik vienas darbo identifikavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="2e739-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="2e739-263">Jei nurodote naują vietą, bus sukuriami du darbo identifikavimo kodai.</span><span class="sxs-lookup"><span data-stu-id="2e739-263">If you specify a new location, two work IDs are created.</span></span>
