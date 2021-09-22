---
title: Pristatymo likučio atšaukimas perkelia pirkimo užsakymą į patvirtintą būseną
description: Jei pristatymo likutis atšaukiamas pirkimo užsakyme, kur įjungtas keitimų valdymas, pirkimo užsakymo būsena yra patvirtinta.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477104"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Pristatymo likučio atšaukimas perkelia pirkimo užsakymą į patvirtintą būseną

## <a name="symptoms"></a>Požymiai

Jei vienintelis prašomas pirkimo užsakymo, kuriam taikomas keitimų valdymas, pakeitimas yra pristatymo likučio panaikinimas vienoje ar keliose eilutėse, pirkimo užsakymas bus priskirtas tiesiai į *Patvirtintą* būseną, kai jis bus patvirtintas, o žurnalas nebus sukurtas.

## <a name="resolution"></a>Sprendimas

Pristatymo likučio atšaukimas nedaro poveikio patvirtinimo žurnalo turiniui. Ši funkcija turėtų būti naudojama, kai eilutė buvo gauta iš dalies ir likučio kiekis turėtų būti atšauktas proceso etape po to, kai pirkimo užsakymas yra patvirtintas tiekėjo.

Jei tai turi atsispindėti pirkimo užsakymo patvirtinime, kiekis turi būti pakoreguotas pirkimo užsakymo eilutėje, kad būtų reikalingas patvirtinimas. Taip pat, jei eilutėje nieko negauta, kiekis gali būti pašalintas. Šiuo atveju reikės patvirtinti iš naujo.
