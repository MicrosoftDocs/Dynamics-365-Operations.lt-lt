---
title: Leistinas uždelsimo nuokrypis (neigiamos dienos)
description: Šioje temoje pateikiama informacija apie leistino uždelsimo nuokrypio skaičiavimą ir apie tai, kaip jis veikia suplanuoto užsakymo kūrimą planavimo optimizavime.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a333048e1c30ab7bdb1b5d4af817cb1561c1212a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468615"
---
# <a name="delay-tolerance-negative-days"></a>Leistinas uždelsimo nuokrypis (neigiamos dienos)

[!include [banner](../../includes/banner.md)]

Leistino uždelsimo nuokrypio funkcija įgalina Planavimo optimizavimą atsižvelgti į **Neigiamų dienų** vertę, nustatytą padengimo grupėms. Ji naudojama norint pratęsti leistino uždelsimo nuokrypio laikotarpį, taikomą bendrojo planavimo metu. Tokiu būdu galite išvengti naujų tiekimo užsakymų kūrimo, jei po trumpo vėlavimo esamas tiekimas galės padengti poreikį. Funkcijos paskirtis – nustatyti, ar apsimoka kurti naują konkrečios paklausos tiekimo užsakymą.

## <a name="turn-on-the-feature-in-your-system"></a>Funkcijos įjungimas sistemoje

Norėdami, kad jūsų sistemoje leistino uždelsimo nuokrypio funkcija būtų galima, eikite į [Funkcijų valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite *Negatyvios dienos Planavimo optimizavimui* funkciją.

## <a name="delay-tolerance-in-planning-optimization"></a>Leidžiamas atidėjimas Planavimo optimizavime

Leistinas uždelsimo nuokrypis nurodo dienų skaičių po gamybos laiko, kurį galite laukti prieš užsakę naują papildymą, kai esamas tiekimas jau yra suplanuotas. Leistinas uždelsimo nuokrypis apibrėžiamas naudojant kalendorines, o ne darbo dienas.

Bendrojo planavimo metu, kai sistema apskaičiuoja leistiną uždelsimo nuokrypį, atsižvelgiama į **Neigiamų dienų** nustatymą. Galite nustatyti **Neigiamų dienų** reikšmę **Padengimo grupių** arba **Prekės padengimo** puslapyje.

Sistema susieja atidėjimo nuokrypio skaičiavimą su *anksčiausia papildymo data*, kuri yra lygi šiandienos datai pridėjus gamybos laiką. Leistinas uždelsimo nuokrypis apskaičiuojamas naudojant šią formulę, kurioje *maks()* suranda didesnę iš dviejų verčių:

*maks(Anksčiausia papildymo data, Poreikio terminas)* – *Poreikio terminas* + *Neigiamos dienos*

Ši formulė užtikrina, kad bendrasis planavimas nekuria naujų tiekimo užsakymų, kai tiekimas yra pakankamas produkto gamybos laiku.

> [!NOTE]
> Leistino uždelsimo nuokrypio skaičiavimas Planavimo optimizavime visada naudoja dinaminį neigiamų dienų skaičiavimą iš įtaisytojo bendrojo planavimo. Parametras **Naudoti dinamines neigiamas dienas** puslapyje **Bendrojo planavimo parametrai** neturi įtakos šiai elgsenai.

Jei esamas tiekimas numano poreikio atidėjimą, kuris yra mažesnis arba lygus apskaičiuotam leistinam uždelsimo nuokrypiui, Planavimo optimizavimas iškviestų esamą tiekimą pagal poreikį. Kai kuriais atvejais geriau atidėti poreikį nei turėti tiekimo perviršį.

Toliau pateikti poskyriai pateikia pavyzdžių, kurie parodo, kaip leistinas uždelsimo nuokrypis paveikia suplanuotų užsakymų kūrimą Planavimo optimizavime.

### <a name="example-1"></a>1 pavyzdys

Produktas turi šią konfigūraciją:

- **Gamybos laikas:** *10*
- **Neigiamos dienos:** *2*

Yra toks produkto tiekimas ir poreikis:

- **Poreikis šiandien:** Pardavimo užsakymas, kurio kiekis yra 10
- **Tiekimas per 12 dienų:** Pirkimo užsakymas, kurio kiekis yra 10

Esamas tiekimas gali padengti poreikį per 12 dienų, o šis laikotarpis yra lygus leistinam uždelsimo nuokrypiui. Todėl, kai vykdomas bendrasis planavimas, nesukuriami jokie suplanuoti užsakymai.

### <a name="example-2"></a>2 pavyzdys

Produktas turi šią konfigūraciją:

- **Gamybos laikas:** *10*
- **Neigiamos dienos:** *0*

Yra toks produkto tiekimas ir poreikis:

- **Poreikis šiandien:** Pardavimo užsakymas, kurio kiekis yra 10
- **Tiekimas per 12 dienų:** Pirkimo užsakymas, kurio kiekis yra 10

Esamas tiekimas gali padengti poreikį tik po 12 dienų. Tačiau leistinas uždelsimo nuokrypis yra 10 dienų. Todėl, kai vykdomas bendrasis planavimas, sukuriamas suplanuotas užsakymas, kurio kiekis yra 10.

### <a name="example-3"></a>3 pavyzdys

Produktas turi šią konfigūraciją:

- **Gamybos laikas:** *10*
- **Neigiamos dienos:** *2*

Yra toks produkto tiekimas ir poreikis:

- **Poreikis per 11 dienų:** Pardavimo užsakymas, kurio kiekis yra 10
- **Tiekimas per 14 dienų:** Pirkimo užsakymas, kurio kiekis yra 10

Esamas tiekimas gali padengti poreikį tik po trijų dienų. Tačiau leistinas uždelsimo nuokrypis yra dvi dienos. Šiuo atveju leistinas uždelsimo nuokrypis apima tik dvi neigiamas dienas. Poreikio data neįtraukiama, nes ji yra pasibaigus produkto gamybos laikui. Todėl, kai vykdomas bendrasis planavimas, sukuriamas suplanuotas užsakymas, kurio kiekis yra 10.
