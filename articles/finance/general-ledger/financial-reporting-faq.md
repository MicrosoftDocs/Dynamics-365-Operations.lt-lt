---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami klausimai, susiję su finansinėmis ataskaitomis, kurias turėjo kiti vartotojai.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923030"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="8635b-103">DUK apie finansines ataskaitas</span><span class="sxs-lookup"><span data-stu-id="8635b-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="8635b-104">Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus apie finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="8635b-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="8635b-105">Kaip apriboti prieigą prie ataskaitos naudojant medžio saugą?</span><span class="sxs-lookup"><span data-stu-id="8635b-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="8635b-106">Toliau pateikiamu pavyzdžiu nurodoma, kaip apriboti prieigą prie ataskaitos naudojant medžio saugą.</span><span class="sxs-lookup"><span data-stu-id="8635b-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="8635b-107">Demonstracinė įmonė USMF turi balanso ataskaitą, prie kurios ne visi finansinių ataskaitų vartotojai turi turėti prieigą.</span><span class="sxs-lookup"><span data-stu-id="8635b-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="8635b-108">Norėdami apriboti prieigą galite naudoti medžio saugą, kad apribotumėte prieigą prie vienos ataskaitos ir tik tam tikri vartotojai galėtų pasiekti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="8635b-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="8635b-109">Norėdami apriboti prieigą, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8635b-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="8635b-110">Prisijunkite prie „Financial Reporter Report Designer“.</span><span class="sxs-lookup"><span data-stu-id="8635b-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="8635b-111">Sukurkite naują medžio aprašą.</span><span class="sxs-lookup"><span data-stu-id="8635b-111">Create a new tree definition.</span></span> <span data-ttu-id="8635b-112">Eikite į **Failas > Naujas > Medžio aprašas**.</span><span class="sxs-lookup"><span data-stu-id="8635b-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="8635b-113">Dukart spustelėkite eilutę **Suvestinė** stulpelyje **Vieneto sauga**.</span><span class="sxs-lookup"><span data-stu-id="8635b-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="8635b-114">Pasirinkite **Vartotojai ir grupės**.</span><span class="sxs-lookup"><span data-stu-id="8635b-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="8635b-115">Pasirinkite vartotojus ar grupes, kuriems reikalinga prieiga prie ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="8635b-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="8635b-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="8635b-116">Select **Save**.</span></span>
7. <span data-ttu-id="8635b-117">Į ataskaitos aprašą įtraukite naują medžio aprašą.</span><span class="sxs-lookup"><span data-stu-id="8635b-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="8635b-118">Medžio apraše pasirinkite **Parametras**.</span><span class="sxs-lookup"><span data-stu-id="8635b-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="8635b-119">Dalyje **Ataskaitos vieneto pasirinkimas** pasirinkite **Įtraukti visus vienetus**.</span><span class="sxs-lookup"><span data-stu-id="8635b-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="8635b-120">Kaip nustatyti, kurios sąskaitos neatitinka mano balansų?</span><span class="sxs-lookup"><span data-stu-id="8635b-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="8635b-121">Jei turite ataskaitą, kurioje nėra atitinkančių balansų, štai keli veiksmai, kuriuos galite atlikti norėdami nustatyti kiekvieną sąskaitą ir nukrypimą.</span><span class="sxs-lookup"><span data-stu-id="8635b-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="8635b-122">**„Financial Reporter Report Designer“**</span><span class="sxs-lookup"><span data-stu-id="8635b-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="8635b-123">Naudodami „Financial Reporter Report Designer“, sukurkite naują eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="8635b-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="8635b-124">Pasirinkite **Redaguoti > Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="8635b-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="8635b-125">Pasirinkite **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="8635b-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="8635b-126">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8635b-126">Select **OK**.</span></span>
5. <span data-ttu-id="8635b-127">Įrašykite eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="8635b-127">Save the row definition.</span></span>
6. <span data-ttu-id="8635b-128">Sukurkite naują eilutės aprašą</span><span class="sxs-lookup"><span data-stu-id="8635b-128">Create a new column definition</span></span>
7. <span data-ttu-id="8635b-129">Sukurkite naują ataskaitos aprašą.</span><span class="sxs-lookup"><span data-stu-id="8635b-129">Create a new report definition.</span></span>
8. <span data-ttu-id="8635b-130">Pasirinkite **Parametrai** ir atžymėkite šią parinktį.</span><span class="sxs-lookup"><span data-stu-id="8635b-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="8635b-131">Generuokite ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="8635b-131">Generate the report.</span></span> 
10. <span data-ttu-id="8635b-132">Eksportuokite ataskaitą į „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="8635b-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="8635b-133">**„Dynamics 365 Finance“**</span><span class="sxs-lookup"><span data-stu-id="8635b-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="8635b-134">„Dynamics 365 Finance“ eikite į **Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas**.</span><span class="sxs-lookup"><span data-stu-id="8635b-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="8635b-135">Nustatykite šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="8635b-135">Set the following parameters:</span></span>
   - <span data-ttu-id="8635b-136">**Pradžios data** – įveskite finansinių metų pradžią.</span><span class="sxs-lookup"><span data-stu-id="8635b-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="8635b-137">**Pabaigos data** – įveskite datą, kuriai generuojate ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="8635b-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="8635b-138">**Finansinė dimensija** – nustatykite šį lauką kaip **Pagrindinė sąskaita nustatyta**.</span><span class="sxs-lookup"><span data-stu-id="8635b-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="8635b-139">Pasirinkite **Skaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="8635b-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="8635b-140">Eksportuokite ataskaitą į „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="8635b-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="8635b-141">Dabar turėtų būti galima kopijuoti duomenis iš finansinių ataskaitų rengėjų „Excel“ ataskaitos į bandomojo balanso ataskaitą, kad galėtumėte palyginti **uždarymo balanso** stulpelius.</span><span class="sxs-lookup"><span data-stu-id="8635b-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]