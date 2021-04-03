---
title: Grąžinti „kanban“ užduoties būseną
description: Ši procedūra padeda grąžinti neteisingą „kanban“ užduoties būseną.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94618494b9c338ed27b2558c91dc662c853d3cda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261099"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="379e8-103">Grąžinti „kanban“ užduoties būseną</span><span class="sxs-lookup"><span data-stu-id="379e8-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="379e8-104">Ši procedūra padeda grąžinti neteisingą „kanban“ užduoties būseną.</span><span class="sxs-lookup"><span data-stu-id="379e8-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="379e8-105">Tai naudinga, jei mašinų operatorius atnaujina neteisingą užduotį arba netyčia nustato neteisingą būseną.</span><span class="sxs-lookup"><span data-stu-id="379e8-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="379e8-106">Šios procedūros metu „kanban“ užduotis netyčia užregistruojama kaip paruošta ir jos būsena yra grąžinama.</span><span class="sxs-lookup"><span data-stu-id="379e8-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="379e8-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="379e8-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="379e8-108">Ši procedūra skirta parduotuvės prižiūrėtojui arba mašinų operatoriui, dirbančiam „lean manufacturing“ įmonėje.</span><span class="sxs-lookup"><span data-stu-id="379e8-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="379e8-109">Atidaryti darbo elemento proceso informacijos sritį</span><span class="sxs-lookup"><span data-stu-id="379e8-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="379e8-110">Eikite į proceso užduočių „kanban“ sritį.</span><span class="sxs-lookup"><span data-stu-id="379e8-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="379e8-111">Lauke Darbo elementas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="379e8-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="379e8-112">Pasirinkite 1260 darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="379e8-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="379e8-113">Paruošti „kanban“ užduotį</span><span class="sxs-lookup"><span data-stu-id="379e8-113">Prepare kanban job</span></span>
1. <span data-ttu-id="379e8-114">Spustelėkite „Parengti“.</span><span class="sxs-lookup"><span data-stu-id="379e8-114">Click Prepare.</span></span>
    * <span data-ttu-id="379e8-115">Jei negalite spustelėti Paruošti, nes ši parinktis papilkinta, įsitikinkite, kad pasirinktos „kanban“ užduoties būsena Suplanuota, kurią nurodo tuščia „kanban“ piktograma.</span><span class="sxs-lookup"><span data-stu-id="379e8-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="379e8-116">Jei parinkties Paruošti funkcija nepavyko, įsitikinkite, kad galima naudoti visas išrinkimo dokumento medžiagas.</span><span class="sxs-lookup"><span data-stu-id="379e8-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="379e8-117">Sąraše pasirinkite paruoštą užduotį.</span><span class="sxs-lookup"><span data-stu-id="379e8-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="379e8-118">Pasirinkite pirmą ką tik paruoštą užduotį.</span><span class="sxs-lookup"><span data-stu-id="379e8-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="379e8-119">Atkreipkite dėmesį, kad užduoties būsena yra Paruošta (tai nurodo trikampis „kanban“ piktogramos viduje).</span><span class="sxs-lookup"><span data-stu-id="379e8-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="379e8-120">Grąžinti paruoštos „kanban“ užduoties būseną</span><span class="sxs-lookup"><span data-stu-id="379e8-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="379e8-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="379e8-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="379e8-122">Pasirinkite pirmą paruoštą užduotį.</span><span class="sxs-lookup"><span data-stu-id="379e8-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="379e8-123">Veiksmų srityje spustelėkite Gamyba.</span><span class="sxs-lookup"><span data-stu-id="379e8-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="379e8-124">Spustelėkite Grąžinti būseną.</span><span class="sxs-lookup"><span data-stu-id="379e8-124">Click Revert status.</span></span>
    * <span data-ttu-id="379e8-125">Galite naudoti alternatyvią „kanban“ taisyklę, kai teisingi šie teiginiai: – abiejų taisyklių papildymo strategija yra ta pati;</span><span class="sxs-lookup"><span data-stu-id="379e8-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="379e8-126">- abiejų taisyklių gamybos eigos versija yra ta pati;</span><span class="sxs-lookup"><span data-stu-id="379e8-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="379e8-127">- abiejų taisyklių tiekiamas produktas yra tas pats;</span><span class="sxs-lookup"><span data-stu-id="379e8-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="379e8-128">- bet kokios abiejų taisyklių vėliausiai sukonfigūruotos „kanban“ taisyklių proceso pabaigos veiklos yra tos pačios;</span><span class="sxs-lookup"><span data-stu-id="379e8-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="379e8-129">- sukonfigūruotos tos pačios abiejų taisyklių pateiktos atsargų dimensijos;</span><span class="sxs-lookup"><span data-stu-id="379e8-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="379e8-130">- Sandėliavimo vieneto būsena yra Nepriskirta;</span><span class="sxs-lookup"><span data-stu-id="379e8-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="379e8-131">- įvykio „kanban“ konfigūracija yra pati.</span><span class="sxs-lookup"><span data-stu-id="379e8-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="379e8-132">Įsitikinkite, kad naujoji būsena yra Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="379e8-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="379e8-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="379e8-133">Click OK.</span></span>
5. <span data-ttu-id="379e8-134">Sąraše atžymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="379e8-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="379e8-135">Pasirinkite tą pačią užduotį.</span><span class="sxs-lookup"><span data-stu-id="379e8-135">Select the same job.</span></span>  
    * <span data-ttu-id="379e8-136">Atkreipkite dėmesį, kad „kanban“ užduoties būsena grąžinama į Suplanuota (tai nurodo tuščia „kanban“ piktograma).</span><span class="sxs-lookup"><span data-stu-id="379e8-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]