---
title: Bendrojo žurnalo eilučių PVM apskaičiavimas
description: Šioje temoje paaiškinama, kaip bendrojo žurnalo eilutėse apskaičiuojami įvairių tipų sąskaitų (tiekėjo, kliento, DK ir projekto) PVM.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570199"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="c8a72-103">Bendrojo žurnalo eilučių PVM apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="c8a72-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8a72-104">Šioje temoje paaiškinama, kaip bendrojo žurnalo eilutėse apskaičiuojami įvairių tipų sąskaitų (tiekėjo, kliento, DK ir projekto) PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="c8a72-105">Procesą galima suskirstyti į tris etapus.</span><span class="sxs-lookup"><span data-stu-id="c8a72-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="c8a72-106">PVM krypties nustatymas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="c8a72-107">PVM sumos, kuri bus fiksuojama laikinoje PVM lentelėje, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="c8a72-108">PVM sumos ir kvito sąskaitos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="c8a72-109">PVM krypties nustatymas</span><span class="sxs-lookup"><span data-stu-id="c8a72-109">Determine the sales tax direction</span></span>

<span data-ttu-id="c8a72-110">PVM krypties nustatymo būdas priklauso nuo kvito sąskaitos tipo.</span><span class="sxs-lookup"><span data-stu-id="c8a72-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="c8a72-111">PVM kryptis priklauso nuo sąskaitos tipo ir PVM kodo derinio.</span><span class="sxs-lookup"><span data-stu-id="c8a72-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="c8a72-112">Toliau esančiuose skyriuose galimybės aprašomos išsamiau.</span><span class="sxs-lookup"><span data-stu-id="c8a72-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="c8a72-113">Sąskaitos tipas yra Projektas</span><span class="sxs-lookup"><span data-stu-id="c8a72-113">Account type is Project</span></span>

<span data-ttu-id="c8a72-114">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Projektas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="c8a72-115">Toliau esančiame paveikslėlyje parodyta taisyklė.</span><span class="sxs-lookup"><span data-stu-id="c8a72-115">The following illustration shows the rule.</span></span> <span data-ttu-id="c8a72-116">Toliau pateikiamuose punktuose rodomos galimos projekto sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="c8a72-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="c8a72-117">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="c8a72-118">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c8a72-119">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c8a72-120">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c8a72-121">Kitu atveju PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="c8a72-122">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="c8a72-122">The following diagram illustrates the rule graphically.</span></span>

![Projekto sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="c8a72-124">Sąskaitos tipas yra Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="c8a72-124">Account type is Vendor</span></span>

<span data-ttu-id="c8a72-125">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Tiekėjas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="c8a72-126">Toliau pateikiamuose punktuose rodomos galimos tiekėjų sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="c8a72-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="c8a72-127">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c8a72-128">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="c8a72-129">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="c8a72-130">Kitu atveju PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c8a72-131">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="c8a72-131">The following diagram illustrates the rule graphically.</span></span>

![Tiekėjų sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="c8a72-133">Sąskaitos tipas yra Klientas</span><span class="sxs-lookup"><span data-stu-id="c8a72-133">Account type is Customer</span></span>

<span data-ttu-id="c8a72-134">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Klientas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="c8a72-135">Toliau pateikiamuose punktuose rodomos galimos klientų sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="c8a72-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="c8a72-136">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="c8a72-137">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c8a72-138">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c8a72-139">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c8a72-140">Kitu atveju PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="c8a72-141">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="c8a72-141">The following diagram illustrates the rule graphically.</span></span>

![Klientų sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="c8a72-143">Sąskaitos tipas yra DK</span><span class="sxs-lookup"><span data-stu-id="c8a72-143">Account type is Ledger</span></span>

<span data-ttu-id="c8a72-144">Toliau pateikiamame paveikslėlyje pavaizduota taisyklė, galiojanti, jei kvite yra tik žurnalo eilutės, kurių sąskaitos tipas yra **DK**.</span><span class="sxs-lookup"><span data-stu-id="c8a72-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="c8a72-145">Toliau pateikiamuose punktuose rodomos galimos DK sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="c8a72-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="c8a72-146">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="c8a72-147">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c8a72-148">Kitu atveju, jei žurnalo suma yra debetas (teigiama), PVM kryptis yra Gautinas PVM; jei žurnalo suma yra kreditas (neigiama), PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="c8a72-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c8a72-149">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="c8a72-149">The following diagram illustrates the rule graphically.</span></span>

![DK sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="c8a72-151">PVM krypties keitimas</span><span class="sxs-lookup"><span data-stu-id="c8a72-151">Override the sales tax direction</span></span>

<span data-ttu-id="c8a72-152">Galite pakeisti PVM kryptį, kai kvite yra tik eilutės, kurių sąskaitų tipas yra **DK**.</span><span class="sxs-lookup"><span data-stu-id="c8a72-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="c8a72-153">Eikite į **DK \> Sąskaitų planas \> Sąskaitos \> Pagrindinės sąskaitos** ir pasirinkite FastTab **Juridinio subjekto nepaisymai**.</span><span class="sxs-lookup"><span data-stu-id="c8a72-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="c8a72-154">PVM sumos nustatymas</span><span class="sxs-lookup"><span data-stu-id="c8a72-154">Determine the sales tax amount</span></span>

<span data-ttu-id="c8a72-155">Šiame skyriuje aprašoma, kaip apskaičiuojamas PVM sumos ženklas.</span><span class="sxs-lookup"><span data-stu-id="c8a72-155">This section describes how the sales tax amount sign is calculated.</span></span>

![PVM operacijų puslapis](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="c8a72-157">Šioje lentelėje pateikiama bendroji taisyklė, taikoma nustatant PVM sumų ženklą laikinoje PVM lentelėje.</span><span class="sxs-lookup"><span data-stu-id="c8a72-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="c8a72-158">Žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="c8a72-158">Journal line amount</span></span> | <span data-ttu-id="c8a72-159">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="c8a72-159">Sales tax direction</span></span>  | <span data-ttu-id="c8a72-160">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="c8a72-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="c8a72-161">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-161">Positive</span></span>            | <span data-ttu-id="c8a72-162">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-162">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-163">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-163">Positive</span></span>              |
| <span data-ttu-id="c8a72-164">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-164">Positive</span></span>            | <span data-ttu-id="c8a72-165">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-165">Sales Tax Payable</span></span>    | <span data-ttu-id="c8a72-166">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-166">Negative</span></span>              |
| <span data-ttu-id="c8a72-167">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-167">Negative</span></span>            | <span data-ttu-id="c8a72-168">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-168">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-169">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-169">Negative</span></span>              |
| <span data-ttu-id="c8a72-170">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-170">Negative</span></span>            | <span data-ttu-id="c8a72-171">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-171">Sales Tax Payable</span></span>    | <span data-ttu-id="c8a72-172">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-172">Positive</span></span>              |

<span data-ttu-id="c8a72-173">Yra speciali taisyklė, taikoma kvitams, kuriuose yra tik **Projekto** arba **DK** eilučių, kai PVM grupė arba prekės PVM grupė pasirenkama **DK** eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c8a72-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="c8a72-174">Šią taisyklę valdo funkcija Įgalinti nepriklausomą PVM skaičiavimą bendriesiems žurnalams.</span><span class="sxs-lookup"><span data-stu-id="c8a72-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="c8a72-175">Kai ši funkcija išjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama **Projekto** eilutės debeto / kredito kryptis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="c8a72-176">Kai ši funkcija įjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama jos pačios debeto / kredito kryptis.</span><span class="sxs-lookup"><span data-stu-id="c8a72-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="c8a72-177">Toliau esančiose lentelėse pateikiama kiekvieno scenarijaus taisyklė.</span><span class="sxs-lookup"><span data-stu-id="c8a72-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="c8a72-178">**Taisyklė, kai funkcija įjungta**</span><span class="sxs-lookup"><span data-stu-id="c8a72-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="c8a72-179">Projekto žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="c8a72-179">Journal line amount of project</span></span> | <span data-ttu-id="c8a72-180">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="c8a72-180">Sales tax direction</span></span>  | <span data-ttu-id="c8a72-181">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="c8a72-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="c8a72-182">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-182">Positive</span></span>                       | <span data-ttu-id="c8a72-183">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-183">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-184">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-184">Positive</span></span>              |
| <span data-ttu-id="c8a72-185">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-185">Negative</span></span>                       | <span data-ttu-id="c8a72-186">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-186">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-187">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-187">Negative</span></span>              |

<span data-ttu-id="c8a72-188">**Taisyklė, kai funkcija išjungta**</span><span class="sxs-lookup"><span data-stu-id="c8a72-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="c8a72-189">DK žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="c8a72-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="c8a72-190">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="c8a72-190">Sales tax direction</span></span>  | <span data-ttu-id="c8a72-191">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="c8a72-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="c8a72-192">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-192">Positive</span></span>                       | <span data-ttu-id="c8a72-193">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-193">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-194">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-194">Positive</span></span>              |
| <span data-ttu-id="c8a72-195">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-195">Negative</span></span>                       | <span data-ttu-id="c8a72-196">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-196">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-197">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="c8a72-198">PVM sumos ir kvito sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="c8a72-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="c8a72-199">Kai registruojate PVM, pagrindinė sąskaita gaunama iš DK registravimo grupės profilio.</span><span class="sxs-lookup"><span data-stu-id="c8a72-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="c8a72-200">Kai PVM yra gautinas, sistema naudoja sąskaitą Gautinas PVM, kuris nurodytas profilyje.</span><span class="sxs-lookup"><span data-stu-id="c8a72-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="c8a72-201">Kai PVM yra mokėtinas, sistema naudoja sąskaitą Mokėtinas PVM, kuris nurodytas profilyje.</span><span class="sxs-lookup"><span data-stu-id="c8a72-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="c8a72-202">Šioje lentelėje pateikiama bendroji taisyklė.</span><span class="sxs-lookup"><span data-stu-id="c8a72-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="c8a72-203">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="c8a72-203">Sales tax direction</span></span>  | <span data-ttu-id="c8a72-204">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="c8a72-204">Sales tax amount sign</span></span> | <span data-ttu-id="c8a72-205">PVM sąskaita</span><span class="sxs-lookup"><span data-stu-id="c8a72-205">Sales tax account</span></span>      | <span data-ttu-id="c8a72-206">Kvito suma</span><span class="sxs-lookup"><span data-stu-id="c8a72-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="c8a72-207">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-207">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-208">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-208">Positive</span></span>              | <span data-ttu-id="c8a72-209">Gautino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="c8a72-209">Tax Receivable Account</span></span> | <span data-ttu-id="c8a72-210">Teigiama (debetas)</span><span class="sxs-lookup"><span data-stu-id="c8a72-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="c8a72-211">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-211">Sales Tax Receivable</span></span> | <span data-ttu-id="c8a72-212">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-212">Negative</span></span>              | <span data-ttu-id="c8a72-213">Gautino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="c8a72-213">Tax Receivable Account</span></span> | <span data-ttu-id="c8a72-214">Neigiamas (kreditas)</span><span class="sxs-lookup"><span data-stu-id="c8a72-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="c8a72-215">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-215">Sales Tax Payable</span></span>    | <span data-ttu-id="c8a72-216">Teigiama</span><span class="sxs-lookup"><span data-stu-id="c8a72-216">Positive</span></span>              | <span data-ttu-id="c8a72-217">Mokėtino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="c8a72-217">Tax Payable Account</span></span>    | <span data-ttu-id="c8a72-218">Neigiamas (kreditas)</span><span class="sxs-lookup"><span data-stu-id="c8a72-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="c8a72-219">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="c8a72-219">Sales Tax Payable</span></span>    | <span data-ttu-id="c8a72-220">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="c8a72-220">Negative</span></span>              | <span data-ttu-id="c8a72-221">Mokėtino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="c8a72-221">Tax Payable Account</span></span>    | <span data-ttu-id="c8a72-222">Teigiama (debetas)</span><span class="sxs-lookup"><span data-stu-id="c8a72-222">Positive (Debit)</span></span>  |
