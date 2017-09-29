---
title: "Finansinių ataskaitų dizaino įrankio eilučių aprašai"
description: "Eilutės aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo kiekvienos finansinės ataskaitos eilutės turinį. Eilutės aprašą galima derinti su stulpelių aprašais, ataskaitų medžio aprašais ir ataskaitų aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 06a75889e62cbba6e47a8543cf663868df5ae2e3
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="b9f30-104">Finansinių ataskaitų dizaino įrankio eilučių aprašai</span><span class="sxs-lookup"><span data-stu-id="b9f30-104">Row definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b9f30-105">Eilutės aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo kiekvienos finansinės ataskaitos eilutės turinį.</span><span class="sxs-lookup"><span data-stu-id="b9f30-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="b9f30-106">Eilutės aprašą galima derinti su stulpelių aprašais, ataskaitų medžio aprašais ir ataskaitų aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės.</span><span class="sxs-lookup"><span data-stu-id="b9f30-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

<a name="create-a-row-definition"></a><span data-ttu-id="b9f30-107">Sukurti eilutės apibrėžimą</span><span class="sxs-lookup"><span data-stu-id="b9f30-107">Create a row definition</span></span>
-----------------------

1.  <span data-ttu-id="b9f30-108">Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Eilučių aprašai**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="b9f30-109">Meniu **Failas** spustelėkite **Naujas**, tada spustelėkite **Eilutės aprašas**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="b9f30-110">Daugiau informacijos apie kiekvieno langelio turinį rasite dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b9f30-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="b9f30-111">Eilutės apibrėžimo atidarymas</span><span class="sxs-lookup"><span data-stu-id="b9f30-111">Open a row definition</span></span>
1.  <span data-ttu-id="b9f30-112">Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Eilučių aprašai**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2.  <span data-ttu-id="b9f30-113">Dukart spustelėkite norimo atidaryti eilutės apibrėžimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-113">Double-click the name of the row definition to open.</span></span>
3.  <span data-ttu-id="b9f30-114">Norėdami peržiūrėti kūrimo blokus, susietus su eilutės apibrėžimu, dešiniuoju pelės klavišu spustelėkite eilutės apibrėžimą, tada pasirinkite **Susiejimai**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="b9f30-115"> Eilutės apibrėžimo turinys</span><span class="sxs-lookup"><span data-stu-id="b9f30-115">Contents of a row definition</span></span>
<span data-ttu-id="b9f30-116">Eilutės apraše gali būti iki 20 000 finansinės dimensijos eilučių ir jame gali būti pateikiama tolesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="b9f30-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

-   <span data-ttu-id="b9f30-117">Aprašomasis tekstas, suteikiantis ataskaitai reikšmę, kai sukuriamos skyriaus antraštės, eilutės ir tarpai, pavyzdžiui, **Grynieji pinigai** arba **Visos įplaukos**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
-   <span data-ttu-id="b9f30-118">Saitai į finansinius duomenis, kurie gali apimti dimensijų reikšmes sprendime „Microsoft Dynamics 365 for Finance and Operations“ **Pastaba:** galite nustatyti, kad eilutės apibrėžtis duomenis gautų iš finansinių dimensijų sistemos kaskart, kai generuojama ataskaita.</span><span class="sxs-lookup"><span data-stu-id="b9f30-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations **Note:** You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>
-   <span data-ttu-id="b9f30-119">Eilučių bendrosios sumos ir formulės, kurios pagrįstos susietais finansiniais duomenimis</span><span class="sxs-lookup"><span data-stu-id="b9f30-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="b9f30-120">Paprastai kiekvienoje eilutės apibrėžimo eilutėje yra vieno iš šių tipų informaciją:</span><span class="sxs-lookup"><span data-stu-id="b9f30-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

-   <span data-ttu-id="b9f30-121">Saitai į finansinių dimensijų sistemą</span><span class="sxs-lookup"><span data-stu-id="b9f30-121">References to the financial dimensions system</span></span>
-   <span data-ttu-id="b9f30-122">Bendrosios sumos arba skaičiavimai pagal duomenis</span><span class="sxs-lookup"><span data-stu-id="b9f30-122">Totals or calculations that are based on the data</span></span>
-   <span data-ttu-id="b9f30-123">Formatavimas</span><span class="sxs-lookup"><span data-stu-id="b9f30-123">Formatting</span></span>

<span data-ttu-id="b9f30-124">Informaciją įvesti į eilutės aprašą galima dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="b9f30-124">There are two methods for entering information in a row definition:</span></span>

-   <span data-ttu-id="b9f30-125">Patiems įvesti eilutės informaciją į naują eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="b9f30-126">Daugiau informacijos rasite dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b9f30-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
-   <span data-ttu-id="b9f30-127">Naudojant ataskaitų dizaino įrankį gauti eilutės informaciją tiesiogiai iš finansinių dimensijų.</span><span class="sxs-lookup"><span data-stu-id="b9f30-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="b9f30-128">Norėdami daugiau informacijos, žr. skyrių „Susijusios formulės / eilutės / vienetai“ dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b9f30-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="b9f30-129"> Dimensijų įtraukimas į eilutės apibrėžimą</span><span class="sxs-lookup"><span data-stu-id="b9f30-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="b9f30-130">Dimensija yra duomenų ir reikšmių sankirta.</span><span class="sxs-lookup"><span data-stu-id="b9f30-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="b9f30-131">Ataskaitų dizaino įrankyje galite grupuoti duomenis ir reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b9f30-131">You can group data and values in report designer.</span></span> <span data-ttu-id="b9f30-132">Tada galite išsamiau klasifikuoti ir analizuoti operacijas.</span><span class="sxs-lookup"><span data-stu-id="b9f30-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="b9f30-133">Galite naudoti dialogo langą **Eilučių įterpimas iš dimensijų** ir vienu metu į eilutės apibrėžimą įtraukti kelias eilutes.</span><span class="sxs-lookup"><span data-stu-id="b9f30-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="b9f30-134">Dialogo lange rodoma po vieną kiekvienos dimensijos stulpelį.</span><span class="sxs-lookup"><span data-stu-id="b9f30-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="b9f30-135">Tolesnėje lentelėje nurodyta, kokią informaciją galite nurodyti kiekvienoje dimensijoje.</span><span class="sxs-lookup"><span data-stu-id="b9f30-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="b9f30-136">Parinktis</span><span class="sxs-lookup"><span data-stu-id="b9f30-136">Option</span></span>                | <span data-ttu-id="b9f30-137">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="b9f30-137">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f30-138">Dimensija</span><span class="sxs-lookup"><span data-stu-id="b9f30-138">Dimension</span></span>             | <span data-ttu-id="b9f30-139">Modelį, kuris identifikuoja į eilutės apibrėžimą norimą įtraukti dimensiją.</span><span class="sxs-lookup"><span data-stu-id="b9f30-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="b9f30-140">Šiame modelyje kiekvienai dimensijų padėčiai yra po vieną ampersandą (&) arba skaičiaus ženklą (\#).</span><span class="sxs-lookup"><span data-stu-id="b9f30-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="b9f30-141">Paprastai dimensijai Pagrindinė sąskaita naudojami visi konjunktūros ženklai, o kitoms dimensijoms naudojami visi skaičių ženklai.</span><span class="sxs-lookup"><span data-stu-id="b9f30-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="b9f30-142">Dimensijos intervalo pradžia</span><span class="sxs-lookup"><span data-stu-id="b9f30-142">Dimension Range Start</span></span> | <span data-ttu-id="b9f30-143">Į eilutės apibrėžimą norima įtraukti pirmoji šios dimensijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b9f30-143">The first value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="b9f30-144">Dimensijos intervalo pabaiga</span><span class="sxs-lookup"><span data-stu-id="b9f30-144">Dimension Range End</span></span>   | <span data-ttu-id="b9f30-145">Į eilutės apibrėžimą norima įtraukti paskutinė šios dimensijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b9f30-145">The last value for this dimension to add to the row definition.</span></span>                                                                                                                                                                                                                  |

<span data-ttu-id="b9f30-146">Norėdami į eilutės aprašą įtraukti dimensijų, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b9f30-146">To add dimensions to a row definition, follow these steps.</span></span>

1.  <span data-ttu-id="b9f30-147">Ataskaitų dizaino įrankyje spustelėkite **Eilučių aprašai**, tada atidarykite norimą keisti eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="b9f30-148">Meniu **Redaguoti** spustelėkite **Įterpti eilutes iš dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3.  <span data-ttu-id="b9f30-149">Eilutės **Dimensijos** dialogo lange **Įterpti eilutes iš dimensijų** pasirinkite į eilutės aprašą norimą perkelti dimensijos langelį, tada spustelėkite **Visi &&&**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4.  <span data-ttu-id="b9f30-150">Norėdami apriboti eilutės aprašą iki kelių dimensijos reikšmių, langelyje **Dimensijos intervalo pradžia** įveskite pradžios dimensijos reikšmę, tada langelyje **Dimensijos intervalo pabaiga** įveskite pabaigos dimensijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b9f30-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="b9f30-151">Norėdami įtraukti visas pasirinktos dimensijos reikšmes, palikite šiuos langelius tuščius.</span><span class="sxs-lookup"><span data-stu-id="b9f30-151">To include all values for the selected dimension, leave these cells empty.</span></span> <span data-ttu-id="b9f30-152">**Pastaba:** naudojant pakaitos simbolius (\* arba ?) dimensijos intervaluose gali būti gaunami ne visi norimi rezultatai, priklausomai nuo to, kaip ERP duomenų bazė sujungia duomenis.</span><span class="sxs-lookup"><span data-stu-id="b9f30-152">**Note:** Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>
5.  <span data-ttu-id="b9f30-153">Lauke **Pradžios eilutės kodas** nurodykite pirmos dimensijos reikšmės eilutės kodą, kuris turėtų būti įtraukiamas į eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6.  <span data-ttu-id="b9f30-154">Lauke **Didinti kiekvieną eilutę** nurodykite tarpą tarp vienas paskui kitą einančių eilutės kodų..</span><span class="sxs-lookup"><span data-stu-id="b9f30-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="b9f30-155">Pvz., jei pirmos eilutės kodas yra 100, o padidinimo vertė yra 30, pirmų naujų eilučių kodai yra 100, 130, 160, 190 ir 220.</span><span class="sxs-lookup"><span data-stu-id="b9f30-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="b9f30-156">Naudokite padidinimo vertę, kuria sukuriamas tarpas naujiems formatams ir formulių eilutėms įterpti.</span><span class="sxs-lookup"><span data-stu-id="b9f30-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7.  <span data-ttu-id="b9f30-157">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-157">Click **OK**.</span></span> <span data-ttu-id="b9f30-158">Eilutės apraše kiekvienai pasirinktai dimensijos reikšmei įtraukiama viena eilutė.</span><span class="sxs-lookup"><span data-stu-id="b9f30-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="b9f30-159">Koreguoti eilutės apibrėžimo apvalinimą</span><span class="sxs-lookup"><span data-stu-id="b9f30-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="b9f30-160">Jei turite balansą, kuriame sumos suapvalintos, bendrosios sumos į balansą gali nepatekti.</span><span class="sxs-lookup"><span data-stu-id="b9f30-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="b9f30-161">Pavyzdžiui, taip gali atsitikti, jei balanso ataskaitoje naudojate apvalinimo parinktį, o ataskaitos apraše taip pat nurodomas apvalinimas.</span><span class="sxs-lookup"><span data-stu-id="b9f30-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="b9f30-162">Norėdami subalansuoti balansų sumas, eilutės apraše galite naudoti parinktį **Apvalinimo koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="b9f30-163">Apvalinimą galite išjungti arba modifikuoti ataskaitos aprašo skirtuke **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="b9f30-164">Toliau pateikiamoje lentelėje parodyta, kaip apvalinamos sumos.</span><span class="sxs-lookup"><span data-stu-id="b9f30-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="b9f30-165">Šioje lentelėje įjungus apvalinimą eilučių 100 ir 200 sumos skiriasi.</span><span class="sxs-lookup"><span data-stu-id="b9f30-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="b9f30-166">Eilutės kodas</span><span class="sxs-lookup"><span data-stu-id="b9f30-166">Row code</span></span> | <span data-ttu-id="b9f30-167">Sumos be apvalinimo</span><span class="sxs-lookup"><span data-stu-id="b9f30-167">Amounts without rounding</span></span> | <span data-ttu-id="b9f30-168">Sumos su apvalinimu iki tūkstančių</span><span class="sxs-lookup"><span data-stu-id="b9f30-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="b9f30-169">100</span><span class="sxs-lookup"><span data-stu-id="b9f30-169">100</span></span>      | <span data-ttu-id="b9f30-170">3,600</span><span class="sxs-lookup"><span data-stu-id="b9f30-170">3,600</span></span>                    | <span data-ttu-id="b9f30-171">4</span><span class="sxs-lookup"><span data-stu-id="b9f30-171">4</span></span>                                       |
| <span data-ttu-id="b9f30-172">200</span><span class="sxs-lookup"><span data-stu-id="b9f30-172">200</span></span>      | <span data-ttu-id="b9f30-173">3,700</span><span class="sxs-lookup"><span data-stu-id="b9f30-173">3,700</span></span>                    | <span data-ttu-id="b9f30-174">4</span><span class="sxs-lookup"><span data-stu-id="b9f30-174">4</span></span>                                       |
| <span data-ttu-id="b9f30-175">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="b9f30-175">Total</span></span>    | <span data-ttu-id="b9f30-176">7,300</span><span class="sxs-lookup"><span data-stu-id="b9f30-176">7,300</span></span>                    | <span data-ttu-id="b9f30-177">8</span><span class="sxs-lookup"><span data-stu-id="b9f30-177">8</span></span>                                       |

<span data-ttu-id="b9f30-178">Norėdami koreguoti balanso apvalinimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b9f30-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1.  <span data-ttu-id="b9f30-179">Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2.  <span data-ttu-id="b9f30-180">Meniu **Redaguoti** spustelėkite **Apvalinimo koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3.  <span data-ttu-id="b9f30-181">Dialogo lange **Apvalinimo koregavimai** įveskite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="b9f30-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>
    -   <span data-ttu-id="b9f30-182">**Apvalinimo koregavimo eilutė** – eilutės, kuri bus pakoreguota norint subalansuoti balansą, kodas.</span><span class="sxs-lookup"><span data-stu-id="b9f30-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    -   <span data-ttu-id="b9f30-183">**Viso turto eilutė** – balanso eilutės, kurioje nurodytas bendras turtas, kodas.</span><span class="sxs-lookup"><span data-stu-id="b9f30-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    -   <span data-ttu-id="b9f30-184">**Visų įsipareigojimų ir kapitalo eilutė** – balanso eilutės, kurioje nurodyti visi įsipareigojimai ir kapitalas, kodas.</span><span class="sxs-lookup"><span data-stu-id="b9f30-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    -   <span data-ttu-id="b9f30-185">**Koregavimo sumos riba** – teigiamu sveikuoju skaičiumi išreikšta automatinių koregavimų riba.</span><span class="sxs-lookup"><span data-stu-id="b9f30-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="b9f30-186">Ši suma lyginama su faktinio apvalinimo skirtumo absoliučiąja reikšme.</span><span class="sxs-lookup"><span data-stu-id="b9f30-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    <span data-ttu-id="b9f30-187">**Pastaba:** šie eilutės kodai turi būti susieti su finansiniais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="b9f30-187">**Note:** These row codes must be linked to your financial data.</span></span> <span data-ttu-id="b9f30-188">Kitaip tariant, eilutės dimensijos reikšmė turi būti nurodyta langelyje **Saitas su finansinėmis dimensijomis**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="b9f30-189">**Nepateikite** nuorodos į aprašymo (**DESC**), apskaičiuotą (**CALC**) arba susumuotą (**TOT**) eilutę.</span><span class="sxs-lookup"><span data-stu-id="b9f30-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="b9f30-190">Dabar jūsų balanso sumos įjungus apvalinimą bus tolygiai subalansuotos.</span><span class="sxs-lookup"><span data-stu-id="b9f30-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span> <span data-ttu-id="b9f30-191">**Pastaba:** koregavimo riba taikoma atsižvelgiant į nurodytą ataskaitos aprašo pasirinktį **Apvalinimo tikslumas**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-191">**Note:** The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="b9f30-192">Pavyzdžiui, jei pasirenkate apvalinti savo ataskaitą iki tūkstančių ir lauke **Koregavimo sumos apribojimas** įvedate **2**, lauke **Apvalinimo koregavimo eilutė** nurodytą reikšmę padidinus arba sumažinus daugiau negu 2 000 rodomas įspėjantis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="b9f30-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="b9f30-193">Eilutės ir stulpelio teksto formatavimas</span><span class="sxs-lookup"><span data-stu-id="b9f30-193">Format row and column text</span></span>
<span data-ttu-id="b9f30-194">Galite keisti savo ataskaitų išvaizdą pakeisdami šriftus ir formatuodami tekstą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="b9f30-195">Toliau nurodomuose skyriuose paaiškinama, kaip formatuoti ataskaitos eilučių ir stulpelių išvaizdą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="b9f30-196">Tvarkyti šrifto stilius</span><span class="sxs-lookup"><span data-stu-id="b9f30-196">Manage font styles</span></span>

<span data-ttu-id="b9f30-197">Galite kurti ir modifikuoti ataskaitos šrifto stilius.</span><span class="sxs-lookup"><span data-stu-id="b9f30-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="b9f30-198">Tada galite taikyti šiuos stilius dokumentui arba konkrečiai ataskaitos eilutei ar stulpeliui.</span><span class="sxs-lookup"><span data-stu-id="b9f30-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9f30-199">Kurti šrifto stilių</span><span class="sxs-lookup"><span data-stu-id="b9f30-199">Create a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="b9f30-200">Ataskaitos dizaino įrankio meniu <strong>Formatas </strong>spustelėkite <strong>Stiliai ir formatavimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9f30-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="b9f30-201">Dialogo lange <strong>Stiliai ir formatavimas</strong> spustelėkite <strong>Naujas</strong>, tada įveskite unikalų naujo stiliaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="b9f30-202">Pasirinkite šriftą, tada spustelėkite <strong>Gerai</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9f30-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9f30-203">Modifikuoti šrifto stilių</span><span class="sxs-lookup"><span data-stu-id="b9f30-203">Modify a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="b9f30-204">Ataskaitos dizaino įrankio meniu <strong>Formatas </strong>spustelėkite <strong>Stiliai ir formatavimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9f30-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="b9f30-205">Dialogo lange <strong>Stiliai ir formatavimas</strong> pasirinkite norimą modifikuoti stilių, tada spustelėkite <strong>Modifikuoti</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9f30-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="b9f30-206">Pasirinkite šriftą, tada spustelėkite <strong>Gerai</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9f30-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9f30-207">Taikyti šrifto stilių</span><span class="sxs-lookup"><span data-stu-id="b9f30-207">Apply a font style</span></span></td>
<td><ol>
<li><span data-ttu-id="b9f30-208">Ataskaitų dizaino įrankio apraše, stulpelio apraše arba antraštėse ir poraštėse pasirinkite vieną ar kelis langelius.</span><span class="sxs-lookup"><span data-stu-id="b9f30-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="b9f30-209">Įrankių juostos sąraše <strong>Stilius</strong> pasirinkite šrifto stilių.</span><span class="sxs-lookup"><span data-stu-id="b9f30-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="b9f30-210">Formatuoti eilutės tekstą</span><span class="sxs-lookup"><span data-stu-id="b9f30-210">Format row text</span></span>

<span data-ttu-id="b9f30-211">Eilutės apraše nurodytas formatavimas perrašo stulpelio apraše ir ataskaitos apraše nurodytą formatavimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="b9f30-212">Galite keisti teksto formatą, naudodami formatavimo įrankių juostos valdiklius.</span><span class="sxs-lookup"><span data-stu-id="b9f30-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="b9f30-213">Šie valdikliai yra standartiniai „Microsoft Windows“ valdikliai.</span><span class="sxs-lookup"><span data-stu-id="b9f30-213">These controls are standard Microsoft Windows controls.</span></span>

1.  <span data-ttu-id="b9f30-214">Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-214">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="b9f30-215">Pažymėkite norimus formatuoti langelius.</span><span class="sxs-lookup"><span data-stu-id="b9f30-215">Select the cells to format.</span></span> <span data-ttu-id="b9f30-216">Norėdami pažymėti kelis langelius, laikykite nuspaudę klavišą Ctrl ir pasirinkite langelį.</span><span class="sxs-lookup"><span data-stu-id="b9f30-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3.  <span data-ttu-id="b9f30-217">Norėdami taikyti, spustelėkite įrankių juostos formato mygtuką.</span><span class="sxs-lookup"><span data-stu-id="b9f30-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="b9f30-218">Pvz., norėdami įtraukti eilutę, pasirinkite eilutę, tada įrankių juostoje spustelėkite **Padidinti įtrauką** ![Padidinti įtrauką](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Padidinti įtrauką").</span><span class="sxs-lookup"><span data-stu-id="b9f30-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="b9f30-219">Koreguoti stulpelius, kol kuriamos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="b9f30-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="b9f30-220">Kad būtų lengviau peržiūrėti stulpelius, su kuriais dirbate eilutės apraše, galite koreguoti stulpelių plotį ir slėpti (sumažinti) arba rodyti stulpelius peržiūros srityje.</span><span class="sxs-lookup"><span data-stu-id="b9f30-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="b9f30-221">Atlikti keitimai turi įtakos tik stulpelių vaizdui ekrane.</span><span class="sxs-lookup"><span data-stu-id="b9f30-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="b9f30-222">Jie neturi įtakos ataskaitų stulpelių formatavimui.</span><span class="sxs-lookup"><span data-stu-id="b9f30-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="b9f30-223">Stulpelio pločio keitimas peržiūros srityje</span><span class="sxs-lookup"><span data-stu-id="b9f30-223">Change the width of a column in the view pane</span></span>

1.  <span data-ttu-id="b9f30-224">Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-224">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="b9f30-225">Meniu **Formatas** pasirinkite **Stulpelio plotis**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-225">On the **Format** menu, select **Column Width**.</span></span>
3.  <span data-ttu-id="b9f30-226">Dialogo lange **Stulpelio plotis** įveskite reikšmę ir tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="b9f30-227">Stulpelio plotį pakeisti taip pat galite vilkdami stulpelio antraštės langelio dešiniąją kraštinę.</span><span class="sxs-lookup"><span data-stu-id="b9f30-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="b9f30-228">Stulpelių slėpimas peržiūros rodinyje</span><span class="sxs-lookup"><span data-stu-id="b9f30-228">Hide columns in the view pane</span></span>

1.  <span data-ttu-id="b9f30-229">Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-229">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="b9f30-230">Pasirinkite norimą sumažinti stulpelį arba stulpelius.</span><span class="sxs-lookup"><span data-stu-id="b9f30-230">Select the column or columns to minimize.</span></span>
3.  <span data-ttu-id="b9f30-231">Spustelėkite dešinįjį pelės mygtuką, tada spustelėkite **Slėpti**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="b9f30-232">Visų paslėptų stulpelių rodymas peržiūros srityje</span><span class="sxs-lookup"><span data-stu-id="b9f30-232">Show all hidden columns in the view pane</span></span>

1.  <span data-ttu-id="b9f30-233">Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="b9f30-233">In Report Designer, open the row definition to modify.</span></span>
2.  <span data-ttu-id="b9f30-234">Dešiniuoju pelės mygtuku spustelėkite sumažintą stulpelį, kurį norite rodyti, tada spustelėkite **Nebeslėpti**.</span><span class="sxs-lookup"><span data-stu-id="b9f30-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


<a name="see-also"></a><span data-ttu-id="b9f30-235">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="b9f30-235">See also</span></span>
--------

[<span data-ttu-id="b9f30-236">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="b9f30-236">Financial reporting</span></span>](financial-reporting-intro.md)



