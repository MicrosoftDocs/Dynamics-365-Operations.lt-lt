---
title: Parengti „kanban“ užduoties apdorojimą, kai yra darbo elemento medžiagų
description: Šios užduoties tikslas yra parengti proceso „kanban“ užduotį, kai yra visų darbo elemento medžiagų.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12773cc6d94a34197084c8fe12c90167d4dca62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977768"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="c2633-103">Parengti „kanban“ užduoties apdorojimą, kai yra darbo elemento medžiagų</span><span class="sxs-lookup"><span data-stu-id="c2633-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2633-104">Šios užduoties tikslas yra parengti proceso „kanban“ užduotį, kai yra visų darbo elemento medžiagų.</span><span class="sxs-lookup"><span data-stu-id="c2633-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="c2633-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="c2633-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c2633-106">Ši užduotis skirta mašinos operatoriui.</span><span class="sxs-lookup"><span data-stu-id="c2633-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="c2633-107">Eikite į proceso užduočių „kanban“ sritį.</span><span class="sxs-lookup"><span data-stu-id="c2633-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="c2633-108">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c2633-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c2633-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c2633-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c2633-110">Pasirinkite darbo elementą 1250 ir spustelėkite „Gerai“.</span><span class="sxs-lookup"><span data-stu-id="c2633-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="c2633-111">Sąraše pasirinkite 4 eilutę.</span><span class="sxs-lookup"><span data-stu-id="c2633-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="c2633-112">Švarioje demonstracinėje įmonėje pirmas dar nebaigta užduotis yra „Kanban“ 000329 4 eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c2633-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="c2633-113">Perjunkite skyriaus „Išrinkimo dokumentas“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="c2633-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="c2633-114">Patikrinkite, ar išrinkimo dokumente yra visų prekių tiekimo būsena.</span><span class="sxs-lookup"><span data-stu-id="c2633-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="c2633-115">Pasirinkus kelias užduotis, išrinkimo dokumentas rodys visų pasirinktoms užduotims reikalingų prekių sumą.</span><span class="sxs-lookup"><span data-stu-id="c2633-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="c2633-116">Spustelėkite „Parengti“.</span><span class="sxs-lookup"><span data-stu-id="c2633-116">Click Prepare.</span></span>
    * <span data-ttu-id="c2633-117">Dabar paruošimo procesas baigtas.</span><span class="sxs-lookup"><span data-stu-id="c2633-117">The preparation process is now completed.</span></span> <span data-ttu-id="c2633-118">Pasirinktas visų išrinkimo dokumente esančių eilučių žymės langelis nurodo, kad tiekimo būsena paimta.</span><span class="sxs-lookup"><span data-stu-id="c2633-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

