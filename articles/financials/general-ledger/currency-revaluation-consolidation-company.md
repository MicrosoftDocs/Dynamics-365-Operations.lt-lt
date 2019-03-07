---
title: Valiutos kurso pasikeitimas konsoliduotoje įmonėje
description: Šioje temoje aprašoma, kaip pakeisti valiutos kursą konsoliduotoje įmonėje.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "338756"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="2afd4-103">Valiutos kurso pasikeitimas konsoliduotoje įmonėje</span><span class="sxs-lookup"><span data-stu-id="2afd4-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2afd4-104">Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti.</span><span class="sxs-lookup"><span data-stu-id="2afd4-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="2afd4-105">Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="2afd4-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="2afd4-106">Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus.</span><span class="sxs-lookup"><span data-stu-id="2afd4-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="2afd4-107">Negautas pelnas arba nuostoliai tada atitinkamai atnaujinami atsižvelgiant į naują valiutos kursą ir datą.</span><span class="sxs-lookup"><span data-stu-id="2afd4-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="2afd4-108">Šiame pavyzdyje parodyti apskaitos įrašai, sukurti vykdant procesą.</span><span class="sxs-lookup"><span data-stu-id="2afd4-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="2afd4-109">Įmonės sąranka</span><span class="sxs-lookup"><span data-stu-id="2afd4-109">Company setup</span></span>
-   <span data-ttu-id="2afd4-110">**Šaltinio / veikianti įmonė (USMF)** – JAV doleriai (USD) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="2afd4-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="2afd4-111">**Konsoliduota įmonės (CON)** – eurai (EUR) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="2afd4-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="2afd4-112">**Gautas pelnas** – DK sąskaita 801500</span><span class="sxs-lookup"><span data-stu-id="2afd4-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="2afd4-113">**Patirtas nuostolis** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="2afd4-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2afd4-114">**Negautas pelnas** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="2afd4-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2afd4-115">**Nepatirtas nuostolis** – DK sąskaita 801400</span><span class="sxs-lookup"><span data-stu-id="2afd4-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="2afd4-116">Pradinės operacijos</span><span class="sxs-lookup"><span data-stu-id="2afd4-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="2afd4-117">Grynųjų pinigų gavimo operacijos USMF</span><span class="sxs-lookup"><span data-stu-id="2afd4-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="2afd4-118">Data</span><span class="sxs-lookup"><span data-stu-id="2afd4-118">Date</span></span>       | <span data-ttu-id="2afd4-119">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="2afd4-119">Ledger account</span></span>               | <span data-ttu-id="2afd4-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="2afd4-120">Currency</span></span> | <span data-ttu-id="2afd4-121">Suma</span><span class="sxs-lookup"><span data-stu-id="2afd4-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="2afd4-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2afd4-122">10/11/2015</span></span> | <span data-ttu-id="2afd4-123">110110 – grynieji</span><span class="sxs-lookup"><span data-stu-id="2afd4-123">110110 – Cash</span></span>                | <span data-ttu-id="2afd4-124">USD</span><span class="sxs-lookup"><span data-stu-id="2afd4-124">USD</span></span>      | <span data-ttu-id="2afd4-125">500</span><span class="sxs-lookup"><span data-stu-id="2afd4-125">500</span></span>    |
| <span data-ttu-id="2afd4-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2afd4-126">10/11/2015</span></span> | <span data-ttu-id="2afd4-127">130100 – gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="2afd4-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="2afd4-128">USD</span><span class="sxs-lookup"><span data-stu-id="2afd4-128">USD</span></span>      | <span data-ttu-id="2afd4-129">–500</span><span class="sxs-lookup"><span data-stu-id="2afd4-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="2afd4-130">Valiutos kursai</span><span class="sxs-lookup"><span data-stu-id="2afd4-130">Exchange rates</span></span>

| <span data-ttu-id="2afd4-131">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="2afd4-131">From currency</span></span> | <span data-ttu-id="2afd4-132">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="2afd4-132">To currency</span></span> | <span data-ttu-id="2afd4-133">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="2afd4-133">Start date</span></span> | <span data-ttu-id="2afd4-134">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="2afd4-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="2afd4-135">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-135">EUR</span></span>           | <span data-ttu-id="2afd4-136">USD</span><span class="sxs-lookup"><span data-stu-id="2afd4-136">USD</span></span>         | <span data-ttu-id="2afd4-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="2afd4-137">10/1/2015</span></span>  | <span data-ttu-id="2afd4-138">200</span><span class="sxs-lookup"><span data-stu-id="2afd4-138">200</span></span>           |
| <span data-ttu-id="2afd4-139">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-139">EUR</span></span>           | <span data-ttu-id="2afd4-140">USD</span><span class="sxs-lookup"><span data-stu-id="2afd4-140">USD</span></span>         | <span data-ttu-id="2afd4-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="2afd4-141">11/1/2015</span></span>  | <span data-ttu-id="2afd4-142">150</span><span class="sxs-lookup"><span data-stu-id="2afd4-142">150</span></span>           |
| <span data-ttu-id="2afd4-143">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-143">EUR</span></span>           | <span data-ttu-id="2afd4-144">USD</span><span class="sxs-lookup"><span data-stu-id="2afd4-144">USD</span></span>         | <span data-ttu-id="2afd4-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="2afd4-145">12/1/2012</span></span>  | <span data-ttu-id="2afd4-146">100</span><span class="sxs-lookup"><span data-stu-id="2afd4-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="2afd4-147">2015 m. spalio konsolidavimas</span><span class="sxs-lookup"><span data-stu-id="2afd4-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2afd4-148">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="2afd4-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="2afd4-149">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="2afd4-149">Ledger account</span></span> | <span data-ttu-id="2afd4-150">Valiuta</span><span class="sxs-lookup"><span data-stu-id="2afd4-150">Currency</span></span> | <span data-ttu-id="2afd4-151">Suma</span><span class="sxs-lookup"><span data-stu-id="2afd4-151">Amount</span></span> | <span data-ttu-id="2afd4-152">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="2afd4-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="2afd4-153">110110</span><span class="sxs-lookup"><span data-stu-id="2afd4-153">110110</span></span>         | <span data-ttu-id="2afd4-154">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-154">EUR</span></span>      | <span data-ttu-id="2afd4-155">250</span><span class="sxs-lookup"><span data-stu-id="2afd4-155">250</span></span>    | <span data-ttu-id="2afd4-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="2afd4-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="2afd4-157">130100</span><span class="sxs-lookup"><span data-stu-id="2afd4-157">130100</span></span>         | <span data-ttu-id="2afd4-158">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-158">EUR</span></span>      | <span data-ttu-id="2afd4-159">–250</span><span class="sxs-lookup"><span data-stu-id="2afd4-159">-250</span></span>   | <span data-ttu-id="2afd4-160">–500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="2afd4-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="2afd4-161">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. lapkričio 30 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="2afd4-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2afd4-162">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="2afd4-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="2afd4-163">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="2afd4-163">Ledger account</span></span> | <span data-ttu-id="2afd4-164">Valiuta</span><span class="sxs-lookup"><span data-stu-id="2afd4-164">Currency</span></span> | <span data-ttu-id="2afd4-165">Suma</span><span class="sxs-lookup"><span data-stu-id="2afd4-165">Amount</span></span>  | <span data-ttu-id="2afd4-166">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="2afd4-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="2afd4-167">110110</span><span class="sxs-lookup"><span data-stu-id="2afd4-167">110110</span></span>         | <span data-ttu-id="2afd4-168">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-168">EUR</span></span>      | <span data-ttu-id="2afd4-169">333.33</span><span class="sxs-lookup"><span data-stu-id="2afd4-169">333.33</span></span>  | <span data-ttu-id="2afd4-170">Pradinė suma 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="2afd4-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="2afd4-171">130100</span><span class="sxs-lookup"><span data-stu-id="2afd4-171">130100</span></span>         | <span data-ttu-id="2afd4-172">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-172">EUR</span></span>      | <span data-ttu-id="2afd4-173">–333,33</span><span class="sxs-lookup"><span data-stu-id="2afd4-173">-333.33</span></span> | <span data-ttu-id="2afd4-174">Pradinė suma –500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="2afd4-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="2afd4-175">801400</span><span class="sxs-lookup"><span data-stu-id="2afd4-175">801400</span></span>         | <span data-ttu-id="2afd4-176">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-176">EUR</span></span>      | <span data-ttu-id="2afd4-177">83.33</span><span class="sxs-lookup"><span data-stu-id="2afd4-177">83.33</span></span>   | <span data-ttu-id="2afd4-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="2afd4-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="2afd4-179">801600</span><span class="sxs-lookup"><span data-stu-id="2afd4-179">801600</span></span>         | <span data-ttu-id="2afd4-180">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-180">EUR</span></span>      | <span data-ttu-id="2afd4-181">–83,33</span><span class="sxs-lookup"><span data-stu-id="2afd4-181">-83.33</span></span>  | <span data-ttu-id="2afd4-182">-333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="2afd4-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="2afd4-183">Matysite papildomas ataskaitų valiutos sumų operacijas.</span><span class="sxs-lookup"><span data-stu-id="2afd4-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="2afd4-184">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. gruodžio 31 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="2afd4-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2afd4-185">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="2afd4-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="2afd4-186">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="2afd4-186">Ledger account</span></span> | <span data-ttu-id="2afd4-187">Valiuta</span><span class="sxs-lookup"><span data-stu-id="2afd4-187">Currency</span></span> | <span data-ttu-id="2afd4-188">Suma</span><span class="sxs-lookup"><span data-stu-id="2afd4-188">Amount</span></span>  | <span data-ttu-id="2afd4-189">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="2afd4-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="2afd4-190">110110</span><span class="sxs-lookup"><span data-stu-id="2afd4-190">110110</span></span>         | <span data-ttu-id="2afd4-191">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-191">EUR</span></span>      | <span data-ttu-id="2afd4-192">500,00</span><span class="sxs-lookup"><span data-stu-id="2afd4-192">500.00</span></span>  | <span data-ttu-id="2afd4-193">Pradinė suma 500 × 1</span><span class="sxs-lookup"><span data-stu-id="2afd4-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="2afd4-194">130100</span><span class="sxs-lookup"><span data-stu-id="2afd4-194">130100</span></span>         | <span data-ttu-id="2afd4-195">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-195">EUR</span></span>      | <span data-ttu-id="2afd4-196">–500,00</span><span class="sxs-lookup"><span data-stu-id="2afd4-196">-500.00</span></span> | <span data-ttu-id="2afd4-197">Pradinė suma –500 × 1</span><span class="sxs-lookup"><span data-stu-id="2afd4-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="2afd4-198">801400</span><span class="sxs-lookup"><span data-stu-id="2afd4-198">801400</span></span>         | <span data-ttu-id="2afd4-199">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-199">EUR</span></span>      | <span data-ttu-id="2afd4-200">250</span><span class="sxs-lookup"><span data-stu-id="2afd4-200">250</span></span>     | <span data-ttu-id="2afd4-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="2afd4-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="2afd4-202">801600</span><span class="sxs-lookup"><span data-stu-id="2afd4-202">801600</span></span>         | <span data-ttu-id="2afd4-203">EUR</span><span class="sxs-lookup"><span data-stu-id="2afd4-203">EUR</span></span>      | <span data-ttu-id="2afd4-204">–250</span><span class="sxs-lookup"><span data-stu-id="2afd4-204">-250</span></span>    | <span data-ttu-id="2afd4-205">-500 – (–333,33) = –166,67 – 166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="2afd4-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





