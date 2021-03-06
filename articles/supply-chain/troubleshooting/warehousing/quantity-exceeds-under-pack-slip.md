---
title: Kiekis viršija pristatymo trūkumo procentą važtaraščio kūrimo metu
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo trūkumo procentą.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249140"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Kiekis viršija pristatymo trūkumo procentą važtaraščio kūrimo metu

Klaidos kodas: SYS24921

## <a name="symptoms"></a>Požymiai

Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija pristatymo trūkumo procentą.

Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:

> Eilutės pristatymo trūkumas yra %1 procentai, o leistinas pristatymo trūkumas yra tik %2 procentai.

Todėl negalite sugeneruoti krovinio važtaraščio.

## <a name="cause"></a>Priežastis

Paimtas krovinio arba siuntos kiekis yra mažesnis nei užsakytas kiekis ir nėra pristatymo trūkumo procento diapazone.

## <a name="resolution"></a>Sprendimas

Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Pakoreguokite perviršio trūkumo procentą.
- Atšaukite ir atlikite koregavimus.

### <a name="adjust-the-under-delivery-percentage"></a>Perviršio trūkumo procento koregavimas

Norėdami pakoreguoti pristatymo trūkumo procentą, naudokite nurodytą procedūrą.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.
1. Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.
1. Skirtuke  **Pardavimo užsakymo eilutės** pasirinkite prekės, viršijančios pristatymo trūkumo procentą, pardavimo užsakymo eilutę.
1. Skirtuke  **Eilutės informacija** pasirinkite **Pristatymas**.
1. Nustatykite lauką **Pristatymo trūkumas** į didesnį procentą, sutalpinantį pagal krovinio kiekį paimtą kiekį, kad būtų galima atlikti važtaraščio generavimą.

### <a name="reverse-and-make-adjustments"></a>Atšaukimas ir koregavimų atlikimas

Atšaukite viską, kas buvo užregistruota kroviniui (pavyzdžiui, važtaraštį, siuntos patvirtinimą ir darbą), atlikite pardavimo užsakymo koregavimus, iš naujo paleiskite užsakymą į sandėlį ir pabaikite siuntimo procedūrą.

Norėdami atšaukti važtaraštį, naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti važtaraščius**.

Naudokite šią procedūrą norėdami atšaukti siuntos patvirtinimą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.

Norėdami atšaukti darbą naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Veiksmų juostos skirtuke  **Kroviniai**, grupėje  **Darbas** pasirinkite  **Atšaukti darbą**.
