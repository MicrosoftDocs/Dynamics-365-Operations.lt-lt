---
title: PVM sudengimo laikotarpių nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti PVM sudengimo laikotarpius sistemoje „Dynamics 365 Finance“.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c17a0240c29dad58c958ab1ce844ee5d8384bd1f
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658934"
---
# <a name="set-up-sales-tax-settlement-periods"></a>PVM sudengimo laikotarpių nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje paaiškinta, kaip nustatyti PVM sudengimo laikotarpius. PVM sudengimo laikotarpiuose pateikiama informacija apie laikotarpių intervalus, už kuriuos reikia pranešti apie PVM ir jį sumokėti. Galima vykdyti konkrečios datos intervalo sudengimo laikotarpio procesą. Bus sudengti visi mokesčių kodai, susieti su sudengimo laikotarpiu. Atsižvelgiant į susijusios PVM institucijos sąranką, mokestiniai įsipareigojimai registruojami arba tiekėjui, arba DK sąskaitoje.

Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Naršymo srityje eikite į **Moduliai > Mokestis > Netiesioginiai mokesčiai > PVM > PVM sudengimo laikotarpiai**.
2. Pasirinkite **Naujas**.
3. Lauke **Sudengimo laikotarpis** įveskite reikšmę.
4. Lauke **Aprašo laukas**surinkite reikšmę.
5. Lauke **Institucija** pasirinkite PVM instituciją, kuri gauna už sudengimo laikotarpį sukurtas ataskaitas ir mokėjimus.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Lauke **Mokėjimo sąlygos** iš išplečiamojo meniu pasirinkite norimą įrašą. Susijusią PVM instituciją galima nustatyti kaip tiekėją ir, sudengiant PVM, bus sukurta atidaryta tiekėjo SF. Mokėjimo sąlygos apibrėžia atidarytos tiekėjo SF terminą.  
8. Pasirinkite sudengimo laikotarpių intervalų tipą.
9. Įveskite laikotarpio intervalo vienetų skaičių vienam laikotarpiui. Pavyzdžiui, ketvirtį sudaro 3 mėnesiai.
10. Pažymėkite arba išvalykite žymės langelį **Sudengiant PVM naudoti paketinį apdorojimą**. Sudengimo laikotarpio procesą galima apdoroti kaip paketinę užduotį fone. Tai rekomenduojama atlikti su daug mokesčių operacijų, patenkančių į laikotarpio intervalą.  
    > [!NOTE]
    > Šiuo metu ši funkcija nepalaikoma Ispanijoje, Japonijoje ir Nyderlanduose.
11. Pažymėkite arba išvalykite žymės langelį **Neleisti generuoti korespondentinių mokesčių operacijų**. Pagal numatytuosius parametrus sudengimo proceso metu sistema generuoja korespondentines mokesčių operacijas, galinčias sukelti našumo problemų, jei laikotarpio intervale yra daug mokesčių operacijų. Norėdami neleisti generuoti korespondentinių mokesčių operacijų pažymėkite šį žymės langelį.
12. Išplėskite skirtuką **Laikotarpio intervalai**.
13. Pasirinkite **Įtraukti**.
14. Lauke **Pradžios data** naujoje eilutėje įveskite datą.
15. Lauke **Pabaigos data** įveskite datą.
16. Pasirinkite **Naujo laikotarpio intervalas**. Įvedus pirmąjį laikotarpio intervalą, galima automatiškai kurti naujus laikotarpius. Jei reikia, galite grįžti ir pridėti naujų laikotarpių intervalų.  
17. Uždarykite puslapį.

