--- 
title: "Nebenaudojamų produktų variantų radimas"
description: "Šioje procedūroje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 402f387ac58d550037fbae2011b176c09f45185a
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="157da-103">Nebenaudojamų produktų variantų radimas</span><span class="sxs-lookup"><span data-stu-id="157da-103">Find obsolete product variants</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="157da-104">Šioje procedūroje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais.</span><span class="sxs-lookup"><span data-stu-id="157da-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="157da-105">Būtinoji sąlyga: prieš paleisdami šį užduočių vedlį turite nurodyti bent vieną produkto ciklo būseną, kuri yra neaktyvi planuojant.</span><span class="sxs-lookup"><span data-stu-id="157da-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="157da-106">Modeliavimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="157da-106">Run a simulation</span></span>
1. <span data-ttu-id="157da-107">Eikite į Produkto informacijos valdymas > Periodinės užduotys > Keisti pasenusių produktų ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="157da-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="157da-108">Lauke Naujo produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="157da-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="157da-109">Lauke Vykdyti modeliavimą nenaujinant produktų duomenų pažymėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="157da-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="157da-110">Lauke Neįtraukti produktų, sukurtų per ši dienų skaičių įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="157da-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="157da-111">Lauke Neįtraukti produktų, naudojamų operacijose (tam tikrą dienų skaičių) įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="157da-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="157da-112">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="157da-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="157da-113">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="157da-113">Click Filter.</span></span>
8. <span data-ttu-id="157da-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="157da-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="157da-115">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="157da-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="157da-116">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="157da-116">Click OK.</span></span>
11. <span data-ttu-id="157da-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="157da-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="157da-118">Jei ketinate ieškoti daug produktų, modeliavimą rekomenduojama atlikti pakete.</span><span class="sxs-lookup"><span data-stu-id="157da-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="157da-119">Taip pat įsitikinkite, kad modeliavimas neatliekamas aktyviausiu įmonės darbo metu.</span><span class="sxs-lookup"><span data-stu-id="157da-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="157da-120">Peržiūrėti modeliavimo rezultatus</span><span class="sxs-lookup"><span data-stu-id="157da-120">Review the simulation results</span></span>
1. <span data-ttu-id="157da-121">Eikite į Produkto informacijos valdymas > Užklausos ir ataskaitos > Produkto ciklo būsenos priežiūros istorija.</span><span class="sxs-lookup"><span data-stu-id="157da-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="157da-122">Šia puslapyje galite peržiūrėti modeliavimo rezultatus ir įvertinti, kiek produktų ir produkto variantų bus susieti su nauja produkto ciklo būsena vykdant naujinimą be modeliavimo.</span><span class="sxs-lookup"><span data-stu-id="157da-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="157da-123">Paleisti pasenusių produktų ciklo būsenos atnaujinimą</span><span class="sxs-lookup"><span data-stu-id="157da-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="157da-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="157da-124">Close the page.</span></span>
2. <span data-ttu-id="157da-125">Eikite į Produkto informacijos valdymas > Periodinės užduotys > Keisti pasenusių produktų ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="157da-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="157da-126">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="157da-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="157da-127">Atkreipkite dėmesį į tai, kad paskutinis pasirinkimas išsaugomas.</span><span class="sxs-lookup"><span data-stu-id="157da-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="157da-128">Lauke Vykdyti modeliavimą nenaujinant produktų duomenų pažymėkite Ne.</span><span class="sxs-lookup"><span data-stu-id="157da-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="157da-129">Išplėskite dalį Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="157da-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="157da-130">Priklausomai nuo to, kiek esama paveiktų produktų ir produkto variantų, apsvarstykite galimybę paleisti šią užduotį pakete.</span><span class="sxs-lookup"><span data-stu-id="157da-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="157da-131">Įsitikinkite, kad aktyviausiu įmonės darbo metu nevykdomos didelės apimties naujinimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="157da-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="157da-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="157da-132">Click OK.</span></span>
7. <span data-ttu-id="157da-133">Eikite į Produkto informacijos valdymas > Užklausos ir ataskaitos > Produkto ciklo būsenos priežiūros istorija.</span><span class="sxs-lookup"><span data-stu-id="157da-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="157da-134">Peržiūrėkite pakeistus ir išleistus produktus ir produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="157da-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="157da-135">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="157da-135">In the list, find and select the desired record.</span></span>


