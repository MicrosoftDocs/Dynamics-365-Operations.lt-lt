---
title: 'ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis – Formato modifikavimas ir paleidimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de075899547d194fb9eb0e68947efd005c101851
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550699"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="81da8-103">ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis – Formato modifikavimas ir paleidimas)</span><span class="sxs-lookup"><span data-stu-id="81da8-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81da8-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="81da8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="81da8-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="81da8-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="81da8-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis): formato paleidimas“. Formato susiejimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="81da8-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="81da8-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="81da8-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="81da8-108">Keiskite formatą, jei norite priedus įvesti į generuojamus pranešimus dvejetainiu formatu</span><span class="sxs-lookup"><span data-stu-id="81da8-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="81da8-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="81da8-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="81da8-110">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="81da8-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="81da8-111">Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="81da8-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="81da8-112">Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="81da8-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="81da8-113">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="81da8-113">Click Designer.</span></span>
    * <span data-ttu-id="81da8-114">SF pranešimas bus automatiškai įvedamas generuojamoje išvestyje kaip XML failas naudojant UNICODE kodavimą.</span><span class="sxs-lookup"><span data-stu-id="81da8-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="81da8-115">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="81da8-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="81da8-116">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="81da8-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="81da8-117">Lauke Pavadinimas įveskite XML pranešimas.</span><span class="sxs-lookup"><span data-stu-id="81da8-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="81da8-118">XML pranešimas</span><span class="sxs-lookup"><span data-stu-id="81da8-118">Xml message</span></span>  
9. <span data-ttu-id="81da8-119">Lauke „Kodavimas“ įveskite „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="81da8-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="81da8-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="81da8-120">UTF-8</span></span>  
10. <span data-ttu-id="81da8-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81da8-121">Click OK.</span></span>
    * <span data-ttu-id="81da8-122">Sukonfigūruokite generuojamą išvestį kaip suglaudintą failą.</span><span class="sxs-lookup"><span data-stu-id="81da8-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="81da8-123">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="81da8-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="81da8-124">Medyje pasirinkite Bendra / aplankas.</span><span class="sxs-lookup"><span data-stu-id="81da8-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="81da8-125">Lauke Pavadinimas įveskite ZIP išvestis.</span><span class="sxs-lookup"><span data-stu-id="81da8-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="81da8-126">ZIP išvestis</span><span class="sxs-lookup"><span data-stu-id="81da8-126">Zip output</span></span>  
14. <span data-ttu-id="81da8-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81da8-127">Click OK.</span></span>
15. <span data-ttu-id="81da8-128">Medyje pasirinkite ZIP išvestis.</span><span class="sxs-lookup"><span data-stu-id="81da8-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="81da8-129">Pridėkite priedų prie generuojamo suglaudinto failo kaip failus su pradiniais pavadinimais ir plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="81da8-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="81da8-130">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="81da8-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="81da8-131">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="81da8-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="81da8-132">Lauke Pavadinimas įveskite Pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="81da8-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="81da8-133">Pridėtas failas</span><span class="sxs-lookup"><span data-stu-id="81da8-133">Attached file</span></span>  
19. <span data-ttu-id="81da8-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81da8-134">Click OK.</span></span>
20. <span data-ttu-id="81da8-135">Medyje pasirinkite ZIP išvestis / pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="81da8-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="81da8-136">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="81da8-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="81da8-137">Medyje pasirinkite Text\Base64.</span><span class="sxs-lookup"><span data-stu-id="81da8-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="81da8-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81da8-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="81da8-139">Susiekite naujo formato elementus su duomenų modeliu</span><span class="sxs-lookup"><span data-stu-id="81da8-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="81da8-140">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="81da8-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="81da8-141">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="81da8-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="81da8-142">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="81da8-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="81da8-143">Medyje pasirinkite ZIP išvestis / pridėtas failas / Base64.</span><span class="sxs-lookup"><span data-stu-id="81da8-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="81da8-144">Medyje pasirinkite model\Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="81da8-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="81da8-145">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="81da8-145">Click Bind.</span></span>
7. <span data-ttu-id="81da8-146">Medyje pasirinkite ZIP išvestis / pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="81da8-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="81da8-147">Spustelėkite Redaguoti failo vardą.</span><span class="sxs-lookup"><span data-stu-id="81da8-147">Click Edit filename.</span></span>
9. <span data-ttu-id="81da8-148">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="81da8-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="81da8-149">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="81da8-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="81da8-150">Medyje pasirinkite model\Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="81da8-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="81da8-151">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="81da8-151">Click Add data source.</span></span>
13. <span data-ttu-id="81da8-152">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="81da8-152">Click Save.</span></span>
14. <span data-ttu-id="81da8-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="81da8-153">Close the page.</span></span>
15. <span data-ttu-id="81da8-154">Medyje pasirinkite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="81da8-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="81da8-155">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="81da8-155">Click Bind.</span></span>
17. <span data-ttu-id="81da8-156">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="81da8-156">Click Save.</span></span>
18. <span data-ttu-id="81da8-157">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="81da8-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="81da8-158">Paleiskite sukurtą pasirinktos SF ataskaitą</span><span class="sxs-lookup"><span data-stu-id="81da8-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="81da8-159">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="81da8-159">Click Run.</span></span>
2. <span data-ttu-id="81da8-160">Išplėskite dalį Įtrauktini įrašai ().</span><span class="sxs-lookup"><span data-stu-id="81da8-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="81da8-161">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="81da8-161">Click Filter.</span></span>
4. <span data-ttu-id="81da8-162">Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="81da8-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="81da8-163">Lauko Kriterijai kriterijų lauke Pardavimo užsakymas įveskite užsakymo numerį 000148.</span><span class="sxs-lookup"><span data-stu-id="81da8-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="81da8-164">000148</span><span class="sxs-lookup"><span data-stu-id="81da8-164">000148</span></span>  
6. <span data-ttu-id="81da8-165">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81da8-165">Click OK.</span></span>
7. <span data-ttu-id="81da8-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81da8-166">Click OK.</span></span>
    * <span data-ttu-id="81da8-167">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="81da8-167">Review the generated output.</span></span> <span data-ttu-id="81da8-168">Atkreipkite dėmesį, kad be SF pranešimo XML formatu sukuriamas vienas failas kiekvienam priedui.</span><span class="sxs-lookup"><span data-stu-id="81da8-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="81da8-169">Priedų failai yra užpildomi įvedant suglaudintos išvesties duomenis dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="81da8-169">The attachment files are populated with the zipped output in binary format.</span></span>  

