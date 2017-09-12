--- 
title: "Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui"
description: "Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų."
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
ms.openlocfilehash: 392cb83ceb8612a2e73cc54bb2d8d40c62a6b7b6
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="4637d-103">Kurti ir priskirti savikainos veikimo būdo strategiją savikainos kontrolės įtaisui</span><span class="sxs-lookup"><span data-stu-id="4637d-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4637d-104">Išlaidų taisyklė yra išlaidų klasifikavimas kaip fiksuotų arba kintamų.</span><span class="sxs-lookup"><span data-stu-id="4637d-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="4637d-105">Kainos kontrolės įtaisui turi būti priskirta strategija ir atitinkamos taisyklės, kad strategija pasidarytų veiksminga.</span><span class="sxs-lookup"><span data-stu-id="4637d-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="4637d-106">Naudokite šią procedūrą norėdami sukurti strategiją, ir tada priskirkite strategiją išlaidų kontrolės įtaisui.</span><span class="sxs-lookup"><span data-stu-id="4637d-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="4637d-107">Sukurkite išlaidų taisyklių hierarchiją</span><span class="sxs-lookup"><span data-stu-id="4637d-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="4637d-108">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="4637d-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="4637d-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-109">Click New.</span></span>
3. <span data-ttu-id="4637d-110">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="4637d-110">Click Create.</span></span>
4. <span data-ttu-id="4637d-111">Dimensijų hierarchijos pavadinimo lauke įveskite „Išlaidų taisyklės hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="4637d-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="4637d-112">Lauke Dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-113">Pasirinkite Savikainos elementai.</span><span class="sxs-lookup"><span data-stu-id="4637d-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="4637d-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4637d-114">Click Save.</span></span>
7. <span data-ttu-id="4637d-115">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="4637d-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="4637d-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-116">Click New.</span></span>
9. <span data-ttu-id="4637d-117">Lauke Mazgo pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="4637d-118">Įveskite Fiksuotą savikainą.</span><span class="sxs-lookup"><span data-stu-id="4637d-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="4637d-119">Medyje pasirinkite „Išlaidų taisyklės hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="4637d-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="4637d-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-120">Click New.</span></span>
12. <span data-ttu-id="4637d-121">Lauke Mazgo pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="4637d-122">Įveskite Kintamą savikainą.</span><span class="sxs-lookup"><span data-stu-id="4637d-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="4637d-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4637d-123">Click Save.</span></span>
14. <span data-ttu-id="4637d-124">Medyje pasirinkite „Cost behavior hierarchy\Fixed cost“.</span><span class="sxs-lookup"><span data-stu-id="4637d-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="4637d-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-125">Click New.</span></span>
16. <span data-ttu-id="4637d-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4637d-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="4637d-127">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-128">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="4637d-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="4637d-129">Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-130">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="4637d-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="4637d-131">Medyje pasirinkite „Cost behavior hierarchy\Variable cost“.</span><span class="sxs-lookup"><span data-stu-id="4637d-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="4637d-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-132">Click New.</span></span>
21. <span data-ttu-id="4637d-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4637d-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="4637d-134">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-135">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="4637d-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="4637d-136">Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-137">Dimensijos narių diapazone gali būti tarpų, tačiau nariai negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="4637d-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="4637d-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4637d-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="4637d-139">Sukurkite strategiją ir taisykles</span><span class="sxs-lookup"><span data-stu-id="4637d-139">Create the policy and rules</span></span>
1. <span data-ttu-id="4637d-140">Eikite į Išlaidų apskaita > Strategijos > Išlaidų taisyklės strategijos.</span><span class="sxs-lookup"><span data-stu-id="4637d-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="4637d-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-141">Click New.</span></span>
3. <span data-ttu-id="4637d-142">Lauke Strategijos pavadinimas įrašykite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4637d-143">Lauke Savikainos elementų dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-144">Pasirinkite savo ką tik sukurtą strategijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="4637d-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="4637d-145">Lauke Savikainos objekto dimensijų hierarchija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-146">Pasirinkti organizaciją</span><span class="sxs-lookup"><span data-stu-id="4637d-146">Select Organization.</span></span>  
6. <span data-ttu-id="4637d-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4637d-147">Click Save.</span></span>
7. <span data-ttu-id="4637d-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-148">Click New.</span></span>
8. <span data-ttu-id="4637d-149">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4637d-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4637d-150">Lauke Savikainos elementų dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-151">Išplėskite hierarchiją, kad pasirinktumėte Kintamą savikainą.</span><span class="sxs-lookup"><span data-stu-id="4637d-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="4637d-152">Lauke Savikainos objekto dimensijų hierarchijos mazgas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4637d-153">Numatytai kintamas procentas yra 100 procentų.</span><span class="sxs-lookup"><span data-stu-id="4637d-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="4637d-154">Spustelėkite Savikainos kontrolės įtaiso strategijos priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="4637d-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="4637d-155">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4637d-155">Click New.</span></span>
13. <span data-ttu-id="4637d-156">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4637d-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4637d-157">Lauke Galioja nuo apskaitos datos įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="4637d-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="4637d-158">Taisyklės taikomos pagal datą, ir vartotojas arba sistema gali baigti taisyklės galiojimą, jei sukurta naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="4637d-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="4637d-159">Lauke Savikainos kontrolės įtaisas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4637d-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="4637d-160">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4637d-160">Click Save.</span></span>


