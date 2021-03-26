---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami klausimai, susiję su finansinėmis ataskaitomis, kurias turėjo kiti vartotojai.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249312"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d1305-103">DUK apie finansines ataskaitas</span><span class="sxs-lookup"><span data-stu-id="d1305-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="d1305-104">Šioje temoje pateikiami klausimai, susiję su finansinėmis ataskaitomis, kurias turėjo kiti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="d1305-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="d1305-105">Kaip apriboti prieigą prie ataskaitos naudojant medžio saugą?</span><span class="sxs-lookup"><span data-stu-id="d1305-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="d1305-106">Scenarijus: USMF demonstracinė įmonė turi balanso ataskaitą ir nenori, kad visi finansinių ataskaitų vartotojai galėtų peržiūrėti naudodami D365.</span><span class="sxs-lookup"><span data-stu-id="d1305-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="d1305-107">Sprendimas: galite naudoti medžio saugą, kad apribotumėte prieigą prie vienos ataskaitos, kad tik tam tikri vartotojai galėtų pasiekti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="d1305-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="d1305-108">Prisijunkite prie finansinių ataskaitų rengėjų ataskaitų dizaino įrankio</span><span class="sxs-lookup"><span data-stu-id="d1305-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="d1305-109">Sukurkite naują medžio apibrėžimą (Failas | Naujas | Medžio aprašas) a.</span><span class="sxs-lookup"><span data-stu-id="d1305-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="d1305-110">Dukart spustelėkite eilutę **Suvestinė** stulpelyje **Vieneto sauga**.</span><span class="sxs-lookup"><span data-stu-id="d1305-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="d1305-111">i.</span><span class="sxs-lookup"><span data-stu-id="d1305-111">i.</span></span>    <span data-ttu-id="d1305-112">Spustelėkite Vartotojai ir grupės.</span><span class="sxs-lookup"><span data-stu-id="d1305-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="d1305-113">1. Pasirinkite vartotojus ar grupę, kuri galės pasiekti šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="d1305-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="d1305-114">[![vartotojo ekranas](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="d1305-115">[![saugos ekranas](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1305-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="d1305-116">b.</span><span class="sxs-lookup"><span data-stu-id="d1305-116">b.</span></span>    <span data-ttu-id="d1305-117">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d1305-117">Click **Save**.</span></span>
  
<span data-ttu-id="d1305-118">[![įrašymo mygtukas](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="d1305-119">Savo ataskaitos apraše įtraukite naują medžio aprašą</span><span class="sxs-lookup"><span data-stu-id="d1305-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="d1305-120">[![medžio aprašo forma](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1305-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="d1305-121">A.</span><span class="sxs-lookup"><span data-stu-id="d1305-121">A.</span></span>  <span data-ttu-id="d1305-122">Medžio apraše spustelėkite Parametras ir dalyje Ataskaitos vieneto pasirinkimas pažymėkite Įtraukti visus vienetus</span><span class="sxs-lookup"><span data-stu-id="d1305-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="d1305-123">[![ataskaitos vieneto pasirinkimo forma](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1305-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="d1305-124">**Prieš:** [![ekrano nuotrauka](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="d1305-125">**Po:** [![ekrano nuotrauka](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="d1305-126">Pastaba: pirmiau pateikto pranešimo priežastis ta, kad mano vartotojas neturi prieigos prie šios ataskaitos pritaikius vieneto saugą</span><span class="sxs-lookup"><span data-stu-id="d1305-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="d1305-127">Kaip nustatyti, kurios sąskaitos neatitinka mano balansų D365?</span><span class="sxs-lookup"><span data-stu-id="d1305-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="d1305-128">Kai turite ataskaitą, kuri neatitinka to, ko tikitės iš D365, štai keli veiksmai, kuriuos galite atlikti norėdami nustatyti šias sąskaitas ir nukrypimus.</span><span class="sxs-lookup"><span data-stu-id="d1305-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="d1305-129">Naudodami finansinių ataskaitų rengėjų ataskaitų dizaino įrankį</span><span class="sxs-lookup"><span data-stu-id="d1305-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="d1305-130">Sukurkite naują eilutės aprašą a.</span><span class="sxs-lookup"><span data-stu-id="d1305-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="d1305-131">Spustelėkite Redaguoti | Įterpti eilutes iš dimensijų i.</span><span class="sxs-lookup"><span data-stu-id="d1305-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="d1305-132">Pasirinkite MainAccount [![Pasirinkite Pagrindinis ekranas_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="d1305-133">ii.</span><span class="sxs-lookup"><span data-stu-id="d1305-133">ii.</span></span> <span data-ttu-id="d1305-134">Spustelėkite Gerai b.</span><span class="sxs-lookup"><span data-stu-id="d1305-134">Click Ok b.</span></span>    <span data-ttu-id="d1305-135">Eilutės aprašo įrašymas</span><span class="sxs-lookup"><span data-stu-id="d1305-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="d1305-136">Naujo stulpelio aprašo kūrimas [![Naujo stulpelio aprašo kūrimas](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="d1305-137">Sukurkite naują ataskaitos aprašą a.</span><span class="sxs-lookup"><span data-stu-id="d1305-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="d1305-138">Spustelėkite Parametrai ir atžymėkite [![formą Parametrai](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="d1305-139">Generuokite ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="d1305-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="d1305-140">Eksportuokite ataskaitą į „Excel“.</span><span class="sxs-lookup"><span data-stu-id="d1305-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="d1305-141">Naudodami D365:</span><span class="sxs-lookup"><span data-stu-id="d1305-141">In D365:</span></span> 
1.  <span data-ttu-id="d1305-142">Spustelėkite DK | Užklausos ir ataskaitos | Bandomasis balansas a.</span><span class="sxs-lookup"><span data-stu-id="d1305-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="d1305-143">Parametrai i.</span><span class="sxs-lookup"><span data-stu-id="d1305-143">Parameters i.</span></span>  <span data-ttu-id="d1305-144">Pradžios data: finansinių metų pradžia ii.</span><span class="sxs-lookup"><span data-stu-id="d1305-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="d1305-145">Pabaigos data: data, kuriai sugeneravote ataskaitą iii.</span><span class="sxs-lookup"><span data-stu-id="d1305-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="d1305-146">Finansinių dimensijų rinkinys „Pagrindinės sąskaitos rinkinys“ [![Pagrindinės sąskaitos forma](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="d1305-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="d1305-147">b.</span><span class="sxs-lookup"><span data-stu-id="d1305-147">b.</span></span>    <span data-ttu-id="d1305-148">Spustelėkite Skaičiuoti</span><span class="sxs-lookup"><span data-stu-id="d1305-148">Click Calculate</span></span>

2.  <span data-ttu-id="d1305-149">Ataskaitos eksportavimas į „Excel“</span><span class="sxs-lookup"><span data-stu-id="d1305-149">Export the report to Excel</span></span>

<span data-ttu-id="d1305-150">Dabar turėtų būti galima kopijuoti duomenis iš FR „Excel“ ataskaitos į D365 bandomojo balanso ataskaitą ir palyginti uždarymo balanso stulpelius.</span><span class="sxs-lookup"><span data-stu-id="d1305-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]