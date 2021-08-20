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
ms.openlocfilehash: 05e9d6441cf99dce3f4663b9d5ba57e2b386e8c2f3060f75550270083f3b98b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741458"
---
# <a name="payroll-position"></a>Algalapių padėtis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomas Pareigų algalapio objektas „Dynamics 365 Human Resources“.

Faktinis pavadinimas: „mshr_payrollpositionentity”.

### <a name="description"></a>Aprašas

Šiame objekte pateikta informacija apie nurodytą darbuotojo pareigas.

Faktinis pavadinimas: 

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Įprastos darbo valandos per metus**<br>„annualregularhours”<br>*Dešimtainis* | Tik skaitomas<br>Būtina | Pareigoms nustatytos įprastos darbo valandos per metus.  |
| **Išsamios algalapio pareigų informacijos objekto ID**<br>„payrollpositiondetailsentityid”<br>*Guid* | Būtina<br>Sugeneruota sistemos. | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti poziciją.  |
| **Pirminis laukas**<br>mshr_primaryfield<br>*Eilutė* | Būtina<br>Sistemos sugeneruota |  |
| **Darbo pareigų ID reikšmė**<br>„_mshr_fk_positionjob_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity” |Darbo ID yra susietas su pareigomis.|
| **Pastovios atlyginimo dalies plano ID reikšmė**<br>„_mshr_fk_fixedcompplan_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity”  | Pastovios atlyginimo dalies plano ID yra susietas su pareigomis. |
| **Mokėjimų ciklo ID**<br>mshr_primaryfield<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigose apibrėžtas mokėjimo ciklas. |
| **Apmokėta juridinio subjekto**<br>„paidbylegalentity”<br>*Eilutė* | Tik skaitomas<br>Būtina | Juridinis subjektas, atsakingas už apmokėjimus, apibrėžtas pareigose. |
| **Pareigų ID**<br>mshr_positionid<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigų ID. |
| **Galioja iki**<br>„validto”<br>*Datos ir Laiko poslinkis* | Tik skaitomas<br>Būtina |Data, nuo kurios galioja išsami informacija apie pareigas.  |
| **Galioja nuo**<br>„validfrom”<br>*Datos ir Laiko poslinkis* | Tik skaitomas<br>Būtina |Data, iki kurios galioja išsami informacija apie pareigas.  |

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
