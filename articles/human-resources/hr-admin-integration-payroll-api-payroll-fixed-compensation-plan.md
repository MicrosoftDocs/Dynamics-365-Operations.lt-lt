---
title: Algalapio pastoviosios atlyginimo dalies planas
description: Šiame straipsnyje pateikiama išsami informacija ir atlyginimo pastoviosios atlyginimo dalies plano objekto pavyzdys Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909852"
---
# <a name="payroll-fixed-compensation-plan"></a>Algalapio pastoviosios atlyginimo dalies planas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomas atlyginimo pastoviosios atlyginimo dalies plano objektas Dynamics 365 Human Resources.

### <a name="description"></a>Aprašas

Šis objektas pateikia pastoviosios atlyginimo dalies planą, priskirtą tam tikroms darbuotojo pareigoms.

Faktinis pavadinimas: „mshr_payrollfixedcompensationplanentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Plano ID**</br>„mshr_planid”</br>*Eilutė* | Tik skaitomas | Nurodo atlyginimo dalies planą.  |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas | Unikalus darbuotojo personalo numeris. |
| **Užmokesčio tarifas**</br>„mshr_payrate”</br>*Dešimtainis* | Tik skaitomas | Pastoviosios atlyginimo dalies plane apibrėžtas darbo užmokesčio tarifas. |
| **Pareigų ID**</br>mshr_positionid</br>*Eilutė* | Tik skaitomas | Pareigų ID, kuris susietas su darbuotoju ir pastoviosios atlyginimo dalies plano registracija. |
| **Galioja nuo**</br>„mshr_validfrom”</br>*Datos ir Laiko poslinkis* |  Tik skaitomas | Data, nuo kurios galioja darbuotojo pastovioji atlyginimo dalis.  |
| **Galioja iki**</br>„mshr_validto”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Data, iki kurios galioja darbuotojo pastovioji atlyginimo dalis. |
| **Išmokos dažnumas**</br>„mshr_payfrequency”</br>*Eilutė* | Tik skaitomas | Kompensavimo mokėjimo [dažnumo ID pagal tam tikrą](hr-admin-integration-payroll-api-compensation-pay-frequency.md) užmokesčio tarifą. |
| **Valiuta**</br>„mshr_currency”</br>*Eilutė* | Tik skaitomas | Valiuta, apibrėžta pastoviosios atlyginimo dalies planui. |
| **Algalapio pastoviosios atlyginimo dalies objektas**</br>„mshr_payrollfixedcompensationplanentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sukurta GUID vertė siekiant unikaliai atpažinti atlyginimo dalies planą. |

## <a name="relations"></a>Ryšiai

|Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Atsiliepimas**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
