---
title: Kiekis viršija pristatymo perviršio procentą važtaraščio kūrimo metu
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo perviršio procentą.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bc74c5748950b1f0f001fd89acb2e023640065ee
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920055"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Kiekis viršija pristatymo perviršio procentą važtaraščio kūrimo metu

Klaidos kodas: SYS24920

## <a name="symptoms"></a>Požymiai

Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo perviršio procentą.

Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:

> Eilutės pristatymo perteklius yra %1 procentai, o leistinas pristatymo perteklius yra tik %2 procentai.

Todėl negalite sugeneruoti krovinio važtaraščio.

## <a name="cause"></a>Priežastis

Paimtas krovinio arba siuntos kiekis yra didesnis nei užsakytas kiekis ir nėra pristatymo perviršio procento diapazone.

## <a name="resolution"></a>Sprendimas

Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Pakoreguokite krovinio eilutės kiekį.
- Pakoreguokite pristatymo perviršio procentą.
- Atšaukite ir atlikite koregavimus.

### <a name="adjust-the-load-line-quantity"></a>Krovinio eilutės kiekio koregavimas

Norėdami pakoreguoti krovinio eilutės kiekį, naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. Veiksmų srities skirtuko Siuntimas **ir Gauti** grupėje Atšaukimas pasirinkite Atšaukti **siuntos** **patvirtinimą**.
1. Skirtuke **Krovinio** eilutės pasirinkite prekės, viršijančios pristatymo perviršį procentais, krovinio eilutę.
1. Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.
1. Skirtuke **Eilutės informacija pasirinkite** **Užsakymas**.
1. Nustatykite **Kiekio** lauką į paimtą kiekį (tai yra, į lauko **Darbo sukurto kiekio** reikšmę), kad būtų galima atlikti važtaraščio generavimą.

### <a name="adjust-the-over-delivery-percentage"></a>Pristatymo perviršio procento koregavimas

Norėdami pakoreguoti pristatymo perviršio procentą, naudokite nurodytą procedūrą.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.
1. Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.
1. Skirtuke **Pardavimo užsakymo eilutės pasirinkite** prekės, viršijančios pristatymo perviršį procentais, pardavimo užsakymo eilutę.
1. Skirtuke **Eilutės informacija pasirinkite** **Pristatymas**.
1. Nustatykite lauką **Perviršis** į didesnį procentą, sutalpinantį pagal krovinio kiekį paimtą kiekį, kad būtų galima atlikti važtaraščio generavimą.

### <a name="reverse-and-make-adjustments"></a>Atšaukimas ir koregavimų atlikimas

Atšaukite viską, kas buvo užregistruota kroviniui (pavyzdžiui, važtaraštį, siuntos patvirtinimą ir darbą), atlikite pardavimo užsakymo koregavimus, iš naujo paleiskite užsakymą į sandėlį ir pabaikite siuntimo procedūrą.

Norėdami atšaukti važtaraštį, naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Veiksmų srities skirtuko Siuntimas **ir gauti** grupėje Atšaukti pasirinkite **Atšaukti** **važtaraščius**.

Naudokite šią procedūrą norėdami atšaukti siuntos patvirtinimą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Veiksmų srities skirtuko Siuntimas **ir Gauti** grupėje Atšaukimas pasirinkite Atšaukti **siuntos** **patvirtinimą**.

Norėdami atšaukti darbą naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Veiksmų srities skirtuke **Kroviniai**, darbo **grupėje**, pasirinkite Atšaukti **darbą**.
