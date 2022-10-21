---
title: Turto prastovos priežiūros scenarijus
description: Šiame straipsnyje aprašomas turto priežiūros scenarijus, kuris leidžia naudoti jutiklio duomenis skaitiklio įrašams, kurie seka įrenginio turto naudojimą, kurti.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2d103406118be4385177b678de424df12af69c2e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689406"
---
# <a name="the-asset-maintenance-scenario"></a>Turto prastovos priežiūros scenarijus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Turto *priežiūros scenarijus* leidžia naudoti jutiklių duomenis skaitiklio įrašams kurti. Skaitiklio įrašai seka įrenginio turto naudojimą ir naudojami kaip įvestis įrenginių turto priežiūros grafikui generuoti.

## <a name="video-instructions"></a>Vaizdo įrašų instrukcijos

Toliau pateiktame vaizdo įraše parodyta, kaip nustatyti ir išbandyti turto priežiūros scenarijų naudojant standartinius demonstracinius [duomenis](../../fin-ops-core/fin-ops/get-started/demo-data.md). Likusiuose šio straipsnio skyriuose tos pačios instrukcijos pateikiamos tekstiniu formatu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Parengti demonstracinius duomenis turto priežiūros scenarijui

Jei norite *naudoti* demonstracinę sistemą turto priežiūros scenarijui patikrinti, naudokite sistemą, [kurioje](../../fin-ops-core/fin-ops/get-started/demo-data.md) įdiegti demonstraciniai duomenys, *pasirinkite USMF* juridinį subjektą (įmonę) ir paruoškite papildomus demonstracinius duomenis, kaip aprašyta šiame skyriuje. Jei naudojate savo jutiklius ir duomenis, galite praleisti šį skyrių.

Šiame skyriuje kaip pavyzdį bus nustatytas *AK-101, oro transporto turto* demonstraciniai duomenys. Tada pamatysite, kaip būsimų techninės priežiūros darbų galima nuspėti remiantis jutiklio signalais, kurie matuoja valandų, kurias buvo vykdomas oras, skaičių. Taip pat nustatote priežiūros planą, kuriame oro valandos turi būti tvarkomos kas 10 000 valandų.

### <a name="set-up-a-sensor-simulator"></a>Jutiklio simuliatoriaus nustatymas

Jei norite išbandyti šį scenarijų nenaudodami fizinio jutiklio, galite nustatyti simuliatorių, kad sugeneruotumėte reikiamus signalus. Norėdami gauti daugiau informacijos, žr [. Sumodeliuotos bandymo jutiklio nustatyti](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Kurti turto skaitiklį gamybos valandoms sekti

Norėdami sukurti turto skaitiklį gamybos valandoms sekti, atlikite šiuos veiksmus.

1. Eikite į **Turto valdymas \> Sąranka \> Turto tipai \> Skaitikliai**.
1. Veiksmų srityje pasirinkite Naujas, kad sukurtumėte **skaitiklį**.
1. Antraštėje nustatykite šias vertes:

    - **Skaitiklis:** *ProductionHr*
    - **Pavadinimas: gamybos** *valandos*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Vienetas: personalas** *·*
    - **Atnaujinti: neautomatinis** *·*
    - **Bendra suma:** *suma*

1. Turto tipų **"** FastTab" pasirinkite Įtraukti **eilutę**.
1. Naujoje eilutėje lauke Turto **tipas nustatykite** oro *transporto eilutę*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Kurti turto priežiūros planą

Norėdami sukurti turto priežiūros planą, atlikite šiuos veiksmus.

1. Eikite į turto **valdymo nustatymo \> prevencinę \> priežiūros \> planą**.
1. Norėdami sukurti priežiūros planą, veiksmų **srityje** pasirinkite Naujas.
1. Antraštėje nustatykite šias vertes:

    - **Priežiūros planas:** *"AirKnife"*
    - **Pavadinimas:** *oro kniavimo planas*

1. „FastTab“ **Išsami informacija** nustatykite šias vertes:

    - **Plano data:** įveskite šiandienos datą.
    - **Įjungta:** *Taip*

1. Norėdami į **tinklelį** įtraukti eilutę **, "FastTab" eilutėse pasirinkite** Įtraukti turto skaitiklį. Tada nustatykite šias jo vertes:

    - **Darbo užsakymo aprašas:** *oro sistemos priežiūra*
    - **Priežiūros užduoties tipas: prevencinis** *·*
    - **Intervalo tipas:** *pakartotas iš paskutinio darbo užsakymo*
    - **Laikotarpio dažnis:** *10 000*
    - **Skaitiklis:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Nustatyti turto priežiūros scenarijų

Norėdami nustatyti turto priežiūros scenarijų tiekimo *grandinės valdymo dalyje*, atlikite šiuos veiksmus.

1. Eikite į **turto valdymo nustatymo \> " \> Jutiklio duomenų" \> scenarijus**.
1. Turto priežiūros **scenarijaus lauke** pasirinkite Konfigūruoti, kad **atidarytumėte** šio scenarijaus nustatymo vedlį.
1. Puslapyje Jutikliai **pasirinkite** Naujas, kad **į** tinklelį būtų galima įtraukti jutiklio. Tada nustatykite šiuos jo laukus:

    - **Jutiklio ID – įveskite jutiklio ID**, kurį naudojate. (Jei naudojate Rasp azure PI Azure IoT Online Simuliatorių ir nustatėte jį taip, kaip aprašyta [Nustatykite imituojamas bandymo jutiklis](sdi-set-up-simulated-sensor.md), įveskite *AssetMaintenance*.)
    - **Jutiklio** aprašas – įveskite jutiklio aprašymą.

1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu jutikliu, kurį norite pridėti dabar. Galite grįžti ir pridėti daugiau jutiklių bet kuriuo metu.
1. Pasirinkite **Toliau**.
1. Veiklos įrašų **susiejimo** puslapio dalyje **Jutikliai** pasirinkite įrašą vienam iš ką tik pridėtų jutiklių.
1. Verslo įrašų **susiejimo skyriuje pasirinkite** Naujas **, kad** į tinklelį įtraukumėte eilutę.
1. Naujoje eilutėje verslo įrašo **tipo laukas turi** būti automatiškai nustatytas į *Assets(EntAssetObjectTable)*. Nustatykite **verslo įrašo** lauką kaip išteklių, kuriuos naudojate pasirinktą jutiklio monitorių. (Jei naudojate demonstracinius duomenis, kuriuos sukūrėte anksčiau šiame straipsnyje, nustatykite juos kaip *AK-101, AK-101 1* eilutei oro".)
1. Iškart po to, kai pasirenkate verslo įrašo tipą eilutei, kurią pridėjote prie ankstesnio veiksmo, antra eilutė automatiškai pridedama prie tinklelio. Šioje eilutėje verslo įrašo **tipo laukas turi** būti nustatytas kaip *Counters(EntAssetCounterType)*. Nustatykite **turto skaitiklio** lauką Verslo įrašas, kurį atnaujinate pagal pasirinkto jutiklio signalus. (Jei naudojate demonstracinius duomenis, kuriuos sukūrėte anksčiau šiame straipsnyje, nustatykite juos kaip *ProductionUr, gamybos valandos*.)
1. Pasirinkite **Toliau**.
1. Skirtuko Aktyvuoti **jutiklius** puslapyje tinklelyje pasirinkite jutiklio funkciją, kurią pridėjote, tada pasirinkite **Aktyvinti**. Kiekvienam aktyviam jutikliui tinklelyje rodoma varnelė aktyviame **stulpelyje**.
1. Pasirinkite **Baigti**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Darbas su turto priežiūros scenarijumi

### <a name="view-counter-values"></a>Peržiūrėti skaitiklio vertes

Kai duomenys paruošti, o *turto* priežiūros scenarijus konfigūruojamas ir suaktyvinamas, galite matyti, kaip remiantis jutiklio duomenimis įterpiami turto skaitiklio įrašai.

1. Eikite į **Turto valdymo turtas \>\> Visas turtas**.
1. Raskite ir pasirinkite turtą, kurį norite patikrinti. (Jei naudojate demonstracinius duomenis, kuriuos sukūrėte anksčiau šiame straipsnyje, pasirinkite *AK-101*.)
1. Veiksmų srities turto skirtuke, **·** **prevencinę** grupę, pasirinkite Skaitikliai **turto** *AK-101 skaitiklio įrašų puslapiui atidaryti.*

> [!NOTE]
> Numatyta, kad skaitiklio įrašai bus įterpti kas tris valandas, t. y. jutiklio duomenys bus sujungti tuo intervalu. Intervalą galite pakeisti redaguodami užklausą "Azure Stream Analytics" komponente.

### <a name="generate-maintenance-work-orders"></a>Generuoti priežiūros darbo užsakymus

Įjungę turto *priežiūros scenarijų* ir nustatę priežiūros planą, galite vykdyti priežiūros grafiką, kad sugeneruotumėte priežiūros darbo užsakymus. Daugiau informacijos apie tai, kaip dirbti su prevencinę priežiūrą, ieškokite Prevencinių [priežiūros peržiūra](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
