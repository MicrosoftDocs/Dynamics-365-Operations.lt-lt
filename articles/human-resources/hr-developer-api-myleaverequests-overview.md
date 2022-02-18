---
title: MyLeaveRequests apžvalga
description: Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41ef8c6fc0e896e7f2cefd94801abab610083b81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070873"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests apžvalga


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.

## <a name="key"></a>Raktas

  | Ypatybės pavadinimas | Duomenų tipas |
  |---------------|-----------|
  | dataAreaId    | Eilutė    |
  | RequestId     | Eilutė    |
  | „LeaveType”     | Eilutė    |
  | LeaveDate     | Data      |
  
## <a name="properties"></a>Ypatybės

  | Ypatybės pavadinimas     | Duomenų tipas | Būtinas |
  |-------------------|-----------|----------|
  | dataAreaId        | Eilutė    | X        |
  | RequestId         | Eilutė    | X        |
  | „LeaveType”         | Eilutė    | X        |
  | LeaveDate         | Data      | X        |
  | ReasonCodeId      | Eilutė    |          |
  | PersonnelNumber   | Eilutė    | X        |
  | RequestDate       | Data      | X        |
  | Komentuoti           | Eilutė    |          |
  | Būsena            | Išvardijimas      | X        |
  | Suma            | Tikrasis      |          |
  | HalfDayDefinition | Išvardijimas      |          |

## <a name="actions"></a>Veiksmai

 | Veiksmo pavadinimas                               | Aprašymas                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [pateikti](hr-developer-api-myleaverequests-submit.md)   | Pateikti užklausą, kurią reikia apdoroti naudojant darbo eigą. |

## <a name="see-also"></a>Taip pat žiūrėkite

- [Prašymo išeiti atostogų pateikimas darbo eigai](hr-developer-api-myleaverequests-submit.md)
- [Autentifikavimas](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
