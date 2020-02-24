---
title: Darbo jėgos organizavimas naudojant padalinius, užduotis ir pareigas
description: Padaliniai, užduotys ir pareigos yra organizaciniai elementai, tvarkomi modulyje Personalas. Šiame straipsnyje pateikiama abstrakti informacija apie šiuos elementus.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources, Retail
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 98b9ba7f45a3af38fdd24c09b9a3164d1547a0d5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009914"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="e9d88-104">Darbo jėgos organizavimas naudojant padalinius, užduotis ir pareigas</span><span class="sxs-lookup"><span data-stu-id="e9d88-104">Organize your workforce by using departments, jobs, and positions</span></span>

<span data-ttu-id="e9d88-105">Padaliniai, užduotys ir pareigos yra organizaciniai elementai, tvarkomi modulyje Personalas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="e9d88-106">Šiame straipsnyje pateikiama abstrakti informacija apie šiuos elementus.</span><span class="sxs-lookup"><span data-stu-id="e9d88-106">This article describes conceptual information about these elements.</span></span> 

<span data-ttu-id="e9d88-107">Šis pavyzdys skirtas sąvokoms, aprašytoms šiame straipsnyje, iliustruoti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-107">The following example is used to illustrate the concepts described in this article.</span></span>

|<span data-ttu-id="e9d88-108">**Skyrius**</span><span class="sxs-lookup"><span data-stu-id="e9d88-108">**Department**</span></span>|<span data-ttu-id="e9d88-109">**Pozicija**</span><span class="sxs-lookup"><span data-stu-id="e9d88-109">**Position**</span></span>|<span data-ttu-id="e9d88-110">**Užduotis**</span><span class="sxs-lookup"><span data-stu-id="e9d88-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="e9d88-111">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="e9d88-111">**Sales**</span></span>|<span data-ttu-id="e9d88-112">Pardavimo vadybininkas (rytų regionas)</span><span class="sxs-lookup"><span data-stu-id="e9d88-112">Sales manager (East)</span></span>|<span data-ttu-id="e9d88-113">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="e9d88-113">Sales manager</span></span>|
|<span data-ttu-id="e9d88-114">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="e9d88-114">**Sales**</span></span>|<span data-ttu-id="e9d88-115">Pardavimo vadybininkas (vakarų regionas)</span><span class="sxs-lookup"><span data-stu-id="e9d88-115">Sales manager (West)</span></span>|<span data-ttu-id="e9d88-116">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="e9d88-116">Sales manager</span></span>|
|<span data-ttu-id="e9d88-117">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="e9d88-117">**Sales**</span></span>|<span data-ttu-id="e9d88-118">Pardavimo vadybininkas (centrinis regionas)</span><span class="sxs-lookup"><span data-stu-id="e9d88-118">Sales manager (Central)</span></span>|<span data-ttu-id="e9d88-119">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="e9d88-119">Sales manager</span></span>|
|<span data-ttu-id="e9d88-120">**Apskaita**</span><span class="sxs-lookup"><span data-stu-id="e9d88-120">**Accounting**</span></span>|<span data-ttu-id="e9d88-121">Apskaitos prižiūrėtojas</span><span class="sxs-lookup"><span data-stu-id="e9d88-121">Accounting supervisor</span></span>|<span data-ttu-id="e9d88-122">Apskaitos vadovas</span><span class="sxs-lookup"><span data-stu-id="e9d88-122">Accounting manager</span></span>|
|<span data-ttu-id="e9d88-123">**Apskaita**</span><span class="sxs-lookup"><span data-stu-id="e9d88-123">**Accounting**</span></span>|<span data-ttu-id="e9d88-124">A-apskaita</span><span class="sxs-lookup"><span data-stu-id="e9d88-124">Accounting-A</span></span>|<span data-ttu-id="e9d88-125">Buhalteris</span><span class="sxs-lookup"><span data-stu-id="e9d88-125">Accountant</span></span>|
|<span data-ttu-id="e9d88-126">**Personalas**</span><span class="sxs-lookup"><span data-stu-id="e9d88-126">**Human resources**</span></span>|<span data-ttu-id="e9d88-127">Personalo vadovas (rytų regionas)</span><span class="sxs-lookup"><span data-stu-id="e9d88-127">HR manager (East)</span></span>|<span data-ttu-id="e9d88-128">Personalo vadovas</span><span class="sxs-lookup"><span data-stu-id="e9d88-128">HR manager</span></span>|
|<span data-ttu-id="e9d88-129">**Personalas**</span><span class="sxs-lookup"><span data-stu-id="e9d88-129">**Human resources**</span></span>|<span data-ttu-id="e9d88-130">Personalo vadovas (vakarų regionas)</span><span class="sxs-lookup"><span data-stu-id="e9d88-130">HR manager (West)</span></span>|<span data-ttu-id="e9d88-131">Personalo vadovas</span><span class="sxs-lookup"><span data-stu-id="e9d88-131">HR manager</span></span>|
|<span data-ttu-id="e9d88-132">**Personalas**</span><span class="sxs-lookup"><span data-stu-id="e9d88-132">**Human resources**</span></span>|<span data-ttu-id="e9d88-133">Personalo vadovas (centrinis regionas)</span><span class="sxs-lookup"><span data-stu-id="e9d88-133">HR manager (Central)</span></span>|<span data-ttu-id="e9d88-134">Personalo vadovas</span><span class="sxs-lookup"><span data-stu-id="e9d88-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="e9d88-135">Padaliniai</span><span class="sxs-lookup"><span data-stu-id="e9d88-135">Departments</span></span>
------------

<span data-ttu-id="e9d88-136">Padalinys yra valdymo vienetas, atitinkantis organizacijos kategoriją arba funkcinę sritį, skirtą tam tikrai organizacijos veiklos sričiai, pvz., pardavimui arba apskaitai, valdyti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="e9d88-137">Padalinys naudojamas informuoti apie funkcines sritis ir jam gali būti priskirta pelno ir nuostolio atsakomybė.</span><span class="sxs-lookup"><span data-stu-id="e9d88-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="e9d88-138">Be to, padalinyje gali būti išlaidų centrų grupė.</span><span class="sxs-lookup"><span data-stu-id="e9d88-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="e9d88-139">Pardavimo, apskaitos ir personalo valdymo skyriai galėtų būti vieni iš organizacijos padalinių pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="e9d88-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="e9d88-140"> Užduotys ir pareigos</span><span class="sxs-lookup"><span data-stu-id="e9d88-140">Jobs and positions</span></span>
<span data-ttu-id="e9d88-141">Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="e9d88-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="e9d88-142">Pozicija yra individualus užduoties egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="e9d88-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="e9d88-143">Užduočiai atlikti būtinos atsakomybės ribos, darbo užduotys, užduočių funkcijos, įgūdžiai, išsilavinimo informacija taip pat būtini pareigoms, susijusioms su ta užduotimi, eiti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="e9d88-144">Darbo užduotys</span><span class="sxs-lookup"><span data-stu-id="e9d88-144">Job tasks</span></span>

<span data-ttu-id="e9d88-145">Galite sukurti darbo užduotis, apibūdinančias pagrindines užduotis, kurias atitinkamoms pareigoms priskirtas darbuotojas turi atlikti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="e9d88-146">Tą pačią darbo užduotį galima įtraukti į kelias užduotis ir su šiomis užduotimis susijusios pareigos bus papildytos šiomis darbo užduotimis.</span><span class="sxs-lookup"><span data-stu-id="e9d88-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="e9d88-147">Šioje lentelėje pateikta keletas darbo užduočių pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="e9d88-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9d88-148">Užduotis</span><span class="sxs-lookup"><span data-stu-id="e9d88-148">Job</span></span></th>
<th><span data-ttu-id="e9d88-149">Darbo užduotis</span><span class="sxs-lookup"><span data-stu-id="e9d88-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9d88-150">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="e9d88-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="e9d88-151"><span class="input">Efektyvumo peržiūros</span> – peržiūrėti kiekvieno pardavėjo darbo efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="e9d88-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="e9d88-152"><span class="input">Neatvykimų apžvalga</span> – patvirtinti arba atmesti kiekvieno pardavėjo prašymus leisti neatvykti arba registracijas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9d88-153">Buhalteris</span><span class="sxs-lookup"><span data-stu-id="e9d88-153">Accountant</span></span></td>
<td><span data-ttu-id="e9d88-154"><span class="input">Finansinės ataskaitos</span> – pateikti savaitės finansines ataskaitas vyriausiajam finansininkui.</span><span class="sxs-lookup"><span data-stu-id="e9d88-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="e9d88-155">Užduoties funkcijos</span><span class="sxs-lookup"><span data-stu-id="e9d88-155">Job functions</span></span>

<span data-ttu-id="e9d88-156">Užduoties funkcijos panašios į darbo užduotis.</span><span class="sxs-lookup"><span data-stu-id="e9d88-156">Job functions are like job tasks.</span></span> <span data-ttu-id="e9d88-157">Užduoties funkcija apibūdina vieną ar daugiau užduočių, pareigų ar įsipareigojimų, priskirtų užduočiai.</span><span class="sxs-lookup"><span data-stu-id="e9d88-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="e9d88-158">Užduočių funkcijos gali būti priskiriamos užduotims ir naudojamos atlyginimo planų tinkamumo taisyklėms nustatyti ir įgyvendinti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="e9d88-159">Šioje lentelėje pateikta keletas užduočių funkcijų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="e9d88-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="e9d88-160">Užduotis</span><span class="sxs-lookup"><span data-stu-id="e9d88-160">Job</span></span>           | <span data-ttu-id="e9d88-161">Užduoties funkcija</span><span class="sxs-lookup"><span data-stu-id="e9d88-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="e9d88-162">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="e9d88-162">Sales manager</span></span> | <span data-ttu-id="e9d88-163">Žmonių valdymas – valdyti žmones, kurie jums teikia ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="e9d88-164">Buhalteris</span><span class="sxs-lookup"><span data-stu-id="e9d88-164">Accountant</span></span>    | <span data-ttu-id="e9d88-165">Finansinės informacijos peržiūra – tvarkyti sąskaitų rinkinio finansinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="e9d88-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="e9d88-166">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="e9d88-166">Job types</span></span>

<span data-ttu-id="e9d88-167">Užduočių tipai naudojami panašiems darbams klasifikuoti į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="e9d88-168">Kaip ir užduočių funkcijos, užduočių tipai gali būti priskiriami užduotims ir naudojami atlyginimo planų tinkamumo taisyklėms nustatyti ir įgyvendinti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="e9d88-169">Toliau pateiktame sąraše pateikti keli užduočių tipų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="e9d88-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="e9d88-170">Visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="e9d88-170">Full-time</span></span>
-   <span data-ttu-id="e9d88-171">Ne visą darbo dieną</span><span class="sxs-lookup"><span data-stu-id="e9d88-171">Part-time</span></span>
-   <span data-ttu-id="e9d88-172">Atlyginimas</span><span class="sxs-lookup"><span data-stu-id="e9d88-172">Salary</span></span>
-   <span data-ttu-id="e9d88-173">Valandinis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="e9d88-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="e9d88-174">Atsakomybės ribos</span><span class="sxs-lookup"><span data-stu-id="e9d88-174">Areas of responsibility</span></span>

<span data-ttu-id="e9d88-175">Atsakomybės ribos naudojamos užduotį atliekančio darbuotojo darbo vaidmenims, procesams ir produktams, už kuriuos jis yra atsakingas, apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="e9d88-176">Pvz., buhalterio atsakomybės ribos gali būti apibrėžtos kaip „Produkto A finansinės ataskaitos“.</span><span class="sxs-lookup"><span data-stu-id="e9d88-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="e9d88-177">Pareigybės</span><span class="sxs-lookup"><span data-stu-id="e9d88-177">Positions</span></span>
----------

<span data-ttu-id="e9d88-178">Pareigos yra svarbus žemesniojo organizacijos hierarchijos lygio elementas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="e9d88-179">Pozicija yra individualus užduoties egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="e9d88-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="e9d88-180">Pvz., pareigos „Pardavimo vadybininkas (rytų regionas)“ yra tik vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“.</span><span class="sxs-lookup"><span data-stu-id="e9d88-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="e9d88-181">Pareigos atitinka padalinį ir yra priskiriamos darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="e9d88-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="e9d88-182">Pareigų kūrimas ir priežiūra</span><span class="sxs-lookup"><span data-stu-id="e9d88-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="e9d88-183">Lengvai pasiekiamame sąrašo puslapyje galite peržiūrėti su pareigomis susijusių sistemos pakeitimų retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="e9d88-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="e9d88-184">Galite sukurti priežasčių kodus, kuriuos kurdami ir modifikuodami pareigas galės pasirinkti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="e9d88-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="e9d88-185">Galite sukurti personalo veiksmų tipus ir priskirti jiems numeraciją.</span><span class="sxs-lookup"><span data-stu-id="e9d88-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="e9d88-186">Galite nustatyti darbo eigą taip, kad naujoms pareigoms įtraukti ir esamoms keisti būtų reikalingas patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="e9d88-187">Pareigų trukmė</span><span class="sxs-lookup"><span data-stu-id="e9d88-187">Position duration</span></span>

<span data-ttu-id="e9d88-188">Kiekvienoms pareigoms taikomas galiojimo laikas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="e9d88-189">Šis galiojimo laikas yra nurodytas kaip trukmė.</span><span class="sxs-lookup"><span data-stu-id="e9d88-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="e9d88-190">Pvz., vasaros pareigos gali trukti nuo 2015 m. gegužės 1 d. iki 2015 m. rugpjūčio 31 d.</span><span class="sxs-lookup"><span data-stu-id="e9d88-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="e9d88-191">Darbininkų priskyrimai</span><span class="sxs-lookup"><span data-stu-id="e9d88-191">Worker assignments</span></span>

<span data-ttu-id="e9d88-192">Kai priskiriate darbuotoją pareigoms, reiškia, kad šios pareigos jau užpildytos.</span><span class="sxs-lookup"><span data-stu-id="e9d88-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="e9d88-193">Galite priskirti darbuotojus kelioms pareigoms, tačiau vienu metu tam tikroms pareigoms galima priskirti tik vieną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="e9d88-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="e9d88-194">Ataskaitų ryšiai</span><span class="sxs-lookup"><span data-stu-id="e9d88-194">Reporting relationships</span></span>

<span data-ttu-id="e9d88-195">Pareigos yra svarbus žemesniojo organizacijos hierarchijos lygio elementas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="e9d88-196">Pareigų formoje galite nurodyti pareigų atskaitingumo ryšius.</span><span class="sxs-lookup"><span data-stu-id="e9d88-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="e9d88-197">Priskyrę darbuotoją pareigoms, kurios atskaitingos kitoms pareigoms, sukuriate atskaitingumo ryšį tarp šioms dviems pareigoms priskirtų darbuotojų.</span><span class="sxs-lookup"><span data-stu-id="e9d88-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="e9d88-198">Pvz., pareigų „Buhalteris-A“ atstovas atskaitingas pareigų „Apskaitos prižiūrėtojas“ atstovui.</span><span class="sxs-lookup"><span data-stu-id="e9d88-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="e9d88-199">Kim Akers priskirtas pareigoms „Apskaitos prižiūrėtojas“, o Sanjay Patel priskirtas pareigoms „Buhalteris-A“.</span><span class="sxs-lookup"><span data-stu-id="e9d88-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="e9d88-200">Tai reiškia, kad Sanjay Patel teikia ataskaitas Kim Akers.</span><span class="sxs-lookup"><span data-stu-id="e9d88-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="e9d88-201">Jei jūsų organizacijoje naudojama matricos hierarchija ar kita pasirinktinė hierarchija, galite nustatyti pareigų hierarchijų tipus ir įtraukti pareigų ataskaitų ryšius į kiekvieno hierarchijos tipo, kurį nustatote, pareigas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="e9d88-202">Pavyzdžiui, Lori Penor yra „Adventure Works“ generalinė direktorė ir yra priskirta pareigoms „Generalinis direktorius“.</span><span class="sxs-lookup"><span data-stu-id="e9d88-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="e9d88-203">Lori valdo produkto, skirto valymui atlikti, vystymą.</span><span class="sxs-lookup"><span data-stu-id="e9d88-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="e9d88-204">Lori reikia buhalterio, kuris galėtų padėti jai finansinėje produkto vystymo srityje.</span><span class="sxs-lookup"><span data-stu-id="e9d88-204">Lori requires an accountant to help her with the finances for developing the product.</span></span> <span data-ttu-id="e9d88-205">Todėl ji įdarbino Sanjay Patel buhalterio pareigoms užimti.</span><span class="sxs-lookup"><span data-stu-id="e9d88-205">Therefore, she has recruited Sanjay Patel to be her accountant.</span></span> <span data-ttu-id="e9d88-206">Sanjay tiesiogiai atsiskaito Kim Akers, tačiau taip pat bendradarbiauja su Lori Penor atlikdamas užduotis, susijusias su finansine produkto vystymo sritimi.</span><span class="sxs-lookup"><span data-stu-id="e9d88-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="e9d88-207">Remiantis pirmiau pateiktu pavyzdžiu, Sanjay Patel ir Lori Penor darbo santykiams nustatyti reikėtų atlikti toliau išvardytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="e9d88-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="e9d88-208">Sukurti pasirinktinį pareigų hierarchijos tipą vadinamą „Produktas“, kad būtų sukurta hierarchija, apimanti pareigas, kurių atstovai atsakingi už darbą su produktu.</span><span class="sxs-lookup"><span data-stu-id="e9d88-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="e9d88-209">Nustatyti generalinio direktoriaus pareigas kaip pareigas, kurioms Buhalteris-A yra atskaitingas Produkto hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="e9d88-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="e9d88-210">Peržiūrėti pareigų atskaitingumo struktūrą naudojant pareigų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="e9d88-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="e9d88-211">Jei naudojate keletą pareigų hierarchijų, galite peržiūrėti kiekvieno tipo hierarchiją pareigų hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="e9d88-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="e9d88-212">Taip pat galite ieškoti pareigų pagal pareigų ID arba darbuotojo, kuris yra priskirtas toms pareigoms, pavardę.</span><span class="sxs-lookup"><span data-stu-id="e9d88-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="e9d88-213">Pareigų hierarchija priklauso nuo organizacijos hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="e9d88-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="e9d88-214">Galiojančių datų įrašai</span><span class="sxs-lookup"><span data-stu-id="e9d88-214">Date effective records</span></span>
<span data-ttu-id="e9d88-215">Galite nurodyti būsimus kai kurių įrašų pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="e9d88-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="e9d88-216">Ši informacija priklauso nuo datos.</span><span class="sxs-lookup"><span data-stu-id="e9d88-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9d88-217">Įrašai</span><span class="sxs-lookup"><span data-stu-id="e9d88-217">Records</span></span></th>
<th><span data-ttu-id="e9d88-218">Nuo datos priklausanti informacija</span><span class="sxs-lookup"><span data-stu-id="e9d88-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9d88-219">Užduotys</span><span class="sxs-lookup"><span data-stu-id="e9d88-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="e9d88-220">Tam tikra išsami užduoties informacija</span><span class="sxs-lookup"><span data-stu-id="e9d88-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="e9d88-221">Užduočių klasifikacijos informacija</span><span class="sxs-lookup"><span data-stu-id="e9d88-221">Job classification information</span></span></li>
<li><span data-ttu-id="e9d88-222">Kompensacijos informacija</span><span class="sxs-lookup"><span data-stu-id="e9d88-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9d88-223">Pareigos</span><span class="sxs-lookup"><span data-stu-id="e9d88-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="e9d88-224">Tam tikra išsami pareigų informacija</span><span class="sxs-lookup"><span data-stu-id="e9d88-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="e9d88-225">Darbuotojų priskyrimai</span><span class="sxs-lookup"><span data-stu-id="e9d88-225">Worker assignments</span></span></li>
<li><span data-ttu-id="e9d88-226">Pareigų trukmė</span><span class="sxs-lookup"><span data-stu-id="e9d88-226">Position durations</span></span></li>
<li><span data-ttu-id="e9d88-227">Pareigų hierarchijos</span><span class="sxs-lookup"><span data-stu-id="e9d88-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e9d88-228">Galite keisti lentelėje pateiktą informaciją, susijusią su pareigomis ar užduotimis, ir nurodyti datą, kada įsigalios šie pareigų arba užduočių pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="e9d88-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="e9d88-229">Pvz., pareigoms gali būti priskirtas tik vienas darbuotojas, tačiau Sanjay Patel, kuris yra priskirtas buhalterio-A pareigoms, po dviejų savaičių paliks šias pareigas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="e9d88-230">Joe Healy pakeis Sanjay Patel šiam išėjus.</span><span class="sxs-lookup"><span data-stu-id="e9d88-230">Joe Healy will replace Sanjay Patel when he leaves.</span></span> <span data-ttu-id="e9d88-231">Sanjay toliau liekant priskirtam jo pareigoms, galite priskirti Joe Healy toms pačioms pareigoms, tačiau šis priskyrimas įsigalios tik po paskutinės Sanjay dienos einant šias pareigas.</span><span class="sxs-lookup"><span data-stu-id="e9d88-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>





