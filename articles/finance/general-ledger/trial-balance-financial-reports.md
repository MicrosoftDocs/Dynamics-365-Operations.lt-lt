---
title: Bandomojo balanso finansinės ataskaitos
description: Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103663"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="6a759-104">Bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="6a759-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a759-105">Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="6a759-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="6a759-106">Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.</span><span class="sxs-lookup"><span data-stu-id="6a759-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="6a759-107">Numatytosios bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="6a759-107">Default trial balance reports</span></span>

<span data-ttu-id="6a759-108">Finansinėse ataskaitose galimos trys bandomojo balanso ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="6a759-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="6a759-109">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="6a759-109">Default report</span></span>                                 | <span data-ttu-id="6a759-110">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="6a759-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a759-111">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="6a759-112">Joje pateikiama visų sąskaitų balanso informaciją ir debeto bei kredito balansai ir jų grynosios reikšmės, taip pat operacijos data, kvitas ir žurnalo aprašymas.</span><span class="sxs-lookup"><span data-stu-id="6a759-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="6a759-113">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="6a759-114">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="6a759-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="6a759-115">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="6a759-116">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų šių ir praėjusių metų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="6a759-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="6a759-117">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="6a759-117">Building blocks</span></span>
<span data-ttu-id="6a759-118">Bandomojo balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="6a759-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="6a759-119">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="6a759-119">Default report</span></span>                                 | <span data-ttu-id="6a759-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="6a759-120">Row definition</span></span>          | <span data-ttu-id="6a759-121">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="6a759-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="6a759-122">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="6a759-123">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="6a759-123">Trial Balance - Default</span></span> | <span data-ttu-id="6a759-124">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="6a759-125">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="6a759-126">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="6a759-126">Trial Balance - Default</span></span> | <span data-ttu-id="6a759-127">Bandomojo balanso suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="6a759-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="6a759-128">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="6a759-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="6a759-129">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="6a759-129">Trial Balance - Default</span></span> | <span data-ttu-id="6a759-130">Bandomojo balanso suvestinė metams bėgant – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="6a759-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="6a759-131">Vykdydami **Bandomojo balanso** ataskaitą „Financial reporting”, būtinai pasirinkite žymės langelius **Rodyti eilutes be sumų** ir **Rodyti ataskaitas be aktyvių eilučių**, esančius **Parametrų** skirtuke.</span><span class="sxs-lookup"><span data-stu-id="6a759-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="6a759-132">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="6a759-132">Row definition</span></span>

<span data-ttu-id="6a759-133">Eilutės apibrėžime Bandomasis balansas – numatytasis yra viena eilutė, į kurią įtrauktos visos pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="6a759-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="6a759-134">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="6a759-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="6a759-135">Kai peržiūrite ataskaitą, detalizuojate vieną eilutę, kad pamatytumėte išsamią informaciją apie kiekvieną sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="6a759-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="6a759-136">Galite keisti eilutės apibrėžimą, kad į ją būtų įtraukta daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="6a759-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="6a759-137">Norėdami keisti eilutės Bandomasis balansas – Numatytasis apibrėžimą, kad į ją būtų įtrauktos visų sąskaitų eilutės, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6a759-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="6a759-138">Spustelėkite **Redaguoti**, tada spustelėkite **Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="6a759-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="6a759-139">Komanda **Įterpti eilutes iš dimensijų** leidžia pasirinkti, kokias dimensijas norite turėti savo eilutės apibrėžime.</span><span class="sxs-lookup"><span data-stu-id="6a759-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="6a759-140">Šiam eilutės apibrėžimui naudosite **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="6a759-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="6a759-141">Įsitikinkite, kad dalyje **Pagrindinė sąskaita** yra visi konjunkcijos ženklai (&), tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6a759-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="6a759-142">Dabar eilutės apibrėžime yra visos jūsų numatytojo juridinio subjekto pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="6a759-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="6a759-143">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="6a759-143">Column definition</span></span>

<span data-ttu-id="6a759-144">Kiekvienoje bandomojo balanso ataskaitoje naudojamas kitas stulpelio aprašas.</span><span class="sxs-lookup"><span data-stu-id="6a759-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="6a759-145">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, šiuose stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="6a759-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="6a759-146">**Išsamus bandomasis balansas – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="6a759-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="6a759-147">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="6a759-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="6a759-148">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="6a759-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="6a759-149">**ATTR (3)** – Atributai:</span><span class="sxs-lookup"><span data-stu-id="6a759-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="6a759-150">Operacijos data</span><span class="sxs-lookup"><span data-stu-id="6a759-150">Transaction Date</span></span>
        -   <span data-ttu-id="6a759-151">Kvitas</span><span class="sxs-lookup"><span data-stu-id="6a759-151">Voucher</span></span>
        -   <span data-ttu-id="6a759-152">Žurnalo aprašymas</span><span class="sxs-lookup"><span data-stu-id="6a759-152">Journal Description</span></span>
    -   <span data-ttu-id="6a759-153">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="6a759-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="6a759-154">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="6a759-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="6a759-155">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="6a759-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="6a759-156">**Bandomojo balanso suvestinė – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="6a759-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="6a759-157">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="6a759-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="6a759-158">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="6a759-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="6a759-159">**ATTR** – Atributas:</span><span class="sxs-lookup"><span data-stu-id="6a759-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="6a759-160">Kvitas</span><span class="sxs-lookup"><span data-stu-id="6a759-160">Voucher</span></span>
    -   <span data-ttu-id="6a759-161">**FD** – Pradžios balanso finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="6a759-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="6a759-162">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="6a759-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="6a759-163">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="6a759-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="6a759-164">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="6a759-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="6a759-165">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="6a759-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="6a759-166">**Bandomojo balanso suvestinė metams bėgant – Numatytoji:**</span><span class="sxs-lookup"><span data-stu-id="6a759-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="6a759-167">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="6a759-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="6a759-168">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="6a759-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="6a759-169">**ATTR** – Atributas</span><span class="sxs-lookup"><span data-stu-id="6a759-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="6a759-170">Kvitas</span><span class="sxs-lookup"><span data-stu-id="6a759-170">Voucher</span></span>
    -   <span data-ttu-id="6a759-171">**FD** – Pradžios balanso šių metų finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="6a759-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="6a759-172">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų debetas</span><span class="sxs-lookup"><span data-stu-id="6a759-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="6a759-173">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="6a759-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="6a759-174">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="6a759-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="6a759-175">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="6a759-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="6a759-176">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų debetas</span><span class="sxs-lookup"><span data-stu-id="6a759-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="6a759-177">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="6a759-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a759-178">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6a759-178">Additional resources</span></span>

[<span data-ttu-id="6a759-179">Finansinių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="6a759-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="6a759-180">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="6a759-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="6a759-181">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="6a759-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
