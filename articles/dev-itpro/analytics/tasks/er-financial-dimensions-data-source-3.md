--- 
title: "Ataskaitų, pagal kurias finansinės dimensijos būtų naudojamos kaip duomenų šaltiniai, kūrimas"
description: "Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="fc0eb-103">Ataskaitų, pagal kurias finansinės dimensijos būtų naudojamos kaip duomenų šaltiniai, kūrimas</span><span class="sxs-lookup"><span data-stu-id="fc0eb-103">Design reports to use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc0eb-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fc0eb-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="fc0eb-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (2 dalis: modelio susiejimas)“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="fc0eb-107">Ataskaitos kūrimas finansinėms dimensijoms pateikti</span><span class="sxs-lookup"><span data-stu-id="fc0eb-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="fc0eb-108">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fc0eb-109">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fc0eb-110">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="fc0eb-111">Lauke Naujas įveskite Formatas, pagrįstas duomenų modeliu Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="fc0eb-112">Naudokite modelį, kuris buvo iš anksto sukurtas kaip naujos ataskaitos duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="fc0eb-113">Lauke Pavadinimas, įveskite DK žurnalo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="fc0eb-114">Lauke Duomenų modelio aprašas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="fc0eb-115">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-115">Click Create configuration.</span></span>
8. <span data-ttu-id="fc0eb-116">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-116">Click Designer.</span></span>
9. <span data-ttu-id="fc0eb-117">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="fc0eb-118">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="fc0eb-119">Lauke Pavadinimas įveskite Šaknis.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="fc0eb-120">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-120">Click OK.</span></span>
13. <span data-ttu-id="fc0eb-121">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="fc0eb-122">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="fc0eb-123">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="fc0eb-124">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-124">Click OK.</span></span>
17. <span data-ttu-id="fc0eb-125">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="fc0eb-126">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="fc0eb-127">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="fc0eb-128">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-128">Click OK.</span></span>
21. <span data-ttu-id="fc0eb-129">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="fc0eb-130">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="fc0eb-131">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="fc0eb-132">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="fc0eb-133">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-133">Click OK.</span></span>
26. <span data-ttu-id="fc0eb-134">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="fc0eb-135">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="fc0eb-136">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="fc0eb-137">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-137">Click OK.</span></span>
30. <span data-ttu-id="fc0eb-138">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="fc0eb-139">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="fc0eb-140">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="fc0eb-141">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="fc0eb-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-142">Click OK.</span></span>
35. <span data-ttu-id="fc0eb-143">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="fc0eb-144">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="fc0eb-145">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-145">Click OK.</span></span>
38. <span data-ttu-id="fc0eb-146">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="fc0eb-147">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="fc0eb-148">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-148">Click OK.</span></span>
41. <span data-ttu-id="fc0eb-149">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="fc0eb-150">Lauke Pavadinimas Dt.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="fc0eb-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-151">Click OK.</span></span>
44. <span data-ttu-id="fc0eb-152">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="fc0eb-153">Lauke Pavadinimas įveskite Ct.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="fc0eb-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-154">Click OK.</span></span>
47. <span data-ttu-id="fc0eb-155">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="fc0eb-156">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="fc0eb-157">Lauke Pavadinimas įveskite Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="fc0eb-158">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-158">Click OK.</span></span>
51. <span data-ttu-id="fc0eb-159">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="fc0eb-160">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="fc0eb-161">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="fc0eb-162">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="fc0eb-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-163">Click OK.</span></span>
56. <span data-ttu-id="fc0eb-164">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="fc0eb-165">Lauke Pavadinimas įveskite Reikšmė.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="fc0eb-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-166">Click OK.</span></span>
59. <span data-ttu-id="fc0eb-167">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="fc0eb-168">Lauke Pavadinimas įveskite Aprašas.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="fc0eb-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="fc0eb-170">Ataskaitos elementų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="fc0eb-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="fc0eb-171">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="fc0eb-172">Medyje išplėskite dalį model: Data model Financial dimensions sample model.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fc0eb-173">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="fc0eb-174">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="fc0eb-175">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="fc0eb-176">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="fc0eb-177">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="fc0eb-178">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-178">Click Bind.</span></span>
9. <span data-ttu-id="fc0eb-179">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="fc0eb-180">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="fc0eb-181">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-181">Click Bind.</span></span>
12. <span data-ttu-id="fc0eb-182">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="fc0eb-183">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="fc0eb-184">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-184">Click Bind.</span></span>
15. <span data-ttu-id="fc0eb-185">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="fc0eb-186">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="fc0eb-187">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-187">Click Bind.</span></span>
18. <span data-ttu-id="fc0eb-188">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="fc0eb-189">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="fc0eb-190">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-190">Click Bind.</span></span>
21. <span data-ttu-id="fc0eb-191">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="fc0eb-192">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="fc0eb-193">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-193">Click Bind.</span></span>
24. <span data-ttu-id="fc0eb-194">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="fc0eb-195">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="fc0eb-196">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-196">Click Bind.</span></span>
27. <span data-ttu-id="fc0eb-197">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="fc0eb-198">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="fc0eb-199">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-199">Click Bind.</span></span>
30. <span data-ttu-id="fc0eb-200">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="fc0eb-201">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="fc0eb-202">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-202">Click Bind.</span></span>
33. <span data-ttu-id="fc0eb-203">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="fc0eb-204">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="fc0eb-205">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-205">Click Bind.</span></span>
36. <span data-ttu-id="fc0eb-206">Medyje pasirinkite Root: XML Element\Journal: XML Element\Batch: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="fc0eb-207">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="fc0eb-208">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-208">Click Bind.</span></span>
39. <span data-ttu-id="fc0eb-209">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="fc0eb-210">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="fc0eb-211">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-211">Click Bind.</span></span>
42. <span data-ttu-id="fc0eb-212">Medyje pasirinkite Root: XML Element\Company: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="fc0eb-213">Medyje pasirinkite model: Data model Financial dimensions sample model\Company: String.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="fc0eb-214">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-214">Click Bind.</span></span>
45. <span data-ttu-id="fc0eb-215">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-215">Click Save.</span></span>
46. <span data-ttu-id="fc0eb-216">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-216">Close the page.</span></span>


