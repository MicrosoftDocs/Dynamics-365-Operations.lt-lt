---
title: Asmens atranka
description: Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: 5129348f928fd709a5fabe73917522799a2d47e0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066298"
---
# <a name="person-screening"></a>Asmens atranka


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.

Fizinis pavadinimas: mshr_hcmpersonscreeningentity

## <a name="description"></a>aprašymas

Šis objektas aprašo atrankas, kurias pretendentas praėjo ar turi praieti dėl samdymo.

## <a name="json-representation"></a>JSON atstovavimas

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | aprašymas |
| --- | --- | --- |
| **Asmens atrankos objekto ID**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Tik skaitomas<br>Būtina<br>Sukurta sistemos | Unikalus pirminis identifikatorius asmens atrankos įrašui. |
| **Šalies numeris**<br>mshr_partynumber<br>*Eilutė* | Skaitymas/rašymas<br>Būtina | Šalies (asmens) numeris susietas su pretendentu. |
| **Asmens ID vertė**<br>_mshr_fk_person_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_dirpersonentityid of mshr_dirpersonentity | Sistemos sukurtas šalies (asmens) identifikatoriaus objekto įrašas. |
| **Atrankos tipo ID**<br>mshr_screeningtypeid<br>*Eilutė* | Skaitymas/rašymas<br>Būtina<br>Užsienio rarktas: atrankos tipas | Atrankos tipo nustatyto žmogiškuosiuose ištekliuose identifikatorius. |
| **Atrankos tipo ID vertė**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Tik skaitomas<br>Būtina<br>Užsienio raktas: mshr_hcmscreeningtypeentityid mshr_hcmscreeningtypeentity | Sistemos sukurtas unikalus identifikatorius atrankos tipo įrašui susietame objekte. |
| **Prašomas**<br>mshr_requiredby<br>*Data laikas* | Skaitymas/rašymas<br>Pasirinktinai | Diena, kurią atranka turi būti baigta. |
| **Būsena**<br>mshr_status<br>*mshr_hcmcompletionstatus parinkties nustatymas*<br>Skaitymas/rašymas<br>Būtina | Suteikia pretendento statusą atrankai. |
| **Užbaigimo data**<br>mshr_completeddate<br>*Data laikas* | Skaitymas/rašymas<br>Pasirinktinai | Data, kai atranka buvo užbaigta. |
| **Pastabos**<br>mshr_note<br>*Eilutė* | Skaitymas/rašymas<br>Pasirinktinai | Komentarai, kuriuos naudoja vadovai ar samdantys asmenys. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Aplikanto sekimo sistemos integravimo API įžanga](hr-admin-integration-ats-api-introduction.md)<br>
[Samdomo pretendento pavyzdžio užklausa](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
