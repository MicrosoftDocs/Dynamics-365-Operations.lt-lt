---
title: Įrenginio būsenos scenarijus
description: Šiame straipsnyje aprašomas įrenginio būsenos scenarijus, kuris leidžia naudoti jutiklio duomenis, kad būtų galima stebėti įrangos prieinamumą.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 1f2b424dccf1963a7917059d412b5df7937496ee
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428997"
---
# <a name="the-machine-status-scenario"></a>Įrenginio būsenos scenarijus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Įrenginio *būsenos* scenarijus leidžia naudoti jutiklių duomenis, kad būtų galima stebėti įrangos prieinamumą. Jei nustatote jutiklio, kuris siunčia signalą, kai įrenginių išeigos gamybos užduotis sukuria išeigą, bet nesiunčiamas jokio jutiklio signalo nurodytame intervale, prižiūrėtojo skelbimų juostoje rodomas pranešimas.

## <a name="scenario-dependencies"></a>Scenarijaus priklausomybės

Kompiuterio *būsenos* scenarijus turi šias priklausomybes:

- Pranešimas gali būti suaktyvintas tik jei gamybos užduotis vykdoma susieta mašina.
- Signalas, kuris reiškia iš *dalies siunčiamą* signalą, turi būti nusiųstas į "IoT" centrą.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Paruošti demonstracinius duomenis įrenginio būsenos scenarijui

Jei norite *naudoti* demonstracinę sistemą įrenginio būsenos scenarijui patikrinti, naudokite sistemą, [kurioje](../../fin-ops-core/fin-ops/get-started/demo-data.md) įdiegti demonstraciniai duomenys, *pasirinkite USMF* juridinį subjektą (įmonę) ir paruoškite papildomus demonstracinius duomenis, kaip aprašyta šiame skyriuje. Jei naudojate savo jutiklius ir duomenis, galite praleisti šį skyrių.

### <a name="set-up-a-sensor-simulator"></a>Jutiklio simuliatoriaus nustatymas

Jei norite išbandyti šį scenarijų nenaudodami fizinio jutiklio, galite nustatyti simuliatorių, kad sugeneruotumėte reikiamus signalus. Norėdami gauti daugiau informacijos, žr [. Sumodeliuotos bandymo jutiklio nustatyti](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Patikrinti, ar ištekliai 3118 yra naudojami produktui P0111

Gamybos užsakymas bus suplanuotas ir paleistas. Dėl to *gamybos užduotis išleidžiama į 3118* išteklius (pjaustymo *mašina*). Atlikite šiuos veiksmus norėdami patikrinti, ar *jūsų demonstracinių duomenų produkte P0111* naudojamas išteklius *3118*.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Raskite ir pasirinkite produktą, kur **nustatytas** prekės numerio laukas *P0111*.
1. Veiksmų srities skirtuko Inžinierius grupėje Rodinys pasirinkite **Maršrutas**.**·** **·**
1. Puslapio **apačioje**, maršruto **puslapyje**, skirtuke Peržiūra, pasirinkite eilutę, kurioje yra **Oper. Nr.** Lauke <a0/& *nustatyta 30*.
1. Skirtuko Išteklių **reikalavimai puslapio** apačioje įsitikinkite, *kad ištekliai 3118* (*pjaustymo* mašinos) yra susieti su operacija.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Produkto P0111 gamybos užsakymo kūrimas ir išleidimas

Norėdami sukurti ir paleisti produkto P0111 gamybos užsakymą, *atlikite šiuos veiksmus*.

1. Eikite į **Gamybos valdymas \> Gamybos užsakymai \> Visi gamybos užsakymai**.
1. **Veiksmų srities puslapyje Visi** gamybos užsakymai pasirinkite Naujas paketinis **užsakymas**.
1. Dialogo lange **Kurti** paketą nustatykite šias vertes:

    - **Prekės numeris:** *P0111*
    - **Kiekis:** *10*

1. Jei **norite sukurti** užsakymą ir grįžti į puslapį Visi gamybos **užsakymai pasirinkite** Kurti.
1. Naudokite lauką **Filtras**, norėdami ieškoti gamybos užsakymų, kurių **prekės** numerio laukas nustatytas į *P0111*. Tada raskite ir pasirinkite ką tik sukurtą gamybos užsakymą.
1. Veiksmų juostoje, **Gamybos užsakymas** skirtuke, **Procesas** grupėje pasirinkite **Apskaičiuoti**.
1. Dialogo lange **Įvertinimas** pasirinkite Gerai **, kad** būtų vykdomas vertinimas.
1. Veiksmų srities, skirtuke Gamybos užsakymas **, procesų grupėje** **, pasirinkite** Paleidimas **.**
1. Paleidimo **dialogo** lange įrašykite ką tik sukurto paketinio užsakymo numerio pastabą.
1. Pasirinkite **Gerai**, jei norite išleisti užsakymą.

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Gamybos cecho vykdymo sąsajos konfigūravimas

Naudodami gamybos laiko vykdymo sąsają pradėsite *užduotį, kuri buvo suplanuota ir paleista ankstesniame skyriuje naudojant prekės numerį P0111*. Norėdami konfigūruoti gamybos laiko vykdymo sąsają, atlikite šiuos veiksmus.

1. Eikite į **Gamybos kontrolė \> Gamybos vykdymas \> Gamybos cecho vykdymas**.
1. Jei anksčiau nenustatėte sąsajos, pasirodys prisijungimo puslapis. Įveskite savo kredencialus.
1. Pasisveikimo puslapyje pasirinkite Konfigūruoti **, kad atidarytumėte** įrenginio **konfigūravimo vedlį**.
1. Konfigūravimo **įrenginyje – 1 veiksmas – pasirinkite konfigūracijos** puslapį, pasirinkite numatytąją *konfigūraciją*.
1. Pasirinkite **Toliau**.
1. Įrenginyje konfigūruoti **– 2 veiksmas – nustatykite gamybos laiko srities puslapį**, išteklių **lauką** nustatykite kaip *3118*.
1. Pasirinkite **Gerai**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a> Įjungti ieškos parinktį gamybos laiko vykdymo sąsajoje

Kad būtų lengviau rasti anksčiau pateikto gamybos užsakymo gamybos užduotį, atlikite šiuos veiksmus, kad gamybos laiko vykdymo sąsajoje įgalintumėte ieškos pasirinktį.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**.
1. Pasirinkite numatytąją *konfigūraciją*.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Bendrajame **"** FastTab" nustatykite pasirinktį **Įgalinti iešką** kaip *Taip*.
1. Uždarykite puslapį.

### <a name="start-the-first-job-in-the-batch-order"></a>Pradėti pirmą paketinio užsakymo užduotį

Norėdami pradėti suplanuotą užduotį 3118 ištekliuje *, atlikite šiuos veiksmus*.

1. Eikite į **Gamybos kontrolė \> Gamybos vykdymas \> Gamybos cecho vykdymas**.
1. Lauke " **Badge ID** " įveskite *123*. Tada pasirinkite **prisijungti**.
1. Jei būsite paraginti pateikti neatvykimo priežastį, pasirinkite vieną iš neatvykimo kortelių ir pasirinkite **Gerai**.
1. Lauke Ieška **įveskite** paketinio užsakymo numerį, apie kurį anksčiau padarėte pastabą. Tada pasirinkite grąžinimo **raktą**.
1. Pasirinkite užsakymą, o tada pasirinkite Pradėti **užduotį**.
1. Dialogo lange **Pradėti** užduotį pasirinkite **Pradėti**.

## <a name="set-up-the-machine-status-scenario"></a>Įrenginio būsenos scenarijaus nustatymas

Norėdami nustatyti įrenginio būsenos scenarijų tiekimo *grandinės valdymo* dalyje, atlikite šiuos veiksmus.

1. Eikite į **gamybos kontrolės \> nustatymo " \> Jutiklio duomenų" \> scenarijus**.
1. Kompiuterio būsenos **scenarijaus lauke** pasirinkite Konfigūruoti, kad **būtų** atidarytas šio scenarijaus sąrankos vedlys.
1. Puslapyje Jutikliai **pasirinkite** Naujas, kad **į** tinklelį būtų galima įtraukti jutiklio. Tada nustatykite šiuos jo laukus:

    - **Jutiklio ID – įveskite jutiklio ID**, kurį naudojate. (Jei naudojate Rasp azure PI Azure IoT Online Simuliatorių ir nustatėte jį taip, kaip aprašyta [Nustatykite imituojamas bandymo jutiklis](sdi-set-up-simulated-sensor.md), įveskite *MachineStatus*.)
    - **Jutiklio** aprašas – įveskite jutiklio aprašymą.

1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu jutikliu, kurį norite pridėti dabar. Galite grįžti ir pridėti daugiau jutiklių bet kuriuo metu.
1. Pasirinkite **Toliau**.
1. Veiklos įrašų **susiejimo** puslapio dalyje **Jutikliai** pasirinkite įrašą vienam iš ką tik pridėtų jutiklių.
1. Verslo įrašų **susiejimo skyriuje pasirinkite** Naujas **, kad** į tinklelį įtraukumėte eilutę.
1. Naujoje eilutėje nustatykite verslo **įrašo lauką** kaip išteklių, kuriuos naudojate pasirinktą jutiklio monitorių. (Jei naudojate demonstracinius duomenis, kuriuos anksčiau sukūrėte šiame straipsnyje, *nustatykite lauką kaip 3118, Pjaustymo mašina*.)
1. Pasirinkite **Toliau**.
1. Kompiuterio būsenos **ribinės vertės** puslapyje nurodykite, kaip ilgai po *paskutinio* siunčiamo signalo sistema turi išsiųsti įrenginio būsenos pranešimą. Yra du būdai ribinei vertei nustatyti:

    - **Numatytoji ribinė vertė (minutėmis)** – nustatykite šį lauką, kad jis apibrėžtų numatytąją ribinę vertę. Tada vertė bus taikoma visiems ištekliams **, kurių ribinė reikšmė, norint nustatyti, kad įrenginys neatsakys (minutėmis),** yra nustatytas į dvi minutes ar mažiau. Mažiausia vertė yra *2* (minutės).
    - **Ribinė vertė, nustatyti, ar įrenginys neatsako (minutėmis)** – įveskite kiekvieno tinklelyje esančio ištekliaus, kurio nenorite naudoti numatytosios ribinės vertės, šiame lauke įveskite perrašymo vertę. Ištekliams, kurie nustatyti taip, kad būtų naudojama dviejų minučių arba mažesnė ribinė reikšmė **, bus naudojamas numatytosios ribinės vertės (minučių)** parametras.

    > [!NOTE]
    > Paprastai, norėdami stebėti įrenginio būseną *,* naudojate ne dalies signalą. Todėl turėtumėte patikrinti, ar kiekvieno įrenginio išteklių ribinė vertė yra didesnė už mašinos kiekvienai daliai pagaminti.

1. Pasirinkite **Toliau**.
1. Skirtuko Aktyvuoti **jutiklius** puslapyje tinklelyje pasirinkite jutiklio funkciją, kurią pridėjote, tada pasirinkite **Aktyvinti**. Kiekvienam aktyviam jutikliui tinklelyje rodoma varnelė aktyviame **stulpelyje**.
1. Pasirinkite **Baigti**.

## <a name="work-with-the-machine-status-scenario"></a>Darbas su įrenginio būsenos scenarijumi

Kai įdiegsite jutiklius ir sukonfigūravote scenarijų, galėsite peržiūrėti mašinų būsenos įvykius tiekimo grandinės valdymo srityje. Šiame skyriuje aprašoma, kur ir kaip peržiūrėti šią informaciją.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Peržiūrėti įrenginio būsenos duomenis išteklių būsenos puslapyje

Išteklių būsenos **puslapyje** prižiūrėtojai *gali* stebėti iš dalies gaunamo signalo, gaunamo iš jutiklių, kurie susieti su kiekvienu įrenginio šaltiniu, laiko juostą. Norėdami sukonfigūruoti laiko juostą, atlikite šiuos veiksmus.

1. Eikite į **gamybos valdymo \> gamybos vykdymo \> išteklių būseną**.
1. Dialogo lange **Konfigūruoti** nustatykite šiuos laukus:

    - **Ištekliai** – pasirinkite išteklius, kuriuos norite stebėti. (Jei dirbate su demonstraciniai duomenimis, pasirinkite *3118*.)
    - **1** laiko serija – pasirinkite įrašą (metrinį raktą), kurio pavadinimo formatas yra toks: *MachineReportingStatus:&lt; Jutiklis&gt;*
    - **Rodomas pavadinimas** – įveskite signalo *dalis*.

Šioje iliustracijoje pateikiamas kompiuterio būsenos duomenų pavyzdys išteklių **būsenos puslapyje standartinės** operacijos metu.

![Įrenginio būsenos duomenys išteklių būsenos puslapyje, atliekant standartinę operaciją.](media/sdi-resource-status-downtime-up.png "Įrenginio būsenos duomenys išteklių būsenos puslapyje atliekant standartinę operaciją")

Toliau esanti iliustracija rodo įrenginio būsenos duomenų pavyzdį, kai aptinkami downtime.

![Aptikus downtime įrenginio būsenos duomenys išteklių būsenos puslapyje.](media/sdi-resource-status-downtime-down.png "Aptikus downtime įrenginio būsenos duomenys išteklių būsenos puslapyje")

### <a name="view-machine-status-on-the-notifications-page"></a>Peržiūrėti įrenginio būseną pranešimų puslapyje

Pranešimų puslapyje **prižiūrėtojai** gali peržiūrėti *pranešimus*, kurie sugeneruoti, kai praėjo per daug laiko nuo paskutinio jutiklio pristatymo iš dalies signalo. Kiekviename pranešime pateikiama gamybos užduoties, kurią paveikė neskryžas, peržiūra ir galima iš naujo priskirti paveiktą užduotį kitam ištekliui.

Norėdami atidaryti pranešimo **puslapį**, eikite į gamybos **kontrolės užklausas \> ir ataskaitas "\> Jutiklio duomenų tyrimų \>" pranešimai**.

Toliau esanti iliustracija rodo įrenginio būsenos pranešimo pavyzdį.

![Įrenginio būsenos pranešimo pavyzdys.](media/sdi-resource-status-downtime-notification.png "Įrenginio būsenos pranešimo pavyzdys")
