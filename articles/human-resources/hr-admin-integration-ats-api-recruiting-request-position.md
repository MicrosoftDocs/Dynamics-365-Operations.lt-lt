---
title: Įdarbinimo užklausų pareigos
description: Šioje temoje aprašomas samdytino užklausos pareigų objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 24ea00c13030d09fb9cda02950ac7b79bfe0d03d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065506"
---
# <a name="recruiting-request-position"></a>Įdarbinimo užklausų pareigos


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas samdytino užklausos pareigų objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>aprašymas

Aprašo pareigas ar kelias jas, kurias reikia užpildyti įdarbinimo užklausai. Pareigų įtraukimas į įdarbinimo užklausą yra pasirinktinas. Pareigų ypatybės yra skirtos tik skaityti, nes pareigų ypatybės neturi skirtis įdarbinimo užklausoje nuo pagrindiniame pareigų įraše. Jei ypatybes reikia keisti, tai reikia padaryti pareigų pagrindiniame įraše prieš įtraukiant pareigas į įdarbinimo užklausą.

### <a name="json-representation"></a>JSON atstovavimas
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Įdarbinimo užklausos pareigų objekto ID**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Tik skaitomas<br>Būtina |    Sistemos sukurtas unikalus idnetifikatorius susijusio pareigų įrašas. |
| **Įdarbinimo užklausos ID**<br>mshr_recruitingrequestid<br>*Eilutė* | Rašyti kartą<br>Būtina | Vartotojo perskaitomas unikalus idnetifikatorius susijusio samdymo užklausai. |
| **Įdarbinimo užklausos ID vertė**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmrecruitingrequestentityid mshr_hcmrecruitingrequestentity objektas | Sistemos sukurtas unikalus idnetifikatorius įdarbinimo užklausia, kuriai priskirtos pareigos. |
| **Pareigų ID**<br>mshr_positionid<br>*Eilutė* | Rašyti kartą<br>Būtina | Vartotojo perskaitomas unikalus idnetifikatorius pareigoms. |
| **Pareigų ID vertė**<br>_mshr_fk_position_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmpositionv2entityid mshr_hcmpositionv2entity objektas | Sistemos sukurtas pareigų identifikatorius. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigų aprašas. |
| **Pareigų tipo ID**<br>mshr_positiontypeid<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Vartotojo perskaitomas unikalus idnetifikatorius pareigų tipui. |
| **Pareigų tipo ID vertė**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmpositiontypeentityid of mshr_hcmpositiontypeentity objektas | Sistmos sukurtas unikalus idnetifikatorius pareigų tipui. |
| **Būsena**<br>mshr_status<br>*RecruitingRequestPositionStatus* parinkties nustatymas | Skaitymas/rašymas<br>Būtina | Įdarbinimo užklausos pareigū būsena. |
| **Padalinio numeris**<br>mshr_departmentnumber<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai<br> | Pareigų skyriaus numeris. |
| **Skyriaus ID vertė**<br>_mshr_fk_department_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_omdepartmententityid mshr_omdepartmententity objektas | Sistemos sukurtas sukurtas unikalus identifikatorius pareigų skyriui. |
| **Ataskaitos pareigoms ID**<br>mshr_reportstopositionid<br>*Eilutė* | Tik skaitomas<br>Būtina | Vartotojo perskaitomas pareigų ID, prie kurio įdarbintas asmuo praneša organizacijos hierarchijoje. |
| **Ataskaitos pareigoms ID vertė**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmpositionv2entityid mshr_hcmpositionv2entity objektas | Sistemos sukurtas unikalus ID pareigoms, prie kurių įdarbintos pareigos pranešamos. |
| **Ataskaitos asmens numeriui**<br>mshr_reportstopersonnelnumber<br>*Eilutė* | Tik skaitomas<br>Būtina | Darbuotojo ID, kurioms darbuotojas yra pasamdytas bus praneštas. |
| **Ataskaitos darbuotojo ID vertė**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmworkerbaseentityid mshr_hcmworkerbaseentity objektas | Sistemos sukurtas ID, kuriam darbuotojas yra pasamdytas bus praneštas. |
| **Finansinė dimensija**<br>mshr_financialdimension<br>*Eilutė* | Tik skaitomas<br>Pasirinktinai | Finansinė dimensija (pavyzdžiui, kaštų centras) priskirta pareigoms. Finansinė dimensija yra priskirta kiekvienoms pareigoms pagal juridinį asmenį. Kaštų centrai yra nustatyti dimensijose ir prieinami per mshr_dimattributeomcostcenterentity objektą. |
| **Duomenų srities ID**<br>mshr_dataareaid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Nurodo jurdinį asmenį (bendrovę) įdarbinimo pareigų užklausai. |
| **Duomenų srities ID vertė**<br>_mshr_dataareaid_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: cdm_companyid of cdm_company objektas | Sistemos sukurta GUID vertė rodanti juridnį asmenį (įmonę) įdarbinimo pareigų užklausai. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Įdarbinimo užklausos vertės, pareigų ID, kaip kito metodo taip pat identifikuojančio įrašą, derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Pavyzdinė užklausa Samdymo prašymui](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
