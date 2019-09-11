---
title: Pirkimo užsakymų darbo šablono nustatymas
description: Šioje temoje aprašyta, kaip nustatyti paprastą darbo šabloną, kuris bus naudojamas atidedant gautas prekes.
author: ShylaThompson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 227a6865df826caf8ce154f9c44ebe082acd76a5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916746"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="ace66-103">Pirkimo užsakymų darbo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="ace66-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ace66-104">Šioje temoje aprašyta, kaip nustatyti paprastą darbo šabloną, kuris bus naudojamas atidedant gautas prekes.</span><span class="sxs-lookup"><span data-stu-id="ace66-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="ace66-105">Darbo šablonai nustato instrukcijų rinkinį, pateiktą sandėlio darbuotojui mobiliajame įrenginyje, perkeliant prekes iš gavimo srities.</span><span class="sxs-lookup"><span data-stu-id="ace66-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="ace66-106">Šią procedūrą galite naudoti su demonstracinių duomenų įmonės USMF nurodytais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="ace66-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="ace66-107">Prieš paleisdami šį vadovą, sukurkite darbo telkinio ID.</span><span class="sxs-lookup"><span data-stu-id="ace66-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="ace66-108">Šiame pavyzdyje naudojamas darbo telkinio ID, iškviestas iš Gaunama.</span><span class="sxs-lookup"><span data-stu-id="ace66-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="ace66-109">Ši procedūra skirta sandėlio vadovui.</span><span class="sxs-lookup"><span data-stu-id="ace66-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="ace66-110">Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Darbas > Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ace66-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="ace66-111">Lauke **Darbo užsakymo tipas** pasirinkite **Pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ace66-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="ace66-112">Sukurti darbo šablono antraštę</span><span class="sxs-lookup"><span data-stu-id="ace66-112">Create a work template header</span></span>
1. <span data-ttu-id="ace66-113">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ace66-113">Select **New**.</span></span>
2. <span data-ttu-id="ace66-114">Lauke **Sekos skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ace66-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="ace66-115">Tai seka, pagal kurią yra vertinami darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="ace66-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="ace66-116">Seką, jei reikia, galite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="ace66-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="ace66-117">Lauke **Darbo šablonas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ace66-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="ace66-118">Tai unikalus šio šablono identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="ace66-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="ace66-119">Lauke **Darbo šablono aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ace66-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="ace66-120">Parinktis **Galioja** nebus pažymėta tol, kol neįvesite visos šablonui reikalingos informacijos ir nepažymėsite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ace66-120">The **Valid** option will not be checked until you’ve completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="ace66-121">Darbo užsakymo, kurio tipas yra **Pirkimo užsakymas**, automatiškai apdoroti negalima, todėl palikite parinkties **Apdoroti automatiškai** nuostatą **Ne**.</span><span class="sxs-lookup"><span data-stu-id="ace66-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="ace66-122">Lauke **Darbo telkinio ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ace66-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="ace66-123">Darbo telkinio ID leidžia skirstyti darbą į grupes.</span><span class="sxs-lookup"><span data-stu-id="ace66-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="ace66-124">Čia nustatyta vertė bus bet kurio darbo, sukurto naudojant šį šabloną, numatytoji vertė.</span><span class="sxs-lookup"><span data-stu-id="ace66-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="ace66-125">Lauke **Darbo prioritetas** įveskite `1`.</span><span class="sxs-lookup"><span data-stu-id="ace66-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="ace66-126">Tai nurodo darbo svarbą, o čia nustatyta vertė bus kiekvieno darbo, sukurto naudojant šį šabloną, numatytoji vertė.</span><span class="sxs-lookup"><span data-stu-id="ace66-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="ace66-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ace66-127">Select **Save**.</span></span> <span data-ttu-id="ace66-128">Reikia įrašyti darbo šablono antraštę, kad mygtukas **Redaguoti užklausą** taptų pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="ace66-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="ace66-129">Nustatyti darbo šablono užklausą</span><span class="sxs-lookup"><span data-stu-id="ace66-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="ace66-130">Pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="ace66-130">Select **Edit query**.</span></span> <span data-ttu-id="ace66-131">Mes nustatysime apribojimą, pagal kurį šablonas gali būti naudojamas tik tam tikrame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="ace66-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="ace66-132">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="ace66-132">Select **Add**.</span></span>
3. <span data-ttu-id="ace66-133">Naujos eilutės lauke **Laukas** įveskite `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="ace66-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="ace66-134">Lauke **Kriterijai** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ace66-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="ace66-135">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ace66-135">Select **OK**.</span></span>
6. <span data-ttu-id="ace66-136">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ace66-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="ace66-137">Nustatyti darbo šablono informaciją</span><span class="sxs-lookup"><span data-stu-id="ace66-137">Set work template details</span></span>
1. <span data-ttu-id="ace66-138">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ace66-138">Select **New**.</span></span>
2. <span data-ttu-id="ace66-139">Lauke **Darbo tipas** pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="ace66-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="ace66-140">Lauke **Darbo klasės ID** įrašykite `purchase`.</span><span class="sxs-lookup"><span data-stu-id="ace66-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="ace66-141">Čia nustatyta darbo klasė bus numatytoji visose paėmimo tipo darbo eilutėse, kurios sukurtos naudojant šį šabloną.</span><span class="sxs-lookup"><span data-stu-id="ace66-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="ace66-142">Darbo klasės negalima nepaisyti darbo užsakymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="ace66-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="ace66-143">Darbo klasės naudojamos nukreipti ir (arba) apriboti darbo tipo užsakymo eilutes, kurias sandėlio darbuotojas gali apdoroti mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="ace66-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="ace66-144">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ace66-144">Select **New**.</span></span>
5. <span data-ttu-id="ace66-145">Lauke **Darbo tipas** pasirinkite **Padėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ace66-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="ace66-146">Lauke **Darbo klasės ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ace66-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="ace66-147">Paėmimo ir padėjimo instrukcijos yra rinkinys.</span><span class="sxs-lookup"><span data-stu-id="ace66-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="ace66-148">Kiekvienas paėmimo / padėjimo rinkinys turi būti tos pačios darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="ace66-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="ace66-149">Naudokite tą pačią darbo klasę, kurią nurodėte paėmimo instrukcijoje.</span><span class="sxs-lookup"><span data-stu-id="ace66-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="ace66-150">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ace66-150">Select **Save**.</span></span> <span data-ttu-id="ace66-151">Atkreipkite dėmesį, kad žymimasis langelis **Galioja** dabar yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="ace66-151">Note that the **Valid** checkbox is now checked.</span></span>  

