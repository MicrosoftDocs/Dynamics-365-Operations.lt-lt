---
title: PVM mokėjimo ir apvalinimo taisyklės
description: Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adc48d1841903670577684b1c3d773d323c19ea1
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275679"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="e01eb-103">PVM mokėjimo ir apvalinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="e01eb-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e01eb-104">Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="e01eb-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="e01eb-105">Periodiškai reikia pranešti apie PVM ir sumokėti jį mokesčių institucijoms.</span><span class="sxs-lookup"><span data-stu-id="e01eb-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="e01eb-106">Tai galite padaryti atlikdami sudengimą ir registruodami PVM procesą puslapyje PVM.</span><span class="sxs-lookup"><span data-stu-id="e01eb-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="e01eb-107">Laikotarpio PVM bus sudengtas pagal PVM sąskaitas ir PVM balansas bus registruojamas PVM sudengimo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="e01eb-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="e01eb-108">PVM balansą, registruojamą PVM sudengimo sąskaitoje, galima apvalinti pagal mokesčių institucijos reikalavimus, nustačius apvalinimo taisyklę puslapyje PVM.</span><span class="sxs-lookup"><span data-stu-id="e01eb-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="e01eb-109">Apvalinimo skirtumas užregistruojamas PVM apvalinimo sąskaitoje, pasirinktoje dalies Didžioji knyga lauke Automatinių operacijų sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="e01eb-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="e01eb-110">Tolesniame pavyzdyje pavaizduota, kaip veikia apvalinimo taisyklė PVM institucijai.</span><span class="sxs-lookup"><span data-stu-id="e01eb-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="e01eb-111">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="e01eb-111">Examples</span></span>

<span data-ttu-id="e01eb-112">Rodoma, kad bendrojo laikotarpio PVM kredito balansas yra –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="e01eb-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="e01eb-113">Juridinis subjektas surinko daugiau PVM, nei sumokėjo.</span><span class="sxs-lookup"><span data-stu-id="e01eb-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="e01eb-114">Taigi juridinis subjektas skolingas mokesčių institucijai.</span><span class="sxs-lookup"><span data-stu-id="e01eb-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="e01eb-115">Juridinis subjektas nori naudoti apvalinimo metodą, kuris apvalina likutį iki artimiausio 1,00.</span><span class="sxs-lookup"><span data-stu-id="e01eb-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="e01eb-116">Naudotojas, atsakingas už PVM apskaitą, atlieka toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e01eb-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="e01eb-117">Spustelėkite **Mokestis** > **Netiesioginiai mokesčiai** > **PVM** > **PVM institucijos**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="e01eb-118">„FastTab“ konteineryje **Bendra** esančiame lauke **Apvalinimo forma** pasirinkite **Įprasta**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="e01eb-119">Lauke **Apvalinimas** įveskite 1,00.</span><span class="sxs-lookup"><span data-stu-id="e01eb-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="e01eb-120">Kai ateina laikas mokėti PVM mokesčių inspekcijai, eikite į **Mokestis** > **Deklaracijos** > **PVM** > **Sudengti ir užregistruoti PVM**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="e01eb-121">PVM sudengimo sąskaitoje galite matyti, kad mokesčių skolos suma **98 765,43** suapvalinama iki **98 765**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="e01eb-122">Toliau pateikiamoje lentelėje parodoma, kaip 98 765,43 suma suapvalinama taikant kiekvieną apvalinimo metodą, galimą puslapio **PVM rinkėjai** lauke **Apvalinimo forma**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="e01eb-123">Jei apvalinimo reikšmė nustatyta kaip 0,00, tada:</span><span class="sxs-lookup"><span data-stu-id="e01eb-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="e01eb-124">Apvalinant įprastai, apvalinimo veiksmas yra toks pats, kaip **Apvalinimas = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="e01eb-125">Naudojant **Apvalinimo formos parinktys**, **Mažinant**, **Apvalinimas** ir **Pranašumas**, veiksmas yra toks pats kaip **Apvalinimas = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="e01eb-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="e01eb-126">Apvalinimo formos parinktis</span><span class="sxs-lookup"><span data-stu-id="e01eb-126">Rounding form option</span></span>                | <span data-ttu-id="e01eb-127">Apvalinimo vertė = 0,01</span><span class="sxs-lookup"><span data-stu-id="e01eb-127">Round-off value = 0.01</span></span> | <span data-ttu-id="e01eb-128">Apvalinimo vertė = 0,10</span><span class="sxs-lookup"><span data-stu-id="e01eb-128">Round-off value = 0.10</span></span> | <span data-ttu-id="e01eb-129">Apvalinimo vertė = 1,00</span><span class="sxs-lookup"><span data-stu-id="e01eb-129">Round-off value = 1.00</span></span> | <span data-ttu-id="e01eb-130">Apvalinimo vertė = 100,00</span><span class="sxs-lookup"><span data-stu-id="e01eb-130">Round-off value = 100.00</span></span> | <span data-ttu-id="e01eb-131">Apvalinimo vertė = 0,00</span><span class="sxs-lookup"><span data-stu-id="e01eb-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="e01eb-132">Įprasta</span><span class="sxs-lookup"><span data-stu-id="e01eb-132">Normal</span></span>                              | <span data-ttu-id="e01eb-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e01eb-133">98,765.43</span></span>              | <span data-ttu-id="e01eb-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="e01eb-134">98,765.40</span></span>              | <span data-ttu-id="e01eb-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-135">98,765.00</span></span>              | <span data-ttu-id="e01eb-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-136">98,800.00</span></span>                | <span data-ttu-id="e01eb-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e01eb-137">98,765.43</span></span>                |
| <span data-ttu-id="e01eb-138">Žemyn</span><span class="sxs-lookup"><span data-stu-id="e01eb-138">Downward</span></span>                            | <span data-ttu-id="e01eb-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e01eb-139">98,765.43</span></span>              | <span data-ttu-id="e01eb-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="e01eb-140">98,765.40</span></span>              | <span data-ttu-id="e01eb-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-141">98,765.00</span></span>              | <span data-ttu-id="e01eb-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-142">98,700.00</span></span>                | <span data-ttu-id="e01eb-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-143">98,765.00</span></span>                |
| <span data-ttu-id="e01eb-144">Apvalinimas į didesnę pusę</span><span class="sxs-lookup"><span data-stu-id="e01eb-144">Rounding-up</span></span>                         | <span data-ttu-id="e01eb-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e01eb-145">98,765.43</span></span>              | <span data-ttu-id="e01eb-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="e01eb-146">98,765.50</span></span>              | <span data-ttu-id="e01eb-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-147">98,766.00</span></span>              | <span data-ttu-id="e01eb-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-148">98,800.00</span></span>                | <span data-ttu-id="e01eb-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-149">98,766.00</span></span>                |
| <span data-ttu-id="e01eb-150">Pranašumas, kredito balansas</span><span class="sxs-lookup"><span data-stu-id="e01eb-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="e01eb-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e01eb-151">98,765.43</span></span>              | <span data-ttu-id="e01eb-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="e01eb-152">98,765.40</span></span>              | <span data-ttu-id="e01eb-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-153">98,765.00</span></span>              | <span data-ttu-id="e01eb-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-154">98,700.00</span></span>                | <span data-ttu-id="e01eb-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-155">98,765.00</span></span>                |
| <span data-ttu-id="e01eb-156">Pranašumas, debeto balansas</span><span class="sxs-lookup"><span data-stu-id="e01eb-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="e01eb-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e01eb-157">98,765.43</span></span>              | <span data-ttu-id="e01eb-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="e01eb-158">98,765.50</span></span>              | <span data-ttu-id="e01eb-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-159">98,766.00</span></span>              | <span data-ttu-id="e01eb-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-160">98,800.00</span></span>                | <span data-ttu-id="e01eb-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="e01eb-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="e01eb-162">Įprastas apvalinimas, o apvalinimo tikslumas yra 0,01</span><span class="sxs-lookup"><span data-stu-id="e01eb-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="e01eb-163">Apvalinimas</span><span class="sxs-lookup"><span data-stu-id="e01eb-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="e01eb-164">Skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="e01eb-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e01eb-165">apvalinimas (1,015; 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="e01eb-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="e01eb-166">apvalinimas (1,015 / 0,01; 0) = apvalinimas (101,5; 0) = 102</span><span class="sxs-lookup"><span data-stu-id="e01eb-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="e01eb-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="e01eb-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e01eb-168">apvalinimas (1,014; 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="e01eb-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="e01eb-169">apvalinimas (1,014 / 0,01; 0) = apvalinimas (101,4; 0) = 101</span><span class="sxs-lookup"><span data-stu-id="e01eb-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="e01eb-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="e01eb-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e01eb-171">apvalinimas (1,011; 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="e01eb-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="e01eb-172">apvalinimas (1,011 / 0,02; 0) = apvalinimas (50,55; 0) = 51</span><span class="sxs-lookup"><span data-stu-id="e01eb-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="e01eb-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="e01eb-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e01eb-174">apvalinimas (1,009; 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="e01eb-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="e01eb-175">apvalinimas (1,009 / 0,02; 0) = apvalinimas (50,45; 0) = 50</span><span class="sxs-lookup"><span data-stu-id="e01eb-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="e01eb-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="e01eb-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="e01eb-177">Jei pasirinksite Pranašumas, visada bus apvalinama juridinio subjekto naudai.</span><span class="sxs-lookup"><span data-stu-id="e01eb-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="e01eb-178">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="e01eb-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="e01eb-179">PVM apžvalga</span><span class="sxs-lookup"><span data-stu-id="e01eb-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="e01eb-180">PVM mokėjimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="e01eb-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="e01eb-181">PVM operacijų kūrimas dokumentuose</span><span class="sxs-lookup"><span data-stu-id="e01eb-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="e01eb-182">Registruotų PVM operacijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="e01eb-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="e01eb-183">apvalinimo funkcija</span><span class="sxs-lookup"><span data-stu-id="e01eb-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


