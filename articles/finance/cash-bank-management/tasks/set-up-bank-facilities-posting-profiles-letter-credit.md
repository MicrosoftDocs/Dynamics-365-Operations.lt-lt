---
title: Nustatyti akredityvo banko priemones ir registravimo šablonus
description: Ši procedūra padeda sukurti banko priemonę ir užregistruoti šabloną, reikalingą norint apdoroti akredityvus.
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
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779468"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Nustatyti akredityvo banko priemones ir registravimo šablonus

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda sukurti banko priemonę ir užregistruoti šabloną, reikalingą norint apdoroti akredityvus. 

Šioje užduotyje naudojama demonstracinė įmonė „USMF‟.


## <a name="general-ledger-parameter"></a>Didžiosios knygos parametras
1. Pereikite į **grynųjų pinigų ir banko valdymo > nustatykite > grynųjų pinigų ir banko valdymo parametrus**.
2. Išplėskite banko **dokumento** skyrių.
3. Pasirinkite parinktį **Įgalinti importo akredityvo** funkciją.
4. Pasirinkite parinktį **Įgalinti eksporto akredityvo** funkciją.
5. Spustelėkite **Įrašyti**.
6. Uždarykite puslapį.

## <a name="create-bank-facility"></a>Banko priemonės kūrimas
1. Pereikite prie **grynųjų pinigų ir banko valdymo > Banko > priemonės**.
2. Spustelėkite **Naujas**.
3. Lauke Paslaugų **grupė** įveskite banko paslaugų grupės pavadinimą.
4. **Lauke Aprašas** įveskite banko priemonių grupės aprašymą.
5. Spustelėkite **Įrašyti**.
6. Spustelėkite skirtuką **Priemonės** tipai.
7. Spustelėkite **Naujas**.
8. **Lauke Priemonės tipas** įveskite unikalų kodą.
9. Lauke **Aprašo laukas** surinkite reikšmę.
10. Lauke Priemonės **grupė spustelėkite** išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. **Priemonės pobūdžio lauke** pasirinkite banko priemonės pobūdį.
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.

## <a name="bank-posting-profile"></a>Banko registravimo šablonas
1. Eikite į **grynųjų pinigų ir banko > nustatymo > banko dokumentų registravimo šabloną**.
2. Spustelėkite **Naujas**.
3. Lauke Sąskaitos **/grupės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Pasirinkite pagrindinę atsiskaitymo sąskaitą.
    * Ši sąskaita naudojama skaičiuojant grynųjų pinigų srautų prognozę.  
7. **Lauke Išlaidų sąskaita** pasirinkite išlaidų operacijų sąskaitą.
8. Lauke Maržos **sąskaita** pasirinkite maržos operacijų sąskaitą.
    * Ši sąskaita debetuojama registruojant atidarymo maržą ir kredituojama registruojant mokėjimą.  
9. Spustelėkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
