---
title: Darbo eigos veiksmai
description: "Šiame straipsnyje aprašyti veiksmai, kurių kiekvienas darbo eigos patvirtinimo proceso dalyvis gali imtis."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a4717accfa7e5879ee757820c39f000fa7d3e95
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-actions"></a><span data-ttu-id="a8bb1-103">Darbo eigos veiksmai</span><span class="sxs-lookup"><span data-stu-id="a8bb1-103">Workflow actions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a8bb1-104">Šiame straipsnyje aprašyti veiksmai, kurių kiekvienas darbo eigos patvirtinimo proceso dalyvis gali imtis.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="a8bb1-105">Darbo eiga gali apimti keletą žmonių grupių: iniciatorių, užduočių priėmėjus, sprendimus priimančius asmenis ir tvirtintojus.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="a8bb1-106">Pavyzdžiui, šioje išlaidų ataskaitos darbo eigoje Samas yra iniciatorius, eilės nariai yra užduočių priėmėjai, Johnas yra sprendimų priėmėjas, o Frankas, Sue ir Ann yra tvirtintojai.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>   

<span data-ttu-id="a8bb1-107">[![Darbo eiga\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="a8bb1-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span> 

<span data-ttu-id="a8bb1-108">Tolesniuose skyriuose paaiškinami darbo eigos veiksmai, kuriuos gali atlikti kiekviena grupė.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="a8bb1-109">Veiksmai, kuriuos gali atlikti iniciatorius</span><span class="sxs-lookup"><span data-stu-id="a8bb1-109">Actions that an originator can perform</span></span>
<span data-ttu-id="a8bb1-110">Iniciatorius paleidžia darbo eigos egzempliorių pateikdamas dokumentą apdoroti.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="a8bb1-111">Pvz., Samas turi spustelėti mygtuką **Pateikti**, esantį **Išlaidų ataskaitos** puslapyje, kad pateiktų savo išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="a8bb1-112">Veiksmai, kuriuos gali atlikti užduoties priėmėjas</span><span class="sxs-lookup"><span data-stu-id="a8bb1-112">Actions that a task assignee can perform</span></span>
<span data-ttu-id="a8bb1-113">Užduotis gali būti priskirta keliems žmonėms arba darbo elementų eilei, kurią stebi keli žmonės.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="a8bb1-114">Tačiau tik vienas asmuo gali atlikti užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-114">However, only one person can complete a task.</span></span> <span data-ttu-id="a8bb1-115">Pvz., Semas pateikė išlaidų ataskaitą ir savo produktų gavimo kvitus perdavė organizacijos Išlaidų ataskaitų skyriui, kad juos peržiūrėtų.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span> 

<span data-ttu-id="a8bb1-116">Eilę stebi „Adventure Works‟ Išlaidų ataskaitų skyriaus nariai.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="a8bb1-117">Julie, to skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="a8bb1-118">Dabar ji gali atlikti vieną iš šių veiksmų: užbaigti, atmesti, perduoti, prašyti pakeisti, priskirti iš naujo ar išleisti.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span> 

<span data-ttu-id="a8bb1-119">**Pastaba.** Galimi veiksmai skiriasi: tai priklauso nuo to, kaip programinės įrangos kūrėjas sukūrė užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-119">**Note:** The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="a8bb1-120">Baigti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-120">Complete</span></span>

<span data-ttu-id="a8bb1-121">Kai naudotojas pabaigia užduotį, apdoroti pateiktas dokumentas priskiriamas kitam darbo eigos naudotojui, jei kitas naudotojas yra.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="a8bb1-122">Jei papildomas apdorojimas nereikalingas, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-122">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="a8bb1-123">Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="a8bb1-124">Julie atlikus peržiūrą, dokumentas priskiriamas Johnui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="a8bb1-125">Atmesti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-125">Reject</span></span>

<span data-ttu-id="a8bb1-126">Kai naudotojas atmeta dokumentą, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-126">When a user rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="a8bb1-127">Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="a8bb1-128">Jei Julie atmeta išlaidų ataskaitą, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-128">If Julie rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="a8bb1-129">Samas tada gali išlaidų ataskaitą pateikti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="a8bb1-130">Pirmiausia jis gali ataskaitą keisti, arba gali iš naujo pateikti pradinę versiją.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="a8bb1-131">Jei Samas pakartotinai pateikia išlaidų ataskaitą, darbo eigos procesas prasideda rankinės peržiūros užduotimi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="a8bb1-132">Perduoti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-132">Delegate</span></span>

<span data-ttu-id="a8bb1-133">Kai vartotojas perduoda užduotį, užduotis priskiriama kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-133">When a user delegates a task, the task is assigned to another user.</span></span> 

<span data-ttu-id="a8bb1-134">Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="a8bb1-135">Julie šią užduotį perduoda Timui, kuris yra jos padėjėjas.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-135">Julie delegates this task to Tim, who is her assistant.</span></span> 

<span data-ttu-id="a8bb1-136">Timas tada veikia Julie vardu.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="a8bb1-137">Todėl, kai Timas atlieka peržiūrą, išlaidų ataskaita priskiriama Johnui, lygiai taip, jei užduotį būtų atlikusi Julie.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="a8bb1-138">Reikalauti keitimo</span><span class="sxs-lookup"><span data-stu-id="a8bb1-138">Request change</span></span>

<span data-ttu-id="a8bb1-139">Kai naudotojas reikalauja pateikto dokumento keitimo, dokumentas grąžinamas iniciatoriui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span> 

<span data-ttu-id="a8bb1-140">Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="a8bb1-141">Julie išlaidų ataskaitoje pastebi keletą klaidų ir reikalauja pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="a8bb1-142">Išlaidų ataskaita vėl siunčiama Samui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-142">The expense report is sent back to Sam.</span></span> 

<span data-ttu-id="a8bb1-143">Samas gali išlaidų ataskaitą pateikti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="a8bb1-144">Pirmiausia jis gali atlikti pageidautus keitimus, arba gali iš naujo pateikti pradinę versiją.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="a8bb1-145">Jei Samas pakartotinai pateikia išlaidų ataskaitą, darbo elementų eilės narys turi vėl peržiūrėti išlaidų ataskaitą ir produktų gavimo kvitus.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="a8bb1-146">Priskirti iš naujo</span><span class="sxs-lookup"><span data-stu-id="a8bb1-146">Reassign</span></span>

<span data-ttu-id="a8bb1-147">Darbo elementų eilės nariai gali toje eilėje esančius dokumentus iš naujo priskirti kitai eilei.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span> 

<span data-ttu-id="a8bb1-148">Pavyzdžiui, eilę stebi Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="a8bb1-149">Norėdama subalansuoti darbo krūvį, išlaidų ataskaitą ir prie jos pridėtus kvitus ji gali iš naujo priskirti kitai eilei.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="a8bb1-150">Paleisti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-150">Release</span></span>

<span data-ttu-id="a8bb1-151">Kartais darbo elementų eilės narys gali užduotį priimti, bet tada nuspręsti, kad jis ar ji užduoties atlikti negali.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="a8bb1-152">Šiuo atveju asmuo, kuris priėmė užduotį, dokumentą gali vėl išleisti į darbo elementų eilę.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span> 

<span data-ttu-id="a8bb1-153">Pavyzdžiui, Julie, „Adventure Works‟ Išlaidų ataskaitų skyriaus narė, priėmė Samo išlaidų ataskaitos ir produktų gavimo kvitų peržiūros užduotį.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="a8bb1-154">Jei Julie nusprendžia, kad užduoties atlikti negali, ji gali dokumentą išleisti.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="a8bb1-155">Išlaidų ataskaita grąžinama į eilę, kad užduotį galėtų atlikti kiti „Adventure Works‟ Išlaidų ataskaitų skyriaus nariai.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="a8bb1-156">Veiksmai, kuriuos gali atlikti sprendimų priėmėjas</span><span class="sxs-lookup"><span data-stu-id="a8bb1-156">Actions that a decision maker can perform</span></span>
<span data-ttu-id="a8bb1-157">Paprastai dokumentas priskiriamas sprendimų priėmėjui todėl, kad yra klausimas, į kurį turi atsakyti sprendimų priėmėjas.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="a8bb1-158">Atsakymas į klausimą paprastai yra **Taip** arba **Ne**, arba **Teisinga** arba **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="a8bb1-159">Jei sprendimų priėmėjas vieno iš tų pasirinkimų nepasirenka, jis arba ji sprendimą gali perduoti.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="a8bb1-160">\[1 pasirinkimas\] arba \[2 pasirinkimas\]</span><span class="sxs-lookup"><span data-stu-id="a8bb1-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="a8bb1-161">Sprendimų priėmėjas turi atsakyti į klausimą, susijusį su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="a8bb1-162">Atsakymas į klausimą paprastai yra **Taip** arba **Ne**, arba **Teisinga** arba **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="a8bb1-163">Atsakymu, kurį pasirenka sprendimų priėmėjas, nustatoma darbo eigos šaka, naudojama apdoroti dokumentui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span> 

<span data-ttu-id="a8bb1-164">Pvz., Samo išlaidų ataskaita priskiriama Johnui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="a8bb1-165">Johnas turi nuspręsti, ar dėl dokumento informacijos reikia skambinti Samo vadovui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="a8bb1-166">Jei Johnas nusprendžia, kad skambinti reikia, išlaidų ataskaita priskiriama Arethai, kuri tada turi paskambinti Samo vadovui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="a8bb1-167">Jei Johnas nusprendžia, kad skambinti nereikia, išlaidų ataskaita priskiriama Frankui, kad ją patvirtintų.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="a8bb1-168">Perduoti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-168">Delegate</span></span>

<span data-ttu-id="a8bb1-169">Kai sprendimų priėmėjas sprendimą perduoda, dokumentas priskiriamas kitam naudotojui, kuris turi priimti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span> 

<span data-ttu-id="a8bb1-170">Pvz., Samo išlaidų ataskaita priskiriama Johnui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="a8bb1-171">Johnas sprendimą perduoda Mariai, kuri yra jo padėjėja.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-171">John delegates the decision to Maria, who is his assistant.</span></span> 

<span data-ttu-id="a8bb1-172">Maria tada veikia Johno vardu.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="a8bb1-173">Jei Maria nusprendžia, kad reikia skambinti Samo vadovui, išlaidų ataskaita priskiriama Arethai, kuri tada turi paskambinti Samo vadovui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="a8bb1-174">Jei Maria nusprendžia, kad skambinti nereikia, išlaidų ataskaita priskiriama Frankui, kad ją patvirtintų.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="a8bb1-175">Veiksmai, kuriuos gali atlikti tvirtintojas</span><span class="sxs-lookup"><span data-stu-id="a8bb1-175">Actions that an approver can perform</span></span>
<span data-ttu-id="a8bb1-176">Kai dokumentas priskirtas tvirtintojui, tvirtintojas gali atlikti vieną iš šių veiksmų: patvirtinti, atmesti, perduoti arba prašyti pakeisti.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="a8bb1-177">Patvirtinti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-177">Approve</span></span>

<span data-ttu-id="a8bb1-178">Kai tvirtintojas patvirtina dokumentą, dokumentas priskiriamas kitam darbo eigos naudotojui, jei kitas naudotojas yra.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="a8bb1-179">Jei papildomas apdorojimas nereikalingas, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-179">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="a8bb1-180">Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 6 000 USD ir šis dokumentas priskiriamas Frankui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="a8bb1-181">Kai Frankas patvirtina dokumentą, jis priskiriamas tvirtinti Sue.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="a8bb1-182">Kai Sue patvirtina išlaidų ataskaitą, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="a8bb1-183">Atmesti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-183">Reject</span></span>

<span data-ttu-id="a8bb1-184">Kai tvirtintojas atmeta dokumentą, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-184">When an approver rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="a8bb1-185">Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 12 000 USD ir šis dokumentas priskiriamas Sue.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="a8bb1-186">Jei Sue atmeta išlaidų ataskaitą, darbo eigos procesas baigiasi.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-186">If Sue rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="a8bb1-187">Samas gali išlaidų ataskaitą pateikti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="a8bb1-188">Pirmiausia jis gali atlikti keitimus, arba gali iš naujo pateikti pradinę išlaidų ataskaitos versiją.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="a8bb1-189">Jei Samas pakartotinai pateikia išlaidų ataskaitą, darbo eigos procesas prasideda tvirtinimo procesu.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="a8bb1-190">Perduoti</span><span class="sxs-lookup"><span data-stu-id="a8bb1-190">Delegate</span></span>

<span data-ttu-id="a8bb1-191">Kai tvirtintojas perduoda dokumentą, dokumentas priskiriamas tvirtinti kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span> 

<span data-ttu-id="a8bb1-192">Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 12 000 USD ir šis dokumentas priskiriamas Frankui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="a8bb1-193">Frenkas perduoda išlaidų ataskaitą Anai.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-193">Frank delegates the expense report to Ann.</span></span> 

<span data-ttu-id="a8bb1-194">Tada Ann veikia Franko vardu.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="a8bb1-195">Todėl kai Ann patvirtina dokumentą, jis priskiriamas tvirtinti Sue, lygia taip, jei jį būtų patvirtinęs Frankas.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="a8bb1-196">Kai Sue patvirtina dokumentą, jis siunčiamas tvirtinti Ann.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="a8bb1-197">Reikalauti keitimo</span><span class="sxs-lookup"><span data-stu-id="a8bb1-197">Request change</span></span>

<span data-ttu-id="a8bb1-198">Kai tvirtintojas reikalauja dokumento keitimo, dokumentas grąžinamas iniciatoriui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span> 

<span data-ttu-id="a8bb1-199">Pavyzdžiui, Samas pateikė išlaidų ataskaitą už 12 000 USD ir šis dokumentas priskiriamas Sue.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="a8bb1-200">Jei Sue reikalauja pakeitimo, išlaidų ataskaita grąžinama Samui.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-200">If Sue requests a change, the expense report is sent back to Sam.</span></span> 

<span data-ttu-id="a8bb1-201">Samas gali išlaidų ataskaitą pateikti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="a8bb1-202">Pirmiausia jis gali atlikti pageidautus keitimus, arba gali iš naujo pateikti pradinę išlaidų ataskaitos versiją.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="a8bb1-203">Jeigu Samas pakartotinai pateikia išlaidų ataskaitą, ji siunčiama tvirtinti Frankui, nes Frankas yra pirmasis tvirtintojas patvirtinimo procese.</span><span class="sxs-lookup"><span data-stu-id="a8bb1-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>




