---
title: Kurti numatytąją produkto ciklo būseną
description: Ši procedūra nurodo, kaip sukurti numatytąją produkto ciklo būseną, taip pat kaip susieti numatytąją būseną su išleistais produktais.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16f604d5e06859b15c6f610e7a5c822ef2089ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966910"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="7d198-103">Kurti numatytąją produkto ciklo būseną</span><span class="sxs-lookup"><span data-stu-id="7d198-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d198-104">Ši procedūra nurodo, kaip sukurti numatytąją produkto ciklo būseną, taip pat kaip susieti numatytąją būseną su išleistais produktais.</span><span class="sxs-lookup"><span data-stu-id="7d198-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="7d198-105">Kurti numatytąją ciklo būseną</span><span class="sxs-lookup"><span data-stu-id="7d198-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="7d198-106">Eikite į Produkto informacijos valdymas > Sąranka > Produkto ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="7d198-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="7d198-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7d198-107">Click New.</span></span>
3. <span data-ttu-id="7d198-108">Lauke Būsena įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="7d198-109">Lauke Numatytoji reikšmė, kai išduodama juridiniam subjektui pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="7d198-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="7d198-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="7d198-111">Lauke Suaktyvinta planavimui pažymėkite Ne.</span><span class="sxs-lookup"><span data-stu-id="7d198-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="7d198-112">Jei naujas išleistas produktas neturėtų būti įtrauktas į procesą Bendrasis planavimas, pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="7d198-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="7d198-113">Jei jis turėtų būti įtrauktas į procesą Bendrasis planavimas, palikite numatytąją valdiklio reikšmę Taip.</span><span class="sxs-lookup"><span data-stu-id="7d198-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="7d198-114">Kurti naują išleistą produktą</span><span class="sxs-lookup"><span data-stu-id="7d198-114">Create a new released product</span></span>
1. <span data-ttu-id="7d198-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7d198-115">Close the page.</span></span>
2. <span data-ttu-id="7d198-116">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="7d198-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="7d198-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7d198-117">Click New.</span></span>
4. <span data-ttu-id="7d198-118">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="7d198-119">Lauke Produkto pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="7d198-120">Lauke Ieškos pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="7d198-121">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="7d198-122">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7d198-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="7d198-123">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="7d198-124">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="7d198-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7d198-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="7d198-126">Numatytoji produkto ciklo būsena yra visuotinis apibrėžimas.</span><span class="sxs-lookup"><span data-stu-id="7d198-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="7d198-127">Keisti produkto būseną aktyvia</span><span class="sxs-lookup"><span data-stu-id="7d198-127">Change the product to an active state</span></span>
1. <span data-ttu-id="7d198-128">Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d198-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="7d198-129">Tarkime, kad nustatėte aktyvią būseną, todėl dabar galite pasirinkti tokią aktyvią būseną, kuri leistų naudoti produktą vykstant procesams Bendrasis planavimas ir Lygio KS skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="7d198-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="7d198-130">Žinoma, tai prasminga tik tuo atveju, jei nurodyta visa norint atlikti nuoseklų planavimą reikalinga produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="7d198-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

