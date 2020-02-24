---
title: MyLeaveRequests apžvalga
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009935"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests apžvalga

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