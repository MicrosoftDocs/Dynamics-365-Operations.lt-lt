---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. rugsėjo 16 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. rugsėjo 16 d.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b07bfb27bbe5e546dac9d72666b3225cc202670
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890704"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="c8f5c-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. rugsėjo 16 d.)</span><span class="sxs-lookup"><span data-stu-id="c8f5c-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c8f5c-104">Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c8f5c-105">Pakeitimai taikomi 8.1.3557 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="c8f5c-106">Prie kai kurių funkcijų esantys skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="c8f5c-107">Kas yra įtraukta į šį leidimą?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-107">Included in this release</span></span>

-  [<span data-ttu-id="c8f5c-108">Įrašyti rodiniai – bendras pasiekiamumas</span><span class="sxs-lookup"><span data-stu-id="c8f5c-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="c8f5c-109">- Norėdami gauti išsamesnės informacijos, žr.: [Įrašytos peržiūros](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="c8f5c-110">Formoje **Pareigų veiksmai** yra atnaujintas dimensijų tinklelis ir naujas dialogas (469495).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="c8f5c-111">Jeigu nustatote **Riboti prieigą prie darbuotojo informacijos** į taip **Išplėstinė prieiga** srityje **Personalo bendri parametrai**, dabar išmokos formose rodomi tik atitinkami darbuotojai (393384).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="c8f5c-112">Naujo kalendoriaus sukūrimo parinktys **Darbo kalendoriaus** objekte (477055):</span><span class="sxs-lookup"><span data-stu-id="c8f5c-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="c8f5c-113">- Numatytasis pabaigos laikas</span><span class="sxs-lookup"><span data-stu-id="c8f5c-113">- Default ending time</span></span><br><span data-ttu-id="c8f5c-114">- Numatytasis pradžios laikas</span><span class="sxs-lookup"><span data-stu-id="c8f5c-114">-    Default starting time</span></span><br><span data-ttu-id="c8f5c-115">- Ar penktadienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-115">-  Is Friday working day</span></span><br><span data-ttu-id="c8f5c-116">- Ar pirmadienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-116">-  Is Monday working day</span></span><br><span data-ttu-id="c8f5c-117">- Ar šeštadienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-117">-  Is Saturday working day</span></span><br><span data-ttu-id="c8f5c-118">- Ar sekmadienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-118">- Is Sunday working day</span></span><br><span data-ttu-id="c8f5c-119">- Ar ketvirtadienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-119">- Is Thursday working day</span></span><br><span data-ttu-id="c8f5c-120">- Ar antradienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-120">- Is Tuesday working day</span></span><br><span data-ttu-id="c8f5c-121">- Ar trečiadienis yra darbo diena?</span><span class="sxs-lookup"><span data-stu-id="c8f5c-121">- Is Wednesday working day</span></span><br><span data-ttu-id="c8f5c-122">- Darbo kalendoriaus atostogų ID</span><span class="sxs-lookup"><span data-stu-id="c8f5c-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="c8f5c-123">Objekte **LeaveBankTransactionV1** dabar yra priežasties kodas (477823).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="c8f5c-124">Dabar galite įrašyti užduočių įrašus (492923).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="c8f5c-125">Dabar duomenys sėkmingai publikuojami iš **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="c8f5c-126">„FastTab” skirtuke **Kompensacija** dabar rodomi rangovo darbuotojų tipui formoje **Darbuotojo veiksmai** (482494).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="c8f5c-127">Laukai **Lygis** ir **Planas** dabar yra privalomi, jei nustatysite **Pastoviąją atlyginimo dalį**.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="c8f5c-128">Parodomas klaidos pranešimas, jei paliekate šiuos laukus tuščius (482497).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="c8f5c-129">Laukas **Plano tipas**, esantis skyriuje **Išmokos** dabar yra išplečiamasis sąrašas (488768).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="c8f5c-130">Sistemos administratoriai dabar gauna pranešimą, jei pasirinktas laukas yra panaikintas iš žmogiškųjų išteklių (481408).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="c8f5c-131">Nutraukus darbuotojų procesą, personalas elgiasi taip, kaip tikėtasi, o po to, kai ji rodoma užrakinti (479877), nepasikeičia pasirinktoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="c8f5c-132">Vadovai nebegali pridėti numerio stulpelio per personalizavimą (485317).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="c8f5c-133">Vadovai nebegali pašalinti duomenų diapazono filtro iš identifikacijos numerių, kurių galiojimo laikas baigiasi (485321).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="c8f5c-134">Kai laukas **Ataskaitos į** yra tuščias, pareigų išsami informacija vis dar rodoma, kai pelės žymeklis užvedamas ant pareigų (433328).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="c8f5c-135">Darbuotojai dabar gali peržiūrėti išmokų plano informaciją darbuotojų savitarnos tarnyboje (481676).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="c8f5c-136">Dabar darbuotojai gali matyti visus užregistruotus kursus (429048).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="c8f5c-137">Dabar galite apriboti peržiūros parinktis **Profesionalių sertifikatų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="c8f5c-138">Galite apriboti peržiūros parinktis dabartiniame juridiniame subjekte pagal darbuotojo būseną ir pagal darbuotojo tipą (451501).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="c8f5c-139">Peržiūroje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="c8f5c-140">„Human Resources“ programa „Teams“</span><span class="sxs-lookup"><span data-stu-id="c8f5c-140">Human Resources app in Teams</span></span>

<span data-ttu-id="c8f5c-141">Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="c8f5c-142">Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="c8f5c-143">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="c8f5c-143">For more information, see:</span></span>

- <span data-ttu-id="c8f5c-144">[Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 1 plane</span><span class="sxs-lookup"><span data-stu-id="c8f5c-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="c8f5c-145">[„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md) „Human Resources” dokumentacijoje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="c8f5c-146">„Human Resources“ programėlė „Teams“ peržiūros funkcijose</span><span class="sxs-lookup"><span data-stu-id="c8f5c-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="c8f5c-147">**Pranešimai**: ne darbo laiko užklausų pateikėjai ir tvirtintojai bus informuojami „Teams” esančioje „Human Resources” programėlėje.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="c8f5c-148">Tvirtintojai gali patvirtinti arba atmesti prašymus išleisti iš darbo.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="c8f5c-149">Pateikėjams bus pranešta, ar užklausa buvo patvirtinta, ar atmesta.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="c8f5c-150">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="c8f5c-150">For more information, see:</span></span>
   - <span data-ttu-id="c8f5c-151">[Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 2 plane</span><span class="sxs-lookup"><span data-stu-id="c8f5c-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="c8f5c-152">[„Human Resources“ programos „Teams“ pranešimų įjungimas](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) „Human Resources” dokumentacijoje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="c8f5c-153">[„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) „Human Resources” dokumentacijoje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="c8f5c-154">[„Teams” pranešimai](./hr-teams-leave-app.md#respond-to-teams-notifications) „Human Resources” dokumentacijoje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="c8f5c-155">[Jūsų komandos atostogų kalendoriaus peržiūra](./hr-teams-leave-app.md#view-your-teams-leave-calendar) „Human Resources” dokumentacijoje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="c8f5c-156">**Vadovo ne darbo laiko kalendorius**: Vadovai gali peržiūrėti savo tiesioginių ataskaitų kalendoriaus rodinyje patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="c8f5c-157">Šis rodinys leidžia lengvai suprasti, kada jų komandos nariai nėra darbe.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="c8f5c-158">Daugiau informacijos, žr.:</span><span class="sxs-lookup"><span data-stu-id="c8f5c-158">For more information, see:</span></span>
   - <span data-ttu-id="c8f5c-159">[Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 2 plane</span><span class="sxs-lookup"><span data-stu-id="c8f5c-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="c8f5c-160">[Jūsų komandos atostogų kalendoriaus peržiūra](./hr-teams-leave-app.md#view-your-teams-leave-calendar) „Human Resources” dokumentacijoje</span><span class="sxs-lookup"><span data-stu-id="c8f5c-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="c8f5c-161">Konfigūracijos pasirinktis, skirta sąrašui Man priskirti darbo elementai perkelti (477004)</span><span class="sxs-lookup"><span data-stu-id="c8f5c-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="c8f5c-162">Nauja parinktis dabar galima norint perkelti sąrašą **Man priskirti darbo elementai** į ataskaitų srities dešinėje pusėje esantį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="c8f5c-163">Dėl šio pakeitimo visi darbo elementai ir darbo sąrašai rodomi toje pačioje srityje.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="c8f5c-164">Įgalinkite šią funkciją, įjungdami **Peržiūra – darbo eigos patobulinimai** funkcijų valdyme.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="c8f5c-165">Daugiau informacijos apie peržiūros funkcijas, žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="c8f5c-166">Ši funkcija taip pat skatina darbo eigos pasirinktis, kurios rodomos personalo veiksmų formose.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="c8f5c-167">Darbo eigos parinktys taip pat rodomos virš veiksmų „FastTab“, skirto sparčiajai prieigai.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="c8f5c-168">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="c8f5c-168">For more information, see:</span></span> 

- <span data-ttu-id="c8f5c-169">[Organizacijos ir personalo valdymo darbo eigos patobulinimai](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) „Dynamics 365“ 2020 m. leidimo 2 bangos plane</span><span class="sxs-lookup"><span data-stu-id="c8f5c-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Man priskirti darbo elementai](./media/hr-workflow-work-items-assigned-to-me.png)

![Darbo eigos elementų sparčioji prieiga](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="c8f5c-172">Atostogų ir neatvykimų kalendorius</span><span class="sxs-lookup"><span data-stu-id="c8f5c-172">Leave and absence calendar</span></span>

<span data-ttu-id="c8f5c-173">Šis leidimas apima papildomas kalendoriaus pasirinktis, skirtas atostogų ir neatvykimų kalendoriams.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="c8f5c-174">Daugiau informacijos žr. [Komandos ir įmonės kalendorių peržiūra](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="c8f5c-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c8f5c-175">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="c8f5c-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="c8f5c-176">Kontrolinio sąrašo objektai, nurodyti „Dataverse”</span><span class="sxs-lookup"><span data-stu-id="c8f5c-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="c8f5c-177">Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="c8f5c-178">Išmokų valdymo priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="c8f5c-178">Benefits management reason codes</span></span>

<span data-ttu-id="c8f5c-179">Išmokų valdymo priežasčių kodai netrukus bus sujungti su esamais „Human Resources” priežasčių kodais.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="c8f5c-180">Jei išmokų valdyme sukūrėte priežasčių kodų, kurie sudaryti iš daugiau nei 15 simbolių, turite pakeisti priežasties kodo pavadinimą išmokų valdymo formoje **Priežasčių kodai**, kad jį sudarytų 15 ar mažiau simbolių.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="c8f5c-181">Atnaujinus pavadinimą, priežasties kodas atsiras esamoje priežasties kodo formoje personalo valdyme.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="c8f5c-182">Šis pakeitimas bus prieinamas ateityje ir neturės įtakos jau esamoms funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8f5c-183">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="c8f5c-183">See also</span></span>

[<span data-ttu-id="c8f5c-184">Kas nauja ar pasikeitė „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="c8f5c-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c8f5c-185">„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga</span><span class="sxs-lookup"><span data-stu-id="c8f5c-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c8f5c-186">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="c8f5c-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c8f5c-187">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="c8f5c-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
