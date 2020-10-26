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
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986196"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="53170-103">Produktų klasifikacijų hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="53170-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53170-104">Ši procedūra nurodo, kaip sukurti naują kategorijų hierarchiją ir priskirti prekių kodų hierarchijos tipą.</span><span class="sxs-lookup"><span data-stu-id="53170-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="53170-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="53170-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="53170-106">Ši procedūra skirta kategorijų vadovui.</span><span class="sxs-lookup"><span data-stu-id="53170-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="53170-107">Kurti naują kategorijų hierarchiją</span><span class="sxs-lookup"><span data-stu-id="53170-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="53170-108">Pasirinkite **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Sąranka > Kategorijos ir atributai > Kategorijų hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="53170-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="53170-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="53170-109">Click **New**.</span></span>
3. <span data-ttu-id="53170-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="53170-111">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="53170-112">Spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="53170-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="53170-113">Kurti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="53170-113">Build the hierarchy</span></span>
1. <span data-ttu-id="53170-114">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="53170-114">Click **New** category node.</span></span>
2. <span data-ttu-id="53170-115">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="53170-116">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="53170-117">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="53170-118">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="53170-118">Click **New** category node.</span></span>
6. <span data-ttu-id="53170-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="53170-120">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="53170-121">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="53170-122">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="53170-122">Click **New** category node.</span></span>
10. <span data-ttu-id="53170-123">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="53170-124">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="53170-125">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="53170-126">Spustelėkite kategorijos mazgą **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="53170-126">Click **New** category node.</span></span>
14. <span data-ttu-id="53170-127">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="53170-128">Lauke **Kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="53170-129">Lauke **Patogus pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53170-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="53170-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="53170-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="53170-131">Klasifikuoti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="53170-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="53170-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="53170-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="53170-133">Lauke **Veiksmų sritis** spustelėkite **Kategorijų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="53170-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="53170-134">Spustelėkite **Susieti hierarchijos tipą**.</span><span class="sxs-lookup"><span data-stu-id="53170-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="53170-135">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="53170-135">Click **New**.</span></span>
5. <span data-ttu-id="53170-136">Lauke **Kategorijų hierarchijos tipas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="53170-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="53170-137">Pasirinkite **Prekių kodų kategorijų hierarchijos tipas, skirtas produktų klasifikacijai**.</span><span class="sxs-lookup"><span data-stu-id="53170-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="53170-138">Lauke **Kategorijų hierarchija** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="53170-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="53170-139">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="53170-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="53170-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="53170-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="53170-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="53170-141">Close the page.</span></span>

