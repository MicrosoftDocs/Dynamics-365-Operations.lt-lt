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
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804107"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Nustatyti garantinio rašto banko priemones ir registravimo šablonus

[!include [banner](../../includes/banner.md)]

Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.



Šioje užduotyje naudojama demonstracinė įmonė USMF. 




## <a name="general-ledger-parameter"></a>Didžiosios knygos parametras
1. Eikite į **grynųjų pinigų ir banko valdymo > nustatykite > grynųjų pinigų ir banko valdymo parametrus**.
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
1. Pereikite į **grynųjų pinigų ir banko valdymo > Nustatymo > banko paslaugos**.
2. Spustelėkite **Naujas**.
3. Lauke Priemonių **grupė įveskite** garantinio rašto operacijos banko paslaugų grupės pavadinimą.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Spustelėkite skirtuką **Priemonės** tipai.
7. Spustelėkite **Naujas**.
8.  **Lauke Priemonės tipas** įveskite banko priemonės tipo, susijusio su banko paslaugų sutartimi, pavadinimą.
9. Lauke **Aprašo laukas** surinkite reikšmę.
10. Lauke Priemonės **grupė spustelėkite** išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13.  **Priemonės pobūdžio lauke** pasirinkite pasirinktį.
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.

## <a name="bank-posting-profile"></a>Banko registravimo šablonas
1. Pereikite į **grynųjų pinigų ir banko valdymo > nustatymo > banko dokumentų registravimo šabloną**.
2. Spustelėkite **Naujas**.
3. Lauke Sąskaitos **/grupės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke Sudengimo **sąskaita** pasirinkite pagrindinę sudengimo sąskaitą.
7.  **Lauke Išlaidų sąskaita** pasirinkite išlaidų operacijų sąskaitą.
8. Lauke Maržos **sąskaita** pasirinkite maržos operacijos sąskaitą.
9. Likvidavimo **sąskaitos lauke** pasirinkite garantinio rašto operacijos likvidavimo sąskaitą. 
10. Spustelėkite **Įrašyti**.
11. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
