---
title: Vietos plano kūrimas
description: Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "364769"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="5e54f-103">Vietos plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="5e54f-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e54f-104">Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="5e54f-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="5e54f-105">Kai sukurti šaltinių pasiūlymai, užsakymus jis randa vietoje, kuriai planuoja ir juos patvirtina, pradėdamas nuo skubių.</span><span class="sxs-lookup"><span data-stu-id="5e54f-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="5e54f-106">Skubiausi užsakymai yra tie, kuriuos patvirtinti reikia šią dieną.</span><span class="sxs-lookup"><span data-stu-id="5e54f-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="5e54f-107">Šioms užduotims atlikti naudokite demonstracinių duomenų įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="5e54f-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="5e54f-108">Prekės medžiagų ir pajėgumų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="5e54f-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="5e54f-109">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="5e54f-109">Click Master planning.</span></span>
    * <span data-ttu-id="5e54f-110">Turite pereiti į numatytąją ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="5e54f-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="5e54f-111">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="5e54f-111">Click Run.</span></span>
3. <span data-ttu-id="5e54f-112">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="5e54f-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="5e54f-113">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="5e54f-113">Click Filter.</span></span>
5. <span data-ttu-id="5e54f-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="5e54f-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="5e54f-115">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5e54f-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="5e54f-116">Pavyzdys: D0001</span><span class="sxs-lookup"><span data-stu-id="5e54f-116">Example: D0001</span></span>  
7. <span data-ttu-id="5e54f-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5e54f-117">Click OK.</span></span>
8. <span data-ttu-id="5e54f-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5e54f-118">Click OK.</span></span>
    * <span data-ttu-id="5e54f-119">Tai gali užtrukti keletą minučių.</span><span class="sxs-lookup"><span data-stu-id="5e54f-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="5e54f-120">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5e54f-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="5e54f-121">Skubių suplanuotų prekės užsakymų identifikavimas</span><span class="sxs-lookup"><span data-stu-id="5e54f-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="5e54f-122">Atidarykite stulpelio filtrą Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="5e54f-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="5e54f-123">Lauke „Prekės numeris‟ pritaikykite filtrą, naudodami reikšmę „D0001‟ ir filtro operatorių „prasideda‟.</span><span class="sxs-lookup"><span data-stu-id="5e54f-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="5e54f-124">Atidarykite stulpelio filtrą Užsakymo data.</span><span class="sxs-lookup"><span data-stu-id="5e54f-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="5e54f-125">Laukui Užsakymo data taikykite filtrą – šios dienos reikšmę, naudodami filtro operatorių „yra tiksliai‟.</span><span class="sxs-lookup"><span data-stu-id="5e54f-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="5e54f-126">Visų skubių prekės užsakymų patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="5e54f-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="5e54f-127">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="5e54f-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="5e54f-128">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="5e54f-128">Click Firm.</span></span>
3. <span data-ttu-id="5e54f-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5e54f-129">Click OK.</span></span>

