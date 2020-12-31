---
title: Darbo eigos elementai
description: Šioje temoje aprašomi įvairūs elementai, sudarantys darbo eigą.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b681d4da750df502987bd00ab52c1cb6eecdf30e
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694244"
---
# <a name="workflow-elements"></a><span data-ttu-id="c706b-103">Darbo eigos elementai</span><span class="sxs-lookup"><span data-stu-id="c706b-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c706b-104">Šioje temoje aprašomi įvairūs elementai, sudarantys darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="c706b-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="c706b-105">Darbo eigą sudaro elementai.</span><span class="sxs-lookup"><span data-stu-id="c706b-105">A workflow consists of elements.</span></span> <span data-ttu-id="c706b-106">Tolesniuose skyriuose aprašomi visi elementų tipai.</span><span class="sxs-lookup"><span data-stu-id="c706b-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="c706b-107">Užduotys</span><span class="sxs-lookup"><span data-stu-id="c706b-107">Tasks</span></span>

<span data-ttu-id="c706b-108">*Užduotis* yra darbo vienetas, kurį reikia atlikti.</span><span class="sxs-lookup"><span data-stu-id="c706b-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="c706b-109">Į darbo eigą galima įtraukti dviejų tipų užduotis: rankines užduotis ir automatizuotas užduotis.</span><span class="sxs-lookup"><span data-stu-id="c706b-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="c706b-110">Rankiniu būdu nustatyta užduotis</span><span class="sxs-lookup"><span data-stu-id="c706b-110">Manual task</span></span>

<span data-ttu-id="c706b-111">*Rankinė užduotis* yra darbo vienetas, kurį turi atlikti vartotojas.</span><span class="sxs-lookup"><span data-stu-id="c706b-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="c706b-112">Pavyzdžiui, išlaidų ataskaitų darbo eigoje gali būti rankinių užduočių, kurioms reikia priskirtų vartotojų, kad atliktų šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c706b-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="c706b-113">Peržiūrėti kvitus, pateiktus kartu su išlaidų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="c706b-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="c706b-114">Skambinti darbuotojo vadybininkui.</span><span class="sxs-lookup"><span data-stu-id="c706b-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="c706b-115">Automatizuota užduotis</span><span class="sxs-lookup"><span data-stu-id="c706b-115">Automated task</span></span>

<span data-ttu-id="c706b-116">*Automatizuota užduotis* yra darbo vienetas, kurį turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="c706b-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="c706b-117">Žmogui nereikia atlikti jokių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="c706b-117">No human interaction is required.</span></span> <span data-ttu-id="c706b-118">Pavyzdžiui, pardavimo užsakymo darbo eigoje gali būti automatizuotų užduočių, kurioms reikia, kad sistema atliktų šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c706b-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="c706b-119">Atlikite kredito tikrinimą.</span><span class="sxs-lookup"><span data-stu-id="c706b-119">Perform a credit check.</span></span>
- <span data-ttu-id="c706b-120">Klientui sukurti kliento įrašą, jei jo dar nėra.</span><span class="sxs-lookup"><span data-stu-id="c706b-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="c706b-121">Patvirtinimo procesai</span><span class="sxs-lookup"><span data-stu-id="c706b-121">Approval processes</span></span>

<span data-ttu-id="c706b-122">*Patvirtinimo procesas* yra procesas, susidedantis iš kelių žingsnių.</span><span class="sxs-lookup"><span data-stu-id="c706b-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="c706b-123">Atlikdamas kiekvieną patvirtinimo veiksmą, vartotojas gali atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c706b-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="c706b-124">Patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c706b-124">Approve the document.</span></span>
- <span data-ttu-id="c706b-125">Atmesti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c706b-125">Reject the document.</span></span>
- <span data-ttu-id="c706b-126">Prašyti pakeisti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c706b-126">Request a change to the document.</span></span>
- <span data-ttu-id="c706b-127">Priskirti dokumentą kitam vartotojui tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="c706b-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="c706b-128">Eilutės elemento darbo eigos elementai</span><span class="sxs-lookup"><span data-stu-id="c706b-128">Line-item workflow elements</span></span>

<span data-ttu-id="c706b-129">Galima sukurti darbo eigą tvarkyti dokumentus arba dokumento eilutės elementus.</span><span class="sxs-lookup"><span data-stu-id="c706b-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="c706b-130">Pavyzdžiui, sukūrėte tabelių patvirtinimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="c706b-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="c706b-131">(Ši darbo eiga bus vadinama dokumento *darbo eiga*.) Į to dokumento darbo eigą galite įtraukti elementą *eilutės elemento darbo eiga*.</span><span class="sxs-lookup"><span data-stu-id="c706b-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="c706b-132">Paleidus eilutės elementą, kiekvienas dokumento eilutės elementas pateikiamas apdoroti.</span><span class="sxs-lookup"><span data-stu-id="c706b-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="c706b-133">Norėdami galite apdoroti visus eilutės elementus vykdydami tos pačios eilutės elemento darbo eigą arba galite kiekvieną eilutės elementą apdoroti atliekant skirtingas eilutės elemento darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="c706b-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="c706b-134">Įsivaizduokite, kad darbuotojas pateikė tabelį, panašų į tabelį toliau pateikiamame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="c706b-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Darbo eiga su eilutės elementais](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="c706b-136">Tokiu atveju galbūt norėsite sukurti tokias eilutės elemento darbo eigas:</span><span class="sxs-lookup"><span data-stu-id="c706b-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="c706b-137">**1 eilutės elemento darbo eiga** – ši darbo eiga naudojama apdoroti eilutės elementus, kai projekto ID yra 1111.</span><span class="sxs-lookup"><span data-stu-id="c706b-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="c706b-138">**2 eilutės elemento darbo eiga** – ši darbo eiga naudojama apdoroti eilutės elementus, kai projekto ID yra 2222.</span><span class="sxs-lookup"><span data-stu-id="c706b-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="c706b-139">**3 eilutės elemento darbo eiga** – ši darbo eiga naudojama apdoroti eilutės elementus, kai projekto ID yra 3333.</span><span class="sxs-lookup"><span data-stu-id="c706b-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="c706b-140">Srauto valdiklių elementai</span><span class="sxs-lookup"><span data-stu-id="c706b-140">Flow-control elements</span></span>

<span data-ttu-id="c706b-141">Šie elementai suteikia galimybę kurti darbo eigas, kurios turi alternatyvias šakas arba šakas, vykdomas tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="c706b-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="c706b-142">Neautomatinis sprendimas</span><span class="sxs-lookup"><span data-stu-id="c706b-142">Manual decision</span></span>

<span data-ttu-id="c706b-143">*Rankinis sprendimas* – tai taškas, kuriame darbo eiga padalijama į dvi šakas.</span><span class="sxs-lookup"><span data-stu-id="c706b-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="c706b-144">Vartotojas turi nuspręsti, o šis sprendimas nurodo, kuri šaka naudojama apdoroti pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c706b-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="c706b-145">Sąlyginis sprendimas</span><span class="sxs-lookup"><span data-stu-id="c706b-145">Conditional decision</span></span>

<span data-ttu-id="c706b-146">*Sąlyginis sprendimas* – taip pat yra taškas, kuriame darbo eiga padalijama į dvi šakas.</span><span class="sxs-lookup"><span data-stu-id="c706b-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="c706b-147">Tačiau sistema nusprendžia, kurią šaką naudoti apdorojant pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="c706b-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="c706b-148">Siekiant nuspręsti sistema įvertina dokumentą, kad nustatytų, ar jis atitinka nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c706b-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="c706b-149">Lygiagreti veikla</span><span class="sxs-lookup"><span data-stu-id="c706b-149">Parallel activity</span></span>

<span data-ttu-id="c706b-150">*Lygiagreti veikla* – tai darbo eigos elementas, apimantis dvi ar daugiau vienu metu veikiančių darbo eigos šakų</span><span class="sxs-lookup"><span data-stu-id="c706b-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="c706b-151">Antrinė darbo eiga</span><span class="sxs-lookup"><span data-stu-id="c706b-151">Subworkflow</span></span>

<span data-ttu-id="c706b-152">*Antrinė darbo eiga* yra darbo eiga, kuri vyksta kitos darbo eigos kontekste.</span><span class="sxs-lookup"><span data-stu-id="c706b-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
