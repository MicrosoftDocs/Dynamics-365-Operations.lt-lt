---
title: "Kurti naują sandėlio maketą"
description: "Ši procedūra rodo, kaip nustatyti informaciją apie sandėlio vietas."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="9d0c8-103">Kurti naują sandėlio maketą</span><span class="sxs-lookup"><span data-stu-id="9d0c8-103">Create a new warehouse layout</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d0c8-104">Ši procedūra rodo, kaip nustatyti informaciją apie sandėlio vietas.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="9d0c8-105">Tai taikoma tik tiems sandėliams, kurie sukurti naudojant funkciją „pagrindinis sandėliavimas‟, esančią modulyje Atsargų valdymas, o ne tiems, kurie sukurti modulyje Sandėlio valdymas.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="9d0c8-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="9d0c8-107">Nustatyti numatytuosius vietos pajėgumus</span><span class="sxs-lookup"><span data-stu-id="9d0c8-107">Set the default location capacity</span></span>
1. <span data-ttu-id="9d0c8-108">Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="9d0c8-109">Spustelėkite skirtuką Vietos.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="9d0c8-110">Lauke Standartinis plotis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="9d0c8-111">Lauke Standartinis gylis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="9d0c8-112">Lauke Standartinis aukštis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="9d0c8-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-113">Click Save.</span></span>
7. <span data-ttu-id="9d0c8-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="9d0c8-115">Nustatyti vietos pavadinimo formatą</span><span class="sxs-lookup"><span data-stu-id="9d0c8-115">Define the location name format</span></span>
1. <span data-ttu-id="9d0c8-116">Eikite į Atsargų valdymas > Nustatymas > Atsargų paskirstymas > Sandėliai.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="9d0c8-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-117">Click New.</span></span>
3. <span data-ttu-id="9d0c8-118">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="9d0c8-119">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9d0c8-120">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9d0c8-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9d0c8-122">Perjunkite sekcijos Vietų pavadinimai išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="9d0c8-123">Parinktys šiame skyriuje nurodo numatytąjį vietos pavadinimų formatą.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="9d0c8-124">Savo pavyzdyje įtrauksime perėjimo numerį, stelažo numerį ir lentynos numerį.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="9d0c8-125">Parinktį Įtraukti perėjimą nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="9d0c8-126">Parinktį Įtraukti stelažą nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="9d0c8-127">Stelažo lauke Formatas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="9d0c8-128">Pavyzdžiui: -##</span><span class="sxs-lookup"><span data-stu-id="9d0c8-128">For example: -##</span></span>  
11. <span data-ttu-id="9d0c8-129">Parinktį Įtraukti lentyną nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="9d0c8-130">Lentynos lauke Formatas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="9d0c8-131">Pavyzdžiui: -##</span><span class="sxs-lookup"><span data-stu-id="9d0c8-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="9d0c8-132">Nustatyti sandėlio vietas</span><span class="sxs-lookup"><span data-stu-id="9d0c8-132">Define warehouse locations</span></span>
1. <span data-ttu-id="9d0c8-133">Veiksmų srityje spustelėkite Sandėlis.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="9d0c8-134">Spustelėkite Vietų vedlys.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="9d0c8-135">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-135">Click Next.</span></span>
4. <span data-ttu-id="9d0c8-136">Atžymėkite parinktį Pakrovimo rampos</span><span class="sxs-lookup"><span data-stu-id="9d0c8-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="9d0c8-137">Atžymėkite parinktį Buferinės vietos</span><span class="sxs-lookup"><span data-stu-id="9d0c8-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="9d0c8-138">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-138">Click Next.</span></span>
7. <span data-ttu-id="9d0c8-139">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-139">Click Next.</span></span>
8. <span data-ttu-id="9d0c8-140">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-140">Click Next.</span></span>
9. <span data-ttu-id="9d0c8-141">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-141">Click Next.</span></span>
10. <span data-ttu-id="9d0c8-142">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-142">Click Next.</span></span>
11. <span data-ttu-id="9d0c8-143">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-143">Click Next.</span></span>
12. <span data-ttu-id="9d0c8-144">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-144">Click Next.</span></span>
    * <span data-ttu-id="9d0c8-145">Nepamirškite, kad faktinės dimensijos, rodomos šiame puslapyje, yra tos, kurias nustatote šios procedūros pradžioje.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="9d0c8-146">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-146">Click Next.</span></span>
14. <span data-ttu-id="9d0c8-147">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-147">Click Finish.</span></span>
15. <span data-ttu-id="9d0c8-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-148">Close the page.</span></span>
16. <span data-ttu-id="9d0c8-149">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9d0c8-149">Refresh the page.</span></span>

