---
title: Planavimo užduoties atšaukimas
description: Šioje temoje paaiškinama, kaip atšaukti aktyvią planavimo užduotį, naudojančią planavimo optimizavimo funkciją.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b731aa4573b438e594ede702e6556c1be2daa549
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213476"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="48eb8-103">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="48eb8-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="48eb8-104">Programoje „Microsoft Dynamics 365 Supply Chain Management“ galite atšaukti aktyvią planavimo užduotį, naudojančią planavimo optimizavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="48eb8-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="48eb8-105">Kai dialogo lange pasirenkate **Atšaukti**, kai planavimo optimizavimo užduotis suaktyvinama tiesiogiai iš vartotojo sąsajos (ne fone), planavimo optimizavimo užduotis atšaukta nebus.</span><span class="sxs-lookup"><span data-stu-id="48eb8-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="48eb8-106">Net jei gaunate įspėjimą, pvz., Operacija atšaukta, vis tiek reikės atlikti šiuos veiksmus, kad būtų atšaukta planavimo optimizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="48eb8-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="48eb8-107">Norėdami atšaukti aktyvią planavimo užduotį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="48eb8-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="48eb8-108">Atšaukti galima tik aktyvias užduotis.</span><span class="sxs-lookup"><span data-stu-id="48eb8-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="48eb8-109">Eikite į **Bendrasis planavimas \>Sąranka \>Planai**.</span><span class="sxs-lookup"><span data-stu-id="48eb8-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="48eb8-110">Pasirinkite planavimo vykdymui tinkamą planą.</span><span class="sxs-lookup"><span data-stu-id="48eb8-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="48eb8-111">Pasirinkite **Istorija**.</span><span class="sxs-lookup"><span data-stu-id="48eb8-111">Select **History**.</span></span>
4. <span data-ttu-id="48eb8-112">Pasirinkite planavimo užduotį, kurią reikia atšaukti.</span><span class="sxs-lookup"><span data-stu-id="48eb8-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="48eb8-113">Pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="48eb8-113">Select **Cancel**.</span></span>

<span data-ttu-id="48eb8-114">Užduoties būsena bus **Atšaukiama**, kol planavimo optimizavimo tarnyba patvirtins, kad užduotis atšaukta.</span><span class="sxs-lookup"><span data-stu-id="48eb8-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="48eb8-115">Būsena tada bus pakeista į **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="48eb8-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="48eb8-116">Norėdami pamatyti būsenos pasikeitimus, turite atnaujinti puslapį pasirinkdami mygtuką **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="48eb8-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48eb8-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="48eb8-117">Additional resources</span></span>

[<span data-ttu-id="48eb8-118">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="48eb8-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="48eb8-119">Darbo su planavimo optimizavimu pradžia</span><span class="sxs-lookup"><span data-stu-id="48eb8-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="48eb8-120">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="48eb8-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="48eb8-121">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="48eb8-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="48eb8-122">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="48eb8-122">Apply filters to a plan</span></span>](plan-filters.md)
