---
title: Kiekis, kurį bandote atnaujinti, viršija gautą/pristatytą kiekį.
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija darbo kiekį, kuris buvo paimtas ir rezervuotas pardavimo užsakymui.
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
ms.openlocfilehash: ec5e0ac8dd097e5ebf016683fc5c17df7ecb2305
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920403"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Kiekis, kurį bandote atnaujinti, viršija gautą/pristatytą kiekį

Klaidos kodas: SYS7676

## <a name="symptoms"></a>Požymiai

Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, kuris viršija darbo kiekį, kuris buvo paimtas ir rezervuotas pardavimo užsakymui.

Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:

> Kiekis, kurį bandote atnaujinti, viršija gautą / pristatytą kiekį.

Todėl negalite sugeneruoti krovinio važtaraščio.

## <a name="cause"></a>Priežastis

Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje. Pavyzdžiui, ši problema gali kilti, jei krovinio eilutės kiekis, sukurto darbo kiekis arba paimtas kiekis nėra tikslus.

## <a name="resolution"></a>Sprendimas

Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.
- Pakoreguokite krovinio eilutės kiekį.
- Atšaukite visas paėmimo registracijas ir perdarykite paėmimą.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka

Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, kuriam nepavyksta sugeneruoti siuntimo.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.
1. Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.

### <a name="adjust-the-load-line-quantity"></a>Krovinio eilutės kiekio koregavimas

Norėdami pakoreguoti krovinio eilutės kiekį, naudokite nurodytą procedūrą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. Veiksmų srities skirtuko Siuntimas **ir Gauti** grupėje Atšaukimas pasirinkite Atšaukti **siuntos** **patvirtinimą**.
1. Skirtuke **Krovinio** eilutės pasirinkite prekės, kuri lemia išdavimą, krovinio eilutę.
1. Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.
1. Nustatykite **Sumažinti krovinio eilutę** lauką, kad koregavimai atsispindėtų krovinio eilutėje.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Atšaukite visas paėmimo registracijas ir perdarykite paėmimą

Jei kas nors panaudojo paėmimo registraciją krovinio eilutei uždaryti be darbo, gali atsirasti neatitikimas tarp krovinio eilutės kiekio ir paimto kiekio. Tokiu atveju rankinio paėmimo registravimas turi būti atšauktas, o paėmimas turi būti baigtas naudojant „Warehouse Management Mobile App”.

Norėdami atšaukti paėmimo registravimą, naudokite toliau pateiktą procedūrą.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi užsakymai**.
1. Pasirinkite pardavimo užsakymą, kuriam negalite registruoti krovinio važtaraščio.
1. Skirtuke **Pardavimo užsakymo eilutės pasirinkite pardavimo užsakymo** eilutę, kurios išrinkimo registracija buvo atlikta.
1. Pasirinkite **Atnaujinti eilutę \> Paėmimas**, jei norite atsisakyti prekių paėmimo.
