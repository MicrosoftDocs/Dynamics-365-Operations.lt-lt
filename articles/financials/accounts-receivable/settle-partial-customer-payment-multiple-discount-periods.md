---
title: "Dalinio kliento mokėjimo, turinčio kelis nuolaidos laikotarpius, sudengimas"
description: "Šiame straipsnyje parodoma, kaip sudengiami daliniai kliento mokėjimai, kai yra keli nuolaidos laikotarpiai."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 048a4ca44d457849e2f632da1686dfbeb81dd61b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a><span data-ttu-id="15fed-103">Dalinio kliento mokėjimo, turinčio kelis nuolaidos laikotarpius, sudengimas</span><span class="sxs-lookup"><span data-stu-id="15fed-103">Settle a partial customer payment that has multiple discount periods</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="15fed-104">Šiame straipsnyje parodoma, kaip sudengiami daliniai kliento mokėjimai, kai yra keli nuolaidos laikotarpiai.</span><span class="sxs-lookup"><span data-stu-id="15fed-104">This article shows how partial customer payments are settled when there are multiple discount periods.</span></span>

<span data-ttu-id="15fed-105">„Fabrikam“ 4031 klientui siūlo du mokėjimo nuolaidos laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="15fed-105">Fabrikam offers customer 4031 two cash discount periods.</span></span> <span data-ttu-id="15fed-106">Klientas gauna 2 procentų mokėjimo nuolaidą, jei SF yra apmokama per penkias dienas, arba 1 procento mokėjimo nuolaidą, jei SF apmokama per 14 dienų.</span><span class="sxs-lookup"><span data-stu-id="15fed-106">The customer receives a 2-percent cash discount if the invoice is paid in five days and a 1-percent cash discount if the invoice is paid in 14 days.</span></span> <span data-ttu-id="15fed-107">„Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="15fed-107">Fabrikam also offers cash discounts on partial payments.</span></span> <span data-ttu-id="15fed-108">Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="15fed-108">The settlement parameters are located on the **Accounts receivable parameters** page.</span></span>

## <a name="invoice"></a><span data-ttu-id="15fed-109">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-109">Invoice</span></span>
<span data-ttu-id="15fed-110">Birželio 25 d. Eglė 4031 klientui įveda ir užregistruoja sąskaitą faktūrą 1 000,00 sumai.</span><span class="sxs-lookup"><span data-stu-id="15fed-110">On June 25, Arnie enters and posts an invoice for 1,000.00 for customer 4031.</span></span> <span data-ttu-id="15fed-111">Peržiūrėdama šios sąskaitos faktūros mokėjimo nuolaidą, Eglė mato, kad 4031 klientas gaus 20,00 nuolaidą, jei sąskaita faktūra bus apmokėta iki birželio 30 d.</span><span class="sxs-lookup"><span data-stu-id="15fed-111">When he reviews the cash discounts for this invoice, Arnie sees that customer 4031 receives a 20.00 discount if the invoice is paid by June 30.</span></span> <span data-ttu-id="15fed-112">Jei sąskaita faktūra bus apmokėta iki liepos 9 d., klientas gaus 10,00 nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="15fed-112">If the invoice is paid by July 9, the customer receives a 10.00 discount.</span></span>

| <span data-ttu-id="15fed-113">Mokėjimo nuolaidos data</span><span class="sxs-lookup"><span data-stu-id="15fed-113">Cash discount date</span></span> | <span data-ttu-id="15fed-114">Mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="15fed-114">Cash discount amount</span></span> | <span data-ttu-id="15fed-115">Suma operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="15fed-115">Amount in transaction currency</span></span> |
|--------------------|----------------------|--------------------------------|
| <span data-ttu-id="15fed-116">2015-06-30</span><span class="sxs-lookup"><span data-stu-id="15fed-116">6/30/2015</span></span>          | <span data-ttu-id="15fed-117">20,00</span><span class="sxs-lookup"><span data-stu-id="15fed-117">20.00</span></span>                | <span data-ttu-id="15fed-118">980,00</span><span class="sxs-lookup"><span data-stu-id="15fed-118">980.00</span></span>                         |
| <span data-ttu-id="15fed-119">2015-07-09</span><span class="sxs-lookup"><span data-stu-id="15fed-119">7/9/2015</span></span>           | <span data-ttu-id="15fed-120">10,00</span><span class="sxs-lookup"><span data-stu-id="15fed-120">10.00</span></span>                | <span data-ttu-id="15fed-121">990,00</span><span class="sxs-lookup"><span data-stu-id="15fed-121">990.00</span></span>                         |
| <span data-ttu-id="15fed-122">2015-07-25</span><span class="sxs-lookup"><span data-stu-id="15fed-122">7/25/2015</span></span>          | <span data-ttu-id="15fed-123">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-123">0.00</span></span>                 | <span data-ttu-id="15fed-124">1000,00</span><span class="sxs-lookup"><span data-stu-id="15fed-124">1,000.00</span></span>                       |

<span data-ttu-id="15fed-125">Arnas gali šią operaciją peržiūrėti puslapyje **Kliento operacijos**.</span><span class="sxs-lookup"><span data-stu-id="15fed-125">Arnie can view this transaction on the **Customer transactions** page.</span></span>

| <span data-ttu-id="15fed-126">Kvitas</span><span class="sxs-lookup"><span data-stu-id="15fed-126">Voucher</span></span>   | <span data-ttu-id="15fed-127">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15fed-127">Transaction type</span></span> | <span data-ttu-id="15fed-128">Data</span><span class="sxs-lookup"><span data-stu-id="15fed-128">Date</span></span>      | <span data-ttu-id="15fed-129">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-129">Invoice</span></span> | <span data-ttu-id="15fed-130">Operacijos valiutos debeto suma</span><span class="sxs-lookup"><span data-stu-id="15fed-130">Amount in transaction currency debit</span></span> | <span data-ttu-id="15fed-131">Operacijos valiutos kredito suma</span><span class="sxs-lookup"><span data-stu-id="15fed-131">Amount in transaction currency credit</span></span> | <span data-ttu-id="15fed-132">Likutis</span><span class="sxs-lookup"><span data-stu-id="15fed-132">Balance</span></span>  | <span data-ttu-id="15fed-133">Valiuta</span><span class="sxs-lookup"><span data-stu-id="15fed-133">Currency</span></span> |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| <span data-ttu-id="15fed-134">LFSF-10030</span><span class="sxs-lookup"><span data-stu-id="15fed-134">FTI-10030</span></span> | <span data-ttu-id="15fed-135">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-135">Invoice</span></span>          | <span data-ttu-id="15fed-136">2015-06-25</span><span class="sxs-lookup"><span data-stu-id="15fed-136">6/25/2015</span></span> | <span data-ttu-id="15fed-137">10030</span><span class="sxs-lookup"><span data-stu-id="15fed-137">10030</span></span>   | <span data-ttu-id="15fed-138">1000,00</span><span class="sxs-lookup"><span data-stu-id="15fed-138">1,000.00</span></span>                             |                                       | <span data-ttu-id="15fed-139">1000,00</span><span class="sxs-lookup"><span data-stu-id="15fed-139">1,000.00</span></span> | <span data-ttu-id="15fed-140">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-140">USD</span></span>      |

## <a name="partial-payment-before-the-cash-discount-date"></a><span data-ttu-id="15fed-141">Dalinis mokėjimas prieš mokėjimo nuolaidos datą</span><span class="sxs-lookup"><span data-stu-id="15fed-141">Partial payment before the cash discount date</span></span>
<span data-ttu-id="15fed-142">Birželio 28 d. 4031 klientas atliko 294,00 dalinį mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="15fed-142">On June 28, Customer 4031 makes a partial payment of 294.00.</span></span> <span data-ttu-id="15fed-143">Kadangi birželio 28 d. patenka į pirmąjį mokėjimo nuolaidos laikotarpį, klientui taikoma 6,00 nuolaida.</span><span class="sxs-lookup"><span data-stu-id="15fed-143">Because June 28 is within the first cash discount period, the customer takes a 6.00 discount.</span></span> <span data-ttu-id="15fed-144">Puslapyje **Sudengti operacijas** lauko **Mokėjimo nuolaidos suma** reikšmė yra 20,00, o **Taikytinos mokėjimo nuolaidos suma** reikšmė yra 6,00.</span><span class="sxs-lookup"><span data-stu-id="15fed-144">On the **Settle transactions** page, the **Cash discount amount** value is 20.00, and the **Cash discount amount to take** value is 6.00.</span></span>

| <span data-ttu-id="15fed-145">Žymėti</span><span class="sxs-lookup"><span data-stu-id="15fed-145">Mark</span></span>     | <span data-ttu-id="15fed-146">Naudokite mokėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="15fed-146">Use cash discount</span></span> | <span data-ttu-id="15fed-147">Kvitas</span><span class="sxs-lookup"><span data-stu-id="15fed-147">Voucher</span></span>   | <span data-ttu-id="15fed-148">Paskyra</span><span class="sxs-lookup"><span data-stu-id="15fed-148">Account</span></span> | <span data-ttu-id="15fed-149">Data</span><span class="sxs-lookup"><span data-stu-id="15fed-149">Date</span></span>      | <span data-ttu-id="15fed-150">Terminas</span><span class="sxs-lookup"><span data-stu-id="15fed-150">Due date</span></span>  | <span data-ttu-id="15fed-151">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-151">Invoice</span></span> | <span data-ttu-id="15fed-152">Suma operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="15fed-152">Amount in transaction currency</span></span> | <span data-ttu-id="15fed-153">Valiuta</span><span class="sxs-lookup"><span data-stu-id="15fed-153">Currency</span></span> | <span data-ttu-id="15fed-154">Sudengtina suma</span><span class="sxs-lookup"><span data-stu-id="15fed-154">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="15fed-155">Pasirinkta</span><span class="sxs-lookup"><span data-stu-id="15fed-155">Selected</span></span> | <span data-ttu-id="15fed-156">Įprastas</span><span class="sxs-lookup"><span data-stu-id="15fed-156">Normal</span></span>            | <span data-ttu-id="15fed-157">LFSF-10030</span><span class="sxs-lookup"><span data-stu-id="15fed-157">FTI-10030</span></span> | <span data-ttu-id="15fed-158">4031</span><span class="sxs-lookup"><span data-stu-id="15fed-158">4031</span></span>    | <span data-ttu-id="15fed-159">2015-06-25</span><span class="sxs-lookup"><span data-stu-id="15fed-159">6/25/2015</span></span> | <span data-ttu-id="15fed-160">2015-07-25</span><span class="sxs-lookup"><span data-stu-id="15fed-160">7/25/2015</span></span> | <span data-ttu-id="15fed-161">10030</span><span class="sxs-lookup"><span data-stu-id="15fed-161">10030</span></span>   | <span data-ttu-id="15fed-162">1000,00</span><span class="sxs-lookup"><span data-stu-id="15fed-162">1,000.00</span></span>                       | <span data-ttu-id="15fed-163">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-163">USD</span></span>      | <span data-ttu-id="15fed-164">294,00</span><span class="sxs-lookup"><span data-stu-id="15fed-164">294.00</span></span>           |

<span data-ttu-id="15fed-165">Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.</span><span class="sxs-lookup"><span data-stu-id="15fed-165">Discount information appears at the bottom of the **Settle open transactions** page.</span></span> <span data-ttu-id="15fed-166">Jei lauko **Sudengtina suma** reikšmės nepakeisite į **294,00**, rodomos lauko **Mokėjimo nuolaidos suma** reikšmės skirsis.</span><span class="sxs-lookup"><span data-stu-id="15fed-166">If you don't change the **Amount to settle** value to **294.00**, the **Cash discount amount** values that appear will differ.</span></span> <span data-ttu-id="15fed-167">Tačiau užregistravus mokėjimą bus taikoma 6,00 mokėjimo nuolaida, nes sudengimo funkcija automatiškai koreguoja lauko **Sudengtina suma** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="15fed-167">However, 6.00 will be taken as the cash discount when the payment is posted, because settlement automatically adjusts the **Amount to settle** value for you.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="15fed-168">Mokėjimo nuolaidos data</span><span class="sxs-lookup"><span data-stu-id="15fed-168">Cash discount date</span></span>           | <span data-ttu-id="15fed-169">2015-06-30</span><span class="sxs-lookup"><span data-stu-id="15fed-169">6/30/2015</span></span> |
| <span data-ttu-id="15fed-170">Mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="15fed-170">Cash discount amount</span></span>         | <span data-ttu-id="15fed-171">20,00</span><span class="sxs-lookup"><span data-stu-id="15fed-171">20.00</span></span>     |
| <span data-ttu-id="15fed-172">Naudokite mokėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="15fed-172">Use cash discount</span></span>            | <span data-ttu-id="15fed-173">Įprastas</span><span class="sxs-lookup"><span data-stu-id="15fed-173">Normal</span></span>    |
| <span data-ttu-id="15fed-174">Pritaikyta mokėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="15fed-174">Cash discount taken</span></span>          | <span data-ttu-id="15fed-175">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-175">0.00</span></span>      |
| <span data-ttu-id="15fed-176">Taikytinos mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="15fed-176">Cash discount amount to take</span></span> | <span data-ttu-id="15fed-177">6,00</span><span class="sxs-lookup"><span data-stu-id="15fed-177">6.00</span></span>      |

<span data-ttu-id="15fed-178">Kai Arnas užregistruoja mokėjimą, SF balansas yra 700,00.</span><span class="sxs-lookup"><span data-stu-id="15fed-178">After Arnie posts the payment, the invoice balance is 700.00.</span></span>

## <a name="partial-payment-before-the-second-cash-discount-date"></a><span data-ttu-id="15fed-179">Dalinis mokėjimas prieš antrąją mokėjimo nuolaidos datą</span><span class="sxs-lookup"><span data-stu-id="15fed-179">Partial payment before the second cash discount date</span></span>
<span data-ttu-id="15fed-180">Liepos 8 d. klientas sumoka likusią SF sumą.</span><span class="sxs-lookup"><span data-stu-id="15fed-180">On July 8, the customer pays the rest of the invoice amount.</span></span> <span data-ttu-id="15fed-181">Pritaikoma 7,00 nuolaida (1 procento), nes mokėjimas atliktas per antrąjį mokėjimo nuolaidos laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="15fed-181">A 7.00 discount (1 percent) is taken, because the payment was made within the second cash discount period.</span></span>

| <span data-ttu-id="15fed-182">Žymėti</span><span class="sxs-lookup"><span data-stu-id="15fed-182">Mark</span></span>     | <span data-ttu-id="15fed-183">Naudokite mokėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="15fed-183">Use cash discount</span></span> | <span data-ttu-id="15fed-184">Kvitas</span><span class="sxs-lookup"><span data-stu-id="15fed-184">Voucher</span></span>   | <span data-ttu-id="15fed-185">Paskyra</span><span class="sxs-lookup"><span data-stu-id="15fed-185">Account</span></span> | <span data-ttu-id="15fed-186">Data</span><span class="sxs-lookup"><span data-stu-id="15fed-186">Date</span></span>      | <span data-ttu-id="15fed-187">Terminas</span><span class="sxs-lookup"><span data-stu-id="15fed-187">Due date</span></span>  | <span data-ttu-id="15fed-188">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-188">Invoice</span></span> | <span data-ttu-id="15fed-189">Operacijos valiutos debeto suma</span><span class="sxs-lookup"><span data-stu-id="15fed-189">Amount in transaction currency debit</span></span> | <span data-ttu-id="15fed-190">Operacijos valiutos kredito suma</span><span class="sxs-lookup"><span data-stu-id="15fed-190">Amount in transaction currency credit</span></span> | <span data-ttu-id="15fed-191">Valiuta</span><span class="sxs-lookup"><span data-stu-id="15fed-191">Currency</span></span> | <span data-ttu-id="15fed-192">Sudengtina suma</span><span class="sxs-lookup"><span data-stu-id="15fed-192">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| <span data-ttu-id="15fed-193">Pasirinkta</span><span class="sxs-lookup"><span data-stu-id="15fed-193">Selected</span></span> | <span data-ttu-id="15fed-194">Įprastas</span><span class="sxs-lookup"><span data-stu-id="15fed-194">Normal</span></span>            | <span data-ttu-id="15fed-195">LFSF-10030</span><span class="sxs-lookup"><span data-stu-id="15fed-195">FTI-10030</span></span> | <span data-ttu-id="15fed-196">4031</span><span class="sxs-lookup"><span data-stu-id="15fed-196">4031</span></span>    | <span data-ttu-id="15fed-197">2015-06-25</span><span class="sxs-lookup"><span data-stu-id="15fed-197">6/25/2015</span></span> | <span data-ttu-id="15fed-198">2015-07-25</span><span class="sxs-lookup"><span data-stu-id="15fed-198">7/25/2015</span></span> | <span data-ttu-id="15fed-199">10030</span><span class="sxs-lookup"><span data-stu-id="15fed-199">10030</span></span>   | <span data-ttu-id="15fed-200">700,00</span><span class="sxs-lookup"><span data-stu-id="15fed-200">700.00</span></span>                               |                                       | <span data-ttu-id="15fed-201">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-201">USD</span></span>      | <span data-ttu-id="15fed-202">693,00</span><span class="sxs-lookup"><span data-stu-id="15fed-202">693.00</span></span>           |

<span data-ttu-id="15fed-203">Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.</span><span class="sxs-lookup"><span data-stu-id="15fed-203">Discount information appears at the bottom of the **Settle open transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="15fed-204">Mokėjimo nuolaidos data</span><span class="sxs-lookup"><span data-stu-id="15fed-204">Cash discount date</span></span>           | <span data-ttu-id="15fed-205">2015-07-09</span><span class="sxs-lookup"><span data-stu-id="15fed-205">7/09/2015</span></span> |
| <span data-ttu-id="15fed-206">Mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="15fed-206">Cash discount amount</span></span>         | <span data-ttu-id="15fed-207">30,00</span><span class="sxs-lookup"><span data-stu-id="15fed-207">30.00</span></span>     |
| <span data-ttu-id="15fed-208">Naudokite mokėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="15fed-208">Use cash discount</span></span>            | <span data-ttu-id="15fed-209">Įprastas</span><span class="sxs-lookup"><span data-stu-id="15fed-209">Normal</span></span>    |
| <span data-ttu-id="15fed-210">Pritaikyta mokėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="15fed-210">Cash discount taken</span></span>          | <span data-ttu-id="15fed-211">6,00</span><span class="sxs-lookup"><span data-stu-id="15fed-211">6.00</span></span>      |
| <span data-ttu-id="15fed-212">Taikytinos mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="15fed-212">Cash discount amount to take</span></span> | <span data-ttu-id="15fed-213">7,00</span><span class="sxs-lookup"><span data-stu-id="15fed-213">7.00</span></span>      |

<span data-ttu-id="15fed-214">Dabar SF balansas yra 0,00.</span><span class="sxs-lookup"><span data-stu-id="15fed-214">The invoice balance is now 0.00.</span></span> <span data-ttu-id="15fed-215">Arnas peržiūri šią operaciją puslapyje **Kliento operacijos**.</span><span class="sxs-lookup"><span data-stu-id="15fed-215">Arnie views the information on the **Customer transactions** page.</span></span>

| <span data-ttu-id="15fed-216">Kvitas</span><span class="sxs-lookup"><span data-stu-id="15fed-216">Voucher</span></span>    | <span data-ttu-id="15fed-217">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15fed-217">Transaction type</span></span> | <span data-ttu-id="15fed-218">Data</span><span class="sxs-lookup"><span data-stu-id="15fed-218">Date</span></span>      | <span data-ttu-id="15fed-219">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-219">Invoice</span></span> | <span data-ttu-id="15fed-220">Operacijos valiutos debeto suma</span><span class="sxs-lookup"><span data-stu-id="15fed-220">Amount in transaction currency debit</span></span> | <span data-ttu-id="15fed-221">Operacijos valiutos kredito suma</span><span class="sxs-lookup"><span data-stu-id="15fed-221">Amount in transaction currency credit</span></span> | <span data-ttu-id="15fed-222">Likutis</span><span class="sxs-lookup"><span data-stu-id="15fed-222">Balance</span></span> | <span data-ttu-id="15fed-223">Valiuta</span><span class="sxs-lookup"><span data-stu-id="15fed-223">Currency</span></span> |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| <span data-ttu-id="15fed-224">LFSF-10030</span><span class="sxs-lookup"><span data-stu-id="15fed-224">FTI-10030</span></span>  | <span data-ttu-id="15fed-225">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15fed-225">Invoice</span></span>          | <span data-ttu-id="15fed-226">2015-06-25</span><span class="sxs-lookup"><span data-stu-id="15fed-226">6/25/2015</span></span> | <span data-ttu-id="15fed-227">10030</span><span class="sxs-lookup"><span data-stu-id="15fed-227">10030</span></span>   | <span data-ttu-id="15fed-228">1000,00</span><span class="sxs-lookup"><span data-stu-id="15fed-228">1,000.00</span></span>                             |                                       | <span data-ttu-id="15fed-229">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-229">0.00</span></span>    | <span data-ttu-id="15fed-230">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-230">USD</span></span>      |
| <span data-ttu-id="15fed-231">ARP-10030</span><span class="sxs-lookup"><span data-stu-id="15fed-231">ARP-10030</span></span>  |  <span data-ttu-id="15fed-232">Mokėjimas</span><span class="sxs-lookup"><span data-stu-id="15fed-232">Payment</span></span>         | <span data-ttu-id="15fed-233">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="15fed-233">6/28/2015</span></span> |         |                                      | <span data-ttu-id="15fed-234">294,00</span><span class="sxs-lookup"><span data-stu-id="15fed-234">294.00</span></span>                                | <span data-ttu-id="15fed-235">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-235">0.00</span></span>    | <span data-ttu-id="15fed-236">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-236">USD</span></span>      |
| <span data-ttu-id="15fed-237">NUOL-10030</span><span class="sxs-lookup"><span data-stu-id="15fed-237">DISC-10030</span></span> |  <span data-ttu-id="15fed-238">Mokėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="15fed-238">Cash discount</span></span>   | <span data-ttu-id="15fed-239">2015-06-28</span><span class="sxs-lookup"><span data-stu-id="15fed-239">6/28/2015</span></span> |         |                                      | <span data-ttu-id="15fed-240">6,00</span><span class="sxs-lookup"><span data-stu-id="15fed-240">6.00</span></span>                                  | <span data-ttu-id="15fed-241">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-241">0.00</span></span>    | <span data-ttu-id="15fed-242">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-242">USD</span></span>      |
| <span data-ttu-id="15fed-243">ARP-10031</span><span class="sxs-lookup"><span data-stu-id="15fed-243">ARP-10031</span></span>  |  <span data-ttu-id="15fed-244">Mokėjimas</span><span class="sxs-lookup"><span data-stu-id="15fed-244">Payment</span></span>         | <span data-ttu-id="15fed-245">2015-07-08</span><span class="sxs-lookup"><span data-stu-id="15fed-245">7/8/2015</span></span>  |         |                                      | <span data-ttu-id="15fed-246">693,00</span><span class="sxs-lookup"><span data-stu-id="15fed-246">693.00</span></span>                                | <span data-ttu-id="15fed-247">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-247">0.00</span></span>    | <span data-ttu-id="15fed-248">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-248">USD</span></span>      |
| <span data-ttu-id="15fed-249">NUOL-1031</span><span class="sxs-lookup"><span data-stu-id="15fed-249">DISC-1031</span></span>  |  <span data-ttu-id="15fed-250">Mokėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="15fed-250">Cash discount</span></span>   | <span data-ttu-id="15fed-251">2015-07-08</span><span class="sxs-lookup"><span data-stu-id="15fed-251">7/8/2015</span></span>  |         |                                      | <span data-ttu-id="15fed-252">7,00</span><span class="sxs-lookup"><span data-stu-id="15fed-252">7.00</span></span>                                  | <span data-ttu-id="15fed-253">0,00</span><span class="sxs-lookup"><span data-stu-id="15fed-253">0.00</span></span>    | <span data-ttu-id="15fed-254">USD</span><span class="sxs-lookup"><span data-stu-id="15fed-254">USD</span></span>      |





