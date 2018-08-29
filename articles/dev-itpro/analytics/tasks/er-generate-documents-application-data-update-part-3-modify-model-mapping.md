--- 
title: "Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys"
description: "Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (2 dalis: generuoti dokumentus)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="3a376-103">Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys</span><span class="sxs-lookup"><span data-stu-id="3a376-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a376-104">Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (2 dalis: generuoti dokumentus)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="3a376-105">Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="3a376-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="3a376-106">Taikydami šią procedūrą modifikuosite ER konfigūracijas, kad jas pradėtumėte naudoti elektroniniams dokumentams generuoti ir programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="3a376-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="3a376-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="3a376-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="3a376-108">Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="3a376-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="3a376-109">Keiskite duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="3a376-109">Modify data model</span></span>
1. <span data-ttu-id="3a376-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="3a376-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3a376-111">Medyje pasirinkite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="3a376-112">Jūs išplėsite, kaip naudojate duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="3a376-112">You will extend how you use the data model.</span></span> <span data-ttu-id="3a376-113">Be jo naudojimo kaip duomenų šaltinio Intrastat ataskaitai generuoti, duomenų modelis bus naudojamas informacijai apie Intrastat ataskaitų teikimo procesą rinkti.</span><span class="sxs-lookup"><span data-stu-id="3a376-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="3a376-114">Informacija paskui bus naudojama programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="3a376-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="3a376-115">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3a376-115">Click Designer.</span></span>
4. <span data-ttu-id="3a376-116">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="3a376-117">Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.</span><span class="sxs-lookup"><span data-stu-id="3a376-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="3a376-118">Lauke Pavadinimas įrašykite „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="3a376-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="3a376-119">Programos duomenų atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="3a376-119">For application data update</span></span>  
7. <span data-ttu-id="3a376-120">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-120">Click Add.</span></span>
8. <span data-ttu-id="3a376-121">Medyje pasirinkite „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="3a376-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="3a376-122">Šis naujas šakninis elementas įtraukiamas, norint nurodyti duomenų srautą duomenims iš Intrastat ataskaitos perkelti (naudojamas kaip duomenų šaltinis) į programos lenteles (atnaujinimo paskirtis).</span><span class="sxs-lookup"><span data-stu-id="3a376-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="3a376-123">Atkreipkite dėmesį, kad skirtingi šakniniai elementai turi būti naudojami, norint gauti duomenis, kurie yra registruojami siunčiamam dokumentui, ir gaunant duomenis iš dokumento, kuris naudojamas norint atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="3a376-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="3a376-124">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="3a376-125">Lauke Pavadinimas įrašykite „Archyvo antraštė“.</span><span class="sxs-lookup"><span data-stu-id="3a376-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="3a376-126">Archyvo antraštė</span><span class="sxs-lookup"><span data-stu-id="3a376-126">Archive header</span></span>  
11. <span data-ttu-id="3a376-127">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="3a376-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="3a376-128">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-128">Click Add.</span></span>
    * <span data-ttu-id="3a376-129">Kadangi jūs kursite kiekvienos sugeneruotos Intrastat ataskaitos įrašą, turite tam sukurti naują elementą.</span><span class="sxs-lookup"><span data-stu-id="3a376-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="3a376-130">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="3a376-131">Lauke Pavadinimas įveskite Failo vardas.</span><span class="sxs-lookup"><span data-stu-id="3a376-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="3a376-132">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="3a376-132">File name</span></span>  
15. <span data-ttu-id="3a376-133">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="3a376-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="3a376-134">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-134">Click Add.</span></span>
17. <span data-ttu-id="3a376-135">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="3a376-136">Lauke „Pavadinimas“ įrašykite „Eilučių skaičius“.</span><span class="sxs-lookup"><span data-stu-id="3a376-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="3a376-137">Eilučių skaičius</span><span class="sxs-lookup"><span data-stu-id="3a376-137">Number of lines</span></span>  
19. <span data-ttu-id="3a376-138">Lauke „Prekės tipas“ pasirinkite „Sveikasis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="3a376-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="3a376-139">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-139">Click Add.</span></span>
    * <span data-ttu-id="3a376-140">Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="3a376-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="3a376-141">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="3a376-142">Lauke Pavadinimas įrašykite „Archyvuoti eilutes“.</span><span class="sxs-lookup"><span data-stu-id="3a376-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="3a376-143">Archyvo eilutės</span><span class="sxs-lookup"><span data-stu-id="3a376-143">Archive lines</span></span>  
23. <span data-ttu-id="3a376-144">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="3a376-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="3a376-145">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-145">Click Add.</span></span>
    * <span data-ttu-id="3a376-146">Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="3a376-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="3a376-147">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="3a376-148">Lauke „Pavadinimas“ įveskite „Suma“.</span><span class="sxs-lookup"><span data-stu-id="3a376-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="3a376-149">Suma</span><span class="sxs-lookup"><span data-stu-id="3a376-149">Amount</span></span>  
27. <span data-ttu-id="3a376-150">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="3a376-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="3a376-151">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-151">Click Add.</span></span>
29. <span data-ttu-id="3a376-152">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="3a376-153">Lauke Pavadinimas įrašykite „Prekės įr. ID“.</span><span class="sxs-lookup"><span data-stu-id="3a376-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="3a376-154">Prekės įr. ID</span><span class="sxs-lookup"><span data-stu-id="3a376-154">Commodity rec id</span></span>  
31. <span data-ttu-id="3a376-155">Lauke „Prekės tipas“ pasirinkite „Int64“.</span><span class="sxs-lookup"><span data-stu-id="3a376-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="3a376-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-156">Click Add.</span></span>
33. <span data-ttu-id="3a376-157">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3a376-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="3a376-158">Lauke „Pavadinimas“ įrašykite „Prekės numeris“.</span><span class="sxs-lookup"><span data-stu-id="3a376-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="3a376-159">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="3a376-159">Item number</span></span>  
35. <span data-ttu-id="3a376-160">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="3a376-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="3a376-161">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-161">Click Add.</span></span>
37. <span data-ttu-id="3a376-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3a376-162">Click Save.</span></span>
38. <span data-ttu-id="3a376-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3a376-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="3a376-164">Keiskite modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="3a376-164">Modify model mapping</span></span>
1. <span data-ttu-id="3a376-165">Medyje išplėskite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="3a376-166">Medyje pasirinkite „Intrastat (model)\Intrastat (mapping)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="3a376-167">Keiskite esamą modelio susiejimą, norėdami pradėti jį naudoti programos duomenų atnaujinimui ir Intrastat ataskaitų teikimo informacijai archyvuoti.</span><span class="sxs-lookup"><span data-stu-id="3a376-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="3a376-168">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3a376-168">Click Designer.</span></span>
4. <span data-ttu-id="3a376-169">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3a376-169">Click New.</span></span>
5. <span data-ttu-id="3a376-170">Lauke Pavadinimas įrašykite „Atnaujinti archyvą“.</span><span class="sxs-lookup"><span data-stu-id="3a376-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="3a376-171">Atnaujinti archyvą</span><span class="sxs-lookup"><span data-stu-id="3a376-171">Update archive</span></span>  
6. <span data-ttu-id="3a376-172">Lauke Kryptis pasirinkite „Į paskirtį“.</span><span class="sxs-lookup"><span data-stu-id="3a376-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="3a376-173">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3a376-173">Click Save.</span></span>
    * <span data-ttu-id="3a376-174">Šis naujas susiejimas nurodo duomenų srautą duomenims perkelti (Intrastat ataskaitų teikimo informacija) į programos lenteles (atnaujinimo paskirtis).</span><span class="sxs-lookup"><span data-stu-id="3a376-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="3a376-175">Atkreipkite dėmesį, kad kitokio modelio šakniniai elementai turi būti naudojami, norint gauti duomenis iš programos ataskaitų teikimo procesui, o tada naudokite duomenis iš duomenų modelio programos duomenų atnaujinimui.</span><span class="sxs-lookup"><span data-stu-id="3a376-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="3a376-176">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3a376-176">Click Designer.</span></span>
9. <span data-ttu-id="3a376-177">Medyje pasirinkite „Data model\Data model“.</span><span class="sxs-lookup"><span data-stu-id="3a376-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="3a376-178">Pridėkite reikiamą duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="3a376-178">Add the required data source.</span></span> <span data-ttu-id="3a376-179">Tai yra duomenų modelis, kuriame yra informacija apie Intrastat operacijas, apie kurias pateikta ataskaita, kurios turi būti archyvuojamos.</span><span class="sxs-lookup"><span data-stu-id="3a376-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="3a376-180">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="3a376-180">Click Add root.</span></span>
11. <span data-ttu-id="3a376-181">Lauke Pavadinimas įrašykite „modelis“.</span><span class="sxs-lookup"><span data-stu-id="3a376-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="3a376-182">modelis</span><span class="sxs-lookup"><span data-stu-id="3a376-182">model</span></span>  
12. <span data-ttu-id="3a376-183">Lauke Apibrėžtis įveskite arba pasirinkite reikšmę „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="3a376-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="3a376-184">Programos duomenų atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="3a376-184">For application data update</span></span>  
13. <span data-ttu-id="3a376-185">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3a376-185">Click OK.</span></span>
14. <span data-ttu-id="3a376-186">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="3a376-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="3a376-187">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="3a376-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="3a376-188">Medyje pasirinkite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="3a376-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="3a376-189">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3a376-189">Click Add.</span></span>
    * <span data-ttu-id="3a376-190">Kadangi norite sunumeruoti Intrastat operacijas, apie kurias pateikta ataskaita, archyvavimui, turi būti pridėtas tinkamas duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="3a376-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="3a376-191">Lauke Pavadinimas įrašykite „Sunumeruotos eilutės“.</span><span class="sxs-lookup"><span data-stu-id="3a376-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="3a376-192">Sunumeruotos eilutės</span><span class="sxs-lookup"><span data-stu-id="3a376-192">Enumerated lines</span></span>  
19. <span data-ttu-id="3a376-193">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="3a376-193">Click Edit formula.</span></span>
20. <span data-ttu-id="3a376-194">Medyje pasirinkite „List\ENUMERATE“.</span><span class="sxs-lookup"><span data-stu-id="3a376-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="3a376-195">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="3a376-195">Click Add function.</span></span>
22. <span data-ttu-id="3a376-196">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="3a376-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="3a376-197">Medyje išplėskite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="3a376-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="3a376-198">Medyje pasirinkite „model\Archive header\Archive lines“.</span><span class="sxs-lookup"><span data-stu-id="3a376-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="3a376-199">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="3a376-199">Click Add data source.</span></span>
26. <span data-ttu-id="3a376-200">Lauke Formulė įveskite „ENUMERATE(model.'Archive header'.'Archive lines')“.</span><span class="sxs-lookup"><span data-stu-id="3a376-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="3a376-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="3a376-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="3a376-202">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3a376-202">Click Save.</span></span>
28. <span data-ttu-id="3a376-203">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3a376-203">Close the page.</span></span>
29. <span data-ttu-id="3a376-204">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3a376-204">Click OK.</span></span>
30. <span data-ttu-id="3a376-205">Spustelėkite Pridėti paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="3a376-205">Click Add destination.</span></span>
    * <span data-ttu-id="3a376-206">Pridėkite programos lentelių kaip privalomų paskirčių, kurias reikia naujinti, norint archyvuoti Intrastat operacijų, apie kurias pateikta ataskaita, informaciją.</span><span class="sxs-lookup"><span data-stu-id="3a376-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="3a376-207">Lauke Pavadinimas įrašykite „Archyvas“.</span><span class="sxs-lookup"><span data-stu-id="3a376-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="3a376-208">Archyvuoti</span><span class="sxs-lookup"><span data-stu-id="3a376-208">Archive</span></span>  
32. <span data-ttu-id="3a376-209">Lauke Lentelės pavadinimas įrašykite „IntrastatArchiveGeneral“.</span><span class="sxs-lookup"><span data-stu-id="3a376-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="3a376-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="3a376-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="3a376-211">Išlaikykite įrašo veiksmą „Įterpti“, kad galėtumėte pridėti įrašų per kiekvieno Intrastat ataskaitų kūrimo proceso informacijos archyvavimą.</span><span class="sxs-lookup"><span data-stu-id="3a376-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="3a376-212">Lauke Įrašo inform. žurnalas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3a376-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="3a376-213">Pasirinkite Taip, kad gautumėte informaciją apie programos duomenų atnaujinimo problemas.</span><span class="sxs-lookup"><span data-stu-id="3a376-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="3a376-214">Lauke Praleisti įrašo veiksmo tikrinimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3a376-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="3a376-215">Pasirinkite Taip, jei norite nerodyti tikrinimo klaidų apie tuščią lauką „Intrastat archyvo ID“.</span><span class="sxs-lookup"><span data-stu-id="3a376-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="3a376-216">Tai bus padaryta pridėjus įrašus, pagal eilės numerio parametrus, kurie konfigūruojami šiai lentelei užsienio prekybos parametrų formoje.</span><span class="sxs-lookup"><span data-stu-id="3a376-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="3a376-217">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3a376-217">Click OK.</span></span>
    * <span data-ttu-id="3a376-218">Susiekite įtraukto duomenų šaltinio elementus (filtruotas modelis, pagrįstas pasirinktu šakniniu elementu) su elementais iš pridėtos paskirties.</span><span class="sxs-lookup"><span data-stu-id="3a376-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="3a376-219">Medyje išplėskite „Archyvas“</span><span class="sxs-lookup"><span data-stu-id="3a376-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="3a376-220">Medyje išplėskite „Archive\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="3a376-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="3a376-221">Medyje išplėskite „Archive\<Relations\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="3a376-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="3a376-222">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="3a376-223">Medyje išplėskite „model\Archive header\Enumerated lines“.</span><span class="sxs-lookup"><span data-stu-id="3a376-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="3a376-224">Medyje išplėskite „model\Archive header\Enumerated lines\Value“.</span><span class="sxs-lookup"><span data-stu-id="3a376-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="3a376-225">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Amount“.</span><span class="sxs-lookup"><span data-stu-id="3a376-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="3a376-226">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-226">Click Bind.</span></span>
44. <span data-ttu-id="3a376-227">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="3a376-228">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Commodity rec id“.</span><span class="sxs-lookup"><span data-stu-id="3a376-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="3a376-229">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-229">Click Bind.</span></span>
47. <span data-ttu-id="3a376-230">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="3a376-231">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Item number“.</span><span class="sxs-lookup"><span data-stu-id="3a376-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="3a376-232">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-232">Click Bind.</span></span>
50. <span data-ttu-id="3a376-233">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="3a376-234">Medyje pasirinkite „model\Archive header\Enumerated lines\Number“.</span><span class="sxs-lookup"><span data-stu-id="3a376-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="3a376-235">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-235">Click Bind.</span></span>
53. <span data-ttu-id="3a376-236">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="3a376-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="3a376-237">Medyje pasirinkite „model\Archive header\Enumerated lines“.</span><span class="sxs-lookup"><span data-stu-id="3a376-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="3a376-238">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-238">Click Bind.</span></span>
56. <span data-ttu-id="3a376-239">Medyje pasirinkite „Archive\File name(FileName)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="3a376-240">Medyje pasirinkite „model\Archive header\File name“.</span><span class="sxs-lookup"><span data-stu-id="3a376-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="3a376-241">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-241">Click Bind.</span></span>
59. <span data-ttu-id="3a376-242">Medyje pasirinkite „Archive\Number of lines(NumberOfLines)“.</span><span class="sxs-lookup"><span data-stu-id="3a376-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="3a376-243">Medyje pasirinkite „model\Archive header\Number of lines“.</span><span class="sxs-lookup"><span data-stu-id="3a376-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="3a376-244">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-244">Click Bind.</span></span>
62. <span data-ttu-id="3a376-245">Medyje pasirinkite „Archive“.</span><span class="sxs-lookup"><span data-stu-id="3a376-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="3a376-246">Medyje pasirinkite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="3a376-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="3a376-247">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3a376-247">Click Bind.</span></span>
65. <span data-ttu-id="3a376-248">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3a376-248">Click Save.</span></span>
66. <span data-ttu-id="3a376-249">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3a376-249">Close the page.</span></span>
67. <span data-ttu-id="3a376-250">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3a376-250">Close the page.</span></span>


