---
title: Algalapio pastoviosios atlyginimo dalies planas
description: Šioje temoje pateikiama informacija ir Algalapio pastoviosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021301"
---
# <a name="payroll-fixed-compensation-plan"></a>Algalapio pastoviosios atlyginimo dalies planas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje pateikiama informacija ir Algalapio pastoviosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudoti | Aprašas |
| --- | --- | --- |
| **Darbuotojo ID**<br>„mshr_fk_employee_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_Employee_id of mshr_payrollemployeeentity entity”  | Darbuotojo ID |
| **Užmokesčio tarifas**<br>„mshr_payrate”<br>*Dešimtainis* | Tik skaitomas<br>Būtina | Pastoviosios atlyginimo dalies plane apibrėžtas darbo užmokesčio tarifas. |
| **Plano ID**<br>„mshr_planid”<br>*Eilutė* | Tik skaitomas<br>Būtina |Nurodo atlyginimo dalies planą.  |
| **Galioja nuo**<br>„mshr_validfrom”<br>*Datos ir Laiko poslinkis* |  Tik skaitomas<br>Būtina |Data, nuo kurios galioja darbuotojo pastovioji atlyginimo dalis.  |
| **Algalapio pastoviosios atlyginimo dalies objektas**<br>„mshr_payrollfixedcompensationplanentityid”<br>*GUID* | Būtina<br>Sugeneruota sistemos | Sistemos sukurta GUID vertė siekiant unikaliai atpažinti atlyginimo dalies planą. |
| **Mokėjimų dažnumas**<br>„mshr_payfrequency”<br>*Eilutė* | Tik skaitomas<br>Būtina |Dažnumas, kuriuo bus mokama darbuotojui.  |
| **Galioja iki**<br>„mshr_validto”<br>*Datos ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Data, iki kurios galioja darbuotojo pastovioji atlyginimo dalis. |
| **Pareigų ID**<br>mshr_positionid<br>*Eilutė* | Tik skaitomas <br>Būtina | Pareigų ID, susietas su darbuotoju ir pastoviosios atlyginimo dalies plano registracija. |
| **Valiuta**<br>„mshr_currency”<br>*Eilutė* | Tik skaitomas <br>Būtina |Valiuta, apibrėžta pastoviosios atlyginimo dalies planui   |
| **Personalo numeris**<br>„mshr_personnelnumber”<br>*Eilutė* | Tik skaitomas<br>Būtina |Unikalus darbuotojo personalo numeris.  |

**Užklausa**

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
