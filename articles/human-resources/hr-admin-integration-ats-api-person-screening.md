---
title: Asmens atranka
description: Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059285"
---
# <a name="person-screening"></a><span data-ttu-id="8deba-103">Asmens atranka</span><span class="sxs-lookup"><span data-stu-id="8deba-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8deba-104">Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="8deba-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8deba-105">Fizinis pavadinimas: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="8deba-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="8deba-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-106">Description</span></span>

<span data-ttu-id="8deba-107">Šis objektas aprašo atrankas, kurias pretendentas praėjo ar turi praieti dėl samdymo.</span><span class="sxs-lookup"><span data-stu-id="8deba-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8deba-108">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="8deba-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="8deba-109">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="8deba-109">Properties</span></span>

| <span data-ttu-id="8deba-110">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="8deba-110">Property</span></span><br><span data-ttu-id="8deba-111">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="8deba-111">**Physical name**</span></span><br><span data-ttu-id="8deba-112">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="8deba-112">**_Type_**</span></span> | <span data-ttu-id="8deba-113">Naudoti</span><span class="sxs-lookup"><span data-stu-id="8deba-113">Use</span></span> | <span data-ttu-id="8deba-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8deba-115">**Asmens atrankos objekto ID**</span><span class="sxs-lookup"><span data-stu-id="8deba-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="8deba-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="8deba-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="8deba-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8deba-117">*GUID*</span></span> | <span data-ttu-id="8deba-118">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="8deba-118">Read-only</span></span><br><span data-ttu-id="8deba-119">Būtina</span><span class="sxs-lookup"><span data-stu-id="8deba-119">Required</span></span><br><span data-ttu-id="8deba-120">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="8deba-120">System-generated</span></span> | <span data-ttu-id="8deba-121">Unikalus pirminis identifikatorius asmens atrankos įrašui.</span><span class="sxs-lookup"><span data-stu-id="8deba-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="8deba-122">**Šalies numeris**</span><span class="sxs-lookup"><span data-stu-id="8deba-122">**Party Number**</span></span><br><span data-ttu-id="8deba-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="8deba-123">mshr_partynumber</span></span><br><span data-ttu-id="8deba-124">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="8deba-124">*String*</span></span> | <span data-ttu-id="8deba-125">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-125">Read/write</span></span><br><span data-ttu-id="8deba-126">Būtina</span><span class="sxs-lookup"><span data-stu-id="8deba-126">Required</span></span> | <span data-ttu-id="8deba-127">Šalies (asmens) numeris susietas su pretendentu.</span><span class="sxs-lookup"><span data-stu-id="8deba-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="8deba-128">**Asmens ID vertė**</span><span class="sxs-lookup"><span data-stu-id="8deba-128">**Person ID Value**</span></span><br><span data-ttu-id="8deba-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="8deba-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="8deba-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8deba-130">*GUID*</span></span> | <span data-ttu-id="8deba-131">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="8deba-131">Read-only</span></span><br><span data-ttu-id="8deba-132">Būtina</span><span class="sxs-lookup"><span data-stu-id="8deba-132">Required</span></span><br><span data-ttu-id="8deba-133">Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="8deba-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="8deba-134">Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas.</span><span class="sxs-lookup"><span data-stu-id="8deba-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="8deba-135">**Atrankos tipo ID**</span><span class="sxs-lookup"><span data-stu-id="8deba-135">**Screening Type ID**</span></span><br><span data-ttu-id="8deba-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="8deba-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="8deba-137">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="8deba-137">*String*</span></span> | <span data-ttu-id="8deba-138">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-138">Read/write</span></span><br><span data-ttu-id="8deba-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="8deba-139">Required</span></span><br><span data-ttu-id="8deba-140">Užsienio rarktas: atrankos tipas</span><span class="sxs-lookup"><span data-stu-id="8deba-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="8deba-141">Atrankos tipo nustatyto žmogiškuosiuose ištekliuose identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="8deba-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="8deba-142">**Atrankos tipo ID vertė**</span><span class="sxs-lookup"><span data-stu-id="8deba-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="8deba-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="8deba-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="8deba-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8deba-144">*GUID*</span></span> | <span data-ttu-id="8deba-145">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="8deba-145">Read-only</span></span><br><span data-ttu-id="8deba-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="8deba-146">Required</span></span><br><span data-ttu-id="8deba-147">Užsienio raktas: mshr_hcmscreeningtypeentityid mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="8deba-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="8deba-148">Sistemos sukurtas unikalus identifikatorius atrankos tipo įrašui susietame objekte.</span><span class="sxs-lookup"><span data-stu-id="8deba-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="8deba-149">**Prašomas**</span><span class="sxs-lookup"><span data-stu-id="8deba-149">**Required By**</span></span><br><span data-ttu-id="8deba-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="8deba-150">mshr_requiredby</span></span><br><span data-ttu-id="8deba-151">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="8deba-151">*Datetime*</span></span> | <span data-ttu-id="8deba-152">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-152">Read/write</span></span><br><span data-ttu-id="8deba-153">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="8deba-153">Optional</span></span> | <span data-ttu-id="8deba-154">Diena, kurią atranka turi būti baigta.</span><span class="sxs-lookup"><span data-stu-id="8deba-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="8deba-155">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="8deba-155">**Status**</span></span><br><span data-ttu-id="8deba-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="8deba-156">mshr_status</span></span><br><span data-ttu-id="8deba-157">*mshr_hcmcompletionstatus parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="8deba-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="8deba-158">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-158">Read/write</span></span><br><span data-ttu-id="8deba-159">Būtina</span><span class="sxs-lookup"><span data-stu-id="8deba-159">Required</span></span> | <span data-ttu-id="8deba-160">Suteikia pretendento statusą atrankai.</span><span class="sxs-lookup"><span data-stu-id="8deba-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="8deba-161">**Užbaigimo data**</span><span class="sxs-lookup"><span data-stu-id="8deba-161">**Completed Date**</span></span><br><span data-ttu-id="8deba-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="8deba-162">mshr_completeddate</span></span><br><span data-ttu-id="8deba-163">*Data laikas*</span><span class="sxs-lookup"><span data-stu-id="8deba-163">*Datetime*</span></span> | <span data-ttu-id="8deba-164">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-164">Read/write</span></span><br><span data-ttu-id="8deba-165">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="8deba-165">Optional</span></span> | <span data-ttu-id="8deba-166">Data, kai atranka buvo užbaigta.</span><span class="sxs-lookup"><span data-stu-id="8deba-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="8deba-167">**Pastabos**</span><span class="sxs-lookup"><span data-stu-id="8deba-167">**Notes**</span></span><br><span data-ttu-id="8deba-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="8deba-168">mshr_note</span></span><br><span data-ttu-id="8deba-169">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="8deba-169">*String*</span></span> | <span data-ttu-id="8deba-170">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="8deba-170">Read/write</span></span><br><span data-ttu-id="8deba-171">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="8deba-171">Optional</span></span> | <span data-ttu-id="8deba-172">Komentarai, kuriuos naudoja vadovai ar samdantys asmenys.</span><span class="sxs-lookup"><span data-stu-id="8deba-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8deba-173">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="8deba-173">See also</span></span>

[<span data-ttu-id="8deba-174">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="8deba-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8deba-175">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="8deba-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]