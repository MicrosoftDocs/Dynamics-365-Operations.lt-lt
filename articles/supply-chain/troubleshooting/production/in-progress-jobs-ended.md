---
title: Eigos užduotys baigiasi, pranešant apie paskutinės užduoties dalinį kiekį
description: Naudodami darbo kortelės įrenginį siekiant pranešti apie dalinį kiekį paskutiniame darbe gamybos užsakyme visi ankstesni darbai tame užsakyme turi progreso būseną ir automatiškai užbaigiami.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477134"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Eigos užduotys baigiasi, pranešant apie ankstesnės užduoties dalinį kiekį

## <a name="symptoms"></a>Požymiai

Naudodami darbo kortelės įrenginį siekiant pranešti apie dalinį kiekį paskutiniame darbe gamybos užsakyme visi ankstesni darbai tame užsakyme turi progreso būseną ir automatiškai užbaigiami.

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. Puslapyje **Gamybos užsakymo nustatytosios vertės** skirtuke **Pranešti kaip baigtą** yra parinktis pavadinimus **Paskutinės žymos kelias**. Jei ši tema nustatyta į *Taip*, kelio kortelės žurnalas yra viešinamas kaip darbuotojas naudoja darbo kortelės įrenginį ir darbo kortelės terminalą siekiant pranešti apie paskutinę operaciją. Šis žurnalas rodo visas operacijas kaip baigtas ir užbaigia visus gamybos darbus. Kai **Paskutinės žymos kelio** parinktis yra nustatyta į *Taip*, sistema nebeatsižvelgia į darbo būseną, kurią darbuotojas pasirinko jam pranešant apie paskutinę operaciją. Sistema taip pat neatsižvelgia į tai, ar darbuotojas praneša visą ar dalinį kiekį.
