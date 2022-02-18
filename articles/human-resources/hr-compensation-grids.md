---
title: Kompensavimo tinklelių nustatymas
description: Kompensavimo tinkleliai naudojami nustatyti ir prižiūrėti pastoviųjų atlyginimo dalių planų mokėjimo struktūras.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51b98320eac539e49787d352f32683efadc11f41
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071753"
---
# <a name="set-up-compensation-grids"></a>Kompensavimo tinklelių nustatymas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensavimo tinkleliai naudojami nustatyti ir prižiūrėti pastoviųjų atlyginimo dalių planų mokėjimo struktūras. Kompensacijos tinklelius galima bendrai naudoti keliems planams arba nukopijuoti kuriant naują kompensavimo planą.  Prieš kuriant kompensacijos tinklelį, Lygiai ir Nuorodos taškai turi būti nustatyti. Šiame pavyzdyje bus sukurtas naujas kompensacijos tinklelio Klasės tipas naudojant demonstracinius duomenis Lygiams ir Nuorodos taškams. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Nustatyti informaciją apie kompensacijos tinklelį
1. Eikite į **Personalas** > **Kompensacija** > **Pastovioji atlyginimo dalis** > **Kompensacijos tinkleliai**.
2. Spustelėkite **Naujas**.
3. Lauke **Tinklelis** įveskite vertę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Tipas** pasirinkite parinktį.
6. Nustatymo lauke **Nuoroda** įveskite arba pasirinkite vertę.
7. Lauke **Valiuta** įveskite arba pažymėkite reikšmę.
8. Lauke **Įsigaliojimo data** įveskite datą.

## <a name="add-levels-to-the-compensation-structure"></a>Įtraukti lygius į kompensacijos struktūrą
1. Spustelėkite **Kompensacijos struktūra**.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke **Lygis** įveskite arba pasirinkite vertę.
4. Spustelėkite **Naujas**.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke **Lygis** įveskite arba pasirinkite vertę.
7. Spustelėkite **Naujas**.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke **Lygis** įveskite arba pasirinkite vertę.
10. Spustelėkite **Naujas**.
11. Sąraše pažymėkite pasirinktą eilutę.
12. Lauke **Lygis** įveskite arba pasirinkite vertę.
13. Spustelėkite **Naujas**.
14. Sąraše pažymėkite pasirinktą eilutę.
15. Lauke **Lygis** įveskite arba pasirinkite vertę.

## <a name="fill-in-the-compensation-structure-with-values"></a>Užpildyti kompensacijos struktūrą vertėmis
1. Sąraše pažymėkite pasirinktą eilutę.
    * Šiuo momentu kompensacijų vertes galima įvesti rankiniu būdu į kiekvieną lentelės lauką arba galima naudoti Masinio keitimo funkciją norint lengvai užpildyti kelis laukus ir atlikti pagrindinius skaičiavimus.  
2. Spustelėkite **Masinis keitimas**.
    * Šiam tinkleliui pirmiausia pritaikysime pirmojo lygio vidurio taško vertę visuose lentelės laukuose. Tai bus kompensavimo matricos pagrindas.  
3. Lauke **Koregavimo tipas** pasirinkite parinktį.
4. Lauke **Koregavimo suma** įveskite skaičių.
5. Pažymėkite arba atžymėkite visas sąrašo eilutes.
6. Spustelėkite **Taikyti tinkleliui**.
    * Dabar naudojame masinio keitimo funkciją sumai padidinti kiekviename tolesniame lygyje pagal tam tikrą procentą arba sumą. Šiame pavyzdyje kiekvienas lygis turės 12,5 % paplitimą tarp jų vidurio taškų.  
7. Lauke **Koregavimo tipas** pasirinkite parinktį.
8. Lauke **Koregavimo suma** įveskite skaičių.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Spustelėkite **Taikyti tinkleliui**.
    * Dabar naudosime masinio keitimo funkciją kiekvieno lygio minimaliam ir maksimaliam nuorodos taškams koreguoti. Šiame pavyzdyje naudosime 50 % paplitimą, kad Minimalus atskaitos taškas būtų pakoreguotas -20 %, o Maksimalus – pakoreguotas +20 %.  
11. Lauke **Koregavimo suma** įveskite skaičių.
12. Lauke **Nuorodos taškas** įveskite arba pasirinkite vertę.
13. Pažymėkite arba atžymėkite visas sąrašo eilutes.
14. Spustelėkite **Taikyti tinkleliui**.
15. Lauke **Koregavimo suma** įveskite skaičių.
16. Lauke **Nuorodos taškas** įveskite arba pasirinkite vertę.
17. Pažymėkite arba atžymėkite visas sąrašo eilutes.
18. Spustelėkite **Taikyti tinkleliui**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
