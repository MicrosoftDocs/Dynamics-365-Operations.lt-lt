---
title: Darbo eigos sistema
description: Šioje temoje aprašyta „Microsoft Dynamics 365 for Finance and Operations“ darbo eigų sistema.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545814"
---
# <a name="workflow-system"></a><span data-ttu-id="29840-103">Darbo eigos sistema</span><span class="sxs-lookup"><span data-stu-id="29840-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29840-104">Šioje temoje aprašyta „Microsoft Dynamics 365 for Finance and Operations“ darbo eigų sistema.</span><span class="sxs-lookup"><span data-stu-id="29840-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="29840-105">Kas yra darbo eiga?</span><span class="sxs-lookup"><span data-stu-id="29840-105">What is workflow?</span></span>

<span data-ttu-id="29840-106">Terminą *darbo eiga* galima apibrėžti dviem būdais: kaip sistemą ir kaip veiklos procesą.</span><span class="sxs-lookup"><span data-stu-id="29840-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="29840-107">Darbo eiga yra sistema</span><span class="sxs-lookup"><span data-stu-id="29840-107">Workflow is a system</span></span>

<span data-ttu-id="29840-108">Darbo eiga yra sistema, diegiama kartu su „Finance and Operations“ ir veikianti programos objektų serveryje (AOS).</span><span class="sxs-lookup"><span data-stu-id="29840-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="29840-109">Darbo eigos sistema turi funkcijų, kurias galite naudoti atskiroms darbo eigoms arba verslo procesams kurti.</span><span class="sxs-lookup"><span data-stu-id="29840-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="29840-110">Darbo eiga yra verslo procesas</span><span class="sxs-lookup"><span data-stu-id="29840-110">Workflow is a business process</span></span>

<span data-ttu-id="29840-111">Darbo eiga rodo verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="29840-111">A workflow represents a business process.</span></span> <span data-ttu-id="29840-112">Ji apibrėžia, kaip dokumentas juda sistemoje, parodydama, kas turi įvykdyti užduotį, priimti sprendimą ar patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="29840-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="29840-113">Pavyzdžiui, toliau pateikiamoje iliustracijoje rodoma išlaidų ataskaitų darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="29840-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Darbo eiga, kurios elementai priskirti vartotojams](./media/workflow_user.gif)

<span data-ttu-id="29840-115">Norėdami geriau suprasti šią darbo eigą, įsivaizduokite, kad Semas pateikia 7 000 USD išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="29840-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="29840-116">Tokiu atveju Ivanas turi peržiūrėti Semo jam pateiktus kvitus.</span><span class="sxs-lookup"><span data-stu-id="29840-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="29840-117">Tada Frank ir Sue turi patvirtinti išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="29840-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="29840-118">O dabar tarkime, kad Semas pateikia 11 000 USD išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="29840-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="29840-119">Tokiu atveju Ivanas turi peržiūrėti kvitus, o Frenkas, Sju ir Ana turi patvirtinti išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="29840-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="29840-120"> Darbo eigos sistemos naudojimo privalumai</span><span class="sxs-lookup"><span data-stu-id="29840-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="29840-121">Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:</span><span class="sxs-lookup"><span data-stu-id="29840-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="29840-122">**Procesų nuoseklumas** – galite nustatyti, kaip apdorojami konkretūs dokumentai, pvz., pirkimo paraiškos ir išlaidų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="29840-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="29840-123">Naudodamiesi darbo eigos sistema užtikrinate, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.</span><span class="sxs-lookup"><span data-stu-id="29840-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="29840-124">**Proceso matomumas** – galite sekti darbo eigos egzempliorių efektyvumo metriką.</span><span class="sxs-lookup"><span data-stu-id="29840-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="29840-125">Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="29840-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="29840-126">**Centralizuotas darbų sąrašas** – vartotojai gali peržiūrėti centralizuotų darbų sąrašą, kuriame rodomos jiems priskirtos darbo eigos užduotys ir patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="29840-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="29840-127">Darbo eigos turinys</span><span class="sxs-lookup"><span data-stu-id="29840-127">Workflow content</span></span>

+ [<span data-ttu-id="29840-128">Darbo eigos architektūra</span><span class="sxs-lookup"><span data-stu-id="29840-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="29840-129">Darbo eigos elementai</span><span class="sxs-lookup"><span data-stu-id="29840-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="29840-130">Darbo eigos veiksmai</span><span class="sxs-lookup"><span data-stu-id="29840-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="29840-131">Darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="29840-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="29840-132">Darbo eigos ypatybių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="29840-133">Neautomatizuotos darbo eigos užduoties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="29840-134">Automatizuotos darbo eigos užduoties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="29840-135">Darbo eigos patvirtinimo proceso konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="29840-136">Darbo eigos patvirtinimo veiksmo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="29840-137">Neautomatizuoto darbo eigos sprendimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="29840-138">Sąlyginio darbo eigos sprendimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="29840-139">Lygiagrečios darbo eigos veiklos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="29840-140">Lygiagrečios darbo eigos šakos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="29840-141">Eilutės elemento darbo eigos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29840-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="29840-142">DUK apie darbo eigas</span><span class="sxs-lookup"><span data-stu-id="29840-142">Workflow FAQ</span></span>](workflow-FAQ.md)
