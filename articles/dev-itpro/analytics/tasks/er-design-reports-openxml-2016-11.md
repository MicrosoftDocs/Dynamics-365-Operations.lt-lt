---
title: 'ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas (2016 m. lapkričio mėn.)'
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninių dokumentų generavimo OPENXML formatu šabloną.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "326658"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="31d0f-103">ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="31d0f-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31d0f-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninių dokumentų generavimo OPENXML formatu šabloną.</span><span class="sxs-lookup"><span data-stu-id="31d0f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="31d0f-105">Ši konfigūracija bus naudojama apdoroti tiekėjų mokėjimams.</span><span class="sxs-lookup"><span data-stu-id="31d0f-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="31d0f-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti GBSI įmonėje.</span><span class="sxs-lookup"><span data-stu-id="31d0f-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="31d0f-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="31d0f-108">Taip pat reikia turėti „Excel‟ failą, kuris bus importuotas kuriant šabloną.</span><span class="sxs-lookup"><span data-stu-id="31d0f-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="31d0f-109">Šį failą galima rasti srityje [Mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="31d0f-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="31d0f-110">Mokėjimų duomenų modelio konfigūracijos nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="31d0f-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="31d0f-111">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="31d0f-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="31d0f-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="31d0f-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="31d0f-113">Pasirinkite pavyzdinės įmonės „Litware, Inc“ konfigūracijos teikėją. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite užbaigti procedūros „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų" veiksmus.</span><span class="sxs-lookup"><span data-stu-id="31d0f-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="31d0f-114">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="31d0f-114">Click Set active.</span></span>
4. <span data-ttu-id="31d0f-115">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="31d0f-115">Click Repositories.</span></span>
    * <span data-ttu-id="31d0f-116">Jei yra, pasirinkite tipo Operacijų ištekliai saugyklą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="31d0f-117">Jei tokia yra, praleiskite tolesnius naujos saugyklos kūrimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="31d0f-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="31d0f-118">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="31d0f-119">Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="31d0f-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="31d0f-120">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-120">Click Create repository.</span></span>
8. <span data-ttu-id="31d0f-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="31d0f-121">Click OK.</span></span>
9. <span data-ttu-id="31d0f-122">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-122">Click Open.</span></span>
10. <span data-ttu-id="31d0f-123">Medyje pasirinkite Mokėjimo modelis.</span><span class="sxs-lookup"><span data-stu-id="31d0f-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="31d0f-124">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-124">Click Import.</span></span>
    * <span data-ttu-id="31d0f-125">Importuokite šį duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-125">Import this data model.</span></span> <span data-ttu-id="31d0f-126">Jis bus naudojamas kaip duomenų šaltinis naujoje formato konfigūracijoje.</span><span class="sxs-lookup"><span data-stu-id="31d0f-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="31d0f-127">Jei ši konfigūracija jau importuota, šį veiksmą praleiskite.</span><span class="sxs-lookup"><span data-stu-id="31d0f-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="31d0f-128">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="31d0f-128">Click Yes.</span></span>
13. <span data-ttu-id="31d0f-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-129">Close the page.</span></span>
14. <span data-ttu-id="31d0f-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="31d0f-131">Kurti naują formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="31d0f-131">Create a new format configuration</span></span>
1. <span data-ttu-id="31d0f-132">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="31d0f-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="31d0f-133">Medyje pasirinkite Mokėjimo modelis.</span><span class="sxs-lookup"><span data-stu-id="31d0f-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="31d0f-134">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="31d0f-135">Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="31d0f-136">Sukurkite formatą, paremtą duomenų modeliu „PaymentModel‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="31d0f-137">Lauke Pavadinimas įveskite „Darbalapio ataskaitos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="31d0f-138">Darbalapio ataskaitos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="31d0f-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="31d0f-139">Lauke Aprašas įveskite „Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="31d0f-140">Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="31d0f-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="31d0f-141">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="31d0f-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="31d0f-142">Pasirinkite apibrėžtį „CustomerCreditTransferInitiation‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="31d0f-143">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="31d0f-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="31d0f-144">Naujo dokumento kūrimas OPENXML darbalapio formatu</span><span class="sxs-lookup"><span data-stu-id="31d0f-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="31d0f-145">Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="31d0f-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="31d0f-146">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="31d0f-146">Click Designer.</span></span>
3. <span data-ttu-id="31d0f-147">Veiksmų srityje spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="31d0f-148">Spustelėkite Importuoti iš „Excel‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="31d0f-149">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="31d0f-149">Click Attachments.</span></span>
    * <span data-ttu-id="31d0f-150">Kaip šabloną pridėkite esamą „Excel‟ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="31d0f-151">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-151">Click New.</span></span>
7. <span data-ttu-id="31d0f-152">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-152">Click File.</span></span>
    * <span data-ttu-id="31d0f-153">Nurodykite esamą „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="31d0f-154">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-154">Close the page.</span></span>
9. <span data-ttu-id="31d0f-155">Lauke Šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="31d0f-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="31d0f-156">Pasirinkite pridėtą „Excel‟ failą, kuris bus naudojamas kaip šablonas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="31d0f-157">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="31d0f-157">Click OK.</span></span>
    * <span data-ttu-id="31d0f-158">Atkreipkite dėmesį, kad ER formato komponentai sukurti kūrimo formatu, paremtu susijusio „MS Excel‟ dokumento struktūra (įvardytaisiais diapazonais).</span><span class="sxs-lookup"><span data-stu-id="31d0f-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="31d0f-159">Naujo duomenų šaltinio kūrimas, kad būtų galima skaičiuoti bendrąsias sumas pagal valiutos kodus</span><span class="sxs-lookup"><span data-stu-id="31d0f-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="31d0f-160">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="31d0f-161">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="31d0f-162">Medyje pasirinkite Funkcijos\Grupuoti pagal.</span><span class="sxs-lookup"><span data-stu-id="31d0f-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="31d0f-163">Lauke Pavadinimas įveskite „PaymentByCurrency‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="31d0f-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="31d0f-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="31d0f-165">Spustelėkite Redaguoti grupę pagal.</span><span class="sxs-lookup"><span data-stu-id="31d0f-165">Click Edit group by.</span></span>
6. <span data-ttu-id="31d0f-166">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="31d0f-167">Medyje pasirinkite „modelis \ Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="31d0f-168">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="31d0f-168">Click Add field to.</span></span>
9. <span data-ttu-id="31d0f-169">Spustelėkite Ką grupuoti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-169">Click What to group.</span></span>
10. <span data-ttu-id="31d0f-170">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="31d0f-171">Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="31d0f-172">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="31d0f-172">Click Add field to.</span></span>
13. <span data-ttu-id="31d0f-173">Spustelėkite Sugrupuoti laukai.</span><span class="sxs-lookup"><span data-stu-id="31d0f-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="31d0f-174">Medyje pasirinkite „modelis \ Mokėjimai \ Nurodyta suma (InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="31d0f-175">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="31d0f-175">Click Add field to.</span></span>
16. <span data-ttu-id="31d0f-176">Spustelėkite Telkimo laukai.</span><span class="sxs-lookup"><span data-stu-id="31d0f-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="31d0f-177">Lauke Metodas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="31d0f-178">Pasirinkite telkimo funkciją SUM.</span><span class="sxs-lookup"><span data-stu-id="31d0f-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="31d0f-179">Lauke Pavadinimas įveskite „TotalInstructuredAmount‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="31d0f-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="31d0f-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="31d0f-181">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-181">Click Save.</span></span>
20. <span data-ttu-id="31d0f-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-182">Close the page.</span></span>
21. <span data-ttu-id="31d0f-183">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="31d0f-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="31d0f-184">Formato komponentų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="31d0f-184">Map format components to data sources</span></span>
1. <span data-ttu-id="31d0f-185">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="31d0f-186">Medyje išplėskite „modelis \ Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="31d0f-187">Medyje išplėskite „modelis \ Mokėjimai \ Inicijuojanti šalis(InitiatingParty)‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="31d0f-188">Medyje pasirinkite „modelis \ Mokėjimai \ Inicijuojanti šalis(InitiatingParty) \ Pavadinimas‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="31d0f-189">Medyje išplėskite „Excel \ ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="31d0f-190">Medyje pasirinkite „Excel \ ReportHeader \ CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="31d0f-191">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-191">Click Bind.</span></span>
8. <span data-ttu-id="31d0f-192">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="31d0f-193">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Identifikacija‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="31d0f-194">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Identifikacija \ Šaltinio ID(SourceID)‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="31d0f-195">Medyje išplėskite „Excel \ PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="31d0f-196">Medyje pasirinkite „Excel \ PaymLines \ VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="31d0f-197">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-197">Click Bind.</span></span>
14. <span data-ttu-id="31d0f-198">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="31d0f-199">Medyje pasirinkite „Excel \ PaymLines \ VendName”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="31d0f-200">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-200">Click Bind.</span></span>
17. <span data-ttu-id="31d0f-201">Medyje išplėskite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent)‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="31d0f-202">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent) \ Pavadinimas‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="31d0f-203">Medyje pasirinkite „Excel \ PaymLines \ Bankas”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="31d0f-204">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-204">Click Bind.</span></span>
21. <span data-ttu-id="31d0f-205">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent) \ Banko numeris(RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="31d0f-206">Medyje pasirinkite „Excel \ PaymLines \ RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="31d0f-207">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-207">Click Bind.</span></span>
24. <span data-ttu-id="31d0f-208">Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="31d0f-209">Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)\Identifikacija‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="31d0f-210">Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus sąskaita(CreditorAccount) \ Identifikacija \ Numeris‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="31d0f-211">Medyje pasirinkite „Excel \ PaymLines \ AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="31d0f-212">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-212">Click Bind.</span></span>
29. <span data-ttu-id="31d0f-213">Medyje pasirinkite „modelis \ Mokėjimai \ Nurodyta suma (InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="31d0f-214">Medyje pasirinkite „Excel \ PaymLines \ Debetas”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="31d0f-215">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-215">Click Bind.</span></span>
32. <span data-ttu-id="31d0f-216">Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="31d0f-217">Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="31d0f-218">Medyje išplėskite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent)‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="31d0f-219">Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="31d0f-220">Medyje pasirinkite „Excel \ PaymLines \ Valiuta”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="31d0f-221">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-221">Click Bind.</span></span>
38. <span data-ttu-id="31d0f-222">Medyje išplėskite „PaymentByCurrency‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="31d0f-223">Medyje išplėskite „PaymentByCurrency \ sugrupuota‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="31d0f-224">Medyje pasirinkite „PaymentByCurrency \ sugrupuota \ Valiuta‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="31d0f-225">Medyje išplėskite „Excel \ SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="31d0f-226">Medyje pasirinkite „Excel \ SummaryLines \ SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="31d0f-227">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-227">Click Bind.</span></span>
44. <span data-ttu-id="31d0f-228">Medyje išplėskite „PaymentByCurrency \ sutelkta‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="31d0f-229">Medyje pasirinkite „PaymentByCurrency \ sutelkta \ TotalInstructuredAmount‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="31d0f-230">Medyje pasirinkite „Excel \ SummaryLines \ SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="31d0f-231">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-231">Click Bind.</span></span>
48. <span data-ttu-id="31d0f-232">Medyje pasirinkite „PaymentByCurrency‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="31d0f-233">Medyje pasirinkite „Excel \ SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="31d0f-234">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-234">Click Bind.</span></span>
51. <span data-ttu-id="31d0f-235">Medyje pasirinkite „modelis \ Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="31d0f-236">Medyje pasirinkite „Excel \ PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="31d0f-237">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-237">Click Bind.</span></span>
54. <span data-ttu-id="31d0f-238">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-238">Click Save.</span></span>
55. <span data-ttu-id="31d0f-239">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="31d0f-240">Naudokite sukurtą konfigūraciją mokėjimams apdoroti</span><span class="sxs-lookup"><span data-stu-id="31d0f-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="31d0f-241">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="31d0f-241">Click Change status.</span></span>
2. <span data-ttu-id="31d0f-242">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-242">Click Complete.</span></span>
3. <span data-ttu-id="31d0f-243">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="31d0f-243">Click OK.</span></span>
4. <span data-ttu-id="31d0f-244">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-244">Close the page.</span></span>
5. <span data-ttu-id="31d0f-245">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-245">Close the page.</span></span>
6. <span data-ttu-id="31d0f-246">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="31d0f-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="31d0f-247">Norėdami filtruoti lauką Mokėjimo būdas pagal reikšmę „Elektroninis“, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="31d0f-248">Elektroninis</span><span class="sxs-lookup"><span data-stu-id="31d0f-248">Electronic</span></span>  
8. <span data-ttu-id="31d0f-249">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-249">Click Edit.</span></span>
9. <span data-ttu-id="31d0f-250">Išplėskite dalį Failo formatai.</span><span class="sxs-lookup"><span data-stu-id="31d0f-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="31d0f-251">Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="31d0f-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="31d0f-252">Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="31d0f-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="31d0f-253">Pasirinkite konfigūraciją „Darbalapio ataskaitos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="31d0f-254">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-254">Click Save.</span></span>
13. <span data-ttu-id="31d0f-255">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="31d0f-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="31d0f-256">Sukurtosios konfigūracijos naudojimas tikrinant mokėjimo žurnalų apdorojimą</span><span class="sxs-lookup"><span data-stu-id="31d0f-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="31d0f-257">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="31d0f-258">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-258">Click New.</span></span>
    * <span data-ttu-id="31d0f-259">Sukurkite naują mokėjimų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="31d0f-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="31d0f-260">Lauke Pavadinimas įveskite „VendPay“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="31d0f-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="31d0f-261">VendPay</span></span>  
4. <span data-ttu-id="31d0f-262">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="31d0f-262">Click Lines.</span></span>
5. <span data-ttu-id="31d0f-263">Lauke Sąskaita nurodykite reikšmes „GB_SI_000001“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="31d0f-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="31d0f-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="31d0f-265">Debetas nustatykite į „1000‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="31d0f-266">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-266">Click New.</span></span>
8. <span data-ttu-id="31d0f-267">Lauke Sąskaita nurodykite reikšmes „GB_SI_000005“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="31d0f-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="31d0f-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="31d0f-269">Debetas nustatykite į „2000‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="31d0f-270">Lauke Valiuta įveskite „EUR‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="31d0f-271">EUR</span><span class="sxs-lookup"><span data-stu-id="31d0f-271">EUR</span></span>  
11. <span data-ttu-id="31d0f-272">Lauke Korespondentinė sąskaita nurodykite reikšmes „GBSI OPER“.</span><span class="sxs-lookup"><span data-stu-id="31d0f-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="31d0f-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="31d0f-273">GBSI OPER</span></span>  
12. <span data-ttu-id="31d0f-274">Lauke Mokėjimo būdas įveskite „Elektroninis‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="31d0f-275">Elektroninis</span><span class="sxs-lookup"><span data-stu-id="31d0f-275">Electronic</span></span>  
13. <span data-ttu-id="31d0f-276">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="31d0f-276">Click Save.</span></span>
14. <span data-ttu-id="31d0f-277">Spustelėkite Generuoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="31d0f-277">Click Generate payments.</span></span>
15. <span data-ttu-id="31d0f-278">Lauke Mokėjimo būdas įveskite „Elektroninis‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="31d0f-279">Elektroninis</span><span class="sxs-lookup"><span data-stu-id="31d0f-279">Electronic</span></span>  
16. <span data-ttu-id="31d0f-280">Lauke Failo vardas, įveskite „Mokėjimai”.</span><span class="sxs-lookup"><span data-stu-id="31d0f-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="31d0f-281">Pvz., įveskite „Mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="31d0f-282">Lauke Banko sąskaita įveskite „GBSI OPER‟.</span><span class="sxs-lookup"><span data-stu-id="31d0f-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="31d0f-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="31d0f-283">GBSI OPER</span></span>  
18. <span data-ttu-id="31d0f-284">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="31d0f-284">Click OK.</span></span>
19. <span data-ttu-id="31d0f-285">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="31d0f-285">Click OK.</span></span>
    * <span data-ttu-id="31d0f-286">Peržiūrėkite sukurtąjį darbalapį – išsamią mokėjimo eilučių informaciją bei kiekvieno šiame mokėjimo pranešime naudojamo valiutos kodo bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="31d0f-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

