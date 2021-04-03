---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų peržiūra
description: Šioje temoje aprašoma, kaip kurti elektroninių ataskaitų konfigūraciją, norint generuoti elektroninius dokumentus su įdėtaisiais vaizdais. (1 dalis – Parametrų nustatymas).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6aa5c4d45f9139c65f3aaf1ae392829e3e4967df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569443"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="556cc-104">Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="556cc-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="556cc-105">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus užduočių vedlyje „ER: ataskaitų kūrimas „MS Office“ formatais su įdėtaisiais vaizdais (1 dalis. Parametrų nustatymas)“.</span><span class="sxs-lookup"><span data-stu-id="556cc-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="556cc-106">Ši procedūra parodo, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, norint generuoti elektroninius dokumentus, kuriuose yra įdėtųjų vaizdų „Microsoft Excel“ ir „Microsoft Word“.</span><span class="sxs-lookup"><span data-stu-id="556cc-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="556cc-107">Šiame pavyzdyje peržiūrėsite pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="556cc-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="556cc-108">Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="556cc-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="556cc-109">Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="556cc-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="556cc-110">Peržiūrėkite importuotų duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="556cc-110">Review the imported data model</span></span>
1. <span data-ttu-id="556cc-111">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="556cc-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="556cc-112">Medyje pasirinkite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="556cc-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="556cc-113">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="556cc-113">Click Designer.</span></span>
    * <span data-ttu-id="556cc-114">Šis modelis skirtas nurodyti, kokius mokėjimo čekius naudoja įmonė, ir parodyti šio modelio susiejimą su programos duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="556cc-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="556cc-115">Peržiūrėkite šį modelį naudodami ER operacijų kūrimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="556cc-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="556cc-116">Atkreipkite dėmesį į pateiktus modelio elementų atributus: struktūrą, pavadinimą, aprašymą, duomenų tipą ir t.t.</span><span class="sxs-lookup"><span data-stu-id="556cc-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="556cc-117">Medyje išplėskite „root“.</span><span class="sxs-lookup"><span data-stu-id="556cc-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="556cc-118">Medyje pasirinkite „root\cheques“.</span><span class="sxs-lookup"><span data-stu-id="556cc-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="556cc-119">Medyje išplėskite „root\cheques“.</span><span class="sxs-lookup"><span data-stu-id="556cc-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="556cc-120">Medyje išplėskite „root\cheques\attributes“.</span><span class="sxs-lookup"><span data-stu-id="556cc-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="556cc-121">Medyje išplėskite „root\payer“.</span><span class="sxs-lookup"><span data-stu-id="556cc-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="556cc-122">Medyje pasirinkite „root\istestrun“.</span><span class="sxs-lookup"><span data-stu-id="556cc-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="556cc-123">Medyje pasirinkite „root\layout“.</span><span class="sxs-lookup"><span data-stu-id="556cc-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="556cc-124">Šio modelio išdėstymo elementą sudaro pasirinktos banko sąskaitos čekio formos maketo spausdinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="556cc-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="556cc-125">Taip pat apima du konteinerio duomenų tipo mazgus vaizdams saugoti.</span><span class="sxs-lookup"><span data-stu-id="556cc-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="556cc-126">Medyje išplėskite „root\layout“.</span><span class="sxs-lookup"><span data-stu-id="556cc-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="556cc-127">Medyje pasirinkite „root\layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="556cc-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="556cc-128">Medyje išplėskite „root\layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="556cc-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="556cc-129">Medyje pasirinkite „root\layout\company logo\image“.</span><span class="sxs-lookup"><span data-stu-id="556cc-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="556cc-130">Medyje pasirinkite „root\layout\company logo\isprinted“.</span><span class="sxs-lookup"><span data-stu-id="556cc-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="556cc-131">Medyje pasirinkite „root\layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="556cc-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="556cc-132">Medyje išplėskite „root\layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="556cc-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="556cc-133">Medyje pasirinkite „root\layout\signature\image“.</span><span class="sxs-lookup"><span data-stu-id="556cc-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="556cc-134">Medyje pasirinkite „root\layout\signature\isprinted“.</span><span class="sxs-lookup"><span data-stu-id="556cc-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="556cc-135">Atkreipkite dėmesį, kad du vaizdo duomenų modelio elementai susieti su lentelių laukais, kuriuose yra įmonės logotipas ir įgaliotojo asmens parašas dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="556cc-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="556cc-136">Medyje išplėskite „root\layout\watermark“.</span><span class="sxs-lookup"><span data-stu-id="556cc-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="556cc-137">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="556cc-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="556cc-138">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="556cc-138">Click Designer.</span></span>
23. <span data-ttu-id="556cc-139">Medyje išplėskite „chequesselected“.</span><span class="sxs-lookup"><span data-stu-id="556cc-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="556cc-140">Medyje išplėskite „layout“.</span><span class="sxs-lookup"><span data-stu-id="556cc-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="556cc-141">Medyje išplėskite „layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="556cc-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="556cc-142">Medyje išplėskite „layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="556cc-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="556cc-143">Medyje išplėskite „layout\watermark“.</span><span class="sxs-lookup"><span data-stu-id="556cc-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="556cc-144">Įjunkite „Rodyti išsamią informaciją”.</span><span class="sxs-lookup"><span data-stu-id="556cc-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="556cc-145">Atkreipkite dėmesį, kad čekių duomenų modelio elementas yra susietas su TmpChequePrintout lentele, kurioje vykdant bus čekių įrašai, kuriuos vartotojas pasirinko spausdinti.</span><span class="sxs-lookup"><span data-stu-id="556cc-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="556cc-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="556cc-146">Close the page.</span></span>
30. <span data-ttu-id="556cc-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="556cc-147">Close the page.</span></span>
31. <span data-ttu-id="556cc-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="556cc-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="556cc-149">Peržiūrėkite importuotą formatą</span><span class="sxs-lookup"><span data-stu-id="556cc-149">Review the imported format</span></span>
1. <span data-ttu-id="556cc-150">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="556cc-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="556cc-151">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="556cc-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="556cc-152">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="556cc-152">Click Designer.</span></span>
4. <span data-ttu-id="556cc-153">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="556cc-153">Click Attachments.</span></span>
5. <span data-ttu-id="556cc-154">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="556cc-154">Click Open.</span></span>
    * <span data-ttu-id="556cc-155">Atidarykite pridėtą ataskaitos šabloną „Excel“.</span><span class="sxs-lookup"><span data-stu-id="556cc-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="556cc-156">Peržiūrėkite pridėtos ataskaitos „Excel“ šabloną, kuris bus naudojamas čekiams spausdinti.</span><span class="sxs-lookup"><span data-stu-id="556cc-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="556cc-157">Šablone yra du čekiai puslapyje, jis skirtas čekiams spausdinti iš anksto išspausdintoje formoje.</span><span class="sxs-lookup"><span data-stu-id="556cc-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="556cc-158">Atkreipkite dėmesį, kad yra įdėti du tušti vaizdai.</span><span class="sxs-lookup"><span data-stu-id="556cc-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="556cc-159">Šie tušti vaizdai skirti įmonės logotipui ir parašui asmens, kuris autorizuoja mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="556cc-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="556cc-160">Patikrinkite, ar vaizdai pavadinti CompLogo ir SignatureImage, atitinkamai, „Excel“.</span><span class="sxs-lookup"><span data-stu-id="556cc-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="556cc-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="556cc-161">Close the page.</span></span>
7. <span data-ttu-id="556cc-162">Medyje išplėskite „Report“.</span><span class="sxs-lookup"><span data-stu-id="556cc-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="556cc-163">Medyje išplėskite „Report\ChequeLines“.</span><span class="sxs-lookup"><span data-stu-id="556cc-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="556cc-164">Medyje pasirinkite „Report\ChequeLines\CompLogo“.</span><span class="sxs-lookup"><span data-stu-id="556cc-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="556cc-165">Įjunkite „Rodyti išsamią informaciją”.</span><span class="sxs-lookup"><span data-stu-id="556cc-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="556cc-166">Atkreipkite dėmesį, kad „CompLogo“ formato langelio elementas rodo „Excel“ elementą, naudojamą įmonės logotipo vaizdui įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="556cc-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="556cc-167">Šis formato elementas yra susietas su vaizdo duomenų modelio elementu, vykdant jame yra įmonės logotipo vaizdas dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="556cc-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="556cc-168">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="556cc-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="556cc-169">Spustelėkite Redagavimas įgalintas</span><span class="sxs-lookup"><span data-stu-id="556cc-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="556cc-170">Atkreipkite dėmesį, kad galite nustatyti „CompLogo“ formato langelio elementą taip, kad jis daugiau nebūtų įjungtas.</span><span class="sxs-lookup"><span data-stu-id="556cc-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="556cc-171">Šiuo atveju susietas „Excel“ vaizdo elementas paslėps įmonės logotipą sugeneruotoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="556cc-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="556cc-172">Jei įgalintos išraiškos rezultatas TRUE ir apibrėžtas susiejimas neteikia vaizdo, susietas „Excel“ vaizdo elementas rodys vaizdą, kuris buvo įrašytas „Excel“ šablone.</span><span class="sxs-lookup"><span data-stu-id="556cc-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="556cc-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="556cc-173">Close the page.</span></span>
14. <span data-ttu-id="556cc-174">Medyje išplėskite „labels: Container“.</span><span class="sxs-lookup"><span data-stu-id="556cc-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="556cc-175">Kai kurios etiketės, kurios pateikiamos iš anksto išspausdintoje čekio formoje, bus įtrauktos į ataskaitą, kai ji sukuriama bandymo tikslu.</span><span class="sxs-lookup"><span data-stu-id="556cc-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="556cc-176">Tačiau tos etiketės nebus išspausdintos spausdinant tinkamas etiketes, nes iš anksto išspausdintoje formoje jos jau yra.</span><span class="sxs-lookup"><span data-stu-id="556cc-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="556cc-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="556cc-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]