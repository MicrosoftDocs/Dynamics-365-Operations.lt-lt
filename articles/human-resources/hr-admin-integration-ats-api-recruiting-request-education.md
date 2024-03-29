---
title: Samdymo užklausos išsilavinimas
description: Šiame straipsnyje aprašomas įdarbinimo užklausos išsilavinimo subjektas Dynamics 365 Human Resources.
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
ms.openlocfilehash: bcdb5e2cc61ce551af21401ea34d8e85bc21fc6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893851"
---
# <a name="recruiting-request-education"></a>Samdymo užklausos išsilavinimas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas įdarbinimo užklausos išsilavinimo subjektas Dynamics 365 Human Resources.

Fizinis pavadinimas: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>aprašymas

Aprašo išsilavinimo reikalavimus samdymo užklausai.

### <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Įdarbinimo užklausos išsilavinimo objekto ID**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius samdymo užklausos išsilavinimo įrašui. |
| **Įdarbinimo užklausos ID**<br>mshr_recruitingrequestid<br>*Eilutė* | Rašyti kartą<br>Būtina | Vartotojo perskaitomas unikalus idnetifikatorius susijusio samdymo užklausai. |
| **Įdarbinimo užklausos ID vertė**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmrecruitingrequestentityid mshr_hcmrecruitingrequestentity | Sistemos sukurtas unikalus idnetifikatorius susijusio samdymo užklausai. |
| **Išsilavinimo lygio ID**<br>mshr_educationlevelid<br>*Eilutė* | Rašyti kartą<br>Būtina | Būtino išsilavinimo lygis. |
| **Išsilavinimo lygio ID vertė**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmeducationlevelentityid mshr_hcmeducationlevelentity | Sistemos sukurtas unikalus būtino išsilavinimo lygio identifikatorius. |
| **Išsilavinimo lygio aprašas**<br>mshr_educationleveldescription<br>*Eilutė* | Tik skaitomas<br>Būtina | Įgūdžiams būtino lygio aprašas. |
| **Išsilavinimo disciplinos ID**<br>mshr_educationdisciplinedescription<br>*Eilutė* | Rašyti kartą<br>Būtina | Išsilavinimo disciplinos sritis. |
| **Išsilavinimo disciplinos ID vertė**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmeducationdisciplineentityid mshr_hcmeducationdisciplineentity | Sistemos sukurtas unikalus būtino išsilavinimo disciplinos sritis. |
| **Išsilavinimo disciplinos aprašas**<br>mshr_educationdisciplinedescription<br>Eilutė | Tik skaitomas<br>Būtina | Išsilavinimo disciplinos srities aprašas. |
| **Duomenų srities ID**<br>mshr_dataareaid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Nurodo juridinį asmenį (įmonę).|
| **Duomenų srities ID vertė**<br>_mshr_dataareaid_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: cdm_companyid of cdm_company objektas | Sistemos sukurta GUID vertė rodanti juridnį asmenį (įmonę). |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Įdarbinimo užklausos vertės, išsilavinimo lygio ID ir išsilavinimo disciplinos ID, kaip kito metodo taip pat identifikuojančio įrašą, derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
