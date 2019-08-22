---
title: Nustatyti garantinio rašto banko priemones ir registravimo šablonus
description: Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 427159048ffbb17749e813d67a900622900a7f21
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841926"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Nustatyti garantinio rašto banko priemones ir registravimo šablonus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.



Šioje užduotyje naudojama demonstracinė įmonė USMF. 




## <a name="general-ledger-parameter"></a>Didžiosios knygos parametras
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.
2. Išplėskite skyrių Banko dokumentas.
3. Pasirinkite parinktį Įjungti garantinį raštą.
4. Lauke Operacijų žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite skirtuką Numeracijos.
    * Garantinio rašto numerio ir garantinio rašto operacijos nuorodų numeracijos kodo nustatymas  
8. Spustelėkite Įrašyti.
9. Uždarykite puslapį.

## <a name="create-bank-facility"></a>Banko priemonės kūrimas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko priemonės.
2. Spustelėkite Naujas.
3. Lauke Priemonių grupė įveskite garantinio rašto operacijos banko priemonių grupės pavadinimą.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite skirtuką Paslaugų tipai.
7. Spustelėkite Naujas.
8. Lauke Priemonės tipas įveskite banko priemonės tipo, kuris yra susijęs su banko priemonės sutartimi, pavadinimą.
9. Lauke Aprašas surinkite reikšmę.
10. Lauke Priemonių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Lauke Priemonės pobūdis pasirinkite parinktį.
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.

## <a name="bank-posting-profile"></a>Banko registravimo šablonas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko dokumentų registravimo šablonas.
2. Spustelėkite Naujas.
3. Lauke Sąskaitos / grupės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke Sudengimo sąskaita pasirinkite pagrindinę sudengimo sąskaitą.
7. Lauke Išlaidų sąskaita pasirinkite išlaidų operacijų sąskaitą.
8. Lauke Maržos sąskaita pasirinkite maržos operacijos sąskaitą.
9. Lauke Likvidavimo sąskaita pasirinkite garantinio rašto operacijos likvidavimo sąskaitą. 
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.

