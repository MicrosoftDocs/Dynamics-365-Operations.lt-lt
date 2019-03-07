---
title: Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys
description: 'Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (2 dalis: generuoti dokumentus)“.'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "361940"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="3ceb3-103">Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys</span><span class="sxs-lookup"><span data-stu-id="3ceb3-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ceb3-104">Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (2 dalis: generuoti dokumentus)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="3ceb3-105">Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="3ceb3-106">Taikydami šią procedūrą modifikuosite ER konfigūracijas, kad jas pradėtumėte naudoti elektroniniams dokumentams generuoti ir programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="3ceb3-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="3ceb3-108">Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="3ceb3-109">Keiskite duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="3ceb3-109">Modify data model</span></span>
1. <span data-ttu-id="3ceb3-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3ceb3-111">Medyje pasirinkite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="3ceb3-112">Jūs išplėsite, kaip naudojate duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-112">You will extend how you use the data model.</span></span> <span data-ttu-id="3ceb3-113">Be jo naudojimo kaip duomenų šaltinio Intrastat ataskaitai generuoti, duomenų modelis bus naudojamas informacijai apie Intrastat ataskaitų teikimo procesą rinkti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="3ceb3-114">Informacija paskui bus naudojama programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="3ceb3-115">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-115">Click Designer.</span></span>
4. <span data-ttu-id="3ceb3-116">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="3ceb3-117">Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="3ceb3-118">Lauke Pavadinimas įrašykite „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="3ceb3-119">Programos duomenų atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="3ceb3-119">For application data update</span></span>  
7. <span data-ttu-id="3ceb3-120">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-120">Click Add.</span></span>
8. <span data-ttu-id="3ceb3-121">Medyje pasirinkite „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="3ceb3-122">Šis naujas šakninis elementas įtraukiamas, norint nurodyti duomenų srautą duomenims iš Intrastat ataskaitos perkelti (naudojamas kaip duomenų šaltinis) į programos lenteles (atnaujinimo paskirtis).</span><span class="sxs-lookup"><span data-stu-id="3ceb3-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="3ceb3-123">Atkreipkite dėmesį, kad skirtingi šakniniai elementai turi būti naudojami, norint gauti duomenis, kurie yra registruojami siunčiamam dokumentui, ir gaunant duomenis iš dokumento, kuris naudojamas norint atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="3ceb3-124">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="3ceb3-125">Lauke Pavadinimas įrašykite „Archyvo antraštė“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="3ceb3-126">Archyvo antraštė</span><span class="sxs-lookup"><span data-stu-id="3ceb3-126">Archive header</span></span>  
11. <span data-ttu-id="3ceb3-127">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="3ceb3-128">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-128">Click Add.</span></span>
    * <span data-ttu-id="3ceb3-129">Kadangi jūs kursite kiekvienos sugeneruotos Intrastat ataskaitos įrašą, turite tam sukurti naują elementą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="3ceb3-130">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="3ceb3-131">Lauke Pavadinimas įveskite Failo vardas.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="3ceb3-132">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="3ceb3-132">File name</span></span>  
15. <span data-ttu-id="3ceb3-133">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="3ceb3-134">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-134">Click Add.</span></span>
17. <span data-ttu-id="3ceb3-135">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="3ceb3-136">Lauke „Pavadinimas“ įrašykite „Eilučių skaičius“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="3ceb3-137">Eilučių skaičius</span><span class="sxs-lookup"><span data-stu-id="3ceb3-137">Number of lines</span></span>  
19. <span data-ttu-id="3ceb3-138">Lauke „Prekės tipas“ pasirinkite „Sveikasis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="3ceb3-139">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-139">Click Add.</span></span>
    * <span data-ttu-id="3ceb3-140">Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="3ceb3-141">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="3ceb3-142">Lauke Pavadinimas įrašykite „Archyvuoti eilutes“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="3ceb3-143">Archyvo eilutės</span><span class="sxs-lookup"><span data-stu-id="3ceb3-143">Archive lines</span></span>  
23. <span data-ttu-id="3ceb3-144">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="3ceb3-145">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-145">Click Add.</span></span>
    * <span data-ttu-id="3ceb3-146">Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="3ceb3-147">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="3ceb3-148">Lauke „Pavadinimas“ įveskite „Suma“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="3ceb3-149">Suma</span><span class="sxs-lookup"><span data-stu-id="3ceb3-149">Amount</span></span>  
27. <span data-ttu-id="3ceb3-150">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="3ceb3-151">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-151">Click Add.</span></span>
29. <span data-ttu-id="3ceb3-152">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="3ceb3-153">Lauke Pavadinimas įrašykite „Prekės įr. ID“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="3ceb3-154">Prekės įr. ID</span><span class="sxs-lookup"><span data-stu-id="3ceb3-154">Commodity rec id</span></span>  
31. <span data-ttu-id="3ceb3-155">Lauke „Prekės tipas“ pasirinkite „Int64“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="3ceb3-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-156">Click Add.</span></span>
33. <span data-ttu-id="3ceb3-157">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="3ceb3-158">Lauke „Pavadinimas“ įrašykite „Prekės numeris“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="3ceb3-159">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-159">Item number</span></span>  
35. <span data-ttu-id="3ceb3-160">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="3ceb3-161">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-161">Click Add.</span></span>
37. <span data-ttu-id="3ceb3-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-162">Click Save.</span></span>
38. <span data-ttu-id="3ceb3-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="3ceb3-164">Keiskite modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="3ceb3-164">Modify model mapping</span></span>
1. <span data-ttu-id="3ceb3-165">Medyje išplėskite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="3ceb3-166">Medyje pasirinkite „Intrastat (model)\Intrastat (mapping)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="3ceb3-167">Keiskite esamą modelio susiejimą, norėdami pradėti jį naudoti programos duomenų atnaujinimui ir Intrastat ataskaitų teikimo informacijai archyvuoti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="3ceb3-168">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-168">Click Designer.</span></span>
4. <span data-ttu-id="3ceb3-169">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-169">Click New.</span></span>
5. <span data-ttu-id="3ceb3-170">Lauke Pavadinimas įrašykite „Atnaujinti archyvą“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="3ceb3-171">Atnaujinti archyvą</span><span class="sxs-lookup"><span data-stu-id="3ceb3-171">Update archive</span></span>  
6. <span data-ttu-id="3ceb3-172">Lauke Kryptis pasirinkite „Į paskirtį“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="3ceb3-173">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-173">Click Save.</span></span>
    * <span data-ttu-id="3ceb3-174">Šis naujas susiejimas nurodo duomenų srautą duomenims perkelti (Intrastat ataskaitų teikimo informacija) į programos lenteles (atnaujinimo paskirtis).</span><span class="sxs-lookup"><span data-stu-id="3ceb3-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="3ceb3-175">Atkreipkite dėmesį, kad kitokio modelio šakniniai elementai turi būti naudojami, norint gauti duomenis iš programos ataskaitų teikimo procesui, o tada naudokite duomenis iš duomenų modelio programos duomenų atnaujinimui.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="3ceb3-176">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-176">Click Designer.</span></span>
9. <span data-ttu-id="3ceb3-177">Medyje pasirinkite „Data model\Data model“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="3ceb3-178">Pridėkite reikiamą duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-178">Add the required data source.</span></span> <span data-ttu-id="3ceb3-179">Tai yra duomenų modelis, kuriame yra informacija apie Intrastat operacijas, apie kurias pateikta ataskaita, kurios turi būti archyvuojamos.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="3ceb3-180">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-180">Click Add root.</span></span>
11. <span data-ttu-id="3ceb3-181">Lauke Pavadinimas įrašykite „modelis“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="3ceb3-182">modelis</span><span class="sxs-lookup"><span data-stu-id="3ceb3-182">model</span></span>  
12. <span data-ttu-id="3ceb3-183">Lauke Apibrėžtis įveskite arba pasirinkite reikšmę „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="3ceb3-184">Programos duomenų atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="3ceb3-184">For application data update</span></span>  
13. <span data-ttu-id="3ceb3-185">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-185">Click OK.</span></span>
14. <span data-ttu-id="3ceb3-186">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="3ceb3-187">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="3ceb3-188">Medyje pasirinkite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="3ceb3-189">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-189">Click Add.</span></span>
    * <span data-ttu-id="3ceb3-190">Kadangi norite sunumeruoti Intrastat operacijas, apie kurias pateikta ataskaita, archyvavimui, turi būti pridėtas tinkamas duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="3ceb3-191">Lauke Pavadinimas įrašykite „Sunumeruotos eilutės“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="3ceb3-192">Sunumeruotos eilutės</span><span class="sxs-lookup"><span data-stu-id="3ceb3-192">Enumerated lines</span></span>  
19. <span data-ttu-id="3ceb3-193">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-193">Click Edit formula.</span></span>
20. <span data-ttu-id="3ceb3-194">Medyje pasirinkite „List\ENUMERATE“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="3ceb3-195">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-195">Click Add function.</span></span>
22. <span data-ttu-id="3ceb3-196">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="3ceb3-197">Medyje išplėskite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="3ceb3-198">Medyje pasirinkite „model\Archive header\Archive lines“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="3ceb3-199">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-199">Click Add data source.</span></span>
26. <span data-ttu-id="3ceb3-200">Lauke Formulė įveskite „ENUMERATE(model.'Archive header'.'Archive lines')“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="3ceb3-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="3ceb3-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="3ceb3-202">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-202">Click Save.</span></span>
28. <span data-ttu-id="3ceb3-203">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-203">Close the page.</span></span>
29. <span data-ttu-id="3ceb3-204">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-204">Click OK.</span></span>
30. <span data-ttu-id="3ceb3-205">Spustelėkite Pridėti paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-205">Click Add destination.</span></span>
    * <span data-ttu-id="3ceb3-206">Pridėkite programos lentelių kaip privalomų paskirčių, kurias reikia naujinti, norint archyvuoti Intrastat operacijų, apie kurias pateikta ataskaita, informaciją.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="3ceb3-207">Lauke Pavadinimas įrašykite „Archyvas“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="3ceb3-208">Archyvuoti</span><span class="sxs-lookup"><span data-stu-id="3ceb3-208">Archive</span></span>  
32. <span data-ttu-id="3ceb3-209">Lauke Lentelės pavadinimas įrašykite „IntrastatArchiveGeneral“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="3ceb3-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="3ceb3-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="3ceb3-211">Išlaikykite įrašo veiksmą „Įterpti“, kad galėtumėte pridėti įrašų per kiekvieno Intrastat ataskaitų kūrimo proceso informacijos archyvavimą.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="3ceb3-212">Lauke Įrašo inform. žurnalas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="3ceb3-213">Pasirinkite Taip, kad gautumėte informaciją apie programos duomenų atnaujinimo problemas.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="3ceb3-214">Lauke Praleisti įrašo veiksmo tikrinimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="3ceb3-215">Pasirinkite Taip, jei norite nerodyti tikrinimo klaidų apie tuščią lauką „Intrastat archyvo ID“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="3ceb3-216">Tai bus padaryta pridėjus įrašus, pagal eilės numerio parametrus, kurie konfigūruojami šiai lentelei užsienio prekybos parametrų formoje.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="3ceb3-217">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-217">Click OK.</span></span>
    * <span data-ttu-id="3ceb3-218">Susiekite įtraukto duomenų šaltinio elementus (filtruotas modelis, pagrįstas pasirinktu šakniniu elementu) su elementais iš pridėtos paskirties.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="3ceb3-219">Medyje išplėskite „Archyvas“</span><span class="sxs-lookup"><span data-stu-id="3ceb3-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="3ceb3-220">Medyje išplėskite „Archive\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="3ceb3-221">Medyje išplėskite „Archive\<Relations\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="3ceb3-222">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="3ceb3-223">Medyje išplėskite „model\Archive header\Enumerated lines“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="3ceb3-224">Medyje išplėskite „model\Archive header\Enumerated lines\Value“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="3ceb3-225">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Amount“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="3ceb3-226">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-226">Click Bind.</span></span>
44. <span data-ttu-id="3ceb3-227">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="3ceb3-228">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Commodity rec id“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="3ceb3-229">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-229">Click Bind.</span></span>
47. <span data-ttu-id="3ceb3-230">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="3ceb3-231">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Item number“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="3ceb3-232">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-232">Click Bind.</span></span>
50. <span data-ttu-id="3ceb3-233">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="3ceb3-234">Medyje pasirinkite „model\Archive header\Enumerated lines\Number“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="3ceb3-235">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-235">Click Bind.</span></span>
53. <span data-ttu-id="3ceb3-236">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="3ceb3-237">Medyje pasirinkite „model\Archive header\Enumerated lines“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="3ceb3-238">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-238">Click Bind.</span></span>
56. <span data-ttu-id="3ceb3-239">Medyje pasirinkite „Archive\File name(FileName)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="3ceb3-240">Medyje pasirinkite „model\Archive header\File name“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="3ceb3-241">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-241">Click Bind.</span></span>
59. <span data-ttu-id="3ceb3-242">Medyje pasirinkite „Archive\Number of lines(NumberOfLines)“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="3ceb3-243">Medyje pasirinkite „model\Archive header\Number of lines“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="3ceb3-244">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-244">Click Bind.</span></span>
62. <span data-ttu-id="3ceb3-245">Medyje pasirinkite „Archive“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="3ceb3-246">Medyje pasirinkite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="3ceb3-247">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-247">Click Bind.</span></span>
65. <span data-ttu-id="3ceb3-248">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-248">Click Save.</span></span>
66. <span data-ttu-id="3ceb3-249">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-249">Close the page.</span></span>
67. <span data-ttu-id="3ceb3-250">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3ceb3-250">Close the page.</span></span>

