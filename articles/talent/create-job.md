---
title: "Užduoties komponentų nustatymas"
description: "Šioje temoje aprašomi abstraktūs elementai, kurie gali sudaryti užduotį, ir pateikiami pavyzdžiai, kaip tuos elementus galite naudoti savo organizacijoje."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: a5fa86bace459d694ab0a2ec289e11b0e4420932
ms.openlocfilehash: c616637922e617661482875d78531ea79fda4407
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="48b00-103">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="48b00-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="48b00-104">Šioje temoje aprašomi abstraktūs elementai, kurie gali sudaryti užduotį, ir pateikiami pavyzdžiai, kaip tuos elementus galite naudoti savo organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="48b00-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="48b00-105">Prieš kurdami užduotis turite nustatyti tam tikrą nuorodos informaciją.</span><span class="sxs-lookup"><span data-stu-id="48b00-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="48b00-106">Galite kurti užduotį, kuri turi tik pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="48b00-106">You can create a job that has only a name.</span></span> <span data-ttu-id="48b00-107">Tačiau įtraukdami papildomą informaciją, pvz., pareigas, turite pateikti numatytąsias užduočiai priskirtų pareigų vertes.</span><span class="sxs-lookup"><span data-stu-id="48b00-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="48b00-108">Be to, kai kurią informaciją, kurią įvedate, galima naudoti kompensavimo planams į konkrečias užduotis filtruoti.</span><span class="sxs-lookup"><span data-stu-id="48b00-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="48b00-109">Jei norite nustatyti tinkamumą, kurį galite naudoti kompensavimo planams į konkrečią užduotį filtruoti, prieš nustatydami užduotis turite nustatyti užduočių funkcijas ir tipus.</span><span class="sxs-lookup"><span data-stu-id="48b00-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="48b00-110">Nustatę šias numatytąsias reikšmes sutaupysite laiko, kai užduotį įtraukiate pareigas.</span><span class="sxs-lookup"><span data-stu-id="48b00-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="48b00-111">Kai kuri užduoties informacija, pvz., pareigos, tipas ir funkcija, turi galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="48b00-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="48b00-112">Jei šiandien sukuriate užduotį, bet šios informacijos iš karto neįtraukiate, o tada peržiūrite užduotį jos sukūrimo dieną, ši informacija nebus rodoma.</span><span class="sxs-lookup"><span data-stu-id="48b00-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="48b00-113">Todėl turėtumėte sukurti dalį šios nuorodos informacijos, nes jos gali prireikti vėliau.</span><span class="sxs-lookup"><span data-stu-id="48b00-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="48b00-114">Tokiu būdu informaciją galite įtraukti į naujas užduotis tada, kai jas kuriate.</span><span class="sxs-lookup"><span data-stu-id="48b00-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="48b00-115">Pareigos</span><span class="sxs-lookup"><span data-stu-id="48b00-115">Job titles</span></span>
<span data-ttu-id="48b00-116">Tam, kad galėtumėte kurti darbo vietas, turite nustatyti tų darbo vietų pareigas.</span><span class="sxs-lookup"><span data-stu-id="48b00-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="48b00-117">Pareigoms suteikiami darbo vietų, su kuriomis tos pareigos susietos, pareigų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="48b00-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="48b00-118">Tvarkykite pareigas puslapyje **Pareigos**, kurį galite atidaryti naudodami ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="48b00-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="48b00-119">Puslapyje **Pareigos** įveskite pareigas, kurias planuojate priskirti užduotims.</span><span class="sxs-lookup"><span data-stu-id="48b00-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="48b00-120">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="48b00-120">Job types</span></span>
<span data-ttu-id="48b00-121">Užduočių tipai naudojami panašioms užduotims į kategorijas sugrupuoti.</span><span class="sxs-lookup"><span data-stu-id="48b00-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="48b00-122">Užduočių tipai nėra būtini.</span><span class="sxs-lookup"><span data-stu-id="48b00-122">Job types aren't required.</span></span> <span data-ttu-id="48b00-123">Tačiau jei užduočių tipus planuojate naudoti nustatydami kompensavimo valdymo tinkamumo taisykles, užduočių tipus turite nustatyti prieš nustatydami užduotis.</span><span class="sxs-lookup"><span data-stu-id="48b00-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="48b00-124">Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis.</span><span class="sxs-lookup"><span data-stu-id="48b00-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="48b00-125">Užduočių tipus galite tvarkyti puslapyje **Užduočių tipai**.</span><span class="sxs-lookup"><span data-stu-id="48b00-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="48b00-126">Puslapyje **Užduočių tipai** įveskite užduoties tipo pavadinimą ir trumpą aprašymą.</span><span class="sxs-lookup"><span data-stu-id="48b00-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="48b00-127">Lauke **Neapmokestinimo būsena** pasirinkite vieną iš toliau nurodytų parinkčių, kad nurodytumėte šio tipo užduočių Sąžiningo darbo standartų akto (FLSA) neapmokestinimo būseną.</span><span class="sxs-lookup"><span data-stu-id="48b00-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="48b00-128">**Neapmokestinama** – pagal FLSA užduočių viršvalandžiai nėra apmokestinami.</span><span class="sxs-lookup"><span data-stu-id="48b00-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="48b00-129">**Apmokestinama** – pagal FLSA užduočių viršvalandžiai yra apmokestinami.</span><span class="sxs-lookup"><span data-stu-id="48b00-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="48b00-130">**Netaikoma** – FLSA netaikomas.</span><span class="sxs-lookup"><span data-stu-id="48b00-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="48b00-131">Užduoties funkcijos</span><span class="sxs-lookup"><span data-stu-id="48b00-131">Job functions</span></span>
<span data-ttu-id="48b00-132">Užduočių funkcijos nurodo aukšto lygio funkcines kategorijas susieja aukšto lygio pareigas.</span><span class="sxs-lookup"><span data-stu-id="48b00-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="48b00-133">Užduočių funkcijos nėra būtinos.</span><span class="sxs-lookup"><span data-stu-id="48b00-133">Job functions aren't required.</span></span> <span data-ttu-id="48b00-134">Užduočių funkcijas ir užduočių tipus galite naudoti norėdami filtruoti kompensavimo planus, ieškodami konkrečių užduočių.</span><span class="sxs-lookup"><span data-stu-id="48b00-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="48b00-135">Užduočių funkcijos ir užduočių tipai susiejami su kompensavimo planais nustatant tinkamumo taisykles puslapyje **Tinkamumo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="48b00-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="48b00-136">Tada prie kompensavimo plano galite pridėti lygių, taikomų konkrečiam užduoties tipo ir užduoties funkcijos junginiui, kurį apibrėžėte naudodami tinkamumo taisyklę, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="48b00-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="48b00-137">(Šios funkcijos taikoms tiek pastoviosios atlyginimo dalies planams, tiek kintamosios atlyginimo dalies planams.) Tačiau, jei užduočių funkcijas planuojate naudoti nustatydami kompensavimo valdymo tinkamumo taisykles, užduočių funkcijas turite nustatyti prieš nustatydami užduotis.</span><span class="sxs-lookup"><span data-stu-id="48b00-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="48b00-138">Tolesnėje lentelėje pateikta keletas užduočių funkcijų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="48b00-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="48b00-139">Užduotis</span><span class="sxs-lookup"><span data-stu-id="48b00-139">Job</span></span>           | <span data-ttu-id="48b00-140">Užduoties funkcija</span><span class="sxs-lookup"><span data-stu-id="48b00-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="48b00-141">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="48b00-141">Sales manager</span></span> | <span data-ttu-id="48b00-142">Vidurinio lygio vadovas</span><span class="sxs-lookup"><span data-stu-id="48b00-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="48b00-143">Buhalteris</span><span class="sxs-lookup"><span data-stu-id="48b00-143">Accountant</span></span>    | <span data-ttu-id="48b00-144">Specialistai</span><span class="sxs-lookup"><span data-stu-id="48b00-144">Professionals</span></span>        |

<span data-ttu-id="48b00-145">Užduočių funkcijas galite tvarkyti puslapyje **Užduočių funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="48b00-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="48b00-146">Puslapyje **Užduočių funkcijos** įveskite užduoties funkcijos identifikavimo kodą ir trumpą aprašymą.</span><span class="sxs-lookup"><span data-stu-id="48b00-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="48b00-147">Darbo užduotys</span><span class="sxs-lookup"><span data-stu-id="48b00-147">Job tasks</span></span>
<span data-ttu-id="48b00-148">Darbo užduotys apibūdina pagrindines užduotis, kurias atitinkamoms pareigoms priskirtas darbuotojas turi atlikti.</span><span class="sxs-lookup"><span data-stu-id="48b00-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="48b00-149">Tą pačią darbo užduotį galima įtraukti į kelias užduotis ir užduočių, kurios naudoja tas darbo užduotis, pareigas.</span><span class="sxs-lookup"><span data-stu-id="48b00-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="48b00-150">Tolesnėje lentelėje pateikta keletas darbo užduočių pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="48b00-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48b00-151">Užduotis</span><span class="sxs-lookup"><span data-stu-id="48b00-151">Job</span></span></th>
<th><span data-ttu-id="48b00-152">Darbo užduotis</span><span class="sxs-lookup"><span data-stu-id="48b00-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48b00-153">Pardavimo vadybininkas</span><span class="sxs-lookup"><span data-stu-id="48b00-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="48b00-154"><strong>Efektyvumo apžvalga</strong> – peržiūrėti kiekvieno pardavėjo darbo efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="48b00-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="48b00-155"><strong>Neatvykimų apžvalga</strong> – patvirtinti arba atmesti kiekvieno pardavėjo prašymus leisti neatvykti arba registracijas.</span><span class="sxs-lookup"><span data-stu-id="48b00-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48b00-156">Buhalteris</span><span class="sxs-lookup"><span data-stu-id="48b00-156">Accountant</span></span></td>
<td><span data-ttu-id="48b00-157"><strong>Finansinės ataskaitos</strong> – pateikti savaitės finansines ataskaitas vyriausiajam finansininkui.</span><span class="sxs-lookup"><span data-stu-id="48b00-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="48b00-158">Darbo užduotis galite tvarkyti puslapyje **Darbo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="48b00-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="48b00-159">Puslapyje **Darbo užduotys** įveskite darbo užduoties pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="48b00-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="48b00-160">Lauke **Pastaba** galite pasirinktinai įvesti papildomą informaciją.</span><span class="sxs-lookup"><span data-stu-id="48b00-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="48b00-161">Galima naujinti konkrečios užduoties pastabas, nepakeičiant čia įvestų pastabų.</span><span class="sxs-lookup"><span data-stu-id="48b00-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="48b00-162">Atsakomybės ribos</span><span class="sxs-lookup"><span data-stu-id="48b00-162">Areas of responsibility</span></span>
<span data-ttu-id="48b00-163">Atsakomybės ribos naudojamos užduotį atliekančio darbuotojo darbo vaidmenims, procesams ir produktams, už kuriuos jis yra atsakingas, apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="48b00-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="48b00-164">Pvz., jei užduotis pavadinta „Buhalteris“, viena atsakomybės sritis gali būti apibrėžta kaip „A produkto finansinės ataskaitos“.</span><span class="sxs-lookup"><span data-stu-id="48b00-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="48b00-165">Atsakomybės sritis galite tvarkyti puslapyje **Atsakomybės sritys**, kurį galite rasti naudodami ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="48b00-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="48b00-166">Puslapyje **Atsakomybės sritys** įveskite atsakomybės pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="48b00-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="48b00-167">Lauke **Pastaba** galite pasirinktinai įvesti papildomą informaciją.</span><span class="sxs-lookup"><span data-stu-id="48b00-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="48b00-168">Galima naujinti konkrečios užduoties pastabas, nepakeičiant čia įvestų pastabų.</span><span class="sxs-lookup"><span data-stu-id="48b00-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>



