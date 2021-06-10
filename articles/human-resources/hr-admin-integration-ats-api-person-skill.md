---
title: Asmens įgūdžiai
description: Šioje temoje aprašomas asmens įgūdžių objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 03181d6377fdacee0faa600551e8b7ad7c68a76d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059237"
---
# <a name="person-skill"></a>Asmens įgūdžiai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens įgūdžių objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmpersonskillentity

## <a name="description"></a>aprašymas

Šis objektas aprašo kandidato įgūdžius.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens įgūdžių objekto ID**<br>mshr_hcmpersonskillentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius objekto įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina |   Susijusios šalies (asmens) įrašo ID. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas. |
| **Sertifikuotojas**<br>mshr_certifier<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens numeris darbuotojo, kuris sertifikavo šį įgūdį. |
| **Sertifikuotojo ID vertė**<br>_mshr_fk_certifier_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmworkerentityid mshr_hcmworkerentity | Sistemos sukurtas unikalus identifikatorius darbuotojo įrašo darbuotojui, kuris sertifikato įgūdį. |
| **Įgūdžio ID**<br>mshr_skillid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Įgūdžio nustatyto „Human Resources“ identifikatorius. |
| **Įgūdžio ID vertė**<br>_mshr_fk_skill_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmskillentityid mshr_hcmskillentity | Sistemos sukurtas šalies pasirinkto įgūdžio identifikatorius. |
| **Patirties metai**<br>mshr_yearsofexperience<br>*Dešimtainis* | Skaitymas/rašymas<br>Pasirinktinai | Patirties metai, kuriuos kandidatas turi šį įgūdį. |
| **Reitingavimo ID**<br>mshr_ratingid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Reitingavimo skalės tipas. Šiame objektui vertė yra **Įgūdžiai**. |
| **Lygio tipas**<br>mshr_leveltype<br>*mshr_hrmskillleveltype parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Kategorizavimo tipas lygiui, kuris priskirtas įgūdžiui. |
| **Lygio ID**<br>mshr_levelid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Reitingo lygio ID kandidatui, kuris turi šį įgūdį. |
| **Reitingo lygio ID vertė**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmratinglevelentityid mshr_hcmratinglevelentity | Sistemos sukurtas reitingo lygio identifikatorius. |
| **Lygio data**<br>mshr_leveldate<br>*Data laikas* | Skaitymas/rašymas<br>Būtina | Data, kurią kandidatas buvo reitinguotas šiam įgūdžiui. |
| **Reitingo lygio egzaminuotojas**<br>mshr_ratinglevelexaminer<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Asmens numeris darbuotojo, kuris reitingavo kandidatą. |
| **Reitingo lygio egzaminuotojo ID vertė**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmworkerentityid mshr_hcmworkerentity | Sistemos sukurtas identifikatorius darbuotojui, kuris egzaminavo kandidato įgūdžių lygį. |
| **Patikrinta**<br>mshr_verified<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Būtina | Rodo, ar įvertintas įgūdžio lygis buvo patvirtintas. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius. Šalies numerio, lygio tipo, įgūdžio ID ir lygio datos derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]