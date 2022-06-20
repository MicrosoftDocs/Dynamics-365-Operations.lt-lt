---
title: Įdarbinimo užklausų vieta
description: Šiame straipsnyje aprašomas įdarbinimo užklausos vietos objektas Dynamics 365 Human Resources.
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
ms.openlocfilehash: d31af9ab62db310b89fbc7a2d7099621b59a356d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893822"
---
# <a name="recruiting-request-location"></a>Įdarbinimo užklausų vieta


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas įdarbinimo užklausos vietos objektas Dynamics 365 Human Resources.

Fizinis pavadinimas: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>aprašymas

Vietų sąrašas nustatytas kaip vietos, kuriose samdyti daarbuotojai dirbs po įdarbinimo. Šios vietos sukuriamos visuose juridiniuose asmenyse.

### <a name="json-representation"></a>JSON atstovavimas

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Vietos ID**<br>mshr_locationid<br>*Eilutė* | Rašyti kartą<br>Būtina | Sistemos sukurtas vartotojo perskaitomas identifikatorius samdymo vietai. |
| **Samdymo užklausos vieta**<br>mshr_recruitingrequestlocationid<br>*Eilutė* | Rašyti kartą<br>Būtina | Vartotojo nustatytas unikalus identifikatorius samdymo vietai. |
| **Įdarbinimo užklausos vietos objekto ID**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius samdymo užklausos vietai. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Vietos aprašymas. |
| **Šalies regiono ID**<br>mshr_countryregionid<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Nurodo šalį ar regioną, kurios piliečiu pretendentas yra. |
| **Šalies regiono ID vertė**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_logisticaddresscountryregionentityid mshr_logisticsaddresscountryregionentity | Sistemos sukurtas unikalus asmens identifikatoriaus šalies/regiono adresui. |
| **Zip kodas**<br>mshr_zipcode<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Zip/pašto kodas. |
| **Gatvė**<br>mshr_street<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Gatvės adresas. |
| **Miestas**<br>mshr_city<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Miestas. |
| **Apskritis**<br>mshr_state<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Valstija ar apskritis. |
| **Apygarda**<br>mshr_county<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Šalis. |
| **Telefonas**<br>mshr_telephone<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Vietos telefono numeris. |
| **El. pašto adresas**<br>mshr_email<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | El. pašto adresas. |
| **Interneto adresas**<br>mshr_internetaddress<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | URL vietos svetainei. |
| **Duomenų srities ID**<br>mshr_dataareaid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Nurodo juridinį asmenį (įmonę). |
| **Duomenų srities ID vertė**<br>_mshr_dataareaid_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: cdm_companyid of cdm_company objektas | Sistemos sukurta GUID vertė rodanti juridnį asmenį (įmonę). |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
