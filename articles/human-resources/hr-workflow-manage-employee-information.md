---
title: Darbo eigų naudojimas darbuotojų informacijai valdyti
description: Šioje temoje paaiškinama, kaip galite naudoti darbo eigas darbuotojų informacijai valdyti.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18863ad12cc3b5ee328184da5ffb35e7f5958b52
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771489"
---
# <a name="use-workflows-to-manage-employee-information"></a>Darbo eigų naudojimas darbuotojų informacijai valdyti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją. Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus.

Darbo eigos tinkamumas personalui suteikia galimybę pritaikyti daugybę darbo eigų personalo veiklai tvarkyti. Be to, yra daugybė parinkčių, kuriomis pasinaudoję galite modifikuoti konkrečias darbo eigas ir susieti jas su ataskaitų hierarchija. Darbo eigos yra galimos padėti valdyti kelių tipų darbuotojų informacijos pakeitimus. Darbo eigą galite susieti su pareigomis. Tada, jei darbuotojai pakeičia savo įrašus, pradedama darbo eiga, kurią reikia patvirtinti prieš išsaugant naują informaciją. Šių tipų informacijos darbo eigos yra iš anksto nustatytos, kad padėtų efektyviai valdyti pakeitimus ir išlaikyti tikslų darbuotojų duomenis:

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

Pasamdžius, perkėlus ar atleidus darbuotojus į darbo eigą gali būti įtrauktas peržiūros procesas. Tokiu būdu dokumentas gali būti peržiūrėtas arba veiksmo sąlygos gali būti apibrėžtos kaip darbo eigos dalis. Atlikus peržiūros procesą, parengiamas dokumentas arba užbaigiamas veiksmas, o darbo eiga perkeliama į paskutinį patvirtinimo veiksmą.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Darbo eigos susiejimas su pareigų hierarchija
Darbo eigą galite susieti su bet kuria jūsų sukonfigūruota hierarchija. Pavyzdžiui, jei pareigos susiejamos su ataskaitų hierarchijos matrica, galite sukonfigūruoti darbo eigą, nukreipiančią konkretaus projekto išlaidas projekto vadovui, o ne darbuotojo, susieto su tomis pareigomis, vadovui. Norėdami sukurti naują darbo eigą arba modifikuoti esamą darbo eigą, personalo **darbo eigos puslapyje pasirinkite** **Nauja**. Sąraše pasirinkite darbo eigą, kad atidarytumėte darbo eigos konstruktorių. Dizaino įrankį galite naudoti kurdami naują darbo eigą arba keisdami jau esančios darbo eigos veiksmus. Pakeitus esamą darbo eigą pakeitimai išsaugomi kaip nauja versija. Todėl, jei reikia, galite bet kada sugrįžti prie ankstesnės versijos.

## <a name="configure-a-human-resources-workflow"></a>Personalo darbo eigos konfigūravimas
Norėdami sukonfigūruoti pagrindinę darbo eigą, pradedamą darbuotojui pareikalavus pakeisti asmens identifikavimą, atlikite toliau nurodytus veiksmus.

1.  Personalo **darbo eigos puslapyje** pasirinkite **Naujas**.
2.  Galimų darbo eigų sąraše pasirinkite **Identifikavimo numeriai**.
3.  Norėdami **atidaryti darbo eigos** konstruktorių pasirinkite Vykdyti, tada, kai būsite paraginti, įveskite vartotojo vardą ir slaptažodį.
4.  Elementą **Patvirtinti identifikavimo numerį** iš darbo eigos elementų sąrašo nuvilkite į dizaino įrankio lauką.
5.  Patvirtinimo elementą sujunkite su **Pradėti** ir **Baigti**.
6.  Dukart pažymėkite (arba du kartus spustelėkite) **Patvirtinkite elementą, pasirinkite** ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku), tada pasirinkite **·** Ypatybės.
7.  Norėdami įtraukti darbo elemento instrukcijų, atlikite nurodytus veiksmus.

    1.  Pasirinkite **Priskyrimas**, tada iš priskyrimo tipo pasirinkite **Hierarchija**.
    2.  Pasirinkimo srityje **Hierarchija** pasirinkite **Konfigūruojama hierarchija**.
    3.  Įtraukite sustabdymo sąlygą ir uždarykite puslapį.

8.  Atlikite papildomas instrukcijas (neturi būti jokių papildomų įspėjimų).
9.  Pasirinkite **Įrašyti ir uždaryti**. Atsidarius dialogo langui aktyvinkite naują darbo eigą ir pasirinkite **Padaryti aktyvų**.
10. Pasirinkite **Personalas** &gt; **Pareigos** &gt; **Pareigų hierarchijos tipai**.
11. Pasirinkite **Matrica**.
12. Įtraukite darbo eigą **Darbininko identifikavimo numeris** į sąrašą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Peržiūrėti ir valdyti adresų pakeitimus](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
