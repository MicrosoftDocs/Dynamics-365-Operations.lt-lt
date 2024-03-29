---
title: Atostogų balansas
description: Šiame straipsnyje pateikiama informacija ir atostogų balanso objekto pavyzdys Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4792c316b8b7af3e86b097029eb281af4a10d113
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899707"
---
# <a name="leave-balance"></a>Atostogų balansas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas atostogų balanso objektas, skirtas Dynamics 365 Human Resources.

### <a name="description"></a>Aprašymas

Šis objektas pateikia nurodyto darbuotojo atostogų balansą pagal atostogų tipą.

Faktinis pavadinimas: „mshr_essleavebalanceentities”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas | Unikalus darbuotojo personalo numeris. |
| **Dabartinis balansas**</br>„mshr_balanceavailable”</br>*Dešimtainis* | Tik skaitomas | Dabartinis darbuotojo balansas. |
| **Tipas**</br>„mshr_balanceavailable”</br>*Eilutė* | Tik skaitomas | Atostogų tipo ID. |
| **Kaupimo tarifas**</br>„mshr_accrualratedescription”</br> | Tik skaitomas | Kaupimo koeficientas. |
| **Paskutinė perkeliama suma**</br>„mshr_lastcarryforwardamount”</br>*Dešimtainis* | Tik skaitomas | Paskutinio perkeliamo balanso suma. |
| **Išnaudota šiais metais**</br>„mshr_takenthisyear”</br>*Dešimtainis* | Tik skaitomas | Šiais metais pasiimtų atostogų suma. |
| **Iš viso šiais metais**</br>„mshr_totalthisyear”</br>*Dešimtainis* | Tik skaitomas | Bendra šių metų suma. |
| **Srities Duomenys ID**</br>„mshr_dataareaid_id”</br>*Eilutė* | Tik skaitomas | Nurodo juridinį asmenį (įmonę). |
| **Pirminis laukas**</br>mshr_primaryfield</br>*GUID* | Tik skaitomas</br>Sistemos sugeneruota | |
| **Atostogų tipo Id**</br>„_mshr_fk_leavetype_id_value”</br>*GUID* | Tik skaitomas</br>Išorinis raktas:„mshr_essleavetypeentityid” iš „mshr_essleavetypeentity” objekto  | Atostogų tipo ID |
| **Atostogų balanso objektas**</br>„mshr_essleavebalanceentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti balansą. |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Atsiliepimas**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
