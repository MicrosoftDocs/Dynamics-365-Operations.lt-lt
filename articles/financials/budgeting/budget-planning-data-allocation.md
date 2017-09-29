---
title: "Biudžeto planavimo duomenų paskirstymas"
description: "Šiame straipsnyje aprašyti įvairūs paskirstymo metodai, kuriuos galima naudoti „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise“), ir kaip juos naudoti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: fd7ec30c8253f343b3d41d54c78696cd512b2ef7
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="5693d-103">Biudžeto planavimo duomenų paskirstymas</span><span class="sxs-lookup"><span data-stu-id="5693d-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5693d-104">Šiame straipsnyje aprašyti įvairūs paskirstymo metodai, kuriuos galima naudoti „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise“), ir kaip juos naudoti.</span><span class="sxs-lookup"><span data-stu-id="5693d-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and how they can be used.</span></span>  

<span data-ttu-id="5693d-105">Biudžeto plano duomenis galima paskirstyti keliais būdais, kad būtų tiksliai atvaizduojamos numatomos sumos.</span><span class="sxs-lookup"><span data-stu-id="5693d-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="5693d-106">Paskirstymo būdai</span><span class="sxs-lookup"><span data-stu-id="5693d-106">Allocation methods</span></span>
<span data-ttu-id="5693d-107">Naudojantis trimis paskirstymo būdais (Paskirstyti laikotarpiams, Paskirstyti dimensijoms ir Naudoti DK paskirstymo taisykles) galima sukurti biudžeto plano eilutes, kurios pagrįstos to paties biudžeto plano eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="5693d-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="5693d-108">Naudojantis trimis kitais būdais (Sujungti, Paskirstyti ir Kopijuoti iš biudžeto plano) galima sukurti biudžeto plano eilutes kituose biudžeto planuose.</span><span class="sxs-lookup"><span data-stu-id="5693d-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="5693d-109">Naudodami visus šešis paskirstymo būdus nurodote paskirties scenarijų.</span><span class="sxs-lookup"><span data-stu-id="5693d-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="5693d-110">Paskirties scenarijus gali būti toks pat kaip šaltinio scenarijus arba kitoks negu šaltinio scenarijus.</span><span class="sxs-lookup"><span data-stu-id="5693d-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="5693d-111">Be to, galite nurodyti, ar prie biudžeto plano prijungti naujas eilutes, ar pakeisti dabartines biudžeto plano eilutes.</span><span class="sxs-lookup"><span data-stu-id="5693d-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="5693d-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Paskirstyti laikotarpiams** – norint paskirstyti šaltinio biudžeto plano scenarijaus biudžeto plano eilutes paskirties scenarijaus laikotarpiams naudojama laikotarpio paskirstymo kategorija.</span><span class="sxs-lookup"><span data-stu-id="5693d-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="5693d-113">Šaltinio suma priskiriama kelioms paskirties scenarijaus eilutėms, priklausomai nuo laikotarpio paskirstymo kategorijoje nurodyto procento ir datos.</span><span class="sxs-lookup"><span data-stu-id="5693d-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="5693d-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Paskirstyti dimensijoms** – biudžeto plano eilutės iš šaltinio biudžeto planavimo scenarijaus paskirstomos į vieną ar kelias paskirties scenarijaus eilutes, priklausomai nuo pasirinktose biudžeto paskirstymo sąlygose nurodytų procentų ir finansinių dimensijų.</span><span class="sxs-lookup"><span data-stu-id="5693d-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="5693d-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Sujungti** – biudžeto plano eilutės sujungiamos iš šaltinio biudžeto plano scenarijaus susijusiuose (antriniuose) biudžeto planuose į paskirties scenarijų pirminiame biudžeto plane.</span><span class="sxs-lookup"><span data-stu-id="5693d-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="5693d-116">Naudojantis šiuo būdu galima naudoti tas biudžeto sumas, kurios žemesniame organizacijos lygyje yra paruoštos konsolidavimui aukštesniame lygyje.</span><span class="sxs-lookup"><span data-stu-id="5693d-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="5693d-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Paskirstyti** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto planavimo scenarijaus pirminiame biudžeto plane į paskirties scenarijų susijusiuose (antriniuose) biudžeto planuose, priklausomai nuo susijusių planų organizacijos vienetų finansinių dimensijų.</span><span class="sxs-lookup"><span data-stu-id="5693d-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="5693d-118">Naudojantis šiuo būdu galima naudoti tas biudžeto sumas, kurios aukštesniame organizacijos lygyje yra paruoštos labiau lokalizuotai peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="5693d-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="5693d-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Naudoti DK paskirstymo taisykles** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto plano scenarijaus į paskirties biudžeto plano scenarijų pagal pasirinktą DK paskirstymo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="5693d-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="5693d-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopijuoti iš biudžeto plano** – naudojant paskirstymo platinimo būdą biudžeto plano eilutės sukuriamos paskirtyje, priklausomai nuo susijusio biudžeto plano eilučių.</span><span class="sxs-lookup"><span data-stu-id="5693d-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="5693d-121">Tačiau naudojant šį būdą šaltinio biudžeto planas neturi būti pirminis, bet gali būti aukštesniame biudžeto plano hierarchijos lygmenyje.</span><span class="sxs-lookup"><span data-stu-id="5693d-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="5693d-122">Šis paskirstymo būdas naudingas, jei į biudžetą iš pradžių buvo įtrauktos daug aukštesnio lygio konsoliduotos sumos, kurios turi būti perkeltos į žemesnį organizacijos lygį, kad prieš joms gaunant aukštesnio lygio patvirtinimą būtų galima atlikti išsamią peržiūrą ir koreguoti.</span><span class="sxs-lookup"><span data-stu-id="5693d-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="5693d-123">Paskirstymo būdų naudojimas biudžeto plane</span><span class="sxs-lookup"><span data-stu-id="5693d-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="5693d-124">Norėdami atlikti paskirstymus biudžeto plano puslapyje, pasirinkite eilutes, kurias reikia paskirstyti, tada spustelėkite **Paskirstyti biudžetą**.</span><span class="sxs-lookup"><span data-stu-id="5693d-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="5693d-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="5693d-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="5693d-126">Po to pasirinkite paskirstymo būdą.</span><span class="sxs-lookup"><span data-stu-id="5693d-126">Next, select an allocation method.</span></span> <span data-ttu-id="5693d-127">Tada pagal jūsų pasirinktą metodą nustatomi likusieji laukai.</span><span class="sxs-lookup"><span data-stu-id="5693d-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="5693d-128">Šiuose laukuose nurodomas biudžeto plano duomenų šaltinis, paskirtis ir pasirinktis, kuri kuriant paskirties sumas leidžia padauginti šaltinį iš nurodyto koeficiento, kad būtų paprasčiau koreguoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="5693d-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="5693d-129">Taip pat galite nustatyti pasirinktį **Pridėti prie plano** .</span><span class="sxs-lookup"><span data-stu-id="5693d-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="5693d-130">Jeigu norite pakeisti esamas biudžeto plano eilutes, pasirinkite **Ne** arba, jeigu norite išsaugoti esamas biudžeto plano eilutes ir įtraukti naujų eilučių, skirtų paskirstytoms sumoms, pasirinkite  **Taip**.</span><span class="sxs-lookup"><span data-stu-id="5693d-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="5693d-131">Paskirstymų automatizavimas darbo eigos metu</span><span class="sxs-lookup"><span data-stu-id="5693d-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="5693d-132">Viena galinga funkcija leidžia paskirstymus atlikti automatiškai, kaip biudžeto planavimo darbo eigos dalį.</span><span class="sxs-lookup"><span data-stu-id="5693d-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="5693d-133">Vykstant biudžeto plano darbo eigai automatizuotos užduotys gali iškviesti nurodyto biudžeto planavimo etapo paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="5693d-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="5693d-134">Norėdami nustatyti automatinį paskirstymą, pirmiausia puslapyje **Biudžeto planavimo konfigūracija** turite sukurti paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="5693d-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="5693d-135">Paskirstymo grafike nurodomas paskirstymo būdas, kuris bus naudojamas vykdant automatinį paskirstymą, ir įvairių paskirstymo pasirinkčių (žr. jų aprašymus ankstesniame skyriuje) reikšmės.</span><span class="sxs-lookup"><span data-stu-id="5693d-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="5693d-136">Po to puslapyje **Biudžeto planavimo konfigūracija** sukurkite etapo paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="5693d-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="5693d-137">Etapo paskirstymas priskiria paskirstymo grafiką biudžeto planavimo darbo eigai ir etapui.</span><span class="sxs-lookup"><span data-stu-id="5693d-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="5693d-138">Galiausiai pridėkite norimo darbo eigos etapo biudžeto planavimo etapo paskirstymo automatizuotą užduotį.</span><span class="sxs-lookup"><span data-stu-id="5693d-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="5693d-139">Šiame pavyzdyje į darbo eigą įtraukti du biudžeto planavimo etapo paskirstymai (pažymėti raudonai).</span><span class="sxs-lookup"><span data-stu-id="5693d-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="5693d-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="5693d-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>



