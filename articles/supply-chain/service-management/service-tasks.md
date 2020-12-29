---
title: Aptarnavimo užduočių apžvalga
description: Norėdami aprašyti aptarnavimo užsakymo metu turimą atlikti užduotį naudokite aptarnavimo užduotis. Šią informaciją gali matyti ir technikai, ir klientai.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b433632523bfd64119fda62f8e4b108ff9b5dccd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433275"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="21f1c-104">Aptarnavimo užduočių apžvalga</span><span class="sxs-lookup"><span data-stu-id="21f1c-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21f1c-105">Norėdami aprašyti aptarnavimo užsakymo metu turimą atlikti užduotį naudokite aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="21f1c-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="21f1c-106">Šią informaciją gali matyti ir technikai, ir klientai.</span><span class="sxs-lookup"><span data-stu-id="21f1c-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="21f1c-107">Aptarnavimo užduotis galite kurti puslapyje **Aptarnavimo užduotys** ir aptarnavimo užduotis galite susieti su tam tikra aptarnavimo sutartimi arba aptarnavimo užsakymu sukurdami aptarnavimo užduočių ryšius.</span><span class="sxs-lookup"><span data-stu-id="21f1c-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="21f1c-108">Kiekvieną kartą sukūrę aptarnavimo užduoties ryšį, galite sukurti:</span><span class="sxs-lookup"><span data-stu-id="21f1c-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="21f1c-109">Vidines užduoties pastabas, tokias kaip smulkios techninės užklausos, kurios yra svarbios technikui.</span><span class="sxs-lookup"><span data-stu-id="21f1c-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="21f1c-110">Išorinės pastabos, kurias gali matyti klientas.</span><span class="sxs-lookup"><span data-stu-id="21f1c-110">External notes that the customer can see.</span></span> <span data-ttu-id="21f1c-111">Jose gali būti ne taip techniškai paaiškinta pagal sutartį tarp kliento ir aptarnavimo įmonės atliekama užduotis.</span><span class="sxs-lookup"><span data-stu-id="21f1c-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="21f1c-112">Sukūrę aptarnavimo užduoties ryšį tarp aptarnavimo užduoties ir aptarnavimo užsakymo arba aptarnavimo sutarties, galite nurodyti šią aptarnavimo užduotį kurdami aptarnavimo užsakymo eilutes arba aptarnavimo sutarties eilutes esamam aptarnavimo užsakymui ar aptarnavimo sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="21f1c-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="21f1c-113">Kurdami aptarnavimo užsakymus iš aptarnavimo sutarties, galite naudoti kiekvienai aptarnavimo sutarties eilutei priskirtas aptarnavimo užduotis, kad sugrupuotumėte aptarnavimo užsakymo eilutes į aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="21f1c-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="21f1c-114">Aptarnavimo užduoties kūrimas</span><span class="sxs-lookup"><span data-stu-id="21f1c-114">Create a service task</span></span>

1. <span data-ttu-id="21f1c-115">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="21f1c-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="21f1c-116">Sukurkite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="21f1c-116">Create a new line.</span></span>
3. <span data-ttu-id="21f1c-117">Įveskite aptarnavimo ID ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="21f1c-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="21f1c-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="21f1c-118">Example</span></span>

<span data-ttu-id="21f1c-119">Technikas privalo atlikti dvi pavarų dėžės užduotis (aptarnavimo objektas GB-1234) kliento patalpose.</span><span class="sxs-lookup"><span data-stu-id="21f1c-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="21f1c-120">Klientui sukuriama aptarnavimo sutartis ir su užduotimis susiejamos kelios operacijos.</span><span class="sxs-lookup"><span data-stu-id="21f1c-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="21f1c-121">Aptarnavimo sutartis ir aptarnavimo sutarties eilutės šioms dviem užduotims parodytos čia:</span><span class="sxs-lookup"><span data-stu-id="21f1c-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="21f1c-122">Aptarnavimo sutartis</span><span class="sxs-lookup"><span data-stu-id="21f1c-122">Service agreement</span></span>

| <span data-ttu-id="21f1c-123">Project</span><span class="sxs-lookup"><span data-stu-id="21f1c-123">Project</span></span> | <span data-ttu-id="21f1c-124">Aptarnavimo sutartis</span><span class="sxs-lookup"><span data-stu-id="21f1c-124">Service agreement</span></span> | <span data-ttu-id="21f1c-125">aprašymas</span><span class="sxs-lookup"><span data-stu-id="21f1c-125">Description</span></span>                                  | <span data-ttu-id="21f1c-126">Grupuoti</span><span class="sxs-lookup"><span data-stu-id="21f1c-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="21f1c-127">9012</span><span class="sxs-lookup"><span data-stu-id="21f1c-127">9012</span></span>    | <span data-ttu-id="21f1c-128">000008 \_ 001</span><span class="sxs-lookup"><span data-stu-id="21f1c-128">000008\_001</span></span>       | <span data-ttu-id="21f1c-129">Patikrinimas ir programos pakeitimas – GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="21f1c-130">Priedas</span><span class="sxs-lookup"><span data-stu-id="21f1c-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="21f1c-131">Aptarnavimo sutarties eilutės</span><span class="sxs-lookup"><span data-stu-id="21f1c-131">Service agreement lines</span></span>

| <span data-ttu-id="21f1c-132">aprašymas</span><span class="sxs-lookup"><span data-stu-id="21f1c-132">Description</span></span>             | <span data-ttu-id="21f1c-133">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="21f1c-133">Transaction type</span></span> | <span data-ttu-id="21f1c-134">Aptarnavimo objektas</span><span class="sxs-lookup"><span data-stu-id="21f1c-134">Service object</span></span> | <span data-ttu-id="21f1c-135">Aptarnavimo užduotis</span><span class="sxs-lookup"><span data-stu-id="21f1c-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="21f1c-136">Patikrinimas ir valymas</span><span class="sxs-lookup"><span data-stu-id="21f1c-136">Inspection and cleaning</span></span> | <span data-ttu-id="21f1c-137">Valanda</span><span class="sxs-lookup"><span data-stu-id="21f1c-137">Hour</span></span>             | <span data-ttu-id="21f1c-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-138">GB-1234</span></span>        | <span data-ttu-id="21f1c-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-139">I/C - GB1234</span></span> |
| <span data-ttu-id="21f1c-140">Kelionė</span><span class="sxs-lookup"><span data-stu-id="21f1c-140">Travel</span></span>                  | <span data-ttu-id="21f1c-141">Expense</span><span class="sxs-lookup"><span data-stu-id="21f1c-141">Expense</span></span>          | <span data-ttu-id="21f1c-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-142">GB-1234</span></span>        | <span data-ttu-id="21f1c-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-143">I/C - GB1234</span></span> |
| <span data-ttu-id="21f1c-144">Medžiagos</span><span class="sxs-lookup"><span data-stu-id="21f1c-144">Materials</span></span>               | <span data-ttu-id="21f1c-145">Produktas</span><span class="sxs-lookup"><span data-stu-id="21f1c-145">Item</span></span>             | <span data-ttu-id="21f1c-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-146">GB-1234</span></span>        | <span data-ttu-id="21f1c-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-147">I/C - GB1234</span></span> |
| <span data-ttu-id="21f1c-148">Programos pakeitimas</span><span class="sxs-lookup"><span data-stu-id="21f1c-148">Routine replacement</span></span>     | <span data-ttu-id="21f1c-149">Valanda</span><span class="sxs-lookup"><span data-stu-id="21f1c-149">Hour</span></span>             | <span data-ttu-id="21f1c-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-150">GB-1234</span></span>        | <span data-ttu-id="21f1c-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-151">RR - GB1234</span></span>  |
| <span data-ttu-id="21f1c-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="21f1c-152">GR-1</span></span>                    | <span data-ttu-id="21f1c-153">Produktas</span><span class="sxs-lookup"><span data-stu-id="21f1c-153">Item</span></span>             | <span data-ttu-id="21f1c-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-154">GB-1234</span></span>        | <span data-ttu-id="21f1c-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-155">RR - GB1234</span></span>  |
| <span data-ttu-id="21f1c-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="21f1c-156">GR-5</span></span>                    | <span data-ttu-id="21f1c-157">Produktas</span><span class="sxs-lookup"><span data-stu-id="21f1c-157">Item</span></span>             | <span data-ttu-id="21f1c-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-158">GB-1234</span></span>        | <span data-ttu-id="21f1c-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-159">RR - GB1234</span></span>  |

<span data-ttu-id="21f1c-160">Dviejų užduočių aptarnavimo sutarčių eilutės turi dvi prie jų pridėtas aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="21f1c-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="21f1c-161">Aptarnavimo užduotys apibrėžia kiekvienai užduočiai priklausančias operacijas.</span><span class="sxs-lookup"><span data-stu-id="21f1c-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="21f1c-162">Pirmuoju atveju aptarnavimo užduotis I/C - GB1234 identifikuoja visas aptarnavimo sutarties eilutes, kurios yra susijusios su objekto GB-1234 patikrinimu ir valymu.</span><span class="sxs-lookup"><span data-stu-id="21f1c-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="21f1c-163">Antruoju atveju aptarnavimo užduotis RR - GB1234 identifikuoja visas aptarnavimo sutarties eilutes, kurios yra susijusios su planinio pakeitimo užduoties įvykdymu.</span><span class="sxs-lookup"><span data-stu-id="21f1c-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="21f1c-164">Aptarnavimo užduoties ryšiai, jungiantys aptarnavimo užduotis su tam tikra sutartimi yra tokie:</span><span class="sxs-lookup"><span data-stu-id="21f1c-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="21f1c-165">Aptarnavimo užduotys</span><span class="sxs-lookup"><span data-stu-id="21f1c-165">Service tasks</span></span>

| <span data-ttu-id="21f1c-166">Aptarnavimo užduotis</span><span class="sxs-lookup"><span data-stu-id="21f1c-166">Service task</span></span> | <span data-ttu-id="21f1c-167">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="21f1c-167">Description</span></span>                             | <span data-ttu-id="21f1c-168">Vidinė pastaba</span><span class="sxs-lookup"><span data-stu-id="21f1c-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="21f1c-169">Išorinė pastaba</span><span class="sxs-lookup"><span data-stu-id="21f1c-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="21f1c-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-170">I/C - GB1234</span></span> | <span data-ttu-id="21f1c-171">Pavarų dėžės GB-1234 patikrinimas</span><span class="sxs-lookup"><span data-stu-id="21f1c-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="21f1c-172">GB-1234 pavarų dėžės apžiūra ir mechaninis patikrinimas bei valymas.</span><span class="sxs-lookup"><span data-stu-id="21f1c-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="21f1c-173">Planinis pavarų dėžės patikrinimas</span><span class="sxs-lookup"><span data-stu-id="21f1c-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="21f1c-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="21f1c-174">RR - GB1234</span></span>  | <span data-ttu-id="21f1c-175">Planinis GB-1234 dalių pakeitimas</span><span class="sxs-lookup"><span data-stu-id="21f1c-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="21f1c-176">Planinis aptarnavimo GR-1 ir GR-5 komponentų pakeitimas (iki 2002 m. pagamintoms pavarų dėžėms taip pat pakeiskite GR-2 komponentą)</span><span class="sxs-lookup"><span data-stu-id="21f1c-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="21f1c-177">Planinis dalių pakeitimas</span><span class="sxs-lookup"><span data-stu-id="21f1c-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="21f1c-178">Grupuoti aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="21f1c-178">Group service orders</span></span>

<span data-ttu-id="21f1c-179">Automatiškai kurdami aptarnavimo užsakymus, aptarnavimo užduotis galite naudoti kaip grupavimo kriterijų.</span><span class="sxs-lookup"><span data-stu-id="21f1c-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="21f1c-180">Norėdami sugrupuoti aptarnavimo užsakymus, aptarnavimo sutartyje nurodykite, kad pagal aptarnavimo sutartį atliekami aptarnavimo užsakymai turi būti grupuojami pagal aptarnavimo užduoties ID, laikant pastarąjį jų pradiniu grupavimo kriterijumi.</span><span class="sxs-lookup"><span data-stu-id="21f1c-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="21f1c-181">**Grupavimas pagal aptarnavimo užduotį**</span><span class="sxs-lookup"><span data-stu-id="21f1c-181">**Group by service task**</span></span>

1. <span data-ttu-id="21f1c-182">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="21f1c-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="21f1c-183">Skirtuke **Sąranka** pasirinkite laukelyje **Jungti aptarnavimo užsakymus** esantį kriterijų **Pagal aptarnavimo užduotį**.</span><span class="sxs-lookup"><span data-stu-id="21f1c-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


