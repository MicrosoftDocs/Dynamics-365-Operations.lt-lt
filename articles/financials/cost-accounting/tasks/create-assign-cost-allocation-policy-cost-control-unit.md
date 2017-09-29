--- 
title: "Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui"
description: "Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="b860b-103">Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="b860b-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b860b-104">Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="b860b-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="b860b-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="b860b-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="b860b-106">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="b860b-106">Create a policy</span></span>
1. <span data-ttu-id="b860b-107">Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="b860b-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="b860b-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b860b-108">Click New.</span></span>
3. <span data-ttu-id="b860b-109">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="b860b-110">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b860b-111">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="b860b-111">Select Organization.</span></span>  
5. <span data-ttu-id="b860b-112">Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="b860b-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b860b-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="b860b-114">Sukurkite paskirstymo taisykles</span><span class="sxs-lookup"><span data-stu-id="b860b-114">Create allocation rules</span></span>
1. <span data-ttu-id="b860b-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b860b-115">Click New.</span></span>
2. <span data-ttu-id="b860b-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b860b-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b860b-117">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="b860b-118">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="b860b-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="b860b-119">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="b860b-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b860b-120">Click New.</span></span>
7. <span data-ttu-id="b860b-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b860b-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b860b-122">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="b860b-123">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="b860b-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="b860b-124">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="b860b-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b860b-125">Click New.</span></span>
12. <span data-ttu-id="b860b-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b860b-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b860b-127">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="b860b-128">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="b860b-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="b860b-129">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="b860b-130">Tęskite, kol sukursite visas taisykles.</span><span class="sxs-lookup"><span data-stu-id="b860b-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="b860b-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b860b-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="b860b-132">Priskirkite strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="b860b-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="b860b-133">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="b860b-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="b860b-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b860b-134">Click New.</span></span>
3. <span data-ttu-id="b860b-135">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b860b-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b860b-136">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b860b-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="b860b-137">Taisyklės taikomos pagal datą.</span><span class="sxs-lookup"><span data-stu-id="b860b-137">The rules are date-effective.</span></span> <span data-ttu-id="b860b-138">Vartotojas arba sistema gali baigti taisyklių galiojimą, jei sukurta naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="b860b-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="b860b-139">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b860b-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="b860b-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b860b-140">Click Save.</span></span>


