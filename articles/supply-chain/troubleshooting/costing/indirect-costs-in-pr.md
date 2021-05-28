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
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026746"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="a2220-103">Netiesioginių išlaidų proceso ataskaita apima panaikintus gamybos užsakymus</span><span class="sxs-lookup"><span data-stu-id="a2220-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="a2220-104">KB numeris: 4612748</span><span class="sxs-lookup"><span data-stu-id="a2220-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="a2220-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="a2220-105">Symptoms</span></span>

<span data-ttu-id="a2220-106">Proceso **netiesioginių išlaidų ataskaitoje** pateikiama informacija apie gamybos užsakymus, kurie buvo iš dalies apdoroti ir vėliau panaikinti.</span><span class="sxs-lookup"><span data-stu-id="a2220-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2220-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="a2220-107">Resolution</span></span>

<span data-ttu-id="a2220-108">Atšaukę gamybos užsakymą, taip pat atšaukiate visas to gamybos užsakymo operacijas.</span><span class="sxs-lookup"><span data-stu-id="a2220-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="a2220-109">Kai panaikinate gamybos užsakymą, papildomos knygos lentelės ir DK išlieka visos su juo susijusios operacijos.</span><span class="sxs-lookup"><span data-stu-id="a2220-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="a2220-110">Ataskaitose papildomos knygos lentelėse bus pateikiamos operacijos.</span><span class="sxs-lookup"><span data-stu-id="a2220-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="a2220-111">Konkretaus gamybos užsakymo grynoji vertė turi būti 0,00.</span><span class="sxs-lookup"><span data-stu-id="a2220-111">For the specific production order, the net value should be 0.00.</span></span>
