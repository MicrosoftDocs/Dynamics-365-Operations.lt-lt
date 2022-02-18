---
title: Asmens sertifiktas
description: Šioje temoje aprašomas asmens sertifikato objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 300bf294bb4b2fadd4c5d3e68e74674a69dd48f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067834"
---
# <a name="person-certificate"></a>Asmens sertifiktas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens sertifikato objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmpersoncertificateentity

## <a name="description"></a>aprašymas

Šis objektas aprašo profesinius kandidato sertifikatus.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens sertifikato objekto ID**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Tik skaitomas<br>Būtina | Sistemos sukurtas unikalus identifikatorius asmens sertifikato objekto įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Šalies (asmens) kandidato ID. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas. |
| **Sertifikato tipo ID**<br>mshr_certificatetypeid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina |  Sertifikato tipo nustatyto žmogiškuosiuose ištekliuose identifikatorius. |
| **Sertifikato tipo ID vertė**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmcertificatetypeentityid mshr_hcmcertificatetypeentity | Sistemos sukurtas unikalus identifikatorius sertifikato tipui susietame objekte. |
| **Pradžios data**<br>mshr_startdate<br>*Data laikas* | Skaitymas/rašymas<br>Būtina | Sertifikato išdavimo data. |
| **Pabaigos data**<br>mshr_enddate<br>*Data laikas* | Skaitymas/rašymas<br>Pasirinktinai | Data, kada sertifikatas nustos galioti. |
| **Pastabos**<br>mshr_notes<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Komentarai, kuriuos naudoja vadovai ar samdantys asmenys. |
| **Pirminis laukelis**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina |  Laukelis, kuris turi būti naudojamas kaip objekto įrašo identifikatorius. Šalies numerio, sertifikato tipo ID ir pradžios datos derinys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
