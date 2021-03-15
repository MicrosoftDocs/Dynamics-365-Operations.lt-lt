---
title: Paėmimo eilutės grupavimas
description: Šioje temoje pateikiama paėmimo eilutės grupavimo apžvalga.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989723"
---
# <a name="pick-line-grouping"></a>Paėmimo eilutės grupavimas

[!include [banner](../includes/banner.md)]

Paėmimo eilutės grupavimas leidžia sujungti keletą darbo eilučių, turinčias ta pačią prekę ir vietą, į vieną paėmimą, kuris pateikiamas vartotojui mobiliajame įrenginyje. Todėl sandėlio darbuotojai gali gauti pačias naudingiausias instrukcijas, tačiau būtinas darbo eilučių atskyrimas (pavyzdžiui, skirtingiems konteineriams, užsakymams ir kita) sistemoje.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Paėmimo eilutės funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo erdvę tam, kad patikrintų funkcijos būseną, ir jei būtina, ją įjungtų. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Paėmimo eilutės grupavimas*

## <a name="set-up-pick-line-grouping"></a>Paėmimo eilutės grupavimo nustatymas

### <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Lauke **Meniu elemento pavadinimas** įveskite *Pardavimo grupės eilutės paėmimas*.
1. Lauke **Pavadinimas** įveskite *Pardavimo grupės eilutės paėmimas*. Šis pavadinimas bus rodomas mobiliojo įrenginio meniu.
1. Lauke **Režimas** pasirinkite *Darbas*.
1. Nustatykite pasirinkties **Naudoti esamą darbą** padėtį *Taip*.
1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - Lauke **Nukreipė** pasirinkite *Vartotojo nurodyta*.
    - Nustatykite parinkties **Generuoti numerio lentelę** vertę *Taip*.
    - Nustatykite parinkties **Grupinis paėmimas** vertę *Taip*.
    - Priimkite numatytąsias vertes likusioms parinktims.

1. Atlikite toliau pateikiamus veiksmus, kad sukonfigūruotumėte mobiliojo įrenginio meniu elemento tinkamas darbo klases.

    1. „FastTab” **Darbo klasės** pasirinkite **Nauja**.
    2. Lauke **Darbo klasės ID** galite pasirinkti arba *Pardavimas* arba *PrdU paėmimas*, atsižvelgiant į sandėlį, kurį naudosite. Šiame scenarijuje pasirinkite *PrdU Paėmimas*.

        Laukas **Darbo užsakymo tipas** yra automatiškai nustatomas į *Pardavimo užsakymai*.

### <a name="set-up-a-mobile-device-menu"></a>Mobiliojo įrenginio meniu nustatymas

Atlikite šiuos veiksmus norėdami įtraukti meniu elementą, kurį ką tik sukūrėte **Siunčiama** meniu.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Sąrašo srityje rodomi visi esami mobiliojo įrenginio meniu. Pasirinkite *Siunčiama* iš sąrašo.
1. Sąraše **Prieinami meniu ir meniu elementai** suraskite ir pasirinkite jūsų sukurtą *Pardavimo grupės eilutės paėmimas* meniu elementą.
1. Pasirinkite dešiniosios rodyklės mygtuką *Pardavimo grupės eilutės paėmimas* meniu elementui perkelti į **Meniu struktūra** sąrašą.
1. Naudokite rodyklės aukštyn ir žemyn mygtukus perkelti meniu prekei į norimą meniu struktūros padėtį.
1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-a-work-template"></a>Darbo šablono nustatymas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.
1. Tinklelyje **Peržiūra** raskite ir pasirinkite darbo šabloną, kuris turėtų būti naudojamas su šia funkcija. Šiame scenarijuje pasirinkite *51 paėmimo iki etapo* šabloną.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos redaktoriaus teksto laukelio skirtuke **Rūšiavimas** pasirinkite **Įtraukti**, o tada nustatykite šias naujos eilutės vertes:

    - Stulpelyje **Lentelė** pasirinkite *Laikino darbo operacijos*.
    - Stulpelyje **Išvestinė lentelė** pasirinkite *Laikino darbo operacijos*.
    - Stulpelyje **Laukas** pasirinkite *Prekės numeris*.
    - Stulpelyje **Ieškos kryptis** pasirinkite *Didėjimo tvarka*.

1. Pasirinkite **Gerai** dialogo lango uždarymui ir jūsų pasirinkimo įrašymui.
1. Jūs gaunate šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“ Pasirinkite **Taip** tam, kad tęstumėte.

> [!IMPORTANT]
> Norint, kad paėmimo eilutės grupavimo funkcija veiktų, darbo eilutės turi būti surūšiuotos pagal prekės ID. Jei eilutės, kuriose yra tos pačios prekės, nepateikiamos viena po kitos, jos nebus grupuojamos.

## <a name="example"></a>Pavyzdys

### <a name="create-picking-work"></a>Paėmimo darbo kūrimas

Kad galėtumėte nustatyti paėmimo eilutės grupavimą, turite sukurti tinkamą siuntimo darbą.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Lauke **Kliento kodas** pasirinkite *„US-004”*.
1. „FastTab“ **Bendra** lauke **Sandėlis** pasirinkite *51*.
1. Pasirinkite **Gerai**.
1. „FastTab” **Pardavimo užsakymo eilutės** įtraukite toliau pateikiamas šešias eilutes:

    - **1 eilutė.** Lauke **Prekės numeris** pasirinkite *M9200*. Lauke **Kiekis** įveskite *3*.
    - **2 eilutė.** Lauke **Prekės numeris** pasirinkite *M9201*. Lauke **Kiekis** įveskite *3*.
    - **3 eilutė.** Lauke **Prekės numeris** pasirinkite *M9202*. Lauke **Kiekis** įveskite *2*.
    - **4 eilutė.** Lauke **Prekės numeris** pasirinkite *M9200*. Lauke **Kiekis** įveskite *1*.
    - **5 eilutė.** Lauke **Prekės numeris** pasirinkite *M9200*. Lauke **Kiekis** įveskite *3*.
    - **6 eilutė.** Lauke **Prekės numeris** pasirinkite *M9202*. Lauke **Kiekis** įveskite *7*.

    Toliau pateikiama kiekvienos prekės bendro kiekio suvestinė.

    - **Prekė M9200:** *7* vienetai
    - **Prekė M9201:** *3* vienetai
    - **Prekė M9202:** *9* vienetai

1. Prieš perduodami užsakymus į sandėlį, turite įsitikinti, kad paėmimo vietose pakanka atsargų visoms prekėms visuose užsakymuose pateikti. Patikrinkite parametrą **Vietos nurodymas**, kad nustatytumėte paėmimo vietas, naudojamas pardavimo užsakymo paėmimui atlikti. Jei naudojate „Contoso” demonstracinių duomenų aplinką *„51”* sandėliui, patvirtinkite, kad yra galimų atsargų.

    Dabar turite rezervuoti atsargas kiekvienai eilutei.

1. „FastTab” **Pardavimo užsakymo eilutės** pasirinkite vieną iš eilučių, kurias reikia rezervuoti.
1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. Puslapio **Rezervavimas** veiksmų srityje pasirinkite **Rezervuoti partiją** rezervavimo taikymui. Tada uždarykite puslapį.
1. Pakartokite 8‑10 veiksmus eilutėms, kurias reikia rezervuoti.

    Dabar privalote išleisti pardavimo užsakymą į sandėlį.

1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Gausite pranešimą, kad siunta ir banga buvo sukurtos ir, kad banga buvo pateikta vykdyti pakete.

    Kai banga ir visos proceso pabaigos užduotys yra baigtos, sukuriamas darbo, kuriame yra šešios eilutės, ID. Eilutės rūšiuojamos pagal prekės numerį.

1. Eikite į **Sandėlio valdymas \> Darbas \> Visas darbas** sukurtam darbui peržiūrėti. Pasižymėkite **Darbo ID** reikšmę, nes ji bus reikalinga kitoje procedūroje.

### <a name="initiate-picking-from-the-mobile-device"></a>Paėmimo inicijavimas iš mobiliojo įrenginio

1. Prisijunkite prie mobilaus prietaiso kaip vartotojas nustatytas sandėliui *51*.
1. Mobiliajame įrenginyje pasirinkite meniu, kuriame yra naujas mobiliojo įrenginio meniu elementas. Šiame scenarijuje pasirinkite **Siunčiama**.
1. Pasirinkite meniu elementą **Pardavimo grupės eilutės paėmimas** paėmimo inicijavimui.
1. Įveskite **Darbo ID** vertę, kurią pasižymėjote ankstesnėje procedūroje.

    Turėtumėte matyti paėmimo veiksmą, kuriame sugrupuotos visos prekės *„M9200”* paėmimo eilutės, ir turėtumėte gauti instrukcijas, kaip paimti *7'* prekės *„M9200”* vienetus.

    > [!IMPORTANT]
    > Mobiliajame įrenginyje trijų paėmimo darbo eilučių paėmimo darbas buvo sujungtas į vieną paėmimo veiksmą vartotojui.

1. Patvirtinkite paėmimo veiksmą.
1. Perėję į darbo ID darbo puslapį pastebėsite, kad visos trys prekės *„M9200”* paėmimo eilutės buvo uždarytos vienu metu.
1. Grįžkite į mobilųjį įrenginį ir toliau atlikite paėmimą. Turi būti pristatyta 4‑a prekės *„M9201”* darbo eilutė. Kadangi užsakyme buvo tik viena darbo eilutė, nieko negalima sujungti.
1. Patvirtinkite paėmimo veiksmą.
1. Per paskutinį paėmimo veiksmą mobiliajame įrenginyje sujungiamos dvi paskutinės darbo užsakymo paėmimo eilutės.
1. Atlikite paėmimo veiksmą *9'* prekės *„M9202”* vienetams.
1. Patvirtinkite padėjimo veiksmą ir visas papildomas paėmimo / padėjimo poras, kad užbaigtumėte darbą.

> [!IMPORTANT]
>
> - Darbo eilutes galima grupuoti tik tuo atveju, jei jos pateikiamos iš eilės.
> - Toliau nurodytos funkcijos nepalaikomos.
>
>   - Esamo svorio prekės
>
>    Jei darbe yra esamo svorio prekių, prieš pradėdami paėmimą matote klaidos pranešimą.
>
>   - Vienetų paėmimas
>   - Darbo eilutės, kuriose nebaigtas papildymo darbas
>   - Viršytas paėmimo kiekis
>   - Nevisiškas paėmimas ir prekių perskirstymas


[!INCLUDE[footer-include](../../includes/footer-banner.md)]