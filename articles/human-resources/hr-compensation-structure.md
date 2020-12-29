---
title: Kompensacijos struktūros kūrimas
description: Šiame straipsnyje apžvelgiama, kaip kurti pastoviosios kompensacijos planą ir į jį užregistruoti darbuotojus taikant tinkamumo taisykles.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419748"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="2db76-103">Kompensacijos struktūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="2db76-103">Develop a compensation structure</span></span>

<span data-ttu-id="2db76-104">Šiame straipsnyje apžvelgiama, kaip kurti pastoviosios kompensacijos planą ir į jį užregistruoti darbuotojus taikant tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="2db76-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="2db76-105">Šiame straipsnyje naudojami USMF demonstraciniai duomenys ir jis skirtas kompensacijų bei išmokų vadovams.</span><span class="sxs-lookup"><span data-stu-id="2db76-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="2db76-106">Pastoviosios atlyginimo dalies plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="2db76-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="2db76-107">Pasirinkite **Kompensacijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="2db76-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="2db76-108">Pasirinkite **Pastoviosios kompensacijos planai**.</span><span class="sxs-lookup"><span data-stu-id="2db76-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="2db76-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2db76-109">Select **New**.</span></span>

4. <span data-ttu-id="2db76-110">Lauke **Planas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="2db76-111">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="2db76-112">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="2db76-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="2db76-113">Lauke **Tipas** pasirinkite, ar pastoviosios kompensacijos planas yra **Intervalo**, **Kategorijos** ar **Veiksmo**.</span><span class="sxs-lookup"><span data-stu-id="2db76-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="2db76-114">Žymės langelis **Leistina rekomendacija** veikia kaip bet kokių veiksmų, įtrauktų į šį planą apdorojimo įvykyje, numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2db76-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="2db76-115">Leidę rekomendacijas galėsite nepaisyti paskaičiuotos siūlomos sumos apdorodami kompensaciją.</span><span class="sxs-lookup"><span data-stu-id="2db76-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="2db76-116">Laukas **Leistinas nepatekimas į intervalą** leidžia nurodyti, kaip norite elgtis su kompensacijų sumomis, kurios nepatenka į nurodytą pateikto lygio kompensavimo struktūros diapazoną.</span><span class="sxs-lookup"><span data-stu-id="2db76-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="2db76-117">Lauką **Leistinas nepatekimas į intervalą** nustačius kaip **Joks**, galima naudoti bet kokią kompensacijos sumą.</span><span class="sxs-lookup"><span data-stu-id="2db76-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="2db76-118">Pasirinkus parinktį **Negriežtas nuokrypis**, vartotojas įspėjamas, jei kompensacijos suma yra mažesnė, nei minimali to lygio atskaitos taško suma, arba didesnė, nei maksimali to lygio suma.</span><span class="sxs-lookup"><span data-stu-id="2db76-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="2db76-119">Vartotojai gali įspėjimo nepaisyti ir tęsti veiklą.</span><span class="sxs-lookup"><span data-stu-id="2db76-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="2db76-120">Pasirinkus parinktį **Griežtas nuokrypis**, sugeneruojama klaida, jei darbuotojo kompensacija nustatyta ne tarp minimalių ir maksimalių to lygio atskaitos taškų, ir darbuotojo kompensacija automatiškai pakoreguojama, kad ji patektų į šį intervalą.</span><span class="sxs-lookup"><span data-stu-id="2db76-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="2db76-121">Laukas **Samdos taisyklė** apskaičiuoja darbuotojo kompensaciją apdorojimo įvykio metu.</span><span class="sxs-lookup"><span data-stu-id="2db76-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="2db76-122">**Procentinė** **samdos taisyklė** apskaičiuoja padidėjimą, proporcingą laiko trukmei, kurią darbuotojas dirba cikle.</span><span class="sxs-lookup"><span data-stu-id="2db76-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="2db76-123">Lauke **Valiuta** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="2db76-124">Lauke **Užmokesčio tarifo konvertavimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="2db76-125">Išplėskite dalį **Intervalo realizavimo matrica**.</span><span class="sxs-lookup"><span data-stu-id="2db76-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="2db76-126">Papildomai galite įtraukti diapazono realizavimo įrašų, kad darbuotojai greičiau pasiektų vidurio tašką ir kad sulėtintumėte spartą, kuria jie juda link savo diapazono maksimumo.</span><span class="sxs-lookup"><span data-stu-id="2db76-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="2db76-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2db76-127">Select **Save**.</span></span> <span data-ttu-id="2db76-128">Taip įjungiamas mygtukas **Nustatyti kompensaciją** ir toliau nustatoma kompensacijos plano struktūra.</span><span class="sxs-lookup"><span data-stu-id="2db76-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="2db76-129">Pasirinkite **Nustatyti kompensaciją**.</span><span class="sxs-lookup"><span data-stu-id="2db76-129">Select **Set up compensation**.</span></span> <span data-ttu-id="2db76-130">Kompensacijos struktūrą galite sukurti vienu iš toliau nurodytų trijų būdų.</span><span class="sxs-lookup"><span data-stu-id="2db76-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="2db76-131">Sukurti visiškai naują struktūrą, pasirenkant atskaitos taškų rinkinį ir įtraukiant lygių bei sukuriant savą struktūrą.</span><span class="sxs-lookup"><span data-stu-id="2db76-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="2db76-132">Kompensacijos struktūrą kopijuoti iš esamo plano kaip pradžios tašką ir ją modifikuoti naujajam planui.</span><span class="sxs-lookup"><span data-stu-id="2db76-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="2db76-133">Pasirinkti esamą kompensacijų tinklelį.</span><span class="sxs-lookup"><span data-stu-id="2db76-133">Select an existing compensation grid.</span></span> <span data-ttu-id="2db76-134">Jei kompensacijų tinklelį jau naudoja kitas planas, visi atlikti tinklelio pakeitimai taip pat atsispindi kitame plane.</span><span class="sxs-lookup"><span data-stu-id="2db76-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="2db76-135">Pasirinkite **Pagal esamą kompensavimo matricą sukurti naują**.</span><span class="sxs-lookup"><span data-stu-id="2db76-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="2db76-136">Lauke **Kopijuoti iš tinklelio** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="2db76-137">Jei norite, galite keisti naujojo kompensacijų tinklelio, kurį sukuriate nukopijuodami pasirinktą tinklelį, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2db76-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="2db76-138">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2db76-138">Select **OK**.</span></span>

19. <span data-ttu-id="2db76-139">Pasirinkite **Masinis keitimas**.</span><span class="sxs-lookup"><span data-stu-id="2db76-139">Select **Mass change**.</span></span> <span data-ttu-id="2db76-140">**Masinis keitimas** leidžia išlaikyti kompensacijų matricos sumas, vieną ar kelis lygius ir (arba) atskaitos taškus padidinant procentine dalimi arba standartine suma.</span><span class="sxs-lookup"><span data-stu-id="2db76-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="2db76-141">Lauke **Koregavimo suma** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2db76-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="2db76-142">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="2db76-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="2db76-143">Spustelėkite **Taikyti tinkleliui**.</span><span class="sxs-lookup"><span data-stu-id="2db76-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="2db76-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2db76-144">Close the page.</span></span> <span data-ttu-id="2db76-145">Sukūrę kompensavimo struktūrą, galite pasirinkti, kurie atskaitos taškai turėtų būti naudojami kaip pastoviosios kompensacijos plano kontrolinis taškas.</span><span class="sxs-lookup"><span data-stu-id="2db76-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="2db76-146">Kontrolinis taškas naudojamas darbuotojo lyginamajam koeficientui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="2db76-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="2db76-147">Lauke **Kontrolinis taškas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="2db76-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2db76-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="2db76-149">Pastoviosios kompensacijos plano tinkamumo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="2db76-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="2db76-150">Pastoviosios kompensacijos plano darbuotojui priskirti negalite tol, kol nenustatote plano tinkamumo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="2db76-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="2db76-151">Pasirinkite **Tinkamumo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="2db76-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="2db76-152">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2db76-152">Select **New**.</span></span>

3. <span data-ttu-id="2db76-153">Lauke **Tinkamumas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="2db76-154">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="2db76-155">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="2db76-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="2db76-156">Tinkamumo taisyklės naudojamos tiek pastoviosios, tiek kintamosios kompensacijos planuose.</span><span class="sxs-lookup"><span data-stu-id="2db76-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="2db76-157">Lauke **Tipas** pasirinkite plano tipą.</span><span class="sxs-lookup"><span data-stu-id="2db76-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="2db76-158">Lauke **Planas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2db76-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="2db76-159">Pasirinkite kriterijus, kuriuos turi atitikti darbuotojas, kad turėtų teisę į kompensavimo planą.</span><span class="sxs-lookup"><span data-stu-id="2db76-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="2db76-160">Toliau nurodyti galimi kriterijai.</span><span class="sxs-lookup"><span data-stu-id="2db76-160">Criteria can include:</span></span>

    - <span data-ttu-id="2db76-161">**Skyrius**</span><span class="sxs-lookup"><span data-stu-id="2db76-161">**Department**</span></span>
    - <span data-ttu-id="2db76-162">**Profesinė sąjunga**</span><span class="sxs-lookup"><span data-stu-id="2db76-162">**Labor union**</span></span>
    - <span data-ttu-id="2db76-163">**Vieta** (**Kompensacijų regionas**)</span><span class="sxs-lookup"><span data-stu-id="2db76-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="2db76-164">**Užduotis**</span><span class="sxs-lookup"><span data-stu-id="2db76-164">**Job**</span></span>
    - <span data-ttu-id="2db76-165">**Funkcija**</span><span class="sxs-lookup"><span data-stu-id="2db76-165">**Function**</span></span>
    - <span data-ttu-id="2db76-166">**Užduoties tipas**</span><span class="sxs-lookup"><span data-stu-id="2db76-166">**Job type**</span></span>
    - <span data-ttu-id="2db76-167">**Kompensavimo lygis**</span><span class="sxs-lookup"><span data-stu-id="2db76-167">**Compensation level**</span></span>
    
    <span data-ttu-id="2db76-168">Kad turėtų teisę į kompensavimo planą, darbuotojas turi atitikti visus nurodytus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="2db76-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="2db76-169">Jei nenurodote jokių kriterijų, į kompensacijos planą teisę turi visi darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="2db76-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="2db76-170">Jei darbuotojas neatitinka tinkamumo taisyklėje nurodytų kriterijų, arba jei kompensavimo plano tinkamumo taisyklė nenurodyta, kuriant darbuotojo pastoviosios kompensacijos įrašą, peržvalgoje kompensavimo planas nebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="2db76-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="2db76-171">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2db76-171">Close the page.</span></span>

8. <span data-ttu-id="2db76-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2db76-172">Close the page.</span></span>

