---
title: Nustatyti garantinio rašto banko priemones ir registravimo šablonus
description: Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bfdef0cd535f47bb1df9fb7494043d3dd519c5b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779886"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Nustatyti garantinio rašto banko priemones ir registravimo šablonus

[!include [banner](../../includes/banner.md)]

Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.



Šioje užduotyje naudojama demonstracinė įmonė USMF. 




## <a name="general-ledger-parameter"></a>Didžiosios knygos parametras
1. Pereikite į **grynųjų pinigų ir banko valdymo > nustatykite > grynųjų pinigų ir banko valdymo parametrus**.
2. Išplėskite banko **dokumento** skyrių.
3. Pasirinkite parinktį **Įjungti garantinį** raštą.
4. Operacijos žurnalo **lauke** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite skirtuką **Numeracijos**.
    * Garantinio rašto numerio ir garantinio rašto operacijos nuorodų numeracijos kodo nustatymas  
8. Spustelėkite **Įrašyti**.
9. Uždarykite puslapį.

## <a name="create-bank-facility"></a>Banko priemonės kūrimas
1. Pereikite prie **grynųjų pinigų ir banko valdymo > Banko > priemonės**.
2. Spustelėkite **Naujas**.
3. Lauke Priemonių **grupė įveskite** garantinio rašto operacijos banko paslaugų grupės pavadinimą.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Spustelėkite skirtuką **Priemonės** tipai.
7. Spustelėkite **Naujas**.
8. **Lauke Priemonės tipas** įveskite banko priemonės tipo, susijusio su banko paslaugų sutartimi, pavadinimą.
9. Lauke **Aprašo laukas** surinkite reikšmę.
10. Lauke Priemonės **grupė spustelėkite** išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Lauke **Priemonės pobūdis, pasirinkite pasirinktį.
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.

## <a name="bank-posting-profile"></a>Banko registravimo šablonas
1. Eikite į **grynųjų pinigų ir banko > nustatymo > banko dokumentų registravimo šabloną**.
2. Spustelėkite **Naujas**.
3. Lauke Sąskaitos **/grupės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke Sudengimo **sąskaita** pasirinkite pagrindinę sudengimo sąskaitą.
7. **Lauke Išlaidų sąskaita** pasirinkite išlaidų operacijų sąskaitą.
8. Lauke Maržos **sąskaita** pasirinkite maržos operacijos sąskaitą.
9. Likvidavimo **sąskaitos lauke** pasirinkite garantinio rašto operacijos likvidavimo sąskaitą. 
10. Spustelėkite **Įrašyti**.
11. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
