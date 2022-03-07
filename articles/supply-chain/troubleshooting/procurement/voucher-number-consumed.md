---
title: Produkto gavimo kvito numeris suvartojamas net tada, kai nėra generuojamas kvitas
description: Produkto gavimo kvito numeris sunaudotas, net jei produkto gavimo metu nesukuriamas joks finansinis kvitas
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
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477086"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Produkto gavimo kvito numeris suvartojamas net tada, kai nėra generuojamas kvitas

## <a name="symptoms"></a>Požymiai

Produkto gavimo kvito numeris sunaudotas, net jei produkto gavimo metu nesukuriamas joks finansinis kvitas.

## <a name="resolution"></a>Sprendimas

Jei pasirinktis **Sukaupti įsipareigojimus gavimo dokumente** prekės modelių grupei nustatyta kaip *Ne*, didžiojoje knygoje nebus vykdomi jokie registravimai. Tačiau faktinis įvykis bus įrašytas papildomos knygos apskaitos tikslais, o tam įvykiui būtinas kvito numeris. Šis kvito numeris yra numeris, nurodomas atsargų operacijose.

Rekomenduojame nustatyti pasirinktį **Sukaupti įsipareigojimus gavimo dokumente** kaip *Taip*, kaip ir aprašyta šiame tinklaraščio įraše: [Registruoti pap. išlaidas produkto gavimo metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
