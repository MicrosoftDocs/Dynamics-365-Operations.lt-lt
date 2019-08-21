---
title: Kurti paraišką, kurioje naudojamas RFQ
description: Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d80f84c148ff26bf008a97b06098bfd18c9062d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844161"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="c8a6a-103">Kurti paraišką, kurioje naudojamas RFQ</span><span class="sxs-lookup"><span data-stu-id="c8a6a-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8a6a-104">Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="c8a6a-105">Šiame vedlyje pateiktą pavyzdį galite naudoti demonstracinių duomenų įmonėje USMF, o norėdami atlikti visus veiksmus turite būti prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="c8a6a-106">Paprastai šio vedlio užduotis atlieka įsigijimo specialistai.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="c8a6a-107">Kurti paraišką</span><span class="sxs-lookup"><span data-stu-id="c8a6a-107">Create a requisition</span></span>
1. <span data-ttu-id="c8a6a-108">Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="c8a6a-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-109">Click New.</span></span>
3. <span data-ttu-id="c8a6a-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c8a6a-111">Lauke „Pageidaujama data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="c8a6a-112">Lauke „Apskaitos data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="c8a6a-113">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-113">Click OK.</span></span>
7. <span data-ttu-id="c8a6a-114">Lauke Priežastis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="c8a6a-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-115">Click Add line.</span></span>
9. <span data-ttu-id="c8a6a-116">Lauke Įsigijimo kategorija pasirinkite kategoriją medyje ir tada spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="c8a6a-117">Lauke „Produkto pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="c8a6a-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="c8a6a-119">Lauke Vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="c8a6a-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-120">Click Save.</span></span>
14. <span data-ttu-id="c8a6a-121">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="c8a6a-122">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-122">Click Submit.</span></span>
16. <span data-ttu-id="c8a6a-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-123">Close the page.</span></span>
17. <span data-ttu-id="c8a6a-124">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="c8a6a-125">Iš naujo priskirti darbo eigos užduotį</span><span class="sxs-lookup"><span data-stu-id="c8a6a-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="c8a6a-126">Kitos užduoties metu kuriamas RFQ, siekiant gauti tiekėjų kainų pasiūlymus už produktą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="c8a6a-127">USMF demonstraciniuose duomenyse paraiškos darbo eiga nustatoma naudojant taisyklę, pagal kurią RFQ kūrimo užduotis priskiriama konkrečiam darbuotojui, jei nėra pasirinktas tiekėjas arba jei eilutės vieneto kaina yra 0.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="c8a6a-128">Norėdami toliau vykdyti šio vedlio užduotis, tą užduotį turite priskirti kitam vartotojui (sau).</span><span class="sxs-lookup"><span data-stu-id="c8a6a-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="c8a6a-129">Tai galite atlikti tik jei esate prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="c8a6a-130">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="c8a6a-131">Spustelėkite Peržiūrėti retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-131">Click View history.</span></span>
3. <span data-ttu-id="c8a6a-132">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-132">Refresh the page.</span></span>
4. <span data-ttu-id="c8a6a-133">Išplėskite sekciją Sekimo informacija.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="c8a6a-134">Medyje pasirinkite eilutę, kuri prasideda „Eilutės darbo eiga suaktyvinta“.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="c8a6a-135">Spustelėkite Peržiūrėti darbo eigos informaciją.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-135">Click View workflow details.</span></span>
7. <span data-ttu-id="c8a6a-136">Išplėskite sekciją Darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="c8a6a-137">Spustelėkite Priskirti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-137">Click Reassign.</span></span>
9. <span data-ttu-id="c8a6a-138">Lauke Vartotojas pasirinkite Administratorius.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="c8a6a-139">Spustelėkite Priskirti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-139">Click Reassign.</span></span>
11. <span data-ttu-id="c8a6a-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-140">Close the page.</span></span>
12. <span data-ttu-id="c8a6a-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="c8a6a-142">Kurti RFQ</span><span class="sxs-lookup"><span data-stu-id="c8a6a-142">Create an RFQ</span></span>
1. <span data-ttu-id="c8a6a-143">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-143">Refresh the page.</span></span>
2. <span data-ttu-id="c8a6a-144">Spustelėkite Pasiūlymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="c8a6a-145">Lauke Perkantis juridinis subjektas pasirinkite USMF.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="c8a6a-146">Turite pasirinkti tokį patį juridinį subjektą, koks nurodytas paraiškos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="c8a6a-147">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c8a6a-148">Jei pirkimo paraiškoje yra kelios eilutės, pasirinkite visas eilutes, kurias norite įtraukti į RFQ.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="c8a6a-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-149">Click OK.</span></span>
6. <span data-ttu-id="c8a6a-150">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-150">Refresh the page.</span></span>
7. <span data-ttu-id="c8a6a-151">Atidarykite „FactBox“ ir tada išplėskite sekciją Susiję dokumentai.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="c8a6a-152">Gali būti, kad „FactBox“ jau atidarytas.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-152">You may already have the FactBox open.</span></span> <span data-ttu-id="c8a6a-153">Jame suraskite piktogramą su rodykle (dešinėje eilučių / antraštės perjungimo mygtukų pusėje).</span><span class="sxs-lookup"><span data-stu-id="c8a6a-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="c8a6a-154">Jei rodyklė rodo į dešinę, „FactBox“ jau atidarytas.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="c8a6a-155">Jei rodyklė rodo į kairę, spustelėkite ją, kad atidarytumėte „FactBox“.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="c8a6a-156">Spustelėkite lauko Pasiūlymo patvirtinimas saitą, kad atidarytumėte ką tik sukurtą RFQ.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="c8a6a-157">Spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-157">Click Header.</span></span>
10. <span data-ttu-id="c8a6a-158">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-158">Click Add.</span></span>
11. <span data-ttu-id="c8a6a-159">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="c8a6a-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-160">Click Add.</span></span>
13. <span data-ttu-id="c8a6a-161">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="c8a6a-162">Spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-162">Click Send.</span></span>
15. <span data-ttu-id="c8a6a-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-163">Click OK.</span></span>
16. <span data-ttu-id="c8a6a-164">Spustelėkite Įvesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-164">Click Enter reply.</span></span>
17. <span data-ttu-id="c8a6a-165">Veiksmų srityje spustelėkite Atsakymas.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="c8a6a-166">Spustelėkite Kopijuoti duomenis į atsakymą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="c8a6a-167">Tokiu būdu iš RFQ į atsakymą nukopijuojami duomenys, pvz., kiekis ir datos.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="c8a6a-168">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="c8a6a-169">Tai yra kaina, gauta iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="c8a6a-170">Galbūt taip pat norėsite įvesti papildomą tiekėjo informaciją.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="c8a6a-171">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-171">Click Accept.</span></span>
21. <span data-ttu-id="c8a6a-172">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="c8a6a-173">Patikrinti, ar tiekėjas ir kaina perkelti į paraišką</span><span class="sxs-lookup"><span data-stu-id="c8a6a-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="c8a6a-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-174">Close the page.</span></span>
2. <span data-ttu-id="c8a6a-175">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-175">Click Lines.</span></span>
3. <span data-ttu-id="c8a6a-176">Spustelėkite Susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-176">Click Related information.</span></span>
4. <span data-ttu-id="c8a6a-177">Spustelėkite Pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="c8a6a-178">Pasirinkite eilutę, kuri buvo perkelta į RFQ.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="c8a6a-179">Patikrinkite, ar kaina ir tiekėjas nukopijuoti į paraišką.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="c8a6a-180">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="c8a6a-181">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-181">Click Complete.</span></span>
8. <span data-ttu-id="c8a6a-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-182">Close the page.</span></span>
9. <span data-ttu-id="c8a6a-183">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="c8a6a-183">Click Complete.</span></span>

