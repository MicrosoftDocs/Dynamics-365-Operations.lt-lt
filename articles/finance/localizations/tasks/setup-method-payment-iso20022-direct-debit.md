---
title: ISO20022 tiesioginio debeto mokėjimo būdo nustatymas
description: Šioje procedūroje parodoma, kaip nustatyti kliento mokėjimo būdą, skirtą atlikti ISO20022 tiesioginio debeto arba bet kokio kito tipo mokėjimą, naudojant elektronines ataskaitas.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c6a692553867d7e8679099210dc44b9d9e4d0f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838687"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>ISO20022 tiesioginio debeto mokėjimo būdo nustatymas

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]