---
title: Algalapio kintamosios atlyginimo dalies planas
description: Šioje temoje pateikiama informacija ir Algalapio kintamosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c30df23debed9e2ab90745e6ea9d0e6b8a05b6d5
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429272"
---
# <a name="payroll-variable-compensation-plan"></a>Algalapio kintamosios atlyginimo dalies planas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas algalapio kintamosios atlyginimo dalies objektas „Dynamics 365 Human Resources“.

### <a name="description"></a>Aprašas

Šis objektas pateikia kintamosios atlyginimo dalies planą, priskirtą tam tikroms darbuotojo pareigoms.

Faktinis pavadinimas: „mshr_payrollvariablecompensationawardentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Darbuotojo numeris**</br>„mshr_personnelnumber”</br>*Eilutė* | Tik skaitomas | Unikalus darbuotojo personalo numeris.  |
| **Sutarties sudarymo data**</br>„mshr_awarddate”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Premijos gavimo data. |
| **Premijos tipas**</br>„mshr_awardtype”</br>*[„mshr_HrmCompVarAwardEmplType” parinkties nustatymas](hr-admin-integration-payroll-api-award-type.md)* | Tik skaitomas | Premijos tipas, apibrėžtas kintamosios atlyginimo dalies planui. |
| **Valiuta**</br>„mshr_unitcurrencycode”</br>*Eilutė* | Tik skaitomas |Valiuta, apibrėžta kintamosios atlyginimo dalies planui.   |
| **Pastoviosios atlyginimo dalies plano ID**</br>„mshr_fixedplanid”</br>*Eilutė* | Tik skaitomas | Pastoviosios atlyginimo dalies planas, kuris naudojamas kaip premijos skaičiavimo pagrindas. |
| **Vieneto vertė**</br>„mshr_awardamount”</br>*Dešimtainis* | Tik skaitomas | Vieneto reikšmė |
| **Proceso tipas**</br>„mshr_processtype”</br>*[„mshr_hrmCompProcessType” parinkties nustatymas](hr-admin-integration-payroll-api-process-type.md)* | Tik skaitomas | Proceso tipas. |
| **Kintamosios atlyginimo dalies plano tipas**</br>Eilutė</br>*„mshr_typeid”* | Tik skaitomas | Kintamosios atlyginimo dalies plano tipas. |
| **Kintamosios atlyginimo dalies plano ID**</br>Eilutė</br>*„mshr_planid”* | Tik skaitomas | Kintamosios atlyginimo dalies plano id. |
| **Vienetų skaičius**</br>Dešimtainis</br>*mshr_numberofunits* | Tik skaitomas | Įveskite apdovanojimo vienetų skaičių. |
| **Pirminis laukas**</br>mshr_primaryfield</br>*GUID* | Tik skaitomas</br>Sugeneruota sistemos. | |
| **Algalapio kintamosios atlyginimo dalies plano objektas**</br>„mshr_payrollvariablecompensationawardentityid”</br>*GUID* | Sistemos sugeneruota | Sistemos sukurta GUID vertė siekiant unikaliai atpažinti atlyginimo dalies planą. |

## <a name="relations"></a>Ryšiai 

|Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Atsiliepimas**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
