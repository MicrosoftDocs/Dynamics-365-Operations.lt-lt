---
title: Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys
description: Šioje temoje aprašoma, kaip kurti elektroninių ataskaitų konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis. (2 dalis – Dokumentų generavimas).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567097"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="1aa6d-104">Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys</span><span class="sxs-lookup"><span data-stu-id="1aa6d-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1aa6d-105">Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: dokumentų su programos duomenų atnaujinimu generavimas (2 dalis. Dokumentų generavimas)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="1aa6d-106">Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="1aa6d-107">Taikydami šią procedūrą modifikuosite ER konfigūracijas, kad jas pradėtumėte naudoti elektroniniams dokumentams generuoti ir programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="1aa6d-108">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="1aa6d-109">Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="1aa6d-110">Keiskite duomenų modelį</span><span class="sxs-lookup"><span data-stu-id="1aa6d-110">Modify data model</span></span>
1. <span data-ttu-id="1aa6d-111">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1aa6d-112">Medyje pasirinkite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="1aa6d-113">Jūs išplėsite, kaip naudojate duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-113">You will extend how you use the data model.</span></span> <span data-ttu-id="1aa6d-114">Be jo naudojimo kaip duomenų šaltinio Intrastat ataskaitai generuoti, duomenų modelis bus naudojamas informacijai apie Intrastat ataskaitų teikimo procesą rinkti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="1aa6d-115">Informacija paskui bus naudojama programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="1aa6d-116">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-116">Click Designer.</span></span>
4. <span data-ttu-id="1aa6d-117">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="1aa6d-118">Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="1aa6d-119">Lauke Pavadinimas įrašykite „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="1aa6d-120">Programos duomenų atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="1aa6d-120">For application data update</span></span>  
7. <span data-ttu-id="1aa6d-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-121">Click Add.</span></span>
8. <span data-ttu-id="1aa6d-122">Medyje pasirinkite „Programos duomenų atnaujinimui“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="1aa6d-123">Šis naujas šakninis elementas įtraukiamas, norint nurodyti duomenų srautą duomenims iš Intrastat ataskaitos perkelti (naudojamas kaip duomenų šaltinis) į programos lenteles (atnaujinimo paskirtis).</span><span class="sxs-lookup"><span data-stu-id="1aa6d-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="1aa6d-124">Atkreipkite dėmesį, kad skirtingi šakniniai elementai turi būti naudojami, norint gauti duomenis, kurie yra registruojami siunčiamam dokumentui, ir gaunant duomenis iš dokumento, kuris naudojamas norint atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="1aa6d-125">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="1aa6d-126">Lauke Pavadinimas įrašykite „Archyvo antraštė“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="1aa6d-127">Archyvo antraštė</span><span class="sxs-lookup"><span data-stu-id="1aa6d-127">Archive header</span></span>  
11. <span data-ttu-id="1aa6d-128">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="1aa6d-129">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-129">Click Add.</span></span>
    * <span data-ttu-id="1aa6d-130">Kadangi jūs kursite kiekvienos sugeneruotos Intrastat ataskaitos įrašą, turite tam sukurti naują elementą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="1aa6d-131">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="1aa6d-132">Lauke Pavadinimas įveskite Failo vardas.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="1aa6d-133">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="1aa6d-133">File name</span></span>  
15. <span data-ttu-id="1aa6d-134">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="1aa6d-135">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-135">Click Add.</span></span>
17. <span data-ttu-id="1aa6d-136">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="1aa6d-137">Lauke „Pavadinimas“ įrašykite „Eilučių skaičius“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="1aa6d-138">Eilučių skaičius</span><span class="sxs-lookup"><span data-stu-id="1aa6d-138">Number of lines</span></span>  
19. <span data-ttu-id="1aa6d-139">Lauke „Prekės tipas“ pasirinkite „Sveikasis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="1aa6d-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-140">Click Add.</span></span>
    * <span data-ttu-id="1aa6d-141">Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="1aa6d-142">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="1aa6d-143">Lauke Pavadinimas įrašykite „Archyvuoti eilutes“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="1aa6d-144">Archyvo eilutės</span><span class="sxs-lookup"><span data-stu-id="1aa6d-144">Archive lines</span></span>  
23. <span data-ttu-id="1aa6d-145">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="1aa6d-146">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-146">Click Add.</span></span>
    * <span data-ttu-id="1aa6d-147">Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="1aa6d-148">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="1aa6d-149">Lauke „Pavadinimas“ įveskite „Suma“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="1aa6d-150">Suma</span><span class="sxs-lookup"><span data-stu-id="1aa6d-150">Amount</span></span>  
27. <span data-ttu-id="1aa6d-151">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="1aa6d-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-152">Click Add.</span></span>
29. <span data-ttu-id="1aa6d-153">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="1aa6d-154">Lauke Pavadinimas įrašykite „Prekės įr. ID“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="1aa6d-155">Prekės įr. ID</span><span class="sxs-lookup"><span data-stu-id="1aa6d-155">Commodity rec id</span></span>  
31. <span data-ttu-id="1aa6d-156">Lauke „Prekės tipas“ pasirinkite „Int64“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="1aa6d-157">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-157">Click Add.</span></span>
33. <span data-ttu-id="1aa6d-158">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="1aa6d-159">Lauke „Pavadinimas“ įrašykite „Prekės numeris“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="1aa6d-160">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-160">Item number</span></span>  
35. <span data-ttu-id="1aa6d-161">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="1aa6d-162">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-162">Click Add.</span></span>
37. <span data-ttu-id="1aa6d-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-163">Click Save.</span></span>
38. <span data-ttu-id="1aa6d-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="1aa6d-165">Keiskite modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="1aa6d-165">Modify model mapping</span></span>
1. <span data-ttu-id="1aa6d-166">Medyje išplėskite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="1aa6d-167">Medyje pasirinkite „Intrastat (model)\Intrastat (mapping)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="1aa6d-168">Keiskite esamą modelio susiejimą, norėdami pradėti jį naudoti programos duomenų atnaujinimui ir Intrastat ataskaitų teikimo informacijai archyvuoti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="1aa6d-169">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-169">Click Designer.</span></span>
4. <span data-ttu-id="1aa6d-170">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-170">Click New.</span></span>
5. <span data-ttu-id="1aa6d-171">Lauke Pavadinimas įrašykite „Atnaujinti archyvą“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="1aa6d-172">Atnaujinti archyvą</span><span class="sxs-lookup"><span data-stu-id="1aa6d-172">Update archive</span></span>  
6. <span data-ttu-id="1aa6d-173">Lauke Kryptis pasirinkite „Į paskirtį“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="1aa6d-174">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-174">Click Save.</span></span>
    * <span data-ttu-id="1aa6d-175">Šis naujas susiejimas nurodo duomenų srautą duomenims perkelti (Intrastat ataskaitų teikimo informacija) į programos lenteles (atnaujinimo paskirtis).</span><span class="sxs-lookup"><span data-stu-id="1aa6d-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="1aa6d-176">Atkreipkite dėmesį, kad kitokio modelio šakniniai elementai turi būti naudojami, norint gauti duomenis iš programos ataskaitų teikimo procesui, o tada naudokite duomenis iš duomenų modelio programos duomenų atnaujinimui.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="1aa6d-177">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-177">Click Designer.</span></span>
9. <span data-ttu-id="1aa6d-178">Medyje pasirinkite „Data model\Data model“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="1aa6d-179">Pridėkite reikiamą duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-179">Add the required data source.</span></span> <span data-ttu-id="1aa6d-180">Tai yra duomenų modelis, kuriame yra informacija apie Intrastat operacijas, apie kurias pateikta ataskaita, kurios turi būti archyvuojamos.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="1aa6d-181">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-181">Click Add root.</span></span>
11. <span data-ttu-id="1aa6d-182">Lauke Pavadinimas įrašykite „modelis“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="1aa6d-183">modelis</span><span class="sxs-lookup"><span data-stu-id="1aa6d-183">model</span></span>  
12. <span data-ttu-id="1aa6d-184">Lauke Apibrėžtis įveskite arba pasirinkite reikšmę „Programos duomenų naujinimui“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="1aa6d-185">Programos duomenų atnaujinimui</span><span class="sxs-lookup"><span data-stu-id="1aa6d-185">For application data update</span></span>  
13. <span data-ttu-id="1aa6d-186">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-186">Click OK.</span></span>
14. <span data-ttu-id="1aa6d-187">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="1aa6d-188">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="1aa6d-189">Medyje pasirinkite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="1aa6d-190">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-190">Click Add.</span></span>
    * <span data-ttu-id="1aa6d-191">Kadangi norite sunumeruoti Intrastat operacijas, apie kurias pateikta ataskaita, archyvavimui, turi būti pridėtas tinkamas duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="1aa6d-192">Lauke Pavadinimas įrašykite „Sunumeruotos eilutės“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="1aa6d-193">Sunumeruotos eilutės</span><span class="sxs-lookup"><span data-stu-id="1aa6d-193">Enumerated lines</span></span>  
19. <span data-ttu-id="1aa6d-194">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-194">Click Edit formula.</span></span>
20. <span data-ttu-id="1aa6d-195">Medyje pasirinkite „List\ENUMERATE“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="1aa6d-196">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-196">Click Add function.</span></span>
22. <span data-ttu-id="1aa6d-197">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="1aa6d-198">Medyje išplėskite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="1aa6d-199">Medyje pasirinkite „model\Archive header\Archive lines“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="1aa6d-200">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-200">Click Add data source.</span></span>
26. <span data-ttu-id="1aa6d-201">Lauke Formulė įveskite „ENUMERATE(model.'Archive header'.'Archive lines')“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="1aa6d-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="1aa6d-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="1aa6d-203">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-203">Click Save.</span></span>
28. <span data-ttu-id="1aa6d-204">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-204">Close the page.</span></span>
29. <span data-ttu-id="1aa6d-205">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-205">Click OK.</span></span>
30. <span data-ttu-id="1aa6d-206">Spustelėkite Pridėti paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-206">Click Add destination.</span></span>
    * <span data-ttu-id="1aa6d-207">Pridėkite programos lentelių kaip privalomų paskirčių, kurias reikia naujinti, norint archyvuoti Intrastat operacijų, apie kurias pateikta ataskaita, informaciją.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="1aa6d-208">Lauke Pavadinimas įrašykite „Archyvas“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="1aa6d-209">Archyvuoti</span><span class="sxs-lookup"><span data-stu-id="1aa6d-209">Archive</span></span>  
32. <span data-ttu-id="1aa6d-210">Lauke Lentelės pavadinimas įrašykite „IntrastatArchiveGeneral“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="1aa6d-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="1aa6d-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="1aa6d-212">Išlaikykite įrašo veiksmą „Įterpti“, kad galėtumėte pridėti įrašų per kiekvieno „Intrastat“ ataskaitų kūrimo proceso informacijos archyvavimą.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="1aa6d-213">Lauke Įrašo inform. žurnalas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="1aa6d-214">Pasirinkite Taip, kad gautumėte informaciją apie programos duomenų atnaujinimo problemas.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="1aa6d-215">Lauke Praleisti įrašo veiksmo tikrinimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="1aa6d-216">Pasirinkite Taip, jei norite nerodyti tikrinimo klaidų, kad laukas „Intrastat“ archyvo ID“ tuščias.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="1aa6d-217">Tai bus padaryta pridėjus įrašus, pagal eilės numerio parametrus, kurie konfigūruojami šiai lentelei užsienio prekybos parametrų formoje.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="1aa6d-218">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-218">Click OK.</span></span>
    * <span data-ttu-id="1aa6d-219">Susiekite įtraukto duomenų šaltinio elementus (filtruotas modelis, pagrįstas pasirinktu šakniniu elementu) su elementais iš pridėtos paskirties.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="1aa6d-220">Medyje išplėskite „Archyvas“</span><span class="sxs-lookup"><span data-stu-id="1aa6d-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="1aa6d-221">Medyje išplėskite „Archive\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="1aa6d-222">Medyje išplėskite „Archive\<Relations\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="1aa6d-223">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="1aa6d-224">Medyje išplėskite „model\Archive header\Enumerated lines“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="1aa6d-225">Medyje išplėskite „model\Archive header\Enumerated lines\Value“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="1aa6d-226">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Amount“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="1aa6d-227">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-227">Click Bind.</span></span>
44. <span data-ttu-id="1aa6d-228">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="1aa6d-229">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Commodity rec id“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="1aa6d-230">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-230">Click Bind.</span></span>
47. <span data-ttu-id="1aa6d-231">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="1aa6d-232">Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Item number“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="1aa6d-233">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-233">Click Bind.</span></span>
50. <span data-ttu-id="1aa6d-234">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="1aa6d-235">Medyje pasirinkite „model\Archive header\Enumerated lines\Number“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="1aa6d-236">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-236">Click Bind.</span></span>
53. <span data-ttu-id="1aa6d-237">Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="1aa6d-238">Medyje pasirinkite „model\Archive header\Enumerated lines“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="1aa6d-239">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-239">Click Bind.</span></span>
56. <span data-ttu-id="1aa6d-240">Medyje pasirinkite „Archive\File name(FileName)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="1aa6d-241">Medyje pasirinkite „model\Archive header\File name“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="1aa6d-242">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-242">Click Bind.</span></span>
59. <span data-ttu-id="1aa6d-243">Medyje pasirinkite „Archive\Number of lines(NumberOfLines)“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="1aa6d-244">Medyje pasirinkite „model\Archive header\Number of lines“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="1aa6d-245">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-245">Click Bind.</span></span>
62. <span data-ttu-id="1aa6d-246">Medyje pasirinkite „Archive“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="1aa6d-247">Medyje pasirinkite „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="1aa6d-248">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-248">Click Bind.</span></span>
65. <span data-ttu-id="1aa6d-249">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-249">Click Save.</span></span>
66. <span data-ttu-id="1aa6d-250">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-250">Close the page.</span></span>
67. <span data-ttu-id="1aa6d-251">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]