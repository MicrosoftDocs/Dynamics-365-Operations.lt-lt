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
ms.openlocfilehash: 354076dbc14f34b83d1cd24f591874b9af856af1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186307"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="65b68-103">Bendrojo žurnalo eilučių PVM apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="65b68-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="65b68-104">Šioje temoje paaiškinama, kaip bendrojo žurnalo eilutėse apskaičiuojami įvairių tipų sąskaitų (tiekėjo, kliento, DK ir projekto) PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="65b68-105">Procesą galima suskirstyti į tris etapus.</span><span class="sxs-lookup"><span data-stu-id="65b68-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="65b68-106">PVM krypties nustatymas.</span><span class="sxs-lookup"><span data-stu-id="65b68-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="65b68-107">PVM sumos, kuri bus fiksuojama laikinoje PVM lentelėje, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="65b68-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="65b68-108">PVM sumos ir kvito sąskaitos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="65b68-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="65b68-109">PVM krypties nustatymas</span><span class="sxs-lookup"><span data-stu-id="65b68-109">Determine the sales tax direction</span></span>

<span data-ttu-id="65b68-110">PVM krypties nustatymo būdas priklauso nuo kvito sąskaitos tipo.</span><span class="sxs-lookup"><span data-stu-id="65b68-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="65b68-111">PVM kryptis priklauso nuo sąskaitos tipo ir PVM kodo derinio.</span><span class="sxs-lookup"><span data-stu-id="65b68-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="65b68-112">Toliau esančiuose skyriuose galimybės aprašomos išsamiau.</span><span class="sxs-lookup"><span data-stu-id="65b68-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="65b68-113">Sąskaitos tipas yra Projektas</span><span class="sxs-lookup"><span data-stu-id="65b68-113">Account type is Project</span></span>

<span data-ttu-id="65b68-114">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Projektas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="65b68-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="65b68-115">Toliau esančiame paveikslėlyje parodyta taisyklė.</span><span class="sxs-lookup"><span data-stu-id="65b68-115">The following illustration shows the rule.</span></span> <span data-ttu-id="65b68-116">Toliau pateikiamuose punktuose rodomos galimos projekto sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="65b68-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="65b68-117">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="65b68-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="65b68-118">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="65b68-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="65b68-119">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="65b68-120">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="65b68-121">Kitu atveju PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="65b68-122">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="65b68-122">The following diagram illustrates the rule graphically.</span></span>

![Projekto sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="65b68-124">Sąskaitos tipas yra Tiekėjas</span><span class="sxs-lookup"><span data-stu-id="65b68-124">Account type is Vendor</span></span>

<span data-ttu-id="65b68-125">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Tiekėjas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="65b68-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="65b68-126">Toliau pateikiamuose punktuose rodomos galimos tiekėjų sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="65b68-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="65b68-127">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="65b68-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="65b68-128">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="65b68-129">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="65b68-130">Kitu atveju PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="65b68-131">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="65b68-131">The following diagram illustrates the rule graphically.</span></span>

![Tiekėjų sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="65b68-133">Sąskaitos tipas yra Klientas</span><span class="sxs-lookup"><span data-stu-id="65b68-133">Account type is Customer</span></span>

<span data-ttu-id="65b68-134">Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Klientas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis.</span><span class="sxs-lookup"><span data-stu-id="65b68-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="65b68-135">Toliau pateikiamuose punktuose rodomos galimos klientų sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="65b68-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="65b68-136">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="65b68-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="65b68-137">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="65b68-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="65b68-138">• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="65b68-139">• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="65b68-140">Kitu atveju PVM kryptis yra Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="65b68-141">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="65b68-141">The following diagram illustrates the rule graphically.</span></span>

![Klientų sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="65b68-143">Sąskaitos tipas yra DK</span><span class="sxs-lookup"><span data-stu-id="65b68-143">Account type is Ledger</span></span>

<span data-ttu-id="65b68-144">Toliau pateikiamame paveikslėlyje pavaizduota taisyklė, galiojanti, jei kvite yra tik žurnalo eilutės, kurių sąskaitos tipas yra **DK**.</span><span class="sxs-lookup"><span data-stu-id="65b68-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="65b68-145">Toliau pateikiamuose punktuose rodomos galimos DK sąskaitų mokesčių kryptys.</span><span class="sxs-lookup"><span data-stu-id="65b68-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="65b68-146">• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="65b68-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="65b68-147">• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="65b68-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="65b68-148">Kitu atveju, jei žurnalo suma yra debetas (teigiama), PVM kryptis yra Gautinas PVM; jei žurnalo suma yra kreditas (neigiama), PVM kryptis yra Mokėtinas PVM.</span><span class="sxs-lookup"><span data-stu-id="65b68-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="65b68-149">Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.</span><span class="sxs-lookup"><span data-stu-id="65b68-149">The following diagram illustrates the rule graphically.</span></span>

![DK sąskaitų mokesčių krypties galimybės](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="65b68-151">PVM krypties keitimas</span><span class="sxs-lookup"><span data-stu-id="65b68-151">Override the sales tax direction</span></span>

<span data-ttu-id="65b68-152">Galite pakeisti PVM kryptį, kai kvite yra tik eilutės, kurių sąskaitų tipas yra **DK**.</span><span class="sxs-lookup"><span data-stu-id="65b68-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="65b68-153">Eikite į **DK \> Sąskaitų planas \> Sąskaitos \> Pagrindinės sąskaitos** ir pasirinkite FastTab **Juridinio subjekto nepaisymai**.</span><span class="sxs-lookup"><span data-stu-id="65b68-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="65b68-154">PVM sumos nustatymas</span><span class="sxs-lookup"><span data-stu-id="65b68-154">Determine the sales tax amount</span></span>

<span data-ttu-id="65b68-155">Šiame skyriuje aprašoma, kaip apskaičiuojamas PVM sumos ženklas.</span><span class="sxs-lookup"><span data-stu-id="65b68-155">This section describes how the sales tax amount sign is calculated.</span></span>

![PVM operacijų puslapis](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="65b68-157">Šioje lentelėje pateikiama bendroji taisyklė, taikoma nustatant PVM sumų ženklą laikinoje PVM lentelėje.</span><span class="sxs-lookup"><span data-stu-id="65b68-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="65b68-158">Žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="65b68-158">Journal line amount</span></span> | <span data-ttu-id="65b68-159">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="65b68-159">Sales tax direction</span></span>  | <span data-ttu-id="65b68-160">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="65b68-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="65b68-161">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-161">Positive</span></span>            | <span data-ttu-id="65b68-162">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-162">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-163">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-163">Positive</span></span>              |
| <span data-ttu-id="65b68-164">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-164">Positive</span></span>            | <span data-ttu-id="65b68-165">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-165">Sales Tax Payable</span></span>    | <span data-ttu-id="65b68-166">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-166">Negative</span></span>              |
| <span data-ttu-id="65b68-167">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-167">Negative</span></span>            | <span data-ttu-id="65b68-168">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-168">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-169">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-169">Negative</span></span>              |
| <span data-ttu-id="65b68-170">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-170">Negative</span></span>            | <span data-ttu-id="65b68-171">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-171">Sales Tax Payable</span></span>    | <span data-ttu-id="65b68-172">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-172">Positive</span></span>              |

<span data-ttu-id="65b68-173">Yra speciali taisyklė, taikoma kvitams, kuriuose yra tik **Projekto** arba **DK** eilučių, kai PVM grupė arba prekės PVM grupė pasirenkama **DK** eilutėje.</span><span class="sxs-lookup"><span data-stu-id="65b68-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="65b68-174">Šią taisyklę valdo funkcija Įgalinti nepriklausomą PVM skaičiavimą bendriesiems žurnalams.</span><span class="sxs-lookup"><span data-stu-id="65b68-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="65b68-175">Kai ši funkcija išjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama **Projekto** eilutės debeto / kredito kryptis.</span><span class="sxs-lookup"><span data-stu-id="65b68-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="65b68-176">Kai ši funkcija įjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama jos pačios debeto / kredito kryptis.</span><span class="sxs-lookup"><span data-stu-id="65b68-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="65b68-177">Toliau esančiose lentelėse pateikiama kiekvieno scenarijaus taisyklė.</span><span class="sxs-lookup"><span data-stu-id="65b68-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="65b68-178">**Taisyklė, kai funkcija įjungta**</span><span class="sxs-lookup"><span data-stu-id="65b68-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="65b68-179">Projekto žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="65b68-179">Journal line amount of project</span></span> | <span data-ttu-id="65b68-180">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="65b68-180">Sales tax direction</span></span>  | <span data-ttu-id="65b68-181">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="65b68-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="65b68-182">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-182">Positive</span></span>                       | <span data-ttu-id="65b68-183">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-183">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-184">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-184">Positive</span></span>              |
| <span data-ttu-id="65b68-185">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-185">Negative</span></span>                       | <span data-ttu-id="65b68-186">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-186">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-187">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-187">Negative</span></span>              |

<span data-ttu-id="65b68-188">**Taisyklė, kai funkcija išjungta**</span><span class="sxs-lookup"><span data-stu-id="65b68-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="65b68-189">DK žurnalo eilutės suma</span><span class="sxs-lookup"><span data-stu-id="65b68-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="65b68-190">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="65b68-190">Sales tax direction</span></span>  | <span data-ttu-id="65b68-191">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="65b68-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="65b68-192">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-192">Positive</span></span>                       | <span data-ttu-id="65b68-193">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-193">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-194">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-194">Positive</span></span>              |
| <span data-ttu-id="65b68-195">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-195">Negative</span></span>                       | <span data-ttu-id="65b68-196">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-196">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-197">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="65b68-198">PVM sumos ir kvito sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="65b68-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="65b68-199">Kai registruojate PVM, pagrindinė sąskaita gaunama iš DK registravimo grupės profilio.</span><span class="sxs-lookup"><span data-stu-id="65b68-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="65b68-200">Kai PVM yra gautinas, sistema naudoja sąskaitą Gautinas PVM, kuris nurodytas profilyje.</span><span class="sxs-lookup"><span data-stu-id="65b68-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="65b68-201">Kai PVM yra mokėtinas, sistema naudoja sąskaitą Mokėtinas PVM, kuris nurodytas profilyje.</span><span class="sxs-lookup"><span data-stu-id="65b68-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="65b68-202">Šioje lentelėje pateikiama bendroji taisyklė.</span><span class="sxs-lookup"><span data-stu-id="65b68-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="65b68-203">PVM kryptis</span><span class="sxs-lookup"><span data-stu-id="65b68-203">Sales tax direction</span></span>  | <span data-ttu-id="65b68-204">PVM sumos ženklas</span><span class="sxs-lookup"><span data-stu-id="65b68-204">Sales tax amount sign</span></span> | <span data-ttu-id="65b68-205">PVM sąskaita</span><span class="sxs-lookup"><span data-stu-id="65b68-205">Sales tax account</span></span>      | <span data-ttu-id="65b68-206">Kvito suma</span><span class="sxs-lookup"><span data-stu-id="65b68-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="65b68-207">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-207">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-208">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-208">Positive</span></span>              | <span data-ttu-id="65b68-209">Gautino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="65b68-209">Tax Receivable Account</span></span> | <span data-ttu-id="65b68-210">Teigiama (debetas)</span><span class="sxs-lookup"><span data-stu-id="65b68-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="65b68-211">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-211">Sales Tax Receivable</span></span> | <span data-ttu-id="65b68-212">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-212">Negative</span></span>              | <span data-ttu-id="65b68-213">Gautino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="65b68-213">Tax Receivable Account</span></span> | <span data-ttu-id="65b68-214">Neigiamas (kreditas)</span><span class="sxs-lookup"><span data-stu-id="65b68-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="65b68-215">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-215">Sales Tax Payable</span></span>    | <span data-ttu-id="65b68-216">Teigiama</span><span class="sxs-lookup"><span data-stu-id="65b68-216">Positive</span></span>              | <span data-ttu-id="65b68-217">Mokėtino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="65b68-217">Tax Payable Account</span></span>    | <span data-ttu-id="65b68-218">Neigiamas (kreditas)</span><span class="sxs-lookup"><span data-stu-id="65b68-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="65b68-219">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="65b68-219">Sales Tax Payable</span></span>    | <span data-ttu-id="65b68-220">Neigiamas</span><span class="sxs-lookup"><span data-stu-id="65b68-220">Negative</span></span>              | <span data-ttu-id="65b68-221">Mokėtino mokesčio sąskaita</span><span class="sxs-lookup"><span data-stu-id="65b68-221">Tax Payable Account</span></span>    | <span data-ttu-id="65b68-222">Teigiama (debetas)</span><span class="sxs-lookup"><span data-stu-id="65b68-222">Positive (Debit)</span></span>  |
