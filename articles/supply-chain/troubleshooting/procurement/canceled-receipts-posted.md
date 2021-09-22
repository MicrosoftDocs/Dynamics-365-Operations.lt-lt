---
title: Perlaidos gali būti publikuojamos į patalpintą DK sąskaitą
description: Jei gavimo dokumentas yra atšauktas, sistema leidžia operacijas užregistruoti laikinai sustabdytose DK sąskaitose, net jei pagrindinės sąskaitos yra sustabdytos
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477140"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Perlaidos gali būti publikuojamos į patalpintą DK sąskaitą

## <a name="symptoms"></a>Požymiai

Jei gavimo dokumentas yra atšauktas, sistema leidžia operacijas užregistruoti laikinai sustabdytose DK sąskaitose, net jei pagrindinės sąskaitos yra sustabdytos.

## <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. **Mokėtinų sumų parametrai** puslapyje, skirtuke **Bendra**, įsitikinkite, kad parinktis **Gavimo dokumentą registruoti DK** nustatyta kaip *Taip*.
1. Sukurkite pirkimo užsakymą ir pridėkite užsakymo eilutę, kurioje yra kiekis lygus *1000* vienam produktui.
1. Patvirtinkite pirkimo užsakymą.
1. Užregistruokite gavimo dokumentą ir patikrinkite kvitus.
1. Sustabdykite atitinkamas pagrindines sąskaitas, *200140* ir *140200*.
1. Atšaukite užregistruotą gavimo dokumentą.
1. Atkreipkite dėmesį, kad operacijos gali būti registruojamos laikinai sustabdytose DK sąskaitose.

## <a name="resolution"></a>Sprendimas

Operacijos gali būti registruojamos laikinai sustabdytose DK sąskaitose, kai atšaukiami gavimo dokumentai, nes toks veikimo būdas leidžia atlikti teisingus registravimus.
