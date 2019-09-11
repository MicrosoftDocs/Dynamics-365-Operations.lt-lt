---
title: 'ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)'
description: Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali kurti formato konfigūraciją elektroninėms ataskaitoms (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fd41b1724eb2e0405c0e7a7e0ff0aea4a945e0
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866807"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="25b6b-103">ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="25b6b-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25b6b-104">Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali kurti formato konfigūraciją elektroninėms ataskaitoms (ER).</span><span class="sxs-lookup"><span data-stu-id="25b6b-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="25b6b-105">Ši formato konfigūracija apibrėš mokėjimų apdorojimui naudojamų elektroninių dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="25b6b-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ formato konfigūraciją. Norėdami užbaigti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Susieti modelį su duomenų šaltiniais“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="25b6b-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="25b6b-107">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="25b6b-107">Create a new format configuration</span></span>
1. <span data-ttu-id="25b6b-108">Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="25b6b-109">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="25b6b-110">Medyje pasirinkite **„Mokėjimai (supaprastintas modelis)“**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="25b6b-111">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="25b6b-112">Jei nematote **Kurti konfigūraciją**, turite įgalinti dizaino režimą puslapyje **Elektroninės ataskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="25b6b-113">Lauke **Naujas** įveskite **Formatas pagal duomenų modelį PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="25b6b-114">Lauke **Pavadinimas**, įveskite **BACS (JK fiktyvus)**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="25b6b-115">Lauke **Aprašas** įveskite **BACS mokėjimo tiekėjui formatas (JK fiktyvus)**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="25b6b-116">Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="25b6b-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="25b6b-117">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="25b6b-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="25b6b-118">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="25b6b-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="25b6b-119">Galima apibrėžti konkretų elektroninio dokumento formatą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="25b6b-120">Palikite šį lauką tuščią, jei norite pasirinkti formatą vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="25b6b-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="25b6b-121">Lauke **Duomenų modelio aprašas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25b6b-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="25b6b-122">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-122">Click **Create configuration**.</span></span> <span data-ttu-id="25b6b-123">Sukurta nauja konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="25b6b-123">A new configuration has been created.</span></span> <span data-ttu-id="25b6b-124">Juodraščio versijoje galima laikyti elektroninių dokumentų valdymui skirtą dizaino formatą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="25b6b-125">Kurti elektroninio dokumento formatą</span><span class="sxs-lookup"><span data-stu-id="25b6b-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="25b6b-126">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-126">Click **Designer**.</span></span>
2. <span data-ttu-id="25b6b-127">Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="25b6b-128">Medyje pasirinkite **Bendra \ Failas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="25b6b-129">Lauke **Pavadinimas** įveskite **XML**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="25b6b-130">Lauke **Kodavimas** įveskite **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="25b6b-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-131">Click **OK**.</span></span>
7. <span data-ttu-id="25b6b-132">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-132">Click **Add**.</span></span>
8. <span data-ttu-id="25b6b-133">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="25b6b-134">Lauke **Pavadinimas** įveskite **Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="25b6b-135">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-135">Click **OK**.</span></span>
11. <span data-ttu-id="25b6b-136">Medyje pasirinkite **Xml \ Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="25b6b-137">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="25b6b-138">Lauke **Pavadinimas** įveskite **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="25b6b-139">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-139">Click **OK**.</span></span>
15. <span data-ttu-id="25b6b-140">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="25b6b-141">Lauke „Pavadinimas“ įveskite **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="25b6b-142">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-142">Click **OK**.</span></span>
18. <span data-ttu-id="25b6b-143">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="25b6b-144">Lauke **Pavadinimas**, įveskite **Mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="25b6b-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-145">Click **OK**.</span></span>
21. <span data-ttu-id="25b6b-146">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="25b6b-147">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="25b6b-148">Lauke **Pavadinimas** įveskite **Prekė**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="25b6b-149">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-149">Click **OK**.</span></span>
25. <span data-ttu-id="25b6b-150">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="25b6b-151">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-151">Click **Add**.</span></span>
27. <span data-ttu-id="25b6b-152">Medyje pasirinkite **XML \ Atributas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="25b6b-153">Lauke „Pavadinimas“ įveskite **Id**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="25b6b-154">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-154">Click **OK**.</span></span>
30. <span data-ttu-id="25b6b-155">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-155">Click **Add**.</span></span>
31. <span data-ttu-id="25b6b-156">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="25b6b-157">Lauke „Pavadinimas“ įveskite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="25b6b-158">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-158">Click **OK**.</span></span>
34. <span data-ttu-id="25b6b-159">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="25b6b-160">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="25b6b-161">Lauke „Pavadinimas“ įveskite **Agentas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="25b6b-162">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-162">Click **OK**.</span></span>
38. <span data-ttu-id="25b6b-163">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="25b6b-164">Lauke **Pavadinimas** įveskite **Bankas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="25b6b-165">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-165">Click **OK**.</span></span>
41. <span data-ttu-id="25b6b-166">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="25b6b-167">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="25b6b-168">Lauke **Pavadinimas** įveskite **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="25b6b-169">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-169">Click **OK**.</span></span>
45. <span data-ttu-id="25b6b-170">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="25b6b-171">Lauke **Pavadinimas** įveskite **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="25b6b-172">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-172">Click **OK**.</span></span>
48. <span data-ttu-id="25b6b-173">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="25b6b-174">Spustelėkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-174">Click **Copy**.</span></span>
50. <span data-ttu-id="25b6b-175">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="25b6b-176">Spustelėkite **Įklijuoti**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-176">Click **Paste**.</span></span>
52. <span data-ttu-id="25b6b-177">Lauke **Pavadinimas** įveskite **Mokėtojas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="25b6b-178">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="25b6b-179">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="25b6b-180">Lauke **Pavadinimas** įveskite **Valiuta**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="25b6b-181">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-181">Click **OK**.</span></span>
57. <span data-ttu-id="25b6b-182">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="25b6b-183">Lauke **Pavadinimas**, įveskite **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="25b6b-184">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-184">Click **OK**.</span></span>
60. <span data-ttu-id="25b6b-185">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="25b6b-186">Lauke Pavadinimas įveskite **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="25b6b-187">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-187">Click **OK**.</span></span>
63. <span data-ttu-id="25b6b-188">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="25b6b-189">Lauke Pavadinimas įveskite **Suma**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="25b6b-190">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="25b6b-191">Parengti formato komponentus susiejimui su duomenų modelio elementais</span><span class="sxs-lookup"><span data-stu-id="25b6b-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="25b6b-192">Medyje pasirinkite **Xml \ Pranešimas \ ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="25b6b-193">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="25b6b-194">Medyje pasirinkite **Tekstas \ DateTime**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="25b6b-195">Lauke **Formatas** įveskite **mmmm-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="25b6b-196">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-196">Click **OK**.</span></span>
6. <span data-ttu-id="25b6b-197">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="25b6b-198">Spustelėkite **Įtraukti DateTime**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="25b6b-199">Lauke **Formatas** įveskite **mmmm-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="25b6b-200">Lauke **DateTime tipas** pasirinkite **Data**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="25b6b-201">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-201">Click **OK**.</span></span>
11. <span data-ttu-id="25b6b-202">Medyje pasirinkite **Xml \ Pranešimas \ MessageId**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="25b6b-203">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="25b6b-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="25b6b-204">Medyje pasirinkite **Tekstas \ Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="25b6b-205">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-205">Click **OK**.</span></span>
15. <span data-ttu-id="25b6b-206">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="25b6b-207">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-207">Click **Add String**.</span></span>
17. <span data-ttu-id="25b6b-208">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-208">Click **OK**.</span></span>
18. <span data-ttu-id="25b6b-209">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="25b6b-210">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-210">Click **Add String**.</span></span>
20. <span data-ttu-id="25b6b-211">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-211">Click **OK**.</span></span>
21. <span data-ttu-id="25b6b-212">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="25b6b-213">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-213">Click **Add String**.</span></span>
23. <span data-ttu-id="25b6b-214">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-214">Click **OK**.</span></span>
24. <span data-ttu-id="25b6b-215">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="25b6b-216">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-216">Click **Add String**.</span></span>
26. <span data-ttu-id="25b6b-217">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-217">Click **OK**.</span></span>
27. <span data-ttu-id="25b6b-218">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="25b6b-219">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-219">Click **Add String**.</span></span>
29. <span data-ttu-id="25b6b-220">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-220">Click **OK**.</span></span>
30. <span data-ttu-id="25b6b-221">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="25b6b-222">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-222">Click **Add String**.</span></span>
32. <span data-ttu-id="25b6b-223">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-223">Click **OK**.</span></span>
33. <span data-ttu-id="25b6b-224">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="25b6b-225">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-225">Click **Add String**.</span></span>
35. <span data-ttu-id="25b6b-226">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-226">Click **OK**.</span></span>
36. <span data-ttu-id="25b6b-227">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="25b6b-228">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-228">Click **Add String**.</span></span>
38. <span data-ttu-id="25b6b-229">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-229">Click **OK**.</span></span>
39. <span data-ttu-id="25b6b-230">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="25b6b-231">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-231">Click **Add String**.</span></span>
41. <span data-ttu-id="25b6b-232">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-232">Click **OK**.</span></span>
42. <span data-ttu-id="25b6b-233">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="25b6b-233">Click **Save**.</span></span>
43. <span data-ttu-id="25b6b-234">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25b6b-234">Close the page.</span></span>

