---
title: Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų
description: Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756708"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų

Klaidos kodai: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų %1. Paleiskite sandėlio krovinio svorio vientisumo tikrinkite, ar norite perskaičiuoti svorio laukus.

## <a name="cause"></a>Priežastis

**Grynasis svoris** ir **Taros svoris** laukeliai yra nustatyti į *0* (nulį) pakrovimo eilutėje. Tačiau produkto svorio matavimo svorio laukai *nėra* nustatomi kaip 0. Jei krovinio eilutėje nėra nustatyti svorio laukai, bet kokie kiekio koregavimai krovinio eilutėje gali svorio skaičiavimą atlikti neteisingai. Ši problema gali kilti, jei sukūrus krovinio eilutę produkto svoris buvo pakeistas.

## <a name="resolution"></a>Skiriamoji geba

Pagal numatytuosius nustatymus, kai sukuriama krovinio eilutė, į ją įvedami produkto svorio laukai. Jei svoris lygus nuliui, galite jį perskaičiuoti naudodami sandėlio *krovinio svorio vientisumo* tikrinimo funkciją.

1. Eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenš bazę \> Periodinis tikrinimas**.
1. Žymės **langelyje** Vientisumas nustatykite **modulio** lauką kaip *Sandėlio* valdymas.
1. Nustatykite **Tikrinti/Taisyti** laukelį į *Taisyti klaidą*.
1. Žymės langelyje pažymėkite žymės langelį Sandėlio krovinio svorio nuoseklumas ir įsitikinkite, kad pažymėtas **tik** šio žymės langelio eilutė.
1. Žymės langelio sąrašo viršuje pasirinkite elipsės mygtuką (... ), tada **meniu** pasirinkite **Tekstas**.
1. Sandėlio **krovinio svorio vientisumo žymės lange nustatykite šiuos laukus, norėdami nurodyti kriterijus, pagal** kuriuos turėtų būti vykdomas vientisumo tikrinimas:

    - **Krovinio ID:** nurodykite krovinio ID. Palikite šį tuščią, jei norite patikrinti visus krovinio ID.
    - **Prekės numeris:** nurodykite prekės numerį. Palikite šį tuščią, jei norite patikrinti visas prekes.
    - **Visada perskaičiuoti krovinio svorį:** nustatykite šią parinktį *kaip* Taip.
    - **Leisti perrašyti svorį krovinio eilutėse:** nustatykite šią parinktį *kaip* Taip.

1. Pasirinkite **Gerai,** kad uždarytumėte žymės langelį **Sandėlio krovinio svorio** vientisumas.
1. Pasirinkite elipsės mygtuką, tada **meniu** pasirinkite Vykdyti.

Svoris perskaičiuojamas pagal jūsų nurodytus kriterijus. Pasirinkti saitą **Pranešimo** informacija, kad būtų galima peržiūrėti vientisumo tikrinimo rezultatus.
