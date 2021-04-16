---
title: Klasterio padėtis pilna
description: Šioje temoje pateikiama informacija apie funkciją Klasterio padėtis pilna. Ši funkcija suteikia alternatyvą griežtesniam darbo paskirstymo taisyklių vykdymui, kai naudojamas klasterio paėmimas, nes ji leidžia didesnę konteinerių ar krepšių tūrinių apribojimų paklaidos ribą.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad0f8e2fa6b3767c6b5d5549a36d52990f871531
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808851"
---
# <a name="cluster-position-full"></a><span data-ttu-id="ff532-104">Klasterio padėtis pilna</span><span class="sxs-lookup"><span data-stu-id="ff532-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff532-105">Funkcija *Klasterio padėtis pilna* suteikia alternatyvą griežtesniam darbo paskirstymo taisyklių vykdymui, kai naudojamas klasterio paėmimas, nes ji leidžia didesnę konteinerių ar krepšių tūrinių apribojimų paklaidos ribą.</span><span class="sxs-lookup"><span data-stu-id="ff532-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="ff532-106">Įprastu atveju ne visos darbo užsakymo prekės telpa į pasirinktą konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ff532-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="ff532-107">Sandėlio darbuotojai, vykdantys klasterio paėmimą, tokiu atveju turi mažai pasirinkimų: jie turi pakeisti konteinerio dydį į didesnį arba dirbti su prižiūrėtoju, kad sugalvotų kitą sprendimo būdą.</span><span class="sxs-lookup"><span data-stu-id="ff532-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="ff532-108">Ši funkcija teikia galimybę vykdyti mygtuką **Pilnas** viename iš klasterio darbo vienetų.</span><span class="sxs-lookup"><span data-stu-id="ff532-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="ff532-109">Senesnėse versijose ši parinktis buvo pasiekiama įprastų užsakymų paėmimui, o ne klasterių paėmimui.</span><span class="sxs-lookup"><span data-stu-id="ff532-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="ff532-110">Tačiau ši funkcija skiriasi nuo standartinio mygtuko **Pilnas** tuo, kad ji atšaukia likusį darbą.</span><span class="sxs-lookup"><span data-stu-id="ff532-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="ff532-111">Ji nesiūlo vartotojui įtraukti kitos dėžės į tą patį klasterį ir automatiškai nesukuria naujo darbo.</span><span class="sxs-lookup"><span data-stu-id="ff532-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="ff532-112">Funkcijos Klasterio padėtis pilna įjungimas</span><span class="sxs-lookup"><span data-stu-id="ff532-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="ff532-113">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="ff532-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ff532-114">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="ff532-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ff532-115">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="ff532-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ff532-116">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="ff532-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ff532-117">**Funkcijos pavadinimas:** *Klasterio padėtis pilna*</span><span class="sxs-lookup"><span data-stu-id="ff532-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="ff532-118">Sąranka</span><span class="sxs-lookup"><span data-stu-id="ff532-118">Setup</span></span>

<span data-ttu-id="ff532-119">Šiame skyriuje pateikiamos gairės ir pavyzdys, rodantis, kaip nustatyti ir naudoti funkciją *Klasterio padėtis pilna*.</span><span class="sxs-lookup"><span data-stu-id="ff532-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="ff532-120">Įgalinkite duomenų pavyzdį</span><span class="sxs-lookup"><span data-stu-id="ff532-120">Make sample data available</span></span>

<span data-ttu-id="ff532-121">Tam, kad dirbtumėte su [pavyzdiniu scenarijumi](#example-scenario) naudodami pavyzdinius įrašus ir vertes nurodytas čia, turite būti sistemoje, kurioje standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yra įdiegti.</span><span class="sxs-lookup"><span data-stu-id="ff532-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ff532-122">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="ff532-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="ff532-123">Taip pat galite naudoti pavyzdinį scenarijų kaip darbo su šia funkcija gamybos sistemoje instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="ff532-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="ff532-124">Tačiau tokiu atveju turite pakeisti čia aprašytus parametrus jūsų pačių reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="ff532-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="ff532-125">Klasterio šablonai</span><span class="sxs-lookup"><span data-stu-id="ff532-125">Cluster profiles</span></span>

<span data-ttu-id="ff532-126">Turite nurodyti, ar klasterių ID sugeneruojami automatiškai, kiek padėčių naudojama, kai klasteriai skaidomi, ir kaip nustatoma paėmimo darbų seka bei vykdomas jų tikrinimas.</span><span class="sxs-lookup"><span data-stu-id="ff532-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="ff532-127">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Klasterio šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="ff532-128">Sąrašo srityje pažymėkite įrašą **Kurti klasterį**.</span><span class="sxs-lookup"><span data-stu-id="ff532-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="ff532-129">„FastTab” **Bendra** patikrinkite toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ff532-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="ff532-130">**Generuoti klasterio ID:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ff532-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="ff532-131">**Aktyvinti padėtis:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ff532-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="ff532-132">**Padėčių skaičius:** *2*</span><span class="sxs-lookup"><span data-stu-id="ff532-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="ff532-133">**Padėties pavadinimas:** *Skaitinis*</span><span class="sxs-lookup"><span data-stu-id="ff532-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="ff532-134">**Skaidyti klasterį:** *Dėti*</span><span class="sxs-lookup"><span data-stu-id="ff532-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="ff532-135">**Rūšiavimo patikros tipas:** *Padėties nuskaitymas*</span><span class="sxs-lookup"><span data-stu-id="ff532-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="ff532-136">„FastTab” **Klasterio rūšiavimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="ff532-137">Tinklelis turėtų būti tuščias (t. y., jame turi nebūti jokių eilučių).</span><span class="sxs-lookup"><span data-stu-id="ff532-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="ff532-138">Darbo šablonai</span><span class="sxs-lookup"><span data-stu-id="ff532-138">Work templates</span></span>

<span data-ttu-id="ff532-139">Turite nurodyti, kaip kuriamas klasterio paėmimo darbas.</span><span class="sxs-lookup"><span data-stu-id="ff532-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="ff532-140">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ff532-141">Puslapio viršuje nustatykite lauką **Darbo užsakymo tipas** į *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="ff532-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="ff532-142">Įsitikinkite, kad išvardyti toliau pateikti demonstracinių duomenų darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="ff532-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="ff532-143">Jei jų nėra, negalėsite užbaigti scenarijaus.</span><span class="sxs-lookup"><span data-stu-id="ff532-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="ff532-144">61 SO surinkimo vieta</span><span class="sxs-lookup"><span data-stu-id="ff532-144">61 SO Stage</span></span>
    - <span data-ttu-id="ff532-145">61 SO klasterio paėmimas</span><span class="sxs-lookup"><span data-stu-id="ff532-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="ff532-146">Vietos nurodymai</span><span class="sxs-lookup"><span data-stu-id="ff532-146">Location directives</span></span>

<span data-ttu-id="ff532-147">Turite nurodyti, iš kur prekės yra paimamos ir kur jos padedamos.</span><span class="sxs-lookup"><span data-stu-id="ff532-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="ff532-148">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ff532-149">Sąrašo antraštėje nustatykite lauką **Darbo užsakymo tipas** į *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="ff532-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="ff532-150">Įsitikinkite, kad išvardytos toliau pateiktos demonstracinių duomenų pardavimų užsakymų direktyvos.</span><span class="sxs-lookup"><span data-stu-id="ff532-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="ff532-151">Jei jų nėra, negalėsite užbaigti scenarijaus.</span><span class="sxs-lookup"><span data-stu-id="ff532-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="ff532-152">61 klasterio paėmimas</span><span class="sxs-lookup"><span data-stu-id="ff532-152">61 Cluster pick</span></span>
    - <span data-ttu-id="ff532-153">61 SO paėmimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="ff532-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="ff532-154">Mobiliojo įrenginio meniu elementai</span><span class="sxs-lookup"><span data-stu-id="ff532-154">Mobile device menu items</span></span>

<span data-ttu-id="ff532-155">Turite sukonfigūruoti mobiliojo įrenginio meniu elementą, kad galėtumėte naudoti esamą darbą, kurį nukreipė klasterio paėmimas.</span><span class="sxs-lookup"><span data-stu-id="ff532-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="ff532-156">Klasterio paėmimo mobiliojo įrenginio meniu elemento parametras **Leisti darbo skaidymą** turi būti įjungtas ir turi būti įtraukta darbo klasė *SO paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="ff532-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="ff532-157">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ff532-158">Sąrašo srityje pažymėkite įrašą **Klasterio paėmimo kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="ff532-159">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ff532-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="ff532-160">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ff532-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ff532-161">**Nukreipė:** *Klasterio paėmimas*</span><span class="sxs-lookup"><span data-stu-id="ff532-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="ff532-162">**Generuoti numerio lentelę:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ff532-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="ff532-163">**Leisti darbo skaidymą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ff532-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="ff532-164">**Klasterio profilio ID:** *Kurti klasterį*</span><span class="sxs-lookup"><span data-stu-id="ff532-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="ff532-165">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="ff532-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="ff532-166">„FastTab” **Darbo klasės** įtraukite dvi toliau pateiktas eilutes, kaip nurodyta.</span><span class="sxs-lookup"><span data-stu-id="ff532-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="ff532-167">1 eilutė (dažniausiai pateikiama demonstraciniuose duomenyse):</span><span class="sxs-lookup"><span data-stu-id="ff532-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="ff532-168">**Darbo klasės ID:** *Pardavimai*</span><span class="sxs-lookup"><span data-stu-id="ff532-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="ff532-169">**Darbo užsakymo tipas:** *Pardavimų užsakymai*</span><span class="sxs-lookup"><span data-stu-id="ff532-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="ff532-170">2 eilutė (tikriausiai nepateikiama demonstraciniuose duomenyse):</span><span class="sxs-lookup"><span data-stu-id="ff532-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="ff532-171">**Darbo klasės ID:** *SO paėmimas*</span><span class="sxs-lookup"><span data-stu-id="ff532-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="ff532-172">**Darbo užsakymo tipas:** *Pardavimų užsakymai*</span><span class="sxs-lookup"><span data-stu-id="ff532-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="ff532-173">Veiksmų srityje eikite į **Darbo patvirtinimo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="ff532-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="ff532-174">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ff532-174">Select **Edit**.</span></span>
1. <span data-ttu-id="ff532-175">Tinklelio eilutėje įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ff532-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="ff532-176">**Darbo tipas** - *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="ff532-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="ff532-177">**Produkto patvirtinimas** - *Pasirinkti žymės langelį*</span><span class="sxs-lookup"><span data-stu-id="ff532-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="ff532-178">Veiksmų srityje pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ff532-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="ff532-179">Paėmimo darbo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ff532-179">Create picking work</span></span>

<span data-ttu-id="ff532-180">Prieš pradedant klasterio paėmimą, turite sukurti siuntimo darbą.</span><span class="sxs-lookup"><span data-stu-id="ff532-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="ff532-181">Anksčiau sukurtame klasterio profilyje nurodytos dvi klasterio padėtys.</span><span class="sxs-lookup"><span data-stu-id="ff532-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="ff532-182">Todėl turi būti sukurti bent du pardavimų užsakymo paėmimo darbo ID.</span><span class="sxs-lookup"><span data-stu-id="ff532-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="ff532-183">Pagal šį scenarijų operacijos įvyks *61* sandėlyje ir bus naudojamos prekės *L0101* ir *T0100*.</span><span class="sxs-lookup"><span data-stu-id="ff532-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="ff532-184">Demonstraciniuose duomenyse turi būti pakankamai šių prekių turimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="ff532-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="ff532-185">Įsitikinkite, kad turite pakankamai atsargų operacijoms atlikti.</span><span class="sxs-lookup"><span data-stu-id="ff532-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="ff532-186">1 pardavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ff532-186">Create sales order 1</span></span>

1. <span data-ttu-id="ff532-187">Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ff532-188">Norėdami sukurti 1 pardavimo užsakymą, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="ff532-189">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ff532-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ff532-190">**Kliento sąskaita:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="ff532-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="ff532-191">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="ff532-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ff532-192">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-192">Select **OK**.</span></span>
1. <span data-ttu-id="ff532-193">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ff532-193">The new sales order is opened.</span></span> <span data-ttu-id="ff532-194">**Prekybos užsakymai** „FastTab“, įtraukite eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="ff532-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="ff532-195">**Prekės numeris:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="ff532-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="ff532-196">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="ff532-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="ff532-197">„FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="ff532-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="ff532-198">„FastTab” **Pardavimo užsakymo eilutės** įtraukite antrą eilutę, kurioje yra toliau pateikti parametrai.</span><span class="sxs-lookup"><span data-stu-id="ff532-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="ff532-199">**Prekės numeris:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="ff532-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="ff532-200">**Kiekis:** *20*</span><span class="sxs-lookup"><span data-stu-id="ff532-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="ff532-201">„FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="ff532-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="ff532-202">Kiekvienai eilutei, kurią įtraukėte, atlikite toliau pateiktus veiksmus siekiant rezervuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="ff532-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="ff532-203">Pasirinkite eilutę rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="ff532-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="ff532-204">**Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="ff532-205">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="ff532-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="ff532-206">Uždarykite **Rezervavimas** puslapį.</span><span class="sxs-lookup"><span data-stu-id="ff532-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="ff532-207">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ff532-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ff532-208">Kai išleidimas bus atliktas, gausite informacinį pranešimą, kuriame bus rodomi sukurti bangos ir krovinio ID.</span><span class="sxs-lookup"><span data-stu-id="ff532-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="ff532-209">Pardavimo užsakymo 2 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="ff532-209">Create sales order 2</span></span>

1. <span data-ttu-id="ff532-210">Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ff532-211">Norėdami sukurti 2 pardavimo užsakymą, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="ff532-212">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ff532-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ff532-213">**Kliento sąskaita:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="ff532-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="ff532-214">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="ff532-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ff532-215">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-215">Select **OK**.</span></span>
1. <span data-ttu-id="ff532-216">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ff532-216">The new sales order is opened.</span></span> <span data-ttu-id="ff532-217">**Prekybos užsakymai** „FastTab“, įtraukite eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="ff532-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="ff532-218">**Prekės numeris:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="ff532-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="ff532-219">**Kiekis:** *20*</span><span class="sxs-lookup"><span data-stu-id="ff532-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="ff532-220">„FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="ff532-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="ff532-221">„FastTab” **Pardavimo užsakymo eilutės** įtraukite antrą eilutę, kurioje yra toliau pateikti parametrai.</span><span class="sxs-lookup"><span data-stu-id="ff532-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="ff532-222">**Prekės numeris:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="ff532-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="ff532-223">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="ff532-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="ff532-224">„FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="ff532-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="ff532-225">Kiekvienai eilutei, kurią įtraukėte, atlikite toliau pateiktus veiksmus siekiant rezervuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="ff532-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="ff532-226">Pasirinkite eilutę rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="ff532-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="ff532-227">**Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="ff532-228">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="ff532-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="ff532-229">Uždarykite **Rezervavimas** puslapį.</span><span class="sxs-lookup"><span data-stu-id="ff532-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="ff532-230">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ff532-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ff532-231">Kai išleidimas bus atliktas, gausite informacinį pranešimą, kuriame bus rodomi sukurti bangos ir krovinio ID.</span><span class="sxs-lookup"><span data-stu-id="ff532-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="ff532-232">Darbo ID ir numerio lentelių gavimas</span><span class="sxs-lookup"><span data-stu-id="ff532-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="ff532-233">Turėjo būti sukurti du darbo ID, kurių kiekviename yra dvi paėmimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="ff532-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="ff532-234">Norėdami rasti darbo ID ir numerio lenteles, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ff532-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="ff532-235">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="ff532-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ff532-236">Tinklelyje **Apžvalga** ieškokite dviejų pardavimo užsakymų, kuriuos sukūrėte, stulpelio **Užsakymo numeris**.</span><span class="sxs-lookup"><span data-stu-id="ff532-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="ff532-237">Pasižymėkite kiekvieno pardavimo užsakymo atitinkamą darbo ID.</span><span class="sxs-lookup"><span data-stu-id="ff532-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="ff532-238">Pasirinkite kiekvieno pardavimo užsakymo eilutę, kad tinklelyje **Eilutės** būtų rodoma susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="ff532-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="ff532-239">Pasižymėkite kiekvienos prekės vietą, kur ji bus paimta.</span><span class="sxs-lookup"><span data-stu-id="ff532-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="ff532-240">Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="ff532-241">Veiksmų srityje pasirinkite **Dimensijos**, kad būtų atidarytas dialogo langas **Dimensijų rodymas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="ff532-242">Patikrinkite, ar pažymėti žymės langeliai **Numerio lentelė**, **Sandėlis** ir **Prekės numeris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ff532-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="ff532-243">Srityje **Filtras**, nustatykite toliau nurodytus filtrus.</span><span class="sxs-lookup"><span data-stu-id="ff532-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="ff532-244">**Prekės numeris** – **vienas iš dviejų** – *L0101* arba *T100*</span><span class="sxs-lookup"><span data-stu-id="ff532-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="ff532-245">**Sandėlis** – **prasideda** – *61*</span><span class="sxs-lookup"><span data-stu-id="ff532-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="ff532-246">Pasižymėkite rodomas **numerio lentelės** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ff532-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="ff532-247">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="ff532-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="ff532-248">Mobiliojo įrenginio srauto vykdymas – produkto darbo patvirtinimo sąranka</span><span class="sxs-lookup"><span data-stu-id="ff532-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="ff532-249">Prisijunkite prie sandėlio mobiliųjų įrenginių programėlė kaip vartotojas sandėlyje *61*.</span><span class="sxs-lookup"><span data-stu-id="ff532-249">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="ff532-250">Eikite į **Siuntimas \> Klasterio paėmimo kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="ff532-251">Atidaromas puslapis **UŽDUOTIS. Darbo priskyrimas klasteriui**.</span><span class="sxs-lookup"><span data-stu-id="ff532-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="ff532-252">Įveskite 1 pardavimo užsakymo ID, kad priskirtumėte jį 1 klasterio padėčiai.</span><span class="sxs-lookup"><span data-stu-id="ff532-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="ff532-253">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-254">Įveskite 2 pardavimo užsakymo ID, kad priskirtumėte jį 2 klasterio padėčiai.</span><span class="sxs-lookup"><span data-stu-id="ff532-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="ff532-255">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="ff532-256">Atidaromas puslapis **UŽDUOTIS. Klasterio paėmimo kūrimas. Paėmimas** ir rodoma *Prekė L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="ff532-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="ff532-257">Kadangi klasterio profilyje padėčių skaičius nustatytas į 2, sistema automatiškai nukreipia į pirmą konsoliduotąjį paėmimą: du prekės *L0101* padėklai (PL).</span><span class="sxs-lookup"><span data-stu-id="ff532-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="ff532-258">Bet kuriuo toliau pateiktų veiksmų metu galite pasirinkti skirtuką **Išsami informacija**, norėdami peržiūrėti informaciją apie užduotį, pvz., paėmimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ff532-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="ff532-259">Nustatykite lauką **PREKĖ** į *L0101*.</span><span class="sxs-lookup"><span data-stu-id="ff532-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="ff532-260">Tai patvirtina prekės numerį, reikalingą šiam meniu elementui (tai sukonfigūravote anksčiau, pasirinkę **Darbo patvirtinimo sąranka** puslapyje **Mobiliojo įrenginio meniu elementas**, kurdami šį meniu elementą).</span><span class="sxs-lookup"><span data-stu-id="ff532-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="ff532-261">Įveskite numerio lentelės numerį, susietą su preke, jos paėmimo vietoje.</span><span class="sxs-lookup"><span data-stu-id="ff532-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="ff532-262">Pasiimsite du padėklus.</span><span class="sxs-lookup"><span data-stu-id="ff532-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="ff532-263">Nustatykite lauką **LP** į *LP\_PAĖMIMAS\_01*.</span><span class="sxs-lookup"><span data-stu-id="ff532-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="ff532-264">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="ff532-265">Atidaromas puslapis **UŽDUOTIS. Rūšiavimas. Klasterio paėmimo kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="ff532-266">Jame rūšiuosite du paimamus padėklus į paėmimo padėtį.</span><span class="sxs-lookup"><span data-stu-id="ff532-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="ff532-267">Ši padėtis gali būti krepšys ar konteineris, naudojamas atskirti paimamas atsargas pagal pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ff532-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="ff532-268">Peržiūrėkite rodomą prekės (*L0101*) ir kiekio (*20* vnt.) išsamią informaciją, kuri bus rūšiuojama į 1 padėtį (1 pardavimo užsakymo).</span><span class="sxs-lookup"><span data-stu-id="ff532-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="ff532-269">Nustatykite lauką **PADĖTIES PAVADINIMAS** į *1*.</span><span class="sxs-lookup"><span data-stu-id="ff532-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="ff532-270">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-271">Peržiūrėkite rodomą prekės (*L0101*) ir kiekio (*20* vnt.) išsamią informaciją, kuri bus rūšiuojama į 2 padėtį (2 pardavimo užsakymo).</span><span class="sxs-lookup"><span data-stu-id="ff532-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="ff532-272">Nustatykite lauką **PADĖTIES PAVADINIMAS** į *2*.</span><span class="sxs-lookup"><span data-stu-id="ff532-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="ff532-273">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="ff532-274">Atidaromas puslapis **UŽDUOTIS. Klasterio paėmimo kūrimas. Paėmimas** ir rodoma *Prekė T0100 7 vnt*.</span><span class="sxs-lookup"><span data-stu-id="ff532-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="ff532-275">Pagal šį scenarijų 1 padėtis negali priimti viso prekių, kurias reikia paimti siekiant atlikti 1 pardavimo užsakymą, kiekio.</span><span class="sxs-lookup"><span data-stu-id="ff532-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="ff532-276">Padėtis turi būti pažymėta kaip pilna.</span><span class="sxs-lookup"><span data-stu-id="ff532-276">A position must be marked as full.</span></span> <span data-ttu-id="ff532-277">Pagal šį scenarijų atliksite antros prekės paėmimą dalimis.</span><span class="sxs-lookup"><span data-stu-id="ff532-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="ff532-278">Antra prekė bus paimta dalimis pagal 1 padėtį ir bus sukurtas naujas darbas, kad būtų paimtas likęs kiekis ir atliktas užsakymas.</span><span class="sxs-lookup"><span data-stu-id="ff532-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="ff532-279">Pasirinkite mygtuką Meniu (kartais vadinamą mėsainiu arba mėsainio mygtuku) ir tada pasirinkite **Padėtis pilna**.</span><span class="sxs-lookup"><span data-stu-id="ff532-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="ff532-280">Nurodykite pilną padėtį ir pasirinkite *1*.</span><span class="sxs-lookup"><span data-stu-id="ff532-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="ff532-281">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-282">Įveskite paėmimo kiekį, kurį galima paimti su 1 padėtimi.</span><span class="sxs-lookup"><span data-stu-id="ff532-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="ff532-283">Sistema gali nustatyti, kuris prekės numeris paimamas.</span><span class="sxs-lookup"><span data-stu-id="ff532-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="ff532-284">Įveskite *2*.</span><span class="sxs-lookup"><span data-stu-id="ff532-284">Enter *2*.</span></span>
1. <span data-ttu-id="ff532-285">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-286">Patvirtinkite prekės numerį, kad užbaigtumėte likusios prekės paėmimą su 2 padėtimi.</span><span class="sxs-lookup"><span data-stu-id="ff532-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="ff532-287">Nustatykite lauką **PREKĖ** į *T0100*.</span><span class="sxs-lookup"><span data-stu-id="ff532-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="ff532-288">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-289">Įveskite numerio lentelę, iš kur prekė paimama, nustatydami lauką **LP** į *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="ff532-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="ff532-290">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-291">Peržiūrėkite rodomą prekės (*T0100*) ir kiekio (*2* vnt.) išsamią informaciją, kuri bus rūšiuojama į 2 padėtį (2 pardavimo užsakymo).</span><span class="sxs-lookup"><span data-stu-id="ff532-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="ff532-292">Nustatykite lauką **PADĖTIES PAVADINIMAS** į *2*.</span><span class="sxs-lookup"><span data-stu-id="ff532-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="ff532-293">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="ff532-294">Peržiūrėkite rodomą prekės (*T0100*) ir kiekio (*2* vnt.) išsamią informaciją, kuri bus rūšiuojama į 1 padėtį (1 pardavimo užsakymo).</span><span class="sxs-lookup"><span data-stu-id="ff532-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="ff532-295">Nustatykite lauką **PADĖTIES PAVADINIMAS** į *1*.</span><span class="sxs-lookup"><span data-stu-id="ff532-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="ff532-296">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="ff532-297">Atidaromas puslapis **UŽDUOTIS. Klasterio paėmimo kūrimas. Padėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ff532-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="ff532-298">Pagal šį scenarijų klasterio paėmimas užbaigiamas ir vartotojas nukreipiamas padėti paimamas 1 padėties ir 2 padėties prekes į surinkimo vietą *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="ff532-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="ff532-299">Peržiūrėkite puslapio informaciją.</span><span class="sxs-lookup"><span data-stu-id="ff532-299">Review the information on the page.</span></span> <span data-ttu-id="ff532-300">Rodoma, kad bendras kiekis, kuris yra *44*, bus padėtas į surinkimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ff532-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="ff532-301">Pasirinkite **Gerai** (varnelės simbolis).</span><span class="sxs-lookup"><span data-stu-id="ff532-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="ff532-302">Bus pateiktas pranešimas „Klasteris užbaigtas”.</span><span class="sxs-lookup"><span data-stu-id="ff532-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="ff532-303">Dabar galite naudoti meniu elementą **Pardavimo paėmimas**, norėdami paimti likusį kiekį.</span><span class="sxs-lookup"><span data-stu-id="ff532-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="ff532-304">Tada galite naudoti meniu elementą **Pardavimo krovimas**, norėdami perkelti prekes iš surinkimo vietos į krovimo rampą.</span><span class="sxs-lookup"><span data-stu-id="ff532-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]