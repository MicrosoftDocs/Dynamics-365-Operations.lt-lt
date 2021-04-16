---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 28 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources funkcijos 2020 m. gegužės 28 d.
author: andreabichsel
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e15891a2cb75851d195e08b87bbfc9efb78e66e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803398"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="78aae-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 28 d.)</span><span class="sxs-lookup"><span data-stu-id="78aae-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="78aae-104">Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos.</span><span class="sxs-lookup"><span data-stu-id="78aae-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="78aae-105">Pakeitimai taikomi 8.1.3287 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="78aae-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="78aae-106">Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="78aae-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="78aae-107">Objektas „LeaveRequest“ neveikia, kai įgalinate kelis tipus pagal atostogų planui (447498)</span><span class="sxs-lookup"><span data-stu-id="78aae-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="78aae-108">Šiuo pakeitimu **„LeaveEnrollmentV2Entity“** nuo šiol galima taisyti klaidą, kuri įvyksta, kai įgalinami keli atostogų plano tipai.</span><span class="sxs-lookup"><span data-stu-id="78aae-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="78aae-109">Paketinio konflikto sumažinimo priemonė (peržiūra) (446619)</span><span class="sxs-lookup"><span data-stu-id="78aae-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="78aae-110">Kai įgalinate šią funkciją, galite tikėtis, kad sumažės blokavimų paketinės sistemos lentelėse, kai pasirenkate ir užbaigiate užduotis.</span><span class="sxs-lookup"><span data-stu-id="78aae-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="78aae-111">„UpdateConflict“ įrašant darbuotoją neleidžia redaguoti įrašo dalyje Žmonės (427915)</span><span class="sxs-lookup"><span data-stu-id="78aae-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="78aae-112">Šis pakeitimas ištaiso klaidą, pateikiamą, kai įtraukiamas naujas darbuotojas, naujinama adreso informacija ir keičiamos kalbos nuostatos.</span><span class="sxs-lookup"><span data-stu-id="78aae-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="78aae-113">Šiame unikaliame scenarijuje pateikiama klaida, rodanti, kad įrašo nepavyko atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="78aae-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="78aae-114">Nepavyksta įtraukti priedo prie patvirtintos atostogų užklausos pakartotiniam pateikimui (425407)</span><span class="sxs-lookup"><span data-stu-id="78aae-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="78aae-115">Šis pakeitimas nuo šiol leidžia priedus patvirtintiems atostogų prašymams.</span><span class="sxs-lookup"><span data-stu-id="78aae-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="78aae-116">Vartotojas gali įvesti darbuotojo kompensaciją kitoje juridinio subjekto formoje (409529)</span><span class="sxs-lookup"><span data-stu-id="78aae-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="78aae-117">Šiuo pakeitimu išjungiamos kompensavimo parinktys, siekiant išvengti netyčinio netinkamo juridinio subjekto kompensacijų įrašų įvedimo.</span><span class="sxs-lookup"><span data-stu-id="78aae-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="78aae-118">Klaida, kai perkeliant darbuotoją, darbuotojo pareigų priskyrimo data yra ankstesnė nei pareigų trukmė (429402)</span><span class="sxs-lookup"><span data-stu-id="78aae-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="78aae-119">Klaidos pranešimai perkeliant darbuotoją šiame scenarijuje buvo atnaujintas, kad aiškiau aprašytų problemą ir reikalingus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="78aae-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="78aae-120">Priedų galimybės darbuotojo savitarnos išmokų registracijoje</span><span class="sxs-lookup"><span data-stu-id="78aae-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="78aae-121">Nuo šiol galite įtraukti priedus išmokų registracijos proceso metu kiekvienam planui, kuriam darbuotojas registruojasi.</span><span class="sxs-lookup"><span data-stu-id="78aae-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="78aae-122">Tada galite peržiūrėti priedus, esančius formoje **Darbuotojo užregistruotos išmokos**.</span><span class="sxs-lookup"><span data-stu-id="78aae-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="78aae-123">Peržiūros režimu</span><span class="sxs-lookup"><span data-stu-id="78aae-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="78aae-124">„Human Resources“ programa programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="78aae-124">Human Resources application in Teams</span></span>

<span data-ttu-id="78aae-125">Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="78aae-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="78aae-126">Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą.</span><span class="sxs-lookup"><span data-stu-id="78aae-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="78aae-127">Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="78aae-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="78aae-128">Atostogų sustabdymas</span><span class="sxs-lookup"><span data-stu-id="78aae-128">Leave suspension</span></span>

<span data-ttu-id="78aae-129">Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą.</span><span class="sxs-lookup"><span data-stu-id="78aae-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="78aae-130">Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus.</span><span class="sxs-lookup"><span data-stu-id="78aae-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="78aae-131">Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukuria proporcingai paskirstytą darbuotojo atostogų balanso koregavimą.</span><span class="sxs-lookup"><span data-stu-id="78aae-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="78aae-132">Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="78aae-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="78aae-133">Vartotojo patirties naujinimas nurodyti, jog kaupimas sustabdytas (429550)</span><span class="sxs-lookup"><span data-stu-id="78aae-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="78aae-134">Dabar vartotojo patirtis nurodo, kad plano kaupimas buvo sustabdytas.</span><span class="sxs-lookup"><span data-stu-id="78aae-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="78aae-135">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="78aae-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="78aae-136">Duomenų bazės registravimas (peržiūra nuo birželio mėn.)</span><span class="sxs-lookup"><span data-stu-id="78aae-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="78aae-137">Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi.</span><span class="sxs-lookup"><span data-stu-id="78aae-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="78aae-138">Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="78aae-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="78aae-139">Ilgalaikiams pokyčiams stebėti suteikiamos užklausos galimybės.</span><span class="sxs-lookup"><span data-stu-id="78aae-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="78aae-140">Atostogų pirkimas ir pardavimas (peržiūra nuo birželio 1 d.)</span><span class="sxs-lookup"><span data-stu-id="78aae-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="78aae-141">Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas.</span><span class="sxs-lookup"><span data-stu-id="78aae-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="78aae-142">Šis procesas dažnai valdomas neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="78aae-142">This process is often managed manually.</span></span> <span data-ttu-id="78aae-143">Ši funkcija suteikia automatizuotą būdą tvarkyti žmogiškųjų išteklių skyriaus strategijas ir reikalavimus, taip pat padeda pašalinti klaidas, tuo pačiu supaprastinant atostogų tvarkymo procesą.</span><span class="sxs-lookup"><span data-stu-id="78aae-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="78aae-144">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="78aae-144">For more information, see:</span></span>

- [<span data-ttu-id="78aae-145">Atostogų pirkimo ir pardavimo strategijų valdymas</span><span class="sxs-lookup"><span data-stu-id="78aae-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="78aae-146">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="78aae-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="78aae-147">Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui</span><span class="sxs-lookup"><span data-stu-id="78aae-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="78aae-148">Išmokų valdymo objektai ir išleidimas.</span><span class="sxs-lookup"><span data-stu-id="78aae-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="78aae-149">DMF objektai leidžia importuoti ir eksportuoti duomenis, kad būtų lengviau konfigūruoti išmokų valdymą.</span><span class="sxs-lookup"><span data-stu-id="78aae-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="78aae-150">Išmokų valdymo šablonu taip pat bus galima perkelti duomenis.</span><span class="sxs-lookup"><span data-stu-id="78aae-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="78aae-151">Šablonas nuosekliai eksportuoja ir importuoja duomenis, išsaugodamas duomenų ryšius.</span><span class="sxs-lookup"><span data-stu-id="78aae-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="78aae-152">Priežasties kodo įtraukimas į kaupimo sustabdymus (birželio 1 d.)</span><span class="sxs-lookup"><span data-stu-id="78aae-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="78aae-153">Į kaupimo sustabdymus įtraukti priežasties kodai.</span><span class="sxs-lookup"><span data-stu-id="78aae-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="78aae-154">Taisyklių perkėlimas (birželio 1 d.)</span><span class="sxs-lookup"><span data-stu-id="78aae-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="78aae-155">Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai.</span><span class="sxs-lookup"><span data-stu-id="78aae-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="78aae-156">Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="78aae-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="78aae-157">Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="78aae-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="78aae-158">Nurodytų atostogų tipų atostogų kaupimo sustabdymas (birželio 1 d.)</span><span class="sxs-lookup"><span data-stu-id="78aae-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="78aae-159">Šiame leidime personalas gali sukurti taisyklę, skirtą sustabdyti darbuotojų, įvedusių atostogų užklausas neapmokamoms atostogoms, atostogų kaupimus.</span><span class="sxs-lookup"><span data-stu-id="78aae-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="78aae-160">Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma.</span><span class="sxs-lookup"><span data-stu-id="78aae-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="78aae-161">Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.</span><span class="sxs-lookup"><span data-stu-id="78aae-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="78aae-162">DMF objektas pasiekiamas kaupimo sustabdymams (birželio 1 d.)</span><span class="sxs-lookup"><span data-stu-id="78aae-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="78aae-163">DMF objektas dabar pasiekiamas kaupimo sustabdymams.</span><span class="sxs-lookup"><span data-stu-id="78aae-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="78aae-164">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="78aae-164">See also</span></span>

[<span data-ttu-id="78aae-165">Kas nauja ar pasikeitė „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="78aae-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="78aae-166">„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga</span><span class="sxs-lookup"><span data-stu-id="78aae-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="78aae-167">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="78aae-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="78aae-168">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="78aae-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]