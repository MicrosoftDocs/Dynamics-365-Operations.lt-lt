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
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d65430d09c293fd5bca032b8b0e88c971d5a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246098"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="8e16c-103">„Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas</span><span class="sxs-lookup"><span data-stu-id="8e16c-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e16c-104">„Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti.</span><span class="sxs-lookup"><span data-stu-id="8e16c-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="8e16c-105">Registravimo režimai</span><span class="sxs-lookup"><span data-stu-id="8e16c-105">Registration modes</span></span>
------------------

<span data-ttu-id="8e16c-106">„FastTab“ skirtuke **Skaitytuvo registravimas** galite pasirinkti registravimo režimą, kuris valdo veiksmą, kai nuskaitote „kanban“ kortelės numerį arba patys įvedate numerį „kanban“ kortelės numerio lauke.</span><span class="sxs-lookup"><span data-stu-id="8e16c-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="8e16c-107">Nustatyti registravimo režimą</span><span class="sxs-lookup"><span data-stu-id="8e16c-107">Set registration mode</span></span> | <span data-ttu-id="8e16c-108">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8e16c-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e16c-109">Paleisti</span><span class="sxs-lookup"><span data-stu-id="8e16c-109">Start</span></span>                 | <span data-ttu-id="8e16c-110">Registruoja „kanban“ perkėlimo užduotį kaip nebaigtą.</span><span class="sxs-lookup"><span data-stu-id="8e16c-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="8e16c-111">Baigti</span><span class="sxs-lookup"><span data-stu-id="8e16c-111">Complete</span></span>              | <span data-ttu-id="8e16c-112">Registruoja „kanban“ perkėlimo užduotį kaip baigtą.</span><span class="sxs-lookup"><span data-stu-id="8e16c-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="8e16c-113">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8e16c-113">Empty</span></span>                 | <span data-ttu-id="8e16c-114">Registruoja medžiagų sandėliavimo vienetą, „kanban“ kortelėje nurodytą kaip tuščią.</span><span class="sxs-lookup"><span data-stu-id="8e16c-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="8e16c-115">Pasirinkti</span><span class="sxs-lookup"><span data-stu-id="8e16c-115">Select</span></span>                | <span data-ttu-id="8e16c-116">Registruoja „kanban“ kortelės numerį ir automatiškai pasirenka nurodytą užduotį „kanban“ sąraše.</span><span class="sxs-lookup"><span data-stu-id="8e16c-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="8e16c-117">Registravimo režimas Pasirinkti</span><span class="sxs-lookup"><span data-stu-id="8e16c-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="8e16c-118">Kai naudojate brūkšninių kodų skaitytuvą, kad pasirinktumėte užduotį, pasikeičia „kanban“ srities rodymo režimas.</span><span class="sxs-lookup"><span data-stu-id="8e16c-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="8e16c-119">Dirbant šiuo režimu taikomos toliau nurodytos sąlygos:</span><span class="sxs-lookup"><span data-stu-id="8e16c-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="8e16c-120">Rodomos tik nuskaitytos „kanban“ užduotys.</span><span class="sxs-lookup"><span data-stu-id="8e16c-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="8e16c-121">Pasirinktos užduoties informacija rodoma „FastTab“ skirtuke **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="8e16c-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="8e16c-122">„FastTab“ skirtuke **Pranešimai** rodomi tik pasirinktos užduoties pranešimai.</span><span class="sxs-lookup"><span data-stu-id="8e16c-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="8e16c-123">Galite keisti užduoties būseną naudodami funkcijas, esančias dalyje Veiksmų sritis.</span><span class="sxs-lookup"><span data-stu-id="8e16c-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="8e16c-124">„Kanban“ perkėlimo sritis tuo metu toliau rodo tik vieną užduotį.</span><span class="sxs-lookup"><span data-stu-id="8e16c-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="8e16c-125">Galite patys atnaujinti užduočių sąrašo informaciją dalyje Veiksmų sritis spustelėdami **Atnaujinti** („Shift“ + F5).</span><span class="sxs-lookup"><span data-stu-id="8e16c-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="8e16c-126">Atnaujinus informaciją vėl rodomi visi užduoties filtro rezultatai.</span><span class="sxs-lookup"><span data-stu-id="8e16c-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="8e16c-127">Užduoties būsena ir galimi veiksmai</span><span class="sxs-lookup"><span data-stu-id="8e16c-127">Job status and possible actions</span></span>
<span data-ttu-id="8e16c-128">Pasirinktos užduoties būsena ir bet kurios iškviestos įvykio užduoties „kanban“ būsena nurodo, ar galima vykdyti užduotį toliau.</span><span class="sxs-lookup"><span data-stu-id="8e16c-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="8e16c-129">Toliau pateiktoje lentelėje rodoma informacija apie šias būsenas ir užduotis:</span><span class="sxs-lookup"><span data-stu-id="8e16c-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="8e16c-130">Galimos užduočių arba sandėliavimo vienetų, nurodytų užduotyse, būsenos.</span><span class="sxs-lookup"><span data-stu-id="8e16c-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="8e16c-131">Kiekviena užduotis, kurią gali atlikti vykdant užduotį.</span><span class="sxs-lookup"><span data-stu-id="8e16c-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="8e16c-132">Užduoties tipas</span><span class="sxs-lookup"><span data-stu-id="8e16c-132">Job type</span></span></th>
<th><span data-ttu-id="8e16c-133">Užduoties būsena arba sandėliavimo vieneto būsena</span><span class="sxs-lookup"><span data-stu-id="8e16c-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="8e16c-134">Naujinti išrinkimo dokumentą</span><span class="sxs-lookup"><span data-stu-id="8e16c-134">Update picking list</span></span></th>
<th><span data-ttu-id="8e16c-135">Paleisti</span><span class="sxs-lookup"><span data-stu-id="8e16c-135">Start</span></span></th>
<th><span data-ttu-id="8e16c-136">Atnaujinti registraciją</span><span class="sxs-lookup"><span data-stu-id="8e16c-136">Update registration</span></span></th>
<th><span data-ttu-id="8e16c-137">Baigti</span><span class="sxs-lookup"><span data-stu-id="8e16c-137">Complete</span></span></th>
<th><span data-ttu-id="8e16c-138">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8e16c-138">Empty</span></span></th>
<th><span data-ttu-id="8e16c-139">Kurti įvykio „kanban“</span><span class="sxs-lookup"><span data-stu-id="8e16c-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e16c-140">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="8e16c-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="8e16c-141">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="8e16c-141">Not planned</span></span></li>
<li><span data-ttu-id="8e16c-142">Nėra iškviestų užduočių, arba iškviestų užduočių būsena yra Baigta</span><span class="sxs-lookup"><span data-stu-id="8e16c-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="8e16c-143">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-143">Yes</span></span></td>
<td><span data-ttu-id="8e16c-144">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-144">Yes</span></span></td>
<td><span data-ttu-id="8e16c-145">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-145">Yes</span></span></td>
<td><span data-ttu-id="8e16c-146">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-146">Yes</span></span></td>
<td><span data-ttu-id="8e16c-147">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-147">No</span></span></td>
<td><span data-ttu-id="8e16c-148">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e16c-149">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="8e16c-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="8e16c-150">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="8e16c-150">Not planned</span></span></li>
<li><span data-ttu-id="8e16c-151">Iškviestos užduoties būsena nėra Baigta</span><span class="sxs-lookup"><span data-stu-id="8e16c-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="8e16c-152">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-152">Yes</span></span></td>
<td><span data-ttu-id="8e16c-153">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-153">No</span></span></td>
<td><span data-ttu-id="8e16c-154">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-154">Yes</span></span></td>
<td><span data-ttu-id="8e16c-155">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-155">No</span></span></td>
<td><span data-ttu-id="8e16c-156">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-156">No</span></span></td>
<td><span data-ttu-id="8e16c-157">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e16c-158">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="8e16c-158">Transfer</span></span></td>
<td><span data-ttu-id="8e16c-159">Vykdoma</span><span class="sxs-lookup"><span data-stu-id="8e16c-159">In progress</span></span></td>
<td><span data-ttu-id="8e16c-160">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-160">Yes</span></span></td>
<td><span data-ttu-id="8e16c-161">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-161">No</span></span></td>
<td><span data-ttu-id="8e16c-162">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-162">Yes</span></span></td>
<td><span data-ttu-id="8e16c-163">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-163">Yes</span></span></td>
<td><span data-ttu-id="8e16c-164">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-164">No</span></span></td>
<td><span data-ttu-id="8e16c-165">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e16c-166">Perkėlimas</span><span class="sxs-lookup"><span data-stu-id="8e16c-166">Transfer</span></span></td>
<td><span data-ttu-id="8e16c-167">Atlikta</span><span class="sxs-lookup"><span data-stu-id="8e16c-167">Completed</span></span></td>
<td><span data-ttu-id="8e16c-168">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-168">No</span></span></td>
<td><span data-ttu-id="8e16c-169">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-169">No</span></span></td>
<td><span data-ttu-id="8e16c-170">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-170">No</span></span></td>
<td><span data-ttu-id="8e16c-171">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-171">No</span></span></td>
<td><span data-ttu-id="8e16c-172">Taip</span><span class="sxs-lookup"><span data-stu-id="8e16c-172">Yes</span></span></td>
<td><span data-ttu-id="8e16c-173">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e16c-174">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="8e16c-174">Transfer or process</span></span></td>
<td><span data-ttu-id="8e16c-175">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8e16c-175">Empty</span></span></td>
<td><span data-ttu-id="8e16c-176">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-176">No</span></span></td>
<td><span data-ttu-id="8e16c-177">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-177">No</span></span></td>
<td><span data-ttu-id="8e16c-178">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-178">No</span></span></td>
<td><span data-ttu-id="8e16c-179">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-179">No</span></span></td>
<td><span data-ttu-id="8e16c-180">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-180">No</span></span></td>
<td><span data-ttu-id="8e16c-181">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e16c-182">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="8e16c-182">Transfer or process</span></span></td>
<td><span data-ttu-id="8e16c-183">Nerasta „kanban“ kortelė</span><span class="sxs-lookup"><span data-stu-id="8e16c-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="8e16c-184">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-184">No</span></span></td>
<td><span data-ttu-id="8e16c-185">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-185">No</span></span></td>
<td><span data-ttu-id="8e16c-186">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-186">No</span></span></td>
<td><span data-ttu-id="8e16c-187">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-187">No</span></span></td>
<td><span data-ttu-id="8e16c-188">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-188">No</span></span></td>
<td><span data-ttu-id="8e16c-189">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e16c-190">Perkėlimas arba procesas</span><span class="sxs-lookup"><span data-stu-id="8e16c-190">Transfer or process</span></span></td>
<td><span data-ttu-id="8e16c-191">„Kanban“ kortelė rasta, bet ji nepriskirta „kanban“</span><span class="sxs-lookup"><span data-stu-id="8e16c-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="8e16c-192">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-192">No</span></span></td>
<td><span data-ttu-id="8e16c-193">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-193">No</span></span></td>
<td><span data-ttu-id="8e16c-194">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-194">No</span></span></td>
<td><span data-ttu-id="8e16c-195">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-195">No</span></span></td>
<td><span data-ttu-id="8e16c-196">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-196">No</span></span></td>
<td><span data-ttu-id="8e16c-197">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e16c-198">Apdoroti</span><span class="sxs-lookup"><span data-stu-id="8e16c-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="8e16c-199">Nesuplanuota</span><span class="sxs-lookup"><span data-stu-id="8e16c-199">Not planned</span></span></li>
<li><span data-ttu-id="8e16c-200">Parengta</span><span class="sxs-lookup"><span data-stu-id="8e16c-200">Prepared</span></span></li>
<li><span data-ttu-id="8e16c-201">Vykdoma</span><span class="sxs-lookup"><span data-stu-id="8e16c-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="8e16c-202">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-202">No</span></span></td>
<td><span data-ttu-id="8e16c-203">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-203">No</span></span></td>
<td><span data-ttu-id="8e16c-204">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-204">No</span></span></td>
<td><span data-ttu-id="8e16c-205">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-205">No</span></span></td>
<td><span data-ttu-id="8e16c-206">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-206">No</span></span></td>
<td><span data-ttu-id="8e16c-207">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e16c-208">Apdoroti</span><span class="sxs-lookup"><span data-stu-id="8e16c-208">Process</span></span></td>
<td><span data-ttu-id="8e16c-209">Atlikta</span><span class="sxs-lookup"><span data-stu-id="8e16c-209">Completed</span></span></td>
<td><span data-ttu-id="8e16c-210">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-210">No</span></span></td>
<td><span data-ttu-id="8e16c-211">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-211">No</span></span></td>
<td><span data-ttu-id="8e16c-212">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-212">No</span></span></td>
<td><span data-ttu-id="8e16c-213">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-213">No</span></span></td>
<td><span data-ttu-id="8e16c-214">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-214">No</span></span></td>
<td><span data-ttu-id="8e16c-215">Ne</span><span class="sxs-lookup"><span data-stu-id="8e16c-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]