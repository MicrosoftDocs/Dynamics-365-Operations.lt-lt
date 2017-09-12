---
title: "Kelių juridinių subjektų personalo parametrų nustatymas"
description: "Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 90d348f8b8414d6e31092cdd18760375dd283155
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="2b955-104">Kelių juridinių subjektų personalo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b955-104">Set up HR parameters across legal entities</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="2b955-105">Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos.</span><span class="sxs-lookup"><span data-stu-id="2b955-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="2b955-106">Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.</span><span class="sxs-lookup"><span data-stu-id="2b955-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="2b955-107">Kai kurių tipų įrašai, pvz., pareigų įrašai, yra bendrai naudojami keliose įmonėse.</span><span class="sxs-lookup"><span data-stu-id="2b955-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="2b955-108">Šiems įrašams reikia nustatyti bendrai naudojamus parametrus.</span><span class="sxs-lookup"><span data-stu-id="2b955-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="2b955-109">Pavyzdžiui, galite naudoti puslapį **Bendrai naudojami personalo parametrai** kelių juridinių subjektų personalo parametrams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="2b955-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="2b955-110">Puslapyje **Bendrai naudojami personalo parametrai** parametrai sugrupuoti į sritis pagal jų funkcijas.</span><span class="sxs-lookup"><span data-stu-id="2b955-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="2b955-111">Anksčiau išleistos funkcijos</span><span class="sxs-lookup"><span data-stu-id="2b955-111">Previously released functionality</span></span>
<span data-ttu-id="2b955-112">Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje.</span><span class="sxs-lookup"><span data-stu-id="2b955-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="2b955-113">Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="2b955-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="2b955-114">Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**.</span><span class="sxs-lookup"><span data-stu-id="2b955-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="2b955-115">Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalo valdymas** &gt; **skirtuką Saitai** &gt; **Sąranka** &gt; **Identifikavimo tipai**.</span><span class="sxs-lookup"><span data-stu-id="2b955-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="2b955-116">Galite įvesti paprastą kodą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="2b955-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="2b955-117">Jei naudojate „Dynamics 365 for Talent‟</span><span class="sxs-lookup"><span data-stu-id="2b955-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="2b955-118">Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje.</span><span class="sxs-lookup"><span data-stu-id="2b955-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="2b955-119">Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="2b955-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="2b955-120">Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**.</span><span class="sxs-lookup"><span data-stu-id="2b955-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="2b955-121">Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalas** &gt; **Sąranka** &gt; **Identifikavimo tipai**.</span><span class="sxs-lookup"><span data-stu-id="2b955-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="2b955-122">Galite įvesti paprastą kodą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="2b955-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="2b955-123">Skirtuke **Numeracijos** galite pasirinkti numeracijas, naudojamas šiuose įrašuose: darbuotojo numeryje, pareigose, vartotojo užklausos ID, I-9 dokumente, pretendente, diskusijoje, išmokos ID ir personalo veiksme (jei šis įrašo tipas suaktyvintas).</span><span class="sxs-lookup"><span data-stu-id="2b955-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="2b955-124">Norėdami tvarkyti numeravimo nuorodas ir kodus, naudokite sąrašo puslapį **Numeracijos**.</span><span class="sxs-lookup"><span data-stu-id="2b955-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="2b955-125">Norėdami rasti šį puslapį, naudokite puslapio ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="2b955-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="2b955-126">Skirtuke **Pareigos** nurodykite, ar pagal numatytuosius nustatymus naujas pareigas galima priskirti.</span><span class="sxs-lookup"><span data-stu-id="2b955-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="2b955-127">**Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas.</span><span class="sxs-lookup"><span data-stu-id="2b955-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="2b955-128">Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.</span><span class="sxs-lookup"><span data-stu-id="2b955-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="2b955-129">**Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas.</span><span class="sxs-lookup"><span data-stu-id="2b955-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="2b955-130">Pasirinkus šią pasirinktį, reikės atidaryti puslapį **Pareigos** apdorojant kiekvienas naujas pareigas, kai jas bus galima naudoti, ir tada skirtuke **Bendra** įvesti **Galima priskirti** datą , kad būtų suaktyvintas darbuotojo priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="2b955-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="2b955-131">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="2b955-131">See also</span></span>
--------

[<span data-ttu-id="2b955-132">Konkrečios įmonės personalo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b955-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




