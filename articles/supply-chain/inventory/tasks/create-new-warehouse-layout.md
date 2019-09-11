---
title: Naujo sandėlio maketo kūrimas
description: Šioje temoje aprašoma, kaip nustatyti informaciją apie vietas sandėlyje.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 302c028a93dfdb57972e4759abbbc4fdedabbd17
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867245"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="96fa9-103">Naujo sandėlio maketo kūrimas</span><span class="sxs-lookup"><span data-stu-id="96fa9-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96fa9-104">Šioje temoje aprašoma, kaip nustatyti informaciją apie vietas sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="96fa9-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="96fa9-105">Tai taikoma tik tiems sandėliams, kurie sukurti naudojant funkciją „pagrindinis sandėliavimas‟, esančią modulyje Atsargų valdymas, o ne tiems, kurie sukurti modulyje Sandėlio valdymas.</span><span class="sxs-lookup"><span data-stu-id="96fa9-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="96fa9-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="96fa9-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="96fa9-107">Nustatyti numatytuosius vietos pajėgumus</span><span class="sxs-lookup"><span data-stu-id="96fa9-107">Set the default location capacity</span></span>
1. <span data-ttu-id="96fa9-108">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų ir sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="96fa9-109">Pažymėkite skirtuką **Vietos**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="96fa9-110">Lauke **Standartinis plotis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="96fa9-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="96fa9-111">Lauke **Standartinis gylis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="96fa9-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="96fa9-112">Lauke **Standartinis aukštis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="96fa9-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="96fa9-113">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-113">Select **Save**.</span></span>
7. <span data-ttu-id="96fa9-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="96fa9-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="96fa9-115">Nustatyti vietos pavadinimo formatą</span><span class="sxs-lookup"><span data-stu-id="96fa9-115">Define the location name format</span></span>
1. <span data-ttu-id="96fa9-116">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų paskirstymas > Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="96fa9-117">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-117">Select **New**.</span></span>
3. <span data-ttu-id="96fa9-118">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="96fa9-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="96fa9-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="96fa9-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="96fa9-120">Lauke **Vieta** peržvalgoje pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="96fa9-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="96fa9-121">Perjunkite skyriaus **Vietos pavadinimai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="96fa9-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="96fa9-122">Parinktys šiame skyriuje nurodo numatytąjį vietos pavadinimų formatą.</span><span class="sxs-lookup"><span data-stu-id="96fa9-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="96fa9-123">Savo pavyzdyje įtrauksime perėjimo numerį, stelažo numerį ir lentynos numerį.</span><span class="sxs-lookup"><span data-stu-id="96fa9-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="96fa9-124">Pažymėkite parinktį **Įtraukti perėjimą** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="96fa9-125">Pažymėkite parinktį **Įtraukti stelažą** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="96fa9-126">Lauke **Formatas** įveskite stelažo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="96fa9-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="96fa9-127">Pažymėkite parinktį **Įtraukti lentyną** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="96fa9-128">Lauke **Formatas** įveskite lentynos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="96fa9-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="96fa9-129">Nustatyti sandėlio vietas</span><span class="sxs-lookup"><span data-stu-id="96fa9-129">Define warehouse locations</span></span>
1. <span data-ttu-id="96fa9-130">Veiksmų srityje pažymėkite **Sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="96fa9-131">Pažymėkite **Vietos vedlys**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="96fa9-132">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-132">Select **Next**.</span></span>
4. <span data-ttu-id="96fa9-133">Atžymėkite parinktį **Pakrovimo rampos** </span><span class="sxs-lookup"><span data-stu-id="96fa9-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="96fa9-134">Atžymėkite parinktį **Palaidų krovinių vietos** </span><span class="sxs-lookup"><span data-stu-id="96fa9-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="96fa9-135">Spauskite **Toliau**, kol galėsite pažymėti **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="96fa9-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="96fa9-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="96fa9-136">Close the page.</span></span>
8. <span data-ttu-id="96fa9-137">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="96fa9-137">Refresh the page.</span></span>

