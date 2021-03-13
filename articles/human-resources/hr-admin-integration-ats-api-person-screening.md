---
title: Asmens atranka
description: Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125382"
---
# <a name="person-screening"></a><span data-ttu-id="deb5b-103">Asmens atranka</span><span class="sxs-lookup"><span data-stu-id="deb5b-103">Person screening</span></span>

<span data-ttu-id="deb5b-104">Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="deb5b-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="deb5b-105">Fizinis pavadinimas: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="deb5b-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="deb5b-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-106">Description</span></span>

<span data-ttu-id="deb5b-107">Šis objektas aprašo atrankas, kurias pretendentas praėjo ar turi praieti dėl samdymo.</span><span class="sxs-lookup"><span data-stu-id="deb5b-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="deb5b-108">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="deb5b-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="deb5b-109">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="deb5b-109">Properties</span></span>

| <span data-ttu-id="deb5b-110">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="deb5b-110">Property</span></span><br><span data-ttu-id="deb5b-111">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="deb5b-111">**Physical name**</span></span><br><span data-ttu-id="deb5b-112">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="deb5b-112">**_Type_**</span></span> | <span data-ttu-id="deb5b-113">Naudoti</span><span class="sxs-lookup"><span data-stu-id="deb5b-113">Use</span></span> | <span data-ttu-id="deb5b-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="deb5b-115">**Asmens atrankos objekto ID**</span><span class="sxs-lookup"><span data-stu-id="deb5b-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="deb5b-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="deb5b-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="deb5b-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="deb5b-117">*GUID*</span></span> | <span data-ttu-id="deb5b-118">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="deb5b-118">Read-only</span></span><br><span data-ttu-id="deb5b-119">Būtina</span><span class="sxs-lookup"><span data-stu-id="deb5b-119">Required</span></span><br><span data-ttu-id="deb5b-120">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="deb5b-120">System-generated</span></span> | <span data-ttu-id="deb5b-121">Unikalus pirminis identifikatorius asmens atrankos įrašui.</span><span class="sxs-lookup"><span data-stu-id="deb5b-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="deb5b-122">**Šalies numeris**</span><span class="sxs-lookup"><span data-stu-id="deb5b-122">**Party Number**</span></span><br><span data-ttu-id="deb5b-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="deb5b-123">mshr_partynumber</span></span><br><span data-ttu-id="deb5b-124">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="deb5b-124">*String*</span></span> | <span data-ttu-id="deb5b-125">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-125">Read/write</span></span><br><span data-ttu-id="deb5b-126">Būtina</span><span class="sxs-lookup"><span data-stu-id="deb5b-126">Required</span></span> | <span data-ttu-id="deb5b-127">Šalies (asmens) numeris susietas su pretendentu.</span><span class="sxs-lookup"><span data-stu-id="deb5b-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="deb5b-128">**Asmens ID vertė**</span><span class="sxs-lookup"><span data-stu-id="deb5b-128">**Person ID Value**</span></span><br><span data-ttu-id="deb5b-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="deb5b-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="deb5b-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="deb5b-130">*GUID*</span></span> | <span data-ttu-id="deb5b-131">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="deb5b-131">Read-only</span></span><br><span data-ttu-id="deb5b-132">Būtina</span><span class="sxs-lookup"><span data-stu-id="deb5b-132">Required</span></span><br><span data-ttu-id="deb5b-133">Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="deb5b-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="deb5b-134">Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas.</span><span class="sxs-lookup"><span data-stu-id="deb5b-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="deb5b-135">**Atrankos tipo ID**</span><span class="sxs-lookup"><span data-stu-id="deb5b-135">**Screening Type ID**</span></span><br><span data-ttu-id="deb5b-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="deb5b-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="deb5b-137">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="deb5b-137">*String*</span></span> | <span data-ttu-id="deb5b-138">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-138">Read/write</span></span><br><span data-ttu-id="deb5b-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="deb5b-139">Required</span></span><br><span data-ttu-id="deb5b-140">Užsienio rarktas: atrankos tipas</span><span class="sxs-lookup"><span data-stu-id="deb5b-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="deb5b-141">Atrankos tipo nustatyto žmogiškuosiuose ištekliuose identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="deb5b-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="deb5b-142">**Atrankos tipo ID vertė**</span><span class="sxs-lookup"><span data-stu-id="deb5b-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="deb5b-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="deb5b-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="deb5b-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="deb5b-144">*GUID*</span></span> | <span data-ttu-id="deb5b-145">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="deb5b-145">Read-only</span></span><br><span data-ttu-id="deb5b-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="deb5b-146">Required</span></span><br><span data-ttu-id="deb5b-147">Užsienio raktas: mshr_hcmscreeningtypeentityid mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="deb5b-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="deb5b-148">Sistemos sukurtas unikalus identifikatorius atrankos tipo įrašui susietame objekte.</span><span class="sxs-lookup"><span data-stu-id="deb5b-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="deb5b-149">**Prašomas**</span><span class="sxs-lookup"><span data-stu-id="deb5b-149">**Required By**</span></span><br><span data-ttu-id="deb5b-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="deb5b-150">mshr_requiredby</span></span><br><span data-ttu-id="deb5b-151">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="deb5b-151">*Datetime*</span></span> | <span data-ttu-id="deb5b-152">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-152">Read/write</span></span><br><span data-ttu-id="deb5b-153">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="deb5b-153">Optional</span></span> | <span data-ttu-id="deb5b-154">Diena, kurią atranka turi būti baigta.</span><span class="sxs-lookup"><span data-stu-id="deb5b-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="deb5b-155">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="deb5b-155">**Status**</span></span><br><span data-ttu-id="deb5b-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="deb5b-156">mshr_status</span></span><br><span data-ttu-id="deb5b-157">*mshr_hcmcompletionstatus parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="deb5b-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="deb5b-158">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-158">Read/write</span></span><br><span data-ttu-id="deb5b-159">Būtina</span><span class="sxs-lookup"><span data-stu-id="deb5b-159">Required</span></span> | <span data-ttu-id="deb5b-160">Suteikia pretendento statusą atrankai.</span><span class="sxs-lookup"><span data-stu-id="deb5b-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="deb5b-161">**Užbaigimo data**</span><span class="sxs-lookup"><span data-stu-id="deb5b-161">**Completed Date**</span></span><br><span data-ttu-id="deb5b-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="deb5b-162">mshr_completeddate</span></span><br><span data-ttu-id="deb5b-163">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="deb5b-163">*Datetime*</span></span> | <span data-ttu-id="deb5b-164">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-164">Read/write</span></span><br><span data-ttu-id="deb5b-165">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="deb5b-165">Optional</span></span> | <span data-ttu-id="deb5b-166">Data, kai atranka buvo užbaigta.</span><span class="sxs-lookup"><span data-stu-id="deb5b-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="deb5b-167">**Pastabos**</span><span class="sxs-lookup"><span data-stu-id="deb5b-167">**Notes**</span></span><br><span data-ttu-id="deb5b-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="deb5b-168">mshr_note</span></span><br><span data-ttu-id="deb5b-169">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="deb5b-169">*String*</span></span> | <span data-ttu-id="deb5b-170">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="deb5b-170">Read/write</span></span><br><span data-ttu-id="deb5b-171">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="deb5b-171">Optional</span></span> | <span data-ttu-id="deb5b-172">Komentarai, kuriuos naudoja vadovai ar samdantys asmenys.</span><span class="sxs-lookup"><span data-stu-id="deb5b-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="deb5b-173">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="deb5b-173">See also</span></span>

[<span data-ttu-id="deb5b-174">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="deb5b-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="deb5b-175">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="deb5b-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

