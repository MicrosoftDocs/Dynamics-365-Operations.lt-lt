---
title: Nuomos registravimo tipai
description: Šioje temoje aprašomi registravimo tipai, naudojami turto nuomos operacijose.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b79b02f7e241783d19a315ccff5bb6874a238c38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995423"
---
# <a name="lease-posting-types"></a>Nuomos registravimo tipai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi registravimo tipai, naudojami turto nuomos operacijose.

## <a name="lease-asset"></a>Nuomos turtas

Sąskaita yra susieta su naudojimo teise valdomu (ROU) turtu. Ši sąskaita debetuojama, kai nuoma iš pradžių pripažįstama naujais nuomos apskaitos standartais, Apskaitos standartų kodifikavimu tema Nr. 842 (ASC 842) ir Tarptautinių finansinių ataskaitų standartu Nr. 16 (IFRS 16). Jei nuoma modifikuota, ši sąskaita gali būti debetuojama arba kredituojama, atsižvelgiant į tai, ar modifikavimas padidina, ar sumažina nuomos įsipareigojimą.

**Žurnalo įrašų pavyzdys:** pirminis pripažinimas<br>
**Debetas:** nuomos turtas XXX<br>
**Kreditas:** nuomos įsipareigojimas XXX

## <a name="lease-liability"></a>Nuomos įsipareigojimas

Sąskaita yra susieta su nuomos įsipareigojimu, kuris atsiranda, kai mokėjimai yra diskontuojami naudojant naujus IFRS 16 ir ASC 842 standartus. Ši sąskaita kredituojama, kai nuoma iš pradžių pripažįstama naujais standartais. Ji debetuojama vykdant nuomos mokėjimus ir kredituojama kaupiant palūkanas.

**Žurnalo įrašų pavyzdys:** pirminis pripažinimas<br>
**Debetas:** nuomos turtas XXX<br>
**Kreditas:** nuomos įsipareigojimas XXX

**Žurnalo įrašų pavyzdys:** palūkanų kaupimas<br>
**Debetas:** palūkanų sąnaudos XXX<br>
**Kreditas:** nuomos įsipareigojimas XXX

**Žurnalo įrašų pavyzdys:** nuomos mokestis<br>
**Debetas:** nuomos įsipareigojimas XXX<br>
**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX

## <a name="short-term-lease-liability"></a>Trumpalaikis nuomos įsipareigojimas

Sąskaita yra susieta su trumpalaikiu nuomos įsipareigojimu, kai užregistruojamas trumpalaikis nuomos įsipareigojimų perklasifikavimo žurnalo įrašas. Ši sąskaita kredituojama už trumpalaikį įsipareigojimą iš amortizacijos grafiko paskutinę mėnesio dieną. Tačiau ta pati suma debetuojama kito mėnesio pirmąją dieną.

**Žurnalo įrašų pavyzdys:** trumpalaikis nuomos įsipareigojimų perklasifikavimas<br>
**Debetas:** nuomos įsipareigojimas XXX<br>
**Kreditas:** trumpalaikis nuomos įsipareigojimas XXX<br>
**Debetas:** trumpalaikis nuomos įsipareigojimas XXX<br>
**Kreditas:** nuomos įsipareigojimas XXX

## <a name="depreciation-expense"></a>Likvidavimo išlaidos

Sąskaita yra susieta su išlaidomis, susijusiomis su naudojimo teise valdomo turto nusidėvėjimu pagal IFRS 16, ASC 842 bei finansine nuoma pagal IAS 17 ir ASC 840. Ši sąskaita debetuojama, kai naudojimo teise valdomas turtas nusidėvi kiekvieną mėnesį.

**Žurnalo įrašų pavyzdys:** nusidėvėjimo kaupimas<br>
**Debetas:** nusidėvėjimo išlaidos XXX<br>
**Kreditas:** sukauptas nusidėvėjimas XXX

## <a name="gainloss-on-lease-modification"></a>Nuomos modifikavimo pelnas / nuostolis

Sąskaita yra susieta su bet kokiu pelnu ar nuostoliu, atsirandančiu dėl nuomos pakeitimų. Pelnas gali kilti dėl nuomos modifikacijos, jei modifikavus nuomos įsipareigojimas sumažėja suma, viršijančia naudojimo teise valdomo turto balansinę vertę.

Pavyzdžiui, dabartinė nuomos įsipareigojimo balansinė vertė yra 150 000 USD, o naudojimo teise valdomo turto balansinė vertė yra 100 000 USD. Nuomos sutartis keičiama, o šis pakeitimas sukuria naują dabartinę būsimų minimalių nuomos mokesčių (PVFMLP) vertę – 40 000 USD. Todėl nuomos įsipareigojimas bus debetuojamas – 110 000 USD (150 000 USD – 40 000 USD). Kadangi naudojimo teise valdomas turtas yra tik 100 000 USD, 110 000 USD sumažinimas sumažins turto vertę į mažiau nei 0 (nulį). Todėl apskaitos rekomendacijose nurodyta, kad likutis turi būti užsakytas į pelno sąskaitą. Šiuo atveju galutinis žurnalo įrašas bus 110 000 USD nuomos įsipareigojimo debetas, 100 000 USD nuomos turto kreditas ir 10 000 USD kreditas į pelno sąskaitą.

**Žurnalo įrašų pavyzdys:** nuomos modifikavimas<br>
**Debetas:** nuomos įsipareigojimas XXX<br>
**Kreditas:** nuomos turtas XXX<br>
**Kreditas:** pelnas XXX

## <a name="accumulated-depreciation"></a>Sukauptas nusidėvėjimas

Sąskaita yra susieta su naudojimo teise valdomo turto priešpriešine turto sąskaita. Sąskaita kredituojama, kai užregistruojamos nusidėvėjimo išlaidos.

**Žurnalo įrašų pavyzdys:** nusidėvėjimo kaupimas<br>
**Debetas:** nusidėvėjimo išlaidos XXX<br>
**Kreditas:** sukauptas nusidėvėjimas XXX

## <a name="retained-earnings"></a>Nepaskirstytas pelnas

Sąskaita yra susieta su išsaugotomis pajamomis. Ši sąskaita gali būti debetuota arba kredituota į perkėlimo koregavimo žurnalo įrašą, naudojant visos retrospektyvos metodą arba kaupiamąjį atgalinės datos parinkties A metodą. Skirtumo tarp pradinio naudojimo teise valdomo turto ir noro uostos įsipareigojimo suma rezervuojama kaip išaugotos pajamos. Retais atvejais nepaskirstytas pelnas taip pat gali būti paveiktas atliekant nuomos modifikaciją, jei nuomos klasifikacija pasikeičia iš finansų į veiklos, kad būtų galima padidinti arba sumažinti naudojimo teise valdomo turto vertę ir prilyginti nuomos įsipareigojimui.

**Žurnalo įrašų pavyzdžiai:** perkėlimo koregavimas (visos retrospektyvos arba kaupiamasis atgalinės datos parinkties A metodas)<br>
**Debetas:** nuomos įsipareigojimas XXX<br>
**Kreditas:** nuomos turtas XXX<br>
**Kreditas:** išsaugotos pajamos XXX

## <a name="variable-payment"></a>Kintamas mokėjimas

Sąskaita yra susieta su kintamaisiais nuomos mokėjimais, kuriuos sukuria indekso perkainojimas pagal ASC 842, ASC 840 ir IAS 17 nuomos sutartis. Nuomos mokėjimo grafike kintamieji mokėjimai įtraukiami į stulpelį **Kintamieji mokėjimai**. Ši sąskaita debetuojama, kai SF kuriama pagal mokėjimo grafiko eilutę, kurioje yra kintamasis mokėjimas.

**Žurnalo įrašų pavyzdys:** nuomos mokestis<br>
**Debetas:** nuomos įsipareigojimas XXX<br>
**Debetas:** kintamasis mokėjimas XXX<br>
**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX

## <a name="deferred-rent-asset-liability"></a>Atidėtojo nuomos mokėjimo turtas (įsipareigojimas)

Sąskaita yra susieta su atidėtojo nuomos mokėjimo turtu arba įsipareigojimu, kurį sukuria atidėtųjų nuomos mokėjimų apdorojimo nuoma. Ši sąskaita debetuojama, kai SF užregistruojama pagal atidėtojo nuomos mokėjimo apdorojimo nuomą, jei nuomos mokesčio suma yra didesnė nei laikotarpio tiesinės nuomos išlaidos. Ji kredituojama, jei nuomos mokestis yra mažesnis už laikotarpio tiesines nuomos išlaidas.

**Žurnalo įrašų pavyzdžiai:** nuomos mokestis (atidėtojo nuomos mokėjimo apdorojimo nuoma)<br>
**Debetas:** nuomos išlaidos XXX<br>
**Kreditas:** atidėtojo nuomos mokėjimo įsipareigojimas XXX<br>
**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX

## <a name="lease-expense"></a>Nuomos išlaidos

Sąskaita yra susieta su nuomos išlaidomis, jei nuoma klasifikuojama kaip atidėtojo nuomos mokėjimo apdorojimo nuoma. Ši sąskaita debetuojama, kai SF užregistruojama pagal atidėtojo nuomos mokėjimo apdorojimo nuomą.

**Žurnalo įrašų pavyzdžiai:** nuomos mokestis (atidėtojo nuomos mokėjimo apdorojimo nuoma)<br>
**Debetas:** nuomos išlaidos XXX<br>
**Kreditas:** atidėtojo nuomos mokėjimo įsipareigojimas XXX<br>
**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX

## <a name="impairment-expense"></a>Nuvertėjimo išlaidos

Sąskaita užregistruojama, kai nuoma nuvertėja. Ši sąskaita debetuojama, o naudojimo teise valdomo turto sąskaita tiesiogiai kredituojama.

**Žurnalo įrašų pavyzdys:** nuomos mokestis<br>
**Debetas:** nuvertėjimo išlaidos XXX<br>
**Kreditas:** naudojimo teise valdomas turtas XXX

## <a name="lease-payment"></a>Nuomos mokestis

Sąskaita užregistruojama, jei parametras **Mokėti tiekėjui** yra išjungtas. Ši sąskaita kredituojama vietoj tiekėjo mokėtinos sumos, jei parametras išjungtas.

**Žurnalo įrašų pavyzdys:** nuomos mokestis<br>
**Debetas:** nuomos įsipareigojimas XXX<br>
**Kreditas:** nuomos mokestis XXX

## <a name="expense-type-postings"></a>Išlaidų tipo registravimas

Sąskaita, kuri pasirenkama kiekvienam išlaidų tipui, debetuojama, kai sugeneruojamas išlaidų tipo mokėjimas. Pavyzdžiui, nurodyta išlaidų tipo **Draudimas** sąskaita debetuojama kiekvieną kartą, kai SF arba mokėjimo žurnalo įrašas sukuriamas iš eksploatavimo išlaidų grafiko, skirto draudimo išlaidoms.

**Žurnalo įrašų pavyzdys:** draudimo mokestis<br>
**Debetas:** draudimo išlaidų tipo sąskaita XXX<br>
**Kreditas:** korespondentinė sąskaita XXX

> [!NOTE]
> Korespondentinė sąskaita pasirenkama nuomos lygyje eilutėse, skirtose eksploatavimo išlaidų mokėjimo grafikui. Ši korespondentinė sąskaita gali būti susieta su tiekėju arba su DK sąskaita.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]