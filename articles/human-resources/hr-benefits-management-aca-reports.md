---
title: Kurti prieinamą priežiūros akto ataskaits išmokų valdyme
description: Šioje temoje aprašoma, kaip išmokų valdymas padeda jums sekti informaciją pateiktą formoje 1095-B ir formoje 1095-C prieinamos priežiūros akto (ACA) darbuotojo mandatui.
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1417232baeaf03721bd0b25cc3f9fd5f750c65d5
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052270"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="3c579-103">Kurti ACA ataskaitas išmokų valdymą</span><span class="sxs-lookup"><span data-stu-id="3c579-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3c579-104">Išmokų valdymas padeda jums sekti informaciją pateiktą formoje 1095-B ir formoje 1095-C prieinamos priežiūros akto (ACA) darbuotojo mandatui.</span><span class="sxs-lookup"><span data-stu-id="3c579-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="3c579-105">Kaip ACA ataskaitų pajėgumai, sena **Išmokų** darbo sritis, ši funkcija taikimoa tik juridiniams asmenims JAV.</span><span class="sxs-lookup"><span data-stu-id="3c579-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="3c579-106">Norėdami naudoti šią funkciją, turite pirma įjungti **Papildomų išmokų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="3c579-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="3c579-107">Dėl daugiau informacijos, įskaitant svarbius konfliktus apie išmokų valdymą, žr. [Įjungti ar išjungti išmokų valdymą](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="3c579-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c579-108">Galite naudoti ACA ataskaitas tik iš **Išmokų valdymo** darbo srities ar senos **Išmokų** darbo srities, ne iš abiejų.</span><span class="sxs-lookup"><span data-stu-id="3c579-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="3c579-109">Pavyzdžiui, jei perjungiate į išmokų valdymą, ACA ataskaitos bus prieinamos tik iš **Išmokų valdymo** darbo srities, ne iš senos **Išmokų** darbo srities.</span><span class="sxs-lookup"><span data-stu-id="3c579-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="3c579-110">Jei perjungsite į išmokų valdymą įtraukimo metų viduryjė, turite tiksliai konfigūruoti darbuotojo duomenis visiems metams išmokų valdyme.</span><span class="sxs-lookup"><span data-stu-id="3c579-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="3c579-111">Tokiu būdu, užtikrinsite, kad gausite tikslią ataskaitos informaciją už visus metus.</span><span class="sxs-lookup"><span data-stu-id="3c579-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="3c579-112">Darbo pradžia</span><span class="sxs-lookup"><span data-stu-id="3c579-112">Getting started</span></span>

<span data-ttu-id="3c579-113">Norėdami sekti informaciją 1095 formoms, pirmiausia sukurkite vieną ir daugiau išlaikomos priežiūros aprėpties grupių.</span><span class="sxs-lookup"><span data-stu-id="3c579-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="3c579-114">Šios grupės nurodo šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="3c579-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="3c579-115">Aprėpties pasiūlymas pateiktas darbuotojui</span><span class="sxs-lookup"><span data-stu-id="3c579-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="3c579-116">Darbuotojo dalis mažiausių kaštų mėnesio premijos, jei kaštai viršija federalinį skurdo lygį</span><span class="sxs-lookup"><span data-stu-id="3c579-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="3c579-117">Saugus uostas naudojamas darbuotojo, jei taikomas</span><span class="sxs-lookup"><span data-stu-id="3c579-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="3c579-118">Išlaiikymo priežiūros aprėpties grupės jums padeda valdyti šią informaciją keliems darbuotojų įrašams, kurie turi tokią pačią sąlygą.</span><span class="sxs-lookup"><span data-stu-id="3c579-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="3c579-119">Galite nesunkiai priskirti grupes vienam ar keliems darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="3c579-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="3c579-120">Kurti ar redaguoti išlaikomos priežiūros aprėpties grupę</span><span class="sxs-lookup"><span data-stu-id="3c579-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="3c579-121">Darbo srityje **Išmokų valdymas** rinkitės **Išlaikymo priežiūros aprėpties grupė**.</span><span class="sxs-lookup"><span data-stu-id="3c579-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Rinkitės išlaikomos priežiūros aprėpties grupę](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="3c579-123">Rinkitės **Nauja** tam, kad sukurtumėtė nauja išlaikymo priežiūros aprėpties grupę arba **Redaguotumėte** siekiant keisti esančią grupę.</span><span class="sxs-lookup"><span data-stu-id="3c579-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Rinktis naują ar redaguoti](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="3c579-125">Užpildykite toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="3c579-125">Set the following fields.</span></span>

    | <span data-ttu-id="3c579-126">Laukas</span><span class="sxs-lookup"><span data-stu-id="3c579-126">Field</span></span> | <span data-ttu-id="3c579-127">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3c579-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="3c579-128">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="3c579-128">Name</span></span> | <span data-ttu-id="3c579-129">Įvesti grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3c579-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="3c579-130">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3c579-130">Description</span></span> | <span data-ttu-id="3c579-131">Įveskite grupės aprašą.</span><span class="sxs-lookup"><span data-stu-id="3c579-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="3c579-132">Draudimo pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="3c579-132">Offer of coverage</span></span> | <span data-ttu-id="3c579-133">Aprėptis siūloma darbuotojams, jų sutuoktiniams ar partneriams ir jų išlaikytiniams.</span><span class="sxs-lookup"><span data-stu-id="3c579-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="3c579-134">Darbuotojui tenkanti išlaidų dalis</span><span class="sxs-lookup"><span data-stu-id="3c579-134">Employee share of cost</span></span> | <span data-ttu-id="3c579-135">Suma, už kurią atsakingas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="3c579-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="3c579-136">Taikomas 4980H skyrius dėl saugaus prieglobsčio</span><span class="sxs-lookup"><span data-stu-id="3c579-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="3c579-137">4980H saugaus uosto ar perlaidos atleidimo kodas.</span><span class="sxs-lookup"><span data-stu-id="3c579-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="3c579-138">Plano pradžios mėnuo</span><span class="sxs-lookup"><span data-stu-id="3c579-138">Plan start month</span></span> | <span data-ttu-id="3c579-139">Rinktis kalendorinį mėnesį, kai jūsų išmokos plano metai prasideda.</span><span class="sxs-lookup"><span data-stu-id="3c579-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="3c579-140">Grupė galioja nuo</span><span class="sxs-lookup"><span data-stu-id="3c579-140">Group valid from</span></span> | <span data-ttu-id="3c579-141">Pirmoji data, kada įsigalioja įrašas.</span><span class="sxs-lookup"><span data-stu-id="3c579-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="3c579-142">Grupė galioja iki</span><span class="sxs-lookup"><span data-stu-id="3c579-142">Group valid through</span></span> | <span data-ttu-id="3c579-143">Paskutinė data, kada galioja įrašas.</span><span class="sxs-lookup"><span data-stu-id="3c579-143">The last date when this record is valid.</span></span> <span data-ttu-id="3c579-144">Jei nėra galiojimo pabaigos datos, įveskite **Niekada**.</span><span class="sxs-lookup"><span data-stu-id="3c579-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Kurti aprėpties grupę](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="3c579-146">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="3c579-147">Priskirti kelis darbuotojus išlaikymo priežiūros aprėpties grupei</span><span class="sxs-lookup"><span data-stu-id="3c579-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="3c579-148">Darbo srityje **Išmokų valdymas** rinkitės **Išlaikymo priežiūros aprėpties grupė**.</span><span class="sxs-lookup"><span data-stu-id="3c579-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="3c579-149">Rinktis grupę siekiant priskirti darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="3c579-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="3c579-150">Rinktis **Masinis priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="3c579-150">Select **Mass assignment**.</span></span>

    ![Rinktis Masinis priskyrimas](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="3c579-152">Rinktis darbuotojus sąraše ir tuomet rinktis **Priskirti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Priskirti pasirinktus darbuotojus grupei](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="3c579-154">Išlaikyti kelias aprėpties parinkties versijas</span><span class="sxs-lookup"><span data-stu-id="3c579-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="3c579-155">Galite išlaikyti kelias bet kurios aprėpties grupės versijas.</span><span class="sxs-lookup"><span data-stu-id="3c579-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="3c579-156">Kai kas nors keičiasi jūsų organizacijoje arba siūlomose išmokoste, galite laikyti grupės informaciją naujintą be poreikio kurti naują grupę ar paskirti iš naujo darbuotjous jai.</span><span class="sxs-lookup"><span data-stu-id="3c579-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="3c579-157">Jums sukūrus išlaikytinos priežiūros aprėpties grupę, galite priskirti masiškai darbuotojus jai.</span><span class="sxs-lookup"><span data-stu-id="3c579-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="3c579-158">Galite ir atskirai priskirti darbuotojus grupėms ir nurodyti,ar ACA informacija yra sekama ir pranešama.</span><span class="sxs-lookup"><span data-stu-id="3c579-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="3c579-159">Jei neturite sekti ir pranešti ACA informacijos darbuotojui, galite nustatyti **Pranešti aprėptį** parinktį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="3c579-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="3c579-160">Pavyzdžiui, jums gali reikėti ne viso etato darbuotojų, kuriems nereikia ACA pranešimų.</span><span class="sxs-lookup"><span data-stu-id="3c579-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="3c579-161">Viršyti nustatytas darbuotojui vertes</span><span class="sxs-lookup"><span data-stu-id="3c579-161">Override default values for an employee</span></span>

<span data-ttu-id="3c579-162">Darbuotojams, kurie turi priskirtą išlaikymo priežiūros aprėpties grupę, galite keisti tolesnes parinktis bet kuriems mėnesiams, kuriems reikia kitų verčių:</span><span class="sxs-lookup"><span data-stu-id="3c579-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="3c579-163">Draudimo pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="3c579-163">Offer of coverage</span></span>
- <span data-ttu-id="3c579-164">Darbuotojui tenkanti išlaidų dalis</span><span class="sxs-lookup"><span data-stu-id="3c579-164">Employee share of cost</span></span>
- <span data-ttu-id="3c579-165">Taikomas 4980H skyrius dėl saugaus prieglobsčio</span><span class="sxs-lookup"><span data-stu-id="3c579-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="3c579-166">2020 ACA ataskaitoms, turite pranešti darbo ir namų ZIP kodus Formoje 1095-C.</span><span class="sxs-lookup"><span data-stu-id="3c579-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="3c579-167">Vertės užpildomos automatiškai pagal esamas aktyvias vietas.</span><span class="sxs-lookup"><span data-stu-id="3c579-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="3c579-168">Jei bet kuri vieta skiriasi bet kada metuose, turite viršyti vertę.</span><span class="sxs-lookup"><span data-stu-id="3c579-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="3c579-169">**ZIP kodo** laukelis (eilutę 17) 1095-C ataskaitoje yra užpildomas tik, jei **Aprėpties siūlymas** kode yra **1L** iki **1Q**, kaip štai:</span><span class="sxs-lookup"><span data-stu-id="3c579-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="3c579-170">**1L, 1M, ar 1N:** Pagrindinės gyvenamosios vietos ZIP kodas</span><span class="sxs-lookup"><span data-stu-id="3c579-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="3c579-171">**1O, 1P, ar 1Q:** Pagrindinės darbo vietos ZIP kodas</span><span class="sxs-lookup"><span data-stu-id="3c579-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="3c579-172">Norėdami įvesti išlygas bet kurioms išlaikymo priežiūros aprėpties grupės vertėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c579-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="3c579-173">**Žmogiškuosiuose ištekliuose** darbo srityje pasirinkite **Nuorodos** ir tuomet pasirinkite **Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="3c579-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="3c579-174">Rinkitės darbuotoją sąraše.</span><span class="sxs-lookup"><span data-stu-id="3c579-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="3c579-175">Skirtuke **Įdarbinimas**, **Daugiau informacijos** skyriuje rinkitės **Išlaikymo priežiūros aprėpties grupė**.</span><span class="sxs-lookup"><span data-stu-id="3c579-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Keičiančios vienam darbuotojui parinktys](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="3c579-177">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-177">Select **Edit**.</span></span>
5. <span data-ttu-id="3c579-178">Kiekvienam mėnesiui, kuriam reikia keitimų, rinkitės **Viršyti numatytą** žymimą laukelį ir tada keiskite kitas vertes, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="3c579-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Numatytų verčių viršijimas](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="3c579-180">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="3c579-181">Pranešti apie sveikatos priežiūros draudimą</span><span class="sxs-lookup"><span data-stu-id="3c579-181">Report health care coverage</span></span>

<span data-ttu-id="3c579-182">Turite sekti visus darbuotojo išlaikomu, savarankiško sveikatos priežiūros draudimo atvejus pilno ir nepilno etato darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="3c579-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="3c579-183">Įtraukite visus darbuotojus, kartu su jų išlaikytiniais į 1095-C ataskaitą už mėnesius, kai jie buvo drausti.</span><span class="sxs-lookup"><span data-stu-id="3c579-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="3c579-184">Norėdami nurodyti, ar išmokų planas bus praneštas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c579-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="3c579-185">Darbo srityje **Išmokų valdymas** rinkitės **Išmokų planai**.</span><span class="sxs-lookup"><span data-stu-id="3c579-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="3c579-186">Pasirinkite išmokų planą, kurį pranešite.</span><span class="sxs-lookup"><span data-stu-id="3c579-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="3c579-187">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-187">Select **Edit**.</span></span>
4. <span data-ttu-id="3c579-188">Rinkitės **Pranešti pagal prieinamų sevikatos priežiūros paslaugų akto** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c579-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Sveikatos priežiūros draudimo ataskaitos](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="3c579-190">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-190">Select **Save**.</span></span>

<span data-ttu-id="3c579-191">Jei darbuotojas pasirenka sveikatos priežiūros apimtį išlaikytiniui, jo aprėpties laikotarpis nustatomas pagal datą, kai išlaikytinis buvo įtrauktas ar pašalintas.</span><span class="sxs-lookup"><span data-stu-id="3c579-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="3c579-192">Aprėpties datos priklausiniams yra automatiškai skaičiuojamos pagal laikotarpį, kai išlaikytinis atitiko ir buvo aktyvus plane įsitraukimo metais.</span><span class="sxs-lookup"><span data-stu-id="3c579-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="3c579-193">Kurti 1095-B ir 1095-C formas</span><span class="sxs-lookup"><span data-stu-id="3c579-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="3c579-194">Galite taip pat kurti ACA 1095-B ir 1095-C formas produkte ir tada dalyti juos visiems savo darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="3c579-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="3c579-195">Galite elektroniniu būdu kurti formą 1095-C ir atitinkamą 1094-C perdavimo failą siekiant nusiųsti vidaus pajamų paslaugas (IRS).</span><span class="sxs-lookup"><span data-stu-id="3c579-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="3c579-196">Darbo srityje **Išmokų valdymas**, rinkitės **ACA 1095-B formą** ar **ACA 1095-C formą**.</span><span class="sxs-lookup"><span data-stu-id="3c579-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="3c579-197">Keiskite parametrus kaip reikia ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3c579-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3c579-198">Jei spausdinate 1095-C formas daugiau nei 500 darbuotojų, gausite daugiau nei vieną PDF failą.</span><span class="sxs-lookup"><span data-stu-id="3c579-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="3c579-199">Rekomenduojame jums padidinti vertę **Maksimalus failo dydis megabaitais** laukelį **Dokumento valdymo parametrų** puslapyje iki **150**.</span><span class="sxs-lookup"><span data-stu-id="3c579-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="3c579-200">(Tam, kad greitai atvertumėte tą puslapį, galitet naudoti paieškos laukelį naršymo juostoje.)</span><span class="sxs-lookup"><span data-stu-id="3c579-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Maksimalaus failo dydžio keitimas](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="3c579-202">Norėdami patikrinti savo ataskaitų statusą ir jas peržiūrėti, naudokite paieškos laukelį naršymo juostoje, kad atvertumėte **Elektroninių ataskaitų darbų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="3c579-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Elektroninių ataskaitų darbų puslapio paieška](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="3c579-204">Rinkitės peržiūrimą ataskaitą ir tada rinkitės **Rodyti failus**.</span><span class="sxs-lookup"><span data-stu-id="3c579-204">Select the report to view, and then select **Show files**.</span></span>

    ![Failų rodymas](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="3c579-206">Pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-206">Select **Open**.</span></span>

    ![Failo atidarymas](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="3c579-208">Pranešimų juostoje, kuri pasirodo naršymo lango apačioje, atverkite zip failą ir tada rinkitės ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3c579-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="3c579-209">Galite peržiūrėti ar spausdinti PDF failą.</span><span class="sxs-lookup"><span data-stu-id="3c579-209">You can view or print the PDF file.</span></span>

    ![Pavyzdžio 1095-C forma](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="3c579-211">Peržiūrėti ACA aprėpties informaciją</span><span class="sxs-lookup"><span data-stu-id="3c579-211">View ACA coverage information</span></span>

<span data-ttu-id="3c579-212">**Darbuotojo prieinamų sveikatos priežiūros paslaugų** puslapis rodo šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="3c579-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="3c579-213">Darbuotojai priskirti kiekvienai aprėpties grupei</span><span class="sxs-lookup"><span data-stu-id="3c579-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="3c579-214">Darbuotojai neturintys būti įtraukti į ataskaitą</span><span class="sxs-lookup"><span data-stu-id="3c579-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="3c579-215">Nepriskirti darbuotojai</span><span class="sxs-lookup"><span data-stu-id="3c579-215">Unassigned employees</span></span>

<span data-ttu-id="3c579-216">Norėdami peržiūrėti šią informaciją, imkitės tokių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3c579-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="3c579-217">Darbo srityje **Išmokų valdymas** rinkitės **Darbuotojo priežiūros aprėpties grupė**.</span><span class="sxs-lookup"><span data-stu-id="3c579-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="3c579-218">Laukelyje **Grupės pavadiimas** rinkitės grupę.</span><span class="sxs-lookup"><span data-stu-id="3c579-218">In the **Group name** field, select a group.</span></span>

    ![Aprėpties ACA peržiūra](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="3c579-220">Jei bet kurios iš numatytų verčių prieinamų sveikatos priežiūros paslaugų grupė buvo viršyta, žvaigždutė pasirodo šalia pakeistos vertės.</span><span class="sxs-lookup"><span data-stu-id="3c579-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="3c579-221">Jei vertės visiems 12 mėnesių yra tokios pačios ir jos nebuvo viršytos, vertė pasirodo **Visų 12 mėnesių** stulpelyje.</span><span class="sxs-lookup"><span data-stu-id="3c579-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="3c579-222">Galite peržiūrėti darbuotoją, kuris yra pažymėtas kaip ne ACA pranešamas ir kuris neturi formos 1095-C.</span><span class="sxs-lookup"><span data-stu-id="3c579-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="3c579-223">Laukelyje **Filtruoti pagal** rinkitės **Ne ACA įtraukiamas į ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="3c579-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="3c579-224">Galite peržiūrėti darbuotojus, kurie nėra priskirti grupei ar kurie nėra priskirti pasibaigusiai grupei.</span><span class="sxs-lookup"><span data-stu-id="3c579-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="3c579-225">Laukelyje **Filtruoti pagal** rinkitės **Nepriskirta ar pasibaigusi grupė**.</span><span class="sxs-lookup"><span data-stu-id="3c579-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="3c579-226">Eksportuoti į Excel</span><span class="sxs-lookup"><span data-stu-id="3c579-226">Export to Excel</span></span>

<span data-ttu-id="3c579-227">Norėdami eksportuoti bet kokius sąrašus į „Microsoft Excel“, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="3c579-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="3c579-228">Pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“**.</span><span class="sxs-lookup"><span data-stu-id="3c579-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="3c579-229">Rinkitės **HCM „Human Resources“ laikina lentelė vidaus vartojimui**.</span><span class="sxs-lookup"><span data-stu-id="3c579-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="3c579-230">Rinkitės **Atsisiųsti**.</span><span class="sxs-lookup"><span data-stu-id="3c579-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="3c579-231">Peržiūrėti ACA ataskaitos išlaikytinius</span><span class="sxs-lookup"><span data-stu-id="3c579-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="3c579-232">Jums būtina pranešti apdraustus asmenis, nes suteikiate savarankišką draudimą, galite peržiūrėti visus išlaikytinius, kurie apdrausti išmokų planais ir pažymėti kaip **ACA pranešama**.</span><span class="sxs-lookup"><span data-stu-id="3c579-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="3c579-233">Veiksmų juostoje rinkitės **Žiūrėti išlaikytinių draudimą**.</span><span class="sxs-lookup"><span data-stu-id="3c579-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Aprėpties išlaikytinio peržiūra](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="3c579-235">Aprėpties informacija darbuotojo išlaikytiniams yra rodoma.</span><span class="sxs-lookup"><span data-stu-id="3c579-235">Coverage information for the employee's dependents is shown.</span></span>

![Išlaikytinių draudimas](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="3c579-237">Puslapis rodo tik išmokų planus, kurie pažymėti kaip **ACA pranešami**.</span><span class="sxs-lookup"><span data-stu-id="3c579-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]