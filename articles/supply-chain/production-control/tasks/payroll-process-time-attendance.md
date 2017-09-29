--- 
title: "Įgalinti laiko ir buvimo darbe algalapio procesą"
description: "Ši procedūra parodo, kaip įgalinti laiko ir buvimo darbe algalapio procesą."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 22ce633f65847f10fbe507b71bfc2bb33f595501
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="d8b9f-103">Įgalinti laiko ir buvimo darbe algalapio procesą</span><span class="sxs-lookup"><span data-stu-id="d8b9f-103">Enable the payroll process for time and attendance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8b9f-104">Ši procedūra parodo, kaip įgalinti laiko ir buvimo darbe algalapio procesą.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="d8b9f-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="d8b9f-106">Kurti mokėjimo tipą su susijusiu darbo užmokesčio tarifu</span><span class="sxs-lookup"><span data-stu-id="d8b9f-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="d8b9f-107">Laikas ir buvimas darbe > Nustatymas > Algalapis > Mokėjimo tipai</span><span class="sxs-lookup"><span data-stu-id="d8b9f-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="d8b9f-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-108">Click New.</span></span>
3. <span data-ttu-id="d8b9f-109">Lauke Mokėjimo tipas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="d8b9f-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8b9f-111">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-111">Click Save.</span></span>
6. <span data-ttu-id="d8b9f-112">Spustelėkite Tarifai.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-112">Click Rates.</span></span>
    * <span data-ttu-id="d8b9f-113">Mokėjimo tipų koeficientai nustatomi tam tikriems laiko intervalams, o darbuotojams gali būti sukurti atskiri koeficientai.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="d8b9f-114">Ne visada būtina kurti laiko ir buvimo darbe mokėjimo tipų koeficientus.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="d8b9f-115">Ši informacija jau gali būti algalapių sistemoje, kuri naudojama atlyginimams generuoti.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="d8b9f-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-116">Click New.</span></span>
8. <span data-ttu-id="d8b9f-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d8b9f-118">Lauke Tarifas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="d8b9f-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="d8b9f-120">Mokėjimo sutarties kūrimas</span><span class="sxs-lookup"><span data-stu-id="d8b9f-120">Create a pay agreement</span></span>
1. <span data-ttu-id="d8b9f-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-121">Close the page.</span></span>
2. <span data-ttu-id="d8b9f-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-122">Close the page.</span></span>
3. <span data-ttu-id="d8b9f-123">Eikite į Mokėjimo sutartys.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="d8b9f-124">Laikas ir buvimas darbe > Nustatymas > Mokėjimo sutartys</span><span class="sxs-lookup"><span data-stu-id="d8b9f-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="d8b9f-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-125">Click New.</span></span>
5. <span data-ttu-id="d8b9f-126">Lauke Mokėjimo sutartis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="d8b9f-127">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="d8b9f-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-128">Click Save.</span></span>
8. <span data-ttu-id="d8b9f-129">Spustelėkite Sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="d8b9f-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-130">Click New.</span></span>
10. <span data-ttu-id="d8b9f-131">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="d8b9f-132">Lauke Profilio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="d8b9f-133">Lauke Mokėjimo tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="d8b9f-134">Nustatyti laiko ir registracijos darbuotojo mokėjimo sutartį</span><span class="sxs-lookup"><span data-stu-id="d8b9f-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="d8b9f-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-135">Close the page.</span></span>
2. <span data-ttu-id="d8b9f-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-136">Close the page.</span></span>
3. <span data-ttu-id="d8b9f-137">Eikite į Laiko registracijos darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="d8b9f-138">Laikas ir buvimas darbe > Nustatymas > Laiko registracijos darbuotojai</span><span class="sxs-lookup"><span data-stu-id="d8b9f-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="d8b9f-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d8b9f-140">Spustelėkite skirtuką Užimtumas.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="d8b9f-141">Išplėskite skyrių Laiko registracija.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="d8b9f-142">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-142">Click Edit.</span></span>
8. <span data-ttu-id="d8b9f-143">Lauke Mokėjimo sutartis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d8b9f-143">In the Pay agreement field, enter or select a value.</span></span>

