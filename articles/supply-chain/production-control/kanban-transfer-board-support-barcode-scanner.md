---
title: "„Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas"
description: "„Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8393efd51032271d3023f1e0569425a16222cc3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="6ff94-103">„Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas</span><span class="sxs-lookup"><span data-stu-id="6ff94-103">Kanban transfer board support for barcode scanners</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ff94-104">„Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti.</span><span class="sxs-lookup"><span data-stu-id="6ff94-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="6ff94-105">Registravimo režimai</span><span class="sxs-lookup"><span data-stu-id="6ff94-105">Registration modes</span></span>
------------------

<span data-ttu-id="6ff94-106">„FastTab“ skirtuke **Skaitytuvo registravimas** galite pasirinkti registravimo režimą, kuris valdo veiksmą, kai nuskaitote „kanban“ kortelės numerį arba patys įvedate numerį „kanban“ kortelės numerio lauke.</span><span class="sxs-lookup"><span data-stu-id="6ff94-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>
| <span data-ttu-id="6ff94-107">Nustatyti registravimo režimą</span><span class="sxs-lookup"><span data-stu-id="6ff94-107">Set registration mode</span></span> | <span data-ttu-id="6ff94-108">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6ff94-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff94-109">Paleisti</span><span class="sxs-lookup"><span data-stu-id="6ff94-109">Start</span></span>                 | <span data-ttu-id="6ff94-110">Registruoja „kanban“ perkėlimo užduotį kaip nebaigtą.</span><span class="sxs-lookup"><span data-stu-id="6ff94-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="6ff94-111">Baigti</span><span class="sxs-lookup"><span data-stu-id="6ff94-111">Complete</span></span>              | <span data-ttu-id="6ff94-112">Registruoja „kanban“ perkėlimo užduotį kaip baigtą.</span><span class="sxs-lookup"><span data-stu-id="6ff94-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="6ff94-113">Tuščias</span><span class="sxs-lookup"><span data-stu-id="6ff94-113">Empty</span></span>                 | <span data-ttu-id="6ff94-114">Registruoja medžiagų sandėliavimo vienetą, „kanban“ kortelėje nurodytą kaip tuščią.</span><span class="sxs-lookup"><span data-stu-id="6ff94-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="6ff94-115">Pasirinkti</span><span class="sxs-lookup"><span data-stu-id="6ff94-115">Select</span></span>                | <span data-ttu-id="6ff94-116">Registruoja „kanban“ kortelės numerį ir automatiškai pasirenka nurodytą užduotį „kanban“ sąraše.</span><span class="sxs-lookup"><span data-stu-id="6ff94-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="6ff94-117">Registravimo režimas Pasirinkti</span><span class="sxs-lookup"><span data-stu-id="6ff94-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="6ff94-118">Kai naudojate brūkšninių kodų skaitytuvą, kad pasirinktumėte užduotį, pasikeičia „kanban“ srities rodymo režimas.</span><span class="sxs-lookup"><span data-stu-id="6ff94-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="6ff94-119">Dirbant šiuo režimu taikomos toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="6ff94-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="6ff94-120">Rodomos tik nuskaitytos „kanban“ užduotys.</span><span class="sxs-lookup"><span data-stu-id="6ff94-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="6ff94-121">Pasirinktos užduoties informacija rodoma „FastTab“ skirtuke **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="6ff94-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="6ff94-122">„FastTab“ skirtuke **Pranešimai** rodomi tik pasirinktos užduoties pranešimai.</span><span class="sxs-lookup"><span data-stu-id="6ff94-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="6ff94-123">Galite keisti užduoties būseną naudodami funkcijas, esančias dalyje Veiksmų sritis.</span><span class="sxs-lookup"><span data-stu-id="6ff94-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="6ff94-124">„Kanban“ perkėlimo sritis tuo metu toliau rodo tik vieną užduotį.</span><span class="sxs-lookup"><span data-stu-id="6ff94-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="6ff94-125">Galite patys atnaujinti užduočių sąrašo informaciją dalyje Veiksmų sritis spustelėdami **Atnaujinti** („Shift“ + F5).</span><span class="sxs-lookup"><span data-stu-id="6ff94-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="6ff94-126">Atnaujinus informaciją vėl rodomi visi užduoties filtro rezultatai.</span><span class="sxs-lookup"><span data-stu-id="6ff94-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="6ff94-127">Užduoties būsena ir galimi veiksmai</span><span class="sxs-lookup"><span data-stu-id="6ff94-127">Job status and possible actions</span></span>
<span data-ttu-id="6ff94-128">Pasirinktos užduoties būsena ir bet kurios iškviestos įvykio užduoties „kanban“ būsena nurodo, ar galima vykdyti užduotį toliau.</span><span class="sxs-lookup"><span data-stu-id="6ff94-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="6ff94-129">Toliau pateiktoje lentelėje rodoma informacija apie šias būsenas ir užduotis:</span><span class="sxs-lookup"><span data-stu-id="6ff94-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="6ff94-130">Galimos užduočių arba sandėliavimo vienetų, nurodytų užduotyse, būsenos.</span><span class="sxs-lookup"><span data-stu-id="6ff94-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="6ff94-131">Kiekviena užduotis, kurią gali atlikti vykdant užduotį.</span><span class="sxs-lookup"><span data-stu-id="6ff94-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ff94-132">Užduoties tipas</span><span class="sxs-lookup"><span data-stu-id="6ff94-132">Job type</span></span></th>
<th><span data-ttu-id="6ff94-133">Užduoties būsena arba sandėliavimo vieneto būsena</span><span class="sxs-lookup"><span data-stu-id="6ff94-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="6ff94-134">Naujinti išrinkimo dokumentą</span><span class="sxs-lookup"><span data-stu-id="6ff94-134">Update picking list</span></span></th>
<th><span data-ttu-id="6ff94-135">Paleisti</span><span class="sxs-lookup"><span data-stu-id="6ff94-135">Start</span></span></th>
<th><span data-ttu-id="6ff94-136">Atnaujinti registraciją</span><span class="sxs-lookup"><span data-stu-id="6ff94-136">Update registration</span></span></th>
<th><span data-ttu-id="6ff94-137">Baigti</span><span class="sxs-lookup"><span data-stu-id="6ff94-137">Complete</span></span></th>
<th><span data-ttu-id="6ff94-138">Tuščias</span><span class="sxs-lookup"><span data-stu-id="6ff94-138">Empty</span></span></th>
<th><span data-ttu-id="6ff94-139">Kurti įvykio „kanban“</span><span class="sxs-lookup"><span data-stu-id="6ff94-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ff94-140">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="6ff94-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="6ff94-141">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="6ff94-141">Not planned</span></span></li>
<li><span data-ttu-id="6ff94-142">Nėra iškviestų užduočių, arba iškviestų užduočių būsena yra Baigta</span><span class="sxs-lookup"><span data-stu-id="6ff94-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="6ff94-143">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-143">Yes</span></span></td>
<td><span data-ttu-id="6ff94-144">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-144">Yes</span></span></td>
<td><span data-ttu-id="6ff94-145">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-145">Yes</span></span></td>
<td><span data-ttu-id="6ff94-146">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-146">Yes</span></span></td>
<td><span data-ttu-id="6ff94-147">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-147">No</span></span></td>
<td><span data-ttu-id="6ff94-148">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ff94-149">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="6ff94-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="6ff94-150">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="6ff94-150">Not planned</span></span></li>
<li><span data-ttu-id="6ff94-151">Iškviestos užduoties būsena nėra Baigta</span><span class="sxs-lookup"><span data-stu-id="6ff94-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="6ff94-152">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-152">Yes</span></span></td>
<td><span data-ttu-id="6ff94-153">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-153">No</span></span></td>
<td><span data-ttu-id="6ff94-154">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-154">Yes</span></span></td>
<td><span data-ttu-id="6ff94-155">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-155">No</span></span></td>
<td><span data-ttu-id="6ff94-156">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-156">No</span></span></td>
<td><span data-ttu-id="6ff94-157">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ff94-158">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="6ff94-158">Transfer</span></span></td>
<td><span data-ttu-id="6ff94-159">Vykdoma</span><span class="sxs-lookup"><span data-stu-id="6ff94-159">In progress</span></span></td>
<td><span data-ttu-id="6ff94-160">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-160">Yes</span></span></td>
<td><span data-ttu-id="6ff94-161">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-161">No</span></span></td>
<td><span data-ttu-id="6ff94-162">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-162">Yes</span></span></td>
<td><span data-ttu-id="6ff94-163">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-163">Yes</span></span></td>
<td><span data-ttu-id="6ff94-164">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-164">No</span></span></td>
<td><span data-ttu-id="6ff94-165">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ff94-166">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="6ff94-166">Transfer</span></span></td>
<td><span data-ttu-id="6ff94-167">Atlikta</span><span class="sxs-lookup"><span data-stu-id="6ff94-167">Completed</span></span></td>
<td><span data-ttu-id="6ff94-168">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-168">No</span></span></td>
<td><span data-ttu-id="6ff94-169">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-169">No</span></span></td>
<td><span data-ttu-id="6ff94-170">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-170">No</span></span></td>
<td><span data-ttu-id="6ff94-171">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-171">No</span></span></td>
<td><span data-ttu-id="6ff94-172">Taip</span><span class="sxs-lookup"><span data-stu-id="6ff94-172">Yes</span></span></td>
<td><span data-ttu-id="6ff94-173">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ff94-174">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="6ff94-174">Transfer or process</span></span></td>
<td><span data-ttu-id="6ff94-175">Tuščias</span><span class="sxs-lookup"><span data-stu-id="6ff94-175">Empty</span></span></td>
<td><span data-ttu-id="6ff94-176">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-176">No</span></span></td>
<td><span data-ttu-id="6ff94-177">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-177">No</span></span></td>
<td><span data-ttu-id="6ff94-178">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-178">No</span></span></td>
<td><span data-ttu-id="6ff94-179">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-179">No</span></span></td>
<td><span data-ttu-id="6ff94-180">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-180">No</span></span></td>
<td><span data-ttu-id="6ff94-181">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ff94-182">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="6ff94-182">Transfer or process</span></span></td>
<td><span data-ttu-id="6ff94-183">Nerasta „kanban“ kortelė</span><span class="sxs-lookup"><span data-stu-id="6ff94-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="6ff94-184">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-184">No</span></span></td>
<td><span data-ttu-id="6ff94-185">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-185">No</span></span></td>
<td><span data-ttu-id="6ff94-186">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-186">No</span></span></td>
<td><span data-ttu-id="6ff94-187">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-187">No</span></span></td>
<td><span data-ttu-id="6ff94-188">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-188">No</span></span></td>
<td><span data-ttu-id="6ff94-189">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ff94-190">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="6ff94-190">Transfer or process</span></span></td>
<td><span data-ttu-id="6ff94-191">„Kanban“ kortelė rasta, bet ji nepriskirta „kanban“</span><span class="sxs-lookup"><span data-stu-id="6ff94-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="6ff94-192">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-192">No</span></span></td>
<td><span data-ttu-id="6ff94-193">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-193">No</span></span></td>
<td><span data-ttu-id="6ff94-194">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-194">No</span></span></td>
<td><span data-ttu-id="6ff94-195">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-195">No</span></span></td>
<td><span data-ttu-id="6ff94-196">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-196">No</span></span></td>
<td><span data-ttu-id="6ff94-197">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ff94-198">Apdoroti</span><span class="sxs-lookup"><span data-stu-id="6ff94-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="6ff94-199">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="6ff94-199">Not planned</span></span></li>
<li><span data-ttu-id="6ff94-200">Parengta</span><span class="sxs-lookup"><span data-stu-id="6ff94-200">Prepared</span></span></li>
<li><span data-ttu-id="6ff94-201">Vykdoma</span><span class="sxs-lookup"><span data-stu-id="6ff94-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="6ff94-202">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-202">No</span></span></td>
<td><span data-ttu-id="6ff94-203">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-203">No</span></span></td>
<td><span data-ttu-id="6ff94-204">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-204">No</span></span></td>
<td><span data-ttu-id="6ff94-205">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-205">No</span></span></td>
<td><span data-ttu-id="6ff94-206">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-206">No</span></span></td>
<td><span data-ttu-id="6ff94-207">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ff94-208">Apdoroti</span><span class="sxs-lookup"><span data-stu-id="6ff94-208">Process</span></span></td>
<td><span data-ttu-id="6ff94-209">Atlikta</span><span class="sxs-lookup"><span data-stu-id="6ff94-209">Completed</span></span></td>
<td><span data-ttu-id="6ff94-210">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-210">No</span></span></td>
<td><span data-ttu-id="6ff94-211">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-211">No</span></span></td>
<td><span data-ttu-id="6ff94-212">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-212">No</span></span></td>
<td><span data-ttu-id="6ff94-213">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-213">No</span></span></td>
<td><span data-ttu-id="6ff94-214">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-214">No</span></span></td>
<td><span data-ttu-id="6ff94-215">Ne</span><span class="sxs-lookup"><span data-stu-id="6ff94-215">No</span></span></td>
</tr>
</tbody>
</table>






