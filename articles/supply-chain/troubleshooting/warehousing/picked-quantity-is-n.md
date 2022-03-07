---
title: Paimtas kiekis yra nepakankamas važtaraščio generavimo metu
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra paimtas kiekis, neatitinkantis sukurto darbo kiekio krovinio eilutėje.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249144"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Paimtas kiekis yra nepakankamas važtaraščio generavimo metu

Klaidos kodas: SYS54073

## <a name="symptoms"></a>Požymiai

Kai generuojate važtaraštį, siunčiamame krovinyje yra paimtas kiekis, neatitinkantis sukurto darbo kiekio krovinio eilutėje.

Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:

> Kadangi %1 yra paimta, nepakanka atnaujinti %2, kai vėliau likutis turi būti %3.

Todėl negalite sugeneruoti krovinio važtaraščio.

## <a name="cause"></a>Priežastis

Važtaraščio negalima sugeneruoti dabartinėje būsenoje, nes gali egzistuoti viena iš šių sąlygų:

- Susijęs darbas dar neparinktas ir perkeltas į galutinę siuntimo vietą.
- Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.
- Krovinio eilutės kiekis, sukurto darbo kiekis ir paimtas kiekis nesutampa.

## <a name="resolution"></a>Sprendimas

Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.
- Pakoreguokite krovinio eilutės kiekį.
- Atšaukite visas paėmimo registracijas ir perdarykite paėmimą.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka

Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.
1. Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.

### <a name="adjust-the-load-line-quantity"></a>Krovinio eilutės kiekio koregavimas

Norėdami pakoreguoti krovinio eilutės kiekį, naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.
1. Skirtuke  **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.
1. Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.
1. Nustatykite **Sumažinti krovinio eilutę** lauką, kad koregavimai atsispindėtų krovinio eilutėje.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Atšaukite visas paėmimo registracijas ir perdarykite paėmimą

Problema gali kilti dėl to, kad kažkas panaudojo paėmimo registraciją uždaryti krovinio eilutei be darbo. Tokiu atveju rankinio paėmimo registravimas turi būti atšauktas, o paėmimas turi būti baigtas naudojant „Warehouse Management Mobile App”.

Norėdami atšaukti paėmimo registravimą, naudokite toliau pateiktą procedūrą.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.
1. Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.
1. Skirtuke  **Pardavimo užsakymo eilutės** pasirinkite pardavimo užsakymo eilutę, kuriai buvo atliktas paėmimo registravimas.
1. Pasirinkite **Atnaujinti eilutę \> Paėmimas**, jei norite atsisakyti prekių paėmimo.
