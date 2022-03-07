---
title: Faktinis likęs kiekis, nurodytas vienetais, negali būti lygus nuliui
description: Kai generuojate važtaraštį, į jį pateikiami duomenys turi ne nulinį atsargų kiekį, bet nulinį pardavimų kiekį.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248794"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Faktinis likęs kiekis, nurodytas vienetais, negali būti lygus nuliui

Klaidos kodas: SYS19591

## <a name="symptoms"></a>Požymiai

Kai generuojate važtaraštį, į jį pateikiami duomenys turi ne nulinį atsargų kiekį, bet nulinį pardavimų kiekį.

Kai bandote sugeneruoti važtaraštį, sistema rodo šį klaidos pranešimą:

> Faktinis likęs kiekis, išreikštas vienetu %1, negali būti lygus nuliui.

Todėl negalite sugeneruoti krovinio važtaraščio.

## <a name="cause"></a>Priežastis

Sistema įvertina faktiškai likusį kiekį atsargų vienetu ir faktiškai likusį kiekį siuntimo vienetu. Jei sistema nustato, kad faktinis likęs kiekis siuntimo vienetu yra 0 (nulis), bet faktinis likęs kiekis atsargų vienetu nėra 0, negalite sugeneruoti važtaraščio. Pavyzdžiui, ši problema gali kilti, jei prekės pardavimo ir atsargų vienetai skiriasi, o konvertavimas tarp vienetų nėra tikslus.

## <a name="resolution"></a>Sprendimas

Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.
- Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be apvalinimo problemų.
- Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.
- Įsitikinkite, kad atsargų matavimo vienetas yra mažesnis nei pardavimų matavimo vienetas.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Peržiūrėkite savo krovinio eilutes ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka

Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.
1. Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be apvalinimo problemų

Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte savo krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be apvalinimo problemų.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.
1. Skirtuke  **Krovinio eilutės** pasirinkite prekės, viršijančios pristatymo perviršį, krovinio eilutę.
1. Pasirinkite **Sumažinti paimtą kiekį**, kad pakoreguotumėte paimtą kiekį.
1. Skirtuke  **Eilutės informacija** pasirinkite **Užsakymas**.
1. Nustatykite **Kiekio** lauką į paimtą kiekį (tai yra, į lauko **Darbo sukurto kiekio** reikšmę), kad būtų galima atlikti važtaraščio generavimą.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu

Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. „FastTab” **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę. Pasižymėkite laukų **Kiekis** ir **Vienetas** reikšmes.
1. Eikite į **Organizacijos administravimas \> Vienetai \> Vienetai**.
1. Pasirinkite vienetą, pagal kurį negalima sugeneruoti važtaraščio.
1. Pakoreguokite lauko **Dešimtainis tikslumas** reikšmę, jei reikia.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Įsitikinkite, kad atsargų matavimo vienetas yra mažesnis nei pardavimų matavimo vienetas

Įsitikinkite, kad atsargų matavimo vienetas yra mažesnis nei pardavimų matavimo vienetas. Jei reikia, apsvarstykite galimybę iš naujo sukonfigūruoti prekės matavimo vienetą.
