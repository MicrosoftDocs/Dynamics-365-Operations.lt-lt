---
title: Pardavimo retrospektyvos valymo našumo patobulinimai
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
ms.openlocfilehash: 3dc36c8562f39a076bd4871524e2d132d1883d28
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860722"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Pardavimo retrospektyvos valymo našumo patobulinimai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] 
<!-- KFM: Preview until GA with 10.0.24 -->

Periodinis partinis darbas **Pardavimų retrospektyvos valymas** gali ilgai užtrukti, jei jis nedažnai vykdomas aplinkose, kuriose yra didelis pardavimų naujinimų kiekis. Tokiais atvejais *Pardavimo retrospektyvos valymo našumo patobulinimų* priemonė gali padėti sumažinti vykdymo trukmę ir padidinti patikimumą.

Priemonė pagerina esamą valymo užduotį šiais būdais:

- Ji išskaido išvalymą į paketus (pritaikymais galite keisti paketo dydį).
- Jis veiks daugiausia 2 valandas (pritaikymo metu galite keisti trukmę).
- Kai įmanoma, jis pritaiko svertą duomenų bazės galimybėms, kad valymo metu būtų sumažinti užrakinimų ginčai ir būtų išvengta operacinių lentelių prijungimo.

Įgalinus šią priemonę, **Pardavimo atnaujinimo retrospektyvos valymo** paketinė užduotis (**Pardavimo ir rinkodaros \> Periodinė užduotis \> Valymas \> Pardavimo atnaujinimo retrospektyvos valymas**) bus vykdoma taip, kaip buvo anksčiau, tačiau geresniu veikimu ir daugiausiai 2 valandoms. Tai reiškia, kad gali tekti paleisti kelis kartus, kad išvalytumėte visus duomenis per tam tikrą saugojimo laikotarpį.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Įjunkite pardavimo istorijos valymo našumo patobulinimų funkciją

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Pardavimai ir rinkodara*
- **Funkcijos pavadinimas:** *Pardavimo istorijos valymo našumo patobulinimai*
