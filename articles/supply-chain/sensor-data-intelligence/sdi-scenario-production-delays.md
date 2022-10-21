---
title: Gamybos atidėjimų scenarijus
description: Šiame straipsnyje aprašomas gamybos delsos scenarijus, kuris generuoja pranešimą, jei gamybos našumas viršija konkrečią ribinę vertę.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690027"
---
# <a name="the-production-delays-scenario"></a>Gamybos atidėjimų scenarijus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Gamybos *delsos scenarijus* generuoja pranešimą, jei gamybos našumas viršija konkrečią ribinę vertę. Tokiu atveju, kiekvienai *pagamintai prekei* iš dalies Microsoft Azure siunčiamas signalas į "IoT" centrą. Užsakymo Dynamics 365 Supply Chain Management atidėjimas skaičiuojamas pagal suplanuotą gamybos užsakymo vykdymo laiką, gaminamų prekių skaičių, *užduoties* vykdymo laiką ir ne dalies signalų, kurie buvo gauti, skaičių. Delsos pranešimas generuojamas, jei užduoties *ne* dalies signalų skaičius yra mažesnis už ribinę vertę.

## <a name="scenario-dependencies"></a>Scenarijaus priklausomybės

Gamybos *delsos* scenarijus turi šių priklausomybių:

- Norint suaktyvinti įspėjimą, susietame įrenginyje turi būti paleistas gamybos užsakymas.
- Į "IoT Hub" turi būti siunčiamas *signalas*, kuris reiškia susieto įrenginio dalies signalą, ir turi būti įtrauktas unikalus ypatybės pavadinimas.
- „UNIX” laiko žymos ypatybė, kurioje vertė išreiškiama milisekundėmis (ms), turi būti „Azure IoT Hub” pranešime.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Paruošti demonstracinius duomenis produkto vėlavimo scenarijui

Jei norite *naudoti demonstracinę sistemą gamybos delsos scenarijui patikrinti, naudokite sistemą,*[kurioje įdiegti demonstraciniai duomenys,](../../fin-ops-core/fin-ops/get-started/demo-data.md) pasirinkite USMF *juridinį subjektą (įmonę) ir paruoškite papildomus demonstracinius* duomenis, kaip aprašyta šiame skyriuje. Jei naudojate savo jutiklius ir duomenis, galite praleisti šį skyrių.

### <a name="set-up-sensor-simulator"></a>Nustatyti jutiklio simuliatorių

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

## <a name="set-up-the-production-delays-scenario"></a>Nustatyti gamybos delsos scenarijų

Norėdami nustatyti gamybos delsos scenarijų *tiekimo grandinės valdymo* dalyje, atlikite šiuos veiksmus.

1. Eikite į **gamybos kontrolės \> nustatymo " \> Jutiklio duomenų" \> scenarijus**.
1. Gamybos delsos **scenarijaus** lauke pasirinkite Konfigūruoti, **kad** būtų atidarytas šio scenarijaus nustatymo vedlys.
1. Puslapyje Jutikliai **pasirinkite** Naujas, kad **į** tinklelį būtų galima įtraukti jutiklio. Tada nustatykite šiuos jo laukus:

    - **Jutiklio ID – įveskite jutiklio ID**, kurį naudojate. (Jei naudojate Rasp azure PI Azure IoT Online Simuliatorių ir nustatėte jį taip, kaip aprašyta [Nustatykite imituojamas bandymo jutiklis](sdi-set-up-simulated-sensor.md), įveskite *ProductionDelay*.)
    - **Jutiklio** aprašas – įveskite jutiklio aprašymą.

1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu jutikliu, kurį norite pridėti dabar. Galite grįžti ir pridėti daugiau jutiklių bet kuriuo metu.
1. Pasirinkite **Toliau**.
1. Veiklos įrašų **susiejimo** puslapio dalyje **Jutikliai** pasirinkite įrašą vienam iš ką tik pridėtų jutiklių.
1. Verslo įrašų **susiejimo skyriuje pasirinkite** Naujas **, kad** į tinklelį įtraukumėte eilutę.
1. Naujoje eilutėje nustatykite **verslo įrašą** kaip išteklių, kuriuos naudojate pasirinktą jutiklio monitorių. (Jei naudojate demonstracinius duomenis, kuriuos anksčiau sukūrėte šiame straipsnyje, *nustatykite jį į 3118, Pjaustymo mašina*.)
1. Pasirinkite **Toliau**.
1. Gamybos delsos **nuokrypio slenksčio** puslapyje, jei naudojate demonstracinius duomenis, kuriuos sukūrėte anksčiau šiame straipsnyje, atlikite šiuos veiksmus:

    1. Pasirinkite prekės **ryšio stulpelio** antraštę, norėdami atidaryti išplečiamąjį dialogo langą, kuriame yra stulpelio ieškos filtrai. Ieškos *lauke įveskite P0111*, tada pasirinkite **Taikyti**.
    2. Pasirinkite eilutę, kurioje operacijos **laukas** nustatytas į Apkarpyti */Iškirpti*. Nustatykite **delsos pranešimo ribinę vertę (%)** lauke nustatykite ribinę vertę (kaip procentinę dalį), iki kurios turi būti siunčiamas pranešimas.

1. Pasirinkite **Toliau**.
1. Skirtuko Aktyvuoti **jutiklius** puslapyje tinklelyje pasirinkite jutiklio funkciją, kurią pridėjote, tada pasirinkite **Aktyvinti**. Kiekvienam aktyviam jutikliui tinklelyje rodoma varnelė aktyviame **stulpelyje**.
1. Pasirinkite **Baigti**.

## <a name="work-with-the-production-delays-scenario"></a>Darbas su gamybos delsos scenarijumi

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Peržiūrėti gamybos delsos duomenis išteklių būsenos puslapyje

Išteklių būsenos **puslapyje** prižiūrėtojai gali stebėti signalų, gautų iš jutiklių, kurie susieti su kiekvienu įrenginio šaltiniu, laiko juostą. Norėdami sukonfigūruoti laiko juostą, atlikite šiuos veiksmus.

1. Eikite į **gamybos valdymo \> gamybos vykdymo \> išteklių būseną**.
1. Dialogo lange **Konfigūruoti** nustatykite šiuos laukus:

    - **Ištekliai** – pasirinkite išteklius, kuriuos norite stebėti. (Jei dirbate su demonstraciniai duomenimis, pasirinkite *3118*.)
    - **1** laiko serija – pasirinkite įrašą (metrinę raktą), kurio formatas toks: *ProductionJobDelayed:ActualQuantity:&lt; JobId&gt;*
    - **Rodomas pavadinimas** – įveskite signalo *dalis*.
