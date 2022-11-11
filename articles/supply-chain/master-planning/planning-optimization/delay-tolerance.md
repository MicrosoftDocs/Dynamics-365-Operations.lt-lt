---
title: Leistinas uždelsimo nuokrypis (neigiamos dienos)
description: Šiame straipsnyje pateikiama informacija apie leidžiamo delsos nuokrypio skaičiavimą ir apie tai, kaip jis veikia suplanuoto užsakymo kūrimą planavimo optimizavime.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 78ba4236705f1a200d9fe796eb80d0241b0fa537
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740474"
---
# <a name="delay-tolerance-negative-days"></a>Leistinas uždelsimo nuokrypis (neigiamos dienos)
<!-- KFM: Split topic into PO and classic -->

[!include [banner](../../includes/banner.md)]

Leidžiamo vėlavimo funkcija įgalina **planavimo** optimizavimą atsižvelgti į neigiamų dienų vertę, nustatytą padengimo grupėms, prekių padengimui ir ( arba) visiems planams. Ji naudojama norint pratęsti leistino uždelsimo nuokrypio laikotarpį, taikomą bendrojo planavimo metu. Tokiu būdu galite išvengti naujų tiekimo užsakymų kūrimo, jei po trumpo vėlavimo esamas tiekimas galės padengti poreikį. Funkcijos paskirtis – nustatyti, ar apsimoka kurti naują konkrečios paklausos tiekimo užsakymą.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Įjungti arba išjungti leidžiamo delsos nuokrypio funkcijas

Jei norite, kad jūsų sistemoje būtų galima naudoti atidėjimo leistino nuokrypio funkcijas, [eikite](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) į Funkcijų valdymą ir įjunkite šias funkcijas:

- *Neigiamos planavimo optimizavimo dienos* – ši funkcija leidžia padengimo grupių ir prekių padengimo neigiamų dienų parametrus. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima.
- *Gamybos pagal užsakymą tiekimo automatizavimas* – ši funkcija įgalina neigiamų dienų nustatymus pagrindiniuose planuose. (Daugiau informacijos žr. [Gamybos pagal užsakymą tiekimo automatizavimas](../make-to-order-supply-automation.md).)

## <a name="delay-tolerance-in-planning-optimization"></a>Leidžiamas atidėjimas Planavimo optimizavime

Leistinas uždelsimo nuokrypis nurodo dienų skaičių po gamybos laiko, kurį galite laukti prieš užsakę naują papildymą, kai esamas tiekimas jau yra suplanuotas. Leistinas uždelsimo nuokrypis apibrėžiamas naudojant kalendorines, o ne darbo dienas.

Bendrojo planavimo metu, kai sistema apskaičiuoja leistiną uždelsimo nuokrypį, atsižvelgiama į **Neigiamų dienų** nustatymą. Galite nustatyti neigiamų **dienų vertę** padengimo **grupių puslapyje**, prekių padengimo **puslapyje** arba bendrojo **planų** puslapyje. Jei neigiamos dienos priskiriamos daugiau nei viename lygyje, sistema taiko šią hierarchiją, kad nuspręstų, kurį parametrą naudoti:

- Jei bendrojo plano puslapyje įgalintos neigiamos **dienos**, šis parametras panaikina visus kitus neigiamus dienų nustatymus, kai vykdomas planas.
- Jei neigiamos dienos yra sukonfigūruotos prekių padengimo **puslapyje**, šis parametras panaikina padengimo grupės nustatymus.
- Neigiamos dienos, kurios sukonfigūruotos padengimo **grupių** puslapyje, taikomos tik tada, jei atitinkamos prekės arba plano neigiamos dienos nebuvo sukonfigūruotos.

Sistema susieja atidėjimo nuokrypio skaičiavimą su *anksčiausia papildymo data*, kuri yra lygi šiandienos datai pridėjus gamybos laiką. Leistinas uždelsimo nuokrypis apskaičiuojamas naudojant šią formulę *, kur max()* suranda didesnę iš dviejų verčių:

*maks(Anksčiausia papildymo data, Poreikio terminas)* – *Poreikio terminas* + *Neigiamos dienos*

Ši formulė užtikrina, kad bendrasis planavimas nekuria naujų tiekimo užsakymų, kai tiekimas yra pakankamas produkto gamybos laiku.

> [!NOTE]
> Planavimo optimizavimo leidžiamo delsos nuokrypio skaičiavimas visada naudoja dinaminį neigiamų dienų skaičiavimą iš pasenusio bendrojo planavimo modulio. Parametras **Naudoti dinamines neigiamas dienas** puslapyje **Bendrojo planavimo parametrai** neturi įtakos šiai elgsenai.

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
