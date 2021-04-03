---
title: MyLeaveRequests apžvalga
description: Objektas MyLeaveRequests programoje „Microsoft Dynamics 365 Human Resources“ pateikia sistemoje esančių atostogų užklausų sąrašą, apribotą iki užklausų, pasiekiamų dabartiniam vartotojui, siunčiančiam užklausą šiam objektui.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465515"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests apžvalga

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