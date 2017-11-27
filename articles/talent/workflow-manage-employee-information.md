---
title: Darbo eigos naudojimas darbuotojo informacijai tvarkyti
description: "Šioje temoje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją. Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47c569f3531bf00795078b7b042bf899b51bad8d
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="9f09b-104">Darbo eigos naudojimas darbuotojo informacijai tvarkyti</span><span class="sxs-lookup"><span data-stu-id="9f09b-104">Use workflows to manage employee information</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9f09b-105">Šioje temoje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją.</span><span class="sxs-lookup"><span data-stu-id="9f09b-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="9f09b-106">Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus.</span><span class="sxs-lookup"><span data-stu-id="9f09b-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="9f09b-107">Darbo eigos tinkamumas personalui suteikia galimybę pritaikyti daugybę darbo eigų personalo veiklai tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="9f09b-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="9f09b-108">Be to, yra daugybė parinkčių, kuriomis pasinaudoję galite modifikuoti konkrečias darbo eigas ir susieti jas su ataskaitų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="9f09b-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="9f09b-109">Naudojant darbo eigas jos padeda tvarkyti keleto standartinių darbuotojo informacijos tipų pokyčius.</span><span class="sxs-lookup"><span data-stu-id="9f09b-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="9f09b-110">Darbo eigą galite susieti su pareigomis.</span><span class="sxs-lookup"><span data-stu-id="9f09b-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="9f09b-111">Tada, jei darbuotojai pakeičia savo įrašus, pradedama darbo eiga, kurią reikia patvirtinti prieš išsaugant naują informaciją.</span><span class="sxs-lookup"><span data-stu-id="9f09b-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="9f09b-112">Toliau nurodytų informacijos tipų darbo eigos yra nustatytos iš karto, kad padėtų efektyviai tvarkyti pokyčius, o darbuotojų duomenys išliktų tikslūs.</span><span class="sxs-lookup"><span data-stu-id="9f09b-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="9f09b-113">Identifikavimo numeriai</span><span class="sxs-lookup"><span data-stu-id="9f09b-113">Identification numbers</span></span>
-   <span data-ttu-id="9f09b-114">Kursai</span><span class="sxs-lookup"><span data-stu-id="9f09b-114">Courses</span></span>
-   <span data-ttu-id="9f09b-115">Išsilavinimas</span><span class="sxs-lookup"><span data-stu-id="9f09b-115">Education</span></span>
-   <span data-ttu-id="9f09b-116">Vaizdas</span><span class="sxs-lookup"><span data-stu-id="9f09b-116">Image</span></span>
-   <span data-ttu-id="9f09b-117">Panaudos prekės</span><span class="sxs-lookup"><span data-stu-id="9f09b-117">Loaned items</span></span>
-   <span data-ttu-id="9f09b-118">Profesinė patirtis</span><span class="sxs-lookup"><span data-stu-id="9f09b-118">Professional experience</span></span>
-   <span data-ttu-id="9f09b-119">Darbo projektuose patirtis</span><span class="sxs-lookup"><span data-stu-id="9f09b-119">Project experience</span></span>
-   <span data-ttu-id="9f09b-120">Įgūdžiai</span><span class="sxs-lookup"><span data-stu-id="9f09b-120">Skills</span></span>
-   <span data-ttu-id="9f09b-121">Atsakingos pareigos</span><span class="sxs-lookup"><span data-stu-id="9f09b-121">Positions of trust</span></span>
-   <span data-ttu-id="9f09b-122">Personalo veiksmai</span><span class="sxs-lookup"><span data-stu-id="9f09b-122">Human resources actions</span></span>
-   <span data-ttu-id="9f09b-123">Kursų registracija</span><span class="sxs-lookup"><span data-stu-id="9f09b-123">Course registration</span></span>

<span data-ttu-id="9f09b-124">Pasamdžius, perkėlus ar atleidus darbuotojus į darbo eigą gali būti įtrauktas peržiūros procesas.</span><span class="sxs-lookup"><span data-stu-id="9f09b-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="9f09b-125">Tokiu būdu galima peržiūrėti dokumentą arba veiksmo sąlygas apibrėžti kaip darbo eigos dalį.</span><span class="sxs-lookup"><span data-stu-id="9f09b-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="9f09b-126">Atlikus peržiūros procesą, parengiamas dokumentas arba užbaigiamas veiksmas, o darbo eiga perkeliama į paskutinį patvirtinimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="9f09b-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="9f09b-127">Darbo eigos susiejimas su pareigų hierarchija</span><span class="sxs-lookup"><span data-stu-id="9f09b-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="9f09b-128">Darbo eigą galite susieti su bet kuria jūsų sukonfigūruota hierarchija.</span><span class="sxs-lookup"><span data-stu-id="9f09b-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="9f09b-129">Pavyzdžiui, jei pareigos susiejamos su ataskaitų hierarchijos matrica, galite sukonfigūruoti darbo eigą, nukreipiančią konkretaus projekto išlaidas projekto vadovui, o ne darbuotojo, susieto su tomis pareigomis, vadovui.</span><span class="sxs-lookup"><span data-stu-id="9f09b-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="9f09b-130">Norėdami sukurti naują darbo eigą arba modifikuoti esamą, puslapyje **Personalo darbo eiga** spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="9f09b-131">Sąraše pasirinkite darbo eigą, kad paleistumėte darbo eigos dizaino įrankį.</span><span class="sxs-lookup"><span data-stu-id="9f09b-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="9f09b-132">Dizaino įrankį galite naudoti kurdami naują darbo eigą arba keisdami jau esančios darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9f09b-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="9f09b-133">Pakeitus esamą darbo eigą pakeitimai išsaugomi kaip nauja versija.</span><span class="sxs-lookup"><span data-stu-id="9f09b-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="9f09b-134">Todėl, jei reikia, galite bet kada sugrįžti prie ankstesnės versijos.</span><span class="sxs-lookup"><span data-stu-id="9f09b-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="9f09b-135">Personalo darbo eigos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9f09b-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="9f09b-136">Norėdami sukonfigūruoti pagrindinę darbo eigą, pradedamą darbuotojui pareikalavus pakeisti asmens identifikavimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9f09b-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="9f09b-137">Puslapyje **Personalo darbo eigos** spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="9f09b-138">Galimų darbo eigų sąraše pasirinkite **Identifikavimo numeriai**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="9f09b-139">Spustelėkite **Vykdyti**, kad paleistumėte darbo eigos dizaino įrankį, tada, kai būsite paraginti, įveskite vartotojo vardą ir slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="9f09b-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="9f09b-140">Elementą **Patvirtinti identifikavimo numerį** iš darbo eigos elementų sąrašo nuvilkite į dizaino įrankio lauką.</span><span class="sxs-lookup"><span data-stu-id="9f09b-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="9f09b-141">Patvirtinimo elementą sujunkite su **Pradėti** ir **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="9f09b-142">Dukart spustelėkite **Patvirtinti elementą**, tada spustelėkite dešinįjį pelės klavišą ir pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="9f09b-143">Norėdami įtraukti darbo elemento instrukcijų, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9f09b-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="9f09b-144">Pasirinkite **Priskyrimas**, tada iš priskyrimo tipo pasirinkite **Hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="9f09b-145">Pasirinkimo srityje **Hierarchija** pasirinkite **Konfigūruojama hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="9f09b-146">Įtraukite sustabdymo sąlygą ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9f09b-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="9f09b-147">Atlikite papildomas instrukcijas (neturi būti jokių papildomų įspėjimų).</span><span class="sxs-lookup"><span data-stu-id="9f09b-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="9f09b-148">Spustelėkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-148">Click **Save and close**.</span></span> <span data-ttu-id="9f09b-149">Atsidarius dialogo langui aktyvinkite naują darbo eigą ir pasirinkite **Padaryti aktyvų**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="9f09b-150">Pasirinkite **Personalas** &gt; **Pareigos** &gt; **Pareigų hierarchijos tipai**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="9f09b-151">Pasirinkite **Matrica**.</span><span class="sxs-lookup"><span data-stu-id="9f09b-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="9f09b-152">Įtraukite darbo eigą **Darbininko identifikavimo numeris** į sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9f09b-152">Add the **Worker identification number** workflow to the list.</span></span>





