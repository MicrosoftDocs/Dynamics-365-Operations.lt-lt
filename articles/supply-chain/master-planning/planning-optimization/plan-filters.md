---
title: Filtrų taikymas planui
description: Šioje temoje paaiškinama, kaip naudoti plano filtrus, kai naudojama „Planning Optimization“ funkcija.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
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
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774015"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="59c5b-103">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="59c5b-103">Apply filters to a plan</span></span>

<span data-ttu-id="59c5b-104">Kai naudojama „Planning Optimization“ funkcija, galite taikyti plano filtrą.</span><span class="sxs-lookup"><span data-stu-id="59c5b-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="59c5b-105">Plano filtras bus taikomas visuomet, kai vykdomas bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="59c5b-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="59c5b-106">Plano filtras yra naudingas, kai norite apriboti planą tam tikrai prekių grupei, ir įsitikinti, kad nė viena kita prekė nebūtų įtraukta į gautą bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="59c5b-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="59c5b-107">Jei taikomas plano filtras ir apdorojimo filtras vykdant bendrąjį planavimą, į planavimo vykdymą įtraukiamas tik šių dviejų filtrų sutapimo taškas.</span><span class="sxs-lookup"><span data-stu-id="59c5b-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="59c5b-108">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="59c5b-108">Example scenario</span></span>

<span data-ttu-id="59c5b-109">Plano filtras nustatytas taip, kad jį sudarytų A, B ir C prekės. Tada bendrojo planavimo vykdymai taikomi tam pačiam planui, bet taikomi skirtingi padorojimo filtrai:</span><span class="sxs-lookup"><span data-stu-id="59c5b-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="59c5b-110">**Apdorojimo filtras, kuriame yra D prekė:** nėra suplanuotų prekių, nes nėra sutapimo taško tarp plano filtro ir padorojimo filtro.</span><span class="sxs-lookup"><span data-stu-id="59c5b-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="59c5b-111">**Apdorojimo filtras, kuriame yra A ir D prekės:** tik A prekė įtraukiama į planavimo vykdymą, nes D prekė nėra plano filtro dalis.</span><span class="sxs-lookup"><span data-stu-id="59c5b-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="59c5b-112">**Apdorojimo filtras, kuriame yra B prekė:** tik B prekė įtraukiama į planavimo vykdymą ir ankstesnė A prekės planavimo išvestis yra išsaugoma.</span><span class="sxs-lookup"><span data-stu-id="59c5b-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="59c5b-113">**Apdorojimo filtras, kuriame yra visos prekės (tuščias filtras):** A, B ir C yra įtraukiamos į planavimo vykdymą, o ankstesnio prekių A ir B planavimo išvestis perrašoma.</span><span class="sxs-lookup"><span data-stu-id="59c5b-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="59c5b-114">Neturėtumėte nustatyti plano filtro plane, kuris yra pasirinktas kaip **Dabartinis dinaminis bendrasis planas** puslapyje **Bendrojo planavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="59c5b-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="59c5b-115">Kitu atveju dinaminio bendrojo plano funkcija bus apribota filtruotomis prekėmis.</span><span class="sxs-lookup"><span data-stu-id="59c5b-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="59c5b-116">Pavyzdžiui, jei atnaujinami prekės, kuris nėra plano filtro dalis, grynieji poreikiai, nebus sugeneruota jokių rezultatų.</span><span class="sxs-lookup"><span data-stu-id="59c5b-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="59c5b-117">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="59c5b-117">Related resources</span></span>

[<span data-ttu-id="59c5b-118">„Planning Optimization“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="59c5b-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="59c5b-119">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="59c5b-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="59c5b-120">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="59c5b-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="59c5b-121">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="59c5b-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="59c5b-122">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="59c5b-122">Cancel a planning job</span></span>](cancel-planning-job.md)
