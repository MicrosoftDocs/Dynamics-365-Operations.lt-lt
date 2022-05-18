---
title: Gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetams
description: Ši tema aprašo, kaip dirbti su gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetais.
author: johanhoffmann
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: johanho
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b30e16489b0b0169f08e52c70cf4489c9bf4ce1b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674060"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Gamybos vykdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Gamybos vykdymo darbo krūvį šiuo metu galima naudoti tik peržiūroje.
>
> Kai kurios verslo funkcijos nėra visiškai palaikomos viešoje peržiūroje, kai darbo apkrovos skalės vienetai yra naudojami.
>
> Negalima vykdyti gamybos vykdymo darbo krūvio peržiūros skalės vienete, kuriame taip pat įdiegtas sandėlio vykdymo darbo krūvis.

Vykstant gamybai, skalės vienetai suteikia šias galimybes:

- Mašinos operatoriai ir parduotuvės aukšto vadovai gali prieiti prie operacijos gamybos plano.
- Mašinos operatoriai gali vis atnaujintą planą diskretiškam vykdymui ir proceso gamybos darbams.
- Parduotuvės aukšto vadovas gali keisti operacijos planą.
- Darbuotojai gali prieiti prie laiko ir lankymosi su laikrodžiu ir be jo veikiančiame krašte siekiant pataisyti darbuotojo užmokesčio skaičiuoklę.

Ši tema aprašo, kaip dirbti su gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetais.

## <a name="the-manufacturing-lifecycle"></a>Gamybos gyvavimo ciklas

Tolesnis paveikslėlis rodo gamybos gyvavimo ciklo padalijimą į tris etapus: *Planavimas*, *Vykdymas* ir *Užbaigimas*.

[![Gamybos vykdymo etapai, kai viena aplinka naudojama](media/mes-phases.png "Gamybos vykdymo etapai, kai viena aplinka naudojama.")](media/mes-phases-large.png)

Etapas _Planavimas_ apima produkto sąvoką, planavimą, užsakymo sukūrimą ir planavimą ir išleidimą. Išleidimo žingsnis rodo perėjimą nuo _Planavimo_ etapo į _Vykdymo_ etapą. Kai gamybos užsakymas yra paleistas, gamybos užsakymo darbai bus matomi gamybos aukšte ir parengti vykdymui.

Kai gamybos darbas yra pažymėtas kaip baigtas, jis juda nuo _Vykdymo_ etapo prie _Užbaigimo_ etapo. Etape _Užbaigti_ registracijos nuo *Vykdymo* etapo pereina pro patvirtinimo darbo eigą, kai jos yra apskaičiuojamos, patvirtinamos ir perduodamos. Tuo metu, gamybos užsakymas yra užbaigtas. Dėl to, bazinis darbuotojo užmokestis yra sukuriamas.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Vykdymo etapo atskyrimas į keletą darbo apkrovų

Kaip rodo kitas paveikslėlis, kai skalės vienetai naudojami, _Vykdymo_ etapas yra paskirstomas kaip atskira darbo apkrova.

[![Gamybos vykdymo etapai, kai naudojami skalės vienetai](media/mes-phases-workloads.png "Gamybos vykdymo etapai, kai naudojami skalės vienetai.")](media/mes-phases-workloads-large.png)

Modelis dabar eina nuo vieno elemento diegimo iki modelio, kuris yra pagrįstas centru ir skalės vienetais. Etapai _Planavimas_ ir _Užbaigimas_ vyksta, kai ne su klientais susijusios operacijos vykdomos centre ir gamybos vykdymo darbo apkrova vykdoma skalės vienetuose. Duomenys yra perduodami nesinchroniniu būdu tarp centro ir skalės vienetų.

Kai gamybos užsakymas išleidžiamas į centrą, visi duomenys yra būtini siekiant apdoroti gamybos darbus, kurie perduodami į skalės vienetą. Šie duomenys apima gamybos užsakymus, maršrutus, medžiagų aprašus ir gaminius. Duomenys nėra susiję su gamybos užsakymu (tokiu kaip netiesioginės veiklos, nebuvimo kodai ir gamybos parametrai) yra taip pat perduodami iš centro į skalės vienetą. Kaip taisyklės, duomenys ateinantys iš centro ir perduodami į skalės vienetą negali būti sukruti ar naujinti tik centre. Pavyzdžiui, naujas nebuvimo kodas ar netiesioginė veikla negali būti sukurta skalės vienete&mdash;jie gali būti panaudojami tik registravimui. Registravimai atlikti skalės vienete vykdymo metu yra tada perduodami į centrą, kuriame laikas ir buvimo patvirtinimas, inventorius ir finansiniai naujiniai yra apdorojami.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Gamybos vykdymo užduotys, kurios gali vykti darbo apkrovose

Tolesnės gamybos vykdymo užduotys šiuo metu gali būti vykdomos darbo apkrovose, kai skalės vienetai naudojami:

- Laiko suderinimas, prisijungimas ir laiko išderinimas ir nebuvimas
- Pradėti užduotį
- Pluoštiniai darbai
- Pranešti apie eigą
- Pranešti apie atliekas
- Netiesioginiai veiksmai
- Pertrauka
- Pranešti, kad baigta ir padėti (reikia, kad sandėlio vykdymo darbo krūvį paleistumėte ir savo skalės vienete, taip pat žr. ataskaitą kaip baigtą ir padėti [ant svarstyklių vieneto](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Darbas su gamybos vykdymo darbo eigomis centre

Dažniausiai, procesai, kuriems reikia vykdyti gamybos darbo krūvius veikia automatiškai, kad palaikytų centrą ir skalės vienetus sinchroniniu būdu, kaip būtina. Nepaisant to, jei susiduriate su sunkumais, galite rankiniu būdu paleisti neapdorotų registracijų tvarkymą, kuris gaunamas iš darbo krūvių ir (arba) tikrinti registracijos tvarkymo žurnalą.

### <a name="manually-process-raw-registrations"></a>Rankiniu būdu tvarkykite neapdorotas registracijas

Palaidų vienetų darbas „Supply Chain Management“ veikia automatiniu būdu ir tvarko visas registracijas, gautas iš darbo krūvių. Sukurtiems darbams reikia gamybos žurnalų ir žurnalų knygos įrašų, kai registracija yra apdorojama baigtam darbui darbo krūvyje.

Nepaisant to, kad darbas dažniausiai vyksta automatiniu būdu, galite vykdyti jį rankiniu būdu bet kuriuo metu prisijungę prie centro ir patekę į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Neapdorotų registracijų tvarkymas**.

### <a name="check-the-raw-registration-processing-log"></a>Patikrinkite neapdorotos registracijos tvarkymo žurnalą

Norėdami peržiūrėti registracijos apdorojimo žurnalą, prisijunkite prie centro ir eikite į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Neapdorotų registracijų tvarkymo žurnalas**. Puslapyje **Neapdorotų registracijų tvarkymo žurnalas** rodomos apdorotos žalios registracijos ir visų registracijų būsena.

![Žaliavų registracijos tvarkymo žurnalo puslapis.](media/mes-processing-log.png "Žaliavų registracijos tvarkymo žurnalo puslapis")

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

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Pranešti, kad baigta, ir padėti ant svarstyklių vieneto

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

Dabartiniame leidime sandėlio vykdymo darbo krūvis palaiko operacijas kaip baigtas ir padėjusias (baigtų produktų, sudėtinųjų ir tarpinių produktų) operacijas [ne gamybos vykdymo darbo krūvį](cloud-edge-workload-warehousing.md). Todėl, norėdami šią funkciją naudoti prijungę prie svarstyklių vieneto, turite atlikti šiuos veiksmus:

- Įdiekite sandėlio vykdymo darbo krūvį ir gamybos vykdymo darbo krūvį savo skalės vienete.
- „Warehouse Management“ mobiliąją programą naudokite norėdami pranešti, kad baigta, ir apdoroti atidavimo darbą. Gamybos laiko vykdymo sąsaja šiuo metu nepalaiko šių procesų.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

## <a name="enable-and-use-the-start-operation-on-a-scale-unit"></a>Įjungti ir naudoti pradžios operaciją svarstyklių vienetais

Šiame leidime gamybos ir paketinių užsakymų pradžios operaciją palaiko [sandėlio vykdymo darbo krūvis](cloud-edge-workload-warehousing.md) (ne gamybos vykdymo darbo krūvis). Todėl norėdami naudoti šią funkciją kai esate prisijungę prie svarstyklių vieneto, turite atlikti šias užduotis:

- Įdiekite sandėlio vykdymo darbo krūvį ir gamybos vykdymo darbo krūvį savo skalės vienete.
- Funkcijų valdymo funkcijai *debesies ir kraštų skalės vieneto funkcijai įjungti sandėlio valdymo darbo* krūvį Pradėti [gamybos užsakymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Norėdami pradėti gamybos arba paketinį užsakymą naudokite sandėlio valdymo mobiliąją programą.

## <a name="enable-and-use-material-consumption-on-a-scale-unit"></a>Įgalinti ir naudoti medžiagų suvartojimą svarstyklių vienetais

Dabartiniame leidime sandėlio [valdymo](cloud-edge-workload-warehousing.md) mobiliosios programos srautą medžiagų suvartojimui registruoti palaiko sandėlio vykdymo darbo krūvis (ne gamybos vykdymo darbo krūvis). Todėl norėdami naudoti šią funkciją kai esate prisijungę prie svarstyklių vieneto, turite atlikti šias užduotis:

- Įdiekite sandėlio vykdymo darbo krūvį ir gamybos vykdymo darbo krūvį savo skalės vienete.
- Įgalinkite *registruoti medžiagų suvartojimą mobilioje programoje skalės vieneto* funkcija, kuri yra [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Naudokite sandėlio valdymo mobiliąją programą medžiagų suvartojimui registruoti.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
