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
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d040f9495c7fb36985b5f96c15ac43aa226da24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179034"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="df5e5-103">Kurti ir priskirti savikainos paskirstymo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="df5e5-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df5e5-104">Savikainos paskirstymo taisyklės naudojamos norint paskirstyti savikainą, kuri buvo finansiškai apskaičiuota kolektyviniame išlaidų centre.</span><span class="sxs-lookup"><span data-stu-id="df5e5-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="df5e5-105">Savikainos apskaitininkas užtikrina, kad savikaina būtų paskirstyta išlaidų centrams remiantis paskirstymo pagrindu.</span><span class="sxs-lookup"><span data-stu-id="df5e5-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="df5e5-106">Strategija ir atitinkamos taisyklės priskiriamos savikainos kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="df5e5-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="df5e5-107">Šiame užduočių vedlyje naudojamas pavyzdys, norint parodyti, kaip sukurti savikainos paskirstymo strategiją ir atitinkamas taisykles.</span><span class="sxs-lookup"><span data-stu-id="df5e5-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="df5e5-108">Sukurkite strategiją</span><span class="sxs-lookup"><span data-stu-id="df5e5-108">Create a policy</span></span>
1. <span data-ttu-id="df5e5-109">Eikite į Išlaidų apskaita > Strategijos > Savikainos paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="df5e5-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="df5e5-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="df5e5-110">Click New.</span></span>
3. <span data-ttu-id="df5e5-111">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="df5e5-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="df5e5-113">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-114">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="df5e5-114">Select Organization.</span></span>  
6. <span data-ttu-id="df5e5-115">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-116">Pasirinkite CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="df5e5-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="df5e5-117">Lauke Statistikos dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-118">Pasirinkite statistinius elementus.</span><span class="sxs-lookup"><span data-stu-id="df5e5-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="df5e5-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="df5e5-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="df5e5-120">Sukurkite taisykles strategijai</span><span class="sxs-lookup"><span data-stu-id="df5e5-120">Create rules for the policy</span></span>
1. <span data-ttu-id="df5e5-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="df5e5-121">Click New.</span></span>
2. <span data-ttu-id="df5e5-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="df5e5-123">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-124">Išplėskite hierarchiją, kad pasirinktumėte 094.</span><span class="sxs-lookup"><span data-stu-id="df5e5-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="df5e5-125">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-126">Pasirinkite Kitos veiklos išlaidos ir tada pasirinkite 605110 valymas.</span><span class="sxs-lookup"><span data-stu-id="df5e5-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="df5e5-127">Lauke Savikainos taisyklė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="df5e5-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="df5e5-128">Pasirinkite Fiksuota savikaina.</span><span class="sxs-lookup"><span data-stu-id="df5e5-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="df5e5-129">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="df5e5-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="df5e5-130">Click New.</span></span>
8. <span data-ttu-id="df5e5-131">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="df5e5-132">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-133">Išplėskite hierarchiją, kad pasirinktumėte 094.</span><span class="sxs-lookup"><span data-stu-id="df5e5-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="df5e5-134">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="df5e5-135">Pasirinkite Kitos veiklos išlaidos ir tada pasirinkite 605150 nuoma.</span><span class="sxs-lookup"><span data-stu-id="df5e5-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="df5e5-136">Lauke Savikainos taisyklė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="df5e5-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="df5e5-137">Pasirinkite Fiksuota savikaina.</span><span class="sxs-lookup"><span data-stu-id="df5e5-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="df5e5-138">Lauke Paskirstymo pagrindas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="df5e5-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="df5e5-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="df5e5-140">Priskirkite taisykles išlaidų kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="df5e5-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="df5e5-141">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="df5e5-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="df5e5-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="df5e5-142">Click New.</span></span>
3. <span data-ttu-id="df5e5-143">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="df5e5-144">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="df5e5-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="df5e5-145">Pasirinkite tinkamų finansinių metų rugsėjo 1.</span><span class="sxs-lookup"><span data-stu-id="df5e5-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="df5e5-146">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df5e5-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="df5e5-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="df5e5-147">Click Save.</span></span>

