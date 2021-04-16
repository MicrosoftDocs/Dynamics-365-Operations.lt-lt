---
title: Kurti daug pardavimo pasiūlymų
description: Ši procedūra parodo, kaip efektyviai kurti pasiūlymus, kuriuose siūlomi produktų ar paslaugų rinkiniai, ketinami siųsti keliems klientams.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0422817576d9d93d0ec6bbfb5f3777013ee09ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817706"
---
# <a name="mass-create-sales-quotations"></a>Kurti daug pardavimo pasiūlymų

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip efektyviai kurti pasiūlymus, kuriuose siūlomi produktų ar paslaugų rinkiniai, ketinami siųsti keliems klientams. Šis masinis pasiūlymo kūrimas pagrįstas pasiūlymų šablonais. Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.


## <a name="create-a-quotation-template"></a>Kurti pasiūlymo šabloną
1. Eikite į Pardavimas ir rinkodaras > Nustatymas > Pasiūlymai > Šablonų grupės.
2. Spustelėkite Naujas.
3. Lauke Grupės ID įveskite savo pasirinktą ID.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Uždarykite puslapį.
7. Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.
8. Spustelėkite Naujas.
9. Lauke Sąskaitos tipas pasirinkite Klientas.
10. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
11. Spustelėkite GERAI.
    * Tam, kad pasiūlymas taptų šablonu, turite atlikti pasiūlymo antraštės nustatymo veiksmus. Tai reikia padaryti prieš įtraukiant eilutes į pasiūlymą.   
12. Veiksmų srityje spustelėkite Parinktys.
13. Spustelėkite Keisti rodinį.
14. Spustelėkite antraštės rodinį.
15. Išplėskite skyrių Nustatymas.
16. Lauke Grupės ID įveskite arba pasirinkite vertę.
17. Lauke Šablono pavadinimas surinkite reikšmę.
18. Lauke Aktyvus pasirinkite Taip.
    * Kai taikote šabloną naujam pardavimo pasiūlymui, galima naudoti tik aktyvius šablonus.  
19. Veiksmų srityje spustelėkite Parinktys.
20. Spustelėkite Keisti rodinį.
21. Spustelėkite Eilutės rodinys.
22. Lauke Prekė įveskite arba pasirinkite vertę.
23. Lauke Prekė įveskite vertę.
24. Uždarykite puslapį.
25. Lauke Nuolaidos procentas įveskite skaičių.
26. Spustelėkite Pridėti eilutę.
27. Lauke Prekė įveskite arba pasirinkite vertę.
28. Lauke Prekė įveskite vertę.
29. Uždarykite puslapį.
30. Lauke Vieneto kaina įveskite naują kainą arba pakeiskite dabartinę.
31. Spustelėkite Pridėti eilutę.
32. Lauke Prekė įveskite arba pasirinkite vertę.
33. Lauke Prekė įveskite vertę.
34. Uždarykite puslapį.
35. Lauke Kiekis įveskite skaičių.
36. Lauke Nuolaida įveskite skaičių.
37. Spustelėkite Įrašyti.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Taikyti šabloną vienam pasiūlymui sukurti
1. Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.
    * Atkreipkite dėmesį, kad pasiūlymas, kurį ką tik sukūrėte pažymėtas kaip šablonas.  
2. Spustelėkite Naujas.
3. Lauke Sąskaitos tipas pasirinkite Klientas.
4. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
5. Išplėskite skyrių Šablonas.
6. Lauke Grupės ID įveskite arba pasirinkite vertę.
7. Lauke Šablono pavadinimas įveskite arba pasirinkite vertę.
8. Lauke Skaičiavimo metodas, pasirinkite 'Pagrįsta šablonų vertėmis'.
9. Spustelėkite GERAI.
    * Naujas pasiūlymas sukurtas atsižvelgiant į šablono duomenis ir sąlygas.  
10. Uždarykite puslapį.
11. Uždarykite puslapį.

## <a name="apply-the-template-to-mass-create-quotations"></a>Taikyti šabloną kuriant daug pasiūlymų
1. Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Pasiūlymo atnaujinimas > Kurti daug pasiūlymų.
2. Lauke Sąskaitos tipas pasirinkite Klientas.
3. Lauke Grupės ID įveskite arba pasirinkite vertę.
4. Lauke Šablono pavadinimas įveskite arba pasirinkite vertę.
5. Lauke Skaičiavimo metodas, pasirinkite 'Pagrįsta šablonų vertėmis'.
6. Išplėskite dalį Įtrauktini įrašai.
7. Spustelėkite Filtras.
8. Lauke Kriterijus nustatykite filtrą, kuris apimtų diapazoną klientų, kuriuos norite įtraukti į šio masinio pasiūlymo kūrimą. Naudokite šį formatą: „Customer1... CustomerN.
    * Pvz., galite nustatyti filtrą į: US-001... US-004  
9. Spustelėkite GERAI.
10. Spustelėkite GERAI.
11. Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.
    * Patikrinkite, kad pasiūlymai buvo sukurti visiems klientams, nurodytiems masinio atnaujinimo procedūros metu, remiantis pasirinktu šablonu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]