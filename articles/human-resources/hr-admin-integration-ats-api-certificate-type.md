---
title: Sertifikato tipas
description: Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 962bccb3aaab16322d072417660ec3aac821183b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467486"
---
# <a name="certificate-type"></a><span data-ttu-id="f4503-103">Sertifikato tipas</span><span class="sxs-lookup"><span data-stu-id="f4503-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f4503-104">Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="f4503-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f4503-105">Fizinis pavadinimas: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="f4503-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="f4503-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="f4503-106">Description</span></span>

<span data-ttu-id="f4503-107">Šis objektas nustato profesionalių sertifikato tipų sąrašą, kuris nustatytas žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="f4503-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="f4503-108">Objektas nėra būdingas juridiniam asmeniui (įmonei).</span><span class="sxs-lookup"><span data-stu-id="f4503-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="f4503-109">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="f4503-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="f4503-110">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="f4503-110">Properties</span></span>

| <span data-ttu-id="f4503-111">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="f4503-111">Property</span></span><br><span data-ttu-id="f4503-112">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="f4503-112">**Physical name**</span></span><br><span data-ttu-id="f4503-113">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="f4503-113">**_Type_**</span></span> | <span data-ttu-id="f4503-114">Naudoti</span><span class="sxs-lookup"><span data-stu-id="f4503-114">Use</span></span> | <span data-ttu-id="f4503-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="f4503-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f4503-116">**Sertifikato tipo objekto ID**</span><span class="sxs-lookup"><span data-stu-id="f4503-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="f4503-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="f4503-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="f4503-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f4503-118">*GUID*</span></span> | <span data-ttu-id="f4503-119">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4503-119">Read-only</span></span><br><span data-ttu-id="f4503-120">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4503-120">Required</span></span> 
<span data-ttu-id="f4503-121">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="f4503-121">System-generated</span></span> | <span data-ttu-id="f4503-122">Unikalus pirminis identifikatorius sertifikato tipui.</span><span class="sxs-lookup"><span data-stu-id="f4503-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="f4503-123">**Sertifikato tipas**</span><span class="sxs-lookup"><span data-stu-id="f4503-123">**Certificate Type**</span></span><br><span data-ttu-id="f4503-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="f4503-124">mshr_certificatetype</span></span><br><span data-ttu-id="f4503-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f4503-125">*String*</span></span> | <span data-ttu-id="f4503-126">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="f4503-126">Read/write</span></span><br><span data-ttu-id="f4503-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4503-127">Required</span></span> | <span data-ttu-id="f4503-128">Unikalus vartotojo perskaitomas identifikatorius sertifikato tipui.</span><span class="sxs-lookup"><span data-stu-id="f4503-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="f4503-129">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="f4503-129">**Description**</span></span><br><span data-ttu-id="f4503-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="f4503-130">mshr_description</span></span><br><span data-ttu-id="f4503-131">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f4503-131">*String*</span></span> | <span data-ttu-id="f4503-132">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="f4503-132">Read/write</span></span><br><span data-ttu-id="f4503-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4503-133">Required</span></span> | <span data-ttu-id="f4503-134">Sertifikato tipo aprašas.</span><span class="sxs-lookup"><span data-stu-id="f4503-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="f4503-135">**Reikalauti naujinimo**</span><span class="sxs-lookup"><span data-stu-id="f4503-135">**Require Renewal**</span></span><br><span data-ttu-id="f4503-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="f4503-136">mshr_requirerenewal</span></span><br><span data-ttu-id="f4503-137">*mshr_noyes parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="f4503-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="f4503-138">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="f4503-138">Read/write</span></span><br><span data-ttu-id="f4503-139">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="f4503-139">Optional</span></span> | <span data-ttu-id="f4503-140">Nurodo, ar naujinimo reikia sertifikatui.</span><span class="sxs-lookup"><span data-stu-id="f4503-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f4503-141">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f4503-141">See also</span></span>

[<span data-ttu-id="f4503-142">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="f4503-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f4503-143">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="f4503-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]