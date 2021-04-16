---
title: Naujo sandėlio maketo kūrimas
description: Šioje temoje aprašoma, kaip nustatyti informaciją apie vietas sandėlyje.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a329df85c339c90e4bdc620c8a63837ebc19a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833982"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="0e8d7-103">Naujo sandėlio maketo kūrimas</span><span class="sxs-lookup"><span data-stu-id="0e8d7-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e8d7-104">Šioje temoje aprašoma, kaip nustatyti informaciją apie vietas sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="0e8d7-105">Tai taikoma tik tiems sandėliams, kurie sukurti naudojant funkciją „pagrindinis sandėliavimas‟, esančią modulyje Atsargų valdymas, o ne tiems, kurie sukurti modulyje Sandėlio valdymas.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="0e8d7-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="0e8d7-107">Nustatyti numatytuosius vietos pajėgumus</span><span class="sxs-lookup"><span data-stu-id="0e8d7-107">Set the default location capacity</span></span>
1. <span data-ttu-id="0e8d7-108">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų ir sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="0e8d7-109">Pažymėkite skirtuką **Vietos**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="0e8d7-110">Lauke **Standartinis plotis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="0e8d7-111">Lauke **Standartinis gylis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="0e8d7-112">Lauke **Standartinis aukštis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="0e8d7-113">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-113">Select **Save**.</span></span>
7. <span data-ttu-id="0e8d7-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="0e8d7-115">Nustatyti vietos pavadinimo formatą</span><span class="sxs-lookup"><span data-stu-id="0e8d7-115">Define the location name format</span></span>
1. <span data-ttu-id="0e8d7-116">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų paskirstymas > Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="0e8d7-117">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-117">Select **New**.</span></span>
3. <span data-ttu-id="0e8d7-118">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="0e8d7-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0e8d7-120">Lauke **Vieta** peržvalgoje pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="0e8d7-121">Perjunkite skyriaus **Vietos pavadinimai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="0e8d7-122">Parinktys šiame skyriuje nurodo numatytąjį vietos pavadinimų formatą.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="0e8d7-123">Savo pavyzdyje įtrauksime perėjimo numerį, stelažo numerį ir lentynos numerį.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="0e8d7-124">Pažymėkite parinktį **Įtraukti perėjimą** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="0e8d7-125">Pažymėkite parinktį **Įtraukti stelažą** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="0e8d7-126">Lauke **Formatas** įveskite stelažo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="0e8d7-127">Pažymėkite parinktį **Įtraukti lentyną** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="0e8d7-128">Lauke **Formatas** įveskite lentynos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="0e8d7-129">Nustatyti sandėlio vietas</span><span class="sxs-lookup"><span data-stu-id="0e8d7-129">Define warehouse locations</span></span>
1. <span data-ttu-id="0e8d7-130">Veiksmų srityje pažymėkite **Sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="0e8d7-131">Pažymėkite **Vietos vedlys**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="0e8d7-132">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-132">Select **Next**.</span></span>
4. <span data-ttu-id="0e8d7-133">Atžymėkite parinktį **Pakrovimo rampos**</span><span class="sxs-lookup"><span data-stu-id="0e8d7-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="0e8d7-134">Atžymėkite parinktį **Palaidų krovinių vietos**</span><span class="sxs-lookup"><span data-stu-id="0e8d7-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="0e8d7-135">Spauskite **Toliau**, kol galėsite pažymėti **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="0e8d7-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-136">Close the page.</span></span>
8. <span data-ttu-id="0e8d7-137">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0e8d7-137">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]