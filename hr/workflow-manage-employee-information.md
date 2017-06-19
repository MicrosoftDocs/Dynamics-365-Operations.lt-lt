---
title: Darbo eigos naudojimas darbuotojo informacijai tvarkyti
description: "Šioje temoje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją. Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 806860e5df9252c074e04e9e1670f4215fd94ca2
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Darbo eigos naudojimas darbuotojo informacijai tvarkyti

[!include[banner](includes/banner.md)]


Šioje temoje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją. Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus.

Darbo eigos tinkamumas personalui suteikia galimybę pritaikyti daugybę darbo eigų personalo veiklai tvarkyti. Be to, yra daugybė parinkčių, kuriomis pasinaudoję galite modifikuoti konkrečias darbo eigas ir susieti jas su ataskaitų hierarchija. Naudojant darbo eigas jos padeda tvarkyti keleto standartinių darbuotojo informacijos tipų pokyčius. Darbo eigą galite susieti su pareigomis. Tada, jei darbuotojai pakeičia savo įrašus, pradedama darbo eiga, kurią reikia patvirtinti prieš išsaugant naują informaciją. Toliau nurodytų informacijos tipų darbo eigos yra nustatytos iš karto, kad padėtų efektyviai tvarkyti pokyčius, o darbuotojų duomenys išliktų tikslūs.

-   Identifikavimo numeriai
-   Kursai
-   Išsilavinimas
-   Vaizdas
-   Panaudos prekės
-   Profesinė patirtis
-   Darbo projektuose patirtis
-   Įgūdžiai
-   Atsakingos pareigos
-   Personalo veiksmai
-   Kursų registracija

Pasamdžius, perkėlus ar atleidus darbuotojus į darbo eigą gali būti įtrauktas peržiūros procesas. Tokiu būdu galima peržiūrėti dokumentą arba veiksmo sąlygas apibrėžti kaip darbo eigos dalį. Atlikus peržiūros procesą, parengiamas dokumentas arba užbaigiamas veiksmas, o darbo eiga perkeliama į paskutinį patvirtinimo veiksmą.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Darbo eigos susiejimas su pareigų hierarchija
Darbo eigą galite susieti su bet kuria jūsų sukonfigūruota hierarchija. Pavyzdžiui, jei pareigos susiejamos su ataskaitų hierarchijos matrica, galite sukonfigūruoti darbo eigą, nukreipiančią konkretaus projekto išlaidas projekto vadovui, o ne darbuotojo, susieto su tomis pareigomis, vadovui. Norėdami sukurti naują darbo eigą arba modifikuoti esamą, puslapyje **Personalo darbo eiga** spustelėkite **Naujas**. Sąraše pasirinkite darbo eigą, kad paleistumėte darbo eigos dizaino įrankį. Dizaino įrankį galite naudoti kurdami naują darbo eigą arba keisdami jau esančios darbo eigos veiksmus. Pakeitus esamą darbo eigą pakeitimai išsaugomi kaip nauja versija. Todėl, jei reikia, galite bet kada sugrįžti prie ankstesnės versijos.

## <a name="configure-a-human-resources-workflow"></a>Personalo darbo eigos konfigūravimas
Norėdami sukonfigūruoti pagrindinę darbo eigą, pradedamą darbuotojui pareikalavus pakeisti asmens identifikavimą, atlikite toliau nurodytus veiksmus.

1.  Puslapyje **Personalo darbo eigos** spustelėkite **Naujas**.
2.  Galimų darbo eigų sąraše pasirinkite **Identifikavimo numeriai**.
3.  Spustelėkite **Vykdyti**, kad paleistumėte darbo eigos dizaino įrankį, tada, kai būsite paraginti, įveskite vartotojo vardą ir slaptažodį.
4.  Elementą **Patvirtinti identifikavimo numerį** iš darbo eigos elementų sąrašo nuvilkite į dizaino įrankio lauką.
5.  Patvirtinimo elementą sujunkite su **Pradėti** ir **Baigti**.
6.  Dukart spustelėkite **Patvirtinti elementą**, tada spustelėkite dešinįjį pelės klavišą ir pasirinkite **Ypatybės**.
7.  Norėdami įtraukti darbo elemento instrukcijų, atlikite nurodytus veiksmus.
    1.  Pasirinkite **Priskyrimas**, tada iš priskyrimo tipo pasirinkite **Hierarchija**.
    2.  Pasirinkimo srityje **Hierarchija** pasirinkite **Konfigūruojama hierarchija**.
    3.  Įtraukite sustabdymo sąlygą ir uždarykite puslapį.

8.  Atlikite papildomas instrukcijas (neturi būti jokių papildomų įspėjimų).
9.  Spustelėkite **Įrašyti ir uždaryti**. Atsidarius dialogo langui aktyvinkite naują darbo eigą ir pasirinkite **Padaryti aktyvų**.
10. Pasirinkite **Personalas** &gt; **Pareigos** &gt; **Pareigų hierarchijos tipai**.
11. Pasirinkite **Matrica**.
12. Įtraukite darbo eigą **Darbininko identifikavimo numeris** į sąrašą.





