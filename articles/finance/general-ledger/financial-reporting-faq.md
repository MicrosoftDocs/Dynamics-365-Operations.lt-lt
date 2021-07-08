---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie finansines ataskaitas.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266638"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="02b66-103">DUK apie finansines ataskaitas</span><span class="sxs-lookup"><span data-stu-id="02b66-103">Financial reporting FAQ</span></span>

<span data-ttu-id="02b66-104">Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus apie finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="02b66-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="02b66-105">Kaip apriboti prieigą prie ataskaitos naudojant medžio saugą?</span><span class="sxs-lookup"><span data-stu-id="02b66-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="02b66-106">Toliau pateikiamu pavyzdžiu nurodoma, kaip apriboti prieigą prie ataskaitos naudojant medžio saugą.</span><span class="sxs-lookup"><span data-stu-id="02b66-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="02b66-107">Demonstracinė įmonė USMF turi **balanso ataskaitą** , prie kurios ne visi finansinių ataskaitų vartotojai turi turėti prieigą.</span><span class="sxs-lookup"><span data-stu-id="02b66-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="02b66-108">Galite naudoti medžio saugą, kad apribotumėte prieigą prie vienos ataskaitos, kad tik tam tikri vartotojai galėtų ją pasiekti.</span><span class="sxs-lookup"><span data-stu-id="02b66-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="02b66-109">Prisijungti prie „Financial Reporter Report Designer”.</span><span class="sxs-lookup"><span data-stu-id="02b66-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="02b66-110">Pasirinkite **Failas \> Naujas \> Medžio aprašas**, kad sukurtumėte naują medžio aprašą.</span><span class="sxs-lookup"><span data-stu-id="02b66-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="02b66-111">Dukart bakstelėkite (arba dukart spustelėkite) eilutę **Suvestinė** stulpelyje **Vieneto sauga**.</span><span class="sxs-lookup"><span data-stu-id="02b66-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="02b66-112">Pasirinkite **Vartotojai ir grupės**.</span><span class="sxs-lookup"><span data-stu-id="02b66-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="02b66-113">Pasirinkite vartotojus ar grupes, kuriems reikalinga prieiga prie ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="02b66-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="02b66-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="02b66-114">Select **Save**.</span></span>
7. <span data-ttu-id="02b66-115">Į ataskaitos aprašą įtraukite naują medžio aprašą.</span><span class="sxs-lookup"><span data-stu-id="02b66-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="02b66-116">Medžio apraše pasirinkite **Parametras**.</span><span class="sxs-lookup"><span data-stu-id="02b66-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="02b66-117">Tada dalyje **Ataskaitos vieneto pasirinkimas** pasirinkite **Įtraukti visus vienetus**.</span><span class="sxs-lookup"><span data-stu-id="02b66-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="02b66-118">Kaip nustatyti, kurios sąskaitos neatitinka mano balansų?</span><span class="sxs-lookup"><span data-stu-id="02b66-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="02b66-119">Jei turite ataskaitą, kurioje nėra atitinkančių balansų, naudokite toliau pateikiamas procedūras norėdami nustatyti kiekvieną paskyrą ir nukrypimą.</span><span class="sxs-lookup"><span data-stu-id="02b66-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="02b66-120">„Financial Reporter Report Designer“</span><span class="sxs-lookup"><span data-stu-id="02b66-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="02b66-121">Sukurkite naują eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="02b66-121">Create a new row definition.</span></span>
2. <span data-ttu-id="02b66-122">Pasirinkite **Redaguoti \> Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="02b66-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="02b66-123">Pasirinkite **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="02b66-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="02b66-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="02b66-124">Select **OK**.</span></span>
5. <span data-ttu-id="02b66-125">Įrašykite eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="02b66-125">Save the row definition.</span></span>
6. <span data-ttu-id="02b66-126">Sukurkite naują stulpelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="02b66-126">Create a new column definition.</span></span>
7. <span data-ttu-id="02b66-127">Sukurkite naują ataskaitos aprašą.</span><span class="sxs-lookup"><span data-stu-id="02b66-127">Create a new report definition.</span></span>
8. <span data-ttu-id="02b66-128">Pasirinkite **Parametrai** ir atžymėkite šią parinktį.</span><span class="sxs-lookup"><span data-stu-id="02b66-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="02b66-129">Generuokite ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="02b66-129">Generate the report.</span></span> 
10. <span data-ttu-id="02b66-130">Eksportuokite ataskaitą į „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="02b66-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="02b66-131">„Dynamics 365 Finance“</span><span class="sxs-lookup"><span data-stu-id="02b66-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="02b66-132">Eikite į **Didžioji knyga \> Užklausos ir ataskaitos \> Bandomasis balansas**.</span><span class="sxs-lookup"><span data-stu-id="02b66-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="02b66-133">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="02b66-133">Set the following fields:</span></span>

    - <span data-ttu-id="02b66-134">**Pradžios data** – įveskite finansinių metų pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="02b66-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="02b66-135">**Pabaigos data** – įveskite datą, kuriai generuojate ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="02b66-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="02b66-136">**Finansinė dimensija** – nustatykite šį lauką kaip **Pagrindinė sąskaita nustatyta**.</span><span class="sxs-lookup"><span data-stu-id="02b66-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="02b66-137">Pasirinkite **Skaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="02b66-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="02b66-138">Eksportuokite ataskaitą į „Excel“.</span><span class="sxs-lookup"><span data-stu-id="02b66-138">Export the report to Excel.</span></span>

<span data-ttu-id="02b66-139">Dabar turėtų būti galima kopijuoti duomenis iš „Financial Reporter“ „Excel“ ataskaitos į **bandomojo balanso** ataskaitą, kad galėtumėte palyginti **uždarymo balanso** stulpelius.</span><span class="sxs-lookup"><span data-stu-id="02b66-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="02b66-140">Kai kuriu ataskaitą „Report Designer“ arba generuoju finansinę ataskaitą, gaunu šį pranešimą: „Operacijos nepavyko užbaigti dėl duomenų teikėjo sistemos problemos“.</span><span class="sxs-lookup"><span data-stu-id="02b66-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="02b66-141">Kaip turėčiau atsakyti?</span><span class="sxs-lookup"><span data-stu-id="02b66-141">How should I respond?</span></span>

<span data-ttu-id="02b66-142">Pranešimas nurodo, kad problema įvyko, kai sistema bandė nuskaityti finansinius metaduomenis iš duomenų srities, kol naudojote finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="02b66-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="02b66-143">Yra du būdai atsakyti į šią problemą:</span><span class="sxs-lookup"><span data-stu-id="02b66-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="02b66-144">Peržiūrėkite duomenų integravimo būseną „Report Designer“ eidami į **Įrankiai \> Integravimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="02b66-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="02b66-145">Jei integravimas neužbaigtas, palaukite, kol jis bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="02b66-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="02b66-146">Tada, kartokite tai, ką darėte, kai gavote pranešimą.</span><span class="sxs-lookup"><span data-stu-id="02b66-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="02b66-147">Norėdami nustatyti ir išspręsti problemą, susisiekite su palaikymo tarnyba.</span><span class="sxs-lookup"><span data-stu-id="02b66-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="02b66-148">Sistemoje gali būti pateikti nenuoseklūs duomenys.</span><span class="sxs-lookup"><span data-stu-id="02b66-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="02b66-149">Palaikymo inžinieriai gali padėti nustatyti problemą serveryje ir rasti konkrečius duomenis, kuriuos gali reikėti atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="02b66-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
