---
title: Keisti apdorojimo užduoties „kanban“ taisykles
description: Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554281"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="7535f-103">Keisti apdorojimo užduoties „kanban“ taisykles</span><span class="sxs-lookup"><span data-stu-id="7535f-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7535f-104">Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“.</span><span class="sxs-lookup"><span data-stu-id="7535f-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="7535f-105">Tai naudinga norint išlyginti arba paskirstyti krovinio išteklius.</span><span class="sxs-lookup"><span data-stu-id="7535f-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="7535f-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="7535f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7535f-107">Ši procedūra skirta planuotojui, dirbančiam „lean“ gamybos įmonėje, kuri yra atsakinga už vertės srautą.</span><span class="sxs-lookup"><span data-stu-id="7535f-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="7535f-108">Kopijuokite „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="7535f-108">Copy kanban rule</span></span>
1. <span data-ttu-id="7535f-109">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="7535f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7535f-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7535f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7535f-111">Pasirinkite L0001 įvykio „Kanban“ taisyklę 000022.</span><span class="sxs-lookup"><span data-stu-id="7535f-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="7535f-112">Spustelėkite „Kanban“ taisyklės kopijavimas.</span><span class="sxs-lookup"><span data-stu-id="7535f-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="7535f-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7535f-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="7535f-114">Keisti „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="7535f-114">Change kanban rule</span></span>
1. <span data-ttu-id="7535f-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7535f-115">Close the page.</span></span>
2. <span data-ttu-id="7535f-116">Pasirinkite „Kanban“ užduoties planavimas.</span><span class="sxs-lookup"><span data-stu-id="7535f-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="7535f-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7535f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7535f-118">Pasirinkite eilutę su „Kanban“ 000177.</span><span class="sxs-lookup"><span data-stu-id="7535f-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="7535f-119">Spustelėkite Naudoti alternatyvią „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7535f-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="7535f-120">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="7535f-120">Click Next.</span></span>
6. <span data-ttu-id="7535f-121">Lauke „Kanban“ taisyklė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7535f-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="7535f-122">Pasirinkite anksčiau sukurtą „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7535f-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="7535f-123">Tai yra „kanban“ taisyklė, kurios numeris didžiausias.</span><span class="sxs-lookup"><span data-stu-id="7535f-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="7535f-124">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="7535f-124">Click Finish.</span></span>
    * <span data-ttu-id="7535f-125">Dabar „kanban“ užduotis naudoja kitą „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7535f-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="7535f-126">Tai gali būti naudinga norint išlyginti krovinio darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7535f-126">This can be useful to level load work cells.</span></span>  

