---
title: 'ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis – Formato modifikavimas ir paleidimas)'
description: Šioje temoje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų (ER) formatą, kad būtų galima naudoti dokumentų valdymo failus (priedus) ER išvestyje. (5 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f954b76a09bf7c5edd4c608d400318fbd9386778
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749098"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="901ed-104">ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis – Formato modifikavimas ir paleidimas)</span><span class="sxs-lookup"><span data-stu-id="901ed-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="901ed-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="901ed-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="901ed-106">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="901ed-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="901ed-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis. Formato paleidimas)“.</span><span class="sxs-lookup"><span data-stu-id="901ed-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="901ed-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="901ed-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="901ed-109">Keiskite formatą, jei norite priedus įvesti į generuojamus pranešimus dvejetainiu formatu</span><span class="sxs-lookup"><span data-stu-id="901ed-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="901ed-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="901ed-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="901ed-111">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="901ed-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="901ed-112">Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="901ed-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="901ed-113">Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="901ed-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="901ed-114">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="901ed-114">Click Designer.</span></span>
    * <span data-ttu-id="901ed-115">SF pranešimas bus automatiškai įvedamas generuojamoje išvestyje kaip XML failas naudojant UNICODE kodavimą.</span><span class="sxs-lookup"><span data-stu-id="901ed-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="901ed-116">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="901ed-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="901ed-117">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="901ed-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="901ed-118">Lauke Pavadinimas įveskite XML pranešimas.</span><span class="sxs-lookup"><span data-stu-id="901ed-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="901ed-119">XML pranešimas</span><span class="sxs-lookup"><span data-stu-id="901ed-119">Xml message</span></span>  
9. <span data-ttu-id="901ed-120">Lauke „Kodavimas“ įveskite „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="901ed-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="901ed-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="901ed-121">UTF-8</span></span>  
10. <span data-ttu-id="901ed-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="901ed-122">Click OK.</span></span>
    * <span data-ttu-id="901ed-123">Sukonfigūruokite generuojamą išvestį kaip suglaudintą failą.</span><span class="sxs-lookup"><span data-stu-id="901ed-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="901ed-124">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="901ed-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="901ed-125">Medyje pasirinkite Bendra / aplankas.</span><span class="sxs-lookup"><span data-stu-id="901ed-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="901ed-126">Lauke Pavadinimas įveskite ZIP išvestis.</span><span class="sxs-lookup"><span data-stu-id="901ed-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="901ed-127">ZIP išvestis</span><span class="sxs-lookup"><span data-stu-id="901ed-127">Zip output</span></span>  
14. <span data-ttu-id="901ed-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="901ed-128">Click OK.</span></span>
15. <span data-ttu-id="901ed-129">Medyje pasirinkite ZIP išvestis.</span><span class="sxs-lookup"><span data-stu-id="901ed-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="901ed-130">Pridėkite priedų prie generuojamo suglaudinto failo kaip failus su pradiniais pavadinimais ir plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="901ed-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="901ed-131">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="901ed-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="901ed-132">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="901ed-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="901ed-133">Lauke Pavadinimas įveskite Pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="901ed-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="901ed-134">Pridėtas failas</span><span class="sxs-lookup"><span data-stu-id="901ed-134">Attached file</span></span>  
19. <span data-ttu-id="901ed-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="901ed-135">Click OK.</span></span>
20. <span data-ttu-id="901ed-136">Medyje pasirinkite ZIP išvestis / pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="901ed-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="901ed-137">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="901ed-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="901ed-138">Medyje pasirinkite Text\Base64.</span><span class="sxs-lookup"><span data-stu-id="901ed-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="901ed-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="901ed-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="901ed-140">Susiekite naujo formato elementus su duomenų modeliu</span><span class="sxs-lookup"><span data-stu-id="901ed-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="901ed-141">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="901ed-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="901ed-142">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="901ed-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="901ed-143">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="901ed-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="901ed-144">Medyje pasirinkite ZIP išvestis / pridėtas failas / Base64.</span><span class="sxs-lookup"><span data-stu-id="901ed-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="901ed-145">Medyje pasirinkite model\Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="901ed-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="901ed-146">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="901ed-146">Click Bind.</span></span>
7. <span data-ttu-id="901ed-147">Medyje pasirinkite ZIP išvestis / pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="901ed-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="901ed-148">Spustelėkite Redaguoti failo vardą.</span><span class="sxs-lookup"><span data-stu-id="901ed-148">Click Edit filename.</span></span>
9. <span data-ttu-id="901ed-149">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="901ed-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="901ed-150">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="901ed-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="901ed-151">Medyje pasirinkite model\Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="901ed-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="901ed-152">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="901ed-152">Click Add data source.</span></span>
13. <span data-ttu-id="901ed-153">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="901ed-153">Click Save.</span></span>
14. <span data-ttu-id="901ed-154">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="901ed-154">Close the page.</span></span>
15. <span data-ttu-id="901ed-155">Medyje pasirinkite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="901ed-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="901ed-156">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="901ed-156">Click Bind.</span></span>
17. <span data-ttu-id="901ed-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="901ed-157">Click Save.</span></span>
18. <span data-ttu-id="901ed-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="901ed-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="901ed-159">Paleiskite sukurtą pasirinktos SF ataskaitą</span><span class="sxs-lookup"><span data-stu-id="901ed-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="901ed-160">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="901ed-160">Click Run.</span></span>
2. <span data-ttu-id="901ed-161">Išplėskite dalį Įtrauktini įrašai ().</span><span class="sxs-lookup"><span data-stu-id="901ed-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="901ed-162">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="901ed-162">Click Filter.</span></span>
4. <span data-ttu-id="901ed-163">Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="901ed-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="901ed-164">Lauko Kriterijai kriterijų lauke „Pardavimo užsakymas“ įveskite užsakymo numerį 000148.</span><span class="sxs-lookup"><span data-stu-id="901ed-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="901ed-165">000148</span><span class="sxs-lookup"><span data-stu-id="901ed-165">000148</span></span>  
6. <span data-ttu-id="901ed-166">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="901ed-166">Click OK.</span></span>
7. <span data-ttu-id="901ed-167">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="901ed-167">Click OK.</span></span>
    * <span data-ttu-id="901ed-168">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="901ed-168">Review the generated output.</span></span> <span data-ttu-id="901ed-169">Atkreipkite dėmesį, kad be SF pranešimo XML formatu sukuriamas vienas failas kiekvienam priedui.</span><span class="sxs-lookup"><span data-stu-id="901ed-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="901ed-170">Priedų failai yra užpildomi įvedant suglaudintos išvesties duomenis dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="901ed-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]