--- 
title: "Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą"
description: "Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus."
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4721ec8437ff7907a417a331bba887847c7e447a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="8505f-103">Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="8505f-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8505f-104">Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="8505f-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="8505f-105">Paprastai tai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="8505f-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="8505f-106">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="8505f-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="8505f-107">Prieš pradėdami šį vadovą, turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute.</span><span class="sxs-lookup"><span data-stu-id="8505f-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="8505f-108">Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="8505f-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="8505f-109">Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje įgalintas sandėlio valdymo procesas.</span><span class="sxs-lookup"><span data-stu-id="8505f-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="8505f-110">Naudojamas sandėlis turi būti įgalintas naudoti sandėlio valdymo procesus, o naudojama gavimo vieta turi būti kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="8505f-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="8505f-111">Jei naudojate USMF, norėdami sukurti savo PO, galite naudoti įmonės sąskaitą 1001, 51 sandėlį ir prekę M9200.</span><span class="sxs-lookup"><span data-stu-id="8505f-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="8505f-112">Pasižymėkite savo sukurto pirkimo užsakymo numerį ir prekės numerį bei pirkimo užsakymo eilutėje naudotą vietą.</span><span class="sxs-lookup"><span data-stu-id="8505f-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="8505f-113">Prekių gavimo žurnalo antraštės kūrimas</span><span class="sxs-lookup"><span data-stu-id="8505f-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="8505f-114">Eikite į Prekių gavimas.</span><span class="sxs-lookup"><span data-stu-id="8505f-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="8505f-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8505f-115">Click New.</span></span>
3. <span data-ttu-id="8505f-116">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8505f-117">Jei naudojate USMF, galite surinkti WHS.</span><span class="sxs-lookup"><span data-stu-id="8505f-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="8505f-118">Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinkote, turi turėti toliau nurodytas ypatybes: Tikrinti paėmimo vietą turi būti nustatyta į Ne ir Sulaikymo valdymas turi būti nustatyta į Ne.</span><span class="sxs-lookup"><span data-stu-id="8505f-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="8505f-119">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="8505f-120">Lauke Teritorija surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="8505f-121">Pasirinkite vietą, kurią naudojote savo pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8505f-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="8505f-122">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8505f-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="8505f-123">Jei USMF naudojote 51 sandėlį, pasirinkite 5 vietą.</span><span class="sxs-lookup"><span data-stu-id="8505f-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="8505f-124">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="8505f-125">Pasirinkite tinkamą pasirinktos vietos sandėlį.</span><span class="sxs-lookup"><span data-stu-id="8505f-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="8505f-126">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8505f-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="8505f-127">Jei USMF naudojate reikšmių pavyzdžius, pasirinkite 51.</span><span class="sxs-lookup"><span data-stu-id="8505f-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="8505f-128">Lauke Vieta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="8505f-129">Pasirinkite tinkamą pasirinkto sandėlio vietą.</span><span class="sxs-lookup"><span data-stu-id="8505f-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="8505f-130">Vieta turi būti susieta su vietos šablonu, kuris yra kontroliuojamas pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="8505f-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="8505f-131">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8505f-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="8505f-132">Jei USMF naudojate reikšmių pavyzdžius, pasirinkite Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="8505f-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="8505f-133">Dešiniuoju pelės mygtuku spustelėkite lauko Numerio lentelė išplečiamąją rodyklę ir pasirinkite Peržiūrėti išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="8505f-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="8505f-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8505f-134">Click New.</span></span>
10. <span data-ttu-id="8505f-135">Lauke Numerio lentelė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="8505f-136">Pasižymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="8505f-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8505f-137">Click Save.</span></span>
12. <span data-ttu-id="8505f-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8505f-138">Close the page.</span></span>
13. <span data-ttu-id="8505f-139">Lauke Numerio lentelė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="8505f-140">Įveskite ką tik sukurtos numerio lentelės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="8505f-141">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8505f-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="8505f-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8505f-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="8505f-143">Įtraukti eilutę</span><span class="sxs-lookup"><span data-stu-id="8505f-143">Add a line</span></span>
1. <span data-ttu-id="8505f-144">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="8505f-144">Click Add line.</span></span>
2. <span data-ttu-id="8505f-145">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8505f-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8505f-146">Įveskite prekės numerį, kurį naudojote pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8505f-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="8505f-147">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8505f-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8505f-148">Įveskite norimą registruoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="8505f-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="8505f-149">Lauke Data nurodoma data, kada atsargose bus užregistruotas turimas šios prekės kiekis.</span><span class="sxs-lookup"><span data-stu-id="8505f-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="8505f-150">Lauką Partijos ID užpildys sistema, jei jį galima identifikuoti pagal pateiktą informaciją.</span><span class="sxs-lookup"><span data-stu-id="8505f-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="8505f-151">Kitu atveju turite įtraukti jį patys.</span><span class="sxs-lookup"><span data-stu-id="8505f-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="8505f-152">Tai yra privalomas laukas, kuris susieja šią registraciją su konkrečia šaltinio dokumento eilute.</span><span class="sxs-lookup"><span data-stu-id="8505f-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="8505f-153">Registracijos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="8505f-153">Complete the registration</span></span>
1. <span data-ttu-id="8505f-154">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="8505f-154">Click Validate.</span></span>
    * <span data-ttu-id="8505f-155">Patikrinama, ar žurnalas parengtas registruoti.</span><span class="sxs-lookup"><span data-stu-id="8505f-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="8505f-156">Jei patikrinti nepavyksta, norint registruoti žurnalą reikia ištaisyti klaidas.</span><span class="sxs-lookup"><span data-stu-id="8505f-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="8505f-157">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8505f-157">Click OK.</span></span>
    * <span data-ttu-id="8505f-158">Spustelėję Gerai, patikrinkite pranešimą.</span><span class="sxs-lookup"><span data-stu-id="8505f-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="8505f-159">Turėtumėte gauti pranešimą, kuriame parašyta, kad žurnale problemų nėra.</span><span class="sxs-lookup"><span data-stu-id="8505f-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="8505f-160">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="8505f-160">Click Post.</span></span>
4. <span data-ttu-id="8505f-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8505f-161">Click OK.</span></span>
    * <span data-ttu-id="8505f-162">Spustelėję Gerai, patikrinkite pranešimų juostą.</span><span class="sxs-lookup"><span data-stu-id="8505f-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="8505f-163">Turėtumėte gauti pranešimą, kuriame parašyta, kad operacija baigta.</span><span class="sxs-lookup"><span data-stu-id="8505f-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="8505f-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8505f-164">Close the page.</span></span>


