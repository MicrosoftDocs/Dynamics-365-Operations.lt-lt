---
title: Projekto biudžetų perkėlimas finansinių metų pabaigoje
description: Šiame straipsnyje pateikiama inoformation apie tai, kaip perkelti likusias biudžeto sumas į būsimus metus ir sukurti biudžeto registro informaciją.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172335"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="af0c7-103">Projekto biudžetų perkėlimas finansinių metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="af0c7-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af0c7-104">Dirbant su daugiamečiu projektu gali likti biudžeto finansinių metų pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="af0c7-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="af0c7-105">Galite perkelti likusias biudžeto sumas būsimiems metams ir sukurti tų sumų biudžeto registro išsamią informaciją susietosiose DK sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="af0c7-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="af0c7-106">Prieš perkeldami likusias sumas, peržiūrėkite ir išanalizuokite likusias biudžeto sumas.</span><span class="sxs-lookup"><span data-stu-id="af0c7-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="af0c7-107">Likusių biudžeto sumų peržiūra ir analizė</span><span class="sxs-lookup"><span data-stu-id="af0c7-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="af0c7-108">Atlikite toliau nurodytus veiksmus, kad peržiūrėtumėte metų pabaigos biudžeto sumas, taikomas projektams, jų neperkeldami.</span><span class="sxs-lookup"><span data-stu-id="af0c7-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="af0c7-109">Eikite į **Projektų valdymas ir apskaita** > **Periodiniai** > **Biudžetai** > **Perkeliami biudžetai**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="af0c7-110">Puslapyje **Projekto biudžeto perkėlimo procesas**, skirtuke **Metų pabaigos parinktys**, patikrinkite, ar neįgalinta **Perkelti likusias projekto biudžeto sumas**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="af0c7-111">Skirtuke **Parametrai** tab, lauke **Projekto biudžeto metai**, pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="af0c7-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="af0c7-112">Lauke **Atviri finansiniai metai** pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="af0c7-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="af0c7-113">Lauke **Iš prognozės modelio** pasirinkite **Likęs biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="af0c7-114">Norėdami įtraukti atitinkančius pasirinktus kriterijus ir neturinčius likusio biudžeto projektus, pasirinkite **Rodyti nulinį likutį**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="af0c7-115">Skirtuke **Pasirinkti biudžetus** pasirinkite **Grąžinti visus biudžetus**, kad būtų įkelti visi jūsų pasirinktus kriterijus atitinkantys biudžetai, tada pasirinkite **Apdoroti**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="af0c7-116">Norėdami sukurti duomenų bazės užklausą, kuri įkelia konkretų biudžetų rinkinį į sritį, pasirinkite **Grąžinti pasirinktus biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="af0c7-117">Norėdami gauti daugiau informacijos apie konkrečią srities eilutę, pasirinkite eilutę ir pasirinkite **Peržiūrėti biudžeto išsamią informaciją** arba **Peržiūrėti sąskaitas**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="af0c7-118">Likusių biudžeto sumų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="af0c7-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="af0c7-119">Kai apdorojate likusias biudžeto sumas, galite sukurti operacijas DK, taikomas sumoms, kurias perkeliate.</span><span class="sxs-lookup"><span data-stu-id="af0c7-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="af0c7-120">Norėdami sukurti DK operacijas, atlikite skyriaus veiksmus, [Biudžeto sumų perkėlimas kuriant DK operacijas](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="af0c7-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="af0c7-121">Perkeliamos biudžeto sumos perkeliamos į prognozės modelį, kuris pasirinktas puslapyje **Prognozių modeliai** kaip perkėlimo prognozės modelis.</span><span class="sxs-lookup"><span data-stu-id="af0c7-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="af0c7-122">Biudžeto sumų perkėlimas kuriant DK operacijas</span><span class="sxs-lookup"><span data-stu-id="af0c7-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="af0c7-123">Pasirinkite **Projektų valdymas ir apskaita** > **Periodiniai** > **Biudžetai** > **Perkeliami biudžetai**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="af0c7-124">Puslapyje **Projekto biudžeto perkėlimo procesas** pasirinkite **Metų pabaiga** ir įgalinkite **Perkelti likusias projekto biudžeto sumas** ir **Sukurti biudžeto registro įrašus DK**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="af0c7-125">Skirtuke **Parametrai**, esančiame laukų grupėje **Projekto parametrai**, pasirinkite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="af0c7-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="af0c7-126">**Projekto biudžeto metai**: pasirinkite finansinių metų, kurių likusias biudžeto sumas norite peržiūrėti, pradžią.</span><span class="sxs-lookup"><span data-stu-id="af0c7-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="af0c7-127">**Pelnas ir nuostolis**: sukurkite pelno ir nuostolio operacijų Didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="af0c7-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="af0c7-128">**NG**: sukurkite nebaigtos gamybos (NG) operacijų Didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="af0c7-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="af0c7-129">**Algalapis**: sukurkite algalapių paskirstymo operacijų Didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="af0c7-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="af0c7-130">Laukų grupėje **Didžioji knyga** pateikta toliau nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="af0c7-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="af0c7-131">Lauke **Atviri finansiniai metai** pasirinkite finansinių metų, į kuriuos norite perkelti likusias biudžeto sumas, taikomas projektams.</span><span class="sxs-lookup"><span data-stu-id="af0c7-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="af0c7-132">Numatytoji reikšmė yra vieni metai po reikšmės, nurodytos lauke **Projekto biudžeto metai**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="af0c7-133">Lauke **Perkeliamas laikotarpis** pasirinkite laikotarpį, kuriam DK norite sukurti biudžeto registro išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="af0c7-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="af0c7-134">Taip paprastai yra pirmasis atvirų finansinių metų laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="af0c7-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="af0c7-135">Laukų grupėje **Kopijuoti iš / į** pateikta toliau nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="af0c7-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="af0c7-136">Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis biudžeto sumomis, taikomomis projektams, kurias norite perkelti.</span><span class="sxs-lookup"><span data-stu-id="af0c7-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="af0c7-137">Lauke **Į DK biudžeto modelį** pasirinkite DK biudžeto modelį, susietą su biudžeto sumomis,, kurias norite perkelti į DK.</span><span class="sxs-lookup"><span data-stu-id="af0c7-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="af0c7-138">Norėdami naudoti projekto pardavimo valiutą DK operacijose, kurios sukurtos perkeliant biudžeto sumas, taikomas projektams, pažymėkite **Perkelti pardavimo valiutą**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="af0c7-139">Jei parinktis nepažymėta, operacijos naudoja apskaitos valiutą.</span><span class="sxs-lookup"><span data-stu-id="af0c7-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="af0c7-140">Norėdami įtraukti projektus, kurių likusių biudžeto sumų nėra, bet kurie atitinka kitus kriterijus, kuriuos pasirinkote apatinėje srityje rodomiems projektams, pažymėkite **Rodyti nulinį likutį**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="af0c7-141">Skirtuke **Pasirinkti biudžetus** pasirinkite **Grąžinti visus biudžetus**, kad būtų įkelti visi jūsų pasirinktus kriterijus atitinkantys biudžetai.</span><span class="sxs-lookup"><span data-stu-id="af0c7-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="af0c7-142">Jei pageidaujate, galite sukurti duomenų bazės užklausą, kuri įkelia konkretų projekto biudžetų rinkinį į sritį, pasirinkite **Grąžinti pasirinktus biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="af0c7-143">Pažymėkite kiekvieno norimo apdoroti projekto parinktį projekto eilutės pradžioje.</span><span class="sxs-lookup"><span data-stu-id="af0c7-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="af0c7-144">Norėdami pasirinkti visus arba daugumą projektų, viršutiniame kairiajame kampe pasirinkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="af0c7-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="af0c7-145">Norėdami neįtraukti projekto apdorojimo, atžymėkite projekto žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="af0c7-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="af0c7-146">Pasirinkite **Apdoroti**, norėdami perkelti likusias biudžeto sumas, taikomas pasirinktiems projektams, į pasirinktus finansinius metus ir sukurtumėte biudžeto registro išsamią informaciją DK.</span><span class="sxs-lookup"><span data-stu-id="af0c7-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="af0c7-147">Biudžeto sumų perkėlimas nekuriant DK operacijų</span><span class="sxs-lookup"><span data-stu-id="af0c7-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="af0c7-148">Eikite į **Projektų valdymas ir apskaita** > **Periodiniai** > **Biudžetai** > **Perkeliami biudžetai**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="af0c7-149">Puslapyje **Projekto biudžeto perkėlimo procesas**, lauke **Metų pabaigos parinktys**, pasirinkite **Perkelti likusias projekto biudžeto sumas**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="af0c7-150">Grupėje **Parametrai**, lauke **Projekto biudžeto metai**, pasirinkite finansinius metus, kurių likusias biudžeto sumas norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="af0c7-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="af0c7-151">Grupėje **Kopijuoti iš / į** pateikta toliau nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="af0c7-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="af0c7-152">Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis biudžeto sumomis, taikomomis projektams, kurias norite perkelti.</span><span class="sxs-lookup"><span data-stu-id="af0c7-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="af0c7-153">Pasirinkite **Rodyti nulinį likutį**, norėdami įtraukti neturinčius likusio biudžeto sumų, tačiau atitinkančius kitus pasirinktus kriterijus, projektus.</span><span class="sxs-lookup"><span data-stu-id="af0c7-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="af0c7-154">Grupėje **Pasirinkti biudžetus** pasirinkite **Grąžinti visus biudžetus**, kad būtų įkelti visi jūsų pasirinktus kriterijus atitinkantys biudžetai.</span><span class="sxs-lookup"><span data-stu-id="af0c7-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="af0c7-155">Norėdami sukurti duomenų bazės užklausą, kuri įkelia konkretų projekto biudžetų rinkinį į sritį, pasirinkite **Grąžinti pasirinktus biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="af0c7-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="af0c7-156">Pažymėkite kiekvieno norimo apdoroti projekto parinktį projekto eilutės pradžioje.</span><span class="sxs-lookup"><span data-stu-id="af0c7-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="af0c7-157">Pasirinkite **Apdoroti**, kad perkeltumėte likusias biudžeto sumas, taikomas pasirinktiems projektams, į pasirinktus finansinius metus.</span><span class="sxs-lookup"><span data-stu-id="af0c7-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

