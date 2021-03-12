---
title: Nuomos registravimo tipai
description: Šioje temoje aprašomi registravimo tipai, naudojami turto nuomos operacijose.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b79b02f7e241783d19a315ccff5bb6874a238c38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995423"
---
# <a name="lease-posting-types"></a><span data-ttu-id="7d8c2-103">Nuomos registravimo tipai</span><span class="sxs-lookup"><span data-stu-id="7d8c2-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d8c2-104">Šioje temoje aprašomi registravimo tipai, naudojami turto nuomos operacijose.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="7d8c2-105">Nuomos turtas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-105">Lease asset</span></span>

<span data-ttu-id="7d8c2-106">Sąskaita yra susieta su naudojimo teise valdomu (ROU) turtu.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="7d8c2-107">Ši sąskaita debetuojama, kai nuoma iš pradžių pripažįstama naujais nuomos apskaitos standartais, Apskaitos standartų kodifikavimu tema Nr. 842 (ASC 842) ir Tarptautinių finansinių ataskaitų standartu Nr. 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="7d8c2-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="7d8c2-108">Jei nuoma modifikuota, ši sąskaita gali būti debetuojama arba kredituojama, atsižvelgiant į tai, ar modifikavimas padidina, ar sumažina nuomos įsipareigojimą.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="7d8c2-109">**Žurnalo įrašų pavyzdys:** pirminis pripažinimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="7d8c2-110">**Debetas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="7d8c2-111">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="7d8c2-112">Nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-112">Lease liability</span></span>

<span data-ttu-id="7d8c2-113">Sąskaita yra susieta su nuomos įsipareigojimu, kuris atsiranda, kai mokėjimai yra diskontuojami naudojant naujus IFRS 16 ir ASC 842 standartus.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="7d8c2-114">Ši sąskaita kredituojama, kai nuoma iš pradžių pripažįstama naujais standartais.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="7d8c2-115">Ji debetuojama vykdant nuomos mokėjimus ir kredituojama kaupiant palūkanas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="7d8c2-116">**Žurnalo įrašų pavyzdys:** pirminis pripažinimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="7d8c2-117">**Debetas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="7d8c2-118">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="7d8c2-119">**Žurnalo įrašų pavyzdys:** palūkanų kaupimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="7d8c2-120">**Debetas:** palūkanų sąnaudos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="7d8c2-121">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="7d8c2-122">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7d8c2-123">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-124">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="7d8c2-125">Trumpalaikis nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-125">Short-term lease liability</span></span>

<span data-ttu-id="7d8c2-126">Sąskaita yra susieta su trumpalaikiu nuomos įsipareigojimu, kai užregistruojamas trumpalaikis nuomos įsipareigojimų perklasifikavimo žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="7d8c2-127">Ši sąskaita kredituojama už trumpalaikį įsipareigojimą iš amortizacijos grafiko paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="7d8c2-128">Tačiau ta pati suma debetuojama kito mėnesio pirmąją dieną.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="7d8c2-129">**Žurnalo įrašų pavyzdys:** trumpalaikis nuomos įsipareigojimų perklasifikavimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="7d8c2-130">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-131">**Kreditas:** trumpalaikis nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-132">**Debetas:** trumpalaikis nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-133">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="7d8c2-134">Likvidavimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="7d8c2-134">Depreciation expense</span></span>

<span data-ttu-id="7d8c2-135">Sąskaita yra susieta su išlaidomis, susijusiomis su naudojimo teise valdomo turto nusidėvėjimu pagal IFRS 16, ASC 842 bei finansine nuoma pagal IAS 17 ir ASC 840.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="7d8c2-136">Ši sąskaita debetuojama, kai naudojimo teise valdomas turtas nusidėvi kiekvieną mėnesį.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="7d8c2-137">**Žurnalo įrašų pavyzdys:** nusidėvėjimo kaupimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="7d8c2-138">**Debetas:** nusidėvėjimo išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="7d8c2-139">**Kreditas:** sukauptas nusidėvėjimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="7d8c2-140">Nuomos modifikavimo pelnas / nuostolis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="7d8c2-141">Sąskaita yra susieta su bet kokiu pelnu ar nuostoliu, atsirandančiu dėl nuomos pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="7d8c2-142">Pelnas gali kilti dėl nuomos modifikacijos, jei modifikavus nuomos įsipareigojimas sumažėja suma, viršijančia naudojimo teise valdomo turto balansinę vertę.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="7d8c2-143">Pavyzdžiui, dabartinė nuomos įsipareigojimo balansinė vertė yra 150 000 USD, o naudojimo teise valdomo turto balansinė vertė yra 100 000 USD.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="7d8c2-144">Nuomos sutartis keičiama, o šis pakeitimas sukuria naują dabartinę būsimų minimalių nuomos mokesčių (PVFMLP) vertę – 40 000 USD.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="7d8c2-145">Todėl nuomos įsipareigojimas bus debetuojamas – 110 000 USD (150 000 USD – 40 000 USD).</span><span class="sxs-lookup"><span data-stu-id="7d8c2-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="7d8c2-146">Kadangi naudojimo teise valdomas turtas yra tik 100 000 USD, 110 000 USD sumažinimas sumažins turto vertę į mažiau nei 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="7d8c2-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="7d8c2-147">Todėl apskaitos rekomendacijose nurodyta, kad likutis turi būti užsakytas į pelno sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="7d8c2-148">Šiuo atveju galutinis žurnalo įrašas bus 110 000 USD nuomos įsipareigojimo debetas, 100 000 USD nuomos turto kreditas ir 10 000 USD kreditas į pelno sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="7d8c2-149">**Žurnalo įrašų pavyzdys:** nuomos modifikavimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="7d8c2-150">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-151">**Kreditas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="7d8c2-152">**Kreditas:** pelnas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="7d8c2-153">Sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-153">Accumulated depreciation</span></span>

<span data-ttu-id="7d8c2-154">Sąskaita yra susieta su naudojimo teise valdomo turto priešpriešine turto sąskaita.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="7d8c2-155">Sąskaita kredituojama, kai užregistruojamos nusidėvėjimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="7d8c2-156">**Žurnalo įrašų pavyzdys:** nusidėvėjimo kaupimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="7d8c2-157">**Debetas:** nusidėvėjimo išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="7d8c2-158">**Kreditas:** sukauptas nusidėvėjimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="7d8c2-159">Nepaskirstytas pelnas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-159">Retained earnings</span></span>

<span data-ttu-id="7d8c2-160">Sąskaita yra susieta su išsaugotomis pajamomis.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="7d8c2-161">Ši sąskaita gali būti debetuota arba kredituota į perkėlimo koregavimo žurnalo įrašą, naudojant visos retrospektyvos metodą arba kaupiamąjį atgalinės datos parinkties A metodą.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="7d8c2-162">Skirtumo tarp pradinio naudojimo teise valdomo turto ir noro uostos įsipareigojimo suma rezervuojama kaip išaugotos pajamos.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="7d8c2-163">Retais atvejais nepaskirstytas pelnas taip pat gali būti paveiktas atliekant nuomos modifikaciją, jei nuomos klasifikacija pasikeičia iš finansų į veiklos, kad būtų galima padidinti arba sumažinti naudojimo teise valdomo turto vertę ir prilyginti nuomos įsipareigojimui.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="7d8c2-164">**Žurnalo įrašų pavyzdžiai:** perkėlimo koregavimas (visos retrospektyvos arba kaupiamasis atgalinės datos parinkties A metodas)</span><span class="sxs-lookup"><span data-stu-id="7d8c2-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="7d8c2-165">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-166">**Kreditas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="7d8c2-167">**Kreditas:** išsaugotos pajamos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="7d8c2-168">Kintamas mokėjimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-168">Variable payment</span></span>

<span data-ttu-id="7d8c2-169">Sąskaita yra susieta su kintamaisiais nuomos mokėjimais, kuriuos sukuria indekso perkainojimas pagal ASC 842, ASC 840 ir IAS 17 nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="7d8c2-170">Nuomos mokėjimo grafike kintamieji mokėjimai įtraukiami į stulpelį **Kintamieji mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="7d8c2-171">Ši sąskaita debetuojama, kai SF kuriama pagal mokėjimo grafiko eilutę, kurioje yra kintamasis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="7d8c2-172">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7d8c2-173">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-174">**Debetas:** kintamasis mokėjimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="7d8c2-175">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="7d8c2-176">Atidėtojo nuomos mokėjimo turtas (įsipareigojimas)</span><span class="sxs-lookup"><span data-stu-id="7d8c2-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="7d8c2-177">Sąskaita yra susieta su atidėtojo nuomos mokėjimo turtu arba įsipareigojimu, kurį sukuria atidėtųjų nuomos mokėjimų apdorojimo nuoma.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="7d8c2-178">Ši sąskaita debetuojama, kai SF užregistruojama pagal atidėtojo nuomos mokėjimo apdorojimo nuomą, jei nuomos mokesčio suma yra didesnė nei laikotarpio tiesinės nuomos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="7d8c2-179">Ji kredituojama, jei nuomos mokestis yra mažesnis už laikotarpio tiesines nuomos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="7d8c2-180">**Žurnalo įrašų pavyzdžiai:** nuomos mokestis (atidėtojo nuomos mokėjimo apdorojimo nuoma)</span><span class="sxs-lookup"><span data-stu-id="7d8c2-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="7d8c2-181">**Debetas:** nuomos išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="7d8c2-182">**Kreditas:** atidėtojo nuomos mokėjimo įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="7d8c2-183">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="7d8c2-184">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="7d8c2-184">Lease expense</span></span>

<span data-ttu-id="7d8c2-185">Sąskaita yra susieta su nuomos išlaidomis, jei nuoma klasifikuojama kaip atidėtojo nuomos mokėjimo apdorojimo nuoma.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="7d8c2-186">Ši sąskaita debetuojama, kai SF užregistruojama pagal atidėtojo nuomos mokėjimo apdorojimo nuomą.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="7d8c2-187">**Žurnalo įrašų pavyzdžiai:** nuomos mokestis (atidėtojo nuomos mokėjimo apdorojimo nuoma)</span><span class="sxs-lookup"><span data-stu-id="7d8c2-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="7d8c2-188">**Debetas:** nuomos išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="7d8c2-189">**Kreditas:** atidėtojo nuomos mokėjimo įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="7d8c2-190">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="7d8c2-191">Nuvertėjimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="7d8c2-191">Impairment expense</span></span>

<span data-ttu-id="7d8c2-192">Sąskaita užregistruojama, kai nuoma nuvertėja.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="7d8c2-193">Ši sąskaita debetuojama, o naudojimo teise valdomo turto sąskaita tiesiogiai kredituojama.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="7d8c2-194">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7d8c2-195">**Debetas:** nuvertėjimo išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="7d8c2-196">**Kreditas:** naudojimo teise valdomas turtas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="7d8c2-197">Nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-197">Lease payment</span></span>

<span data-ttu-id="7d8c2-198">Sąskaita užregistruojama, jei parametras **Mokėti tiekėjui** yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="7d8c2-199">Ši sąskaita kredituojama vietoj tiekėjo mokėtinos sumos, jei parametras išjungtas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="7d8c2-200">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7d8c2-201">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7d8c2-202">**Kreditas:** nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="7d8c2-203">Išlaidų tipo registravimas</span><span class="sxs-lookup"><span data-stu-id="7d8c2-203">Expense type postings</span></span>

<span data-ttu-id="7d8c2-204">Sąskaita, kuri pasirenkama kiekvienam išlaidų tipui, debetuojama, kai sugeneruojamas išlaidų tipo mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="7d8c2-205">Pavyzdžiui, nurodyta išlaidų tipo **Draudimas** sąskaita debetuojama kiekvieną kartą, kai SF arba mokėjimo žurnalo įrašas sukuriamas iš eksploatavimo išlaidų grafiko, skirto draudimo išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="7d8c2-206">**Žurnalo įrašų pavyzdys:** draudimo mokestis</span><span class="sxs-lookup"><span data-stu-id="7d8c2-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="7d8c2-207">**Debetas:** draudimo išlaidų tipo sąskaita XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="7d8c2-208">**Kreditas:** korespondentinė sąskaita XXX</span><span class="sxs-lookup"><span data-stu-id="7d8c2-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="7d8c2-209">Korespondentinė sąskaita pasirenkama nuomos lygyje eilutėse, skirtose eksploatavimo išlaidų mokėjimo grafikui.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="7d8c2-210">Ši korespondentinė sąskaita gali būti susieta su tiekėju arba su DK sąskaita.</span><span class="sxs-lookup"><span data-stu-id="7d8c2-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
