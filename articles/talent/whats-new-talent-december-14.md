---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. gruodžio 14 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c972c04638f436f2fd56055e83bbcf06b29a9f20
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551869"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a><span data-ttu-id="f042c-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. gruodžio 14 d.)</span><span class="sxs-lookup"><span data-stu-id="f042c-103">What's new or changed in Dynamics 365 Talent - Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f042c-104">**8.1.2085 versija**</span><span class="sxs-lookup"><span data-stu-id="f042c-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="f042c-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="f042c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="f042c-106">Pakeitimai</span><span class="sxs-lookup"><span data-stu-id="f042c-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="f042c-107">JAV – ACA (įstatymas dėl prieinamos sveikatos priežiūros) palaiko 2018 mokestinių metų 1095-B ir 1095-C formas</span><span class="sxs-lookup"><span data-stu-id="f042c-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="f042c-108">Kiekvienais metais „Applicable Large Employers“ (ALE) turi pateikti kiekvieno visą darbo dieną dirbančio darbuotojo 1095-C formą.</span><span class="sxs-lookup"><span data-stu-id="f042c-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="f042c-109">Be to, jei darbdavys teikia savarankišką draudimą, jis turi pateikti 1095-C (jei jis yra ALE) ir 1095-B (jei jis yra smulkus darbdavys) formą bet kuriam visą darbo dieną arba ne visą darbo dieną dirbančiam darbuotojui, kuriam taikomas vienas iš jo siūlomų sveikatos planų.</span><span class="sxs-lookup"><span data-stu-id="f042c-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="f042c-110">Ši funkcija numato spausdintines tiek 1095-C, tiek 1095-B formas.</span><span class="sxs-lookup"><span data-stu-id="f042c-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="f042c-111">Importuojant nepaisoma lauko SubmittedByPersonId, esančio HcmPerfJournalEntity</span><span class="sxs-lookup"><span data-stu-id="f042c-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="f042c-112">Importuojant / eksportuojant našumo žurnalo įrašus, nepaisoma lauko **Pateikė**.</span><span class="sxs-lookup"><span data-stu-id="f042c-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="f042c-113">Atlikus šį pakeitimą, vertė **importuota / eksportuota** parodys vertę lentelėje eksportuojant, kai importuojama sistema atnaujinama pagal importavimo faile pateiktą vertę.</span><span class="sxs-lookup"><span data-stu-id="f042c-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="f042c-114">Darbo srities „Atostogos ir neatvykimai“ analizės skirtuke rodoma ne sistemos administratoriaus vaidmenų klaida „OpenConnectionError“</span><span class="sxs-lookup"><span data-stu-id="f042c-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="f042c-115">Įdiegus šį naujinimą, atidarant darbo srities **Atostogos ir neatvykimai** skirtuką **Analizė** nekils jokių klaidų.</span><span class="sxs-lookup"><span data-stu-id="f042c-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="f042c-116">Darbuotojų savitarnos, pareigų hierarchijos išklotinės detalizavimui nepavyksta gauti pirminio mazgo</span><span class="sxs-lookup"><span data-stu-id="f042c-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="f042c-117">Atliktas pakeitimas siekiant ištaisyti klaidą „Nepavyko gauti pirminio mazgo“, personalizavus pareigų hierarchiją, kuri turi būti rodoma esamoje darbo srityje, ir pasirinkus pareigas hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="f042c-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="f042c-118">Reikia būti sistemos administratoriumi, norint peržiūrėti puslapyje Pareigos esantį skirtuką Algalapis</span><span class="sxs-lookup"><span data-stu-id="f042c-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="f042c-119">Atliktas pakeitimas siekiant įtraukti tinkamus saugos elementus į esamą teisę: „Tvarkyti algalapio darbuotojo ir pareigų informaciją“.</span><span class="sxs-lookup"><span data-stu-id="f042c-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="f042c-120">Atlikus šį pakeitimą, pagal numatytuosius parametrus algalapio administratorius turės prieigą prie pareigų puslapyje esančių algalapio laukų.</span><span class="sxs-lookup"><span data-stu-id="f042c-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="f042c-121">Klaida, kai vadovui pateikiama našumo rezultatų apžvalga ir pateikimo instrukcijose naudojamas vietos rezervavimo ženklas %Reviews.PerfPeriod%</span><span class="sxs-lookup"><span data-stu-id="f042c-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="f042c-122">Atliktas pakeitimas, kuris ištaiso klaidą „Nulinė nuoroda“, kai pateikimo instrukcijose naudojamas vietos rezervavimo ženklas %Reviews.PerfPeriod%.</span><span class="sxs-lookup"><span data-stu-id="f042c-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="f042c-123">Darbo jėgos „Power BI“ ataskaitoje rodoma klaida, kai darbuotojo paaukštinimo data yra keliamoji diena</span><span class="sxs-lookup"><span data-stu-id="f042c-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="f042c-124">Atlikus šį pakeitimą, keliamosios dienos dabar palaikomos „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="f042c-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="f042c-125">Integravimas tarp „Core HR“ ir „Attract“</span><span class="sxs-lookup"><span data-stu-id="f042c-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="f042c-126">Atliktas pakeitimas siekiant atnaujinti su samdytinais kandidatais susijusį integravimą tarp „Core HR“ ir „Attract“.</span><span class="sxs-lookup"><span data-stu-id="f042c-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="f042c-127">Kad samdytini kandidatai būtų matomi darbo srityje **Personalo valdymas**, naudojami šie „Common Data Service“ objektai.</span><span class="sxs-lookup"><span data-stu-id="f042c-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="f042c-128">Prašymas įdarbinti</span><span class="sxs-lookup"><span data-stu-id="f042c-128">Job Application</span></span>
- <span data-ttu-id="f042c-129">Būsenos tipas turi būti nustatytas kaip Pasiūlymas priimtas</span><span class="sxs-lookup"><span data-stu-id="f042c-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="f042c-130">Pateikiamas kandidatas ir laisva darbo vieta</span><span class="sxs-lookup"><span data-stu-id="f042c-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="f042c-131">Pretendentas</span><span class="sxs-lookup"><span data-stu-id="f042c-131">Candidate</span></span>
-   <span data-ttu-id="f042c-132">Pateikiama kandidato informacija</span><span class="sxs-lookup"><span data-stu-id="f042c-132">Provides Candidate information</span></span>

<span data-ttu-id="f042c-133">Laisva darbo vieta</span><span class="sxs-lookup"><span data-stu-id="f042c-133">Job Opening</span></span>
-   <span data-ttu-id="f042c-134">Pateikiamas laisvos darbo vietos skelbimo ID ir laisvos darbo vietos dalyviai</span><span class="sxs-lookup"><span data-stu-id="f042c-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="f042c-135">Laisvos darbo vietos dalyviai</span><span class="sxs-lookup"><span data-stu-id="f042c-135">Job Opening Participants</span></span>
-   <span data-ttu-id="f042c-136">Pateikiamas samdos vadovas</span><span class="sxs-lookup"><span data-stu-id="f042c-136">Provides Hiring Manager</span></span>

<span data-ttu-id="f042c-137">Kandidatą įtraukus į personalo valdymą, jo dabar taip pat galima atsisakyti naudojant naują kandidato kortelėje esančią parinktį.</span><span class="sxs-lookup"><span data-stu-id="f042c-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f042c-138">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="f042c-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="f042c-139">Atostogos ir neatvykimai: būsimų atostogų ir prognozuojamų atostogų balansai</span><span class="sxs-lookup"><span data-stu-id="f042c-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="f042c-140">Atlikus pakeitimus tam, kad darbuotojai galėtų prognozuoti ne darbo laiką ir teikti būsimo ne darbo laiko prašymus, taip pat keičiasi būdas, kaip bus rodomi ne darbo laiko balansai, nepaveikiant jų dabartinio ne darbo laiko balansų.</span><span class="sxs-lookup"><span data-stu-id="f042c-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="f042c-141">Šiuo metu rodomas turimas balansas yra prašymams teikti galima ne darbo laiko suma, įskaitant šios dienos kaupimus ir visus patvirtintus atostogų prašymus iki laiko pabaigos.</span><span class="sxs-lookup"><span data-stu-id="f042c-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="f042c-142">Pateikus galimybę prognozuoti, rodomas balansas bus toks, koks bus dabartinis ne darbo laiko balansas, įskaitant šios dienos kaupimus ir šios dienos prašymus.</span><span class="sxs-lookup"><span data-stu-id="f042c-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="f042c-143">Darbuotojai ir vadovai šiuos atnaujintus balansus matys darbuotojo ir vadovo savitarnos kortelėje **Ne darbo laikas** ir lange **Ne darbo laiko balansai**.</span><span class="sxs-lookup"><span data-stu-id="f042c-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="f042c-144">Personalo vadovai šiuos atnaujintus balansus matys darbo srityje **Žmonės** ir darbuotojo lange **Priskirti atostogų planai**.</span><span class="sxs-lookup"><span data-stu-id="f042c-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="f042c-145">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="f042c-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance"></a><span data-ttu-id="f042c-146">Susiejimo klaidos integruojant su „Finance“</span><span class="sxs-lookup"><span data-stu-id="f042c-146">Mapping errors in the integration with Finance</span></span>

<span data-ttu-id="f042c-147">Dabartiniame „Talent“ integravimo su „Dynamics 365 Finance“ šablone buvo nustatytos toliau nurodytos problemos.</span><span class="sxs-lookup"><span data-stu-id="f042c-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 Finance.</span></span> <span data-ttu-id="f042c-148">Netrukus bus paskelbtas naujas šablonas, kurį bus galima taikyti visiems naujai sukurtiems integravimo projektams.</span><span class="sxs-lookup"><span data-stu-id="f042c-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="f042c-149">Esamiems integravimo projektams užduočių susiejimai gali būti atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="f042c-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="f042c-150">Atnaujintų susiejimų žr. toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="f042c-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="f042c-151">Neintegruojami pareigų, skirtų pareigų pirminės užduoties priskyrimui, užduoties duomenys.</span><span class="sxs-lookup"><span data-stu-id="f042c-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="f042c-152">Ši problema šiuo metu sprendžiama.</span><span class="sxs-lookup"><span data-stu-id="f042c-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="f042c-153">Nėra dabartinio susiejimo problemos sprendimo būdo.</span><span class="sxs-lookup"><span data-stu-id="f042c-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="f042c-154">Padalinių, skirtų valdymo vienetui, užduočiai reikia atnaujinti šiuos susiejimus.</span><span class="sxs-lookup"><span data-stu-id="f042c-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="f042c-155">Esamas šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-155">Existing source field</span></span>          | <span data-ttu-id="f042c-156">Naujas šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="f042c-157">cdm_description (aprašas)</span><span class="sxs-lookup"><span data-stu-id="f042c-157">cdm_description (Description)</span></span>  | <span data-ttu-id="f042c-158">cdm_name (pavadinimas)</span><span class="sxs-lookup"><span data-stu-id="f042c-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="f042c-159">Taip pat reikia įtraukti papildomą susiejimą.</span><span class="sxs-lookup"><span data-stu-id="f042c-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="f042c-160">Norėdami įtraukti šį susiejimą, pasirinkite paskutinį lauką **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="f042c-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="f042c-161">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-161">Source field</span></span>                   | <span data-ttu-id="f042c-162">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="f042c-163">cdm_description (aprašas)</span><span class="sxs-lookup"><span data-stu-id="f042c-163">cdm_description (Description)</span></span>  | <span data-ttu-id="f042c-164">NAMEALIAS (PAVADINIMO PSEUDONIMAS)</span><span class="sxs-lookup"><span data-stu-id="f042c-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="f042c-165">Atnaujinti susiejimai turėtų atrodyti taip, kaip toliau parodytame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="f042c-165">The updated mappings should look like the following image.</span></span>

![Padalinių, skirtų valdymo vienetams, užduotis](./media/DepartmentMapping.png)


<span data-ttu-id="f042c-167">Pareigų, skirtų pareigų informacijai, užduočiai reikia atnaujinti šiuos susiejimus.</span><span class="sxs-lookup"><span data-stu-id="f042c-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="f042c-168">Esamas šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-168">Existing source field</span></span>          | <span data-ttu-id="f042c-169">Naujas šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="f042c-170">cdm_name (pavadinimas)</span><span class="sxs-lookup"><span data-stu-id="f042c-170">cdm_name (Name)</span></span>                | <span data-ttu-id="f042c-171">cdm_description (aprašas)</span><span class="sxs-lookup"><span data-stu-id="f042c-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="f042c-172">cdm_name (aprašas)</span><span class="sxs-lookup"><span data-stu-id="f042c-172">cdm_name (Description)</span></span>         | <span data-ttu-id="f042c-173">cdm_jobdescription (užduoties aprašas)</span><span class="sxs-lookup"><span data-stu-id="f042c-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="f042c-174">Atnaujinti susiejimai turėtų atrodyti taip, kaip žemiau parodytame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="f042c-174">The updated mappings should look like the image below.</span></span>

![Pareigų, skirtų pareigų informacijai, užduotis](./media/JobMapping.png)

<span data-ttu-id="f042c-176">Darbuotojų, skirtų darbui, užduočiai reikia atnaujinti šiuos susiejimus.</span><span class="sxs-lookup"><span data-stu-id="f042c-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="f042c-177">Esamas šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-177">Existing source field</span></span>                 | <span data-ttu-id="f042c-178">Naujas šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="f042c-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="f042c-179">cdm_emailaddress1 (1 el. pašto adresas)</span><span class="sxs-lookup"><span data-stu-id="f042c-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="f042c-180">cdm_primaryemailaddress (pagrindinis el. pašto adresas)</span><span class="sxs-lookup"><span data-stu-id="f042c-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="f042c-181">cdm_telephone1 (1 telefonas)</span><span class="sxs-lookup"><span data-stu-id="f042c-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="f042c-182">cdm_primarytelephone (pagrindinis telefonas)</span><span class="sxs-lookup"><span data-stu-id="f042c-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="f042c-183">Taip pat reikia atnaujinti lyties lauko transformaciją.</span><span class="sxs-lookup"><span data-stu-id="f042c-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="f042c-184">Pasirinkite lyties susiejimo tipą **fn** (funkcija) ir atnaujinkite šiuos vertės susiejimus.</span><span class="sxs-lookup"><span data-stu-id="f042c-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="f042c-185">„Common Data Service“ vertė</span><span class="sxs-lookup"><span data-stu-id="f042c-185">Common Data Service value</span></span>                   | <span data-ttu-id="f042c-186">„Finance and Operations“ vertė</span><span class="sxs-lookup"><span data-stu-id="f042c-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="f042c-187">75440000</span><span class="sxs-lookup"><span data-stu-id="f042c-187">75440000</span></span>                    | <span data-ttu-id="f042c-188">Vyras</span><span class="sxs-lookup"><span data-stu-id="f042c-188">Male</span></span>                                             |
| <span data-ttu-id="f042c-189">75440001</span><span class="sxs-lookup"><span data-stu-id="f042c-189">75440001</span></span>                    | <span data-ttu-id="f042c-190">Moteris</span><span class="sxs-lookup"><span data-stu-id="f042c-190">Female</span></span>                                           |
| <span data-ttu-id="f042c-191">75440002</span><span class="sxs-lookup"><span data-stu-id="f042c-191">75440002</span></span>                    | <span data-ttu-id="f042c-192">Joks</span><span class="sxs-lookup"><span data-stu-id="f042c-192">None</span></span>                                             | 
| <span data-ttu-id="f042c-193">75440003</span><span class="sxs-lookup"><span data-stu-id="f042c-193">75440003</span></span>                    | <span data-ttu-id="f042c-194">Neapibrėžta</span><span class="sxs-lookup"><span data-stu-id="f042c-194">NonSpecific</span></span>                                      |

<span data-ttu-id="f042c-195">Atnaujinti susiejimai turėtų atrodyti taip, kaip toliau parodytuose paveikslėliuose.</span><span class="sxs-lookup"><span data-stu-id="f042c-195">The updated mappings should look like the following images.</span></span>

![Darbuotojų, skirtų darbuotojui, užduotis](./media/WorkerMapping.png)

![Lyties lauko transformacija](./media/WorkerTransform.png)
