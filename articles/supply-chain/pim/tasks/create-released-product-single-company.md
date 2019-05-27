---
title: Kurti vienos įmonės išleistą produktą
description: Ši procedūra žingsnis po žingsnio padeda sukurti vieną išleistą produktą vieno juridinio vieneto kontekste.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9265ee4311ac89ae88ff7dd089519251828b1e3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552629"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="08c3f-103">Kurti vienos įmonės išleistą produktą</span><span class="sxs-lookup"><span data-stu-id="08c3f-103">Create a released product for a single company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08c3f-104">Ši procedūra žingsnis po žingsnio padeda sukurti vieną išleistą produktą vieno juridinio vieneto kontekste.</span><span class="sxs-lookup"><span data-stu-id="08c3f-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="08c3f-105">Sukūrus išleistą produktą, jį galima iš karto naudoti tik šiame vienete.</span><span class="sxs-lookup"><span data-stu-id="08c3f-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="08c3f-106">Šią procedūrą galite žingsnis po žingsnio atlikti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="08c3f-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="08c3f-107">Šią užduotį paprastai atlieka produkto dizaineris.</span><span class="sxs-lookup"><span data-stu-id="08c3f-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="08c3f-108">Kurti išleistą produktą</span><span class="sxs-lookup"><span data-stu-id="08c3f-108">Create a released product</span></span>
1. <span data-ttu-id="08c3f-109">Eikite į Išleisti produktai.</span><span class="sxs-lookup"><span data-stu-id="08c3f-109">Go to Released products.</span></span>
2. <span data-ttu-id="08c3f-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="08c3f-110">Click New.</span></span>
3. <span data-ttu-id="08c3f-111">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08c3f-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="08c3f-112">Jei produkto numeris automatiškai lauke „Produkto numeris“ neįvestas, įveskite unikalų produkto numerį.</span><span class="sxs-lookup"><span data-stu-id="08c3f-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="08c3f-113">Šį veiksmą atlikti reikia tik jei nenustatyta produktų numeracija.</span><span class="sxs-lookup"><span data-stu-id="08c3f-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="08c3f-114">Lauke Produkto pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08c3f-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="08c3f-115">Produkto pavadinimas naudojamas kaip numatytasis paieškos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="08c3f-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="08c3f-116">Jei reikia, galite paieškos pavadinimą keisti.</span><span class="sxs-lookup"><span data-stu-id="08c3f-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="08c3f-117">Lauke Prekių modelių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-118">Prekės modelių grupėse yra parametrų, kurie nustato, kaip prekės kontroliuojamos ir tvarkomos jas gaunant ir išduodant.</span><span class="sxs-lookup"><span data-stu-id="08c3f-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="08c3f-119">Nuostatos taip pat nustato, kaip turi būti skaičiuojamas prekių suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="08c3f-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="08c3f-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="08c3f-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="08c3f-122">Lauke Prekių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-123">Prekių grupės naudojamos atsargoms valdyti dalinant atsargas į grupes pagal prekės charakteristikas.</span><span class="sxs-lookup"><span data-stu-id="08c3f-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="08c3f-124">Pavyzdžiui, norėdami valdyti, kaip informacija registruojama pagrindinėse sąskaitose, galite sukurti skirtingų prekių grupių, susietų su konkrečiomis pagrindinėmis sąskaitomis, seriją.</span><span class="sxs-lookup"><span data-stu-id="08c3f-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="08c3f-125">Tai suteikia galimybę stebėti atsargų reikšmę įvairiais etapais.</span><span class="sxs-lookup"><span data-stu-id="08c3f-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="08c3f-126">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="08c3f-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="08c3f-128">Lauke Saugojimo dimensijų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-129">Sandėliavimo dimensijos padeda kontroliuoti, kaip prekės saugomos ir paimamos iš atsargų.</span><span class="sxs-lookup"><span data-stu-id="08c3f-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="08c3f-130">Pvz., saugojimo dimensija gali būti teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="08c3f-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="08c3f-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="08c3f-132">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="08c3f-133">Lauke Sekimo dimensijų grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-134">Sekimo dimensijų grupė nustato, kurias sekimo dimensijas galite pridėti prie produkto.</span><span class="sxs-lookup"><span data-stu-id="08c3f-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="08c3f-135">Pvz., paketo numeris ir serijos numeris yra naudojami atsargų prekėms sekti.</span><span class="sxs-lookup"><span data-stu-id="08c3f-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="08c3f-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="08c3f-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="08c3f-138">Lauke „Atsargų vienetas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-139">Atsargų vienetas nustato, kaip prekė išreiškiama, ją saugant atsargose.</span><span class="sxs-lookup"><span data-stu-id="08c3f-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="08c3f-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="08c3f-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="08c3f-142">Lauke „Pirkimo vienetas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-143">Pirkimo vienetas nustato, kaip produktas išreiškiamas, jį perkant iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="08c3f-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="08c3f-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="08c3f-145">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="08c3f-146">Lauke „Pardavimo vienetas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-147">Pardavimo vienetas nustato, kaip produktas išreiškiamas, jį parduodant klientui.</span><span class="sxs-lookup"><span data-stu-id="08c3f-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="08c3f-148">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="08c3f-149">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="08c3f-150">Lauke „KS vienetas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-151">KS vienetas nustato, kaip produktas išreiškiamas, jį įtraukiant į komplektavimo specifikaciją (KS).</span><span class="sxs-lookup"><span data-stu-id="08c3f-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="08c3f-152">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="08c3f-153">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="08c3f-154">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-155">Pardavimo apmokestinimo grupės prekės PVM grupė nulemia, kaip apskaičiuojamas kiekvienos prekės PVM.</span><span class="sxs-lookup"><span data-stu-id="08c3f-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="08c3f-156">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="08c3f-157">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="08c3f-158">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="08c3f-159">Pirkimo apmokestinimo grupės prekės PVM grupė nulemia, kaip apskaičiuojamas kiekvienos prekės pirkimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="08c3f-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="08c3f-160">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="08c3f-161">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="08c3f-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08c3f-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="08c3f-163">Pridėti produkto charakteristikas</span><span class="sxs-lookup"><span data-stu-id="08c3f-163">Add product characteristics</span></span>
1. <span data-ttu-id="08c3f-164">Išplėskite arba sutraukite sekciją Tvarkyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="08c3f-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="08c3f-165">Lauke „Grynasis svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08c3f-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="08c3f-166">Lauke „Taros svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08c3f-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="08c3f-167">Lauke „Gylis bruto“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08c3f-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="08c3f-168">Lauke „Plotis bruto“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08c3f-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="08c3f-169">Lauke „Aukštis bruto“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08c3f-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="08c3f-170">Lauke „Tūris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08c3f-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="08c3f-171">Pridėti finansines dimensijas</span><span class="sxs-lookup"><span data-stu-id="08c3f-171">Add financial dimensions</span></span>
1. <span data-ttu-id="08c3f-172">Išplėskite arba sutraukite skyrių Finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="08c3f-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="08c3f-173">Lauke „BusinessUnit“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="08c3f-174">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="08c3f-175">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="08c3f-176">Lauke „CostCenter“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="08c3f-177">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="08c3f-178">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="08c3f-179">Lauke Skyrius spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="08c3f-180">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="08c3f-181">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="08c3f-182">Lauke Prekių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="08c3f-183">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="08c3f-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="08c3f-184">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08c3f-184">In the list, click the link in the selected row.</span></span>

