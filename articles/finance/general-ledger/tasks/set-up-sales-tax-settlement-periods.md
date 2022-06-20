---
title: Nustatyti PVM sudengimo laikotarpius
description: Šiame straipsnyje paaiškinama, kaip nustatyti PVM sudengimo laikotarpius "Dynamics 365 Finance".
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f8514494b5d3534fc236def817df0d58fe80d70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846689"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Nustatyti PVM sudengimo laikotarpius

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti PVM sudengimo laikotarpius. PVM sudengimo laikotarpiuose pateikiama informacija apie laikotarpių intervalus, už kuriuos reikia pranešti apie PVM ir jį sumokėti. Galima vykdyti konkrečios datos intervalo sudengimo laikotarpio procesą. Bus sudengti visi mokesčių kodai, susieti su sudengimo laikotarpiu. Atsižvelgiant į susijusios PVM institucijos sąranką, mokestiniai įsipareigojimai registruojami arba tiekėjui, arba DK sąskaitoje.

Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pereikite į **PVM > sudengimo > PVM > pvm sudengimo laikotarpius**.
2. Pasirinkite **Naujas**.
3. Lauke **Sudengimo laikotarpis** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Institucija** pasirinkite PVM instituciją, kuri gauna už sudengimo laikotarpį sukurtas ataskaitas ir mokėjimus.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Lauke **Mokėjimo sąlygos** iš išplečiamojo meniu pasirinkite norimą įrašą. Susijusią PVM instituciją galima nustatyti kaip tiekėją ir, sudengiant PVM, bus sukurta atidaryta tiekėjo SF. Mokėjimo sąlygos apibrėžia atidarytos tiekėjo SF terminą.  
8. Pasirinkite sudengimo laikotarpių intervalų tipą.
9. Įveskite laikotarpio intervalo vienetų skaičių vienam laikotarpiui. Pavyzdžiui, ketvirtį sudaro 3 mėnesiai.
10. Pažymėkite arba išvalykite žymės langelį **Sudengiant PVM naudoti paketinį apdorojimą**. Sudengimo laikotarpio procesą galima apdoroti kaip paketinę užduotį fone. Tai rekomenduojama atlikti su daug mokesčių operacijų, patenkančių į laikotarpio intervalą.
11. Pažymėkite arba išvalykite žymės langelį **Neleisti generuoti korespondentinių mokesčių operacijų**. Pagal numatytuosius parametrus sudengimo proceso metu sistema generuoja korespondentines mokesčių operacijas, galinčias sukelti našumo problemų, jei laikotarpio intervale yra daug mokesčių operacijų. Norėdami neleisti generuoti korespondentinių mokesčių operacijų pažymėkite šį žymės langelį.
12. Išplėskite skirtuką **Laikotarpio intervalai**.
13. Pasirinkite **Įtraukti**.
14. Lauke **Pradžios data** naujoje eilutėje įveskite datą.
15. Lauke **Pabaigos data** įveskite datą.
16. Pasirinkite **Naujo laikotarpio intervalas**. Įvedus pirmąjį laikotarpio intervalą, galima automatiškai kurti naujus laikotarpius. Jei reikia, galite grįžti ir pridėti naujų laikotarpių intervalų.  
17. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
