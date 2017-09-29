--- 
title: "Vietos plano kūrimas"
description: "Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="e5305-103">Vietos plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="e5305-103">Create a plan for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5305-104">Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e5305-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="e5305-105">Kai sukurti šaltinių pasiūlymai, užsakymus jis randa vietoje, kuriai planuoja ir juos patvirtina, pradėdamas nuo skubių.</span><span class="sxs-lookup"><span data-stu-id="e5305-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="e5305-106">Skubiausi užsakymai yra tie, kuriuos patvirtinti reikia šią dieną.</span><span class="sxs-lookup"><span data-stu-id="e5305-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="e5305-107">Šioms užduotims atlikti naudokite demonstracinių duomenų įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="e5305-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="e5305-108">Prekės medžiagų ir pajėgumų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="e5305-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="e5305-109">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="e5305-109">Click Master planning.</span></span>
    * <span data-ttu-id="e5305-110">Turite pereiti į numatytąją ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="e5305-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="e5305-111">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="e5305-111">Click Run.</span></span>
3. <span data-ttu-id="e5305-112">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="e5305-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="e5305-113">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="e5305-113">Click Filter.</span></span>
5. <span data-ttu-id="e5305-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="e5305-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e5305-115">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e5305-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e5305-116">Pavyzdys: D0001</span><span class="sxs-lookup"><span data-stu-id="e5305-116">Example: D0001</span></span>  
7. <span data-ttu-id="e5305-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e5305-117">Click OK.</span></span>
8. <span data-ttu-id="e5305-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e5305-118">Click OK.</span></span>
    * <span data-ttu-id="e5305-119">Tai gali užtrukti keletą minučių.</span><span class="sxs-lookup"><span data-stu-id="e5305-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="e5305-120">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e5305-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="e5305-121">Skubių suplanuotų prekės užsakymų identifikavimas</span><span class="sxs-lookup"><span data-stu-id="e5305-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="e5305-122">Atidarykite stulpelio filtrą Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="e5305-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="e5305-123">Lauke „Prekės numeris‟ pritaikykite filtrą, naudodami reikšmę „D0001‟ ir filtro operatorių „prasideda‟.</span><span class="sxs-lookup"><span data-stu-id="e5305-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="e5305-124">Atidarykite stulpelio filtrą Užsakymo data.</span><span class="sxs-lookup"><span data-stu-id="e5305-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="e5305-125">Laukui Užsakymo data taikykite filtrą – šios dienos reikšmę, naudodami filtro operatorių „yra tiksliai‟.</span><span class="sxs-lookup"><span data-stu-id="e5305-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="e5305-126">Visų skubių prekės užsakymų patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="e5305-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="e5305-127">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="e5305-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="e5305-128">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="e5305-128">Click Firm.</span></span>
3. <span data-ttu-id="e5305-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e5305-129">Click OK.</span></span>

