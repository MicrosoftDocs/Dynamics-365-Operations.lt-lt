---
title: Asmens sertifiktas
description: Šioje temoje aprašomas asmens sertifikato objektas „Dynamics 365 Human Resources“.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
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
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466525"
---
# <a name="person-certificate"></a><span data-ttu-id="35448-103">Asmens sertifiktas</span><span class="sxs-lookup"><span data-stu-id="35448-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="35448-104">Šioje temoje aprašomas asmens sertifikato objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="35448-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="35448-105">Fizinis pavadinimas: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="35448-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="35448-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="35448-106">Description</span></span>

<span data-ttu-id="35448-107">Šis objektas aprašo profesinius kandidato sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="35448-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="35448-108">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="35448-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="35448-109">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="35448-109">Properties</span></span>

| <span data-ttu-id="35448-110">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="35448-110">Property</span></span><br><span data-ttu-id="35448-111">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="35448-111">**Physical name**</span></span><br><span data-ttu-id="35448-112">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="35448-112">**_Type_**</span></span> | <span data-ttu-id="35448-113">Naudoti</span><span class="sxs-lookup"><span data-stu-id="35448-113">Use</span></span> | <span data-ttu-id="35448-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="35448-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="35448-115">**Asmens sertifikato objekto ID**</span><span class="sxs-lookup"><span data-stu-id="35448-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="35448-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="35448-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="35448-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="35448-117">*GUID*</span></span> | <span data-ttu-id="35448-118">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="35448-118">Read-only</span></span><br><span data-ttu-id="35448-119">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-119">Required</span></span> | <span data-ttu-id="35448-120">Sistemos sukurtas unikalus identifikatorius asmens sertifikato objekto įrašui.</span><span class="sxs-lookup"><span data-stu-id="35448-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="35448-121">**Šalies numeris**</span><span class="sxs-lookup"><span data-stu-id="35448-121">**Party Number**</span></span><br><span data-ttu-id="35448-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="35448-122">mshr_partynumber</span></span><br><span data-ttu-id="35448-123">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="35448-123">*String*</span></span> | <span data-ttu-id="35448-124">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="35448-124">Read/write</span></span><br><span data-ttu-id="35448-125">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-125">Required</span></span> | <span data-ttu-id="35448-126">Šalies (asmens) kandidato ID.</span><span class="sxs-lookup"><span data-stu-id="35448-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="35448-127">**Asmens ID vertė**</span><span class="sxs-lookup"><span data-stu-id="35448-127">**Person ID Value**</span></span><br><span data-ttu-id="35448-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="35448-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="35448-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="35448-129">*GUID*</span></span> | <span data-ttu-id="35448-130">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="35448-130">Read-only</span></span><br><span data-ttu-id="35448-131">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-131">Required</span></span><br><span data-ttu-id="35448-132">Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="35448-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="35448-133">Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas.</span><span class="sxs-lookup"><span data-stu-id="35448-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="35448-134">**Sertifikato tipo ID**</span><span class="sxs-lookup"><span data-stu-id="35448-134">**Certificate Type ID**</span></span><br><span data-ttu-id="35448-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="35448-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="35448-136">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="35448-136">*String*</span></span> | <span data-ttu-id="35448-137">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="35448-137">Read/write</span></span><br><span data-ttu-id="35448-138">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-138">Required</span></span> |  <span data-ttu-id="35448-139">Sertifikato tipo nustatyto žmogiškuosiuose ištekliuose identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="35448-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="35448-140">**Sertifikato tipo ID vertė**</span><span class="sxs-lookup"><span data-stu-id="35448-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="35448-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="35448-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="35448-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="35448-142">*GUID*</span></span> | <span data-ttu-id="35448-143">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="35448-143">Read-only</span></span><br><span data-ttu-id="35448-144">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-144">Required</span></span><br><span data-ttu-id="35448-145">Užsienio raktas: mshr_hcmcertificatetypeentityid mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="35448-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="35448-146">Sistemos sukurtas unikalus identifikatorius sertifikato tipui susietame objekte.</span><span class="sxs-lookup"><span data-stu-id="35448-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="35448-147">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="35448-147">**Start Date**</span></span><br><span data-ttu-id="35448-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="35448-148">mshr_startdate</span></span><br><span data-ttu-id="35448-149">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="35448-149">*Datetime*</span></span> | <span data-ttu-id="35448-150">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="35448-150">Read/write</span></span><br><span data-ttu-id="35448-151">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-151">Required</span></span> | <span data-ttu-id="35448-152">Sertifikato išdavimo data.</span><span class="sxs-lookup"><span data-stu-id="35448-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="35448-153">**Pabaigos data**</span><span class="sxs-lookup"><span data-stu-id="35448-153">**End Date**</span></span><br><span data-ttu-id="35448-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="35448-154">mshr_enddate</span></span><br><span data-ttu-id="35448-155">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="35448-155">*Datetime*</span></span> | <span data-ttu-id="35448-156">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="35448-156">Read/write</span></span><br><span data-ttu-id="35448-157">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="35448-157">Optional</span></span> | <span data-ttu-id="35448-158">Data, kada sertifikatas nustos galioti.</span><span class="sxs-lookup"><span data-stu-id="35448-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="35448-159">**Pastabos**</span><span class="sxs-lookup"><span data-stu-id="35448-159">**Notes**</span></span><br><span data-ttu-id="35448-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="35448-160">mshr_notes</span></span><br><span data-ttu-id="35448-161">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="35448-161">*String*</span></span> | <span data-ttu-id="35448-162">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="35448-162">Read/write</span></span><br><span data-ttu-id="35448-163">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="35448-163">Optional</span></span> | <span data-ttu-id="35448-164">Komentarai, kuriuos naudoja vadovai ar samdantys asmenys.</span><span class="sxs-lookup"><span data-stu-id="35448-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="35448-165">**Pirminis laukelis**</span><span class="sxs-lookup"><span data-stu-id="35448-165">**Primary Field**</span></span><br><span data-ttu-id="35448-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="35448-166">mshr_primaryfield</span></span><br><span data-ttu-id="35448-167">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="35448-167">*String*</span></span> | <span data-ttu-id="35448-168">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="35448-168">Read-only</span></span><br><span data-ttu-id="35448-169">Būtina</span><span class="sxs-lookup"><span data-stu-id="35448-169">Required</span></span> |  <span data-ttu-id="35448-170">Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="35448-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="35448-171">Šalies numerio, sertifikato tipo ID ir pradžios datos derinys.</span><span class="sxs-lookup"><span data-stu-id="35448-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="35448-172">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="35448-172">See also</span></span>

[<span data-ttu-id="35448-173">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="35448-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="35448-174">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="35448-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]