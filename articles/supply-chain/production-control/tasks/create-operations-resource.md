---
title: Kurti operacijų išteklių
description: Operacijų išteklius atlieka projekto arba gamybos proceso veiklas.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 514b0b27065b4318891a84f364b39e8e378d6a4a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255090"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="bcfba-103">Kurti operacijų išteklių</span><span class="sxs-lookup"><span data-stu-id="bcfba-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcfba-104">Operacijų išteklius atlieka projekto arba gamybos proceso veiklas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="bcfba-105">Ši procedūra rodo, kaip apibrėžti operacijų išteklių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="bcfba-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="bcfba-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="bcfba-107">Eikite į Ištekliai.</span><span class="sxs-lookup"><span data-stu-id="bcfba-107">Go to Resources.</span></span>
2. <span data-ttu-id="bcfba-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-108">Click New.</span></span>
3. <span data-ttu-id="bcfba-109">Lauke Išteklius surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="bcfba-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="bcfba-111">Apibrėžti pajėgumų ir suvartojimo parametrus</span><span class="sxs-lookup"><span data-stu-id="bcfba-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="bcfba-112">Išplėskite skyrių Operacija.</span><span class="sxs-lookup"><span data-stu-id="bcfba-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="bcfba-113">Lauke Atliekų procentinė dalis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="bcfba-114">Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfba-115">Nurodykite išlaidų kategoriją, kuri apibrėžia, kaip paaiškinti nustatymo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="bcfba-116">Lauke Apdorojimo laiko kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfba-117">Nurodykite išlaidų kategoriją, kuri apibrėžia, kaip paaiškinti vykdymo laiko išlaidas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="bcfba-118">Lauke Kiekio kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfba-119">Nurodykite išlaidų kategoriją, kuri apibrėžia, kaip paaiškinti išteklių išlaidas pagal išeigos kiekį.</span><span class="sxs-lookup"><span data-stu-id="bcfba-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="bcfba-120">Lauke Pajėgumo vienetas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bcfba-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="bcfba-121">Nurodykite vienetą, kuriuo išreikšti operacijų ištekliaus pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="bcfba-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="bcfba-122">Lauke Pajėgumas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="bcfba-123">Lauke Efektyvumo procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="bcfba-124">Nurodykite efektyvumą, kurio tikitės iš operacijų ištekliaus.</span><span class="sxs-lookup"><span data-stu-id="bcfba-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="bcfba-125">Efektyvumo procentas reguliuoja operacijų ištekliaus našumą ir veikia ištekliui rezervuotą laiką.</span><span class="sxs-lookup"><span data-stu-id="bcfba-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="bcfba-126">Lauke Operacijų planavimo procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="bcfba-127">Nurodykite maksimalų operacijos ištekliaus pajėgumo procentą, kurį norite naudoti planuodami operacijas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="bcfba-128">Lauke Ribotas pajėgumas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="bcfba-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="bcfba-129">Jei operacijos išteklius turėtų būti planuojamas pagal faktinį turimą pajėgumą ir jei reikia atsižvelgti į esamų pajėgumų rezervavimus, šią parinktį nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="bcfba-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="bcfba-130">Jei ši parinktis nustatyta į Ne, daroma prielaida, kad operacijos ištekliaus pajėgumas yra neribotas, ir šis išteklius gali būti perpildytas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="bcfba-131">Lauke Ribotosios spartos išteklius pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="bcfba-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="bcfba-132">Apibrėžti darbo laikus</span><span class="sxs-lookup"><span data-stu-id="bcfba-132">Define working times</span></span>
1. <span data-ttu-id="bcfba-133">Išplėskite skyrių Kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="bcfba-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="bcfba-134">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bcfba-134">Click Add.</span></span>
3. <span data-ttu-id="bcfba-135">Lauke Kalendorius įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfba-136">Nurodykite darbo laiko kalendorių, apibrėžiantį ištekliaus pajėgumą (valandomis).</span><span class="sxs-lookup"><span data-stu-id="bcfba-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="bcfba-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bcfba-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bcfba-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bcfba-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="bcfba-139">Apibrėžkite išteklių galimybės</span><span class="sxs-lookup"><span data-stu-id="bcfba-139">Define resource capabilities</span></span>
1. <span data-ttu-id="bcfba-140">Išplėskite dalį Pajėgumai.</span><span class="sxs-lookup"><span data-stu-id="bcfba-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="bcfba-141">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bcfba-141">Click Add.</span></span>
    * <span data-ttu-id="bcfba-142">Pajėgumas yra operacijų ištekliaus gebėjimas atlikti tam tikrą veiklą.</span><span class="sxs-lookup"><span data-stu-id="bcfba-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="bcfba-143">Planavimo mechanizmas išteklius paskirsto derindamas kiekvienos veiklos išteklių poreikius ir turimų operacijų išteklių pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="bcfba-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="bcfba-144">Lauke Pajėgumas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="bcfba-145">Lauke Lygis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="bcfba-146">Nurodykite įgudimo lygį, kuriuo išteklius apdoroja pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="bcfba-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="bcfba-147">Lauke Prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bcfba-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="bcfba-148">Nurodykite operacijų ištekliaus prioritetą pajėgumo atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="bcfba-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="bcfba-149">Planuojant pagal prioritetą, pirmiausia pasirenkamas operacijų išteklius, kurio prioritetas aukščiausias (mažiausia skaitinė reikšmė).</span><span class="sxs-lookup"><span data-stu-id="bcfba-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="bcfba-150">Priskirti išteklių išteklių grupei</span><span class="sxs-lookup"><span data-stu-id="bcfba-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="bcfba-151">Išplėskite dalį Išteklių grupės.</span><span class="sxs-lookup"><span data-stu-id="bcfba-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="bcfba-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bcfba-152">Click Add.</span></span>
    * <span data-ttu-id="bcfba-153">Išteklių grupė apibrėžia operacijų ištekliaus teritoriją, gamybos vienetą ir sandėlio kontekstą.</span><span class="sxs-lookup"><span data-stu-id="bcfba-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="bcfba-154">Operacijų išteklių planuoti galima tik kai jis priskirtas išteklių grupei ir tik toje teritorijoje, kurioje išteklių grupė yra.</span><span class="sxs-lookup"><span data-stu-id="bcfba-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="bcfba-155">Lauke Išteklių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="bcfba-156">Lauke Įvesties vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcfba-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="bcfba-157">Nurodykite sandėlio vietą, iš kurios operacijų išteklius vartoja medžiagas.</span><span class="sxs-lookup"><span data-stu-id="bcfba-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]