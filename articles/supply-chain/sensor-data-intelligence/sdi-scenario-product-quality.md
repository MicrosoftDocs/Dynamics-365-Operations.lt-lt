---
title: Produkto kokybės scenarijus
description: Šiame straipsnyje pateikiama informacija apie produkto kokybės scenarijų. Šis scenarijus naudoja jutiklio seriją produktų paketo kokybei išmatuoti ir generuoja įspėjimą, jei matavimas nepatenka į nurodytą ribinę vertę.
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
ms.openlocfilehash: 8c4808ea3a0389c2a8699f0e11ea154705a6916d
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429003"
---
# <a name="the-product-quality-scenario"></a>Produkto kokybės scenarijus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Produkto kokybės scenarijuje* jutiklis nustatomas taip, kad būtų galima išmatuoti produkto paketo kokybę darbo laiko metu. Jei matavimas viršija nustatytą produkto ribinę vertę, vadovo skelbimų srityje rodomas pranešimas. Pvz., jutiklis matuoja maisto produktų, kurie pasirodo iš gamybos eilutės, pereitų persodą. Jei matavimas yra už leidžiamos minimalios ar maksimalios produkto vertės ribų, generuojamas pranešimas.

## <a name="scenario-dependencies"></a>Scenarijaus priklausomybės

Produkto *kokybės* scenarijus turi šias priklausomybes:

- Įspėjimas gali būti suaktyvintas tik tada, jei gamybos užsakymas vykdomas susietas kompiuteryje ir jei ta mašina gamina produktą, turiį susietą paketo atributą.
- Signalas, atitinkantis paketo atributą, turi būti išsiųstas į „IoT Hub“ ir turi būti įtrauktas unikalus ypatybės pavadinimas.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Paruošti demonstracinius duomenis produkto kokybės scenarijui

Jei norite *naudoti* demonstracinę sistemą produkto kokybės scenarijui patikrinti, naudokite sistemą, [kurioje](../../fin-ops-core/fin-ops/get-started/demo-data.md) įdiegti demonstraciniai duomenys, *pasirinkite USMF* juridinį subjektą (įmonę) ir paruoškite papildomus demonstracinius duomenis, kaip aprašyta šiame skyriuje. Jei naudojate savo jutiklius ir duomenis, galite praleisti šį skyrių.

Šiame skyriuje bus nustatyti demonstraciniai duomenys *, kad naudodami išleistą produktą P0111* (*Sudėtinis* atvejis) būtų galima naudoti su *produkto kokybės scenarijumi*. Šiame scenarijuje sistema seka, ar paketo atributo vertė, kurią matuoja jutiklis, viršija nustatytą paketo atributo, susieto su produktu, ribą.

### <a name="set-up-a-sensor-simulator"></a>Jutiklio simuliatoriaus nustatymas

Jei norite išbandyti šį scenarijų nenaudodami fizinio jutiklio, galite nustatyti simuliatorių, kad sugeneruotumėte reikiamus signalus. Norėdami gauti daugiau informacijos, žr [. Sumodeliuotos bandymo jutiklio nustatyti](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Susieti paketo atributą ir išteklių su produktu P0111

Norėdami susieti paketo atributą *su produktu P0111* (*sudėtinis* atvejis) *ir patikrinti, ar jai naudojamas išteklius 3118* (*tipo* pjaustymo mašina), atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Raskite ir pasirinkite produktą, kur **nustatytas** prekės numerio laukas *P0111*.
1. Veiksmų srities skirtuko Tvarkyti atsargas **grupėje** Paketo atributai **pasirinkite** Produktas **·**.
1. Konkretaus produkto **puslapyje pasirinkite** Naujas, kad **sukurtumėte** konkrečiam produktui brinktą paketo atributą.
1. Antraštėje nustatykite šiuos laukus:

    - **Atributo** kodas – pasirinkite atributų, kuriuos stebėsite, aprėptį (*Lentelė*, *Grupė* arba *Visi*). Šiame scenarijuje pasirinkite *Lentelė*, nes visada galėsite stebėti vieną atributą.
    - **Atributo** ryšys – pasirinkite atributą, kurį naudosite *produkto* kokybės scenarijus norėdami stebėti vertę. Pavyzdžiui, pasirinkite Parametrai, kurie *yra* atributai, įtraukti į standartinius demonstracinius duomenis.

1. Laukuose **Minimali** ir Maksimali vertė **apibrėžkite** **priimtinų** verčių, kurias atributas turi pateikti, kad kokybės patikrinimas būtų patikrintas, diapazoną. Jei jutiklis praneša už šio diapazono ribų, sistema identifikuos ją kaip kokybės pažeidimą. Kiti šio "FastTab" laukai nėra susiję su produkto *kokybės scenarijumi*. Numatytosios vertės, kurias šiuo metu matote, yra iš demonstracinių duomenų. Todėl palikite juos tušius **ir** **uždarykite** konkretaus produkto puslapį, kad grįžkite į P0111 prekės išleisto *produkto informacijos puslapį.*
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

### <a name="configure-the-production-floor-execution-interface"></a>Gamybos cecho vykdymo sąsajos konfigūravimas

Jei to dar nepadarėte, sukonfigūruokite gamybos laiko vykdymo sąsają, *kad ji rodytų užduotis, priskirtas ištekliui 3118* (tamsinimo *mašina*). Instrukcijų ieškokite toliau pateikiamuose skyriuose:

- [Gamybos vietos vykdymo sąsajos konfigūravimas](sdi-scenario-equipment-downtime.md#config-pfe)
- [Įjungti ieškos parinktį gamybos laiko vykdymo sąsajoje](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Pradėti pirmą paketinio užsakymo užduotį

Norėdami pradėti pirmą paketinio užsakymo užduotį, atlikite šiuos veiksmus.

1. Eikite į **Gamybos kontrolė \> Gamybos vykdymas \> Gamybos cecho vykdymas**.
1. Lauke " **Badge ID** " įveskite *123*. Tada pasirinkite **prisijungti**.
1. Jei būsite paraginti pateikti neatvykimo priežastį, pasirinkite vieną iš neatvykimo kortelių ir pasirinkite **Gerai**.
1. Lauke Ieška **įveskite** paketinio užsakymo numerį, apie kurį anksčiau padarėte pastabą. Tada pasirinkite grąžinimo **raktą**.
1. Pasirinkite užsakymą, o tada pasirinkite Pradėti **užduotį**.
1. Dialogo lange **Pradėti** užduotį pasirinkite **Pradėti**.

## <a name="set-up-the-product-quality-scenario"></a>Nustatyti produkto kokybės scenarijų

Norėdami nustatyti produkto kokybės scenarijų tiekimo grandinės *valdymo* dalyje, atlikite šiuos veiksmus.

1. Eikite į **gamybos kontrolės \> nustatymo " \> Jutiklio duomenų" \> scenarijus**.
1. Produkto kokybės **scenarijaus lauke** pasirinkite Konfigūruoti, kad **atidarytumėte** šio scenarijaus nustatymo vedlį.
1. Puslapyje Jutikliai **pasirinkite** Naujas, kad **į** tinklelį būtų galima įtraukti jutiklio. Tada nustatykite šiuos jo laukus:

    - **Jutiklio ID – įveskite jutiklio ID**, kurį naudojate. (Jei naudojate Rasp azure PI Azure IoT Online Simuliatorių ir nustatėte jį taip, kaip aprašyta [Nustatykite imituojamas bandymo jutiklis](sdi-set-up-simulated-sensor.md), įveskite *Kokybę*.)
    - **Jutiklio** aprašas – įveskite jutiklio aprašymą.

1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu jutikliu, kurį norite pridėti dabar. Galite grįžti ir pridėti daugiau jutiklių bet kuriuo metu.
1. Pasirinkite **Toliau**.
1. Veiklos įrašų **susiejimo** puslapio dalyje **Jutikliai** pasirinkite įrašą vienam iš ką tik pridėtų jutiklių.
1. Verslo įrašų **susiejimo skyriuje pasirinkite** Naujas **, kad** į tinklelį įtraukumėte eilutę.
1. Naujoje eilutėje laukas **Verslo įrašo tipas turi** būti automatiškai nustatytas kaip *Resources(WrkCtrTable)*. Nustatykite **verslo įrašo** lauką kaip išteklių, kuriuos naudojate pasirinktą jutiklio monitorių. (Jei naudojate demonstracinius duomenis, kuriuos anksčiau sukūrėte šiame straipsnyje, *nustatykite jį į 3118, Pjaustymo mašina*.)
1. Iškart po to, kai pasirenkate verslo įrašo tipą eilutei, kurią pridėjote prie ankstesnio veiksmo, antra eilutė automatiškai pridedama prie tinklelio. Šioje eilutėje laukas Verslo **įrašo tipas turi** būti nustatytas kaip *Paketo atributai(PdsBatchAttrib)*. Nustatyti verslo **įrašo lauką** kaip paketo atributą, kurį naudojate pasirinktą jutiklio monitorių. (Jei naudojate demonstracinius duomenis, kuriuos sukūrėte anksčiau šiame straipsnyje, nustatykite juos kaip *Komponento, ribinės vertės procentai*.)
1. Pasirinkite **Toliau**.
1. Skirtuko Aktyvuoti **jutiklius** puslapyje tinklelyje pasirinkite jutiklio funkciją, kurią pridėjote, tada pasirinkite **Aktyvinti**. Kiekvienam aktyviam jutikliui tinklelyje rodoma varnelė aktyviame **stulpelyje**.
1. Pasirinkite **Baigti**.

## <a name="work-with-the-product-quality-scenario"></a>Dirbti su produkto kokybės scenarijumi

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Peržiūrėti produkto kokybės duomenis išteklių būsenos puslapyje

Išteklių būsenos **puslapyje** prižiūrėtojai gali stebėti produkto kokybės signalo, gaunamo iš jutiklių, kurie susieti su kiekvienu įrenginio ištekliumi, laiko juostą. Norėdami sukonfigūruoti laiko juostą, atlikite šiuos veiksmus.

1. Eikite į **gamybos valdymo \> gamybos vykdymo \> išteklių būseną**.
1. Dialogo lange **Konfigūruoti** nustatykite šiuos laukus:

    - **Ištekliai** – pasirinkite išteklius, kuriuos norite stebėti. (Jei dirbate su demonstraciniai duomenimis, pasirinkite *3118*.)
    - **1** laiko serija – pasirinkite įrašą (metrikos raktą), kurio formatas toks: *ProductQuality:&lt; JobId&gt;:&lt; AttributeName&gt;*
    - **Rodomas pavadinimas** – įveskite paketo *atributo vertes*.

Šioje iliustracijoje pateikiamas produkto kokybės duomenų pavyzdys išteklių **būsenos** puslapyje, kai vertė yra priimtinų verčių diapazone.

![Produkto kokybės duomenys išteklių būsenos puslapyje, kai vertė yra diapazone.](media/sdi-product-quality-in-range.png "Produkto kokybės duomenys išteklių būsenos puslapyje, kai vertė yra diapazone")

Ši iliustracija rodo produkto kokybės duomenų pavyzdį, kai aptinkama diapazono vertė, kuri išeina už diapazono ribų.

![Produkto kokybės duomenys išteklių būsenos puslapyje, kai aptikta diapazono vertė, kuri išeina už diapazono ribų.](media/sdi-product-quality-out-of-range.png "Produkto kokybės duomenys išteklių būsenos puslapyje, kai aptikta diapazono reikšmė, kuri yra už diapazono ribų")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Peržiūrėti produkto kokybės duomenis pranešimų puslapyje

Pranešimų puslapyje **prižiūrėtojai** gali peržiūrėti pranešimą, sugeneruotą, kai jutiklis reiškia paketo atributo vertę, kuri viršija nustatytą paketo atributo ribinę vertę. Kiekviename pranešime pateikiama gamybos užduoties, kurią paveikė neskryžas, peržiūra ir galima iš naujo priskirti paveiktą užduotį kitam ištekliui.

Norėdami atidaryti pranešimo **puslapį**, eikite į gamybos **kontrolės užklausas \> ir ataskaitas "\> Jutiklio duomenų tyrimų \>" pranešimai**.

Šioje iliustracijoje pateikiamas produkto kokybės pranešimo pavyzdys.

![Produkto kokybės pranešimo pavyzdys.](media/sdi-product-quality-notification.png "Produkto kokybės pranešimo pavyzdys")
