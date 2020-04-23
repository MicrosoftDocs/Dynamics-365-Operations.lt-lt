---
title: Medžiagų su „kanban‟ užduotimis perkėlimas
description: Šios procedūros tikslas yra vykdyti išėmimo „kanban“ užduotį, kad būtų perkeltos medžiagos.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210369"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="50f2f-103">Medžiagų su „kanban‟ užduotimis perkėlimas</span><span class="sxs-lookup"><span data-stu-id="50f2f-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50f2f-104">Šios procedūros tikslas yra vykdyti išėmimo „kanban“ užduotį, kad būtų perkeltos medžiagos.</span><span class="sxs-lookup"><span data-stu-id="50f2f-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="50f2f-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="50f2f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="50f2f-106">Ši procedūra skirta sandėlio darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="50f2f-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="50f2f-107">Rodyti perkėlimo užduotis</span><span class="sxs-lookup"><span data-stu-id="50f2f-107">Display transfer jobs</span></span>
1. <span data-ttu-id="50f2f-108">Eikite į Gamybos kontrolė > „Kanban“ > Perkėlimo užduočių „Kanban“ sritis.</span><span class="sxs-lookup"><span data-stu-id="50f2f-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="50f2f-109">Išplėskite arba sutraukite skyrių Filtrai.</span><span class="sxs-lookup"><span data-stu-id="50f2f-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="50f2f-110">Skyriuje „Filtrai“ galite nurodyti, kokias užduotis norite matyti, filtruodami gamybos eigą, veiklos pavadinimą, išvykimo sandėlį ir vietą, atvykimo sandėlį ir vietą.</span><span class="sxs-lookup"><span data-stu-id="50f2f-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="50f2f-111">Lauke „Išvykimo sandėlis“ įveskite „11“.</span><span class="sxs-lookup"><span data-stu-id="50f2f-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="50f2f-112">Lauke „Atvykimo vieta“ įveskite „12“.</span><span class="sxs-lookup"><span data-stu-id="50f2f-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="50f2f-113">Pradėti perkėlimo užduotį</span><span class="sxs-lookup"><span data-stu-id="50f2f-113">Start a transfer job</span></span>
1. <span data-ttu-id="50f2f-114">Sąraše atžymėkite pasirinktą eilutę, jei tokių yra.</span><span class="sxs-lookup"><span data-stu-id="50f2f-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="50f2f-115">Sąraše pasirinkite 4 eilutę.</span><span class="sxs-lookup"><span data-stu-id="50f2f-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="50f2f-116">Pasirinkite pirmą užduotį, kurios būsena „Nesuplanuota“.</span><span class="sxs-lookup"><span data-stu-id="50f2f-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="50f2f-117">Įsitikinkite, kad tai yra vienintelė pasirinkta užduotis.</span><span class="sxs-lookup"><span data-stu-id="50f2f-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="50f2f-118">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="50f2f-118">Click Start.</span></span>
    * <span data-ttu-id="50f2f-119">Atkreipkite dėmesį į piktogramą, kuri nurodo, kad užduotis pradėta.</span><span class="sxs-lookup"><span data-stu-id="50f2f-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="50f2f-120">Pasirinkti antrą perkėlimo užduotį ir pakeisti kiekį</span><span class="sxs-lookup"><span data-stu-id="50f2f-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="50f2f-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="50f2f-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50f2f-122">Galite pasirinkti kelias užduotis, tačiau dabar pasirinkite 5 eilutę.</span><span class="sxs-lookup"><span data-stu-id="50f2f-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="50f2f-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="50f2f-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50f2f-124">Įsitikinkite, kad pažymėta tik ankstesnio veiksmo užduotis.</span><span class="sxs-lookup"><span data-stu-id="50f2f-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="50f2f-125">Atžymėkite visas kitas užduotis.</span><span class="sxs-lookup"><span data-stu-id="50f2f-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="50f2f-126">Užsirašykite lauke „Užduočių kiekis“ esančią reikšmę, kad vėliau ją žinotumėte</span><span class="sxs-lookup"><span data-stu-id="50f2f-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="50f2f-127">Nustatykite užduočių kiekio reikšmę „30“.</span><span class="sxs-lookup"><span data-stu-id="50f2f-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="50f2f-128">Atkreipkite dėmesį į perspėjimą!</span><span class="sxs-lookup"><span data-stu-id="50f2f-128">Notice the warning!</span></span> <span data-ttu-id="50f2f-129">Jums neleidžiama perkelti 30.</span><span class="sxs-lookup"><span data-stu-id="50f2f-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="50f2f-130">Pagal „kanban“ taisyklės konfigūraciją, galite perkelti tik pradinį kiekį.</span><span class="sxs-lookup"><span data-stu-id="50f2f-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="50f2f-131">Naudoti anksčiau užsirašytą reikšmę lauke „Užduočių kiekis“</span><span class="sxs-lookup"><span data-stu-id="50f2f-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="50f2f-132">Nustatykite užduočių kiekį į ankstesnę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="50f2f-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="50f2f-133">Pradėti antrą perkėlimo užduotį</span><span class="sxs-lookup"><span data-stu-id="50f2f-133">Start the second transfer job</span></span>
1. <span data-ttu-id="50f2f-134">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="50f2f-134">Click Start.</span></span>
    * <span data-ttu-id="50f2f-135">Tai pradės užduoties 5 eilutėje perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="50f2f-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="50f2f-136">Baigti abi perkėlimo užduotis</span><span class="sxs-lookup"><span data-stu-id="50f2f-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="50f2f-137">Sąraše pasirinkite 4 eilutę.</span><span class="sxs-lookup"><span data-stu-id="50f2f-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="50f2f-138">Dabar 4 ir 5 eilutėse pažymėtos dvi perkėlimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="50f2f-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="50f2f-139">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="50f2f-139">Click Complete.</span></span>
    * <span data-ttu-id="50f2f-140">Tai užbaigs abiejų užduočių perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="50f2f-140">This will complete the transfer of both jobs.</span></span>  

