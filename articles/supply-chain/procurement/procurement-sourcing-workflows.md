---
title: Įsigijimo ir šaltinio pasirinkimo darbo eigos
description: Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas. Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d25ca64fb6a3fa7d7898ec68568703f3de7b1595
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572724"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="f10d3-104">Paraiškų darbo eigos</span><span class="sxs-lookup"><span data-stu-id="f10d3-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f10d3-105">Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas.</span><span class="sxs-lookup"><span data-stu-id="f10d3-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="f10d3-106">Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="f10d3-107">Darbo eiga rodo verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-107">A workflow represents a business process.</span></span> <span data-ttu-id="f10d3-108">Ji nustato dokumento kelią sistemoje ir parodo, kas turi atlikti užduotį arba patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="f10d3-109">Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:</span><span class="sxs-lookup"><span data-stu-id="f10d3-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="f10d3-110">**Procesų nuoseklumas** — galite nustatyti konkrečių dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="f10d3-111">Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.</span><span class="sxs-lookup"><span data-stu-id="f10d3-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="f10d3-112">**Proceso matomumas** — galite sekti konkretaus darbo eigos egzemplioriaus efektyvumo metriką.</span><span class="sxs-lookup"><span data-stu-id="f10d3-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="f10d3-113">Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="f10d3-114">**Centralizuotas darbų sąrašas**– vartotojai norėdami sužinoti darbo eigos užduotis ir patvirtinimus, jiems priskirtus visose darbo eigose, kuriose jie dalyvauja, gali peržiūrėti centralizuotų darbų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="f10d3-115">Tai galima padaryti puslapyje Darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="f10d3-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="f10d3-116"> Darbo eigų tipai, kuriuos galite sukurti</span><span class="sxs-lookup"><span data-stu-id="f10d3-116">The types of workflows that you can create</span></span>
<span data-ttu-id="f10d3-117">Įsigijimo ir šaltinio pasirinkimo procese galima naudoti toliau išvardintų tipų darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="f10d3-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f10d3-118">**Tipas**</span><span class="sxs-lookup"><span data-stu-id="f10d3-118">**Type**</span></span>                         | <span data-ttu-id="f10d3-119">**Naudokite šį tipą norėdami**</span><span class="sxs-lookup"><span data-stu-id="f10d3-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="f10d3-120">Pirkimo paraiškos peržiūra</span><span class="sxs-lookup"><span data-stu-id="f10d3-120">Purchase requisition review</span></span>      | <span data-ttu-id="f10d3-121">Kurkite pirkimo paraiškų peržiūros ir patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="f10d3-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="f10d3-122">Pirkimo paraiškos eilutės peržiūra</span><span class="sxs-lookup"><span data-stu-id="f10d3-122">Purchase requisition line review</span></span> | <span data-ttu-id="f10d3-123">Kurkite pirkimo paraiškų eilučių peržiūros ir patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="f10d3-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="f10d3-124">Pirkimo užsakymo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="f10d3-124">Purchase order workflow</span></span>          | <span data-ttu-id="f10d3-125">Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="f10d3-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="f10d3-126">Pirkimo užsakymo eilutės darbo eiga</span><span class="sxs-lookup"><span data-stu-id="f10d3-126">Purchase order line workflow</span></span>     | <span data-ttu-id="f10d3-127">Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymų eilutėms.</span><span class="sxs-lookup"><span data-stu-id="f10d3-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="f10d3-128">Tiekėjo įtraukimo prašymo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="f10d3-128">Vendor add application workflow</span></span>  | <span data-ttu-id="f10d3-129">Kurkite naujų tiekėjų įtraukimo naudojant tiekėjo užklausas peržiūros ir patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="f10d3-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="f10d3-130">Darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="f10d3-130">Creating a workflow</span></span>

<span data-ttu-id="f10d3-131">Norėdami kurti darbo eigą, pasirinkite Įsigijimas ir šaltinio pasirinkimas &gt; Nustatymas &gt; Įsigijimo ir šaltinio pasirinkimo darbo eigos ir sukurkite naują darbo eigą, pasirinkdami norimą darbo eigos tipą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="f10d3-132">Darbo eigos srityje darbo eigos elementus galite nuvilkti į kūrimo priemonę ir susieti elementus su eiga.</span><span class="sxs-lookup"><span data-stu-id="f10d3-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="f10d3-133">Darbo eigos elementai turi būti sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="f10d3-133">The workflow elements should be configured.</span></span> <span data-ttu-id="f10d3-134">Konfigūruodami patvirtinimo ir užduoties darbo eigos elementus galite nustatyti, kuris dalyvis turėtų atlikti veiksmą.</span><span class="sxs-lookup"><span data-stu-id="f10d3-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="f10d3-135">Dalyvių tipai</span><span class="sxs-lookup"><span data-stu-id="f10d3-135">Types of participants</span></span>

<span data-ttu-id="f10d3-136">Galite priskirti patvirtinimo veiksmą toliau nurodytoms dalyvių grupėms.</span><span class="sxs-lookup"><span data-stu-id="f10d3-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="f10d3-137">Vartotojų grupė</span><span class="sxs-lookup"><span data-stu-id="f10d3-137">User group</span></span>    | <span data-ttu-id="f10d3-138">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f10d3-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f10d3-139">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="f10d3-139">Participant</span></span>   | <span data-ttu-id="f10d3-140">Priskirkite patvirtinimo veiksmą grupės arba vaidmens nariams.</span><span class="sxs-lookup"><span data-stu-id="f10d3-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="f10d3-141">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="f10d3-141">Hierarchy</span></span>     | <span data-ttu-id="f10d3-142">Priskirkite patvirtinimo veiksmą konkrečios organizacijos hierarchijos vartotojams.</span><span class="sxs-lookup"><span data-stu-id="f10d3-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="f10d3-143">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="f10d3-143">Workflow user</span></span> | <span data-ttu-id="f10d3-144">Priskirkite patvirtinimo veiksmą šios darbo eigos vartotojams.</span><span class="sxs-lookup"><span data-stu-id="f10d3-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="f10d3-145">Darbo grupė</span><span class="sxs-lookup"><span data-stu-id="f10d3-145">Queue</span></span>         | <span data-ttu-id="f10d3-146">Priskirti patvirtinimo veiksmą darbo elementų eilei.</span><span class="sxs-lookup"><span data-stu-id="f10d3-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="f10d3-147">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="f10d3-147">User</span></span>          | <span data-ttu-id="f10d3-148">Priskirkite patvirtinimo veiksmą konkretiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="f10d3-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="f10d3-149">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f10d3-149">Additional resources</span></span>

- [<span data-ttu-id="f10d3-150">Pirkimo paraiškų verslo procesų darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f10d3-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="f10d3-151">Pirkimo paraiškos darbo eiga</span><span class="sxs-lookup"><span data-stu-id="f10d3-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="f10d3-152">Tiekėjų supažindinimas</span><span class="sxs-lookup"><span data-stu-id="f10d3-152">Onboarding vendors</span></span>](vendor-onboarding.md)

