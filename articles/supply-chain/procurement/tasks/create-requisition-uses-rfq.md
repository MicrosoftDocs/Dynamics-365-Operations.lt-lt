--- 
title: "Kurti paraišką, kurioje naudojamas RFQ"
description: "Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2c2daad961ec5c47ca49b2e53a2118570caf6a58
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="51889-103">Kurti paraišką, kurioje naudojamas RFQ</span><span class="sxs-lookup"><span data-stu-id="51889-103">Create a requisition that uses an RFQ</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51889-104">Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką.</span><span class="sxs-lookup"><span data-stu-id="51889-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="51889-105">Šiame vedlyje pateiktą pavyzdį galite naudoti demonstracinių duomenų įmonėje USMF, o norėdami atlikti visus veiksmus turite būti prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="51889-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="51889-106">Paprastai šio vedlio užduotis atlieka įsigijimo specialistai.</span><span class="sxs-lookup"><span data-stu-id="51889-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="51889-107">Kurti paraišką</span><span class="sxs-lookup"><span data-stu-id="51889-107">Create a requisition</span></span>
1. <span data-ttu-id="51889-108">Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos.</span><span class="sxs-lookup"><span data-stu-id="51889-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="51889-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="51889-109">Click New.</span></span>
3. <span data-ttu-id="51889-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="51889-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="51889-111">Lauke „Pageidaujama data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="51889-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="51889-112">Lauke „Apskaitos data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="51889-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="51889-113">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="51889-113">Click OK.</span></span>
7. <span data-ttu-id="51889-114">Lauke Priežastis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="51889-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="51889-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="51889-115">Click Add line.</span></span>
9. <span data-ttu-id="51889-116">Lauke Įsigijimo kategorija pasirinkite kategoriją medyje ir tada spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="51889-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="51889-117">Lauke „Produkto pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="51889-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="51889-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="51889-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="51889-119">Lauke Vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="51889-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="51889-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="51889-120">Click Save.</span></span>
14. <span data-ttu-id="51889-121">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="51889-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="51889-122">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="51889-122">Click Submit.</span></span>
16. <span data-ttu-id="51889-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-123">Close the page.</span></span>
17. <span data-ttu-id="51889-124">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="51889-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="51889-125">Iš naujo priskirti darbo eigos užduotį</span><span class="sxs-lookup"><span data-stu-id="51889-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="51889-126">Kitos užduoties metu kuriamas RFQ, siekiant gauti tiekėjų kainų pasiūlymus už produktą.</span><span class="sxs-lookup"><span data-stu-id="51889-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="51889-127">USMF demonstraciniuose duomenyse paraiškos darbo eiga nustatoma naudojant taisyklę, pagal kurią RFQ kūrimo užduotis priskiriama konkrečiam darbuotojui, jei nėra pasirinktas tiekėjas arba jei eilutės vieneto kaina yra 0.</span><span class="sxs-lookup"><span data-stu-id="51889-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="51889-128">Norėdami toliau vykdyti šio vedlio užduotis, tą užduotį turite priskirti kitam vartotojui (sau).</span><span class="sxs-lookup"><span data-stu-id="51889-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="51889-129">Tai galite atlikti tik jei esate prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="51889-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="51889-130">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="51889-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="51889-131">Spustelėkite Peržiūrėti retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="51889-131">Click View history.</span></span>
3. <span data-ttu-id="51889-132">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-132">Refresh the page.</span></span>
4. <span data-ttu-id="51889-133">Išplėskite sekciją Sekimo informacija.</span><span class="sxs-lookup"><span data-stu-id="51889-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="51889-134">Medyje pasirinkite eilutę, kuri prasideda „Eilutės darbo eiga suaktyvinta“.</span><span class="sxs-lookup"><span data-stu-id="51889-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="51889-135">Spustelėkite Peržiūrėti darbo eigos informaciją.</span><span class="sxs-lookup"><span data-stu-id="51889-135">Click View workflow details.</span></span>
7. <span data-ttu-id="51889-136">Išplėskite sekciją Darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="51889-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="51889-137">Spustelėkite Priskirti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="51889-137">Click Reassign.</span></span>
9. <span data-ttu-id="51889-138">Lauke Vartotojas pasirinkite Administratorius.</span><span class="sxs-lookup"><span data-stu-id="51889-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="51889-139">Spustelėkite Priskirti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="51889-139">Click Reassign.</span></span>
11. <span data-ttu-id="51889-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-140">Close the page.</span></span>
12. <span data-ttu-id="51889-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="51889-142">Kurti RFQ</span><span class="sxs-lookup"><span data-stu-id="51889-142">Create an RFQ</span></span>
1. <span data-ttu-id="51889-143">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-143">Refresh the page.</span></span>
2. <span data-ttu-id="51889-144">Spustelėkite Pasiūlymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="51889-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="51889-145">Lauke Perkantis juridinis subjektas pasirinkite USMF.</span><span class="sxs-lookup"><span data-stu-id="51889-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="51889-146">Turite pasirinkti tokį patį juridinį subjektą, koks nurodytas paraiškos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="51889-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="51889-147">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="51889-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="51889-148">Jei pirkimo paraiškoje yra kelios eilutės, pasirinkite visas eilutes, kurias norite įtraukti į RFQ.</span><span class="sxs-lookup"><span data-stu-id="51889-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="51889-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="51889-149">Click OK.</span></span>
6. <span data-ttu-id="51889-150">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-150">Refresh the page.</span></span>
7. <span data-ttu-id="51889-151">Atidarykite „FactBox“ ir tada išplėskite sekciją Susiję dokumentai.</span><span class="sxs-lookup"><span data-stu-id="51889-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="51889-152">Gali būti, kad „FactBox“ jau atidarytas.</span><span class="sxs-lookup"><span data-stu-id="51889-152">You may already have the FactBox open.</span></span> <span data-ttu-id="51889-153">Jame suraskite piktogramą su rodykle (dešinėje eilučių / antraštės perjungimo mygtukų pusėje).</span><span class="sxs-lookup"><span data-stu-id="51889-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="51889-154">Jei rodyklė rodo į dešinę, „FactBox“ jau atidarytas.</span><span class="sxs-lookup"><span data-stu-id="51889-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="51889-155">Jei rodyklė rodo į kairę, spustelėkite ją, kad atidarytumėte „FactBox“.</span><span class="sxs-lookup"><span data-stu-id="51889-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="51889-156">Spustelėkite lauko Pasiūlymo patvirtinimas saitą, kad atidarytumėte ką tik sukurtą RFQ.</span><span class="sxs-lookup"><span data-stu-id="51889-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="51889-157">Spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="51889-157">Click Header.</span></span>
10. <span data-ttu-id="51889-158">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="51889-158">Click Add.</span></span>
11. <span data-ttu-id="51889-159">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="51889-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="51889-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="51889-160">Click Add.</span></span>
13. <span data-ttu-id="51889-161">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="51889-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="51889-162">Spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="51889-162">Click Send.</span></span>
15. <span data-ttu-id="51889-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="51889-163">Click OK.</span></span>
16. <span data-ttu-id="51889-164">Spustelėkite Įvesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="51889-164">Click Enter reply.</span></span>
17. <span data-ttu-id="51889-165">Veiksmų srityje spustelėkite Atsakymas.</span><span class="sxs-lookup"><span data-stu-id="51889-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="51889-166">Spustelėkite Kopijuoti duomenis į atsakymą.</span><span class="sxs-lookup"><span data-stu-id="51889-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="51889-167">Tokiu būdu iš RFQ į atsakymą nukopijuojami duomenys, pvz., kiekis ir datos.</span><span class="sxs-lookup"><span data-stu-id="51889-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="51889-168">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="51889-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="51889-169">Tai yra kaina, gauta iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="51889-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="51889-170">Galbūt taip pat norėsite įvesti papildomą tiekėjo informaciją.</span><span class="sxs-lookup"><span data-stu-id="51889-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="51889-171">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="51889-171">Click Accept.</span></span>
21. <span data-ttu-id="51889-172">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="51889-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="51889-173">Patikrinti, ar tiekėjas ir kaina perkelti į paraišką</span><span class="sxs-lookup"><span data-stu-id="51889-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="51889-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-174">Close the page.</span></span>
2. <span data-ttu-id="51889-175">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="51889-175">Click Lines.</span></span>
3. <span data-ttu-id="51889-176">Spustelėkite Susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="51889-176">Click Related information.</span></span>
4. <span data-ttu-id="51889-177">Spustelėkite Pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="51889-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="51889-178">Pasirinkite eilutę, kuri buvo perkelta į RFQ.</span><span class="sxs-lookup"><span data-stu-id="51889-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="51889-179">Patikrinkite, ar kaina ir tiekėjas nukopijuoti į paraišką.</span><span class="sxs-lookup"><span data-stu-id="51889-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="51889-180">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="51889-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="51889-181">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="51889-181">Click Complete.</span></span>
8. <span data-ttu-id="51889-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51889-182">Close the page.</span></span>
9. <span data-ttu-id="51889-183">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="51889-183">Click Complete.</span></span>


