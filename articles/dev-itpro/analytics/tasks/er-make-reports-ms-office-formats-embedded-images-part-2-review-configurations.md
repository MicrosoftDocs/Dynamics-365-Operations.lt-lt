--- 
title: "Ataskaitų kūrimo „Microsoft Office“ formatais su įdėtaisiais vaizdais konfigūracijų peržiūra"
description: "Norėdami atlikti šiuos veiksmus, turite užbaigti veiksmus užduočių vedlyje „ER padaryti ataskaitas „MS Office“ formatais su įdėtaisiais vaizdais (1 dalis: nustatyti parametrus)“."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe58809c60fa27a605d84a61893ff569ded058ef
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images"></a><span data-ttu-id="f4c2a-103">Ataskaitų kūrimo „Microsoft Office“ formatais su įdėtaisiais vaizdais konfigūracijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="f4c2a-103">Review configurations to make reports in Microsoft Office formats with embedded images</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4c2a-104">Norėdami atlikti šiuos veiksmus, turite užbaigti veiksmus užduočių vedlyje „ER padaryti ataskaitas „MS Office“ formatais su įdėtaisiais vaizdais (1 dalis: nustatyti parametrus)“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="f4c2a-105">Ši procedūra parodo, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, norint generuoti elektroninius dokumentus, kuriuose yra įdėtųjų vaizdų „Microsoft Excel“ ir „Microsoft Word“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="f4c2a-106">Šiame pavyzdyje peržiūrėsite pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="f4c2a-107">Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="f4c2a-108">Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="f4c2a-109">Peržiūrėkite importuotų duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="f4c2a-109">Review the imported data model</span></span>
1. <span data-ttu-id="f4c2a-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f4c2a-111">Medyje pasirinkite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="f4c2a-112">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-112">Click Designer.</span></span>
    * <span data-ttu-id="f4c2a-113">Šis modelis skirtas atstovauti mokėjimo čekius verslo požiūriu ir susieti šį modelį su programos duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="f4c2a-114">Peržiūrėkite šį modelį naudodami ER operacijų kūrimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="f4c2a-115">Atkreipkite dėmesį į pateiktus modelio elementų atributus: struktūrą, pavadinimą, aprašymą, duomenų tipą ir t.t.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="f4c2a-116">Medyje išplėskite „root“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="f4c2a-117">Medyje pasirinkite „root\cheques“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="f4c2a-118">Medyje išplėskite „root\cheques“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="f4c2a-119">Medyje išplėskite „root\cheques\attributes“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="f4c2a-120">Medyje išplėskite „root\payer“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="f4c2a-121">Medyje pasirinkite „root\istestrun“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="f4c2a-122">Medyje pasirinkite „root\layout“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="f4c2a-123">Šio modelio išdėstymo elementą sudaro pasirinktos banko sąskaitos čekio formos maketo spausdinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="f4c2a-124">Taip pat apima du konteinerio duomenų tipo mazgus vaizdams saugoti.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="f4c2a-125">Medyje išplėskite „root\layout“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="f4c2a-126">Medyje pasirinkite „root\layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="f4c2a-127">Medyje išplėskite „root\layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="f4c2a-128">Medyje pasirinkite „root\layout\company logo\image“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="f4c2a-129">Medyje pasirinkite „root\layout\company logo\isprinted“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="f4c2a-130">Medyje pasirinkite „root\layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="f4c2a-131">Medyje išplėskite „root\layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="f4c2a-132">Medyje pasirinkite „root\layout\signature\image“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="f4c2a-133">Medyje pasirinkite „root\layout\signature\isprinted“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="f4c2a-134">Atkreipkite dėmesį, kad du vaizdo duomenų modelio elementai susieti su lentelių laukais, kuriuose yra įmonės logotipas ir įgalioto asmens parašas dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="f4c2a-135">Medyje išplėskite „root\layout\watermark“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="f4c2a-136">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="f4c2a-137">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-137">Click Designer.</span></span>
23. <span data-ttu-id="f4c2a-138">Medyje išplėskite „chequesselected“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="f4c2a-139">Medyje išplėskite „layout“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="f4c2a-140">Medyje išplėskite „layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="f4c2a-141">Medyje išplėskite „layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="f4c2a-142">Medyje išplėskite „layout\watermark“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="f4c2a-143">Įjunkite „Rodyti išsamią informaciją”.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="f4c2a-144">Atkreipkite dėmesį, kad čekių duomenų modelio elementas yra susietas su TmpChequePrintout lentele, kurioje vykdant bus čekių įrašai, kuriuos vartotojas pasirinko spausdinti.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="f4c2a-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-145">Close the page.</span></span>
30. <span data-ttu-id="f4c2a-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-146">Close the page.</span></span>
31. <span data-ttu-id="f4c2a-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="f4c2a-148">Peržiūrėkite importuotą formatą</span><span class="sxs-lookup"><span data-stu-id="f4c2a-148">Review the imported format</span></span>
1. <span data-ttu-id="f4c2a-149">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="f4c2a-150">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="f4c2a-151">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-151">Click Designer.</span></span>
4. <span data-ttu-id="f4c2a-152">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-152">Click Attachments.</span></span>
5. <span data-ttu-id="f4c2a-153">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-153">Click Open.</span></span>
    * <span data-ttu-id="f4c2a-154">Atidarykite pridėtą ataskaitos šabloną „Excel“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="f4c2a-155">Peržiūrėkite pridėtos ataskaitos „Excel“ šabloną, kuris bus naudojamas čekiams spausdinti.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="f4c2a-156">Šablone yra du čekiai puslapyje, jis skirtas čekiams spausdinti iš anksto išspausdintoje formoje.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="f4c2a-157">Atkreipkite dėmesį, kad yra įdėti du tušti vaizdai.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="f4c2a-158">Šie tušti vaizdai skirti įmonės logotipui ir parašui asmens, kuris autorizuoja mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="f4c2a-159">Patikrinkite, ar vaizdai pavadinti CompLogo ir SignatureImage, atitinkamai, „Excel“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="f4c2a-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-160">Close the page.</span></span>
7. <span data-ttu-id="f4c2a-161">Medyje išplėskite „Report“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="f4c2a-162">Medyje išplėskite „Report\ChequeLines“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="f4c2a-163">Medyje pasirinkite „Report\ChequeLines\CompLogo“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="f4c2a-164">Įjunkite „Rodyti išsamią informaciją”.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="f4c2a-165">Atkreipkite dėmesį, kad „CompLogo“ formato langelio elementas rodo „Excel“ elementą, naudojamą įmonės logotipo vaizdui įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="f4c2a-166">Šis formato elementas yra susietas su vaizdo duomenų modelio elementu, vykdant jame yra įmonės logotipo vaizdas dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="f4c2a-167">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="f4c2a-168">Spustelėkite Redagavimas įgalintas</span><span class="sxs-lookup"><span data-stu-id="f4c2a-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="f4c2a-169">Atkreipkite dėmesį, kad galite padaryti „CompLogo“ formato langelio elementą, kuris nebeįgalintas.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="f4c2a-170">Šiuo atveju susietas „Excel“ vaizdo elementas paslėps įmonės logotipą sugeneruotoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="f4c2a-171">Jei įgalintos išraiškos rezultatas TRUE ir apibrėžtas susiejimas neteikia vaizdo, susietas „Excel“ vaizdo elementas rodys vaizdą, kuris buvo įrašytas „Excel“ šablone.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="f4c2a-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-172">Close the page.</span></span>
14. <span data-ttu-id="f4c2a-173">Medyje išplėskite „labels: Container“.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="f4c2a-174">Kai kurios etiketės, kurios pateikiamos iš anksto išspausdintoje čekio formoje, bus įtrauktos į ataskaitą, kai sukuriama bandymams.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="f4c2a-175">Tačiau tos etiketės nebus išspausdintos spausdinant iš tikrųjų, nes iš anksto išspausdintoje formoje jos jau yra.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="f4c2a-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4c2a-176">Close the page.</span></span>


