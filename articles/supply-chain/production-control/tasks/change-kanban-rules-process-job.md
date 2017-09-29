--- 
title: "Keisti apdorojimo užduoties „kanban“ taisykles"
description: "Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="7481a-103">Keisti apdorojimo užduoties „kanban“ taisykles</span><span class="sxs-lookup"><span data-stu-id="7481a-103">Change kanban rules for a process job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7481a-104">Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“.</span><span class="sxs-lookup"><span data-stu-id="7481a-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="7481a-105">Tai naudinga norint išlyginti arba paskirstyti krovinio išteklius.</span><span class="sxs-lookup"><span data-stu-id="7481a-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="7481a-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="7481a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7481a-107">Ši procedūra skirta planuotojui, dirbančiam „lean“ gamybos įmonėje, kuri yra atsakinga už vertės srautą.</span><span class="sxs-lookup"><span data-stu-id="7481a-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="7481a-108">Kopijuokite „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="7481a-108">Copy kanban rule</span></span>
1. <span data-ttu-id="7481a-109">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="7481a-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7481a-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7481a-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7481a-111">Pasirinkite L0001 įvykio „Kanban“ taisyklę 000022.</span><span class="sxs-lookup"><span data-stu-id="7481a-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="7481a-112">Spustelėkite „Kanban“ taisyklės kopijavimas.</span><span class="sxs-lookup"><span data-stu-id="7481a-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="7481a-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7481a-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="7481a-114">Keisti „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="7481a-114">Change kanban rule</span></span>
1. <span data-ttu-id="7481a-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7481a-115">Close the page.</span></span>
2. <span data-ttu-id="7481a-116">Pasirinkite „Kanban“ užduoties planavimas.</span><span class="sxs-lookup"><span data-stu-id="7481a-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="7481a-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7481a-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7481a-118">Pasirinkite eilutę su „Kanban“ 000177.</span><span class="sxs-lookup"><span data-stu-id="7481a-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="7481a-119">Spustelėkite Naudoti alternatyvią „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7481a-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="7481a-120">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="7481a-120">Click Next.</span></span>
6. <span data-ttu-id="7481a-121">Lauke „Kanban“ taisyklė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7481a-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="7481a-122">Pasirinkite anksčiau sukurtą „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7481a-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="7481a-123">Tai yra „kanban“ taisyklė, kurios numeris didžiausias.</span><span class="sxs-lookup"><span data-stu-id="7481a-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="7481a-124">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="7481a-124">Click Finish.</span></span>
    * <span data-ttu-id="7481a-125">Dabar „kanban“ užduotis naudoja kitą „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7481a-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="7481a-126">Tai gali būti naudinga norint išlyginti krovinio darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7481a-126">This can be useful to level load work cells.</span></span>  

