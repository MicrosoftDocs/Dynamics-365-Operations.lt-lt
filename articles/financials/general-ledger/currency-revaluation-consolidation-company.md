---
title: "Valiutos kurso pasikeitimas konsoliduotoje įmonėje"
description: "Šioje temoje aprašoma, kaip pakeisti valiutos kursą konsoliduotoje įmonėje."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 27059b0d2a781453a7594bdc430005df6ea5c167
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="9262a-103">Valiutos kurso pasikeitimas konsoliduotoje įmonėje</span><span class="sxs-lookup"><span data-stu-id="9262a-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="9262a-104">Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti.</span><span class="sxs-lookup"><span data-stu-id="9262a-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="9262a-105">Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="9262a-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="9262a-106">Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus.</span><span class="sxs-lookup"><span data-stu-id="9262a-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="9262a-107">Negautas pelnas arba nuostoliai tada atitinkamai atnaujinami atsižvelgiant į naują valiutos kursą ir datą.</span><span class="sxs-lookup"><span data-stu-id="9262a-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="9262a-108">Šiame pavyzdyje parodyti apskaitos įrašai, sukurti vykdant procesą.</span><span class="sxs-lookup"><span data-stu-id="9262a-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="9262a-109">Įmonės sąranka</span><span class="sxs-lookup"><span data-stu-id="9262a-109">Company setup</span></span>
-   <span data-ttu-id="9262a-110">**Šaltinio / veikianti įmonė (USMF)** – JAV doleriai (USD) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="9262a-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="9262a-111">**Konsoliduota įmonės (CON)** – eurai (EUR) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="9262a-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="9262a-112">**Gautas pelnas **– DK sąskaita 801500</span><span class="sxs-lookup"><span data-stu-id="9262a-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="9262a-113">**Patirtas nuostolis** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="9262a-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="9262a-114">**Negautas pelnas** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="9262a-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="9262a-115">**Nepatirtas nuostolis** – DK sąskaita 801400</span><span class="sxs-lookup"><span data-stu-id="9262a-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="9262a-116">Pradinės operacijos</span><span class="sxs-lookup"><span data-stu-id="9262a-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="9262a-117">Grynųjų pinigų gavimo operacijos USMF</span><span class="sxs-lookup"><span data-stu-id="9262a-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="9262a-118">Data</span><span class="sxs-lookup"><span data-stu-id="9262a-118">Date</span></span>       | <span data-ttu-id="9262a-119">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="9262a-119">Ledger account</span></span>               | <span data-ttu-id="9262a-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="9262a-120">Currency</span></span> | <span data-ttu-id="9262a-121">Suma</span><span class="sxs-lookup"><span data-stu-id="9262a-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="9262a-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="9262a-122">10/11/2015</span></span> | <span data-ttu-id="9262a-123">110110 – grynieji</span><span class="sxs-lookup"><span data-stu-id="9262a-123">110110 – Cash</span></span>                | <span data-ttu-id="9262a-124">USD</span><span class="sxs-lookup"><span data-stu-id="9262a-124">USD</span></span>      | <span data-ttu-id="9262a-125">500</span><span class="sxs-lookup"><span data-stu-id="9262a-125">500</span></span>    |
| <span data-ttu-id="9262a-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="9262a-126">10/11/2015</span></span> | <span data-ttu-id="9262a-127">130100 – gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="9262a-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="9262a-128">USD</span><span class="sxs-lookup"><span data-stu-id="9262a-128">USD</span></span>      | <span data-ttu-id="9262a-129">–500</span><span class="sxs-lookup"><span data-stu-id="9262a-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="9262a-130">Valiutos kursai</span><span class="sxs-lookup"><span data-stu-id="9262a-130">Exchange rates</span></span>
| <span data-ttu-id="9262a-131">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="9262a-131">From currency</span></span> | <span data-ttu-id="9262a-132">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="9262a-132">To currency</span></span> | <span data-ttu-id="9262a-133">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="9262a-133">Start date</span></span> | <span data-ttu-id="9262a-134">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="9262a-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="9262a-135">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-135">EUR</span></span>           | <span data-ttu-id="9262a-136">USD</span><span class="sxs-lookup"><span data-stu-id="9262a-136">USD</span></span>         | <span data-ttu-id="9262a-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="9262a-137">10/1/2015</span></span>  | <span data-ttu-id="9262a-138">200</span><span class="sxs-lookup"><span data-stu-id="9262a-138">200</span></span>           |
| <span data-ttu-id="9262a-139">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-139">EUR</span></span>           | <span data-ttu-id="9262a-140">USD</span><span class="sxs-lookup"><span data-stu-id="9262a-140">USD</span></span>         | <span data-ttu-id="9262a-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="9262a-141">11/1/2015</span></span>  | <span data-ttu-id="9262a-142">150</span><span class="sxs-lookup"><span data-stu-id="9262a-142">150</span></span>           |
| <span data-ttu-id="9262a-143">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-143">EUR</span></span>           | <span data-ttu-id="9262a-144">USD</span><span class="sxs-lookup"><span data-stu-id="9262a-144">USD</span></span>         | <span data-ttu-id="9262a-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="9262a-145">12/1/2012</span></span>  | <span data-ttu-id="9262a-146">100</span><span class="sxs-lookup"><span data-stu-id="9262a-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="9262a-147">2015 m. spalio konsolidavimas</span><span class="sxs-lookup"><span data-stu-id="9262a-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="9262a-148">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="9262a-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="9262a-149">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="9262a-149">Ledger account</span></span> | <span data-ttu-id="9262a-150">Valiuta</span><span class="sxs-lookup"><span data-stu-id="9262a-150">Currency</span></span> | <span data-ttu-id="9262a-151">Suma</span><span class="sxs-lookup"><span data-stu-id="9262a-151">Amount</span></span> | <span data-ttu-id="9262a-152">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9262a-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="9262a-153">110110</span><span class="sxs-lookup"><span data-stu-id="9262a-153">110110</span></span>         | <span data-ttu-id="9262a-154">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-154">EUR</span></span>      | <span data-ttu-id="9262a-155">250</span><span class="sxs-lookup"><span data-stu-id="9262a-155">250</span></span>    | <span data-ttu-id="9262a-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="9262a-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="9262a-157">130100</span><span class="sxs-lookup"><span data-stu-id="9262a-157">130100</span></span>         | <span data-ttu-id="9262a-158">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-158">EUR</span></span>      | <span data-ttu-id="9262a-159">–250</span><span class="sxs-lookup"><span data-stu-id="9262a-159">-250</span></span>   | <span data-ttu-id="9262a-160">–500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="9262a-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="9262a-161">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. lapkričio 30 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="9262a-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="9262a-162">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="9262a-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="9262a-163">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="9262a-163">Ledger account</span></span> | <span data-ttu-id="9262a-164">Valiuta</span><span class="sxs-lookup"><span data-stu-id="9262a-164">Currency</span></span> | <span data-ttu-id="9262a-165">Suma</span><span class="sxs-lookup"><span data-stu-id="9262a-165">Amount</span></span>  | <span data-ttu-id="9262a-166">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9262a-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="9262a-167">110110</span><span class="sxs-lookup"><span data-stu-id="9262a-167">110110</span></span>         | <span data-ttu-id="9262a-168">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-168">EUR</span></span>      | <span data-ttu-id="9262a-169">333.33</span><span class="sxs-lookup"><span data-stu-id="9262a-169">333.33</span></span>  | <span data-ttu-id="9262a-170">Pradinė suma 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="9262a-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="9262a-171">130100</span><span class="sxs-lookup"><span data-stu-id="9262a-171">130100</span></span>         | <span data-ttu-id="9262a-172">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-172">EUR</span></span>      | <span data-ttu-id="9262a-173">–333,33</span><span class="sxs-lookup"><span data-stu-id="9262a-173">-333.33</span></span> | <span data-ttu-id="9262a-174">Pradinė suma –500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="9262a-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="9262a-175">801400</span><span class="sxs-lookup"><span data-stu-id="9262a-175">801400</span></span>         | <span data-ttu-id="9262a-176">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-176">EUR</span></span>      | <span data-ttu-id="9262a-177">83.33</span><span class="sxs-lookup"><span data-stu-id="9262a-177">83.33</span></span>   | <span data-ttu-id="9262a-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="9262a-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="9262a-179">801600</span><span class="sxs-lookup"><span data-stu-id="9262a-179">801600</span></span>         | <span data-ttu-id="9262a-180">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-180">EUR</span></span>      | <span data-ttu-id="9262a-181">–83,33</span><span class="sxs-lookup"><span data-stu-id="9262a-181">-83.33</span></span>  | <span data-ttu-id="9262a-182">-333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="9262a-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="9262a-183">Matysite papildomas ataskaitų valiutos sumų operacijas.</span><span class="sxs-lookup"><span data-stu-id="9262a-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="9262a-184">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. gruodžio 31 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="9262a-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="9262a-185">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="9262a-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="9262a-186">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="9262a-186">Ledger account</span></span> | <span data-ttu-id="9262a-187">Valiuta</span><span class="sxs-lookup"><span data-stu-id="9262a-187">Currency</span></span> | <span data-ttu-id="9262a-188">Suma</span><span class="sxs-lookup"><span data-stu-id="9262a-188">Amount</span></span>  | <span data-ttu-id="9262a-189">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9262a-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="9262a-190">110110</span><span class="sxs-lookup"><span data-stu-id="9262a-190">110110</span></span>         | <span data-ttu-id="9262a-191">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-191">EUR</span></span>      | <span data-ttu-id="9262a-192">500,00</span><span class="sxs-lookup"><span data-stu-id="9262a-192">500.00</span></span>  | <span data-ttu-id="9262a-193">Pradinė suma 500 × 1</span><span class="sxs-lookup"><span data-stu-id="9262a-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="9262a-194">130100</span><span class="sxs-lookup"><span data-stu-id="9262a-194">130100</span></span>         | <span data-ttu-id="9262a-195">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-195">EUR</span></span>      | <span data-ttu-id="9262a-196">–500,00</span><span class="sxs-lookup"><span data-stu-id="9262a-196">-500.00</span></span> | <span data-ttu-id="9262a-197">Pradinė suma –500 × 1</span><span class="sxs-lookup"><span data-stu-id="9262a-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="9262a-198">801400</span><span class="sxs-lookup"><span data-stu-id="9262a-198">801400</span></span>         | <span data-ttu-id="9262a-199">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-199">EUR</span></span>      | <span data-ttu-id="9262a-200">250</span><span class="sxs-lookup"><span data-stu-id="9262a-200">250</span></span>     | <span data-ttu-id="9262a-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="9262a-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="9262a-202">801600</span><span class="sxs-lookup"><span data-stu-id="9262a-202">801600</span></span>         | <span data-ttu-id="9262a-203">EUR</span><span class="sxs-lookup"><span data-stu-id="9262a-203">EUR</span></span>      | <span data-ttu-id="9262a-204">–250</span><span class="sxs-lookup"><span data-stu-id="9262a-204">-250</span></span>    | <span data-ttu-id="9262a-205">-500 – (–333,33) = –166,67 – 166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="9262a-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






