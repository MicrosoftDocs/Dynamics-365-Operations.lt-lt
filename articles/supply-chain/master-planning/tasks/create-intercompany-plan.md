---
title: Kurti vidinės įmonės planą
description: Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433453"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="a6674-103">Kurti vidinės įmonės planą</span><span class="sxs-lookup"><span data-stu-id="a6674-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6674-104">Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.</span><span class="sxs-lookup"><span data-stu-id="a6674-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="a6674-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a6674-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="a6674-106">Vidinės įmonės planavimo grupės nustatymas</span><span class="sxs-lookup"><span data-stu-id="a6674-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="a6674-107">**Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Sąranka > Vidinės įmonės planavimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="a6674-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="a6674-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="a6674-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a6674-109">Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.</span><span class="sxs-lookup"><span data-stu-id="a6674-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="a6674-110">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6674-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a6674-111">Spustelėkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="a6674-111">Click **Delete**.</span></span> <span data-ttu-id="a6674-112">Šis veiksmas yra būtinas, norint sutrumpinti vidinės įmonės planavimą.</span><span class="sxs-lookup"><span data-stu-id="a6674-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="a6674-113">Vidinės įmonės planavimo procesas vykdys bendrąjį planavimą visose planavimo grupės įmonėse, pradedant nuo žemiausio planavimo sekos.</span><span class="sxs-lookup"><span data-stu-id="a6674-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="a6674-114">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a6674-114">Click **Yes**.</span></span>
6. <span data-ttu-id="a6674-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6674-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="a6674-116">Vidinės įmonės plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="a6674-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="a6674-117">**Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Darbo sritys > Pagrindinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="a6674-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="a6674-118">Spustelėkite **Vidinės įmonės pagrindinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="a6674-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="a6674-119">Lauke **Vidinės įmonės planavimo grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a6674-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a6674-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a6674-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="a6674-121">Pasirinkite 10 vidinės įmonės planavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="a6674-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="a6674-122">Lauke **Vidinės įmonės planavimo derinių skaičius** įveskite „2“.</span><span class="sxs-lookup"><span data-stu-id="a6674-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="a6674-123">10 vidinės įmonės planavimo grupėje yra du nariai.</span><span class="sxs-lookup"><span data-stu-id="a6674-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="a6674-124">Norėdami atidėjimus perduoti iš šaltinio įmonės (USMF) į kliento įmonę (DEMF), turėsite vykdyti vidinės įmonę abiejose įmonėse du kartus.</span><span class="sxs-lookup"><span data-stu-id="a6674-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="a6674-125">Vykdant pirmąjį kartojimą bus perduotas poreikis ir nustatyti atidėjimai šaltinio įmonėje (USMF).</span><span class="sxs-lookup"><span data-stu-id="a6674-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="a6674-126">Vykdant antrąjį kartojimą atidėjimai bus perduoti iš USMF į DEMF.</span><span class="sxs-lookup"><span data-stu-id="a6674-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="a6674-127">Lauke **Pirmas derinys** pažymėkite Regeneravimas.</span><span class="sxs-lookup"><span data-stu-id="a6674-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="a6674-128">Lauke **Kiti deriniai** pažymėkite Regeneravimas.</span><span class="sxs-lookup"><span data-stu-id="a6674-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="a6674-129">Lauke **Gijų skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a6674-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="a6674-130">Tai nurodo lygiagrečių gijų, naudojamų planuojant, skaičių.</span><span class="sxs-lookup"><span data-stu-id="a6674-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="a6674-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a6674-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="a6674-132">Plano rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a6674-132">View the result of the plan</span></span>
1. <span data-ttu-id="a6674-133">Lauke **Planas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a6674-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a6674-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a6674-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="a6674-135">Spustelėkite StaticPlan saitą.</span><span class="sxs-lookup"><span data-stu-id="a6674-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="a6674-136">Turite būti įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="a6674-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="a6674-137">Spustelėkite **Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a6674-137">Click **Planned orders**.</span></span>

