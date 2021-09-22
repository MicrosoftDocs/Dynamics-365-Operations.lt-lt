---
title: Įvertinkite visus „Multi SKU“ vietos nustatymo direktyvų veiksmus
description: Nauja funkcija, buvo įtraukta siekiant įvertinti visus veiksmus kelioms SKU vietos kryptims. Šiame puslapyje pateikta informacija, kaip ją įjungti.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477075"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Keli SKU pasirinktis neįvertina kelių vietos nustatymo veiksmų

## <a name="symptoms"></a>Požymiai

Krypties vietos *Pardavimo užsakymų* darbo tvarkos tipas ir *Padėjimo* darbo tipas nevertina kelių vietos krypties veiksmų, kai **Kelių SKU** parinktis pasirenkama. Tik pirmasis vietos krypties veiksmas yra vertinamas.

## <a name="resolution"></a>Sprendimas

Nauja funkcija, *Vertinti visus veiksmus kelioms SKU vietos kryptims* buvo įtraukta į versiją 10.0.15 (žr. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Ši funkcija vertina visus veiksmus kelioms SKU vietos kryptims. Jei jums reikia šios funkcijos, naudokite [Funkcijos valdymą](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) tam, kad ją įjungtumėte.
