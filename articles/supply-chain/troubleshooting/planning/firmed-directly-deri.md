---
title: Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos
description: Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos, kurios būsena yra peržiūrima.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026753"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="c33f1-103">Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos</span><span class="sxs-lookup"><span data-stu-id="c33f1-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="c33f1-104">KB numeris: 4612450</span><span class="sxs-lookup"><span data-stu-id="c33f1-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="c33f1-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="c33f1-105">Symptoms</span></span>

<span data-ttu-id="c33f1-106">Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos, kurios būsena yra *peržiūrima*.</span><span class="sxs-lookup"><span data-stu-id="c33f1-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c33f1-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="c33f1-107">Resolution</span></span>

<span data-ttu-id="c33f1-108">Kai keitimo sekimas yra įjungtas, *Peržiūrima* būsena yra priskirta pasirašytiems išvestiniams užsakymams (papildomos sutarties pirkimo užsakymams).</span><span class="sxs-lookup"><span data-stu-id="c33f1-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="c33f1-109">Todėl, jei pirkimo užsakymas išvestas (subrangos pirkimo užsakymas), jis pateikiamas tik darbo eigai.</span><span class="sxs-lookup"><span data-stu-id="c33f1-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="c33f1-110">Jei pirkimo užsakymas yra patvirtintas suplanuotas pirkimo užsakymas, jis automatiškai patvirtintas siekiant užtikrinti, kad planavimo variklis nekuria naujų suplanuotų užsakymų, kol pirkimo užsakymo būsena dar yra *Juodraštis*.</span><span class="sxs-lookup"><span data-stu-id="c33f1-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
