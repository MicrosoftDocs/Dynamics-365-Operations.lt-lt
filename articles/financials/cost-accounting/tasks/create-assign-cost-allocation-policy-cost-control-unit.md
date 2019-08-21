---
title: Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui
description: Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841398"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="c5200-103">Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="c5200-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5200-104">Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="c5200-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="c5200-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="c5200-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c5200-106">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="c5200-106">Create a policy</span></span>
1. <span data-ttu-id="c5200-107">Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="c5200-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="c5200-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c5200-108">Click New.</span></span>
3. <span data-ttu-id="c5200-109">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c5200-110">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c5200-111">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="c5200-111">Select Organization.</span></span>  
5. <span data-ttu-id="c5200-112">Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="c5200-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c5200-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="c5200-114">Sukurkite paskirstymo taisykles</span><span class="sxs-lookup"><span data-stu-id="c5200-114">Create allocation rules</span></span>
1. <span data-ttu-id="c5200-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c5200-115">Click New.</span></span>
2. <span data-ttu-id="c5200-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5200-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c5200-117">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="c5200-118">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="c5200-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="c5200-119">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="c5200-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c5200-120">Click New.</span></span>
7. <span data-ttu-id="c5200-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5200-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c5200-122">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="c5200-123">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="c5200-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="c5200-124">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="c5200-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c5200-125">Click New.</span></span>
12. <span data-ttu-id="c5200-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5200-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c5200-127">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="c5200-128">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="c5200-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="c5200-129">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="c5200-130">Tęskite, kol sukursite visas taisykles.</span><span class="sxs-lookup"><span data-stu-id="c5200-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="c5200-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c5200-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="c5200-132">Priskirkite strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="c5200-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="c5200-133">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="c5200-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="c5200-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c5200-134">Click New.</span></span>
3. <span data-ttu-id="c5200-135">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5200-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c5200-136">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="c5200-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="c5200-137">Taisyklės taikomos pagal datą.</span><span class="sxs-lookup"><span data-stu-id="c5200-137">The rules are date-effective.</span></span> <span data-ttu-id="c5200-138">Vartotojas arba sistema gali baigti taisyklių galiojimą, jei sukurta naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="c5200-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="c5200-139">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5200-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="c5200-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c5200-140">Click Save.</span></span>

