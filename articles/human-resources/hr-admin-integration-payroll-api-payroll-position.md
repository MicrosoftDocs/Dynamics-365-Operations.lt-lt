---
title: Algalapio informacija pareigoms
description: Šioje temoje pateikiama Algalapio išsamios informacijos, skirtos Pareigų objektui, užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
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
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069812"
---
# <a name="payroll-position"></a>Algalapių padėtis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas Pareigų algalapio objektas „Dynamics 365 Human Resources“.

Faktinis pavadinimas: „mshr_payrollpositionentity”.

### <a name="description"></a>Aprašas

Šiame objekte pateikta informacija apie nurodytą darbuotojo pareigas.

Faktinis pavadinimas: „mshr_payrollpositionentity”.

## <a name="properties"></a>Ypatybės

| Ypatybė</br>**Faktinis pavadinimas**</br>**_Tipas_** | Naudoti | Aprašymas |
| --- | --- | --- |
| **Pareigų ID**</br>mshr_positionid</br>*Eilutė* | Tik skaitomas | Pareigų ID. |
| **Mokėjimų ciklo ID**</br>mshr_paycycleid</br>*Eilutė* | Tik skaitomas | Pareigose apibrėžtas mokėjimo ciklas. |
| **Įprastos darbo valandos per metus**</br>„annualregularhours”</br>*Dešimtainis* | Tik skaitomas | Pareigoms nustatytos įprastos darbo valandos per metus. |
| **Apmokėta juridinio subjekto**</br>„paidbylegalentity”</br>*Eilutė* | Tik skaitomas | Juridinis subjektas, kuris yra atsakingas už apmokėjimus, apibrėžtas pareigose. |
| **Galioja iki**</br>„validto”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Data, iki kurios galioja išsami informacija apie pareigas. |
| **Galioja nuo**</br>„validfrom”</br>*Datos ir Laiko poslinkis* | Tik skaitomas | Data, iki kurios galioja išsami informacija apie pareigas. |
| **Pirminis laukas**</br>mshr_primaryfield</br>*Eilutė* | Sistemos sugeneruota | Pirminis laukas. |
| **Išsamios algalapio pareigų informacijos objekto ID**</br>„payrollpositiondetailsentityid”</br>*Guid* | Būtina</br>Sugeneruota sistemos. | Sistemos sugeneruota visuotinai unikali identifikatoriaus (GUID) vertė, norint unikaliai identifikuoti pareigas. |

## <a name="relations"></a>Ryšiai

| Ypatybės vertė | Susijęs objektas | Naršymo ypatybė | Rinkimo tipas |
| --- | --- | --- | --- |
| „_mshr_fk_fixedcompplan_id_value” | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Netaikoma |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Netaikoma |

## <a name="example-query"></a>Pavyzdinė užklausa

**Prašymas**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Atsiliepimas**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
