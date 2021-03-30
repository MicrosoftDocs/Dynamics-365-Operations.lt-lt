---
title: Papildymo pagal zoną ribinės vertės
description: Pagal zoną paremtas papildymas naudoja minimalių / maksimalių (min. / maks.) verčių papildymo strategiją, įvertinančią visas sandėlio zonas, o ne tik atskiras vietas. Todėl sandėlio vadovai gali greičiau sužinoti, kada paėmimų zonose reikia papildomų atsargų.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6aaa139fb206c035b25b7056e681d086fde6447f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245063"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="80c5c-104">Papildymo pagal zoną ribinės vertės</span><span class="sxs-lookup"><span data-stu-id="80c5c-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80c5c-105">Pagal zoną paremtas papildymas naudoja minimalių/maksimalių (min/max) verčių [papildymo](replenishment.md) strategiją, įvertinančią visas sandėlio zonas, o ne tik atskiras vietas.</span><span class="sxs-lookup"><span data-stu-id="80c5c-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="80c5c-106">Todėl sandėlio vadovai gali greičiau sužinoti, kada paėmimų zonose reikia papildomų atsargų.</span><span class="sxs-lookup"><span data-stu-id="80c5c-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="80c5c-107">Šios funkcijos nustatymas yra panašus į vieta pagrįsto papildymo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="80c5c-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="80c5c-108">Tačiau, kai nustatote min. / maks. papildymo šabloną, taip pat galite nurodyti, ar ribinė vertė turi būti vertinama pagal vietą arba pagal zoną.</span><span class="sxs-lookup"><span data-stu-id="80c5c-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="80c5c-109">Jei nustatote vertinimą, paremtą zonomis, turite pridėti konkrečias zonas prie srities parinkties užklausos.</span><span class="sxs-lookup"><span data-stu-id="80c5c-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="80c5c-110">Kaip ir vieta pagrįstas min. / maks. papildymo, zonomis pagrįsto min. / maks. papildymo pagrindas yra minimalios atsargų ribinės vertės nustatymas, kuris sukuria pažymėtų prekių papildymo darbo kūrimą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="80c5c-111">Šis papildymo darbas padidins atsargas iki nurodytos maksimalios ribos zonai.</span><span class="sxs-lookup"><span data-stu-id="80c5c-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="80c5c-112">Zonomis pagrįsto papildymo procesai nėra palaikomi produktų variantams dabartiniame leidime.</span><span class="sxs-lookup"><span data-stu-id="80c5c-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="80c5c-113">Skirtingai nei vieta pagrįstame min. / maks. papildyme, zona pagrįstame min. / maks. papildyme nereikia fiksuoti vietų, siekiant įvertinti, ar jos turi saugoti konkrečią prekę.</span><span class="sxs-lookup"><span data-stu-id="80c5c-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="80c5c-114">Todėl, zona pagrįstame papildyme galima naudoti min. / maks. papildymą, net jei neužfiksavote vietos kiekvienai prekei ar prekės variantui sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="80c5c-115">Kai zonoje esantis kiekis yra mažesnis už nurodytą minimalią ribinę vertę, sukuriamas papildymo darbas.</span><span class="sxs-lookup"><span data-stu-id="80c5c-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="80c5c-116">Vietos nustatymo nurodymuose bus nustatoma, konkreti vieta, į kurią reikia padėti atsargas.</span><span class="sxs-lookup"><span data-stu-id="80c5c-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="80c5c-117">Papildymo pagal zoną ribinės vertės įjungimo funkcija</span><span class="sxs-lookup"><span data-stu-id="80c5c-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="80c5c-118">Norėdami naudoti *Papildymo pagal zoną ribinės vertės* funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="80c5c-119">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="80c5c-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="80c5c-120">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="80c5c-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="80c5c-121">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="80c5c-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="80c5c-122">**Funkcijos pavadinimas** *Papildymo pagal zoną ribinės vertės*</span><span class="sxs-lookup"><span data-stu-id="80c5c-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="80c5c-123">Nustatyti papildymą pagal zoną</span><span class="sxs-lookup"><span data-stu-id="80c5c-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="80c5c-124">Norėdami zona pagrįstą papildymą, turite sukonfigūruoti kelias sistemos dalis.</span><span class="sxs-lookup"><span data-stu-id="80c5c-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="80c5c-125">Šiame skyriuje supažindinama su įvairiais parametrais ir pateikiamos demonstracinių duomenų vertės, kurias galite įvesti, jei norite pagal scenarijų šios temos pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="80c5c-126">Vietos nurodymų nustatymas</span><span class="sxs-lookup"><span data-stu-id="80c5c-126">Set up directive codes</span></span>

<span data-ttu-id="80c5c-127">[Vietos nurodymai](control-warehouse-location-directives.md) leidžia tiksliau nustatyti vietos šabloną, naudojamą darbo šablone.</span><span class="sxs-lookup"><span data-stu-id="80c5c-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="80c5c-128">Kiekvienas kodas nustato bendrąją vertę, kurią galite nurodyti konfigūruodami kiekvieną šablono tipą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="80c5c-129">Peržiūrėti ir redaguoti nurodymo kodus</span><span class="sxs-lookup"><span data-stu-id="80c5c-129">View and edit directive codes</span></span>

<span data-ttu-id="80c5c-130">Norėdami peržiūrėti arba redaguoti savo nurodymų kodus, eikite į **Sandėlio valdymas \> Nustatymai \> Nurodymų kodai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="80c5c-131">Nurodymo kodų parodomųjų duomenų paruošimas</span><span class="sxs-lookup"><span data-stu-id="80c5c-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="80c5c-132">Šis pavyzdys parodo, kaip paruošti nurodymo kodą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="80c5c-133">Jei jūs planuojate dirbti per scenarijų šios temos pabaigoje, naudokitės čia pateiktomis demonstracinių duomenų vertėmis.</span><span class="sxs-lookup"><span data-stu-id="80c5c-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="80c5c-134">Kitu atveju naudokite savo vertes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="80c5c-135">Pasirinkite **USMF** juridinį subjektą dirbti su demonstraciniais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="80c5c-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="80c5c-136">Eikite į **Sandėlio valdymas \> Nustatymas \> Nurodymų kodai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="80c5c-137">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-138">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-139">**Nurodymo kodas:** _Zone replen_</span><span class="sxs-lookup"><span data-stu-id="80c5c-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="80c5c-140">**Nurodymo aprašas:** _Papildymas pagal zoną_</span><span class="sxs-lookup"><span data-stu-id="80c5c-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="80c5c-141">Pasirinkite **Įrašyti**, kad įrašytumėte naują kodą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="80c5c-142">Nustatyti papildymo šablonus</span><span class="sxs-lookup"><span data-stu-id="80c5c-142">Set up replenishment templates</span></span>

<span data-ttu-id="80c5c-143">[Min. / maks. papildymo šablonai](tasks/set-up-min-max-replenishment-process.md) yra pagrindinis mechanizmas, skirtas palaikyti optimalų prekių kiekį paėmimo vietose.</span><span class="sxs-lookup"><span data-stu-id="80c5c-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="80c5c-144">Šiuose šablonuose turite nustatyti taisykles, kurios bus naudojamos atsargoms papildyti sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="80c5c-145">Papildymas, kurį galima naudoti šablonuose, apima zona pagrįstą papildymą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="80c5c-146">Peržiūrėti ir redaguoti papildymo šablonus</span><span class="sxs-lookup"><span data-stu-id="80c5c-146">View and edit replenishment templates</span></span>

<span data-ttu-id="80c5c-147">Papildymo šablonas yra taisyklės, kuriomis remiantis kontroliuojama, kada ir kaip vietos yra papildomos.</span><span class="sxs-lookup"><span data-stu-id="80c5c-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="80c5c-148">Pasirinkite šabloną kontroliuoti, kada ir kaip bus vykdomas papildymas.</span><span class="sxs-lookup"><span data-stu-id="80c5c-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="80c5c-149">Papildymo šablonų peržiūrai ir redagavimui eikite į **Sandėlio valdymas \> Nustatymas \> Papildymas \> Papildymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="80c5c-150">Paruošti demonstracinius duomenis papildymo šablone</span><span class="sxs-lookup"><span data-stu-id="80c5c-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="80c5c-151">Šis pavyzdys parodo, kaip paruošti papildymo šabloną.</span><span class="sxs-lookup"><span data-stu-id="80c5c-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="80c5c-152">Jei jūs planuojate dirbti per scenarijų šios temos pabaigoje, naudokitės čia pateiktomis demonstracinių duomenų vertėmis.</span><span class="sxs-lookup"><span data-stu-id="80c5c-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="80c5c-153">Kitu atveju naudokite savo vertes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="80c5c-154">Pasirinkite **USMF** juridinį subjektą dirbti su demonstraciniais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="80c5c-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="80c5c-155">Eikite į **Sandėlio valdymas \> Nustatymas \> Papildymas \> Papildymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="80c5c-156">Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.</span><span class="sxs-lookup"><span data-stu-id="80c5c-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="80c5c-157">Veiksmų srityje pasirinkite **Nauja,** kad pridėtumėte eilutę į **Peržiūros** tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="80c5c-158">Naujoje eilutėje nustatykite šias vertes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-158">In the new row, set the following values.</span></span> <span data-ttu-id="80c5c-159">Priimkite numatytąsias vertes visuose kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="80c5c-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="80c5c-160">**Papildyti šabloną:** _Zone min/maks replen_</span><span class="sxs-lookup"><span data-stu-id="80c5c-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="80c5c-161">**Aprašas:** _Zonos min. / maks. papildymas_</span><span class="sxs-lookup"><span data-stu-id="80c5c-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="80c5c-162">**Papildymo tipas:** _Minimalus arba maksimalus_</span><span class="sxs-lookup"><span data-stu-id="80c5c-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="80c5c-163">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-163">Select **Save**.</span></span>
1. <span data-ttu-id="80c5c-164">Kol nauja eilutė vis dar pasirenkama **Peržiūros** tinklelyje, pasirinkite **Naujas** virš **Papildymo šablono informacija,** kad pridėtumėte eilutę, susijusią su jau sukurtu *Zone Min/Max replen* papildymo šablonu.</span><span class="sxs-lookup"><span data-stu-id="80c5c-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="80c5c-165">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-166">**Sekos numeris:** Įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="80c5c-167">**Aprašas:** Įveskite _Paėmimo zonos papildymas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="80c5c-168">**Papildymo vienetas:** Pasirinkite _EA_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="80c5c-169">**Užklausos tipas** – palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="80c5c-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="80c5c-170">**Nurodymo kodas:** Šis laukas susieja papildymo šabloną su vietos nurodymu.</span><span class="sxs-lookup"><span data-stu-id="80c5c-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="80c5c-171">Pasirinkite demonstracinių duomenų nuorodos kodą, kurį sukūrėte anksčiau (_Zone replen_).</span><span class="sxs-lookup"><span data-stu-id="80c5c-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="80c5c-172">**Darbo šablonas** – Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="80c5c-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="80c5c-173">**Minimalus kiekis:** Šis laukas nustato kiekį, kuris suaktyvins papildymą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="80c5c-174">Įveskite _50_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-174">Enter _50_.</span></span>
    - <span data-ttu-id="80c5c-175">**Maksimalus kiekis:** Šis laukas nustato maksimalų prekės kiekį, kurį galima pristatyti zonoje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="80c5c-176">Sugeneruotas papildymo darbas padidins atsargų kiekį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="80c5c-177">Įveskite _150_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-177">Enter _150_.</span></span>
    - <span data-ttu-id="80c5c-178">**Vienetas:** Šis laukas nustato minimalių ir maksimalių verčių vienetą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="80c5c-179">Pasirinkite _EA_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-179">Select _ea_.</span></span>
    - <span data-ttu-id="80c5c-180">**Paklausos padidėjimas:** pasirinkite _Apvalinti_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="80c5c-181">**Papildyti tuščias fiksuotas vietas:** pasirinkite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="80c5c-182">**Papildyti tik fiksuotas vietas:** išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-183">**Produkto užklausos režimas:** Pasirinkite _Produkto užklausa_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="80c5c-184">**Papildymo ribinės vertės aprėptis:** Šis laukas nurodo, ar šablonas turėtų būti įvertintas pagal zoną, ar pagal konkrečią vietą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="80c5c-185">Pasirinkite _Zone_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-185">Select _Zone_.</span></span>
    - <span data-ttu-id="80c5c-186">**Sandėlis:** Pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="80c5c-187">Pasirinkite **Pasirinkit produktus** virš **Papildymo šablono informacijos** tinklelio.</span><span class="sxs-lookup"><span data-stu-id="80c5c-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="80c5c-188">Dialogo lango **Produkto užklausa** skirtuke **Diapazonas** pasirinkite **Pridėti** eilutei pridėti į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-189">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-190">**Lentelė:** _Prekės_</span><span class="sxs-lookup"><span data-stu-id="80c5c-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="80c5c-191">**Išvestinė lentelė:** _Prekės_</span><span class="sxs-lookup"><span data-stu-id="80c5c-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="80c5c-192">**Laukas:** _Prekės numeris_</span><span class="sxs-lookup"><span data-stu-id="80c5c-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="80c5c-193">**Kriterijai:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="80c5c-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="80c5c-194">Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="80c5c-195">Pasirinkite **Pasirinkit papildymo produktus** virš **Papildymo šablono informacijos** tinklelio.</span><span class="sxs-lookup"><span data-stu-id="80c5c-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="80c5c-196">Dialogo lango **Zonos užklausa** skirtuke **Diapazonas** pridėkite eilutei į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-197">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-198">**Lentelė:** _Sandėlio zona_</span><span class="sxs-lookup"><span data-stu-id="80c5c-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="80c5c-199">**Išvestinė lentelė:** _Sandėlio zona_</span><span class="sxs-lookup"><span data-stu-id="80c5c-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="80c5c-200">**Laukas:** _Zonos ID_</span><span class="sxs-lookup"><span data-stu-id="80c5c-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="80c5c-201">**Kriterijai:** _AUKŠTAS_</span><span class="sxs-lookup"><span data-stu-id="80c5c-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="80c5c-202">Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="80c5c-203">Nustatyti vietos nurodymus</span><span class="sxs-lookup"><span data-stu-id="80c5c-203">Set up location directives</span></span>

<span data-ttu-id="80c5c-204">Skirtingai nei vieta pagrįstas min. / maks. papildymas, zona pagrįstas min. / maks. papildyme, reikia nustatyti tiek paėmimo, tiek padėjimo vietos direktyvas, nes sistema įvertina visą zoną, o ne tik vieną paėmimo vietą siuntimo darbui.</span><span class="sxs-lookup"><span data-stu-id="80c5c-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="80c5c-205">Peržiūrėti ir redaguoti vietos nurodymus</span><span class="sxs-lookup"><span data-stu-id="80c5c-205">View and edit location directives</span></span>

<span data-ttu-id="80c5c-206">Norėdami peržiūrėti arba redaguoti vietos nurodymus, eikite į **Sandėlio valdymas \> Nustatymai \> Vietos nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="80c5c-207">Pavyzdžiai, kuriais rodoma, kaip naudoti nustatymus siekiant sukurti reikiamos paėmimo vietos nurodymus ir nustatyti vietos nurodymus, pateikiami kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="80c5c-208">Vietos nurodymo demonstracinių duomenų paruošimas</span><span class="sxs-lookup"><span data-stu-id="80c5c-208">Prepare demo data location directives</span></span>

<span data-ttu-id="80c5c-209">Norėdami paruošti demonstracinius duomenis taip, kad juos būtų galima naudoti scenarijuje šios temos pabaigoje, turite sukurti du vietos nurodymus: vieną paėmimui ir kitą padėjimui.</span><span class="sxs-lookup"><span data-stu-id="80c5c-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="80c5c-210">Papildymo paėmimo vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="80c5c-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="80c5c-211">Pasirinkite **USMF** juridinį subjektą dirbti su demonstraciniais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="80c5c-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="80c5c-212">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="80c5c-213">Kairinės srities lauką **Darbo užsakymo tipas** nustatykite į _Papildymas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="80c5c-214">Veiksmų srityje pasirinkite **Nauja** naujam nurodymui sukurti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="80c5c-215">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-215">Set the following values:</span></span>

    - <span data-ttu-id="80c5c-216">**Sekos numeris:** Priimkite numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="80c5c-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="80c5c-217">**Pavadinimas:** Įvesti _Zonos paėmimas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="80c5c-218">**Darbo tipas:** pasirinkite _Paėmimas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="80c5c-219">**Saitas** Pasirinkite _6_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="80c5c-220">**Sandėlis:** Pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="80c5c-221">**Nurodymo kodas:** Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="80c5c-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="80c5c-222">**Keli SKU:** Nustatykite šią pasirinktį į _Ne_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="80c5c-223">Pasirinkite **įrašyti,** kad būtų kuriama nuoroda su parametrais, kuriuos sukonfigūravote iki šiol.</span><span class="sxs-lookup"><span data-stu-id="80c5c-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="80c5c-224">„FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="80c5c-225">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="80c5c-226">**Sekos numeris:** Įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="80c5c-227">**Kiekis Nuo** įveskite _0_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="80c5c-228">**Kiekis Iki:** įveskite _10000000_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="80c5c-229">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="80c5c-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="80c5c-230">**Rasti kiekį:** Pasirinkite _Nėra_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="80c5c-231">**Riboti pagal vienetą:** išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-232">**Apvalinti iki vieneto:** išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-233">**Rasti pakavimo kiekį:** Išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-234">**Leisti skaidyti:** pasirinkite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="80c5c-235">Pasirinkite **Įrašyti** naujai eilutei įrašyti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="80c5c-236">Kol jūsų nauja eilutė vis dar pasirenkama **Eilučių** tinklelyje, pasirinkite **Naujas** „FastTab“ **Vietos nurodymų veiksmai** eilutei įtraukti į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-237">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-238">**Sekos numeris:** Įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="80c5c-239">**Pavadinimas:** Įveskite _Paėmimas iš krovinio_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="80c5c-240">**Fiksuotos vietos naudojimas:** Pasirinkite _Fiksuotos ir nefiksuotos vietos_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="80c5c-241">**Leisti neigiamas atsargas:** Išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-242">**Paketas įgalintas:** Išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-243">**Strategija:** Pasirinkite _Nėra_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="80c5c-244">Pasirinkite **Įrašyti** naujam veiksmui įrašyti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="80c5c-245">Kol vis dar pasirinktas naujas veiksmas, virš **Vietos nurodymų veiksmų tinklelio** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="80c5c-246">Atsiranda užklausos dialogo langas, kuriame galite pasirinkti vietas, kurias norite papildyti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="80c5c-247">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-248">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-249">**Lentelė:** _Vietos_</span><span class="sxs-lookup"><span data-stu-id="80c5c-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="80c5c-250">**Išvestinė lentelė:** _Vietos_</span><span class="sxs-lookup"><span data-stu-id="80c5c-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="80c5c-251">**Laukas:** _Zonos ID_</span><span class="sxs-lookup"><span data-stu-id="80c5c-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="80c5c-252">**Kriterijai:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="80c5c-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="80c5c-253">Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="80c5c-254">Pasirinkite **Įrašyti**, kad įrašytumėte vietos nurodymą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="80c5c-255">Papildymo padėjimo vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="80c5c-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="80c5c-256">Įsitikinkite, kas puslapio **Vietos nurodymai** kairiojoje srityje laukas **Darbo užsakymo tipas** vis dar nustatytas kaip _Papildymas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="80c5c-257">Veiksmų srityje pasirinkite **Nauja** kitam nurodymui sukurti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="80c5c-258">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-258">Set the following values:</span></span>

    - <span data-ttu-id="80c5c-259">**Sekos numeris:** Priimkite numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="80c5c-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="80c5c-260">**Pavadinimas:** Įvesti _Zonos padėjimas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="80c5c-261">**Darbo užsakymo tipas:** pasirinkite _Padėjimas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="80c5c-262">**Saitas:** Pasirinkite _6_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="80c5c-263">**Sandėlis:** Pasirinkite _61_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="80c5c-264">**Nurodymo kodas:** Pasirinkite _Zone replen_ norėdami susieti šį vietos nurodymo su papildymo šablonu, kuris buvo sukurtas anksčiau, naudojant anksčiau sukurtą kodą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="80c5c-265">**Keli SKU:** Nustatykite šią pasirinktį į _Ne_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="80c5c-266">Pasirinkite **įrašyti,** kad būtų kuriama nuoroda su parametrais, kuriuos sukonfigūravote iki šiol.</span><span class="sxs-lookup"><span data-stu-id="80c5c-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="80c5c-267">„FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="80c5c-268">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="80c5c-269">**Sekos numeris:** Įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="80c5c-270">**Kiekis Nuo** įveskite _0_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="80c5c-271">**Kiekis Iki:** įveskite _10000000_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="80c5c-272">**Vienetas:** lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="80c5c-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="80c5c-273">**Rasti kiekį:** Pasirinkite _Nėra_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="80c5c-274">**Riboti pagal vienetą:** išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-275">**Apvalinti iki vieneto:** išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-276">**Rasti pakavimo kiekį:** Išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-277">**Leisti skaidyti:** pasirinkite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="80c5c-278">Pasirinkite **Įrašyti** naujai eilutei įrašyti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="80c5c-279">Kol jūsų nauja eilutė vis dar pasirenkama **Eilučių** tinklelyje, pasirinkite **Naujas** „FastTab“ **Vietos nurodymų veiksmai** eilutei įtraukti į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-280">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-281">**Sekos numeris:** Įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="80c5c-282">**Pavadinimas:** Įvesti _Zonos padėjimas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="80c5c-283">**Fiksuotos vietos naudojimas:** Pasirinkite _Fiksuotos ir nefiksuotos vietos_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="80c5c-284">**Leisti neigiamas atsargas:** Išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-285">**Paketas įgalintas:** Išvalykite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="80c5c-286">**Strategija:** Pasirinkti _Konsolidavimas_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="80c5c-287">Pasirinkite **Įrašyti** naujam veiksmui įrašyti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="80c5c-288">Kol vis dar pasirenkamas naujas veiksmas, pasirinkite **Redaguoti užklausą** virš **Vietos nurodymų veiksmų** tinklelio.</span><span class="sxs-lookup"><span data-stu-id="80c5c-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="80c5c-289">Atsiranda užklausos dialogo langas, kuriame galite pasirinkti zonas, kurias norite papildyti.</span><span class="sxs-lookup"><span data-stu-id="80c5c-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="80c5c-290">Ši zona turi būti ta pati zona, kuri nurodyta papildymo šablone.</span><span class="sxs-lookup"><span data-stu-id="80c5c-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="80c5c-291">Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="80c5c-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="80c5c-292">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="80c5c-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="80c5c-293">**Lentelė:** _Vietos_</span><span class="sxs-lookup"><span data-stu-id="80c5c-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="80c5c-294">**Išvestinė lentelė:** _Vietos_</span><span class="sxs-lookup"><span data-stu-id="80c5c-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="80c5c-295">**Laukas:** _Zonos ID_</span><span class="sxs-lookup"><span data-stu-id="80c5c-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="80c5c-296">**Kriterijai:** _AUKŠTAS_</span><span class="sxs-lookup"><span data-stu-id="80c5c-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="80c5c-297">Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="80c5c-298">Pasirinkite **Įrašyti**, kad įrašytumėte vietos nurodymą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="80c5c-299">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="80c5c-299">Scenario</span></span>

<span data-ttu-id="80c5c-300">Šiame skyriuje pateikiamas pavyzdinis scenarijus, rodantis, kaip dirbti su funkcija.</span><span class="sxs-lookup"><span data-stu-id="80c5c-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="80c5c-301">Paruošti pavyzdinius duomenis, reikalingus pavyzdžio scenarijui</span><span class="sxs-lookup"><span data-stu-id="80c5c-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="80c5c-302">Prieš pradėdami dirbti pagal scenarijų, turite suaktyvinti pavyzdinius duomenis ir nustatyti šią funkciją, kaip aprašyta šiame ir ankstesniame šios temos skyriuose.</span><span class="sxs-lookup"><span data-stu-id="80c5c-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="80c5c-303">Naudokite USMF juridinį subjektą</span><span class="sxs-lookup"><span data-stu-id="80c5c-303">Use the USMF legal entity</span></span>

<span data-ttu-id="80c5c-304">Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="80c5c-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="80c5c-305">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="80c5c-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="80c5c-306">Paruošti papildomus pavyzdžio duomenis</span><span class="sxs-lookup"><span data-stu-id="80c5c-306">Prepare additional sample data</span></span>

<span data-ttu-id="80c5c-307">Pasirinkę **USMF** juridinį subjektą, pridėkite papildomus pavyzdinius duomenis, kaip nurodyta ankstesnėje šios temoje dalyje [nustatyti zonos papildymo ](#setup).</span><span class="sxs-lookup"><span data-stu-id="80c5c-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="80c5c-308">Turimų atsargų patikrinimas</span><span class="sxs-lookup"><span data-stu-id="80c5c-308">Check your on-hand inventory</span></span>

<span data-ttu-id="80c5c-309">Atlikite šiuos veiksmus, norėdami įsitikinti, kad jūsų sistemoje yra pakankamai atsargų, kad būtų įvykdomas pavyzdinis scenarijus.</span><span class="sxs-lookup"><span data-stu-id="80c5c-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="80c5c-310">Įsitikinkite, kad yra prekės *A0001* turimos atsargos, esančios dvejose skirtingose paėmimo zonos (*AUKŠTAS*) vietose, yra nurodytos papildymo šablone.</span><span class="sxs-lookup"><span data-stu-id="80c5c-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="80c5c-311">Tačiau bendroji atsargų suma turėtų būti mažesnė nei būtinas minimalus kiekis (*50*), nurodytas papildymo šablone.</span><span class="sxs-lookup"><span data-stu-id="80c5c-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="80c5c-312">Tokiu būdu galite modeliuoti, kaip skaičiuoti visą zoną, o ne tik vieną vietą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="80c5c-313">**Naudokite bet kurį sandėlio procesą atsargų koregavimui koreguoti kaip reikia.**</span><span class="sxs-lookup"><span data-stu-id="80c5c-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="80c5c-314">Įsitikinkite, kad yra pakankamai prekės *A0001* atsargų masinėje vietoje, kuri yra nurodyta zonos paėmimo vietos nurodyme, kur papildymo darbas turėtų paimti prekes iš zonos ID *BULK*.</span><span class="sxs-lookup"><span data-stu-id="80c5c-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="80c5c-315">Tačiau bendroji atsargų suma turėtų būti mažesnė nei būtinas maksimalus kiekis (*150*), nurodytas papildymo šablone.</span><span class="sxs-lookup"><span data-stu-id="80c5c-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="80c5c-316">Nebūtina, bet rekomenduojama: Vykdydami šiuos veiksmus sukursite atsargų koregavimo žurnalą:</span><span class="sxs-lookup"><span data-stu-id="80c5c-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="80c5c-317">Eikite į **Atsargų valdymas \> Žurnalo įrašai \> Prekės \> Atsargų koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="80c5c-318">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-318">Select **New**.</span></span>
    1. <span data-ttu-id="80c5c-319">Dialogo lango **Kurti atsargų žurnalą** lauke **Sandėlis** pasirinkite *61*.</span><span class="sxs-lookup"><span data-stu-id="80c5c-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="80c5c-320">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-320">Select **OK**.</span></span>
    1. <span data-ttu-id="80c5c-321">„FastTab skirtuke“ **Žurnalo eilutės** naudokite mygtuką **Nauja,** norėdami įtraukti tris eilutes į tinklelį ir nustatyti tolimesnes vertes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="80c5c-322">Kai baigsite nustatyti kiekvieną eilutę, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="80c5c-323">**Eilutė 1:**</span><span class="sxs-lookup"><span data-stu-id="80c5c-323">**Line 1:**</span></span>

            - <span data-ttu-id="80c5c-324">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80c5c-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="80c5c-325">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="80c5c-325">**Site:** *6*</span></span>
            - <span data-ttu-id="80c5c-326">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="80c5c-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="80c5c-327">**Vieta:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="80c5c-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="80c5c-328">**Numerio lentelė:** Iš sąrašo pasirinkite esamą numerio lentelę arba sukurkite naują numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="80c5c-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="80c5c-329">**Kiekis:** *1000*</span><span class="sxs-lookup"><span data-stu-id="80c5c-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="80c5c-330">**Eilutė 2:**</span><span class="sxs-lookup"><span data-stu-id="80c5c-330">**Line 2:**</span></span>

            - <span data-ttu-id="80c5c-331">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80c5c-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="80c5c-332">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="80c5c-332">**Site:** *6*</span></span>
            - <span data-ttu-id="80c5c-333">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="80c5c-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="80c5c-334">**Vieta:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="80c5c-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="80c5c-335">**Numerio lentelė:** Iš sąrašo pasirinkite esamą numerio lentelę arba sukurkite naują numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="80c5c-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="80c5c-336">**Kiekis:** *15*</span><span class="sxs-lookup"><span data-stu-id="80c5c-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="80c5c-337">**Eilutė 3:**</span><span class="sxs-lookup"><span data-stu-id="80c5c-337">**Line 3:**</span></span>

            - <span data-ttu-id="80c5c-338">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80c5c-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="80c5c-339">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="80c5c-339">**Site:** *6*</span></span>
            - <span data-ttu-id="80c5c-340">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="80c5c-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="80c5c-341">**Vieta:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="80c5c-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="80c5c-342">**Numerio lentelė:** Iš sąrašo pasirinkite esamą numerio lentelę arba sukurkite naują numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="80c5c-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="80c5c-343">**Kiekis:** *10*</span><span class="sxs-lookup"><span data-stu-id="80c5c-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="80c5c-344">Veiksmų srityje pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="80c5c-345">Prieš pereidami prie kito žingsnio, ištaisykite visas aptiktas klaidas.</span><span class="sxs-lookup"><span data-stu-id="80c5c-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="80c5c-346">Veiksmų srityje pasirinkite **Registruoti,** kad atliktumėte atsargų registravimą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="80c5c-347">Scenarijaus pavyzdys: paleisti zona pagrįstą min. / maks. papildymą</span><span class="sxs-lookup"><span data-stu-id="80c5c-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="80c5c-348">Kai visi būtinųjų sąlygų pavyzdžio duomenys yra vietoje, galite suaktyvinti papildymą atlikdami šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80c5c-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="80c5c-349">Eikite į **Sandėlio valdymas \> Papildymas \> Papildymai**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="80c5c-350">Dialogo lango **Papildymas**„FastTab” skirtuke **Įtrauktini įrašai** Pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="80c5c-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="80c5c-351">Dialogo lango **Užklausa** skirtuke **Diapazonas** redaguokite numatytąją lentelės eilutę taip:</span><span class="sxs-lookup"><span data-stu-id="80c5c-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="80c5c-352">**Lentelė:** Pasirinkti _Papildymo šablonai_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="80c5c-353">**Išvestinė lentelė:** Pasirinkti _Papildymo šablonai_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="80c5c-354">**Laukas:** Pasirinkti _Papildymo šablonai_.</span><span class="sxs-lookup"><span data-stu-id="80c5c-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="80c5c-355">**Kriterijai:** Pasirinkite _Zoną min/maks replen__.</span><span class="sxs-lookup"><span data-stu-id="80c5c-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="80c5c-356">Šis papildymo šablonas yra sukuriamas, kai paruošiate demonstracinius duomenis šiam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="80c5c-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="80c5c-357">Pasirinkite **Gerai,** kad įrašytumėte užklausą ir sugrįžtumėte į **Papildymo** dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="80c5c-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="80c5c-358">Pasirinkite **Gerai,** norėdami paleisti papildymo šabloną.</span><span class="sxs-lookup"><span data-stu-id="80c5c-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="80c5c-359">Papildymo darbas yra sukuriamas, kad būtų galima paimti atsargas iš *BULK* zonos ir papildyti jomis *AUKŠTO* zoną.</span><span class="sxs-lookup"><span data-stu-id="80c5c-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="80c5c-360">Pastabos ir patarimai</span><span class="sxs-lookup"><span data-stu-id="80c5c-360">Notes and tips</span></span>

<span data-ttu-id="80c5c-361">Pateikiame kelias pastabas ir patarimus, kaip dirbti su funkcija:</span><span class="sxs-lookup"><span data-stu-id="80c5c-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="80c5c-362">Norėdami nustatyti papildymo darbą, kuris eina į pageidaujamą zoną, papildymo šablono eilutes ir vietos nurodymus galite susieti vienu iš šių būdų:</span><span class="sxs-lookup"><span data-stu-id="80c5c-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="80c5c-363">Redaguoti vietos nurodymo antraštės užklausą ir filtruoti pasirinktas papildymo šablono eilutes.</span><span class="sxs-lookup"><span data-stu-id="80c5c-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="80c5c-364">Naudojant nurodymo kodą papildymo šablone galima jį susieti su paėmimo vietos nurodymu.</span><span class="sxs-lookup"><span data-stu-id="80c5c-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="80c5c-365">Jei naudojate dinamines vietas, papildymo darbas bus pirmiausia sukurtas pirmoje galimoje vietoje arba toje vietoje, kurioje jau yra atsargų, jei vietos nustatymo veiksmas nustatomas taip, kad būtų galima naudoti **Konsolidavimo** strategiją.</span><span class="sxs-lookup"><span data-stu-id="80c5c-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="80c5c-366">Jei naudojate fiksuotas vietas, o ne zonas, turite naudoti [standartinį min. / maks. papildymą](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="80c5c-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]