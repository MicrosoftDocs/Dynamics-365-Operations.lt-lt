---
title: Algalapio objektų generavimas ir peržiūra
description: Šioje temoje aprašoma, kaip sugeneruoti ir peržiūrėti algalapio objektus.
author: andreabichsel
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6e043498d4e36e38575a16c6475a5edfef51fc6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882039"
---
# <a name="generate-payroll-entities"></a><span data-ttu-id="fe705-103">Algalapio objektų generavimas</span><span class="sxs-lookup"><span data-stu-id="fe705-103">Generate payroll entities</span></span>

<span data-ttu-id="fe705-104">Naudokite šią „OData” funkciją generuoti objektams, reikalingiems algalapio integravimui.</span><span class="sxs-lookup"><span data-stu-id="fe705-104">Use this OData function to generate the entities needed for payroll integration.</span></span> <span data-ttu-id="fe705-105">Jei Personalo valdyme atlikti bet kokie šių objektų pakeitimai, pavyzdžiui, įtraukti pasirinktiniai laukai, šią funkciją galima iškviesti dar kartą kiekvieno objekto metaduomenų atnaujinimui.</span><span class="sxs-lookup"><span data-stu-id="fe705-105">If any changes are made to these entities in Human Resources, such as adding custom fields, this function can be called again to refresh the metadata of each entity.</span></span> <span data-ttu-id="fe705-106">Atsake yra operacijos ID, kurį galite stebėti, kad žinotumėte, kada generavimo procesas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="fe705-106">The response contains an operation ID that you can monitor so you know when the generation process has completed.</span></span>

<span data-ttu-id="fe705-107">**Užklausa**</span><span class="sxs-lookup"><span data-stu-id="fe705-107">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/RefreshHumanResourcesVirtualEntities
```

<span data-ttu-id="fe705-108">**pagrindinis tekstas**</span><span class="sxs-lookup"><span data-stu-id="fe705-108">**body**</span></span>

```json
{
    "PhysicalNames" : ["PayrollEmployeeEntity", "HcmWorkerBaseEntity", "PayrollPositionEntity", "PayrollPositionJobEntity", "PayrollWorkerAddressEntity", "HcmJobDetailEntity", "HcmCompFixedPlanTableEntity", "PayrollFixedCompensationPlanEntity", "HcmEmploymentDetailEntity"]
}
```

<span data-ttu-id="fe705-109">**Atsakas**</span><span class="sxs-lookup"><span data-stu-id="fe705-109">**Response**</span></span>

```json
{
    "AsyncOperationId": "8b98d338-f939-4c86-9a91-80b76b6ab2ea"
}
```

## <a name="review-payroll-entities"></a><span data-ttu-id="fe705-110">Peržiūrėti algalapio objektus</span><span class="sxs-lookup"><span data-stu-id="fe705-110">Review payroll entities</span></span>

<span data-ttu-id="fe705-111">Naudokite šį API, kad gautumėte sėkmingai sugeneruotų ir paruoštų naudoti objektų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="fe705-111">Use this API to retrieve a list of the entities that have been successfully generated and are ready for use.</span></span>

<span data-ttu-id="fe705-112">**Užklausa**</span><span class="sxs-lookup"><span data-stu-id="fe705-112">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hrvirtualentitycatalogs?$filter=mshr_hasbeengenerated eq true
```

<span data-ttu-id="fe705-113">**Atsakas**</span><span class="sxs-lookup"><span data-stu-id="fe705-113">**Response**</span></span>

```json
{
      "value": [
        {
            "mshr_physicalname": "PayrollWorkerAddressEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-1c00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmJobDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6400-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmCompFixedPlanTableEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6b00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollEmployeeEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6d00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmEmploymentDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-7e00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollFixedCompensationPlanEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-9300-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmWorkerBaseEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-c000-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollPositionJobEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-e700-005001000000",
            "mshr_refresh": null
        }
    ]
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]