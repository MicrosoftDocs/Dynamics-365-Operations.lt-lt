---
title: Sinchronizavimas su „Supply Chain Management“ kainodaros mechanizmu pareikalavus
description: Šioje temoje aprašoma, kaip naudoti "Microsoft Dynamics 365 Supply Chain Management Microsoft Dynamics " iš "365" pardavimo kainų nustatymo modulį.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6b0cc8f403be866ff00b89a33f6c59089c987bb0
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402835"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Sinchronizavimas su „Supply Chain Management“ kainodaros mechanizmu pareikalavus

[!include [banner](../../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management” apima kainodaros mechanizmą, kuris tvarko prekybos sutartis, kainoraščius, kliento lojalumo programas, akcijas ir nuolaidas. Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą. Kai naudojate dvigubo rašymo kainą, **·** **naudojate** statinę kainodarą arba tiekimo grandinės valdymo kainodaros Microsoft Dynamics sistemą pasiūlymo ir užsakymo puslapiuose, 365 pardavimo puslapiuose.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Kainodaros mechanizmo iš „Supply Chain Management”, esančio „Sales“ programoje, naudojimas

1. Programoje „Sales“ eikite į **Pardavimas \>Užsakymai**.
1. Norėdami sukurti užsakymą pasirinkite **Naujas** arba sąraše **Mano užsakymai** pasirinkite esamą užsakymą.
1. Įtraukite naują užsakymo eilutę.
1. Jei kuriate naują užsakymą, veiksmų **srityje pasirinkite** Kainos užsakymas. Jei atnaujinate esamą užsakymą, veiksmų srityje pasirinkite **Perskaičiuoti**.
1. Automatiškai užpildomi šie stulpeliai:

    - Išsami suma
    - Nuolaida %
    - Nuolaida
    - Suma be transportavimo mokesčio
    - Suma su transportavimo mokesčiu
    - Bendra mokesčio suma
    - Iš viso

> [!NOTE]
> Panašus procesas taikomas kuriant pasiūlymus.

## <a name="how-it-works"></a>Kaip tai veikia

Kai sukuriate pardavimo užsakymą, šis užsakymas nedelsiant sinchronizuojamas su tiekimo grandinės valdymu naudojant vertes, kurias įvedėte į Pardavimą. Kai **pasirenkate** **pardavimo** kainos užsakymą arba kainos pasiūlymą, tiekimo grandinės valdymas apskaičiuoja kiekvienos užsakymo eilutės kainą ir bendrą užsakymą, paremtą prekybos sutarties taisyklėmis, apibrėžtomis Tiekimo grandinės valdymas. Tada naujos apskaičiuotos vertės sinchronizuojamos atgal į Pardavimą.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Nustatykite prekybos sutarties vertinimo parinktis tiekimo grandinės valdymo dalyje

Tiekimo grandinės valdymą galite konfigūruoti taip, kad jis neatsižvelgtų į arba nepaisytų prekybos sutarčių, kai skaičiuoja pardavimo metu sukurto užsakymo kainą. Norėdami nustatyti šią pasirinktį, atlikite šiuos veiksmus.

1. Prisiregistruokite savo tiekimo grandinės valdymo aplinkoje.
1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
1. Skirtuke **Kainos** skirtuke Prekybos **sutarties** įvertinimo "FastTab **" pridėkite arba pašalinkite eilutę neautomatinio įrašo** strategijai, jei to reikia. Šios strategijos buvimo ar neatvykimo valdymas ar tiekimo grandinės valdymo kainodaros sistema automatiškai nepaisys pardavimo kainos, kuri buvo įvesta į Pardavimą.

    - Jei Prekybos **sutarties** vertinimo *nustatyme nėra* neautomatinio **įrašo** strategijos, tiekimo grandinės valdymas yra pagrindinė kaina. Kai vartotojas pardavimo veiksmų srityje pasirenka kainos užsakymą arba kainos pasiūlymą, iškvie įvedamas tiekimo grandinės valdymo **kainodaros** **mechanizmas** ir pardavimo kaina, įvesta pardavimo kaina perrašoma, nebent ji lygi pardavimo kainai, apskaičiuotai tiekimo grandinės valdymo sistemoje.
    - Jei Prekybos **sutarties** įvertinimo *nustatyme* yra neautomatinio **įrašo** strategija, pardavimas yra pagrindinis kainos kodas. Pardavimo kaina, įvesta **į** **pardavimą**, negali būti automatiškai perrašyta, kai vartotojas pardavimo veiksmų srityje pasirenka kainos užsakymą arba kainos pasiūlymą.
    - Užsakymo eilutės ir pasiūlymo eilutės, **kurių** vieneto kaina ir/**·** *arba nuolaidos vertė pardavimo metu yra 0* (nulis), laikomos specialiu atveju. Jei yra tinkama prekybos sutarties kaina, tiekimo grandinės valdymas visada *bus* taikomas šiems laukams, nepaisant **prekybos sutarties įvertinimo** nustatymo.

    Kaip pavyzdį peržiūrėkite kiekvieno iš šių atvejų atvejus.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>1 pavyzdis scenarijus: Prekybos sutarties vertinimas be pasirinkties Įvesti rankiniu būdu

Šiame scenarijuje Prekybos **sutarties įvertinimo nustatymas** tiekimo grandinės valdymo dalyje *neapima* įvedimo **rankiniu būdu** strategijos. Pardavimo vartotojas įveda užsakymo eilutę, kurios pardavimo kaina nėra lygi nuliui, o tiekimo grandinės valdymo elementui nėra nurodyta jokia pardavimo kaina.

1. Pardavimo metu vartotojas sukuria užsakymo eilutę, kurios vieneto **kaina yra** 1 JAV doleris (USD).
1. Užsakymo eilutė sinchronizuojama su tiekimo grandinės valdymu, kai pardavimo kaina 1 USD.
1. Dalyje Pardavimas vartotojas veiksmų **srityje** pasirenka Kainos užsakymą.
1. Tiekimo grandinės valdymas ieško atitinkamų kainų ir nuolaidų, tada apskaičiuoja bendras sumas. Kadangi tiekimo grandinės valdymą prekė neturi pardavimo kainos, skaičiavimas atnaujina eilutę taip, kad jos pardavimo kaina būtų 0 USD.
1. Nauja eilutės pardavimo kaina sinchronizuojama atgal su Pardavimu.
1. Rezultatas yra pardavimo užsakymo eilutė, kurios pardavimo kaina – 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>2 pavyzdis scenarijus: Prekybos sutarties vertinimas naudojant parinktį Įvesti rankiniu būdu

Šiame scenarijuje Prekybos **sutarties įvertinimo nustatymas tiekimo** grandinės valdymo dalyje *apima* neautomatinio **įrašo** strategiją. Pardavimo vartotojas įveda užsakymo eilutę, kurios pardavimo kaina nėra nulinė, pardavimas. Tiekimo grandinės valdymas apima prekybos sutartį, pagal kurią nustatoma 2 USD prekės pardavimo kaina.

1. Pardavimo metu vartotojas sukuria prekės, kurios vieneto kaina yra 1 **USD**.
1. Užsakymo eilutė sinchronizuojama su tiekimo grandinės valdymu, kai pardavimo kaina 1 USD.
1. Dalyje Pardavimas vartotojas veiksmų **srityje** pasirenka Kainos užsakymą.
1. Tiekimo grandinės **valdymo prekybos** **sutarties** įvertinimo nustatymas apima neautomatinę įrašo strategiją, todėl pardavimo kaina nepasikeičia, nors taikoma prekybos sutartis nurodo kitą pardavimo kainą.
1. Pardavimo kaina nekinta pardavimo ir tiekimo grandinės valdymo metu.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>3 pavyzdinis scenarijus: prekės, kurios pardavimo kaina pardavimo kaina pardavimo lauke yra nulis, vertinimas

Šiame scenarijuje Prekybos **sutarties įvertinimo nustatymas tiekimo** grandinės valdymo dalyje *apima* neautomatinio **įrašo** strategiją. Pardavimo vartotojas pardavimo eilutėje įveda užsakymo eilutę, kurios pardavimo kaina pardavimo kaina lygi 0 (nuliui). Tiekimo grandinės valdymas apima prekybos sutartį, pagal kurią nustatoma 2 USD prekės pardavimo kaina.

1. Pardavimo metu vartotojas sukuria užsakymo **eilutę**, kurios vieneto vertė yra 0 USD **, o eilutės nuolaidos** vertė – 0 USD.
1. Užsakymo eilutė sinchronizuojama su tiekimo grandinės valdymu, kai pardavimo kaina 0 USD.
1. Kadangi ji gavo užsakymo eilutę, kurios pardavimo kaina lygi 0 (nuliui), tiekimo grandinės valdymas iškeirauos kainos vadovą, **net** jei įgalinta įrašo rankiniu būdu pasirinktis. Kainų nustatymo variklis grąžina pardavimo kainą prekės2 USD kuri nustatyta prekybos sutartimi, ir atnaujina tiekimo grandinės valdymo užsakymo eilutę.
1. Atnaujinta pardavimo kaina dar nesinchronizuota su pardavimo užsakymo eilute.
1. Dalyje Pardavimas vartotojas veiksmų **srityje** pasirenka Kainos užsakymą.
1. Tiekimo grandinės valdymo užsakymo eilutėje išlaikoma pardavimo kaina 2 USD, kuri sinchronizuojama atgal į pardavimą. Todėl pardavimo **užsakymo eilutės** vieneto vertė kaina atnaujinama iš lauko 0 USD į 2 USD.
1. Pardavimo metu vartotojas įveda naują prekės **eilutės nuolaidos** 0.50 USD. Dabar pardavimas skaičiuoja **, kad eilutės** išplėstinės sumos vertė yra 1.50 USD.
1. Užsakymo eilutė sinchronizuojama su tiekimo grandinės valdymu ir kainos **eilutės** nuolaidos 0.50 USD.
1. Dalyje Pardavimas vartotojas veiksmų **srityje** pasirenka Kainos užsakymą.
1. Pardavimo užsakymo eilutės kainų ar nuolaidų negalima keisti.

## <a name="limitations"></a>Apribojimai

Kai užpildyti „Sales“ stulpeliai, taikomi šie apribojimai:

- „Supply Chain Management” mokesčių ir išlaidų paskirstymo sąranka nėra dubliuojama programoje „Sales“.
- Kainodaroje neatsižvelgiama į specialią mažmeninės prekybos kainodarą, nurodytą l **Mažmeninės prekybos kanalas** stulpelyje, esančiame „Supply Chain Management” pardavimo užsakymo eilutės puslapyje.
- Neatsižvelgiama į nuolaidas, nurodytas „Supply Chain Management” skyriuje **Prekybos nuolaidų valdymas**.
- Kainodara neatsižvelgia į pardavimų sutartis.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
