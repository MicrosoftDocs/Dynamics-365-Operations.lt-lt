---
title: „Lean“ iškvietimas iš pardavimo užsakymų
description: Ši procedūra padės iškvietimo medį patikrinti iš pardavimo eilutės, kurioje prekė gaminama naudojant „kanban“.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457e7128bed2232a3e092b31136f768940482741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994184"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="4c659-103">„Lean“ iškvietimas iš pardavimo užsakymų</span><span class="sxs-lookup"><span data-stu-id="4c659-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c659-104">Ši procedūra padės iškvietimo medį patikrinti iš pardavimo eilutės, kurioje prekė gaminama naudojant „kanban“.</span><span class="sxs-lookup"><span data-stu-id="4c659-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="4c659-105">Patikrinus iškvietimo medį, suplanuojamos visos „kanban“ užduotys.</span><span class="sxs-lookup"><span data-stu-id="4c659-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="4c659-106">Tai naudinga užsakymų scenarijuose, kai užsakymo priėmėjas turi užtikrinti, kad gamybą galima pradėti iš karto.</span><span class="sxs-lookup"><span data-stu-id="4c659-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="4c659-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="4c659-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4c659-108">Ši procedūra skirta detalesnio užsakymo priėmėjui, dirbančiam „lean“ įmonėje.</span><span class="sxs-lookup"><span data-stu-id="4c659-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="4c659-109">Kurti „kanban“ valdomos prekės pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="4c659-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="4c659-110">Eikite į Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="4c659-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="4c659-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4c659-111">Click New.</span></span>
3. <span data-ttu-id="4c659-112">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4c659-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="4c659-113">Naudokite US-001.</span><span class="sxs-lookup"><span data-stu-id="4c659-113">Use US-001.</span></span>  
4. <span data-ttu-id="4c659-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4c659-114">Click OK.</span></span>
5. <span data-ttu-id="4c659-115">Lauke „Prekės numeris“ įveskite „L0001“.</span><span class="sxs-lookup"><span data-stu-id="4c659-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="4c659-116">Nustatykite kiekį – 30.</span><span class="sxs-lookup"><span data-stu-id="4c659-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="4c659-117">Kiekis būtinai turi būti didesnis nei 24, kad įvykio „kanban“ taisyklė būtų paleista.</span><span class="sxs-lookup"><span data-stu-id="4c659-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="4c659-118">Atidaryti iškvietimo medį</span><span class="sxs-lookup"><span data-stu-id="4c659-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="4c659-119">Spustelėkite Produktas ir tiekimas.</span><span class="sxs-lookup"><span data-stu-id="4c659-119">Click Product and supply.</span></span>
2. <span data-ttu-id="4c659-120">Spustelėkite Peržiūrėti iškvietimo medį.</span><span class="sxs-lookup"><span data-stu-id="4c659-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="4c659-121">Atkreipkite dėmesį, kad iškvietimo medyje rodomi visi reikiami pardavimo užsakymo eilutės iškvietimo lygiai.</span><span class="sxs-lookup"><span data-stu-id="4c659-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="4c659-122">Šiuo atveju rodomi du „kanban“ lygiai ir visi būtini komponentai.</span><span class="sxs-lookup"><span data-stu-id="4c659-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="4c659-123">Planuoti iškvietimo medį</span><span class="sxs-lookup"><span data-stu-id="4c659-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="4c659-124">Medyje pasirinkite „Pardavimo eilutė 000832 \ „kanban“ 000558“.</span><span class="sxs-lookup"><span data-stu-id="4c659-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="4c659-125">Išplėskite sekciją „Kanban“ užduotys.</span><span class="sxs-lookup"><span data-stu-id="4c659-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="4c659-126">Atkreipkite dėmesį, kad „kanban“ užduoties būsena yra Nesuplanuota.</span><span class="sxs-lookup"><span data-stu-id="4c659-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="4c659-127">Spustelėkite Planuoti visą iškvietimo medį.</span><span class="sxs-lookup"><span data-stu-id="4c659-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="4c659-128">Šiuo būdu bus suplanuotos visos iškvietimo medžio „kanban“ taisyklės ir užduočių būsenos bus pakeistos iš Nesuplanuota į Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="4c659-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="4c659-129">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4c659-129">Refresh the page.</span></span>
    * <span data-ttu-id="4c659-130">Atkreipkite dėmesį, kad „kanban“ užduoties būsena iš Nesuplanuota pasikeitė į Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="4c659-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="4c659-131">Medyje pasirinkite „Pardavimo eilutė 000832 \ „Kanban“ 000558 \ Išdavimas, skirtas L0001 \ „Kanban“ 000559“.</span><span class="sxs-lookup"><span data-stu-id="4c659-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="4c659-132">Antroji „kanban“ taisyklė taip pat suplanuota, nes suplanuotas visas iškvietimo medis.</span><span class="sxs-lookup"><span data-stu-id="4c659-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="4c659-133">Atkreipkite dėmesį, kad „kanban“ užduoties būsena iš Nesuplanuota pasikeitė į Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="4c659-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

