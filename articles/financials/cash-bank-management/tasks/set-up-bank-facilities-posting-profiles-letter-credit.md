--- 
title: "Nustatyti akredityvo banko priemones ir registravimo šablonus"
description: "Ši procedūra padeda sukurti banko priemonę ir užregistruoti šabloną, reikalingą norint apdoroti akredityvus."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 43422627f8529768ab9377c04568da531d6565c6
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Nustatyti akredityvo banko priemones ir registravimo šablonus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padeda sukurti banko priemonę ir užregistruoti šabloną, reikalingą norint apdoroti akredityvus. 

Šioje užduotyje naudojama demonstracinė įmonė „USMF‟.






## <a name="general-ledger-parameter"></a>Didžiosios knygos parametras
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.
2. Išplėskite skyrių Banko dokumentas.
3. Pasirinkite parinktį Įjungti importo akredityvą.
4. Pasirinkite parinktį Įjungti eksporto akredityvą.
5. Spustelėkite Įrašyti.
6. Uždarykite puslapį.

## <a name="create-bank-facility"></a>Banko priemonės kūrimas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko priemonės.
2. Spustelėkite Naujas.
3. Lauke Priemonių grupė įveskite banko priemonių grupės pavadinimą.
4. Lauke Aprašas įveskite banko priemonių grupės aprašymą.
5. Spustelėkite Įrašyti.
6. Spustelėkite skirtuką Paslaugų tipai.
7. Spustelėkite Naujas.
8. Lauke Paslaugų tipai įveskite unikalų kodą.
9. Lauke Aprašas įveskite reikšmę.
10. Lauke Priemonių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Lauke Priemonės pobūdis pasirinkite banko priemonės pobūdį.
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.

## <a name="bank-posting-profile"></a>Banko registravimo šablonas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko dokumentų registravimo šablonas.
2. Spustelėkite Naujas.
3. Lauke Sąskaitos / grupės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Pasirinkite pagrindinę atsiskaitymo sąskaitą.
    * Ši sąskaita naudojama skaičiuojant grynųjų pinigų srautų prognozę.  
7. Lauke Išlaidų sąskaita pasirinkite išlaidų operacijų sąskaitą.
8. Lauke Maržos sąskaita pasirinkite maržos operacijų sąskaitą.
    * Ši sąskaita debetuojama registruojant atidarymo maržą ir kredituojama registruojant mokėjimą.  
9. Spustelėkite Įrašyti.


