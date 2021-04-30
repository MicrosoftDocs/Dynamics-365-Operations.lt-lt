---
title: Algalapio informacija pareigoms
description: Šioje temoje pateikiama Algalapio išsamios informacijos, skirtos Pareigų objektui, užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882036"
---
# <a name="payroll-position"></a>Algalapio pareigos

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje pateikiama Algalapio išsamios informacijos, skirtos Pareigų objektui, užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Įprastos darbo valandos per metus**<br>„annualregularhours”<br>*Dešimtainis* | Tik skaitomas<br>Būtina | Pareigoms nustatytos įprastos darbo valandos per metus.  |
| **Išsamios algalapio pareigų informacijos objekto ID**<br>„payrollpositiondetailsentityid”<br>*Guid* | Būtina<br>Sugeneruota sistemos. | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti poziciją.  |
| **Pirminis laukas**<br>mshr_primaryfield<br>*Eilutė* | Būtina<br>Sistemos sugeneruota |  |
| **Darbo pareigų ID reikšmė**<br>„_mshr_fk_positionjob_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity” |Darbo ID yra susietas su pareigomis.|
| **Pastovios atlyginimo dalies plano ID reikšmė**<br>„_mshr_fk_fixedcompplan_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity”  | Pastovios atlyginimo dalies plano ID yra susietas su pareigomis. |
| **Mokėjimų ciklo ID**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigose apibrėžtas mokėjimo ciklas. |
| **Apmokėta juridinio subjekto**<br>„paidbylegalentity”<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigose apibrėžtas juridinis subjektas, atsakingas už apmokėjimus. |
| **Pareigų ID**<br>mshr_positionid<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigų ID. |
| **Galioja iki**<br>„validto”<br>*Datos ir Laiko poslinkis* | Tik skaitomas<br>Būtina |Data, nuo kurios galioja išsami informacija apie pareigas.  |
| **Galioja nuo**<br>„validfrom”<br>*Datos ir Laiko poslinkis* | Tik skaitomas<br>Būtina |Data, iki kurios galioja išsami informacija apie pareigas.  |

**Užklausa**

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
