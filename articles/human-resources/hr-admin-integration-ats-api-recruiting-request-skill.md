---
title: Samdymo užklausos įgūdžiai
description: Šioje temoje aprašomas įdarbinimo užklausos įgūdžių objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: b0e6f4d2a38b092eb8460c5f5f4b8b6d290533a8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464675"
---
# <a name="recruiting-request-skill"></a>Samdymo užklausos įgūdžiai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas įdarbinimo užklausos įgūdžių objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>aprašymas

Aprašo įgūdžių reikalavimus samdymo užklausai.

### <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Įdarbinimo užklausos įgūdžių objekto ID**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius **Samdymo užklausos įgūdžių** užklausai. |
| **Įdarbinimo užklausos ID**<br>mshr_recruitingrequestid<br>*Eilutė* | Rašyti kartą<br>Būtina | Vartotojo perskaitomas unikalus susijusio identifikatoriaus samdymo užklausai. |
| **Įdarbinimo užklausos ID vertė**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br> Užsienio raktas: mshr_hcmrecruitingrequestentityid mshr_hcmrecruitingrequestentity objektas | Sistemos sukurtas unikalus idnetifikatorius susijusio samdymo užklausai. |
| **Įgūdžio ID**<br>mshr_skillid<br>*Eilutė*<br> | Rašyti kartą<br>Būtina | Vartotojo perskaitomas unikalus būtinų įgūdžių idnetifikatorius. |
| **Įgūdžio ID vertė**<br>_mshr_fk_skill_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmskillentityid mshr_hcmskillentity objektas | Sistemos sukurtas unikalus būtino įgūdžio identifikatorius. |
| **Reitingo lygio ID**<br>mshr_ratinglevelid<br>*Eilutė* | Rašyti kartą<br>Pasirinktinai | Būtino įgūdžio lygio vertė pasirinktam darbui pagal reitingavimo modelį priskirtą įgūdžiui. |
| **Reitingo lygio ID vertė**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmratinglevelentityid mshr_hcmratinglevelentity objektas | Sistemos sukurtas unikalus identifikatorius lygiui. |
| **Įgūdžio aprašas**<br>mshr_skilldescription<br>*Eilutė* | Tik skaitomas<br>Būtina | Įgūdžio aprašas. |
| **Reitingavimo lygio aprašas**<br>mshr_ratingleveldescription<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Pasirinkto įgūdžio lygio aprašas. |
| **Duomenų srities ID**<br>mshr_dataareaid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Nurodo juridinį asmenį (įmonę). |
| **Duomenų srities ID vertė**<br>_mshr_dataareaid_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: cdm_companyid of cdm_company objektas | Sistemos sukurta GUID vertė rodanti juridnį asmenį (įmonę). |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Įdarbinimo užklausos vertės, įgūdžio ID, kaip kito metodo taip pat identifikuojančio įrašą, derinys. |
| **Reitingo modelio ID**<br>mshr_ratingmodelid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Reitingavimo modelis, naudojamas reitinguot įgūdį. |
| **Reitingo modelio ID vertė**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmratingmodelentityid mshr_hcmratingmodelentity objektas | Sistemos sukurtas unikalus identifikatorius reitingavimo modeliui, naudojamam reitinguoti įgūdį. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]