--- 
title: "Parengti „kanban“ užduoties apdorojimą, kai yra darbo elemento medžiagų"
description: "Šios užduoties tikslas yra parengti proceso „kanban“ užduotį, kai yra visų darbo elemento medžiagų."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 62f3f71cc5e47f0fb027211a911e61673ca2e375
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="4dc64-103">Parengti „kanban“ užduoties apdorojimą, kai yra darbo elemento medžiagų</span><span class="sxs-lookup"><span data-stu-id="4dc64-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dc64-104">Šios užduoties tikslas yra parengti proceso „kanban“ užduotį, kai yra visų darbo elemento medžiagų.</span><span class="sxs-lookup"><span data-stu-id="4dc64-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="4dc64-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="4dc64-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="4dc64-106">Ši užduotis skirta mašinos operatoriui.</span><span class="sxs-lookup"><span data-stu-id="4dc64-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="4dc64-107">Eikite į proceso užduočių „kanban“ sritį.</span><span class="sxs-lookup"><span data-stu-id="4dc64-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="4dc64-108">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4dc64-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4dc64-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4dc64-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4dc64-110">Pasirinkite darbo elementą 1250 ir spustelėkite „Gerai“.</span><span class="sxs-lookup"><span data-stu-id="4dc64-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="4dc64-111">Sąraše pasirinkite 4 eilutę.</span><span class="sxs-lookup"><span data-stu-id="4dc64-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="4dc64-112">Švarioje demonstracinėje įmonėje pirmas dar nebaigta užduotis yra „Kanban“ 000329 4 eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4dc64-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="4dc64-113">Perjunkite skyriaus „Išrinkimo dokumentas“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="4dc64-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="4dc64-114">Patikrinkite, ar išrinkimo dokumente yra visų prekių tiekimo būsena.</span><span class="sxs-lookup"><span data-stu-id="4dc64-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="4dc64-115">Pasirinkus kelias užduotis, išrinkimo dokumentas rodys visų pasirinktoms užduotims reikalingų prekių sumą.</span><span class="sxs-lookup"><span data-stu-id="4dc64-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="4dc64-116">Spustelėkite „Parengti“.</span><span class="sxs-lookup"><span data-stu-id="4dc64-116">Click Prepare.</span></span>
    * <span data-ttu-id="4dc64-117">Dabar paruošimo procesas baigtas.</span><span class="sxs-lookup"><span data-stu-id="4dc64-117">The preparation process is now completed.</span></span> <span data-ttu-id="4dc64-118">Pasirinktas visų išrinkimo dokumente esančių eilučių žymės langelis nurodo, kad tiekimo būsena paimta.</span><span class="sxs-lookup"><span data-stu-id="4dc64-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  


