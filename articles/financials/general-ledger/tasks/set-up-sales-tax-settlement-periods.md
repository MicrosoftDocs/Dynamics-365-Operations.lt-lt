---
title: Nustatyti PVM sudengimo laikotarpius
description: PVM sudengimo laikotarpiuose pateikiama informacija apie laikotarpių intervalus, už kuriuos reikia pranešti apie PVM ir jį sumokėti.
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
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862993"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Nustatyti PVM sudengimo laikotarpius

[!include [task guide banner](../../includes/task-guide-banner.md)]

PVM sudengimo laikotarpiuose pateikiama informacija apie laikotarpių intervalus, už kuriuos reikia pranešti apie PVM ir jį sumokėti. Galima vykdyti konkrečios datos intervalo sudengimo laikotarpio procesą. Bus sudengti visi mokesčių kodai, susieti su sudengimo laikotarpiu. Atsižvelgiant į susijusios PVM institucijos sąranką, mokestiniai įsipareigojimai registruojami arba tiekėjui, arba DK sąskaitoje.



Šioje užduotyje naudojama demonstracinė įmonė USMF.



1. Pasirinkite Mokestis > Netiesioginiai mokesčiai > PVM > PVM sudengimo laikotarpiai.
2. Spustelėkite Naujas.
3. Lauke Sudengimo laikotarpis surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Institucija pasirinkite PVM instituciją, kuri gauna ataskaitas ir mokėjimus, sukurtus už sudengimo laikotarpį.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke Mokėjimo sąlygos spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Susijusią PVM instituciją galima nustatyti kaip tiekėją ir, sudengiant PVM, bus sukurta atidaryta tiekėjo SF. Mokėjimo sąlygos apibrėžia atidarytos tiekėjo SF terminą.  
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Pasirinkite sudengimo laikotarpių intervalų tipą.
12. Įveskite laikotarpio intervalo vienetų skaičių vienam laikotarpiui. Pavyzdžiui, ketvirtį sudaro 3 mėnesiai.
13. Pažymėkite arba atžymėkite žymės langelį Sudengiant PVM naudoti paketinį apdorojimą.
    * Sudengimo laikotarpio procesą galima apdoroti kaip paketinę užduotį fone. Tai rekomenduojama atlikti su daug mokesčių operacijų, patenkančių į laikotarpio intervalą.  
    > [!NOTE]
    > Šiuo metu ši funkcija nepalaikoma Austrijoje, Belgijoje, Ispanijoje, Italijoje, Japonijoje ir Nyderlanduose.
14. Pažymėkite arba išvalykite žymės langelį Neleisti generuoti korespondentinių mokesčių operacijų.
    * Pagal numatytuosius parametrus sudengimo proceso metu sistema generuoja korespondentines mokesčių operacijas, galinčias sukelti našumo problemų, jei laikotarpio intervale yra daug mokesčių operacijų. Norėdami neleisti generuoti korespondentinių mokesčių operacijų pažymėkite šį žymės langelį.
15. Išplėskite skirtuką Laikotarpio intervalai.
16. Spustelėkite Pridėti.
17. Sąraše pažymėkite pasirinktą eilutę.
18. Lauke Pradžios data įveskite datą.
19. Lauke Pabaigos data įveskite datą.
20. Spustelėkite Naujas laikotarpio intervalas.
    * Įvedus pirmąjį laikotarpio intervalą, galima automatiškai kurti naujus laikotarpius. Jei reikia, galite grįžti ir pridėti naujų laikotarpių intervalų.  
21. Uždarykite puslapį.

