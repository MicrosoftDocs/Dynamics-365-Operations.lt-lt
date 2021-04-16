---
title: Asmens tapatybės numeris
description: Šioje temoje aprašomas asmens tapatybės numerio objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: a8fa924898472302e67dd4e32251ca0c94da0ea9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798086"
---
# <a name="person-identification-number"></a>Asmens tapatybės numeris

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens tapatybės numerio objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>aprašymas

Šis objektas aprašo asmens tapatybės numerius kandidatui. Jis įjungia API vartotojui galimybę rašyti tapatybės numerius, tokius kaip socialino draudimo numeriai ar paso numeriai į kandidato įrašą. Tapatybės numeriai yra ieškomi darbuotojo įraše, bet ne kandidato įraše. Integruojanti programa gali rašyti vertes į „Human Resources“ duomenų bazę, tačiau numeriai nebus matomi „Human Resources“ iki tol, kol kandidato darbuotojo įrašas nebus sukurtas.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens tapatybės numerio objekto ID**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Unikalus pirminis identifikatorius asmens tapatybės numerio įrašui. |
| **Įrašo tipas**<br>mshr_entrytype<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Laisva vertė nuorodos objekto tipui tapatybės numeriui. |
| **Aprašas**<br>mshr_description<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Identifikacijos numerio aprašas. |
| **Galiojimo pabaigos data**<br>mshr_expirationdate<br>*Data laikas* | Skaitymas/rašymas<br>Pasirinktinai | Asmens tapatybės ar susieto dokumento galiojimo pabaigos data. |
| **Pagrindinis**<br>mshr_isprimary<br>*mshr_noyes parinkties nustatymas* | Skaitymas/rašymas<br>Pasirinktinai | Nustato, ar asmens tapatybės numeris yra pirminis įrašas asmeniui šiam atapžinimo tipui. |
| **Identifikavimo numeris**<br>mshr_identificationnumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Identifikacijos numeris. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Šalies (asmens), turinčio tapatybės numerį, identifikatorius. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid mshr_dirpersonentity objektas | Unikalus šalies (asmens) identifikatorius. |
| **Tapatybės tipo ID**<br>mshr_identificationtypeid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Tapatybės numerio tipas. |
| **Tapatybės tipo ID vertė**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmidentificationtypeentityid mshr_hcmidentificationtypeentity objektas | Sistemos sukurtas unikalus asmens identifikatoriaus tipas. |
| **Išdavusios įstaigos ID**<br>mshr_issuingagencyid<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Tapatybės numerį išdavusi įstaiga ar organizacija. |
| **Išdavusios įstaigos ID vertė**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Tik skaitomas<br>Pasirinktinai<br>Užsienio raktas: mshr_hcmissuingagencyentityid mshr_hcmissuingagencyentity objektas | Sistemos sukurtas unikalus agentūros, išdavusios tapatybės numerį, identifikatorius. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius. Šalies numerio, tapatybės tipo ID ir tapatybės numerio derinys. |
| **Išdavimo data**<br>mshr_issuedate<br>*Data* | Skaitymas/rašymas<br>Pasirinktinai | Tapatybės numerio išdavimo data. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]