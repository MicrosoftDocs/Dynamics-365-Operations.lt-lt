---
title: Nustatyti pirkimo užsakymų darbo šabloną
description: Ši procedūra sutelkta į paprasto darbo šablono nustatymą, kuris bus naudojamas padedant gautas prekes.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "318033"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="bfa18-103">Nustatyti pirkimo užsakymų darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="bfa18-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bfa18-104">Ši procedūra sutelkta į paprasto darbo šablono nustatymą, kuris bus naudojamas padedant gautas prekes.</span><span class="sxs-lookup"><span data-stu-id="bfa18-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="bfa18-105">Darbo šablonai nustato instrukcijų rinkinį, pateiktą sandėlio darbuotojui mobiliajame įrenginyje, perkeliant prekes iš gavimo srities.</span><span class="sxs-lookup"><span data-stu-id="bfa18-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="bfa18-106">Šią procedūrą galite naudoti su demonstracinių duomenų įmonės USMF nurodytais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="bfa18-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="bfa18-107">Prieš paleisdami šį vadovą, sukurkite darbo telkinio ID.</span><span class="sxs-lookup"><span data-stu-id="bfa18-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="bfa18-108">Šiame pavyzdyje naudojamas darbo telkinio ID, iškviestas iš Gaunama.</span><span class="sxs-lookup"><span data-stu-id="bfa18-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="bfa18-109">Ši procedūra skirta sandėlio vadovui.</span><span class="sxs-lookup"><span data-stu-id="bfa18-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="bfa18-110">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="bfa18-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="bfa18-111">Lauke Darbo užsakymo tipas pasirinkite „Pirkimo užsakymai“.</span><span class="sxs-lookup"><span data-stu-id="bfa18-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="bfa18-112">Sukurti darbo šablono antraštę</span><span class="sxs-lookup"><span data-stu-id="bfa18-112">Create a work template header</span></span>
1. <span data-ttu-id="bfa18-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bfa18-113">Click New.</span></span>
2. <span data-ttu-id="bfa18-114">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bfa18-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bfa18-115">Tai seka, pagal kurią yra vertinami darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="bfa18-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="bfa18-116">Seką, jei reikia, galite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="bfa18-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="bfa18-117">Lauke „Darbo šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bfa18-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="bfa18-118">Tai unikalus šio šablono identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="bfa18-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="bfa18-119">Lauke Darbo šablonas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="bfa18-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="bfa18-120">Pasirinktis Galiojantis nebus pažymėta tol, kol užpildysite visą informaciją, kuri yra reikalinga pagal šabloną, ir spustelėsite įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bfa18-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="bfa18-121">Pirkimo užsakymo tipo darbo užsakymo negalima automatiškai apdoroti, todėl pasirinktį Automatiškai apdoroti palikite nustatytą kaip Ne.</span><span class="sxs-lookup"><span data-stu-id="bfa18-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="bfa18-122">Lauke Darbo telkinio ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="bfa18-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="bfa18-123">Darbo telkinio ID leidžia skirstyti darbą į grupes.</span><span class="sxs-lookup"><span data-stu-id="bfa18-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="bfa18-124">Čia nustatyta vertė bus bet kurio darbo, sukurto naudojant šį šabloną, numatytoji vertė.</span><span class="sxs-lookup"><span data-stu-id="bfa18-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="bfa18-125">Lauke Darbo prioritetas įveskite '1'.</span><span class="sxs-lookup"><span data-stu-id="bfa18-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="bfa18-126">Tai nurodo darbo svarbą, o čia nustatyta vertė bus kiekvieno darbo, sukurto naudojant šį šabloną, numatytoji vertė.</span><span class="sxs-lookup"><span data-stu-id="bfa18-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="bfa18-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bfa18-127">Click Save.</span></span>
    * <span data-ttu-id="bfa18-128">Pirma turite įrašyti darbo šablono antraštę, tik tada galimas mygtukas Redaguoti užklausą.</span><span class="sxs-lookup"><span data-stu-id="bfa18-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="bfa18-129">Nustatyti darbo šablono užklausą</span><span class="sxs-lookup"><span data-stu-id="bfa18-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="bfa18-130">Spustelėkite Redaguoti užklausą.</span><span class="sxs-lookup"><span data-stu-id="bfa18-130">Click Edit query.</span></span>
    * <span data-ttu-id="bfa18-131">Mes nustatysime apribojimą, pagal kurį šablonas gali būti naudojamas tik tam tikrame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="bfa18-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="bfa18-132">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bfa18-132">Click Add.</span></span>
3. <span data-ttu-id="bfa18-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bfa18-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bfa18-134">Lauke Laukas įveskite 'sandėlis'.</span><span class="sxs-lookup"><span data-stu-id="bfa18-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="bfa18-135">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bfa18-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="bfa18-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bfa18-136">Click OK.</span></span>
7. <span data-ttu-id="bfa18-137">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="bfa18-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="bfa18-138">Nustatyti darbo šablono informaciją</span><span class="sxs-lookup"><span data-stu-id="bfa18-138">Set work template details</span></span>
1. <span data-ttu-id="bfa18-139">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bfa18-139">Click New.</span></span>
2. <span data-ttu-id="bfa18-140">Lauke Darbo tipas pasirinkite 'Paimti'.</span><span class="sxs-lookup"><span data-stu-id="bfa18-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="bfa18-141">Lauke Darbo klasės ID įveskite 'pirkimas'.</span><span class="sxs-lookup"><span data-stu-id="bfa18-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="bfa18-142">Čia nustatyta darbo klasė bus numatytoji visose paėmimo tipo darbo eilutėse, kurios sukurtos naudojant šį šabloną.</span><span class="sxs-lookup"><span data-stu-id="bfa18-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="bfa18-143">Darbo klasės negalima nepaisyti darbo užsakymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="bfa18-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="bfa18-144">Darbo klasės naudojamos nukreipti ir (arba) apriboti darbo tipo užsakymo eilutes, kurias sandėlio darbuotojas gali apdoroti mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="bfa18-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="bfa18-145">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bfa18-145">Click New.</span></span>
5. <span data-ttu-id="bfa18-146">Lauke Darbo tipas pasirinkite „Padėjimas“.</span><span class="sxs-lookup"><span data-stu-id="bfa18-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="bfa18-147">Lauke Darbo klasės ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bfa18-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="bfa18-148">Paėmimo ir padėjimo instrukcijos yra rinkinys.</span><span class="sxs-lookup"><span data-stu-id="bfa18-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="bfa18-149">Kiekvienas paėmimo / padėjimo rinkinys turi būti tos pačios darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="bfa18-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="bfa18-150">Naudokite tą pačią darbo klasę, kurią nurodėte paėmimo instrukcijoje.</span><span class="sxs-lookup"><span data-stu-id="bfa18-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="bfa18-151">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bfa18-151">Click Save.</span></span>
    * <span data-ttu-id="bfa18-152">Atkreipkite dėmesį, kad dabar žymės langelis Galiojantis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="bfa18-152">Note that the Valid checkbox is now checked.</span></span>  

