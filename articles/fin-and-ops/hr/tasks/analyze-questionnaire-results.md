---
title: Klausimyno rezultatų analizavimas
description: Klausimyno statistiką galima naudoti skaičiuojant vidurkius, bendrąsias sumas ir procentus, remiantis demografinių duomenų rinkiniu.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a70ea145d8c7134a32e8f0fc6980daca9a010bb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "332753"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="303da-103">Klausimyno rezultatų analizavimas</span><span class="sxs-lookup"><span data-stu-id="303da-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="303da-104">Klausimyno statistiką galima naudoti skaičiuojant vidurkius, bendrąsias sumas ir procentus, remiantis demografinių duomenų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="303da-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="303da-105">Norėdami pradėti šią procedūrą, pasirinkite Klausimynas > Peržiūrėti ir analizuoti rezultatus > Klausimyno statistika.</span><span class="sxs-lookup"><span data-stu-id="303da-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="303da-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="303da-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="303da-107">Sukurti klausimyno statistikos įrašą</span><span class="sxs-lookup"><span data-stu-id="303da-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="303da-108">Eikite į „Klausimyno statistika“.</span><span class="sxs-lookup"><span data-stu-id="303da-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="303da-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="303da-109">Click New.</span></span>
3. <span data-ttu-id="303da-110">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="303da-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="303da-111">Lauke „Statistika“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="303da-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="303da-112">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="303da-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="303da-113">Lauke „Klausimynas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="303da-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="303da-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="303da-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="303da-115">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="303da-115">Click the General tab.</span></span>
    * <span data-ttu-id="303da-116">Pasirinkite, jei norite įtraukti anoniminius rezultatus arba darbuotojų, kontaktinių asmenų ir pretendentų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="303da-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="303da-117">Pažymėkite arba išvalykite žymės langelį „Darbuotojas“.</span><span class="sxs-lookup"><span data-stu-id="303da-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="303da-118">Jei peržiūrėsite rezultatus pagal darbo stažą arba amžių, nurodykite intervalus, kuriuos norėtumėte naudoti rezultatams grupuoti.</span><span class="sxs-lookup"><span data-stu-id="303da-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="303da-119">Į amžiaus intervalą įvedus skaičių 5, rezultatai bus sugrupuoti pagal penkerių metų amžiaus intervalus.</span><span class="sxs-lookup"><span data-stu-id="303da-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="303da-120">Lauke „Amžius“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="303da-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="303da-121">Pasirinkite, jei norite vykdyti skaičiavimą pagal visą klausimyną, kiekvieną rezultatų grupę, kiekvieną klausimą arba kiekvieną klausimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="303da-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="303da-122">Pasirinkite, kaip norėtumėte grupuoti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="303da-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="303da-123">Pvz., jei skaičiuosite vidutinį vieno klausimo taškų skaičių, galite būti patogu matyti klausimus sugrupuotus pagal rezultatų grupę.</span><span class="sxs-lookup"><span data-stu-id="303da-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="303da-124">Pasirinkite duomenis, kuriais bus paremtas skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="303da-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="303da-125">Pvz., jei norite palyginti vidutinį procentą, kurį iš klausimyno gavo jūsų darbuotojai, su vidutiniu jūsų darbuotojų surinktu taškų skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="303da-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="303da-126">Spustelėkite skirtuką „Diapazonas“.</span><span class="sxs-lookup"><span data-stu-id="303da-126">Click the Range tab.</span></span>
    * <span data-ttu-id="303da-127">Naudokite diapazonus, kad apribotumėte savo rezultatų rinkinį tik iki tokių, kurie atitinka diapazono kriterijus.</span><span class="sxs-lookup"><span data-stu-id="303da-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="303da-128">Spustelėkite „Grupuoti pagal skirtuką“.</span><span class="sxs-lookup"><span data-stu-id="303da-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="303da-129">Naudokite grupes, kad nustatytumėte, kaip turėtų būti rodomi rezultatai.</span><span class="sxs-lookup"><span data-stu-id="303da-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="303da-130">Pvz., grupuokite rezultatus pirmiausia pagal lytį, o tada pagal amžių.</span><span class="sxs-lookup"><span data-stu-id="303da-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="303da-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="303da-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="303da-132">Perkelkite grupes į pasirinktą pusę ir išrikiuokite jas norimą tvarka.</span><span class="sxs-lookup"><span data-stu-id="303da-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="303da-133">Vykdyti statistikos skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="303da-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="303da-134">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="303da-134">Click Execute.</span></span>
    * <span data-ttu-id="303da-135">Pasirinkite, kokią rezultatų skaičiavimo funkciją norėtumėte atlikti.</span><span class="sxs-lookup"><span data-stu-id="303da-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="303da-136">Pvz., skaičiuokite pasirinktų grupių iš viso klausimyno gautus vidutinius procentus arba bendrą pasirinktų grupių taškų skaičių visose rezultatų grupėse.</span><span class="sxs-lookup"><span data-stu-id="303da-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="303da-137">Pasirinkite arba išvalykite žymės langelį „Ištrinti ankstesnes paieškas“.</span><span class="sxs-lookup"><span data-stu-id="303da-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="303da-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="303da-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="303da-139">Peržiūrėkite klausimyno statistikos vykdymo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="303da-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="303da-140">Spustelėkite Rezultatas.</span><span class="sxs-lookup"><span data-stu-id="303da-140">Click Result.</span></span>
2. <span data-ttu-id="303da-141">Spustelėkite Rezultatas.</span><span class="sxs-lookup"><span data-stu-id="303da-141">Click Result.</span></span>
3. <span data-ttu-id="303da-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="303da-142">Close the page.</span></span>

