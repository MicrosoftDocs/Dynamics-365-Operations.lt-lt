---
title: Faktiškai atnaujinamo kiekio dešimtainis apvalinimas yra neteisingas
description: Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, neatitinkantis vienete apibrėžto dešimtainio tikslumo.
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726566"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Faktiškai atnaujinamo kiekio dešimtainis apvalinimas yra neteisingas

Klaidos kodas: SYS19589

## <a name="symptoms"></a>Požymiai

Kai generuojate važtaraštį, siunčiamame krovinyje yra kiekis, neatitinkantis vienete apibrėžto dešimtainio tikslumo.

Kai bandote sukurti važtaraštį, sistema rodo šį klaidos pranešimą:

> Neteisingas faktiškai atnaujinamo kiekio, išreikšto vienetu %1, dešimtainis apvalinimas.

Todėl negalite sugeneruoti krovinio važtaraščio.

## <a name="cause"></a>Priežastis

Sistema įvertina, ar siuntimo kiekio dešimtainis apvalinimas atitinka dešimtainį tikslumą, apibrėžtą siuntimo vienetui. Kai sistema suapvalina siuntimo kiekį iki nurodyto dešimtainio kablelio skaičiaus, jeigu ji nustato, kad suapvalintas siuntimo kiekis neatitinka faktinio siuntimo kiekio, važtaraščio sugeneruoti negalite. Pavyzdžiui, ši problema gali kilti, jei pardavimo kiekis yra 1,75 kilogramo (kg), bet dešimtainis tikslumas nustatytas į *1*.

## <a name="resolution"></a>Sprendimas

Krovinys arba siunta šiuo metu yra tokioje būsenoje, kad nepavyksta važtaraščio generavimas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be dešimtainių skaičių ir kitų apvalinimo problemų.
- Peržiūrėkite krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad vienetas ir kiekis yra sulygiuoti dešimtainiu vieneto tikslumu.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Peržiūrėkite savo krovinio eilutes ir atlikite koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be dešimtainių skaičių ir kitų apvalinimo problemų

Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte savo krovinio eilutes ir atliktumėte koregavimus, siekiant užtikrinti, kad kiekis gali būti sukonvertuotas be dešimtainių skaičių ir kitų apvalinimo problemų.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, pagal kurį negalima sugeneruoti važtaraščio.
1. Veiksmų srities skirtuke  **Siųsti ir gauti**, grupėje  **Atšaukti** pasirinkite  **Atšaukti siuntos patvirtinimą**.
1. Skirtuke  **Krovinio eilutės** pasirinkite prekės, sukeliančios problemą, krovinio eilutę.
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
