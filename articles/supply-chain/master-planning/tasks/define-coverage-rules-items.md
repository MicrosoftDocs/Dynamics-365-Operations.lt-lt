---
title: Apibrėžti prekių padengimo taisykles
description: Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 680d7c9339b089a4da82bef18bae3af41e23af30
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845183"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="b5374-103">Apibrėžti prekių padengimo taisykles</span><span class="sxs-lookup"><span data-stu-id="b5374-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5374-104">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b5374-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b5374-105">Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų.</span><span class="sxs-lookup"><span data-stu-id="b5374-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="b5374-106">Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.</span><span class="sxs-lookup"><span data-stu-id="b5374-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="b5374-107">Padengimo grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="b5374-107">Create a coverage group</span></span>
1. <span data-ttu-id="b5374-108">Eikite į **„Naršymo sritis“ > „Moduliai“ > „Bendrasis planavimas“ > „Sąranka“ > „Padengimo grupės“**.</span><span class="sxs-lookup"><span data-stu-id="b5374-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="b5374-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b5374-109">Click **New**.</span></span>
3. <span data-ttu-id="b5374-110">Lauke **Coverage group** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="b5374-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="b5374-111">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b5374-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b5374-112">Lauke **Kalendorius** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b5374-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="b5374-113">Pasirinkite kalendorių, kurį bendrasis planavimas naudos norėdamas sukurti šios grupės prekių papildymo pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="b5374-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="b5374-114">Lauke **Coverage code** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b5374-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="b5374-115">Pasirinkite Reikalavimai šiai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="b5374-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="b5374-116">Lauke **Coverage time fence (days) field** įveskite „90‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="b5374-117">Prekėms šioje grupėje bendrasis planavimas iki 90 dienų ateityje kurs papildymo pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="b5374-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="b5374-118">Lauke **Negative days** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="b5374-119">Lauke **Positive days** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="b5374-120">Išplėskite arba sutraukite sekciją **Other**.</span><span class="sxs-lookup"><span data-stu-id="b5374-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="b5374-121">Skyriaus **Safety margins in days** lauke **Receipt margin added to requirement date** įveskite „1“.</span><span class="sxs-lookup"><span data-stu-id="b5374-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="b5374-122">Pavyzdžiui, jei nustatytas 1 dienos gavimo laiko rezervas, o pirkimo užsakymo eilutę planuojama gauti gegužės 15 d., bendrajame planavime gavimo data bus pakoreguota į gegužės 16 d.</span><span class="sxs-lookup"><span data-stu-id="b5374-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="b5374-123">Lauke **Issue margin deducted from requirement date** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="b5374-124">Pavyzdžiui, jei nustatytas 1 dienos laiko rezervas, o pardavimo užsakymo eilutę planuojama pristatyti gegužės 15 d., bendrajame planavime pristatymo data bus pakoreguota į gegužės 14 d.</span><span class="sxs-lookup"><span data-stu-id="b5374-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="b5374-125">Lauke **Reorder margin added to item lead time** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="b5374-126">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5374-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="b5374-127">Naujo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="b5374-127">Create a new product</span></span>
1. <span data-ttu-id="b5374-128">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="b5374-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="b5374-129">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b5374-129">Click **New**.</span></span>
3. <span data-ttu-id="b5374-130">Lauke **Product number** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b5374-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="b5374-131">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="b5374-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="b5374-132">Lauke **Item model group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b5374-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b5374-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b5374-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b5374-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b5374-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b5374-135">Lauke **Item group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b5374-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b5374-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b5374-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b5374-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b5374-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b5374-138">Lauke **Storage dimension group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b5374-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b5374-139">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b5374-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="b5374-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b5374-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b5374-141">Lauke **Tracking dimension group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b5374-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b5374-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b5374-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="b5374-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b5374-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b5374-144">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b5374-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="b5374-145">Nustatyti numatytąsias užsakymo nuostatas</span><span class="sxs-lookup"><span data-stu-id="b5374-145">Setup default order settings</span></span>
1. <span data-ttu-id="b5374-146">Parinktyje **Action Pane** spustelėkite **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b5374-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="b5374-147">Dalyje **Order settings** spustelėkite **Default order settings**.</span><span class="sxs-lookup"><span data-stu-id="b5374-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="b5374-148">Po **Purchase order** lauku **Default site** įveskite teritoriją, kuri naudojama kaip numatytoji, kai kuriami pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b5374-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="b5374-149">Lauke **Default warehouse** įveskite vietą, kurioje saugoma prekė.</span><span class="sxs-lookup"><span data-stu-id="b5374-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="b5374-150">Išplėskite arba sutraukite sekciją **Inventory**.</span><span class="sxs-lookup"><span data-stu-id="b5374-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="b5374-151">Lauke **Multiple** įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="b5374-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="b5374-152">Lauke **„Minimalus užsakymo kiekis** įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="b5374-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="b5374-153">Lauke **„Maksimalus užsakymo kiekis** įveskite „100“.</span><span class="sxs-lookup"><span data-stu-id="b5374-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="b5374-154">Lauke **Standard order quantity** įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="b5374-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="b5374-155">Lauke **Purchase lead time** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b5374-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="b5374-156">Pažymėkite arba išvalykite žymės langelį **Working days**.</span><span class="sxs-lookup"><span data-stu-id="b5374-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="b5374-157">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5374-157">Click **Save**.</span></span>
13. <span data-ttu-id="b5374-158">Lauke **Default order type** pasirinkite „Pirkimo užsakymas“.</span><span class="sxs-lookup"><span data-stu-id="b5374-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="b5374-159">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5374-159">Click **Save**.</span></span>
15. <span data-ttu-id="b5374-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b5374-160">Close the page.</span></span> <span data-ttu-id="b5374-161">Uždarykite puslapį Numatytieji užsakymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="b5374-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="b5374-162">Pridėti prekę į padengimo grupę</span><span class="sxs-lookup"><span data-stu-id="b5374-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="b5374-163">Išplėskite arba sutraukite sekciją **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b5374-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="b5374-164">Lauke **Coverage group** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b5374-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b5374-165">Sąraše raskite **Coverage group**, kurią sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="b5374-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="b5374-166">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b5374-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="b5374-167">Kurti prekių padengimo taisykles</span><span class="sxs-lookup"><span data-stu-id="b5374-167">Create item coverage rules</span></span>
1. <span data-ttu-id="b5374-168">Parinktyje **Action Pane** spustelėkite **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b5374-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="b5374-169">Dalyje **Coverage** spustelėkite **Item coverage**.</span><span class="sxs-lookup"><span data-stu-id="b5374-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="b5374-170">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b5374-170">Click **New**.</span></span>
4. <span data-ttu-id="b5374-171">Spustelėkite skirtuką **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="b5374-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="b5374-172">Pažymėkite funkcijos **Override coverage group** parametrų antraštės langelį.</span><span class="sxs-lookup"><span data-stu-id="b5374-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="b5374-173">Lauke **Coverage time fence (days)** įveskite „60‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="b5374-174">Nors prekės padengimo grupėje Poreikis yra planuojamos 90 dienų į priekį, ši prekė bus planuojama 60 dienų į priekį.</span><span class="sxs-lookup"><span data-stu-id="b5374-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="b5374-175">Lauke **Negative days** įveskite „2‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="b5374-176">Lauke **Positive days** įveskite „2‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="b5374-177">Spustelėkite skirtuką **Lead time**.</span><span class="sxs-lookup"><span data-stu-id="b5374-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="b5374-178">Pažymėkite antraštės **Purchase** langelį.</span><span class="sxs-lookup"><span data-stu-id="b5374-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="b5374-179">Lauke **Purchase time** įveskite „5‟.</span><span class="sxs-lookup"><span data-stu-id="b5374-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="b5374-180">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b5374-180">Click **Save**.</span></span>

