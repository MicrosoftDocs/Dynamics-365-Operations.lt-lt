---
title: "Produkto variantų numerių ir pavadinimų nomenklatūra"
description: "Šioje temoje aprašoma, kaip nustatyti produkto numerių nomenklatūrą, norint pakeisti fiksuotą [bendrojo produkto numeris – konfigūracija – dydis – spalva – stilius] formatą. Naujojoje nomenklatūroje naudojamas tikslinis formatas, kuris apima bendrojo produkto numerį, aktyvias produkto dimensijas ir pasirinktus teksto skyriklius. Taip pat galite kurti produkto pavadinimų nomenklatūrą. Galiausiai galite kurti nomenklatūrą, norėdami nustatyti konfigūracijas, kurias sukūrė apribojimais pagrįstas produkto konfigūratorius. Į šias nomenklatūras galima įtraukti pasirinktus atributus."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="35ce1-107">Produkto variantų numerių ir pavadinimų nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="35ce1-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="35ce1-108">Šioje temoje aprašoma, kaip nustatyti produkto numerių nomenklatūrą, norint pakeisti fiksuotą [bendrojo produkto numeris – konfigūracija – dydis – spalva – stilius] formatą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="35ce1-109">Naujojoje nomenklatūroje naudojamas tikslinis formatas, kuris apima bendrojo produkto numerį, aktyvias produkto dimensijas ir pasirinktus teksto skyriklius.</span><span class="sxs-lookup"><span data-stu-id="35ce1-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="35ce1-110">Taip pat galite kurti produkto pavadinimų nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="35ce1-111">Galiausiai galite kurti nomenklatūrą, norėdami nustatyti konfigūracijas, kurias sukūrė apribojimais pagrįstas produkto konfigūratorius.</span><span class="sxs-lookup"><span data-stu-id="35ce1-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="35ce1-112">Į šias nomenklatūras galima įtraukti pasirinktus atributus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="35ce1-113">Naujoji produkto variantų numerių ir produkto variantų pavadinimų nomenklatūra suteikia galimybę į produkto variantų identifikatorius įtraukti segmentus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="35ce1-114">Šie segmentai gali būti bendrojo produkto numeris ir pavadinimas, produkto dimensijų ID ir pavadinimai, numeracijos, teksto konstantos ir atributai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="35ce1-115">Naudodami šią funkciją galite greitai rasti konkretų produkto variantą, kai kuriate pardavimo užsakymą arba pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="35ce1-116">Produkto variantų numerių ir produkto variantų pavadinimų nomenklatūras galite kurti naudodami puslapį **Produkto nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="35ce1-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="35ce1-117">Norėdami atidaryti šį puslapį, spustelėkite **Produkto informacijos valdymas** &gt; **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="35ce1-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="35ce1-118">Iš anksto apibrėžtų produkto variantų nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="35ce1-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="35ce1-119">Pagrindinių produktų variantai generuojami pagal vieną iš trijų konfigūravimo technologijų.</span><span class="sxs-lookup"><span data-stu-id="35ce1-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="35ce1-120">Iš anksto apibrėžti variantai</span><span class="sxs-lookup"><span data-stu-id="35ce1-120">Predefined variants</span></span>
-   <span data-ttu-id="35ce1-121">Pagrįsti apribojimais</span><span class="sxs-lookup"><span data-stu-id="35ce1-121">Constraint-based</span></span>
-   <span data-ttu-id="35ce1-122">Pagrįsti dimensijomis</span><span class="sxs-lookup"><span data-stu-id="35ce1-122">Dimension-based</span></span>

<span data-ttu-id="35ce1-123">Kiekvienas produkto variantas turi numerį ir pavadinimą, o produkto variantų identifikavimo nomenklatūros suteikia galimybę pasirinkti segmentus, kurie bus įtraukti į kiekvieno produkto varianto numerį arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="35ce1-124">Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="35ce1-125">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="35ce1-125">Product master number</span></span>
-   <span data-ttu-id="35ce1-126">Bendrojo produkto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-126">Product master name</span></span>
-   <span data-ttu-id="35ce1-127">Numeracijos reikšmė</span><span class="sxs-lookup"><span data-stu-id="35ce1-127">Number sequence value</span></span>
-   <span data-ttu-id="35ce1-128">Teksto konstanta</span><span class="sxs-lookup"><span data-stu-id="35ce1-128">Text constant</span></span>
-   <span data-ttu-id="35ce1-129">Produktų dimensijos</span><span class="sxs-lookup"><span data-stu-id="35ce1-129">Product dimensions</span></span>
    -   <span data-ttu-id="35ce1-130">Konfigūracijos ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="35ce1-131">Spalvos ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-131">Color ID or name</span></span>
    -   <span data-ttu-id="35ce1-132">Dydžio ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-132">Size ID or name</span></span>
    -   <span data-ttu-id="35ce1-133">Stiliaus ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-133">Style ID or name</span></span>

<span data-ttu-id="35ce1-134">Apibrėžus produkto variantų identifikavimo numerių nomenklatūrą, ją galima susieti su produkto dimensijų grupe.</span><span class="sxs-lookup"><span data-stu-id="35ce1-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="35ce1-135">Tada visiems bendriesiems produktams, nurodantiems šią produkto dimensijų grupę, bus priskirti produkto variantų numeriai, atsižvelgiant į nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="35ce1-136">Tačiau produkto variantų pavadinimų nomenklatūrų negalima susieti su produkto dimensijų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="35ce1-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="35ce1-137">Taip pat produkto variantų identifikavimo nomenklatūrą galite tiesiogiai priskirti bendrajam produktui.</span><span class="sxs-lookup"><span data-stu-id="35ce1-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="35ce1-138">Šiuo atveju produkto variantams, kurie priklauso bendrajam produktui, bus priskirti produkto variantų numeriai ir pavadinimai, atsižvelgiant į nomenklatūras.</span><span class="sxs-lookup"><span data-stu-id="35ce1-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="35ce1-139">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="35ce1-139">Example</span></span>

<span data-ttu-id="35ce1-140">Gaminami trijų dydžių (S, M, L), keturių spalvų (raudona, žalia, mėlyna, geltona) ir dviejų tipų (Polo, V) marškinėliai (TS1234).</span><span class="sxs-lookup"><span data-stu-id="35ce1-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="35ce1-141">Todėl galimi 24 produkto variantai (= 3 x 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="35ce1-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="35ce1-142">Galite kurti produkto variantų numerių nomenklatūrą, kurioje yra toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="35ce1-143">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="35ce1-143">Product master number</span></span>
2.  <span data-ttu-id="35ce1-144">Teksto konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="35ce1-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="35ce1-145">Spalva</span><span class="sxs-lookup"><span data-stu-id="35ce1-145">Color</span></span>
4.  <span data-ttu-id="35ce1-146">Teksto konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="35ce1-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="35ce1-147">Dydis</span><span class="sxs-lookup"><span data-stu-id="35ce1-147">Size</span></span>
6.  <span data-ttu-id="35ce1-148">Teksto konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="35ce1-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="35ce1-149">Stilius</span><span class="sxs-lookup"><span data-stu-id="35ce1-149">Style</span></span>

<span data-ttu-id="35ce1-150">Šiuo atveju raudonų S dydžio Polo marškinėlių produkto varianto numeris bus: TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="35ce1-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="35ce1-151">Konfigūravimo pagal apribojimus nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="35ce1-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="35ce1-152">Atliekant konfigūravimą pagal apribojimus galima kurti specialią konfigūracijos produkto dimensijos nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="35ce1-153">Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="35ce1-154">Numeracijos reikšmė</span><span class="sxs-lookup"><span data-stu-id="35ce1-154">Number sequence value</span></span>
-   <span data-ttu-id="35ce1-155">Teksto konstanta</span><span class="sxs-lookup"><span data-stu-id="35ce1-155">Text constant</span></span>
-   <span data-ttu-id="35ce1-156">Atributo vertė</span><span class="sxs-lookup"><span data-stu-id="35ce1-156">Attribute value</span></span>

<span data-ttu-id="35ce1-157">Kiekvienam produkto konfigūracijos modelio komponentui gali būti priskirta atskira konfigūracijos nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="35ce1-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="35ce1-158">Galima naudoti tik komponentui priklausančius atributus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="35ce1-159">Subkomponentų arba vartotojo reikalavimų atributų naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="35ce1-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="35ce1-160">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="35ce1-160">Example</span></span>

<span data-ttu-id="35ce1-161">Produkto konfigūracijos modeliui priskiriamas šakninis komponentas su dviem atributais.</span><span class="sxs-lookup"><span data-stu-id="35ce1-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="35ce1-162">Medžiagos (plastmasė, medis, plienas)</span><span class="sxs-lookup"><span data-stu-id="35ce1-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="35ce1-163">Ilgis (10... 100)</span><span class="sxs-lookup"><span data-stu-id="35ce1-163">Length (10...100)</span></span>

<span data-ttu-id="35ce1-164">Galite kurti konfigūracijos nomenklatūrą, kurioje yra toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="35ce1-165">Atributo reikšmė: medžiagos</span><span class="sxs-lookup"><span data-stu-id="35ce1-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="35ce1-166">Teksto konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="35ce1-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="35ce1-167">Atributo reikšmė: ilgis</span><span class="sxs-lookup"><span data-stu-id="35ce1-167">Attribute value: Length</span></span>

<span data-ttu-id="35ce1-168">Šiuo atveju medžiagos iš medžio, kurios ilgis 78, konfigūracijos ID bus: WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="35ce1-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="35ce1-169">Konfigūravimo pagal dimensijas nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="35ce1-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="35ce1-170">Atliekant konfigūravimą pagal dimensijas galima kurti specialią konfigūracijos produkto dimensijos nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="35ce1-171">Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="35ce1-172">Numeracijos reikšmė</span><span class="sxs-lookup"><span data-stu-id="35ce1-172">Number sequence value</span></span>
-   <span data-ttu-id="35ce1-173">Teksto konstanta</span><span class="sxs-lookup"><span data-stu-id="35ce1-173">Text constant</span></span>
-   <span data-ttu-id="35ce1-174">Konfigūracijos grupės prekė</span><span class="sxs-lookup"><span data-stu-id="35ce1-174">Configuration group item</span></span>

<span data-ttu-id="35ce1-175">Galima nurodyti konfigūracijos nomenklatūrą, skirtą komplektavimo specifikacijai (KS).</span><span class="sxs-lookup"><span data-stu-id="35ce1-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="35ce1-176">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="35ce1-176">Example</span></span>

<span data-ttu-id="35ce1-177">KS yra keturios KS eilutes, suskirstytos į dvi konfigūracijų grupes.</span><span class="sxs-lookup"><span data-stu-id="35ce1-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="35ce1-178">KS eilutė: M0007, standartinė spintelė</span><span class="sxs-lookup"><span data-stu-id="35ce1-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="35ce1-179">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="35ce1-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="35ce1-180">KS eilutė: M0008, aukštos kokybės spintelė</span><span class="sxs-lookup"><span data-stu-id="35ce1-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="35ce1-181">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="35ce1-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="35ce1-182">KS eilutė: M0021, priekinės grotelės iš audinio</span><span class="sxs-lookup"><span data-stu-id="35ce1-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="35ce1-183">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="35ce1-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="35ce1-184">KS eilutė: M0022, priekinės grotelės iš metalo</span><span class="sxs-lookup"><span data-stu-id="35ce1-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="35ce1-185">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="35ce1-185">Configuration group: Front grill</span></span>

<span data-ttu-id="35ce1-186">Galite kurti konfigūracijos nomenklatūrą, kurioje yra toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="35ce1-187">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="35ce1-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="35ce1-188">Teksto konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="35ce1-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="35ce1-189">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="35ce1-189">Configuration group: Front grill</span></span>

<span data-ttu-id="35ce1-190">Šiuo atveju standartinės spintelės su priekinėmis grotelėmis iš audinio konfigūracijos ID bus: M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="35ce1-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="35ce1-191">Produkto variantų ir konfigūracijų derinio nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="35ce1-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="35ce1-192">Kai naudojate konfigūravimo pagal apribojimus arba konfigūravimo pagal dimensijas technologiją, norėdami konfigūruoti pagrindinio produkto variantus, į produkto variantų numerius gali būti įtraukta konfigūracijos dimensijos nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="35ce1-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="35ce1-193">Norėdami konfigūruoti variantus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="35ce1-194">Puslapyje **Produkto nomenklatūra** nurodykite produkto variantų numerių nomenklatūrą, į kurią įtraukta konfigūracijos dimensija.</span><span class="sxs-lookup"><span data-stu-id="35ce1-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="35ce1-195">Priskirkite nomenklatūrą produkto dimensijų grupei su konfigūracijos dimensija.</span><span class="sxs-lookup"><span data-stu-id="35ce1-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="35ce1-196">Nurodykite komponentų arba KS konfigūracijos nomenklatūrą, kuri bus naudojama konfigūruojant produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="35ce1-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="35ce1-197">Taip pat galite kurti produkto variantų pavadinimų nomenklatūras.</span><span class="sxs-lookup"><span data-stu-id="35ce1-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="35ce1-198">Produkto variantų pavadinimus galima konfigūruoti ir įtraukti konfigūracijos ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="35ce1-199">Konfigūravimo pagal apribojimus pavyzdys</span><span class="sxs-lookup"><span data-stu-id="35ce1-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="35ce1-200">Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="35ce1-201">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="35ce1-201">Product master number</span></span>
2.  <span data-ttu-id="35ce1-202">Teksto konstanta: "\_"</span><span class="sxs-lookup"><span data-stu-id="35ce1-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="35ce1-203">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-203">Configuration</span></span>

<span data-ttu-id="35ce1-204">Konfigūracijos nomenklatūrą sudaro toliau pateikti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="35ce1-205">Atributo reikšmė: medžiagos</span><span class="sxs-lookup"><span data-stu-id="35ce1-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="35ce1-206">Teksto konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="35ce1-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="35ce1-207">Atributo reikšmė: ilgis</span><span class="sxs-lookup"><span data-stu-id="35ce1-207">Attribute value: Length</span></span>

<span data-ttu-id="35ce1-208">Galite įvesti toliau nurodytas segmentų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="35ce1-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="35ce1-209">Bendrojo produkto numeris = **M0099**</span><span class="sxs-lookup"><span data-stu-id="35ce1-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="35ce1-210">Medžiagos = **plastmasė**</span><span class="sxs-lookup"><span data-stu-id="35ce1-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="35ce1-211">Ilgis = **12**</span><span class="sxs-lookup"><span data-stu-id="35ce1-211">Length = **12**</span></span>

<span data-ttu-id="35ce1-212">Šiuo atveju produkto varianto numeris bus: M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="35ce1-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="35ce1-213">Konfigūravimo pagal dimensijas pavyzdys</span><span class="sxs-lookup"><span data-stu-id="35ce1-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="35ce1-214">Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="35ce1-215">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="35ce1-215">Product master number</span></span>
2.  <span data-ttu-id="35ce1-216">Teksto konstanta: "//"</span><span class="sxs-lookup"><span data-stu-id="35ce1-216">Text constant "//"</span></span>
3.  <span data-ttu-id="35ce1-217">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-217">Configuration</span></span>

<span data-ttu-id="35ce1-218">Konfigūracijos nomenklatūrą sudaro toliau pateikti segmentai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="35ce1-219">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="35ce1-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="35ce1-220">Teksto konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="35ce1-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="35ce1-221">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="35ce1-221">Configuration group: Front grill</span></span>

<span data-ttu-id="35ce1-222">Galite įvesti toliau nurodytas segmentų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="35ce1-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="35ce1-223">Bendrojo produkto numeris = **D0123**</span><span class="sxs-lookup"><span data-stu-id="35ce1-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="35ce1-224">Spintelė = **M0008**</span><span class="sxs-lookup"><span data-stu-id="35ce1-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="35ce1-225">Priekinės grotelės = **M0022**</span><span class="sxs-lookup"><span data-stu-id="35ce1-225">Front grill = **M0022**</span></span>

<span data-ttu-id="35ce1-226">Šiuo atveju produkto varianto numeris bus: D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="35ce1-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="35ce1-227">Numeravimo nesuderinamumai</span><span class="sxs-lookup"><span data-stu-id="35ce1-227">Numbering conflicts</span></span>
<span data-ttu-id="35ce1-228">Kai kuriais atvejais naudojant nustatytą produkto variantų numerių nomenklatūrą nebus kuriami unikalūs produkto variantų numeriai.</span><span class="sxs-lookup"><span data-stu-id="35ce1-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="35ce1-229">Pavyzdžiui, produkto variantų numeriai nebus unikalūs, jei viena aktyvi produkto dimensija nėra įtraukta į bendrojo produkto, kuriame naudojama apibrėžta variantų konfigūravimo technologija, nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="35ce1-230">Konfliktų sprendimo būdas priklauso nuo konfigūracijos technologijos.</span><span class="sxs-lookup"><span data-stu-id="35ce1-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="35ce1-231">Iš anksto apibrėžti variantai</span><span class="sxs-lookup"><span data-stu-id="35ce1-231">Predefined variants</span></span>

<span data-ttu-id="35ce1-232">Jei automatiškai arba neautomatiškai bandysite generuoti produkto variantus, kurių daugiau nei vienas turės tokį patį produkto varianto numerį, įvyks klaida.</span><span class="sxs-lookup"><span data-stu-id="35ce1-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="35ce1-233">Norėdami to išvengti, turite naudoti visas aktyvias produkto dimensijų grupės produkto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="35ce1-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="35ce1-234">Taip pat galite įtraukti numeraciją ir taip užtikrinti, kad produkto varianto numeriai bus unikalūs.</span><span class="sxs-lookup"><span data-stu-id="35ce1-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="35ce1-235">Konfigūravimas pagal apribojimus</span><span class="sxs-lookup"><span data-stu-id="35ce1-235">Constraint-based configurations</span></span>

<span data-ttu-id="35ce1-236">Priklausomai nuo nomenklatūros, sistema gali bandyti konfigūracijai priskirti ne unikalų produkto varianto numerį.</span><span class="sxs-lookup"><span data-stu-id="35ce1-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="35ce1-237">Tokiu atveju sistema naudos konfigūracijos dimensijos numeraciją kaip produkto varianto numerį ir bus rodomas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="35ce1-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="35ce1-238">Siekiant to išvengti, į nomenklatūrą turėtumėte įtraukti pakankamai atributų ir taip užtikrinti, kad produkto variantų numeriai bus unikalūs.</span><span class="sxs-lookup"><span data-stu-id="35ce1-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="35ce1-239">Taip pat įsitikinkite, kad įjungta komponento parinktis **Naudoti pakartotinai**.</span><span class="sxs-lookup"><span data-stu-id="35ce1-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="35ce1-240">Konfigūravimas pagal dimensijas</span><span class="sxs-lookup"><span data-stu-id="35ce1-240">Dimension-based configurations</span></span>

<span data-ttu-id="35ce1-241">Į konfigūravimo procesą įtrauktas etapas, kurio metu sistema pasiūlys konfigūracijos reikšmę pagal nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="35ce1-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="35ce1-242">Šio etapo metu galite neautomatiškai keisti konfigūracijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="35ce1-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="35ce1-243">Kai įrašote konfigūraciją, sistema patikrins, ar konfigūracijos reikšmė yra unikali.</span><span class="sxs-lookup"><span data-stu-id="35ce1-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="35ce1-244">Jei įvesta vertė nėra unikali, bus rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="35ce1-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="35ce1-245">Turite įvesti unikalią konfigūracijos reikšmę, kad galėtumėte konfigūraciją įrašyti.</span><span class="sxs-lookup"><span data-stu-id="35ce1-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="35ce1-246">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="35ce1-246">See also</span></span>
--------

[<span data-ttu-id="35ce1-247">Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="35ce1-248">Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="35ce1-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


