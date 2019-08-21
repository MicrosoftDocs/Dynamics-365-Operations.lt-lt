---
title: Nustatyti pažangiosios gamybos planavimo grupes
description: Pažangiosios gamybos planavimo grupės apibrėžtos grupuoti ir atskirti produktus iš „kanban“ planavimo.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0cb17c68abbc4979a65e33c50450be575df3d93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836269"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="314fc-103">Nustatyti pažangiosios gamybos planavimo grupes</span><span class="sxs-lookup"><span data-stu-id="314fc-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="314fc-104">Pažangiosios gamybos planavimo grupės apibrėžtos grupuoti ir atskirti produktus iš „kanban“ planavimo.</span><span class="sxs-lookup"><span data-stu-id="314fc-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="314fc-105">Grupavimą galima atlikti kaip bendrąjį susiejimą visoje įmonėje arba būdingą darbo elementui.</span><span class="sxs-lookup"><span data-stu-id="314fc-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="314fc-106">Kiekviena grupė turi spalvos kodą, priskirtą vizualiai nurodyti "kanban" planavimo „listpage“.</span><span class="sxs-lookup"><span data-stu-id="314fc-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="314fc-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="314fc-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="314fc-108">Apibrėžti pažangiosios gamybos planavimo grupę</span><span class="sxs-lookup"><span data-stu-id="314fc-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="314fc-109">Eikite į Produkto informacijos valdymas > „Lean manufacturing“ > Pažangiosios gamybos planavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="314fc-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="314fc-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="314fc-110">Click New.</span></span>
3. <span data-ttu-id="314fc-111">Lauke Grafiko grupė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="314fc-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="314fc-112">Planavimo grupę galima apibrėžti kaip visuotinę grupę arba būdingą darbo elementui.</span><span class="sxs-lookup"><span data-stu-id="314fc-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="314fc-113">Šiame paprastame pavyzdyje nustatėme visuotinę grupę, o darbo elementą palikome tuščią.</span><span class="sxs-lookup"><span data-stu-id="314fc-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="314fc-114">Šios grupės nustatymai taikomi visiems darbo elementams, kurie neturi tam tikrų planavimo grupių.</span><span class="sxs-lookup"><span data-stu-id="314fc-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="314fc-115">Iš spalvų pasirinkimo pasirinkite spalvą.</span><span class="sxs-lookup"><span data-stu-id="314fc-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="314fc-116">Spalvos naudojamos išryškinti užduotis „kanban“ grafiko sąrašo puslapyje ar „kanban“ proceso srityje.</span><span class="sxs-lookup"><span data-stu-id="314fc-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="314fc-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="314fc-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="314fc-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="314fc-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="314fc-119">Susieti produktą</span><span class="sxs-lookup"><span data-stu-id="314fc-119">Associate product</span></span>
1. <span data-ttu-id="314fc-120">Susieti konkretų produktą</span><span class="sxs-lookup"><span data-stu-id="314fc-120">Associate a specific product</span></span>
    * <span data-ttu-id="314fc-121">Yra du būdai susieti produktus su pažangiosios gamybos planavimo grupėmis: arba kaip konkretų produktą (Prekės ryšio tipas = Prekė), arba kaip prekių paskirstymo raktą (prekės ryšio tipas = grupė).</span><span class="sxs-lookup"><span data-stu-id="314fc-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="314fc-122">Lauke Prekės ryšio tipas pasirinkite Prekė</span><span class="sxs-lookup"><span data-stu-id="314fc-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="314fc-123">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="314fc-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="314fc-124">Lauke Našumo dažnis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="314fc-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="314fc-125">Numatytasis Našumo koeficientas yra 1, tai reiškia, kad susijusiems produktams suvartojamas tiksliai toks pajėgumas, koks nurodytas gamybos eigos proceso veikloje.</span><span class="sxs-lookup"><span data-stu-id="314fc-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="314fc-126">Našumo santykis > 1 nurodo didesnį išteklių suvartojimą, Našumo koeficientas < 1 nurodo mažesnį išteklių suvartojimą.</span><span class="sxs-lookup"><span data-stu-id="314fc-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="314fc-127">Koeficientas naudojamas skaičiuojant savikainą ir „kanban“ užduoties suvartojimui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="314fc-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="314fc-128">Susieti prekių paskirstymo raktą</span><span class="sxs-lookup"><span data-stu-id="314fc-128">Associate item allocation key</span></span>
1. <span data-ttu-id="314fc-129">Susieti prekių paskirstymo raktą</span><span class="sxs-lookup"><span data-stu-id="314fc-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="314fc-130">Į prekių paskirstymo raktą įtraukite sąsają naudodami prekės ryšio tipą Grupė.</span><span class="sxs-lookup"><span data-stu-id="314fc-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="314fc-131">Atkreipkite dėmesį, kad šiam procesui reikia, kad jūsų duomenyse būtų nustatyta prekių paskirstymo rakto prognozė.</span><span class="sxs-lookup"><span data-stu-id="314fc-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="314fc-132">Lauke Prekės ryšio tipas pasirinkite Grupė</span><span class="sxs-lookup"><span data-stu-id="314fc-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="314fc-133">Lauke Prekės susiejimo raktas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="314fc-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="314fc-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="314fc-134">In the list, click the link in the selected row.</span></span>

