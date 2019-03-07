---
title: 'ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)'
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją.
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
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
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 29e19b6d91e5761178627ef2051f3385f5d7cfe5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2019
ms.locfileid: "377554"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="576f3-103">ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="576f3-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="576f3-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="576f3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="576f3-105">Ši formato konfigūracija apibrėš mokėjimų apdorojimui naudojamų elektroninių dokumentų formatą.</span><span class="sxs-lookup"><span data-stu-id="576f3-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="576f3-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ formato konfigūraciją. Norėdami užbaigti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Susieti modelį su duomenų šaltiniais“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="576f3-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="576f3-107">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="576f3-107">Create a new format configuration</span></span>
1. <span data-ttu-id="576f3-108">Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="576f3-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="576f3-109">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="576f3-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="576f3-110">Medyje pasirinkite **„Mokėjimai (supaprastintas modelis)“**.</span><span class="sxs-lookup"><span data-stu-id="576f3-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="576f3-111">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="576f3-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="576f3-112">Jei nematote **Kurti konfigūraciją**, turite įgalinti dizaino režimą puslapyje **Elektroninės ataskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="576f3-113">Lauke **Naujas** įveskite **Formatas pagal duomenų modelį PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="576f3-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="576f3-114">Lauke **Pavadinimas**, įveskite **BACS (JK fiktyvus)**.</span><span class="sxs-lookup"><span data-stu-id="576f3-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="576f3-115">Lauke **Aprašas** įveskite **BACS mokėjimo tiekėjui formatas (JK fiktyvus)**.</span><span class="sxs-lookup"><span data-stu-id="576f3-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="576f3-116">Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="576f3-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="576f3-117">Šis teikėjas galės prižiūrėti šią konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="576f3-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="576f3-118">Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.</span><span class="sxs-lookup"><span data-stu-id="576f3-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="576f3-119">Galima apibrėžti konkretų elektroninio dokumento formatą.</span><span class="sxs-lookup"><span data-stu-id="576f3-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="576f3-120">Palikite šį lauką tuščią, jei norite pasirinkti formatą vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="576f3-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="576f3-121">Lauke **Duomenų modelio aprašas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="576f3-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="576f3-122">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="576f3-122">Click **Create configuration**.</span></span> <span data-ttu-id="576f3-123">Sukurta nauja konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="576f3-123">A new configuration has been created.</span></span> <span data-ttu-id="576f3-124">Juodraščio versijoje galima laikyti elektroninių dokumentų valdymui skirtą dizaino formatą.</span><span class="sxs-lookup"><span data-stu-id="576f3-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="576f3-125">Kurti elektroninio dokumento formatą</span><span class="sxs-lookup"><span data-stu-id="576f3-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="576f3-126">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="576f3-126">Click **Designer**.</span></span>
2. <span data-ttu-id="576f3-127">Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="576f3-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="576f3-128">Medyje pasirinkite **Bendra \ Failas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="576f3-129">Lauke **Pavadinimas** įveskite **XML**.</span><span class="sxs-lookup"><span data-stu-id="576f3-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="576f3-130">Lauke **Kodavimas** įveskite **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="576f3-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="576f3-131">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-131">Click **OK**.</span></span>
7. <span data-ttu-id="576f3-132">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="576f3-132">Click **Add**.</span></span>
8. <span data-ttu-id="576f3-133">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="576f3-134">Lauke **Pavadinimas** įveskite **Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="576f3-135">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-135">Click **OK**.</span></span>
11. <span data-ttu-id="576f3-136">Medyje pasirinkite **Xml \ Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="576f3-137">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="576f3-138">Lauke **Pavadinimas** įveskite **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="576f3-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="576f3-139">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-139">Click **OK**.</span></span>
15. <span data-ttu-id="576f3-140">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="576f3-141">Lauke „Pavadinimas“ įveskite **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="576f3-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="576f3-142">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-142">Click **OK**.</span></span>
18. <span data-ttu-id="576f3-143">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="576f3-144">Lauke **Pavadinimas**, įveskite **Mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="576f3-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-145">Click **OK**.</span></span>
21. <span data-ttu-id="576f3-146">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="576f3-147">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="576f3-148">Lauke **Pavadinimas** įveskite **Prekė**.</span><span class="sxs-lookup"><span data-stu-id="576f3-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="576f3-149">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-149">Click **OK**.</span></span>
25. <span data-ttu-id="576f3-150">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="576f3-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="576f3-151">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="576f3-151">Click **Add**.</span></span>
27. <span data-ttu-id="576f3-152">Medyje pasirinkite **XML \ Atributas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="576f3-153">Lauke „Pavadinimas“ įveskite **Id**.</span><span class="sxs-lookup"><span data-stu-id="576f3-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="576f3-154">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-154">Click **OK**.</span></span>
30. <span data-ttu-id="576f3-155">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="576f3-155">Click **Add**.</span></span>
31. <span data-ttu-id="576f3-156">Medyje pasirinkite **XML \ Elementas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="576f3-157">Lauke „Pavadinimas“ įveskite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="576f3-158">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-158">Click **OK**.</span></span>
34. <span data-ttu-id="576f3-159">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="576f3-160">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="576f3-161">Lauke „Pavadinimas“ įveskite **Agentas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="576f3-162">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-162">Click **OK**.</span></span>
38. <span data-ttu-id="576f3-163">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="576f3-164">Lauke **Pavadinimas** įveskite **Bankas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="576f3-165">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-165">Click **OK**.</span></span>
41. <span data-ttu-id="576f3-166">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="576f3-167">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="576f3-168">Lauke **Pavadinimas** įveskite **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="576f3-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="576f3-169">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-169">Click **OK**.</span></span>
45. <span data-ttu-id="576f3-170">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="576f3-171">Lauke **Pavadinimas** įveskite **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="576f3-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="576f3-172">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-172">Click **OK**.</span></span>
48. <span data-ttu-id="576f3-173">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="576f3-174">Spustelėkite **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="576f3-174">Click **Copy**.</span></span>
50. <span data-ttu-id="576f3-175">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="576f3-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="576f3-176">Spustelėkite **Įklijuoti**.</span><span class="sxs-lookup"><span data-stu-id="576f3-176">Click **Paste**.</span></span>
52. <span data-ttu-id="576f3-177">Lauke **Pavadinimas** įveskite **Mokėtojas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="576f3-178">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.</span><span class="sxs-lookup"><span data-stu-id="576f3-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="576f3-179">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="576f3-180">Lauke **Pavadinimas** įveskite **Valiuta**.</span><span class="sxs-lookup"><span data-stu-id="576f3-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="576f3-181">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-181">Click **OK**.</span></span>
57. <span data-ttu-id="576f3-182">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="576f3-183">Lauke **Pavadinimas**, įveskite **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="576f3-184">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-184">Click **OK**.</span></span>
60. <span data-ttu-id="576f3-185">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="576f3-186">Lauke Pavadinimas įveskite **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="576f3-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="576f3-187">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-187">Click **OK**.</span></span>
63. <span data-ttu-id="576f3-188">Spustelėkite **Įtraukti elementą**.</span><span class="sxs-lookup"><span data-stu-id="576f3-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="576f3-189">Lauke Pavadinimas įveskite **Suma**.</span><span class="sxs-lookup"><span data-stu-id="576f3-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="576f3-190">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="576f3-191">Parengti formato komponentus susiejimui su duomenų modelio elementais</span><span class="sxs-lookup"><span data-stu-id="576f3-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="576f3-192">Medyje pasirinkite **Xml \ Pranešimas \ ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="576f3-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="576f3-193">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="576f3-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="576f3-194">Medyje pasirinkite **Tekstas \ DateTime**.</span><span class="sxs-lookup"><span data-stu-id="576f3-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="576f3-195">Lauke **Formatas** įveskite **mmmm-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="576f3-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="576f3-196">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-196">Click **OK**.</span></span>
6. <span data-ttu-id="576f3-197">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate**.</span><span class="sxs-lookup"><span data-stu-id="576f3-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="576f3-198">Spustelėkite **Įtraukti DateTime**.</span><span class="sxs-lookup"><span data-stu-id="576f3-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="576f3-199">Lauke **Formatas** įveskite **mmmm-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="576f3-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="576f3-200">Lauke **DateTime tipas** pasirinkite **Data**.</span><span class="sxs-lookup"><span data-stu-id="576f3-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="576f3-201">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-201">Click **OK**.</span></span>
11. <span data-ttu-id="576f3-202">Medyje pasirinkite **Xml \ Pranešimas \ MessageId**.</span><span class="sxs-lookup"><span data-stu-id="576f3-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="576f3-203">Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="576f3-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="576f3-204">Medyje pasirinkite **Tekstas \ Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="576f3-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="576f3-205">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-205">Click **OK**.</span></span>
15. <span data-ttu-id="576f3-206">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="576f3-207">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-207">Click **Add String**.</span></span>
17. <span data-ttu-id="576f3-208">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-208">Click **OK**.</span></span>
18. <span data-ttu-id="576f3-209">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="576f3-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="576f3-210">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-210">Click **Add String**.</span></span>
20. <span data-ttu-id="576f3-211">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-211">Click **OK**.</span></span>
21. <span data-ttu-id="576f3-212">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="576f3-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="576f3-213">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-213">Click **Add String**.</span></span>
23. <span data-ttu-id="576f3-214">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-214">Click **OK**.</span></span>
24. <span data-ttu-id="576f3-215">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="576f3-216">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-216">Click **Add String**.</span></span>
26. <span data-ttu-id="576f3-217">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-217">Click **OK**.</span></span>
27. <span data-ttu-id="576f3-218">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="576f3-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="576f3-219">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-219">Click **Add String**.</span></span>
29. <span data-ttu-id="576f3-220">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-220">Click **OK**.</span></span>
30. <span data-ttu-id="576f3-221">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="576f3-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="576f3-222">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-222">Click **Add String**.</span></span>
32. <span data-ttu-id="576f3-223">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-223">Click **OK**.</span></span>
33. <span data-ttu-id="576f3-224">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta**.</span><span class="sxs-lookup"><span data-stu-id="576f3-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="576f3-225">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-225">Click **Add String**.</span></span>
35. <span data-ttu-id="576f3-226">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-226">Click **OK**.</span></span>
36. <span data-ttu-id="576f3-227">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="576f3-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="576f3-228">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-228">Click **Add String**.</span></span>
38. <span data-ttu-id="576f3-229">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-229">Click **OK**.</span></span>
39. <span data-ttu-id="576f3-230">Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma**.</span><span class="sxs-lookup"><span data-stu-id="576f3-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="576f3-231">Spustelėkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="576f3-231">Click **Add String**.</span></span>
41. <span data-ttu-id="576f3-232">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="576f3-232">Click **OK**.</span></span>
42. <span data-ttu-id="576f3-233">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="576f3-233">Click **Save**.</span></span>
43. <span data-ttu-id="576f3-234">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="576f3-234">Close the page.</span></span>

