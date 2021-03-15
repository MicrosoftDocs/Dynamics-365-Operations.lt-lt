---
title: Asmens atranka
description: Šioje temoje aprašomas asmens atrankos objektas „Dynamics 365 Human Resources“.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125382"
---
# <a name="person-screening"></a>Asmens atranka

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