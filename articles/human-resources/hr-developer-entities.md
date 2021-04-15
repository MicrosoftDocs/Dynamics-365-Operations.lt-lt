---
title: „Dataverse“ lentelės
description: „Microsoft Dynamics 365 Human Resources“ naudoja „Dataverse“, kad įgalintų išplečiamumo ir integravimo scenarijus.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793614"
---
# <a name="dataverse-tables"></a><span data-ttu-id="b02cd-103">„Dataverse“ lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b02cd-104">„Microsoft Dynamics 365 Human Resources“ naudoja „Dataverse“, kad įgalintų išplečiamumo ir integravimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="b02cd-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="b02cd-105">„Human Resources“ objektai atitinka „Dataverse“ lenteles.</span><span class="sxs-lookup"><span data-stu-id="b02cd-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="b02cd-106">Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="b02cd-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="b02cd-107">Tolesnės „Dataverse“ lentelės yra prieinamos pagal „Human Resources“ objektus.</span><span class="sxs-lookup"><span data-stu-id="b02cd-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="b02cd-108">Išmokų lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-108">Benefit tables</span></span>

| <span data-ttu-id="b02cd-109">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-109">Name</span></span> | <span data-ttu-id="b02cd-110">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-111">Išmokos apskaičiavimo dažnumas</span><span class="sxs-lookup"><span data-stu-id="b02cd-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="b02cd-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="b02cd-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="b02cd-113">Išmokų skaičiavimo dažnumo mokėjimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="b02cd-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="b02cd-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="b02cd-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="b02cd-115">Išmokų apskaičiavimo tarifas</span><span class="sxs-lookup"><span data-stu-id="b02cd-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="b02cd-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="b02cd-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="b02cd-117">Išmokų apskaičiavimo tarifų informacija</span><span class="sxs-lookup"><span data-stu-id="b02cd-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="b02cd-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="b02cd-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="b02cd-119">Išmokų parinktis</span><span class="sxs-lookup"><span data-stu-id="b02cd-119">Benefit Option</span></span> | <span data-ttu-id="b02cd-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="b02cd-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="b02cd-121">Išmokų planas</span><span class="sxs-lookup"><span data-stu-id="b02cd-121">Benefit Plan</span></span> | <span data-ttu-id="b02cd-122">cdm_benefitplan (neįgalintas pasirinktinių laukų palaikymo atveju)</span><span class="sxs-lookup"><span data-stu-id="b02cd-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="b02cd-123">Išmokos tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-123">Benefit Type</span></span> | <span data-ttu-id="b02cd-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="b02cd-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="b02cd-125">Verslo proceso užduočių lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-125">Business process tasks tables</span></span>

| <span data-ttu-id="b02cd-126">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-126">Name</span></span> | <span data-ttu-id="b02cd-127">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-128">Verslo proceso kalendorius</span><span class="sxs-lookup"><span data-stu-id="b02cd-128">Business Process Calendar</span></span> | <span data-ttu-id="b02cd-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="b02cd-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="b02cd-130">Verslo proceso grupės priskyrimas</span><span class="sxs-lookup"><span data-stu-id="b02cd-130">Business Process Group Assignment</span></span> | <span data-ttu-id="b02cd-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="b02cd-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="b02cd-132">Verslo proceso bibliotekos užduočių grupė</span><span class="sxs-lookup"><span data-stu-id="b02cd-132">Business Process Library Task Group</span></span> | <span data-ttu-id="b02cd-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="b02cd-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="b02cd-134">Verslo proceso etapas</span><span class="sxs-lookup"><span data-stu-id="b02cd-134">Business Process Stage</span></span> | <span data-ttu-id="b02cd-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="b02cd-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="b02cd-136">Kontrolinio sąrašo šablono antraštė</span><span class="sxs-lookup"><span data-stu-id="b02cd-136">Checklist Template Header</span></span> | <span data-ttu-id="b02cd-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="b02cd-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="b02cd-138">Kontrolinio sąrašo užduotis</span><span class="sxs-lookup"><span data-stu-id="b02cd-138">Checklist Template Task</span></span> | <span data-ttu-id="b02cd-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="b02cd-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="b02cd-140">Užmokesčio lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-140">Compensation tables</span></span>

| <span data-ttu-id="b02cd-141">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-141">Name</span></span> | <span data-ttu-id="b02cd-142">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-143">Pastoviosios atlyginimo dalies planas</span><span class="sxs-lookup"><span data-stu-id="b02cd-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="b02cd-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="b02cd-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="b02cd-145">Kompensavimo tinklelis</span><span class="sxs-lookup"><span data-stu-id="b02cd-145">Compensation Grid</span></span> | <span data-ttu-id="b02cd-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="b02cd-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="b02cd-147">Kompensacijos lygis</span><span class="sxs-lookup"><span data-stu-id="b02cd-147">Compensation Level</span></span> | <span data-ttu-id="b02cd-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="b02cd-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="b02cd-149">Kompensavimo išmokų dažnumas</span><span class="sxs-lookup"><span data-stu-id="b02cd-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="b02cd-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="b02cd-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="b02cd-151">Kompensavimo atskaitos taškų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b02cd-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="b02cd-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="b02cd-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="b02cd-153">Kompensavimo atskaitos taškų nustatymo eilutė</span><span class="sxs-lookup"><span data-stu-id="b02cd-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="b02cd-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="b02cd-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="b02cd-155">Kompensacijos sritis</span><span class="sxs-lookup"><span data-stu-id="b02cd-155">Compensation Region</span></span> | <span data-ttu-id="b02cd-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="b02cd-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="b02cd-157">Kompensavimo struktūra</span><span class="sxs-lookup"><span data-stu-id="b02cd-157">Compensation Structure</span></span> | <span data-ttu-id="b02cd-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="b02cd-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="b02cd-159">Kompensacijų kitimo planas</span><span class="sxs-lookup"><span data-stu-id="b02cd-159">Compensation Variable Plan</span></span> | <span data-ttu-id="b02cd-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="b02cd-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="b02cd-161">Kompensacijų kitimo plano lygis</span><span class="sxs-lookup"><span data-stu-id="b02cd-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="b02cd-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="b02cd-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="b02cd-163">Kompensacijų kitimo plano tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="b02cd-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="b02cd-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="b02cd-165">Pastoviosios atlyginimo dalies įvykis</span><span class="sxs-lookup"><span data-stu-id="b02cd-165">Fixed Compensation Event</span></span> | <span data-ttu-id="b02cd-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="b02cd-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="b02cd-167">Kintamosios atlyginimo dalies paskirstymo taisyklė</span><span class="sxs-lookup"><span data-stu-id="b02cd-167">Vesting Rule</span></span> | <span data-ttu-id="b02cd-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="b02cd-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="b02cd-169">Darbuotojo pastovioji atlyginimo dalis</span><span class="sxs-lookup"><span data-stu-id="b02cd-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="b02cd-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="b02cd-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="b02cd-171">Organizacijos lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-171">Organization tables</span></span>

| <span data-ttu-id="b02cd-172">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-172">Name</span></span> | <span data-ttu-id="b02cd-173">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-174">Padalinys</span><span class="sxs-lookup"><span data-stu-id="b02cd-174">Department</span></span> | <span data-ttu-id="b02cd-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="b02cd-175">cdm_department</span></span> |
| <span data-ttu-id="b02cd-176">Įdarbinimas</span><span class="sxs-lookup"><span data-stu-id="b02cd-176">Employment</span></span> | <span data-ttu-id="b02cd-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="b02cd-177">cdm_employment</span></span> |
| <span data-ttu-id="b02cd-178">Įmonė</span><span class="sxs-lookup"><span data-stu-id="b02cd-178">Company</span></span> | <span data-ttu-id="b02cd-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="b02cd-179">cdm_company</span></span> |
| <span data-ttu-id="b02cd-180">Pareigos</span><span class="sxs-lookup"><span data-stu-id="b02cd-180">Job</span></span> | <span data-ttu-id="b02cd-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="b02cd-181">cdm_job</span></span> |
| <span data-ttu-id="b02cd-182">Darbo funkcija</span><span class="sxs-lookup"><span data-stu-id="b02cd-182">Job Function</span></span> | <span data-ttu-id="b02cd-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="b02cd-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="b02cd-184">Pareigos</span><span class="sxs-lookup"><span data-stu-id="b02cd-184">Job Position</span></span> | <span data-ttu-id="b02cd-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="b02cd-185">cdm_jobposition</span></span> |
| <span data-ttu-id="b02cd-186">Pareigų tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-186">Position Type</span></span> | <span data-ttu-id="b02cd-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="b02cd-187">cdm_positiontype</span></span> |
| <span data-ttu-id="b02cd-188">Darbininko paskyrimas į pareigas</span><span class="sxs-lookup"><span data-stu-id="b02cd-188">Position Worker Assignment</span></span> | <span data-ttu-id="b02cd-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="b02cd-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="b02cd-190">Pareigų dimensija</span><span class="sxs-lookup"><span data-stu-id="b02cd-190">Job Position Dimension</span></span> | <span data-ttu-id="b02cd-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="b02cd-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="b02cd-192">Darbo tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-192">Job Type</span></span> | <span data-ttu-id="b02cd-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="b02cd-193">cdm_jobtype</span></span> |
| <span data-ttu-id="b02cd-194">Kalba</span><span class="sxs-lookup"><span data-stu-id="b02cd-194">Language</span></span> | <span data-ttu-id="b02cd-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="b02cd-195">cdm_language</span></span> |
| <span data-ttu-id="b02cd-196">Kreipinys</span><span class="sxs-lookup"><span data-stu-id="b02cd-196">Title</span></span> | <span data-ttu-id="b02cd-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="b02cd-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="b02cd-198">**Pareigų tipas**, **Darbuotojo pareigoms priskyrimas** ir **Įdarbinimas** finansinės dimensijos suteikia vienos krypties integraciją su „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="b02cd-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="b02cd-199">Finansinių dimensijų naujinimai dabar negali būti sinchronizuojami iš „Dataverse“ į „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="b02cd-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="b02cd-200">Atostogų ir nebuvmo lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-200">Leave and absence tables</span></span>

| <span data-ttu-id="b02cd-201">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-201">Name</span></span> | <span data-ttu-id="b02cd-202">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-203">Atostogų banko operacija</span><span class="sxs-lookup"><span data-stu-id="b02cd-203">Leave Bank Transaction</span></span> | <span data-ttu-id="b02cd-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="b02cd-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="b02cd-205">Atostogų registracija</span><span class="sxs-lookup"><span data-stu-id="b02cd-205">Leave Enrollment</span></span> | <span data-ttu-id="b02cd-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="b02cd-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="b02cd-207">Atostogų planas</span><span class="sxs-lookup"><span data-stu-id="b02cd-207">Leave Plan</span></span> | <span data-ttu-id="b02cd-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="b02cd-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="b02cd-209">Atostogų prašymas</span><span class="sxs-lookup"><span data-stu-id="b02cd-209">Leave Request</span></span> | <span data-ttu-id="b02cd-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="b02cd-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="b02cd-211">Atostogų užklausos informacija</span><span class="sxs-lookup"><span data-stu-id="b02cd-211">Leave Request Detail</span></span> | <span data-ttu-id="b02cd-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="b02cd-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="b02cd-213">Atostogų tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-213">Leave Type</span></span> | <span data-ttu-id="b02cd-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="b02cd-214">cdm_leavetype</span></span> |
| <span data-ttu-id="b02cd-215">Atostogų tipo priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="b02cd-215">Leave Type Reason Code</span></span> | <span data-ttu-id="b02cd-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="b02cd-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="b02cd-217">Algalapio lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-217">Payroll tables</span></span>

| <span data-ttu-id="b02cd-218">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-218">Name</span></span> | <span data-ttu-id="b02cd-219">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-220">Mokėjimo ciklas</span><span class="sxs-lookup"><span data-stu-id="b02cd-220">Pay Cycle</span></span> | <span data-ttu-id="b02cd-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="b02cd-221">cdm_paycycle</span></span> |
| <span data-ttu-id="b02cd-222">Mokėjimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="b02cd-222">Pay Period</span></span> | <span data-ttu-id="b02cd-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="b02cd-223">cdm_payperiod</span></span> |
| <span data-ttu-id="b02cd-224">Algalapio pajamų kodas</span><span class="sxs-lookup"><span data-stu-id="b02cd-224">Payroll Earning Code</span></span> | <span data-ttu-id="b02cd-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="b02cd-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="b02cd-226">Banko sąskaitos išmoka</span><span class="sxs-lookup"><span data-stu-id="b02cd-226">Bank Account Disbursement</span></span> | <span data-ttu-id="b02cd-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="b02cd-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="b02cd-228">Mokesčių regionas</span><span class="sxs-lookup"><span data-stu-id="b02cd-228">Tax Region</span></span> | <span data-ttu-id="b02cd-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="b02cd-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="b02cd-230">Darbuotojo lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-230">Worker tables</span></span>

| <span data-ttu-id="b02cd-231">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-231">Name</span></span> | <span data-ttu-id="b02cd-232">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-233">Darbuotojas</span><span class="sxs-lookup"><span data-stu-id="b02cd-233">Worker</span></span> | <span data-ttu-id="b02cd-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="b02cd-234">cdm_worker</span></span> |
| <span data-ttu-id="b02cd-235">Darbininko adresas</span><span class="sxs-lookup"><span data-stu-id="b02cd-235">Worker Address</span></span> | <span data-ttu-id="b02cd-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="b02cd-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="b02cd-237">Darbininko asmeninė informacija</span><span class="sxs-lookup"><span data-stu-id="b02cd-237">Worker Personal Detail</span></span> | <span data-ttu-id="b02cd-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="b02cd-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="b02cd-239">Darbininko asmens tapatybės numeris</span><span class="sxs-lookup"><span data-stu-id="b02cd-239">Worker Person Identification Number</span></span> | <span data-ttu-id="b02cd-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="b02cd-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="b02cd-241">Darbininko asmens tapatybės tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-241">Worker Person Identification Type</span></span> | <span data-ttu-id="b02cd-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="b02cd-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="b02cd-243">Darbo kalendorius</span><span class="sxs-lookup"><span data-stu-id="b02cd-243">Work Calendar</span></span> | <span data-ttu-id="b02cd-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="b02cd-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="b02cd-245">Darbo kalendoriaus diena</span><span class="sxs-lookup"><span data-stu-id="b02cd-245">Work Calendar Day</span></span> | <span data-ttu-id="b02cd-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="b02cd-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="b02cd-247">Darbo kalendoriaus šventė</span><span class="sxs-lookup"><span data-stu-id="b02cd-247">Work Calendar Holiday</span></span> |<span data-ttu-id="b02cd-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="b02cd-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="b02cd-249">Darbo kalendoriaus šventės eilutė</span><span class="sxs-lookup"><span data-stu-id="b02cd-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="b02cd-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="b02cd-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="b02cd-251">Darbo kalendoriaus laiko intervalas</span><span class="sxs-lookup"><span data-stu-id="b02cd-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="b02cd-252">cdm_workcalendartimeinterval (neįgalintas pasirinktinių laukų palaikymo atveju)</span><span class="sxs-lookup"><span data-stu-id="b02cd-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="b02cd-253">Darbininko banko sąskaita</span><span class="sxs-lookup"><span data-stu-id="b02cd-253">Worker Bank Account</span></span> | <span data-ttu-id="b02cd-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="b02cd-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="b02cd-255">Darbuotojo nustatymo lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-255">Worker setup tables</span></span>

| <span data-ttu-id="b02cd-256">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-256">Name</span></span> | <span data-ttu-id="b02cd-257">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-258">Seniai dirbančiojo būsena</span><span class="sxs-lookup"><span data-stu-id="b02cd-258">Veteran Status</span></span> | <span data-ttu-id="b02cd-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="b02cd-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="b02cd-260">Etninė kilmė</span><span class="sxs-lookup"><span data-stu-id="b02cd-260">Ethnic Origin</span></span> | <span data-ttu-id="b02cd-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="b02cd-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="b02cd-262">Priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="b02cd-262">Reason Code</span></span> | <span data-ttu-id="b02cd-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="b02cd-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="b02cd-264">Asmens identifikavimo pažymėjimus išduodanti įstaiga</span><span class="sxs-lookup"><span data-stu-id="b02cd-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="b02cd-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="b02cd-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="b02cd-266">Kompetencijos lentelės</span><span class="sxs-lookup"><span data-stu-id="b02cd-266">Competency tables</span></span>

| <span data-ttu-id="b02cd-267">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="b02cd-267">Name</span></span> | <span data-ttu-id="b02cd-268">Lentelė</span><span class="sxs-lookup"><span data-stu-id="b02cd-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b02cd-269">Įgūdžių tipas</span><span class="sxs-lookup"><span data-stu-id="b02cd-269">Skill Type</span></span> | <span data-ttu-id="b02cd-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="b02cd-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="b02cd-271">Lentelės ryšių modeliai</span><span class="sxs-lookup"><span data-stu-id="b02cd-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="b02cd-272">Darbuotojas</span><span class="sxs-lookup"><span data-stu-id="b02cd-272">Worker</span></span>

![Darbuotojas](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="b02cd-274">Užduotis ir pareigos</span><span class="sxs-lookup"><span data-stu-id="b02cd-274">Job and Job Position</span></span>

![Užduotis ir pareigos](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="b02cd-276">Išmokos</span><span class="sxs-lookup"><span data-stu-id="b02cd-276">Benefits</span></span>

![Išmokos](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="b02cd-278">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="b02cd-278">Compensation</span></span>

![Kompensacija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="b02cd-280">Išeiti</span><span class="sxs-lookup"><span data-stu-id="b02cd-280">Leave</span></span>

![Išeiti](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="b02cd-282">Darbo kalendorius</span><span class="sxs-lookup"><span data-stu-id="b02cd-282">Work Calendar</span></span>

![Darbo kalendorius](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="b02cd-284">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="b02cd-284">See also</span></span>

[<span data-ttu-id="b02cd-285">Duomenų integravimo technologijos pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="b02cd-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="b02cd-286">„Dataverse“ integravimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b02cd-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="b02cd-287">Konfigūruokite „Dataverse“ virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="b02cd-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="b02cd-288">„Human Resources“ virtualių lentelių DUK</span><span class="sxs-lookup"><span data-stu-id="b02cd-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="b02cd-289">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="b02cd-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="b02cd-290">Terminologijos naujinimai</span><span class="sxs-lookup"><span data-stu-id="b02cd-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]