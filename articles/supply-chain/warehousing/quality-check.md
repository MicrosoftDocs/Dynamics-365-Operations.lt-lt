---
title: Kokybės patikra
description: Šioje temoje pateikiama informacija apie kokybės tikrinimo funkciją. Ši funkcija leidžia sandėlio darbuotojams atlikti greitą vietos kokybės tikrinimą, jiems gaunant prekes vidaus doko vietoje.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c270426a228ac58652f1f60d6fe99d4886071fa6
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621443"
---
# <a name="quality-check"></a><span data-ttu-id="3d9b2-104">Kokybės patikra</span><span class="sxs-lookup"><span data-stu-id="3d9b2-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d9b2-105">*Kokybės tikrinimo* funkcija leidžia sandėlio darbuotojams greitai tikrinti vietą dėl kokybės, jiems gaunant prekes vidaus doko vietoje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="3d9b2-106">Šios vietos patikros yra naudingos, kai darbuotojai tikrina pakuotę arba lengvai atpažįsta prekės dalis.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="3d9b2-107">Funkcijas veda darbuotojus tam, kad jie greitai peržiūrėtų, ar esama akivaizdžių klaidų ar pažeidimų prieš tai, kai jie deda atsargas atidėjimo vietoje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="3d9b2-108">Ši funkcija yra alternatyvi funkcija standartiniam kokybės patikros procesui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="3d9b2-109">Ji siūlo daugiau lankstuma ir greitesnį apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="3d9b2-110">Naudojant šią funkciją atvykimo ir kokybės kontrolė vyksta tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="3d9b2-111">Kroviniui atvykus sandėlio darbuotojas užregistruoja atvykimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="3d9b2-112">Darbuotojas taip pat nuskaito licencijos numerį tam, kad užregistruotų vietą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="3d9b2-113">Darbuotojas atlieka greitą kokybės patikrą ir įrašo rezultatus (atitiko ar neatitiko) licencijos numeriui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="3d9b2-114">Įvyksta vienas iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="3d9b2-115">Jei kokybės tikrinimas atitiko, licencijos numeris priimtas ir vedamas į gavimo vietą, kaip įprasta.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="3d9b2-116">Jei kokybės patikra nepavyko, licencijos numeris yra atmetamas ir esantis atidėjimo darbas jai yra nukreipiamas į alternatyvią vietą tolesniam tyrimui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="3d9b2-117">Sukuriamas naujas kokybės užsakymas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-117">A new quality order is created.</span></span> <span data-ttu-id="3d9b2-118">Tam, kad peržiūrėtumėte kokybės užsakymą, kuris yra sukurtas dėl nepavykusio kokybės patikrinimo, eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="3d9b2-119">Šis procesas taip pat gali būti nustatytas taip, kad visi nuskaityti licencijos numeriai būtų nedelsiant nukreipti į kokybės tikrinimo vietą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="3d9b2-120">Įjunkite kokybės tikrinimo funkciją</span><span class="sxs-lookup"><span data-stu-id="3d9b2-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="3d9b2-121">Prieš tai kai galite naudoti *Kokybės tikrinimo* funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="3d9b2-122">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3d9b2-123">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3d9b2-124">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3d9b2-125">**Funkcijos pavadinimas:** *Kokybės tikrinimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="3d9b2-126">Nustatykite funkciją pavyzdiniam scenarijui</span><span class="sxs-lookup"><span data-stu-id="3d9b2-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="3d9b2-127">Šis skyrius aprašo gaires ir pavyzdį, kuris rodo, kaip nustatyti *Kokybės tikrinimo* funkciją ir paruošti pavyzdinius duomenis pavyzdiniam scenarijui, kuris pateiktas vėliau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="3d9b2-128">Įgalinkite duomenų pavyzdį</span><span class="sxs-lookup"><span data-stu-id="3d9b2-128">Make sample data available</span></span>

<span data-ttu-id="3d9b2-129">Tam, kad dirbtumėte su [pavyzdiniu scenarijumi](#example-scenario) naudodami pavyzdinius įrašus ir vertes nurodytas čia, turite būti sistemoje, kurioje standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yra įdiegti.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="3d9b2-130">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="3d9b2-131">Kokybės patikrinimo šablonas</span><span class="sxs-lookup"><span data-stu-id="3d9b2-131">Quality check template</span></span>

<span data-ttu-id="3d9b2-132">Kokybės tikrinimo šablonas nustato taisykles dėl greitos taško kokybės patikros gavimo metu.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="3d9b2-133">Eikite į **Sandėlio valdymą \> Nustatymai \> Darbas \> Kokybės tikrinimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="3d9b2-134">Pasirinkite **Naujas** tam, kad įtrauktumėte šabloną į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="3d9b2-135">Nustatykite tolesnes vertes tam, kad nustatytumėte naują šabloną:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="3d9b2-136">**Kokybės tikrinimo šablono pavadinimas:** *Doko tikrinimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="3d9b2-137">Įveskite pavadinimą, kuris nustato politikas taikomas šiam šablonui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="3d9b2-138">**Priėmimo politika:** *Vartotojo skatinimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="3d9b2-139">Nurodykite, ar vartotojai turi būti skatinami priimti ar atsisakyti atsargų kokybės darbo apdorojimo metu, ar kokybės turi būti automatiškai atsisakoma.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="3d9b2-140">Šios prieinamos parinktys yra *Automatinis atsisakymas* ir *Vartotojo skatinimas*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="3d9b2-141">**Kokybės apdorojimo politika:** *Sukurkite kokybės užsakymą*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="3d9b2-142">Pasirinkite politiką, kuri turi būti naudojama, kai kokybės inventoriaus yra atsisakoma.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="3d9b2-143">Galimos toliau nurodytos parinktys.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-143">The following options are available:</span></span>

        - <span data-ttu-id="3d9b2-144">*Sukurti tik darbą* – Tik sukurkite darbą, kad palengvintumėte inventoriaus judėjimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="3d9b2-145">*Sukurkite kokybės užsakymą* – Sukurkite kokybės užsakymą, kad palengvintumėte kokybės testus.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="3d9b2-146">**Bandymų grupė:** *Priedas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="3d9b2-147">Nurodykite testo grupę, kuri turi būti naudojama sukurtame kokybės užsakyme.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="3d9b2-148">Testo grupės yra nustatytos **Atsargų valdymo** modulyje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="3d9b2-149">Palikite **Destrukcinio teksto** parinktį išjungtą testinei grupei.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="3d9b2-150">Ši parinktis nustato, ar pavyzdys bus sunaikinamas kaip dalis testo testinėje grupėje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="3d9b2-151">Jei destruukcinis testas yra naudojamas, sistema generuoja atsargų perlaidą, kai kokybės užsakymas yra sukurtas elementui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="3d9b2-152">Nauja atsargų operacija numato tikrinimo kiekio atsargų sumažėjimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="3d9b2-153">Atsargų sumažinimas atsitinka, kai kokybės užsakymas yra pabaigiamas per patvirtinimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="3d9b2-154">Atsargų operacija nurodoma kaip kokybės užsakymas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="3d9b2-155">Darbo klasė - Kokybės tikrinimas</span><span class="sxs-lookup"><span data-stu-id="3d9b2-155">Work class – Quality check</span></span>

<span data-ttu-id="3d9b2-156">Darbo klasės yra naudojamos valdyti ir (arba) apriboti darbo tvarkos tipo eilutes, kurias sandėlio darbuotojai gali apdoroti mobiliame prietaise.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="3d9b2-157">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="3d9b2-158">Pasirinkite **Naujas**, kad sukurtumėte darbo klasę.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="3d9b2-159">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-160">**Darbo klasės ID:** *QC patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="3d9b2-161">Įveskite pavadinimą, kuris nustato darbo klasę.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="3d9b2-162">**Aprašas:** *QC tikrinimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="3d9b2-163">Įveskite trumpą aprašą, kuris nurodo, kokia darbo klasė jam naudojama.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="3d9b2-164">**Darbo užsakymo tipas:** *Kokybė kokybės patikroje*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="3d9b2-165">Pasirinkite darbo užsakymo tipą, kuris kuriamas pagal darbo klasę.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="3d9b2-166">Jums nustatant kokybės patikrinimo darbą, visuomet pasirinkite *Kokybė kokybės patikroje*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="3d9b2-167">**Tvirtinimo įdėjimo vietos tipas** „FastTab“, palikite **Vietos tipo** laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="3d9b2-168">Jei pasirinkote vietos tipą, apribojote vietas, kuriose elementai gali būti padedami po jų paėmimo.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="3d9b2-169">Šis laukelis naudojamas, kai vietos direktyva bando išspręsti vietą arba kai sandėlio darbuotojas rankiniu būdu nustato vietą mobilaus prietaiso meniu elementui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="3d9b2-170">Dėl išsamesnės informacijos apie darbo klases ir kaip jas sukurti, žr. [Sukurti darbo klasę](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="3d9b2-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="3d9b2-171">Darbo šablonas</span><span class="sxs-lookup"><span data-stu-id="3d9b2-171">Work template</span></span>

<span data-ttu-id="3d9b2-172">Darbo šablonai leidžia jums nustatyti darbo operacijas, kurios turi būti atliekamos sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="3d9b2-173">Dažniausiai sandėlio darbo operacijas sudaro pora veiksmų: sandėlio darbuotojas paima turimas atsargas aukštyn į vietą vietą ir tuomet padeda paimtas atsargas žemyn į kitą vietą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="3d9b2-174">Darbo šablonas kokybės kontrolei nustato darbo operacijas kokybės patikrų atlikimui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="3d9b2-175">Pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="3d9b2-175">Purchase orders</span></span>

1. <span data-ttu-id="3d9b2-176">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="3d9b2-177">Antraštėje nustatykite **Darbo užsakymo tipo** laukelį į *Įsigijimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="3d9b2-178">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3d9b2-179">Pasirinkite darbo šabloną, kuris turi apimti kokybės tikrinimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="3d9b2-180">**Peržiūros** skyriuje, **Darbo šablonas** laukelyje pasirinkite *51 PO kvitas*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="3d9b2-181">**Darbo šablono išsami informacija** skyriuje, atkreipkite dėmesį, kad tinklelis turi dvi egzistuojančias eilutes: vieną *Paėmimui* ir kitą *Padėjimui*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="3d9b2-182">**Darbo šablono išsami informacijos** skyriuje pasirinkite **Naujas** tam, kad įtrauktumėte eilutę kokybės kontrolei tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="3d9b2-183">Atkrepkite dėmesį, kad**Eilutės numeris** laukelis yra naujai eilutei nustatytai į *3*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="3d9b2-184">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-184">On the new line, set the following values.</span></span> <span data-ttu-id="3d9b2-185">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="3d9b2-186">**Darbo tipas:** *Kokybės patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="3d9b2-187">**Darbo klasės ID:** *Įsigijimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="3d9b2-188">**Kokybės tikrinimo šablono pavadinimas:** *Doko tikrinimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="3d9b2-189">Pasirinkite unikalųjį darbo klasės ID.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="3d9b2-190">Galite naudodami šią reikšmę konfigūruoti meniu elementus mobiliajame įrenginyje ir darbų, kuriuos tie meniu elementai gali apdoroti, tipus.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="3d9b2-191">Veiksmų juostoje pasirinkite **Įrašyti**, kad įrašytumėte savo darbą iki dabar.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="3d9b2-192">Gausite informacinį pranešimą sakantį „Negalima - kokybės patikra turi eiti iškart po paėmimo.“</span><span class="sxs-lookup"><span data-stu-id="3d9b2-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="3d9b2-193">Dėl to, privalote pakeisti **Eilutės numerio** vertę eilutei, kuri buvo kątik įtraukta.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="3d9b2-194">Atlikite šiuos žingsnius, kad pakeistumėte **Eilutės numerio** vertę naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="3d9b2-195">**Darbo šablono išsamios informacijos** skyriuje pasirinkite eilutę, kurioje **Darbo tipo** laukelis yra nustatytas į *Kokybės patikrinimas*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="3d9b2-196">Pasirinkite **Eiti aukštyn** ar **Eiti žemyn** mygtuką, kad judintumėte *Kokybės tikrinimo* eilutę taip, kad ji būtų po *Paėmimo* eilute.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="3d9b2-197">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="3d9b2-198">Kokybė kokybės patikrinime</span><span class="sxs-lookup"><span data-stu-id="3d9b2-198">Quality in quality check</span></span>

<span data-ttu-id="3d9b2-199">Po to, sukurkite darbo šabloną kokybės patikrai.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="3d9b2-200">**Darbo šablono** puslapio antraštėje, pakeiskite **Darbo užsakumo tipo** vertęs laukelį į *Kiekis kiekio tikrinime*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="3d9b2-201">Veiksmų juostoje pasirinkite **Naujas**tam, kad įtrauktumėte eilutę tinklelyje **Peržiūros** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="3d9b2-202">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-203">**Darbo šablonas:** *51 kokybės patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="3d9b2-204">Įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="3d9b2-205">**Darbo šablono aprašas:** *51 kokybės patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="3d9b2-206">Veiksmų juostoje pasirinkite **Įrašyti** tam, kad padarytumėte **Darbo šablono išsamios informacijos** skyrių prieinamą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="3d9b2-207">Kai naujas šablonas vis dar yra pasirinktas **Peržiūros** skyriuje, pasirinkite **Naujas** **Išsamiso darbo šablono informacijos** skyriuje, kad įtrauktumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="3d9b2-208">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-209">**Darbo tipas:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="3d9b2-210">**Darbo klasės ID:** *QC patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="3d9b2-211">Pasirinkite [darbo klasės](#work-class) pavadinimą, kurį sukūrėte anksčiau kokybės kontrolės darbui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="3d9b2-212">**Darbo šablono išsamios informacijos** skyriuje pasirinkite**Naujas** dar kartą, kad įtrauktumėte kitą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="3d9b2-213">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-214">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3d9b2-215">**Darbo klasės ID:** *QC patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="3d9b2-216">Pasirinkite [darbo klasės](#work-class) pavadinimą, kurį sukūrėte anksčiau kokybės kontrolės darbui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="3d9b2-217">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="3d9b2-218">Dėl išsamesnės informacijos apie darbo šablonus,, žr. [Sandėlio darbo valdymas naudojant darbo šablonus ir vietos direktyvas](control-warehouse-location-directives.md).</span><span class="sxs-lookup"><span data-stu-id="3d9b2-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="3d9b2-219">Vietos direktyva - Kokybės klaidos</span><span class="sxs-lookup"><span data-stu-id="3d9b2-219">Location directive – Quality failures</span></span>

<span data-ttu-id="3d9b2-220">Vietos nurodymai yra taisyklės, kurios padeda identifikuoti atsargų judėjimo paėmimo ir padėjimo vietas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="3d9b2-221">Pavyzdžiui, prekybos užsakymo perlaidoje, vietos direktyva nulemia, ar elementai bus paimami ir, kur paimti elementai turi būti padėti.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="3d9b2-222">Privalote konfigūruoti vietos direktyvos taisyklę, kad nustatytumėte, kaip nepavykusios kokybės patikros bus valdomos.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="3d9b2-223">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3d9b2-224">Kairiojoje juostoje, nustatykite **Darbo užsakymo tipo** laukelį į *Įsigijimo užsakymai* tam, kad dirbtumėte su to tipo vietos direktyvomis.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="3d9b2-225">Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte vietos direktyvą kokybės patikroms.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="3d9b2-226">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-227">**Sekos numeris:** Priimkite numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="3d9b2-228">**Pavadinimas:** *51 į kokybę*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="3d9b2-229">„FastTab“ skirtuke **Vietų nurodymai** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="3d9b2-230">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="3d9b2-231">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3d9b2-232">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-232">**Site:** *5*</span></span>
    - <span data-ttu-id="3d9b2-233">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="3d9b2-234">Veiksmų juostoje pasirinkite **Įrašyti** tam, kad įrašytumėte savo direktyvą ir padarytumėte **Eilutes** „FastTab“ prieinamą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="3d9b2-235">„FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3d9b2-236">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-236">On the new line, set the following values.</span></span> <span data-ttu-id="3d9b2-237">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="3d9b2-238">**Pradinis kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="3d9b2-239">**Galutinis kiekis:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="3d9b2-240">Veiksmų juostoje pasirinkite **Įrašyti** tam, kad įrašytumėte naują eilutę ir padarytumėte **Vietos direktyvos veiksmą** „FastTab“ prieinamą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="3d9b2-241">Kol nauja eilutę yra dar pasirinkta **Eilutės** „FastTab“, pasirinkite **Naujas** skyriuje **Vietos direktyvos veiksmai** „FastTab“ tam, kad įtrauktumėte eilutę į tinklelį taip, kad galėtumėte nustatyti veiksmą eilutei.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="3d9b2-242">Naujoje eilutėje, nustatykite**Pavadinimas** laukelį į *Kokybę*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="3d9b2-243">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="3d9b2-244">Veiksmų juostoje pasirinkite **Įrašyti** tam, kad padarytumėte **Redaguoti užklausą** mygtuką **Vietos direktyvos veiksmų** „FastTab“ prieinamą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="3d9b2-245">Kol jūsų kątik įtraukta eilutė vis dar yra pasirinkta **Vietos direktyvos veiksmuose** „FastTab“, pasirinkite **Redaguoti užklausą** tam, kad atidarytumėte teksto laukelį, kuriame galite redaguoti užklausą veiksmui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="3d9b2-246">**Intervalas** skirtuke, pasirinkite **Įtraukti** tam, kad įtrauktumėte eilutę į užklausą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="3d9b2-247">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-248">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="3d9b2-249">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="3d9b2-250">**Laukas:** *Vieta*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="3d9b2-251">**Kriterijai:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="3d9b2-252">*QMS* vieta yra sandėlio vietoje kokybei.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="3d9b2-253">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="3d9b2-254">Privalote pakeisti įsigijimo užsakymo vietos seką sandėlio direktyvoms *51*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="3d9b2-255">Pasirinkite naują *51 į kokybę* vietos direktyvą, atnaujinkite puslapį ir tuomet pasirinkite vietos direktyvą sąraše.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="3d9b2-256">Tuomet naudokite **Judinimo aukštyn** ir **Judinimo žemyn** mygtukus veiksmų juostoje, kad padėtumėte vietos direktyvą sandėliui *51* tokia tvarka.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="3d9b2-257">(Prieš pasirinkdami **Judėjimą aukštyn** ar **Judėjimą žemyn**, privalote pasirinkti vietos direktyvą sąraše.)</span><span class="sxs-lookup"><span data-stu-id="3d9b2-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="3d9b2-258">51 į kokybę</span><span class="sxs-lookup"><span data-stu-id="3d9b2-258">51 To Quality</span></span>
    2. <span data-ttu-id="3d9b2-259">51 PO Direct</span><span class="sxs-lookup"><span data-stu-id="3d9b2-259">51 PO Direct</span></span>
    3. <span data-ttu-id="3d9b2-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="3d9b2-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="3d9b2-261">Mobiliojo įrenginio meniu elementai</span><span class="sxs-lookup"><span data-stu-id="3d9b2-261">Mobile device menu items</span></span>

<span data-ttu-id="3d9b2-262">Konfigūruokite meniu elementą taip, kad mobilsu prietaisas galėtų atlikti **Kokybės tikrinimo** funkciją.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="3d9b2-263">Įsigijimo atidėjimas</span><span class="sxs-lookup"><span data-stu-id="3d9b2-263">Purchase putaway</span></span>

1. <span data-ttu-id="3d9b2-264">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3d9b2-265">Sąraše pasirinkite **Įsigijimo atidėjimo** meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="3d9b2-266">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3d9b2-267">**Darbo klasės** skyriuje pasirinkite**Naujas** tam, kad įtrauktumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="3d9b2-268">Naujoje eilutėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-269">**Darbo klasės ID:** *QC patikra*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="3d9b2-270">Įveskite [darbo klasės](#work-class) pavadinimą, kurį sukūrėte anksčiau kokybės kontrolės darbui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="3d9b2-271">**Darbo užsakymo tipas:** *Kokybė kokybės patikroje*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="3d9b2-272">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="3d9b2-273">Gaunama pirkimo užsakymo eilutė</span><span class="sxs-lookup"><span data-stu-id="3d9b2-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="3d9b2-274">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3d9b2-275">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3d9b2-276">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-277">**Meniu elemento pavadinimas:** *PU eilutės gavimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="3d9b2-278">**Pavadinimas:** *PU eilutės gavimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="3d9b2-279">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="3d9b2-280">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="3d9b2-281">Skirtuke **Bendra** „FastTab“, nustatykite tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="3d9b2-282">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="3d9b2-283">**Darbo sukūrimo procesas:** *Įsigijimo užsakymo linijos gavimas ir atidėjimas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="3d9b2-284">**Generuoti numerio lentelę:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="3d9b2-285">**Darbo šablonas:** *51 PO kvitas*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="3d9b2-286">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="3d9b2-287">Meniu elemento įtraukimas į mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="3d9b2-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="3d9b2-288">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="3d9b2-289">Kairiojoje juostoje, pasirinkite esamą **Vidaus** meniu.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="3d9b2-290">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3d9b2-291">**Esami meniu ar meniu elementai** stulpelyje pasirinkite naują **PO eilutės gavimo** meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="3d9b2-292">Pasirinkite dešinę rodyklės mygtuką, kad judintumėte **PO leilutės gavimą** į **Meniu struktūros** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="3d9b2-293">**Meniu struktūros** stulpelyje pasirinkite **PO eilutės gavimą** ir tuomet pasirinkite rodyklę aukštyn ar žemyn mygtuką tam, kad judintumėte meniu elemntus į norimą padėtį mobilaus prietaiso meniu.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="3d9b2-294">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="3d9b2-295">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="3d9b2-295">Example scenario</span></span>

<span data-ttu-id="3d9b2-296">Po to, kai atliksite visus anksčiau aprašytus pavyzdžio duomenis esančius ir nustatytus, galite dirbti su šiuo scenarijumis tam, kad bandytumėte *Kokybės tikrinimo* funkciją.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="3d9b2-297">Šiame scenarijuje rodomos vertės apima tai, kad jūs dirbate su standartiniais demonstraciniais duomenimis, kuriuos pasirinkote **USMF** teisiniame subjekte ir tai, kad rengiate pavyzdžio įrašus, kurie yra aprašyti anksčiau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="3d9b2-298">Scenarijus taip pat naudingas kaip pavyzdys rodantis, kaip funkcija gali būti naudojama gamybos parametruose.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="3d9b2-299">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="3d9b2-299">Create a purchase order</span></span>

1. <span data-ttu-id="3d9b2-300">Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="3d9b2-301">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3d9b2-302">Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-303">**Tiekėjo paskyra:** *104*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="3d9b2-304">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="3d9b2-305">Pasirinkite **Gerai** tam, kad uždarytumėte teksto laukelį ir atidarytumėte naują įsigijimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="3d9b2-306">**Įsigijimo užsakymo linijos** „FastTab“ tinklelis turi naują, tuščią liniją.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="3d9b2-307">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="3d9b2-308">**Prekės numeris:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="3d9b2-309">**Kiekis:** *3*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="3d9b2-310">**Vienetas:** *PL*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="3d9b2-311">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="3d9b2-312">Proceso kokybės tikrinimo gavimas</span><span class="sxs-lookup"><span data-stu-id="3d9b2-312">Process quality check receiving</span></span>

<span data-ttu-id="3d9b2-313">Po to, kai įsigijimo užsakymas buvo sukurtas, jis gali būti gaunamas naudojant **PO eilutės gavimo** meniu elementą ir *Kokybės tikrinimo* funkciją.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="3d9b2-314">Gauti padėklą 1</span><span class="sxs-lookup"><span data-stu-id="3d9b2-314">Receive pallet 1</span></span>

1. <span data-ttu-id="3d9b2-315">Prisijungti prie sandėlio programos kaip sandėlio naudotojas *51*.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="3d9b2-316">(Įveskite *51* kaip vartotojo ID ir *1* slaptažodį.)</span><span class="sxs-lookup"><span data-stu-id="3d9b2-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="3d9b2-317">Eikite į **Vidaus \> PO linijos gavimas**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="3d9b2-318">**PONUM** laukelį, įveskite įsigijimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="3d9b2-319">Patvirtinkite įsigijimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="3d9b2-320">**LINENUM** laukelyje įveskite įsigijimo užsakymo eilutės numerį, kuris yra gaunamas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="3d9b2-321">Kadangi užsakymas turi tik vieną eilutę šiame scenarijuje, jūs taip pat įvesite *1* **LINENUM** laukelyje kiekvienam gavimo žingsniui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="3d9b2-322">Patvirtinkite eilutės numerį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-322">Confirm the line number.</span></span>
1. <span data-ttu-id="3d9b2-323">**QTY** laukelyje įveskite gaunamą kiekį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="3d9b2-324">Kadangi įsigijimo užsakymas yra trims padėklams (*PL*) šiame scenarijuje ir esama trijų gavimo žingsnių, įvesite *1* **QTY** laukelyje kiekvienam gavimo žingsniui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="3d9b2-325">Patvirtinkite kiekį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-325">Confirm the quantity.</span></span>

    <span data-ttu-id="3d9b2-326">**Kokybės tikrinimo** puslapis pasirodo neturintis jokių įrašų laukelių.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="3d9b2-327">Jis turi tik patvirtinimą (žymimos žymės) mygtuką meniu mygtuko apačioje (**≡**) viršuje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="3d9b2-328">(Meniu mygtukas kartais vadinamas mėsainiu ar mėsainio mygtuku.) Jis skirtas tirti kokybės tikrinimo procesą, kai padėklai praeina kokybės tikrinimą, vartotojas tik patvirtina **Kokybės tikrinimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="3d9b2-329">![Kokybės patikros puslapis](media/quality-check.png "Kokybės patikros puslapis")</span><span class="sxs-lookup"><span data-stu-id="3d9b2-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="3d9b2-330">Pasirinkite patvirtinimo mygtuką, kad jis praeitų kokybės tikrinimą padėklui 1 eilutėje 1.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="3d9b2-331">**Įsigijimo užsakymai: Padėti** puslapis, kuris rodo informaciją apie paėjimo darbą:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="3d9b2-332">**LOC:** Sistemos nustatyta vieta</span><span class="sxs-lookup"><span data-stu-id="3d9b2-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="3d9b2-333">Ši vieta yra nustatyta gaunamo įsigijamo užsakymo atidėjimo vietai. </span><span class="sxs-lookup"><span data-stu-id="3d9b2-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="3d9b2-334">**LP:** Sistema kuria licencijos numerio ID</span><span class="sxs-lookup"><span data-stu-id="3d9b2-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="3d9b2-335">**Prekė:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="3d9b2-336">**Kiekis:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="3d9b2-337">Rodomas ir elemento aprašas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-337">The item description is also shown.</span></span>

1. <span data-ttu-id="3d9b2-338">Patvirtinkite atidėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="3d9b2-339">**Užduoties** puslapyje įsigijimo užsakymo linijos gavime, matysite „Darbas užbaigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="3d9b2-340">**LINENUM** laukelis yra prieinamas, todėl galite pradėti gauti kitą padėklą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="3d9b2-341">Gauti padėklą 2</span><span class="sxs-lookup"><span data-stu-id="3d9b2-341">Receive pallet 2</span></span>

<span data-ttu-id="3d9b2-342">Šiame scenarijuje antras padėklas bus atmestas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="3d9b2-343">**LINENUM** laukelyje, įveskite *1* ir patvirtinkite eilutės numerį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="3d9b2-344">**QTY** laukelis dabar prieinamas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-344">The **QTY** field is now available.</span></span> <span data-ttu-id="3d9b2-345">Įveskite *1* ir patvirinkite kiekį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="3d9b2-346">**Kokybės patikra** puslapis pasirodo.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-346">The **Quality check** page appears.</span></span> <span data-ttu-id="3d9b2-347">Dėl šio kvito, padėklas bus atmestas dėl kokybės ir bus padėtas į *QMS* kokybės vietą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="3d9b2-348">Pasirinkite meniu mygtuką (**≡**) puslapio viršuje ir tuomet meniu pasirinkite **Atsisakyti** grįžimui į meniu.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="3d9b2-349">**Užduoties** pasirodančiame puslapyje įveskite **QMS** kaip *Padėta* vietoje tam, kad siųstumėte padėklą tolesnei patikrai.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="3d9b2-350">**Kokybė kokybės patikroje: Padėti** puslapis, kuris rodo informaciją apie paėjimo darbą:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="3d9b2-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="3d9b2-352">Ši vieta yra nustatyta gaunamo įsigijamo užsakymo atšauktos kokybės gavimui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="3d9b2-353">**LP:** Sistema kuria licencijos numerio ID</span><span class="sxs-lookup"><span data-stu-id="3d9b2-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="3d9b2-354">**Prekė:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="3d9b2-355">**Kiekis:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="3d9b2-356">Rodomas ir elemento aprašas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-356">The item description is also shown.</span></span>

1. <span data-ttu-id="3d9b2-357">Patvirtinkite atidėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="3d9b2-358">**Užduoties** puslapyje įsigijimo užsakymo linijos gavime, matysite „Darbas užbaigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="3d9b2-359">**LINENUM** laukelis yra prieinamas, todėl galite pradėti gauti kitą padėklą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="3d9b2-360">Dabar baigėte kokybės tikrinimą ir sukūrėte kokybės užsakymą atsisakytam padėklui.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="3d9b2-361">Tam, kad peržiūrėtumėte sukurtą užsakymą, eikite į **Atsargų valymdas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="3d9b2-362">Kokybės užsakymo testavimas dabar gali būti pradėtas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="3d9b2-363">Kokybės testavimas nėra aptariamas šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="3d9b2-364">Dėl išsamesnės informacijos apie kokybės valdymą, žr. [Kokybės valdymo peržiūra](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="3d9b2-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="3d9b2-365">Gauti padėklą 3</span><span class="sxs-lookup"><span data-stu-id="3d9b2-365">Receive pallet 3</span></span>

<span data-ttu-id="3d9b2-366">Šiame scenarijuje trečias padėklas bus priimtas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="3d9b2-367">**LINENUM** laukelyje, įveskite *1* ir patvirtinkite eilutės numerį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="3d9b2-368">**QTY** laukelis dabar prieinamas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-368">The **QTY** field is now available.</span></span> <span data-ttu-id="3d9b2-369">Įveskite *1* ir patvirinkite kiekį.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="3d9b2-370">**Kokybės patikra** puslapis pasirodo.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-370">The **Quality check** page appears.</span></span> <span data-ttu-id="3d9b2-371">Dėl šio kvito, padėklas bus priimtas dėl kokybės ir bus padėtas į nesupakuotų krovinių atidėjimo vietą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="3d9b2-372">Pasirinkite patvirtinimo mygtuką, kad jis praeitų kokybės patikrą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="3d9b2-373">**Įsigijimo užsakymai: Padėti** puslapis, kuris rodo informaciją apie paėjimo darbą:</span><span class="sxs-lookup"><span data-stu-id="3d9b2-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="3d9b2-374">**LOC:** Sistemos nustatyta vieta</span><span class="sxs-lookup"><span data-stu-id="3d9b2-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="3d9b2-375">Ši vieta yra nustatyta gaunamo įsigijamo užsakymo atidėjimo vietai. </span><span class="sxs-lookup"><span data-stu-id="3d9b2-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="3d9b2-376">**LP:** Sistema kuria licencijos numerio ID</span><span class="sxs-lookup"><span data-stu-id="3d9b2-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="3d9b2-377">**Prekė:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="3d9b2-378">**Kiekis:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="3d9b2-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="3d9b2-379">Rodomas ir elemento aprašas.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-379">The item description is also shown.</span></span>

1. <span data-ttu-id="3d9b2-380">Patvirtinkite atidėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="3d9b2-381">**Užduoties** puslapyje įsigijimo užsakymo linijos gavime, matysite „Darbas užbaigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="3d9b2-382">**LINENUM** laukelis yra prieinamas, todėl galite pradėti gauti kitą padėklą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="3d9b2-383">Pasirinkite meniu mygtuką (**≡**) puslapio viršuje ir tuomet meniu pasirinkite **Atšaukti** grįžimui į meniu.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="3d9b2-384">Dabar galite uždaryti mobiliąją programą.</span><span class="sxs-lookup"><span data-stu-id="3d9b2-384">You can now close the mobile app.</span></span>
