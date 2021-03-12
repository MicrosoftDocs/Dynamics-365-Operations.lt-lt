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
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006310d07dfa5b75941ca248736800bbb9e8e7b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969333"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="78294-103">Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="78294-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78294-104">Naudokite šią procedūrą norėdami sukurti ir priskirti savikainos paskirstymo strategiją ir atitinkamas taisykles savikainos kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="78294-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="78294-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="78294-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="78294-106">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="78294-106">Create a policy</span></span>
1. <span data-ttu-id="78294-107">Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="78294-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="78294-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78294-108">Click New.</span></span>
3. <span data-ttu-id="78294-109">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="78294-110">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="78294-111">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="78294-111">Select Organization.</span></span>  
5. <span data-ttu-id="78294-112">Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="78294-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78294-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="78294-114">Sukurkite paskirstymo taisykles</span><span class="sxs-lookup"><span data-stu-id="78294-114">Create allocation rules</span></span>
1. <span data-ttu-id="78294-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78294-115">Click New.</span></span>
2. <span data-ttu-id="78294-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="78294-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="78294-117">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="78294-118">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="78294-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="78294-119">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="78294-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78294-120">Click New.</span></span>
7. <span data-ttu-id="78294-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="78294-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="78294-122">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="78294-123">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="78294-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="78294-124">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="78294-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78294-125">Click New.</span></span>
12. <span data-ttu-id="78294-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="78294-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="78294-127">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="78294-128">Lauke Savikainos taisyklės pasirinkite „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="78294-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="78294-129">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="78294-130">Tęskite, kol sukursite visas taisykles.</span><span class="sxs-lookup"><span data-stu-id="78294-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="78294-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78294-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="78294-132">Priskirkite strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="78294-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="78294-133">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="78294-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="78294-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78294-134">Click New.</span></span>
3. <span data-ttu-id="78294-135">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="78294-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="78294-136">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="78294-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="78294-137">Taisyklės taikomos pagal datą.</span><span class="sxs-lookup"><span data-stu-id="78294-137">The rules are date-effective.</span></span> <span data-ttu-id="78294-138">Vartotojas arba sistema gali baigti taisyklių galiojimą, jei sukurta naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="78294-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="78294-139">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78294-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="78294-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78294-140">Click Save.</span></span>

