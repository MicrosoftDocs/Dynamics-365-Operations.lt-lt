---
title: Algalapių pareigų užduotis
description: Šioje temoje pateikiama informacija ir Algalapio pareigų užduoties objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722636"
---
# <a name="payroll-position-job"></a>Algalapių padėties užduotis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas Pareigų užduoties algalapio objektas „Dynamics 365 Human Resources“.

### <a name="description"></a>Aprašas

Šis objektas pateikia ryšį tarp pareigų ir užduočių nurodytam pastoviosios atlyginimo dalies planui.

Faktinis pavadinimas: „mshr_payrollpositionjobentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Užduoties ID**<br>mshr_jobid<br>*Eilutė* | Tik skaitomas<br>Būtina |Užduoties ID. |
| **Galioja nuo**<br>„mshr_validto”<br>*Datos ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Data, nuo kurios galioja pareigų ir užduoties ryšys. |
| **Galioja iki**<br>„mshr_validto”<br>*Data ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Data, iki kurios galioja pareigų ir užduoties ryšys.  |
| **Pareigų ID**<br>mshr_positionid<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigų ID. |
| **Pirminis laukas**<br>mshr_primaryfield<br>*Eilutė* | Būtina<br>Sistemos sugeneruota |  |
| **Darbo pareigų ID reikšmė**<br>„_mshr_fk_positionjob_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity” |Darbo ID yra susietas su pareigomis.|
| **Pastovios atlyginimo dalies plano ID reikšmė**<br>„_mshr_fk_fixedcompplan_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity”  | Pastovios atlyginimo dalies plano ID yra susietas su pareigomis. |
| **Algalapio darbo pareigų objekto ID**<br>„mshr_payrollpositionjobentityid”<br>*Guid* | Būtina<br>Sugeneruota sistemos. | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti užduotį.  |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Atsiliepimas**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
