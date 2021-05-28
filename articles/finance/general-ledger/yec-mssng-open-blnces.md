---
title: Uždarymo metų pabaigoje trūkstami pradiniai balansai
description: Šioje temoje paaiškinama, kodėl uždarius metus gali trūkti pradinių balansų ir kaip atkurti tuos balansus, jei jų trūksta.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028577"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="57707-103">Uždarymo metų pabaigoje trūkstami pradiniai balansai</span><span class="sxs-lookup"><span data-stu-id="57707-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57707-104">Šioje temoje paaiškinama, kodėl uždarius metus gali trūkti pradinių balansų ir kaip atkurti tuos balansus, jei jų trūksta.</span><span class="sxs-lookup"><span data-stu-id="57707-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="57707-105">Požymis</span><span class="sxs-lookup"><span data-stu-id="57707-105">Symptom</span></span>

<span data-ttu-id="57707-106">Kodėl nėra pradinių balansų paleidus didžiosios knygos uždarymą metų pabaigoje?</span><span class="sxs-lookup"><span data-stu-id="57707-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="57707-107">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="57707-107">Resolution</span></span>

<span data-ttu-id="57707-108">Štai ką reikia patikrinti, jei metus uždarėte didžiojoje knygoje ir vėliau sugeneravote bandomąjį balansą, kuriame nerodomi kitų finansinių metų pradiniai balansai.</span><span class="sxs-lookup"><span data-stu-id="57707-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="57707-109">Jei laukas **Anuliuoti ankstesnį uždarymą** nustatytas į **Taip**, ankstesnis tų pačių finansinių metų uždarymas metų pabaigoje yra atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="57707-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="57707-110">Paleidus uždarymo metų pabaigoje atšaukimo procesą, visi uždarymo ir pradinių balansų įrašai bus panaikinti, tarytum metai niekada nebūtų uždaryti.</span><span class="sxs-lookup"><span data-stu-id="57707-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="57707-111">Kvitai taip pat panaikinami.</span><span class="sxs-lookup"><span data-stu-id="57707-111">The vouchers are also deleted.</span></span> <span data-ttu-id="57707-112">Uždarymo metų pabaigoje procesas nebus paleistas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="57707-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="57707-113">Būtina iš naujo pradėti procesą šį kartą parinktį **Anuliuoti ankstesnį uždarymą** atnaujinant į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="57707-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="57707-114">Šis scenarijus įtrauktas į DUK apie uždarymą metų pabaigoje temą.</span><span class="sxs-lookup"><span data-stu-id="57707-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="57707-115">Daugiau informacijos ieškokite dalyje [DUK apie metų pabaigos veiklas](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="57707-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="57707-116">Požymis</span><span class="sxs-lookup"><span data-stu-id="57707-116">Symptom</span></span>

<span data-ttu-id="57707-117">Uždarymas metų pabaigoje buvo paleistas parinktį **Anuliuoti ankstesnį uždarymą** nustačius į **Ne**, tačiau vis dar neturiu finansinių metų pradinių balansų.</span><span class="sxs-lookup"><span data-stu-id="57707-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="57707-118">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="57707-118">Resolution</span></span>

<span data-ttu-id="57707-119">Pirmiausia patikrinkite paketinės užduoties būseną.</span><span class="sxs-lookup"><span data-stu-id="57707-119">First check the status of the batch job.</span></span> <span data-ttu-id="57707-120">Uždarant metus atliekamos įvairios atskiros užduotys, tačiau svarbiausias veiksmas yra paketinė užduotis su užduoties aprašu **5.0.0 veiksmas**.</span><span class="sxs-lookup"><span data-stu-id="57707-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="57707-121">Atliekant šį veiksmą didžiojoje knygoje registruojamos atidarymo operacijos ir pasirinktinai uždaromos operacijos.</span><span class="sxs-lookup"><span data-stu-id="57707-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="57707-122">[![Paketo retrospektyvų sąrašas](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="57707-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="57707-123">Jei šis veiksmas atliktas sėkmingai, bet puslapyje **Bandomojo balanso užklausa** (**Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas**) nematote pradinių balansų, peržiūrėkite uždarymo metų pabaigoje paketinės užduoties rezultatus, kad sužinotumėte, ar perkėlimo balansų veiksmas atliktas sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="57707-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="57707-124">[![Uždarymo metų pabaigoje paketinės užduoties rezultatai](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="57707-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="57707-125">Jei šis veiksmas dėl kokių nors priežasčių nepavyko, atidarymo (ir pasirinktinai uždarymo) operacijos greičiausiai buvo sėkmingai užregistruotos.</span><span class="sxs-lookup"><span data-stu-id="57707-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="57707-126">Galite patikrinti, ar didžiosios knygos operacijos buvo sėkmingai užregistruotos, puslapyje **Kvito operacijų užklausa** nurodydami kvito numerį ir datą, pateiktą uždarymo metų pabaigoje dialogo lange jūsų uždarytiems metams (**Didžioji knyga > Užklausos ir ataskaitos > Kvito operacijos**).</span><span class="sxs-lookup"><span data-stu-id="57707-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="57707-127">[![Kvito operacijų užklausa](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="57707-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="57707-128">Jei yra atidarymo (ir pasirinktinai uždarymo) kvitai, metų pabaigos dar kartą uždaryti nereikia.</span><span class="sxs-lookup"><span data-stu-id="57707-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="57707-129">Informacijos apie tai, kaip pereiti prie kitų veiksmų, ieškokite kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="57707-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="57707-130">Požymis</span><span class="sxs-lookup"><span data-stu-id="57707-130">Symptom</span></span>

<span data-ttu-id="57707-131">Veiksmas „Atkurti balansus“ uždarymo metų pabaigoje nepavyko, ar man reikia iš naujo paleisti visą uždarymo metų pabaigoje procesą?</span><span class="sxs-lookup"><span data-stu-id="57707-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="57707-132">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="57707-132">Resolution</span></span>

<span data-ttu-id="57707-133">Veiksmu Atkurti balansus atnaujinami didžiosios knygos balansai, kurie naudojami generuojant bandomojo balanso užklausą.</span><span class="sxs-lookup"><span data-stu-id="57707-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="57707-134">Tai paskutinis veiksmas uždarymo metų pabaigoje procese.</span><span class="sxs-lookup"><span data-stu-id="57707-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="57707-135">Jei šis veiksmas yra vienintelis nesėkmingas veiksmas, didžiosios knygos operacijos sėkmingai užregistruotos.</span><span class="sxs-lookup"><span data-stu-id="57707-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="57707-136">Neturite dar kartą paleisti uždarymo metų pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="57707-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="57707-137">Galite rankiniu būdu paleisti balansų atkūrimo procesą puslapyje **Finansinių dimensijų rinkiniai** (**Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinių dimensijų rinkiniai**).</span><span class="sxs-lookup"><span data-stu-id="57707-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="57707-138">[![Mygtukas Atkurti balansus puslapyje Finansinių dimensijų rinkiniai](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="57707-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="57707-139">Jei šis veiksmas užtrunka ilgai, rekomenduojame peržiūrėti geriausią finansinių dimensijų rinkinių praktiką, aprašytą dalyje [Geriausia finansinių dimensijų rinkinių naujinimo praktika](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="57707-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

