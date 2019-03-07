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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "344989"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="f11f0-103">Kurti paraišką, kurioje naudojamas RFQ</span><span class="sxs-lookup"><span data-stu-id="f11f0-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f11f0-104">Šiame vedlyje parodoma, kaip iš RFQ proceso kainos ir tiekėjo informaciją įtraukti į pirkimo paraišką.</span><span class="sxs-lookup"><span data-stu-id="f11f0-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="f11f0-105">Šiame vedlyje pateiktą pavyzdį galite naudoti demonstracinių duomenų įmonėje USMF, o norėdami atlikti visus veiksmus turite būti prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="f11f0-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="f11f0-106">Paprastai šio vedlio užduotis atlieka įsigijimo specialistai.</span><span class="sxs-lookup"><span data-stu-id="f11f0-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="f11f0-107">Kurti paraišką</span><span class="sxs-lookup"><span data-stu-id="f11f0-107">Create a requisition</span></span>
1. <span data-ttu-id="f11f0-108">Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos.</span><span class="sxs-lookup"><span data-stu-id="f11f0-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="f11f0-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f11f0-109">Click New.</span></span>
3. <span data-ttu-id="f11f0-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f11f0-111">Lauke „Pageidaujama data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="f11f0-112">Lauke „Apskaitos data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="f11f0-113">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f11f0-113">Click OK.</span></span>
7. <span data-ttu-id="f11f0-114">Lauke Priežastis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="f11f0-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-115">Click Add line.</span></span>
9. <span data-ttu-id="f11f0-116">Lauke Įsigijimo kategorija pasirinkite kategoriją medyje ir tada spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f11f0-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="f11f0-117">Lauke „Produkto pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="f11f0-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f11f0-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="f11f0-119">Lauke Vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="f11f0-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-120">Click Save.</span></span>
14. <span data-ttu-id="f11f0-121">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="f11f0-122">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-122">Click Submit.</span></span>
16. <span data-ttu-id="f11f0-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-123">Close the page.</span></span>
17. <span data-ttu-id="f11f0-124">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="f11f0-125">Iš naujo priskirti darbo eigos užduotį</span><span class="sxs-lookup"><span data-stu-id="f11f0-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="f11f0-126">Kitos užduoties metu kuriamas RFQ, siekiant gauti tiekėjų kainų pasiūlymus už produktą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="f11f0-127">USMF demonstraciniuose duomenyse paraiškos darbo eiga nustatoma naudojant taisyklę, pagal kurią RFQ kūrimo užduotis priskiriama konkrečiam darbuotojui, jei nėra pasirinktas tiekėjas arba jei eilutės vieneto kaina yra 0.</span><span class="sxs-lookup"><span data-stu-id="f11f0-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="f11f0-128">Norėdami toliau vykdyti šio vedlio užduotis, tą užduotį turite priskirti kitam vartotojui (sau).</span><span class="sxs-lookup"><span data-stu-id="f11f0-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="f11f0-129">Tai galite atlikti tik jei esate prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="f11f0-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="f11f0-130">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="f11f0-131">Spustelėkite Peržiūrėti retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-131">Click View history.</span></span>
3. <span data-ttu-id="f11f0-132">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-132">Refresh the page.</span></span>
4. <span data-ttu-id="f11f0-133">Išplėskite sekciją Sekimo informacija.</span><span class="sxs-lookup"><span data-stu-id="f11f0-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="f11f0-134">Medyje pasirinkite eilutę, kuri prasideda „Eilutės darbo eiga suaktyvinta“.</span><span class="sxs-lookup"><span data-stu-id="f11f0-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="f11f0-135">Spustelėkite Peržiūrėti darbo eigos informaciją.</span><span class="sxs-lookup"><span data-stu-id="f11f0-135">Click View workflow details.</span></span>
7. <span data-ttu-id="f11f0-136">Išplėskite sekciją Darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="f11f0-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="f11f0-137">Spustelėkite Priskirti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="f11f0-137">Click Reassign.</span></span>
9. <span data-ttu-id="f11f0-138">Lauke Vartotojas pasirinkite Administratorius.</span><span class="sxs-lookup"><span data-stu-id="f11f0-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="f11f0-139">Spustelėkite Priskirti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="f11f0-139">Click Reassign.</span></span>
11. <span data-ttu-id="f11f0-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-140">Close the page.</span></span>
12. <span data-ttu-id="f11f0-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="f11f0-142">Kurti RFQ</span><span class="sxs-lookup"><span data-stu-id="f11f0-142">Create an RFQ</span></span>
1. <span data-ttu-id="f11f0-143">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-143">Refresh the page.</span></span>
2. <span data-ttu-id="f11f0-144">Spustelėkite Pasiūlymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="f11f0-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="f11f0-145">Lauke Perkantis juridinis subjektas pasirinkite USMF.</span><span class="sxs-lookup"><span data-stu-id="f11f0-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="f11f0-146">Turite pasirinkti tokį patį juridinį subjektą, koks nurodytas paraiškos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f11f0-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="f11f0-147">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f11f0-148">Jei pirkimo paraiškoje yra kelios eilutės, pasirinkite visas eilutes, kurias norite įtraukti į RFQ.</span><span class="sxs-lookup"><span data-stu-id="f11f0-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="f11f0-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f11f0-149">Click OK.</span></span>
6. <span data-ttu-id="f11f0-150">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-150">Refresh the page.</span></span>
7. <span data-ttu-id="f11f0-151">Atidarykite „FactBox“ ir tada išplėskite sekciją Susiję dokumentai.</span><span class="sxs-lookup"><span data-stu-id="f11f0-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="f11f0-152">Gali būti, kad „FactBox“ jau atidarytas.</span><span class="sxs-lookup"><span data-stu-id="f11f0-152">You may already have the FactBox open.</span></span> <span data-ttu-id="f11f0-153">Jame suraskite piktogramą su rodykle (dešinėje eilučių / antraštės perjungimo mygtukų pusėje).</span><span class="sxs-lookup"><span data-stu-id="f11f0-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="f11f0-154">Jei rodyklė rodo į dešinę, „FactBox“ jau atidarytas.</span><span class="sxs-lookup"><span data-stu-id="f11f0-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="f11f0-155">Jei rodyklė rodo į kairę, spustelėkite ją, kad atidarytumėte „FactBox“.</span><span class="sxs-lookup"><span data-stu-id="f11f0-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="f11f0-156">Spustelėkite lauko Pasiūlymo patvirtinimas saitą, kad atidarytumėte ką tik sukurtą RFQ.</span><span class="sxs-lookup"><span data-stu-id="f11f0-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="f11f0-157">Spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="f11f0-157">Click Header.</span></span>
10. <span data-ttu-id="f11f0-158">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-158">Click Add.</span></span>
11. <span data-ttu-id="f11f0-159">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="f11f0-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-160">Click Add.</span></span>
13. <span data-ttu-id="f11f0-161">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f11f0-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="f11f0-162">Spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-162">Click Send.</span></span>
15. <span data-ttu-id="f11f0-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f11f0-163">Click OK.</span></span>
16. <span data-ttu-id="f11f0-164">Spustelėkite Įvesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-164">Click Enter reply.</span></span>
17. <span data-ttu-id="f11f0-165">Veiksmų srityje spustelėkite Atsakymas.</span><span class="sxs-lookup"><span data-stu-id="f11f0-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="f11f0-166">Spustelėkite Kopijuoti duomenis į atsakymą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="f11f0-167">Tokiu būdu iš RFQ į atsakymą nukopijuojami duomenys, pvz., kiekis ir datos.</span><span class="sxs-lookup"><span data-stu-id="f11f0-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="f11f0-168">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f11f0-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="f11f0-169">Tai yra kaina, gauta iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="f11f0-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="f11f0-170">Galbūt taip pat norėsite įvesti papildomą tiekėjo informaciją.</span><span class="sxs-lookup"><span data-stu-id="f11f0-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="f11f0-171">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-171">Click Accept.</span></span>
21. <span data-ttu-id="f11f0-172">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f11f0-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="f11f0-173">Patikrinti, ar tiekėjas ir kaina perkelti į paraišką</span><span class="sxs-lookup"><span data-stu-id="f11f0-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="f11f0-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-174">Close the page.</span></span>
2. <span data-ttu-id="f11f0-175">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="f11f0-175">Click Lines.</span></span>
3. <span data-ttu-id="f11f0-176">Spustelėkite Susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="f11f0-176">Click Related information.</span></span>
4. <span data-ttu-id="f11f0-177">Spustelėkite Pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="f11f0-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="f11f0-178">Pasirinkite eilutę, kuri buvo perkelta į RFQ.</span><span class="sxs-lookup"><span data-stu-id="f11f0-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="f11f0-179">Patikrinkite, ar kaina ir tiekėjas nukopijuoti į paraišką.</span><span class="sxs-lookup"><span data-stu-id="f11f0-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="f11f0-180">Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f11f0-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="f11f0-181">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-181">Click Complete.</span></span>
8. <span data-ttu-id="f11f0-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f11f0-182">Close the page.</span></span>
9. <span data-ttu-id="f11f0-183">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="f11f0-183">Click Complete.</span></span>

