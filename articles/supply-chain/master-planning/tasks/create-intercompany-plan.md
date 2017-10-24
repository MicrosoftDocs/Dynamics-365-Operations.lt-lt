--- 
title: "Kurti vidinės įmonės planą"
description: "Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="98ee5-103">Kurti vidinės įmonės planą</span><span class="sxs-lookup"><span data-stu-id="98ee5-103">Create an intercompany plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98ee5-104">Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.</span><span class="sxs-lookup"><span data-stu-id="98ee5-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="98ee5-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="98ee5-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="98ee5-106">Vidinės įmonės planavimo grupės nustatymas</span><span class="sxs-lookup"><span data-stu-id="98ee5-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="98ee5-107">Pasirinkite Vidinės įmonės planavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="98ee5-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="98ee5-108">Bendrasis planavimas > Sąranka > Vidinės įmonės planavimo grupės</span><span class="sxs-lookup"><span data-stu-id="98ee5-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="98ee5-109">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="98ee5-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="98ee5-110">Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.</span><span class="sxs-lookup"><span data-stu-id="98ee5-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="98ee5-111">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="98ee5-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="98ee5-112">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="98ee5-112">Click Delete.</span></span>
    * <span data-ttu-id="98ee5-113">Šis veiksmas yra būtinas, norint sutrumpinti vidinės įmonės planavimą.</span><span class="sxs-lookup"><span data-stu-id="98ee5-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="98ee5-114">Vidinės įmonės planavimo procesas vykdys bendrąjį planavimą visose planavimo grupės įmonėse, pradedant nuo žemiausio planavimo sekos.</span><span class="sxs-lookup"><span data-stu-id="98ee5-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="98ee5-115">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="98ee5-115">Click Yes.</span></span>
6. <span data-ttu-id="98ee5-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="98ee5-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="98ee5-117">Kurti vidinės įmonės planą</span><span class="sxs-lookup"><span data-stu-id="98ee5-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="98ee5-118">Spustelėkite Vidinės įmonės bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="98ee5-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="98ee5-119">Tai pateikiama darbo srityje Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="98ee5-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="98ee5-120">Lauke Vidinės įmonės planavimo grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="98ee5-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="98ee5-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="98ee5-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98ee5-122">Pasirinkite 10 vidinės įmonės planavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="98ee5-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="98ee5-123">Lauke Vidinės įmonės planavimo pakartojimų skaičius įveskite skaičių 2.</span><span class="sxs-lookup"><span data-stu-id="98ee5-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="98ee5-124">10 vidinės įmonės planavimo grupėje yra du nariai.</span><span class="sxs-lookup"><span data-stu-id="98ee5-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="98ee5-125">Norėdami atidėjimus perduoti iš šaltinio įmonės (USMF) į kliento įmonę (DEMF), turėsite vykdyti vidinės įmonę abiejose įmonėse du kartus.</span><span class="sxs-lookup"><span data-stu-id="98ee5-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="98ee5-126">Vykdant pirmąjį kartojimą bus perduotas poreikis ir nustatyti atidėjimai šaltinio įmonėje (USMF).</span><span class="sxs-lookup"><span data-stu-id="98ee5-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="98ee5-127">Vykdant antrąjį kartojimą atidėjimai bus perduoti iš USMF į DEMF.</span><span class="sxs-lookup"><span data-stu-id="98ee5-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="98ee5-128">Lauke Pirmasis kartojimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="98ee5-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="98ee5-129">Lauke Pirmasis kartojimas pasirinkite Regeneravimas.</span><span class="sxs-lookup"><span data-stu-id="98ee5-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="98ee5-130">Lauke Paskesni pakartojimai pasirinkite Regeneravimas.</span><span class="sxs-lookup"><span data-stu-id="98ee5-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="98ee5-131">Lauke Gijų skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="98ee5-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="98ee5-132">Tai nurodo lygiagrečių gijų, naudojamų planuojant, skaičių.</span><span class="sxs-lookup"><span data-stu-id="98ee5-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="98ee5-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="98ee5-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="98ee5-134">Plano rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="98ee5-134">View the result of the plan</span></span>
1. <span data-ttu-id="98ee5-135">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="98ee5-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="98ee5-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="98ee5-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98ee5-137">Spustelėkite StaticPlan saitą.</span><span class="sxs-lookup"><span data-stu-id="98ee5-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="98ee5-138">Turite būti įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="98ee5-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="98ee5-139">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="98ee5-139">Click Planned orders.</span></span>


