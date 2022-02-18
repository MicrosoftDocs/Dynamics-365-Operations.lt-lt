---
title: Darbo eigų naudojimas darbuotojų informacijai valdyti
description: Šioje temoje paaiškinama, kaip galite naudoti darbo eigas darbuotojų informacijai tvarkyti.
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
ms.openlocfilehash: d80ed49a4f423179997ac35562284a4e28af803f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068090"
---
# <a name="use-workflows-to-manage-employee-information"></a>Darbo eigų naudojimas darbuotojų informacijai valdyti


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją. Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus.

Darbo eigos tinkamumas personalui suteikia galimybę pritaikyti daugybę darbo eigų personalo veiklai tvarkyti. Be to, yra daugybė parinkčių, kuriomis pasinaudoję galite modifikuoti konkrečias darbo eigas ir susieti jas su ataskaitų hierarchija. Galimos darbo eigos, padedančios valdyti kelių tipų darbuotojų informacijos pakeitimus. Darbo eigą galite susieti su pareigomis. Tada, jei darbuotojai pakeičia savo įrašus, pradedama darbo eiga, kurią reikia patvirtinti prieš išsaugant naują informaciją. Darbo eigos yra iš anksto nustatytos toliau nurodytų tipų informacijai, kad padėtų jums efektyviai valdyti pokyčius ir išlaikyti tikslius darbuotojų duomenis:

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
Darbo eigą galite susieti su bet kuria jūsų sukonfigūruota hierarchija. Pavyzdžiui, jei pareigos susiejamos su ataskaitų hierarchijos matrica, galite sukonfigūruoti darbo eigą, nukreipiančią konkretaus projekto išlaidas projekto vadovui, o ne darbuotojo, susieto su tomis pareigomis, vadovui. Norėdami sukurti naują darbo eigą arba modifikuoti esamą darbo eigą, **Žmogiškųjų išteklių darbo eiga** puslapį, pasirinkite **Nauja**. Sąraše pasirinkite darbo eigą, kad atidarytumėte darbo eigos dizainerį. Dizaino įrankį galite naudoti kurdami naują darbo eigą arba keisdami jau esančios darbo eigos veiksmus. Pakeitus esamą darbo eigą pakeitimai išsaugomi kaip nauja versija. Todėl, jei reikia, galite bet kada sugrįžti prie ankstesnės versijos.

## <a name="configure-a-human-resources-workflow"></a>Personalo darbo eigos konfigūravimas
Norėdami sukonfigūruoti pagrindinę darbo eigą, pradedamą darbuotojui pareikalavus pakeisti asmens identifikavimą, atlikite toliau nurodytus veiksmus.

1.  Ant **Žmogiškųjų išteklių darbo eigos** puslapį, pasirinkite **Nauja**.
2.  Galimų darbo eigų sąraše pasirinkite **Identifikavimo numeriai**.
3.  Pasirinkite **Bėk** kad atidarytumėte darbo eigos dizainerį, tada įveskite savo vartotojo vardą ir slaptažodį, kai būsite paraginti.
4.  Elementą **Patvirtinti identifikavimo numerį** iš darbo eigos elementų sąrašo nuvilkite į dizaino įrankio lauką.
5.  Patvirtinimo elementą sujunkite su **Pradėti** ir **Baigti**.
6.  Dukart bakstelėkite (arba dukart spustelėkite) **Patvirtinti elementą**, pasirinkite ir palaikykite (arba spustelėkite dešiniuoju pelės mygtuku), tada pasirinkite **Savybės**.
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
