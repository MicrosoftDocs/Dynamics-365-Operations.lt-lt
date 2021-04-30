---
title: Kurti vidinės įmonės planą
description: Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867355"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="3a890-103">Kurti vidinės įmonės planą</span><span class="sxs-lookup"><span data-stu-id="3a890-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a890-104">Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.</span><span class="sxs-lookup"><span data-stu-id="3a890-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="3a890-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="3a890-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="3a890-106">Vidinės įmonės planavimo grupės nustatymas</span><span class="sxs-lookup"><span data-stu-id="3a890-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="3a890-107">**Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Sąranka > Vidinės įmonės planavimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="3a890-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="3a890-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="3a890-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3a890-109">Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.</span><span class="sxs-lookup"><span data-stu-id="3a890-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="3a890-110">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3a890-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3a890-111">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="3a890-111">Select **Delete**.</span></span> <span data-ttu-id="3a890-112">Šis veiksmas yra būtinas, norint sutrumpinti vidinės įmonės planavimą.</span><span class="sxs-lookup"><span data-stu-id="3a890-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="3a890-113">Vidinės įmonės planavimo procesas vykdys bendrąjį planavimą visose planavimo grupės įmonėse, pradedant nuo žemiausio planavimo sekos.</span><span class="sxs-lookup"><span data-stu-id="3a890-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="3a890-114">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3a890-114">Select **Yes**.</span></span>
6. <span data-ttu-id="3a890-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3a890-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="3a890-116">Vidinės įmonės bendrojo plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="3a890-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="3a890-117">**Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Darbo sritys > Pagrindinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="3a890-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="3a890-118">Pasirinkite **Vidinės įmonės bendrasis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="3a890-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="3a890-119">Lauke **Vidinės įmonės planavimo grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3a890-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3a890-120">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3a890-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="3a890-121">Pasirinkite 10 vidinės įmonės planavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="3a890-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="3a890-122">Lauke **Vidinės įmonės planavimo derinių skaičius** įveskite „2“.</span><span class="sxs-lookup"><span data-stu-id="3a890-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="3a890-123">10 vidinės įmonės planavimo grupėje yra du nariai.</span><span class="sxs-lookup"><span data-stu-id="3a890-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="3a890-124">Norėdami atidėjimus perduoti iš šaltinio įmonės (USMF) į kliento įmonę (DEMF), turėsite vykdyti vidinės įmonę abiejose įmonėse du kartus.</span><span class="sxs-lookup"><span data-stu-id="3a890-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="3a890-125">Vykdant pirmąjį kartojimą bus perduotas poreikis ir nustatyti atidėjimai šaltinio įmonėje (USMF).</span><span class="sxs-lookup"><span data-stu-id="3a890-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="3a890-126">Vykdant antrąjį kartojimą atidėjimai bus perduoti iš USMF į DEMF.</span><span class="sxs-lookup"><span data-stu-id="3a890-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="3a890-127">Lauke **Pirmas derinys** pažymėkite Regeneravimas.</span><span class="sxs-lookup"><span data-stu-id="3a890-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="3a890-128">Lauke **Kiti deriniai** pažymėkite Regeneravimas.</span><span class="sxs-lookup"><span data-stu-id="3a890-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="3a890-129">Lauke **Gijų skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3a890-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="3a890-130">Tai nurodo lygiagrečių gijų, naudojamų planuojant, skaičių.</span><span class="sxs-lookup"><span data-stu-id="3a890-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="3a890-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3a890-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="3a890-132">Plano rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="3a890-132">View the result of the plan</span></span>

1. <span data-ttu-id="3a890-133">Lauke **Planas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3a890-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="3a890-134">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3a890-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="3a890-135">Pasirinkite saitą Statiniam planui.</span><span class="sxs-lookup"><span data-stu-id="3a890-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="3a890-136">Turite būti įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="3a890-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="3a890-137">Pažymėkite **Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3a890-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]