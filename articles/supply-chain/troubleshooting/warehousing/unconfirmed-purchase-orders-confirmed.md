---
title: Atnaujinti gavimo kvitų užduotį, patvirtina nepatvirtintus užsakymus
description: Paleidus Atnaujinti gavimo kvitus, sistema patvirtina nepatvirtintus užsakymus, kurių būsena yra Užregistruota. Sužinokite apie šią problemą ištaisa priemonę.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477057"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Nepatvirtinti prekybos užsakymai yra patvirtinti įvykdžius naujinimo produktų kvitus

## <a name="symptoms"></a>Požymiai

Man įvykdžius *Naujinimo produkto gavimų* periodinę užduotį, sistema automatiškai patvirtina nepatvirtintus pirkimo užsakymus, kurie turi inventoriaus perlaidos būseną *Registruotą*.

## <a name="resolution"></a>Sprendimas

Nauja įvesties apkrovos tvarkymo funkcija, *Per krovinio kiekių gavimą*, ištaiso šią triktį. Norėdami įjungti šią funkciją, eikite į [Funkcijos valdymas](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) darbo sritį ir įjunkite tolesnes funkcijas tam, kad jos būtų sąraše:

1. Susieti pirkimo užsakymo atsargų operacijas su kroviniu
2. Krovinio kiekio perviršis

Dėl išsamesnės informacijos, žr. [Publikuoti registruotus produktų kiekius pagal pirkimo užsakymus](/dynamics365/supply-chain/warehousing/inbound-load-handling).
