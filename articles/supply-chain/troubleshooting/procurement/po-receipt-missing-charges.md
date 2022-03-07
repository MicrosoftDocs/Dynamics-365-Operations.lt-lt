---
title: Pirkimo užsakymo kvite nenurodyti visi mokesčiai
description: Pirkimo užsakymo kvite nenurodyti visi mokesčiai
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477050"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Pirkimo užsakymo kvite nenurodyti visi mokesčiai

## <a name="symptoms"></a>Požymiai

Kai gaunate pirkimo užsakymą, ne visos išlaidos įtraukiamos į gavimą.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Puslapio **Įsigijimo ir šaltinio pasirinkimo parametrai** skirtuke **Pristatymas** įsitikinkite, kad parinktis **Generuoti mokesčius produkto gavimo kvite** nustatyta kaip *Taip*.
1. Sukurkite pirkimo užsakymą, apimantį mokesčius.
1. Patvirtinkite pirkimo užsakymą.
1. Gaukite pirkimo užsakymą.
1. Peržiūrėkite bendrąją kvito sumą ir palyginkite ją su numatoma bendrąja suma.
1. Atkreipkite dėmesį, kad ne visi mokesčiai yra įtraukti į pirkimo užsakymo kvitą.

## <a name="resolution"></a>Sprendimas

Paaiškinimas priklauso nuo to, kaip buvo nustatytos papildomos išlaidos. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti papildomas išlaidas, atitinkančias jūsų poreikius, žr. šiuos internetinio dienoraščio pranešimus: [Užregistruokite papildomas išlaidas produkto gavimo kvito metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
