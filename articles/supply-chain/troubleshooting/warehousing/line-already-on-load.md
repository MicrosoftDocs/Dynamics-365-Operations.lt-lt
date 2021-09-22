---
title: Viena iš eilučių jau yra krovinyje
description: 'Šiame puslapyje paaiškinama, kodėl gavote klaidą: „Viena iš eilučių jau yra krovinyje. Nepavyko išleisti į sandėlį" ir kaip išspręsti problemą.'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477142"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Viena iš eilučių jau yra krovinyje

## <a name="symptoms"></a>Požymiai

Dirbdami su pakrovimo kūrimais ir siuntimais, galite gauti tokį klaidos pranešimą:

> Viena iš eilučių jau yra krovinyje. Negali išleisti į sandėlį.

Jei rankiniu būdu sukuriate krovinius arba jei nustatote procesą taip, kad kroviniai jau sukuriami prieš prekybos užsakymo eilutės objektą, prielaida yra tokia, kad tolesnis išleidimas bus atliktas rankiniu būdu ir kad maršrutas bei kainos iš krovinio bus naudojamos.

Kitu galimu scenarijumi, bandote atlikti automatinį paleidimą į sandėlį, tačiau bangos procesui nepavyko sukurti darbą. Dėl to, atviras siuntimas ar krovinys vis dar yra sukurtas. Šis atviras siuntimas arba krovinys tuomet užblokuoja vėlesnius bandymus automatiškai paleisti užsakymą iki tol, kol panaikinsite atvirą siuntimą ar krovinį, arba rankiniu būdu iš naujo apdorosite bangą.

## <a name="resolution"></a>Sprendimas

Galite išleisti iš prekybos užsakymo puslapio ar automatinis paleidimas gali būti atliktas iš išleidimo prekybos užsakymo puslapio tik jei nėra jokio krovinio prieš išleidimą į sandėlį. Krovinys bus sukuriamas automatiniu būdu po bangos apdorojimo.
