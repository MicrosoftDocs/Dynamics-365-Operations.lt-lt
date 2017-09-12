---
title: "Valiutos kurso pasikeitimas į konsoliduotoje įmonėje"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="4d3fb-102">Valiutos kurso pasikeitimas į konsoliduotoje įmonėje</span><span class="sxs-lookup"><span data-stu-id="4d3fb-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="4d3fb-103">Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="4d3fb-104">Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="4d3fb-105">Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="4d3fb-106">Negautas pelnas arba nuostoliai tada atitinkamai atnaujinami atsižvelgiant į naują valiutos kursą ir datą.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="4d3fb-107">Šiame pavyzdyje parodyti apskaitos įrašai, sukurti vykdant procesą.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="4d3fb-108">Įmonės sąranka</span><span class="sxs-lookup"><span data-stu-id="4d3fb-108">Company setup</span></span>
-   <span data-ttu-id="4d3fb-109">**Šaltinio / veikianti įmonė (USMF)** – JAV doleriai (USD) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="4d3fb-110">**Konsoliduota įmonės (CON)** – eurai (EUR) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="4d3fb-111">**Gautas pelnas **– DK sąskaita 801500</span><span class="sxs-lookup"><span data-stu-id="4d3fb-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="4d3fb-112">**Patirtas nuostolis** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="4d3fb-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="4d3fb-113">**Negautas pelnas** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="4d3fb-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="4d3fb-114">**Nepatirtas nuostolis** – DK sąskaita 801400</span><span class="sxs-lookup"><span data-stu-id="4d3fb-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="4d3fb-115">Pradinės operacijos</span><span class="sxs-lookup"><span data-stu-id="4d3fb-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="4d3fb-116">Grynųjų pinigų gavimo operacijos USMF</span><span class="sxs-lookup"><span data-stu-id="4d3fb-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="4d3fb-117">Data</span><span class="sxs-lookup"><span data-stu-id="4d3fb-117">Date</span></span>       | <span data-ttu-id="4d3fb-118">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="4d3fb-118">Ledger account</span></span>               | <span data-ttu-id="4d3fb-119">Valiuta</span><span class="sxs-lookup"><span data-stu-id="4d3fb-119">Currency</span></span> | <span data-ttu-id="4d3fb-120">Suma</span><span class="sxs-lookup"><span data-stu-id="4d3fb-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="4d3fb-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="4d3fb-121">10/11/2015</span></span> | <span data-ttu-id="4d3fb-122">110110 – grynieji</span><span class="sxs-lookup"><span data-stu-id="4d3fb-122">110110 – Cash</span></span>                | <span data-ttu-id="4d3fb-123">USD</span><span class="sxs-lookup"><span data-stu-id="4d3fb-123">USD</span></span>      | <span data-ttu-id="4d3fb-124">500</span><span class="sxs-lookup"><span data-stu-id="4d3fb-124">500</span></span>    |
| <span data-ttu-id="4d3fb-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="4d3fb-125">10/11/2015</span></span> | <span data-ttu-id="4d3fb-126">130100 – gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="4d3fb-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="4d3fb-127">USD</span><span class="sxs-lookup"><span data-stu-id="4d3fb-127">USD</span></span>      | <span data-ttu-id="4d3fb-128">–500</span><span class="sxs-lookup"><span data-stu-id="4d3fb-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="4d3fb-129">Valiutos kursai</span><span class="sxs-lookup"><span data-stu-id="4d3fb-129">Exchange rates</span></span>
| <span data-ttu-id="4d3fb-130">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="4d3fb-130">From currency</span></span> | <span data-ttu-id="4d3fb-131">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="4d3fb-131">To currency</span></span> | <span data-ttu-id="4d3fb-132">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="4d3fb-132">Start date</span></span> | <span data-ttu-id="4d3fb-133">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="4d3fb-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="4d3fb-134">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-134">EUR</span></span>           | <span data-ttu-id="4d3fb-135">USD</span><span class="sxs-lookup"><span data-stu-id="4d3fb-135">USD</span></span>         | <span data-ttu-id="4d3fb-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="4d3fb-136">10/1/2015</span></span>  | <span data-ttu-id="4d3fb-137">200</span><span class="sxs-lookup"><span data-stu-id="4d3fb-137">200</span></span>           |
| <span data-ttu-id="4d3fb-138">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-138">EUR</span></span>           | <span data-ttu-id="4d3fb-139">USD</span><span class="sxs-lookup"><span data-stu-id="4d3fb-139">USD</span></span>         | <span data-ttu-id="4d3fb-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="4d3fb-140">11/1/2015</span></span>  | <span data-ttu-id="4d3fb-141">150</span><span class="sxs-lookup"><span data-stu-id="4d3fb-141">150</span></span>           |
| <span data-ttu-id="4d3fb-142">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-142">EUR</span></span>           | <span data-ttu-id="4d3fb-143">USD</span><span class="sxs-lookup"><span data-stu-id="4d3fb-143">USD</span></span>         | <span data-ttu-id="4d3fb-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="4d3fb-144">12/1/2012</span></span>  | <span data-ttu-id="4d3fb-145">100</span><span class="sxs-lookup"><span data-stu-id="4d3fb-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="4d3fb-146">2015 m. spalio konsolidavimas</span><span class="sxs-lookup"><span data-stu-id="4d3fb-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4d3fb-147">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="4d3fb-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="4d3fb-148">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="4d3fb-148">Ledger account</span></span> | <span data-ttu-id="4d3fb-149">Valiuta</span><span class="sxs-lookup"><span data-stu-id="4d3fb-149">Currency</span></span> | <span data-ttu-id="4d3fb-150">Suma</span><span class="sxs-lookup"><span data-stu-id="4d3fb-150">Amount</span></span> | <span data-ttu-id="4d3fb-151">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="4d3fb-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="4d3fb-152">110110</span><span class="sxs-lookup"><span data-stu-id="4d3fb-152">110110</span></span>         | <span data-ttu-id="4d3fb-153">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-153">EUR</span></span>      | <span data-ttu-id="4d3fb-154">250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-154">250</span></span>    | <span data-ttu-id="4d3fb-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="4d3fb-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="4d3fb-156">130100</span><span class="sxs-lookup"><span data-stu-id="4d3fb-156">130100</span></span>         | <span data-ttu-id="4d3fb-157">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-157">EUR</span></span>      | <span data-ttu-id="4d3fb-158">–250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-158">-250</span></span>   | <span data-ttu-id="4d3fb-159">–500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="4d3fb-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="4d3fb-160">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. lapkričio 30 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="4d3fb-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4d3fb-161">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="4d3fb-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="4d3fb-162">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="4d3fb-162">Ledger account</span></span> | <span data-ttu-id="4d3fb-163">Valiuta</span><span class="sxs-lookup"><span data-stu-id="4d3fb-163">Currency</span></span> | <span data-ttu-id="4d3fb-164">Suma</span><span class="sxs-lookup"><span data-stu-id="4d3fb-164">Amount</span></span>  | <span data-ttu-id="4d3fb-165">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="4d3fb-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="4d3fb-166">110110</span><span class="sxs-lookup"><span data-stu-id="4d3fb-166">110110</span></span>         | <span data-ttu-id="4d3fb-167">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-167">EUR</span></span>      | <span data-ttu-id="4d3fb-168">333.33</span><span class="sxs-lookup"><span data-stu-id="4d3fb-168">333.33</span></span>  | <span data-ttu-id="4d3fb-169">Pradinė suma 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="4d3fb-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="4d3fb-170">130100</span><span class="sxs-lookup"><span data-stu-id="4d3fb-170">130100</span></span>         | <span data-ttu-id="4d3fb-171">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-171">EUR</span></span>      | <span data-ttu-id="4d3fb-172">–333,33</span><span class="sxs-lookup"><span data-stu-id="4d3fb-172">-333.33</span></span> | <span data-ttu-id="4d3fb-173">Pradinė suma –500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="4d3fb-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="4d3fb-174">801400</span><span class="sxs-lookup"><span data-stu-id="4d3fb-174">801400</span></span>         | <span data-ttu-id="4d3fb-175">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-175">EUR</span></span>      | <span data-ttu-id="4d3fb-176">83.33</span><span class="sxs-lookup"><span data-stu-id="4d3fb-176">83.33</span></span>   | <span data-ttu-id="4d3fb-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="4d3fb-178">801600</span><span class="sxs-lookup"><span data-stu-id="4d3fb-178">801600</span></span>         | <span data-ttu-id="4d3fb-179">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-179">EUR</span></span>      | <span data-ttu-id="4d3fb-180">–83,33</span><span class="sxs-lookup"><span data-stu-id="4d3fb-180">-83.33</span></span>  | <span data-ttu-id="4d3fb-181">-333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="4d3fb-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="4d3fb-182">Matysite papildomas ataskaitų valiutos sumų operacijas.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="4d3fb-183">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. gruodžio 31 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="4d3fb-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4d3fb-184">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="4d3fb-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="4d3fb-185">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="4d3fb-185">Ledger account</span></span> | <span data-ttu-id="4d3fb-186">Valiuta</span><span class="sxs-lookup"><span data-stu-id="4d3fb-186">Currency</span></span> | <span data-ttu-id="4d3fb-187">Suma</span><span class="sxs-lookup"><span data-stu-id="4d3fb-187">Amount</span></span>  | <span data-ttu-id="4d3fb-188">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="4d3fb-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="4d3fb-189">110110</span><span class="sxs-lookup"><span data-stu-id="4d3fb-189">110110</span></span>         | <span data-ttu-id="4d3fb-190">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-190">EUR</span></span>      | <span data-ttu-id="4d3fb-191">500,00</span><span class="sxs-lookup"><span data-stu-id="4d3fb-191">500.00</span></span>  | <span data-ttu-id="4d3fb-192">Pradinė suma 500 × 1</span><span class="sxs-lookup"><span data-stu-id="4d3fb-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="4d3fb-193">130100</span><span class="sxs-lookup"><span data-stu-id="4d3fb-193">130100</span></span>         | <span data-ttu-id="4d3fb-194">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-194">EUR</span></span>      | <span data-ttu-id="4d3fb-195">–500,00</span><span class="sxs-lookup"><span data-stu-id="4d3fb-195">-500.00</span></span> | <span data-ttu-id="4d3fb-196">Pradinė suma –500 × 1</span><span class="sxs-lookup"><span data-stu-id="4d3fb-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="4d3fb-197">801400</span><span class="sxs-lookup"><span data-stu-id="4d3fb-197">801400</span></span>         | <span data-ttu-id="4d3fb-198">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-198">EUR</span></span>      | <span data-ttu-id="4d3fb-199">250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-199">250</span></span>     | <span data-ttu-id="4d3fb-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="4d3fb-201">801600</span><span class="sxs-lookup"><span data-stu-id="4d3fb-201">801600</span></span>         | <span data-ttu-id="4d3fb-202">EUR</span><span class="sxs-lookup"><span data-stu-id="4d3fb-202">EUR</span></span>      | <span data-ttu-id="4d3fb-203">–250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-203">-250</span></span>    | <span data-ttu-id="4d3fb-204">-500 – (–333,33) = –166,67 – 166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="4d3fb-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






