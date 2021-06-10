---
title: Atrankos tipai
description: Šioje temoje aprašomas atrankų tipų objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 2acb99c2fb57df883ab376c7f6aab547073bd0ff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058301"
---
# <a name="screening-types"></a><span data-ttu-id="5948f-103">Atrankos tipai</span><span class="sxs-lookup"><span data-stu-id="5948f-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5948f-104">Šioje temoje aprašomas atrankų tipų objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="5948f-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5948f-105">Fizinis pavadinimas: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="5948f-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="5948f-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-106">Description</span></span>

<span data-ttu-id="5948f-107">Šis objektas aprašo atrankų tipus, kurie nustatyti bendrovės išankstiniam įdarbinimui ir vykstančiam darbuotojų atrankos procesams.</span><span class="sxs-lookup"><span data-stu-id="5948f-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5948f-108">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="5948f-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="5948f-109">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="5948f-109">Properties</span></span>

| <span data-ttu-id="5948f-110">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="5948f-110">Property</span></span><br><span data-ttu-id="5948f-111">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="5948f-111">**Physical name**</span></span><br><span data-ttu-id="5948f-112">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="5948f-112">**_Type_**</span></span> | <span data-ttu-id="5948f-113">Naudoti</span><span class="sxs-lookup"><span data-stu-id="5948f-113">Use</span></span> | <span data-ttu-id="5948f-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5948f-115">**Atrankos tipo objekto ID**</span><span class="sxs-lookup"><span data-stu-id="5948f-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="5948f-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="5948f-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="5948f-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5948f-117">*GUID*</span></span> | <span data-ttu-id="5948f-118">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="5948f-118">Read-only</span></span><br><span data-ttu-id="5948f-119">Būtina</span><span class="sxs-lookup"><span data-stu-id="5948f-119">Required</span></span><br><span data-ttu-id="5948f-120">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="5948f-120">System-generated</span></span> | <span data-ttu-id="5948f-121">Unikalus pirminis identifikatorius asmens tipo įrašui.</span><span class="sxs-lookup"><span data-stu-id="5948f-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="5948f-122">**Atrankos tipo ID**</span><span class="sxs-lookup"><span data-stu-id="5948f-122">**Screening Type ID**</span></span><br><span data-ttu-id="5948f-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="5948f-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="5948f-124">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="5948f-124">*String*</span></span> | <span data-ttu-id="5948f-125">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-125">Read/write</span></span><br><span data-ttu-id="5948f-126">Būtina</span><span class="sxs-lookup"><span data-stu-id="5948f-126">Required</span></span> | <span data-ttu-id="5948f-127">Vartotojo nustatytas unikalus identifikatorius atrankos tipui.</span><span class="sxs-lookup"><span data-stu-id="5948f-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="5948f-128">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="5948f-128">**Description**</span></span><br><span data-ttu-id="5948f-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="5948f-129">mshr_description</span></span><br><span data-ttu-id="5948f-130">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="5948f-130">*String*</span></span> | <span data-ttu-id="5948f-131">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-131">Read/write</span></span><br><span data-ttu-id="5948f-132">Būtina</span><span class="sxs-lookup"><span data-stu-id="5948f-132">Required</span></span> | <span data-ttu-id="5948f-133">Atrankos tipo aprašas.</span><span class="sxs-lookup"><span data-stu-id="5948f-133">The description of the screening type.</span></span> |
| <span data-ttu-id="5948f-134">**Dažnio vienetas**</span><span class="sxs-lookup"><span data-stu-id="5948f-134">**Frequency Unit**</span></span><br><span data-ttu-id="5948f-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="5948f-135">mshr_frequencyunit</span></span><br><span data-ttu-id="5948f-136">*mshr_hcmfrequencyunit parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="5948f-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="5948f-137">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-137">Read/write</span></span><br><span data-ttu-id="5948f-138">Būtina</span><span class="sxs-lookup"><span data-stu-id="5948f-138">Required</span></span> | <span data-ttu-id="5948f-139">Aprašo dažnumą, kuriuo atranka turi būti užbaigta paskirto asmens.</span><span class="sxs-lookup"><span data-stu-id="5948f-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="5948f-140">**Kurti iš**</span><span class="sxs-lookup"><span data-stu-id="5948f-140">**Generate From**</span></span><br><span data-ttu-id="5948f-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="5948f-141">mshr_generatefrom</span></span><br><span data-ttu-id="5948f-142">*mshr_hcmfrequencygeneratefrom parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="5948f-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="5948f-143">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-143">Read-write</span></span><br><span data-ttu-id="5948f-144">Būtina</span><span class="sxs-lookup"><span data-stu-id="5948f-144">Required</span></span> | <span data-ttu-id="5948f-145">Jei dažnumo vertė yra bet kokia kita vertė nei „Tik vieną kartą“, Kurti iš vertė nustato datą, nuo kurios bus skaičiuojamas kitas atrankos įvykis.</span><span class="sxs-lookup"><span data-stu-id="5948f-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="5948f-146">**Dažnio intervalas**</span><span class="sxs-lookup"><span data-stu-id="5948f-146">**Frequency Interval**</span></span><br><span data-ttu-id="5948f-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="5948f-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="5948f-148">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="5948f-148">*Integer*</span></span> | <span data-ttu-id="5948f-149">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5948f-149">Read-write</span></span><br><span data-ttu-id="5948f-150">Būtina</span><span class="sxs-lookup"><span data-stu-id="5948f-150">Required</span></span> | <span data-ttu-id="5948f-151">Jei dažnumo vertė yra bet kokia kita vertė nei „Tik vieną kartą“, turite nustatyti intervalą laiko vienetams tarp kiekvieno atrankos įvykio.</span><span class="sxs-lookup"><span data-stu-id="5948f-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5948f-152">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5948f-152">See also</span></span>

[<span data-ttu-id="5948f-153">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="5948f-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5948f-154">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="5948f-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]