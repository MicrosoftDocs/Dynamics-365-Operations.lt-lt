---
title: Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui
description: Savikainos paskirstymo taisyklės naudojamos norint paskirstyti savikainą, kuri buvo finansiškai apskaičiuota kolektyviniame išlaidų centre.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b269c731776e26df24658feedfa301181c309a14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969283"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="ebe2d-103">Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="ebe2d-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebe2d-104">Savikainos paskirstymo taisyklės naudojamos norint paskirstyti savikainą, kuri buvo finansiškai apskaičiuota kolektyviniame išlaidų centre.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="ebe2d-105">Savikainos apskaitininkas užtikrina, kad savikaina būtų paskirstyta išlaidų centrams remiantis paskirstymo pagrindu.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="ebe2d-106">Strategija ir atitinkamos taisyklės priskiriamos savikainos kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="ebe2d-107">Šiame užduočių vedlyje naudojamas pavyzdys, norint parodyti, kaip sukurti savikainos paskirstymo strategiją ir atitinkamas taisykles.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="ebe2d-108">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="ebe2d-108">Create a policy</span></span>
1. <span data-ttu-id="ebe2d-109">Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="ebe2d-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-110">Click New.</span></span>
3. <span data-ttu-id="ebe2d-111">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="ebe2d-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ebe2d-113">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-114">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="ebe2d-114">Select Organization.</span></span>  
6. <span data-ttu-id="ebe2d-115">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-116">Pasirinkite CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="ebe2d-117">Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-118">Pasirinkite statistinius elementus.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="ebe2d-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="ebe2d-120">Sukurkite taisykles strategijai</span><span class="sxs-lookup"><span data-stu-id="ebe2d-120">Create rules for the policy</span></span>
1. <span data-ttu-id="ebe2d-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-121">Click New.</span></span>
2. <span data-ttu-id="ebe2d-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ebe2d-123">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-124">Išplėskite hierarchiją, kad pasirinktumėte 094.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="ebe2d-125">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-126">Pasirinkite Kitos veiklos išlaidos ir tada pasirinkite 605110 valymas.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="ebe2d-127">Lauke Savikainos taisyklė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="ebe2d-128">Pasirinkite Fiksuota savikaina.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="ebe2d-129">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="ebe2d-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-130">Click New.</span></span>
8. <span data-ttu-id="ebe2d-131">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ebe2d-132">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-133">Išplėskite hierarchiją, kad pasirinktumėte 094.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="ebe2d-134">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ebe2d-135">Pasirinkite Kitos veiklos išlaidos ir tada pasirinkite 605150 nuoma.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="ebe2d-136">Lauke Savikainos taisyklė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="ebe2d-137">Pasirinkite Fiksuota savikaina.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="ebe2d-138">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="ebe2d-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="ebe2d-140">Priskirkite taisykles išlaidų kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="ebe2d-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="ebe2d-141">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="ebe2d-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-142">Click New.</span></span>
3. <span data-ttu-id="ebe2d-143">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ebe2d-144">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="ebe2d-145">Pasirinkite tinkamų finansinių metų rugsėjo 1.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="ebe2d-146">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="ebe2d-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ebe2d-147">Click Save.</span></span>

