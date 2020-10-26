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
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983602"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="988e8-103">Bendrojo žurnalo eilučių PVM apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="988e8-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="988e8-104">Šioje temoje paaiškinama, kaip bendrojo žurnalo eilutėse apskaičiuojami įvairių tipų sąskaitų (tiekėjo, kliento, DK ir projekto) PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="988e8-105">Procesą galima suskirstyti į tris etapus.</span><span class="sxs-lookup"><span data-stu-id="988e8-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="988e8-106">PVM krypties nustatymas.</span><span class="sxs-lookup"><span data-stu-id="988e8-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="988e8-107">PVM sumos, kuri bus fiksuojama laikinoje PVM lentelėje, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="988e8-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="988e8-108">PVM sumos ir kvito sąskaitos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="988e8-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="988e8-109">PVM krypties nustatymas</span><span class="sxs-lookup"><span data-stu-id="988e8-109">Determine the sales tax direction</span></span>

<span data-ttu-id="988e8-110">PVM krypties nustatymo būdas priklauso nuo kvito sąskaitos tipo.</span><span class="sxs-lookup"><span data-stu-id="988e8-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="988e8-111">PVM kryptis priklauso nuo sąskaitos tipo ir PVM kodo derinio.</span><span class="sxs-lookup"><span data-stu-id="988e8-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="988e8-112">Toliau esančiuose skyriuose galimybės aprašomos išsamiau.</span><span class="sxs-lookup"><span data-stu-id="988e8-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="988e8-113">Sąskaitos tipas yra Projektas</span><span class="sxs-lookup"><span data-stu-id="988e8-113">Account type is Project</span></span>

<span data-ttu-id="988e8-114">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Projektas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="988e8-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="988e8-115">Toliau esančiame paveikslėlyje parodyta taisyklė.</span><span class="sxs-lookup"><span data-stu-id="988e8-115">The following illustration shows the rule.</span></span> <span data-ttu-id="988e8-116">Toliau pateikiamuose punktuose rodomos galimos projekto sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="988e8-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="988e8-117">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="988e8-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="988e8-118">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="988e8-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="988e8-119">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="988e8-120">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="988e8-121">Kitu atveju PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="988e8-122">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="988e8-122">The following diagram illustrates the rule graphically.</span></span>

![Projekto sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="988e8-124">Sąskaitos tipas yra Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="988e8-124">Account type is Vendor</span></span>

<span data-ttu-id="988e8-125">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Tiekėjas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="988e8-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="988e8-126">Toliau pateikiamuose punktuose rodomos galimos tiekėjų sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="988e8-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="988e8-127">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="988e8-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="988e8-128">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="988e8-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="988e8-129">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="988e8-130">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="988e8-131">Kitu atveju PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="988e8-132">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="988e8-132">The following diagram illustrates the rule graphically.</span></span>

![Tiekėjų sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="988e8-134">Sąskaitos tipas yra Klientas</span><span class="sxs-lookup"><span data-stu-id="988e8-134">Account type is Customer</span></span>

<span data-ttu-id="988e8-135">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Klientas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="988e8-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="988e8-136">Toliau pateikiamuose punktuose rodomos galimos klientų sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="988e8-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="988e8-137">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="988e8-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="988e8-138">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="988e8-139">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="988e8-140">Kitu atveju PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="988e8-141">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="988e8-141">The following diagram illustrates the rule graphically.</span></span>

![Klientų sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="988e8-143">Sąskaitos tipas yra DK</span><span class="sxs-lookup"><span data-stu-id="988e8-143">Account type is Ledger</span></span>

<span data-ttu-id="988e8-144">Toliau pateikiamame paveikslėlyje pavaizduota taisyklė, galiojanti, jei kvite yra tik žurnalo eilutės, kurių sąskaitos tipas yra **DK**.</span><span class="sxs-lookup"><span data-stu-id="988e8-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="988e8-145">Toliau pateikiamuose punktuose rodomos galimos DK sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="988e8-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="988e8-146">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="988e8-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="988e8-147">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="988e8-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="988e8-148">Kitu atveju, jei žurnalo suma yra debetas (teigiama), PVM kryptis yra Gautinas PVM; jei žurnalo suma yra kreditas (neigiama), PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="988e8-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="988e8-149">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="988e8-149">The following diagram illustrates the rule graphically.</span></span>

![DK sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="988e8-151">PVM krypties keitimas</span><span class="sxs-lookup"><span data-stu-id="988e8-151">Override the sales tax direction</span></span>

<span data-ttu-id="988e8-152">Galite pakeisti PVM kryptį, kai kvite yra tik eilutės, kurių sąskaitų tipas yra **DK**.</span><span class="sxs-lookup"><span data-stu-id="988e8-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="988e8-153">Eikite į **DK \> Sąskaitų planas \> Sąskaitos \> Pagrindinės sąskaitos** ir pasirinkite FastTab **Juridinio subjekto nepaisymai**.</span><span class="sxs-lookup"><span data-stu-id="988e8-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="988e8-154">PVM sumos nustatymas</span><span class="sxs-lookup"><span data-stu-id="988e8-154">Determine the sales tax amount</span></span>

<span data-ttu-id="988e8-155">Šiame skyriuje aprašoma, kaip apskaičiuojamas PVM sumos ženklas.</span><span class="sxs-lookup"><span data-stu-id="988e8-155">This section describes how the sales tax amount sign is calculated.</span></span>

![PVM operacijų puslapis](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="988e8-157">Šioje lentelėje pateikiama bendroji taisyklė, taikoma nustatant PVM sumų ženklą laikinoje PVM lentelėje.</span><span class="sxs-lookup"><span data-stu-id="988e8-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="988e8-158">Žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="988e8-158">Journal line amount</span></span> | <span data-ttu-id="988e8-159">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="988e8-159">Sales tax direction</span></span>  | <span data-ttu-id="988e8-160">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="988e8-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="988e8-161">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-161">Positive</span></span>            | <span data-ttu-id="988e8-162">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-162">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-163">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-163">Positive</span></span>              |
| <span data-ttu-id="988e8-164">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-164">Positive</span></span>            | <span data-ttu-id="988e8-165">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-165">Sales Tax Payable</span></span>    | <span data-ttu-id="988e8-166">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-166">Negative</span></span>              |
| <span data-ttu-id="988e8-167">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-167">Negative</span></span>            | <span data-ttu-id="988e8-168">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-168">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-169">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-169">Negative</span></span>              |
| <span data-ttu-id="988e8-170">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-170">Negative</span></span>            | <span data-ttu-id="988e8-171">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-171">Sales Tax Payable</span></span>    | <span data-ttu-id="988e8-172">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-172">Positive</span></span>              |

<span data-ttu-id="988e8-173">Yra speciali taisyklė, taikoma kvitams, kuriuose yra tik **Projekto** arba **DK** eilučių, kai PVM grupė arba prekės PVM grupė pasirenkama **DK** eilutėje.</span><span class="sxs-lookup"><span data-stu-id="988e8-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="988e8-174">Šią taisyklę valdo funkcija Įgalinti nepriklausomą PVM skaičiavimą bendriesiems žurnalams.</span><span class="sxs-lookup"><span data-stu-id="988e8-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="988e8-175">Kai ši funkcija išjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama **Projekto** eilutės debeto / kredito kryptis.</span><span class="sxs-lookup"><span data-stu-id="988e8-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="988e8-176">Kai ši funkcija įjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama jos pačios debeto / kredito kryptis.</span><span class="sxs-lookup"><span data-stu-id="988e8-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="988e8-177">Toliau esančiose lentelėse pateikiama kiekvieno scenarijaus taisyklė.</span><span class="sxs-lookup"><span data-stu-id="988e8-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="988e8-178">**Taisyklė, kai funkcija įjungta**</span><span class="sxs-lookup"><span data-stu-id="988e8-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="988e8-179">Projekto žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="988e8-179">Journal line amount of project</span></span> | <span data-ttu-id="988e8-180">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="988e8-180">Sales tax direction</span></span>  | <span data-ttu-id="988e8-181">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="988e8-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="988e8-182">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-182">Positive</span></span>                       | <span data-ttu-id="988e8-183">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-183">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-184">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-184">Positive</span></span>              |
| <span data-ttu-id="988e8-185">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-185">Negative</span></span>                       | <span data-ttu-id="988e8-186">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-186">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-187">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-187">Negative</span></span>              |

<span data-ttu-id="988e8-188">**Taisyklė, kai funkcija išjungta**</span><span class="sxs-lookup"><span data-stu-id="988e8-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="988e8-189">DK žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="988e8-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="988e8-190">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="988e8-190">Sales tax direction</span></span>  | <span data-ttu-id="988e8-191">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="988e8-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="988e8-192">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-192">Positive</span></span>                       | <span data-ttu-id="988e8-193">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-193">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-194">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-194">Positive</span></span>              |
| <span data-ttu-id="988e8-195">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-195">Negative</span></span>                       | <span data-ttu-id="988e8-196">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-196">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-197">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="988e8-198">PVM sumos ir kvito sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="988e8-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="988e8-199">Kai registruojate PVM, pagrindinė sąskaita gaunama iš DK registravimo grupės profilio.</span><span class="sxs-lookup"><span data-stu-id="988e8-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="988e8-200">Kai PVM yra gautinas, sistema naudoja sąskaitą Gautinas PVM, kuris nurodytas profilyje.</span><span class="sxs-lookup"><span data-stu-id="988e8-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="988e8-201">Kai PVM yra mokėtinas, sistema naudoja sąskaitą Mokėtinas PVM, kuris nurodytas profilyje.</span><span class="sxs-lookup"><span data-stu-id="988e8-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="988e8-202">Šioje lentelėje pateikiama bendroji taisyklė.</span><span class="sxs-lookup"><span data-stu-id="988e8-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="988e8-203">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="988e8-203">Sales tax direction</span></span>  | <span data-ttu-id="988e8-204">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="988e8-204">Sales tax amount sign</span></span> | <span data-ttu-id="988e8-205">PVM sąskaita</span><span class="sxs-lookup"><span data-stu-id="988e8-205">Sales tax account</span></span>      | <span data-ttu-id="988e8-206">Kvito suma</span><span class="sxs-lookup"><span data-stu-id="988e8-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="988e8-207">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-207">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-208">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-208">Positive</span></span>              | <span data-ttu-id="988e8-209">Gautino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="988e8-209">Tax Receivable Account</span></span> | <span data-ttu-id="988e8-210">Teigiama (debetas)</span><span class="sxs-lookup"><span data-stu-id="988e8-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="988e8-211">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-211">Sales Tax Receivable</span></span> | <span data-ttu-id="988e8-212">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-212">Negative</span></span>              | <span data-ttu-id="988e8-213">Gautino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="988e8-213">Tax Receivable Account</span></span> | <span data-ttu-id="988e8-214">Neigiamas (kreditas)</span><span class="sxs-lookup"><span data-stu-id="988e8-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="988e8-215">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-215">Sales Tax Payable</span></span>    | <span data-ttu-id="988e8-216">Teigiama</span><span class="sxs-lookup"><span data-stu-id="988e8-216">Positive</span></span>              | <span data-ttu-id="988e8-217">Mokėtino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="988e8-217">Tax Payable Account</span></span>    | <span data-ttu-id="988e8-218">Neigiamas (kreditas)</span><span class="sxs-lookup"><span data-stu-id="988e8-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="988e8-219">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="988e8-219">Sales Tax Payable</span></span>    | <span data-ttu-id="988e8-220">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="988e8-220">Negative</span></span>              | <span data-ttu-id="988e8-221">Mokėtino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="988e8-221">Tax Payable Account</span></span>    | <span data-ttu-id="988e8-222">Teigiama (debetas)</span><span class="sxs-lookup"><span data-stu-id="988e8-222">Positive (Debit)</span></span>  |
