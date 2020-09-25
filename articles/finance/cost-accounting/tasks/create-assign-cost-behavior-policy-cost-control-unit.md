---
title: Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui
description: Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f52133df2d374d6dc0f1efb33ffc85eb7d11fa9
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759237"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="63879-103">Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="63879-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63879-104">Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų.</span><span class="sxs-lookup"><span data-stu-id="63879-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="63879-105">Kainos kontrolės įtaisui turi būti priskirta strategija ir atitinkamos taisyklės, kad strategija pasidarytų veiksminga.</span><span class="sxs-lookup"><span data-stu-id="63879-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="63879-106">Naudokite šią procedūrą norėdami sukurti strategiją, ir tada priskirkite strategiją išlaidų kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="63879-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="63879-107">Sukurkite išlaidų taisyklių hierarchiją</span><span class="sxs-lookup"><span data-stu-id="63879-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="63879-108">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="63879-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="63879-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-109">Click New.</span></span>
3. <span data-ttu-id="63879-110">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="63879-110">Click Create.</span></span>
4. <span data-ttu-id="63879-111">Dimensijų hierarchijos pavadinimo lauke įveskite „Išlaidų taisyklės hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="63879-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="63879-112">Lauke Dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-113">Pasirinkite Savikainos elementai.</span><span class="sxs-lookup"><span data-stu-id="63879-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="63879-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63879-114">Click Save.</span></span>
7. <span data-ttu-id="63879-115">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="63879-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="63879-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-116">Click New.</span></span>
9. <span data-ttu-id="63879-117">Lauke Mazgo pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="63879-118">Įveskite Fiksuotą savikainą.</span><span class="sxs-lookup"><span data-stu-id="63879-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="63879-119">Medyje pasirinkite „Išlaidų taisyklės hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="63879-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="63879-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-120">Click New.</span></span>
12. <span data-ttu-id="63879-121">Lauke Mazgo pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="63879-122">Įveskite Kintamą savikainą.</span><span class="sxs-lookup"><span data-stu-id="63879-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="63879-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63879-123">Click Save.</span></span>
14. <span data-ttu-id="63879-124">Medyje pasirinkite „Cost behavior hierarchy\Fixed cost“.</span><span class="sxs-lookup"><span data-stu-id="63879-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="63879-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-125">Click New.</span></span>
16. <span data-ttu-id="63879-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="63879-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="63879-127">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-128">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="63879-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="63879-129">Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-130">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="63879-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="63879-131">Medyje pasirinkite „Cost behavior hierarchy\Variable cost“.</span><span class="sxs-lookup"><span data-stu-id="63879-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="63879-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-132">Click New.</span></span>
21. <span data-ttu-id="63879-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="63879-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="63879-134">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-135">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="63879-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="63879-136">Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-137">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="63879-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="63879-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63879-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="63879-139">Sukurkite strategiją ir taisykles</span><span class="sxs-lookup"><span data-stu-id="63879-139">Create the policy and rules</span></span>
1. <span data-ttu-id="63879-140">Eikite į Išlaidų apskaita > Strategijos > Išlaidų taisyklės strategijos.</span><span class="sxs-lookup"><span data-stu-id="63879-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="63879-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-141">Click New.</span></span>
3. <span data-ttu-id="63879-142">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="63879-143">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-144">Pasirinkite savo ką tik sukurtą strategijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="63879-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="63879-145">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-146">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="63879-146">Select Organization.</span></span>  
6. <span data-ttu-id="63879-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63879-147">Click Save.</span></span>
7. <span data-ttu-id="63879-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-148">Click New.</span></span>
8. <span data-ttu-id="63879-149">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="63879-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="63879-150">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-151">Išplėskite hierarchiją, kad pasirinktumėte Kintamą savikainą.</span><span class="sxs-lookup"><span data-stu-id="63879-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="63879-152">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="63879-153">Numatytai kintamas procentas yra 100 procentų.</span><span class="sxs-lookup"><span data-stu-id="63879-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="63879-154">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="63879-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="63879-155">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63879-155">Click New.</span></span>
13. <span data-ttu-id="63879-156">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="63879-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="63879-157">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="63879-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="63879-158">Taisyklės taikomos pagal datą, ir vartotojas arba sistema gali baigti taisyklės galiojimą, jei sukurta naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="63879-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="63879-159">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63879-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="63879-160">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63879-160">Click Save.</span></span>

