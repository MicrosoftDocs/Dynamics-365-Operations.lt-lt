---
title: Valiutos kurso pasikeitimas konsoliduotoje įmonėje
description: Šioje temoje aprašoma, kaip pakeisti valiutos kursą konsoliduotoje įmonėje.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212234"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f09ec-103">Valiutos kurso pasikeitimas konsoliduotoje įmonėje</span><span class="sxs-lookup"><span data-stu-id="f09ec-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f09ec-104">Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti.</span><span class="sxs-lookup"><span data-stu-id="f09ec-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f09ec-105">Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="f09ec-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f09ec-106">Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus.</span><span class="sxs-lookup"><span data-stu-id="f09ec-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f09ec-107">Negautas pelnas arba nuostoliai tada atitinkamai atnaujinami atsižvelgiant į naują valiutos kursą ir datą.</span><span class="sxs-lookup"><span data-stu-id="f09ec-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f09ec-108">Šiame pavyzdyje parodyti apskaitos įrašai, sukurti vykdant procesą.</span><span class="sxs-lookup"><span data-stu-id="f09ec-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f09ec-109">Įmonės sąranka</span><span class="sxs-lookup"><span data-stu-id="f09ec-109">Company setup</span></span>
-   <span data-ttu-id="f09ec-110">**Šaltinio / veikianti įmonė (USMF)** – JAV doleriai (USD) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="f09ec-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f09ec-111">**Konsoliduota įmonės (CON)** – eurai (EUR) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="f09ec-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f09ec-112">**Gautas pelnas** – DK sąskaita 801500</span><span class="sxs-lookup"><span data-stu-id="f09ec-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="f09ec-113">**Patirtas nuostolis** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="f09ec-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f09ec-114">**Negautas pelnas** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="f09ec-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f09ec-115">**Nepatirtas nuostolis** – DK sąskaita 801400</span><span class="sxs-lookup"><span data-stu-id="f09ec-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f09ec-116">Pradinės operacijos</span><span class="sxs-lookup"><span data-stu-id="f09ec-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f09ec-117">Grynųjų pinigų gavimo operacijos USMF</span><span class="sxs-lookup"><span data-stu-id="f09ec-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f09ec-118">Data</span><span class="sxs-lookup"><span data-stu-id="f09ec-118">Date</span></span>       | <span data-ttu-id="f09ec-119">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="f09ec-119">Ledger account</span></span>               | <span data-ttu-id="f09ec-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="f09ec-120">Currency</span></span> | <span data-ttu-id="f09ec-121">Suma</span><span class="sxs-lookup"><span data-stu-id="f09ec-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f09ec-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="f09ec-122">10/11/2015</span></span> | <span data-ttu-id="f09ec-123">110110 – grynieji</span><span class="sxs-lookup"><span data-stu-id="f09ec-123">110110 – Cash</span></span>                | <span data-ttu-id="f09ec-124">USD</span><span class="sxs-lookup"><span data-stu-id="f09ec-124">USD</span></span>      | <span data-ttu-id="f09ec-125">500</span><span class="sxs-lookup"><span data-stu-id="f09ec-125">500</span></span>    |
| <span data-ttu-id="f09ec-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="f09ec-126">10/11/2015</span></span> | <span data-ttu-id="f09ec-127">130100 – gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="f09ec-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f09ec-128">USD</span><span class="sxs-lookup"><span data-stu-id="f09ec-128">USD</span></span>      | <span data-ttu-id="f09ec-129">–500</span><span class="sxs-lookup"><span data-stu-id="f09ec-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f09ec-130">Valiutos kursai</span><span class="sxs-lookup"><span data-stu-id="f09ec-130">Exchange rates</span></span>

| <span data-ttu-id="f09ec-131">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="f09ec-131">From currency</span></span> | <span data-ttu-id="f09ec-132">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="f09ec-132">To currency</span></span> | <span data-ttu-id="f09ec-133">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="f09ec-133">Start date</span></span> | <span data-ttu-id="f09ec-134">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="f09ec-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f09ec-135">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-135">EUR</span></span>           | <span data-ttu-id="f09ec-136">USD</span><span class="sxs-lookup"><span data-stu-id="f09ec-136">USD</span></span>         | <span data-ttu-id="f09ec-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="f09ec-137">10/1/2015</span></span>  | <span data-ttu-id="f09ec-138">200</span><span class="sxs-lookup"><span data-stu-id="f09ec-138">200</span></span>           |
| <span data-ttu-id="f09ec-139">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-139">EUR</span></span>           | <span data-ttu-id="f09ec-140">USD</span><span class="sxs-lookup"><span data-stu-id="f09ec-140">USD</span></span>         | <span data-ttu-id="f09ec-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="f09ec-141">11/1/2015</span></span>  | <span data-ttu-id="f09ec-142">150</span><span class="sxs-lookup"><span data-stu-id="f09ec-142">150</span></span>           |
| <span data-ttu-id="f09ec-143">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-143">EUR</span></span>           | <span data-ttu-id="f09ec-144">USD</span><span class="sxs-lookup"><span data-stu-id="f09ec-144">USD</span></span>         | <span data-ttu-id="f09ec-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="f09ec-145">12/1/2012</span></span>  | <span data-ttu-id="f09ec-146">100</span><span class="sxs-lookup"><span data-stu-id="f09ec-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f09ec-147">2015 m. spalio konsolidavimas</span><span class="sxs-lookup"><span data-stu-id="f09ec-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f09ec-148">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="f09ec-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="f09ec-149">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="f09ec-149">Ledger account</span></span> | <span data-ttu-id="f09ec-150">Valiuta</span><span class="sxs-lookup"><span data-stu-id="f09ec-150">Currency</span></span> | <span data-ttu-id="f09ec-151">Suma</span><span class="sxs-lookup"><span data-stu-id="f09ec-151">Amount</span></span> | <span data-ttu-id="f09ec-152">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="f09ec-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f09ec-153">110110</span><span class="sxs-lookup"><span data-stu-id="f09ec-153">110110</span></span>         | <span data-ttu-id="f09ec-154">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-154">EUR</span></span>      | <span data-ttu-id="f09ec-155">250</span><span class="sxs-lookup"><span data-stu-id="f09ec-155">250</span></span>    | <span data-ttu-id="f09ec-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f09ec-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="f09ec-157">130100</span><span class="sxs-lookup"><span data-stu-id="f09ec-157">130100</span></span>         | <span data-ttu-id="f09ec-158">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-158">EUR</span></span>      | <span data-ttu-id="f09ec-159">–250</span><span class="sxs-lookup"><span data-stu-id="f09ec-159">-250</span></span>   | <span data-ttu-id="f09ec-160">–500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f09ec-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f09ec-161">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. lapkričio 30 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="f09ec-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f09ec-162">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="f09ec-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="f09ec-163">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="f09ec-163">Ledger account</span></span> | <span data-ttu-id="f09ec-164">Valiuta</span><span class="sxs-lookup"><span data-stu-id="f09ec-164">Currency</span></span> | <span data-ttu-id="f09ec-165">Suma</span><span class="sxs-lookup"><span data-stu-id="f09ec-165">Amount</span></span>  | <span data-ttu-id="f09ec-166">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="f09ec-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f09ec-167">110110</span><span class="sxs-lookup"><span data-stu-id="f09ec-167">110110</span></span>         | <span data-ttu-id="f09ec-168">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-168">EUR</span></span>      | <span data-ttu-id="f09ec-169">333.33</span><span class="sxs-lookup"><span data-stu-id="f09ec-169">333.33</span></span>  | <span data-ttu-id="f09ec-170">Pradinė suma 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f09ec-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f09ec-171">130100</span><span class="sxs-lookup"><span data-stu-id="f09ec-171">130100</span></span>         | <span data-ttu-id="f09ec-172">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-172">EUR</span></span>      | <span data-ttu-id="f09ec-173">–333,33</span><span class="sxs-lookup"><span data-stu-id="f09ec-173">-333.33</span></span> | <span data-ttu-id="f09ec-174">Pradinė suma –500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f09ec-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f09ec-175">801400</span><span class="sxs-lookup"><span data-stu-id="f09ec-175">801400</span></span>         | <span data-ttu-id="f09ec-176">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-176">EUR</span></span>      | <span data-ttu-id="f09ec-177">83.33</span><span class="sxs-lookup"><span data-stu-id="f09ec-177">83.33</span></span>   | <span data-ttu-id="f09ec-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="f09ec-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="f09ec-179">801600</span><span class="sxs-lookup"><span data-stu-id="f09ec-179">801600</span></span>         | <span data-ttu-id="f09ec-180">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-180">EUR</span></span>      | <span data-ttu-id="f09ec-181">–83,33</span><span class="sxs-lookup"><span data-stu-id="f09ec-181">-83.33</span></span>  | <span data-ttu-id="f09ec-182">-333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="f09ec-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f09ec-183">Matysite papildomas ataskaitų valiutos sumų operacijas.</span><span class="sxs-lookup"><span data-stu-id="f09ec-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f09ec-184">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. gruodžio 31 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="f09ec-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f09ec-185">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="f09ec-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="f09ec-186">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="f09ec-186">Ledger account</span></span> | <span data-ttu-id="f09ec-187">Valiuta</span><span class="sxs-lookup"><span data-stu-id="f09ec-187">Currency</span></span> | <span data-ttu-id="f09ec-188">Suma</span><span class="sxs-lookup"><span data-stu-id="f09ec-188">Amount</span></span>  | <span data-ttu-id="f09ec-189">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="f09ec-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f09ec-190">110110</span><span class="sxs-lookup"><span data-stu-id="f09ec-190">110110</span></span>         | <span data-ttu-id="f09ec-191">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-191">EUR</span></span>      | <span data-ttu-id="f09ec-192">500,00</span><span class="sxs-lookup"><span data-stu-id="f09ec-192">500.00</span></span>  | <span data-ttu-id="f09ec-193">Pradinė suma 500 × 1</span><span class="sxs-lookup"><span data-stu-id="f09ec-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f09ec-194">130100</span><span class="sxs-lookup"><span data-stu-id="f09ec-194">130100</span></span>         | <span data-ttu-id="f09ec-195">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-195">EUR</span></span>      | <span data-ttu-id="f09ec-196">–500,00</span><span class="sxs-lookup"><span data-stu-id="f09ec-196">-500.00</span></span> | <span data-ttu-id="f09ec-197">Pradinė suma –500 × 1</span><span class="sxs-lookup"><span data-stu-id="f09ec-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f09ec-198">801400</span><span class="sxs-lookup"><span data-stu-id="f09ec-198">801400</span></span>         | <span data-ttu-id="f09ec-199">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-199">EUR</span></span>      | <span data-ttu-id="f09ec-200">250</span><span class="sxs-lookup"><span data-stu-id="f09ec-200">250</span></span>     | <span data-ttu-id="f09ec-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="f09ec-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f09ec-202">801600</span><span class="sxs-lookup"><span data-stu-id="f09ec-202">801600</span></span>         | <span data-ttu-id="f09ec-203">EUR</span><span class="sxs-lookup"><span data-stu-id="f09ec-203">EUR</span></span>      | <span data-ttu-id="f09ec-204">–250</span><span class="sxs-lookup"><span data-stu-id="f09ec-204">-250</span></span>    | <span data-ttu-id="f09ec-205">-500 – (–333,33) = –166,67 – 166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="f09ec-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]