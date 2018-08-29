--- 
title: "Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas"
description: "Šios temos veiksmuose pateikiama informacijos apie tai, kaip kurti elektroninių ataskaitų (ER) konfigūracijas, generuojančias „Microsoft Office“ formatų („Excel“ ir „Word“) elektroninius dokumentus, kuriuose yra įdėtųjų vaizdų."
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="54de4-103">Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="54de4-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54de4-104">Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu.“</span><span class="sxs-lookup"><span data-stu-id="54de4-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="54de4-105">Šia procedūra paaiškinama, kaip kurti elektroninių ataskaitų (ER) konfigūracijas, norint generuoti „Microsoft Excel“ ar „Word“ dokumentą su įdėtaisiais vaizdais.</span><span class="sxs-lookup"><span data-stu-id="54de4-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="54de4-106">Atlikdami šią procedūrą, kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="54de4-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="54de4-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="54de4-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="54de4-108">Prieš pradėdami, atsisiųskite ir įrašykite failus, išvardytus žinyno temoje [Vaizdų ir figūrų įdėjimas į verslo dokumentus, sugeneruotus naudojant elektroninių ataskaitų įrankį](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="54de4-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="54de4-109">Failai: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png ir Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="54de4-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="54de4-110">Būtinų sąlygų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="54de4-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="54de4-111">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="54de4-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="54de4-112">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="54de4-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="54de4-113">Jei nematote šio konfigūracijų teikėjo, atlikite procedūros „Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="54de4-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="54de4-114">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="54de4-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="54de4-115">Įtraukti naują ER modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="54de4-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="54de4-116">Užuot kūrę naują modelį, galite įkelti ankščiau įrašytą ER modelio konfigūracijos failą (Model for cheques.xml).</span><span class="sxs-lookup"><span data-stu-id="54de4-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="54de4-117">Šiame faile yra mokėjimo čekių duomenų modelio pavyzdys ir duomenų modelio susiejimas su programos „Dynamics 365 for Operations“ duomenų komponentais.</span><span class="sxs-lookup"><span data-stu-id="54de4-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="54de4-118">Versijų FastTab spustelėkite Keitimas.</span><span class="sxs-lookup"><span data-stu-id="54de4-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="54de4-119">Spustelėkite Įkelti iš XML failo.</span><span class="sxs-lookup"><span data-stu-id="54de4-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="54de4-120">Spustelėkite Naršyti ir pasirinkite Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="54de4-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="54de4-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54de4-121">Click OK.</span></span>  
 6. <span data-ttu-id="54de4-122">Įkeltas modelis bus naudojamas kaip duomenų informacijos šaltinis kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.</span><span class="sxs-lookup"><span data-stu-id="54de4-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="54de4-123">Įtraukite naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="54de4-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="54de4-124">Užuot kūrę naują formatą, galite įkelti ankščiau įrašytą ER formato konfigūracijos failą (Cheques printing format.xml).</span><span class="sxs-lookup"><span data-stu-id="54de4-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="54de4-125">Šiame faile yra formato maketo pavyzdys, kai čekiai spausdinami naudojant iš anksto išspausdintą formą, ir šio formato susiejimas su duomenų modeliu „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="54de4-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="54de4-126">Spustelėkite Keitimas.</span><span class="sxs-lookup"><span data-stu-id="54de4-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="54de4-127">Spustelėkite Įkelti iš XML failo.</span><span class="sxs-lookup"><span data-stu-id="54de4-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="54de4-128">Spustelėkite Naršyti ir pasirinkite failą Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="54de4-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="54de4-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54de4-129">Click OK.</span></span>  
 6. <span data-ttu-id="54de4-130">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="54de4-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="54de4-131">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="54de4-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="54de4-132">Įkeltas formatas bus naudojamas kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.</span><span class="sxs-lookup"><span data-stu-id="54de4-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="54de4-133">ER naudotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="54de4-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="54de4-134">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="54de4-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="54de4-135">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="54de4-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="54de4-136">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54de4-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="54de4-137">Įjunkite žymę „Paleisti juodraštį“, kad galėtumėte paleisti pasirinkto formato juodraščio versiją, o ne baigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="54de4-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="54de4-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="54de4-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="54de4-139">Modulio Grynųjų pinigų ir banko valdymas parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="54de4-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="54de4-140">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="54de4-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="54de4-141">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „USMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="54de4-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="54de4-142">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="54de4-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="54de4-143">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="54de4-143">Click Check.</span></span>  
 5. <span data-ttu-id="54de4-144">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="54de4-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="54de4-145">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="54de4-145">Click Edit.</span></span>  
 7. <span data-ttu-id="54de4-146">Lauke Įmonės logotipas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54de4-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="54de4-147">Spustelėkite Įmonės logotipas.</span><span class="sxs-lookup"><span data-stu-id="54de4-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="54de4-148">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="54de4-148">Click Change.</span></span>  
 10. <span data-ttu-id="54de4-149">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="54de4-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="54de4-150">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54de4-150">Click Save.</span></span>  
 12. <span data-ttu-id="54de4-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54de4-151">Close the page.</span></span>  
 13. <span data-ttu-id="54de4-152">Išplėskite skyrių Parašas.</span><span class="sxs-lookup"><span data-stu-id="54de4-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="54de4-153">Lauke Spausdinti pirmą parašą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54de4-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="54de4-154">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="54de4-154">Click Change.</span></span>  
 16. <span data-ttu-id="54de4-155">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="54de4-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="54de4-156">Išplėskite skyrių Kopijos.</span><span class="sxs-lookup"><span data-stu-id="54de4-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="54de4-157">Lauke Vandenženklis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="54de4-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="54de4-158">Lauke Bendrasis eksporto elektroniniu būdu formatas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54de4-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="54de4-159">Pasirinkite konfigūraciją „Cheques printing form“.</span><span class="sxs-lookup"><span data-stu-id="54de4-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="54de4-160">Dabar pasirinktas ER formatas naudojamas spausdinant čekius.</span><span class="sxs-lookup"><span data-stu-id="54de4-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="54de4-161">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="54de4-161">Click Attach.</span></span>  
 23. <span data-ttu-id="54de4-162">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="54de4-162">Click New.</span></span>  
 24. <span data-ttu-id="54de4-163">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="54de4-163">Click File.</span></span>  
 25. <span data-ttu-id="54de4-164">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="54de4-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="54de4-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54de4-165">Close the page.</span></span>  
 27. <span data-ttu-id="54de4-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54de4-166">Close the page.</span></span>  
 28. <span data-ttu-id="54de4-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54de4-167">Close the page.</span></span>  
 29. <span data-ttu-id="54de4-168">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="54de4-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="54de4-169">Lauke Leisti kurti išankstinį pranešimą neaktyviuose banko koduose: pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="54de4-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="54de4-170">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="54de4-170">Click Save.</span></span>  
 32. <span data-ttu-id="54de4-171">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="54de4-171">Close the page.</span></span>  

