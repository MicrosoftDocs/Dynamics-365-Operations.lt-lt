---
title: ISO20022 tiesioginio debeto mokėjimo būdo nustatymas
description: Šioje procedūroje parodoma, kaip nustatyti kliento mokėjimo būdą, skirtą atlikti ISO20022 tiesioginio debeto arba bet kokio kito tipo mokėjimą, naudojant elektronines ataskaitas.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848652"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>ISO20022 tiesioginio debeto mokėjimo būdo nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip nustatyti kliento mokėjimo būdą, skirtą atlikti ISO20022 tiesioginio debeto arba bet kokio kito tipo mokėjimą, naudojant elektronines ataskaitas. 



Prieš atlikdami šią užduotį, turite nustatyti eksporto formato konfigūracijas ir mokėjimo sąskaitas.



Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.



Tai yra trečioji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.

1. Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Mokėjimo būdas reikšme „ELEKTRONINIS“.
3. Spustelėkite Redaguoti.
4. Lauke Mokėjimo sąskaita nurodykite reikšmes „DEMF OPER‟.
5. Išplėskite dalį Failo formatai.
6. Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.
7. Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.
    * Sąraše pasirinkite ISO20022 tiesioginis debetas (DE).  Jei sąrašas yra tuščias, nėra importuotos ir aktyvios kliento mokėjimų eksporto formato konfigūracijos.  
8. Lauke Reikalauti įgaliojimo pasirinkite Taip.
    * Pasirinkite kliento mokėjimo formatų parametrą Reikalauti įgaliojimo, kurį nustačius į mokėjimo pranešimą reikia įtraukti įgaliojimo informaciją, pvz., SEPA tiesioginis debetą.  
9. Spustelėkite Įrašyti.

