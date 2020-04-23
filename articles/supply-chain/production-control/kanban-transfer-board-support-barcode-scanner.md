---
title: „Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas
description: „Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bd6f1bdd847f74cee7d3594d19b72454063c0cb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207191"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="7367a-103">„Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas</span><span class="sxs-lookup"><span data-stu-id="7367a-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7367a-104">„Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti.</span><span class="sxs-lookup"><span data-stu-id="7367a-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="7367a-105">Registravimo režimai</span><span class="sxs-lookup"><span data-stu-id="7367a-105">Registration modes</span></span>
------------------

<span data-ttu-id="7367a-106">„FastTab“ skirtuke **Skaitytuvo registravimas** galite pasirinkti registravimo režimą, kuris valdo veiksmą, kai nuskaitote „kanban“ kortelės numerį arba patys įvedate numerį „kanban“ kortelės numerio lauke.</span><span class="sxs-lookup"><span data-stu-id="7367a-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="7367a-107">Nustatyti registravimo režimą</span><span class="sxs-lookup"><span data-stu-id="7367a-107">Set registration mode</span></span> | <span data-ttu-id="7367a-108">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7367a-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7367a-109">Paleisti</span><span class="sxs-lookup"><span data-stu-id="7367a-109">Start</span></span>                 | <span data-ttu-id="7367a-110">Registruoja „kanban“ perkėlimo užduotį kaip nebaigtą.</span><span class="sxs-lookup"><span data-stu-id="7367a-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="7367a-111">Baigti</span><span class="sxs-lookup"><span data-stu-id="7367a-111">Complete</span></span>              | <span data-ttu-id="7367a-112">Registruoja „kanban“ perkėlimo užduotį kaip baigtą.</span><span class="sxs-lookup"><span data-stu-id="7367a-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="7367a-113">Tuščias</span><span class="sxs-lookup"><span data-stu-id="7367a-113">Empty</span></span>                 | <span data-ttu-id="7367a-114">Registruoja medžiagų sandėliavimo vienetą, „kanban“ kortelėje nurodytą kaip tuščią.</span><span class="sxs-lookup"><span data-stu-id="7367a-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="7367a-115">Pasirinkti</span><span class="sxs-lookup"><span data-stu-id="7367a-115">Select</span></span>                | <span data-ttu-id="7367a-116">Registruoja „kanban“ kortelės numerį ir automatiškai pasirenka nurodytą užduotį „kanban“ sąraše.</span><span class="sxs-lookup"><span data-stu-id="7367a-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="7367a-117">Registravimo režimas Pasirinkti</span><span class="sxs-lookup"><span data-stu-id="7367a-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="7367a-118">Kai naudojate brūkšninių kodų skaitytuvą, kad pasirinktumėte užduotį, pasikeičia „kanban“ srities rodymo režimas.</span><span class="sxs-lookup"><span data-stu-id="7367a-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="7367a-119">Dirbant šiuo režimu taikomos toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="7367a-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="7367a-120">Rodomos tik nuskaitytos „kanban“ užduotys.</span><span class="sxs-lookup"><span data-stu-id="7367a-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="7367a-121">Pasirinktos užduoties informacija rodoma „FastTab“ skirtuke **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="7367a-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="7367a-122">„FastTab“ skirtuke **Pranešimai** rodomi tik pasirinktos užduoties pranešimai.</span><span class="sxs-lookup"><span data-stu-id="7367a-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="7367a-123">Galite keisti užduoties būseną naudodami funkcijas, esančias dalyje Veiksmų sritis.</span><span class="sxs-lookup"><span data-stu-id="7367a-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="7367a-124">„Kanban“ perkėlimo sritis tuo metu toliau rodo tik vieną užduotį.</span><span class="sxs-lookup"><span data-stu-id="7367a-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="7367a-125">Galite patys atnaujinti užduočių sąrašo informaciją dalyje Veiksmų sritis spustelėdami **Atnaujinti** („Shift“ + F5).</span><span class="sxs-lookup"><span data-stu-id="7367a-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="7367a-126">Atnaujinus informaciją vėl rodomi visi užduoties filtro rezultatai.</span><span class="sxs-lookup"><span data-stu-id="7367a-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="7367a-127">Užduoties būsena ir galimi veiksmai</span><span class="sxs-lookup"><span data-stu-id="7367a-127">Job status and possible actions</span></span>
<span data-ttu-id="7367a-128">Pasirinktos užduoties būsena ir bet kurios iškviestos įvykio užduoties „kanban“ būsena nurodo, ar galima vykdyti užduotį toliau.</span><span class="sxs-lookup"><span data-stu-id="7367a-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="7367a-129">Toliau pateiktoje lentelėje rodoma informacija apie šias būsenas ir užduotis:</span><span class="sxs-lookup"><span data-stu-id="7367a-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="7367a-130">Galimos užduočių arba sandėliavimo vienetų, nurodytų užduotyse, būsenos.</span><span class="sxs-lookup"><span data-stu-id="7367a-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="7367a-131">Kiekviena užduotis, kurią gali atlikti vykdant užduotį.</span><span class="sxs-lookup"><span data-stu-id="7367a-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="7367a-132">Užduoties tipas</span><span class="sxs-lookup"><span data-stu-id="7367a-132">Job type</span></span></th>
<th><span data-ttu-id="7367a-133">Užduoties būsena arba sandėliavimo vieneto būsena</span><span class="sxs-lookup"><span data-stu-id="7367a-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="7367a-134">Naujinti išrinkimo dokumentą</span><span class="sxs-lookup"><span data-stu-id="7367a-134">Update picking list</span></span></th>
<th><span data-ttu-id="7367a-135">Paleisti</span><span class="sxs-lookup"><span data-stu-id="7367a-135">Start</span></span></th>
<th><span data-ttu-id="7367a-136">Atnaujinti registraciją</span><span class="sxs-lookup"><span data-stu-id="7367a-136">Update registration</span></span></th>
<th><span data-ttu-id="7367a-137">Baigti</span><span class="sxs-lookup"><span data-stu-id="7367a-137">Complete</span></span></th>
<th><span data-ttu-id="7367a-138">Tuščias</span><span class="sxs-lookup"><span data-stu-id="7367a-138">Empty</span></span></th>
<th><span data-ttu-id="7367a-139">Kurti įvykio „kanban“</span><span class="sxs-lookup"><span data-stu-id="7367a-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7367a-140">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="7367a-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="7367a-141">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="7367a-141">Not planned</span></span></li>
<li><span data-ttu-id="7367a-142">Nėra iškviestų užduočių, arba iškviestų užduočių būsena yra Baigta</span><span class="sxs-lookup"><span data-stu-id="7367a-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="7367a-143">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-143">Yes</span></span></td>
<td><span data-ttu-id="7367a-144">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-144">Yes</span></span></td>
<td><span data-ttu-id="7367a-145">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-145">Yes</span></span></td>
<td><span data-ttu-id="7367a-146">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-146">Yes</span></span></td>
<td><span data-ttu-id="7367a-147">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-147">No</span></span></td>
<td><span data-ttu-id="7367a-148">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7367a-149">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="7367a-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="7367a-150">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="7367a-150">Not planned</span></span></li>
<li><span data-ttu-id="7367a-151">Iškviestos užduoties būsena nėra Baigta</span><span class="sxs-lookup"><span data-stu-id="7367a-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="7367a-152">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-152">Yes</span></span></td>
<td><span data-ttu-id="7367a-153">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-153">No</span></span></td>
<td><span data-ttu-id="7367a-154">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-154">Yes</span></span></td>
<td><span data-ttu-id="7367a-155">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-155">No</span></span></td>
<td><span data-ttu-id="7367a-156">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-156">No</span></span></td>
<td><span data-ttu-id="7367a-157">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7367a-158">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="7367a-158">Transfer</span></span></td>
<td><span data-ttu-id="7367a-159">Vykdoma</span><span class="sxs-lookup"><span data-stu-id="7367a-159">In progress</span></span></td>
<td><span data-ttu-id="7367a-160">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-160">Yes</span></span></td>
<td><span data-ttu-id="7367a-161">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-161">No</span></span></td>
<td><span data-ttu-id="7367a-162">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-162">Yes</span></span></td>
<td><span data-ttu-id="7367a-163">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-163">Yes</span></span></td>
<td><span data-ttu-id="7367a-164">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-164">No</span></span></td>
<td><span data-ttu-id="7367a-165">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7367a-166">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="7367a-166">Transfer</span></span></td>
<td><span data-ttu-id="7367a-167">Atlikta</span><span class="sxs-lookup"><span data-stu-id="7367a-167">Completed</span></span></td>
<td><span data-ttu-id="7367a-168">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-168">No</span></span></td>
<td><span data-ttu-id="7367a-169">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-169">No</span></span></td>
<td><span data-ttu-id="7367a-170">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-170">No</span></span></td>
<td><span data-ttu-id="7367a-171">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-171">No</span></span></td>
<td><span data-ttu-id="7367a-172">Taip</span><span class="sxs-lookup"><span data-stu-id="7367a-172">Yes</span></span></td>
<td><span data-ttu-id="7367a-173">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7367a-174">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="7367a-174">Transfer or process</span></span></td>
<td><span data-ttu-id="7367a-175">Tuščias</span><span class="sxs-lookup"><span data-stu-id="7367a-175">Empty</span></span></td>
<td><span data-ttu-id="7367a-176">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-176">No</span></span></td>
<td><span data-ttu-id="7367a-177">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-177">No</span></span></td>
<td><span data-ttu-id="7367a-178">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-178">No</span></span></td>
<td><span data-ttu-id="7367a-179">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-179">No</span></span></td>
<td><span data-ttu-id="7367a-180">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-180">No</span></span></td>
<td><span data-ttu-id="7367a-181">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7367a-182">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="7367a-182">Transfer or process</span></span></td>
<td><span data-ttu-id="7367a-183">Nerasta „kanban“ kortelė</span><span class="sxs-lookup"><span data-stu-id="7367a-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="7367a-184">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-184">No</span></span></td>
<td><span data-ttu-id="7367a-185">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-185">No</span></span></td>
<td><span data-ttu-id="7367a-186">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-186">No</span></span></td>
<td><span data-ttu-id="7367a-187">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-187">No</span></span></td>
<td><span data-ttu-id="7367a-188">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-188">No</span></span></td>
<td><span data-ttu-id="7367a-189">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7367a-190">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="7367a-190">Transfer or process</span></span></td>
<td><span data-ttu-id="7367a-191">„Kanban“ kortelė rasta, bet ji nepriskirta „kanban“</span><span class="sxs-lookup"><span data-stu-id="7367a-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="7367a-192">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-192">No</span></span></td>
<td><span data-ttu-id="7367a-193">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-193">No</span></span></td>
<td><span data-ttu-id="7367a-194">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-194">No</span></span></td>
<td><span data-ttu-id="7367a-195">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-195">No</span></span></td>
<td><span data-ttu-id="7367a-196">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-196">No</span></span></td>
<td><span data-ttu-id="7367a-197">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7367a-198">Apdoroti</span><span class="sxs-lookup"><span data-stu-id="7367a-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="7367a-199">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="7367a-199">Not planned</span></span></li>
<li><span data-ttu-id="7367a-200">Parengta</span><span class="sxs-lookup"><span data-stu-id="7367a-200">Prepared</span></span></li>
<li><span data-ttu-id="7367a-201">Vykdoma</span><span class="sxs-lookup"><span data-stu-id="7367a-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="7367a-202">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-202">No</span></span></td>
<td><span data-ttu-id="7367a-203">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-203">No</span></span></td>
<td><span data-ttu-id="7367a-204">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-204">No</span></span></td>
<td><span data-ttu-id="7367a-205">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-205">No</span></span></td>
<td><span data-ttu-id="7367a-206">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-206">No</span></span></td>
<td><span data-ttu-id="7367a-207">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7367a-208">Apdoroti</span><span class="sxs-lookup"><span data-stu-id="7367a-208">Process</span></span></td>
<td><span data-ttu-id="7367a-209">Atlikta</span><span class="sxs-lookup"><span data-stu-id="7367a-209">Completed</span></span></td>
<td><span data-ttu-id="7367a-210">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-210">No</span></span></td>
<td><span data-ttu-id="7367a-211">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-211">No</span></span></td>
<td><span data-ttu-id="7367a-212">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-212">No</span></span></td>
<td><span data-ttu-id="7367a-213">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-213">No</span></span></td>
<td><span data-ttu-id="7367a-214">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-214">No</span></span></td>
<td><span data-ttu-id="7367a-215">Ne</span><span class="sxs-lookup"><span data-stu-id="7367a-215">No</span></span></td>
</tr>
</tbody>
</table>





