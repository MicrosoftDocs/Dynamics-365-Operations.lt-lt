---
title: Mokesčiuose dviejų valiutų palaikymas
description: Šioje temoje paaiškinama, kaip išplėsti dviejų valiutų apskaitos funkciją mokesčių srityje, ir nurodoma, koks gali būti poveikis mokesčiams apskaičiuoti ir registruoti
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3f7ca56fef636431e152b2db424f1f972a507721
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212210"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="781b1-103">PVM dviejų valiutų palaikymas</span><span class="sxs-lookup"><span data-stu-id="781b1-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="781b1-104">Šioje temoje paaiškinama, kaip išplėsti dviejų valiutų apskaitos funkciją PVM srityje, ir nurodoma, koks gali būti poveikis PVM apskaičiuoti, registruoti ir sudengti.</span><span class="sxs-lookup"><span data-stu-id="781b1-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="781b1-105">„Dynamics 365 Finance“ dviejų valiutų funkcija atsirado 8.1 versijoje (2018 m. spalio mėn.).</span><span class="sxs-lookup"><span data-stu-id="781b1-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="781b1-106">Ji pakeitė, kaip apskaičiuojami apskaitos įrašai ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="781b1-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="781b1-107">Ankstesnėse versijose operacijos buvo konvertuojamos į ataskaitų valiutą tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="781b1-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="781b1-108">Operacijos suma buvo apskaičiuota operacijos valiuta > operacijos suma buvo konvertuota į apskaitos valiutą > apskaitos valiutos suma buvo konvertuota į ataskaitų valiutą</span><span class="sxs-lookup"><span data-stu-id="781b1-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="781b1-109">Įjungus dviejų valiutų funkciją, operacijos buvo konvertuotos į ataskaitų valiutą tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="781b1-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="781b1-110">Suma operacijos valiuta > Suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="781b1-111">Daugiau informacijos apie dviejų valiutų funkciją rasite [Dvi valiutos](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="781b1-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="781b1-112">Dėl dviejų valiutų palaikymo funkcijų valdyme atsirado dvi naujos funkcijos:</span><span class="sxs-lookup"><span data-stu-id="781b1-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="781b1-113">Prekybos mokesčių konvertavimas (naujas versijoje 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="781b1-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="781b1-114">Dviejų valiutų palaikymas PVM srityje užtikrina, kad mokesčiai bus tiksliai apskaičiuoti mokesčių valiuta ir kad PVM sudengimo balansas bus apskaičiuotas tiksliai ir apskaitos valiuta, ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="781b1-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="781b1-115">PVM konvertavimas</span><span class="sxs-lookup"><span data-stu-id="781b1-115">Sales tax conversion</span></span>

<span data-ttu-id="781b1-116">Parametras **PVM konvertavimas** suteikia dvi parinktis, kaip galima konvertuoti mokesčių sumą iš operacijos valiutos į mokesčių valiutą.</span><span class="sxs-lookup"><span data-stu-id="781b1-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="781b1-117">Apskaitos valiuta: kelias: Suma operacijos valiuta > Suma apskaitos valiuta > Suma mokesčių valiuta.</span><span class="sxs-lookup"><span data-stu-id="781b1-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="781b1-118">Apskaitos valiutos keitimo kurso tipas (konfigūruojamas mokesčių valiutos nustatyme) bus naudojamas valiutos konvertavimui.</span><span class="sxs-lookup"><span data-stu-id="781b1-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="781b1-119">Ataskaitų valiuta: kelias: Suma operacijos valiuta > Suma ataskaitų valiuta > Suma mokesčių valiuta.</span><span class="sxs-lookup"><span data-stu-id="781b1-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="781b1-120">Ataskaitų valiutos keitimo kurso tipas (konfigūruojamas mokesčių valiutos nustatyme) bus naudojamas valiutos konvertavimui.</span><span class="sxs-lookup"><span data-stu-id="781b1-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="781b1-121">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="781b1-121">Example</span></span>

<span data-ttu-id="781b1-122">Paprastas pavyzdys, skirtas šiai funkcijai pademonstruoti:</span><span class="sxs-lookup"><span data-stu-id="781b1-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="781b1-123">DK ir mokesčių valiutos nustatymas</span><span class="sxs-lookup"><span data-stu-id="781b1-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="781b1-124">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-124">Transaction currency</span></span> | <span data-ttu-id="781b1-125">Apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-125">Accounting currency</span></span> | <span data-ttu-id="781b1-126">Ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-126">Reporting currency</span></span> | <span data-ttu-id="781b1-127">Mokesčių valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="781b1-128">EUR</span><span class="sxs-lookup"><span data-stu-id="781b1-128">EUR</span></span>                  | <span data-ttu-id="781b1-129">USD</span><span class="sxs-lookup"><span data-stu-id="781b1-129">USD</span></span>                 | <span data-ttu-id="781b1-130">LT</span><span class="sxs-lookup"><span data-stu-id="781b1-130">GBP</span></span>                | <span data-ttu-id="781b1-131">LT</span><span class="sxs-lookup"><span data-stu-id="781b1-131">GBP</span></span>          |

<span data-ttu-id="781b1-132">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="781b1-132">Exchange rate</span></span>

| <span data-ttu-id="781b1-133">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="781b1-133">From currency</span></span> | <span data-ttu-id="781b1-134">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="781b1-134">To currency</span></span> | <span data-ttu-id="781b1-135">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="781b1-135">Factor</span></span> | <span data-ttu-id="781b1-136">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="781b1-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="781b1-137">EUR</span><span class="sxs-lookup"><span data-stu-id="781b1-137">EUR</span></span>           | <span data-ttu-id="781b1-138">USD</span><span class="sxs-lookup"><span data-stu-id="781b1-138">USD</span></span>         | <span data-ttu-id="781b1-139">1</span><span class="sxs-lookup"><span data-stu-id="781b1-139">1</span></span>      | <span data-ttu-id="781b1-140">1.11</span><span class="sxs-lookup"><span data-stu-id="781b1-140">1.11</span></span>          |
| <span data-ttu-id="781b1-141">EUR</span><span class="sxs-lookup"><span data-stu-id="781b1-141">EUR</span></span>           | <span data-ttu-id="781b1-142">LT</span><span class="sxs-lookup"><span data-stu-id="781b1-142">GBP</span></span>         | <span data-ttu-id="781b1-143">1</span><span class="sxs-lookup"><span data-stu-id="781b1-143">1</span></span>      | <span data-ttu-id="781b1-144">0.83</span><span class="sxs-lookup"><span data-stu-id="781b1-144">0.83</span></span>          |
| <span data-ttu-id="781b1-145">USD</span><span class="sxs-lookup"><span data-stu-id="781b1-145">USD</span></span>           | <span data-ttu-id="781b1-146">LT</span><span class="sxs-lookup"><span data-stu-id="781b1-146">GBP</span></span>         | <span data-ttu-id="781b1-147">1</span><span class="sxs-lookup"><span data-stu-id="781b1-147">1</span></span>      | <span data-ttu-id="781b1-148">0.75</span><span class="sxs-lookup"><span data-stu-id="781b1-148">0.75</span></span>          |

<span data-ttu-id="781b1-149">Mokesčio sumos skaičiavimas naudojant skirtingas parametro parinktis</span><span class="sxs-lookup"><span data-stu-id="781b1-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="781b1-150">Mokesčio suma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="781b1-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="781b1-151">PVM konvertavimo parametrai</span><span class="sxs-lookup"><span data-stu-id="781b1-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="781b1-152">Operacijos valiuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="781b1-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="781b1-153">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="781b1-153">Accounting currency (USD)</span></span> | <span data-ttu-id="781b1-154">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="781b1-155">Mokesčių valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="781b1-156">Apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-156">Accounting currency</span></span>             | <span data-ttu-id="781b1-157">100</span><span class="sxs-lookup"><span data-stu-id="781b1-157">100</span></span>                        | <span data-ttu-id="781b1-158">111</span><span class="sxs-lookup"><span data-stu-id="781b1-158">111</span></span>                       | <span data-ttu-id="781b1-159">83</span><span class="sxs-lookup"><span data-stu-id="781b1-159">83</span></span>                       | <span data-ttu-id="781b1-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="781b1-160">**83.25**</span></span>          |
| <span data-ttu-id="781b1-161">Ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-161">Reporting currency</span></span>              | <span data-ttu-id="781b1-162">100</span><span class="sxs-lookup"><span data-stu-id="781b1-162">100</span></span>                        | <span data-ttu-id="781b1-163">111</span><span class="sxs-lookup"><span data-stu-id="781b1-163">111</span></span>                       | <span data-ttu-id="781b1-164">83</span><span class="sxs-lookup"><span data-stu-id="781b1-164">83</span></span>                       | <span data-ttu-id="781b1-165">**83**</span><span class="sxs-lookup"><span data-stu-id="781b1-165">**83**</span></span>             |

<span data-ttu-id="781b1-166">Šis parametras gali būti sukonfigūruotas, atsižvelgiant į tai, ko reikalauja mokesčių inspekcija.</span><span class="sxs-lookup"><span data-stu-id="781b1-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="781b1-167">Atnaujinimo aplinkybės</span><span class="sxs-lookup"><span data-stu-id="781b1-167">Upgrade Consideration</span></span>

<span data-ttu-id="781b1-168">Ši funkcija bus taikoma tik naujoms operacijoms.</span><span class="sxs-lookup"><span data-stu-id="781b1-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="781b1-169">Mokesčių operacijai, kuri jau įrašyta TAXTRANS lentelėje, bet dar nėra sudengta, sistema neperskaičiuos mokesčių sumos mokesčių valiuta, nes registruojant mokestį nėra valiutos kurso.</span><span class="sxs-lookup"><span data-stu-id="781b1-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="781b1-170">Kad būtų užkirstas kelias ankstesniam scenarijui, rekomenduojame pakeisti šią parametro vertę nauju (švariu) mokesčių sudengimo laikotarpiu, kuriame nėra nesudengtų mokesčių operacijų.</span><span class="sxs-lookup"><span data-stu-id="781b1-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="781b1-171">Norėdami pakeisti šią vertę mokesčių sudengimo laikotarpio viduryje, prieš keisdami šio parametro reikšmę vykdykite dabartinio mokesčių sudengimo laikotarpio programą Sudengti ir registruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="781b1-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="781b1-172">Mokesčių sumos ataskaitų valiuta sekimas</span><span class="sxs-lookup"><span data-stu-id="781b1-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="781b1-173">Trys nauji laukai buvo įtraukti į su mokesčiais susijusias lenteles, kad būtų galima sekti sumas ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="781b1-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="781b1-174">Šie laukai yra lentelėse TAXUNCOMMITTED ir TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="781b1-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="781b1-175">TaxAmountRep: mokesčių suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="781b1-176">TaxBaseAmountRep: bazinė suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="781b1-177">TaxInCostPriceRep: neišskaitoma suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="781b1-178">Mokesčių, tik įrašytų lentelėje TAXUNCOMMITTED, bet dar neužregistruotų atveju sistema perskaičiuos mokesčių sumą ataskaitų valiuta, kai registruos, ir įrašys lentelėje TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="781b1-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="781b1-179">Šioje versijoje nėra pakeitimų, susijusių su ataskaitomis ir formomis, kuriose rodoma mokesčių suma ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="781b1-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="781b1-180">Ataskaitų ir formų pakeitimai bus pristatyti būsimose versijose.</span><span class="sxs-lookup"><span data-stu-id="781b1-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="781b1-181">Mokesčių sudengimo automatinis balansas ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="781b1-182">Jei mokesčių nustatymas yra nesubalansuotas ataskaitų valiutoje dėl tam tikrų priežasčių, tokių kaip prekybos mokesčių konveratvimo kelio „Apskaitos valiuta“ arba keitimo kurso pasikeitimo vieno mokesčio nustatymo laikotarpio metu, tuomet sistema automatiškai sukurs apskaitos įrašus, kad pakeistų mokesčio vertės pokyčius ir paleis juos pagal atliktų keitimų pelną ar nuostolius, kurie konfigūruojami mokesčių valiutos nustatyme.</span><span class="sxs-lookup"><span data-stu-id="781b1-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="781b1-183">Pagal ankstesnį pavyzdį šiai funkcijai pademonstruoti, įsivaizduokite, kad registravimo metu lentelėje TAXTRANS yra tokie duomenys.</span><span class="sxs-lookup"><span data-stu-id="781b1-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="781b1-184">PVM konvertavimo parametrai</span><span class="sxs-lookup"><span data-stu-id="781b1-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="781b1-185">Operacijos valiuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="781b1-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="781b1-186">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="781b1-186">Accounting currency (USD)</span></span> | <span data-ttu-id="781b1-187">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="781b1-188">Mokesčių valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="781b1-189">Apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-189">Accounting currency</span></span>             | <span data-ttu-id="781b1-190">100</span><span class="sxs-lookup"><span data-stu-id="781b1-190">100</span></span>                        | <span data-ttu-id="781b1-191">111</span><span class="sxs-lookup"><span data-stu-id="781b1-191">111</span></span>                       | <span data-ttu-id="781b1-192">83</span><span class="sxs-lookup"><span data-stu-id="781b1-192">83</span></span>                       | <span data-ttu-id="781b1-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="781b1-193">**83.25**</span></span>          |
| <span data-ttu-id="781b1-194">Ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-194">Reporting currency</span></span>              | <span data-ttu-id="781b1-195">100</span><span class="sxs-lookup"><span data-stu-id="781b1-195">100</span></span>                        | <span data-ttu-id="781b1-196">111</span><span class="sxs-lookup"><span data-stu-id="781b1-196">111</span></span>                       | <span data-ttu-id="781b1-197">83</span><span class="sxs-lookup"><span data-stu-id="781b1-197">83</span></span>                       | <span data-ttu-id="781b1-198">**83**</span><span class="sxs-lookup"><span data-stu-id="781b1-198">**83**</span></span>             |

<span data-ttu-id="781b1-199">Paleidus PVM sudengimo programą mėnesio pabaigoje, apskaitos įrašas bus toks:</span><span class="sxs-lookup"><span data-stu-id="781b1-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="781b1-200">Scenarijus: PVM konvertavimas = apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="781b1-201">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="781b1-201">Main account</span></span>           | <span data-ttu-id="781b1-202">Operacijos valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="781b1-203">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="781b1-203">Accounting currency (USD)</span></span> | <span data-ttu-id="781b1-204">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="781b1-205">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="781b1-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="781b1-206">-83,25</span><span class="sxs-lookup"><span data-stu-id="781b1-206">-83.25</span></span>                     | <span data-ttu-id="781b1-207">-111</span><span class="sxs-lookup"><span data-stu-id="781b1-207">-111</span></span>                      | <span data-ttu-id="781b1-208">-83,25</span><span class="sxs-lookup"><span data-stu-id="781b1-208">-83.25</span></span>                   |
| <span data-ttu-id="781b1-209">Mokesčio sudengimas</span><span class="sxs-lookup"><span data-stu-id="781b1-209">Tax Settlement</span></span>         | <span data-ttu-id="781b1-210">83.25</span><span class="sxs-lookup"><span data-stu-id="781b1-210">83.25</span></span>                      | <span data-ttu-id="781b1-211">111</span><span class="sxs-lookup"><span data-stu-id="781b1-211">111</span></span>                       | <span data-ttu-id="781b1-212">83.25</span><span class="sxs-lookup"><span data-stu-id="781b1-212">83.25</span></span>                    |
| <span data-ttu-id="781b1-213">Gautas pelnas / nuostolis</span><span class="sxs-lookup"><span data-stu-id="781b1-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="781b1-214">0</span><span class="sxs-lookup"><span data-stu-id="781b1-214">0</span></span>                          | <span data-ttu-id="781b1-215">0</span><span class="sxs-lookup"><span data-stu-id="781b1-215">0</span></span>                         | <span data-ttu-id="781b1-216">-0,25</span><span class="sxs-lookup"><span data-stu-id="781b1-216">-0.25</span></span>                    |
| <span data-ttu-id="781b1-217">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="781b1-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="781b1-218">0</span><span class="sxs-lookup"><span data-stu-id="781b1-218">0</span></span>                          | <span data-ttu-id="781b1-219">0</span><span class="sxs-lookup"><span data-stu-id="781b1-219">0</span></span>                         | <span data-ttu-id="781b1-220">0.25</span><span class="sxs-lookup"><span data-stu-id="781b1-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="781b1-221">Scenarijus: PVM konvertavimas = ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="781b1-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="781b1-222">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="781b1-222">Main account</span></span>           | <span data-ttu-id="781b1-223">Operacijos valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="781b1-224">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="781b1-224">Accounting currency (USD)</span></span> | <span data-ttu-id="781b1-225">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="781b1-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="781b1-226">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="781b1-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="781b1-227">-83</span><span class="sxs-lookup"><span data-stu-id="781b1-227">-83</span></span>                        | <span data-ttu-id="781b1-228">-110,67</span><span class="sxs-lookup"><span data-stu-id="781b1-228">-110.67</span></span>                   | <span data-ttu-id="781b1-229">-83</span><span class="sxs-lookup"><span data-stu-id="781b1-229">-83</span></span>                      |
| <span data-ttu-id="781b1-230">Mokesčio sudengimas</span><span class="sxs-lookup"><span data-stu-id="781b1-230">Tax Settlement</span></span>         | <span data-ttu-id="781b1-231">83</span><span class="sxs-lookup"><span data-stu-id="781b1-231">83</span></span>                         | <span data-ttu-id="781b1-232">110.67</span><span class="sxs-lookup"><span data-stu-id="781b1-232">110.67</span></span>                    | <span data-ttu-id="781b1-233">83</span><span class="sxs-lookup"><span data-stu-id="781b1-233">83</span></span>                       |
| <span data-ttu-id="781b1-234">Gautas pelnas / nuostolis</span><span class="sxs-lookup"><span data-stu-id="781b1-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="781b1-235">0</span><span class="sxs-lookup"><span data-stu-id="781b1-235">0</span></span>                          | <span data-ttu-id="781b1-236">0.33</span><span class="sxs-lookup"><span data-stu-id="781b1-236">0.33</span></span>                      | <span data-ttu-id="781b1-237">0</span><span class="sxs-lookup"><span data-stu-id="781b1-237">0</span></span>                        |
| <span data-ttu-id="781b1-238">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="781b1-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="781b1-239">0</span><span class="sxs-lookup"><span data-stu-id="781b1-239">0</span></span>                          | <span data-ttu-id="781b1-240">-0,33</span><span class="sxs-lookup"><span data-stu-id="781b1-240">-0.33</span></span>                     | <span data-ttu-id="781b1-241">0</span><span class="sxs-lookup"><span data-stu-id="781b1-241">0</span></span>                        |



<span data-ttu-id="781b1-242">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="781b1-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="781b1-243">Dvi valiutos</span><span class="sxs-lookup"><span data-stu-id="781b1-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="781b1-244">PVM apžvalga</span><span class="sxs-lookup"><span data-stu-id="781b1-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]