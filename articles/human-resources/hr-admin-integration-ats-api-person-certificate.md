---
title: Asmens sertifiktas
description: Šioje temoje aprašomas asmens sertifikato objektas „Dynamics 365 Human Resources“.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055201"
---
# <a name="person-certificate"></a><span data-ttu-id="29b69-103">Asmens sertifiktas</span><span class="sxs-lookup"><span data-stu-id="29b69-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="29b69-104">Šioje temoje aprašomas asmens sertifikato objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="29b69-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="29b69-105">Fizinis pavadinimas: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="29b69-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="29b69-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-106">Description</span></span>

<span data-ttu-id="29b69-107">Šis objektas aprašo profesinius kandidato sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="29b69-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="29b69-108">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="29b69-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="29b69-109">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="29b69-109">Properties</span></span>

| <span data-ttu-id="29b69-110">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="29b69-110">Property</span></span><br><span data-ttu-id="29b69-111">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="29b69-111">**Physical name**</span></span><br><span data-ttu-id="29b69-112">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="29b69-112">**_Type_**</span></span> | <span data-ttu-id="29b69-113">Naudoti</span><span class="sxs-lookup"><span data-stu-id="29b69-113">Use</span></span> | <span data-ttu-id="29b69-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="29b69-115">**Asmens sertifikato objekto ID**</span><span class="sxs-lookup"><span data-stu-id="29b69-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="29b69-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="29b69-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="29b69-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="29b69-117">*GUID*</span></span> | <span data-ttu-id="29b69-118">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="29b69-118">Read-only</span></span><br><span data-ttu-id="29b69-119">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-119">Required</span></span> | <span data-ttu-id="29b69-120">Sistemos sukurtas unikalus identifikatorius asmens sertifikato objekto įrašui.</span><span class="sxs-lookup"><span data-stu-id="29b69-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="29b69-121">**Šalies numeris**</span><span class="sxs-lookup"><span data-stu-id="29b69-121">**Party Number**</span></span><br><span data-ttu-id="29b69-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="29b69-122">mshr_partynumber</span></span><br><span data-ttu-id="29b69-123">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="29b69-123">*String*</span></span> | <span data-ttu-id="29b69-124">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-124">Read/write</span></span><br><span data-ttu-id="29b69-125">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-125">Required</span></span> | <span data-ttu-id="29b69-126">Šalies (asmens) kandidato ID.</span><span class="sxs-lookup"><span data-stu-id="29b69-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="29b69-127">**Asmens ID vertė**</span><span class="sxs-lookup"><span data-stu-id="29b69-127">**Person ID Value**</span></span><br><span data-ttu-id="29b69-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="29b69-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="29b69-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="29b69-129">*GUID*</span></span> | <span data-ttu-id="29b69-130">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="29b69-130">Read-only</span></span><br><span data-ttu-id="29b69-131">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-131">Required</span></span><br><span data-ttu-id="29b69-132">Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="29b69-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="29b69-133">Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas.</span><span class="sxs-lookup"><span data-stu-id="29b69-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="29b69-134">**Sertifikato tipo ID**</span><span class="sxs-lookup"><span data-stu-id="29b69-134">**Certificate Type ID**</span></span><br><span data-ttu-id="29b69-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="29b69-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="29b69-136">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="29b69-136">*String*</span></span> | <span data-ttu-id="29b69-137">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-137">Read/write</span></span><br><span data-ttu-id="29b69-138">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-138">Required</span></span> |  <span data-ttu-id="29b69-139">Sertifikato tipo nustatyto žmogiškuosiuose ištekliuose identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="29b69-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="29b69-140">**Sertifikato tipo ID vertė**</span><span class="sxs-lookup"><span data-stu-id="29b69-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="29b69-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="29b69-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="29b69-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="29b69-142">*GUID*</span></span> | <span data-ttu-id="29b69-143">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="29b69-143">Read-only</span></span><br><span data-ttu-id="29b69-144">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-144">Required</span></span><br><span data-ttu-id="29b69-145">Užsienio raktas: mshr_hcmcertificatetypeentityid mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="29b69-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="29b69-146">Sistemos sukurtas unikalus identifikatorius sertifikato tipui susietame objekte.</span><span class="sxs-lookup"><span data-stu-id="29b69-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="29b69-147">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="29b69-147">**Start Date**</span></span><br><span data-ttu-id="29b69-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="29b69-148">mshr_startdate</span></span><br><span data-ttu-id="29b69-149">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="29b69-149">*Datetime*</span></span> | <span data-ttu-id="29b69-150">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-150">Read/write</span></span><br><span data-ttu-id="29b69-151">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-151">Required</span></span> | <span data-ttu-id="29b69-152">Sertifikato išdavimo data.</span><span class="sxs-lookup"><span data-stu-id="29b69-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="29b69-153">**Pabaigos data**</span><span class="sxs-lookup"><span data-stu-id="29b69-153">**End Date**</span></span><br><span data-ttu-id="29b69-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="29b69-154">mshr_enddate</span></span><br><span data-ttu-id="29b69-155">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="29b69-155">*Datetime*</span></span> | <span data-ttu-id="29b69-156">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-156">Read/write</span></span><br><span data-ttu-id="29b69-157">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="29b69-157">Optional</span></span> | <span data-ttu-id="29b69-158">Data, kada sertifikatas nustos galioti.</span><span class="sxs-lookup"><span data-stu-id="29b69-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="29b69-159">**Pastabos**</span><span class="sxs-lookup"><span data-stu-id="29b69-159">**Notes**</span></span><br><span data-ttu-id="29b69-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="29b69-160">mshr_notes</span></span><br><span data-ttu-id="29b69-161">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="29b69-161">*String*</span></span> | <span data-ttu-id="29b69-162">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="29b69-162">Read/write</span></span><br><span data-ttu-id="29b69-163">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="29b69-163">Optional</span></span> | <span data-ttu-id="29b69-164">Komentarai, kuriuos naudoja vadovai ar samdantys asmenys.</span><span class="sxs-lookup"><span data-stu-id="29b69-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="29b69-165">**Pirminis laukelis**</span><span class="sxs-lookup"><span data-stu-id="29b69-165">**Primary Field**</span></span><br><span data-ttu-id="29b69-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="29b69-166">mshr_primaryfield</span></span><br><span data-ttu-id="29b69-167">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="29b69-167">*String*</span></span> | <span data-ttu-id="29b69-168">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="29b69-168">Read-only</span></span><br><span data-ttu-id="29b69-169">Būtina</span><span class="sxs-lookup"><span data-stu-id="29b69-169">Required</span></span> |  <span data-ttu-id="29b69-170">Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="29b69-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="29b69-171">Šalies numerio, sertifikato tipo ID ir pradžios datos derinys.</span><span class="sxs-lookup"><span data-stu-id="29b69-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="29b69-172">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="29b69-172">See also</span></span>

[<span data-ttu-id="29b69-173">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="29b69-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="29b69-174">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="29b69-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]