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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125718"
---
# <a name="certificate-type"></a><span data-ttu-id="4b01d-103">Sertifikato tipas</span><span class="sxs-lookup"><span data-stu-id="4b01d-103">Certificate type</span></span>

<span data-ttu-id="4b01d-104">Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="4b01d-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4b01d-105">Fizinis pavadinimas: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="4b01d-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="4b01d-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4b01d-106">Description</span></span>

<span data-ttu-id="4b01d-107">Šis objektas nustato profesionalių sertifikato tipų sąrašą, kuris nustatytas žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="4b01d-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="4b01d-108">Objektas nėra būdingas juridiniam asmeniui (įmonei).</span><span class="sxs-lookup"><span data-stu-id="4b01d-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="4b01d-109">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="4b01d-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="4b01d-110">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="4b01d-110">Properties</span></span>

| <span data-ttu-id="4b01d-111">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="4b01d-111">Property</span></span><br><span data-ttu-id="4b01d-112">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="4b01d-112">**Physical name**</span></span><br><span data-ttu-id="4b01d-113">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="4b01d-113">**_Type_**</span></span> | <span data-ttu-id="4b01d-114">Naudoti</span><span class="sxs-lookup"><span data-stu-id="4b01d-114">Use</span></span> | <span data-ttu-id="4b01d-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4b01d-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4b01d-116">**Sertifikato tipo objekto ID**</span><span class="sxs-lookup"><span data-stu-id="4b01d-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="4b01d-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="4b01d-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="4b01d-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4b01d-118">*GUID*</span></span> | <span data-ttu-id="4b01d-119">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="4b01d-119">Read-only</span></span><br><span data-ttu-id="4b01d-120">Būtina</span><span class="sxs-lookup"><span data-stu-id="4b01d-120">Required</span></span> 
<span data-ttu-id="4b01d-121">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="4b01d-121">System-generated</span></span> | <span data-ttu-id="4b01d-122">Unikalus pirminis identifikatorius sertifikato tipui.</span><span class="sxs-lookup"><span data-stu-id="4b01d-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="4b01d-123">**Sertifikato tipas**</span><span class="sxs-lookup"><span data-stu-id="4b01d-123">**Certificate Type**</span></span><br><span data-ttu-id="4b01d-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="4b01d-124">mshr_certificatetype</span></span><br><span data-ttu-id="4b01d-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="4b01d-125">*String*</span></span> | <span data-ttu-id="4b01d-126">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="4b01d-126">Read/write</span></span><br><span data-ttu-id="4b01d-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="4b01d-127">Required</span></span> | <span data-ttu-id="4b01d-128">Unikalus vartotojo perskaitomas identifikatorius sertifikato tipui.</span><span class="sxs-lookup"><span data-stu-id="4b01d-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="4b01d-129">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="4b01d-129">**Description**</span></span><br><span data-ttu-id="4b01d-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="4b01d-130">mshr_description</span></span><br><span data-ttu-id="4b01d-131">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="4b01d-131">*String*</span></span> | <span data-ttu-id="4b01d-132">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="4b01d-132">Read/write</span></span><br><span data-ttu-id="4b01d-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="4b01d-133">Required</span></span> | <span data-ttu-id="4b01d-134">Sertifikato tipo aprašas.</span><span class="sxs-lookup"><span data-stu-id="4b01d-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="4b01d-135">**Reikalauti naujinimo**</span><span class="sxs-lookup"><span data-stu-id="4b01d-135">**Require Renewal**</span></span><br><span data-ttu-id="4b01d-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="4b01d-136">mshr_requirerenewal</span></span><br><span data-ttu-id="4b01d-137">*mshr_noyes parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="4b01d-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="4b01d-138">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="4b01d-138">Read/write</span></span><br><span data-ttu-id="4b01d-139">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="4b01d-139">Optional</span></span> | <span data-ttu-id="4b01d-140">Nurodo, ar naujinimo reikia sertifikatui.</span><span class="sxs-lookup"><span data-stu-id="4b01d-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4b01d-141">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="4b01d-141">See also</span></span>

[<span data-ttu-id="4b01d-142">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="4b01d-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4b01d-143">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="4b01d-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

