--- 
title: "Elektroninių ataskaitų (ER) formato konfigūracijos kūrimas"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="c5ac1-103">Elektroninių ataskaitų (ER) formato konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5ac1-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="c5ac1-105">Ši formato konfigūracija apibrėš mokėjimų apdorojimui naudojamų elektroninių dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="c5ac1-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ formato konfigūraciją. Norėdami užbaigti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Susieti modelį su duomenų šaltiniais“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="c5ac1-107">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="c5ac1-107">Create a new format configuration</span></span>
1. <span data-ttu-id="c5ac1-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c5ac1-109">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c5ac1-110">Medyje pasirinkite „Mokėjimai (supaprastintas modelis)“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="c5ac1-111">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="c5ac1-112">Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="c5ac1-113">Lauke „Pavadinimas“, įveskite „BACS (JK fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="c5ac1-114">BACS (JK fiktyvus)</span><span class="sxs-lookup"><span data-stu-id="c5ac1-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="c5ac1-115">Lauke „Aprašas“ įveskite „BACS mokėjimo tiekėjui formatas (JK fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="c5ac1-116">BACS mokėjimo tiekėjui formatas (JK fiktyvus)</span><span class="sxs-lookup"><span data-stu-id="c5ac1-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="c5ac1-117">Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c5ac1-118">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c5ac1-119">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="c5ac1-120">Galima apibrėžti konkretų elektroninio dokumento formatą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="c5ac1-121">Palikite šį lauką tuščią, jei norite pasirinkti formatą vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="c5ac1-122">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="c5ac1-123">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-123">Click Create configuration.</span></span>
    * <span data-ttu-id="c5ac1-124">Sukurta nauja konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-124">A new configuration has been created.</span></span> <span data-ttu-id="c5ac1-125">Juodraščio versijoje galima laikyti elektroninių dokumentų valdymui skirtą dizaino formatą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="c5ac1-126">Kurti elektroninių dokumentų formatą</span><span class="sxs-lookup"><span data-stu-id="c5ac1-126">Design format of electronic document</span></span>
1. <span data-ttu-id="c5ac1-127">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-127">Click Designer.</span></span>
2. <span data-ttu-id="c5ac1-128">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c5ac1-129">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="c5ac1-130">Lauke „Pavadinimas“ įveskite „XML“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="c5ac1-131">Xml</span><span class="sxs-lookup"><span data-stu-id="c5ac1-131">Xml</span></span>  
5. <span data-ttu-id="c5ac1-132">Lauke „Kodavimas“ įveskite „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c5ac1-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c5ac1-133">UTF-8</span></span>  
6. <span data-ttu-id="c5ac1-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-134">Click OK.</span></span>
7. <span data-ttu-id="c5ac1-135">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="c5ac1-136">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="c5ac1-137">Lauke „Pavadinimas“ įveskite „Pranešimas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="c5ac1-138">Pranešimas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-138">Message</span></span>  
10. <span data-ttu-id="c5ac1-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-139">Click OK.</span></span>
11. <span data-ttu-id="c5ac1-140">Medyje pasirinkite „Xml \ Pranešimas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="c5ac1-141">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-141">Click Add Element.</span></span>
13. <span data-ttu-id="c5ac1-142">Lauke „Pavadinimas“ įveskite „ProcessingDate“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="c5ac1-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="c5ac1-143">ProcessingDate</span></span>  
14. <span data-ttu-id="c5ac1-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-144">Click OK.</span></span>
15. <span data-ttu-id="c5ac1-145">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-145">Click Add Element.</span></span>
16. <span data-ttu-id="c5ac1-146">Lauke „Pavadinimas“ įveskite „MessageId“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="c5ac1-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="c5ac1-147">MessageId</span></span>  
17. <span data-ttu-id="c5ac1-148">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-148">Click OK.</span></span>
18. <span data-ttu-id="c5ac1-149">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-149">Click Add Element.</span></span>
19. <span data-ttu-id="c5ac1-150">Lauke „Pavadinimas“, įveskite „Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="c5ac1-151">Mokėjimai</span><span class="sxs-lookup"><span data-stu-id="c5ac1-151">Payments</span></span>  
20. <span data-ttu-id="c5ac1-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-152">Click OK.</span></span>
21. <span data-ttu-id="c5ac1-153">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="c5ac1-154">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-154">Click Add Element.</span></span>
23. <span data-ttu-id="c5ac1-155">Lauke „Pavadinimas“ įveskite „Prekė“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="c5ac1-156">Produktas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-156">Item</span></span>  
24. <span data-ttu-id="c5ac1-157">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-157">Click OK.</span></span>
25. <span data-ttu-id="c5ac1-158">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="c5ac1-159">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="c5ac1-160">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="c5ac1-161">Lauke „Pavadinimas“ įveskite „Id“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="c5ac1-162">ID</span><span class="sxs-lookup"><span data-stu-id="c5ac1-162">Id</span></span>  
29. <span data-ttu-id="c5ac1-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-163">Click OK.</span></span>
30. <span data-ttu-id="c5ac1-164">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="c5ac1-165">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="c5ac1-166">Lauke „Pavadinimas“ įveskite „Tiekėjas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="c5ac1-167">Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-167">Vendor</span></span>  
33. <span data-ttu-id="c5ac1-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-168">Click OK.</span></span>
34. <span data-ttu-id="c5ac1-169">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="c5ac1-170">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-170">Click Add Element.</span></span>
36. <span data-ttu-id="c5ac1-171">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="c5ac1-172">Vardas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-172">Name</span></span>  
37. <span data-ttu-id="c5ac1-173">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-173">Click OK.</span></span>
38. <span data-ttu-id="c5ac1-174">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-174">Click Add Element.</span></span>
39. <span data-ttu-id="c5ac1-175">Lauke „Pavadinimas“ įveskite „Bankas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="c5ac1-176">Bankas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-176">Bank</span></span>  
40. <span data-ttu-id="c5ac1-177">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-177">Click OK.</span></span>
41. <span data-ttu-id="c5ac1-178">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="c5ac1-179">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-179">Click Add Element.</span></span>
43. <span data-ttu-id="c5ac1-180">Lauke „Pavadinimas“ įveskite „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="c5ac1-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="c5ac1-181">RoutingNumber</span></span>  
44. <span data-ttu-id="c5ac1-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-182">Click OK.</span></span>
45. <span data-ttu-id="c5ac1-183">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-183">Click Add Element.</span></span>
46. <span data-ttu-id="c5ac1-184">Lauke „Pavadinimas“ įveskite „AccountNumber“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="c5ac1-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="c5ac1-185">AccountNumber</span></span>  
47. <span data-ttu-id="c5ac1-186">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-186">Click OK.</span></span>
48. <span data-ttu-id="c5ac1-187">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="c5ac1-188">Spustelėkite Kopijuoti.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-188">Click Copy.</span></span>
50. <span data-ttu-id="c5ac1-189">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="c5ac1-190">Spustelėkite Įklijuoti.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-190">Click Paste.</span></span>
52. <span data-ttu-id="c5ac1-191">Lauke „Pavadinimas“ įveskite „Mokėtojas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="c5ac1-192">Mokėtojas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-192">Payer</span></span>  
53. <span data-ttu-id="c5ac1-193">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="c5ac1-194">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-194">Click Add Element.</span></span>
55. <span data-ttu-id="c5ac1-195">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="c5ac1-196">Valiuta</span><span class="sxs-lookup"><span data-stu-id="c5ac1-196">Currency</span></span>  
56. <span data-ttu-id="c5ac1-197">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-197">Click OK.</span></span>
57. <span data-ttu-id="c5ac1-198">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-198">Click Add Element.</span></span>
58. <span data-ttu-id="c5ac1-199">Lauke „Pavadinimas“, įveskite „Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="c5ac1-200">aprašymas</span><span class="sxs-lookup"><span data-stu-id="c5ac1-200">Description</span></span>  
59. <span data-ttu-id="c5ac1-201">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-201">Click OK.</span></span>
60. <span data-ttu-id="c5ac1-202">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-202">Click Add Element.</span></span>
61. <span data-ttu-id="c5ac1-203">Lauke „Pavadinimas“ įveskite „TransDate“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="c5ac1-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="c5ac1-204">TransDate</span></span>  
62. <span data-ttu-id="c5ac1-205">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-205">Click OK.</span></span>
63. <span data-ttu-id="c5ac1-206">Spustelėkite Įtraukti elementą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-206">Click Add Element.</span></span>
64. <span data-ttu-id="c5ac1-207">Lauke „Pavadinimas“ įveskite „Suma“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="c5ac1-208">Suma</span><span class="sxs-lookup"><span data-stu-id="c5ac1-208">Amount</span></span>  
65. <span data-ttu-id="c5ac1-209">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="c5ac1-210">Parengti formato komponentus susiejimui su duomenų modelio elementais</span><span class="sxs-lookup"><span data-stu-id="c5ac1-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="c5ac1-211">Medyje pasirinkite „Xml \ Pranešimas \ ProcessingDate“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="c5ac1-212">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="c5ac1-213">Medyje pasirinkite „Tekstas \ DateTime“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="c5ac1-214">Lauke „Formatas“ įveskite „mmmm-MM-dd“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c5ac1-215">mmmm-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c5ac1-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="c5ac1-216">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-216">Click OK.</span></span>
6. <span data-ttu-id="c5ac1-217">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="c5ac1-218">Spustelėkite Įtraukti DateTime.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="c5ac1-219">Lauke „Formatas“ įveskite „mmmm-MM-dd“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c5ac1-220">mmmm-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c5ac1-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="c5ac1-221">Lauke „DateTime tipas” pasirinkite „Data”.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="c5ac1-222">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-222">Click OK.</span></span>
11. <span data-ttu-id="c5ac1-223">Medyje pasirinkite „Xml \ Pranešimas \ MessageId“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="c5ac1-224">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="c5ac1-225">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="c5ac1-226">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-226">Click OK.</span></span>
15. <span data-ttu-id="c5ac1-227">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="c5ac1-228">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-228">Click Add String.</span></span>
17. <span data-ttu-id="c5ac1-229">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-229">Click OK.</span></span>
18. <span data-ttu-id="c5ac1-230">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="c5ac1-231">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-231">Click Add String.</span></span>
20. <span data-ttu-id="c5ac1-232">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-232">Click OK.</span></span>
21. <span data-ttu-id="c5ac1-233">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="c5ac1-234">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-234">Click Add String.</span></span>
23. <span data-ttu-id="c5ac1-235">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-235">Click OK.</span></span>
24. <span data-ttu-id="c5ac1-236">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="c5ac1-237">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-237">Click Add String.</span></span>
26. <span data-ttu-id="c5ac1-238">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-238">Click OK.</span></span>
27. <span data-ttu-id="c5ac1-239">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="c5ac1-240">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-240">Click Add String.</span></span>
29. <span data-ttu-id="c5ac1-241">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-241">Click OK.</span></span>
30. <span data-ttu-id="c5ac1-242">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="c5ac1-243">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-243">Click Add String.</span></span>
32. <span data-ttu-id="c5ac1-244">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-244">Click OK.</span></span>
33. <span data-ttu-id="c5ac1-245">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="c5ac1-246">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-246">Click Add String.</span></span>
35. <span data-ttu-id="c5ac1-247">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-247">Click OK.</span></span>
36. <span data-ttu-id="c5ac1-248">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="c5ac1-249">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-249">Click Add String.</span></span>
38. <span data-ttu-id="c5ac1-250">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-250">Click OK.</span></span>
39. <span data-ttu-id="c5ac1-251">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma“.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="c5ac1-252">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-252">Click Add String.</span></span>
41. <span data-ttu-id="c5ac1-253">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-253">Click OK.</span></span>
42. <span data-ttu-id="c5ac1-254">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-254">Click Save.</span></span>
43. <span data-ttu-id="c5ac1-255">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c5ac1-255">Close the page.</span></span>

