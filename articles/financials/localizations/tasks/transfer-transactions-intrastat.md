--- 
title: "Operacijų perkėlimas į Intrastat"
description: "Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat."
author: Anasyash
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cc21497a6905cdb57bd687b7bff0d9dc810ba9eb
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="54e42-103">Operacijų perkėlimas į Intrastat</span><span class="sxs-lookup"><span data-stu-id="54e42-103">Transfer transactions to the Intrastat</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54e42-104">Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat.</span><span class="sxs-lookup"><span data-stu-id="54e42-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="54e42-105">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.</span><span class="sxs-lookup"><span data-stu-id="54e42-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="54e42-106">Naujo prekės kodo kūrimas ir esamo naujinimas</span><span class="sxs-lookup"><span data-stu-id="54e42-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="54e42-107">Pasirinkite Produkto informacijos valdymas > Nustatymas > Kategorijos ir atributai > Kategorijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="54e42-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="54e42-108">Sąraše raskite arba pasirinkite įrašą Intrastat prekių kodai.</span><span class="sxs-lookup"><span data-stu-id="54e42-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="54e42-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="54e42-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54e42-110">Medyje pasirinkite „įrašas‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="54e42-111">Pavyzdžiui, pasirinkite Intrastat \ Garsiakalbis.</span><span class="sxs-lookup"><span data-stu-id="54e42-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="54e42-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="54e42-112">Click Edit.</span></span>
6. <span data-ttu-id="54e42-113">Išplėskite dalį Užsienio prekyba.</span><span class="sxs-lookup"><span data-stu-id="54e42-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="54e42-114">Lauke Papildomi vienetai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-115">Pavyzdžiui, pasirinkite „vnt.‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="54e42-116">Lauke Svoris netaikomas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54e42-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="54e42-117">Medyje pasirinkite Intrastat.</span><span class="sxs-lookup"><span data-stu-id="54e42-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="54e42-118">Spustelėkite „Naujas kategorijos mazgas“.</span><span class="sxs-lookup"><span data-stu-id="54e42-118">Click New category node.</span></span>
11. <span data-ttu-id="54e42-119">Lauke Pavadinimas įveskite prekės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="54e42-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="54e42-120">Pavyzdžiui, įveskite „Kita prekė‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="54e42-121">Lauke Kodas įveskite prekės kodą.</span><span class="sxs-lookup"><span data-stu-id="54e42-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="54e42-122">Pavyzdžiui, įveskite „995 00 00‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="54e42-123">Lauke „Patogus pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="54e42-124">Pavyzdžiui, įveskite „Kita‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="54e42-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54e42-125">Click Save.</span></span>
15. <span data-ttu-id="54e42-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54e42-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="54e42-127">Prekės kodo priskyrimas produktų hierarchijai ir išleistam produktui</span><span class="sxs-lookup"><span data-stu-id="54e42-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="54e42-128">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="54e42-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="54e42-129">Pvz., filtruokite lauką Pavadinimas reikšme „pardavimas“.</span><span class="sxs-lookup"><span data-stu-id="54e42-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="54e42-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="54e42-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="54e42-131">Medyje išplėskite „kategorijos mazgas‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="54e42-132">Pavyzdžiui, išplėskite Pardavimo hierarchija \ Namų garso sistema.</span><span class="sxs-lookup"><span data-stu-id="54e42-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="54e42-133">Medyje pasirinkite „prekės kodui priskirtina kategorija‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="54e42-134">Pavyzdžiui, pasirinkite Pardavimo hierarchija \ Namų garso sistema \ Garsiakalbiai.</span><span class="sxs-lookup"><span data-stu-id="54e42-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="54e42-135">Išplėskite dalį Prekių kodai.</span><span class="sxs-lookup"><span data-stu-id="54e42-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="54e42-136">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="54e42-136">Click Add.</span></span>
7. <span data-ttu-id="54e42-137">Lauke Pasirinkti hierarchiją pasirinkite „Intrastat‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="54e42-138">Sąraše raskite ir pasirinkite prekės kodą.</span><span class="sxs-lookup"><span data-stu-id="54e42-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="54e42-139">Pavyzdžiui, pasirinkite 920 20 34 \ Garsiakalbis.</span><span class="sxs-lookup"><span data-stu-id="54e42-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="54e42-140">Spustelėkite Pasirinkti kodus.</span><span class="sxs-lookup"><span data-stu-id="54e42-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="54e42-141">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-141">Click OK.</span></span>
11. <span data-ttu-id="54e42-142">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="54e42-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="54e42-143">Sąraše pasirinkite išleistą produktą, kurį priskirsite prekės kodui.</span><span class="sxs-lookup"><span data-stu-id="54e42-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="54e42-144">Pavyzdžiui, pasirinkite D0001.</span><span class="sxs-lookup"><span data-stu-id="54e42-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="54e42-145">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="54e42-145">Click Edit.</span></span>
14. <span data-ttu-id="54e42-146">Išplėskite dalį Užsienio prekyba.</span><span class="sxs-lookup"><span data-stu-id="54e42-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="54e42-147">Lauke Prekė įveskite prekės kodą.</span><span class="sxs-lookup"><span data-stu-id="54e42-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="54e42-148">Pavyzdžiui, pasirinkite reikšmę 920 20 34 Garsiakalbis.</span><span class="sxs-lookup"><span data-stu-id="54e42-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="54e42-149">Lauke Išlaidų procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="54e42-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="54e42-150">Pvz., įveskite „3‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="54e42-151">Lauke Šalis / regionas įveskite arba pasirinkite kilmės šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="54e42-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="54e42-152">Pavyzdžiui, pasirinkite AUT.</span><span class="sxs-lookup"><span data-stu-id="54e42-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="54e42-153">Išplėskite dalį Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="54e42-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="54e42-154">Lauke Grynasis svoris įveskite svorį kilogramais.</span><span class="sxs-lookup"><span data-stu-id="54e42-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="54e42-155">Pvz., įveskite „2,5‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="54e42-156">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54e42-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="54e42-157">Intrastat operacijų kodų ir užsienio prekybos parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="54e42-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="54e42-158">Pasirinkite Mokesčiai > Nustatymas > Užsienio prekyba > Operacijų kodai.</span><span class="sxs-lookup"><span data-stu-id="54e42-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="54e42-159">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="54e42-159">Click New.</span></span>
3. <span data-ttu-id="54e42-160">Lauke Operacijos kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="54e42-161">Pavyzdžiui, kaip operacijos kodą, naudojamą kaip grąžinimas, įveskite „21‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="54e42-162">Lauke Pavadinimas įveskite operacijos kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="54e42-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="54e42-163">Pvz., įveskite „Grąžinimas‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="54e42-164">Lauke Statistinė suma pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="54e42-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="54e42-165">Pavyzdžiui, pasirinkite Tuščia – tai nurodo, kad skelbtina operacijų su operacijos kodu „21‟ statistinė reikšmė visada bus nulis.</span><span class="sxs-lookup"><span data-stu-id="54e42-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="54e42-166">Pasirinkite Mokesčiai > Nustatymai > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="54e42-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="54e42-167">Lauke Operacijos kodas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-168">Pavyzdžiui, pasirinkite 11.</span><span class="sxs-lookup"><span data-stu-id="54e42-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="54e42-169">Lauke Kredito pažyma įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-170">Ši reikšmė taip pat nurodo fizinį grąžinimą.</span><span class="sxs-lookup"><span data-stu-id="54e42-170">This value also identifies the physical return.</span></span> <span data-ttu-id="54e42-171">Fizinio grąžinimo kredito pažyma bus perkelta į Intrastat žurnalą su priešinga kryptimi.</span><span class="sxs-lookup"><span data-stu-id="54e42-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="54e42-172">Pavyzdžiui, gavimo grąžinimas persiunčiamas kaip išsiuntimas.</span><span class="sxs-lookup"><span data-stu-id="54e42-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="54e42-173">Priešingu atveju kredito pažyma laikoma taisymu ir persiunčiama su ta pačia kryptimi ir priešingu ženklu.</span><span class="sxs-lookup"><span data-stu-id="54e42-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="54e42-174">Pavyzdžiui, gavimo taisymas persiunčiamas kaip gavimas su neigiama suma, o aktyvi vėliavėlė nustatoma į „Taisymas“.</span><span class="sxs-lookup"><span data-stu-id="54e42-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="54e42-175">Išplėskite dalį Perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="54e42-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="54e42-176">Lauke Prekės su prekės kodu pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54e42-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="54e42-177">Pasirinkite šią parinktį, kad perkeltumėte tik operacijas su priskirtu prekės kodu.</span><span class="sxs-lookup"><span data-stu-id="54e42-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="54e42-178">Operacijos be prekės kodo į Intrastat perkeltos nebus.</span><span class="sxs-lookup"><span data-stu-id="54e42-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="54e42-179">Lauke Perduoti, kai atitinka kriterijai pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="54e42-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="54e42-180">Pavyzdžiui, pasirinkite Vienas iš pasirinktų.</span><span class="sxs-lookup"><span data-stu-id="54e42-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="54e42-181">Išplėskite dalį Prekių kodų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="54e42-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="54e42-182">Spustelėkite skirtuką Šalies / regiono ypatybės.</span><span class="sxs-lookup"><span data-stu-id="54e42-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="54e42-183">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="54e42-183">Click New.</span></span>
15. <span data-ttu-id="54e42-184">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-185">Pavyzdžiui, pasirinkite reikšmę FRA.</span><span class="sxs-lookup"><span data-stu-id="54e42-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="54e42-186">Lauke Intrastat kodas įveskite šalies ISO kodą.</span><span class="sxs-lookup"><span data-stu-id="54e42-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="54e42-187">Pavyzdžiui, įveskite „FR‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="54e42-188">Lauke Šalies / regiono tipas pasirinkite „ES“.</span><span class="sxs-lookup"><span data-stu-id="54e42-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="54e42-189">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="54e42-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="54e42-190">Pristatymo būdų ir išlaidų įtraukimo į Intrastat taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="54e42-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="54e42-191">Pasirinkite Pardavimas ir rinkodara > Nustatymas > Platinimas > Pristatymo būdai.</span><span class="sxs-lookup"><span data-stu-id="54e42-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="54e42-192">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="54e42-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54e42-193">Pavyzdžiui, pasirinkite 20 Air.</span><span class="sxs-lookup"><span data-stu-id="54e42-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="54e42-194">Išplėskite dalį Užsienio prekyba.</span><span class="sxs-lookup"><span data-stu-id="54e42-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="54e42-195">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="54e42-195">Click Edit.</span></span>
5. <span data-ttu-id="54e42-196">Lauke Transportavimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-197">Pavyzdžiui, pasirinkite 02.</span><span class="sxs-lookup"><span data-stu-id="54e42-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="54e42-198">Pasirinkite Gautinos sumos > Išlaidų nustatymas > Išlaidų kodas.</span><span class="sxs-lookup"><span data-stu-id="54e42-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="54e42-199">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="54e42-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="54e42-200">Pvz., filtruokite lauką Išlaidų kodas reikšme „transportavimas‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="54e42-201">Išplėskite dalį Užsienio prekyba.</span><span class="sxs-lookup"><span data-stu-id="54e42-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="54e42-202">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="54e42-202">Click Edit.</span></span>
10. <span data-ttu-id="54e42-203">Lauke Intrastat sąskaitos faktūros vertė pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54e42-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="54e42-204">Suma bus perkelta į lauką SF išlaidos ir susumuota su suma, perkelta į lauką SF suma.</span><span class="sxs-lookup"><span data-stu-id="54e42-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="54e42-205">Jei keitimų sumą reikia perkelti į lauką Statistinės išlaidos ir susumuoti su statistine suma, lauke Intrastat statistinė reikšmė pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54e42-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="54e42-206">Produktų pardavimas ES klientams</span><span class="sxs-lookup"><span data-stu-id="54e42-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="54e42-207">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="54e42-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="54e42-208">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="54e42-208">Click New.</span></span>
3. <span data-ttu-id="54e42-209">Lauke Kliento sąskaita pasirinkite ES klientą.</span><span class="sxs-lookup"><span data-stu-id="54e42-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="54e42-210">Pavyzdžiui, pasirinkite DE-012 „Litware Retail‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="54e42-211">Išplėskite dalį Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="54e42-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="54e42-212">Lauke Pristatymo būdas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-213">Pavyzdžiui, pasirinkite 20 Air.</span><span class="sxs-lookup"><span data-stu-id="54e42-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="54e42-214">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-214">Click OK.</span></span>
7. <span data-ttu-id="54e42-215">Perkelkite žymeklį ant pirmosios pardavimo užsakymo eilučių eilutės.</span><span class="sxs-lookup"><span data-stu-id="54e42-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="54e42-216">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-217">Pavyzdžiui, pasirinkite D001.</span><span class="sxs-lookup"><span data-stu-id="54e42-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="54e42-218">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="54e42-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="54e42-219">Spustelėkite skirtuką Užsienio prekyba.</span><span class="sxs-lookup"><span data-stu-id="54e42-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="54e42-220">Transportavimas užpildomas automatiškai pagal pasirinktą pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="54e42-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="54e42-221">Lauke Uostas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="54e42-222">Spustelėkite Finansai.</span><span class="sxs-lookup"><span data-stu-id="54e42-222">Click Financials.</span></span>
    * <span data-ttu-id="54e42-223">Pagal parametrus ši suma bus įtraukta į Intrastat sąskaitos faktūros vertę.</span><span class="sxs-lookup"><span data-stu-id="54e42-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="54e42-224">Spustelėkite Prižiūrėti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="54e42-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="54e42-225">Lauke Išlaidų kodas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-226">Pavyzdžiui, pasirinkite TRANSPORTAVIMAS.</span><span class="sxs-lookup"><span data-stu-id="54e42-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="54e42-227">Pažymėkite žymės langelį Laikyti.</span><span class="sxs-lookup"><span data-stu-id="54e42-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="54e42-228">Lauke Išlaidų vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="54e42-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="54e42-229">Pvz., įveskite „10‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="54e42-230">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54e42-230">Click Save.</span></span>
18. <span data-ttu-id="54e42-231">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54e42-231">Close the page.</span></span>
19. <span data-ttu-id="54e42-232">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="54e42-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="54e42-233">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="54e42-233">Click Invoice.</span></span>
21. <span data-ttu-id="54e42-234">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="54e42-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="54e42-235">Lauke Kiekis pasirinkite Visi.</span><span class="sxs-lookup"><span data-stu-id="54e42-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="54e42-236">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="54e42-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="54e42-237">Įveskite datą lauke Sąskaitos faktūros data.</span><span class="sxs-lookup"><span data-stu-id="54e42-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="54e42-238">Pavyzdžiui, įveskite „2015-01-31‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="54e42-239">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-239">Click OK.</span></span>
26. <span data-ttu-id="54e42-240">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-240">Click OK.</span></span>
27. <span data-ttu-id="54e42-241">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54e42-241">Close the page.</span></span>
28. <span data-ttu-id="54e42-242">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="54e42-242">Click New.</span></span>
29. <span data-ttu-id="54e42-243">Lauke Kliento sąskaita pasirinkite ES klientą.</span><span class="sxs-lookup"><span data-stu-id="54e42-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="54e42-244">Pavyzdžiui, pasirinkite DE-013 „Trey‟ didmeninė prekyba</span><span class="sxs-lookup"><span data-stu-id="54e42-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="54e42-245">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-245">Click OK.</span></span>
31. <span data-ttu-id="54e42-246">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="54e42-247">Pavyzdžiui, pasirinkite D0001.</span><span class="sxs-lookup"><span data-stu-id="54e42-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="54e42-248">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54e42-248">Click Save.</span></span>
33. <span data-ttu-id="54e42-249">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="54e42-249">Click Invoice.</span></span>
34. <span data-ttu-id="54e42-250">Įveskite datą lauke Sąskaitos faktūros data.</span><span class="sxs-lookup"><span data-stu-id="54e42-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="54e42-251">Pavyzdžiui, įveskite datą „2015-01-31‟.</span><span class="sxs-lookup"><span data-stu-id="54e42-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="54e42-252">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-252">Click OK.</span></span>
36. <span data-ttu-id="54e42-253">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="54e42-254">Operacijų perkėlimas į Intrastat</span><span class="sxs-lookup"><span data-stu-id="54e42-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="54e42-255">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="54e42-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="54e42-256">Spustelėkite Perkelti.</span><span class="sxs-lookup"><span data-stu-id="54e42-256">Click Transfer.</span></span>
3. <span data-ttu-id="54e42-257">Lauke Kliento SF pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54e42-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="54e42-258">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="54e42-258">Click Filter.</span></span>
5. <span data-ttu-id="54e42-259">Sąraše pažymėkite eilutę su Data.</span><span class="sxs-lookup"><span data-stu-id="54e42-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="54e42-260">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54e42-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="54e42-261">Pavyzdžiui, įveskite 2015 m. sausio laikotarpio filtrą (tiksli reikšmė priklauso nuo jūsų datos formato): 2015-01-01..2015-01-31</span><span class="sxs-lookup"><span data-stu-id="54e42-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="54e42-262">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-262">Click OK.</span></span>
8. <span data-ttu-id="54e42-263">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54e42-263">Click OK.</span></span>
9. <span data-ttu-id="54e42-264">Sąraše raskite ir pasirinkite perkeltą įrašą.</span><span class="sxs-lookup"><span data-stu-id="54e42-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="54e42-265">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="54e42-265">Click the General tab.</span></span>
    * <span data-ttu-id="54e42-266">Peržiūrėkite perkeltus duomenis – paskirties / išsiuntimo šalį / regioną, kilmės šalį, svorį, kiekį, kiekį papildomais vienetais, prekę, operacijos kodą, SF sumas ir statistines sumas.</span><span class="sxs-lookup"><span data-stu-id="54e42-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="54e42-267">Jei reikia, duomenis galite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="54e42-267">You can modify data if necessary.</span></span>  

