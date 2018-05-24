---
title: "Planuoti apkrovos efektyvumą"
description: "Šioje temoje paaiškinama, kaip nustatyti ir planuoti sandėlio apkrovą."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d52ad452c615a61739582431fcd100a7efa3d93a
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a><span data-ttu-id="f2c05-103">Planuoti apkrovos efektyvumą</span><span class="sxs-lookup"><span data-stu-id="f2c05-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f2c05-104">Galite suplanuoti pasirinktų tipų vietų apkrovos efektyvumą, taip pat numatyti esamą bei būsimą apkrovos efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="f2c05-105">Galite numatyti apkrovą vienoje ar keliose vietose, pagal zonos ar sandėlio arba pagal zonos ir sandėlio derinio apkrovos vienetus.</span><span class="sxs-lookup"><span data-stu-id="f2c05-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="f2c05-106">Planuokite ir peržiūrėkite sandėlio arba vietos apkrovą</span><span class="sxs-lookup"><span data-stu-id="f2c05-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="f2c05-107">Norėdami planuoti vietų, sandėlių arba zonų apkrovą, sukuriate erdvės naudojimo sąranką ir susiejate ją su bendruoju planu.</span><span class="sxs-lookup"><span data-stu-id="f2c05-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="f2c05-108">Vietos naudojimo sąrankoje pasinaudodami vietos tipais, pavyzdžiui, **Buferinė vieta** ir **Paėmimo vieta**, galite nurodyti, kaip turi būti numatomas vietos naudojimas.</span><span class="sxs-lookup"><span data-stu-id="f2c05-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="f2c05-109">Taip pat nurodote sandėliavimo apkrovos režimą, pvz., **Zona**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="f2c05-110">Būsimo erdvės naudojimo projekcija grindžiama informacija, apskaičiuota susijusiame bendrajame plane.</span><span class="sxs-lookup"><span data-stu-id="f2c05-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="f2c05-111">Bendruosiuose planuose prognozuojamas išteklių planavimas gaunamiems ir siunčiamiems gamybos ir operacijų užsakymams.</span><span class="sxs-lookup"><span data-stu-id="f2c05-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="f2c05-112">Laisvos erdvės projekcija grindžiama ryšiu tarp erdvės naudojimo sąrankos ir pasirinkto bendrojo plano.</span><span class="sxs-lookup"><span data-stu-id="f2c05-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="f2c05-113">Naudodamiesi sandėliavimo apkrovos režimu, kurį pasirinkote erdvės naudojimo sąrankoje, galite nurodyti, ar reikia numatyti kiekvieno sandėlio arba zonos apkrovą, arba ar projekcijos turi apimti informaciją ir apie sandėlius, ir apie zonas.</span><span class="sxs-lookup"><span data-stu-id="f2c05-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="f2c05-114">Taip pat nurodote, ar skaičiuojant apkrovos efektyvumą reikia pašalinti užblokuotas vietas.</span><span class="sxs-lookup"><span data-stu-id="f2c05-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="f2c05-115">Sukurdami ataskaitą **Sandėlio apkrovos efektyvumas** galite numatyti vietos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="f2c05-116">Kurdami šią ataskaitą, galite nurodyti, ar reikia planuoti kiekvienos vietos, ar kelių vietų, ar pasirinkto apkrovos vieneto, pvz., zonos ar sandėlio apkrovos efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="f2c05-117">Kurkite erdvės naudojimo sąranką sandėliui</span><span class="sxs-lookup"><span data-stu-id="f2c05-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="f2c05-118">Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Sandėlio stebėjimas** \> **Vietos naudojimas**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="f2c05-119">Norėdami kurti vietos naudojimo sąranką, pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="f2c05-120">Nurodykite naujos sąrankos ID ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="f2c05-121">Lauke **Sandėliavimo apkrovos režimas** pasirinkite, ar erdvės naudojimo apžvalgoje turi būti rodoma informacija pagal sandėlį, zoną arba sandėlį ir zoną.</span><span class="sxs-lookup"><span data-stu-id="f2c05-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="f2c05-122">Nustatykite parinkties **Neįtraukti užblokuotų vietų** reikšmę **Taip**, kad užblokuotos atsargų vietos nebūtų įtraukiamos skaičiuojant laisvą vietą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="f2c05-123">Galite blokuoti įvesties ir išvesties atsargų vietą, puslapio **Atsargų vietos** „FastTab“ elemento **Kita** lauke **Įvestis užblokuota** arba **Išvestis užblokuota** nurodydami vietos blokavimo priežastį.</span><span class="sxs-lookup"><span data-stu-id="f2c05-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="f2c05-124">„FastTab“ skirtuke **Vietos tipas** pasirinkite, kokių tipų vietas reikia įtraukti į vietos naudojimo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="f2c05-125">Turite pasirinkti bent vieną vietos tipą projekcijai.</span><span class="sxs-lookup"><span data-stu-id="f2c05-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="f2c05-126">Susiekite erdvės naudojimo sąranką su bendruoju planu</span><span class="sxs-lookup"><span data-stu-id="f2c05-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="f2c05-127">Pasirinkite **Atsargų valdymas** \> **Periodinės užduotys** \> **Apkrovos efektyvumo planavimas**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="f2c05-128">Lauke **Bendrasis planas** pasirinkite bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="f2c05-129">Lauke **Dienų skaičius** nurodykite, kiek dienų reikia įtraukti į dabartinių ir būsimų darbo krūvių projekciją.</span><span class="sxs-lookup"><span data-stu-id="f2c05-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="f2c05-130">Lauke **Vietos naudojimas** pasirinkite erdvės naudojimo sąranką, kurią naudosite dabartinių ir būsimų darbo krūvių projekcijoje.</span><span class="sxs-lookup"><span data-stu-id="f2c05-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="f2c05-131">Nurodykite apkrovos naudojimo projekciją ir peržiūrėkite informaciją</span><span class="sxs-lookup"><span data-stu-id="f2c05-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="f2c05-132">Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Fizinės atsargų ataskaitos** \> **Sandėlio apkrovos efektyvumas**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="f2c05-133">Lauke **Rodoma pagal** pasirinkite erdvės naudojimo projekcijos lygį.</span><span class="sxs-lookup"><span data-stu-id="f2c05-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="f2c05-134">**Vieta** – numatykite kiekvienos vietos erdvės naudojimą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="f2c05-135">Ši projekcija naudinga, jei, pvz., norite peržiūrėti visus vietos sandėlius, kad galėtumėte subalansuoti erdvės naudojimą keliuose sandėliuose.</span><span class="sxs-lookup"><span data-stu-id="f2c05-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="f2c05-136">**Apkrovos vienetas** – numatykite zonų arba sandėlių erdvės naudojimą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="f2c05-137">Laisva vieta tada numatoma pagal sukūrus vietos efektyvumo sąranką puslapio **Vietos naudojimas** lauke **Sandėliavimo apkrovos režimas** pasirinktą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f2c05-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="f2c05-138">Priklausomai nuo ankstesniame veiksme pasirinktos reikšmės, atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="f2c05-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="f2c05-139">Jei lauke **Rodyti pagal** pasirinkote **Vieta**, rodomas laukas **Vieta**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="f2c05-140">Pasirinkite vieną ar kelias vietas, kurias norite įtraukti į projekciją.</span><span class="sxs-lookup"><span data-stu-id="f2c05-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="f2c05-141">Jei lauke **Rodyti pagal** pasirinkote **Apkrovos vienetas**, rodomas laukas **Apkrovos vienetas**.</span><span class="sxs-lookup"><span data-stu-id="f2c05-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="f2c05-142">Pasirinkite apkrovos vienetą.</span><span class="sxs-lookup"><span data-stu-id="f2c05-142">Select the load unit.</span></span>

4. <span data-ttu-id="f2c05-143">Lauke **Apkrovos tipas** pasirinkę **Tūris** arba **Svoris** nurodykite sandėlio valdymo vienetą, kurio erdvę numatysite.</span><span class="sxs-lookup"><span data-stu-id="f2c05-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="f2c05-144">Lauke **Vietos naudojimo sąranka** pasirinkite vietos naudojimo sąranką, kuria bus grindžiama projekcija.</span><span class="sxs-lookup"><span data-stu-id="f2c05-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>

