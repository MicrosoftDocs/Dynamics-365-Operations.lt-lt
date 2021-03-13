---
title: Vertinimo lygis
description: Šioje temoje aprašomas reitingavimo lygio objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125262"
---
# <a name="rating-level"></a><span data-ttu-id="e1532-103">Vertinimo lygis</span><span class="sxs-lookup"><span data-stu-id="e1532-103">Rating level</span></span>

<span data-ttu-id="e1532-104">Šioje temoje aprašomas reitingavimo lygio objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="e1532-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e1532-105">Fizinis pavadinimas: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="e1532-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="e1532-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-106">Description</span></span>

<span data-ttu-id="e1532-107">Šis objektas suteikia reitingavimo lygių galimybę įgūdžiams.</span><span class="sxs-lookup"><span data-stu-id="e1532-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="e1532-108">Reitingavimo lygiai taikomi visiems juridiniams objektams.</span><span class="sxs-lookup"><span data-stu-id="e1532-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e1532-109">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="e1532-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="e1532-110">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="e1532-110">Properties</span></span>

| <span data-ttu-id="e1532-111">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="e1532-111">Property</span></span><br><span data-ttu-id="e1532-112">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="e1532-112">**Physical name**</span></span><br><span data-ttu-id="e1532-113">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="e1532-113">**_Type_**</span></span> | <span data-ttu-id="e1532-114">Naudoti</span><span class="sxs-lookup"><span data-stu-id="e1532-114">Use</span></span> | <span data-ttu-id="e1532-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e1532-116">**Reitingo lygio objekto ID**</span><span class="sxs-lookup"><span data-stu-id="e1532-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="e1532-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="e1532-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="e1532-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e1532-118">*GUID*</span></span> | <span data-ttu-id="e1532-119">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="e1532-119">Read-only</span></span><br><span data-ttu-id="e1532-120">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-120">Required</span></span><br><span data-ttu-id="e1532-121">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="e1532-121">System-generated</span></span> | <span data-ttu-id="e1532-122">Sistemos sukurtas unikalus identifikatorius lygiui.</span><span class="sxs-lookup"><span data-stu-id="e1532-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="e1532-123">**Reitingo lygio ID**</span><span class="sxs-lookup"><span data-stu-id="e1532-123">**Rating Level ID**</span></span><br><span data-ttu-id="e1532-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="e1532-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="e1532-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e1532-125">*String*</span></span> | <span data-ttu-id="e1532-126">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-126">Read/write</span></span><br><span data-ttu-id="e1532-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-127">Required</span></span> | <span data-ttu-id="e1532-128">Vartotojo perskaitomas unikalus identifikatorius lygiui.</span><span class="sxs-lookup"><span data-stu-id="e1532-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="e1532-129">**Reitingo modelio ID**</span><span class="sxs-lookup"><span data-stu-id="e1532-129">**Rating Model ID**</span></span><br><span data-ttu-id="e1532-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="e1532-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="e1532-131">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e1532-131">*String*</span></span> | <span data-ttu-id="e1532-132">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-132">Read/write</span></span><br><span data-ttu-id="e1532-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-133">Required</span></span> | <span data-ttu-id="e1532-134">Reitingavimo modelis, kuriam reitigavimo lygis priklauso.</span><span class="sxs-lookup"><span data-stu-id="e1532-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="e1532-135">**Reitingo modelio objekto ID**</span><span class="sxs-lookup"><span data-stu-id="e1532-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="e1532-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="e1532-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="e1532-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e1532-137">*GUID*</span></span> | <span data-ttu-id="e1532-138">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="e1532-138">Read-only</span></span><br><span data-ttu-id="e1532-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-139">Required</span></span><br><span data-ttu-id="e1532-140">Užsienio raktas: mshr_hcmratingmodelentityid mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="e1532-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="e1532-141">Sistemos sukurtas identifikatorius reitingavimo modeliui, kuriam reitingavimo lygis priklauso.</span><span class="sxs-lookup"><span data-stu-id="e1532-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="e1532-142">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="e1532-142">**Description**</span></span><br><span data-ttu-id="e1532-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="e1532-143">mshr_description</span></span><br><span data-ttu-id="e1532-144">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e1532-144">*String*</span></span> | <span data-ttu-id="e1532-145">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-145">Read/write</span></span><br><span data-ttu-id="e1532-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-146">Required</span></span> | <span data-ttu-id="e1532-147">Reitingavimo lygio aprašas.</span><span class="sxs-lookup"><span data-stu-id="e1532-147">The description of the rating level.</span></span> |
| <span data-ttu-id="e1532-148">**Koeficientas**</span><span class="sxs-lookup"><span data-stu-id="e1532-148">**Factor**</span></span><br><span data-ttu-id="e1532-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="e1532-149">mshr_factor</span></span><br><span data-ttu-id="e1532-150">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="e1532-150">*Integer*</span></span> | <span data-ttu-id="e1532-151">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-151">Read/write</span></span><br><span data-ttu-id="e1532-152">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-152">Required</span></span> | <span data-ttu-id="e1532-153">Reitingavimo lygio faktorius.</span><span class="sxs-lookup"><span data-stu-id="e1532-153">The factor for the rating level.</span></span> <span data-ttu-id="e1532-154">Jums lyginant prekes su skirtingais reitingavimo lygio skaičiais, faktorius yra naudojamas siekiant normalizuoti balus.</span><span class="sxs-lookup"><span data-stu-id="e1532-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="e1532-155">Vertė turi būti integruojama nuo 0 iki 9.</span><span class="sxs-lookup"><span data-stu-id="e1532-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="e1532-156">**Pastaba**</span><span class="sxs-lookup"><span data-stu-id="e1532-156">**Note**</span></span><br><span data-ttu-id="e1532-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="e1532-157">mshr_note</span></span><br><span data-ttu-id="e1532-158">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e1532-158">*String*</span></span> | <span data-ttu-id="e1532-159">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="e1532-159">Read/write</span></span><br><span data-ttu-id="e1532-160">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="e1532-160">Optional</span></span> | <span data-ttu-id="e1532-161">Bet kokios pastabos susijusios su reitingavimo lygiu.</span><span class="sxs-lookup"><span data-stu-id="e1532-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="e1532-162">**Pirminis laukelis**</span><span class="sxs-lookup"><span data-stu-id="e1532-162">**Primary Field**</span></span><br><span data-ttu-id="e1532-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e1532-163">mshr_primaryfield</span></span><br><span data-ttu-id="e1532-164">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e1532-164">*String*</span></span> | <span data-ttu-id="e1532-165">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="e1532-165">Read-only</span></span><br><span data-ttu-id="e1532-166">Būtina</span><span class="sxs-lookup"><span data-stu-id="e1532-166">Required</span></span> | <span data-ttu-id="e1532-167">Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="e1532-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="e1532-168">Reitingavimo lygio ID derinys ir reitingavimo modelio ID.</span><span class="sxs-lookup"><span data-stu-id="e1532-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e1532-169">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="e1532-169">See also</span></span>

[<span data-ttu-id="e1532-170">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="e1532-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e1532-171">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="e1532-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

