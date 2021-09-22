---
title: Negalima įterpti aktyvios KS ir maršruto numerių versijos
description: Jei numatytas saitas ir sandėlis jau yra nustatyti pasirinktam produktui, nebūsite paskatinti įvesti aktyvią KS versiją ir maršruto numerius.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477045"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Kuriant naują gamybos užsakymą negalima įterpti KS ir maršruto

## <a name="symptoms"></a>Požymiai

Jums sukūrus naują gamybos užsakymą ir įvedus prekės numerį, **Vietos** ir **Sandėlio** laukeliai yra automatiškai nustatyti į numatytąją vietą ir sandėlį, kurie yra nurodyti **Numatytojo užsakymo nustatymų** puslapyje baigtų prekių vienetui. Be to, automatiškai įvedamas aktyvus KS numeris ir maršruto numeris, todėl negaunate šio pranešimo, kuriame raginama nurodyti šias vertes:

> Įvesti galiojančią važtaraščio versiją ir maršrutą?

## <a name="resolution"></a>Sprendimas

Nesate skatinamas įvesti BOM ir maršruto skaičius, jei pasirenkate produktą, kurio vieta ir sandėlis yra jau nustatyti **Numatytieji užsakymo nustatymai** puslapyje. Esate skatinamas tik, jei šios vertės nėra nustatytos pasirinktam produktui.
