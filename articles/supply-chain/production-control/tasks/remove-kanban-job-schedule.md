---
title: Pašalinti „kanban“ užduotį iš grafiko
description: Šia procedūra dėmesys skiriamas suplanuotos „kanban‟ apdorojimo užduoties pašalinimui iš grafiko, užduoties būseną pakeičiant į Nesuplanuotą.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210600"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="9e5b8-103">Pašalinti „kanban“ užduotį iš grafiko</span><span class="sxs-lookup"><span data-stu-id="9e5b8-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e5b8-104">Šia procedūra dėmesys skiriamas suplanuotos „kanban‟ apdorojimo užduoties pašalinimui iš grafiko, užduoties būseną pakeičiant į Nesuplanuotą.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="9e5b8-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9e5b8-106">Ši procedūra yra skirta darbo laiko prižiūrėtojui arba gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="9e5b8-107">Rasti suplanuotą „kanban“ užduotį</span><span class="sxs-lookup"><span data-stu-id="9e5b8-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="9e5b8-108">Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ užduočių planavimas.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="9e5b8-109">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9e5b8-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e5b8-111">Pasirinkite 1250 darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="9e5b8-112">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-112">Click Select.</span></span>
5. <span data-ttu-id="9e5b8-113">Lauke Rodyti užduoties būseną pasirinkite „Suplanuota‟.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="9e5b8-114">Pašalinti suplanuotą „kanban“ užduotį iš grafiko</span><span class="sxs-lookup"><span data-stu-id="9e5b8-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="9e5b8-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e5b8-116">Pasirinkite užduotį, kurios būsena Suplanuota, pvz., 2012 m. gruodžio 19 d. užduotį.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="9e5b8-117">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="9e5b8-118">Spustelėkite Grąžinti užduoties būseną.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-118">Click Revert job status.</span></span>
4. <span data-ttu-id="9e5b8-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-119">Click OK.</span></span>
    * <span data-ttu-id="9e5b8-120">Dabartinės užduoties būsena iš „Suplanuotos‟ bus pakeista į „Nesuplanuotą‟ ir ji bus pašalinta iš proceso srities.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

