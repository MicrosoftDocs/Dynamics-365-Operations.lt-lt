---
title: Gaunamų reisų ir siuntimo konteinerių veiklos ciklų sekimas
description: Šioje temoje paaiškinama, kaip galima naudoti gavimo sekimo puslapį, norint sekti savo reisų eigą ir gabenimo konteinerių keliones.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 94754447b3f363716595de4902f48188c4ebbda9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022018"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Gaunamų reisų ir siuntimo konteinerių veiklos ciklų sekimas

[!include [banner](../../includes/banner.md)]

Puslapyje **Gaunamų prekių sekimas** galima sekti savo reisų eigą ir siuntimo konteinerių veiklos ciklus. Kiekvienas reisas ir veiklos ciklas yra skirstomas pagal *veiklas*, kurių kiekviena puslapyje turi savo eilutę. Puslapį galite naudoti numatomoms datoms ir faktinėms datoms peržiūrėti ir įvesti pagal veiklą.

Paprastai, priklausomai nuo sąrankos [sekimo kontrolės centre](delivery-information-setup.md#tracking-control-center) ši veikla automatiškai rodo įvertintą nukreipimo datą galutinėje paskirties vietoje. Taip pat, atsižvelgiant į nustatymą, galutinė data paprastai atnaujina pristatymo datą arba patvirtintą datą pirkimo užsakymo eilutėse. Perkėlimo užsakymo eilutėms galima nustatyti sistemą atnaujinti gavimo dieną.

Kad atidarytumėte puslapį **Gaunamų prekių sekimas**, eikite į **Iškrovimo kaina \> Sekimas \> Gaunamų prekių sekimas**.

## <a name="filter-the-activities-list"></a>Veiklų sąrašo filtravimas

Galite naudoti laukelius **Reisas** ir **Siuntimo konteineris** puslapio **Gaunamų prekių sekimas** viršuje, kad filtruotumėte puslapį taip, kad jame būtų rodomi tik tie veiksmai, kurie yra susiję su pasirinktu reisu ir (arba) siuntimo konteineriu.

## <a name="update-tracking-information"></a>Sekimo informacijos atnaujinimas

Norėdami atnaujinti reiso ar veiklos ciklo grafiką, įveskite pirmosios veiklos pradžios datą. Tada atnaujinama numatoma paskutinės veiklos pabaigos data. Kiekvienos atkarpos ir veiklos ciklo šablono nustatymas [sekimo kontrolės centre](delivery-information-setup.md#tracking-control-center) nustato įvertintą gamybos laiką. Įvertintos pabaigos datos naudoja gamybos laiką nuo veiklos pradžios datos. Tada, kai įrašoma faktinė pabaigos data, kitos veiklos pradžios data atnaujinama į tą pačią datą kaip ir ankstesnės veiklos faktinė pabaigos data. Faktinis gamybos laikas atnaujinamas, kad būtų galima palyginti ir analizuoti. Papildomas pastabas galima įvesti laukelyje **Pastaba**.

Veiklos tinklelyje tvarką lemia atitinkamo veiklos ciklo šablono atkarpų tvarka. Jei pasikeičia pridėtų veiklos ciklo atkarpų tvarka, taip pat pasikeičia ir sekimo kontrolė.

Datas visiems konteineriams galite atnaujinti veiksmų srityje pasirinkdami **Atnaujinti pradžios datą** arba **Atnaujinti faktinę pabaigos datą**. Arba galite įvesti datas kiekvienam siuntos konteineriui. Šis būdas leidžia daugiau lankstumo, nes konteineriai gali būti padalinti į kelių veiklos ciklų aplinką.

## <a name="buttons-on-the-action-pane"></a>Veiksmų srities mygtukai

Puslapio **Gaunamų prekių sekimas** veiksmų srityje galite naudoti mygtukus, dirbdami su įeinančiais reisais ir veiklos ciklais. Šioje lentelėje aprašomi galimi mygtukai.

| Mygtukas | aprašymas |
|---|---|
| Redagavimas | Redaguokite reisą arba siuntimo konteinerio veiklos ciklą. |
| Naujos | Kurkite naują reisą arba siuntimo konteinerio veiklos ciklą. |
| Panaikinti | Ištrinkite pasirinktą reisą arba siuntimo konteinerio veiklos ciklą. |
| Naujinti pradžios datą | Atnaujinkite visų reiso konteinerių veiklos pradžios datą. Atnaujinus konkrečios veiklos ar kelionės atkarpos pradžios datą, kitos numatytos pradžios datos atnaujinamos remiantis nurodytu gamybos laiku. |
| Atnaujinti faktinės pabaigos datą | Atnaujinkite visų reiso konteinerių veiklos pabaigos datą. Atnaujinus konkrečios veiklos pabaigos datą, kitos veiklos atnaujinamos remiantis nurodytu gamybos laiku. |
| Įtraukti veiklas | Rankiniu būdu prie reiso pridėkite veiklą. Pavyzdžiui, galite pridėti fumigacijos veiklą. Pridedant gali pasikeisti patvirtinta transporto priemonės prekių pristatymo data arba reisas. Kai veikla pridedama prie veiklos ciklo, įvertintos dienos neįvedamos, kol nebus atnaujinta veiklos ciklo atkarpos pradžios data. |

## <a name="information-and-settings-on-the-overview-tab"></a>Informacija ir nustatymai apžvalgos skirtuke

Skirtuke **Apžvalga** rodomas visų veiklų, priklausančių reisui ir (arba) siuntimo konteineriui, kuris yra pasirinktas puslapio viršuje, sąrašas. Šioje lentelėje apibūdinami galimi kiekvienos veiklos laukeliai.

| Laukas | aprašymas |
|---|---|
| Atkarpa | Veiklos atkarpos ID, kaip apibrėžiama veiklos ciklo šablone. |
| Pristatymo būdas | Numatomas veiklos pristatymo būdas. |
| Veikla | Šis laukelis paprastai identifikuoja su veikla susietą darbą ar užduotį. Įprasti pavyzdžiai: *Plukdymas* ir *Apmokėjimas*. |
| aprašymas | Ilgesnis veiklos aprašymas. |
| Pradžios data | Šiame laukelyje iš pradžių rodoma numatoma veiklos pradžios data. Tačiau, jei įvesta faktinė ankstesnės veiklos pabaigos data, jame rodoma faktinė pradžios data. Šis laukelis naudojamas numatomai pabaigos datai apibrėžti, atsižvelgiant į gamybos laiką. |
| Numatyta pabaigos data | Šio laukelio vertė apskaičiuojama pagal pradžios datą ir gamybos laiką. Paprastai tiesiogiai vertės redaguoti nereikės. |
| Faktinė pabaigos data | Naudotojas turėtų kaip galima greičiau po veiklos pasirodymo atnaujinti šį laukelį. Tada atnaujinamas faktinis gamybos laikas. |
| Įvertintos dienos | Numatomas laikas (dienomis), reikalingas šiai veiklai atlikti. |
| Faktinės dienos | Faktinis laikas (dienomis), reikalingas šiai veiklai atlikti. |
| Banknotas | Naudokite šį laukelį, norėdami pridėti papildomas pastabas ir informaciją apie veiklą. |

## <a name="information-and-settings-on-the-general-tab"></a>Informacija ir nustatymai skirtuke „Bendra“

Skirtuke **Bendra** rodoma informacija apie atkarpą, pasirinktą skirtuke **Apžvalga**. Nors jame kartojama tam tikra informacija, kuri rodoma skirtuke **Apžvalga**, jame taip pat pateikiama papildoma informacija apie pažymėtą atkarpą.
