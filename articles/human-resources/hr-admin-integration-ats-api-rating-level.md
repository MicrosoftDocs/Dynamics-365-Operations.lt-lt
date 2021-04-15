---
title: Vertinimo lygis
description: Šioje temoje aprašomas reitingavimo lygio objektas „Dynamics 365 Human Resources“.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800338"
---
# <a name="rating-level"></a><span data-ttu-id="dfd9e-103">Vertinimo lygis</span><span class="sxs-lookup"><span data-stu-id="dfd9e-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dfd9e-104">Šioje temoje aprašomas reitingavimo lygio objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="dfd9e-105">Fizinis pavadinimas: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="dfd9e-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="dfd9e-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-106">Description</span></span>

<span data-ttu-id="dfd9e-107">Šis objektas suteikia reitingavimo lygių galimybę įgūdžiams.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="dfd9e-108">Reitingavimo lygiai taikomi visiems juridiniams objektams.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dfd9e-109">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="dfd9e-110">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="dfd9e-110">Properties</span></span>

| <span data-ttu-id="dfd9e-111">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="dfd9e-111">Property</span></span><br><span data-ttu-id="dfd9e-112">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-112">**Physical name**</span></span><br><span data-ttu-id="dfd9e-113">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-113">**_Type_**</span></span> | <span data-ttu-id="dfd9e-114">Naudoti</span><span class="sxs-lookup"><span data-stu-id="dfd9e-114">Use</span></span> | <span data-ttu-id="dfd9e-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dfd9e-116">**Reitingo lygio objekto ID**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="dfd9e-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="dfd9e-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="dfd9e-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-118">*GUID*</span></span> | <span data-ttu-id="dfd9e-119">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-119">Read-only</span></span><br><span data-ttu-id="dfd9e-120">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-120">Required</span></span><br><span data-ttu-id="dfd9e-121">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="dfd9e-121">System-generated</span></span> | <span data-ttu-id="dfd9e-122">Sistemos sukurtas unikalus identifikatorius lygiui.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="dfd9e-123">**Reitingo lygio ID**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-123">**Rating Level ID**</span></span><br><span data-ttu-id="dfd9e-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="dfd9e-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="dfd9e-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-125">*String*</span></span> | <span data-ttu-id="dfd9e-126">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-126">Read/write</span></span><br><span data-ttu-id="dfd9e-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-127">Required</span></span> | <span data-ttu-id="dfd9e-128">Vartotojo perskaitomas unikalus identifikatorius lygiui.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="dfd9e-129">**Reitingo modelio ID**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-129">**Rating Model ID**</span></span><br><span data-ttu-id="dfd9e-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="dfd9e-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="dfd9e-131">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-131">*String*</span></span> | <span data-ttu-id="dfd9e-132">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-132">Read/write</span></span><br><span data-ttu-id="dfd9e-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-133">Required</span></span> | <span data-ttu-id="dfd9e-134">Reitingavimo modelis, kuriam reitigavimo lygis priklauso.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="dfd9e-135">**Reitingo modelio objekto ID**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="dfd9e-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="dfd9e-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="dfd9e-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-137">*GUID*</span></span> | <span data-ttu-id="dfd9e-138">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-138">Read-only</span></span><br><span data-ttu-id="dfd9e-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-139">Required</span></span><br><span data-ttu-id="dfd9e-140">Užsienio raktas: mshr_hcmratingmodelentityid mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="dfd9e-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="dfd9e-141">Sistemos sukurtas identifikatorius reitingavimo modeliui, kuriam reitingavimo lygis priklauso.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="dfd9e-142">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-142">**Description**</span></span><br><span data-ttu-id="dfd9e-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="dfd9e-143">mshr_description</span></span><br><span data-ttu-id="dfd9e-144">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-144">*String*</span></span> | <span data-ttu-id="dfd9e-145">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-145">Read/write</span></span><br><span data-ttu-id="dfd9e-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-146">Required</span></span> | <span data-ttu-id="dfd9e-147">Reitingavimo lygio aprašas.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-147">The description of the rating level.</span></span> |
| <span data-ttu-id="dfd9e-148">**Koeficientas**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-148">**Factor**</span></span><br><span data-ttu-id="dfd9e-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="dfd9e-149">mshr_factor</span></span><br><span data-ttu-id="dfd9e-150">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-150">*Integer*</span></span> | <span data-ttu-id="dfd9e-151">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-151">Read/write</span></span><br><span data-ttu-id="dfd9e-152">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-152">Required</span></span> | <span data-ttu-id="dfd9e-153">Reitingavimo lygio faktorius.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-153">The factor for the rating level.</span></span> <span data-ttu-id="dfd9e-154">Jums lyginant prekes su skirtingais reitingavimo lygio skaičiais, faktorius yra naudojamas siekiant normalizuoti balus.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="dfd9e-155">Vertė turi būti integruojama nuo 0 iki 9.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="dfd9e-156">**Pastaba**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-156">**Note**</span></span><br><span data-ttu-id="dfd9e-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="dfd9e-157">mshr_note</span></span><br><span data-ttu-id="dfd9e-158">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-158">*String*</span></span> | <span data-ttu-id="dfd9e-159">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-159">Read/write</span></span><br><span data-ttu-id="dfd9e-160">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="dfd9e-160">Optional</span></span> | <span data-ttu-id="dfd9e-161">Bet kokios pastabos susijusios su reitingavimo lygiu.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="dfd9e-162">**Pirminis laukelis**</span><span class="sxs-lookup"><span data-stu-id="dfd9e-162">**Primary Field**</span></span><br><span data-ttu-id="dfd9e-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="dfd9e-163">mshr_primaryfield</span></span><br><span data-ttu-id="dfd9e-164">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="dfd9e-164">*String*</span></span> | <span data-ttu-id="dfd9e-165">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="dfd9e-165">Read-only</span></span><br><span data-ttu-id="dfd9e-166">Būtina</span><span class="sxs-lookup"><span data-stu-id="dfd9e-166">Required</span></span> | <span data-ttu-id="dfd9e-167">Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="dfd9e-168">Reitingavimo lygio ID derinys ir reitingavimo modelio ID.</span><span class="sxs-lookup"><span data-stu-id="dfd9e-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="dfd9e-169">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="dfd9e-169">See also</span></span>

[<span data-ttu-id="dfd9e-170">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="dfd9e-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="dfd9e-171">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="dfd9e-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]