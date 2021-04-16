---
title: Bangos šablonų grupavimas
description: Bangos šablonų grupavimas leidžia sistemai naudoti bangos šablono nustatymus, kad remiantis Jūsų nustatytais kriterijais, būtų galima nuspręsti, kaip jis turi išskaidyti išleistas eilutes ir priskirti jas naujai ar esamai bangai. Ši funkcija gali būti naudinga tuose sandėliuose, kuriuose bangos kuriamos pagal tam tikrus kriterijus, bet valdytojai nori sukurti bangas automatiniu, o ne rankiniu būdu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a591624f6611148abe4888e67d8d3a9bbea9cd27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838039"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="b93b9-104">Bangos šablonų grupavimas</span><span class="sxs-lookup"><span data-stu-id="b93b9-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b93b9-105">Bangos šablonų grupavimas leidžia sistemai naudoti [bangos šablono](tasks/configure-wave-processing.md) nustatymus, kad remiantis Jūsų nustatytais kriterijais, būtų galima nuspręsti, kaip jis turi išskaidyti išleistas eilutes ir priskirti jas naujai ar esamai bangai.</span><span class="sxs-lookup"><span data-stu-id="b93b9-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="b93b9-106">Ši funkcija gali būti naudinga tuose sandėliuose, kuriuose bangos kuriamos pagal tam tikrus kriterijus, bet valdytojai nori sukurti bangas automatiniu, o ne rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="b93b9-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="b93b9-107">Tai leidžia sistemai pridėti kiekvieną naujai išleistą siuntą į pirmąją bangą, kuri suranda sutampančias grupavimo laukų vertes.</span><span class="sxs-lookup"><span data-stu-id="b93b9-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="b93b9-108">Jei atitiktis nerandama, sistema naujai siuntai sukuria naują bangą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b93b9-109">Bangos šablonų grupavimo nepalaikomo darbo tipai *Gamybos žaliavų paėmimas* ar " *„Kanban“ paėmimas*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="b93b9-110">Taip yra, nes bangos grupavimo pagrindas yra siuntos, o šie darbo tipai nenaudoja siuntų.</span><span class="sxs-lookup"><span data-stu-id="b93b9-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="b93b9-111">Bangos šablonų grupavimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="b93b9-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="b93b9-112">Norėdami naudoti *Bangos šablonų grupavimo* funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b93b9-113">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="b93b9-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b93b9-114">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="b93b9-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b93b9-115">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="b93b9-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b93b9-116">**Funkcijos pavadinimas:** *Bangos šablonų grupavimas*</span><span class="sxs-lookup"><span data-stu-id="b93b9-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="b93b9-117">Nustatyti bangos šabloną, kad būtų galima naudoti bangos šablono grupavimą</span><span class="sxs-lookup"><span data-stu-id="b93b9-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="b93b9-118">Norėdami, kad būtų galima naudoti bangos šablono grupavimą, atlikite šiuos veiksmus nustatyti [bangos šablonui](tasks/configure-wave-processing.md).</span><span class="sxs-lookup"><span data-stu-id="b93b9-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="b93b9-119">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b93b9-120">Kairiojoje srityje pasirinkite nustatomą bangos šabloną.</span><span class="sxs-lookup"><span data-stu-id="b93b9-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="b93b9-121">Jei ruošiatės dirbti pagal scenarijų, toliau pateiktą šioje temoje naudojant demonstracinius duomenis, pasirinkite **62 pristatymo numatytąjį** šabloną.</span><span class="sxs-lookup"><span data-stu-id="b93b9-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="b93b9-122">Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.</span><span class="sxs-lookup"><span data-stu-id="b93b9-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="b93b9-123">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b93b9-124">**Automatizuoti bangos kūrimą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="b93b9-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="b93b9-125">**Priskirti atviroms bangoms:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="b93b9-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="b93b9-126">**Apdoroti bangą išleidžiant ją į sandėlį** *Ne*</span><span class="sxs-lookup"><span data-stu-id="b93b9-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="b93b9-127">Veiksmų srityje pasirinkite **Redaguoti užklausą,** kad atidarytumėte užklausos dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="b93b9-128">Užklausos dialogo lango skirtuke **Rūšiavimas** peržiūrėkite rūšiavimo kriterijus ir įsitikinkite, kad yra taisyklė, apimanti lauką, kurį norite naudoti savo bangoms grupuoti.</span><span class="sxs-lookup"><span data-stu-id="b93b9-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="b93b9-129">Jei ruošiatės dirbti pagal scenarijų naudojant demonstracinius duomenis, pridėkite eilutę, kurioje yra šios reikšmės:</span><span class="sxs-lookup"><span data-stu-id="b93b9-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="b93b9-130">**Lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="b93b9-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b93b9-131">**Išvestinė lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="b93b9-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b93b9-132">**Laukas:** *Vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="b93b9-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="b93b9-133">Pasirinkus šią reikšmę, gali būti parodytas šis pranešimas: „Vežėjo paslauga nėra indekso laukas.</span><span class="sxs-lookup"><span data-stu-id="b93b9-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="b93b9-134">Ar norite įtraukti rūšiavimą?“</span><span class="sxs-lookup"><span data-stu-id="b93b9-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="b93b9-135">Pasirinkite **Taip** rūšiavimui įtraukti.</span><span class="sxs-lookup"><span data-stu-id="b93b9-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="b93b9-136">**Ieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="b93b9-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b93b9-137">Pasirinkite **Gerai**, kad išsaugotumėte pakeitimus ir uždarykite užklausos dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="b93b9-138">Veiksmų srityje pasirinkite **Bangos šablonų grupavimas**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="b93b9-139">Puslapyje **Bangos šablonų grupavimas** pasirinkite **Grupuoti pagal** žymės langelį kiekvienai eilutei, kurią norite naudoti, kad būtų galima grupuoti užsakymų eilutes į bangą, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="b93b9-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="b93b9-140">Jei ruošiatės dirbti per scenarijų naudojant demonstracinius duomenis, pasirinkite žymės langelį **Grupuoti pagal** *Vežėjo paslaugos* eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="b93b9-141">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-141">Select **Save**.</span></span>
1. <span data-ttu-id="b93b9-142">Uždarykite **Bangos šablono grupavimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="b93b9-143">Pasirinkite **Įrašyti**, kad įrašytumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="b93b9-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="b93b9-144">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="b93b9-144">Scenario</span></span>

<span data-ttu-id="b93b9-145">Šiame skyriuje pateikiamas planas, kuriuo vadovaujantis galite sužinoti, ką ši funkcija atlieka ir kaip ją naudoti.</span><span class="sxs-lookup"><span data-stu-id="b93b9-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="b93b9-146">Įgalinkite duomenų pavyzdį</span><span class="sxs-lookup"><span data-stu-id="b93b9-146">Make sample data available</span></span>

<span data-ttu-id="b93b9-147">Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b93b9-148">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="b93b9-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="b93b9-149">Taip pat galite naudoti šią scenarijų kaip vedlį, kaip naudotis funkcija dirbant gamybos sistemoje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="b93b9-150">Tačiau tokiu atveju, Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="b93b9-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="b93b9-151">Scenarijus: Bangos šablonų grupavimas</span><span class="sxs-lookup"><span data-stu-id="b93b9-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="b93b9-152">Šis scenarijus parodo, kaip naudoti bangos šablonų grupavimą automatiniam kelių bangų sukūrimui, remiantis grupavimo kriterijais, apibrėžtais bangos šablone.</span><span class="sxs-lookup"><span data-stu-id="b93b9-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="b93b9-153">Šiuo atveju bangos šablonas nustatomas sistemoje, kad būtų galima sukurti vieną bangą vienai vežėjo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="b93b9-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="b93b9-154">Prieš pradėdami, paruoškite savo bangos šabloną, kaip aprašyta ankstesniame šios temos skyriuje [nustatyti bangos šabloną anksčiau šioje temoje naudoti bangos šablono grupavimo ](#set-up-template).</span><span class="sxs-lookup"><span data-stu-id="b93b9-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="b93b9-155">Jei šiame scenarijuje dirbsite su demonstraciniais duomenimis, įsitikinkite, kad naudojate siūlomas šios procedūros demonstracines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b93b9-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="b93b9-156">Šis nustatymas bangas sugrupuos pagal vežėjo paslaugą, nustatytą kiekvienam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="b93b9-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="b93b9-157">Pardavimo užsakymo 1 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="b93b9-157">Create sales order 1</span></span>

1. <span data-ttu-id="b93b9-158">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b93b9-159">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b93b9-160">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b93b9-161">„FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–004*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="b93b9-162">„FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="b93b9-163">Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="b93b9-164">Naujas pardavimo užsakymas atidaromas **Eilučių** rodinyje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="b93b9-165">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b93b9-166">Perjunkite **Antraštės** rodinį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b93b9-167">„FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="b93b9-168">**Siuntos vežėjas:** *Oro transportas*</span><span class="sxs-lookup"><span data-stu-id="b93b9-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="b93b9-169">**Vežėjo paslauga:** *oro*</span><span class="sxs-lookup"><span data-stu-id="b93b9-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="b93b9-170">Grįžkite į **Eilučių** rodinį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="b93b9-171">Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę,** kad įtrauktumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="b93b9-172">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b93b9-173">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b93b9-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="b93b9-174">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="b93b9-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b93b9-175">Pasirinkite naują užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b93b9-176">Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b93b9-177">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b93b9-178">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b93b9-179">Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b93b9-180">Pasižymėkite bangos ID ir siuntos ID numerius.</span><span class="sxs-lookup"><span data-stu-id="b93b9-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="b93b9-181">Peržiūrėkite bangą, kuri buvo sukurta iš pardavimo užsakymo 1</span><span class="sxs-lookup"><span data-stu-id="b93b9-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="b93b9-182">Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="b93b9-183">Pasirinkite bangos ID, kuri buvo sukurta iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="b93b9-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="b93b9-184">Pasirinkite bangos ID saitą, kad atidarytumėte puslapį Bangos išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="b93b9-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="b93b9-185">Atkreipkite dėmesį, kad siunta buvo pridėta į „FastTab“ skirtuką **Bangos eilutės**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="b93b9-186">Pardavimo užsakymo 2 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="b93b9-186">Create sales order 2</span></span>

1. <span data-ttu-id="b93b9-187">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b93b9-188">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b93b9-189">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b93b9-190">„FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–005*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="b93b9-191">„FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="b93b9-192">Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="b93b9-193">Naujas pardavimo užsakymas atidaromas **Eilučių** rodinyje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="b93b9-194">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b93b9-195">Perjunkite **Antraštės** rodinį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b93b9-196">„FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="b93b9-197">**Siuntimo vežėjas:** *„Flower moving“*</span><span class="sxs-lookup"><span data-stu-id="b93b9-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="b93b9-198">**Vežėjo paslauga:** *Std*</span><span class="sxs-lookup"><span data-stu-id="b93b9-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="b93b9-199">Grįžkite į **Eilučių** rodinį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="b93b9-200">Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę,** kad įtrauktumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="b93b9-201">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b93b9-202">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b93b9-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b93b9-203">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="b93b9-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b93b9-204">Pasirinkite naują užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b93b9-205">Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b93b9-206">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b93b9-207">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b93b9-208">Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b93b9-209">Pasižymėkite bangos ID ir siuntos ID numerius.</span><span class="sxs-lookup"><span data-stu-id="b93b9-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="b93b9-210">Atkreipkite dėmesį, kad bangos ID skiriasi nuo pirmo pardavimo užsakymo bangos ID.</span><span class="sxs-lookup"><span data-stu-id="b93b9-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="b93b9-211">Peržiūrėkite bangą, kuri buvo sukurta iš pardavimo užsakymo 2</span><span class="sxs-lookup"><span data-stu-id="b93b9-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="b93b9-212">Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="b93b9-213">Pasirinkite bangos ID, kuri buvo sukurta iš antrojo pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="b93b9-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="b93b9-214">Pasirinkite bangos ID saitą, kad atidarytumėte puslapį Bangos išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="b93b9-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="b93b9-215">Atkreipkite dėmesį, kad siunta buvo pridėta į „FastTab“ skirtuką **Bangos eilutės**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="b93b9-216">Buvo sukurta nauja šios siuntos banga, nes ji naudoja kitą vežėjo paslaugą nei pirmas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b93b9-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="b93b9-217">Pardavimo užsakymo 3 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="b93b9-217">Create sales order 3</span></span>

1. <span data-ttu-id="b93b9-218">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b93b9-219">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b93b9-220">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b93b9-221">„FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–006*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="b93b9-222">„FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="b93b9-223">Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="b93b9-224">Naujas pardavimo užsakymas atidaromas **Eilučių** rodinyje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="b93b9-225">Pasižymėkite pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b93b9-226">Perjunkite **Antraštės** rodinį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b93b9-227">„FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="b93b9-228">**Siuntos vežėjas:** *Oro transportas*</span><span class="sxs-lookup"><span data-stu-id="b93b9-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="b93b9-229">**Vežėjo paslauga:** *oro*</span><span class="sxs-lookup"><span data-stu-id="b93b9-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="b93b9-230">Grįžkite į **Eilučių** rodinį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="b93b9-231">Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę,** kad įtrauktumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="b93b9-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="b93b9-232">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="b93b9-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b93b9-233">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b93b9-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b93b9-234">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="b93b9-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b93b9-235">Pasirinkite naują užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b93b9-236">Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="b93b9-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b93b9-237">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b93b9-238">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b93b9-239">Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą.</span><span class="sxs-lookup"><span data-stu-id="b93b9-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b93b9-240">Pasižymėkite bangos ID ir siuntos ID numerius.</span><span class="sxs-lookup"><span data-stu-id="b93b9-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="b93b9-241">Siunta buvo priskirta esamai bangai iš pirmojo pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="b93b9-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="b93b9-242">Peržiūrėti 1 ir 3 pardavimų užsakymų bangas</span><span class="sxs-lookup"><span data-stu-id="b93b9-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="b93b9-243">Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.</span><span class="sxs-lookup"><span data-stu-id="b93b9-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="b93b9-244">Pasirinkite bangos ID, kuri buvo sukurta iš trečiojo pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="b93b9-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="b93b9-245">Pasirinkite bangos ID saitą, kad atidarytumėte puslapį Bangos išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="b93b9-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="b93b9-246">Atkreipkite dėmesį, kad siunta buvo pridėta į „FastTab” skirtuką **Bangos eilutės** kartu su pirma pardavimo užsakymo siunta.</span><span class="sxs-lookup"><span data-stu-id="b93b9-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]