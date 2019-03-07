---
title: Dalinis vietos ciklų skaičiavimas
description: Faktinės skaičiavimo operacijos valdomos pagal ciklo skaičiavimo planus. Galite reikalauti, kad būtų skaičiuojamos ne visos vietoje turimos atsargos, o tik konkretūs produktai ir produkto variantai.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "320655"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="9a742-104">Dalinis vietos ciklų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9a742-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a742-105">Faktinės skaičiavimo operacijos valdomos pagal ciklo skaičiavimo planus.</span><span class="sxs-lookup"><span data-stu-id="9a742-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="9a742-106">Galite reikalauti, kad būtų skaičiuojamos ne visos vietoje turimos atsargos, o tik konkretūs produktai ir produkto variantai.</span><span class="sxs-lookup"><span data-stu-id="9a742-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="9a742-107">Naudodami ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite valdyti faktines skaičiavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="9a742-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="9a742-108">Galite reikalauti, kad būtų skaičiuojamos ne visos vietoje turimos atsargos, o tik konkretūs produktai ir produkto variantai.</span><span class="sxs-lookup"><span data-stu-id="9a742-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="9a742-109">Filtruodamas konkrečius produktus, sandėlio vadovas gali sumažinti peržiūros pridėtines išlaidas, išvengti konsolidavimo klaidų ir sutaupyti laiko.</span><span class="sxs-lookup"><span data-stu-id="9a742-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="9a742-110">Kaip konfigūruoti dalinį vietos ciklo skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="9a742-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="9a742-111">Skaičiavimo operacijoms naudojant sandėlio darbo procesą, kiekvienai vietai sukuriama darbo antraštė.</span><span class="sxs-lookup"><span data-stu-id="9a742-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="9a742-112">Kai nustatote ciklo skaičiavimo planą, galite naudoti užklausą **Pasirinkti vietas**, kad apribotumėte sukurtą ciklo skaičiavimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9a742-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="9a742-113">Kai pasirenkate ciklo skaičiavimo plano produktus, galite pasirinkti produkto ir produkto varianto užklausas, kad patikslintumėte, kas yra skaičiuojama.</span><span class="sxs-lookup"><span data-stu-id="9a742-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="9a742-114">**Darbo šabloną** galite susieti su ciklo skaičiavimo planu, kad nurodytumėte, kaip turi būti sukurtas ciklo skaičiavimo darbas.</span><span class="sxs-lookup"><span data-stu-id="9a742-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="9a742-115">Tiesioginė nuoroda į skaičiavimo operacijoms skirtą darbo šabloną pateikta ciklo skaičiavimo plane.</span><span class="sxs-lookup"><span data-stu-id="9a742-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="9a742-116">Kai apibrėžiate darbo šablono informaciją, galite naudoti parinktį **Darbo eilučių lūžiai**, kad nurodytumėte, ar skaičiavimo darbo eilutės turi būti grupuojamos pagal prekės numerį ar produkto varianto numerį.</span><span class="sxs-lookup"><span data-stu-id="9a742-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="9a742-117">Ši sąranka būtina, jei norite skaičiuoti tik vietoje turimas konkrečių produktų atsargas.</span><span class="sxs-lookup"><span data-stu-id="9a742-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="9a742-118">Sukurtos ciklo skaičiavimo darbo eilutės turės čia nustatytą informacijos lygį, ir valdomos skaičiavimo operacijos bus vykdomos pagal šį lygį.</span><span class="sxs-lookup"><span data-stu-id="9a742-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="9a742-119">Jei susiesite ciklo skaičiavimo planus su darbo šablonais naudodami parinktį **Darbo eilučių lūžiai**, sukurtam ciklo skaičiavimo darbui bus pasirinktas laukas **Dalinis ciklo skaičiavimas**, ir bus sukurtos kelios ciklo skaičiavimo darbo eilutės pagal darbo šablono aprašą.</span><span class="sxs-lookup"><span data-stu-id="9a742-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="9a742-120">Prieš apdorojant dalinį ciklo skaičiavimo darbą, turite bent jau pasirinkti **Rodyti prekės numerį** mobiliojo įrenginio meniu elementui skaičiavimo sąrankos metu.</span><span class="sxs-lookup"><span data-stu-id="9a742-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="9a742-121">Sandėlio operatorius bus paprašytas įrašyti tik skaičiavimo informaciją, susijusią su inventorizacijos eilutėmis (prekių numeriai ir produkto dimensijos).</span><span class="sxs-lookup"><span data-stu-id="9a742-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="9a742-122">Šio skaičiavimo proceso metu visų kitų turimų atsargų bus nepaisoma.</span><span class="sxs-lookup"><span data-stu-id="9a742-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="9a742-123">Dalinio ciklo skaičiavimo proceso atveju vietos **paskutinio ciklo skaičiavimo** data / laikas nebus atnaujinami.</span><span class="sxs-lookup"><span data-stu-id="9a742-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="9a742-124">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9a742-124">Example</span></span>
<span data-ttu-id="9a742-125">Pavyzdžiui, 61 sandėlyje turi būti skaičiuojamas tik prekės numeris A0001.</span><span class="sxs-lookup"><span data-stu-id="9a742-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="9a742-126">Sukuriamas naujas ciklo skaičiavimo darbo šablonas.</span><span class="sxs-lookup"><span data-stu-id="9a742-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="9a742-127">Parinktis **Darbo eilučių lūžiai** naudojama skaičiavimo darbo eilutėms grupuoti pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="9a742-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="9a742-128">Todėl sukurtas ciklo skaičiavimo darbas turės eilutes pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="9a742-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="9a742-129">Eilutes taip pat galite grupuoti pagal produkto varianto numerį.</span><span class="sxs-lookup"><span data-stu-id="9a742-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="9a742-130">Sukuriamas naujo ciklo skaičiavimo planas, kuriame pateikiama nuoroda į naujai sukurtą darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="9a742-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="9a742-131">Ciklo skaičiavimo planas apima visas 61 sandėlyje esančias vietas (užklausa **Pasirinkti vietas**), kuriose yra atsargų pagal prekės numerį A0001.</span><span class="sxs-lookup"><span data-stu-id="9a742-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="9a742-132">Konkrečių produktų pasirinkimas nurodytas skyriuje **Ciklo skaičiavimo produktų pasirinkimas**.</span><span class="sxs-lookup"><span data-stu-id="9a742-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="9a742-133">Galite pasirinkti ciklo skaičiavimo planų produktus, nustatydami lauką **Tuščios vietos** į **Neįtraukti tuščių**.</span><span class="sxs-lookup"><span data-stu-id="9a742-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="9a742-134">Apdorojus ciklo skaičiavimo planą, sukuriamas dalinis ciklo skaičiavimo darbas prekės numeriui A0001.</span><span class="sxs-lookup"><span data-stu-id="9a742-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="9a742-135">Faktinis skaičiavimo procesas gali būti atliekamas naudojant mobiliojo įrenginio meniu elementą, skirtą valdomam ciklo skaičiavimui.</span><span class="sxs-lookup"><span data-stu-id="9a742-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="9a742-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9a742-136">Additional resources</span></span>
--------

[<span data-ttu-id="9a742-137">Ciklų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9a742-137">Cycle counting</span></span>](cycle-counting.md)

