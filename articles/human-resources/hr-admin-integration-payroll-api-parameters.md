---
title: Algalapių integravimo parametrai
description: Šioje temoje aprašomi „Dynamics 365 Human Resources” algalapio integravimo parametrai.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37d4dc52e7fe5ddd95f43d98267db819a275bd92
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069862"
---
# <a name="payroll-integration-parameters"></a>Algalapių integravimo parametrai


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Prieš naudodami „Dynamics 365 Human Resources” algalapio integravimą, turite nustatyti šioje temoje aprašytus parametrus.

## <a name="enable-payroll-address"></a>Algalapio adreso įgalinimas

Norėdami naudoti algalapio adresą, turite jį įgalinti iš [bendrinamų parametrų formos](hr-setup-shared-parameters.md), esančios Algalapio integravimo skirtuke.

## <a name="define-the-identification-type"></a>Identifikacijos tipo apibrėžimas

Norėdami rodyti identifikacijos tipo ID [algalapio darbuotojo objekte](hr-admin-integration-payroll-api-payroll-employee.md), turite [sukonfigūruoti personalo parametrus](hr-setup-shared-parameters.md) kiekvienai įmonei.

1. Darbo srityje **Kompensacijų valdymas**, esančioje po saitais, pasirinkite **Žmogiškųjų išteklių parametrai**. 
2. Skirtuke **Algalapio integravimas** nurodykite šių laukų vertę.

| Laukas | Aprašas |
| --- | --- |
| Apdorodami algalapius naudokite identifikacijos tipus | Pasirinkus šią parinktį, pasirinkto tipo ID bus rodomas algalapio darbuotojo objekte. |
| Identifikacijos tipas | Identifikavimo tipas bus rodomas [algalapio darbuotojo objekto](hr-admin-integration-payroll-api-payroll-employee.md) lauke **„mshr_payrollemployeeentityid”**. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
