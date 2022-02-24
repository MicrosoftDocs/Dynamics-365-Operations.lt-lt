---
title: Gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetams
description: Ši tema aprašo, kaip dirbti su gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetais.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08c46655d3966ad1433935318c5e60667dd10bb6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967773"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetams

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Kai kurios verslo funkcijos nėra visiškai palaikomos viešoje peržiūroje, kai darbo apkrovos skalės vienetai yra naudojami.

Gamybos vykdyme, debesiesi ir krašto skalės pajėgumai pristato tolesnius pajėgumus, net kai krašto vienetai nėra sujungti su centru:

- Mašinos operatoriai ir parduotuvės aukšto vadovai gali prieiti prie oepracijos gamybos plano.
- Mašinos operatiria gali turėti atnaujintą planą diskretiškam vykdymui ir proceso gamybos darbus.
- Parduotuvės aukšto vadovas gali keisti operacijos planą.
- Darbuotojai gali prieiti prie laiko ir lankymosi su laikrodžiu ir be jo veikiančiame krašte siekiant pataisyti darbuotojo užmokesčio skaičiuoklę.

Ši tema aprašo, kaip dirbti su gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetais.

## <a name="the-manufacturing-lifecycle"></a>Gamybos gyvavimo ciklas

Tolesnis paveikslėlis rodo gamybos gyvavimo ciklo padalijimą į tris etapus: *Planavimas*, *Vykdymas* ir *Užbaigimas*.

[![Gamybos vykdymo etapai, kai viena aplinka naudojama](media/mes-phases.png "Gamybos vykdymo etapai, kai viena aplinka naudojama")](media/mes-phases-large.png)

Etapas _Planavimas_ apima produkto sąvoką, planavimą, užsakymo sukūrimą ir planavimą ir išleidimą. Išleidimo žingsnis rodo perėjimą nuo _Planavimo_ etapo į _Vykdymo_ etapą. Kai gamybos užsakymas yra paleistas, gamybos užsakymo darbai bus matomi gamybos aukšte ir parengti vykdymui.

Kai gamybos darbas yra pažymėtas kaip baigtas, jis juda nuo _Vykdymo_ etapo prie _Užbaigimo_ etapo. Etape _Užbaigti_ registracijos nuo *Vykdymo* etapo pereina pro patvirtinimo darbo eigą, kai jos yra apskaičiuojamos, patvirtinamos ir perduodamos. Tuo metu, gamybos užsakymas yra užbaigtas. Dėl to, bazinis darbuotojo užmokestis yra sukuriamas.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Vykdymo etapo atskyrimas į keletą darbo apkrovų

Kaip rodo kitas paveikslėlis, kai skalės vienetai naudojami, _Vykdymo_ etapas yra paskirstomas kaip atskira darbo apkrova.

[![Gamybos vykdymo etapai, kai naudojami skalės vienetai](media/mes-phases-workloads.png "Gamybos vykdymo etapai, kai naudojami skalės vienetai")](media/mes-phases-workloads-large.png)

Modelis dabar eina nuo vieno elemento diegimo iki modelio, kuris yra pagrįstas centru ir skalės vienetais. Etapai _Planavimas_ ir _Užbaigimas_ vyksta, kai ne su klientais susijusios operacijos vykdomos centre ir gamybos vykdymo darbo apkrova vykdoma skalės vienetuose. Duomenys yra perduodami nesinchroniniu būdu tarp centro ir skalės vienetų.

Kai gamybos užsakymas išleidžiamas į centrą, visi duomenys yra būtini siekiant apdoroti gamybos darbus, kuries perduodami į skalės vienetą. Šie duomenys apima gamybos užsakymus, maršrutus, medžiagų aprašus ir gaminius. Duomenys nėra susiję su gamybos užsakymu (tokiu kaip netiesioginės veiklos, nebuvimo kodai ir gamybos parametrai) yra taip pat perduodami iš centro į skalės vienetą. Kaip taisyklės, duomenys ateinantys iš centro ir perduodami į skalės vienetą negali būti sukruti ar naujinti tik centre. Pavyzdžiui, naujas nebuvimo kodas ar netiesioginė veikla negali būti sukurta skalės vienete&mdash;jie gali būti panaudojami tik registravimui. Registravimai atlikti skalės vienete vykdymo metu yra tada perduodami į centrą, kuriame laikas ir buvimo patvirtinimas, inventorius ir finansiniai naujiniai yra apdorojami.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Gamybos vykdymo užduotys, kurios gali vykti darbo apkrovose

Tolesnės gamybos vykdymo užduotys šiuo metu gali būti vykdomos darbo apkrovose, kai skalės vienetai naudojami:

- Laiko suderinimas, prisijungimas ir laiko išderinimas ir nebuvimas
- Pradėti užduotį
- Pluoštiniai darbai
- Pranešti apie eigą
- Pranešti apie atliekas
- Netiesioginiai veiksmai
- Pertrauka

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Darbas su gamybos vykdymo darbo eigomis centre

Dažniausiai, procesai, kuriems reikia vykdyti gamybos darbo krūvius veikia automatiškai, kad palaikytų centrą ir skalės vienetus sinchroniniu būdu, kaip būtina. Nepaisant to, jei susiduriate su sunkumais, galite rankiniu būdu paleisti neapdorotų registracijų tvarkymą, kuris gaunamas iš darbo krūvių ir (arba) tikrinti registracijos tvarkymo žurnalą.

### <a name="manually-process-raw-registrations"></a>Rankiniu būdu tvarkykite neapdorotas registracijas

Palaidų vienetų darbas „Supply Chain Management“ veikia automatiniu būdu ir tvarko visas registacijas, gautas iš darbo krūvių. Sukurtiems darbams reikia gamybos žurnalų ir žurnalų knygos įrašų, kai registracija yra apdorojama baigtam darbui darbo krūvyje.

Nepaisant to, kad darbas dažniausiai vyksta automatiniu būdu, galite vykdyti jį rankiniu būdu bet kuriuo metu prisijungę prie centro ir patekę į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Neapdorotų registracijų tvarkymas**.

### <a name="check-the-raw-registration-processing-log"></a>Patikrinkite neapdorotos registracijos tvarkymo žurnalą

Norėdami peržiūrėti registacijos aprodojimo žurnalą, prisijunkite prie centro ir eikite į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Neapdorotų registracijų tvarkymo žurnalas**. Puslapyje **Neapdorotų registracijų tvarkymo žurnalas** rodomos apdorotos žalios registracijos ir visų registracijų būsena.

![Žialiavų registracijos tvarkymo žurnalo puslapis](media/mes-processing-log.png "Žialiavų registracijos tvarkymo žurnalo puslapis")

Galite dirbti su bet kuria registracija sąraše pasirinkę ją ir tada pasirinkę vieną iš tolesnių mygtukų veiksmų juostoje:

- **Tvarkyti** – Rankiniu būdu tvarkyti pasirinktą registraciją. Šis veiksmas gali būti naudingas, jei _Tvarkyti žalias registracijas_ darbas nevyko arba jis nepavyko.
- **Atšaukti** – Atšaukti pasirinktą registraciją.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Darbas su gamybos vykdymo darbo krūviais skalės vienete

Dažniausiai, procesai, kuriems reikia vykdyti gamybos darbo krūvius veikia automatiškai, kad palaikytų centrą ir skalės vienetus sinchroniniu būdu, kaip būtina. Nepaisant to, jei turite problemų, galite patikrinti užsakymų istoriją, kurie buvo sutvarkyti skalės vienete ar rankiniu būdu vykdyti _Gamybos centro į skalės vienetą pranešimo tvarkytuvas_ darbą.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Peržiūrėkite gamybos darbų istoriją, kurie buvo sutvarkyti skalės vienete

Norėdami peržiūrėti gamybos darbų istoriją, kurie buvo sutvarkyti skalės vienete, prisijunkite prie skalės vieneto mašinos ir eikite į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Gamybos darbų tvarkymo istorija**. Puslapyje **Gamybos darbų tvarkymo istorija** rodoma gamybos užsakymų skalės vienete tvarkymo istorija. Galite dirbti su bet kuriuo gamybos užsakymu sąraše pasirinkę ją ir tada pasirinkę vieną iš tolesnių mygtukų veiksmų juostoje:

- **Tvarkyti** – Rankiniu būdu tvarkyti pasirinktą gamybos užsakymą.
- **Atšaukti** – Atšaukti pasirinktą gamybos užsakymą.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Gamybos centras į skalės vieneto pranešimo tvarkytuvo darbą

_Gamybos centras į skalės vieneto pranešimo tvarkytuvą_ darbas tvarko duomenis iš centro į skalės vienetą. Šis darbas automatiniu būdu pradedamas, kai gamybos vykdymo darbo krūvis yra patalpintas. Nepaisant to, galite vykdyti rankiniu būdu jį bet kuriuo metu patekę į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \>Gamybos centras į skalės vieneto pranešimo tvarkytuvą**.
