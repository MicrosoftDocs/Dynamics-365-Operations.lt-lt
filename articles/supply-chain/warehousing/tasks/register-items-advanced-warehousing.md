---
title: Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą
description: Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f8c39ade92b80c561c9e96220a59e7f222d77e6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216993"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="af683-103">Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="af683-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af683-104">Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="af683-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="af683-105">Paprastai tai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="af683-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="af683-106">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="af683-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="af683-107">Prieš pradėdami šį vadovą, turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute.</span><span class="sxs-lookup"><span data-stu-id="af683-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="af683-108">Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="af683-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="af683-109">Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje įgalintas sandėlio valdymo procesas.</span><span class="sxs-lookup"><span data-stu-id="af683-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="af683-110">Naudojamame sandėlyje turi būti įgalinti sandėlio valdymo procesai, o vieta, kurią naudojate prekių gavimui, turi būti kontroliuojama numerio lentelės.</span><span class="sxs-lookup"><span data-stu-id="af683-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="af683-111">Jei naudojate USMF, kurdami savo pirkimo užsakymą, galite naudoti įmonės klientą 1001, sandėlį 51 ir elementą M9200.</span><span class="sxs-lookup"><span data-stu-id="af683-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="af683-112">Pasižymėkite savo sukurto pirkimo užsakymo numerį ir prekės numerį bei pirkimo užsakymo eilutėje naudotą vietą.</span><span class="sxs-lookup"><span data-stu-id="af683-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="af683-113">Prekių gavimo žurnalo antraštės kūrimas</span><span class="sxs-lookup"><span data-stu-id="af683-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="af683-114">Eikite į Prekių gavimas.</span><span class="sxs-lookup"><span data-stu-id="af683-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="af683-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="af683-115">Click New.</span></span>
3. <span data-ttu-id="af683-116">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="af683-117">Jei naudojate USMF, galite surinkti WHS.</span><span class="sxs-lookup"><span data-stu-id="af683-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="af683-118">Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinksite, turi turėti šias savybes: patikros rinkimo vieta turi būti nustatyta į „Ne“ ir karantino valdymas turi būti nustatytas į „Ne“.</span><span class="sxs-lookup"><span data-stu-id="af683-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="af683-119">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="af683-120">Lauke Teritorija surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="af683-121">Pasirinkite vietą, kurią naudojote savo pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="af683-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="af683-122">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="af683-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="af683-123">Jei USMF naudojote 51 sandėlį, pasirinkite 5 vietą.</span><span class="sxs-lookup"><span data-stu-id="af683-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="af683-124">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="af683-125">Pasirinkite tinkamą jūsų pasirinktos svetainės sandėlį.</span><span class="sxs-lookup"><span data-stu-id="af683-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="af683-126">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="af683-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="af683-127">Jeigu USMF naudojate reikšmių pavyzdžius, pasirinkite „51“.</span><span class="sxs-lookup"><span data-stu-id="af683-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="af683-128">Lauke Vieta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="af683-129">Pasirinkite tinkamą jūsų pasirinktos vietos sandėlį.</span><span class="sxs-lookup"><span data-stu-id="af683-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="af683-130">Vieta turi būti susieta su vietos šablonu, kuris yra kontroliuojamas pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="af683-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="af683-131">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="af683-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="af683-132">Jeigu USMF naudojate reikšmių pavyzdžius, pasirinkite „Bulk-008“.</span><span class="sxs-lookup"><span data-stu-id="af683-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="af683-133">Dešiniuoju pelės mygtuku spustelėkite lauko Numerio lentelė išplečiamąją rodyklę ir pasirinkite Peržiūrėti išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="af683-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="af683-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="af683-134">Click New.</span></span>
10. <span data-ttu-id="af683-135">Lauke Numerio lentelė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="af683-136">Pasižymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="af683-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="af683-137">Click Save.</span></span>
12. <span data-ttu-id="af683-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="af683-138">Close the page.</span></span>
13. <span data-ttu-id="af683-139">Lauke Numerio lentelė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="af683-140">Įveskite ką tik sukurtos numerio lentelės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="af683-141">Tai bus numatytoji visų žurnalo eilučių reikšmė.</span><span class="sxs-lookup"><span data-stu-id="af683-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="af683-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="af683-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="af683-143">Įtraukti eilutę</span><span class="sxs-lookup"><span data-stu-id="af683-143">Add a line</span></span>
1. <span data-ttu-id="af683-144">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="af683-144">Click Add line.</span></span>
2. <span data-ttu-id="af683-145">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af683-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="af683-146">Įveskite prekės numerį, kurį naudojote pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="af683-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="af683-147">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="af683-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="af683-148">Įveskite norimą registruoti kiekį.</span><span class="sxs-lookup"><span data-stu-id="af683-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="af683-149">Lauke Data nurodoma data, kada atsargose bus užregistruotas turimas šios prekės kiekis.</span><span class="sxs-lookup"><span data-stu-id="af683-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="af683-150">Lauką Partijos ID užpildys sistema, jei jį galima identifikuoti pagal pateiktą informaciją.</span><span class="sxs-lookup"><span data-stu-id="af683-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="af683-151">Kitu atveju turite įtraukti jį patys.</span><span class="sxs-lookup"><span data-stu-id="af683-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="af683-152">Tai yra privalomas laukas, kuris susieja šią registraciją su konkrečia šaltinio dokumento eilute.</span><span class="sxs-lookup"><span data-stu-id="af683-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="af683-153">Registracijos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="af683-153">Complete the registration</span></span>
1. <span data-ttu-id="af683-154">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="af683-154">Click Validate.</span></span>
    * <span data-ttu-id="af683-155">Patikrinama, ar žurnalas parengtas registruoti.</span><span class="sxs-lookup"><span data-stu-id="af683-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="af683-156">Jei patikrinti nepavyksta, norint registruoti žurnalą reikia ištaisyti klaidas.</span><span class="sxs-lookup"><span data-stu-id="af683-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="af683-157">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="af683-157">Click OK.</span></span>
    * <span data-ttu-id="af683-158">Spustelėję Gerai, patikrinkite pranešimą.</span><span class="sxs-lookup"><span data-stu-id="af683-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="af683-159">Turėtumėte gauti pranešimą, kuriame parašyta, kad žurnale problemų nėra.</span><span class="sxs-lookup"><span data-stu-id="af683-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="af683-160">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="af683-160">Click Post.</span></span>
4. <span data-ttu-id="af683-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="af683-161">Click OK.</span></span>
    * <span data-ttu-id="af683-162">Spustelėję Gerai, patikrinkite pranešimų juostą.</span><span class="sxs-lookup"><span data-stu-id="af683-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="af683-163">Turėtumėte gauti pranešimą, kuriame parašyta, kad operacija baigta.</span><span class="sxs-lookup"><span data-stu-id="af683-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="af683-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="af683-164">Close the page.</span></span>

