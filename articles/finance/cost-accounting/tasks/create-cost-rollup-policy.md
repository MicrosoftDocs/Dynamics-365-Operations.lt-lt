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
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d32cc2c1844c6c334dd00b249c736e153f13d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446130"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="37ac1-103">Kurti savikainos sumavimo strategija</span><span class="sxs-lookup"><span data-stu-id="37ac1-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37ac1-104">Ši procedūra parodo, kaip sukurti savikainos sumavimo strategiją ir sukurti taisykles strategijai.</span><span class="sxs-lookup"><span data-stu-id="37ac1-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="37ac1-105">Kuriant šią procedūrą buvo naudojami USP2 demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="37ac1-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="37ac1-106">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="37ac1-106">Create a policy</span></span>
1. <span data-ttu-id="37ac1-107">Eikite į Išlaidų apskaita > Strategijos > Savikainos sumavimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="37ac1-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="37ac1-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="37ac1-108">Click New.</span></span>
3. <span data-ttu-id="37ac1-109">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="37ac1-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="37ac1-111">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-112">Pasirinkite Savikainos sumavimo CC.</span><span class="sxs-lookup"><span data-stu-id="37ac1-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="37ac1-113">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-114">Pasirinkite Savikainos sumavimo CC.</span><span class="sxs-lookup"><span data-stu-id="37ac1-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="37ac1-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="37ac1-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="37ac1-116">Sukurkite savikainos sumavimo strategijos taisykles</span><span class="sxs-lookup"><span data-stu-id="37ac1-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="37ac1-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="37ac1-117">Click New.</span></span>
2. <span data-ttu-id="37ac1-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="37ac1-119">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-120">Pasirinkite 007.</span><span class="sxs-lookup"><span data-stu-id="37ac1-120">Select 007.</span></span>  
4. <span data-ttu-id="37ac1-121">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-122">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="37ac1-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="37ac1-123">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-124">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-007 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="37ac1-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="37ac1-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="37ac1-125">Click New.</span></span>
7. <span data-ttu-id="37ac1-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="37ac1-127">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-128">Pasirinkite 008.</span><span class="sxs-lookup"><span data-stu-id="37ac1-128">Select 008.</span></span>  
9. <span data-ttu-id="37ac1-129">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-130">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="37ac1-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="37ac1-131">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-132">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-008 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="37ac1-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="37ac1-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="37ac1-133">Click New.</span></span>
12. <span data-ttu-id="37ac1-134">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="37ac1-135">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-136">Pasirinkite 009.</span><span class="sxs-lookup"><span data-stu-id="37ac1-136">Select 009.</span></span>  
14. <span data-ttu-id="37ac1-137">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-138">Pasirinkite Savikainos sumavimo CE.</span><span class="sxs-lookup"><span data-stu-id="37ac1-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="37ac1-139">Lauke Antrinis savikainos elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="37ac1-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="37ac1-140">Šiam pavyzdžiui priskirkite antrinį savikainos elementą CC-009 išlaidų centrui.</span><span class="sxs-lookup"><span data-stu-id="37ac1-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="37ac1-141">Tęskite, kol visi išlaidų centrai bus susieti su jų atitinkamais antrinės savikainos elementais.</span><span class="sxs-lookup"><span data-stu-id="37ac1-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="37ac1-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="37ac1-142">Click Save.</span></span>

