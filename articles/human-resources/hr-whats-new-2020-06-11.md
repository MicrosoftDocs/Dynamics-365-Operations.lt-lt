---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. birželio mėn. 11 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. birželio 11 d.
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0720b2024a865fcd42cd80fd905586d626388f8f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711799"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="5dc9f-103">Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. birželio mėn. 11 d.)</span><span class="sxs-lookup"><span data-stu-id="5dc9f-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="5dc9f-104">Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5dc9f-105">Pakeitimai taikomi 8.1.3316 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="5dc9f-106">Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="5dc9f-107">Kartais dėl supaprastintos darbuotojo formos neveikia antrinės formos uždarymo (X) mygtukai (442369)</span><span class="sxs-lookup"><span data-stu-id="5dc9f-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="5dc9f-108">Kai nauja **Darbuotojas** forma įjungiama, uždarymo mygtukas ( **X**) retkarčiais neveikia antrinėse formose.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="5dc9f-109">Ši problema pasikartodavo.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-109">This problem was intermittent.</span></span> <span data-ttu-id="5dc9f-110">Galėjote uždaryti formą grįžus ir išėjus.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="5dc9f-111">Pavyzdžiui, galite pasirinkti meniu elementą kairėje ir grįžti į **Darbuotojas** formą, o tada ją uždaryti.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="5dc9f-112">Šios savaitės pataisa išsprendė šią problemą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="5dc9f-113">Darbuotojo asmeninio kontaktinio asmens objektas neeksportuoja asmeninių kontaktų esant pirminiam ryšio tipui</span><span class="sxs-lookup"><span data-stu-id="5dc9f-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="5dc9f-114">Šame leidime **Darbuotojo asmeninio kontaktinio asmuo** objektas eksportuoja visus ryšių tipus.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="5dc9f-115">HcmPozicijosDarbuotojoPriskyrimasV2Objektas turėtų būti įtrauktas į „Ceridian” algalapio integravimo paketą pagal numatytuosius nustatymus (448506)</span><span class="sxs-lookup"><span data-stu-id="5dc9f-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="5dc9f-116">Su šiuo pakeitimu **HcmPozicijaDarbuotojoPriskyrimasV2Objektas** yra įtrauktas į „Ceridian” algalapio integravimo paketą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5dc9f-117">Peržiūros režimu</span><span class="sxs-lookup"><span data-stu-id="5dc9f-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="5dc9f-118">Duomenų bazės registravimas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-118">Database logging</span></span>

<span data-ttu-id="5dc9f-119">Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="5dc9f-120">Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="5dc9f-121">Naudojate duomenų bazės registravimo galimybes, kad laikui bėgant pamatytumėte šiuos pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="5dc9f-122">Daugiau informacijos ieškokite [Duomenų bazės registravimo konfigūravimas ir tvarkymas](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="5dc9f-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="5dc9f-123">„Human Resources“ programa programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="5dc9f-123">Human Resources application in Teams</span></span>

<span data-ttu-id="5dc9f-124">Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="5dc9f-125">Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="5dc9f-126">Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="5dc9f-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="5dc9f-127">Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui</span><span class="sxs-lookup"><span data-stu-id="5dc9f-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="5dc9f-128">Išmokų valdymo objektai ir išleidimas.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="5dc9f-129">DMF objektai leidžia paprastai importuoti ir eksportuoti duomenis, kad lengviau konfigūruotumėte išmokų valdymą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="5dc9f-130">Išmokų valdymo šablonas taps prieinamu duomenų perkėlimui.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="5dc9f-131">Šablonas nuosekliai eksportuoja ir importuoja duomenis išsaugodamas duomenų priklausomumą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="5dc9f-132">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-132">Buy and sell leave</span></span> 

<span data-ttu-id="5dc9f-133">Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="5dc9f-134">Šis procesas dažnai valdomas neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-134">This process is often managed manually.</span></span> <span data-ttu-id="5dc9f-135">Ši funkcija automatizuoja žmogiškųjų išteklių departamento valdymo strategijas ir užklausas.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="5dc9f-136">Ji supaprastina atostogų valdymo procesą ir padeda pašalinti klaidas.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="5dc9f-137">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-137">For more information, see:</span></span>

- [<span data-ttu-id="5dc9f-138">Atostogų pirkimo ir pardavimo strategijų valdymas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="5dc9f-139">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="5dc9f-140">Atostogų kaupimas vienai įmonei arba vienam planui</span><span class="sxs-lookup"><span data-stu-id="5dc9f-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="5dc9f-141">Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="5dc9f-142">Šis gebėjimas suteikia klientams su skirtingais išėjimo į pensiją metais ar atostogomis aiškumo apie kaupimo strategijas.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="5dc9f-143">Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="5dc9f-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="5dc9f-144">Priedų pridėjimas prašymams atidėti</span><span class="sxs-lookup"><span data-stu-id="5dc9f-144">Add attachments to time off requests</span></span>

<span data-ttu-id="5dc9f-145">Galimybė pridėti priedus prie patvirtintų atostogų prašymų yra itin svarbi dabartinėje COVID-19 situacijoje.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="5dc9f-146">Dabar darbuotojai gali pridėti šiuos priedus.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-146">Employees can now add these attachments.</span></span> <span data-ttu-id="5dc9f-147">Jie taip pat turi daugiau įžvalgų apie atostogų prašymų naujinimų kūrimą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="5dc9f-148">Norėdami sužinoti daugiau, skaitykite [Priedo prie esamo prašymo pridėjimas](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="5dc9f-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="5dc9f-149">Priežasties kodo pridėjimas į kaupimo sustabdymus</span><span class="sxs-lookup"><span data-stu-id="5dc9f-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="5dc9f-150">Į kaupimo sustabdymus įtraukti priežasties kodai.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="5dc9f-151">Perkėlimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="5dc9f-151">Carry forward rules</span></span> 

<span data-ttu-id="5dc9f-152">Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="5dc9f-153">Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="5dc9f-154">Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="5dc9f-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="5dc9f-155">Atostogų kaupimo sustabdymas konkretiems atostogų tipams</span><span class="sxs-lookup"><span data-stu-id="5dc9f-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="5dc9f-156">Galite sukurti taisyklę sustabdyti darbuotojų, įvedusių neapmokamų atostogų prašymus, atostogų kaupimą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="5dc9f-157">Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="5dc9f-158">Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="5dc9f-159">DMF objektas pasiekiamas kaupimo sustabdymams</span><span class="sxs-lookup"><span data-stu-id="5dc9f-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="5dc9f-160">DMF objektas dabar pasiekiamas kaupimo sustabdymams.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="5dc9f-161">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="5dc9f-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="5dc9f-162">Naujos platformos galimybės</span><span class="sxs-lookup"><span data-stu-id="5dc9f-162">New platform capabilities</span></span> 

<span data-ttu-id="5dc9f-163">Jūs galėsite padaryti laukus privalomus naudojant personalizavimą.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="5dc9f-164">Norėdami įjungti šią funkciją, įjunkite **Įrašyti rodiniai**.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="5dc9f-165">Darbuotojų savitarnos pavadinimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="5dc9f-166">Nauja parinktis bus prieinama „Human Resources” parametruose, kad galėtumėte atnaujinti Darbuotojo savitarnos darbovietės pavadinimą į Savitarną.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="5dc9f-167">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5dc9f-167">See also</span></span>

[<span data-ttu-id="5dc9f-168">Kas nauja ar pasikeitė „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="5dc9f-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5dc9f-169">„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga</span><span class="sxs-lookup"><span data-stu-id="5dc9f-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5dc9f-170">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5dc9f-171">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="5dc9f-171">Manage features</span></span>](hr-admin-manage-features.md)