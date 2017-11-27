--- 
title: "Konfigūracijos, skirtos generuoti ataskaitoms „OpenXML” formatu, kūrimas elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninių dokumentų generavimo OPENXML formatu šabloną."
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
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="f81ba-103">Konfigūracijos, skirtos generuoti ataskaitoms „OpenXML” formatu, kūrimas elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="f81ba-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f81ba-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninių dokumentų generavimo OPENXML formatu šabloną.</span><span class="sxs-lookup"><span data-stu-id="f81ba-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="f81ba-105">Ši konfigūracija bus naudojama apdoroti tiekėjų mokėjimams.</span><span class="sxs-lookup"><span data-stu-id="f81ba-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="f81ba-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti GBSI įmonėje.</span><span class="sxs-lookup"><span data-stu-id="f81ba-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="f81ba-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="f81ba-108">Taip pat turite atsisiųsti ir įrašyti „Microsoft Excel“ failą [Mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="f81ba-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="f81ba-109">Mokėjimų duomenų modelio konfigūracijos nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="f81ba-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="f81ba-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="f81ba-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f81ba-111">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f81ba-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f81ba-112">Pasirinkite pavyzdinės įmonės „Litware, Inc“ konfigūracijos teikėją. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite užbaigti procedūros „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų" veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f81ba-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="f81ba-113">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="f81ba-113">Click Set active.</span></span>
4. <span data-ttu-id="f81ba-114">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="f81ba-114">Click Repositories.</span></span>
    * <span data-ttu-id="f81ba-115">Jei yra, pasirinkite tipo Operacijų ištekliai saugyklą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="f81ba-116">Jei tokia yra, praleiskite tolesnius naujos saugyklos kūrimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f81ba-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="f81ba-117">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="f81ba-118">Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="f81ba-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="f81ba-119">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-119">Click Create repository.</span></span>
8. <span data-ttu-id="f81ba-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f81ba-120">Click OK.</span></span>
9. <span data-ttu-id="f81ba-121">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-121">Click Open.</span></span>
10. <span data-ttu-id="f81ba-122">Medyje pasirinkite Mokėjimo modelis.</span><span class="sxs-lookup"><span data-stu-id="f81ba-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="f81ba-123">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-123">Click Import.</span></span>
    * <span data-ttu-id="f81ba-124">Importuokite šį duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-124">Import this data model.</span></span> <span data-ttu-id="f81ba-125">Jis bus naudojamas kaip duomenų šaltinis naujoje formato konfigūracijoje.</span><span class="sxs-lookup"><span data-stu-id="f81ba-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="f81ba-126">Jei ši konfigūracija jau importuota, šį veiksmą praleiskite.</span><span class="sxs-lookup"><span data-stu-id="f81ba-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="f81ba-127">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f81ba-127">Click Yes.</span></span>
13. <span data-ttu-id="f81ba-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-128">Close the page.</span></span>
14. <span data-ttu-id="f81ba-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f81ba-130">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="f81ba-130">Create a new format configuration</span></span>
1. <span data-ttu-id="f81ba-131">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f81ba-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="f81ba-132">Medyje pasirinkite Mokėjimo modelis.</span><span class="sxs-lookup"><span data-stu-id="f81ba-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="f81ba-133">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f81ba-134">Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="f81ba-135">Sukurkite formatą, paremtą duomenų modeliu „PaymentModel‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="f81ba-136">Lauke Pavadinimas įveskite „Darbalapio ataskaitos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="f81ba-137">Darbalapio ataskaitos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f81ba-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="f81ba-138">Lauke Aprašas įveskite „Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="f81ba-139">Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f81ba-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="f81ba-140">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f81ba-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="f81ba-141">Pasirinkite apibrėžtį „CustomerCreditTransferInitiation‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="f81ba-142">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="f81ba-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="f81ba-143">Naujo dokumento kūrimas OPENXML darbalapio formatu</span><span class="sxs-lookup"><span data-stu-id="f81ba-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="f81ba-144">Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f81ba-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="f81ba-145">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f81ba-145">Click Designer.</span></span>
3. <span data-ttu-id="f81ba-146">Veiksmų srityje spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="f81ba-147">Spustelėkite Importuoti iš „Excel‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="f81ba-148">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="f81ba-148">Click Attachments.</span></span>
    * <span data-ttu-id="f81ba-149">Kaip šabloną pridėkite esamą „Excel‟ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="f81ba-150">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-150">Click New.</span></span>
7. <span data-ttu-id="f81ba-151">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-151">Click File.</span></span>
    * <span data-ttu-id="f81ba-152">Nurodykite esamą „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="f81ba-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-153">Close the page.</span></span>
9. <span data-ttu-id="f81ba-154">Lauke Šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f81ba-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="f81ba-155">Pasirinkite pridėtą „Excel‟ failą, kuris bus naudojamas kaip šablonas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="f81ba-156">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f81ba-156">Click OK.</span></span>
    * <span data-ttu-id="f81ba-157">Atkreipkite dėmesį, kad ER formato komponentai sukurti kūrimo formatu, paremtu susijusio „MS Excel‟ dokumento struktūra (įvardytaisiais diapazonais).</span><span class="sxs-lookup"><span data-stu-id="f81ba-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="f81ba-158">Naujo duomenų šaltinio kūrimas, kad būtų galima skaičiuoti bendrąsias sumas pagal valiutos kodus</span><span class="sxs-lookup"><span data-stu-id="f81ba-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="f81ba-159">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="f81ba-160">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f81ba-161">Medyje pasirinkite Funkcijos\Grupuoti pagal.</span><span class="sxs-lookup"><span data-stu-id="f81ba-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="f81ba-162">Lauke Pavadinimas įveskite „PaymentByCurrency‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="f81ba-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="f81ba-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="f81ba-164">Spustelėkite Redaguoti grupę pagal.</span><span class="sxs-lookup"><span data-stu-id="f81ba-164">Click Edit group by.</span></span>
6. <span data-ttu-id="f81ba-165">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="f81ba-166">Medyje pasirinkite „modelis \ Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="f81ba-167">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="f81ba-167">Click Add field to.</span></span>
9. <span data-ttu-id="f81ba-168">Spustelėkite Ką grupuoti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-168">Click What to group.</span></span>
10. <span data-ttu-id="f81ba-169">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="f81ba-170">Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="f81ba-171">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="f81ba-171">Click Add field to.</span></span>
13. <span data-ttu-id="f81ba-172">Spustelėkite Sugrupuoti laukai.</span><span class="sxs-lookup"><span data-stu-id="f81ba-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="f81ba-173">Medyje pasirinkite „modelis \ Mokėjimai \ Nurodyta suma (InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="f81ba-174">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="f81ba-174">Click Add field to.</span></span>
16. <span data-ttu-id="f81ba-175">Spustelėkite Telkimo laukai.</span><span class="sxs-lookup"><span data-stu-id="f81ba-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="f81ba-176">Lauke Metodas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="f81ba-177">Pasirinkite telkimo funkciją SUM.</span><span class="sxs-lookup"><span data-stu-id="f81ba-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="f81ba-178">Lauke Pavadinimas įveskite „TotalInstructuredAmount‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="f81ba-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="f81ba-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="f81ba-180">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-180">Click Save.</span></span>
20. <span data-ttu-id="f81ba-181">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-181">Close the page.</span></span>
21. <span data-ttu-id="f81ba-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f81ba-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="f81ba-183">Formato komponentų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="f81ba-183">Map format components to data sources</span></span>
1. <span data-ttu-id="f81ba-184">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="f81ba-185">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="f81ba-186">Medyje išplėskite „modelis \ Mokėjimai \ Inicijuojanti šalis(InitiatingParty)‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="f81ba-187">Medyje pasirinkite „modelis \ Mokėjimai \ Inicijuojanti šalis(InitiatingParty) \ Pavadinimas‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="f81ba-188">Medyje išplėskite „Excel \ ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="f81ba-189">Medyje pasirinkite „Excel \ ReportHeader \ CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="f81ba-190">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-190">Click Bind.</span></span>
8. <span data-ttu-id="f81ba-191">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="f81ba-192">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Identifikacija‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="f81ba-193">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Identifikacija \ Šaltinio ID(SourceID)‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="f81ba-194">Medyje išplėskite „Excel \ PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="f81ba-195">Medyje pasirinkite „Excel \ PaymLines \ VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="f81ba-196">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-196">Click Bind.</span></span>
14. <span data-ttu-id="f81ba-197">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="f81ba-198">Medyje pasirinkite „Excel \ PaymLines \ VendName”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="f81ba-199">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-199">Click Bind.</span></span>
17. <span data-ttu-id="f81ba-200">Medyje išplėskite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent)‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="f81ba-201">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent) \ Pavadinimas‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="f81ba-202">Medyje pasirinkite „Excel \ PaymLines \ Bankas”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="f81ba-203">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-203">Click Bind.</span></span>
21. <span data-ttu-id="f81ba-204">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent) \ Banko numeris(RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="f81ba-205">Medyje pasirinkite „Excel \ PaymLines \ RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="f81ba-206">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-206">Click Bind.</span></span>
24. <span data-ttu-id="f81ba-207">Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="f81ba-208">Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)\Identifikacija‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="f81ba-209">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus sąskaita(CreditorAccount) \ Identifikacija \ Numeris‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="f81ba-210">Medyje pasirinkite „Excel \ PaymLines \ AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="f81ba-211">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-211">Click Bind.</span></span>
29. <span data-ttu-id="f81ba-212">Medyje pasirinkite „modelis \ Mokėjimai \ Nurodyta suma (InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="f81ba-213">Medyje pasirinkite „Excel \ PaymLines \ Debetas”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="f81ba-214">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-214">Click Bind.</span></span>
32. <span data-ttu-id="f81ba-215">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="f81ba-216">Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="f81ba-217">Medyje išplėskite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent)‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="f81ba-218">Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="f81ba-219">Medyje pasirinkite „Excel \ PaymLines \ Valiuta”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="f81ba-220">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-220">Click Bind.</span></span>
38. <span data-ttu-id="f81ba-221">Medyje išplėskite „PaymentByCurrency‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="f81ba-222">Medyje išplėskite „PaymentByCurrency \ sugrupuota‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="f81ba-223">Medyje pasirinkite „PaymentByCurrency \ sugrupuota \ Valiuta‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="f81ba-224">Medyje išplėskite „Excel \ SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="f81ba-225">Medyje pasirinkite „Excel \ SummaryLines \ SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="f81ba-226">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-226">Click Bind.</span></span>
44. <span data-ttu-id="f81ba-227">Medyje išplėskite „PaymentByCurrency \ sutelkta‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="f81ba-228">Medyje pasirinkite „PaymentByCurrency \ sutelkta \ TotalInstructuredAmount‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="f81ba-229">Medyje pasirinkite „Excel \ SummaryLines \ SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="f81ba-230">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-230">Click Bind.</span></span>
48. <span data-ttu-id="f81ba-231">Medyje pasirinkite „PaymentByCurrency‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="f81ba-232">Medyje pasirinkite „Excel \ SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="f81ba-233">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-233">Click Bind.</span></span>
51. <span data-ttu-id="f81ba-234">Medyje pasirinkite „modelis \ Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="f81ba-235">Medyje pasirinkite „Excel \ PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="f81ba-236">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-236">Click Bind.</span></span>
54. <span data-ttu-id="f81ba-237">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-237">Click Save.</span></span>
55. <span data-ttu-id="f81ba-238">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="f81ba-239">Naudokite sukurtą konfigūraciją mokėjimams apdoroti</span><span class="sxs-lookup"><span data-stu-id="f81ba-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="f81ba-240">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="f81ba-240">Click Change status.</span></span>
2. <span data-ttu-id="f81ba-241">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-241">Click Complete.</span></span>
3. <span data-ttu-id="f81ba-242">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f81ba-242">Click OK.</span></span>
4. <span data-ttu-id="f81ba-243">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-243">Close the page.</span></span>
5. <span data-ttu-id="f81ba-244">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-244">Close the page.</span></span>
6. <span data-ttu-id="f81ba-245">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="f81ba-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="f81ba-246">Norėdami filtruoti lauką Mokėjimo būdas pagal reikšmę „Elektroninis“, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="f81ba-247">Elektroninis</span><span class="sxs-lookup"><span data-stu-id="f81ba-247">Electronic</span></span>  
8. <span data-ttu-id="f81ba-248">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-248">Click Edit.</span></span>
9. <span data-ttu-id="f81ba-249">Išplėskite dalį Failo formatai.</span><span class="sxs-lookup"><span data-stu-id="f81ba-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="f81ba-250">Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f81ba-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="f81ba-251">Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f81ba-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="f81ba-252">Pasirinkite konfigūraciją „Darbalapio ataskaitos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="f81ba-253">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-253">Click Save.</span></span>
13. <span data-ttu-id="f81ba-254">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f81ba-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="f81ba-255">Sukurtosios konfigūracijos naudojimas tikrinant mokėjimo žurnalų apdorojimą</span><span class="sxs-lookup"><span data-stu-id="f81ba-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="f81ba-256">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f81ba-257">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-257">Click New.</span></span>
    * <span data-ttu-id="f81ba-258">Sukurkite naują mokėjimų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="f81ba-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="f81ba-259">Lauke Pavadinimas įveskite „VendPay“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="f81ba-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="f81ba-260">VendPay</span></span>  
4. <span data-ttu-id="f81ba-261">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="f81ba-261">Click Lines.</span></span>
5. <span data-ttu-id="f81ba-262">Lauke Sąskaita nurodykite reikšmes „GB_SI_000001“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="f81ba-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="f81ba-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="f81ba-264">Debetas nustatykite į „1000‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="f81ba-265">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-265">Click New.</span></span>
8. <span data-ttu-id="f81ba-266">Lauke Sąskaita nurodykite reikšmes „GB_SI_000005“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="f81ba-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="f81ba-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="f81ba-268">Debetas nustatykite į „2000‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="f81ba-269">Lauke Valiuta įveskite „EUR‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="f81ba-270">EUR</span><span class="sxs-lookup"><span data-stu-id="f81ba-270">EUR</span></span>  
11. <span data-ttu-id="f81ba-271">Lauke Korespondentinė sąskaita nurodykite reikšmes „GBSI OPER“.</span><span class="sxs-lookup"><span data-stu-id="f81ba-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="f81ba-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="f81ba-272">GBSI OPER</span></span>  
12. <span data-ttu-id="f81ba-273">Lauke Mokėjimo būdas įveskite „Elektroninis‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="f81ba-274">Elektroninis</span><span class="sxs-lookup"><span data-stu-id="f81ba-274">Electronic</span></span>  
13. <span data-ttu-id="f81ba-275">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f81ba-275">Click Save.</span></span>
14. <span data-ttu-id="f81ba-276">Spustelėkite Generuoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="f81ba-276">Click Generate payments.</span></span>
15. <span data-ttu-id="f81ba-277">Lauke Mokėjimo būdas įveskite „Elektroninis‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="f81ba-278">Elektroninis</span><span class="sxs-lookup"><span data-stu-id="f81ba-278">Electronic</span></span>  
16. <span data-ttu-id="f81ba-279">Lauke Failo vardas, įveskite „Mokėjimai”.</span><span class="sxs-lookup"><span data-stu-id="f81ba-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="f81ba-280">Pvz., įveskite „Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="f81ba-281">Lauke Banko sąskaita įveskite „GBSI OPER‟.</span><span class="sxs-lookup"><span data-stu-id="f81ba-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="f81ba-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="f81ba-282">GBSI OPER</span></span>  
18. <span data-ttu-id="f81ba-283">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f81ba-283">Click OK.</span></span>
19. <span data-ttu-id="f81ba-284">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f81ba-284">Click OK.</span></span>
    * <span data-ttu-id="f81ba-285">Peržiūrėkite sukurtąjį darbalapį – išsamią mokėjimo eilučių informaciją bei kiekvieno šiame mokėjimo pranešime naudojamo valiutos kodo bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="f81ba-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


