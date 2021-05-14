---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas
description: Šioje temoje apibūdinama, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, generuojančias elektroninius dokumentus „Excel” ir „Word” formatais, kuriuose yra įdėtųjų vaizdų.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944562"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="a87ef-103">Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="a87ef-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a87ef-104">Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu.“</span><span class="sxs-lookup"><span data-stu-id="a87ef-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="a87ef-105">Šia procedūra paaiškinama, kaip kurti elektroninių ataskaitų (ER) konfigūracijas, norint generuoti „Microsoft Excel“ ar „Word“ dokumentą su įdėtaisiais vaizdais.</span><span class="sxs-lookup"><span data-stu-id="a87ef-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="a87ef-106">Atlikdami šią procedūrą, kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="a87ef-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="a87ef-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a87ef-108">Prieš pradėdami, atsisiųskite ir įrašykite šiuos failus:</span><span class="sxs-lookup"><span data-stu-id="a87ef-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="a87ef-109">Aprašas</span><span class="sxs-lookup"><span data-stu-id="a87ef-109">Description</span></span>                                          | <span data-ttu-id="a87ef-110">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="a87ef-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="a87ef-111">ER duomenų modelio konfigūracija</span><span class="sxs-lookup"><span data-stu-id="a87ef-111">ER data model configuration</span></span>                          | [<span data-ttu-id="a87ef-112">cheques.xml šablonas</span><span class="sxs-lookup"><span data-stu-id="a87ef-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="a87ef-113">ER formato konfigūracija</span><span class="sxs-lookup"><span data-stu-id="a87ef-113">ER format configuration</span></span>                              | [<span data-ttu-id="a87ef-114">Čekių spausdinimas formatas.xml</span><span class="sxs-lookup"><span data-stu-id="a87ef-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="a87ef-115">Įmonės logotipo vaizdas</span><span class="sxs-lookup"><span data-stu-id="a87ef-115">Company logo image</span></span>                                   | [<span data-ttu-id="a87ef-116">Įmonės logo.png</span><span class="sxs-lookup"><span data-stu-id="a87ef-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="a87ef-117">Parašo vaizdas</span><span class="sxs-lookup"><span data-stu-id="a87ef-117">Signature image</span></span>                                      | [<span data-ttu-id="a87ef-118">Parašo vaizdas.png</span><span class="sxs-lookup"><span data-stu-id="a87ef-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="a87ef-119">Alternatyvus parašo vaizdas</span><span class="sxs-lookup"><span data-stu-id="a87ef-119">Alternative signature image</span></span>                          | [<span data-ttu-id="a87ef-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="a87ef-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="a87ef-121">„Microsoft Word“ mokėjimo čekių spausdinimo šablonas</span><span class="sxs-lookup"><span data-stu-id="a87ef-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="a87ef-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="a87ef-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="a87ef-123">Būtinų sąlygų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="a87ef-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="a87ef-124">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="a87ef-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="a87ef-125">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="a87ef-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="a87ef-126">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a87ef-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="a87ef-127">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="a87ef-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="a87ef-128">Įtraukti naują ER modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="a87ef-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="a87ef-129">Užuot kūrę naują modelį, galite įkelti ankščiau įrašytą ER modelio konfigūracijos failą (Model for cheques.xml).</span><span class="sxs-lookup"><span data-stu-id="a87ef-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="a87ef-130">Šiame faile yra mokėjimo čekių duomenų modelio pavyzdys ir duomenų modelio susiejimas su programos „Dynamics 365 for Operations“ duomenų komponentais.</span><span class="sxs-lookup"><span data-stu-id="a87ef-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="a87ef-131">Versijų FastTab spustelėkite Keitimas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="a87ef-132">Spustelėkite Įkelti iš XML failo.</span><span class="sxs-lookup"><span data-stu-id="a87ef-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="a87ef-133">Spustelėkite Naršyti ir pasirinkite Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="a87ef-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="a87ef-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a87ef-134">Click OK.</span></span>  
 6. <span data-ttu-id="a87ef-135">Įkeltas modelis bus naudojamas kaip duomenų informacijos šaltinis kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.</span><span class="sxs-lookup"><span data-stu-id="a87ef-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="a87ef-136">Įtraukite naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="a87ef-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="a87ef-137">Užuot kūrę naują formatą, galite įkelti ankščiau įrašytą ER formato konfigūracijos failą (Cheques printing format.xml).</span><span class="sxs-lookup"><span data-stu-id="a87ef-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="a87ef-138">Šiame faile yra formato maketo, skirto čekių spausdinimui naudojant iš anksto išspausdintą formą, pavyzdys ir šio formato susiejimas su duomenų modeliu „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="a87ef-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="a87ef-139">Spustelėkite Keitimas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="a87ef-140">Spustelėkite Įkelti iš XML failo.</span><span class="sxs-lookup"><span data-stu-id="a87ef-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="a87ef-141">Spustelėkite Naršyti ir pasirinkite failą Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="a87ef-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="a87ef-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a87ef-142">Click OK.</span></span>  
 6. <span data-ttu-id="a87ef-143">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="a87ef-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="a87ef-144">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="a87ef-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="a87ef-145">Įkeltas formatas bus naudojamas kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.</span><span class="sxs-lookup"><span data-stu-id="a87ef-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="a87ef-146">ER naudotojo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a87ef-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="a87ef-147">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="a87ef-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="a87ef-148">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="a87ef-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="a87ef-149">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a87ef-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="a87ef-150">Įjunkite žymę „Paleisti juodraštį“, kad galėtumėte paleisti pasirinkto formato juodraščio versiją, o ne baigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="a87ef-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="a87ef-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a87ef-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="a87ef-152">Modulio Grynųjų pinigų ir banko valdymas parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a87ef-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="a87ef-153">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="a87ef-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="a87ef-154">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „USMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="a87ef-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="a87ef-155">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="a87ef-156">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-156">Click Check.</span></span>  
 5. <span data-ttu-id="a87ef-157">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="a87ef-158">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-158">Click Edit.</span></span>  
 7. <span data-ttu-id="a87ef-159">Lauke Įmonės logotipas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a87ef-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="a87ef-160">Spustelėkite Įmonės logotipas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="a87ef-161">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-161">Click Change.</span></span>  
 10. <span data-ttu-id="a87ef-162">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="a87ef-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="a87ef-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-163">Click Save.</span></span>  
 12. <span data-ttu-id="a87ef-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-164">Close the page.</span></span>  
 13. <span data-ttu-id="a87ef-165">Išplėskite skyrių Parašas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="a87ef-166">Lauke Spausdinti pirmą parašą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a87ef-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="a87ef-167">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-167">Click Change.</span></span>  
 16. <span data-ttu-id="a87ef-168">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="a87ef-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="a87ef-169">Išplėskite skyrių Kopijos.</span><span class="sxs-lookup"><span data-stu-id="a87ef-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="a87ef-170">Lauke Vandenženklis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="a87ef-171">Lauke Bendrasis eksporto elektroniniu būdu formatas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a87ef-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="a87ef-172">Pasirinkite konfigūraciją „Cheques printing form“.</span><span class="sxs-lookup"><span data-stu-id="a87ef-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="a87ef-173">Dabar pasirinktas ER formatas naudojamas spausdinant čekius.</span><span class="sxs-lookup"><span data-stu-id="a87ef-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="a87ef-174">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-174">Click Attach.</span></span>  
 23. <span data-ttu-id="a87ef-175">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-175">Click New.</span></span>  
 24. <span data-ttu-id="a87ef-176">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="a87ef-176">Click File.</span></span>  
 25. <span data-ttu-id="a87ef-177">Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="a87ef-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="a87ef-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-178">Close the page.</span></span>  
 27. <span data-ttu-id="a87ef-179">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-179">Close the page.</span></span>  
 28. <span data-ttu-id="a87ef-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-180">Close the page.</span></span>  
 29. <span data-ttu-id="a87ef-181">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="a87ef-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="a87ef-182">Lauke Leisti kurti išankstinį pranešimą neaktyviuose banko koduose: pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a87ef-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="a87ef-183">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a87ef-183">Click Save.</span></span>  
 32. <span data-ttu-id="a87ef-184">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a87ef-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
