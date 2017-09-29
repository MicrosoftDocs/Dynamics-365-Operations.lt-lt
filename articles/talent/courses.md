---
title: "Mokymų kursų nustatymas"
description: "Žmogiškųjų išteklių administratoriai ir vadovai kursų funkcijas gali naudoti siekdami tvarkyti informaciją apie darbuotojams siūlomą mokymą."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0ab79e85872c19e30f24e182ea483687ecc0bc09
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="set-up-training-courses"></a><span data-ttu-id="f3e78-103">Mokymų kursų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f3e78-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f3e78-104">Žmogiškųjų išteklių administratoriai ir vadovai kursų funkcijas gali naudoti siekdami tvarkyti informaciją apie darbuotojams siūlomą mokymą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="f3e78-105"> Nustatyti būtinąsias sąlygas</span><span class="sxs-lookup"><span data-stu-id="f3e78-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="f3e78-106">Prieš kuriant kursus, reikia turėti ir nustatyti toliau pateiktą informaciją.</span><span class="sxs-lookup"><span data-stu-id="f3e78-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="f3e78-107">**Kursų tipai**</span><span class="sxs-lookup"><span data-stu-id="f3e78-107">**Course types**</span></span>

<span data-ttu-id="f3e78-108">Ši informacija yra nebūtina informacija, kurią galite nurodyti apie kursus.</span><span class="sxs-lookup"><span data-stu-id="f3e78-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="f3e78-109">Jei žinote, kad įvesite šią kursų informaciją, turėtumėte ją nustatyti prieš sukurdami kursų įrašus.</span><span class="sxs-lookup"><span data-stu-id="f3e78-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="f3e78-110">**Auditorijų grupės**</span><span class="sxs-lookup"><span data-stu-id="f3e78-110">**Classroom groups**</span></span>
-   <span data-ttu-id="f3e78-111">**Kursų grupės**</span><span class="sxs-lookup"><span data-stu-id="f3e78-111">**Course groups**</span></span>
-   <span data-ttu-id="f3e78-112">**Kursų vietos**</span><span class="sxs-lookup"><span data-stu-id="f3e78-112">**Course locations**</span></span>
-   <span data-ttu-id="f3e78-113">**Auditorijos**</span><span class="sxs-lookup"><span data-stu-id="f3e78-113">**Classrooms**</span></span>
-   <span data-ttu-id="f3e78-114">**Dėstytojai**</span><span class="sxs-lookup"><span data-stu-id="f3e78-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="f3e78-115">Kursų tipai</span><span class="sxs-lookup"><span data-stu-id="f3e78-115">Course types</span></span>
<span data-ttu-id="f3e78-116">Kursų tipus galite naudoti kursams pagal kurso struktūrą arba turinį suskirstyti.</span><span class="sxs-lookup"><span data-stu-id="f3e78-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="f3e78-117">Kurti kursų tipus galite **Kursų tipų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3e78-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="f3e78-118">Kurdami kurso įrašą turite pasirinkti kursų tipą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="f3e78-119">Kursų nustatymo tipas</span><span class="sxs-lookup"><span data-stu-id="f3e78-119">Course setup type</span></span>
<span data-ttu-id="f3e78-120">Šioje lentelėje išvardijami trys kursų nustatymo tipai.</span><span class="sxs-lookup"><span data-stu-id="f3e78-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="f3e78-121">Kurso struktūra yra nustatoma pritaikius nustatymo tipus.</span><span class="sxs-lookup"><span data-stu-id="f3e78-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f3e78-122">Nustatymo tipas</span><span class="sxs-lookup"><span data-stu-id="f3e78-122">Setup type</span></span></th>
<th><span data-ttu-id="f3e78-123">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f3e78-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3e78-124"><strong>Stand.</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="f3e78-125">Pasirinkite šį tipą tiems kursams, kurių darbotvarkė nebus sudaryta kiekvienai dienai.</span><span class="sxs-lookup"><span data-stu-id="f3e78-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="f3e78-126">Tai yra numatytasis nustatymo tipas kuriant naują kursą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e78-127"><strong>Darbotvarkė</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="f3e78-128">Pasirinkite šį tipą, norėdami planuoti kurso, kuris vyksta kelias dienas, kiekvienos dienos informaciją.</span><span class="sxs-lookup"><span data-stu-id="f3e78-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e78-129"><strong>Darbotvarkė + sesija</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="f3e78-130">Pasirinkite šį tipą sudėtingesniems kursams.</span><span class="sxs-lookup"><span data-stu-id="f3e78-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="f3e78-131">Pavyzdžiui, kurso darbotvarkę galite suskirstyti į specializacijas ir sesijas.</span><span class="sxs-lookup"><span data-stu-id="f3e78-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="f3e78-132"><strong>Specializacija</strong> – specializacijos yra konkrečios kurso objekto sritys.</span><span class="sxs-lookup"><span data-stu-id="f3e78-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="f3e78-133"><strong>Sesijos</strong>: specializacijos padalinamos pritaikius sesijas, o sesijos gali padėti identifikuoti konkrečius procesus arba technikas, susijusias su kiekviena specializacija.</span><span class="sxs-lookup"><span data-stu-id="f3e78-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="f3e78-134">Kurso užduotys</span><span class="sxs-lookup"><span data-stu-id="f3e78-134">Course tasks</span></span>
<span data-ttu-id="f3e78-135">Su visais kursais galite atlikti toliau nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="f3e78-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="f3e78-136">Registruoti dalyvius.</span><span class="sxs-lookup"><span data-stu-id="f3e78-136">Register participants</span></span>
-   <span data-ttu-id="f3e78-137">Nurodyti paskutinę registracijos datą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="f3e78-138">Nustatyti mažiausią ir didžiausią dalyvių skaičių.</span><span class="sxs-lookup"><span data-stu-id="f3e78-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="f3e78-139">Priskirti kurso vietą ir auditoriją.</span><span class="sxs-lookup"><span data-stu-id="f3e78-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="f3e78-140">Kurso dalyviams rekomenduoti viešbučius.</span><span class="sxs-lookup"><span data-stu-id="f3e78-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="f3e78-141">Kurti kurso aprašą, kurį galima vėliau paskelbti Darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="f3e78-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="f3e78-142">**Pastaba.** Kursą panaikinti galite tik jei niekas į jį neužsiregistravo.</span><span class="sxs-lookup"><span data-stu-id="f3e78-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="f3e78-143">Kurso būsenos</span><span class="sxs-lookup"><span data-stu-id="f3e78-143">Course statuses</span></span>
<span data-ttu-id="f3e78-144">Šioje lentelėje pateikiamos galimos kurso būsenos ir veiksmai, kuriuos galite atlikti su konkrečios būsenos kursu.</span><span class="sxs-lookup"><span data-stu-id="f3e78-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f3e78-145">Būsena</span><span class="sxs-lookup"><span data-stu-id="f3e78-145">Status</span></span></th>
<th><span data-ttu-id="f3e78-146">Veiksmai</span><span class="sxs-lookup"><span data-stu-id="f3e78-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3e78-147"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f3e78-148">Įvesti ir modifikuoti kurso informaciją.</span><span class="sxs-lookup"><span data-stu-id="f3e78-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="f3e78-149">Kurso būseną keisti į <strong>Atidarytas</strong> – tada darbuotojai galės registruotis į kursą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e78-150"><strong>Atidaryti</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="f3e78-151">Registruoti dalyvius į kursą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="f3e78-152">Šalinti dalyvius iš kurso.</span><span class="sxs-lookup"><span data-stu-id="f3e78-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="f3e78-153">Patvirtinti kurso dalyvius.</span><span class="sxs-lookup"><span data-stu-id="f3e78-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="f3e78-154">Pakeisti kurso būseną į <strong>Uždarytas</strong> arba <strong>Atšauktas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f3e78-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="f3e78-155">Planuoti dalyvių, kurių būsena <strong>Patvirtintas</strong>, klausimynus.</span><span class="sxs-lookup"><span data-stu-id="f3e78-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e78-156"><strong>Uždaryta</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="f3e78-157">Galite iš naujo atidaryti kursą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e78-158"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="f3e78-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="f3e78-159">Galite iš naujo atidaryti kursą.</span><span class="sxs-lookup"><span data-stu-id="f3e78-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="f3e78-160">Kurso dalyviai</span><span class="sxs-lookup"><span data-stu-id="f3e78-160">Course participants</span></span>
<span data-ttu-id="f3e78-161">Kurso dalyviai yra darbuotojai, pretendentai arba kontaktiniai asmenys, dalyvaujantys mokymo kursuose arba renginyje.</span><span class="sxs-lookup"><span data-stu-id="f3e78-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="f3e78-162">Galite užregistruoti dalyvius tik į atvirus kursus.</span><span class="sxs-lookup"><span data-stu-id="f3e78-162">You can only register participants for open courses.</span></span> <span data-ttu-id="f3e78-163">Mažiausias ir didžiausias leistinas registruoti į kursą dalyvių skaičius nustatytas puslapio **Kursai** „FastTab“ skirtuke **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="f3e78-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="f3e78-164">Darbo eiga</span><span class="sxs-lookup"><span data-stu-id="f3e78-164">Workflow</span></span>
--------

<span data-ttu-id="f3e78-165">Darbuotojų, kurie į kursą registruojasi per puslapį **Darbuotojų savitarna**, registraciją galima nukreipti pro darbo eigą, kad būtų patvirtinta.</span><span class="sxs-lookup"><span data-stu-id="f3e78-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="f3e78-166">Darbo eigą priskirti kursui galima puslapio **Kursai** „FastTab‟ **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="f3e78-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>





