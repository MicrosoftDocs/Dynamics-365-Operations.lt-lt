---
title: Bandomojo balanso finansinės ataskaitos
description: Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25a90a137ea3f6dfa43f401354780d99b2fda8fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978491"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="30300-104">Bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="30300-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30300-105">Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="30300-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="30300-106">Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.</span><span class="sxs-lookup"><span data-stu-id="30300-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="30300-107">Numatytosios bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="30300-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="30300-108">Finansinėse ataskaitose galimos trys bandomojo balanso ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="30300-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="30300-109">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="30300-109">Default report</span></span>                                 | <span data-ttu-id="30300-110">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="30300-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30300-111">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="30300-112">Joje pateikiama visų sąskaitų balanso informaciją ir debeto bei kredito balansai ir jų grynosios reikšmės, taip pat operacijos data, kvitas ir žurnalo aprašymas.</span><span class="sxs-lookup"><span data-stu-id="30300-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="30300-113">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="30300-114">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="30300-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="30300-115">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="30300-116">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų šių ir praėjusių metų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="30300-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="30300-117">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="30300-117">Building blocks</span></span>
<span data-ttu-id="30300-118">Bandomojo balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="30300-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="30300-119">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="30300-119">Default report</span></span>                                 | <span data-ttu-id="30300-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="30300-120">Row definition</span></span>          | <span data-ttu-id="30300-121">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="30300-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="30300-122">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="30300-123">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="30300-123">Trial Balance - Default</span></span> | <span data-ttu-id="30300-124">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="30300-125">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="30300-126">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="30300-126">Trial Balance - Default</span></span> | <span data-ttu-id="30300-127">Bandomojo balanso suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="30300-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="30300-128">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="30300-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="30300-129">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="30300-129">Trial Balance - Default</span></span> | <span data-ttu-id="30300-130">Bandomojo balanso suvestinė metams bėgant – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="30300-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="30300-131">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="30300-131">Row definition</span></span>

<span data-ttu-id="30300-132">Eilutės apibrėžime Bandomasis balansas – numatytasis yra viena eilutė, į kurią įtrauktos visos pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="30300-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="30300-133">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="30300-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="30300-134">Kai peržiūrite ataskaitą, detalizuojate vieną eilutę, kad pamatytumėte išsamią informaciją apie kiekvieną sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="30300-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="30300-135">Galite keisti eilutės apibrėžimą, kad į ją būtų įtraukta daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="30300-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="30300-136">Norėdami keisti eilutės Bandomasis balansas – Numatytasis apibrėžimą, kad į ją būtų įtrauktos visų sąskaitų eilutės, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="30300-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="30300-137">Spustelėkite **Redaguoti**, tada spustelėkite **Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="30300-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="30300-138">Komanda **Įterpti eilutes iš dimensijų** leidžia pasirinkti, kokias dimensijas norite turėti savo eilutės apibrėžime.</span><span class="sxs-lookup"><span data-stu-id="30300-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="30300-139">Šiam eilutės apibrėžimui naudosite **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="30300-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="30300-140">Įsitikinkite, kad dalyje **Pagrindinė sąskaita** yra visi konjunkcijos ženklai (&), tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="30300-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="30300-141">Dabar eilutės apibrėžime yra visos jūsų numatytojo juridinio subjekto pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="30300-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="30300-142">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="30300-142">Column definition</span></span>

<span data-ttu-id="30300-143">Kiekvienoje bandomojo balanso ataskaitoje naudojamas kitas stulpelio aprašas.</span><span class="sxs-lookup"><span data-stu-id="30300-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="30300-144">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, šiuose stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="30300-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="30300-145">**Išsamus bandomasis balansas – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="30300-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="30300-146">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="30300-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="30300-147">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="30300-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="30300-148">**ATTR (3)** – Atributai:</span><span class="sxs-lookup"><span data-stu-id="30300-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="30300-149">Operacijos data</span><span class="sxs-lookup"><span data-stu-id="30300-149">Transaction Date</span></span>
        -   <span data-ttu-id="30300-150">Kvitas</span><span class="sxs-lookup"><span data-stu-id="30300-150">Voucher</span></span>
        -   <span data-ttu-id="30300-151">Žurnalo aprašymas</span><span class="sxs-lookup"><span data-stu-id="30300-151">Journal Description</span></span>
    -   <span data-ttu-id="30300-152">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="30300-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="30300-153">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="30300-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="30300-154">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="30300-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="30300-155">**Bandomojo balanso suvestinė – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="30300-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="30300-156">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="30300-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="30300-157">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="30300-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="30300-158">**ATTR** – Atributas:</span><span class="sxs-lookup"><span data-stu-id="30300-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="30300-159">Kvitas</span><span class="sxs-lookup"><span data-stu-id="30300-159">Voucher</span></span>
    -   <span data-ttu-id="30300-160">**FD** – Pradžios balanso finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="30300-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="30300-161">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="30300-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="30300-162">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="30300-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="30300-163">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="30300-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="30300-164">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="30300-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="30300-165">**Bandomojo balanso suvestinė metams bėgant – Numatytoji:**</span><span class="sxs-lookup"><span data-stu-id="30300-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="30300-166">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="30300-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="30300-167">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="30300-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="30300-168">**ATTR** – Atributas</span><span class="sxs-lookup"><span data-stu-id="30300-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="30300-169">Kvitas</span><span class="sxs-lookup"><span data-stu-id="30300-169">Voucher</span></span>
    -   <span data-ttu-id="30300-170">**FD** – Pradžios balanso šių metų finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="30300-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="30300-171">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų debetas</span><span class="sxs-lookup"><span data-stu-id="30300-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="30300-172">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="30300-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="30300-173">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="30300-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="30300-174">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="30300-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="30300-175">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų debetas</span><span class="sxs-lookup"><span data-stu-id="30300-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="30300-176">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="30300-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="30300-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="30300-177">Additional resources</span></span>
--------

[<span data-ttu-id="30300-178">Finansinių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="30300-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="30300-179">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="30300-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="30300-180">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="30300-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



