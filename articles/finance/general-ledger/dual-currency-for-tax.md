---
title: Mokesčiuose dviejų valiutų palaikymas
description: Šioje temoje paaiškinama, kaip išplėsti dviejų valiutų apskaitos funkciją mokesčių srityje, ir nurodoma, koks gali būti poveikis mokesčiams apskaičiuoti ir registruoti
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 1ba4d09240888f0c533fb07614e75ffecea0742c
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124098"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="f3ed8-103">PVM dviejų valiutų palaikymas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3ed8-104">Šioje temoje paaiškinama, kaip išplėsti dviejų valiutų apskaitos funkciją PVM srityje, ir nurodoma, koks gali būti poveikis PVM apskaičiuoti, registruoti ir sudengti.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="f3ed8-105">„Dynamics 365 Finance“ dviejų valiutų funkcija atsirado 8.1 versijoje (2018 m. spalio mėn.).</span><span class="sxs-lookup"><span data-stu-id="f3ed8-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="f3ed8-106">Ji pakeitė, kaip apskaičiuojami apskaitos įrašai ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="f3ed8-107">Ankstesnėse versijose operacijos buvo konvertuojamos į ataskaitų valiutą tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="f3ed8-108">Operacijos suma buvo apskaičiuota operacijos valiuta > operacijos suma buvo konvertuota į apskaitos valiutą > apskaitos valiutos suma buvo konvertuota į ataskaitų valiutą</span><span class="sxs-lookup"><span data-stu-id="f3ed8-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="f3ed8-109">Įjungus dviejų valiutų funkciją, operacijos buvo konvertuotos į ataskaitų valiutą tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="f3ed8-110">Suma operacijos valiuta > Suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="f3ed8-111">Daugiau informacijos apie dviejų valiutų funkciją rasite [Dvi valiutos](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="f3ed8-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="f3ed8-112">Dėl dviejų valiutų palaikymo funkcijų valdyme atsirado dvi naujos funkcijos:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="f3ed8-113">PVM konvertavimas (10.0.9 versijoje)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="f3ed8-114">Mokesčių sudengimo automatinis balansas ataskaitų valiuta (10.0.11 versijoje)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="f3ed8-115">Dviejų valiutų palaikymas PVM srityje užtikrina, kad mokesčiai bus tiksliai apskaičiuoti mokesčių valiuta ir kad PVM sudengimo balansas bus apskaičiuotas tiksliai ir apskaitos valiuta, ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="f3ed8-116">Šiuo metu veikia naujos klientų asmeninės peržiūros funkcijos.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="f3ed8-117">Norėdami įgalinti funkcijas, per atitinkamą kanalą „Microsoft“ pateikite aptarnavimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="f3ed8-118">PVM konvertavimas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-118">Sales tax conversion</span></span>

<span data-ttu-id="f3ed8-119">Parametras **PVM konvertavimas** suteikia dvi parinktis, kaip galima konvertuoti mokesčių sumą iš operacijos valiutos į mokesčių valiutą.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="f3ed8-120">Apskaitos valiuta: kelias: Suma operacijos valiuta > Suma apskaitos valiuta > Suma mokesčių valiuta.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="f3ed8-121">Valiutos konvertavimui bus naudojamas apskaitos valiutos kurso tipas (sukonfigūruotas DK sąrankoje).</span><span class="sxs-lookup"><span data-stu-id="f3ed8-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="f3ed8-122">Ataskaitų valiuta: kelias: Suma operacijos valiuta > Suma ataskaitų valiuta > Suma mokesčių valiuta.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="f3ed8-123">Valiutos konvertavimui bus naudojamas ataskaitų valiutos kurso tipas (sukonfigūruotas DK sąrankoje).</span><span class="sxs-lookup"><span data-stu-id="f3ed8-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="f3ed8-124">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f3ed8-124">Example</span></span>

<span data-ttu-id="f3ed8-125">Paprastas pavyzdys, skirtas šiai funkcijai pademonstruoti:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="f3ed8-126">DK ir mokesčių valiutos nustatymas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="f3ed8-127">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-127">Transaction currency</span></span> | <span data-ttu-id="f3ed8-128">Apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-128">Accounting currency</span></span> | <span data-ttu-id="f3ed8-129">Ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-129">Reporting currency</span></span> | <span data-ttu-id="f3ed8-130">Mokesčių valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="f3ed8-131">EUR</span><span class="sxs-lookup"><span data-stu-id="f3ed8-131">EUR</span></span>                  | <span data-ttu-id="f3ed8-132">USD</span><span class="sxs-lookup"><span data-stu-id="f3ed8-132">USD</span></span>                 | <span data-ttu-id="f3ed8-133">LT</span><span class="sxs-lookup"><span data-stu-id="f3ed8-133">GBP</span></span>                | <span data-ttu-id="f3ed8-134">LT</span><span class="sxs-lookup"><span data-stu-id="f3ed8-134">GBP</span></span>          |

<span data-ttu-id="f3ed8-135">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-135">Exchange rate</span></span>

| <span data-ttu-id="f3ed8-136">Iš valiutos</span><span class="sxs-lookup"><span data-stu-id="f3ed8-136">From currency</span></span> | <span data-ttu-id="f3ed8-137">Į valiutą</span><span class="sxs-lookup"><span data-stu-id="f3ed8-137">To currency</span></span> | <span data-ttu-id="f3ed8-138">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-138">Factor</span></span> | <span data-ttu-id="f3ed8-139">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="f3ed8-140">EUR</span><span class="sxs-lookup"><span data-stu-id="f3ed8-140">EUR</span></span>           | <span data-ttu-id="f3ed8-141">USD</span><span class="sxs-lookup"><span data-stu-id="f3ed8-141">USD</span></span>         | <span data-ttu-id="f3ed8-142">1</span><span class="sxs-lookup"><span data-stu-id="f3ed8-142">1</span></span>      | <span data-ttu-id="f3ed8-143">1.11</span><span class="sxs-lookup"><span data-stu-id="f3ed8-143">1.11</span></span>          |
| <span data-ttu-id="f3ed8-144">EUR</span><span class="sxs-lookup"><span data-stu-id="f3ed8-144">EUR</span></span>           | <span data-ttu-id="f3ed8-145">LT</span><span class="sxs-lookup"><span data-stu-id="f3ed8-145">GBP</span></span>         | <span data-ttu-id="f3ed8-146">1</span><span class="sxs-lookup"><span data-stu-id="f3ed8-146">1</span></span>      | <span data-ttu-id="f3ed8-147">0.83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-147">0.83</span></span>          |
| <span data-ttu-id="f3ed8-148">USD</span><span class="sxs-lookup"><span data-stu-id="f3ed8-148">USD</span></span>           | <span data-ttu-id="f3ed8-149">LT</span><span class="sxs-lookup"><span data-stu-id="f3ed8-149">GBP</span></span>         | <span data-ttu-id="f3ed8-150">1</span><span class="sxs-lookup"><span data-stu-id="f3ed8-150">1</span></span>      | <span data-ttu-id="f3ed8-151">0.75</span><span class="sxs-lookup"><span data-stu-id="f3ed8-151">0.75</span></span>          |

<span data-ttu-id="f3ed8-152">Mokesčio sumos skaičiavimas naudojant skirtingas parametro parinktis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="f3ed8-153">Mokesčio suma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="f3ed8-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="f3ed8-154">PVM konvertavimo parametrai</span><span class="sxs-lookup"><span data-stu-id="f3ed8-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="f3ed8-155">Operacijos valiuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="f3ed8-156">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-156">Accounting currency (USD)</span></span> | <span data-ttu-id="f3ed8-157">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="f3ed8-158">Mokesčių valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="f3ed8-159">Apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-159">Accounting currency</span></span>             | <span data-ttu-id="f3ed8-160">100</span><span class="sxs-lookup"><span data-stu-id="f3ed8-160">100</span></span>                        | <span data-ttu-id="f3ed8-161">111</span><span class="sxs-lookup"><span data-stu-id="f3ed8-161">111</span></span>                       | <span data-ttu-id="f3ed8-162">83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-162">83</span></span>                       | <span data-ttu-id="f3ed8-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-163">**83.25**</span></span>          |
| <span data-ttu-id="f3ed8-164">Ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-164">Reporting currency</span></span>              | <span data-ttu-id="f3ed8-165">100</span><span class="sxs-lookup"><span data-stu-id="f3ed8-165">100</span></span>                        | <span data-ttu-id="f3ed8-166">111</span><span class="sxs-lookup"><span data-stu-id="f3ed8-166">111</span></span>                       | <span data-ttu-id="f3ed8-167">83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-167">83</span></span>                       | <span data-ttu-id="f3ed8-168">**83**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-168">**83**</span></span>             |

<span data-ttu-id="f3ed8-169">Šis parametras gali būti sukonfigūruotas, atsižvelgiant į tai, ko reikalauja mokesčių inspekcija.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="f3ed8-170">Atnaujinimo aplinkybės</span><span class="sxs-lookup"><span data-stu-id="f3ed8-170">Upgrade Consideration</span></span>

<span data-ttu-id="f3ed8-171">Ši funkcija bus taikoma tik naujoms operacijoms.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="f3ed8-172">Mokesčių operacijai, kuri jau įrašyta TAXTRANS lentelėje, bet dar nėra sudengta, sistema neperskaičiuos mokesčių sumos mokesčių valiuta, nes registruojant mokestį nėra valiutos kurso.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="f3ed8-173">Kad būtų užkirstas kelias ankstesniam scenarijui, rekomenduojame pakeisti šią parametro vertę nauju (švariu) mokesčių sudengimo laikotarpiu, kuriame nėra nesudengtų mokesčių operacijų.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="f3ed8-174">Norėdami pakeisti šią vertę mokesčių sudengimo laikotarpio viduryje, prieš keisdami šio parametro reikšmę vykdykite dabartinio mokesčių sudengimo laikotarpio programą Sudengti ir registruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="f3ed8-175">Mokesčių sumos ataskaitų valiuta sekimas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="f3ed8-176">Trys nauji laukai buvo įtraukti į su mokesčiais susijusias lenteles, kad būtų galima sekti sumas ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="f3ed8-177">Šie laukai yra lentelėse TAXUNCOMMITTED ir TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="f3ed8-178">TaxAmountRep: mokesčių suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="f3ed8-179">TaxBaseAmountRep: bazinė suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="f3ed8-180">TaxInCostPriceRep: neišskaitoma suma ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="f3ed8-181">Mokesčių, tik įrašytų lentelėje TAXUNCOMMITTED, bet dar neužregistruotų atveju sistema perskaičiuos mokesčių sumą ataskaitų valiuta, kai registruos, ir įrašys lentelėje TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="f3ed8-182">Šioje versijoje nėra pakeitimų, susijusių su ataskaitomis ir formomis, kuriose rodoma mokesčių suma ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="f3ed8-183">Ataskaitų ir formų pakeitimai bus pristatyti būsimose versijose.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="f3ed8-184">Mokesčių sudengimo automatinis balansas ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="f3ed8-185">Jei mokesčių sudengimas nėra subalansuotas ataskaitų valiuta dėl tam tikrų priežasčių, pvz., PVM konvertavimo kelias yra Apskaitos valiuta, arba valiutos kursas pasikeitė vieno mokesčio sudengimo laikotarpiu, sistema automatiškai sugeneruos apskaitos įrašus, kad būtų galima koreguoti mokesčio sumos nuokrypį ir kompensuoti jį pagal gautą pelną / nuostolį, kuris sukonfigūruotas DK sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="f3ed8-186">Pagal ankstesnį pavyzdį šiai funkcijai pademonstruoti, įsivaizduokite, kad registravimo metu lentelėje TAXTRANS yra tokie duomenys.</span><span class="sxs-lookup"><span data-stu-id="f3ed8-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="f3ed8-187">PVM konvertavimo parametrai</span><span class="sxs-lookup"><span data-stu-id="f3ed8-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="f3ed8-188">Operacijos valiuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="f3ed8-189">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-189">Accounting currency (USD)</span></span> | <span data-ttu-id="f3ed8-190">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="f3ed8-191">Mokesčių valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="f3ed8-192">Apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-192">Accounting currency</span></span>             | <span data-ttu-id="f3ed8-193">100</span><span class="sxs-lookup"><span data-stu-id="f3ed8-193">100</span></span>                        | <span data-ttu-id="f3ed8-194">111</span><span class="sxs-lookup"><span data-stu-id="f3ed8-194">111</span></span>                       | <span data-ttu-id="f3ed8-195">83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-195">83</span></span>                       | <span data-ttu-id="f3ed8-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-196">**83.25**</span></span>          |
| <span data-ttu-id="f3ed8-197">Ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-197">Reporting currency</span></span>              | <span data-ttu-id="f3ed8-198">100</span><span class="sxs-lookup"><span data-stu-id="f3ed8-198">100</span></span>                        | <span data-ttu-id="f3ed8-199">111</span><span class="sxs-lookup"><span data-stu-id="f3ed8-199">111</span></span>                       | <span data-ttu-id="f3ed8-200">83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-200">83</span></span>                       | <span data-ttu-id="f3ed8-201">**83**</span><span class="sxs-lookup"><span data-stu-id="f3ed8-201">**83**</span></span>             |

<span data-ttu-id="f3ed8-202">Paleidus PVM sudengimo programą mėnesio pabaigoje, apskaitos įrašas bus toks:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="f3ed8-203">Scenarijus: PVM konvertavimas = apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="f3ed8-204">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="f3ed8-204">Main account</span></span>           | <span data-ttu-id="f3ed8-205">Operacijos valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="f3ed8-206">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-206">Accounting currency (USD)</span></span> | <span data-ttu-id="f3ed8-207">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="f3ed8-208">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="f3ed8-209">-83,25</span><span class="sxs-lookup"><span data-stu-id="f3ed8-209">-83.25</span></span>                     | <span data-ttu-id="f3ed8-210">-111</span><span class="sxs-lookup"><span data-stu-id="f3ed8-210">-111</span></span>                      | <span data-ttu-id="f3ed8-211">-83,25</span><span class="sxs-lookup"><span data-stu-id="f3ed8-211">-83.25</span></span>                   |
| <span data-ttu-id="f3ed8-212">Mokesčio sudengimas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-212">Tax Settlement</span></span>         | <span data-ttu-id="f3ed8-213">83.25</span><span class="sxs-lookup"><span data-stu-id="f3ed8-213">83.25</span></span>                      | <span data-ttu-id="f3ed8-214">111</span><span class="sxs-lookup"><span data-stu-id="f3ed8-214">111</span></span>                       | <span data-ttu-id="f3ed8-215">83.25</span><span class="sxs-lookup"><span data-stu-id="f3ed8-215">83.25</span></span>                    |
| <span data-ttu-id="f3ed8-216">Gautas pelnas / nuostolis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="f3ed8-217">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-217">0</span></span>                          | <span data-ttu-id="f3ed8-218">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-218">0</span></span>                         | <span data-ttu-id="f3ed8-219">-0,25</span><span class="sxs-lookup"><span data-stu-id="f3ed8-219">-0.25</span></span>                    |
| <span data-ttu-id="f3ed8-220">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="f3ed8-221">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-221">0</span></span>                          | <span data-ttu-id="f3ed8-222">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-222">0</span></span>                         | <span data-ttu-id="f3ed8-223">0.25</span><span class="sxs-lookup"><span data-stu-id="f3ed8-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="f3ed8-224">Scenarijus: PVM konvertavimas = ataskaitų valiuta</span><span class="sxs-lookup"><span data-stu-id="f3ed8-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="f3ed8-225">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="f3ed8-225">Main account</span></span>           | <span data-ttu-id="f3ed8-226">Operacijos valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="f3ed8-227">Apskaitos valiuta (USD)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-227">Accounting currency (USD)</span></span> | <span data-ttu-id="f3ed8-228">Ataskaitų valiuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="f3ed8-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="f3ed8-229">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="f3ed8-230">-83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-230">-83</span></span>                        | <span data-ttu-id="f3ed8-231">-110,67</span><span class="sxs-lookup"><span data-stu-id="f3ed8-231">-110.67</span></span>                   | <span data-ttu-id="f3ed8-232">-83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-232">-83</span></span>                      |
| <span data-ttu-id="f3ed8-233">Mokesčio sudengimas</span><span class="sxs-lookup"><span data-stu-id="f3ed8-233">Tax Settlement</span></span>         | <span data-ttu-id="f3ed8-234">83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-234">83</span></span>                         | <span data-ttu-id="f3ed8-235">110.67</span><span class="sxs-lookup"><span data-stu-id="f3ed8-235">110.67</span></span>                    | <span data-ttu-id="f3ed8-236">83</span><span class="sxs-lookup"><span data-stu-id="f3ed8-236">83</span></span>                       |
| <span data-ttu-id="f3ed8-237">Gautas pelnas / nuostolis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="f3ed8-238">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-238">0</span></span>                          | <span data-ttu-id="f3ed8-239">0.33</span><span class="sxs-lookup"><span data-stu-id="f3ed8-239">0.33</span></span>                      | <span data-ttu-id="f3ed8-240">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-240">0</span></span>                        |
| <span data-ttu-id="f3ed8-241">Mokėtinas / susigrąžinamas mokestis</span><span class="sxs-lookup"><span data-stu-id="f3ed8-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="f3ed8-242">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-242">0</span></span>                          | <span data-ttu-id="f3ed8-243">-0,33</span><span class="sxs-lookup"><span data-stu-id="f3ed8-243">-0.33</span></span>                     | <span data-ttu-id="f3ed8-244">0</span><span class="sxs-lookup"><span data-stu-id="f3ed8-244">0</span></span>                        |



<span data-ttu-id="f3ed8-245">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="f3ed8-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f3ed8-246">Dvi valiutos</span><span class="sxs-lookup"><span data-stu-id="f3ed8-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="f3ed8-247">PVM apžvalga</span><span class="sxs-lookup"><span data-stu-id="f3ed8-247">Sales tax overview</span></span>](indirect-taxes-overview.md)
