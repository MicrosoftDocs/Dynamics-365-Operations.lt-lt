--- 
title: "Perkelti medžiagą su „kanban‟ užduotimis (2016 m. vasario mėn.)"
description: "Šios procedūros tikslas yra vykdyti išėmimo „kanban“ užduotį, kad būtų perkeltos medžiagos."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="508f8-103">Perkelti medžiagą su „kanban‟ užduotimis (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="508f8-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="508f8-104">Šios procedūros tikslas yra vykdyti išėmimo „kanban“ užduotį, kad būtų perkeltos medžiagos.</span><span class="sxs-lookup"><span data-stu-id="508f8-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="508f8-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="508f8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="508f8-106">Ši procedūra skirta sandėlio darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="508f8-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="508f8-107">Rodyti perkėlimo užduotis</span><span class="sxs-lookup"><span data-stu-id="508f8-107">Display transfer jobs</span></span>
1. <span data-ttu-id="508f8-108">Eikite į Gamybos kontrolė > „Kanban“ > Perkėlimo užduočių „Kanban“ sritis.</span><span class="sxs-lookup"><span data-stu-id="508f8-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="508f8-109">Išplėskite arba sutraukite skyrių Filtrai.</span><span class="sxs-lookup"><span data-stu-id="508f8-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="508f8-110">Skyriuje „Filtrai“ galite nurodyti, kokias užduotis norite matyti, filtruodami gamybos eigą, veiklos pavadinimą, išvykimo sandėlį ir vietą, atvykimo sandėlį ir vietą.</span><span class="sxs-lookup"><span data-stu-id="508f8-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="508f8-111">Lauke „Išvykimo sandėlis“ įveskite „11“.</span><span class="sxs-lookup"><span data-stu-id="508f8-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="508f8-112">Lauke „Atvykimo vieta“ įveskite „12“.</span><span class="sxs-lookup"><span data-stu-id="508f8-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="508f8-113">Pradėti perkėlimo užduotį</span><span class="sxs-lookup"><span data-stu-id="508f8-113">Start a transfer job</span></span>
1. <span data-ttu-id="508f8-114">Sąraše atžymėkite pasirinktą eilutę, jei tokių yra.</span><span class="sxs-lookup"><span data-stu-id="508f8-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="508f8-115">Sąraše pasirinkite 4 eilutę.</span><span class="sxs-lookup"><span data-stu-id="508f8-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="508f8-116">Pasirinkite pirmą užduotį, kurios būsena „Nesuplanuota“.</span><span class="sxs-lookup"><span data-stu-id="508f8-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="508f8-117">Įsitikinkite, kad tai yra vienintelė pasirinkta užduotis.</span><span class="sxs-lookup"><span data-stu-id="508f8-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="508f8-118">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="508f8-118">Click Start.</span></span>
    * <span data-ttu-id="508f8-119">Atkreipkite dėmesį į piktogramą, kuri nurodo, kad užduotis pradėta.</span><span class="sxs-lookup"><span data-stu-id="508f8-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="508f8-120">Pasirinkti antrą perkėlimo užduotį ir pakeisti kiekį</span><span class="sxs-lookup"><span data-stu-id="508f8-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="508f8-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="508f8-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="508f8-122">Galite pasirinkti kelias užduotis, tačiau dabar pasirinkite 5 eilutę.</span><span class="sxs-lookup"><span data-stu-id="508f8-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="508f8-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="508f8-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="508f8-124">Įsitikinkite, kad pažymėta tik ankstesnio veiksmo užduotis.</span><span class="sxs-lookup"><span data-stu-id="508f8-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="508f8-125">Atžymėkite visas kitas užduotis.</span><span class="sxs-lookup"><span data-stu-id="508f8-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="508f8-126">Užsirašykite lauke „Užduočių kiekis“ esančią reikšmę, kad vėliau ją žinotumėte</span><span class="sxs-lookup"><span data-stu-id="508f8-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="508f8-127">Nustatykite užduočių kiekio reikšmę „30“.</span><span class="sxs-lookup"><span data-stu-id="508f8-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="508f8-128">Atkreipkite dėmesį į perspėjimą!</span><span class="sxs-lookup"><span data-stu-id="508f8-128">Notice the warning!</span></span> <span data-ttu-id="508f8-129">Jums neleidžiama perkelti 30.</span><span class="sxs-lookup"><span data-stu-id="508f8-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="508f8-130">Pagal „kanban“ taisyklės konfigūraciją, galite perkelti tik pradinį kiekį.</span><span class="sxs-lookup"><span data-stu-id="508f8-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="508f8-131">Naudoti anksčiau užsirašytą reikšmę lauke „Užduočių kiekis“</span><span class="sxs-lookup"><span data-stu-id="508f8-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="508f8-132">Nustatykite užduočių kiekį į ankstesnę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="508f8-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="508f8-133">Pradėti antrą perkėlimo užduotį</span><span class="sxs-lookup"><span data-stu-id="508f8-133">Start the second transfer job</span></span>
1. <span data-ttu-id="508f8-134">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="508f8-134">Click Start.</span></span>
    * <span data-ttu-id="508f8-135">Tai pradės užduoties 5 eilutėje perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="508f8-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="508f8-136">Baigti abi perkėlimo užduotis</span><span class="sxs-lookup"><span data-stu-id="508f8-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="508f8-137">Sąraše pasirinkite 4 eilutę.</span><span class="sxs-lookup"><span data-stu-id="508f8-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="508f8-138">Dabar 4 ir 5 eilutėse pažymėtos dvi perkėlimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="508f8-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="508f8-139">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="508f8-139">Click Complete.</span></span>
    * <span data-ttu-id="508f8-140">Tai užbaigs abiejų užduočių perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="508f8-140">This will complete the transfer of both jobs.</span></span>  

