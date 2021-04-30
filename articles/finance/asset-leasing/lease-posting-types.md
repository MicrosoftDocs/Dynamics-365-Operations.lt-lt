---
title: Nuomos registravimo tipai
description: Šioje temoje aprašomi registravimo tipai, naudojami turto nuomos operacijose.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881137"
---
# <a name="lease-posting-types"></a><span data-ttu-id="27614-103">Nuomos registravimo tipai</span><span class="sxs-lookup"><span data-stu-id="27614-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27614-104">Šioje temoje aprašomi registravimo tipai, naudojami turto nuomos operacijose.</span><span class="sxs-lookup"><span data-stu-id="27614-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="27614-105">Nuomos turtas</span><span class="sxs-lookup"><span data-stu-id="27614-105">Lease asset</span></span>

<span data-ttu-id="27614-106">Sąskaita yra susieta su naudojimo teise valdomu (ROU) turtu.</span><span class="sxs-lookup"><span data-stu-id="27614-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="27614-107">Ši sąskaita debetuojama, kai nuoma iš pradžių pripažįstama naujais nuomos apskaitos standartais, Apskaitos standartų kodifikavimu tema Nr. 842 (ASC 842) ir Tarptautinių finansinių ataskaitų standartu Nr. 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="27614-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="27614-108">Jei nuoma modifikuota, ši sąskaita gali būti debetuojama arba kredituojama, atsižvelgiant į tai, ar modifikavimas padidina, ar sumažina nuomos įsipareigojimą.</span><span class="sxs-lookup"><span data-stu-id="27614-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="27614-109">**Žurnalo įrašų pavyzdys:** pirminis pripažinimas</span><span class="sxs-lookup"><span data-stu-id="27614-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="27614-110">**Debetas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="27614-111">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="27614-112">Nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="27614-112">Lease liability</span></span>

<span data-ttu-id="27614-113">Sąskaita yra susieta su nuomos įsipareigojimu, kuris atsiranda, kai mokėjimai yra diskontuojami naudojant naujus IFRS 16 ir ASC 842 standartus.</span><span class="sxs-lookup"><span data-stu-id="27614-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="27614-114">Ši sąskaita kredituojama, kai nuoma iš pradžių pripažįstama naujais standartais.</span><span class="sxs-lookup"><span data-stu-id="27614-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="27614-115">Ji debetuojama vykdant nuomos mokėjimus ir kredituojama kaupiant palūkanas.</span><span class="sxs-lookup"><span data-stu-id="27614-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="27614-116">**Žurnalo įrašų pavyzdys:** pirminis pripažinimas</span><span class="sxs-lookup"><span data-stu-id="27614-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="27614-117">**Debetas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="27614-118">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="27614-119">**Žurnalo įrašų pavyzdys:** palūkanų kaupimas</span><span class="sxs-lookup"><span data-stu-id="27614-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="27614-120">**Debetas:** palūkanų sąnaudos XXX</span><span class="sxs-lookup"><span data-stu-id="27614-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="27614-121">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="27614-122">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="27614-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="27614-123">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="27614-124">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="27614-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="27614-125">Trumpalaikis nuomos įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="27614-125">Short-term lease liability</span></span>

<span data-ttu-id="27614-126">Sąskaita yra susieta su trumpalaikiu nuomos įsipareigojimu, kai užregistruojamas trumpalaikis nuomos įsipareigojimų perklasifikavimo žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="27614-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="27614-127">Ši sąskaita kredituojama už trumpalaikį įsipareigojimą iš amortizacijos grafiko paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="27614-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="27614-128">Tačiau ta pati suma debetuojama kito mėnesio pirmąją dieną.</span><span class="sxs-lookup"><span data-stu-id="27614-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="27614-129">**Žurnalo įrašų pavyzdys:** trumpalaikis nuomos įsipareigojimų perklasifikavimas</span><span class="sxs-lookup"><span data-stu-id="27614-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="27614-130">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="27614-131">**Kreditas:** trumpalaikis nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="27614-132">**Debetas:** trumpalaikis nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="27614-133">**Kreditas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="27614-134">Likvidavimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="27614-134">Depreciation expense</span></span>

<span data-ttu-id="27614-135">Sąskaita yra susieta su išlaidomis, susijusiomis su naudojimo teise valdomo turto nusidėvėjimu pagal IFRS 16, ASC 842 bei finansine nuoma pagal IAS 17 ir ASC 840.</span><span class="sxs-lookup"><span data-stu-id="27614-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="27614-136">Ši sąskaita debetuojama, kai naudojimo teise valdomas turtas nusidėvi kiekvieną mėnesį.</span><span class="sxs-lookup"><span data-stu-id="27614-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="27614-137">**Žurnalo įrašų pavyzdys:** nusidėvėjimo kaupimas</span><span class="sxs-lookup"><span data-stu-id="27614-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="27614-138">**Debetas:** nusidėvėjimo išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="27614-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="27614-139">**Kreditas:** sukauptas nusidėvėjimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="27614-140">Nuomos modifikavimo pelnas / nuostolis</span><span class="sxs-lookup"><span data-stu-id="27614-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="27614-141">Sąskaita yra susieta su bet kokiu pelnu ar nuostoliu, atsirandančiu dėl nuomos pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="27614-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="27614-142">Pelnas gali kilti dėl nuomos modifikacijos, jei modifikavus nuomos įsipareigojimas sumažėja suma, viršijančia naudojimo teise valdomo turto balansinę vertę.</span><span class="sxs-lookup"><span data-stu-id="27614-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="27614-143">Pavyzdžiui, dabartinė nuomos įsipareigojimo balansinė vertė yra 150 000 USD, o naudojimo teise valdomo turto balansinė vertė yra 100 000 USD.</span><span class="sxs-lookup"><span data-stu-id="27614-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="27614-144">Nuomos sutartis keičiama, o šis pakeitimas sukuria naują dabartinę būsimų minimalių nuomos mokesčių (PVFMLP) vertę – 40 000 USD.</span><span class="sxs-lookup"><span data-stu-id="27614-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="27614-145">Todėl nuomos įsipareigojimas bus debetuojamas – 110 000 USD (150 000 USD – 40 000 USD).</span><span class="sxs-lookup"><span data-stu-id="27614-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="27614-146">Kadangi naudojimo teise valdomas turtas yra tik 100 000 USD, 110 000 USD sumažinimas sumažins turto vertę į mažiau nei 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="27614-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="27614-147">Todėl apskaitos rekomendacijose nurodyta, kad likutis turi būti užsakytas į pelno sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="27614-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="27614-148">Šiuo atveju galutinis žurnalo įrašas bus 110 000 USD nuomos įsipareigojimo debetas, 100 000 USD nuomos turto kreditas ir 10 000 USD kreditas į pelno sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="27614-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="27614-149">**Žurnalo įrašų pavyzdys:** nuomos modifikavimas</span><span class="sxs-lookup"><span data-stu-id="27614-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="27614-150">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="27614-151">**Kreditas:** nuomos turtas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="27614-152">**Kreditas:** pelnas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="27614-153">Sukauptas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="27614-153">Accumulated depreciation</span></span>

<span data-ttu-id="27614-154">Sąskaita yra susieta su naudojimo teise valdomo turto priešpriešine turto sąskaita.</span><span class="sxs-lookup"><span data-stu-id="27614-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="27614-155">Sąskaita kredituojama, kai užregistruojamos nusidėvėjimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="27614-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="27614-156">**Žurnalo įrašų pavyzdys:** nusidėvėjimo kaupimas</span><span class="sxs-lookup"><span data-stu-id="27614-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="27614-157">**Debetas:** nusidėvėjimo išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="27614-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="27614-158">**Kreditas:** sukauptas nusidėvėjimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="27614-159">Kintamas mokėjimas</span><span class="sxs-lookup"><span data-stu-id="27614-159">Variable payment</span></span>

<span data-ttu-id="27614-160">Sąskaita yra susieta su kintamaisiais nuomos mokėjimais, kuriuos sukuria indekso perkainojimas pagal ASC 842, ASC 840 ir IAS 17 nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="27614-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="27614-161">Nuomos mokėjimo grafike kintamieji mokėjimai įtraukiami į stulpelį **Kintamieji mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="27614-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="27614-162">Ši sąskaita debetuojama, kai SF kuriama pagal mokėjimo grafiko eilutę, kurioje yra kintamasis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="27614-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="27614-163">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="27614-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="27614-164">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="27614-165">**Debetas:** kintamasis mokėjimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="27614-166">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="27614-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="27614-167">Atidėtojo nuomos mokėjimo turtas (įsipareigojimas)</span><span class="sxs-lookup"><span data-stu-id="27614-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="27614-168">Sąskaita yra susieta su atidėtojo nuomos mokėjimo turtu arba įsipareigojimu, kurį sukuria atidėtųjų nuomos mokėjimų apdorojimo nuoma.</span><span class="sxs-lookup"><span data-stu-id="27614-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="27614-169">Ši sąskaita debetuojama, kai SF užregistruojama pagal atidėtojo nuomos mokėjimo apdorojimo nuomą, jei nuomos mokesčio suma yra didesnė nei laikotarpio tiesinės nuomos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="27614-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="27614-170">Ji kredituojama, jei nuomos mokestis yra mažesnis už laikotarpio tiesines nuomos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="27614-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="27614-171">**Žurnalo įrašų pavyzdžiai:** nuomos mokestis (atidėtojo nuomos mokėjimo apdorojimo nuoma)</span><span class="sxs-lookup"><span data-stu-id="27614-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="27614-172">**Debetas:** nuomos išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="27614-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="27614-173">**Kreditas:** atidėtojo nuomos mokėjimo įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="27614-174">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="27614-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="27614-175">Nuomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="27614-175">Lease expense</span></span>

<span data-ttu-id="27614-176">Sąskaita yra susieta su nuomos išlaidomis, jei nuoma klasifikuojama kaip atidėtojo nuomos mokėjimo apdorojimo nuoma.</span><span class="sxs-lookup"><span data-stu-id="27614-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="27614-177">Ši sąskaita debetuojama, kai SF užregistruojama pagal atidėtojo nuomos mokėjimo apdorojimo nuomą.</span><span class="sxs-lookup"><span data-stu-id="27614-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="27614-178">**Žurnalo įrašų pavyzdžiai:** nuomos mokestis (atidėtojo nuomos mokėjimo apdorojimo nuoma)</span><span class="sxs-lookup"><span data-stu-id="27614-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="27614-179">**Debetas:** nuomos išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="27614-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="27614-180">**Kreditas:** atidėtojo nuomos mokėjimo įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="27614-181">**Kreditas:** tiekėjo mokėtina suma / nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="27614-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="27614-182">Nuvertėjimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="27614-182">Impairment expense</span></span>

<span data-ttu-id="27614-183">Sąskaita užregistruojama, kai nuoma nuvertėja.</span><span class="sxs-lookup"><span data-stu-id="27614-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="27614-184">Ši sąskaita debetuojama, o naudojimo teise valdomo turto sąskaita tiesiogiai kredituojama.</span><span class="sxs-lookup"><span data-stu-id="27614-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="27614-185">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="27614-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="27614-186">**Debetas:** nuvertėjimo išlaidos XXX</span><span class="sxs-lookup"><span data-stu-id="27614-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="27614-187">**Kreditas:** naudojimo teise valdomas turtas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="27614-188">Nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="27614-188">Lease payment</span></span>

<span data-ttu-id="27614-189">Sąskaita užregistruojama, jei parametras **Mokėti tiekėjui** yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="27614-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="27614-190">Ši sąskaita kredituojama vietoj tiekėjo mokėtinos sumos, jei parametras išjungtas.</span><span class="sxs-lookup"><span data-stu-id="27614-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="27614-191">**Žurnalo įrašų pavyzdys:** nuomos mokestis</span><span class="sxs-lookup"><span data-stu-id="27614-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="27614-192">**Debetas:** nuomos įsipareigojimas XXX</span><span class="sxs-lookup"><span data-stu-id="27614-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="27614-193">**Kreditas:** nuomos mokestis XXX</span><span class="sxs-lookup"><span data-stu-id="27614-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="27614-194">Išlaidų tipo registravimas</span><span class="sxs-lookup"><span data-stu-id="27614-194">Expense type postings</span></span>

<span data-ttu-id="27614-195">Sąskaita, kuri pasirenkama kiekvienam išlaidų tipui, debetuojama, kai sugeneruojamas išlaidų tipo mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="27614-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="27614-196">Pavyzdžiui, nurodyta išlaidų tipo **Draudimas** sąskaita debetuojama kiekvieną kartą, kai SF arba mokėjimo žurnalo įrašas sukuriamas iš eksploatavimo išlaidų grafiko, skirto draudimo išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="27614-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="27614-197">**Žurnalo įrašų pavyzdys:** draudimo mokestis</span><span class="sxs-lookup"><span data-stu-id="27614-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="27614-198">**Debetas:** draudimo išlaidų tipo sąskaita XXX</span><span class="sxs-lookup"><span data-stu-id="27614-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="27614-199">**Kreditas:** korespondentinė sąskaita XXX</span><span class="sxs-lookup"><span data-stu-id="27614-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="27614-200">Korespondentinė sąskaita pasirenkama nuomos lygyje eilutėse, skirtose eksploatavimo išlaidų mokėjimo grafikui.</span><span class="sxs-lookup"><span data-stu-id="27614-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="27614-201">Ši korespondentinė sąskaita gali būti susieta su tiekėju arba su DK sąskaita.</span><span class="sxs-lookup"><span data-stu-id="27614-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
