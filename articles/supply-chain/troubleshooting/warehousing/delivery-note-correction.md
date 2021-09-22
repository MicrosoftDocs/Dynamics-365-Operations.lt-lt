---
title: Pristatymo pažymos koregavimo apdoroti negalima
description: Jei užregistr siuntę mėginsite pataisyti pristatymo pažymą, gausite klaidą. Šiame puslapyje paaiškinama, kaip taisyti užregistruotus WMS įgalintų prekių važtaraščius.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477118"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Pristatymo pažymos koregavimo apdoroti negalima

## <a name="symptoms"></a>Požymiai

Po to, kai publikuojate pristatymo važtaraštį, nebegalite jo atšaukti, nes **Atšaukimo** mygtukas yra neprieinamas. Taip pat, negali koreguoti pristatymo važtaraščio. Jei bandėte, galbūt gausite tolesnį klaidos pranešimą:

> Pristatymo pažymos koregavimo apdoroti negalima. Pristatymo važtaraštyje yra tik prekės, kurias veikia sandėlio valdymo procesai, nes jų nepalaiko pristatymo pažymos koregavimas.

## <a name="resolution"></a>Sprendimas

Siekiant tinkamai publikuoti pakavimo kvitus prekėms, kurios įjungtos išplėstiniam sandėlio valdymui (WMS), privalote publikuoti iš krovinio, o ne tiesiogiai iš užsakymo.
