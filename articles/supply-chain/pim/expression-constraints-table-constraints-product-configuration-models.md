---
title: "Produkto konfigūravimo modelių išraiškos ir lentelės apribojimai"
description: "Šioje temoje apžvelgiamas išraiškos ir lentelės apribojimų naudojimas. Apribojimais valdomos atributo reikšmės, kurias galite pasirinkti konfigūruodami pardavimo užsakymo, pardavimo pasiūlymo, pirkimo užsakymo arba gamybos užsakymo produktus. Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite sukurti apribojimus."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 4964026f0413524590846396859497df02850bfb
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="86adf-105">Produkto konfigūravimo modelių išraiškos ir lentelės apribojimai</span><span class="sxs-lookup"><span data-stu-id="86adf-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="86adf-106">Šioje temoje apžvelgiamas išraiškos ir lentelės apribojimų naudojimas.</span><span class="sxs-lookup"><span data-stu-id="86adf-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="86adf-107">Apribojimais valdomos atributo reikšmės, kurias galite pasirinkti konfigūruodami pardavimo užsakymo, pardavimo pasiūlymo, pirkimo užsakymo arba gamybos užsakymo produktus.</span><span class="sxs-lookup"><span data-stu-id="86adf-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="86adf-108">Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite sukurti apribojimus.</span><span class="sxs-lookup"><span data-stu-id="86adf-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="86adf-109">Apribojimais valdomos atributo reikšmės, kurias galite pasirinkti konfigūruodami pardavimo užsakymo, pardavimo pasiūlymo, pirkimo užsakymo arba gamybos užsakymo produktus.</span><span class="sxs-lookup"><span data-stu-id="86adf-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="86adf-110">Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite sukurti apribojimus.</span><span class="sxs-lookup"><span data-stu-id="86adf-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="86adf-111">Kas yra išraiškos apribojimai?</span><span class="sxs-lookup"><span data-stu-id="86adf-111">What are expression constraints?</span></span>
<span data-ttu-id="86adf-112">Išraiškos apribojimai apibrėžiami išraiška, kurioje naudojami aritmetiniai ir Bulio logikos operatoriai bei funkcijos.</span><span class="sxs-lookup"><span data-stu-id="86adf-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="86adf-113">Produkto konfigūracijos modelyje rašomas konkretaus komponento išraiškos apribojimas.</span><span class="sxs-lookup"><span data-stu-id="86adf-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="86adf-114">Kitas komponentas negali jo pakartotinai arba bendrai naudoti.</span><span class="sxs-lookup"><span data-stu-id="86adf-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="86adf-115">Tačiau komponento išraiškos apribojimai gali nurodyti komponento pakomponenčio atributus.</span><span class="sxs-lookup"><span data-stu-id="86adf-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="86adf-116">Kas yra lentelės apribojimai?</span><span class="sxs-lookup"><span data-stu-id="86adf-116">What are table constraints?</span></span>
<span data-ttu-id="86adf-117">Lentelės apribojimais nurodomi konfigūruojant produktą leidžiami atributų reikšmių deriniai.</span><span class="sxs-lookup"><span data-stu-id="86adf-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="86adf-118">Lentelės apribojimų apibrėžimai gali būti bendrai naudojami.</span><span class="sxs-lookup"><span data-stu-id="86adf-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="86adf-119">Produkto konfigūracijos modelyje kurdami komponento lentelės apribojimą, pasirenkate lentelės apribojimo apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="86adf-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="86adf-120">Norėdami kurti leidžiamus derinius, į komponentus įtraukiate konkrečių tipų atributų.</span><span class="sxs-lookup"><span data-stu-id="86adf-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="86adf-121">Kiekvienas atributo tipas yra konkrečios reikšmės.</span><span class="sxs-lookup"><span data-stu-id="86adf-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="86adf-122">Lentelės apribojimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="86adf-122">Example of a table constraint</span></span>

<span data-ttu-id="86adf-123">Šiame pavyzdyje parodoma, kaip galite riboti garsiakalbio konfigūracijas konkrečiomis spintelės apdailomis ir priekinėmis grotelėmis.</span><span class="sxs-lookup"><span data-stu-id="86adf-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="86adf-124">Pirmoje lentelėje nurodytos spintelių apdailos ir priekinės grotelės, kurias galima konfigūruoti įprastu metu.</span><span class="sxs-lookup"><span data-stu-id="86adf-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="86adf-125">Reikšmės nustatomos atributų tipuose **Spintelių apdaila** ir **Priekinės grotelės**.</span><span class="sxs-lookup"><span data-stu-id="86adf-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="86adf-126">Atributo tipas</span><span class="sxs-lookup"><span data-stu-id="86adf-126">Attribute type</span></span> | <span data-ttu-id="86adf-127">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="86adf-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="86adf-128">Spintelės apdaila</span><span class="sxs-lookup"><span data-stu-id="86adf-128">Cabinet finish</span></span> | <span data-ttu-id="86adf-129">Juoda, ąžuolo, raudonmedžio, balta</span><span class="sxs-lookup"><span data-stu-id="86adf-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="86adf-130">Priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="86adf-130">Front grill</span></span>    | <span data-ttu-id="86adf-131">Juoda, metalo, balta</span><span class="sxs-lookup"><span data-stu-id="86adf-131">Black, Metal, White</span></span>         |

<span data-ttu-id="86adf-132">Kitoje lentelėje nurodyti deriniai, kurie nustatyti pagal lentelės apribojimą **Spalva ir apdaila**.</span><span class="sxs-lookup"><span data-stu-id="86adf-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="86adf-133">Naudodami šį lentelės apribojimą, galite konfigūruoti garsiakalbį, turintį ąžuolinę apdailą ir juodas groteles, raudonmedžio apdailą ir baltas groteles ir t. t.</span><span class="sxs-lookup"><span data-stu-id="86adf-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="86adf-134">Baigti</span><span class="sxs-lookup"><span data-stu-id="86adf-134">Finish</span></span>         | <span data-ttu-id="86adf-135">Grotelės</span><span class="sxs-lookup"><span data-stu-id="86adf-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="86adf-136">Ąžuolo</span><span class="sxs-lookup"><span data-stu-id="86adf-136">Oak</span></span>            | <span data-ttu-id="86adf-137">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-137">Black</span></span>                       |
| <span data-ttu-id="86adf-138">Palisandro</span><span class="sxs-lookup"><span data-stu-id="86adf-138">Rosewood</span></span>       | <span data-ttu-id="86adf-139">Balta</span><span class="sxs-lookup"><span data-stu-id="86adf-139">White</span></span>                       |
| <span data-ttu-id="86adf-140">Balta</span><span class="sxs-lookup"><span data-stu-id="86adf-140">White</span></span>          | <span data-ttu-id="86adf-141">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-141">Black</span></span>                       |
| <span data-ttu-id="86adf-142">Balta</span><span class="sxs-lookup"><span data-stu-id="86adf-142">White</span></span>          | <span data-ttu-id="86adf-143">Balta</span><span class="sxs-lookup"><span data-stu-id="86adf-143">White</span></span>                       |
| <span data-ttu-id="86adf-144">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-144">Black</span></span>          | <span data-ttu-id="86adf-145">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-145">Black</span></span>                       |
| <span data-ttu-id="86adf-146">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-146">Black</span></span>          | <span data-ttu-id="86adf-147">Metalo</span><span class="sxs-lookup"><span data-stu-id="86adf-147">Metal</span></span>                       | 

<span data-ttu-id="86adf-148">Galite sukurti pagal sistemas arba vartotojus nustatytus lentelės apribojimus.</span><span class="sxs-lookup"><span data-stu-id="86adf-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="86adf-149">Daugiau informacijos žr. [Pagal sistemas arba vartotojus nustatyti lentelės apribojimai](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="86adf-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="86adf-150">Kokia sintaksė turi būti naudojama apribojimams rašyti?</span><span class="sxs-lookup"><span data-stu-id="86adf-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="86adf-151">Rašydami apribojimus turite naudoti optimizuoto modeliavimo kalbos (OML) sintaksę.</span><span class="sxs-lookup"><span data-stu-id="86adf-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="86adf-152">Sistema naudoja „Microsoft Solver Foundation“ apribojimų sprendimo priemonę apribojimams išspręsti.</span><span class="sxs-lookup"><span data-stu-id="86adf-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="86adf-153">Turėčiau naudoti lentelės apribojimus ar išraiškos apribojimus?</span><span class="sxs-lookup"><span data-stu-id="86adf-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="86adf-154">Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite konfigūruoti apribojimus.</span><span class="sxs-lookup"><span data-stu-id="86adf-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="86adf-155">Lentelės apribojimą sudarote matricos pagrindu, o išraiškos apribojimas yra atskiras sakinys.</span><span class="sxs-lookup"><span data-stu-id="86adf-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="86adf-156">Konfigūruojant produktą nėra svarbu, kokio tipo apribojimas bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="86adf-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="86adf-157">Kitame pavyzdyje nurodomi abiejų metodų skirtumai.</span><span class="sxs-lookup"><span data-stu-id="86adf-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="86adf-158">Kai produktą konfigūruojate naudodami šiuos apribojimų nustatymus, galima naudoti toliau nurodytus derinius.</span><span class="sxs-lookup"><span data-stu-id="86adf-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="86adf-159">Produktas, kurio spalva Juoda, o dydis 30 arba 50</span><span class="sxs-lookup"><span data-stu-id="86adf-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="86adf-160">Produktas, kurio spalva Raudona, o dydis 20</span><span class="sxs-lookup"><span data-stu-id="86adf-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="86adf-161">Lentelės apribojimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="86adf-161">Table constraint setup</span></span>

| <span data-ttu-id="86adf-162">Spalva</span><span class="sxs-lookup"><span data-stu-id="86adf-162">Color</span></span> | <span data-ttu-id="86adf-163">Dydis</span><span class="sxs-lookup"><span data-stu-id="86adf-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="86adf-164">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-164">Black</span></span> | <span data-ttu-id="86adf-165">30</span><span class="sxs-lookup"><span data-stu-id="86adf-165">30</span></span>   |
| <span data-ttu-id="86adf-166">Juoda</span><span class="sxs-lookup"><span data-stu-id="86adf-166">Black</span></span> | <span data-ttu-id="86adf-167">50</span><span class="sxs-lookup"><span data-stu-id="86adf-167">50</span></span>   |
| <span data-ttu-id="86adf-168">Raudona</span><span class="sxs-lookup"><span data-stu-id="86adf-168">Red</span></span>   | <span data-ttu-id="86adf-169">20</span><span class="sxs-lookup"><span data-stu-id="86adf-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="86adf-170">Išraiškos apribojimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="86adf-170">Expression constraint setup</span></span>

<span data-ttu-id="86adf-171">(Spalva == "Juoda" & (dydis == "30" | dydis == "50")) | (spalva == "Raudona" & dydis = "20")</span><span class="sxs-lookup"><span data-stu-id="86adf-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="86adf-172">Rašydamas išraiškos apribojimus turėčiau naudoti operatorius ar intarpo ženklą?</span><span class="sxs-lookup"><span data-stu-id="86adf-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="86adf-173">Galite rašyti išraiškos apribojimą naudodami galimus prefiksų operatorius arba intarpo ženklą.</span><span class="sxs-lookup"><span data-stu-id="86adf-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="86adf-174">Negalima naudoti intarpo ženklo su operatoriais **Min**, **Max** ir **Abs**.</span><span class="sxs-lookup"><span data-stu-id="86adf-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="86adf-175">Daugumoje programavimo kalbų šie operatoriai yra standartiniai.</span><span class="sxs-lookup"><span data-stu-id="86adf-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="86adf-176">Kokius operatorius ir intarpo ženklus galiu naudoti rašydamas išraiškos apribojimus?</span><span class="sxs-lookup"><span data-stu-id="86adf-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="86adf-177">Šiose lentelėse išvardyti operatoriai ir intarpo ženklai, kuriuos galite naudoti produkto konfigūracijos modelyje rašydami komponento išraiškos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="86adf-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="86adf-178">Pirmoje lentelėje pateiktuose pavyzdžiuose nurodyta, kaip rašyti išraišką naudojant intarpo ženklą arba operatorius.</span><span class="sxs-lookup"><span data-stu-id="86adf-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86adf-179">Operatorius</span><span class="sxs-lookup"><span data-stu-id="86adf-179">Operator</span></span></th>
<th><span data-ttu-id="86adf-180">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="86adf-180">Description</span></span></th>
<th><span data-ttu-id="86adf-181">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="86adf-181">Syntax</span></span></th>
<th><span data-ttu-id="86adf-182">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="86adf-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86adf-183">Implikuoja</span><span class="sxs-lookup"><span data-stu-id="86adf-183">Implies</span></span></td>
<td><span data-ttu-id="86adf-184">Gaunama teisinga, jei pirmoji sąlyga yra klaidinga, jei antroji sąlyga yra teisinga, arba jei pirmoji sąlyga yra klaidinga, o antroji sąlyga yra teisinga.</span><span class="sxs-lookup"><span data-stu-id="86adf-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="86adf-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="86adf-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-186"><strong>Operatorius:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="86adf-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="86adf-187"><strong>Intarpo ženklas:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="86adf-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86adf-188">Ir</span><span class="sxs-lookup"><span data-stu-id="86adf-188">And</span></span></td>
<td><span data-ttu-id="86adf-189">Gaunama teisinga, jei visos sąlygos yra teisingos.</span><span class="sxs-lookup"><span data-stu-id="86adf-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="86adf-190">Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Teisinga</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="86adf-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="86adf-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-192"><strong>Operatorius:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="86adf-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="86adf-193"><strong>Intarpo ženklas:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="86adf-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86adf-194">Arba</span><span class="sxs-lookup"><span data-stu-id="86adf-194">Or</span></span></td>
<td><span data-ttu-id="86adf-195">Gaunama teisinga, jei bet kuri sąlyga yra teisinga.</span><span class="sxs-lookup"><span data-stu-id="86adf-195">This is true if any condition is true.</span></span> <span data-ttu-id="86adf-196">Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Klaidinga</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="86adf-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="86adf-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-198"><strong>Operatorius:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="86adf-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="86adf-199"><strong>Intarpo ženklas::</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="86adf-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86adf-200">Plius</span><span class="sxs-lookup"><span data-stu-id="86adf-200">Plus</span></span></td>
<td><span data-ttu-id="86adf-201">Naudojant šį operatorių, sąlygos sudedamos.</span><span class="sxs-lookup"><span data-stu-id="86adf-201">This sums its conditions.</span></span> <span data-ttu-id="86adf-202">Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="86adf-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="86adf-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-204"><strong>Operatorius:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="86adf-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="86adf-205"><strong>Intarpo ženklas:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="86adf-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86adf-206">Minus</span><span class="sxs-lookup"><span data-stu-id="86adf-206">Minus</span></span></td>
<td><span data-ttu-id="86adf-207">Naudojant šį operatorių, argumentas paneigiamas.</span><span class="sxs-lookup"><span data-stu-id="86adf-207">This negates its argument.</span></span> <span data-ttu-id="86adf-208">Turi būti nurodyta tik viena sąlyga.</span><span class="sxs-lookup"><span data-stu-id="86adf-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="86adf-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="86adf-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-210"><strong>Operatorius:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="86adf-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="86adf-211"><strong>Intarpo ženklas:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="86adf-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86adf-212">Abs</span><span class="sxs-lookup"><span data-stu-id="86adf-212">Abs</span></span></td>
<td><span data-ttu-id="86adf-213">Naudojant šį operatorių, gaunama absoliučioji sąlygos vertė.</span><span class="sxs-lookup"><span data-stu-id="86adf-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="86adf-214">Turi būti nurodyta tik viena sąlyga.</span><span class="sxs-lookup"><span data-stu-id="86adf-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="86adf-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="86adf-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="86adf-216"><strong>Operatorius:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="86adf-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86adf-217">Laikas</span><span class="sxs-lookup"><span data-stu-id="86adf-217">Times</span></span></td>
<td><span data-ttu-id="86adf-218">Naudojant šį operatorių, gaunamas sąlygų produktas.</span><span class="sxs-lookup"><span data-stu-id="86adf-218">This takes the product of its conditions.</span></span> <span data-ttu-id="86adf-219">Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="86adf-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="86adf-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-221"><strong>Operatorius:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="86adf-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="86adf-222"><strong>Intarpo ženklas:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="86adf-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86adf-223">Laipsnis</span><span class="sxs-lookup"><span data-stu-id="86adf-223">Power</span></span></td>
<td><span data-ttu-id="86adf-224">Naudojant šį operatorių, gaunama eksponentė.</span><span class="sxs-lookup"><span data-stu-id="86adf-224">This takes an exponential.</span></span> <span data-ttu-id="86adf-225">Keliama laipsniu iš dešinės į kairę.</span><span class="sxs-lookup"><span data-stu-id="86adf-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="86adf-226">(Kitaip tariant, šis operatorius susietas su dešine puse.) Todėl <strong>Power[a, b, c]</strong> yra lygu <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="86adf-227"><strong>Power</strong> gali būti naudojamas tik jei laipsnio rodiklis yra teigiama konstanta.</span><span class="sxs-lookup"><span data-stu-id="86adf-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="86adf-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="86adf-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-229"><strong>Operatorius:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="86adf-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="86adf-230"><strong>Intarpo ženklas:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="86adf-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86adf-231">Didžiausia</span><span class="sxs-lookup"><span data-stu-id="86adf-231">Max</span></span></td>
<td><span data-ttu-id="86adf-232">Naudojant šį operatorių, gaunama didžiausia sąlyga.</span><span class="sxs-lookup"><span data-stu-id="86adf-232">This produces the largest condition.</span></span> <span data-ttu-id="86adf-233">Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Begalybė</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="86adf-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="86adf-234">Max[args]</span></span></td>
<td><span data-ttu-id="86adf-235"><strong>Operatorius:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="86adf-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86adf-236">Mažiausia</span><span class="sxs-lookup"><span data-stu-id="86adf-236">Min</span></span></td>
<td><span data-ttu-id="86adf-237">Naudojant šį operatorių, gaunama mažiausia sąlyga.</span><span class="sxs-lookup"><span data-stu-id="86adf-237">This produces the smallest condition.</span></span> <span data-ttu-id="86adf-238">Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Begalybė</strong>.</span><span class="sxs-lookup"><span data-stu-id="86adf-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="86adf-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="86adf-239">Min[args]</span></span></td>
<td><span data-ttu-id="86adf-240"><strong>Operatorius:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="86adf-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86adf-241">Ne</span><span class="sxs-lookup"><span data-stu-id="86adf-241">Not</span></span></td>
<td><span data-ttu-id="86adf-242">Naudojant šį operatorių, gaunama sąlygos loginė priešingybė.</span><span class="sxs-lookup"><span data-stu-id="86adf-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="86adf-243">Turi būti nurodyta tik viena sąlyga.</span><span class="sxs-lookup"><span data-stu-id="86adf-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="86adf-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="86adf-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="86adf-245"><strong>Operatorius:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="86adf-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="86adf-246"><strong>Intarpo ženklas:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="86adf-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86adf-247">Kitos lentelės pavyzdžiuose nurodyta, kaip rašyti intarpo ženklą.</span><span class="sxs-lookup"><span data-stu-id="86adf-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="86adf-248">Intarpo ženklas</span><span class="sxs-lookup"><span data-stu-id="86adf-248">Infix notation</span></span>    | <span data-ttu-id="86adf-249">aprašymas</span><span class="sxs-lookup"><span data-stu-id="86adf-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86adf-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="86adf-250">x + y + z</span></span>         | <span data-ttu-id="86adf-251">Priedas</span><span class="sxs-lookup"><span data-stu-id="86adf-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="86adf-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="86adf-252">x \* y \* z</span></span>       | <span data-ttu-id="86adf-253">Daugyba</span><span class="sxs-lookup"><span data-stu-id="86adf-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="86adf-254">x – y</span><span class="sxs-lookup"><span data-stu-id="86adf-254">x - y</span></span>             | <span data-ttu-id="86adf-255">Dvejetainio nario atimtis atliekama lygiai taip pat, kaip dvejetainio nario sudėtis su neigiamu antru nariu.</span><span class="sxs-lookup"><span data-stu-id="86adf-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="86adf-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="86adf-256">x ^ y ^ z</span></span>         | <span data-ttu-id="86adf-257">Kėlimas laipsniu, kai susieta su dešine puse</span><span class="sxs-lookup"><span data-stu-id="86adf-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="86adf-258">!x</span><span class="sxs-lookup"><span data-stu-id="86adf-258">!x</span></span>                | <span data-ttu-id="86adf-259">Bulio logika ne</span><span class="sxs-lookup"><span data-stu-id="86adf-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="86adf-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="86adf-260">x -: y</span></span>            | <span data-ttu-id="86adf-261">Bulio logikos implikacija</span><span class="sxs-lookup"><span data-stu-id="86adf-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="86adf-262">x</span><span class="sxs-lookup"><span data-stu-id="86adf-262">x</span></span> | <span data-ttu-id="86adf-263">y</span><span class="sxs-lookup"><span data-stu-id="86adf-263">y</span></span> | <span data-ttu-id="86adf-264">z</span><span class="sxs-lookup"><span data-stu-id="86adf-264">z</span></span>         | <span data-ttu-id="86adf-265">Bulio logika ar</span><span class="sxs-lookup"><span data-stu-id="86adf-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="86adf-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="86adf-266">x & y & z</span></span>         | <span data-ttu-id="86adf-267">Būlio logika ir</span><span class="sxs-lookup"><span data-stu-id="86adf-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="86adf-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="86adf-268">x == y == z</span></span>       | <span data-ttu-id="86adf-269">Lygybė</span><span class="sxs-lookup"><span data-stu-id="86adf-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="86adf-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="86adf-270">x != y != z</span></span>       | <span data-ttu-id="86adf-271">Ypatingas</span><span class="sxs-lookup"><span data-stu-id="86adf-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="86adf-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="86adf-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="86adf-273">Mažesnis nei</span><span class="sxs-lookup"><span data-stu-id="86adf-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="86adf-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="86adf-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="86adf-275">Didesnis nei</span><span class="sxs-lookup"><span data-stu-id="86adf-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="86adf-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="86adf-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="86adf-277">Mažiau arba lygu</span><span class="sxs-lookup"><span data-stu-id="86adf-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="86adf-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="86adf-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="86adf-279">Daugiau arba lygu</span><span class="sxs-lookup"><span data-stu-id="86adf-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="86adf-280">(x)</span><span class="sxs-lookup"><span data-stu-id="86adf-280">(x)</span></span>               | <span data-ttu-id="86adf-281">Skliausteliuose perrašomas numatytasis pirmumas.</span><span class="sxs-lookup"><span data-stu-id="86adf-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="86adf-282">Kodėl išraiškos apribojimai teisingai nepatvirtinami?</span><span class="sxs-lookup"><span data-stu-id="86adf-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="86adf-283">Produkto konfigūracijos modelyje negalite naudoti rezervuotų raktažodžių kaip atributų, komponentų ar pakomponenčių sprendimo priemonės pavadinimų.</span><span class="sxs-lookup"><span data-stu-id="86adf-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="86adf-284">Toliau pateikiamas rezervuotų raktažodžių, kuriuos galite naudoti, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="86adf-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="86adf-285">Lubos</span><span class="sxs-lookup"><span data-stu-id="86adf-285">Ceiling</span></span>
-   <span data-ttu-id="86adf-286">Elementas</span><span class="sxs-lookup"><span data-stu-id="86adf-286">Element</span></span>
-   <span data-ttu-id="86adf-287">Lygu</span><span class="sxs-lookup"><span data-stu-id="86adf-287">Equal</span></span>
-   <span data-ttu-id="86adf-288">Grindys</span><span class="sxs-lookup"><span data-stu-id="86adf-288">Floor</span></span>
-   <span data-ttu-id="86adf-289">Jei</span><span class="sxs-lookup"><span data-stu-id="86adf-289">If</span></span>
-   <span data-ttu-id="86adf-290">Mažiau</span><span class="sxs-lookup"><span data-stu-id="86adf-290">Less</span></span>
-   <span data-ttu-id="86adf-291">Didesnis</span><span class="sxs-lookup"><span data-stu-id="86adf-291">Greater</span></span>
-   <span data-ttu-id="86adf-292">Implikuoja</span><span class="sxs-lookup"><span data-stu-id="86adf-292">Implies</span></span>
-   <span data-ttu-id="86adf-293">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86adf-293">Log</span></span>
-   <span data-ttu-id="86adf-294">Maks.</span><span class="sxs-lookup"><span data-stu-id="86adf-294">Max</span></span>
-   <span data-ttu-id="86adf-295">Min.</span><span class="sxs-lookup"><span data-stu-id="86adf-295">Min</span></span>
-   <span data-ttu-id="86adf-296">Minusas</span><span class="sxs-lookup"><span data-stu-id="86adf-296">Minus</span></span>
-   <span data-ttu-id="86adf-297">Plius</span><span class="sxs-lookup"><span data-stu-id="86adf-297">Plus</span></span>
-   <span data-ttu-id="86adf-298">Galia</span><span class="sxs-lookup"><span data-stu-id="86adf-298">Power</span></span>
-   <span data-ttu-id="86adf-299">Laikai</span><span class="sxs-lookup"><span data-stu-id="86adf-299">Times</span></span>
-   <span data-ttu-id="86adf-300">Tarpsnis</span><span class="sxs-lookup"><span data-stu-id="86adf-300">Slot</span></span>
-   <span data-ttu-id="86adf-301">Modelis</span><span class="sxs-lookup"><span data-stu-id="86adf-301">Model</span></span>
-   <span data-ttu-id="86adf-302">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="86adf-302">Decision</span></span>
-   <span data-ttu-id="86adf-303">Tikslas</span><span class="sxs-lookup"><span data-stu-id="86adf-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="86adf-304">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="86adf-304">See also</span></span>
--------

<span data-ttu-id="86adf-305">[Išraiškos apribojimo kūrimas (užduočių vedlys)(tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="86adf-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="86adf-306">Skaičiavimo įtraukimas į produkto konfigūravimo modelį (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="86adf-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




