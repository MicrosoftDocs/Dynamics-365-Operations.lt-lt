---
title: Planavimo optimizavimo tinkamumo analizė
description: Šioje temoje paaiškinama, kaip patikrinti dabartinę sąranką ir duomenis, atsižvelgiant į „Planning Optimization“ funkcijos galimybes.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
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
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208759"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="09d78-103">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="09d78-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09d78-104">Norėdami pamatyti, kaip suderinama dabartinė sąranka ir duomenys „Planning Optimization“, eikite į **Bendrasis planavimas** \> **Sąranka** \> **„Planning Optimization“ tinkamumo analizė** ir pasirinkite **Atlikti analizę**.</span><span class="sxs-lookup"><span data-stu-id="09d78-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="09d78-105">Jei atlikus analizę randama neatitikimų, jie pateikiami tame pačiame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="09d78-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="09d78-106">(Analizė gali užtrukti kelias minutes.)</span><span class="sxs-lookup"><span data-stu-id="09d78-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="09d78-107">Jei randama neatitikimų, vis tiek galite naudoti „Planning Optimization“ funkciją.</span><span class="sxs-lookup"><span data-stu-id="09d78-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="09d78-108">Tinkamumo analizės rezultatai rodo tik tas vietas, kuriose planavimo paslauga neatsižvelgs į dabartinę sąranką.</span><span class="sxs-lookup"><span data-stu-id="09d78-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="09d78-109">Kitaip tariant, rodomos vietos, kuriose gali būti nepaisoma kai kurių procesų arba jie gali būti nepalaikomi.</span><span class="sxs-lookup"><span data-stu-id="09d78-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="09d78-110">Analizės rezultatai: 1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="09d78-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="09d78-111">**Funkcija:** gamyba</span><span class="sxs-lookup"><span data-stu-id="09d78-111">**Feature:** Production</span></span>
- <span data-ttu-id="09d78-112">**Problema:** prekės, kurių KS lygis didesnis nei nulis: 56</span><span class="sxs-lookup"><span data-stu-id="09d78-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="09d78-113">**Paaiškinimas:** tinkamumo analizė rado 56 prekes, kurios turi komplektavimo specifikacijos (KS) nustatymus gamybai.</span><span class="sxs-lookup"><span data-stu-id="09d78-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="09d78-114">Kadangi dabartinė „Planning Optimization“ versija nepalaiko gamybos, „Planning Optimization“ sugeneruos suplanuotus pirkimo užsakymus, ne suplanuotus gamybos užsakymus.</span><span class="sxs-lookup"><span data-stu-id="09d78-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="09d78-115">Taip pat bus rodomas įspėjimas, kuriame išvardijamos paveiktos prekės.</span><span class="sxs-lookup"><span data-stu-id="09d78-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="09d78-116">Analizės rezultatai: 2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="09d78-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="09d78-117">**Funkcija:** veiksmai</span><span class="sxs-lookup"><span data-stu-id="09d78-117">**Feature:** Actions</span></span>
- <span data-ttu-id="09d78-118">**Išdavimas:** padengimo grupės su įjungtu veiksmų skaičiavimu: 6</span><span class="sxs-lookup"><span data-stu-id="09d78-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="09d78-119">**Paaiškinimas:** tinkamumo analizė rado šešias padengimo grupes, kuriose veiksmų skaičiavimas įjungtas.</span><span class="sxs-lookup"><span data-stu-id="09d78-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="09d78-120">Kadangi dabartinė „Planning Optimization“ versija nepalaiko veiksmų, bendrojo planavimo metu jokie veiksmai nebus generuojami.</span><span class="sxs-lookup"><span data-stu-id="09d78-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="09d78-121">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="09d78-121">Related resources</span></span>

[<span data-ttu-id="09d78-122">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="09d78-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="09d78-123">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="09d78-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="09d78-124">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="09d78-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="09d78-125">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="09d78-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="09d78-126">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="09d78-126">Cancel a planning job</span></span>](cancel-planning-job.md)
