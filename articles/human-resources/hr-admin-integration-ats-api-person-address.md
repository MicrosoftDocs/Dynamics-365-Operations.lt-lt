---
title: Asmens adresas
description: Šioje temoje aprašomas asmens adreso objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: e16966c30ccfadd69e3d53f1259fa7167896e6d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798158"
---
# <a name="person-address"></a>Asmens adresas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens adreso objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmpersonaddressentities

## <a name="description"></a>aprašymas

Šiame objekte yra pašto adresų sąrašas kandidato įrašams.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens adreso objekto ID**<br>mshr_hcmpersonaddressentityid<br>*Eilutė* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Susijusios šalies (asmens) įrašo ID. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas. |
| **Vietos ID**<br>mshr_locationid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Adreso įrašo vietos ID. Nustatymas mshr_logisticspostaladdresslocationcdsentity objekte. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Kandidato adreso aprašas. |
| **Vaidmenys**<br>mshr_roles<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Vaidmenys priskirti šiam adresui. Daugiau nei vienas vaidmuo gali būti priskirtas. Visi vaidmenys turi būti atskirti kabliataškiu. Galiojančios vertės esančios mshr_logisticslocationroleentity objekte. |
| **Gatvė**<br>mshr_street<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Gatvės numeris. |
| **Miestas**<br>mshr_city<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adrese nurodytas miestas. Nustatymas mshr_logisticsaddresscityentity objekte. |
| **Apskritis**<br>mshr_state<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adreso būsena. Nustatymas mshr_logisticsaddressstateentity objekte. |
| **Apygarda**<br>mshr_county<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adrese nurodyta apygarda. Nustatymas mshr_logisticsaddresscountyentity objekte. |
| **Zip kodas**<br>mshr_zipcode<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adreso ZIP/pašto kodas. Nustatymas mshr_logisticsaddresspostalcodeentity objekte. |
| **Šalies regiono ID**<br>mshr_countryregionid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Adreso šalis arba regionas. |
| **Šalies regiono ID vertė**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_logisticaddresscountryregionentityid mshr_logisticsaddresscountryregionentity | Sistemos sukurtas unikalus asmens identifikatoriaus šalies/regiono adresui. |
| **Pagrindinis**<br>mshr_isprimary<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Nustato, ar šis adresas yra pagrindinis asmens adresas. |
| **Yra privatus**<br>mshr_isprivate<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Nustato, ar šis adresas yra privatus asmens su nustatytu vaidmeniu adresas. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukeliai, kurie naudojami kaip pirminis objekto įrašo identifikatorius. Šalies numerio, tipo ir vietos ID derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]