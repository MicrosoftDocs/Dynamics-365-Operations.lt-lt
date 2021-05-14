---
title: Darbo laiko šablonų kūrimas
description: Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920934"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="badef-103">Darbo laiko šablonų kūrimas</span><span class="sxs-lookup"><span data-stu-id="badef-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="badef-104">Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="badef-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="badef-105">Ši procedūra nurodo, kaip nustatyti darbo laiko šabloną, naudojant darbo laiko planavimo ypatybes, skirtas darbo laiko intervalas skirstyti.</span><span class="sxs-lookup"><span data-stu-id="badef-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="badef-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="badef-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="badef-107">Eikite į **Darbo sritys > Išteklių naudojimo ciklo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="badef-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="badef-108">Rinkitės **Darbo laiko šablonai**.</span><span class="sxs-lookup"><span data-stu-id="badef-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="badef-109">Kurti darbo laiko šabloną</span><span class="sxs-lookup"><span data-stu-id="badef-109">Create working time template</span></span>

1. <span data-ttu-id="badef-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="badef-110">Select **New**.</span></span>
1. <span data-ttu-id="badef-111">Šablono lauke **Darbo laikas** įveskite.</span><span class="sxs-lookup"><span data-stu-id="badef-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="badef-112">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="badef-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="badef-113">Išplėskite skyrių **Pirmadienis**.</span><span class="sxs-lookup"><span data-stu-id="badef-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="badef-114">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="badef-114">Select **Add**.</span></span>
1. <span data-ttu-id="badef-115">Lauke **Nuo** įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="badef-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="badef-116">Nurodykite laiką, kada darbas prasideda ryte.</span><span class="sxs-lookup"><span data-stu-id="badef-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="badef-117">Lauke **Iki** įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="badef-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="badef-118">Nurodykite laiką, kada būna darbuotojų pietų pertrauka.</span><span class="sxs-lookup"><span data-stu-id="badef-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="badef-119">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="badef-119">Select **Add**.</span></span>
1. <span data-ttu-id="badef-120">Lauke **Nuo** įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="badef-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="badef-121">Nurodykite laiką, kada darbas tęsiamas po pietų.</span><span class="sxs-lookup"><span data-stu-id="badef-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="badef-122">Lauke **Iki** įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="badef-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="badef-123">Nurodykite darbo dienos pabaigą.</span><span class="sxs-lookup"><span data-stu-id="badef-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="badef-124">Dubliuoti visos savaitės dienų darbo laikus</span><span class="sxs-lookup"><span data-stu-id="badef-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="badef-125">Pasirinkite **Kopijuoti dieną**.</span><span class="sxs-lookup"><span data-stu-id="badef-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="badef-126">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į antradienį.</span><span class="sxs-lookup"><span data-stu-id="badef-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="badef-127">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="badef-127">Select **OK**.</span></span>
1. <span data-ttu-id="badef-128">Pasirinkite **Kopijuoti dieną**.</span><span class="sxs-lookup"><span data-stu-id="badef-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="badef-129">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į trečiadienį.</span><span class="sxs-lookup"><span data-stu-id="badef-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="badef-130">Lauke **Iki savaitės dienos** laukelyje rinkitės parinktį.</span><span class="sxs-lookup"><span data-stu-id="badef-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="badef-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="badef-131">Select **OK**.</span></span>
1. <span data-ttu-id="badef-132">Pasirinkite **Kopijuoti dieną**.</span><span class="sxs-lookup"><span data-stu-id="badef-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="badef-133">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į ketvirtadienį.</span><span class="sxs-lookup"><span data-stu-id="badef-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="badef-134">Lauke **Iki savaitės dienos** laukelyje rinkitės parinktį.</span><span class="sxs-lookup"><span data-stu-id="badef-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="badef-135">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="badef-135">Select **OK**.</span></span>
1. <span data-ttu-id="badef-136">Pasirinkite **Kopijuoti dieną**.</span><span class="sxs-lookup"><span data-stu-id="badef-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="badef-137">Kopijuokite darbo laiko apibrėžimus iš pirmadienio į penktadienį.</span><span class="sxs-lookup"><span data-stu-id="badef-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="badef-138">Lauke **Iki savaitės dienos** laukelyje rinkitės parinktį.</span><span class="sxs-lookup"><span data-stu-id="badef-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="badef-139">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="badef-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="badef-140">Nurodyti specialiųjų operacijų laiko atkarpas</span><span class="sxs-lookup"><span data-stu-id="badef-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="badef-141">Išplėskite skyrių **Penktadienis**.</span><span class="sxs-lookup"><span data-stu-id="badef-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="badef-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="badef-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="badef-143">Lauke **Ypatybė** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="badef-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="badef-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="badef-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="badef-145">Lauke **Ypatybė** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="badef-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="badef-146">Pažymėti savaitgalio dienas kaip uždarytas, kada negalima paimti</span><span class="sxs-lookup"><span data-stu-id="badef-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="badef-147">Išplėskite skyrių **Šeštadienis**.</span><span class="sxs-lookup"><span data-stu-id="badef-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="badef-148">Lauke *Taip* Uždaryta paimti pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="badef-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="badef-149">Išplėskite skyrių **Sekmadienis**.</span><span class="sxs-lookup"><span data-stu-id="badef-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="badef-150">Lauke *Taip* Uždaryta paimti pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="badef-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]