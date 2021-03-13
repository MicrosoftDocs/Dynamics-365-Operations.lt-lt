---
title: Aplikanto sekimo sistemos integravimo API įžanga
description: Šioje temoje aprašoma „Dynamics 365 Human Resources“ aplikanto seimo sistemos (ATS) integravimo API.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125598"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="1fea7-103">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="1fea7-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="1fea7-104">Šioje temoje aprašoma „Dynamics 365 Human Resources“ aplikanto seimo sistemos (ATS) integravimo API.</span><span class="sxs-lookup"><span data-stu-id="1fea7-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="1fea7-105">API paskirtis yra įjungti paleistą integravimą tarp „Dynamics 365 Human Resources“ ir partnerio ATS.</span><span class="sxs-lookup"><span data-stu-id="1fea7-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS integravimo eiga](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="1fea7-107">Integruota patirtis prasideda žmogiškuosiuose ištekliuose, kai samdantis vadovas sukuria samdymo užklausą.</span><span class="sxs-lookup"><span data-stu-id="1fea7-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="1fea7-108">Kai užklausa aktyvuota, ATS ištraukia išsamią informaciją užklausai siekiant sukurti samdymo projektą.</span><span class="sxs-lookup"><span data-stu-id="1fea7-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="1fea7-109">Tuomet jis seka samdymo vamzdynu, kad pasirinktų ir samdytų pretendentą pareigoms.</span><span class="sxs-lookup"><span data-stu-id="1fea7-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="1fea7-110">Galiausiai ATS užbaigia kelionę aplink integravimą nusiųsdama pasirinkto pretendento įrašą žmogiškiesiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="1fea7-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="1fea7-111">Pretendento įrašas tada gali praieiti pro daugiau samdymo patvirtinimų ir darbo eigų, kad sukurtų darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="1fea7-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="1fea7-112">Norėdami įjungti integravimą, žmogiškieji ištekliai įtraukė šiuos komponentus:</span><span class="sxs-lookup"><span data-stu-id="1fea7-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="1fea7-113">Funkcijas siekiant sukurti samdymo užklausą.</span><span class="sxs-lookup"><span data-stu-id="1fea7-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="1fea7-114">Išplėsto kandidato profilis ir susijusios darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="1fea7-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="1fea7-115">API integravimas atveriantis naujas funkcijas siekiant integruoti paraiškas.</span><span class="sxs-lookup"><span data-stu-id="1fea7-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="1fea7-116">Dėl daugiau informacijos apie samdymo užklausų ir pretendentų funkcijų nustatymą ir naudojimą žr. [Samdyti pretendentus darbui](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="1fea7-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="1fea7-117">„Microsoft Dataverse“</span><span class="sxs-lookup"><span data-stu-id="1fea7-117">Microsoft Dataverse</span></span>

<span data-ttu-id="1fea7-118">API yra sukurtos „Microsoft Dataverse“ (anksčiau „Common Data Service“).</span><span class="sxs-lookup"><span data-stu-id="1fea7-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="1fea7-119">Visos RESTful sąveikos su šiuo API yra daromos per „Microsoft Dataverse“ žiniatinklio API, kurios naudoja OData.</span><span class="sxs-lookup"><span data-stu-id="1fea7-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="1fea7-120">Šis API yra papildomas rinkinys „Dataverse“ žiniatinklio API.</span><span class="sxs-lookup"><span data-stu-id="1fea7-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="1fea7-121">„Dataverse“ žiniatinklio API nustato savybes, tokias kaip autentifikavimas, SLA, rinkinys, konkurencijos kontrolė ir klaidų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="1fea7-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="1fea7-122">Dėl bendresnės informacijos apie „Microsoft Dataverse“ žiniatinklio API, žr.:</span><span class="sxs-lookup"><span data-stu-id="1fea7-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="1fea7-123">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="1fea7-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="1fea7-124">Naudokite „Microsoft Dataverse“ žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1fea7-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="1fea7-125">„Microsoft Dataverse“ kūrėjo gairės</span><span class="sxs-lookup"><span data-stu-id="1fea7-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="1fea7-126">Prieš tai buvusi dokumentacija apima išsamią informaciją ir kūrėjo gaires apie „Dataverse“ žiniatinklio API naudojimą, tokias kaip [autentifikavimo valdymas](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [operacijų atlikimas](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) ir [sekimo keitimo naudojimas ir delta žymos](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) su API.</span><span class="sxs-lookup"><span data-stu-id="1fea7-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="1fea7-127">Parinkties rinkiniai</span><span class="sxs-lookup"><span data-stu-id="1fea7-127">Option sets</span></span>

<span data-ttu-id="1fea7-128">Duomenų modelis ATS integravimui API aprašoma šiame dokumente apima parinkčių rinkinius, kurie pateikia numeravimo vertes susietas su objekto ypatybėmis.</span><span class="sxs-lookup"><span data-stu-id="1fea7-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="1fea7-129">Dėl išsamaus darbo su parinkčių rinkianisi „Dataverse“ žiniatinklių API, žr. [Kurti ir naujinti parinkčių rinkinius su žiniatinklio API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="1fea7-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="1fea7-130">Parinkčių rinkiniai yra nustatyti kiekvienai „Dataverse“ aplinkai.</span><span class="sxs-lookup"><span data-stu-id="1fea7-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="1fea7-131">Virtualios lentelės žmogiškiesiems ištekliams „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="1fea7-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="1fea7-132">Galutiniai taškai ATS integravimui API naudoja virtualios lentelės platformos galimybes „Microsoft Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="1fea7-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="1fea7-133">Pagal nutylėjimą, virtualiso lentelės ir jų susieti API galutiniai taškai nėra talpinami žmogiškųjų išteklių aplinkose, įjungiant organizacijas tam, kad jos nustatytų, kurie OData galutiniai taškai turi būti rodomi aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="1fea7-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="1fea7-134">Norėdami naudoti API, virtualio lentelės žmogiškųjų išteklių objektai turi būti sukurti aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="1fea7-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="1fea7-135">Dėl informacijos apie virtualių lentelių kūrimą API, žr. [Konfigūruoti „Dataverse“ virtualias lenteles](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="1fea7-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="1fea7-136">Duomenų modelis</span><span class="sxs-lookup"><span data-stu-id="1fea7-136">Data model</span></span>

<span data-ttu-id="1fea7-137">Duomenų modelis yra sukoncentruotas apie du pagrindinius objektus:</span><span class="sxs-lookup"><span data-stu-id="1fea7-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="1fea7-138">**Samdymo užklausą** rodančią užklausą ATS siekiant pasamdyti asmenis į vieną ar daugiau atvirų pareigų. Dėl užklausos pavyzdžio, žr. [Pavyzdžio užklausa samdymo užklausai](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="1fea7-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="1fea7-139">**Samdomas pretendentas** rodo pretendento išsamią informaciją, kuris priėmė pasiūlymą į pareigas.</span><span class="sxs-lookup"><span data-stu-id="1fea7-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="1fea7-140">**Asmuo** rodo asmenį, kuris yra pretendentas.</span><span class="sxs-lookup"><span data-stu-id="1fea7-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="1fea7-141">Asmuo gali turėti kelis vaidmenis įmonėje, tokius kaip pretendentas, darbuotojas, darbininkas ar rangovas.</span><span class="sxs-lookup"><span data-stu-id="1fea7-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="1fea7-142">Dėl pavyzdžio užklausos, žr. [Pavyzdžio užklausa samdytinam pretendentui](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="1fea7-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="1fea7-143">Tolesnėje diagramoje rodomi santykiai su API.</span><span class="sxs-lookup"><span data-stu-id="1fea7-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="1fea7-144">Keli tipai turi užsienio raktus su kitais, iš anksto esantys objektai žmogiškuosiuose ištekliuose čia nerodomi.</span><span class="sxs-lookup"><span data-stu-id="1fea7-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="1fea7-145">Dokumente pateikta informacija apie objektus, kurie yra būdingi samdymo integravimo scenarijams.</span><span class="sxs-lookup"><span data-stu-id="1fea7-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="1fea7-146">Nepaisant to, esama daugelio kitų objektų „Dataverse“ žiniatinklio API skirtų „Dynamics 365 Human Resources“, kurie gali būti taip pat svarbūs jūsų integravimui.</span><span class="sxs-lookup"><span data-stu-id="1fea7-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="1fea7-147">Pavyzdžiui, jums gali taip pat reikėti išsamios čia nenustatytos informacijos darbuotojams, darbams, pareigoms ar kitiems objektams.</span><span class="sxs-lookup"><span data-stu-id="1fea7-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="1fea7-148">Daugelis šių objektų yra nukreipiami į užsienio raktų santykius ar naršymo ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1fea7-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS integravimo API duomenų modelis](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="1fea7-150">Samdymo užklausa ir susiję objektai bei parinkčių rinkiniai</span><span class="sxs-lookup"><span data-stu-id="1fea7-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="1fea7-151">Pavyzdinė užklausa:</span><span class="sxs-lookup"><span data-stu-id="1fea7-151">Example query:</span></span> 

- [<span data-ttu-id="1fea7-152">Pavyzdinė užklausa Samdymo prašymui</span><span class="sxs-lookup"><span data-stu-id="1fea7-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="1fea7-153">Objektai:</span><span class="sxs-lookup"><span data-stu-id="1fea7-153">Entities:</span></span>

- [<span data-ttu-id="1fea7-154">Įdarbinimo užklausa</span><span class="sxs-lookup"><span data-stu-id="1fea7-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="1fea7-155">Įdarbinimo užklausų pareigos</span><span class="sxs-lookup"><span data-stu-id="1fea7-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="1fea7-156">Samdymo užklausos įgūdžiai</span><span class="sxs-lookup"><span data-stu-id="1fea7-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="1fea7-157">Samdymo užklausos išsilavinimas</span><span class="sxs-lookup"><span data-stu-id="1fea7-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="1fea7-158">Įdarbinimo užklausų vieta</span><span class="sxs-lookup"><span data-stu-id="1fea7-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="1fea7-159">Parinkties rinkiniai:</span><span class="sxs-lookup"><span data-stu-id="1fea7-159">Option sets:</span></span>

- [<span data-ttu-id="1fea7-160">Atleidimo nuo darbo būsena</span><span class="sxs-lookup"><span data-stu-id="1fea7-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="1fea7-161">Samdymo užklausos pareigų būsena</span><span class="sxs-lookup"><span data-stu-id="1fea7-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="1fea7-162">Samdymo užklausos būsena</span><span class="sxs-lookup"><span data-stu-id="1fea7-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="1fea7-163">Reguliavimo darbo kategorija</span><span class="sxs-lookup"><span data-stu-id="1fea7-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="1fea7-164">Samdomas pretendentas ir susiję objektai ir parinkčių rinkiniai</span><span class="sxs-lookup"><span data-stu-id="1fea7-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="1fea7-165">Pavyzdinė užklausa:</span><span class="sxs-lookup"><span data-stu-id="1fea7-165">Example query:</span></span>

- [<span data-ttu-id="1fea7-166">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="1fea7-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="1fea7-167">Objektai:</span><span class="sxs-lookup"><span data-stu-id="1fea7-167">Entities:</span></span>

- [<span data-ttu-id="1fea7-168">Samdytinas pretendentas</span><span class="sxs-lookup"><span data-stu-id="1fea7-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="1fea7-169">Asmuo</span><span class="sxs-lookup"><span data-stu-id="1fea7-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="1fea7-170">Asmens išsilavinimas</span><span class="sxs-lookup"><span data-stu-id="1fea7-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="1fea7-171">Asmens profesinė patirtis</span><span class="sxs-lookup"><span data-stu-id="1fea7-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="1fea7-172">Asmens adresas</span><span class="sxs-lookup"><span data-stu-id="1fea7-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="1fea7-173">Šalies kontaktai</span><span class="sxs-lookup"><span data-stu-id="1fea7-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="1fea7-174">Asmens įgūdžiai</span><span class="sxs-lookup"><span data-stu-id="1fea7-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="1fea7-175">Vertinimo lygis</span><span class="sxs-lookup"><span data-stu-id="1fea7-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="1fea7-176">Asmens sertifiktas</span><span class="sxs-lookup"><span data-stu-id="1fea7-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="1fea7-177">Sertifikato tipas</span><span class="sxs-lookup"><span data-stu-id="1fea7-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="1fea7-178">Asmens atranka</span><span class="sxs-lookup"><span data-stu-id="1fea7-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="1fea7-179">Atrankos tipai</span><span class="sxs-lookup"><span data-stu-id="1fea7-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="1fea7-180">Asmens tapatybės numeris</span><span class="sxs-lookup"><span data-stu-id="1fea7-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="1fea7-181">Parinkties rinkiniai:</span><span class="sxs-lookup"><span data-stu-id="1fea7-181">Option sets:</span></span>

- [<span data-ttu-id="1fea7-182">Pretendento integravimo rezultatas</span><span class="sxs-lookup"><span data-stu-id="1fea7-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="1fea7-183">Tuščia Taip Ne</span><span class="sxs-lookup"><span data-stu-id="1fea7-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="1fea7-184">Užbaigimo būsena</span><span class="sxs-lookup"><span data-stu-id="1fea7-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="1fea7-185">Kontakto tipas</span><span class="sxs-lookup"><span data-stu-id="1fea7-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="1fea7-186">Išsilavinimo kredito pagrindas</span><span class="sxs-lookup"><span data-stu-id="1fea7-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="1fea7-187">Giminė</span><span class="sxs-lookup"><span data-stu-id="1fea7-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="1fea7-188">Šeiminė padėtis</span><span class="sxs-lookup"><span data-stu-id="1fea7-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="1fea7-189">Metų mėnesiai</span><span class="sxs-lookup"><span data-stu-id="1fea7-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="1fea7-190">Ne Taip</span><span class="sxs-lookup"><span data-stu-id="1fea7-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="1fea7-191">Laikotarpio vienetas</span><span class="sxs-lookup"><span data-stu-id="1fea7-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="1fea7-192">Atrankos dažnumas</span><span class="sxs-lookup"><span data-stu-id="1fea7-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="1fea7-193">Atrankos dažnumas sukuriamas pagal</span><span class="sxs-lookup"><span data-stu-id="1fea7-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="1fea7-194">Įgūdžių lygio tipas</span><span class="sxs-lookup"><span data-stu-id="1fea7-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="1fea7-195">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="1fea7-195">See also</span></span>

[<span data-ttu-id="1fea7-196">Kandidatų į darbo vietas įdarbinimas</span><span class="sxs-lookup"><span data-stu-id="1fea7-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="1fea7-197">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="1fea7-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="1fea7-198">Naudokite „Microsoft Dataverse“ žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1fea7-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="1fea7-199">Kurti ir naujinti parinkčių rinkinius naudojant žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1fea7-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>