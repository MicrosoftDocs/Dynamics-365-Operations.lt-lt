---
title: "Bandomojo balanso finansinės ataskaitos"
description: "Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6405599186c8d07ac5ade19d3b7d27ae83b036ff
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="0f574-104">Bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="0f574-104">Trial balance financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0f574-105">Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="0f574-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="0f574-106">Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.</span><span class="sxs-lookup"><span data-stu-id="0f574-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="0f574-107">Numatytosios bandomojo balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="0f574-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="0f574-108">„Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo modulyje Finansinės ataskaitos pateikiamos trys bandomojo balanso ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="0f574-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

| <span data-ttu-id="0f574-109">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="0f574-109">Default report</span></span>                                 | <span data-ttu-id="0f574-110">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="0f574-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f574-111">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="0f574-112">Joje pateikiama visų sąskaitų balanso informaciją ir debeto bei kredito balansai ir jų grynosios reikšmės, taip pat operacijos data, kvitas ir žurnalo aprašymas.</span><span class="sxs-lookup"><span data-stu-id="0f574-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="0f574-113">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="0f574-114">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="0f574-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="0f574-115">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="0f574-116">Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų šių ir praėjusių metų grynasis skirtumas.</span><span class="sxs-lookup"><span data-stu-id="0f574-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="0f574-117">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="0f574-117">Building blocks</span></span>
<span data-ttu-id="0f574-118">Bandomojo balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="0f574-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="0f574-119">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="0f574-119">Default report</span></span>                                 | <span data-ttu-id="0f574-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="0f574-120">Row definition</span></span>          | <span data-ttu-id="0f574-121">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="0f574-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="0f574-122">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="0f574-123">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="0f574-123">Trial Balance - Default</span></span> | <span data-ttu-id="0f574-124">Išsamus bandomasis balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="0f574-125">Bandomojo balanso suvestinė – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="0f574-126">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="0f574-126">Trial Balance - Default</span></span> | <span data-ttu-id="0f574-127">Bandomojo balanso suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="0f574-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="0f574-128">Bandomojo balanso suvestinė metams bėgant – numatyt.</span><span class="sxs-lookup"><span data-stu-id="0f574-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="0f574-129">Bandomasis balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="0f574-129">Trial Balance - Default</span></span> | <span data-ttu-id="0f574-130">Bandomojo balanso suvestinė metams bėgant – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="0f574-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="0f574-131">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="0f574-131">Row definition</span></span>

<span data-ttu-id="0f574-132">Eilutės apibrėžime Bandomasis balansas – numatytasis yra viena eilutė, į kurią įtrauktos visos pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="0f574-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="0f574-133">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="0f574-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="0f574-134">Kai peržiūrite ataskaitą, detalizuojate vieną eilutę, kad pamatytumėte išsamią informaciją apie kiekvieną sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="0f574-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="0f574-135">Galite keisti eilutės apibrėžimą, kad į ją būtų įtraukta daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="0f574-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="0f574-136">Norėdami keisti eilutės Bandomasis balansas – Numatytasis apibrėžimą, kad į ją būtų įtrauktos visų sąskaitų eilutės, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0f574-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="0f574-137">Spustelėkite **Redaguoti**, tada spustelėkite **Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="0f574-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="0f574-138">Komanda **Įterpti eilutes iš dimensijų** leidžia pasirinkti, kokias dimensijas norite turėti savo eilutės apibrėžime.</span><span class="sxs-lookup"><span data-stu-id="0f574-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="0f574-139">Šiam eilutės apibrėžimui naudosite **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="0f574-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="0f574-140">Įsitikinkite, kad dalyje **Pagrindinė sąskaita** yra visi konjunkcijos ženklai (&), tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0f574-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="0f574-141">Dabar eilutės apibrėžime yra visos jūsų numatytojo juridinio subjekto pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="0f574-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="0f574-142">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="0f574-142">Column definition</span></span>

<span data-ttu-id="0f574-143">Kiekvienoje bandomojo balanso ataskaitoje naudojamas kitas stulpelio aprašas.</span><span class="sxs-lookup"><span data-stu-id="0f574-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="0f574-144">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, šiuose stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="0f574-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="0f574-145">**Išsamus bandomasis balansas – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="0f574-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="0f574-146">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="0f574-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0f574-147">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="0f574-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="0f574-148">**ATTR (3)** – Atributai:</span><span class="sxs-lookup"><span data-stu-id="0f574-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="0f574-149">Operacijos data</span><span class="sxs-lookup"><span data-stu-id="0f574-149">Transaction Date</span></span>
        -   <span data-ttu-id="0f574-150">Kvitas</span><span class="sxs-lookup"><span data-stu-id="0f574-150">Voucher</span></span>
        -   <span data-ttu-id="0f574-151">Žurnalo aprašymas</span><span class="sxs-lookup"><span data-stu-id="0f574-151">Journal Description</span></span>
    -   <span data-ttu-id="0f574-152">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="0f574-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="0f574-153">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="0f574-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="0f574-154">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="0f574-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="0f574-155">**Bandomojo balanso suvestinė – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="0f574-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="0f574-156">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="0f574-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="0f574-157">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="0f574-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0f574-158">**ATTR** – Atributas:</span><span class="sxs-lookup"><span data-stu-id="0f574-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="0f574-159">Kvitas</span><span class="sxs-lookup"><span data-stu-id="0f574-159">Voucher</span></span>
    -   <span data-ttu-id="0f574-160">**FD** – Pradžios balanso finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="0f574-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="0f574-161">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas</span><span class="sxs-lookup"><span data-stu-id="0f574-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="0f574-162">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas</span><span class="sxs-lookup"><span data-stu-id="0f574-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="0f574-163">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="0f574-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="0f574-164">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="0f574-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="0f574-165">**Bandomojo balanso suvestinė metams bėgant – Numatytoji:**</span><span class="sxs-lookup"><span data-stu-id="0f574-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="0f574-166">**ACCT** – Sąskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="0f574-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="0f574-167">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="0f574-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0f574-168">**ATTR** – Atributas</span><span class="sxs-lookup"><span data-stu-id="0f574-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="0f574-169">Kvitas</span><span class="sxs-lookup"><span data-stu-id="0f574-169">Voucher</span></span>
    -   <span data-ttu-id="0f574-170">**FD** – Pradžios balanso šių metų finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="0f574-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="0f574-171">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų debetas</span><span class="sxs-lookup"><span data-stu-id="0f574-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="0f574-172">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="0f574-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="0f574-173">**CALC** – Grynasis skirtumas</span><span class="sxs-lookup"><span data-stu-id="0f574-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="0f574-174">**CALC** – Galutinis balansas</span><span class="sxs-lookup"><span data-stu-id="0f574-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="0f574-175">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų debetas</span><span class="sxs-lookup"><span data-stu-id="0f574-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="0f574-176">**FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų kreditas</span><span class="sxs-lookup"><span data-stu-id="0f574-176">**FD** – Financial data that contains only credits for the last year</span></span>

 

<a name="see-also"></a><span data-ttu-id="0f574-177">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="0f574-177">See also</span></span>
--------

[<span data-ttu-id="0f574-178">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="0f574-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="0f574-179">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="0f574-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="0f574-180">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="0f574-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




