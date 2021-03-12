---
title: Nustatyti ISO20022 kredito pervedimo mokėjimo būdą
description: Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92bc314e69628f2a287ba7c9a7c2d3d73a0bfd33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988107"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Nustatyti ISO20022 kredito pervedimo mokėjimo būdą

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti. 

Prieš atlikdami šią užduotį, turite nustatyti eksporto formato konfigūracijas ir mokėjimo sąskaitas.

Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF.

Tai yra trečioji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.

1. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Mokėjimo būdas reikšme „SEPA CT“.
3. Spustelėkite Redaguoti.
4. Lauke Laikotarpis pasirinkite „Iš viso‟.
5. Lauke Mokėjimo tipas pasirinkite „Elektroninis mokėjimas“.
6. Išplėskite dalį Failo formatai.
7. Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.
8. Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.
    * Sąraše pasirinkite reikšmę ISO20022 kredito pervedimas (DE). Jei sąrašas yra tuščias, nėra importuotos ir aktyvios tiekėjo mokėjimų eksporto formato konfigūracijos.  
9. Lauke Kliento sąskaita pasirinkite „Bankas‟.
10. Lauke Mokėjimo sąskaita nurodykite reikšmes „DEMF OPER‟.
11. Spustelėkite Įrašyti.

