---
title: Palūkanų tarifų nustatymas palūkanų kodui
description: Delspinigių koduose yra parametrų, kurie nustato, kokie delspinigiai taikomi laiku neapmokėtoms sąskaitoms ir kaip jie apskaičiuojami.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62868c30d3ff60e51d99c71b743ab0bbb3c87451
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835201"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="63c97-103">Palūkanų tarifų nustatymas palūkanų kodui</span><span class="sxs-lookup"><span data-stu-id="63c97-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63c97-104">Delspinigių koduose yra parametrų, kurie nustato, kokie delspinigiai taikomi laiku neapmokėtoms sąskaitoms ir kaip jie apskaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="63c97-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="63c97-105">Galite nustatyti vieną delspinigių kodą ir jį taikyti keliems klientų registravimo šablonams, atsiskaitymo kodams arba konkrečioms SF eilutėms.</span><span class="sxs-lookup"><span data-stu-id="63c97-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="63c97-106">Pakeitus delspinigių kodo informaciją, visos kodą naudojančios funkcijos automatiškai pritaikys pakeitimus atliekant naujas operacijas.</span><span class="sxs-lookup"><span data-stu-id="63c97-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="63c97-107">Galite nustatyti dviejų rūšių delspinigių kodo tarifus:</span><span class="sxs-lookup"><span data-stu-id="63c97-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="63c97-108">Pajamų iš delspinigių tarifai − tai įplaukos, gaunamos taikant delspinigius SF arba delspinigių pažymoms.</span><span class="sxs-lookup"><span data-stu-id="63c97-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="63c97-109">Delspinigių mokėjimo tarifai − tai yra mokestis, mokamas už kredito pažymos delspinigius.</span><span class="sxs-lookup"><span data-stu-id="63c97-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="63c97-110">Abu šie tarifai gali būti vienu metu naudojami tame pačiame delspinigių kode.</span><span class="sxs-lookup"><span data-stu-id="63c97-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="63c97-111">Delspinigių tarifai gali būti grindžiami trimis skaičiavimo tipais:</span><span class="sxs-lookup"><span data-stu-id="63c97-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="63c97-112">Delspinigiai pagal procentus.</span><span class="sxs-lookup"><span data-stu-id="63c97-112">Interest by percentage.</span></span>
-   <span data-ttu-id="63c97-113">Delspinigiai pagal sumą.</span><span class="sxs-lookup"><span data-stu-id="63c97-113">Interest by amount.</span></span>
-   <span data-ttu-id="63c97-114">Delspinigiai pagal diapazoną, tada pateikiamas procentas arba suma.</span><span class="sxs-lookup"><span data-stu-id="63c97-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="63c97-115">Jei delspinigiams apskaičiuoti naudojamas delspinigių kodas, kiekvienam delspinigių tarifui, galiojančiam tuo metu, kai mokėjimas viršija operacijos atlikimo terminą, sukuriama atskira delspinigių pažyma.</span><span class="sxs-lookup"><span data-stu-id="63c97-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="63c97-116">**Pajamų** skirtukas, esantis **Delspinigių kodo** puslapyje, naudojamas nustatyti delspinigių, kuriuos gaunate juos nustatę, tarifams.</span><span class="sxs-lookup"><span data-stu-id="63c97-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="63c97-117">Naudokite **Mokėjimų** skirtuką, kad nustatytumėte mokamų delspinigių tarifus.</span><span class="sxs-lookup"><span data-stu-id="63c97-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="63c97-118">Delspinigių tarifai pagal procentą</span><span class="sxs-lookup"><span data-stu-id="63c97-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="63c97-119">Galite nustatyti delspinigių tarifus, kurie apskaičiuoja nurodytą procentą.</span><span class="sxs-lookup"><span data-stu-id="63c97-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="63c97-120">Delspinigių suma taikoma visoms valiutoms.</span><span class="sxs-lookup"><span data-stu-id="63c97-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="63c97-121">Galima įvesti pasirinktinius delspinigių sumos limitus.</span><span class="sxs-lookup"><span data-stu-id="63c97-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="63c97-122">Puslapio **Nustatyti delspinigių kodus** lauke **Skaičiuoti delspinigius pagal** pasirenkama  **Procentą**.</span><span class="sxs-lookup"><span data-stu-id="63c97-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="63c97-123">Pvz., norėdami nustatyti palūkanų kodą, kuris apskaičiuoja 5 proc. palūkanas už kiekvienus du mėnesius, kiek vėluojama apmokėti sąskaitą faktūrą, lauke **Skaičiuoti palūkanas kas** turėtumėte įvesti 2 ir pasirinkti **Mėn.**.</span><span class="sxs-lookup"><span data-stu-id="63c97-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="63c97-124">Naujas delspinigių pažymos apskaičiavimo algoritmas įtraukiamas naudojant funkcijų valdymą.</span><span class="sxs-lookup"><span data-stu-id="63c97-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="63c97-125">Norėdami naudoti šį algoritmą, įgalinkite funkciją **(GBL) Leisti apskaičiuoti dienines palūkanas metinį procentą padalijant iš 365**.</span><span class="sxs-lookup"><span data-stu-id="63c97-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="63c97-126">Daugiau informacijos apie tai, kaip įjungti funkciją, žr. temoje [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="63c97-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="63c97-127">Toliau pateikta delspinigių pažymos sumos apskaičiavimo formulė.</span><span class="sxs-lookup"><span data-stu-id="63c97-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="63c97-128">Delspinigių pažymos suma = Pasiskolinta suma \* Metinės palūkanos % / 365 \* Vėlavimo dienų skaičius</span><span class="sxs-lookup"><span data-stu-id="63c97-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="63c97-129">Ši funkcija pasiekiama 10.0.18 arba vėlesnėje versijoje.</span><span class="sxs-lookup"><span data-stu-id="63c97-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="63c97-130">Delspinigių tarifai pagal sumas</span><span class="sxs-lookup"><span data-stu-id="63c97-130">Interest rates based on amounts</span></span>
<span data-ttu-id="63c97-131">Galite nustatyti delspinigių tarifus, kurie apskaičiuoja nurodytą sumą pagal valiutą.</span><span class="sxs-lookup"><span data-stu-id="63c97-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="63c97-132">Delspinigių kode nurodoma kiekvienos valiutos delspinigių suma.</span><span class="sxs-lookup"><span data-stu-id="63c97-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="63c97-133">Galima įvesti pasirinktinius delspinigių sumos limitus.</span><span class="sxs-lookup"><span data-stu-id="63c97-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="63c97-134">Puslapio **Nustatyti delspinigių kodus** lauke **Skaičiuoti delspinigius pagal** pasirenkama **Sumą**.</span><span class="sxs-lookup"><span data-stu-id="63c97-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="63c97-135">Pvz., norėdami nustatyti palūkanų kodą, kuris apskaičiuoja 25,00 dydžio palūkanas už kiekvienas 20 dienų, kiek vėluojama apmokėti sąskaitą faktūrą, lauke **Skaičiuoti palūkanas kas** turėtumėte įvesti 20 ir pasirinkti **Dien.**.</span><span class="sxs-lookup"><span data-stu-id="63c97-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="63c97-136">Delspinigių tarifai pagal diapazonus</span><span class="sxs-lookup"><span data-stu-id="63c97-136">Interest rates based on ranges</span></span>
<span data-ttu-id="63c97-137">Galite nustatyti delspinigių tarifus, kurie skiriasi atsižvelgiant į pradelstą sumą, pradelstų dienų skaičių arba mėnesių skaičių.</span><span class="sxs-lookup"><span data-stu-id="63c97-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="63c97-138">Norėdami apibrėžti konkrečias kiekvienos valiutos delspinigių nuostatas, galite naudoti skirtuką **Pajamos pagal valiutą**.</span><span class="sxs-lookup"><span data-stu-id="63c97-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="63c97-139">Čia taip pat apibrėšite diapazoną.</span><span class="sxs-lookup"><span data-stu-id="63c97-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="63c97-140">Naudokite **Diapazonų** mygtuką, kad pridėtumėte eilutes, atstojančias norimus nustatyti diapazonus.</span><span class="sxs-lookup"><span data-stu-id="63c97-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="63c97-141">Reikšmė **Nuo** nurodo diapazono pradžią, o **Delspinigių vertės** skaičius nurodo arba procentą, arba sumą – tai priklauso nuo pasirinkties lauke **Skaičiuoti delspinigius pagal**, esančiame puslapyje **Nustatyti delspinigių kodus**.</span><span class="sxs-lookup"><span data-stu-id="63c97-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="63c97-142">1 pavyzdys: delspinigiai pagal diapazoną = suma</span><span class="sxs-lookup"><span data-stu-id="63c97-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="63c97-143">Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas tris mėnesius, kiek vėluojama apmokėti SF.</span><span class="sxs-lookup"><span data-stu-id="63c97-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="63c97-144">Norite skaičiuoti delspinigius pagal procentinę delspinigių vertę, pakopiniais sumos intervalais.</span><span class="sxs-lookup"><span data-stu-id="63c97-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="63c97-145">Delspinigių vertė bus 1 proc. už SF sumas, neviršijančias 1 000,00, 2 proc. už sumas nuo 1 001,00 iki 5 000,00 ir 3 proc. už sumas, viršijančias 5 000,00 sumas.</span><span class="sxs-lookup"><span data-stu-id="63c97-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="63c97-146">Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="63c97-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="63c97-147">**Lauko pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="63c97-147">**Field name**</span></span>                  | <span data-ttu-id="63c97-148">**Lauko vertė**</span><span class="sxs-lookup"><span data-stu-id="63c97-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="63c97-149">**Palūkanų kodas**</span><span class="sxs-lookup"><span data-stu-id="63c97-149">**Interest code**</span></span>               | <span data-ttu-id="63c97-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="63c97-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="63c97-151">**Apskaičiuoti palūkanas kas**</span><span class="sxs-lookup"><span data-stu-id="63c97-151">**Calculate interest every**</span></span>    | <span data-ttu-id="63c97-152">3/mėn.</span><span class="sxs-lookup"><span data-stu-id="63c97-152">3/Month</span></span>         |
| <span data-ttu-id="63c97-153">**Palūkanos pagal diapazoną**</span><span class="sxs-lookup"><span data-stu-id="63c97-153">**Interest by range**</span></span>           | <span data-ttu-id="63c97-154">Suma</span><span class="sxs-lookup"><span data-stu-id="63c97-154">Amount</span></span>          |
| <span data-ttu-id="63c97-155">**Skaičiuoti palūkanas pagal**</span><span class="sxs-lookup"><span data-stu-id="63c97-155">**Calculate interest based on**</span></span> | <span data-ttu-id="63c97-156">Procentai</span><span class="sxs-lookup"><span data-stu-id="63c97-156">Percentage</span></span>      |

<span data-ttu-id="63c97-157">Galite nustatyti diapazono informaciją, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="63c97-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="63c97-158">**Vertė Nuo**</span><span class="sxs-lookup"><span data-stu-id="63c97-158">**From value**</span></span> | <span data-ttu-id="63c97-159">**Palūkanų vertė**</span><span class="sxs-lookup"><span data-stu-id="63c97-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="63c97-160">0</span><span class="sxs-lookup"><span data-stu-id="63c97-160">0</span></span>              | <span data-ttu-id="63c97-161">1</span><span class="sxs-lookup"><span data-stu-id="63c97-161">1</span></span>                  |
| <span data-ttu-id="63c97-162">1,001</span><span class="sxs-lookup"><span data-stu-id="63c97-162">1,001</span></span>          | <span data-ttu-id="63c97-163">2</span><span class="sxs-lookup"><span data-stu-id="63c97-163">2</span></span>                  |
| <span data-ttu-id="63c97-164">5,001</span><span class="sxs-lookup"><span data-stu-id="63c97-164">5,001</span></span>          | <span data-ttu-id="63c97-165">3</span><span class="sxs-lookup"><span data-stu-id="63c97-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="63c97-166">2 pavyzdys: delspinigiai pagal diapazoną = dienos</span><span class="sxs-lookup"><span data-stu-id="63c97-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="63c97-167">Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas 15 dienų, kiek vėluojama apmokėti SF.</span><span class="sxs-lookup"><span data-stu-id="63c97-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="63c97-168">Norite skaičiuoti delspinigius pagal sumos delspinigių vertę, pakopiniais dienos intervalais.</span><span class="sxs-lookup"><span data-stu-id="63c97-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="63c97-169">Delspinigių vertė bus 10,00 už 15 dienų pirmąsias 60 dienų, 15,00 už 15 dienų, kai vėluojama 61–90 d., ir 20,00 už 15 dienų, kai vėluojama daugiau nei 91 d.</span><span class="sxs-lookup"><span data-stu-id="63c97-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="63c97-170">Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="63c97-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="63c97-171">**Lauko pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="63c97-171">**Field name**</span></span>                  | <span data-ttu-id="63c97-172">**Lauko vertė**</span><span class="sxs-lookup"><span data-stu-id="63c97-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="63c97-173">**Palūkanų kodas**</span><span class="sxs-lookup"><span data-stu-id="63c97-173">**Interest code**</span></span>               | <span data-ttu-id="63c97-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="63c97-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="63c97-175">**Apskaičiuoti palūkanas kas**</span><span class="sxs-lookup"><span data-stu-id="63c97-175">**Calculate interest every**</span></span>    | <span data-ttu-id="63c97-176">15/dien.</span><span class="sxs-lookup"><span data-stu-id="63c97-176">15/Day</span></span>          |
| <span data-ttu-id="63c97-177">**Palūkanos pagal diapazoną**</span><span class="sxs-lookup"><span data-stu-id="63c97-177">**Interest by range**</span></span>           | <span data-ttu-id="63c97-178">Dienos</span><span class="sxs-lookup"><span data-stu-id="63c97-178">Days</span></span>            |
| <span data-ttu-id="63c97-179">**Skaičiuoti palūkanas pagal**</span><span class="sxs-lookup"><span data-stu-id="63c97-179">**Calculate interest based on**</span></span> | <span data-ttu-id="63c97-180">Suma</span><span class="sxs-lookup"><span data-stu-id="63c97-180">Amount</span></span>          |

<span data-ttu-id="63c97-181">Galite nustatyti diapazono informaciją, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="63c97-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="63c97-182">**Vertė Nuo**</span><span class="sxs-lookup"><span data-stu-id="63c97-182">**From value**</span></span> | <span data-ttu-id="63c97-183">**Palūkanų vertė**</span><span class="sxs-lookup"><span data-stu-id="63c97-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="63c97-184">0</span><span class="sxs-lookup"><span data-stu-id="63c97-184">0</span></span>              | <span data-ttu-id="63c97-185">10</span><span class="sxs-lookup"><span data-stu-id="63c97-185">10</span></span>                 |
| <span data-ttu-id="63c97-186">61</span><span class="sxs-lookup"><span data-stu-id="63c97-186">61</span></span>             | <span data-ttu-id="63c97-187">15</span><span class="sxs-lookup"><span data-stu-id="63c97-187">15</span></span>                 |
| <span data-ttu-id="63c97-188">91</span><span class="sxs-lookup"><span data-stu-id="63c97-188">91</span></span>             | <span data-ttu-id="63c97-189">20</span><span class="sxs-lookup"><span data-stu-id="63c97-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="63c97-190">3 pavyzdys: delspinigiai pagal diapazoną = mėnesiai</span><span class="sxs-lookup"><span data-stu-id="63c97-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="63c97-191">Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas mėnesį, kiek vėluojama apmokėti SF.</span><span class="sxs-lookup"><span data-stu-id="63c97-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="63c97-192">Norite skaičiuoti delspinigius pagal procentinę delspinigių vertę, pakopiniais mėnesio intervalais.</span><span class="sxs-lookup"><span data-stu-id="63c97-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="63c97-193">Delspinigių vertė bus 1,5 proc. už mėnesį pirmuosius tris mėnesius, kiek vėluojama sumokėti, 2,0 proc. už mėnesį už kitus tris mėnesius, 2,5 proc. už kiekvieną paskesnį mėnesį (kai vėluojama daugiau nei 6 mėnesius).</span><span class="sxs-lookup"><span data-stu-id="63c97-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="63c97-194">Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="63c97-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="63c97-195">**Lauko pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="63c97-195">**Field name**</span></span>                  | <span data-ttu-id="63c97-196">**Lauko vertė**</span><span class="sxs-lookup"><span data-stu-id="63c97-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="63c97-197">**Palūkanų kodas**</span><span class="sxs-lookup"><span data-stu-id="63c97-197">**Interest code**</span></span>               | <span data-ttu-id="63c97-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="63c97-198">1M%ByMth</span></span>        |
| <span data-ttu-id="63c97-199">**Apskaičiuoti palūkanas kas**</span><span class="sxs-lookup"><span data-stu-id="63c97-199">**Calculate interest every**</span></span>    | <span data-ttu-id="63c97-200">1 / Mėn.</span><span class="sxs-lookup"><span data-stu-id="63c97-200">1/Month</span></span>         |
| <span data-ttu-id="63c97-201">**Palūkanos pagal diapazoną**</span><span class="sxs-lookup"><span data-stu-id="63c97-201">**Interest by range**</span></span>           | <span data-ttu-id="63c97-202">Mėnesiai</span><span class="sxs-lookup"><span data-stu-id="63c97-202">Months</span></span>          |
| <span data-ttu-id="63c97-203">**Skaičiuoti palūkanas pagal**</span><span class="sxs-lookup"><span data-stu-id="63c97-203">**Calculate interest based on**</span></span> | <span data-ttu-id="63c97-204">Procentai</span><span class="sxs-lookup"><span data-stu-id="63c97-204">Percentage</span></span>      |

<span data-ttu-id="63c97-205">Galite nustatyti diapazono informaciją, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="63c97-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="63c97-206">**Vertė Nuo**</span><span class="sxs-lookup"><span data-stu-id="63c97-206">**From value**</span></span> | <span data-ttu-id="63c97-207">**Palūkanų vertė**</span><span class="sxs-lookup"><span data-stu-id="63c97-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="63c97-208">0</span><span class="sxs-lookup"><span data-stu-id="63c97-208">0</span></span>              | <span data-ttu-id="63c97-209">1.5</span><span class="sxs-lookup"><span data-stu-id="63c97-209">1.5</span></span>                |
| <span data-ttu-id="63c97-210">4</span><span class="sxs-lookup"><span data-stu-id="63c97-210">4</span></span>              | <span data-ttu-id="63c97-211">2</span><span class="sxs-lookup"><span data-stu-id="63c97-211">2</span></span>                  |
| <span data-ttu-id="63c97-212">7</span><span class="sxs-lookup"><span data-stu-id="63c97-212">7</span></span>              | <span data-ttu-id="63c97-213">2,5</span><span class="sxs-lookup"><span data-stu-id="63c97-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="63c97-214">Naujos versijos</span><span class="sxs-lookup"><span data-stu-id="63c97-214">New versions</span></span>
<span data-ttu-id="63c97-215">Delspinigių kodai turi galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="63c97-215">Interest codes are date effective.</span></span> <span data-ttu-id="63c97-216">Jei norite modifikuoti delspinigių tarifą, galite sukurti **naują versiją**, kuri galiotų nuo būsimos datos.</span><span class="sxs-lookup"><span data-stu-id="63c97-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="63c97-217">Norėdami peržiūrėti skirtingas versijas, galite naudoti meniu pasirinktį **Taikymo pradžios data** ir pasirinkti galutinę datą.</span><span class="sxs-lookup"><span data-stu-id="63c97-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="63c97-218">Taip pat galite pasirinkti **Rodyti visus įrašus**, kad puslapyje matytumėte visus delspinigių kodus.</span><span class="sxs-lookup"><span data-stu-id="63c97-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
