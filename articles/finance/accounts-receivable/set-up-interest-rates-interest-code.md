---
title: Palūkanų tarifų nustatymas palūkanų kodui
description: Delspinigių koduose yra parametrų, kurie nustato, kokie delspinigiai taikomi laiku neapmokėtoms sąskaitoms ir kaip jie apskaičiuojami.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188998"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="ee546-103">Palūkanų tarifų nustatymas palūkanų kodui</span><span class="sxs-lookup"><span data-stu-id="ee546-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee546-104">Delspinigių koduose yra parametrų, kurie nustato, kokie delspinigiai taikomi laiku neapmokėtoms sąskaitoms ir kaip jie apskaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="ee546-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="ee546-105">Galite nustatyti vieną delspinigių kodą ir jį taikyti keliems klientų registravimo šablonams, atsiskaitymo kodams arba konkrečioms SF eilutėms.</span><span class="sxs-lookup"><span data-stu-id="ee546-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="ee546-106">Pakeitus delspinigių kodo informaciją, visos kodą naudojančios funkcijos automatiškai pritaikys pakeitimus atliekant naujas operacijas.</span><span class="sxs-lookup"><span data-stu-id="ee546-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="ee546-107">Galite nustatyti dviejų rūšių delspinigių kodo tarifus:</span><span class="sxs-lookup"><span data-stu-id="ee546-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="ee546-108">Pajamų iš delspinigių tarifai − tai įplaukos, gaunamos taikant delspinigius SF arba delspinigių pažymoms.</span><span class="sxs-lookup"><span data-stu-id="ee546-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="ee546-109">Delspinigių mokėjimo tarifai − tai yra mokestis, mokamas už kredito pažymos delspinigius.</span><span class="sxs-lookup"><span data-stu-id="ee546-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="ee546-110">Abu šie tarifai gali būti vienu metu naudojami tame pačiame delspinigių kode.</span><span class="sxs-lookup"><span data-stu-id="ee546-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="ee546-111">Delspinigių tarifai gali būti grindžiami trimis skaičiavimo tipais:</span><span class="sxs-lookup"><span data-stu-id="ee546-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="ee546-112">Delspinigiai pagal procentus.</span><span class="sxs-lookup"><span data-stu-id="ee546-112">Interest by percentage.</span></span>
-   <span data-ttu-id="ee546-113">Delspinigiai pagal sumą.</span><span class="sxs-lookup"><span data-stu-id="ee546-113">Interest by amount.</span></span>
-   <span data-ttu-id="ee546-114">Delspinigiai pagal diapazoną, tada pateikiamas procentas arba suma.</span><span class="sxs-lookup"><span data-stu-id="ee546-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="ee546-115">Jei delspinigiams apskaičiuoti naudojamas delspinigių kodas, kiekvienam delspinigių tarifui, galiojančiam tuo metu, kai mokėjimas viršija operacijos atlikimo terminą, sukuriama atskira delspinigių pažyma.</span><span class="sxs-lookup"><span data-stu-id="ee546-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="ee546-116">**Pajamų** skirtukas, esantis **Delspinigių kodo** puslapyje, naudojamas nustatyti delspinigių, kuriuos gaunate juos nustatę, tarifams.</span><span class="sxs-lookup"><span data-stu-id="ee546-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="ee546-117">Naudokite **Mokėjimų** skirtuką, kad nustatytumėte mokamų delspinigių tarifus.</span><span class="sxs-lookup"><span data-stu-id="ee546-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="ee546-118">Delspinigių tarifai pagal procentą</span><span class="sxs-lookup"><span data-stu-id="ee546-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="ee546-119">Galite nustatyti delspinigių tarifus, kurie apskaičiuoja nurodytą procentą.</span><span class="sxs-lookup"><span data-stu-id="ee546-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="ee546-120">Delspinigių suma taikoma visoms valiutoms.</span><span class="sxs-lookup"><span data-stu-id="ee546-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="ee546-121">Galima įvesti pasirinktinius delspinigių sumos limitus.</span><span class="sxs-lookup"><span data-stu-id="ee546-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="ee546-122">Puslapio <strong>Nustatyti delspinigių kodus</strong> lauke **Skaičiuoti delspinigius pagal<strong> pasirenkama** </strong> <strong>Procentą</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee546-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="ee546-123">Pvz., norėdami nustatyti palūkanų kodą, kuris apskaičiuoja 5 proc. palūkanas už kiekvienus du mėnesius, kiek vėluojama apmokėti sąskaitą faktūrą, lauke **Skaičiuoti palūkanas kas** turėtumėte įvesti 2 ir pasirinkti **Mėn.**.</span><span class="sxs-lookup"><span data-stu-id="ee546-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="ee546-124">Delspinigių tarifai pagal sumas</span><span class="sxs-lookup"><span data-stu-id="ee546-124">Interest rates based on amounts</span></span>
<span data-ttu-id="ee546-125">Galite nustatyti delspinigių tarifus, kurie apskaičiuoja nurodytą sumą pagal valiutą.</span><span class="sxs-lookup"><span data-stu-id="ee546-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="ee546-126">Delspinigių kode nurodoma kiekvienos valiutos delspinigių suma.</span><span class="sxs-lookup"><span data-stu-id="ee546-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="ee546-127">Galima įvesti pasirinktinius delspinigių sumos limitus.</span><span class="sxs-lookup"><span data-stu-id="ee546-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="ee546-128">Puslapio **Nustatyti delspinigių kodus** lauke **Skaičiuoti delspinigius pagal** pasirenkama **Sumą**.</span><span class="sxs-lookup"><span data-stu-id="ee546-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="ee546-129">Pvz., norėdami nustatyti palūkanų kodą, kuris apskaičiuoja 25,00 dydžio palūkanas už kiekvienas 20 dienų, kiek vėluojama apmokėti sąskaitą faktūrą, lauke **Skaičiuoti palūkanas kas** turėtumėte įvesti 20 ir pasirinkti **Dien.**.</span><span class="sxs-lookup"><span data-stu-id="ee546-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="ee546-130">Delspinigių tarifai pagal diapazonus</span><span class="sxs-lookup"><span data-stu-id="ee546-130">Interest rates based on ranges</span></span>
<span data-ttu-id="ee546-131">Galite nustatyti delspinigių tarifus, kurie skiriasi atsižvelgiant į pradelstą sumą, pradelstų dienų skaičių arba mėnesių skaičių.</span><span class="sxs-lookup"><span data-stu-id="ee546-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="ee546-132">Norėdami apibrėžti konkrečias kiekvienos valiutos delspinigių nuostatas, galite naudoti skirtuką **Pajamos pagal valiutą**.</span><span class="sxs-lookup"><span data-stu-id="ee546-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="ee546-133">Čia taip pat apibrėšite diapazoną.</span><span class="sxs-lookup"><span data-stu-id="ee546-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="ee546-134">Naudokite **Diapazonų** mygtuką, kad pridėtumėte eilutes, atstojančias norimus nustatyti diapazonus.</span><span class="sxs-lookup"><span data-stu-id="ee546-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="ee546-135">Reikšmė **Nuo** nurodo diapazono pradžią, o **Delspinigių vertės** skaičius nurodo arba procentą, arba sumą – tai priklauso nuo pasirinkties lauke **Skaičiuoti delspinigius pagal**, esančiame puslapyje **Nustatyti delspinigių kodus**.</span><span class="sxs-lookup"><span data-stu-id="ee546-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="ee546-136">1 pavyzdys: delspinigiai pagal diapazoną = suma</span><span class="sxs-lookup"><span data-stu-id="ee546-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="ee546-137">Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas tris mėnesius, kiek vėluojama apmokėti SF.</span><span class="sxs-lookup"><span data-stu-id="ee546-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ee546-138">Norite skaičiuoti delspinigius pagal procentinę delspinigių vertę, pakopiniais sumos intervalais.</span><span class="sxs-lookup"><span data-stu-id="ee546-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="ee546-139">Delspinigių vertė bus 1 proc. už SF sumas, neviršijančias 1 000,00, 2 proc. už sumas nuo 1 001,00 iki 5 000,00 ir 3 proc. už sumas, viršijančias 5 000,00 sumas.</span><span class="sxs-lookup"><span data-stu-id="ee546-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="ee546-140">Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="ee546-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ee546-141">**Lauko pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ee546-141">**Field name**</span></span>                  | <span data-ttu-id="ee546-142">**Lauko vertė**</span><span class="sxs-lookup"><span data-stu-id="ee546-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ee546-143">**Palūkanų kodas**</span><span class="sxs-lookup"><span data-stu-id="ee546-143">**Interest code**</span></span>               | <span data-ttu-id="ee546-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="ee546-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="ee546-145">**Apskaičiuoti palūkanas kas**</span><span class="sxs-lookup"><span data-stu-id="ee546-145">**Calculate interest every**</span></span>    | <span data-ttu-id="ee546-146">3/mėn.</span><span class="sxs-lookup"><span data-stu-id="ee546-146">3/Month</span></span>         |
| <span data-ttu-id="ee546-147">**Palūkanos pagal diapazoną**</span><span class="sxs-lookup"><span data-stu-id="ee546-147">**Interest by range**</span></span>           | <span data-ttu-id="ee546-148">Suma</span><span class="sxs-lookup"><span data-stu-id="ee546-148">Amount</span></span>          |
| <span data-ttu-id="ee546-149">**Skaičiuoti palūkanas pagal**</span><span class="sxs-lookup"><span data-stu-id="ee546-149">**Calculate interest based on**</span></span> | <span data-ttu-id="ee546-150">Procentai</span><span class="sxs-lookup"><span data-stu-id="ee546-150">Percentage</span></span>      |

<span data-ttu-id="ee546-151">Galite nustatyti diapazono informaciją, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="ee546-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="ee546-152">**Vertė Nuo**</span><span class="sxs-lookup"><span data-stu-id="ee546-152">**From value**</span></span> | <span data-ttu-id="ee546-153">**Palūkanų vertė**</span><span class="sxs-lookup"><span data-stu-id="ee546-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ee546-154">0</span><span class="sxs-lookup"><span data-stu-id="ee546-154">0</span></span>              | <span data-ttu-id="ee546-155">1</span><span class="sxs-lookup"><span data-stu-id="ee546-155">1</span></span>                  |
| <span data-ttu-id="ee546-156">1,001</span><span class="sxs-lookup"><span data-stu-id="ee546-156">1,001</span></span>          | <span data-ttu-id="ee546-157">2</span><span class="sxs-lookup"><span data-stu-id="ee546-157">2</span></span>                  |
| <span data-ttu-id="ee546-158">5,001</span><span class="sxs-lookup"><span data-stu-id="ee546-158">5,001</span></span>          | <span data-ttu-id="ee546-159">3</span><span class="sxs-lookup"><span data-stu-id="ee546-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="ee546-160">2 pavyzdys: delspinigiai pagal diapazoną = dienos</span><span class="sxs-lookup"><span data-stu-id="ee546-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="ee546-161">Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas 15 dienų, kiek vėluojama apmokėti SF.</span><span class="sxs-lookup"><span data-stu-id="ee546-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ee546-162">Norite skaičiuoti delspinigius pagal sumos delspinigių vertę, pakopiniais dienos intervalais.</span><span class="sxs-lookup"><span data-stu-id="ee546-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="ee546-163">Delspinigių vertė bus 10,00 už 15 dienų pirmąsias 60 dienų, 15,00 už 15 dienų, kai vėluojama 61–90 d., ir 20,00 už 15 dienų, kai vėluojama daugiau nei 91 d.</span><span class="sxs-lookup"><span data-stu-id="ee546-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="ee546-164">Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="ee546-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ee546-165">**Lauko pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ee546-165">**Field name**</span></span>                  | <span data-ttu-id="ee546-166">**Lauko vertė**</span><span class="sxs-lookup"><span data-stu-id="ee546-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ee546-167">**Palūkanų kodas**</span><span class="sxs-lookup"><span data-stu-id="ee546-167">**Interest code**</span></span>               | <span data-ttu-id="ee546-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="ee546-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="ee546-169">**Apskaičiuoti palūkanas kas**</span><span class="sxs-lookup"><span data-stu-id="ee546-169">**Calculate interest every**</span></span>    | <span data-ttu-id="ee546-170">15/dien.</span><span class="sxs-lookup"><span data-stu-id="ee546-170">15/Day</span></span>          |
| <span data-ttu-id="ee546-171">**Palūkanos pagal diapazoną**</span><span class="sxs-lookup"><span data-stu-id="ee546-171">**Interest by range**</span></span>           | <span data-ttu-id="ee546-172">Dienos</span><span class="sxs-lookup"><span data-stu-id="ee546-172">Days</span></span>            |
| <span data-ttu-id="ee546-173">**Skaičiuoti palūkanas pagal**</span><span class="sxs-lookup"><span data-stu-id="ee546-173">**Calculate interest based on**</span></span> | <span data-ttu-id="ee546-174">Suma</span><span class="sxs-lookup"><span data-stu-id="ee546-174">Amount</span></span>          |

<span data-ttu-id="ee546-175">Galite nustatyti diapazono informaciją, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="ee546-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="ee546-176">**Vertė Nuo**</span><span class="sxs-lookup"><span data-stu-id="ee546-176">**From value**</span></span> | <span data-ttu-id="ee546-177">**Palūkanų vertė**</span><span class="sxs-lookup"><span data-stu-id="ee546-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ee546-178">0</span><span class="sxs-lookup"><span data-stu-id="ee546-178">0</span></span>              | <span data-ttu-id="ee546-179">10</span><span class="sxs-lookup"><span data-stu-id="ee546-179">10</span></span>                 |
| <span data-ttu-id="ee546-180">61</span><span class="sxs-lookup"><span data-stu-id="ee546-180">61</span></span>             | <span data-ttu-id="ee546-181">15</span><span class="sxs-lookup"><span data-stu-id="ee546-181">15</span></span>                 |
| <span data-ttu-id="ee546-182">91</span><span class="sxs-lookup"><span data-stu-id="ee546-182">91</span></span>             | <span data-ttu-id="ee546-183">20</span><span class="sxs-lookup"><span data-stu-id="ee546-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="ee546-184">3 pavyzdys: delspinigiai pagal diapazoną = mėnesiai</span><span class="sxs-lookup"><span data-stu-id="ee546-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="ee546-185">Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas mėnesį, kiek vėluojama apmokėti SF.</span><span class="sxs-lookup"><span data-stu-id="ee546-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ee546-186">Norite skaičiuoti delspinigius pagal procentinę delspinigių vertę, pakopiniais mėnesio intervalais.</span><span class="sxs-lookup"><span data-stu-id="ee546-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="ee546-187">Delspinigių vertė bus 1,5 proc. už mėnesį pirmuosius tris mėnesius, kiek vėluojama sumokėti, 2,0 proc. už mėnesį už kitus tris mėnesius, 2,5 proc. už kiekvieną paskesnį mėnesį (kai vėluojama daugiau nei 6 mėnesius).</span><span class="sxs-lookup"><span data-stu-id="ee546-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="ee546-188">Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="ee546-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ee546-189">**Lauko pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ee546-189">**Field name**</span></span>                  | <span data-ttu-id="ee546-190">**Lauko vertė**</span><span class="sxs-lookup"><span data-stu-id="ee546-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ee546-191">**Palūkanų kodas**</span><span class="sxs-lookup"><span data-stu-id="ee546-191">**Interest code**</span></span>               | <span data-ttu-id="ee546-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="ee546-192">1M%ByMth</span></span>        |
| <span data-ttu-id="ee546-193">**Apskaičiuoti palūkanas kas**</span><span class="sxs-lookup"><span data-stu-id="ee546-193">**Calculate interest every**</span></span>    | <span data-ttu-id="ee546-194">1 / Mėn.</span><span class="sxs-lookup"><span data-stu-id="ee546-194">1/Month</span></span>         |
| <span data-ttu-id="ee546-195">**Palūkanos pagal diapazoną**</span><span class="sxs-lookup"><span data-stu-id="ee546-195">**Interest by range**</span></span>           | <span data-ttu-id="ee546-196">Mėnesiai</span><span class="sxs-lookup"><span data-stu-id="ee546-196">Months</span></span>          |
| <span data-ttu-id="ee546-197">**Skaičiuoti palūkanas pagal**</span><span class="sxs-lookup"><span data-stu-id="ee546-197">**Calculate interest based on**</span></span> | <span data-ttu-id="ee546-198">Procentai</span><span class="sxs-lookup"><span data-stu-id="ee546-198">Percentage</span></span>      |

<span data-ttu-id="ee546-199">Galite nustatyti diapazono informaciją, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="ee546-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="ee546-200">**Vertė Nuo**</span><span class="sxs-lookup"><span data-stu-id="ee546-200">**From value**</span></span> | <span data-ttu-id="ee546-201">**Palūkanų vertė**</span><span class="sxs-lookup"><span data-stu-id="ee546-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ee546-202">0</span><span class="sxs-lookup"><span data-stu-id="ee546-202">0</span></span>              | <span data-ttu-id="ee546-203">1.5</span><span class="sxs-lookup"><span data-stu-id="ee546-203">1.5</span></span>                |
| <span data-ttu-id="ee546-204">4</span><span class="sxs-lookup"><span data-stu-id="ee546-204">4</span></span>              | <span data-ttu-id="ee546-205">2</span><span class="sxs-lookup"><span data-stu-id="ee546-205">2</span></span>                  |
| <span data-ttu-id="ee546-206">7</span><span class="sxs-lookup"><span data-stu-id="ee546-206">7</span></span>              | <span data-ttu-id="ee546-207">2,5</span><span class="sxs-lookup"><span data-stu-id="ee546-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="ee546-208">Naujos versijos</span><span class="sxs-lookup"><span data-stu-id="ee546-208">New versions</span></span>
<span data-ttu-id="ee546-209">Delspinigių kodai turi galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="ee546-209">Interest codes are date effective.</span></span> <span data-ttu-id="ee546-210">Jei norite modifikuoti delspinigių tarifą, galite sukurti **naują versiją**, kuri galiotų nuo būsimos datos.</span><span class="sxs-lookup"><span data-stu-id="ee546-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="ee546-211">Norėdami peržiūrėti skirtingas versijas, galite naudoti meniu pasirinktį **Taikymo pradžios data** ir pasirinkti galutinę datą.</span><span class="sxs-lookup"><span data-stu-id="ee546-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="ee546-212">Taip pat galite pasirinkti **Rodyti visus įrašus**, kad puslapyje matytumėte visus delspinigių kodus.</span><span class="sxs-lookup"><span data-stu-id="ee546-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



