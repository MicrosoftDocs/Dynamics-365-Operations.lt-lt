---
title: Turto KPI
description: Šioje temoje aiškinama turto KPI turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3ebbb1016bafed8ad9fb998fc76152e215c08c3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433493"
---
# <a name="asset-kpis"></a>Turto KPI

[!include [banner](../../includes/banner.md)]

 

Turto valdyme galite skaičiuoti įvairius turto ir turto tipų pagrindinius efektyvumo indikatorius (KPI). Naudojate KPI, kad galėtumėte peržiūrėti turto efektyvumą, susijusį, pavyzdžiui, su darbinės būsenos periodu, prastova, remonto laiku ir vidutinio laiku tarp gedimų (MTBF).

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto KPI**.

2. Dialoge lange **Skaičiuoti turto KPI** pažymėkite **Laiko skalė**, kuri bus naudojama skaičiuojant, ir laikotarpį laukuose **Nuo datos** ir **Iki datos**. 

3. „FastTab“ **Įtrauktini įrašai** galite pažymėti konkretų turtą ir turto tipus, kurie bus įtraukti į skaičiavimą, jei reikia.

4. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

5. „FastTab“ **Apžvalga** skaičiavimo rezultatai rodomi tinklelio rodinyje. Kiekvienas turtas rodomas atskiroje eilutėje.

6. „FastTab“ **Pasirinktos eilutės KPI** galite matyti turto, pasirinkto „FastTab“ **Apžvalga**, skaičiavimus. KPI reikšmės kategorizuojamos pagal **Laikas**, **Pasiekiamumas**, **Darbo užsakymai**, **Priežiūra**, **Gedimai**, **Prižiūrimo turto prastova** ir **Išlaidos**.

Lentelėje toliau pateiktas laukų puslapyje **Turto KPI** aprašas.

| Laukas                   | Aprašymas                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ilgalaikio turto                   | Turto ID.                                                                                                                                                                                                                                                                                             |
| Visas laikas              | Bendras laikas, nustatytas kalendoriuje, kuris naudotas skaičiuojant. Jei turtas susijęs su ištekliais, naudojamas ištekių kalendorius. Jei turtas nesusijęs su ištekliais, naudojamas kalendorius, pasirinktas **Turto valdymo parametrai** lauke **Standartinis kalendorius**. |
| Darbinės būsenos periodas                  | Bendras laikas be prastovos.                                                                                                                                                                                                                                                                            |
| Prastova                | Prižiūrimo turto prastovų registracijos, atliktos turtui pasirinktu laikotarpiu.                                                                                                                                                                                                                              |
| Remonto laikas             | Bendras remonto darbo užsakymų vykdymo valandų skaičius.                                                                                                                                                                                                                                            |
| Pasiekiamumas (%)          | Darbinės būsenos periodas, padalintas iš bendro laiko ir padaugintas iš 100.                                                                                                                                                                                                                                                   |
| Gedimų skaičius        | Gedimo priežasčių, užregistruotų pagal turto gedimo požymius pasirinktu laikotarpiu, skaičius.                                                                                                                                                                                                             |
| Vidutinis laikas tarp gedimų (MTBF)                    | Vidutinis laikas tarp gedimų – tai bendras laikas, padalintas iš gedimų, užregistruotų turtui pasirinktu laikotarpiu, skaičiaus. Jei gedimų skaičius yra nulis, vidutinis laikas tarp gedimų (MTBF) nustatomas kaip bendras laikas.                                                                                                                   |
| Gedimų intensyvumas               | 1, padalintas iš vidutinio laiko tarp gedimų (MTBF).                                                                                                                                                                                                                                                                                    |
| Vidutinis remonto laikas (MRT)                     | Vidutinis remonto laikas – tai remonto laikas, padalintas iš gedimų, užregistruotų turtui pasirinktu laikotarpiu. Jei gedimų skaičius yra nulis, vidutinis remonto laikas (MRT) nustatomas kaip bendras laikas.                                                                                                                           |
| Sustabdymų skaičius         | Prižiūrimo turto prastovos registracijų, sukurtų turtui, skaičius.                                                                                                                                                                                                                                     |
| Vidutinis laikas tarp sustabdymų (MTBS)                    | Vidutinis laikas tarp sustabdymų – tai bendras laikas, padalintas iš prižiūrimo turto prastovos registracijų. Jei prižiūrimo turto prastovos registracijų skaičius pasirinktu laikotarpiu yra nulis, vidutinis laikas tarp sustabdymų (MTBS) nustatomas kaip bendras laikas.                                                                                      |
| Prevencinės išlaidos         | Išlaidos, užregistruotos turtui, susijusiam su išlaidų tipu Prevencinės pasirinktu laikotarpiu. Išlaidų tipai nustatomi darbo užsakymų tipuose.                                                                                                                                                                       |
| Koreguojamosios išlaidos         | Išlaidos, užregistruotos turtui, susijusiam su išlaidų tipu Korekcinės pasirinktu laikotarpiu. Išlaidų tipai nustatomi darbo užsakymų tipuose.                                                                                                                                                                       |
| Atkuriamoji vertė       | Reikšmė, apibrėžta turtui kaip pakeitimo išlaidos.                                                                                                                                                                                                                                                  |
| Turto tipas             | Turto tipo, pasirinkto turtui, identifikavimas.                                                                                                                                                                                                                                             |
| Gamintojas           | Gamintojo, pasirinkto turtui, identifikavimas.                                                                                                                                                                                                                                                 |
| Modelis                   | Gamintojo modelio, pasirinkto turtui, identifikavimas.                                                                                                                                                                                                                                           |
| Data Nuo               | KPI skaičiavimo pradžios data. Jei turtas buvo sukurtas po pradžios datos, pasirinktos skaičiavimui, turto pradžios data rodoma šiame lauke.                                                                                                                                  |
| Data Iki                 | KPI skaičiavimo pabaigos data. Jei turtas buvo užregistruotas kaip neaktyvus prieš pabaigos datą, pasirinktą skaičiavimui, data, nuo kurios turtas nėra aktyvus, rodoma šiame lauke.                                                                                               |
| Laiko skalė              | Skaičiuojant KPI, turite pasirinkti laiko skalę valandomis, dienomis arba savaitėmis.                                                                                                                                                                                                            |
| Esamumas            | Darbinės būsenos periodas, padalintas iš bendro laiko.                                                                                                                                                                                                                                                                         |
| Darbo užsakymai             | Bendras darbo užsakymų, įtrauktų į KPI skaičiavimą, skaičius.                                                                                                                                                                                                                                          |
| Darbo užsakymo laikas         | Bendras darbo užsakymų vykdymo valandų skaičius.                                                                                                                                                                                                                                               |
| Pirminiai darbo užsakymai     | Pirminių darbo užsakymų, įtrauktų į KPI skaičiavimą, skaičius.                                                                                                                                                                                                                                        |
| Antriniai darbo užsakymai   | Antrinių darbo užsakymų, įtrauktų į KPI skaičiavimą, skaičius.                                                                                                                                                                                                                                      |
| Darbo užsakymų tvarkymas | Antrinių priežiūros darbų užsakymų, įtrauktų į KPI skaičiavimą, skaičius. Priežiūros darbo užsakymas yra darbo užsakymas be susijusių gedimo priežasčių.                                                                                                                                                             |
| Priežiūros užduotis        | Bendras priežiūros darbo užsakymų vykdymo valandų skaičius.                                                                                                                                                                                                                                       |
| Remonto darbo užsakymai      | Pirminių remonto darbų užsakymų, įtrauktų į KPI skaičiavimą, skaičius. Remonto darbo užsakymas yra darbo užsakymas su susijusia gedimo priežastimi.                                                                                                                                                                        |
| Patikimumas (%)           | Skaičiavimas, pagrįstas numatomu eksponentiniu turto gedimo registracijų pokyčiu reiškia, kad per laiką turtas dėl dėvėjimosi tampa mažiau patikimas. Šio KPI skaičiavimas pagrįstas vidutiniu laiku tarp gedimų (MRBF) ir bendru laiku.                                                            |
| Vidutinis gamybos sustabdymų laikas (MTPS)                    | Vidutinis laikas tarp sustabdymų – tai bendras laikas, padalintas iš prižiūrimo turto prastovos registracijų. Jei prižiūrimo turto prastovos registracijų skaičius pasirinktu laikotarpiu yra nulis, vidutinis gamybos sustabdymų laikas (MTPS) nustatomas kaip nulis.                                                                               |
| Bendroji savikaina              | Bendros išlaidos, užregistruotos turtui pasirinktu laikotarpiu.                                                                                                                                                                                                                                              |
| Investicijų išlaidos         | Išlaidos, užregistruotos turtui, susijusiam su išlaidų tipu Investicija pasirinktu laikotarpiu. Išlaidų tipai nustatomi darbo užsakymų tipuose.                                                                                                                                                                       |

Toliau pateiktame paveiksle rodoma keturių turtų KPI skaičiavimo ekrano kopija.

![Keturių turtų KPI skaičiavimo ekrano kopija](media/11-controlling-and-reporting.png)

- **Visas turtas** galite pažymėti kelis turtus, tada spustelėkite skirtuko **Bendra** mygtuką **Turto KPI**. Tada dialogo lange **Skaičiuoti turto KPI** spustelėkite **Gerai**, kad apskaičiuotumėte pasirinkto turto KPI.  
- Į KPI skaičiavimo rezultatus gali arba negali būti įtrauktos [prižiūrimo turto prastovos registracijos](../work-orders/maintenance-downtime.md) atsižvelgiant į sąranką ir prižiūrimo turto prastovos priežasčių kodų naudojimą. 

