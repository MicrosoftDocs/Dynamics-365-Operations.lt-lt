--- 
title: Kurti savikainos sumavimo strategija
description: "Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="7c874-103">Kurti savikainos sumavimo strategija</span><span class="sxs-lookup"><span data-stu-id="7c874-103">Create a cost rollup policy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c874-104">Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai.</span><span class="sxs-lookup"><span data-stu-id="7c874-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="7c874-105">Kuriant šią procedūrą buvo naudojami USP2 demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="7c874-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="7c874-106">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="7c874-106">Create a policy</span></span>
1. <span data-ttu-id="7c874-107">Eikite į Išlaidų apskaita > Strategijos > Savikainos sumavimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="7c874-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="7c874-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7c874-108">Click New.</span></span>
3. <span data-ttu-id="7c874-109">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="7c874-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7c874-111">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-112">Pasirinkite Savikainos sumavimo CC.</span><span class="sxs-lookup"><span data-stu-id="7c874-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="7c874-113">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-114">Pasirinkite Savikainos sumavimo CC.</span><span class="sxs-lookup"><span data-stu-id="7c874-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="7c874-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7c874-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="7c874-116">Sukurkite savikainos sumavimo strategijos taisykles</span><span class="sxs-lookup"><span data-stu-id="7c874-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="7c874-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7c874-117">Click New.</span></span>
2. <span data-ttu-id="7c874-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7c874-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="7c874-119">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-120">Pasirinkite 007.</span><span class="sxs-lookup"><span data-stu-id="7c874-120">Select 007.</span></span>  
4. <span data-ttu-id="7c874-121">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-122">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="7c874-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="7c874-123">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-124">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-007 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="7c874-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="7c874-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7c874-125">Click New.</span></span>
7. <span data-ttu-id="7c874-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7c874-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7c874-127">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-128">Pasirinkite 008.</span><span class="sxs-lookup"><span data-stu-id="7c874-128">Select 008.</span></span>  
9. <span data-ttu-id="7c874-129">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-130">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="7c874-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="7c874-131">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-132">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-008 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="7c874-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="7c874-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7c874-133">Click New.</span></span>
12. <span data-ttu-id="7c874-134">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7c874-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7c874-135">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-136">Pasirinkite 009.</span><span class="sxs-lookup"><span data-stu-id="7c874-136">Select 009.</span></span>  
14. <span data-ttu-id="7c874-137">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-138">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="7c874-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="7c874-139">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7c874-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="7c874-140">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-009 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="7c874-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="7c874-141">Tęskite, kol visi išlaidų centrai bus susieti su jų atitinkamais antrinės savikainos elementais.</span><span class="sxs-lookup"><span data-stu-id="7c874-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="7c874-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7c874-142">Click Save.</span></span>

