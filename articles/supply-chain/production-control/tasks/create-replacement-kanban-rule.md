--- 
title: "Kurti pakeitimo „kanban“ taisyklę"
description: "Šioje procedūroje parodoma, kaip konkrečią datą esamą „kanban“ taisyklę pakeisti nauja „kanban“ taisykle."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5b27200a8d56192d473887f01076eced0f92e4c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="40a0e-103">Kurti pakeitimo „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="40a0e-103">Create a replacement kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40a0e-104">Šioje procedūroje parodoma, kaip konkrečią datą esamą „kanban“ taisyklę pakeisti nauja „kanban“ taisykle.</span><span class="sxs-lookup"><span data-stu-id="40a0e-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="40a0e-105">Tai naudinga, kai reikia koordinuoti ir planuoti gamybos eigos ar papildymo taisyklių pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="40a0e-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="40a0e-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="40a0e-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="40a0e-107">Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, kai jie parengia pakeistos gamybos eigos arba naujos papildymo taisyklės gamybą.</span><span class="sxs-lookup"><span data-stu-id="40a0e-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="40a0e-108">Atliekant šią užduotį, „kanban“ taisyklė 000022 pakeičiama nauja taisykle ir naujosios taisyklės kiekis nuo 48 padidinamas iki 100.</span><span class="sxs-lookup"><span data-stu-id="40a0e-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="40a0e-109">Keistinos „kanban“ taisyklės pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="40a0e-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="40a0e-110">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="40a0e-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="40a0e-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="40a0e-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40a0e-112">Pasirinkite „kanban“ taisyklę 000022.</span><span class="sxs-lookup"><span data-stu-id="40a0e-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="40a0e-113">Kurti pakeitimo „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="40a0e-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="40a0e-114">Spustelėkite Pakeisti „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="40a0e-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="40a0e-115">Lauke Įsigaliojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="40a0e-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="40a0e-116">Pasirinkite datą ateityje, pvz., viena savaitė nuo dabar.</span><span class="sxs-lookup"><span data-stu-id="40a0e-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="40a0e-117">Tai yra data ir laikas, kada naujoji „kanban“ taisyklė tampa aktyvi ir pakeičia senąją „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="40a0e-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="40a0e-118">Jei „kanban“ taisyklė pakeičią kelią gamybos eigoje, galima pasirinkti kitą veiklą.</span><span class="sxs-lookup"><span data-stu-id="40a0e-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="40a0e-119">Atlikdami šią procedūrą, veiklos nekeisime.</span><span class="sxs-lookup"><span data-stu-id="40a0e-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="40a0e-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="40a0e-120">Click OK.</span></span>
    * <span data-ttu-id="40a0e-121">Atkreipkite dėmesį, kad sukuriama nauja „kanban“ taisyklė, kuri pakeičia „kanban“ taisyklę 000022.</span><span class="sxs-lookup"><span data-stu-id="40a0e-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="40a0e-122">Galiojimo data nustatoma pagal datą, pasirinktą pakeičiant „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="40a0e-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="40a0e-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="40a0e-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="40a0e-124">Pasirinkite pakeistą „kanban“ taisyklę 000022.</span><span class="sxs-lookup"><span data-stu-id="40a0e-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="40a0e-125">Atkreipkite dėmesį, kad pakeistos „kanban“ taisyklės data yra tokia pati, kaip Galiojimo data, nes ji yra galiojimo pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="40a0e-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="40a0e-126">Sąraše pasirinkite 1 eilutę.</span><span class="sxs-lookup"><span data-stu-id="40a0e-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="40a0e-127">Sąrašo viršuje pasirinkite naująją „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="40a0e-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="40a0e-128">Tai yra „kanban“ taisyklė, kurios numeris didžiausias.</span><span class="sxs-lookup"><span data-stu-id="40a0e-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="40a0e-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="40a0e-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="40a0e-130">Spustelėkite „kanban“ taisyklės numerį, kad atidarytumėte „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="40a0e-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="40a0e-131">Senąją pakeičiančios „kanban“ taisyklės didžiausio kiekio modifikavimas</span><span class="sxs-lookup"><span data-stu-id="40a0e-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="40a0e-132">Didžiausias kiekis nustatykite į 100.</span><span class="sxs-lookup"><span data-stu-id="40a0e-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="40a0e-133">Išplėskite „FastTab‟ skirtuką Kiekiai, kad matytumėte lauką Didžiausias kiekis.</span><span class="sxs-lookup"><span data-stu-id="40a0e-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="40a0e-134">Didžiausią kiekį pakeitus į 100, bus galima apdoroti iki 100 „kanban“.</span><span class="sxs-lookup"><span data-stu-id="40a0e-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="40a0e-135">Tai yra paskutinis šios užduoties veiksmas.</span><span class="sxs-lookup"><span data-stu-id="40a0e-135">This is the last step in this task.</span></span>  


