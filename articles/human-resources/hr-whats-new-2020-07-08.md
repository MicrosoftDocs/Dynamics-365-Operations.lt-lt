---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. liepos 8 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. liepos 8 d.
author: andreabichsel
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 433eef4f11f385e85648d137521996a47a8ffd7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053928"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="fd8b6-103">Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. liepos 8 d.)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="fd8b6-104">Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="fd8b6-105">Pakeitimai taikomi 8.1.3382 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="fd8b6-106">Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="fd8b6-107">Duomenų bazės registravimas</span><span class="sxs-lookup"><span data-stu-id="fd8b6-107">Database logging</span></span>

<span data-ttu-id="fd8b6-108">Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="fd8b6-109">Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="fd8b6-110">Naudojate duomenų bazės registravimo galimybes, kad laikui bėgant pamatytumėte šiuos pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="fd8b6-111">Daugiau informacijos ieškokite [Duomenų bazės registravimo konfigūravimas ir tvarkymas](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="fd8b6-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="fd8b6-112">Konfigūruokite Darbuotojo savitarnos paslaugų pavadinimą</span><span class="sxs-lookup"><span data-stu-id="fd8b6-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="fd8b6-113">**Žmogiškųjų išteklių parametruose**, dabar galite pakeisti **Darbuotojo savitarnos paslaugų** darbo srities pavadinimą į **Savitarnos paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="fd8b6-114">Dėl išsamesnės informacijos, žr. [Darbuotojo savitarnos paslaugų darbo srities pavadinimo keitimas](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="fd8b6-115">Naudos valdymo atidarymo įtraukimo prieiga ne laikotarpyje</span><span class="sxs-lookup"><span data-stu-id="fd8b6-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="fd8b6-116">Šis išleidimas pataiso klaidą, kai darbuotojas gali prisijungti prie naudos atidarydamas įtraukimą ne per įtraukimo laikotarpį ar be gyvavimo ciklo įvykio.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="fd8b6-117">Dėl to, jei turite demonstracijoje atidarykite įtraukimą Darbuotojo savitarnos paslaugose, jums reikia pataisyti atidarymo įtraukimo datas į šiandien (ar anksčiau) tam, kad jį padarytumėte prieinamą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="fd8b6-118">Galite pakeisti šį nustatymą **Naudų valdymas > Laikotarpių taisyklės ir parinktys**.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="fd8b6-119">Darbuotojo įtraukimo patvirtinimo siuntimas elektroniniu paštu</span><span class="sxs-lookup"><span data-stu-id="fd8b6-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="fd8b6-120">Dabar galite nusiųsti elektroninį laišką darbuotojams po to, kai jie pabaigs jų naudos pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="fd8b6-121">Galite nusiųsti nustatytąją žinutę ar naudoti organizacijos elektronini pašto šabloną.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="fd8b6-122">Šie nustatymai yra **Žmogiškųjų išteklių parametrai > Privalumų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="fd8b6-123">Atšauktas leidimas vis dar rodomas ateities laiku Žmonių darbo srityje (441358)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="fd8b6-124">Atšauktas leidimas nebėra rodomas kaip ateinantis laikas leidimo kortelėse **Žmonių** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="fd8b6-125">Negalima naudoti skyriaus objekto savybių PositionV2 objekte (456486)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="fd8b6-126">Dabar galite įtraukti skyrių nekurdami dublikuoto ryšio.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="fd8b6-127">PayrollWorkerEnrolledBenefitDetailEntity turi naudoti tik apskaičiuotą laukelį išėjimo į pensiją planams (459779)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="fd8b6-128">Eksportuojant **PayrollWorkerEnrolledBenefitDetailEntity** objektą, eksportavimas nustato, ar jis turi naudoti apskaičiuotą laukelį pagal santykio lentelę, ar naudoti **ContributionAmountCur** laukelį atsarginėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="fd8b6-129">Duomenų objekto naudojama logika naudoja santykio lentelę tais atvejais, kai paraiška įprastai neegzistuoja.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="fd8b6-130">Ši logika lemia objekto eksportavimo grįžimą į nulio vertę šiame stulpelyje, nes nėra apskaičiavimo santykio lentelės ir produktas neleidžia klientui jo nurodyti.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="fd8b6-131">Painūs vertimai čekų kalba Personalo valdyme ir Darbuotojo savitarnos paslaugose (400276)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="fd8b6-132">Šis leidimas pataiso **Bendrovės aplanko**, **Kito registruoto kurso**, **Darbo** ir **Padėties** vertimus.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="fd8b6-133">WorkCalendarEmployment lentelė neturi sukurtų ir pakeistų įjungtų sistemos laukelių (460171)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="fd8b6-134">Sukurti ir pakeisti sistemos laukeliai dabar yra įjungti **WorkCalendarEmployment** lentelėje Žmogiškuosiuose ryšiuose.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="fd8b6-135">Nulinė ataskaitos išimtis Samdymui ir informacijos įtraukimas ateities darbuotojams (455475)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="fd8b6-136">Šis leidimas pataiso klaidą (jokios nuorodos) rodomame darbuotojų įraše, kai jūs priimate į darbą darbuotoją naudodami parinktį **Samdyti ir įtraukti informaciją**.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="fd8b6-137">Pakeitimai atlikti „Dataverse Worker“ objekte nepasirodo Žmogiškuosiuose ištekliuose (455652)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="fd8b6-138">Toliau pateiktų laukelių pakeitimai **Darbuotojas** objekte „Dataverse“ nepasirodys Žmogiškuosiuose ištekliuose:</span><span class="sxs-lookup"><span data-stu-id="fd8b6-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="fd8b6-139">**Darbas iš namų**</span><span class="sxs-lookup"><span data-stu-id="fd8b6-139">**Works from home**</span></span>
- <span data-ttu-id="fd8b6-140">**Paaukštinimo data**</span><span class="sxs-lookup"><span data-stu-id="fd8b6-140">**Seniority date**</span></span>
- <span data-ttu-id="fd8b6-141">**Jubiliejaus data**</span><span class="sxs-lookup"><span data-stu-id="fd8b6-141">**Anniversary date**</span></span>
- <span data-ttu-id="fd8b6-142">**Pradinio įdarbinimo data**</span><span class="sxs-lookup"><span data-stu-id="fd8b6-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="fd8b6-143">Tinkamas užmokesčio lygis nėra nustatytasis pagal pareigoms priskirtą darbą (394136)</span><span class="sxs-lookup"><span data-stu-id="fd8b6-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="fd8b6-144">Šiuo pakeitimu tinkamas užmokesčio lygis yra nustatytasis pagal **Įsigaliojimo datą** ir įrašomas **Pareigų informacija** ir **Pradžios data** esančius **Užmokesčio planavimo priskyrime**.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="fd8b6-145">Peržiūros režimu</span><span class="sxs-lookup"><span data-stu-id="fd8b6-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="fd8b6-146">Privalomi laukai</span><span class="sxs-lookup"><span data-stu-id="fd8b6-146">Mandatory fields</span></span> 

<span data-ttu-id="fd8b6-147">Dabar galite padaryti laukus privalomais naudodami Žmogiškųjų išteklių personalizavimo galimybes.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="fd8b6-148">Šiai funkcijai reikia **Įrašyti rodiniai**.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="fd8b6-149">„Human Resources“ programa programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="fd8b6-149">Human Resources application in Teams</span></span>

<span data-ttu-id="fd8b6-150">Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="fd8b6-151">Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="fd8b6-152">Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="fd8b6-152">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="fd8b6-153">Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui</span><span class="sxs-lookup"><span data-stu-id="fd8b6-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="fd8b6-154">Išmokų valdymo objektai ir išleidimas.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="fd8b6-155">DMF objektai leidžia paprastai importuoti ir eksportuoti duomenis, kad lengviau konfigūruotumėte išmokų valdymą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="fd8b6-156">Išmokų valdymo šablonas taps prieinamu duomenų perkėlimui.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="fd8b6-157">Šablonas nuosekliai eksportuoja ir importuoja duomenis išsaugodamas duomenų priklausomumą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="fd8b6-158">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="fd8b6-158">Buy and sell leave</span></span> 

<span data-ttu-id="fd8b6-159">Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="fd8b6-160">Šis procesas dažnai valdomas neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-160">This process is often managed manually.</span></span> <span data-ttu-id="fd8b6-161">Ši funkcija automatizuoja žmogiškųjų išteklių departamento valdymo strategijas ir užklausas.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="fd8b6-162">Ji supaprastina atostogų valdymo procesą ir padeda pašalinti klaidas.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="fd8b6-163">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="fd8b6-163">For more information, see:</span></span>

- [<span data-ttu-id="fd8b6-164">Atostogų pirkimo ir pardavimo strategijų valdymas</span><span class="sxs-lookup"><span data-stu-id="fd8b6-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="fd8b6-165">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="fd8b6-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="fd8b6-166">Atostogų kaupimas vienai įmonei arba vienam planui</span><span class="sxs-lookup"><span data-stu-id="fd8b6-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="fd8b6-167">Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="fd8b6-168">Tokia galimybė suteikia kaupimo proceso aiškumą klientams su skirtingais išėjimo į pensiją metais ir išėjimo į pensiją kaupimo politika.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="fd8b6-169">Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="fd8b6-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="fd8b6-170">Įtraukite priedus į laiko prašymus</span><span class="sxs-lookup"><span data-stu-id="fd8b6-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="fd8b6-171">Galimybė pridėti priedus prie patvirtintų atostogų prašymų yra itin svarbi dabartinėje COVID-19 situacijoje.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="fd8b6-172">Dabar darbuotojai gali pridėti šiuos priedus.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-172">Employees can now add these attachments.</span></span> <span data-ttu-id="fd8b6-173">Jie taip pat turi daugiau įžvalgų apie atostogų prašymų naujinimų kūrimą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="fd8b6-174">Norėdami sužinoti daugiau, skaitykite [Priedo prie esamo prašymo pridėjimas](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="fd8b6-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="fd8b6-175">Priežasties kodo pridėjimas į kaupimo sustabdymus</span><span class="sxs-lookup"><span data-stu-id="fd8b6-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="fd8b6-176">Į kaupimo sustabdymus įtraukti priežasties kodai.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="fd8b6-177">Perkėlimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="fd8b6-177">Carry forward rules</span></span> 

<span data-ttu-id="fd8b6-178">Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="fd8b6-179">Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="fd8b6-180">Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="fd8b6-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="fd8b6-181">Atostogų kaupimo sustabdymas konkretiems atostogų tipams</span><span class="sxs-lookup"><span data-stu-id="fd8b6-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="fd8b6-182">Galite sukurti taisyklę sustabdyti darbuotojų, įvedusių neapmokamų atostogų prašymus, atostogų kaupimą.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="fd8b6-183">Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="fd8b6-184">Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="fd8b6-185">DMF objektas pasiekiamas kaupimo sustabdymams</span><span class="sxs-lookup"><span data-stu-id="fd8b6-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="fd8b6-186">DMF objektas dabar pasiekiamas kaupimo sustabdymams.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="fd8b6-187">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="fd8b6-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="fd8b6-188">Kontrolinio sąrašo objektai, nurodyti „Dataverse”</span><span class="sxs-lookup"><span data-stu-id="fd8b6-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="fd8b6-189">Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="fd8b6-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd8b6-190">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="fd8b6-190">See also</span></span>

[<span data-ttu-id="fd8b6-191">Kas nauja ar pasikeitė „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="fd8b6-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="fd8b6-192">„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga</span><span class="sxs-lookup"><span data-stu-id="fd8b6-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="fd8b6-193">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="fd8b6-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="fd8b6-194">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="fd8b6-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]