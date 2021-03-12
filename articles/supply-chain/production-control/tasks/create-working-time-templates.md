---
title: Darbo laiko šablonų kūrimas
description: Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e8e43900fd25f0051124d761dc7b06d4f9313a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006821"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="7086e-103">Darbo laiko šablonų kūrimas</span><span class="sxs-lookup"><span data-stu-id="7086e-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7086e-104">Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="7086e-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="7086e-105">Ši procedūra nurodo, kaip nustatyti darbo laiko šabloną, naudojant darbo laiko planavimo ypatybes, skirtas darbo laiko intervalas skirstyti.</span><span class="sxs-lookup"><span data-stu-id="7086e-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="7086e-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="7086e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="7086e-107">Pasirinkite Visos darbo sritys > Išteklių naudojimo ciklo valdymas.</span><span class="sxs-lookup"><span data-stu-id="7086e-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="7086e-108">Spustelėkite Darbo laiko šablonai.</span><span class="sxs-lookup"><span data-stu-id="7086e-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="7086e-109">Kurti darbo laiko šabloną</span><span class="sxs-lookup"><span data-stu-id="7086e-109">Create working time template</span></span>
1. <span data-ttu-id="7086e-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7086e-110">Click New.</span></span>
2. <span data-ttu-id="7086e-111">Šablono lauke Darbo laikas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="7086e-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="7086e-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7086e-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7086e-113">Išplėskite skyrių Pirmadienis.</span><span class="sxs-lookup"><span data-stu-id="7086e-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="7086e-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7086e-114">Click Add.</span></span>
6. <span data-ttu-id="7086e-115">Lauke Nuo įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="7086e-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="7086e-116">Nurodykite laiką, kada darbas prasideda ryte.</span><span class="sxs-lookup"><span data-stu-id="7086e-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="7086e-117">Lauke Iki įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="7086e-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="7086e-118">Nurodykite laiką, kada būna darbuotojų pietų pertrauka.</span><span class="sxs-lookup"><span data-stu-id="7086e-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="7086e-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7086e-119">Click Add.</span></span>
9. <span data-ttu-id="7086e-120">Lauke Nuo įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="7086e-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="7086e-121">Nurodykite laiką, kada darbas tęsiamas po pietų.</span><span class="sxs-lookup"><span data-stu-id="7086e-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="7086e-122">Lauke Iki įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="7086e-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="7086e-123">Nurodykite darbo dienos pabaigą.</span><span class="sxs-lookup"><span data-stu-id="7086e-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="7086e-124">Dubliuoti visos savaitės dienų darbo laikus</span><span class="sxs-lookup"><span data-stu-id="7086e-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="7086e-125">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="7086e-125">Click Copy day.</span></span>
    * <span data-ttu-id="7086e-126">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į antradienį.</span><span class="sxs-lookup"><span data-stu-id="7086e-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="7086e-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7086e-127">Click OK.</span></span>
3. <span data-ttu-id="7086e-128">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="7086e-128">Click Copy day.</span></span>
    * <span data-ttu-id="7086e-129">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į trečiadienį.</span><span class="sxs-lookup"><span data-stu-id="7086e-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="7086e-130">Lauke Į dieną pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="7086e-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="7086e-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7086e-131">Click OK.</span></span>
6. <span data-ttu-id="7086e-132">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="7086e-132">Click Copy day.</span></span>
    * <span data-ttu-id="7086e-133">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į ketvirtadienį.</span><span class="sxs-lookup"><span data-stu-id="7086e-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="7086e-134">Lauke Į dieną pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="7086e-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="7086e-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7086e-135">Click OK.</span></span>
9. <span data-ttu-id="7086e-136">Spustelėkite Kopijuoti dieną.</span><span class="sxs-lookup"><span data-stu-id="7086e-136">Click Copy day.</span></span>
    * <span data-ttu-id="7086e-137">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į penktadienį.</span><span class="sxs-lookup"><span data-stu-id="7086e-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="7086e-138">Lauke Į dieną pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="7086e-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="7086e-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7086e-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="7086e-140">Nurodyti specialiųjų operacijų laiko atkarpas</span><span class="sxs-lookup"><span data-stu-id="7086e-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="7086e-141">Išplėskite skyrių Penktadienis.</span><span class="sxs-lookup"><span data-stu-id="7086e-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="7086e-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7086e-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7086e-143">Lauke Ypatybė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7086e-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="7086e-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7086e-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7086e-145">Lauke Ypatybė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7086e-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="7086e-146">Pažymėti savaitgalio dienas kaip uždarytas, kada negalima paimti</span><span class="sxs-lookup"><span data-stu-id="7086e-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="7086e-147">Išplėskite skyrių Šeštadienis.</span><span class="sxs-lookup"><span data-stu-id="7086e-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="7086e-148">Lauke Uždaryta paimti pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="7086e-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="7086e-149">Išplėskite skyrių Sekmadienis.</span><span class="sxs-lookup"><span data-stu-id="7086e-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="7086e-150">Lauke Uždaryta paimti pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="7086e-150">Select Yes in the Closed for pickup field.</span></span>

