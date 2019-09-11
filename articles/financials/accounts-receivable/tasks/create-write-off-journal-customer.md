---
title: Kurti kliento nurašymo žurnalą
description: Šis užduočių vadovas jums parodys, kaip nustatyti nurašymų parametrus ir tada nurašyti operacijas puslapyje Rinkiniai, puslapyje Atidarytos klientų SF ir puslapyje Klientas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2422f0a9d168daa76d105099c8b7455c97f92125
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916328"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="851c2-103">Kurti kliento nurašymo žurnalą</span><span class="sxs-lookup"><span data-stu-id="851c2-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="851c2-104">Šis užduočių vadovas jums parodys, kaip nustatyti nurašymų parametrus ir tada nurašyti operacijas puslapyje Rinkiniai, puslapyje Atidarytos klientų SF ir puslapyje Klientas.</span><span class="sxs-lookup"><span data-stu-id="851c2-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="851c2-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="851c2-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="851c2-106">Nustatyti nurašymo parametrus</span><span class="sxs-lookup"><span data-stu-id="851c2-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="851c2-107">Eikite į **Naršymo sritis > Moduliai> Kreditas ir mokėjimų priežiūra > Sąranka > Gautinos sumos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="851c2-108">Spustelėkite skirtuką **Mokėjimų priežiūra**.</span><span class="sxs-lookup"><span data-stu-id="851c2-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="851c2-109">Išplėskite arba sutraukite dalį **Nurašyti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="851c2-110">**Nurašymo žurnalas** yra bendrasis žurnalas, kuriame saugomos jūsų sukurtos nurašytos operacijos.</span><span class="sxs-lookup"><span data-stu-id="851c2-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="851c2-111">Prie kiekvieno nurašymo galite pridėti priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="851c2-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="851c2-112">Nurašydami šios numatytosios nuostatos galite nepaisyti.</span><span class="sxs-lookup"><span data-stu-id="851c2-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="851c2-113">Nustatykite **Atskirti pardavimo mokestį** kaip Taip, jei norite atskirti pardavimo mokestį nuo nurašomos originalios operacijos.</span><span class="sxs-lookup"><span data-stu-id="851c2-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="851c2-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-114">Close the page.</span></span>
5. <span data-ttu-id="851c2-115">Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Klientų registravimo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="851c2-116">Nurašyta sąskaita bus naudojama kaip išlaidų sąskaita arba rezervo reguliavimas bendrajame žurnale.</span><span class="sxs-lookup"><span data-stu-id="851c2-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="851c2-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="851c2-118">Nurašyti kliento balansą pagal terminus suskirstytų balansų puslapyje</span><span class="sxs-lookup"><span data-stu-id="851c2-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="851c2-119">Pasirinkite **Kreditas ir mokėjimai > Mokėjimų peržiūra > Suskirstyti pagal terminus balansai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="851c2-120">Pažymėkite kliento eilutę, kurią norite nurašyti.</span><span class="sxs-lookup"><span data-stu-id="851c2-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="851c2-121">Pavyzdžiui, pažymėkite eilutę su Birch Company.</span><span class="sxs-lookup"><span data-stu-id="851c2-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="851c2-122">**Veiksmų sritis** spustelėkite **Surinkti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="851c2-123">Spustelėkite **Nurašyti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-123">Click **Write off**.</span></span>
5. <span data-ttu-id="851c2-124">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-124">Click **OK**.</span></span>
6. <span data-ttu-id="851c2-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-125">Close the page.</span></span>
7. <span data-ttu-id="851c2-126">Eikite į **Naršymo sritis > Moduliai > Bendroji didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="851c2-127">Pasirinkite žurnalo, kuriame yra jūsų nurašymas, paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="851c2-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="851c2-128">Atšaukti kliento balansui sukuriama viena eilutė.</span><span class="sxs-lookup"><span data-stu-id="851c2-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="851c2-129">Viena ar kelios eilutės sukuriamos registruoti nurašymui nurašymo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="851c2-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="851c2-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-130">Close the page.</span></span>
10. <span data-ttu-id="851c2-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="851c2-132">Nurašykite operacijas rinkinių formoje.</span><span class="sxs-lookup"><span data-stu-id="851c2-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="851c2-133">Pasirinkite **Kreditas ir mokėjimai > Mokėjimų peržiūra > Suskirstyti pagal terminus balansai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="851c2-134">Pasirinkite kliento su operacijomis, kurias norite nurašyti, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="851c2-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="851c2-135">Pavyzdžiui, pasirinkite Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="851c2-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="851c2-136">Pažymėkite pirmosios operacijos eilutę.</span><span class="sxs-lookup"><span data-stu-id="851c2-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="851c2-137">Pažymėkite antrosios operacijos eilutę.</span><span class="sxs-lookup"><span data-stu-id="851c2-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="851c2-138">Spustelėkite **Nurašyti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-138">Click **Write off**.</span></span>
6. <span data-ttu-id="851c2-139">Lauke **Priežasties komentaras** įveskite „Blogosios skolos“.</span><span class="sxs-lookup"><span data-stu-id="851c2-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="851c2-140">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-140">Click **OK**.</span></span>
8. <span data-ttu-id="851c2-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-141">Close the page.</span></span>
9. <span data-ttu-id="851c2-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-142">Close the page.</span></span>
10. <span data-ttu-id="851c2-143">Eikite į **Didžio knyga > Žurnalo įrašai > Bendrieji žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="851c2-144">Pasirinkite žurnalo, kuriame yra jūsų nurašymas, paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="851c2-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="851c2-145">Atšaukti kliento balansui sukuriama viena eilutė.</span><span class="sxs-lookup"><span data-stu-id="851c2-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="851c2-146">Viena ar kelios eilutės sukuriamos registruoti nurašymui nurašymo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="851c2-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="851c2-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-147">Close the page.</span></span>
13. <span data-ttu-id="851c2-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="851c2-149">Nurašyti SF puslapyje Atidarytos klientų SF</span><span class="sxs-lookup"><span data-stu-id="851c2-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="851c2-150">Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Sąskaitos faktūros > Atidarytos kliento sąskaitos faktūros**.</span><span class="sxs-lookup"><span data-stu-id="851c2-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="851c2-151">Pažymėkite SF eilutę.</span><span class="sxs-lookup"><span data-stu-id="851c2-151">Mark the line for an invoice.</span></span> <span data-ttu-id="851c2-152">Pvz., pažymėkite eilutę, skirtą CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="851c2-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="851c2-153">**Veiksmų sritis** spustelėkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="851c2-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="851c2-154">Spustelėkite **Nurašyti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-154">Click **Write off**.</span></span>
5. <span data-ttu-id="851c2-155">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-155">Click **OK**.</span></span>
6. <span data-ttu-id="851c2-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="851c2-157">Nurašyti kliento balansą kliento puslapyje</span><span class="sxs-lookup"><span data-stu-id="851c2-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="851c2-158">Eikite į **Gautinos sumos > Klientai > Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="851c2-159">Pasirinkti kliento sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="851c2-159">Select a customer account.</span></span> <span data-ttu-id="851c2-160">Pavyzdžiui, pasirinkite US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="851c2-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="851c2-161">**Veiksmų sritis** spustelėkite **Surinkti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="851c2-162">Spustelėkite **Nurašyti**.</span><span class="sxs-lookup"><span data-stu-id="851c2-162">Click **Write off**.</span></span>
5. <span data-ttu-id="851c2-163">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="851c2-163">Click **OK**.</span></span>
6. <span data-ttu-id="851c2-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="851c2-164">Close the page.</span></span>

