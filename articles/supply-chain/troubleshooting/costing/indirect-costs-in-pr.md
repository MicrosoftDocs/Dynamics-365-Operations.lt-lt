---
title: Netiesioginių išlaidų proceso ataskaita apima panaikintus gamybos užsakymus
description: Proceso netiesioginių išlaidų ataskaitoje pateikiama informacija apie gamybos užsakymus, kurie buvo iš dalies apdoroti ir vėliau panaikinti.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751774"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Netiesioginių išlaidų proceso ataskaita apima panaikintus gamybos užsakymus

KB numeris: 4612748

## <a name="symptoms"></a>Požymiai

Proceso **netiesioginių išlaidų ataskaitoje** pateikiama informacija apie gamybos užsakymus, kurie buvo iš dalies apdoroti ir vėliau panaikinti.

## <a name="resolution"></a>Skiriamoji geba

Atšaukę gamybos užsakymą, taip pat atšaukiate visas to gamybos užsakymo operacijas. Kai panaikinate gamybos užsakymą, papildomos knygos lentelės ir DK išlieka visos su juo susijusios operacijos. Ataskaitose papildomos knygos lentelėse bus pateikiamos operacijos. Konkretaus gamybos užsakymo grynoji vertė turi būti 0,00.
