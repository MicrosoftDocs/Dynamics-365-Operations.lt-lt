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
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102968"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Keli SKU pasirinktis neįvertina kelių vietos nustatymo veiksmų

## <a name="symptoms"></a>Požymiai

Krypties vietos *Pardavimo užsakymų* darbo tvarkos tipas ir *Padėjimo* darbo tipas nevertina kelių vietos krypties veiksmų, kai **Kelių SKU** parinktis pasirenkama. Tik pirmasis vietos krypties veiksmas yra vertinamas.

## <a name="resolution"></a>Sprendimas

Nauja funkcija, *Vertinti visus veiksmus kelioms SKU vietos kryptims* buvo įtraukta į versiją 10.0.15 (žr. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Ši funkcija vertina visus veiksmus kelioms SKU vietos kryptims. Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą.  Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Administratoriai gali naudotis funkcijų [valdymo puslapiu](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), norėdami patikrinti priemonės būseną ir, jei reikia, ją įgalinti arba išjungti.
