--- 
title: "Darbo laiko šablonų kūrimas"
description: "Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="43437-103">Darbo laiko šablonų kūrimas</span><span class="sxs-lookup"><span data-stu-id="43437-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43437-104">Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="43437-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="43437-105">Ši procedūra nurodo, kaip nustatyti darbo laiko šabloną, naudojant darbo laiko planavimo ypatybes, skirtas darbo laiko intervalas skirstyti.</span><span class="sxs-lookup"><span data-stu-id="43437-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="43437-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="43437-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="43437-107">Pasirinkite Visos darbo sritys > Išteklių naudojimo ciklo valdymas.</span><span class="sxs-lookup"><span data-stu-id="43437-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="43437-108">Spustelėkite Darbo laiko šablonai.</span><span class="sxs-lookup"><span data-stu-id="43437-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="43437-109">Kurti darbo laiko šabloną</span><span class="sxs-lookup"><span data-stu-id="43437-109">Create working time template</span></span>
1. <span data-ttu-id="43437-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="43437-110">Click New.</span></span>
2. <span data-ttu-id="43437-111">Šablono lauke Darbo laikas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="43437-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="43437-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="43437-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="43437-113">Išplėskite skyrių Pirmadienis.</span><span class="sxs-lookup"><span data-stu-id="43437-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="43437-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="43437-114">Click Add.</span></span>
6. <span data-ttu-id="43437-115">Lauke Nuo įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="43437-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="43437-116">Nurodykite laiką, kada darbas prasideda ryte.</span><span class="sxs-lookup"><span data-stu-id="43437-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="43437-117">Lauke Iki įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="43437-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="43437-118">Nurodykite laiką, kada būna darbuotojų pietų pertrauka.</span><span class="sxs-lookup"><span data-stu-id="43437-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="43437-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="43437-119">Click Add.</span></span>
9. <span data-ttu-id="43437-120">Lauke Nuo įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="43437-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="43437-121">Nurodykite laiką, kada darbas tęsiamas po pietų.</span><span class="sxs-lookup"><span data-stu-id="43437-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="43437-122">Lauke Iki įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="43437-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="43437-123">Nurodykite darbo dienos pabaigą.</span><span class="sxs-lookup"><span data-stu-id="43437-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="43437-124">Dubliuoti visos savaitės dienų darbo laikus</span><span class="sxs-lookup"><span data-stu-id="43437-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="43437-125">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="43437-125">Click Copy day.</span></span>
    * <span data-ttu-id="43437-126">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į antradienį.</span><span class="sxs-lookup"><span data-stu-id="43437-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="43437-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="43437-127">Click OK.</span></span>
3. <span data-ttu-id="43437-128">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="43437-128">Click Copy day.</span></span>
    * <span data-ttu-id="43437-129">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į trečiadienį.</span><span class="sxs-lookup"><span data-stu-id="43437-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="43437-130">Lauke Į dieną pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="43437-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="43437-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="43437-131">Click OK.</span></span>
6. <span data-ttu-id="43437-132">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="43437-132">Click Copy day.</span></span>
    * <span data-ttu-id="43437-133">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į ketvirtadienį.</span><span class="sxs-lookup"><span data-stu-id="43437-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="43437-134">Lauke Į dieną pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="43437-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="43437-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="43437-135">Click OK.</span></span>
9. <span data-ttu-id="43437-136">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="43437-136">Click Copy day.</span></span>
    * <span data-ttu-id="43437-137">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į penktadienį.</span><span class="sxs-lookup"><span data-stu-id="43437-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="43437-138">Lauke Į dieną pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="43437-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="43437-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="43437-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="43437-140">Nurodyti specialiųjų operacijų laiko atkarpas</span><span class="sxs-lookup"><span data-stu-id="43437-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="43437-141">Išplėskite skyrių Penktadienis.</span><span class="sxs-lookup"><span data-stu-id="43437-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="43437-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="43437-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="43437-143">Lauke Ypatybė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="43437-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="43437-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="43437-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="43437-145">Lauke Ypatybė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="43437-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="43437-146">Pažymėti savaitgalio dienas kaip uždarytas, kada negalima paimti</span><span class="sxs-lookup"><span data-stu-id="43437-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="43437-147">Išplėskite skyrių Šeštadienis.</span><span class="sxs-lookup"><span data-stu-id="43437-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="43437-148">Lauke Uždaryta paimti pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="43437-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="43437-149">Išplėskite skyrių Sekmadienis.</span><span class="sxs-lookup"><span data-stu-id="43437-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="43437-150">Lauke Uždaryta paimti pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="43437-150">Select Yes in the Closed for pickup field.</span></span>


