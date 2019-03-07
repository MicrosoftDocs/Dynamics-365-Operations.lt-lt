---
title: Medžiagų suvartojimo apskaičiavimas
description: Šiame straipsnyje pateikiama informacija apie įvairias parinktis, susijusias su medžiagų suvartojimo skaičiavimu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "316193"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="e3b5b-103">Medžiagų suvartojimo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="e3b5b-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3b5b-104">Šiame straipsnyje pateikiama informacija apie įvairias parinktis, susijusias su medžiagų suvartojimo skaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="e3b5b-105">**Sąrankos** ir **Žingsnio vartojimo** skirtukuose **Linijos duomenys** „FastTab“ skirtuke **Medžiagų kiekių sąraše** yra šie variantai, susiję su medžiagų suvartojimo apskaičiavimais.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="e3b5b-106">Kintamas ir pastovus vartojimas</span><span class="sxs-lookup"><span data-stu-id="e3b5b-106">Variable and constant consumption</span></span>
<span data-ttu-id="e3b5b-107">Lauke **Vartojimas** galite pasirinkti, ar sąnaudos bus apskaičiuojamos kaip pastovus, ar kintamas kiekis.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="e3b5b-108">Pasirinkite **Pastovus**, jei gamybai reikalingas fiksuotas kiekis ar visa apimtis, nepriklausomai nuo pagaminamos produkcijos kiekio.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="e3b5b-109">Pasirinkite **Kintamas**, kuris yra numatytasis parametras, jei gatavoms prekėms reikalingas kiekis medžiagų yra proporcingas pagamintai produkcijai.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="e3b5b-110">Suvartojimo apskaičiavimas iš formulės</span><span class="sxs-lookup"><span data-stu-id="e3b5b-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="e3b5b-111">**Formulės** lauke galite nustatyti įvairias formules apskaičiuoti medžiagų sąnaudoms.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="e3b5b-112">Jei naudojate numatytąją vertę, **Standartinis**, vartojimas pagal formulę neskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="e3b5b-113">Kartu su laukais **Aukštis**, **Plotis**, **Gylis**, **Tankis**, ir **Nuolatinis** taikomos šios formulės:</span><span class="sxs-lookup"><span data-stu-id="e3b5b-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="e3b5b-114">Aukštis \* Konstanta</span><span class="sxs-lookup"><span data-stu-id="e3b5b-114">Height \* Constant</span></span>
-   <span data-ttu-id="e3b5b-115">Aukštis \* Plotis \* Konstanta</span><span class="sxs-lookup"><span data-stu-id="e3b5b-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="e3b5b-116">Aukštis \* Plotis \* Gylis \* Konstanta</span><span class="sxs-lookup"><span data-stu-id="e3b5b-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="e3b5b-117">(Aukštis \* Plotis \* Gylis / Tankis) \* Konstanta</span><span class="sxs-lookup"><span data-stu-id="e3b5b-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="e3b5b-118">Suapvalina ir daugina</span><span class="sxs-lookup"><span data-stu-id="e3b5b-118">Rounding up and multiples</span></span>
<span data-ttu-id="e3b5b-119">Taip pat **Apvalinimo** ir **Dauginimo** laukuose galite suapvalinti medžiagų sąnaudų vertę.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="e3b5b-120">Pavyzdžiui, galite suapvalinti vertę pagal padalinį, kuriame žaliava imama gamybai.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="e3b5b-121">**Suapvalinimo** lauke yra šie variantai: **Kiekis**, **Matavimas**, ir **Suvartojimas**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="e3b5b-122">Kiekis</span><span class="sxs-lookup"><span data-stu-id="e3b5b-122">Quantity</span></span>

<span data-ttu-id="e3b5b-123">Jei suapvalinimui pasirinksite **Kiekis**, tai kiekis bus konkretaus kiekio kartotinis.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="e3b5b-124">Pavyzdžiui, kai reikia sveikų skaičių, lauke **Kartotiniai** nurodykite **1**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="e3b5b-125">Tada skaičiai apvalinami iki kiekio, kuris dalinasi iš 1.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="e3b5b-126">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="e3b5b-126">Measurement</span></span>

<span data-ttu-id="e3b5b-127">Paprastai apvalinimui pasirenkamas **Matavimas**, kai žaliava tiekiama konkrečiais kiekiais.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="e3b5b-128">Pavyzdžiui, gatavam gaminiui reikia 2 metrų metalinio vamzdžio gabalo, o sandėlyje yra 4,5 metrų ilgio metaliniai vamzdžiai.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="e3b5b-129">Šiuo atveju galima naudoti **Matavimo** apvalinimo mechanizmą apskaičiuoti, kiek reikės metalinių vamzdžių pagaminti tam tikrą skaičių gatavų gaminių.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="e3b5b-130">Šiame pavyzdyje laukas **Formulė** yra nustatytas į **Aukštis \* Konstanta**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="e3b5b-131">Laukas **Aukštis** yra nustatytas į **2**, siekiant nurodyti vamzdžio ilgį, reikalingą baigtai prekei.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="e3b5b-132">**Dauginimo** laukas yra nustatytas **4,5** nurodant, kad imamas 4,5 metrų ilgio vamzdis.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="e3b5b-133">Štai skaičiavimas:</span><span class="sxs-lookup"><span data-stu-id="e3b5b-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="e3b5b-134">Kartotiniai, reikalingi 10 vienetų gatavų gaminių gamybai: 10 ÷ 2 = 5 vnt.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="e3b5b-135">Iš viso sąnaudos: 4,5 × 5 = 22,5 metrų metalinio vamzdžio</span><span class="sxs-lookup"><span data-stu-id="e3b5b-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="e3b5b-136">Laikoma, kad kiekvieniems penkiems gabalams sunaudojamo vamzdžio 0,5 metrų vamzdžio išmetama į metalo laužą.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="e3b5b-137">Sunaudojimas</span><span class="sxs-lookup"><span data-stu-id="e3b5b-137">Consumption</span></span>

<span data-ttu-id="e3b5b-138">Paprastai kaip suapvalinimo mechanizmas pasirenkamas**Suvartojimas** kai žaliava konkretaus gaminio gamybai imama sveikais kiekiais.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="e3b5b-139">Pavyzdžiui, vienam gaminiui pagaminti sunaudojamos 2 kvortos dažų, o dažai yra 25 kvortų skardinėse.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="e3b5b-140">Šiuo atveju gali būti naudojamas **Suvartojimo** apvalinimo mechanizmas suapvalinti suvartojimą iki sveikų 25 kvortų skardinių skaičių.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="e3b5b-141">Štai kaip apskaičiuojamas dažų kiekis, kurio reikia pagaminti 180 vienetų gatavų gaminių:</span><span class="sxs-lookup"><span data-stu-id="e3b5b-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="e3b5b-142">Reikalingi dažai, išskyrus atliekas: 180 × 2 = 360 kvortų</span><span class="sxs-lookup"><span data-stu-id="e3b5b-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="e3b5b-143">Skardinių skaičius: 360 ÷ 25 = 14,4, kuris apvalinamas iki 15</span><span class="sxs-lookup"><span data-stu-id="e3b5b-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="e3b5b-144">Reikalingi dažai su atliekomis: 15 × 25 = 375 kvortų</span><span class="sxs-lookup"><span data-stu-id="e3b5b-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="e3b5b-145">Pakopinis vartojimas</span><span class="sxs-lookup"><span data-stu-id="e3b5b-145">Step consumption</span></span>
<span data-ttu-id="e3b5b-146">Vartojimas žingsniais naudojamas apskaičiuoti pastovų vartojimą kiekio intervalais.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="e3b5b-147">Jei skirtuko **Sąranka** lauke **Formulė** pasirenkate **Pakopinis vartojimas**, skirtuke **Pakopinis vartojimas** galite įtraukti informacijos apie pakopas. Fiksuotą suvartotą kiekį galima nustatyti intervalais pagal pagamintą kiekį.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="e3b5b-148">Pavyzdžiui, vartojimas žingsniais yra nustatytas taip, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="e3b5b-149">Serija Nuo</span><span class="sxs-lookup"><span data-stu-id="e3b5b-149">From series</span></span> | <span data-ttu-id="e3b5b-150">Kiekis</span><span class="sxs-lookup"><span data-stu-id="e3b5b-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="e3b5b-151">0,00</span><span class="sxs-lookup"><span data-stu-id="e3b5b-151">0.00</span></span>        | <span data-ttu-id="e3b5b-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="e3b5b-152">10.0000</span></span>  |
| <span data-ttu-id="e3b5b-153">100,00</span><span class="sxs-lookup"><span data-stu-id="e3b5b-153">100.00</span></span>      | <span data-ttu-id="e3b5b-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="e3b5b-154">20.0000</span></span>  |
| <span data-ttu-id="e3b5b-155">200,00</span><span class="sxs-lookup"><span data-stu-id="e3b5b-155">200.00</span></span>      | <span data-ttu-id="e3b5b-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="e3b5b-156">40.0000</span></span>  |

<span data-ttu-id="e3b5b-157">Medžiagų kiekių suvestinėje (KS) nurodytas kiekis yra 1, o pagamintas kiekis yra 110.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="e3b5b-158">Suvartojimo formulė „Iš serijos“ (Kiekis) = Suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="e3b5b-159">Kadangi pagamintas kiekis yra 110, jis patenka į „Iš 100 serijos“.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="e3b5b-160">Todėl kiekis yra 20.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-160">Therefore, the quantity is 20.</span></span>



