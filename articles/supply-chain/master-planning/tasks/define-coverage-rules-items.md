---
title: Apibrėžti prekių padengimo taisykles
description: Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999886"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="5cce5-103">Apibrėžti prekių padengimo taisykles</span><span class="sxs-lookup"><span data-stu-id="5cce5-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5cce5-104">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="5cce5-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5cce5-105">Šioje procedūroje nurodoma, kaip kurti padengimo taisykles ir nepaisyti konkrečios prekės padengimo parametrų.</span><span class="sxs-lookup"><span data-stu-id="5cce5-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="5cce5-106">Jis taip pat parodo, kaip nurodyti numatytąsias atsargų nuostatas.</span><span class="sxs-lookup"><span data-stu-id="5cce5-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="5cce5-107">Padengimo grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="5cce5-107">Create a coverage group</span></span>
1. <span data-ttu-id="5cce5-108">Eikite į **„Naršymo sritis“ > „Moduliai“ > „Bendrasis planavimas“ > „Sąranka“ > „Padengimo grupės“**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="5cce5-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-109">Click **New**.</span></span>
3. <span data-ttu-id="5cce5-110">Lauke **Padengimo grupės** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="5cce5-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="5cce5-111">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5cce5-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="5cce5-112">Lauke **Kalendorius** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5cce5-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="5cce5-113">Pasirinkite kalendorių, kurį bendrasis planavimas naudos norėdamas sukurti šios grupės prekių papildymo pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="5cce5-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="5cce5-114">Lauke **Padengimo kodas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="5cce5-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="5cce5-115">Pasirinkite Reikalavimai šiai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="5cce5-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="5cce5-116">Lauke **Padengimo laik oribos (dienomis)** įveskite 90.</span><span class="sxs-lookup"><span data-stu-id="5cce5-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="5cce5-117">Prekėms šioje grupėje bendrasis planavimas iki 90 dienų ateityje kurs papildymo pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="5cce5-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="5cce5-118">Lauke **Neigiamos dienos** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="5cce5-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="5cce5-119">Lauke **Teigiamos dienos** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="5cce5-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="5cce5-120">Išplėskite arba sutraukite sekciją **Kiti**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="5cce5-121">Sekcijos **Laiko rezervas dienomis** lauke **Gavimo laiko rezervas, pridėtas prie pareikalavimo datos** įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="5cce5-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="5cce5-122">Pavyzdžiui, jei nustatytas 1 dienos gavimo laiko rezervas, o pirkimo užsakymo eilutę planuojama gauti gegužės 15 d., bendrajame planavime gavimo data bus pakoreguota į gegužės 16 d.</span><span class="sxs-lookup"><span data-stu-id="5cce5-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="5cce5-123">Lauke **Išdavimo laiko rezervas, atimtas iš pareikalavimo datos** įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="5cce5-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="5cce5-124">Pavyzdžiui, jei nustatytas 1 dienos laiko rezervas, o pardavimo užsakymo eilutę planuojama pristatyti gegužės 15 d., bendrajame planavime pristatymo data bus pakoreguota į gegužės 14 d.</span><span class="sxs-lookup"><span data-stu-id="5cce5-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="5cce5-125">Lauke **Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką** įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="5cce5-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="5cce5-126">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="5cce5-127">Naujo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="5cce5-127">Create a new product</span></span>
1. <span data-ttu-id="5cce5-128">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="5cce5-129">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-129">Click **New**.</span></span>
3. <span data-ttu-id="5cce5-130">Lauke **Produkto numeris** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5cce5-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="5cce5-131">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="5cce5-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="5cce5-132">Lauke **Prekių modelių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5cce5-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="5cce5-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5cce5-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5cce5-135">Lauke **Prekių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5cce5-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="5cce5-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5cce5-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5cce5-138">Lauke **Saugojimo dimensijų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="5cce5-139">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="5cce5-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5cce5-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="5cce5-141">Lauke **Sekimo dimensijų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5cce5-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="5cce5-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5cce5-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="5cce5-144">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="5cce5-145">Nustatyti numatytąsias užsakymo nuostatas</span><span class="sxs-lookup"><span data-stu-id="5cce5-145">Setup default order settings</span></span>
1. <span data-ttu-id="5cce5-146">Parinktyje **Veiksmų sritis** spustelėkite **Planas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="5cce5-147">Dalyje **Užsakymo parametrai** spustelėkite **Numatytieji užsakymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="5cce5-148">Po **Pirkimo užsakymas** lauku **Numatytoji teritorija** įveskite teritoriją, kuri naudojama kaip numatytoji, kai kuriami pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="5cce5-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="5cce5-149">Lauke **Numatytasis sandėlis** įveskite vietą, kurioje saugoma prekė.</span><span class="sxs-lookup"><span data-stu-id="5cce5-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="5cce5-150">Išplėskite arba sutraukite sekciją **Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="5cce5-151">Lauke **Daugkartinis** įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="5cce5-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="5cce5-152">Lauke **„Minimalus užsakymo kiekis** įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="5cce5-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="5cce5-153">Lauke **„Maksimalus užsakymo kiekis** įveskite „100“.</span><span class="sxs-lookup"><span data-stu-id="5cce5-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="5cce5-154">Lauke **Standartinis užsakymo kiekis** įveskite „10“.</span><span class="sxs-lookup"><span data-stu-id="5cce5-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="5cce5-155">Lauke **Pirkimo vykdymo laikas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5cce5-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="5cce5-156">Pažymėkite arba išvalykite žymės langelį **Darbo dienos**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="5cce5-157">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-157">Click **Save**.</span></span>
13. <span data-ttu-id="5cce5-158">Lauke **Numatytojo užsakymo tipas** pasirinkite „Pirkimo užsakymas“.</span><span class="sxs-lookup"><span data-stu-id="5cce5-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="5cce5-159">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-159">Click **Save**.</span></span>
15. <span data-ttu-id="5cce5-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5cce5-160">Close the page.</span></span> <span data-ttu-id="5cce5-161">Uždarykite puslapį Numatytieji užsakymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="5cce5-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="5cce5-162">Pridėti prekę į padengimo grupę</span><span class="sxs-lookup"><span data-stu-id="5cce5-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="5cce5-163">Išplėskite arba sutraukite sekciją **Planas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="5cce5-164">Lauke **Padengimo grupės** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5cce5-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5cce5-165">Sąraše raskite **Padengimo grupės**, kurią sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="5cce5-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="5cce5-166">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5cce5-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="5cce5-167">Kurti prekių padengimo taisykles</span><span class="sxs-lookup"><span data-stu-id="5cce5-167">Create item coverage rules</span></span>
1. <span data-ttu-id="5cce5-168">Parinktyje **Veiksmų sritis** spustelėkite **Planas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="5cce5-169">Dalyje **Padengimas** spustelėkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="5cce5-170">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-170">Click **New**.</span></span>
4. <span data-ttu-id="5cce5-171">Spustelėkite skirtuką **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="5cce5-172">Pažymėkite **Nepaisyti padengimo grupės parametrų** antraštės langelį.</span><span class="sxs-lookup"><span data-stu-id="5cce5-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="5cce5-173">Lauke **Padengimo laiko ribos (dienomis)** įveskite 60.</span><span class="sxs-lookup"><span data-stu-id="5cce5-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="5cce5-174">Nors prekės padengimo grupėje Poreikis yra planuojamos 90 dienų į priekį, ši prekė bus planuojama 60 dienų į priekį.</span><span class="sxs-lookup"><span data-stu-id="5cce5-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="5cce5-175">Lauke **Neigiamos dienos** įveskite „2‟.</span><span class="sxs-lookup"><span data-stu-id="5cce5-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="5cce5-176">Lauke **Teigiamos dienos** įveskite „2‟.</span><span class="sxs-lookup"><span data-stu-id="5cce5-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="5cce5-177">Spustelėkite skirtuką **Gamybos laikas**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="5cce5-178">Pažymėkite **Pirkti** antraštės langelį.</span><span class="sxs-lookup"><span data-stu-id="5cce5-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="5cce5-179">Lauke **Pirkimo laikas** įveskite 5.</span><span class="sxs-lookup"><span data-stu-id="5cce5-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="5cce5-180">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5cce5-180">Click **Save**.</span></span>

