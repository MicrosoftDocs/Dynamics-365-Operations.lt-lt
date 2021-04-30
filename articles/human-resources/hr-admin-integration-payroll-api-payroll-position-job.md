---
title: Algalapių pareigų užduotis
description: Šioje temoje pateikiama informacija ir Algalapio pareigų užduoties objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
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
ms.openlocfilehash: 72f3109f5bea36a390b04b7165fc3831d777b640
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882040"
---
# <a name="payroll-position-job"></a>Algalapių pareigų užduotis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje pateikiama informacija ir Algalapio pareigų užduoties ryšio objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.

## <a name="properties"></a>Ypatybės

| Ypatybė<br>**Faktinis pavadinimas**<br>**_Tipas_** | Naudojimas | Aprašas |
| --- | --- | --- |
| **Užduoties ID**<br>mshr_jobid<br>*Eilutė* | Tik skaityti<br>Būtina |Užduoties ID. |
| **Galioja nuo**<br>„mshr_validto”<br>*Datos ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Data, nuo kurios įsigalioja pareigų ir užduoties ryšys. |
| **Galioja iki**<br>„mshr_validto”<br>*Data ir Laiko poslinkis* | Tik skaitomas <br>Būtina | Data, iki kurios galioja pareigų ir užduoties ryšys.  |
| **Pareigų ID**<br>mshr_positionid<br>*Eilutė* | Tik skaitomas<br>Būtina | Pareigų ID. |
| **Pirminis laukas**<br>mshr_primaryfield<br>*Eilutė* | Būtina<br>Sistemos sugeneruota |  |
| **Darbo pareigų ID reikšmė**<br>„_mshr_fk_positionjob_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity” |Darbo ID yra susietas su pareigomis.|
| **Pastovios atlyginimo dalies plano ID reikšmė**<br>„_mshr_fk_fixedcompplan_id_value”<br>*GUID* | Tik skaitomas<br>Būtina<br>Išorinis raktas: „mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity”  | Pastovios atlyginimo dalies plano ID yra susietas su pareigomis. |
| **Algalapio darbo pareigų objekto ID**<br>„mshr_payrollpositionjobentityid”<br>*Guid* | Būtina<br>Sugeneruota sistemos. | Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti užduotį.  |

