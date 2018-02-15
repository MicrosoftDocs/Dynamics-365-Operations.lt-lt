--- 
title: "Kurti baigtą produktą (tik 2016 m. vasario mėn.)"
description: "Šios užduoties tikslas yra sukurti galutinį produktą."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 19cba700a2c96a09e0444c17323b8b2d4bf43f7d
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="8475d-103">Kurti baigtą produktą (tik 2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="8475d-103">Create a finished product (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8475d-104">Šios užduoties tikslas yra sukurti galutinį produktą.</span><span class="sxs-lookup"><span data-stu-id="8475d-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="8475d-105">Tai pirmoji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="8475d-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="8475d-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="8475d-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="8475d-107">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="8475d-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="8475d-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8475d-108">Click New.</span></span>
3. <span data-ttu-id="8475d-109">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="8475d-110">Norėdami demonstruoti, įveskite BOM_1.</span><span class="sxs-lookup"><span data-stu-id="8475d-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="8475d-111">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-112">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="8475d-112">Select STD.</span></span> <span data-ttu-id="8475d-113">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="8475d-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="8475d-114">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8475d-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-115">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="8475d-115">For example, select Audio.</span></span> <span data-ttu-id="8475d-116">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="8475d-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="8475d-117">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-118">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="8475d-118">Select SiteWH.</span></span> <span data-ttu-id="8475d-119">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="8475d-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="8475d-120">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-121">Šiame pavyzdyje sekimo dimensijos nenaudojamos; pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="8475d-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="8475d-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8475d-122">Click OK.</span></span>
9. <span data-ttu-id="8475d-123">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="8475d-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="8475d-124">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="8475d-124">Click Default order settings.</span></span>
11. <span data-ttu-id="8475d-125">Lauke „Numatytasis užsakymo tipas” pasirinkite „Gamyba”.</span><span class="sxs-lookup"><span data-stu-id="8475d-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="8475d-126">Kadangi tai galutinis produktas, kuris bus gaminamas, pasirinkite Gamyba.</span><span class="sxs-lookup"><span data-stu-id="8475d-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="8475d-127">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-128">Norėdami demonstruoti, pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="8475d-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="8475d-129">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-130">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="8475d-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="8475d-131">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8475d-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="8475d-132">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="8475d-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="8475d-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8475d-133">Close the page.</span></span>


