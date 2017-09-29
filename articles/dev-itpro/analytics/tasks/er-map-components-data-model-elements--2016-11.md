--- 
title: "Sukurto formato komponentų susiejimas su duomenų modelio elementais elektroninėse ataskaitose (ER)"
description: "Tolesnėje procedūroje parodoma, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali susieti duomenų modelio elementus su sukurtos elektroninių ataskaitų (ER) konfigūracijos, nustatančios verslo mokėjimų srities elektroninio dokumento formatą, komponentais."
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
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
ms.openlocfilehash: 1c81a1268a56164e0d4465359a0f9ec425ee7c31
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a><span data-ttu-id="7acd6-103">Sukurto formato komponentų susiejimas su duomenų modelio elementais elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="7acd6-103">Map components of the created format to data model elements for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7acd6-104">Tolesnėje procedūroje parodoma, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali susieti duomenų modelio elementus su sukurtos elektroninių ataskaitų (ER) konfigūracijos, nustatančios verslo mokėjimų srities elektroninio dokumento formatą, komponentais.</span><span class="sxs-lookup"><span data-stu-id="7acd6-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="7acd6-105">Šį formatą bus galima naudoti vėliau norint generuoti elektroninius mokėjimų apdorojimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="7acd6-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="7acd6-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc.“ formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="7acd6-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="7acd6-107">Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijos bendrinamos visoms įmonėms.</span><span class="sxs-lookup"><span data-stu-id="7acd6-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="7acd6-108">Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti užduočių vadovo „Kurti formato konfigūraciją“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7acd6-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="7acd6-109">Pasirinkti formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="7acd6-109">Select a format configuration</span></span>
1. <span data-ttu-id="7acd6-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="7acd6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7acd6-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="7acd6-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7acd6-112">Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="7acd6-113">Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="7acd6-114">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="7acd6-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="7acd6-115">Susieti formato komponentus su duomenų modelio elementais</span><span class="sxs-lookup"><span data-stu-id="7acd6-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="7acd6-116">Spustelėkite Išplėsti / sutraukti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="7acd6-117">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="7acd6-118">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="7acd6-119">Medyje pasirinkite „Xml \ Pranešimas \ ProcessingDate \ DateTime“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="7acd6-120">Medyje pasirinkite „modelis \ ProcessingDateTime”.</span><span class="sxs-lookup"><span data-stu-id="7acd6-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="7acd6-121">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-121">Click Bind.</span></span>
7. <span data-ttu-id="7acd6-122">Medyje pasirinkite „Xml \ Pranešimas \ MessageId \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="7acd6-123">Medyje pasirinkite „modelis \ MessageIdentification”.</span><span class="sxs-lookup"><span data-stu-id="7acd6-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="7acd6-124">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-124">Click Bind.</span></span>
10. <span data-ttu-id="7acd6-125">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="7acd6-126">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="7acd6-127">Medyje pasirinkite „modelis \ Mokėjimai \ InstructedAmount“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="7acd6-128">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-128">Click Bind.</span></span>
14. <span data-ttu-id="7acd6-129">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate \ DateTime“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="7acd6-130">Medyje pasirinkite „modelis \ Mokėjimai \ TransactionDate“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="7acd6-131">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-131">Click Bind.</span></span>
17. <span data-ttu-id="7acd6-132">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="7acd6-133">Medyje pasirinkite „modelis \ Mokėjimai \ Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="7acd6-134">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-134">Click Bind.</span></span>
20. <span data-ttu-id="7acd6-135">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="7acd6-136">Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="7acd6-137">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-137">Click Bind.</span></span>
23. <span data-ttu-id="7acd6-138">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Id“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="7acd6-139">Medyje pasirinkite „modelis \ Mokėjimai \ End2EndID“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="7acd6-140">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-140">Click Bind.</span></span>
26. <span data-ttu-id="7acd6-141">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="7acd6-142">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="7acd6-143">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Agentas‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="7acd6-144">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="7acd6-145">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="7acd6-146">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-146">Click Bind.</span></span>
32. <span data-ttu-id="7acd6-147">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="7acd6-148">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Agentas \ RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="7acd6-149">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-149">Click Bind.</span></span>
35. <span data-ttu-id="7acd6-150">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="7acd6-151">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita \ Numeris“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="7acd6-152">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-152">Click Bind.</span></span>
38. <span data-ttu-id="7acd6-153">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="7acd6-154">Medyje išplėskite „modelis \ Mokėjimai \ Skolininkas‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="7acd6-155">Medyje išplėskite „modelis \ Mokėjimai \ Skolininkas \ Sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="7acd6-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="7acd6-156">Medyje išplėskite „modelis \ Mokėjimai \ Skolininkas \ Agentas“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="7acd6-157">Medyje pasirinkite „modelis \ Mokėjimai \ Skolininkas \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="7acd6-158">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-158">Click Bind.</span></span>
44. <span data-ttu-id="7acd6-159">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="7acd6-160">Medyje pasirinkite „modelis \ Mokėjimai \ Debitorius \ Agentas \ RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="7acd6-161">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-161">Click Bind.</span></span>
47. <span data-ttu-id="7acd6-162">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber \ Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="7acd6-163">Medyje pasirinkite „modelis \ Mokėjimai \ Skolininkas \ Sąskaita \ Numeris“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="7acd6-164">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-164">Click Bind.</span></span>
50. <span data-ttu-id="7acd6-165">Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="7acd6-166">Medyje pasirinkite „modelis \ Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="7acd6-167">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-167">Click Bind.</span></span>
53. <span data-ttu-id="7acd6-168">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="7acd6-169">Tikrinti formato susiejimą</span><span class="sxs-lookup"><span data-stu-id="7acd6-169">Validate format mapping</span></span>
1. <span data-ttu-id="7acd6-170">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-170">Click Validate.</span></span>
    * <span data-ttu-id="7acd6-171">Norėdami įsitikinti, kad visi susiejimai veikia gerai, patikrinkite naują susiejimą.</span><span class="sxs-lookup"><span data-stu-id="7acd6-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="7acd6-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7acd6-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="7acd6-173">Pakeisti esamos formato konfigūracijos versijos būseną</span><span class="sxs-lookup"><span data-stu-id="7acd6-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="7acd6-174">Atlikdami kitus veiksmus pakeisite formato konfigūracijos būseną iš Juodraštis į Baigta, kad ją būtų galima naudoti generuojant mokėjimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="7acd6-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="7acd6-175">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="7acd6-175">Click Change status.</span></span>
2. <span data-ttu-id="7acd6-176">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="7acd6-176">Click Complete.</span></span>
3. <span data-ttu-id="7acd6-177">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7acd6-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7acd6-178">Pavyzdžiui, „1 versija“.</span><span class="sxs-lookup"><span data-stu-id="7acd6-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="7acd6-179">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7acd6-179">Click OK.</span></span>
5. <span data-ttu-id="7acd6-180">Pasirinkite baigtą esamos konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="7acd6-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="7acd6-181">Atkreipkite dėmesį, kad konfigūracija įrašoma kaip 1.1 baigta versija: formato 1 versija, paremta duomenų modelio 1 versija.</span><span class="sxs-lookup"><span data-stu-id="7acd6-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="7acd6-182">Nustatyti baigtos formato versijos įsigaliojimo datą</span><span class="sxs-lookup"><span data-stu-id="7acd6-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="7acd6-183">Kiekvieną formato versiją galima sukonfigūruoti taip,kad ji būtų parengta naudoti nuo tam tikros datos.</span><span class="sxs-lookup"><span data-stu-id="7acd6-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="7acd6-184">Kai pasirinktą dieną veikia daugiau nei viena formato versija, bus naudojamas naujausias formatas (pagal versijos numerį).</span><span class="sxs-lookup"><span data-stu-id="7acd6-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="7acd6-185">Tinkame versija parenkama naudojant seanso datos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7acd6-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="7acd6-186">Apriboti įmonių prieigą prie sukurto formato</span><span class="sxs-lookup"><span data-stu-id="7acd6-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="7acd6-187">Išplėskite dalį ISO šalies / regiono kodai.</span><span class="sxs-lookup"><span data-stu-id="7acd6-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="7acd6-188">Kiekvieną formato prieigą galima apriboti nustatant konkrečias šalis / regionus, kuriuose veiks šis formatas.</span><span class="sxs-lookup"><span data-stu-id="7acd6-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="7acd6-189">Kai konkretaus formato šalių / regionų sąrašas yra tuščias, šį formatą galima naudoti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="7acd6-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="7acd6-190">Į šalių / regionų sąrašą įterpus ISO šalių / regionų kodus, formatą bus galima naudoti tik įmonėse, kurių pagrindinis adresas yra šalyje / regione.</span><span class="sxs-lookup"><span data-stu-id="7acd6-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

