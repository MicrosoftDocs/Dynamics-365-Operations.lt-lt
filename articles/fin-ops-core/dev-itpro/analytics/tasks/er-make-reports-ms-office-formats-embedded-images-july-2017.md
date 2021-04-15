---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas
description: Šioje temoje apibūdinama, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, generuojančias elektroninius dokumentus „Excel” ir „Word” formatais, kuriuose yra įdėtųjų vaizdų.
author: NickSelin
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1bafc919d73c9e603935398563bb26e8fb277d3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751063"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="4eaa8-103">Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="4eaa8-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4eaa8-104">Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu.“</span><span class="sxs-lookup"><span data-stu-id="4eaa8-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="4eaa8-105">Šia procedūra paaiškinama, kaip kurti elektroninių ataskaitų (ER) konfigūracijas, norint generuoti „Microsoft Excel“ ar „Word“ dokumentą su įdėtaisiais vaizdais.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="4eaa8-106">Atlikdami šią procedūrą, kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="4eaa8-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="4eaa8-108">Prieš pradėdami, atsisiųskite ir įrašykite žinyno temoje nurodytus failus [Įdėtieji vaizdai ir formos dokumentuose, kurie generuojami naudojant ER](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="4eaa8-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="4eaa8-109">Failai: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png ir Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="4eaa8-110">Būtinų sąlygų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="4eaa8-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="4eaa8-111">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="4eaa8-112">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="4eaa8-113">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="4eaa8-114">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="4eaa8-115">Įtraukti naują ER modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="4eaa8-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="4eaa8-116">Užuot kūrę naują modelį, galite įkelti ankščiau įrašytą ER modelio konfigūracijos failą (Model for cheques.xml).</span><span class="sxs-lookup"><span data-stu-id="4eaa8-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="4eaa8-117">Šiame faile yra mokėjimo čekių duomenų modelio pavyzdys ir duomenų modelio susiejimas su programos „Dynamics 365 for Operations“ duomenų komponentais.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="4eaa8-118">Versijų FastTab spustelėkite Keitimas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="4eaa8-119">Spustelėkite Įkelti iš XML failo.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="4eaa8-120">Spustelėkite Naršyti ir pasirinkite Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="4eaa8-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-121">Click OK.</span></span>  
 6. <span data-ttu-id="4eaa8-122">Įkeltas modelis bus naudojamas kaip duomenų informacijos šaltinis kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="4eaa8-123">Įtraukite naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="4eaa8-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="4eaa8-124">Užuot kūrę naują formatą, galite įkelti ankščiau įrašytą ER formato konfigūracijos failą (Cheques printing format.xml).</span><span class="sxs-lookup"><span data-stu-id="4eaa8-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="4eaa8-125">Šiame faile yra formato maketo, skirto čekių spausdinimui naudojant iš anksto išspausdintą formą, pavyzdys ir šio formato susiejimas su duomenų modeliu „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="4eaa8-126">Spustelėkite Keitimas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="4eaa8-127">Spustelėkite Įkelti iš XML failo.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="4eaa8-128">Spustelėkite Naršyti ir pasirinkite failą Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="4eaa8-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-129">Click OK.</span></span>  
 6. <span data-ttu-id="4eaa8-130">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="4eaa8-131">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="4eaa8-132">Įkeltas formatas bus naudojamas kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="4eaa8-133">ER naudotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="4eaa8-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="4eaa8-134">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="4eaa8-135">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="4eaa8-136">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="4eaa8-137">Įjunkite žymę „Paleisti juodraštį“, kad galėtumėte paleisti pasirinkto formato juodraščio versiją, o ne baigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="4eaa8-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="4eaa8-139">Modulio Grynųjų pinigų ir banko valdymas parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="4eaa8-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="4eaa8-140">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="4eaa8-141">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „USMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="4eaa8-142">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="4eaa8-143">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-143">Click Check.</span></span>  
 5. <span data-ttu-id="4eaa8-144">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="4eaa8-145">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-145">Click Edit.</span></span>  
 7. <span data-ttu-id="4eaa8-146">Lauke Įmonės logotipas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="4eaa8-147">Spustelėkite Įmonės logotipas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="4eaa8-148">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-148">Click Change.</span></span>  
 10. <span data-ttu-id="4eaa8-149">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="4eaa8-150">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-150">Click Save.</span></span>  
 12. <span data-ttu-id="4eaa8-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-151">Close the page.</span></span>  
 13. <span data-ttu-id="4eaa8-152">Išplėskite skyrių Parašas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="4eaa8-153">Lauke Spausdinti pirmą parašą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="4eaa8-154">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-154">Click Change.</span></span>  
 16. <span data-ttu-id="4eaa8-155">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="4eaa8-156">Išplėskite skyrių Kopijos.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="4eaa8-157">Lauke Vandenženklis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="4eaa8-158">Lauke Bendrasis eksporto elektroniniu būdu formatas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="4eaa8-159">Pasirinkite konfigūraciją „Cheques printing form“.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="4eaa8-160">Dabar pasirinktas ER formatas naudojamas spausdinant čekius.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="4eaa8-161">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-161">Click Attach.</span></span>  
 23. <span data-ttu-id="4eaa8-162">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-162">Click New.</span></span>  
 24. <span data-ttu-id="4eaa8-163">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-163">Click File.</span></span>  
 25. <span data-ttu-id="4eaa8-164">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="4eaa8-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-165">Close the page.</span></span>  
 27. <span data-ttu-id="4eaa8-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-166">Close the page.</span></span>  
 28. <span data-ttu-id="4eaa8-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-167">Close the page.</span></span>  
 29. <span data-ttu-id="4eaa8-168">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="4eaa8-169">Lauke Leisti kurti išankstinį pranešimą neaktyviuose banko koduose: pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="4eaa8-170">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-170">Click Save.</span></span>  
 32. <span data-ttu-id="4eaa8-171">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4eaa8-171">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]