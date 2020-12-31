---
title: ER dokumentų valdymo failų naudojimas formato išvestyse (3 dalis – formato kūrimas)
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų formatą, norėdamas dokumentų valdymo failus naudoti ER išvestyje.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681858"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="c4d35-103">ER dokumentų valdymo failų naudojimas formato išvestyse (3 dalis – formato kūrimas)</span><span class="sxs-lookup"><span data-stu-id="c4d35-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4d35-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="c4d35-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c4d35-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="c4d35-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c4d35-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis. Duomenų modelio išplėtimas)“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="c4d35-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="c4d35-108">Formato, skirto SF apdoroti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="c4d35-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="c4d35-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c4d35-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c4d35-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c4d35-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c4d35-111">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="c4d35-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="c4d35-112">Medyje pasirinkite dalį Customer invoice model\Customer invoice model (custom).</span><span class="sxs-lookup"><span data-stu-id="c4d35-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="c4d35-113">Sukursite formatą, kurį naudojant būtų generuojami el. laiškai su informacija apie visus failus, pridėtus prie pardavimo užsakymo, susijusio su elektroniniu būdu apdorojama SF.</span><span class="sxs-lookup"><span data-stu-id="c4d35-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="c4d35-114">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="c4d35-115">Lauke Naujas įveskite Formatas pagal duomenų modelį Kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="c4d35-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="c4d35-116">Lauke Pavadinimas įveskite Elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c4d35-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="c4d35-117">Elektroninės SF pranešimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c4d35-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="c4d35-118">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4d35-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="c4d35-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="c4d35-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="c4d35-120">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c4d35-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="c4d35-121">Kurkite formatą, skirtą priedams į generuojamus pranešimą įvesti MIME formatu</span><span class="sxs-lookup"><span data-stu-id="c4d35-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="c4d35-122">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="c4d35-122">Click Designer.</span></span>
2. <span data-ttu-id="c4d35-123">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c4d35-124">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="c4d35-125">Lauke Pavadinimas įveskite SF.</span><span class="sxs-lookup"><span data-stu-id="c4d35-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="c4d35-126">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="c4d35-126">Invoice</span></span>  
5. <span data-ttu-id="c4d35-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-127">Click OK.</span></span>
6. <span data-ttu-id="c4d35-128">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="c4d35-129">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="c4d35-130">Lauke Pavadinimas įveskite SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="c4d35-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="c4d35-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="c4d35-131">SalesOrder</span></span>  
9. <span data-ttu-id="c4d35-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-132">Click OK.</span></span>
10. <span data-ttu-id="c4d35-133">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="c4d35-134">Lauke Pavadinimas įveskite InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="c4d35-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="c4d35-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="c4d35-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="c4d35-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-136">Click OK.</span></span>
13. <span data-ttu-id="c4d35-137">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="c4d35-138">Lauke Pavadinimas įveskite InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="c4d35-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="c4d35-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="c4d35-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="c4d35-140">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-140">Click OK.</span></span>
16. <span data-ttu-id="c4d35-141">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c4d35-142">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="c4d35-143">Lauke Pavadinimas įveskite EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="c4d35-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="c4d35-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="c4d35-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="c4d35-145">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-145">Click OK.</span></span>
20. <span data-ttu-id="c4d35-146">Medyje pasirinkite Invoice\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="c4d35-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="c4d35-147">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-147">Click Add Element.</span></span>
22. <span data-ttu-id="c4d35-148">Lauke Pavadinimas įveskite Dokumentas.</span><span class="sxs-lookup"><span data-stu-id="c4d35-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="c4d35-149">Dokumentas</span><span class="sxs-lookup"><span data-stu-id="c4d35-149">Document</span></span>  
23. <span data-ttu-id="c4d35-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-150">Click OK.</span></span>
24. <span data-ttu-id="c4d35-151">Medyje pasirinkite Invoice\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="c4d35-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="c4d35-152">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="c4d35-153">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="c4d35-154">Lauke Pavadinimas įveskite FileName.</span><span class="sxs-lookup"><span data-stu-id="c4d35-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="c4d35-155">FileName</span><span class="sxs-lookup"><span data-stu-id="c4d35-155">FileName</span></span>  
28. <span data-ttu-id="c4d35-156">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-156">Click OK.</span></span>
29. <span data-ttu-id="c4d35-157">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="c4d35-158">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="c4d35-159">Lauke Pavadinimas įveskite FileContent.</span><span class="sxs-lookup"><span data-stu-id="c4d35-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="c4d35-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="c4d35-160">FileContent</span></span>  
32. <span data-ttu-id="c4d35-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-161">Click OK.</span></span>
33. <span data-ttu-id="c4d35-162">Medyje pasirinkite Invoice\EnclosedDocs\Document\FileContent.</span><span class="sxs-lookup"><span data-stu-id="c4d35-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="c4d35-163">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c4d35-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="c4d35-164">Medyje pasirinkite Text\Base64.</span><span class="sxs-lookup"><span data-stu-id="c4d35-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="c4d35-165">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c4d35-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="c4d35-166">Susiekite formato elementus su duomenų modeliu kaip duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="c4d35-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="c4d35-167">Medyje pasirinkite Invoice\SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="c4d35-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="c4d35-168">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="c4d35-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="c4d35-169">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="c4d35-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="c4d35-170">Medyje pasirinkite model\Sales order number(SalesId).</span><span class="sxs-lookup"><span data-stu-id="c4d35-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="c4d35-171">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-171">Click Bind.</span></span>
6. <span data-ttu-id="c4d35-172">Medyje pasirinkite Invoice\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="c4d35-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="c4d35-173">Medyje išplėskite model\Base invoice(InvoiceBase).</span><span class="sxs-lookup"><span data-stu-id="c4d35-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="c4d35-174">Medyje pasirinkite model\Base invoice(InvoiceBase)\Invoice number(Id).</span><span class="sxs-lookup"><span data-stu-id="c4d35-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="c4d35-175">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-175">Click Bind.</span></span>
10. <span data-ttu-id="c4d35-176">Medyje pasirinkite Invoice\InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="c4d35-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="c4d35-177">Medyje pasirinkite model\Base invoice(InvoiceBase)\Invoice amount(Amount).</span><span class="sxs-lookup"><span data-stu-id="c4d35-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="c4d35-178">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-178">Click Bind.</span></span>
13. <span data-ttu-id="c4d35-179">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="c4d35-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="c4d35-180">Medyje pasirinkite model\Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="c4d35-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="c4d35-181">Medyje pasirinkite Invoice\EnclosedDocs\Document\FileContent\Base64.</span><span class="sxs-lookup"><span data-stu-id="c4d35-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="c4d35-182">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-182">Click Bind.</span></span>
17. <span data-ttu-id="c4d35-183">Medyje pasirinkite model\Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="c4d35-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="c4d35-184">Medyje pasirinkite Invoice\EnclosedDocs\Document\FileName.</span><span class="sxs-lookup"><span data-stu-id="c4d35-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="c4d35-185">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-185">Click Bind.</span></span>
20. <span data-ttu-id="c4d35-186">Medyje pasirinkite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="c4d35-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="c4d35-187">Medyje pasirinkite Invoice\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="c4d35-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="c4d35-188">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-188">Click Bind.</span></span>
23. <span data-ttu-id="c4d35-189">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c4d35-189">Click Save.</span></span>
24. <span data-ttu-id="c4d35-190">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c4d35-190">Close the page.</span></span>

