--- 
title: "Bendrojo planavimo vykdymo stebėjimas"
description: Gamybos planuotojas nori pamatyti, ar vykdomas bendrasis planavimas.
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="c42c4-103">Bendrojo planavimo vykdymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="c42c4-103">Monitor a master planning run</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c42c4-104">Gamybos planuotojas nori pamatyti, ar vykdomas bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="c42c4-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="c42c4-105">Atlikti šiai procedūrai naudokite demonstracinių duomenų įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="c42c4-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="c42c4-106">Vykdyti bendrąjį planavimą</span><span class="sxs-lookup"><span data-stu-id="c42c4-106">Run master planning</span></span>
1. <span data-ttu-id="c42c4-107">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="c42c4-107">Click Master planning.</span></span>
    * <span data-ttu-id="c42c4-108">Tai rasite numatytoje ataskaitų srityje.</span><span class="sxs-lookup"><span data-stu-id="c42c4-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="c42c4-109">Lauke Planas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c42c4-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="c42c4-110">Pavyzdys: statinis planas</span><span class="sxs-lookup"><span data-stu-id="c42c4-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="c42c4-111">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="c42c4-111">Click Run.</span></span>
4. <span data-ttu-id="c42c4-112">Lauke Sekti apdorojimo laiką pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c42c4-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="c42c4-113">Jei laukas jau pasirinktas, šį veiksmą praleiskite.</span><span class="sxs-lookup"><span data-stu-id="c42c4-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="c42c4-114">Lauke Gijų skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c42c4-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="c42c4-115">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="c42c4-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c42c4-116">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="c42c4-116">Click Filter.</span></span>
8. <span data-ttu-id="c42c4-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c42c4-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c42c4-118">Pažymėkite eilutę, kurioje Laukas = Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="c42c4-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="c42c4-119">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c42c4-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="c42c4-120">Pavyzdys: T0001</span><span class="sxs-lookup"><span data-stu-id="c42c4-120">Example: T0001</span></span>  
10. <span data-ttu-id="c42c4-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c42c4-121">Click OK.</span></span>
11. <span data-ttu-id="c42c4-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c42c4-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="c42c4-123">Bendrojo planavimo vykdymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="c42c4-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="c42c4-124">Spustelėkite Istorija.</span><span class="sxs-lookup"><span data-stu-id="c42c4-124">Click History.</span></span>
2. <span data-ttu-id="c42c4-125">Spustelėkite Užklausos.</span><span class="sxs-lookup"><span data-stu-id="c42c4-125">Click Inquiries.</span></span>
3. <span data-ttu-id="c42c4-126">Spustelėkite Proceso užduoties trukmė.</span><span class="sxs-lookup"><span data-stu-id="c42c4-126">Click Process task duration.</span></span>
4. <span data-ttu-id="c42c4-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c42c4-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c42c4-128">Galite apžvelgti, kiek laiko truko atlikti kiekvieną kiekvienos prekės planavimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="c42c4-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


