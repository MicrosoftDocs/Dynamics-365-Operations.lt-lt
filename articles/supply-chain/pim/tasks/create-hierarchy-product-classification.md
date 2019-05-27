---
title: Produktų klasifikacijų hierarchijos kūrimas
description: Ši procedūra nurodo, kaip sukurti naują kategorijų hierarchiją ir priskirti prekių kodų hierarchijos tipą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568425"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="87052-103">Produktų klasifikacijų hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="87052-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87052-104">Ši procedūra nurodo, kaip sukurti naują kategorijų hierarchiją ir priskirti prekių kodų hierarchijos tipą.</span><span class="sxs-lookup"><span data-stu-id="87052-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="87052-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="87052-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="87052-106">Ši procedūra skirta kategorijų vadovui.</span><span class="sxs-lookup"><span data-stu-id="87052-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="87052-107">Kurti naują kategorijų hierarchiją</span><span class="sxs-lookup"><span data-stu-id="87052-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="87052-108">Pasirinkite Produkto informacijos valdymas > Nustatymas > Kategorijos ir atributai > Kategorijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="87052-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="87052-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87052-109">Click New.</span></span>
3. <span data-ttu-id="87052-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="87052-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="87052-112">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="87052-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="87052-113">Kurti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="87052-113">Build the hierarchy</span></span>
1. <span data-ttu-id="87052-114">Spustelėkite „Naujas kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="87052-114">Click New category node.</span></span>
2. <span data-ttu-id="87052-115">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="87052-116">Lauke „Kodas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="87052-117">Lauke „Patogus pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="87052-118">Spustelėkite „Naujas kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="87052-118">Click New category node.</span></span>
6. <span data-ttu-id="87052-119">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="87052-120">Lauke „Kodas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="87052-121">Lauke „Patogus pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="87052-122">Spustelėkite „Naujas kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="87052-122">Click New category node.</span></span>
10. <span data-ttu-id="87052-123">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="87052-124">Lauke „Kodas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="87052-125">Lauke „Patogus pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="87052-126">Spustelėkite „Naujas kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="87052-126">Click New category node.</span></span>
14. <span data-ttu-id="87052-127">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="87052-128">Lauke „Kodas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="87052-129">Lauke „Patogus pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87052-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="87052-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="87052-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="87052-131">Klasifikuoti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="87052-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="87052-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="87052-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="87052-133">Veiksmų srityje spustelėkite „Kategorijų hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="87052-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="87052-134">Spustelėkite „Susieti hierarchijos tipą“.</span><span class="sxs-lookup"><span data-stu-id="87052-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="87052-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87052-135">Click New.</span></span>
5. <span data-ttu-id="87052-136">Lauke „Kategorijų hierarchijos tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="87052-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="87052-137">Pasirinkite prekių kodų kategorijų hierarchijos tipą, skirtą produktų klasifikacijai.</span><span class="sxs-lookup"><span data-stu-id="87052-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="87052-138">Lauke „Kategorijų hierarchija“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="87052-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="87052-139">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="87052-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="87052-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="87052-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="87052-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="87052-141">Close the page.</span></span>

