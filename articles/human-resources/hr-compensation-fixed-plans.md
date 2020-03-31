---
title: Pastoviosios atlyginimo dalies planų kūrimas
description: Pastovioji atlyginimo dalis nurodo darbuotojo pastovų bruto atlyginimą ar darbo užmokestį. Šiame straipsnyje aprašomi komponentai, kurie turi būti nustatyti prieš kuriant pastoviosios atlyginimo dalies planą ir įtraukiant darbuotojus.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 05eea520c656619d72d4601991e255ae887ffe9c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009992"
---
# <a name="create-a-fixed-compensation-plans"></a><span data-ttu-id="25a73-104">Pastoviosios atlyginimo dalies planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="25a73-104">Create a fixed compensation plans</span></span>

<span data-ttu-id="25a73-105">Pastovioji atlyginimo dalis nurodo darbuotojo pastovų bruto atlyginimą ar darbo užmokestį.</span><span class="sxs-lookup"><span data-stu-id="25a73-105">Fixed compensation refers to an employee's regular gross salary or wages.</span></span> <span data-ttu-id="25a73-106">Šiame straipsnyje aprašomi komponentai, kurie turi būti nustatyti prieš kuriant pastoviosios atlyginimo dalies planą ir įtraukiant darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="25a73-106">This article describes the components that must be set up before you can create a fixed compensation plan and enroll employees.</span></span>

<span data-ttu-id="25a73-107">Pastoviosios darbuotojų atlyginimo dalies sumas galima apskaičiuoti pagal tokius veiksnius kaip rezultatai, regionas ir biudžeto padidinimai.</span><span class="sxs-lookup"><span data-stu-id="25a73-107">Fixed compensation amounts can be calculated for your employees, based on factors such as performance, region, and budget increases.</span></span> <span data-ttu-id="25a73-108">„Dynamics 365 Human Resources” palaiko veiksmų, kategorijos ir intervalo kompensacijos tipus.</span><span class="sxs-lookup"><span data-stu-id="25a73-108">Dynamics 365 Human Resources supports step, grade, and band compensation types.</span></span>

## <a name="fixed-compensation-components"></a><span data-ttu-id="25a73-109">Pastoviosios atlyginimo dalies komponentai</span><span class="sxs-lookup"><span data-stu-id="25a73-109">Fixed compensation components</span></span>
### <a name="compensation-levels"></a><span data-ttu-id="25a73-110">kompensacijos lygiai</span><span class="sxs-lookup"><span data-stu-id="25a73-110">Compensation levels</span></span>

<span data-ttu-id="25a73-111">Galite naudoti **kompensacijos lygius**, kad nustatytumėte kompensaciją už įvairias užduotis, užtikrindami, kad šias užduotys atliekantiems darbuotojams būtų sąžiningai mokama.</span><span class="sxs-lookup"><span data-stu-id="25a73-111">You can use **compensation levels** to set compensation for various jobs, to help guarantee that the employees who hold those jobs are paid fairly.</span></span> <span data-ttu-id="25a73-112">Puslapyje **Kompensacijos lygiai** galite nustatyti kompensacijos lygius, kurių reikia kiekvienam veiksmų, kategorijos ir intervalo planui.</span><span class="sxs-lookup"><span data-stu-id="25a73-112">On the **Compensation levels** page, you can set up the compensation levels that are required for each step, grade, and band plan.</span></span> <span data-ttu-id="25a73-113">Naudokite mygtukus **aukštyn** ir **žemyn**, kad išdėstytumėte lygius teisinga tvarka, pagal jų tipą.</span><span class="sxs-lookup"><span data-stu-id="25a73-113">Use the **Up** and **Down** buttons to put the levels in the correct order, according to their type.</span></span> <span data-ttu-id="25a73-114">Nustatydami užduoties kompensacijos lygius, padedate užtikrinti, kad visiems darbuotojams, kurių pareigoms priskirta vienoda užduotis, bus mokama vienodai.</span><span class="sxs-lookup"><span data-stu-id="25a73-114">By setting compensation levels on a job, you help guarantee that all employees who hold a position for that job are paid at the same level.</span></span>

### <a name="reference-points"></a><span data-ttu-id="25a73-115">Atskaitos taškai</span><span class="sxs-lookup"><span data-stu-id="25a73-115">Reference points</span></span>

<span data-ttu-id="25a73-116">**Atskaitos taškai** yra stulpeliai tinklelyje, apibrėžiantys kiekvieno lygio kompensacijos intervalus.</span><span class="sxs-lookup"><span data-stu-id="25a73-116">**Reference points** are the columns in the grid that define the compensation ranges for each level.</span></span> <span data-ttu-id="25a73-117">kompensacijos lygis yra tinklelio eilutė.</span><span class="sxs-lookup"><span data-stu-id="25a73-117">The compensation level is the row in the grid.</span></span> <span data-ttu-id="25a73-118">Įprasti kategorijos tipo plano atskaitos taškai yra mažiausias, vidurinis ir didžiausias.</span><span class="sxs-lookup"><span data-stu-id="25a73-118">Typical reference points for a plan of the grade type are a minimum, a midpoint, and a maximum.</span></span> <span data-ttu-id="25a73-119">Atskaitos taškai kuriami puslapyje **Atskaitos taškų nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="25a73-119">You create reference points on the **Reference point setups** page.</span></span>

### <a name="compensation-grids"></a><span data-ttu-id="25a73-120">Kompensavimo tinkleliai</span><span class="sxs-lookup"><span data-stu-id="25a73-120">Compensation grids</span></span>

<span data-ttu-id="25a73-121">Nustatę lygius ir atskaitos taškus, jie gali būti derinami sukuriant **kompensacijų tinklelį**.</span><span class="sxs-lookup"><span data-stu-id="25a73-121">After you set up the levels and reference points, they can be combined to create a **compensation grid**.</span></span> <span data-ttu-id="25a73-122">Puslapyje **Kompensacijų tinkleliai** nurodyti informaciją apie tinklelį.</span><span class="sxs-lookup"><span data-stu-id="25a73-122">On the **Compensation grids** page, define information about the grid.</span></span> <span data-ttu-id="25a73-123">Pvz., nurodykite, kam sukurtas tinklelis turi būti naudojamas, su kokio tipo planu jis bus naudojamas ir kuriuos atskaitos taškus ar stulpelius rodyti tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="25a73-123">For example, specify what the grid designed to be used for, what type of plan it will be used with, and which reference points or columns are required in the grid.</span></span> <span data-ttu-id="25a73-124">Baigę įvesti šią informaciją, spustelėkite **kompensacijos struktūra**, kad prie savo tinklelio pridėtumėte lygius ir sumas.</span><span class="sxs-lookup"><span data-stu-id="25a73-124">After you've finished entering that information, click **Compensation structure** to add levels and amounts to your grid.</span></span> 

<span data-ttu-id="25a73-125">**Patarimas:** nustatykite pradines sumas naudodami kompensacijos struktūros funkciją **Masiniai keitimai**, tada didinkite procentais arba sumomis savo lygiuose arba atskaitos taškuose.</span><span class="sxs-lookup"><span data-stu-id="25a73-125">**Tip:** Use the **Mass changes** function on the compensation structure to set initial amounts, and then increment by percentages or amounts across your levels or reference points.</span></span>

### <a name="pay-frequencies"></a><span data-ttu-id="25a73-126">Išmokų dažnumas</span><span class="sxs-lookup"><span data-stu-id="25a73-126">Pay frequencies</span></span>

<span data-ttu-id="25a73-127">**Mokėjimo dažnumas** naudojamas norint apibrėžti, kaip nurodyti darbuotojo darbo užmokestį arba kompensaciją (pavyzdžiui, 10 $ per valandą ar 50 000 $ per metus) ir konvertuoti į valandinius, savaitinius, mėnesinis (12 mėnesių) ir metinius tarifus.</span><span class="sxs-lookup"><span data-stu-id="25a73-127">**Pay frequencies** are used to define how an employee's wage or salary is being specified (for example $10 per hour versus $50,000 per year), and the conversion between the hourly, weekly, monthly (12 months), and annual rates.</span></span> <span data-ttu-id="25a73-128">Pavyzdžiui, įmonė, kur valandinį tarifą gaunančių darbuotojų darbo savaitė trunka 38 valandas, nustato mokėjimo dažnumą, kurio valandinis tarifas yra 1, savaitinis tarifas 38, mėnesinis tarifas 164,6666666667 ir metinis tarifas 1,976.</span><span class="sxs-lookup"><span data-stu-id="25a73-128">For example, a company that uses a 38-hour work week for its hourly employees sets up a pay frequency that has an hourly rate of 1, a weekly rate of 38, a monthly rate of 164.6666666667, and an annual rate of 1,976.</span></span> <span data-ttu-id="25a73-129">Konvertavimas naudojamas norint apskaičiuoti įvairius darbuotojo pastoviosios atlyginimo dalies įrašuose nustatomus tarifus.</span><span class="sxs-lookup"><span data-stu-id="25a73-129">These conversions are used to calculate the various pay rates that appear on an employee's fixed compensation record.</span></span>

## <a name="fixed-compensation-plans"></a><span data-ttu-id="25a73-130">Pastoviųjų atlyginimo dalių planai</span><span class="sxs-lookup"><span data-stu-id="25a73-130">Fixed compensation plans</span></span>
<span data-ttu-id="25a73-131">Galite sukurti sujungti pastoviosios atlyginimo dalies planą, apimantį visus jūsų sukonfigūruotus komponentus.</span><span class="sxs-lookup"><span data-stu-id="25a73-131">You can design the fixed compensation plan to combine all the components that you've configured.</span></span> <span data-ttu-id="25a73-132">Norėdami sukurti pastoviosios atlyginimo dalies planą, atidarykite puslapį **Pastoviosios atlyginimo dalies planai**.</span><span class="sxs-lookup"><span data-stu-id="25a73-132">To create a fixed compensation plan, open the **Fixed compensation plans** page.</span></span> <span data-ttu-id="25a73-133">Čia galite suteikti savo planui pavadinimą ir aprašymą, pasirinkti, kokio tipo planas tai yra (veiksmų, kategorijos ar intervalo), pasirinkti darbuotojo užmokesčio tarifo mokėjimo dažnumą (suma per valandą, suma per metus ir t.t.) ir nustatyti kompensacijos apdorojimo tvarkymo parinktis.</span><span class="sxs-lookup"><span data-stu-id="25a73-133">Here, you can give your plan a name and description, select what type of plan it is (step, grade, or band), select the pay frequency that you'll use for the employee's pay rate (amount per hour, amount per year, and so on), and set some options that control how compensation is processed.</span></span> 

<span data-ttu-id="25a73-134">Nustatymas **Nepatenka į leistiną nuokrypio diapazoną** leidžia nurodyti, kaip griežtai norite užtikrinti, kad kompensacijos sumos būtų tarp mažiausios ir didžiausios sumų.</span><span class="sxs-lookup"><span data-stu-id="25a73-134">The **Out of range tolerance** setting lets you specify how strict you want to be about making sure that compensation amounts are between the minimum and maximum amounts.</span></span> <span data-ttu-id="25a73-135">**Griežtas** nuokrypis reikalauja, kad kompensacija patektų į atitinkamo lygio diapazoną.</span><span class="sxs-lookup"><span data-stu-id="25a73-135">A **Hard** tolerance requires that compensation be within the range that is defined for a given level.</span></span> <span data-ttu-id="25a73-136">**Nuosaikus** nuokrypis įspėja, kai kompensacijos suma nebepatenka į diapazoną, bet leidžia tęsti.</span><span class="sxs-lookup"><span data-stu-id="25a73-136">A **Soft** tolerance alerts you when the compensation amount is outside the range but allows you to continue.</span></span> <span data-ttu-id="25a73-137">Jei nustatysite nuokrypio reikšmę **Nėra**, galėsite įvesti darbuotojo kompensacijos sumą sumą ir negauti įspėjimo arba klaidos pranešim..</span><span class="sxs-lookup"><span data-stu-id="25a73-137">If you set the tolerance to **None**, you can enter any compensation amount for an employee without receiving warning or error messages.</span></span> 

<span data-ttu-id="25a73-138">Parametras **Samdos taisyklė** leidžia nurodyti, ar visi darbuotojai turi gauti tokį patį padidėjimą, neatsižvelgiant į jų pasamdymo dieną(**Samdos taisyklė**  = **Nėra**), ar darbuotojai turi gauti procentą nuo premijos, atsižvelgiant į tai, kiek laiko jie dirbo per ciklą (**Samdos taisyklė**  = **Procentas**).</span><span class="sxs-lookup"><span data-stu-id="25a73-138">The **Hire rule** setting lets you specify whether all employees should receive the same increase, regardless of the date that they were hired (**Hire rule** = **None**), or whether employees should receive a percentage of the award, based on how long they were employed during the cycle (**Hire rule** = **Percent**).</span></span> 

<span data-ttu-id="25a73-139">**Diapazono realizavimo matrica** naudinga, jei norite sutrumpinti laiką, kurio reikia darbuotojams, kad pasiektų savo diapazono vidurio tašką, arba pailginti laiką, kurio reikia darbuotojams, kad pasiektų savo diapazono didžiausią atskaitos tašką.</span><span class="sxs-lookup"><span data-stu-id="25a73-139">A **range utilization matrix** is useful if you want either to reduce the time that is required for employees to reach the midpoint of their range, or to increase the time that is required for employees to reach to the maximum reference point in the range.</span></span> <span data-ttu-id="25a73-140">Pavyzdžiui, norite darbuotojams, kurie yra apatinių 25 procentų diapazone, suteikti 110 procentų jų tikslinės premijos, bet darbuotojams, kurie yra viršutinių 25 procentų diapazone, norite suteikti tik 80 procentų jų tikslinės premijos, kad neleistumėte taip greitai pasiekti didžiausios reikšmės.</span><span class="sxs-lookup"><span data-stu-id="25a73-140">For example, you want to give employees who are in the bottom 25 percent of their range 110 percent of their target award, but you want to give employees who are in the top 25 percent of their range only 80 percent of their target award, to prevent them from reaching the maximum as quickly.</span></span> 

<span data-ttu-id="25a73-141">Apibrėžę pastoviosios atlyginimo dalies plano pagrindus, galite nustatyti plano kompensacijos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="25a73-141">After you define the basics of the fixed compensation plan, you can set up the compensation structure for the plan.</span></span> <span data-ttu-id="25a73-142">Spustelėkite **Nustatyti kompensaciją**.</span><span class="sxs-lookup"><span data-stu-id="25a73-142">Click **Set up compensation**.</span></span> <span data-ttu-id="25a73-143">Atidaromas dialogo slankiklis, kuris suteikia tris parinktis.</span><span class="sxs-lookup"><span data-stu-id="25a73-143">A dialog slider opens that gives you three options:</span></span>

-   <span data-ttu-id="25a73-144">Sukurti naują kompensacijų tinklelį pasirenkant atskaitos taško nustatymą ir suteikiant tinkleliui pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="25a73-144">Create a new compensation grid by selecting a reference point setup and giving the grid a name.</span></span>
-   <span data-ttu-id="25a73-145">Sukurti naują kompensacijų tinklelį nukopijuojant esamą tinklelį, kurį galite naudoti kaip pradžios tašką.</span><span class="sxs-lookup"><span data-stu-id="25a73-145">Create a new compensation grid by making a copy of an existing grid that you can use as a starting point.</span></span>
-   <span data-ttu-id="25a73-146">Naudoti esamą kompensacijų tinklelį, kuris jau apibrėžtas.</span><span class="sxs-lookup"><span data-stu-id="25a73-146">Use an existing compensation grid that has already been defined.</span></span> <span data-ttu-id="25a73-147">Visi kompensacijų planai, kurie naudoja tą patį tinklelį, gauna atnaujinimus, jei tas tinklelis pakeičiamas.</span><span class="sxs-lookup"><span data-stu-id="25a73-147">All compensation plans that use the same grid receive updates if that grid is changed.</span></span>

<span data-ttu-id="25a73-148">Kai pasirenkate parinktį, atidaromas puslapis **kompensacijos struktūra** ir galite keisti naują ar esamą kompensacijų tinklelį.</span><span class="sxs-lookup"><span data-stu-id="25a73-148">After you select an option, the **Compensation structure** page opens, and you can make changes to the new compensation grid or the existing compensation grid.</span></span>

## <a name="fixed-compensation-enrollment"></a><span data-ttu-id="25a73-149">Pastoviosios atlyginimo dalies registracija</span><span class="sxs-lookup"><span data-stu-id="25a73-149">Fixed compensation enrollment</span></span>
### <a name="determine-who-is-eligible-for-the-plan"></a><span data-ttu-id="25a73-150">Nustatykite, kas turi teisę gauti planą</span><span class="sxs-lookup"><span data-stu-id="25a73-150">Determine who is eligible for the plan</span></span>

<span data-ttu-id="25a73-151">Pirmasis darbuotojų įtraukimo į pastoviosios atlyginimo dalies planą žingsnis yra nustatyti, kas turi teisę gauti gauti plane apibrėžtą kompensaciją.</span><span class="sxs-lookup"><span data-stu-id="25a73-151">The first step in enrolling employees in a fixed compensation plan is to determine who is eligible for the compensation that is defined in the plan.</span></span> <span data-ttu-id="25a73-152">Kol nenustatysite tinkamumo, negalėsite priskirti plano nė vienam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="25a73-152">Until you determine eligibility, you won't be able to assign the plan to any employees.</span></span> <span data-ttu-id="25a73-153">Norėdami nustatyti tinkamumą, atidarykite puslapį **Tinkamumo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="25a73-153">To set up eligibility, open the **Eligibility rules** page.</span></span> <span data-ttu-id="25a73-154">Čia galite sukurti naują tinkamumo jūsų kompensacijos planui taisyklę ir apibrėžti kriterijus, kuriuos darbuotojas turi atitikti, kad būtų tinkamas šiam planui.</span><span class="sxs-lookup"><span data-stu-id="25a73-154">Here, you create a new eligibility rule for your compensation plan and define the criteria that an employee must meet to be eligible for a plan.</span></span> <span data-ttu-id="25a73-155">Galite riboti tinkamumą pagal padalinį, profesinę sąjungą, kompensacijų regioną (vietą), užduotį, užduoties tipą arba kompensacijos lygį.</span><span class="sxs-lookup"><span data-stu-id="25a73-155">You can limit eligibility based on department, labor union, compensation region (location), job, job function, job type, or compensation level.</span></span> <span data-ttu-id="25a73-156">Darbuotojai gali būti įtraukti į kompensacijos planą tik tada, jei jie atitinka visus kriterijus, nustatytus tinkamumo taisyklėje.</span><span class="sxs-lookup"><span data-stu-id="25a73-156">Employees can be enrolled in a compensation plan only if they meet all conditions that are set on the eligibility rule.</span></span> 

<span data-ttu-id="25a73-157">**Pastaba:** tinkamumo taisyklės naudojamos siekiant nustatyti teisę tiek į pastoviosios, tiek į kintamosios atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="25a73-157">**Note:** Eligibility rules are used to determine eligibility for both fixed and variable compensation plans.</span></span> 

<span data-ttu-id="25a73-158">Tinkamumo taisyklė įvertina konkrečių užduoties, pareigų ir darbuotojo įrašų laukų reikšmę, kad nustatytų, ar darbuotojas turi teisę į kompensacijos planą.</span><span class="sxs-lookup"><span data-stu-id="25a73-158">The eligibility rule considers the value of specific fields in the Job, Position, and Employee records to determine whether an employee is eligible for a compensation plan.</span></span>

-   <span data-ttu-id="25a73-159">Puslapyje **Užduotis** tinkamumo taisyklė atsižvelgia į šiuos laukus:</span><span class="sxs-lookup"><span data-stu-id="25a73-159">On the **Job** page, the eligibility rule considers the following fields:</span></span>
    -   <span data-ttu-id="25a73-160">Lauką **Užduotis**</span><span class="sxs-lookup"><span data-stu-id="25a73-160">The **Job** field</span></span>
    -   <span data-ttu-id="25a73-161">Skirtuke **Užduočių klasifikacija** – į laukus **Funkcija** ir **Užduoties tipas**</span><span class="sxs-lookup"><span data-stu-id="25a73-161">On the **Job classification** tab, the **Function** and **Job type** fields</span></span>
    -   <span data-ttu-id="25a73-162">Skirtuke **Kompensacija** – į lauką **Lygis**</span><span class="sxs-lookup"><span data-stu-id="25a73-162">On the **Compensation** tab, the **Level** field</span></span>
-   <span data-ttu-id="25a73-163">Puslapyje **Pareigos** tinkamumo taisyklė įvertina laukus **Padalinys** ir **Kompensacijų regionas**.</span><span class="sxs-lookup"><span data-stu-id="25a73-163">On the **Positions** page, the eligibility rule considers the **Department** and **Compensation region** fields.</span></span>

<span data-ttu-id="25a73-164">Tinkamumo taisyklė taip pat įvertina su darbuotoju susijusias profesines sąjungas (puslapyje **Darbuotojai**, skirtuke **Darbuotojas**, spustelėkite **Asmeninė informacija** &gt; **Profesinės sąjungos**).</span><span class="sxs-lookup"><span data-stu-id="25a73-164">The eligibility rule also considers labor unions that are associated with the employee (on the **Employees** page, on the **Worker** tab, click **Personal information** &gt; **Labor unions**).</span></span>

### <a name="define-fixed-compensation-actions"></a><span data-ttu-id="25a73-165">Pastoviosios atlyginimo dalies veiksmų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="25a73-165">Define fixed compensation actions</span></span>

<span data-ttu-id="25a73-166">**Pastoviosios atlyginimo dalies veiksmai** naudojami, kai nustatote arba taikoti darbuotojo pastoviosios atlyginimo dalies pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="25a73-166">**Fixed compensation actions** are used when you set or apply changes to an employee's fixed compensation.</span></span> <span data-ttu-id="25a73-167">Pastoviosios atlyginimo dalies veiksmai leidžia pateikti aprašomuosius pavadinimus veiksmų tipams, kuriuos gali atlikti kompensacijų ir išmokų vadovas.</span><span class="sxs-lookup"><span data-stu-id="25a73-167">Fixed compensation actions let you provide descriptive names for the types of actions that a Compensation and benefits manager can perform.</span></span> <span data-ttu-id="25a73-168">Skirtingi veiksmų tipai paremti skirtinga logika, kad jie galėtų būti naudojami tik tam tikru metu.</span><span class="sxs-lookup"><span data-stu-id="25a73-168">Different action types have special logic behind them, so that they can be used at specific times.</span></span> 

<span data-ttu-id="25a73-169">Pvz., nustačius pastoviąją atlyginimo dalį darbuotojui, galima naudoti tik tuos veiksmus, kurių tipas yra **Samda / Pakartotinė samda**.</span><span class="sxs-lookup"><span data-stu-id="25a73-169">For example, when the fixed compensation is set up for an employee, only actions that have a type of **Hire/Rehire** can be used.</span></span> <span data-ttu-id="25a73-170">Tokiu atveju gali būti paranku sukurti tris skirtingus **Samda / Pakartotinė samda** tipo veiksmus ir juos pavadinti **Samdyti**, **Pakartotinai samdyti** ir **Perkelti**.</span><span class="sxs-lookup"><span data-stu-id="25a73-170">In this case, you might want to create three different actions of the **Hire/Rehire** type, and name them **Hire**, **Rehire**, and **Transfer**.</span></span> <span data-ttu-id="25a73-171">Tokiu būdu turėsite detalesnį paaiškinimą, kodėl pastovioji atlyginimo dalis buvo skirta darbuotojui arba pakeista.</span><span class="sxs-lookup"><span data-stu-id="25a73-171">You then have a more descriptive explanation of why the fixed compensation was given to an employee or changed.</span></span>

### <a name="enroll-the-employee"></a><span data-ttu-id="25a73-172">Darbuotojo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="25a73-172">Enroll the employee</span></span>

<span data-ttu-id="25a73-173">Dabar galite pastoviosios atlyginimo dalies planui priskirti darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="25a73-173">You can now assign an employee to a fixed compensation plan.</span></span> <span data-ttu-id="25a73-174">Atidarykite puslapį **Darbuotojai** ir pasirinkite darbuotoją, kurį norite įtraukti į kompensacijos planą.</span><span class="sxs-lookup"><span data-stu-id="25a73-174">Open the **Employees** page, and select the employee to enroll in the compensation plan.</span></span> <span data-ttu-id="25a73-175">Veiksmų srityje spustelėkite **Kompensacija** &gt; **Pastoviosios dalies planas**.</span><span class="sxs-lookup"><span data-stu-id="25a73-175">On the Action Pane, click **Compensation** &gt; **Fixed plan**.</span></span> <span data-ttu-id="25a73-176">Dabar tam darbuotojui galite sukurti naują pastoviosios atlyginimo dalies veiksmą.</span><span class="sxs-lookup"><span data-stu-id="25a73-176">You can now create a new fixed compensation action for that employee.</span></span> 

<span data-ttu-id="25a73-177">**Pastaba:** kompensacijos plano lauke rodomi tik tie planai, į kuriuos darbuotojas turi teisę pagal kiekvienam planui nustatytas tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="25a73-177">**Note:** The compensation plan field shows only the plans that an employee is eligible for under the eligibility rules that were set up for each plan.</span></span> <span data-ttu-id="25a73-178">Jei planas neturi nustatytos tinkamumo taisyklės, į tokį planą negalės būti įtraukti jokie darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="25a73-178">If no eligibility rule is set up for a plan, no employees will be eligible for that plan.</span></span> 

<span data-ttu-id="25a73-179">Sistema patikrina, kad nurodyta kategorijos arba intervalo tipo kompensacijos plano suma yra tarp mažiausio ir didžiausio atskaitos taškų pagal darbuotojo užduočiai priskirtą kompensacijos lygį.</span><span class="sxs-lookup"><span data-stu-id="25a73-179">The system verifies that the compensation amount that is specified for a compensation plan of the grade or band type is within the minimum and maximum reference points for the given compensation level on the employee's job.</span></span> <span data-ttu-id="25a73-180">Jei kompensacijos suma nepatenka į leidžiamą diapazoną, rodomas perspėjimas arba klaidos pranešimas, atsižvelgiant į pastoviosios atlyginimo dalies plano nuokrypio lygį.</span><span class="sxs-lookup"><span data-stu-id="25a73-180">If the compensation amount is outside the allowed range, a warning or error message is displayed, depending on the tolerance level that is set on the fixed compensation plan.</span></span>
