---
title: Darbo eigų naudojimas darbuotojų informacijai valdyti
description: Šiame straipsnyje paaiškinama, kaip galite naudoti darbo eigas darbuotojų informacijai valdyti.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750740"
---
# <a name="use-workflows-to-manage-employee-information"></a>Darbo eigų naudojimas darbuotojų informacijai valdyti

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje paaiškinama, kaip panaudoti darbo eigos tinkamumą personalui, tvarkant darbuotojo informaciją. Pavyzdžiui, darbo eigą galite susieti su pareigomis ir sukonfigūruoti patvirtinimo darbo eigą, kuri pradedama, kai darbuotojai pakeičią savo įrašus.

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

Galite susieti darbo eigą su bet kuria jūsų konfigūruota pareigų hierarchija. Du hierarchijos tipai naudojami darbo eigos nukreipimui: valdymo **ir konfigūruojama** **·**.

- Valdymo **hierarchija** nurodo įmonės arba organizacijos ataskaitų struktūrą. Daugiau informacijos apie šį hierarchijos tipą ieškokite Ataskaitos [pagal pareigas](hr-personnel-positions.md#reports-to-position).
- Konfigūruojama **hierarchija** rodo matricą arba pasirinktinę hierarchiją. Daugiau informacijos apie šį hierarchijos tipą ieškokite [Ryšiai](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Valdymo hierarchijos pavyzdys

Galite konfigūruoti darbo eigą taip, kad kai darbuotojas pateikia pirkimo užklausą naujam kompiuteriui, užklausa būtų nukreipta į darbuotojo vadybininką ir praleidimo lygio vadybininką. Konfigūruokite darbo eigos veiksmą, priskyrimo **tipo lauką** nustatykite kaip **Hierarchija**. Tada **hierarchijos** tipo skirtukas tampa pasiekiamas. Pavyzdžiui, pasirinkite valdymo **hierarchiją**.

### <a name="configurable-hierarchy-example"></a>Konfigūruojamas hierarchijos pavyzdys

Jei pareigos susijusios su matricos ataskaitų hierarchija, galite konfigūruoti darbo eigą, kuri maršrutų išlaidas konkrečiam projektui į galimą projektą, o ne darbuotojo vadybininką. Tokiu atveju nustatykite lauką **Priskyrimo tipas** kaip **Hierarchija**. Tada skirtuke Hierarchijos **tipas** pasirinkite konfigūruojamą **hierarchiją**. Nustatę darbo eigą, darbo **·** **eigos** nustatymo puslapyje pasirinkite hierarchiją Susieti hierarchiją, kad pasirinktumėte hierarchiją, kuri turėtų būti naudojama darbo eigos nukreipimui.

> [!IMPORTANT]
> Kai dokumentas, operacija ar pagrindinis įrašas pateikiamas darbo eigos patvirtinimui, pagrindinės pateikimo vietos bus naudojamos nustatyti, kam dokumentas turėtų būti siunčiamas į kitą.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hierarchijos parametras darbo eigos parametruose

1. Darbo eigos **parametrų puslapyje** eikite į hierarchijos **nukreipimą**.
2. Pagal numatytuosius nustatymus parinktis **Naudoti** pareigų hierarchiją nustatyta kaip **Ne**. Šiuo atveju, darbo eiga išeis iš hierarchijos, naudos pirmines darbuotojo pareigas. Nustatykite pasirinktį **Taip,** jei norite, kad darbo eiga, naršant hierarchiją, naudoja pareigų pirminį elementą.

### <a name="additional-example"></a>Papildomas pavyzdys 

Darbuotojo Grace Sturman turi dvi pareigas: konsultanto ir konsultanto. Pagrindinės atidėjimų pareigos yra atstoja. Kai ji neįgija naujų darbuotojų, ji gali naudotis konsultavimo darbu. Per savo pirmines pareigas, Grace praneša Yrae, personalo direktorius. Turimos ataskaitos į Arbateisą. Atsižvelgiant į projektą, konsultanto pareigose Grace turi keletą punktyrinių eilučių ryšių.

Atidėjimo įmonė sukuria darbo eigos maršruto taisykles, pagrįstas konfigūruojama **hierarchija** (matricomis / projektų hierarchijomis). Ši hierarchija naudoja Grace konsultanto pareigas. Jei **parinktis** **Naudoti pareigų hierarchiją nustatyta kaip Ne**, kai dokumentas yra nukreipiamas į Grace jos patvirtinimui, darbo eiga peržvelgs savo pirmines pareigas (prižiūrės), kad nustatytų, kur dokumentas turi būti nukreipiamas pirmyn. Tokiu atveju jis bus nukreiptas pirmiausia į Turižą, o tada į Jav. Jei pasirinktis nustatyta **kaip** Taip, **o** darbo eiga naudoja konfigūruojamą hierarchiją, darbo eiga peržiūrės Grace konsultanto pareigas ir ataskaitų ryšį, kad nustatytų, kur turi būti nukreipiamas dokumentas kitas.

### <a name="configure-a-human-resources-workflow"></a>Personalo darbo eigos konfigūravimas
Norėdami sukonfigūruoti pagrindinę darbo eigą, pradedamą darbuotojui pareikalavus pakeisti asmens identifikavimą, atlikite toliau nurodytus veiksmus.

1.  Personalo darbo **eigos puslapyje** pasirinkite **Naujas**.
2.  Galimų darbo eigų sąraše pasirinkite **Identifikavimo numeriai**.
3.  Norėdami **atidaryti** darbo eigos konstruktorių pasirinkite Vykdyti, tada įveskite savo vartotojo vardą ir slaptažodį.
4.  Perkelti elementą **Patvirtinti identifikavimo numerį** iš darbo eigos elementų sąrašo į dizainerio sritį.
5.  Patvirtinimo elementą sujunkite su **Pradėti** ir **Baigti**.
6.  Dukart pažymėkite (arba du kartus spustelėkite) Tvirtinti **elementą**, pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku), tada pasirinkite **Ypatybės**.
7.  Norėdami įtraukti darbo elemento instrukcijų, atlikite nurodytus veiksmus.

    1.  Pasirinkite **Priskyrimas**, tada iš priskyrimo tipo pasirinkite **Hierarchija**.
    2.  Pasirinkimo srityje **Hierarchija** pasirinkite **Konfigūruojama hierarchija**.
    3.  Įtraukite sustabdymo sąlygą ir uždarykite puslapį.

8.  Užpildykite visas papildomas instrukcijas.
9.  Pasirinkite **Įrašyti ir uždaryti**. Atsidarius dialogo langui aktyvinkite naują darbo eigą ir pasirinkite **Padaryti aktyvų**.
10. Pasirinkite **Personalas** &gt; **Pareigos** &gt; **Pareigų hierarchijos tipai**.
11. Pasirinkite **Matrica**.
12. Įtraukite darbo eigą **Darbininko identifikavimo numeris** į sąrašą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Peržiūrėti ir valdyti adresų pakeitimus](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
