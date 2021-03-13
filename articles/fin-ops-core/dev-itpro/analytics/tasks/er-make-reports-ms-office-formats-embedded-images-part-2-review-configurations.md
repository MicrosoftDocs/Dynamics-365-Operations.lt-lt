---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų peržiūra
description: Šioje temoje aprašoma, kaip kurti elektroninių ataskaitų konfigūraciją, norint generuoti elektroninius dokumentus su įdėtaisiais vaizdais. (1 dalis – Parametrų nustatymas).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eee6300350dd96c34f2eab44704d1895e6171ff
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093650"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="58b22-104">Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="58b22-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58b22-105">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus užduočių vedlyje „ER: ataskaitų kūrimas „MS Office“ formatais su įdėtaisiais vaizdais (1 dalis. Parametrų nustatymas)“.</span><span class="sxs-lookup"><span data-stu-id="58b22-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="58b22-106">Ši procedūra parodo, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, norint generuoti elektroninius dokumentus, kuriuose yra įdėtųjų vaizdų „Microsoft Excel“ ir „Microsoft Word“.</span><span class="sxs-lookup"><span data-stu-id="58b22-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="58b22-107">Šiame pavyzdyje peržiūrėsite pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="58b22-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="58b22-108">Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="58b22-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="58b22-109">Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="58b22-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="58b22-110">Peržiūrėkite importuotų duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="58b22-110">Review the imported data model</span></span>
1. <span data-ttu-id="58b22-111">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="58b22-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="58b22-112">Medyje pasirinkite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="58b22-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="58b22-113">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="58b22-113">Click Designer.</span></span>
    * <span data-ttu-id="58b22-114">Šis modelis skirtas nurodyti, kokius mokėjimo čekius naudoja įmonė, ir parodyti šio modelio susiejimą su programos duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="58b22-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="58b22-115">Peržiūrėkite šį modelį naudodami ER operacijų kūrimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="58b22-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="58b22-116">Atkreipkite dėmesį į pateiktus modelio elementų atributus: struktūrą, pavadinimą, aprašymą, duomenų tipą ir t.t.</span><span class="sxs-lookup"><span data-stu-id="58b22-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="58b22-117">Medyje išplėskite „root“.</span><span class="sxs-lookup"><span data-stu-id="58b22-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="58b22-118">Medyje pasirinkite „root\cheques“.</span><span class="sxs-lookup"><span data-stu-id="58b22-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="58b22-119">Medyje išplėskite „root\cheques“.</span><span class="sxs-lookup"><span data-stu-id="58b22-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="58b22-120">Medyje išplėskite „root\cheques\attributes“.</span><span class="sxs-lookup"><span data-stu-id="58b22-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="58b22-121">Medyje išplėskite „root\payer“.</span><span class="sxs-lookup"><span data-stu-id="58b22-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="58b22-122">Medyje pasirinkite „root\istestrun“.</span><span class="sxs-lookup"><span data-stu-id="58b22-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="58b22-123">Medyje pasirinkite „root\layout“.</span><span class="sxs-lookup"><span data-stu-id="58b22-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="58b22-124">Šio modelio išdėstymo elementą sudaro pasirinktos banko sąskaitos čekio formos maketo spausdinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="58b22-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="58b22-125">Taip pat apima du konteinerio duomenų tipo mazgus vaizdams saugoti.</span><span class="sxs-lookup"><span data-stu-id="58b22-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="58b22-126">Medyje išplėskite „root\layout“.</span><span class="sxs-lookup"><span data-stu-id="58b22-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="58b22-127">Medyje pasirinkite „root\layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="58b22-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="58b22-128">Medyje išplėskite „root\layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="58b22-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="58b22-129">Medyje pasirinkite „root\layout\company logo\image“.</span><span class="sxs-lookup"><span data-stu-id="58b22-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="58b22-130">Medyje pasirinkite „root\layout\company logo\isprinted“.</span><span class="sxs-lookup"><span data-stu-id="58b22-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="58b22-131">Medyje pasirinkite „root\layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="58b22-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="58b22-132">Medyje išplėskite „root\layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="58b22-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="58b22-133">Medyje pasirinkite „root\layout\signature\image“.</span><span class="sxs-lookup"><span data-stu-id="58b22-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="58b22-134">Medyje pasirinkite „root\layout\signature\isprinted“.</span><span class="sxs-lookup"><span data-stu-id="58b22-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="58b22-135">Atkreipkite dėmesį, kad du vaizdo duomenų modelio elementai susieti su lentelių laukais, kuriuose yra įmonės logotipas ir įgaliotojo asmens parašas dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="58b22-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="58b22-136">Medyje išplėskite „root\layout\watermark“.</span><span class="sxs-lookup"><span data-stu-id="58b22-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="58b22-137">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="58b22-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="58b22-138">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="58b22-138">Click Designer.</span></span>
23. <span data-ttu-id="58b22-139">Medyje išplėskite „chequesselected“.</span><span class="sxs-lookup"><span data-stu-id="58b22-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="58b22-140">Medyje išplėskite „layout“.</span><span class="sxs-lookup"><span data-stu-id="58b22-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="58b22-141">Medyje išplėskite „layout\company logo“.</span><span class="sxs-lookup"><span data-stu-id="58b22-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="58b22-142">Medyje išplėskite „layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="58b22-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="58b22-143">Medyje išplėskite „layout\watermark“.</span><span class="sxs-lookup"><span data-stu-id="58b22-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="58b22-144">Įjunkite „Rodyti išsamią informaciją”.</span><span class="sxs-lookup"><span data-stu-id="58b22-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="58b22-145">Atkreipkite dėmesį, kad čekių duomenų modelio elementas yra susietas su TmpChequePrintout lentele, kurioje vykdant bus čekių įrašai, kuriuos vartotojas pasirinko spausdinti.</span><span class="sxs-lookup"><span data-stu-id="58b22-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="58b22-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58b22-146">Close the page.</span></span>
30. <span data-ttu-id="58b22-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58b22-147">Close the page.</span></span>
31. <span data-ttu-id="58b22-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58b22-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="58b22-149">Peržiūrėkite importuotą formatą</span><span class="sxs-lookup"><span data-stu-id="58b22-149">Review the imported format</span></span>
1. <span data-ttu-id="58b22-150">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="58b22-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="58b22-151">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="58b22-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="58b22-152">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="58b22-152">Click Designer.</span></span>
4. <span data-ttu-id="58b22-153">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="58b22-153">Click Attachments.</span></span>
5. <span data-ttu-id="58b22-154">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="58b22-154">Click Open.</span></span>
    * <span data-ttu-id="58b22-155">Atidarykite pridėtą ataskaitos šabloną „Excel“.</span><span class="sxs-lookup"><span data-stu-id="58b22-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="58b22-156">Peržiūrėkite pridėtos ataskaitos „Excel“ šabloną, kuris bus naudojamas čekiams spausdinti.</span><span class="sxs-lookup"><span data-stu-id="58b22-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="58b22-157">Šablone yra du čekiai puslapyje, jis skirtas čekiams spausdinti iš anksto išspausdintoje formoje.</span><span class="sxs-lookup"><span data-stu-id="58b22-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="58b22-158">Atkreipkite dėmesį, kad yra įdėti du tušti vaizdai.</span><span class="sxs-lookup"><span data-stu-id="58b22-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="58b22-159">Šie tušti vaizdai skirti įmonės logotipui ir parašui asmens, kuris autorizuoja mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="58b22-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="58b22-160">Patikrinkite, ar vaizdai pavadinti CompLogo ir SignatureImage, atitinkamai, „Excel“.</span><span class="sxs-lookup"><span data-stu-id="58b22-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="58b22-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58b22-161">Close the page.</span></span>
7. <span data-ttu-id="58b22-162">Medyje išplėskite „Report“.</span><span class="sxs-lookup"><span data-stu-id="58b22-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="58b22-163">Medyje išplėskite „Report\ChequeLines“.</span><span class="sxs-lookup"><span data-stu-id="58b22-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="58b22-164">Medyje pasirinkite „Report\ChequeLines\CompLogo“.</span><span class="sxs-lookup"><span data-stu-id="58b22-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="58b22-165">Įjunkite „Rodyti išsamią informaciją”.</span><span class="sxs-lookup"><span data-stu-id="58b22-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="58b22-166">Atkreipkite dėmesį, kad „CompLogo“ formato langelio elementas rodo „Excel“ elementą, naudojamą įmonės logotipo vaizdui įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="58b22-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="58b22-167">Šis formato elementas yra susietas su vaizdo duomenų modelio elementu, vykdant jame yra įmonės logotipo vaizdas dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="58b22-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="58b22-168">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="58b22-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="58b22-169">Spustelėkite Redagavimas įgalintas</span><span class="sxs-lookup"><span data-stu-id="58b22-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="58b22-170">Atkreipkite dėmesį, kad galite nustatyti „CompLogo“ formato langelio elementą taip, kad jis daugiau nebūtų įjungtas.</span><span class="sxs-lookup"><span data-stu-id="58b22-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="58b22-171">Šiuo atveju susietas „Excel“ vaizdo elementas paslėps įmonės logotipą sugeneruotoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="58b22-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="58b22-172">Jei įgalintos išraiškos rezultatas TRUE ir apibrėžtas susiejimas neteikia vaizdo, susietas „Excel“ vaizdo elementas rodys vaizdą, kuris buvo įrašytas „Excel“ šablone.</span><span class="sxs-lookup"><span data-stu-id="58b22-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="58b22-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58b22-173">Close the page.</span></span>
14. <span data-ttu-id="58b22-174">Medyje išplėskite „labels: Container“.</span><span class="sxs-lookup"><span data-stu-id="58b22-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="58b22-175">Kai kurios etiketės, kurios pateikiamos iš anksto išspausdintoje čekio formoje, bus įtrauktos į ataskaitą, kai ji sukuriama bandymo tikslu.</span><span class="sxs-lookup"><span data-stu-id="58b22-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="58b22-176">Tačiau tos etiketės nebus išspausdintos spausdinant tinkamas etiketes, nes iš anksto išspausdintoje formoje jos jau yra.</span><span class="sxs-lookup"><span data-stu-id="58b22-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="58b22-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58b22-177">Close the page.</span></span>

