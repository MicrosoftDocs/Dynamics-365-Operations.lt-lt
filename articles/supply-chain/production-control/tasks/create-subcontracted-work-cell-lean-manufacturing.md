--- 
title: "Kurti „lean manufacturing“ subrangovo darbo elementą"
description: "Norėdami modeliuoti subrangovo darbą „lean manufacturing“, turite sukurti darbo elementą, susietą su tiekėju, atliekančiu darbą."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="a7866-103">Kurti „lean manufacturing“ subrangovo darbo elementą</span><span class="sxs-lookup"><span data-stu-id="a7866-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7866-104">Norėdami modeliuoti subrangovo darbą „lean manufacturing“, turite sukurti darbo elementą, susietą su tiekėju, atliekančiu darbą.</span><span class="sxs-lookup"><span data-stu-id="a7866-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="a7866-105">Subrangovo darbo elementas yra susietas su tiekėju, susiejant tiekėjo tipo išteklių.</span><span class="sxs-lookup"><span data-stu-id="a7866-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="a7866-106">Jei leidžiate šį įrašą naudodami USMF demonstracinę įmonę, galite pasirinkti tiekėjo kodo ID 1002 ir 1 svetainę.</span><span class="sxs-lookup"><span data-stu-id="a7866-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="a7866-107">Sukurkite tiekėjo išteklių</span><span class="sxs-lookup"><span data-stu-id="a7866-107">Create a vendor resource</span></span>
1. <span data-ttu-id="a7866-108">Eikite į Ištekliai.</span><span class="sxs-lookup"><span data-stu-id="a7866-108">Go to Resources.</span></span>
2. <span data-ttu-id="a7866-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a7866-109">Click New.</span></span>
3. <span data-ttu-id="a7866-110">Lauke Išteklius surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a7866-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="a7866-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a7866-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a7866-112">Lauke Tipas pasirinkite „Tiekėjas“.</span><span class="sxs-lookup"><span data-stu-id="a7866-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="a7866-113">Lauke „Tiekėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="a7866-114">Sukurkite išteklių grupę</span><span class="sxs-lookup"><span data-stu-id="a7866-114">Create the resource group</span></span>
1. <span data-ttu-id="a7866-115">Eikite į Išteklių grupės.</span><span class="sxs-lookup"><span data-stu-id="a7866-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="a7866-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a7866-116">Click New.</span></span>
3. <span data-ttu-id="a7866-117">Lauke Išteklių grupės surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a7866-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="a7866-118">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a7866-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a7866-119">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a7866-120">Pasirinkti svetainę, kuriai turi būti priskirtas darbo elementas.</span><span class="sxs-lookup"><span data-stu-id="a7866-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="a7866-121">Teoriškai svetainė gali vaizduoti vieną svetainę, kurią valdo tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="a7866-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="a7866-122">Tačiau dauguma atvejų subrangos ištekliai yra tik paskirti svetainei, kuri užsako subrangos darbą.</span><span class="sxs-lookup"><span data-stu-id="a7866-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="a7866-123">Atkreipkite dėmesį, kad subrangovo darbo elementų įvesties ir išvesties sandėliai turi būti toje pačioje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="a7866-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="a7866-124">Lauke Teritorija surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a7866-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="a7866-125">Pažymėkite arba išvalykite žymės langelį „Darbo elementas“.</span><span class="sxs-lookup"><span data-stu-id="a7866-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="a7866-126">Lauke Įeigos sandėlis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a7866-127">Pasirinkite sandėlį ir vietą, kurios naudojamos medžiagai organizuoti tiekėjo valdomam darbo elementui.</span><span class="sxs-lookup"><span data-stu-id="a7866-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="a7866-128">Daugeliu atvejų sandėlis ir vieta modeliuojami naudojant atskirą kiekvieno tiekėjo sandėlį ir vieną vietą darbo elementui.</span><span class="sxs-lookup"><span data-stu-id="a7866-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="a7866-129">Lauke Įeigos vieta spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a7866-130">Lauke Išeigos sandėlis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a7866-131">Apibrėžkite sandėlį ir vietą, kur medžiaga užregistruota užregistravus darbo elemento subrangos veiklą.</span><span class="sxs-lookup"><span data-stu-id="a7866-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="a7866-132">Sandėlis ir vieta gali būti tiekėjo svetainėje, jei tiekėjas praneša apie „kanban“ užduotis.</span><span class="sxs-lookup"><span data-stu-id="a7866-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="a7866-133">Taip pat sandėlis ir vieta gali būti gavimo vieta, susieta su kitu gamybos eigos veiksmu.</span><span class="sxs-lookup"><span data-stu-id="a7866-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="a7866-134">Lauke Išeigos vieta spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a7866-135">Išplėskite arba sutraukite skyrių Kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="a7866-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="a7866-136">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a7866-136">Click Add.</span></span>
15. <span data-ttu-id="a7866-137">Lauke Kalendorius spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a7866-138">Susiekite darbo elemento darbo laiko kalendorių išteklių grupe.</span><span class="sxs-lookup"><span data-stu-id="a7866-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="a7866-139">Kritiniams ištekliams rekomenduojame apibrėžti konkrečius kalendorius, nurodančius tikslų darbo laiką ir susijusius darbo elemento arba tiekėjo svetainės pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="a7866-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="a7866-140">Išplėskite arba sutraukite sekciją Ištekliai.</span><span class="sxs-lookup"><span data-stu-id="a7866-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="a7866-141">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a7866-141">Click Add.</span></span>
    * <span data-ttu-id="a7866-142">Subrangos išteklių grupė turi turėti susietą tiekėjo tipo išteklių, kuris susieja išteklių grupę su tiekėjo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="a7866-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="a7866-143">Lauke Ištekliai spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a7866-144">Pasirinkite arba įveskite tiekėjo strategiją, kurią sukūrėte ankstesnėje papildomoje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="a7866-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="a7866-145">Išplėskite arba sutraukite skyrių Darbo elemento pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="a7866-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="a7866-146">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a7866-146">Click Add.</span></span>
    * <span data-ttu-id="a7866-147">Darbo elementas turi turėti apibrėžtą pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="a7866-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="a7866-148">Šiame pavyzdyje mes kuriame 100 vienetų per standartinę darbo dieną gamybos pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="a7866-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="a7866-149">Lauke Gamybos eigos modelis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="a7866-150">Lauke Pajėgumo laikotarpis pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="a7866-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="a7866-151">Lauke Vidutinis našumo kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a7866-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="a7866-152">Lauke Vienetas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a7866-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="a7866-153">„ResolveChanges“ Vienetas.</span><span class="sxs-lookup"><span data-stu-id="a7866-153">ResolveChanges the Unit.</span></span>


