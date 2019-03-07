---
title: Kurti planą su apribojimais
description: Ši procedūra parodo, kaip sukurti planą, kuris atsižvelgia tiek į medžiagų, tiek į pajėgumų apribojimus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "336042"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="2c9ef-103">Kurti planą su apribojimais</span><span class="sxs-lookup"><span data-stu-id="2c9ef-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c9ef-104">Ši procedūra parodo, kaip sukurti planą, kuris atsižvelgia tiek į medžiagų, tiek į pajėgumų apribojimus.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="2c9ef-105">Planas užtikrina, kad gamyba neprasidėtų tol, kol bus turima medžiagų ir nebus perpildyti ištekliai.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="2c9ef-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2c9ef-107">Ši procedūra yra skirta gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="2c9ef-108">Nustatyti planą su apribojimais</span><span class="sxs-lookup"><span data-stu-id="2c9ef-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="2c9ef-109">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-109">Click Master planning.</span></span>
2. <span data-ttu-id="2c9ef-110">Spustelėkite Bendrieji planai.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-110">Click Master plans.</span></span>
3. <span data-ttu-id="2c9ef-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2c9ef-112">Pavyzdys: statinis planas</span><span class="sxs-lookup"><span data-stu-id="2c9ef-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="2c9ef-113">Lauke Ribotas pajėgumas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="2c9ef-114">Lauke Riboto pajėgumo laiko ribos įveskite „30‟.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="2c9ef-115">Išplėskite dalį Laiko ribos dienomis.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="2c9ef-116">Lauke Pajėgumas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="2c9ef-117">Lauke Pajėgumo planavimo laiko ribos (dienomis) įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="2c9ef-118">Pavyzdys: 60</span><span class="sxs-lookup"><span data-stu-id="2c9ef-118">Example: 60</span></span>  
9. <span data-ttu-id="2c9ef-119">Lauke Apskaičiuoti atidėjimai pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="2c9ef-120">Lauke Apskaičiuotų atidėjimų laiko ribos (dienomis) įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="2c9ef-121">Pavyzdys: 60</span><span class="sxs-lookup"><span data-stu-id="2c9ef-121">Example: 60</span></span>  
11. <span data-ttu-id="2c9ef-122">Išplėskite dalį Apskaičiuoti atidėjimai.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="2c9ef-123">Lauke Pridėti apskaičiuotą atidėjimą prie poreikio datos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="2c9ef-124">Lauke Pridėti apskaičiuotą atidėjimą prie poreikio datos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="2c9ef-125">Lauke Pridėti apskaičiuotą atidėjimą prie poreikio datos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="2c9ef-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="2c9ef-127">Kurti planą su apribojimais</span><span class="sxs-lookup"><span data-stu-id="2c9ef-127">Create a constrained plan</span></span>
1. <span data-ttu-id="2c9ef-128">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-128">Click Run.</span></span>
2. <span data-ttu-id="2c9ef-129">Lauke Bendrasis planas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="2c9ef-130">Pasirinkite planą, kurio apribojimus nustatėte.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="2c9ef-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-131">Click OK.</span></span>
    * <span data-ttu-id="2c9ef-132">Tai gali užtrukti.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-132">This may take a while.</span></span>  
4. <span data-ttu-id="2c9ef-133">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="2c9ef-133">Click Planned orders.</span></span>

