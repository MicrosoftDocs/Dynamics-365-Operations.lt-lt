---
title: Paraiškos, kurioje naudojamas RFQ, kūrimas
description: Šioje temoje aiškinama, kaip įtraukti kainos ir tiekėjo informaciją į pirkimo paraišką iš RFQ proceso.
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
ms.openlocfilehash: abe6745682030766eabcd4411121866c9d890be0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149635"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="2ad6a-103">Paraiškos, kurioje naudojamas RFQ, kūrimas</span><span class="sxs-lookup"><span data-stu-id="2ad6a-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ad6a-104">Šioje temoje aiškinama, kaip įtraukti kainos ir tiekėjo informaciją į pirkimo paraišką iš RFQ proceso.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="2ad6a-105">Šiame vedlyje pateiktą pavyzdį galite naudoti demonstracinių duomenų įmonėje USMF, o norėdami atlikti visus veiksmus turite būti prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="2ad6a-106">Paprastai šio vedlio užduotis atlieka įsigijimo specialistai.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="2ad6a-107">Kurti paraišką</span><span class="sxs-lookup"><span data-stu-id="2ad6a-107">Create a requisition</span></span>
1. <span data-ttu-id="2ad6a-108">Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="2ad6a-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-109">Select **New**.</span></span>
3. <span data-ttu-id="2ad6a-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="2ad6a-111">Lauke **Pageidaujama data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="2ad6a-112">Lauke **Apskaitos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="2ad6a-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-113">Select **OK**.</span></span>
7. <span data-ttu-id="2ad6a-114">Lauke **Priežastis** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="2ad6a-115">Pasirinkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-115">Select **Add line**.</span></span>
9. <span data-ttu-id="2ad6a-116">Lauke **Įsigijimo kategorija** pažymėkite kategoriją medyje, tada pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="2ad6a-117">Lauke **Produkto pavadinimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="2ad6a-118">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="2ad6a-119">Lauke **Vienetas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="2ad6a-120">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-120">Select **Save**.</span></span>
14. <span data-ttu-id="2ad6a-121">Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="2ad6a-122">Pasirinkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-122">Select **Submit**.</span></span>
16. <span data-ttu-id="2ad6a-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-123">Close the page.</span></span>
17. <span data-ttu-id="2ad6a-124">Pasirinkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="2ad6a-125">Iš naujo priskirti darbo eigos užduotį</span><span class="sxs-lookup"><span data-stu-id="2ad6a-125">Reassign a workflow task</span></span>
<span data-ttu-id="2ad6a-126">Kitos užduoties metu kuriamas RFQ, siekiant gauti tiekėjų kainų pasiūlymus už produktą.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="2ad6a-127">USMF demonstraciniuose duomenyse paraiškos darbo eiga nustatoma naudojant taisyklę, pagal kurią RFQ kūrimo užduotis priskiriama konkrečiam darbuotojui, jei nėra pasirinktas tiekėjas arba jei eilutės vieneto kaina yra 0.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="2ad6a-128">Norėdami toliau vykdyti šio vedlio užduotis, tą užduotį turite priskirti kitam vartotojui (sau).</span><span class="sxs-lookup"><span data-stu-id="2ad6a-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="2ad6a-129">Tai galite atlikti tik jei esate prisijungęs kaip Administratorius.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="2ad6a-130">Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="2ad6a-131">Pažymėkite **Žiūrėti istoriją**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-131">Select **View history**.</span></span>
3. <span data-ttu-id="2ad6a-132">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-132">Refresh the page.</span></span>
4. <span data-ttu-id="2ad6a-133">Išplėskite skyrių **Sekimo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="2ad6a-134">Medyje pažymėkite eilutę, kuri prasideda „Eilutės darbo eiga suaktyvinta“.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="2ad6a-135">Pažymėkite **Žiūrėti darbo eigos išsamią informaciją**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="2ad6a-136">Išplėskite skyrių **Darbo elementai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="2ad6a-137">Pažymėkite **Priskirti iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="2ad6a-138">Lauke **Vartotojas** pažymėkite **Administratorius**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="2ad6a-139">Pažymėkite **Priskirti iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="2ad6a-140">Uždarykite du puslapius.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="2ad6a-141">Kurti RFQ</span><span class="sxs-lookup"><span data-stu-id="2ad6a-141">Create an RFQ</span></span>

1. <span data-ttu-id="2ad6a-142">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-142">Refresh the page.</span></span>
2. <span data-ttu-id="2ad6a-143">Pažymėkite **Prašyti kainos**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="2ad6a-144">Lauke **Juridinio asmens pirkimas** pažymėkite **USMF**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="2ad6a-145">Turite pasirinkti tokį patį juridinį subjektą, koks nurodytas paraiškos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="2ad6a-146">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-146">In the list, mark the selected row.</span></span> <span data-ttu-id="2ad6a-147">Jei pirkimo paraiškoje yra kelios eilutės, pasirinkite visas eilutes, kurias norite įtraukti į RFQ.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="2ad6a-148">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-148">Select **OK**.</span></span>
6. <span data-ttu-id="2ad6a-149">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-149">Refresh the page.</span></span>
7. <span data-ttu-id="2ad6a-150">Įsitikinkite, kad „FactBox“ yra atidarytas, tada išplėskite skyrių **Susiję dokumentai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="2ad6a-151">Pažymėkite saitą lauke **Prašyti kainos**, kad atidarytumėte ką tik sukurtą RFQ.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="2ad6a-152">Pažymėkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-152">Select **Header**.</span></span>
10. <span data-ttu-id="2ad6a-153">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-153">Select **Add**.</span></span>
11. <span data-ttu-id="2ad6a-154">Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="2ad6a-155">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-155">Select **Add**.</span></span>
13. <span data-ttu-id="2ad6a-156">Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="2ad6a-157">Pažymėkite **Siųsti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-157">Select **Send**.</span></span>
15. <span data-ttu-id="2ad6a-158">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-158">Select **OK**.</span></span>
16. <span data-ttu-id="2ad6a-159">Pažymėkite **Įvesti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="2ad6a-160">Veiksmų srityje pasirinkite **Atsakymas**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="2ad6a-161">Pažymėkite **Kopijuoti duomenis į atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="2ad6a-162">Tokiu būdu iš RFQ į atsakymą nukopijuojami duomenys, pvz., kiekis ir datos.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="2ad6a-163">Lauke **Vieneto kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="2ad6a-164">Tai yra kaina, gauta iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="2ad6a-165">Galbūt taip pat norėsite įvesti papildomą tiekėjo informaciją.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="2ad6a-166">Pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-166">Select **Accept**.</span></span>
21. <span data-ttu-id="2ad6a-167">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="2ad6a-168">Patikrinti, ar tiekėjas ir kaina perkelti į paraišką</span><span class="sxs-lookup"><span data-stu-id="2ad6a-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="2ad6a-169">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-169">Close the page.</span></span>
2. <span data-ttu-id="2ad6a-170">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-170">Select **Lines**.</span></span>
3. <span data-ttu-id="2ad6a-171">Pažymėkite **Susijusi informacija**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-171">Select **Related information**.</span></span>
4. <span data-ttu-id="2ad6a-172">Pažymėkite **Pirkimo paraiška**.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="2ad6a-173">Pasirinkite eilutę, kuri buvo perkelta į RFQ.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="2ad6a-174">Patikrinkite, ar kaina ir tiekėjas nukopijuoti į paraišką.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="2ad6a-175">Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="2ad6a-176">Pasirinkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-176">Select Complete.</span></span>
8. <span data-ttu-id="2ad6a-177">Pasirinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-177">Select the page.</span></span>
9. <span data-ttu-id="2ad6a-178">Pasirinkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="2ad6a-178">Select Complete.</span></span>

