---
title: Algalapių padėties užduotis
description: Šiame straipsnyje pateikiama išsami informacija ir atlyginimo pareigų užduoties objekto pavyzdys Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864089"
---
# <a name="payroll-position-job"></a>Algalapių padėties užduotis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas algalapių pareigų užduoties objektas Dynamics 365 Human Resources.

### <a name="description"></a>Aprašymas

Šis objektas pateikia ryšį tarp pareigų ir užduočių nurodytam pastoviosios atlyginimo dalies planui.

Faktinis pavadinimas: „mshr_payrollpositionjobentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašymas |
| --- | --- | --- |
| **Pareigų ID**</br>mshr_positionid</br>*Eilutė* | Tik skaitomas | Pareigų ID. |
| **Galioja nuo**</br>„mshr_validto”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Ta data, nuo kurios galioja pareigų ir užduoties ryšys. |
| **Galioja iki**</br>„mshr_validto”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Ta data, iki kurios galioja pareigų ir užduoties ryšys. |
| **Užduoties ID**</br>mshr_jobid</br>*Eilutė* | Tik skaitomas | Užduoties ID. |
| **Pirminis laukas**</br>mshr_primaryfield</br>*Eilutė* | Sistemos sugeneruota | Pirminis laukas. |
| **Algalapio darbo pareigų objekto ID**</br>„mshr_payrollpositionjobentityid”</br>*Guid* | Sugeneruota sistemos. | Sistemos sugeneruota visuotinai unikali identifikatoriaus (GUID) vertė, norint unikaliai identifikuoti darbą. |

## <a name="relations"></a>Ryšiai

| Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| „_mshr_fk_fixedcompplan_id_value” | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Netaikoma |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

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
