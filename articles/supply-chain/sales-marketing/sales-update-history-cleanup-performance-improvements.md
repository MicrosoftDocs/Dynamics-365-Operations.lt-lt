---
title: Pardavimo istorijos valymo našumo patobulinimai
description: Šioje temoje aprašoma pardavimo retrospektyvos valymo našumo patobulinimų priemonė ir kaip ją įgalinti.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985916"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Pardavimo istorijos valymo našumo patobulinimai

[!include [banner](../includes/banner.md)]

Periodinis partinis darbas **Pardavimų retrospektyvos valymas** gali ilgai užtrukti, jei jis nedažnai vykdomas aplinkose, kuriose yra didelis pardavimų naujinimų kiekis. Tokiais atvejais *Pardavimo retrospektyvos valymo našumo patobulinimų* priemonė gali padėti sumažinti vykdymo trukmę ir padidinti patikimumą.

Priemonė pagerina esamą valymo užduotį šiais būdais:

- Ji išskaido išvalymą į paketus (pritaikymais galite keisti paketo dydį).
- Jis veiks daugiausia 2 valandas (pritaikymo metu galite keisti trukmę).
- Kai įmanoma, jis pritaiko svertą duomenų bazės galimybėms, kad valymo metu būtų sumažinti užrakinimų ginčai ir būtų išvengta operacinių lentelių prijungimo.

Įgalinus šią priemonę, **Pardavimo atnaujinimo retrospektyvos valymo** paketinė užduotis (**Pardavimo ir rinkodaros \> Periodinė užduotis \> Valymas \> Pardavimo atnaujinimo retrospektyvos valymas**) bus vykdoma taip, kaip buvo anksčiau, tačiau geresniu veikimu ir daugiausiai 2 valandoms. Tai reiškia, kad gali tekti paleisti kelis kartus, kad išvalytumėte visus duomenis per tam tikrą saugojimo laikotarpį.

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>Įjungti pardavimo retrospektyvos valymo efektyvumo patobulinimų funkciją

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Pardavimai ir rinkodara*
- **Funkcijos pavadinimas:** *Pardavimo istorijos valymo našumo patobulinimai*
