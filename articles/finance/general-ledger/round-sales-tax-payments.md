---
title: PVM mokėjimo ir apvalinimo taisyklės
description: Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
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
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186330"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="4d7d5-103">PVM mokėjimo ir apvalinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="4d7d5-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d7d5-104">Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="4d7d5-105">Periodiškai reikia pranešti apie PVM ir sumokėti jį mokesčių institucijoms.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="4d7d5-106">Tai galite padaryti atlikdami sudengimą ir registruodami PVM procesą puslapyje PVM.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="4d7d5-107">Laikotarpio PVM bus sudengtas pagal PVM sąskaitas ir PVM balansas bus registruojamas PVM sudengimo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="4d7d5-108">PVM balansą, registruojamą PVM sudengimo sąskaitoje, galima apvalinti pagal mokesčių institucijos reikalavimus, nustačius apvalinimo taisyklę puslapyje PVM.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="4d7d5-109">Apvalinimo skirtumas užregistruojamas PVM apvalinimo sąskaitoje, pasirinktoje dalies Didžioji knyga lauke Automatinių operacijų sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="4d7d5-110">Tolesniame pavyzdyje pavaizduota, kaip veikia apvalinimo taisyklė PVM institucijai.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="4d7d5-111">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="4d7d5-111">Examples</span></span>

<span data-ttu-id="4d7d5-112">Rodoma, kad bendrojo laikotarpio PVM kredito balansas yra –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="4d7d5-113">Juridinis subjektas surinko daugiau PVM, nei sumokėjo.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="4d7d5-114">Taigi juridinis subjektas skolingas mokesčių institucijai.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="4d7d5-115">Juridinis subjektas nori naudoti apvalinimo metodą, kuris apvalina likutį iki artimiausio 1,00.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="4d7d5-116">Naudotojas, atsakingas už PVM apskaitą, atlieka toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="4d7d5-117">Spustelėkite Mokestis &gt; Netiesioginiai mokesčiai &gt; PVM &gt; PVM rinkėjai</span><span class="sxs-lookup"><span data-stu-id="4d7d5-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="4d7d5-118">„FastTab“ skirtuke Bendra esančiame lauke Apvalinimo forma pasirinkite parinktį Įprastas.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="4d7d5-119">Lauke Apvalinimas įveskite 1,00.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="4d7d5-120">Kai ateina laikas mokėti PVM mokesčių inspekcijai, atidarykite puslapį Sudengti ir užregistruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="4d7d5-121">(Spustelėkite Mokestis &gt; Deklaracijos &gt; PVM &gt; Sudengti ir užregistruoti PVM.)</span><span class="sxs-lookup"><span data-stu-id="4d7d5-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="4d7d5-122">PVM sudengimo sąskaitoje mokesčių skolos suma 98 765,43 suapvalinama iki 98 765.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="4d7d5-123">Toliau pateikiamoje lentelėje parodoma, kaip 98 765,43 suma suapvalinama taikant kiekvieną apvalinimo metodą, galimą puslapio PVM rinkėjai lauke Apvalinimo forma.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="4d7d5-124">Apvalinimo formos parinktis</span><span class="sxs-lookup"><span data-stu-id="4d7d5-124">Rounding form option</span></span>                | <span data-ttu-id="4d7d5-125">Apvalinimo vertė = 0,01</span><span class="sxs-lookup"><span data-stu-id="4d7d5-125">Round-off value = 0.01</span></span> | <span data-ttu-id="4d7d5-126">Apvalinimo vertė = 0,10</span><span class="sxs-lookup"><span data-stu-id="4d7d5-126">Round-off value = 0.10</span></span> | <span data-ttu-id="4d7d5-127">Apvalinimo vertė = 1,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-127">Round-off value = 1.00</span></span> | <span data-ttu-id="4d7d5-128">Apvalinimo vertė = 100,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="4d7d5-129">Įprastas</span><span class="sxs-lookup"><span data-stu-id="4d7d5-129">Normal</span></span>                              | <span data-ttu-id="4d7d5-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="4d7d5-130">98,765.43</span></span>              | <span data-ttu-id="4d7d5-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="4d7d5-131">98,765.40</span></span>              | <span data-ttu-id="4d7d5-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-132">98,765.00</span></span>              | <span data-ttu-id="4d7d5-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-133">98,800.00</span></span>                |
| <span data-ttu-id="4d7d5-134">Žemyn</span><span class="sxs-lookup"><span data-stu-id="4d7d5-134">Downward</span></span>                            | <span data-ttu-id="4d7d5-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="4d7d5-135">98,765.43</span></span>              | <span data-ttu-id="4d7d5-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="4d7d5-136">98,765.40</span></span>              | <span data-ttu-id="4d7d5-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-137">98,765.00</span></span>              | <span data-ttu-id="4d7d5-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-138">98,700.00</span></span>                |
| <span data-ttu-id="4d7d5-139">Į didesnę pusę</span><span class="sxs-lookup"><span data-stu-id="4d7d5-139">Rounding-up</span></span>                         | <span data-ttu-id="4d7d5-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="4d7d5-140">98,765.43</span></span>              | <span data-ttu-id="4d7d5-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="4d7d5-141">98,765.50</span></span>              | <span data-ttu-id="4d7d5-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-142">98,766.00</span></span>              | <span data-ttu-id="4d7d5-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-143">98,800.00</span></span>                |
| <span data-ttu-id="4d7d5-144">Pranašumas, kredito balansas</span><span class="sxs-lookup"><span data-stu-id="4d7d5-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="4d7d5-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="4d7d5-145">98,765.43</span></span>              | <span data-ttu-id="4d7d5-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="4d7d5-146">98,765.40</span></span>              | <span data-ttu-id="4d7d5-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-147">98,765.00</span></span>              | <span data-ttu-id="4d7d5-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-148">98,700.00</span></span>                |
| <span data-ttu-id="4d7d5-149">Pranašumas, debeto balansas</span><span class="sxs-lookup"><span data-stu-id="4d7d5-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="4d7d5-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4d7d5-150">98,765.43</span></span>              | <span data-ttu-id="4d7d5-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="4d7d5-151">98,765.50</span></span>              | <span data-ttu-id="4d7d5-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-152">98,766.00</span></span>              | <span data-ttu-id="4d7d5-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="4d7d5-154">Apvalinimo nėra, nes apvalinimas yra 0,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="4d7d5-155">apvalinimas (1,0151; 0,00) = 1,0151 apvalinimas (1,0149; 0,00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="4d7d5-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="4d7d5-156">Įprastas apvalinimas, o apvalinimo tikslumas yra 0,01</span><span class="sxs-lookup"><span data-stu-id="4d7d5-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="4d7d5-157">Apvalinimas</span><span class="sxs-lookup"><span data-stu-id="4d7d5-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="4d7d5-158">Skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="4d7d5-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4d7d5-159">apvalinimas (1,015; 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="4d7d5-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="4d7d5-160">apvalinimas (1,015 / 0,01; 0) = apvalinimas (101,5; 0) = 102</span><span class="sxs-lookup"><span data-stu-id="4d7d5-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="4d7d5-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="4d7d5-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4d7d5-162">apvalinimas (1,014; 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="4d7d5-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="4d7d5-163">apvalinimas (1,014 / 0,01; 0) = apvalinimas (101,4; 0) = 101</span><span class="sxs-lookup"><span data-stu-id="4d7d5-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="4d7d5-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="4d7d5-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4d7d5-165">apvalinimas (1,011; 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="4d7d5-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="4d7d5-166">apvalinimas (1,011 / 0,02; 0) = apvalinimas (50,55; 0) = 51</span><span class="sxs-lookup"><span data-stu-id="4d7d5-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="4d7d5-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="4d7d5-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4d7d5-168">apvalinimas (1,009; 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="4d7d5-169">apvalinimas (1,009 / 0,02; 0) = apvalinimas (50,45; 0) = 50</span><span class="sxs-lookup"><span data-stu-id="4d7d5-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="4d7d5-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="4d7d5-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="4d7d5-171">Jei pasirinksite Pranašumas, visada bus apvalinama juridinio subjekto naudai.</span><span class="sxs-lookup"><span data-stu-id="4d7d5-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="4d7d5-172">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="4d7d5-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="4d7d5-173">PVM apžvalga</span><span class="sxs-lookup"><span data-stu-id="4d7d5-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="4d7d5-174">Kurti PVM mokėjimą</span><span class="sxs-lookup"><span data-stu-id="4d7d5-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="4d7d5-175">Kurti pardavimo operacijas dokumentuose</span><span class="sxs-lookup"><span data-stu-id="4d7d5-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="4d7d5-176">Registruotų PVM operacijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="4d7d5-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="4d7d5-177">apvalinimo funkcija</span><span class="sxs-lookup"><span data-stu-id="4d7d5-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


