---
title: Atostogų prašymas
description: Šiame straipsnyje pateikiama informacija ir atostogų užklausos objekto pavyzdys Dynamics 365 Human Resources.
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
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899678"
---
# <a name="leave-request"></a>Atostogų prašymas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas atostogų užklausos objektas dėl Dynamics 365 Human Resources.

### <a name="description"></a>Aprašymas

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
