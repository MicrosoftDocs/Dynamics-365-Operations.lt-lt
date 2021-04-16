---
title: Įsigijimo ir šaltinio pasirinkimo darbo eigos
description: Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas. Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd9ee69e180f2ff605c4f373a95d2346ccc73c0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807949"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="9c8b3-104">Paraiškų darbo eigos</span><span class="sxs-lookup"><span data-stu-id="9c8b3-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c8b3-105">Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="9c8b3-106">Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="9c8b3-107">Darbo eiga rodo verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-107">A workflow represents a business process.</span></span> <span data-ttu-id="9c8b3-108">Ji nustato dokumento kelią sistemoje ir parodo, kas turi atlikti užduotį arba patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="9c8b3-109">Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:</span><span class="sxs-lookup"><span data-stu-id="9c8b3-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="9c8b3-110">**Procesų nuoseklumas** — galite nustatyti konkrečių dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="9c8b3-111">Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="9c8b3-112">**Proceso matomumas** — galite sekti konkretaus darbo eigos egzemplioriaus efektyvumo metriką.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="9c8b3-113">Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="9c8b3-114">**Centralizuotas darbų sąrašas**– vartotojai norėdami sužinoti darbo eigos užduotis ir patvirtinimus, jiems priskirtus visose darbo eigose, kuriose jie dalyvauja, gali peržiūrėti centralizuotų darbų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="9c8b3-115">Tai galima padaryti puslapyje Darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="9c8b3-116">Darbo eigų tipai, kuriuos galite sukurti</span><span class="sxs-lookup"><span data-stu-id="9c8b3-116">The types of workflows that you can create</span></span>

<span data-ttu-id="9c8b3-117">Įsigijimo ir šaltinio pasirinkimo procese galima naudoti toliau išvardintų tipų darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="9c8b3-118">Tipas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-118">Type</span></span> | <span data-ttu-id="9c8b3-119">Naudokite šį tipą norėdami</span><span class="sxs-lookup"><span data-stu-id="9c8b3-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="9c8b3-120">Pirkimo paraiškos peržiūra</span><span class="sxs-lookup"><span data-stu-id="9c8b3-120">Purchase requisition review</span></span> | <span data-ttu-id="9c8b3-121">Kurkite pirkimo paraiškų peržiūros ir patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="9c8b3-122">Pirkimo paraiškos eilutės peržiūra</span><span class="sxs-lookup"><span data-stu-id="9c8b3-122">Purchase requisition line review</span></span> | <span data-ttu-id="9c8b3-123">Kurkite pirkimo paraiškų eilučių peržiūros ir patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="9c8b3-124">Pirkimo užsakymo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-124">Purchase order workflow</span></span> | <span data-ttu-id="9c8b3-125">Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="9c8b3-126">Pirkimo užsakymo eilutės darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-126">Purchase order line workflow</span></span> | <span data-ttu-id="9c8b3-127">Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymų eilutėms.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="9c8b3-128">Tiekėjo įtraukimo prašymo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-128">Vendor add application workflow</span></span> | <span data-ttu-id="9c8b3-129">Kurkite naujų tiekėjų įtraukimo naudojant tiekėjo užklausas peržiūros ir patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="9c8b3-130">Jums įtraukiant naują darbo eiga, galite taip pat matyti tolesnes nebeveikiančias darbo eigas sąraše **Sukurti darbo eigą** teksto laukelyje.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="9c8b3-131">Jos yra susijusios su *gavimo patvirtinimo* funkcija, kuri buvo prieinama [„Dynamics AX“ 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), bet dabar nebegalioja.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="9c8b3-132">Šios darbo eigos dabar jau nebepalaikomos.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="9c8b3-133">Pristatymo termino pranešimo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="9c8b3-134">Pranešimo apie SF gavimą darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="9c8b3-135">Gavimo dokumentas neatitiko pranešimo darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="9c8b3-136">Pranešimo apie nepatvirtinto gavimo dokumento atmetimą darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="9c8b3-137">Darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-137">Creating a workflow</span></span>

<span data-ttu-id="9c8b3-138">Norėdami kurti darbo eigą, pasirinkite Įsigijimas ir šaltinio pasirinkimas &gt; Nustatymas &gt; Įsigijimo ir šaltinio pasirinkimo darbo eigos ir sukurkite naują darbo eigą, pasirinkdami norimą darbo eigos tipą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="9c8b3-139">Darbo eigos srityje darbo eigos elementus galite nuvilkti į kūrimo priemonę ir susieti elementus su eiga.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="9c8b3-140">Darbo eigos elementai turi būti sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-140">The workflow elements should be configured.</span></span> <span data-ttu-id="9c8b3-141">Konfigūruodami patvirtinimo ir užduoties darbo eigos elementus galite nustatyti, kuris dalyvis turėtų atlikti veiksmą.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="9c8b3-142">Dalyvių tipai</span><span class="sxs-lookup"><span data-stu-id="9c8b3-142">Types of participants</span></span>

<span data-ttu-id="9c8b3-143">Galite priskirti patvirtinimo veiksmą toliau nurodytoms dalyvių grupėms.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="9c8b3-144">Vartotojų grupė</span><span class="sxs-lookup"><span data-stu-id="9c8b3-144">User group</span></span> | <span data-ttu-id="9c8b3-145">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-145">Description</span></span> |
|---|---|
| <span data-ttu-id="9c8b3-146">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="9c8b3-146">Participant</span></span> | <span data-ttu-id="9c8b3-147">Priskirkite patvirtinimo veiksmą grupės arba vaidmens nariams.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="9c8b3-148">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="9c8b3-148">Hierarchy</span></span> | <span data-ttu-id="9c8b3-149">Priskirkite patvirtinimo veiksmą konkrečios organizacijos hierarchijos vartotojams.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="9c8b3-150">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-150">Workflow user</span></span> | <span data-ttu-id="9c8b3-151">Priskirkite patvirtinimo veiksmą šios darbo eigos vartotojams.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="9c8b3-152">Darbo grupė</span><span class="sxs-lookup"><span data-stu-id="9c8b3-152">Queue</span></span> | <span data-ttu-id="9c8b3-153">Priskirti patvirtinimo veiksmą darbo elementų eilei.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="9c8b3-154">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-154">User</span></span> | <span data-ttu-id="9c8b3-155">Priskirkite patvirtinimo veiksmą konkretiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9c8b3-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9c8b3-156">Additional resources</span></span>

- [<span data-ttu-id="9c8b3-157">Pirkimo paraiškų verslo procesų darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="9c8b3-158">Pirkimo paraiškos darbo eiga</span><span class="sxs-lookup"><span data-stu-id="9c8b3-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="9c8b3-159">Tiekėjų supažindinimas</span><span class="sxs-lookup"><span data-stu-id="9c8b3-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]