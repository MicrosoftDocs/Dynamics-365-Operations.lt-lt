---
title: Produktų klasifikacijų hierarchijos kūrimas
description: Ši procedūra nurodo, kaip sukurti naują kategorijų hierarchiją ir priskirti prekių kodų hierarchijos tipą.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ff1a2ba20059d3fcb0347220e6e81130e03ac0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203738"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="6b7d2-103">Produktų klasifikacijų hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="6b7d2-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b7d2-104">Ši procedūra nurodo, kaip sukurti naują kategorijų hierarchiją ir priskirti prekių kodų hierarchijos tipą.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="6b7d2-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6b7d2-106">Ši procedūra skirta kategorijų vadovui.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="6b7d2-107">Kurti naują kategorijų hierarchiją</span><span class="sxs-lookup"><span data-stu-id="6b7d2-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="6b7d2-108">Pasirinkite **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Sąranka > Kategorijos ir atributai > Kategorijų hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="6b7d2-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-109">Click **New**.</span></span>
3. <span data-ttu-id="6b7d2-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="6b7d2-111">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6b7d2-112">Spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="6b7d2-113">Kurti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="6b7d2-113">Build the hierarchy</span></span>
1. <span data-ttu-id="6b7d2-114">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-114">Click **New** category node.</span></span>
2. <span data-ttu-id="6b7d2-115">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="6b7d2-116">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="6b7d2-117">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="6b7d2-118">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-118">Click **New** category node.</span></span>
6. <span data-ttu-id="6b7d2-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="6b7d2-120">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="6b7d2-121">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="6b7d2-122">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-122">Click **New** category node.</span></span>
10. <span data-ttu-id="6b7d2-123">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="6b7d2-124">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="6b7d2-125">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="6b7d2-126">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-126">Click **New** category node.</span></span>
14. <span data-ttu-id="6b7d2-127">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="6b7d2-128">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="6b7d2-129">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="6b7d2-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="6b7d2-131">Klasifikuoti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="6b7d2-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="6b7d2-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="6b7d2-133">Lauke **Veiksmų sritis** spustelėkite **Kategorijų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="6b7d2-134">Spustelėkite **Susieti hierarchijos tipą**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="6b7d2-135">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-135">Click **New**.</span></span>
5. <span data-ttu-id="6b7d2-136">Lauke **Kategorijų hierarchijos tipas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="6b7d2-137">Pasirinkite **Prekių kodų kategorijų hierarchijos tipas, skirtas produktų klasifikacijai**.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="6b7d2-138">Lauke **Kategorijų hierarchija** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6b7d2-139">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6b7d2-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6b7d2-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6b7d2-141">Close the page.</span></span>

