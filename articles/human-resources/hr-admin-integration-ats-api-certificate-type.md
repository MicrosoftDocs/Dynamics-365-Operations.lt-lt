---
title: Sertifikato tipas
description: Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798398"
---
# <a name="certificate-type"></a><span data-ttu-id="5ad4b-103">Sertifikato tipas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5ad4b-104">Šioje temoje aprašomas sertifikatos tipo objektas „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="5ad4b-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5ad4b-105">Fizinis pavadinimas: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="5ad4b-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="5ad4b-106">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-106">Description</span></span>

<span data-ttu-id="5ad4b-107">Šis objektas nustato profesionalių sertifikato tipų sąrašą, kuris nustatytas žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="5ad4b-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="5ad4b-108">Objektas nėra būdingas juridiniam asmeniui (įmonei).</span><span class="sxs-lookup"><span data-stu-id="5ad4b-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="5ad4b-109">JSON atstovavimas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="5ad4b-110">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="5ad4b-110">Properties</span></span>

| <span data-ttu-id="5ad4b-111">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="5ad4b-111">Property</span></span><br><span data-ttu-id="5ad4b-112">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="5ad4b-112">**Physical name**</span></span><br><span data-ttu-id="5ad4b-113">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="5ad4b-113">**_Type_**</span></span> | <span data-ttu-id="5ad4b-114">Naudoti</span><span class="sxs-lookup"><span data-stu-id="5ad4b-114">Use</span></span> | <span data-ttu-id="5ad4b-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5ad4b-116">**Sertifikato tipo objekto ID**</span><span class="sxs-lookup"><span data-stu-id="5ad4b-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="5ad4b-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="5ad4b-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="5ad4b-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5ad4b-118">*GUID*</span></span> | <span data-ttu-id="5ad4b-119">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-119">Read-only</span></span><br><span data-ttu-id="5ad4b-120">Būtina</span><span class="sxs-lookup"><span data-stu-id="5ad4b-120">Required</span></span> 
<span data-ttu-id="5ad4b-121">Sukurta sistemos</span><span class="sxs-lookup"><span data-stu-id="5ad4b-121">System-generated</span></span> | <span data-ttu-id="5ad4b-122">Unikalus pirminis identifikatorius sertifikato tipui.</span><span class="sxs-lookup"><span data-stu-id="5ad4b-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="5ad4b-123">**Sertifikato tipas**</span><span class="sxs-lookup"><span data-stu-id="5ad4b-123">**Certificate Type**</span></span><br><span data-ttu-id="5ad4b-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="5ad4b-124">mshr_certificatetype</span></span><br><span data-ttu-id="5ad4b-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="5ad4b-125">*String*</span></span> | <span data-ttu-id="5ad4b-126">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-126">Read/write</span></span><br><span data-ttu-id="5ad4b-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="5ad4b-127">Required</span></span> | <span data-ttu-id="5ad4b-128">Unikalus vartotojo perskaitomas identifikatorius sertifikato tipui.</span><span class="sxs-lookup"><span data-stu-id="5ad4b-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="5ad4b-129">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="5ad4b-129">**Description**</span></span><br><span data-ttu-id="5ad4b-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="5ad4b-130">mshr_description</span></span><br><span data-ttu-id="5ad4b-131">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="5ad4b-131">*String*</span></span> | <span data-ttu-id="5ad4b-132">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-132">Read/write</span></span><br><span data-ttu-id="5ad4b-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="5ad4b-133">Required</span></span> | <span data-ttu-id="5ad4b-134">Sertifikato tipo aprašas.</span><span class="sxs-lookup"><span data-stu-id="5ad4b-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="5ad4b-135">**Reikalauti naujinimo**</span><span class="sxs-lookup"><span data-stu-id="5ad4b-135">**Require Renewal**</span></span><br><span data-ttu-id="5ad4b-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="5ad4b-136">mshr_requirerenewal</span></span><br><span data-ttu-id="5ad4b-137">*mshr_noyes parinkties nustatymas*</span><span class="sxs-lookup"><span data-stu-id="5ad4b-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="5ad4b-138">Skaitymas/rašymas</span><span class="sxs-lookup"><span data-stu-id="5ad4b-138">Read/write</span></span><br><span data-ttu-id="5ad4b-139">Pasirinktinai</span><span class="sxs-lookup"><span data-stu-id="5ad4b-139">Optional</span></span> | <span data-ttu-id="5ad4b-140">Nurodo, ar naujinimo reikia sertifikatui.</span><span class="sxs-lookup"><span data-stu-id="5ad4b-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5ad4b-141">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5ad4b-141">See also</span></span>

[<span data-ttu-id="5ad4b-142">Aplikanto sekimo sistemos integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="5ad4b-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5ad4b-143">Samdomo pretendento pavyzdžio užklausa</span><span class="sxs-lookup"><span data-stu-id="5ad4b-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]