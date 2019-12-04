---
title: Planavimo užduoties atšaukimas
description: Šioje temoje paaiškinama, kaip atšaukti aktyvią planavimo užduotį, naudojančią planavimo optimizavimo funkciją.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774016"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="e19f8-103">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="e19f8-103">Cancel a planning job</span></span>

<span data-ttu-id="e19f8-104">Programoje „Microsoft Dynamics 365 Supply Chain Management“ galite atšaukti aktyvią planavimo užduotį, naudojančią planavimo optimizavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="e19f8-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="e19f8-105">Norėdami atšaukti aktyvią planavimo užduotį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e19f8-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="e19f8-106">Atšaukti galima tik aktyvias užduotis.</span><span class="sxs-lookup"><span data-stu-id="e19f8-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="e19f8-107">Eikite į **Bendrasis planavimas \>Sąranka \>Planai**.</span><span class="sxs-lookup"><span data-stu-id="e19f8-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="e19f8-108">Pasirinkite planavimo vykdymui tinkamą planą.</span><span class="sxs-lookup"><span data-stu-id="e19f8-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="e19f8-109">Pasirinkite **Istorija**.</span><span class="sxs-lookup"><span data-stu-id="e19f8-109">Select **History**.</span></span>
4. <span data-ttu-id="e19f8-110">Pasirinkite planavimo užduotį, kurią reikia atšaukti.</span><span class="sxs-lookup"><span data-stu-id="e19f8-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="e19f8-111">Pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="e19f8-111">Select **Cancel**.</span></span>

<span data-ttu-id="e19f8-112">Užduoties būsena bus **Atšaukiama**, kol planavimo optimizavimo tarnyba patvirtins, kad užduotis atšaukta.</span><span class="sxs-lookup"><span data-stu-id="e19f8-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="e19f8-113">Būsena tada bus pakeista į **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="e19f8-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="e19f8-114">Norėdami pamatyti būsenos pasikeitimus, turite atnaujinti puslapį pasirinkdami mygtuką **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="e19f8-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e19f8-115">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="e19f8-115">Related resources</span></span>

[<span data-ttu-id="e19f8-116">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="e19f8-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e19f8-117">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="e19f8-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="e19f8-118">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="e19f8-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e19f8-119">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="e19f8-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e19f8-120">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="e19f8-120">Apply filters to a plan</span></span>](plan-filters.md)
