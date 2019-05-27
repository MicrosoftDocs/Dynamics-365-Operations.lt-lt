---
title: Kurti savikainos sumavimo strategija
description: Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f1fa434061832bd306cef13afc46c7f3adab0c0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543753"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="3489d-103">Kurti savikainos sumavimo strategija</span><span class="sxs-lookup"><span data-stu-id="3489d-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3489d-104">Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai.</span><span class="sxs-lookup"><span data-stu-id="3489d-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="3489d-105">Kuriant šią procedūrą buvo naudojami USP2 demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="3489d-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="3489d-106">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="3489d-106">Create a policy</span></span>
1. <span data-ttu-id="3489d-107">Eikite į Išlaidų apskaita > Strategijos > Savikainos sumavimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="3489d-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="3489d-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3489d-108">Click New.</span></span>
3. <span data-ttu-id="3489d-109">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3489d-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3489d-111">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-112">Pasirinkite Savikainos sumavimo CC.</span><span class="sxs-lookup"><span data-stu-id="3489d-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="3489d-113">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-114">Pasirinkite Savikainos sumavimo CC.</span><span class="sxs-lookup"><span data-stu-id="3489d-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="3489d-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3489d-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="3489d-116">Sukurkite savikainos sumavimo strategijos taisykles</span><span class="sxs-lookup"><span data-stu-id="3489d-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="3489d-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3489d-117">Click New.</span></span>
2. <span data-ttu-id="3489d-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3489d-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3489d-119">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-120">Pasirinkite 007.</span><span class="sxs-lookup"><span data-stu-id="3489d-120">Select 007.</span></span>  
4. <span data-ttu-id="3489d-121">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-122">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="3489d-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="3489d-123">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-124">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-007 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="3489d-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="3489d-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3489d-125">Click New.</span></span>
7. <span data-ttu-id="3489d-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3489d-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3489d-127">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-128">Pasirinkite 008.</span><span class="sxs-lookup"><span data-stu-id="3489d-128">Select 008.</span></span>  
9. <span data-ttu-id="3489d-129">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-130">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="3489d-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="3489d-131">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-132">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-008 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="3489d-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="3489d-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3489d-133">Click New.</span></span>
12. <span data-ttu-id="3489d-134">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3489d-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3489d-135">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-136">Pasirinkite 009.</span><span class="sxs-lookup"><span data-stu-id="3489d-136">Select 009.</span></span>  
14. <span data-ttu-id="3489d-137">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-138">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="3489d-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="3489d-139">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3489d-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="3489d-140">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-009 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="3489d-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="3489d-141">Tęskite, kol visi išlaidų centrai bus susieti su jų atitinkamais antrinės savikainos elementais.</span><span class="sxs-lookup"><span data-stu-id="3489d-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="3489d-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3489d-142">Click Save.</span></span>

