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
ms.openlocfilehash: ba9cc4dcdfcfbc1bdb933336e85da9b4b6d97a40
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182513"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="72389-103">ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis: formato modifikavimas ir paleidimas)</span><span class="sxs-lookup"><span data-stu-id="72389-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72389-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="72389-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="72389-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="72389-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="72389-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis): formato paleidimas“. Formato susiejimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="72389-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="72389-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="72389-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="72389-108">Keiskite formatą, jei norite priedus įvesti į generuojamus pranešimus dvejetainiu formatu</span><span class="sxs-lookup"><span data-stu-id="72389-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="72389-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="72389-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="72389-110">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="72389-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="72389-111">Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="72389-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="72389-112">Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="72389-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="72389-113">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="72389-113">Click Designer.</span></span>
    * <span data-ttu-id="72389-114">SF pranešimas bus automatiškai įvedamas generuojamoje išvestyje kaip XML failas naudojant UNICODE kodavimą.</span><span class="sxs-lookup"><span data-stu-id="72389-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="72389-115">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="72389-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="72389-116">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="72389-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="72389-117">Lauke Pavadinimas įveskite XML pranešimas.</span><span class="sxs-lookup"><span data-stu-id="72389-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="72389-118">XML pranešimas</span><span class="sxs-lookup"><span data-stu-id="72389-118">Xml message</span></span>  
9. <span data-ttu-id="72389-119">Lauke „Kodavimas“ įveskite „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="72389-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="72389-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="72389-120">UTF-8</span></span>  
10. <span data-ttu-id="72389-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72389-121">Click OK.</span></span>
    * <span data-ttu-id="72389-122">Sukonfigūruokite generuojamą išvestį kaip suglaudintą failą.</span><span class="sxs-lookup"><span data-stu-id="72389-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="72389-123">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="72389-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="72389-124">Medyje pasirinkite Bendra / aplankas.</span><span class="sxs-lookup"><span data-stu-id="72389-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="72389-125">Lauke Pavadinimas įveskite ZIP išvestis.</span><span class="sxs-lookup"><span data-stu-id="72389-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="72389-126">ZIP išvestis</span><span class="sxs-lookup"><span data-stu-id="72389-126">Zip output</span></span>  
14. <span data-ttu-id="72389-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72389-127">Click OK.</span></span>
15. <span data-ttu-id="72389-128">Medyje pasirinkite ZIP išvestis.</span><span class="sxs-lookup"><span data-stu-id="72389-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="72389-129">Pridėkite priedų prie generuojamo suglaudinto failo kaip failus su pradiniais pavadinimais ir plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="72389-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="72389-130">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="72389-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="72389-131">Medyje pasirinkite „Bendra \ Failas“.</span><span class="sxs-lookup"><span data-stu-id="72389-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="72389-132">Lauke Pavadinimas įveskite Pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="72389-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="72389-133">Pridėtas failas</span><span class="sxs-lookup"><span data-stu-id="72389-133">Attached file</span></span>  
19. <span data-ttu-id="72389-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72389-134">Click OK.</span></span>
20. <span data-ttu-id="72389-135">Medyje pasirinkite ZIP išvestis / pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="72389-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="72389-136">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="72389-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="72389-137">Medyje pasirinkite Text\Base64.</span><span class="sxs-lookup"><span data-stu-id="72389-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="72389-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72389-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="72389-139">Susiekite naujo formato elementus su duomenų modeliu</span><span class="sxs-lookup"><span data-stu-id="72389-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="72389-140">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="72389-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="72389-141">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="72389-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="72389-142">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="72389-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="72389-143">Medyje pasirinkite ZIP išvestis / pridėtas failas / Base64.</span><span class="sxs-lookup"><span data-stu-id="72389-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="72389-144">Medyje pasirinkite model\Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="72389-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="72389-145">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="72389-145">Click Bind.</span></span>
7. <span data-ttu-id="72389-146">Medyje pasirinkite ZIP išvestis / pridėtas failas.</span><span class="sxs-lookup"><span data-stu-id="72389-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="72389-147">Spustelėkite Redaguoti failo vardą.</span><span class="sxs-lookup"><span data-stu-id="72389-147">Click Edit filename.</span></span>
9. <span data-ttu-id="72389-148">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="72389-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="72389-149">Medyje išplėskite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="72389-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="72389-150">Medyje pasirinkite model\Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="72389-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="72389-151">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="72389-151">Click Add data source.</span></span>
13. <span data-ttu-id="72389-152">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="72389-152">Click Save.</span></span>
14. <span data-ttu-id="72389-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="72389-153">Close the page.</span></span>
15. <span data-ttu-id="72389-154">Medyje pasirinkite model\Invoice attachments.</span><span class="sxs-lookup"><span data-stu-id="72389-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="72389-155">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="72389-155">Click Bind.</span></span>
17. <span data-ttu-id="72389-156">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="72389-156">Click Save.</span></span>
18. <span data-ttu-id="72389-157">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="72389-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="72389-158">Paleiskite sukurtą pasirinktos SF ataskaitą</span><span class="sxs-lookup"><span data-stu-id="72389-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="72389-159">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="72389-159">Click Run.</span></span>
2. <span data-ttu-id="72389-160">Išplėskite dalį Įtrauktini įrašai ().</span><span class="sxs-lookup"><span data-stu-id="72389-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="72389-161">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="72389-161">Click Filter.</span></span>
4. <span data-ttu-id="72389-162">Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="72389-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="72389-163">Lauko Kriterijai kriterijų lauke Pardavimo užsakymas įveskite užsakymo numerį 000148.</span><span class="sxs-lookup"><span data-stu-id="72389-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="72389-164">000148</span><span class="sxs-lookup"><span data-stu-id="72389-164">000148</span></span>  
6. <span data-ttu-id="72389-165">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72389-165">Click OK.</span></span>
7. <span data-ttu-id="72389-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72389-166">Click OK.</span></span>
    * <span data-ttu-id="72389-167">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="72389-167">Review the generated output.</span></span> <span data-ttu-id="72389-168">Atkreipkite dėmesį, kad be SF pranešimo XML formatu sukuriamas vienas failas kiekvienam priedui.</span><span class="sxs-lookup"><span data-stu-id="72389-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="72389-169">Priedų failai yra užpildomi įvedant suglaudintos išvesties duomenis dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="72389-169">The attachment files are populated with the zipped output in binary format.</span></span>  

