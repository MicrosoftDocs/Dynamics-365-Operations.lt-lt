---
title: Vietos šablone neleidžiamos neigiamos atsargos, bet leidžiamos neigiamos turimos atsargos
description: Vietos šablone nustatyta parinktis Leisti neigiamas atsargas yra nustatyta kaip Ne, bet sistema vis dar leidžia neigiamas turimų atsargų atsargas.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742613"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Vietos šablone neleidžiamos neigiamos atsargos, bet leidžiamos neigiamos turimos atsargos

KB numeris: 4613622

## <a name="symptoms"></a>Požymiai

Vietos šablone nustatyta parinktis **Leisti neigiamas atsargas** yra nustatyta kaip *Ne*, bet sistema vis dar leidžia neigiamas turimų atsargų atsargas.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Vyriausybės reguliuojamų operacijų sistema turi turėti galimybę įrašyti neigiamas atsargas į rezervuoti nuostolius. Norite, kad prekė galėtų rodyti neigiamas atsargas, bet tik tam skirtose vietose, pvz., talpyklose. Tačiau, jei prekių modelių grupė leidžia neigiamas atsargas, reikia išsiaiškinti, ar nustatyta vieta leidžia neigiamas atsargas. Jei prekė nustatyta taip, kad neigiamos atsargos neleidžiamos, nesvarbu, kaip nustatytas vietos šablonas.

## <a name="resolution"></a>Skiriamoji geba

Neigiamas **atsargų parametras Leisti** iš vietos šablono taikomas tik sandėlio procesams, pvz., paėmimui. Tačiau prekių modelių grupės, kurios nustatytos leisti neigiamas atsargas, paveikia visus atsargų valdymo ir sandėlio valdymo modulių procesus, o vietos šablonas nepaiso parametro.

Galite kontroliuoti, ar sandėlyje gali būti neigiamos atsargos. Nustatykite savo prekių modelių grupes taip, kad jų neigiamos faktinės atsargos būtų neleidžiamos, ir nustatykite, kad neigiamos atsargos būtų leidžiamos tik susijusiuose sandėliuose.
