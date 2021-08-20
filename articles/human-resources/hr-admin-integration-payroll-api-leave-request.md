---
title: Atostogų užklausa
description: Šioje temoje pateikiama atostogų užklausos objekto informacija ir užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6c772c26e8a789a54c9eeb36c1cab576a7f94cb3ede547db46fe18a2e89c8ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762027"
---
# <a name="leave-request"></a>Atostogų užklausa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas atostogų užklausos objektas „Dynamics 365 Human Resources“.

### <a name="description"></a>Aprašas

Šiame objekte pateikta informacija apie atostogų užklausą.

Faktinis pavadinimas: „mshr_essleaverequestentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Užklausos id**</br>„mshr_requestid”</br>*Eilutė* | Tik skaitomas | Užklausos ID. |
| **Atostogų tipo id**</br>„mshr_leavetypeid”</br>*Eilutė* | Tik skaitomas | Atostogų tipo ID. |
| **Data**</br>„mshr_leavedate”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Atostogų užklausos data. |
| **Suma**</br>„mshr_amount”</br>*Dešimtainis* | Tik skaitomas | Atostogų užklausos suma. |
| **Pusdienio tipas**</br>„mshr_halfdaydefinition”</br>*„mshr_LeaveHalfDayDefinition” parinkties nustatymas* | Tik skaitomas | Pusės dienos atostogų tipas. |
| **Komentuoti**</br>„mshr_comment”</br>*Eilutė* | Tik skaitomas | Užklausos komentaras. |
| **Būsena**</br>mshr_status</br>*„mshr_status” parinkties nustatymas* | Tik skaitomas | Užklausos būsena. |
| **Data**</br>„mshr_requestdate”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Užklausos data. |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas | Unikalus darbuotojo personalo numeris. |
| **Priežasties kodo id**</br>„mshr_reasoncodeid”</br>*Eilutė* | Tik skaitomas | Priežasties kodo ID. |
| **Srities Duomenys ID**</br>mshr_dataareaid</br>*Eilutė* | Tik skaitomas | Nurodo juridinį asmenį (įmonę). |
| **Pirminis laukas**</br>mshr_primaryfield</br>*GUID* | Tik skaitomas</br>Sistemos sugeneruota | |
| **Atostogų tipo objektas**</br>„mshr_essleaverequestentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti atostogų užklausą. |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Atsiliepimas**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
