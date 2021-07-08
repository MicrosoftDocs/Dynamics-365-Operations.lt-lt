---
title: Atšaukti produkto gavimo kvitai neatnaujina operacijos būsenos į Užregistruota
description: Atšaukus gaunamo krovinio produkto gavimo kvitus, sistema automatiškai atnaujina atsargų operacijos būseną iš Gauta į Užsakyta.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294135"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Atšaukti produkto gavimo kvitai neatnaujina operacijos būsenos į Užregistruota

## <a name="symptoms"></a>Požymiai

Įvykdžius **Atšaukti produkto gavimo kvitus** veiksmą gaunamam kroviniui, sistema automatiškai atnaujina atsargų operacijų būseną iš *Gauta* į *Užsakyta*.

## <a name="resolution"></a>Sprendimas

Atšaukus siunčiamų krovinių važtaraščius, atsargų operacijų būsena lieka *Paimta*. Tačiau kai atšaukiami gaunamo krovinio produktų gavimo kvitai, atsargų operacijų būsena neatkuriama į *Užregistruota*. Todėl atšaukus produkto gavimo kvitą iš gaunamo krovinio, sandėlio darbuotojas turi iš naujo užregistruoti krovinių prekių kiekius.

Daugiau informacijos rasite [Registruoti gaunamo krovinio prekių kiekius](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
