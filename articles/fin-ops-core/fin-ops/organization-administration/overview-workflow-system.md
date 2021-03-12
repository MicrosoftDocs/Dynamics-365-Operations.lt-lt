---
title: Darbo eigos sistemos apžvalga
description: Šioje temoje aprašyta darbo eigų sistema.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660e01618eea66bc611dd51818694d36993ba9ea
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797001"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="50236-103">Darbo eigos sistemos apžvalga</span><span class="sxs-lookup"><span data-stu-id="50236-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50236-104">Šioje temoje aprašyta darbo eigų sistema.</span><span class="sxs-lookup"><span data-stu-id="50236-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="50236-105">Kas yra darbo eiga?</span><span class="sxs-lookup"><span data-stu-id="50236-105">What is workflow?</span></span>

<span data-ttu-id="50236-106">Terminą *darbo eiga* galima apibrėžti dviem būdais: kaip sistemą ir kaip veiklos procesą.</span><span class="sxs-lookup"><span data-stu-id="50236-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="50236-107">Darbo eiga yra sistema</span><span class="sxs-lookup"><span data-stu-id="50236-107">Workflow is a system</span></span>

<span data-ttu-id="50236-108">Darbo eiga yra sistema, veikianti programos objektų serveryje (AOS).</span><span class="sxs-lookup"><span data-stu-id="50236-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="50236-109">Darbo eigos sistema turi funkcijų, kurias galite naudoti atskiroms darbo eigoms arba verslo procesams kurti.</span><span class="sxs-lookup"><span data-stu-id="50236-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="50236-110">Darbo eiga yra verslo procesas</span><span class="sxs-lookup"><span data-stu-id="50236-110">Workflow is a business process</span></span>

<span data-ttu-id="50236-111">Darbo eiga rodo verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="50236-111">A workflow represents a business process.</span></span> <span data-ttu-id="50236-112">Ji apibrėžia, kaip dokumentas juda sistemoje, parodydama, kas turi įvykdyti užduotį, priimti sprendimą ar patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="50236-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="50236-113">Pavyzdžiui, toliau pateikiamoje iliustracijoje rodoma išlaidų ataskaitų darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="50236-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Darbo eiga, kurios elementai priskirti vartotojams](./media/workflow_user.gif)

<span data-ttu-id="50236-115">Norėdami geriau suprasti šią darbo eigą, įsivaizduokite, kad Semas pateikia 7 000 USD išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="50236-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="50236-116">Tokiu atveju Ivanas turi peržiūrėti Semo jam pateiktus kvitus.</span><span class="sxs-lookup"><span data-stu-id="50236-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="50236-117">Tada Frank ir Sue turi patvirtinti išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="50236-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="50236-118">O dabar tarkime, kad Semas pateikia 11 000 USD išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="50236-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="50236-119">Tokiu atveju Ivanas turi peržiūrėti kvitus, o Frenkas, Sju ir Ana turi patvirtinti išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="50236-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="50236-120">Darbo eigos sistemos naudojimo privalumai</span><span class="sxs-lookup"><span data-stu-id="50236-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="50236-121">Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:</span><span class="sxs-lookup"><span data-stu-id="50236-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="50236-122">**Procesų nuoseklumas** – galite nustatyti, kaip apdorojami konkretūs dokumentai, pvz., pirkimo paraiškos ir išlaidų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="50236-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="50236-123">Naudodamiesi darbo eigos sistema užtikrinate, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.</span><span class="sxs-lookup"><span data-stu-id="50236-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="50236-124">**Proceso matomumas** – galite sekti darbo eigos egzempliorių efektyvumo metriką.</span><span class="sxs-lookup"><span data-stu-id="50236-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="50236-125">Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="50236-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="50236-126">**Centralizuotas darbų sąrašas** – vartotojai gali peržiūrėti centralizuotų darbų sąrašą, kuriame rodomos jiems priskirtos darbo eigos užduotys ir patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="50236-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="50236-127">Darbo eigos turinys</span><span class="sxs-lookup"><span data-stu-id="50236-127">Workflow content</span></span>

+ [<span data-ttu-id="50236-128">Darbo eigos sistemos architektūra</span><span class="sxs-lookup"><span data-stu-id="50236-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="50236-129">Darbo eigos elementai</span><span class="sxs-lookup"><span data-stu-id="50236-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="50236-130">Darbo eigos patvirtinimo procesų veiksmai</span><span class="sxs-lookup"><span data-stu-id="50236-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="50236-131">Darbo eigų kūrimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="50236-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="50236-132">Darbo eigos ypatybių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="50236-133">Neautomatizuotų darbo eigos užduočių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="50236-134">Automatizuotų darbo eigos užduočių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="50236-135">Darbo eigos patvirtinimo procesų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="50236-136">Darbo eigos patvirtinimo veiksmų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="50236-137">Neautomatinių darbo eigos sprendimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="50236-138">Sąlyginių darbo eigos sprendimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="50236-139">Lygiagrečių darbo eigos veiklų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="50236-140">Lygiagrečių darbo eigos šakų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="50236-141">Eilutės elemento darbo eigų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="50236-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="50236-142">DUK apie darbo eigas</span><span class="sxs-lookup"><span data-stu-id="50236-142">Workflow FAQ</span></span>](workflow-FAQ.md)
