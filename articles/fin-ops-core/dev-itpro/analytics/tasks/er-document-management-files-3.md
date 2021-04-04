---
title: ER dokumentų valdymo failų naudojimas formato išvestyse (3 dalis – formato kūrimas)
description: Šioje temoje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų formatą, kad būtų galima naudoti dokumentų valdymo failus ER išvestyje. (3 dalis)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1ebc15cd980734aebec63d6758404868c1e36
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559754"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="61e2e-104">ER dokumentų valdymo failų naudojimas formato išvestyse (3 dalis – formato kūrimas)</span><span class="sxs-lookup"><span data-stu-id="61e2e-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61e2e-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="61e2e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="61e2e-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="61e2e-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="61e2e-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis. Duomenų modelio išplėtimas)“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="61e2e-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="61e2e-109">Formato, skirto SF apdoroti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="61e2e-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="61e2e-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="61e2e-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="61e2e-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="61e2e-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="61e2e-112">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="61e2e-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="61e2e-113">Medyje pasirinkite dalį Customer invoice model\Customer invoice model (custom).</span><span class="sxs-lookup"><span data-stu-id="61e2e-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="61e2e-114">Sukursite formatą, kurį naudojant būtų generuojami el. laiškai su informacija apie visus failus, pridėtus prie pardavimo užsakymo, susijusio su elektroniniu būdu apdorojama SF.</span><span class="sxs-lookup"><span data-stu-id="61e2e-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="61e2e-115">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="61e2e-116">Lauke Naujas įveskite Formatas pagal duomenų modelį Kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="61e2e-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="61e2e-117">Lauke Pavadinimas įveskite Elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="61e2e-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="61e2e-118">Elektroninės SF pranešimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="61e2e-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="61e2e-119">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="61e2e-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="61e2e-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="61e2e-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="61e2e-121">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="61e2e-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="61e2e-122">Kurkite formatą, skirtą priedams į generuojamus pranešimą įvesti MIME formatu</span><span class="sxs-lookup"><span data-stu-id="61e2e-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="61e2e-123">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="61e2e-123">Click Designer.</span></span>
2. <span data-ttu-id="61e2e-124">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="61e2e-125">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="61e2e-126">Lauke Pavadinimas įveskite SF.</span><span class="sxs-lookup"><span data-stu-id="61e2e-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="61e2e-127">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="61e2e-127">Invoice</span></span>  
5. <span data-ttu-id="61e2e-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-128">Click OK.</span></span>
6. <span data-ttu-id="61e2e-129">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="61e2e-130">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="61e2e-131">Lauke Pavadinimas įveskite SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="61e2e-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="61e2e-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="61e2e-132">SalesOrder</span></span>  
9. <span data-ttu-id="61e2e-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-133">Click OK.</span></span>
10. <span data-ttu-id="61e2e-134">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="61e2e-135">Lauke Pavadinimas įveskite InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="61e2e-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="61e2e-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="61e2e-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="61e2e-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-137">Click OK.</span></span>
13. <span data-ttu-id="61e2e-138">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="61e2e-139">Lauke Pavadinimas įveskite InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="61e2e-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="61e2e-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="61e2e-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="61e2e-141">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-141">Click OK.</span></span>
16. <span data-ttu-id="61e2e-142">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="61e2e-143">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="61e2e-144">Lauke Pavadinimas įveskite EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="61e2e-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="61e2e-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="61e2e-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="61e2e-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-146">Click OK.</span></span>
20. <span data-ttu-id="61e2e-147">Medyje pasirinkite Invoice\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="61e2e-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="61e2e-148">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-148">Click Add Element.</span></span>
22. <span data-ttu-id="61e2e-149">Lauke Pavadinimas įveskite Dokumentas.</span><span class="sxs-lookup"><span data-stu-id="61e2e-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="61e2e-150">Dokumentas</span><span class="sxs-lookup"><span data-stu-id="61e2e-150">Document</span></span>  
23. <span data-ttu-id="61e2e-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-151">Click OK.</span></span>
24. <span data-ttu-id="61e2e-152">Medyje pasirinkite Invoice\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="61e2e-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="61e2e-153">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="61e2e-154">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="61e2e-155">Lauke Pavadinimas įveskite FileName.</span><span class="sxs-lookup"><span data-stu-id="61e2e-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="61e2e-156">FileName</span><span class="sxs-lookup"><span data-stu-id="61e2e-156">FileName</span></span>  
28. <span data-ttu-id="61e2e-157">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-157">Click OK.</span></span>
29. <span data-ttu-id="61e2e-158">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="61e2e-159">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="61e2e-160">Lauke Pavadinimas įveskite FileContent.</span><span class="sxs-lookup"><span data-stu-id="61e2e-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="61e2e-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="61e2e-161">FileContent</span></span>  
32. <span data-ttu-id="61e2e-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-162">Click OK.</span></span>
33. <span data-ttu-id="61e2e-163">Medyje pasirinkite Invoice\EnclosedDocs\Document\FileContent.</span><span class="sxs-lookup"><span data-stu-id="61e2e-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="61e2e-164">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="61e2e-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="61e2e-165">Medyje pasirinkite Text\Base64.</span><span class="sxs-lookup"><span data-stu-id="61e2e-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="61e2e-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="61e2e-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="61e2e-167">Susiekite formato elementus su duomenų modeliu kaip duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="61e2e-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="61e2e-168">Medyje pasirinkite Invoice\SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="61e2e-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="61e2e-169">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="61e2e-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="61e2e-170">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="61e2e-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="61e2e-171">Medyje pasirinkite model\Sales order number(SalesId).</span><span class="sxs-lookup"><span data-stu-id="61e2e-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="61e2e-172">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-172">Click Bind.</span></span>
6. <span data-ttu-id="61e2e-173">Medyje pasirinkite Invoice\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="61e2e-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="61e2e-174">Medyje išplėskite model\Base invoice(InvoiceBase).</span><span class="sxs-lookup"><span data-stu-id="61e2e-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="61e2e-175">Medyje pasirinkite model\Base invoice(InvoiceBase)\Invoice number(Id).</span><span class="sxs-lookup"><span data-stu-id="61e2e-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="61e2e-176">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-176">Click Bind.</span></span>
10. <span data-ttu-id="61e2e-177">Medyje pasirinkite Invoice\InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="61e2e-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="61e2e-178">Medyje pasirinkite model\Base invoice(InvoiceBase)\Invoice amount(Amount).</span><span class="sxs-lookup"><span data-stu-id="61e2e-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="61e2e-179">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-179">Click Bind.</span></span>
13. <span data-ttu-id="61e2e-180">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="61e2e-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="61e2e-181">Medyje pasirinkite model\Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="61e2e-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="61e2e-182">Medyje pasirinkite Invoice\EnclosedDocs\Document\FileContent\Base64.</span><span class="sxs-lookup"><span data-stu-id="61e2e-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="61e2e-183">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-183">Click Bind.</span></span>
17. <span data-ttu-id="61e2e-184">Medyje pasirinkite model\Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="61e2e-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="61e2e-185">Medyje pasirinkite Invoice\EnclosedDocs\Document\FileName.</span><span class="sxs-lookup"><span data-stu-id="61e2e-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="61e2e-186">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-186">Click Bind.</span></span>
20. <span data-ttu-id="61e2e-187">Medyje pasirinkite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="61e2e-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="61e2e-188">Medyje pasirinkite Invoice\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="61e2e-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="61e2e-189">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-189">Click Bind.</span></span>
23. <span data-ttu-id="61e2e-190">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="61e2e-190">Click Save.</span></span>
24. <span data-ttu-id="61e2e-191">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="61e2e-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]