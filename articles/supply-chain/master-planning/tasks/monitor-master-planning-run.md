---
title: Bendrojo planavimo vykdymo stebėjimas
description: Gamybos planuotojas nori pamatyti, ar vykdomas bendrasis planavimas.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845118"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="d29d3-103">Bendrojo planavimo vykdymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="d29d3-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d29d3-104">Gamybos planuotojas nori pamatyti, ar vykdomas bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="d29d3-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="d29d3-105">Atlikti šiai procedūrai naudokite demonstracinių duomenų įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="d29d3-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="d29d3-106">Vykdyti bendrąjį planavimą</span><span class="sxs-lookup"><span data-stu-id="d29d3-106">Run master planning</span></span>
1. <span data-ttu-id="d29d3-107">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="d29d3-107">Click Master planning.</span></span>
    * <span data-ttu-id="d29d3-108">Tai rasite numatytoje ataskaitų srityje.</span><span class="sxs-lookup"><span data-stu-id="d29d3-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="d29d3-109">Lauke Planas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="d29d3-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="d29d3-110">Pavyzdys: statinis planas</span><span class="sxs-lookup"><span data-stu-id="d29d3-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="d29d3-111">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d29d3-111">Click Run.</span></span>
4. <span data-ttu-id="d29d3-112">Lauke Sekti apdorojimo laiką pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d29d3-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="d29d3-113">Jei laukas jau pasirinktas, šį veiksmą praleiskite.</span><span class="sxs-lookup"><span data-stu-id="d29d3-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="d29d3-114">Lauke Gijų skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d29d3-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="d29d3-115">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="d29d3-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d29d3-116">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="d29d3-116">Click Filter.</span></span>
8. <span data-ttu-id="d29d3-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d29d3-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d29d3-118">Pažymėkite eilutę, kurioje Laukas = Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="d29d3-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="d29d3-119">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d29d3-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="d29d3-120">Pavyzdys: T0001</span><span class="sxs-lookup"><span data-stu-id="d29d3-120">Example: T0001</span></span>  
10. <span data-ttu-id="d29d3-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d29d3-121">Click OK.</span></span>
11. <span data-ttu-id="d29d3-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d29d3-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="d29d3-123">Bendrojo planavimo vykdymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="d29d3-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="d29d3-124">Spustelėkite Istorija.</span><span class="sxs-lookup"><span data-stu-id="d29d3-124">Click History.</span></span>
2. <span data-ttu-id="d29d3-125">Spustelėkite Užklausos.</span><span class="sxs-lookup"><span data-stu-id="d29d3-125">Click Inquiries.</span></span>
3. <span data-ttu-id="d29d3-126">Spustelėkite Proceso užduoties trukmė.</span><span class="sxs-lookup"><span data-stu-id="d29d3-126">Click Process task duration.</span></span>
4. <span data-ttu-id="d29d3-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d29d3-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d29d3-128">Galite apžvelgti, kiek laiko truko atlikti kiekvieną kiekvienos prekės planavimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="d29d3-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

