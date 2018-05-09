---
title: "PVM mokėjimo ir apvalinimo taisyklės"
description: "Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6b910a1e9ea6fe5f0f9e24677175cd88948cec26
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="1848d-103">PVM mokėjimo ir apvalinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="1848d-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1848d-104">Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="1848d-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="1848d-105">Periodiškai reikia pranešti apie PVM ir sumokėti jį mokesčių institucijoms.</span><span class="sxs-lookup"><span data-stu-id="1848d-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="1848d-106">Tai galite padaryti atlikdami sudengimą ir registruodami PVM procesą puslapyje PVM.</span><span class="sxs-lookup"><span data-stu-id="1848d-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="1848d-107">Laikotarpio PVM bus sudengtas pagal PVM sąskaitas ir PVM balansas bus registruojamas PVM sudengimo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="1848d-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="1848d-108">PVM balansą, registruojamą PVM sudengimo sąskaitoje, galima apvalinti pagal mokesčių institucijos reikalavimus, nustačius apvalinimo taisyklę puslapyje PVM.</span><span class="sxs-lookup"><span data-stu-id="1848d-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="1848d-109">Apvalinimo skirtumas užregistruojamas PVM apvalinimo sąskaitoje, pasirinktoje dalies Didžioji knyga lauke Automatinių operacijų sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="1848d-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="1848d-110">Tolesniame pavyzdyje pavaizduota, kaip veikia apvalinimo taisyklė PVM institucijai.</span><span class="sxs-lookup"><span data-stu-id="1848d-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="1848d-111">Pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="1848d-111">Example:</span></span>

<span data-ttu-id="1848d-112">Rodoma, kad bendrojo laikotarpio PVM kredito balansas yra –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="1848d-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="1848d-113">Juridinis subjektas surinko daugiau PVM, nei sumokėjo.</span><span class="sxs-lookup"><span data-stu-id="1848d-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="1848d-114">Taigi juridinis subjektas skolingas mokesčių institucijai.</span><span class="sxs-lookup"><span data-stu-id="1848d-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="1848d-115">Juridinis subjektas nori naudoti apvalinimo metodą, kuris apvalina likutį iki artimiausio 1,00.</span><span class="sxs-lookup"><span data-stu-id="1848d-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="1848d-116">Naudotojas, atsakingas už PVM apskaitą, atlieka toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1848d-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="1848d-117">Spustelėkite Mokestis &gt; Netiesioginiai mokesčiai &gt; PVM &gt; PVM rinkėjai</span><span class="sxs-lookup"><span data-stu-id="1848d-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="1848d-118">„FastTab“ skirtuke Bendra esančiame lauke Apvalinimo forma pasirinkite parinktį Įprastas.</span><span class="sxs-lookup"><span data-stu-id="1848d-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="1848d-119">Lauke Apvalinimas įveskite 1,00.</span><span class="sxs-lookup"><span data-stu-id="1848d-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="1848d-120">Kai ateina laikas mokėti PVM mokesčių inspekcijai, atidarykite puslapį Sudengti ir užregistruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="1848d-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="1848d-121">(Spustelėkite Mokestis &gt; Deklaracijos &gt; PVM &gt; Sudengti ir užregistruoti PVM.)</span><span class="sxs-lookup"><span data-stu-id="1848d-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="1848d-122">PVM sudengimo sąskaitoje mokesčių skolos suma 98 765,43 suapvalinama iki 98 765.</span><span class="sxs-lookup"><span data-stu-id="1848d-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="1848d-123">Toliau pateikiamoje lentelėje parodoma, kaip 98 765,43 suma suapvalinama taikant kiekvieną apvalinimo metodą, galimą puslapio PVM rinkėjai lauke Apvalinimo forma.</span><span class="sxs-lookup"><span data-stu-id="1848d-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="1848d-124">Apvalinimo formos parinktis</span><span class="sxs-lookup"><span data-stu-id="1848d-124">Rounding form option</span></span>                | <span data-ttu-id="1848d-125">Apvalinimo vertė = 0,01</span><span class="sxs-lookup"><span data-stu-id="1848d-125">Round-off value = 0.01</span></span> | <span data-ttu-id="1848d-126">Apvalinimo vertė = 0,10</span><span class="sxs-lookup"><span data-stu-id="1848d-126">Round-off value = 0.10</span></span> | <span data-ttu-id="1848d-127">Apvalinimo vertė = 1,00</span><span class="sxs-lookup"><span data-stu-id="1848d-127">Round-off value = 1.00</span></span> | <span data-ttu-id="1848d-128">Apvalinimo vertė = 100,00</span><span class="sxs-lookup"><span data-stu-id="1848d-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="1848d-129">Įprastas</span><span class="sxs-lookup"><span data-stu-id="1848d-129">Normal</span></span>                              | <span data-ttu-id="1848d-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="1848d-130">98,765.43</span></span>              | <span data-ttu-id="1848d-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="1848d-131">98,765.40</span></span>              | <span data-ttu-id="1848d-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="1848d-132">98,765.00</span></span>              | <span data-ttu-id="1848d-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="1848d-133">98,800.00</span></span>                |
| <span data-ttu-id="1848d-134">Žemyn</span><span class="sxs-lookup"><span data-stu-id="1848d-134">Downward</span></span>                            | <span data-ttu-id="1848d-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="1848d-135">98,765.43</span></span>              | <span data-ttu-id="1848d-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="1848d-136">98,765.40</span></span>              | <span data-ttu-id="1848d-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="1848d-137">98,765.00</span></span>              | <span data-ttu-id="1848d-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="1848d-138">98,700.00</span></span>                |
| <span data-ttu-id="1848d-139">Į didesnę pusę</span><span class="sxs-lookup"><span data-stu-id="1848d-139">Rounding-up</span></span>                         | <span data-ttu-id="1848d-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="1848d-140">98,765.43</span></span>              | <span data-ttu-id="1848d-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="1848d-141">98,765.50</span></span>              | <span data-ttu-id="1848d-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="1848d-142">98,766.00</span></span>              | <span data-ttu-id="1848d-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="1848d-143">98,800.00</span></span>                |
| <span data-ttu-id="1848d-144">Pranašumas, kredito balansas</span><span class="sxs-lookup"><span data-stu-id="1848d-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="1848d-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="1848d-145">98,765.43</span></span>              | <span data-ttu-id="1848d-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="1848d-146">98,765.40</span></span>              | <span data-ttu-id="1848d-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="1848d-147">98,765.00</span></span>              | <span data-ttu-id="1848d-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="1848d-148">98,700.00</span></span>                |
| <span data-ttu-id="1848d-149">Pranašumas, debeto balansas</span><span class="sxs-lookup"><span data-stu-id="1848d-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="1848d-150">98 765,43</span><span class="sxs-lookup"><span data-stu-id="1848d-150">98,765.43</span></span>              | <span data-ttu-id="1848d-151">98 765,50</span><span class="sxs-lookup"><span data-stu-id="1848d-151">98,765.50</span></span>              | <span data-ttu-id="1848d-152">98 766,00</span><span class="sxs-lookup"><span data-stu-id="1848d-152">98,766.00</span></span>              | <span data-ttu-id="1848d-153">98 800,00</span><span class="sxs-lookup"><span data-stu-id="1848d-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="1848d-154">Jei pasirinksite Pranašumas, visada bus apvalinama juridinio subjekto naudai.</span><span class="sxs-lookup"><span data-stu-id="1848d-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="1848d-155">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="1848d-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="1848d-156">PVM apžvalga</span><span class="sxs-lookup"><span data-stu-id="1848d-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="1848d-157">Kurti PVM mokėjimą</span><span class="sxs-lookup"><span data-stu-id="1848d-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="1848d-158">Kurti pardavimo operacijas dokumentuose</span><span class="sxs-lookup"><span data-stu-id="1848d-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="1848d-159">Peržiūrėti užregistruotas PVM operacijas</span><span class="sxs-lookup"><span data-stu-id="1848d-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



