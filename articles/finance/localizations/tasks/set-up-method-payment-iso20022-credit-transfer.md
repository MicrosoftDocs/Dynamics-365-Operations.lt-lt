---
title: Nustatyti ISO20022 kredito pervedimo mokėjimo būdą
description: Šioje procedūroje parodoma, kaip nustatyti tiekėjo mokėjimo būdą, skirtą atlikti ISO20022 kredito pervedimą arba kito tipo mokėjimą, naudojant elektronines ataskaitas failui generuoti.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f87cc0dfa47295f047ef97732f60733c362ca4066d9070418322b34934e3ce3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773665"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]