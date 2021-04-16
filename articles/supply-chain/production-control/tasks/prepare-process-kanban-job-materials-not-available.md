---
title: Parengti „kanban“ užduoties apdorojimą, kai nėra darbo elemento medžiagų
description: Šios procedūros tikslas yra parengti proceso „kanban“ užduotį, kai darbo elementui trūksta kai kurių medžiagų, todėl būtina paimti medžiagas iš sandėlio.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72fd083edc48504b35f540ea7bdc8c8c736418f3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828639"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="b198f-103">Parengti „kanban“ užduoties apdorojimą, kai nėra darbo elemento medžiagų</span><span class="sxs-lookup"><span data-stu-id="b198f-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b198f-104">Šios procedūros tikslas yra parengti proceso „kanban“ užduotį, kai darbo elementui trūksta kai kurių medžiagų, todėl būtina paimti medžiagas iš sandėlio.</span><span class="sxs-lookup"><span data-stu-id="b198f-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="b198f-105">Būtina šios procedūros sukūrimo sąlyga yra procedūra „Parengti proceso „kanban“ užduotį, kai yra reikiamų medžiagų“.</span><span class="sxs-lookup"><span data-stu-id="b198f-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="b198f-106">Ši procedūra skirta mašinos operatoriui.</span><span class="sxs-lookup"><span data-stu-id="b198f-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="b198f-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b198f-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b198f-108">Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ sritis proceso užduotims.</span><span class="sxs-lookup"><span data-stu-id="b198f-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="b198f-109">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b198f-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b198f-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b198f-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b198f-111">Pasirinkite 1250 darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="b198f-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="b198f-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b198f-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b198f-113">Pasirinkite „Kanban“ 000356.</span><span class="sxs-lookup"><span data-stu-id="b198f-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="b198f-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b198f-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b198f-115">Sąraše panaikinkite 4 eilutės žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="b198f-115">In the list, deselect row 4.</span></span> <span data-ttu-id="b198f-116">arba pažymėkite 4 eilutę, jei nebaigėte užduoties „Parengti proceso „kanban“ užduotį, kai yra reikiamų medžiagų“.</span><span class="sxs-lookup"><span data-stu-id="b198f-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="b198f-117">Perjunkite skyriaus „Išrinkimo dokumentas“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="b198f-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="b198f-118">Įrašo „Ne“ piktograma tiekimo būsenoje nurodo, kad darbo elementui trūksta 48 ae prekės P0002.</span><span class="sxs-lookup"><span data-stu-id="b198f-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="b198f-119">Perkelti medžiagas į darbo elementą</span><span class="sxs-lookup"><span data-stu-id="b198f-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="b198f-120">Perjunkite skyriaus „Perkėlimo užduotys“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="b198f-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="b198f-121">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Prekės numeris pagal reikšmę P0002.</span><span class="sxs-lookup"><span data-stu-id="b198f-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="b198f-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b198f-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b198f-123">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="b198f-123">Click Start.</span></span>
    * <span data-ttu-id="b198f-124">Vyksta perdavimas.</span><span class="sxs-lookup"><span data-stu-id="b198f-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="b198f-125">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="b198f-125">Click Complete.</span></span>
    * <span data-ttu-id="b198f-126">Prekė P0002 dabar yra „kanban“ užduoties išrinkimo dokumente.</span><span class="sxs-lookup"><span data-stu-id="b198f-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="b198f-127">Tai reiškia, kad galime paruošti „kanban“ su visomis reikiamomis medžiagomis.</span><span class="sxs-lookup"><span data-stu-id="b198f-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="b198f-128">Spustelėkite „Parengti“.</span><span class="sxs-lookup"><span data-stu-id="b198f-128">Click Prepare.</span></span>
    * <span data-ttu-id="b198f-129">Atkreipkite dėmesį – užduoties būsenos piktograma nurodo, kad užduotis jau parengta.</span><span class="sxs-lookup"><span data-stu-id="b198f-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]