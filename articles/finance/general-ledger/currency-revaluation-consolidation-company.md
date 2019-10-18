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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178995"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="47f58-103">Valiutos kurso pasikeitimas konsoliduotoje įmonėje</span><span class="sxs-lookup"><span data-stu-id="47f58-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47f58-104">Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti.</span><span class="sxs-lookup"><span data-stu-id="47f58-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="47f58-105">Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="47f58-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="47f58-106">Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus.</span><span class="sxs-lookup"><span data-stu-id="47f58-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="47f58-107">Negautas pelnas arba nuostoliai tada atitinkamai atnaujinami atsižvelgiant į naują valiutos kursą ir datą.</span><span class="sxs-lookup"><span data-stu-id="47f58-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="47f58-108">Šiame pavyzdyje parodyti apskaitos įrašai, sukurti vykdant procesą.</span><span class="sxs-lookup"><span data-stu-id="47f58-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="47f58-109">Įmonės sąranka</span><span class="sxs-lookup"><span data-stu-id="47f58-109">Company setup</span></span>
-   <span data-ttu-id="47f58-110">**Šaltinio / veikianti įmonė (USMF)** – JAV doleriai (USD) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="47f58-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="47f58-111">**Konsoliduota įmonės (CON)** – eurai (EUR) naudojami kaip apskaitos ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="47f58-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="47f58-112">**Gautas pelnas** – DK sąskaita 801500</span><span class="sxs-lookup"><span data-stu-id="47f58-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="47f58-113">**Patirtas nuostolis** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="47f58-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="47f58-114">**Negautas pelnas** – DK sąskaita 801600</span><span class="sxs-lookup"><span data-stu-id="47f58-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="47f58-115">**Nepatirtas nuostolis** – DK sąskaita 801400</span><span class="sxs-lookup"><span data-stu-id="47f58-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="47f58-116">Pradinės operacijos</span><span class="sxs-lookup"><span data-stu-id="47f58-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="47f58-117">Grynųjų pinigų gavimo operacijos USMF</span><span class="sxs-lookup"><span data-stu-id="47f58-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="47f58-118">Data</span><span class="sxs-lookup"><span data-stu-id="47f58-118">Date</span></span>       | <span data-ttu-id="47f58-119">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="47f58-119">Ledger account</span></span>               | <span data-ttu-id="47f58-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="47f58-120">Currency</span></span> | <span data-ttu-id="47f58-121">Suma</span><span class="sxs-lookup"><span data-stu-id="47f58-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="47f58-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="47f58-122">10/11/2015</span></span> | <span data-ttu-id="47f58-123">110110 – grynieji</span><span class="sxs-lookup"><span data-stu-id="47f58-123">110110 – Cash</span></span>                | <span data-ttu-id="47f58-124">USD</span><span class="sxs-lookup"><span data-stu-id="47f58-124">USD</span></span>      | <span data-ttu-id="47f58-125">500</span><span class="sxs-lookup"><span data-stu-id="47f58-125">500</span></span>    |
| <span data-ttu-id="47f58-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="47f58-126">10/11/2015</span></span> | <span data-ttu-id="47f58-127">130100 – gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="47f58-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="47f58-128">USD</span><span class="sxs-lookup"><span data-stu-id="47f58-128">USD</span></span>      | <span data-ttu-id="47f58-129">–500</span><span class="sxs-lookup"><span data-stu-id="47f58-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="47f58-130">Valiutos kursai</span><span class="sxs-lookup"><span data-stu-id="47f58-130">Exchange rates</span></span>

| <span data-ttu-id="47f58-131">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="47f58-131">From currency</span></span> | <span data-ttu-id="47f58-132">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="47f58-132">To currency</span></span> | <span data-ttu-id="47f58-133">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="47f58-133">Start date</span></span> | <span data-ttu-id="47f58-134">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="47f58-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="47f58-135">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-135">EUR</span></span>           | <span data-ttu-id="47f58-136">USD</span><span class="sxs-lookup"><span data-stu-id="47f58-136">USD</span></span>         | <span data-ttu-id="47f58-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="47f58-137">10/1/2015</span></span>  | <span data-ttu-id="47f58-138">200</span><span class="sxs-lookup"><span data-stu-id="47f58-138">200</span></span>           |
| <span data-ttu-id="47f58-139">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-139">EUR</span></span>           | <span data-ttu-id="47f58-140">USD</span><span class="sxs-lookup"><span data-stu-id="47f58-140">USD</span></span>         | <span data-ttu-id="47f58-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="47f58-141">11/1/2015</span></span>  | <span data-ttu-id="47f58-142">150</span><span class="sxs-lookup"><span data-stu-id="47f58-142">150</span></span>           |
| <span data-ttu-id="47f58-143">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-143">EUR</span></span>           | <span data-ttu-id="47f58-144">USD</span><span class="sxs-lookup"><span data-stu-id="47f58-144">USD</span></span>         | <span data-ttu-id="47f58-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="47f58-145">12/1/2012</span></span>  | <span data-ttu-id="47f58-146">100</span><span class="sxs-lookup"><span data-stu-id="47f58-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="47f58-147">2015 m. spalio konsolidavimas</span><span class="sxs-lookup"><span data-stu-id="47f58-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="47f58-148">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="47f58-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="47f58-149">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="47f58-149">Ledger account</span></span> | <span data-ttu-id="47f58-150">Valiuta</span><span class="sxs-lookup"><span data-stu-id="47f58-150">Currency</span></span> | <span data-ttu-id="47f58-151">Suma</span><span class="sxs-lookup"><span data-stu-id="47f58-151">Amount</span></span> | <span data-ttu-id="47f58-152">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="47f58-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="47f58-153">110110</span><span class="sxs-lookup"><span data-stu-id="47f58-153">110110</span></span>         | <span data-ttu-id="47f58-154">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-154">EUR</span></span>      | <span data-ttu-id="47f58-155">250</span><span class="sxs-lookup"><span data-stu-id="47f58-155">250</span></span>    | <span data-ttu-id="47f58-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="47f58-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="47f58-157">130100</span><span class="sxs-lookup"><span data-stu-id="47f58-157">130100</span></span>         | <span data-ttu-id="47f58-158">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-158">EUR</span></span>      | <span data-ttu-id="47f58-159">–250</span><span class="sxs-lookup"><span data-stu-id="47f58-159">-250</span></span>   | <span data-ttu-id="47f58-160">–500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="47f58-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="47f58-161">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. lapkričio 30 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="47f58-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="47f58-162">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="47f58-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="47f58-163">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="47f58-163">Ledger account</span></span> | <span data-ttu-id="47f58-164">Valiuta</span><span class="sxs-lookup"><span data-stu-id="47f58-164">Currency</span></span> | <span data-ttu-id="47f58-165">Suma</span><span class="sxs-lookup"><span data-stu-id="47f58-165">Amount</span></span>  | <span data-ttu-id="47f58-166">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="47f58-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="47f58-167">110110</span><span class="sxs-lookup"><span data-stu-id="47f58-167">110110</span></span>         | <span data-ttu-id="47f58-168">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-168">EUR</span></span>      | <span data-ttu-id="47f58-169">333.33</span><span class="sxs-lookup"><span data-stu-id="47f58-169">333.33</span></span>  | <span data-ttu-id="47f58-170">Pradinė suma 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="47f58-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="47f58-171">130100</span><span class="sxs-lookup"><span data-stu-id="47f58-171">130100</span></span>         | <span data-ttu-id="47f58-172">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-172">EUR</span></span>      | <span data-ttu-id="47f58-173">–333,33</span><span class="sxs-lookup"><span data-stu-id="47f58-173">-333.33</span></span> | <span data-ttu-id="47f58-174">Pradinė suma –500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="47f58-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="47f58-175">801400</span><span class="sxs-lookup"><span data-stu-id="47f58-175">801400</span></span>         | <span data-ttu-id="47f58-176">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-176">EUR</span></span>      | <span data-ttu-id="47f58-177">83.33</span><span class="sxs-lookup"><span data-stu-id="47f58-177">83.33</span></span>   | <span data-ttu-id="47f58-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="47f58-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="47f58-179">801600</span><span class="sxs-lookup"><span data-stu-id="47f58-179">801600</span></span>         | <span data-ttu-id="47f58-180">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-180">EUR</span></span>      | <span data-ttu-id="47f58-181">–83,33</span><span class="sxs-lookup"><span data-stu-id="47f58-181">-83.33</span></span>  | <span data-ttu-id="47f58-182">-333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="47f58-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="47f58-183">Matysite papildomas ataskaitų valiutos sumų operacijas.</span><span class="sxs-lookup"><span data-stu-id="47f58-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="47f58-184">Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. gruodžio 31 d. valiutos kursą</span><span class="sxs-lookup"><span data-stu-id="47f58-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="47f58-185">Konsoliduotos įmonės balansai</span><span class="sxs-lookup"><span data-stu-id="47f58-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="47f58-186">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="47f58-186">Ledger account</span></span> | <span data-ttu-id="47f58-187">Valiuta</span><span class="sxs-lookup"><span data-stu-id="47f58-187">Currency</span></span> | <span data-ttu-id="47f58-188">Suma</span><span class="sxs-lookup"><span data-stu-id="47f58-188">Amount</span></span>  | <span data-ttu-id="47f58-189">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="47f58-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="47f58-190">110110</span><span class="sxs-lookup"><span data-stu-id="47f58-190">110110</span></span>         | <span data-ttu-id="47f58-191">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-191">EUR</span></span>      | <span data-ttu-id="47f58-192">500,00</span><span class="sxs-lookup"><span data-stu-id="47f58-192">500.00</span></span>  | <span data-ttu-id="47f58-193">Pradinė suma 500 × 1</span><span class="sxs-lookup"><span data-stu-id="47f58-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="47f58-194">130100</span><span class="sxs-lookup"><span data-stu-id="47f58-194">130100</span></span>         | <span data-ttu-id="47f58-195">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-195">EUR</span></span>      | <span data-ttu-id="47f58-196">–500,00</span><span class="sxs-lookup"><span data-stu-id="47f58-196">-500.00</span></span> | <span data-ttu-id="47f58-197">Pradinė suma –500 × 1</span><span class="sxs-lookup"><span data-stu-id="47f58-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="47f58-198">801400</span><span class="sxs-lookup"><span data-stu-id="47f58-198">801400</span></span>         | <span data-ttu-id="47f58-199">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-199">EUR</span></span>      | <span data-ttu-id="47f58-200">250</span><span class="sxs-lookup"><span data-stu-id="47f58-200">250</span></span>     | <span data-ttu-id="47f58-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="47f58-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="47f58-202">801600</span><span class="sxs-lookup"><span data-stu-id="47f58-202">801600</span></span>         | <span data-ttu-id="47f58-203">EUR</span><span class="sxs-lookup"><span data-stu-id="47f58-203">EUR</span></span>      | <span data-ttu-id="47f58-204">–250</span><span class="sxs-lookup"><span data-stu-id="47f58-204">-250</span></span>    | <span data-ttu-id="47f58-205">-500 – (–333,33) = –166,67 – 166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="47f58-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





