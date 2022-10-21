---
title: Turto prastovos scenarijus
description: Šiame straipsnyje aprašomas turto naudojimo laiko scenarijus, kuris leidžia naudoti jutiklio duomenis, kad būtų galima stebėti turto prieinamumą.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689435"
---
# <a name="the-asset-downtime-scenario"></a>Turto prastovos scenarijus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Turto prastovo scenarijus sugeneruoja priežiūros downtime įrašą, jei joks signalas iš įrenginio ne gaunamas per nustatytą laiko ribą nuo paskutinio signalo gavimo. Scenarijui reikia, kad jūsų kompiuteryje tilptų jutiklis, kuris periodiškai siunčia signalą "Azure IoT" centrui, kol kompiuteris veikia, tačiau nesiunčia signalo, kai kompiuteris neveikia.

## <a name="set-up-the-asset-downtime-scenario"></a>Nustatyti turto prasto laiko scenarijų

Norėdami nustatyti turto prasto laiko scenarijų *tiekimo grandinės* valdymo dalyje, atlikite šiuos veiksmus.

1. Eikite į **turto valdymo \> nustatymo \> "Jutiklio duomenų \> tyrimų scenarijus** ", norėdami atidaryti **scenarijų** puslapį.
2. **Turto prasto scenarijaus** lauke pasirinkite Konfigūruoti, **kad** būtų atidarytas šio scenarijaus nustatymo vedlys.
3. Puslapyje Jutikliai **pasirinkite** Naujas, kad **į** tinklelį būtų galima įtraukti jutiklio. Tada nustatykite šiuos jo laukus:

    - **Jutiklio ID – įveskite jutiklio ID**, kurį naudojate. (Jei naudojate Rasp azure PI Azure IoT Online Simuliatorių ir nustatėte jį taip, kaip aprašyta [Nustatykite imituojamas bandymo jutiklis](sdi-set-up-simulated-sensor.md), įveskite *AssetDownTime*.)
    - **Jutiklio** aprašas – įveskite jutiklio aprašymą.

4. Pakartokite ankstesnį veiksmą su kiekvienu papildomu jutikliu, kurį norite pridėti dabar. Galite grįžti ir pridėti daugiau jutiklių bet kuriuo metu.
5. Pasirinkite **Toliau**.
6. Veiklos įrašų **susiejimo** puslapio dalyje **Jutikliai** pasirinkite įrašą vienam iš ką tik pridėtų jutiklių.
7. Verslo įrašų **susiejimo skyriuje pasirinkite** Naujas **, kad** į tinklelį įtraukumėte eilutę.
8. Naujoje eilutėje nustatykite verslo **įrašo lauką** kaip išteklių, kuriuos naudojate pasirinktą jutiklio monitorių. (Jei naudojate demonstracinius duomenis, pasirinkite *AK-101, 1 eilutės oro pagal orą*.)
9. Pasirinkite **Toliau**.
10. **Turto prasto laiko ribinės vertės** puslapyje nurodykite, kiek laiko po paskutinio signalo sistema turi laukti prieš išsiųsdami pranešimą apie turto prasto laiką. Yra du būdai ribinei vertei nustatyti:

    - **Numatytoji ribinė vertė (minutėmis)** – nustatykite šį lauką, kad jis apibrėžtų numatytąją ribinę vertę. Ši vertė taikoma visiems ištekliams, kurių laukas **Pranešimo ribinė reikšmė (minutėmis)** nustatytas dviem minutėmis ar žemiau. Mažiausia vertė yra *2* (minutės).
    - **Ribinė vertė, nustatyti, ar įrenginys neatsako (minutėmis)** – kiekvienam ištekliui tinklelyje, kur nenorite naudoti numatytosios ribinės vertės, šiame lauke įveskite perrašymo vertę. Ištekliams, kurie nustatyti taip, kad būtų naudojama dviejų minučių arba mažesnė ribinė reikšmė **, bus naudojamas numatytosios ribinės vertės (minučių)** parametras.
11. Pasirinkite **Toliau**.
12. Skirtuko Aktyvuoti **jutiklius** puslapyje tinklelyje pasirinkite nustatytą jutiklių ir pasirinkite **Aktyvinti**. Kiekvienam aktyviam jutikliui tinklelyje rodoma varnelė aktyviame **stulpelyje**.
13. Pasirinkite **Baigti**.

## <a name="work-with-the-asset-downtime-scenario"></a>Darbas su turto prasto laiko scenarijumi

Jei iš turto ne gaunamo jutiklio signalo, kuris patenka į scenarijaus konfigūracijoje nurodytą ribinę vertę, sistema sukurs to turto priežiūros prasto laiko įrašą. Vadybininkai turėtų periodiškai peržiūrėti downtime įrašus (pvz., kartą per kiekvieną darbo pamainą) ir kiekvienai downtime registracijai taikyti atitinkamus priežasčių kodus ir pabaigos laiką. Norėdami peržiūrėti turto priežiūros downtime įrašus, atlikite šiuos veiksmus:

1. Eikite į **Turto valdymo > Turtas > Visas turtas**.
2. Raskite ir pasirinkite turtą, kurį norite patikrinti. (Jei naudojate demonstracinius duomenis, pasirinkite *AK-101*.)
3. Veiksmų srityje atidarykite **skirtuką** **Turtas** ir darbo užsakymų grupėje pasirinkite Priežiūros downtime **,** kad atidarytumėte pasirinkto turto priežiūros downtime įrašų puslapį.
