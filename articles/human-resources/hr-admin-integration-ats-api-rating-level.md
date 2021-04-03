---
title: Vertinimo lygis
description: Šioje temoje aprašomas reitingavimo lygio objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464747"
---
# <a name="rating-level"></a>Vertinimo lygis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas reitingavimo lygio objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmratinglevelentity

## <a name="description"></a>aprašymas

Šis objektas suteikia reitingavimo lygių galimybę įgūdžiams. Reitingavimo lygiai taikomi visiems juridiniams objektams.

## <a name="json-representation"></a>JSON atstovavimas

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

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Reitingo lygio objekto ID**<br>mshr_hcmratinglevelentityid<br>*GUID* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Sistemos sukurtas unikalus identifikatorius lygiui. |
| **Reitingo lygio ID**<br>mshr_ratinglevelid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Vartotojo perskaitomas unikalus identifikatorius lygiui. |
| **Reitingo modelio ID**<br>mshr_ratingmodelid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Reitingavimo modelis, kuriam reitigavimo lygis priklauso. |
| **Reitingo modelio objekto ID**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmratingmodelentityid mshr_hcmratingmodelentity | Sistemos sukurtas identifikatorius reitingavimo modeliui, kuriam reitingavimo lygis priklauso. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Reitingavimo lygio aprašas. |
| **Koeficientas**<br>mshr_factor<br>*Sveikasis skaičius* | Skaitymas/rašymas<br>Būtina | Reitingavimo lygio faktorius. Jums lyginant prekes su skirtingais reitingavimo lygio skaičiais, faktorius yra naudojamas siekiant normalizuoti balus. Vertė turi būti integruojama nuo 0 iki 9. |
| **Pastaba**<br>mshr_note<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Bet kokios pastabos susijusios su reitingavimo lygiu. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius. Reitingavimo lygio ID derinys ir reitingavimo modelio ID. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]