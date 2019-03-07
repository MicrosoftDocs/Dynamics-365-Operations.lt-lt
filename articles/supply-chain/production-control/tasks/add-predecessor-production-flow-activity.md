---
title: Ankstesnės veiklos įtraukimas į gamybos eigos veiklą
description: Gamybos eigos versijoje visos veiklos turi būti įtrauktos seką.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9acb1c2672af70f535f3dce1c8f5a97e8d479158
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "343678"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="9eaea-103">Ankstesnės veiklos įtraukimas į gamybos eigos veiklą</span><span class="sxs-lookup"><span data-stu-id="9eaea-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9eaea-104">Gamybos eigos versijoje visos veiklos turi būti įtrauktos seką.</span><span class="sxs-lookup"><span data-stu-id="9eaea-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="9eaea-105">Veiklai gali būti priskiriama viena arba kelios ankstesnės ar vėlesnės veiklos.</span><span class="sxs-lookup"><span data-stu-id="9eaea-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="9eaea-106">Šioje procedūroje parodoma, kaip ankstesnę veiklą susieti su veikla.</span><span class="sxs-lookup"><span data-stu-id="9eaea-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="9eaea-107">Norint atlikti šią užduotį, jums reikalinga juodraščio versijos gamybos eiga su bent dviem veiklomis, kurias galima sujungti.</span><span class="sxs-lookup"><span data-stu-id="9eaea-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="9eaea-108">Norėdami sužinoti daugiau, skaitykite dokumentą „Lean manufacturing“ gamybos eigos ir veiklos“.</span><span class="sxs-lookup"><span data-stu-id="9eaea-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="9eaea-109">Kaip rasti gamybos eigą ir versiją</span><span class="sxs-lookup"><span data-stu-id="9eaea-109">Find the production flow and version</span></span>
1. <span data-ttu-id="9eaea-110">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="9eaea-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="9eaea-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9eaea-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9eaea-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9eaea-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9eaea-113">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9eaea-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9eaea-114">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="9eaea-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="9eaea-115">Veiklos pasirinkimas ir ankstesnės veiklos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="9eaea-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="9eaea-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9eaea-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="9eaea-117">Spustelėkite Įtraukti ankstesnę veiklą.</span><span class="sxs-lookup"><span data-stu-id="9eaea-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="9eaea-118">Lauke Veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9eaea-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="9eaea-119">Lauke Ciklo laiko koeficientas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9eaea-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="9eaea-120">Numatytasis veiklos ryšio ciklo laiko koeficientas yra 1.</span><span class="sxs-lookup"><span data-stu-id="9eaea-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="9eaea-121">Tai reiškia, kad abi veiklos yra vykdomos tuo pačiu tempu ir jų vieneto gamybos laikai sutampa.</span><span class="sxs-lookup"><span data-stu-id="9eaea-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="9eaea-122">Jei ankstesnė veikla vykdoma didesniu tempu (trumpesnis vieneto gamybos laikas), koeficientas turėtų būti mažesnis už 1, jei ankstesnė veikla vykdoma mažesniu tempu (ilgesnis vieneto gamybos laikas), ciklo laiko koeficientas yra didesnis už 1.</span><span class="sxs-lookup"><span data-stu-id="9eaea-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="9eaea-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9eaea-123">Click OK.</span></span>

