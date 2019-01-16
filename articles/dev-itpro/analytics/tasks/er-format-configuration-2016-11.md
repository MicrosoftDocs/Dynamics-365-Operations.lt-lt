--- 
title: "ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: lt-lt
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="6cfbe-103">ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="6cfbe-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cfbe-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="6cfbe-105">Ši formato konfigūracija apibrėš mokėjimų apdorojimui naudojamų elektroninių dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="6cfbe-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ formato konfigūraciją. Norėdami užbaigti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Susieti modelį su duomenų šaltiniais“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="6cfbe-107">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="6cfbe-107">Create a new format configuration</span></span>
1. <span data-ttu-id="6cfbe-108">Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="6cfbe-109">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="6cfbe-110">Medyje pasirinkite **„Mokėjimai (supaprastintas modelis)“**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="6cfbe-111">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="6cfbe-112">Jei nematote **Kurti konfigūraciją**, turite įgalinti dizaino režimą puslapyje **Elektroninės ataskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="6cfbe-113">Lauke **Naujas** įveskite **Formatas pagal duomenų modelį PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="6cfbe-114">Lauke **Pavadinimas**, įveskite **BACS (JK fiktyvus)**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="6cfbe-115">Lauke **Aprašas** įveskite **BACS mokėjimo tiekėjui formatas (JK fiktyvus)**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="6cfbe-116">Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="6cfbe-117">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="6cfbe-118">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="6cfbe-119">Galima apibrėžti konkretų elektroninio dokumento formatą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="6cfbe-120">Palikite šį lauką tuščią, jei norite pasirinkti formatą vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="6cfbe-121">Lauke **Duomenų modelio aprašas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="6cfbe-122">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-122">Click **Create configuration**.</span></span> <span data-ttu-id="6cfbe-123">Sukurta nauja konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-123">A new configuration has been created.</span></span> <span data-ttu-id="6cfbe-124">Juodraščio versijoje galima laikyti elektroninių dokumentų valdymui skirtą dizaino formatą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="6cfbe-125">Jei nematote **Kurti konfigūraciją**, turite įgalinti dizaino režimą puslapyje **Elektroninės ataskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="6cfbe-126">Kurti elektroninio dokumento formatą</span><span class="sxs-lookup"><span data-stu-id="6cfbe-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="6cfbe-127">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-127">Click **Designer**.</span></span>
2. <span data-ttu-id="6cfbe-128">Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="6cfbe-129">Medyje pasirinkite **Bendra \ Failas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="6cfbe-130">Lauke **Pavadinimas** įveskite **XML**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="6cfbe-131">Lauke **Kodavimas** įveskite **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="6cfbe-132">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-132">Click **OK**.</span></span>
7. <span data-ttu-id="6cfbe-133">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-133">Click **Add**.</span></span>
8. <span data-ttu-id="6cfbe-134">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="6cfbe-135">Lauke **Pavadinimas** įveskite **Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="6cfbe-136">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-136">Click **OK**.</span></span>
11. <span data-ttu-id="6cfbe-137">Medyje pasirinkite **Xml \ Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="6cfbe-138">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="6cfbe-139">Lauke **Pavadinimas** įveskite **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="6cfbe-140">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-140">Click **OK**.</span></span>
15. <span data-ttu-id="6cfbe-141">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="6cfbe-142">Lauke „Pavadinimas“ įveskite **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="6cfbe-143">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-143">Click **OK**.</span></span>
18. <span data-ttu-id="6cfbe-144">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="6cfbe-145">Lauke **Pavadinimas**, įveskite **Mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="6cfbe-146">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-146">Click **OK**.</span></span>
21. <span data-ttu-id="6cfbe-147">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="6cfbe-148">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="6cfbe-149">Lauke **Pavadinimas** įveskite **Prekė**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="6cfbe-150">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-150">Click **OK**.</span></span>
25. <span data-ttu-id="6cfbe-151">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="6cfbe-152">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-152">Click **Add**.</span></span>
27. <span data-ttu-id="6cfbe-153">Medyje pasirinkite **XML \ Atributas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="6cfbe-154">Lauke „Pavadinimas“ įveskite **Id**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="6cfbe-155">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-155">Click **OK**.</span></span>
30. <span data-ttu-id="6cfbe-156">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-156">Click **Add**.</span></span>
31. <span data-ttu-id="6cfbe-157">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="6cfbe-158">Lauke „Pavadinimas“ įveskite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="6cfbe-159">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-159">Click **OK**.</span></span>
34. <span data-ttu-id="6cfbe-160">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="6cfbe-161">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="6cfbe-162">Lauke „Pavadinimas“ įveskite **Agentas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="6cfbe-163">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-163">Click **OK**.</span></span>
38. <span data-ttu-id="6cfbe-164">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="6cfbe-165">Lauke **Pavadinimas** įveskite **Bankas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="6cfbe-166">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-166">Click **OK**.</span></span>
41. <span data-ttu-id="6cfbe-167">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="6cfbe-168">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="6cfbe-169">Lauke **Pavadinimas** įveskite **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="6cfbe-170">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-170">Click **OK**.</span></span>
45. <span data-ttu-id="6cfbe-171">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="6cfbe-172">Lauke **Pavadinimas** įveskite **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="6cfbe-173">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-173">Click **OK**.</span></span>
48. <span data-ttu-id="6cfbe-174">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="6cfbe-175">Spustelėkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-175">Click **Copy**.</span></span>
50. <span data-ttu-id="6cfbe-176">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="6cfbe-177">Spustelėkite **Įklijuoti**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-177">Click **Paste**.</span></span>
52. <span data-ttu-id="6cfbe-178">Lauke **Pavadinimas** įveskite **Mokėtojas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="6cfbe-179">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="6cfbe-180">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="6cfbe-181">Lauke **Pavadinimas** įveskite **Valiuta**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="6cfbe-182">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-182">Click **OK**.</span></span>
57. <span data-ttu-id="6cfbe-183">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="6cfbe-184">Lauke **Pavadinimas**, įveskite **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="6cfbe-185">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-185">Click **OK**.</span></span>
60. <span data-ttu-id="6cfbe-186">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="6cfbe-187">Lauke Pavadinimas įveskite **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="6cfbe-188">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-188">Click **OK**.</span></span>
63. <span data-ttu-id="6cfbe-189">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="6cfbe-190">Lauke Pavadinimas įveskite **Suma**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="6cfbe-191">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="6cfbe-192">Parengti formato komponentus susiejimui su duomenų modelio elementais</span><span class="sxs-lookup"><span data-stu-id="6cfbe-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="6cfbe-193">Medyje pasirinkite **Xml \ Pranešimas \ ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="6cfbe-194">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="6cfbe-195">Medyje pasirinkite **Tekstas \ DateTime**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="6cfbe-196">Lauke **Formatas** įveskite **mmmm-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="6cfbe-197">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-197">Click **OK**.</span></span>
6. <span data-ttu-id="6cfbe-198">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="6cfbe-199">Spustelėkite **Įtraukti DateTime**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="6cfbe-200">Lauke **Formatas** įveskite **mmmm-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="6cfbe-201">Lauke **DateTime tipas** pasirinkite **Data**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="6cfbe-202">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-202">Click **OK**.</span></span>
11. <span data-ttu-id="6cfbe-203">Medyje pasirinkite **Xml \ Pranešimas \ MessageId**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="6cfbe-204">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="6cfbe-205">Medyje pasirinkite **Tekstas \ Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="6cfbe-206">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-206">Click **OK**.</span></span>
15. <span data-ttu-id="6cfbe-207">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="6cfbe-208">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-208">Click **Add String**.</span></span>
17. <span data-ttu-id="6cfbe-209">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-209">Click **OK**.</span></span>
18. <span data-ttu-id="6cfbe-210">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="6cfbe-211">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-211">Click **Add String**.</span></span>
20. <span data-ttu-id="6cfbe-212">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-212">Click **OK**.</span></span>
21. <span data-ttu-id="6cfbe-213">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="6cfbe-214">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-214">Click **Add String**.</span></span>
23. <span data-ttu-id="6cfbe-215">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-215">Click **OK**.</span></span>
24. <span data-ttu-id="6cfbe-216">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="6cfbe-217">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-217">Click **Add String**.</span></span>
26. <span data-ttu-id="6cfbe-218">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-218">Click **OK**.</span></span>
27. <span data-ttu-id="6cfbe-219">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="6cfbe-220">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-220">Click **Add String**.</span></span>
29. <span data-ttu-id="6cfbe-221">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-221">Click **OK**.</span></span>
30. <span data-ttu-id="6cfbe-222">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="6cfbe-223">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-223">Click **Add String**.</span></span>
32. <span data-ttu-id="6cfbe-224">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-224">Click **OK**.</span></span>
33. <span data-ttu-id="6cfbe-225">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="6cfbe-226">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-226">Click **Add String**.</span></span>
35. <span data-ttu-id="6cfbe-227">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-227">Click **OK**.</span></span>
36. <span data-ttu-id="6cfbe-228">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="6cfbe-229">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-229">Click **Add String**.</span></span>
38. <span data-ttu-id="6cfbe-230">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-230">Click **OK**.</span></span>
39. <span data-ttu-id="6cfbe-231">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="6cfbe-232">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-232">Click **Add String**.</span></span>
41. <span data-ttu-id="6cfbe-233">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-233">Click **OK**.</span></span>
42. <span data-ttu-id="6cfbe-234">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-234">Click **Save**.</span></span>
43. <span data-ttu-id="6cfbe-235">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-235">Close the page.</span></span>


