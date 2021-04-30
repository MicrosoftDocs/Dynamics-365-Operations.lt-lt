---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. rugpjūčio 20 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources“ funkcijos 2020 m. rugpjūčio 20 d.
author: andreabichsel
ms.date: 08/20/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 95ffe90795b9781408607257f3f63bf68c489b56
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891822"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="d9b66-103">Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. rugpjūčio 20 d.)</span><span class="sxs-lookup"><span data-stu-id="d9b66-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d9b66-104">Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos.</span><span class="sxs-lookup"><span data-stu-id="d9b66-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d9b66-105">Pakeitimai taikomi 8.1.3478 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="d9b66-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="d9b66-106">Kai kurių antraščių skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.</span><span class="sxs-lookup"><span data-stu-id="d9b66-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="d9b66-107">Būsimų ir laukiamų atostogų laiko informacijos rodymas kortelėms, esančioms darbo srityje Žmonės</span><span class="sxs-lookup"><span data-stu-id="d9b66-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="d9b66-108">Laukiamų ir būsimų atostogų užklausos pasirinktys dabar pasiekiamos atostogų ir neatvykimų kortelėse, esančiose darbo srityje **Žmonės**.</span><span class="sxs-lookup"><span data-stu-id="d9b66-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="d9b66-109">Asmeninis laukas nėra „Taip” pagal numatytuosius parametrus darbuotojo vaidmeniui darbuotojų savitarnoje (477106)</span><span class="sxs-lookup"><span data-stu-id="d9b66-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="d9b66-110">**Asmeninis** laukas dabar nustatomas kaip **Taip**, kai darbuotojai įtraukia naujus adresų įrašus darbuotojų savitarnos **Asmeninės informacijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d9b66-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="d9b66-111">Kandidatai samdyti „FastTab” personalo valdyme, parodo neteisingą kandidatų skaičių (470110)</span><span class="sxs-lookup"><span data-stu-id="d9b66-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="d9b66-112">**Personalo valdymo** puslapyje dabar tiksliai rodomas samdomų kandidatų skaičius.</span><span class="sxs-lookup"><span data-stu-id="d9b66-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="d9b66-113">Negalima įvesti ligos, skirtos atleistam darbuotojui, kai kaupimas nustatytas kaip nulis (446195)</span><span class="sxs-lookup"><span data-stu-id="d9b66-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="d9b66-114">Dabar atostogų operacijos leidžiamos darbuotojams, kurie bus atleisti ateityje, o kaupimas nustatytas kaip nulis.</span><span class="sxs-lookup"><span data-stu-id="d9b66-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="d9b66-115">Atostogų operacijos gali būti įvestos iki darbuotojo atleidimo datos.</span><span class="sxs-lookup"><span data-stu-id="d9b66-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="d9b66-116">Pasirinktinių laukų įtraukimas į naują darbininko formą išjungia atostogų tvarkymo laukus veiksmų srityje (473314)</span><span class="sxs-lookup"><span data-stu-id="d9b66-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="d9b66-117">Veiksmų srities parinktys naujoje **Darbininko** formoje, **Tvarkyti atostogas** parinktyje, nebus išjungtos, jei pasirinktiniai laukai buvo įtraukti į naują **Darbininko** formą.</span><span class="sxs-lookup"><span data-stu-id="d9b66-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="d9b66-118">Darant atostogų komentarų lauką privalomą, leidžiama pateikti atostogų užklausą, kai neįvesta jokių komentarų (473543)</span><span class="sxs-lookup"><span data-stu-id="d9b66-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="d9b66-119">Komentarų laukai dabar gali būti privalomi, o atostogų užklausos atsižvelgia į šį parametrą.</span><span class="sxs-lookup"><span data-stu-id="d9b66-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="d9b66-120">Privalomi laukai yra peržiūros funkcija.</span><span class="sxs-lookup"><span data-stu-id="d9b66-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d9b66-121">DMF objektas pasiekiamas kaupimo sustabdymams</span><span class="sxs-lookup"><span data-stu-id="d9b66-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="d9b66-122">DMF objektas dabar pasiekiamas kaupimo sustabdymams.</span><span class="sxs-lookup"><span data-stu-id="d9b66-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d9b66-123">Peržiūros režimu</span><span class="sxs-lookup"><span data-stu-id="d9b66-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="d9b66-124">Privalomi laukai</span><span class="sxs-lookup"><span data-stu-id="d9b66-124">Mandatory fields</span></span>

<span data-ttu-id="d9b66-125">Galite nustatyti laukelius privalomais naudodami Žmogiškųjų išteklių personalizavimo galimybes.</span><span class="sxs-lookup"><span data-stu-id="d9b66-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="d9b66-126">Šiai funkcijai reikia **Įrašyti rodiniai**.</span><span class="sxs-lookup"><span data-stu-id="d9b66-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="d9b66-127">Dėl platesnės informacijos apie įrašytas peržiūras, žr.:</span><span class="sxs-lookup"><span data-stu-id="d9b66-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="d9b66-128">[Įrašytos peržiūras - bendras prieinamumas](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) „Dynamics 365 2020“ leidime bangos 2 planas</span><span class="sxs-lookup"><span data-stu-id="d9b66-128">[Saved views - general availability](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="d9b66-129">Formų, kurios visiškai išnaudoja įrašytus rodinius, kūrimas</span><span class="sxs-lookup"><span data-stu-id="d9b66-129">Build forms that fully utilize saved views</span></span>](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="d9b66-130">„Human Resources“ programa programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="d9b66-130">Human Resources application in Teams</span></span>

<span data-ttu-id="d9b66-131">Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="d9b66-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d9b66-132">Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą.</span><span class="sxs-lookup"><span data-stu-id="d9b66-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d9b66-133">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="d9b66-133">For more information, see:</span></span>

- <span data-ttu-id="d9b66-134">[Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 1 plane</span><span class="sxs-lookup"><span data-stu-id="d9b66-134">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="d9b66-135">„Human Resources“ programa „Teams“</span><span class="sxs-lookup"><span data-stu-id="d9b66-135">Human Resources app in Teams</span></span>](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a><span data-ttu-id="d9b66-136">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="d9b66-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="d9b66-137">„Human Resources“ programėlė „Teams“ peržiūros funkcijose</span><span class="sxs-lookup"><span data-stu-id="d9b66-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="d9b66-138">**Pranešimai**: ne darbo laiko užklausų pateikėjai ir tvirtintojai bus informuojami „Teams” esančioje „Human Resources” programėlėje.</span><span class="sxs-lookup"><span data-stu-id="d9b66-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="d9b66-139">Tvirtintojai galės patvirtinti arba atmesti ne darbo laiko užklausas, o pateikėjai bus informuojami, jei užklausa buvo patvirtinta arba atmesta.</span><span class="sxs-lookup"><span data-stu-id="d9b66-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="d9b66-140">**Tvarkytuvo ne darbo laiko kalendorius**: vadovai galės peržiūrėti savo tiesioginių ataskaitų kalendoriaus rodinyje patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="d9b66-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="d9b66-141">Šis rodinys leidžia lengvai suprasti, kada jų komandos nariai nėra darbe.</span><span class="sxs-lookup"><span data-stu-id="d9b66-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="d9b66-142">Kontrolinio sąrašo objektai, nurodyti „Dataverse”</span><span class="sxs-lookup"><span data-stu-id="d9b66-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="d9b66-143">Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="d9b66-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="d9b66-144">Žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="d9b66-144">Known issues</span></span>

<span data-ttu-id="d9b66-145">**Ateities valdymas** darbo sritis gali rodyti funkcijas, kurios yra išjungtos kaip peržiūros funkcijos joms bendrai esant įjungtoms.</span><span class="sxs-lookup"><span data-stu-id="d9b66-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="d9b66-146">Toliau pateiktas bendras esamų funkcijų sąrašas, rodantis neteisingą statusą.</span><span class="sxs-lookup"><span data-stu-id="d9b66-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="d9b66-147">Išmokų valdymas</span><span class="sxs-lookup"><span data-stu-id="d9b66-147">Benefits management</span></span>
- <span data-ttu-id="d9b66-148">Atvejų valdymas</span><span class="sxs-lookup"><span data-stu-id="d9b66-148">Case management</span></span>
- <span data-ttu-id="d9b66-149">Duomenų įrašymas (auditavimas)</span><span class="sxs-lookup"><span data-stu-id="d9b66-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="d9b66-150">Atostogų skaičiavimas vienai bendrai ar vienam planui</span><span class="sxs-lookup"><span data-stu-id="d9b66-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="d9b66-151">Atostogų ir nebuvimo skaičiavimo sustabdymas</span><span class="sxs-lookup"><span data-stu-id="d9b66-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="d9b66-152">Balanso keitimo priežasties kodas ir komentaras</span><span class="sxs-lookup"><span data-stu-id="d9b66-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="d9b66-153">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="d9b66-153">Buy and sell leave</span></span>
- <span data-ttu-id="d9b66-154">Atostogų ir nebuvimo kalendorius</span><span class="sxs-lookup"><span data-stu-id="d9b66-154">Leave and absence calendar</span></span>
- <span data-ttu-id="d9b66-155">Atostogų turėjimo perdavimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="d9b66-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="d9b66-156">Atostogų skaičiavimo auditas</span><span class="sxs-lookup"><span data-stu-id="d9b66-156">Leave accrual auditing</span></span>
- <span data-ttu-id="d9b66-157">Atostogų skaičiavimo pašalinimas</span><span class="sxs-lookup"><span data-stu-id="d9b66-157">Leave accrual deletion</span></span>
- <span data-ttu-id="d9b66-158">Atostogų skaičiavimo apvalinimas</span><span class="sxs-lookup"><span data-stu-id="d9b66-158">Leave accrual rounding</span></span>
- <span data-ttu-id="d9b66-159">Konfigūruoti keletą atostogų tipų viename atostogų plane</span><span class="sxs-lookup"><span data-stu-id="d9b66-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="d9b66-160">Atnaujinti nedirbamo laiko papildymus</span><span class="sxs-lookup"><span data-stu-id="d9b66-160">Update time-off enhancements</span></span>
- <span data-ttu-id="d9b66-161">Naudoti darbuotojo FTE apskaičiavimams</span><span class="sxs-lookup"><span data-stu-id="d9b66-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="d9b66-162">Kryžminės bendrovės kompensavimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="d9b66-162">Cross company compensation view</span></span>
- <span data-ttu-id="d9b66-163">Veiklos efektyvumo vertinimų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="d9b66-163">Print performance reviews</span></span>
- <span data-ttu-id="d9b66-164">Atostogų kaupimo šventinių dienų taisymai</span><span class="sxs-lookup"><span data-stu-id="d9b66-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="d9b66-165">Darbuotojų Išmokų plano objektas</span><span class="sxs-lookup"><span data-stu-id="d9b66-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="d9b66-166">Neseniai aptikome dvi problemas, susijusias su **DarbuotojųIšmokųPlano** objektu.</span><span class="sxs-lookup"><span data-stu-id="d9b66-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="d9b66-167">Importuojant darbininkų registracijų galiojimą, **Padengimo kodas** ir **Plano tipo kodas** nustatomi neteisingai.</span><span class="sxs-lookup"><span data-stu-id="d9b66-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="d9b66-168">Dėl šios problemos, darbuotojų išmokų planai rodomi neteisingai **Darbininkų išmokų plano** formoje ir **Atviros registracijos** formoje darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="d9b66-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="d9b66-169">Ši problema taip pat gali paveikti darbuotojo gebėjimą pasirinkti planus darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="d9b66-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="d9b66-170">Šiuo metu nėra problemos sprendimo būdo.</span><span class="sxs-lookup"><span data-stu-id="d9b66-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="d9b66-171">Mes laikome tai kaip aukšto prioriteto pataisą ir pristatysime šią pataisą kitame leidime.</span><span class="sxs-lookup"><span data-stu-id="d9b66-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9b66-172">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="d9b66-172">See also</span></span>

[<span data-ttu-id="d9b66-173">Kas nauja ar pasikeitė „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="d9b66-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d9b66-174">„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga</span><span class="sxs-lookup"><span data-stu-id="d9b66-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d9b66-175">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="d9b66-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d9b66-176">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="d9b66-176">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]