---
title: Gedimų valdymas
description: Šioje temoje aiškinamas gedimų valdymas modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 48c90a8b776cc16804de8e20ada7d8ca347fa5b9
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874744"
---
# <a name="fault-management"></a><span data-ttu-id="bdd60-103">Gedimų valdymas</span><span class="sxs-lookup"><span data-stu-id="bdd60-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bdd60-104">Modulyje Turto valdymas gedimų dizaino įrankiu galite nustatyti turto tipų gedimų požymius, gedimų sritis ir gedimų tipus.</span><span class="sxs-lookup"><span data-stu-id="bdd60-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="bdd60-105">Taip galite valdyti rastus turto gedimus.</span><span class="sxs-lookup"><span data-stu-id="bdd60-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="bdd60-106">Be to, gedimų priežastis ir pasiūlymus dėl gedimų pašalinimo galima užregistruoti darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="bdd60-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="bdd60-107">Gedimų registravimo ir valdymo procesą sudaro toliau pateikiami veiksmai.</span><span class="sxs-lookup"><span data-stu-id="bdd60-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="bdd60-108">Sukurkite turto tipų galimus gedimų požymius, gedimų sritis ir gedimų tipus.</span><span class="sxs-lookup"><span data-stu-id="bdd60-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="bdd60-109">Gedimų dizaino įrankiu nustatykite turto tipų gedimų požymius, gedimų sritis ir gedimų tipus.</span><span class="sxs-lookup"><span data-stu-id="bdd60-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="bdd60-110">Toliau pateikiama pavyzdžių, padėsiančių suprasti skirtumą tarp gedimų požymių, gedimų sričių ir gedimų tipų.</span><span class="sxs-lookup"><span data-stu-id="bdd60-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="bdd60-111">**Gedimų požymiai.**</span><span class="sxs-lookup"><span data-stu-id="bdd60-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="bdd60-112">Įtampų disbalansas</span><span class="sxs-lookup"><span data-stu-id="bdd60-112">Unbalanced voltages</span></span>
- <span data-ttu-id="bdd60-113">Trumpasis jungimas</span><span class="sxs-lookup"><span data-stu-id="bdd60-113">Short circuit</span></span>
- <span data-ttu-id="bdd60-114">Triukšmas</span><span class="sxs-lookup"><span data-stu-id="bdd60-114">Noise</span></span>
- <span data-ttu-id="bdd60-115">Nuotėkis</span><span class="sxs-lookup"><span data-stu-id="bdd60-115">Leak</span></span>
- <span data-ttu-id="bdd60-116">Vibracija</span><span class="sxs-lookup"><span data-stu-id="bdd60-116">Vibrations</span></span>

<span data-ttu-id="bdd60-117">**Gedimų sritys.**</span><span class="sxs-lookup"><span data-stu-id="bdd60-117">**Fault areas:**</span></span>

- <span data-ttu-id="bdd60-118">Elektra</span><span class="sxs-lookup"><span data-stu-id="bdd60-118">Electrical</span></span>
- <span data-ttu-id="bdd60-119">Mechanika</span><span class="sxs-lookup"><span data-stu-id="bdd60-119">Mechanical</span></span>
- <span data-ttu-id="bdd60-120">Hidraulika</span><span class="sxs-lookup"><span data-stu-id="bdd60-120">Hydraulic</span></span>
- <span data-ttu-id="bdd60-121">Pneumatika</span><span class="sxs-lookup"><span data-stu-id="bdd60-121">Pneumatic</span></span>

<span data-ttu-id="bdd60-122">**Gedimų tipai.**</span><span class="sxs-lookup"><span data-stu-id="bdd60-122">**Fault types:**</span></span>

- <span data-ttu-id="bdd60-123">Sugedusi pagrindinė statoriaus apvija</span><span class="sxs-lookup"><span data-stu-id="bdd60-123">Faulty main stator winding</span></span>
- <span data-ttu-id="bdd60-124">Sugedęs diodas</span><span class="sxs-lookup"><span data-stu-id="bdd60-124">Faulty diode</span></span>
- <span data-ttu-id="bdd60-125">Nešvarios apvijos</span><span class="sxs-lookup"><span data-stu-id="bdd60-125">Dirty windings</span></span>
- <span data-ttu-id="bdd60-126">Sugedęs generatorius</span><span class="sxs-lookup"><span data-stu-id="bdd60-126">Defective generator</span></span>
- <span data-ttu-id="bdd60-127">Sugedęs jutiklis</span><span class="sxs-lookup"><span data-stu-id="bdd60-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="bdd60-128">Gedimų požymių kūrimas</span><span class="sxs-lookup"><span data-stu-id="bdd60-128">Create fault symptoms</span></span>

<span data-ttu-id="bdd60-129">Atlikite toliau pateikiamus veiksmus, norėdami sukurti požymių sąrašą, kurį galima naudoti gedimų dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="bdd60-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="bdd60-130">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų požymiai**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="bdd60-131">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="bdd60-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="bdd60-132">Lauke **Gedimo požymis** įveskite gedimo požymio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="bdd60-133">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="bdd60-134">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="bdd60-135">Gedimų sričių kūrimas</span><span class="sxs-lookup"><span data-stu-id="bdd60-135">Create fault areas</span></span>

<span data-ttu-id="bdd60-136">Atlikite toliau pateikiamus veiksmus, norėdami sukurti sričių arba vietų sąrašą, kurį galima naudoti gedimų dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="bdd60-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="bdd60-137">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų sritys**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="bdd60-138">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="bdd60-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="bdd60-139">Lauke **Gedimo sritis** įveskite gedimo srities pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="bdd60-140">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="bdd60-141">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="bdd60-142">Gedimų tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="bdd60-142">Create fault types</span></span>

<span data-ttu-id="bdd60-143">Atlikite toliau pateikiamus veiksmus, norėdami sukurti gedimų tipų sąrašą, kurį galima naudoti gedimų dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="bdd60-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="bdd60-144">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų tipai**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="bdd60-145">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="bdd60-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="bdd60-146">Lauke **Gedimo tipas** įveskite gedimo tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="bdd60-147">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="bdd60-148">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="bdd60-149">Gedimų dizaino įrankio nustatymas</span><span class="sxs-lookup"><span data-stu-id="bdd60-149">Set up the fault designer</span></span>

<span data-ttu-id="bdd60-150">Gedimų dizaino įrankiu nustatomi turto tipų gedimų duomenys.</span><span class="sxs-lookup"><span data-stu-id="bdd60-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="bdd60-151">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="bdd60-152">Kairiojoje srityje pasirinkite turto tipą, kuriam norite sukurti gedimų įrašą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="bdd60-153">FastTab **Gedimo požymis** pasirinkite **Įtraukti eilutę**, paskui lauke **Gedimo požymis** pasirinkite gedimo požymį.</span><span class="sxs-lookup"><span data-stu-id="bdd60-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="bdd60-154">FastTab **Gedimo sritis** pasirinkite **Įtraukti eilutę**, paskui lauke **Gedimo sritis** pasirinkite gedimo sritį.</span><span class="sxs-lookup"><span data-stu-id="bdd60-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="bdd60-155">FastTab **Gedimo tipas** pasirinkite **Įtraukti eilutę**, paskui lauke **Gedimo tipas** pasirinkite gedimo tipą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="bdd60-156">Greitai sukurkite pasirinkto turto tipo visų esamų gedimų požymių, sričių ir tipų derinius, pasirinkę **Kurti gedimų derinius**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="bdd60-157">Ši funkcija naudinga, jei įtraukėte daug gedimų požymių, sričių ir tipų.</span><span class="sxs-lookup"><span data-stu-id="bdd60-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="bdd60-158">Paprasčiau panaikinti turto tipui neaktualias derinių eilutes, nei rankiniu būdu sukurti naujų eilučių.</span><span class="sxs-lookup"><span data-stu-id="bdd60-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bdd60-159">Nukopijuokite gedimų požymių, sričių ir tipų sąranką iš vieno turto tipo į pasirinktą turto tipą, pasirinkę **Kopijuoti iš turto tipo**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="bdd60-160">Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="bdd60-160">Select **Save** to save your changes.</span></span>

![1 pav.](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="bdd60-162">Gedimų priežasčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="bdd60-162">Create fault causes</span></span>

<span data-ttu-id="bdd60-163">Atlikite toliau pateikiamus veiksmus, norėdami sukurti žinomų gedimų priežasčių sąrašą, kurį galima įtraukti į darbo užsakymą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="bdd60-164">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų priežastys**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="bdd60-165">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="bdd60-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="bdd60-166">Lauke **Gedimo priežastis** įveskite gedimo priežasties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="bdd60-167">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="bdd60-168">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="bdd60-169">Gedimų šalinimo priemonių kūrimas</span><span class="sxs-lookup"><span data-stu-id="bdd60-169">Create fault remedies</span></span>

<span data-ttu-id="bdd60-170">Atlikite toliau pateikiamus veiksmus, norėdami sukurti pasiūlymų dėl gedimų šalinimo ir remonto sąrašą, kurį galima įtraukti į darbo užsakymą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="bdd60-171">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Gedimas** \> **Gedimų šalinimo priemonės**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="bdd60-172">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="bdd60-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="bdd60-173">Lauke **Gedimo šalinimo priemonė** įveskite gedimo šalinimo priemonės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="bdd60-174">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bdd60-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="bdd60-175">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bdd60-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="bdd60-176">Jei reikia, galite pakeisti gedimų požymių, sričių, tipų, priežasčių ir šalinimo priemonių pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="bdd60-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="bdd60-177">Pavadinimo pakeitimai automatiškai fiksuojami atitinkamo gedimo registracijos įrašuose.</span><span class="sxs-lookup"><span data-stu-id="bdd60-177">The name changes are automatically reflected in the related fault registrations.</span></span>
