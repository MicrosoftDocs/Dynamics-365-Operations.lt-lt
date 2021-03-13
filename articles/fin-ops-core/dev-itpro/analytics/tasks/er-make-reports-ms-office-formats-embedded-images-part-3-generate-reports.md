---
title: Ataskaitų „Office“ formatu su įdėtaisiais vaizdais generavimas
description: Šioje temoje aprašoma, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, norint generuoti „Excel” ir „Word” elektroninius dokumentus, kuriuose yra įdėtųjų vaizdų.
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
ms.openlocfilehash: 7e15162251e5d6fa91c5a938fd846ef5b5c8cd7f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093828"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="3ffe4-103">Ataskaitų „Office“ formatu su įdėtaisiais vaizdais generavimas</span><span class="sxs-lookup"><span data-stu-id="3ffe4-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ffe4-104">Tolesni veiksmai paaiškina, kaip sistemos administratoriaus arba „Elektroninių ataskaitų kūrėjas“ vaidmenį turintis vartotojas gali sukurti naują elektroninių ataskaitų teikimo (ER) konfigūraciją, skirtą elektroninių dokumentų, turinčių įdėtųjų vaizdų, generavimui „MS office“ formatais („Excel“ ir „Word“).</span><span class="sxs-lookup"><span data-stu-id="3ffe4-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="3ffe4-105">Šiame pavyzdyje naudosite sukurtas kaip pavyzdys pateiktos įmonės „Litware, Inc.“ ER konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="3ffe4-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus užduočių vedlyje „ER: ataskaitų kūrimas „MS Office“ formatais su įdėtaisiais vaizdai (2 dali. Konfigūracijų peržiūra)“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="3ffe4-107">Šiuos veiksmus galima atlikti USMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="3ffe4-108">Paleiskite formatą pradiniu modelio susiejimu</span><span class="sxs-lookup"><span data-stu-id="3ffe4-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="3ffe4-109">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="3ffe4-110">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „USMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="3ffe4-111">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="3ffe4-112">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-112">Click Check.</span></span>
5. <span data-ttu-id="3ffe4-113">Spustelėkite Spausdinti testą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-113">Click Print test.</span></span>
    * <span data-ttu-id="3ffe4-114">Paleiskite formatą bandymams.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="3ffe4-115">Lauke Perduodamo čekio formatas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="3ffe4-116">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-116">Click OK.</span></span>
    * <span data-ttu-id="3ffe4-117">Peržiūrėkite sukurtą išvestį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-117">Review the created output.</span></span> <span data-ttu-id="3ffe4-118">Ataskaitoje yra pateiktas įmonės logotipas ir įgaliotojo asmens parašas.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="3ffe4-119">Parašo vaizdas yra paimtas iš čekio maketo įrašo, kuris susietas su pasirinkta banko sąskaita, duomenų tipo „Konteineris“ lauko.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="3ffe4-120">Išplėskite skyrių Kopijos.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="3ffe4-121">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-121">Click Edit.</span></span>
10. <span data-ttu-id="3ffe4-122">Lauke Vandenženklis įveskite „Spausdinti vandenženklį kaip anuliuotą“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="3ffe4-123">Pakeisti vandenženklio išdėstymo nustatymą, kad būtų rodomas vandenženklio tekstas generuojant dokumentą „Excel“ formos elemente.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="3ffe4-124">Spustelėkite Spausdinti testą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-124">Click Print test.</span></span>
12. <span data-ttu-id="3ffe4-125">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-125">Click OK.</span></span>
    * <span data-ttu-id="3ffe4-126">Peržiūrėkite sukurtą išvestį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-126">Review the created output.</span></span> <span data-ttu-id="3ffe4-127">Vandenženklis rodomas sukurtoje ataskaitoje pagal žymėjimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="3ffe4-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-128">Close the page.</span></span>
14. <span data-ttu-id="3ffe4-129">Veiksmų srityje spustelėkite Valdyti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="3ffe4-130">Spustelėkite Tikrinimai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-130">Click Checks.</span></span>
16. <span data-ttu-id="3ffe4-131">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-131">Click Show filters.</span></span>
17. <span data-ttu-id="3ffe4-132">Taikykite šiuos filtrus: įveskite filtro reikšmę „381“, „385“, „389“ lauke „Čekio numeris“, naudodami filtro operatorių „vienas iš“</span><span class="sxs-lookup"><span data-stu-id="3ffe4-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="3ffe4-133">Sąraše pažymėkite visas eilutes.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="3ffe4-134">Spustelėkite Spausdinti čekio kopiją.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-134">Click Print check copy.</span></span>
    * <span data-ttu-id="3ffe4-135">Paleiskite formatą iš naujo spausdinti pasirinktus čekius.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="3ffe4-136">Peržiūrėkite sukurtą išvestį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-136">Review the created output.</span></span> <span data-ttu-id="3ffe4-137">Turite iš naujo išspausdinti pasirinktus čekius.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="3ffe4-138">Įmonės logotipas ir etiketės nespausdinamos, nes jos pateikiamos iš anksto išspausdintoje formoje.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="3ffe4-139">Pakeiskite importuoto duomenų modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="3ffe4-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="3ffe4-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-140">Close the page.</span></span>
2. <span data-ttu-id="3ffe4-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-141">Close the page.</span></span>
3. <span data-ttu-id="3ffe4-142">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="3ffe4-143">Medyje pasirinkite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="3ffe4-144">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-144">Click Designer.</span></span>
6. <span data-ttu-id="3ffe4-145">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="3ffe4-146">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-146">Click Designer.</span></span>
    * <span data-ttu-id="3ffe4-147">Mes pakeisime duomenų modelio parašo elemento susiejimą, kad gautume parašo vaizdą iš failo, pridėto prie čekio maketo įrašo, susieto su pasirinkta banko sąskaita.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="3ffe4-148">Išjunkite Rodyti išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-148">Turn off Show details.</span></span>
9. <span data-ttu-id="3ffe4-149">Medyje išplėskite „layout“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="3ffe4-150">Medyje išplėskite „layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="3ffe4-151">Medyje pasirinkite „layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="3ffe4-152">Medyje išplėskite „chequesaccount“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="3ffe4-153">Medyje išplėskite „chequesaccount\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="3ffe4-154">Medyje pasirinkite „chequesaccount\<Relations\BankChequeLayout“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="3ffe4-155">Medyje išplėskite „chequesaccount\<Relations\BankChequeLayout\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="3ffe4-156">Medyje išplėskite „chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="3ffe4-157">Medyje pasirinkite „chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="3ffe4-158">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-158">Click Bind.</span></span>
19. <span data-ttu-id="3ffe4-159">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-159">Click Save.</span></span>
20. <span data-ttu-id="3ffe4-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-160">Close the page.</span></span>
21. <span data-ttu-id="3ffe4-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-161">Close the page.</span></span>
22. <span data-ttu-id="3ffe4-162">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-162">Close the page.</span></span>
23. <span data-ttu-id="3ffe4-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="3ffe4-164">Vykdykite formatą, naudodami pakoreguotą modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="3ffe4-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="3ffe4-165">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="3ffe4-166">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3ffe4-167">Pavyzdžiui, filtruokite lauką Banko sąskaita, naudodami reikšmę „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="3ffe4-168">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="3ffe4-169">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-169">Click Check.</span></span>
5. <span data-ttu-id="3ffe4-170">Spustelėkite Spausdinti testą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-170">Click Print test.</span></span>
6. <span data-ttu-id="3ffe4-171">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-171">Click OK.</span></span>
    * <span data-ttu-id="3ffe4-172">Peržiūrėkite sukurtą išvestį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-172">Review the created output.</span></span> <span data-ttu-id="3ffe4-173">Vaizdas iš dokumentų valdymo priedo pateikiamas kaip įgalioto asmens parašas.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="3ffe4-174">Naudokite „MS Word“ dokumentą kaip šabloną importuotame formate</span><span class="sxs-lookup"><span data-stu-id="3ffe4-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="3ffe4-175">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-175">Close the page.</span></span>
2. <span data-ttu-id="3ffe4-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-176">Close the page.</span></span>
3. <span data-ttu-id="3ffe4-177">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="3ffe4-178">Medyje išplėskite „Model for cheques“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="3ffe4-179">Medyje pasirinkite „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="3ffe4-180">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-180">Click Designer.</span></span>
7. <span data-ttu-id="3ffe4-181">Spustelėkite Priedai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-181">Click Attachments.</span></span>
8. <span data-ttu-id="3ffe4-182">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-182">Click Delete.</span></span>
9. <span data-ttu-id="3ffe4-183">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-183">Click Yes.</span></span>
10. <span data-ttu-id="3ffe4-184">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-184">Click New.</span></span>
11. <span data-ttu-id="3ffe4-185">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-185">Click File.</span></span>
    * <span data-ttu-id="3ffe4-186">Spustelėkite Naršyti ir pasirinkite iš anksto atsisiųstą „Cheque template Word.docx" failą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="3ffe4-187">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-187">Close the page.</span></span>
13. <span data-ttu-id="3ffe4-188">Lauke Šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="3ffe4-189">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-189">Click Save.</span></span>
15. <span data-ttu-id="3ffe4-190">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-190">Close the page.</span></span>
16. <span data-ttu-id="3ffe4-191">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-191">Click Edit.</span></span>
17. <span data-ttu-id="3ffe4-192">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="3ffe4-193">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-193">Close the page.</span></span>
19. <span data-ttu-id="3ffe4-194">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="3ffe4-195">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „USMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="3ffe4-196">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-196">Click Check.</span></span>
22. <span data-ttu-id="3ffe4-197">Spustelėkite Spausdinti testą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-197">Click Print test.</span></span>
23. <span data-ttu-id="3ffe4-198">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-198">Click OK.</span></span>
    * <span data-ttu-id="3ffe4-199">Peržiūrėkite sukurtą išvestį.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-199">Review the created output.</span></span> <span data-ttu-id="3ffe4-200">Išvestis sugeneruota kaip „Word“ dokumentas su įdėtaisiais vaizdais, pateikiant įmonės logotipą, įgalioto asmens parašą ir pažymėtą vandenženklio tekstą.</span><span class="sxs-lookup"><span data-stu-id="3ffe4-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

