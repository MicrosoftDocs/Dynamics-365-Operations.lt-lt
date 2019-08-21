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
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 842eecf68f5a658be6cdc7a05c365a18fe7d91dc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846104"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="82b0b-104">Bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="82b0b-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82b0b-105">Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="82b0b-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="82b0b-106">Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.</span><span class="sxs-lookup"><span data-stu-id="82b0b-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="82b0b-107">Numatytosios bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="82b0b-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="82b0b-108">„Microsoft Dynamics 365 for Finance and Operations“ finansinėse ataskaitose galimos trys bandomojo balanso ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="82b0b-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="82b0b-109">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="82b0b-109">Default report</span></span>                                 | <span data-ttu-id="82b0b-110">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="82b0b-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b0b-111">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="82b0b-112">Joje pateikiama visų sąskaitų balanso informaciją ir debeto bei kredito balansai ir jų grynosios reikšmės, taip pat operacijos data, kvitas ir žurnalo aprašymas.</span><span class="sxs-lookup"><span data-stu-id="82b0b-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="82b0b-113">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="82b0b-114">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="82b0b-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="82b0b-115">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="82b0b-116">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų šių ir praėjusių metų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="82b0b-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="82b0b-117">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="82b0b-117">Building blocks</span></span>
<span data-ttu-id="82b0b-118">Bandomojo balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="82b0b-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="82b0b-119">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="82b0b-119">Default report</span></span>                                 | <span data-ttu-id="82b0b-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="82b0b-120">Row definition</span></span>          | <span data-ttu-id="82b0b-121">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="82b0b-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="82b0b-122">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="82b0b-123">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="82b0b-123">Trial Balance - Default</span></span> | <span data-ttu-id="82b0b-124">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="82b0b-125">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="82b0b-126">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="82b0b-126">Trial Balance - Default</span></span> | <span data-ttu-id="82b0b-127">Bandomojo balanso suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="82b0b-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="82b0b-128">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="82b0b-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="82b0b-129">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="82b0b-129">Trial Balance - Default</span></span> | <span data-ttu-id="82b0b-130">Bandomojo balanso suvestinė metams bėgant – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="82b0b-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="82b0b-131">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="82b0b-131">Row definition</span></span>

<span data-ttu-id="82b0b-132">Eilutės apibrėžime Bandomasis balansas – numatytasis yra viena eilutė, į kurią įtrauktos visos pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="82b0b-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="82b0b-133">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="82b0b-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="82b0b-134">Kai peržiūrite ataskaitą, detalizuojate vieną eilutę, kad pamatytumėte išsamią informaciją apie kiekvieną sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="82b0b-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="82b0b-135">Galite keisti eilutės apibrėžimą, kad į ją būtų įtraukta daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="82b0b-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="82b0b-136">Norėdami keisti eilutės Bandomasis balansas – Numatytasis apibrėžimą, kad į ją būtų įtrauktos visų sąskaitų eilutės, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="82b0b-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="82b0b-137">Spustelėkite **Redaguoti**, tada spustelėkite **Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="82b0b-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="82b0b-138">Komanda **Įterpti eilutes iš dimensijų** leidžia pasirinkti, kokias dimensijas norite turėti savo eilutės apibrėžime.</span><span class="sxs-lookup"><span data-stu-id="82b0b-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="82b0b-139">Šiam eilutės apibrėžimui naudosite **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="82b0b-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="82b0b-140">Įsitikinkite, kad dalyje **Pagrindinė sąskaita** yra visi konjunkcijos ženklai (&), tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="82b0b-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="82b0b-141">Dabar eilutės apibrėžime yra visos jūsų numatytojo juridinio subjekto pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="82b0b-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="82b0b-142">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="82b0b-142">Column definition</span></span>

<span data-ttu-id="82b0b-143">Kiekvienoje bandomojo balanso ataskaitoje naudojamas kitas stulpelio aprašas.</span><span class="sxs-lookup"><span data-stu-id="82b0b-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="82b0b-144">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, šiuose stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="82b0b-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="82b0b-145">**Išsamus bandomasis balansas – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="82b0b-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="82b0b-146">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="82b0b-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="82b0b-147">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="82b0b-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="82b0b-148">**ATTR (3)** – Atributai:</span><span class="sxs-lookup"><span data-stu-id="82b0b-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="82b0b-149">Operacijos data</span><span class="sxs-lookup"><span data-stu-id="82b0b-149">Transaction Date</span></span>
        -   <span data-ttu-id="82b0b-150">Kvitas</span><span class="sxs-lookup"><span data-stu-id="82b0b-150">Voucher</span></span>
        -   <span data-ttu-id="82b0b-151">Žurnalo aprašymas</span><span class="sxs-lookup"><span data-stu-id="82b0b-151">Journal Description</span></span>
    -   <span data-ttu-id="82b0b-152">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="82b0b-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="82b0b-153">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="82b0b-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="82b0b-154">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="82b0b-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="82b0b-155">**Bandomojo balanso suvestinė – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="82b0b-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="82b0b-156">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="82b0b-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="82b0b-157">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="82b0b-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="82b0b-158">**ATTR** – Atributas:</span><span class="sxs-lookup"><span data-stu-id="82b0b-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="82b0b-159">Kvitas</span><span class="sxs-lookup"><span data-stu-id="82b0b-159">Voucher</span></span>
    -   <span data-ttu-id="82b0b-160">**FD** – Pradžios balanso finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="82b0b-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="82b0b-161">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="82b0b-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="82b0b-162">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="82b0b-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="82b0b-163">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="82b0b-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="82b0b-164">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="82b0b-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="82b0b-165">**Bandomojo balanso suvestinė metams bėgant – Numatytoji:**</span><span class="sxs-lookup"><span data-stu-id="82b0b-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="82b0b-166">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="82b0b-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="82b0b-167">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="82b0b-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="82b0b-168">**ATTR** – Atributas</span><span class="sxs-lookup"><span data-stu-id="82b0b-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="82b0b-169">Kvitas</span><span class="sxs-lookup"><span data-stu-id="82b0b-169">Voucher</span></span>
    -   <span data-ttu-id="82b0b-170">**FD** – Pradžios balanso šių metų finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="82b0b-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="82b0b-171">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų debetas</span><span class="sxs-lookup"><span data-stu-id="82b0b-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="82b0b-172">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="82b0b-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="82b0b-173">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="82b0b-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="82b0b-174">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="82b0b-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="82b0b-175">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų debetas</span><span class="sxs-lookup"><span data-stu-id="82b0b-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="82b0b-176">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="82b0b-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="82b0b-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="82b0b-177">Additional resources</span></span>
--------

[<span data-ttu-id="82b0b-178">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="82b0b-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="82b0b-179">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="82b0b-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="82b0b-180">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="82b0b-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



