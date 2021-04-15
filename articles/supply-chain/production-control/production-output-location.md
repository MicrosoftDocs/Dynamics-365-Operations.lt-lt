---
title: Gamybos išeigos vieta
description: Šioje temoje aprašoma hierarchija, naudojama gamybos išeigos vietai nustatyti.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48b68c36718fa42b7f80e3ffe1f54b7efbbee8bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814637"
---
# <a name="production-output-location"></a>Gamybos išeigos vieta

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma hierarchija, naudojama gamybos išeigos vietai nustatyti.

Gamybos išeigos vieta yra vieta, kurioje baigta prekė saugoma ją pagaminus. Paprastai ši vieta yra netoli baigtos prekės gamybos proceso vietos. Gamybos išeigos vieta naudojama kaip tarpinė medžiagos saugykla prieš ją perkeliant į siuntimo zoną, saugojimo vietą, proceso pabaigos gamybos proceso gamybos įvesties vietą ir t. t. 

Numatytoji gamybos išeigos vieta nustatoma, kai baigtos prekės užregistruojamos gamybos užsakyme arba paketiniame užsakyme. Toliau nurodyta hierarchija naudojama šiai išeigos vietai nustatyti.

1. Naudokite išeigos vietą, nurodytą gamybos užsakymo arba paketo užsakymo antraštėje.
2. Jei ten vieta nenurodyta, naudokite išeigos vietą, nustatytą ištekliuje, kurį naudoja vėliausia gamybos maršrute nurodyta operacija.
3. Jei ten vieta nenurodyta, naudokite išeigos vietą, nustatytą išteklių grupėje, kurią naudoja vėliausia gamybos maršrute nurodytos operacijos išteklius.
4. Jei ten vieta nenurodyta, naudokite išeigos vietą, nurodytą gamybos užsakymo nustatytame sandėlyje.

Nurodoma tik produktų, kurie nustatomi naudojant patobulintus sandėlio procesus, numatytoji gamybos išeigos vieta. Kai šio tipo prekė yra paskelbta baigta, sukuriamas tipo **Baigtos prekės atidėtos** arba **Sudėtinis produktas ir šalutinis produktas atidėti** sandėlio darbas. Šio tipo darbe gamybos išeigos vieta naudojama kaip paėmimo vieta. Atidėjimo vieta nustatoma pagal vietos nurodymus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]