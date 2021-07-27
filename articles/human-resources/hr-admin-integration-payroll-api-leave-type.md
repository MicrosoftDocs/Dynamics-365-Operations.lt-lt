---
title: Atostogų tipas
description: Šioje temoje pateikiama atostogų tipo objekto informacija ir užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
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
ms.openlocfilehash: a99d53805efd7ee2001217ea3154d46b5d5e66cd
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314448"
---
# <a name="leave-type"></a>Atostogų tipas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas atostogų tipo objektas „Dynamics 365 Human Resources“.

### <a name="description"></a>Aprašas

Šiame objekte pateikta informacija apie nurodytą atostogų tipą.

Faktinis pavadinimas: „mshr_essleavetypeentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Atostogų tipo id**</br>„mshr_leavetypeid”</br>*Eilutė* | Tik skaitomas | Atostogų tipo ID. |
| **Aprašas**</br>mshr_description</br>*Eilutė* | Tik skaitomas | Atostogų tipo aprašas. |
| **Kategorija**</br>„mshr_category”</br>*„mshr_LeaveTypeCategory” parinkties nustatymas* | Tik skaitomas | Atostogų tipo kategorija. |
| **Būtina nurodyti priežasties kodą**</br>„mshr_isreasoncoderequired”</br>*„mshr_NoYes” parinkties nustatymas* | Tik skaitomas | Apibrėžia, ar atostogų tipui reikia priežasties kodo. |
| **Atostogų vienetas**</br>„mshr_leaveamountunit”</br>*„mshr_LeaveAmountUnit” parinkties nustatymas* | Tik skaitomas | Šio atostogų tipo vienetas. |
| **Įgalinti pusdienį**</br>„mshr_enablehalfdaydefinition”</br>*„mshr_NoYes” parinkties nustatymas* | Apibrėžia, ar atostogų tipui įgalintas pusdienis. |
| **Srities Duomenys ID**</br>„mshr_dataareaid_id”</br>*Eilutė* | Tik skaitomas | Nurodo juridinį asmenį (įmonę). |
| **Atostogų tipo objektas**</br>„mshr_essleavetypeentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti atostogų tipą. |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Atsiliepimas**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
