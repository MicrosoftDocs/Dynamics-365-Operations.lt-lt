---
title: Filtrų taikymas planui
description: Šioje temoje paaiškinama, kaip naudoti plano filtrus, kai naudojama „Planning Optimization“ funkcija.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
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
ms.openlocfilehash: 73e4a045ff5a9912b898a7115d3d8f530846ebdd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209794"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="05c9a-103">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="05c9a-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05c9a-104">Kai naudojama „Planning Optimization“ funkcija, galite taikyti plano filtrą.</span><span class="sxs-lookup"><span data-stu-id="05c9a-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="05c9a-105">**Plano filtras** bus taikomas visuomet, kai vykdomas bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="05c9a-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="05c9a-106">**Plano filtras** yra naudingas, kai norite apriboti planą tam tikrai prekių grupei, ir įsitikinti, kad nė viena kita prekė nebūtų įtraukta į gautą bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="05c9a-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="05c9a-107">Jei taikomas **Plano filtras** ir apdorojimo filtras vykdant bendrąjį planavimą, į planavimo vykdymą įtraukiamas tik šių dviejų filtrų sutapimo taškas.</span><span class="sxs-lookup"><span data-stu-id="05c9a-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="05c9a-108">**Plano filtras** pasiekiamas pasirinkus **Bendrieji planai**, kai naudojamas planavimo optimizavimas.</span><span class="sxs-lookup"><span data-stu-id="05c9a-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="05c9a-109">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="05c9a-109">Example scenario</span></span>

<span data-ttu-id="05c9a-110">Plano filtras nustatytas taip, kad jį sudarytų A, B ir C prekės. Tada bendrojo planavimo vykdymai taikomi tam pačiam planui, bet taikomi skirtingi padorojimo filtrai:</span><span class="sxs-lookup"><span data-stu-id="05c9a-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="05c9a-111">**Apdorojimo filtras, kuriame yra D prekė:** nėra suplanuotų prekių, nes nėra sutapimo taško tarp plano filtro ir padorojimo filtro.</span><span class="sxs-lookup"><span data-stu-id="05c9a-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="05c9a-112">**Apdorojimo filtras, kuriame yra A ir D prekės:** tik A prekė įtraukiama į planavimo vykdymą, nes D prekė nėra plano filtro dalis.</span><span class="sxs-lookup"><span data-stu-id="05c9a-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="05c9a-113">**Apdorojimo filtras, kuriame yra B prekė:** tik B prekė įtraukiama į planavimo vykdymą ir ankstesnė A prekės planavimo išvestis yra išsaugoma.</span><span class="sxs-lookup"><span data-stu-id="05c9a-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="05c9a-114">**Apdorojimo filtras, kuriame yra visos prekės (tuščias filtras):** A, B ir C yra įtraukiamos į planavimo vykdymą, o ankstesnio prekių A ir B planavimo išvestis perrašoma.</span><span class="sxs-lookup"><span data-stu-id="05c9a-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="05c9a-115">Neturėtumėte nustatyti plano filtro plane, kuris yra pasirinktas kaip **Dabartinis dinaminis bendrasis planas** puslapyje **Bendrojo planavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="05c9a-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="05c9a-116">Kitu atveju dinaminio bendrojo plano funkcija bus apribota filtruotomis prekėmis.</span><span class="sxs-lookup"><span data-stu-id="05c9a-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="05c9a-117">Pavyzdžiui, jei atnaujinami prekės, kuris nėra plano filtro dalis, grynieji poreikiai, nebus sugeneruota jokių rezultatų.</span><span class="sxs-lookup"><span data-stu-id="05c9a-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="05c9a-118">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="05c9a-118">Related resources</span></span>

[<span data-ttu-id="05c9a-119">„Planning Optimization“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="05c9a-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="05c9a-120">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="05c9a-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="05c9a-121">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="05c9a-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="05c9a-122">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="05c9a-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="05c9a-123">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="05c9a-123">Cancel a planning job</span></span>](cancel-planning-job.md)
