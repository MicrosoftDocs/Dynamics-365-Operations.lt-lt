--- 
title: "Skaičiuoti „kanban“ kiekio pasiūlymus"
description: "Šios procedūros tikslas yra optimizuoti „kanban“ dydį ir kiekį pagal konkrečią „kanban“ taisyklę, naudojant „kanban“ kiekio skaičiavimą."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8c9a7d7e4e2d751722dac8089bc2056334fa96a3
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="be260-103">Skaičiuoti „kanban“ kiekio pasiūlymus</span><span class="sxs-lookup"><span data-stu-id="be260-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be260-104">Šios procedūros tikslas yra optimizuoti „kanban“ dydį ir kiekį pagal konkrečią „kanban“ taisyklę, naudojant „kanban“ kiekio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="be260-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="be260-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="be260-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="be260-106">Ši procedūra skirta vertės srauto vadybininkui.</span><span class="sxs-lookup"><span data-stu-id="be260-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="be260-107">Būtina, kad užbaigtumėte procedūrą „Į „kanban“ taisyklę įtraukti naują „kanban“ kiekio skaičiavimo strategiją“.</span><span class="sxs-lookup"><span data-stu-id="be260-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="be260-108">Kurti „kanban“ kiekio skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="be260-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="be260-109">Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ kiekio skaičiavimas > Skaičiuoti „kanban“ kiekį.</span><span class="sxs-lookup"><span data-stu-id="be260-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="be260-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="be260-110">Click New.</span></span>
3. <span data-ttu-id="be260-111">Lauke „Pavadinimas“, įveskite „Speaker2016“.</span><span class="sxs-lookup"><span data-stu-id="be260-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="be260-112">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="be260-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="be260-113">Pasirinkite strategiją, kurią sukūrėte procedūroje „Į „kanban“ taisyklę įtraukti naują „kanban“ kiekio skaičiavimo strategiją“.</span><span class="sxs-lookup"><span data-stu-id="be260-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="be260-114">Pvz., „Speaker2016“.</span><span class="sxs-lookup"><span data-stu-id="be260-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="be260-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="be260-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="be260-116">Lauke „Taisyklės aktyvumo pradžios data“ nustatykite tokią datą ir laiką: „2012-12-17T08:00:00“.</span><span class="sxs-lookup"><span data-stu-id="be260-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="be260-117">Ši data naudojama kaip pagrindas nustatant, kurios fiksuotos „kanban“ taisyklės įtraukiamos į „kanban“ kiekio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="be260-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="be260-118">Lauke „Patenkinto poreikio laikotarpio pradžios data“ nustatykite tokią datą ir laiką: „2012-11-17T09:00:00“.</span><span class="sxs-lookup"><span data-stu-id="be260-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="be260-119">Data, nuo kurios buvusios poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.</span><span class="sxs-lookup"><span data-stu-id="be260-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="be260-120">Lauke „Patenkinto poreikio laikotarpio pabaigos data“ nustatykite tokią datą ir laiką: „2012-12-17T07:59:59“.</span><span class="sxs-lookup"><span data-stu-id="be260-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="be260-121">Data, iki kurios buvusios poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.</span><span class="sxs-lookup"><span data-stu-id="be260-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="be260-122">Lauke „Poreikio laikotarpio pradžios data“ nustatykite tokią datą ir laiką: „2012-12-17T08:00:00“.</span><span class="sxs-lookup"><span data-stu-id="be260-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="be260-123">Data, nuo kurios dabartinės poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.</span><span class="sxs-lookup"><span data-stu-id="be260-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="be260-124">Lauke „Poreikio laikotarpio pabaigos data“ nustatykite tokią datą ir laiką: „2013-01-16T07:59:59“.</span><span class="sxs-lookup"><span data-stu-id="be260-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="be260-125">Data, iki kurios dabartinės poreikio operacijos įtraukiamos skaičiuojant „kanban“ kiekį.</span><span class="sxs-lookup"><span data-stu-id="be260-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="be260-126">Generuoti „kanban“ kiekio pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="be260-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="be260-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="be260-127">Click Save.</span></span>
2. <span data-ttu-id="be260-128">Spustelėkite „Generuoti“.</span><span class="sxs-lookup"><span data-stu-id="be260-128">Click Generate.</span></span>
    * <span data-ttu-id="be260-129">Tai generuoja „kanban“ taisyklės 000020 „kanban“ kiekio pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="be260-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="be260-130">Vykdyti „kanban“ kiekio skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="be260-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="be260-131">Spustelėkite „Skaičiuoti“.</span><span class="sxs-lookup"><span data-stu-id="be260-131">Click Calculate.</span></span>
    * <span data-ttu-id="be260-132">Tai apskaičiuoja „kanban“ kiekio pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="be260-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="be260-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="be260-133">Click OK.</span></span>
3. <span data-ttu-id="be260-134">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="be260-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="be260-135">Atkreipkite dėmesį, kad siūlomas „kanban“ kiekis yra 2.</span><span class="sxs-lookup"><span data-stu-id="be260-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="be260-136">Pakeisti produktų kiekį ir dar kartą skaičiuoti</span><span class="sxs-lookup"><span data-stu-id="be260-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="be260-137">Nustatykite produkto kiekio reikšmę „5“.</span><span class="sxs-lookup"><span data-stu-id="be260-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="be260-138">Spustelėkite „Skaičiuoti“.</span><span class="sxs-lookup"><span data-stu-id="be260-138">Click Calculate.</span></span>
3. <span data-ttu-id="be260-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="be260-139">Click OK.</span></span>
    * <span data-ttu-id="be260-140">Atkreipkite dėmesį, kad, kai „kanban“ kiekis yra 5, pasiūlymas pakeičiamas į 4 „kanban“ kiekį.</span><span class="sxs-lookup"><span data-stu-id="be260-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="be260-141">Tai lemia aplinkybė, kad, esant mažesniam produkto kiekiui, reikia didesnio kiekio „kanban“, kad būtų patenkintas poreikis.</span><span class="sxs-lookup"><span data-stu-id="be260-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="be260-142">Atnaujinti „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="be260-142">Update kanban rule</span></span>
1. <span data-ttu-id="be260-143">Lauke „Taisyklės įsigaliojimo data“ įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="be260-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="be260-144">Nustatykite ateities datą parinkčiai „Taisyklės aktyvumo pradžios data“.</span><span class="sxs-lookup"><span data-stu-id="be260-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="be260-145">Pvz., šiandien + vieneri metai.</span><span class="sxs-lookup"><span data-stu-id="be260-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="be260-146">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="be260-146">Click Update.</span></span>
3. <span data-ttu-id="be260-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="be260-147">Click OK.</span></span>
4. <span data-ttu-id="be260-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="be260-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="be260-149">Patvirtinti „kanban“ taisyklės pakeitimą</span><span class="sxs-lookup"><span data-stu-id="be260-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="be260-150">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="be260-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="be260-151">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="be260-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be260-152">Pasirinkti „kanban“ taisyklę, kuri buvo sukurta ankstesnėje papildomoje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="be260-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="be260-153">Tai turėtų būti pirmoji „kanban“ taisyklė pagal numerį surūšiuotame sąraše.</span><span class="sxs-lookup"><span data-stu-id="be260-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="be260-154">Perjunkite skyriaus „Išsami informacija“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="be260-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="be260-155">Atkreipkite dėmesį į įsigaliojimo datą, kuri reiškia, kad ši taisyklė iki šios datos neaktyvinama.</span><span class="sxs-lookup"><span data-stu-id="be260-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="be260-156">Perjunkite skyriaus „Kiekiai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="be260-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="be260-157">Atkreipkite dėmesį, kad tai yra numatytasis kiekis, kurį įvedėte į „kanban“ kiekio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="be260-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="be260-158">Atkreipkite dėmesį, kad tai yra fiksuotas 4 „kanban“ kiekis iš „kanban“ kiekio skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="be260-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="be260-159">Spustelėkite skirtuką „ListPanel“.</span><span class="sxs-lookup"><span data-stu-id="be260-159">Click the ListPanel tab.</span></span>


