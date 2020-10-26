---
title: Produkto variantų numerių ir pavadinimų nomenklatūra
description: Šioje temoje aprašoma, kaip nustatyti produkto numerių nomenklatūrą, norint pakeisti fiksuotą [bendrojo produkto numeris – konfigūracija – dydis – spalva – stilius] formatą.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 90c01e4281246d890ef888c56ca137f83e83741c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980488"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="9dabc-103">Produkto variantų numerių ir pavadinimų nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="9dabc-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dabc-104">Šioje temoje aprašoma, kaip nustatyti produkto numerių nomenklatūrą, norint pakeisti fiksuotą [bendrojo produkto numeris – konfigūracija – dydis – spalva – stilius] formatą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="9dabc-105">Naujojoje nomenklatūroje naudojamas tikslinis formatas, kuris apima bendrojo produkto numerį, aktyvias produkto dimensijas ir pasirinktus teksto skyriklius.</span><span class="sxs-lookup"><span data-stu-id="9dabc-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="9dabc-106">Taip pat galite kurti produkto pavadinimų nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="9dabc-107">Galiausiai galite kurti nomenklatūrą, norėdami nustatyti konfigūracijas, kurias sukūrė apribojimais pagrįstas produkto konfigūratorius.</span><span class="sxs-lookup"><span data-stu-id="9dabc-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="9dabc-108">Į šias nomenklatūras galima įtraukti pasirinktus atributus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="9dabc-109">Naujoji produkto variantų numerių ir produkto variantų pavadinimų nomenklatūra suteikia galimybę į produkto variantų identifikatorius įtraukti segmentus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="9dabc-110">Šie segmentai gali būti bendrojo produkto numeris ir pavadinimas, produkto dimensijų ID ir pavadinimai, numeracijos, teksto konstantos ir atributai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="9dabc-111">Naudodami šią funkciją galite greitai rasti konkretų produkto variantą, kai kuriate pardavimo užsakymą arba pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="9dabc-112">Produkto variantų numerių ir produkto variantų pavadinimų nomenklatūras galite kurti naudodami puslapį **Produkto nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="9dabc-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="9dabc-113">Norėdami atidaryti šį puslapį, spustelėkite **Produkto informacijos valdymas** &gt; **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="9dabc-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="9dabc-114">Iš anksto apibrėžtų produkto variantų nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="9dabc-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="9dabc-115">Pagrindinių produktų variantai generuojami pagal vieną iš trijų konfigūravimo technologijų.</span><span class="sxs-lookup"><span data-stu-id="9dabc-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="9dabc-116">Iš anksto apibrėžti variantai</span><span class="sxs-lookup"><span data-stu-id="9dabc-116">Predefined variants</span></span>
-   <span data-ttu-id="9dabc-117">Pagrįsti apribojimais</span><span class="sxs-lookup"><span data-stu-id="9dabc-117">Constraint-based</span></span>
-   <span data-ttu-id="9dabc-118">Pagrįsti dimensijomis</span><span class="sxs-lookup"><span data-stu-id="9dabc-118">Dimension-based</span></span>

<span data-ttu-id="9dabc-119">Kiekvienas produkto variantas turi numerį ir pavadinimą, o produkto variantų identifikavimo nomenklatūros suteikia galimybę pasirinkti segmentus, kurie bus įtraukti į kiekvieno produkto varianto numerį arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="9dabc-120">Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="9dabc-121">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="9dabc-121">Product master number</span></span>
-   <span data-ttu-id="9dabc-122">Bendrojo produkto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-122">Product master name</span></span>
-   <span data-ttu-id="9dabc-123">Numeracijos reikšmė</span><span class="sxs-lookup"><span data-stu-id="9dabc-123">Number sequence value</span></span>
-   <span data-ttu-id="9dabc-124">Teksto konstanta</span><span class="sxs-lookup"><span data-stu-id="9dabc-124">Text constant</span></span>
-   <span data-ttu-id="9dabc-125">Produktų dimensijos</span><span class="sxs-lookup"><span data-stu-id="9dabc-125">Product dimensions</span></span>
    -   <span data-ttu-id="9dabc-126">Konfigūracijos ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="9dabc-127">Spalvos ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-127">Color ID or name</span></span>
    -   <span data-ttu-id="9dabc-128">Dydžio ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-128">Size ID or name</span></span>
    -   <span data-ttu-id="9dabc-129">Stiliaus ID arba pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-129">Style ID or name</span></span>

<span data-ttu-id="9dabc-130">Apibrėžus produkto variantų identifikavimo numerių nomenklatūrą, ją galima susieti su produkto dimensijų grupe.</span><span class="sxs-lookup"><span data-stu-id="9dabc-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="9dabc-131">Tada visiems bendriesiems produktams, nurodantiems šią produkto dimensijų grupę, bus priskirti produkto variantų numeriai, atsižvelgiant į nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="9dabc-132">Tačiau produkto variantų pavadinimų nomenklatūrų negalima susieti su produkto dimensijų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="9dabc-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="9dabc-133">Taip pat produkto variantų identifikavimo nomenklatūrą galite tiesiogiai priskirti bendrajam produktui.</span><span class="sxs-lookup"><span data-stu-id="9dabc-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="9dabc-134">Šiuo atveju produkto variantams, kurie priklauso bendrajam produktui, bus priskirti produkto variantų numeriai ir pavadinimai, atsižvelgiant į nomenklatūras.</span><span class="sxs-lookup"><span data-stu-id="9dabc-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="9dabc-135">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9dabc-135">Example</span></span>

<span data-ttu-id="9dabc-136">Gaminami trijų dydžių (S, M, L), keturių spalvų (raudona, žalia, mėlyna, geltona) ir dviejų tipų (Polo, V) marškinėliai (TS1234).</span><span class="sxs-lookup"><span data-stu-id="9dabc-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="9dabc-137">Todėl galimi 24 produkto variantai (= 3 x 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="9dabc-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="9dabc-138">Galite kurti produkto variantų numerių nomenklatūrą, kurioje yra toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="9dabc-139">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="9dabc-139">Product master number</span></span>
2.  <span data-ttu-id="9dabc-140">Teksto konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="9dabc-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="9dabc-141">Spalva</span><span class="sxs-lookup"><span data-stu-id="9dabc-141">Color</span></span>
4.  <span data-ttu-id="9dabc-142">Teksto konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="9dabc-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="9dabc-143">Dydis</span><span class="sxs-lookup"><span data-stu-id="9dabc-143">Size</span></span>
6.  <span data-ttu-id="9dabc-144">Teksto konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="9dabc-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="9dabc-145">Stilius</span><span class="sxs-lookup"><span data-stu-id="9dabc-145">Style</span></span>

<span data-ttu-id="9dabc-146">Šiuo atveju raudonų S dydžio Polo marškinėlių produkto varianto numeris bus: TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="9dabc-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="9dabc-147">Konfigūravimo pagal apribojimus nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="9dabc-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="9dabc-148">Atliekant konfigūravimą pagal apribojimus galima kurti specialią konfigūracijos produkto dimensijos nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="9dabc-149">Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="9dabc-150">Numeracijos reikšmė</span><span class="sxs-lookup"><span data-stu-id="9dabc-150">Number sequence value</span></span>
-   <span data-ttu-id="9dabc-151">Teksto konstanta</span><span class="sxs-lookup"><span data-stu-id="9dabc-151">Text constant</span></span>
-   <span data-ttu-id="9dabc-152">Atributo vertė</span><span class="sxs-lookup"><span data-stu-id="9dabc-152">Attribute value</span></span>

<span data-ttu-id="9dabc-153">Kiekvienam produkto konfigūracijos modelio komponentui gali būti priskirta atskira konfigūracijos nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="9dabc-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="9dabc-154">Galima naudoti tik komponentui priklausančius atributus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="9dabc-155">Subkomponentų arba vartotojo reikalavimų atributų naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="9dabc-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="9dabc-156">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9dabc-156">Example</span></span>

<span data-ttu-id="9dabc-157">Produkto konfigūracijos modeliui priskiriamas šakninis komponentas su dviem atributais.</span><span class="sxs-lookup"><span data-stu-id="9dabc-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="9dabc-158">Medžiagos (plastmasė, medis, plienas)</span><span class="sxs-lookup"><span data-stu-id="9dabc-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="9dabc-159">Ilgis (10... 100)</span><span class="sxs-lookup"><span data-stu-id="9dabc-159">Length (10...100)</span></span>

<span data-ttu-id="9dabc-160">Galite kurti konfigūracijos nomenklatūrą, kurioje yra toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="9dabc-161">Atributo reikšmė: medžiagos</span><span class="sxs-lookup"><span data-stu-id="9dabc-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="9dabc-162">Teksto konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="9dabc-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="9dabc-163">Atributo reikšmė: ilgis</span><span class="sxs-lookup"><span data-stu-id="9dabc-163">Attribute value: Length</span></span>

<span data-ttu-id="9dabc-164">Šiuo atveju medžiagos iš medžio, kurios ilgis 78, konfigūracijos ID bus: WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="9dabc-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="9dabc-165">Konfigūravimo pagal dimensijas nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="9dabc-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="9dabc-166">Atliekant konfigūravimą pagal dimensijas galima kurti specialią konfigūracijos produkto dimensijos nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="9dabc-167">Puslapyje **Produkto nomenklatūra** galite pasirinkti toliau nurodytus segmentus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="9dabc-168">Numeracijos reikšmė</span><span class="sxs-lookup"><span data-stu-id="9dabc-168">Number sequence value</span></span>
-   <span data-ttu-id="9dabc-169">Teksto konstanta</span><span class="sxs-lookup"><span data-stu-id="9dabc-169">Text constant</span></span>
-   <span data-ttu-id="9dabc-170">Konfigūracijos grupės prekė</span><span class="sxs-lookup"><span data-stu-id="9dabc-170">Configuration group item</span></span>

<span data-ttu-id="9dabc-171">Galima nurodyti konfigūracijos nomenklatūrą, skirtą komplektavimo specifikacijai (KS).</span><span class="sxs-lookup"><span data-stu-id="9dabc-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="9dabc-172">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9dabc-172">Example</span></span>

<span data-ttu-id="9dabc-173">KS yra keturios KS eilutes, suskirstytos į dvi konfigūracijų grupes.</span><span class="sxs-lookup"><span data-stu-id="9dabc-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="9dabc-174">KS eilutė: M0007, standartinė spintelė</span><span class="sxs-lookup"><span data-stu-id="9dabc-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="9dabc-175">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="9dabc-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="9dabc-176">KS eilutė: M0008, aukštos kokybės spintelė</span><span class="sxs-lookup"><span data-stu-id="9dabc-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="9dabc-177">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="9dabc-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="9dabc-178">KS eilutė: M0021, priekinės grotelės iš audinio</span><span class="sxs-lookup"><span data-stu-id="9dabc-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="9dabc-179">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="9dabc-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="9dabc-180">KS eilutė: M0022, priekinės grotelės iš metalo</span><span class="sxs-lookup"><span data-stu-id="9dabc-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="9dabc-181">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="9dabc-181">Configuration group: Front grill</span></span>

<span data-ttu-id="9dabc-182">Galite kurti konfigūracijos nomenklatūrą, kurioje yra toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="9dabc-183">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="9dabc-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="9dabc-184">Teksto konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="9dabc-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="9dabc-185">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="9dabc-185">Configuration group: Front grill</span></span>

<span data-ttu-id="9dabc-186">Šiuo atveju standartinės spintelės su priekinėmis grotelėmis iš audinio konfigūracijos ID bus: M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="9dabc-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="9dabc-187">Produkto variantų ir konfigūracijų derinio nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="9dabc-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="9dabc-188">Kai naudojate konfigūravimo pagal apribojimus arba konfigūravimo pagal dimensijas technologiją, norėdami konfigūruoti pagrindinio produkto variantus, į produkto variantų numerius gali būti įtraukta konfigūracijos dimensijos nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="9dabc-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="9dabc-189">Norėdami konfigūruoti variantus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="9dabc-190">Puslapyje **Produkto nomenklatūra** nurodykite produkto variantų numerių nomenklatūrą, į kurią įtraukta konfigūracijos dimensija.</span><span class="sxs-lookup"><span data-stu-id="9dabc-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="9dabc-191">Priskirkite nomenklatūrą produkto dimensijų grupei su konfigūracijos dimensija.</span><span class="sxs-lookup"><span data-stu-id="9dabc-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="9dabc-192">Nurodykite komponentų arba KS konfigūracijos nomenklatūrą, kuri bus naudojama konfigūruojant produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="9dabc-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="9dabc-193">Taip pat galite kurti produkto variantų pavadinimų nomenklatūras.</span><span class="sxs-lookup"><span data-stu-id="9dabc-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="9dabc-194">Produkto variantų pavadinimus galima konfigūruoti ir įtraukti konfigūracijos ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="9dabc-195">Konfigūravimo pagal apribojimus pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9dabc-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="9dabc-196">Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="9dabc-197">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="9dabc-197">Product master number</span></span>
2.  <span data-ttu-id="9dabc-198">Teksto konstanta: "\_"</span><span class="sxs-lookup"><span data-stu-id="9dabc-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="9dabc-199">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-199">Configuration</span></span>

<span data-ttu-id="9dabc-200">Konfigūracijos nomenklatūrą sudaro toliau pateikti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="9dabc-201">Atributo reikšmė: medžiagos</span><span class="sxs-lookup"><span data-stu-id="9dabc-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="9dabc-202">Teksto konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="9dabc-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="9dabc-203">Atributo reikšmė: ilgis</span><span class="sxs-lookup"><span data-stu-id="9dabc-203">Attribute value: Length</span></span>

<span data-ttu-id="9dabc-204">Galite įvesti toliau nurodytas segmentų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9dabc-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="9dabc-205">Bendrojo produkto numeris = **M0099**</span><span class="sxs-lookup"><span data-stu-id="9dabc-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="9dabc-206">Medžiagos = **plastmasė**</span><span class="sxs-lookup"><span data-stu-id="9dabc-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="9dabc-207">Ilgis = **12**</span><span class="sxs-lookup"><span data-stu-id="9dabc-207">Length = **12**</span></span>

<span data-ttu-id="9dabc-208">Šiuo atveju produkto varianto numeris bus: M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="9dabc-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="9dabc-209">Konfigūravimo pagal dimensijas pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9dabc-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="9dabc-210">Šiame pavyzdyje galite naudoti produkto variantų numerių nomenklatūrą, kurią sudaro toliau nurodyti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="9dabc-211">Bendrojo produkto numeris</span><span class="sxs-lookup"><span data-stu-id="9dabc-211">Product master number</span></span>
2.  <span data-ttu-id="9dabc-212">Teksto konstanta: "//"</span><span class="sxs-lookup"><span data-stu-id="9dabc-212">Text constant "//"</span></span>
3.  <span data-ttu-id="9dabc-213">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-213">Configuration</span></span>

<span data-ttu-id="9dabc-214">Konfigūracijos nomenklatūrą sudaro toliau pateikti segmentai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="9dabc-215">Konfigūracijos grupė: spintelė</span><span class="sxs-lookup"><span data-stu-id="9dabc-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="9dabc-216">Teksto konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="9dabc-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="9dabc-217">Konfigūracijos grupė: priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="9dabc-217">Configuration group: Front grill</span></span>

<span data-ttu-id="9dabc-218">Galite įvesti toliau nurodytas segmentų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9dabc-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="9dabc-219">Bendrojo produkto numeris = **D0123**</span><span class="sxs-lookup"><span data-stu-id="9dabc-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="9dabc-220">Spintelė = **M0008**</span><span class="sxs-lookup"><span data-stu-id="9dabc-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="9dabc-221">Priekinės grotelės = **M0022**</span><span class="sxs-lookup"><span data-stu-id="9dabc-221">Front grill = **M0022**</span></span>

<span data-ttu-id="9dabc-222">Šiuo atveju produkto varianto numeris bus: D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="9dabc-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="9dabc-223">Numeravimo nesuderinamumai</span><span class="sxs-lookup"><span data-stu-id="9dabc-223">Numbering conflicts</span></span>
<span data-ttu-id="9dabc-224">Kai kuriais atvejais naudojant nustatytą produkto variantų numerių nomenklatūrą nebus kuriami unikalūs produkto variantų numeriai.</span><span class="sxs-lookup"><span data-stu-id="9dabc-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="9dabc-225">Pavyzdžiui, produkto variantų numeriai nebus unikalūs, jei viena aktyvi produkto dimensija nėra įtraukta į bendrojo produkto, kuriame naudojama apibrėžta variantų konfigūravimo technologija, nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="9dabc-226">Konfliktų sprendimo būdas priklauso nuo konfigūracijos technologijos.</span><span class="sxs-lookup"><span data-stu-id="9dabc-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="9dabc-227">Iš anksto apibrėžti variantai</span><span class="sxs-lookup"><span data-stu-id="9dabc-227">Predefined variants</span></span>

<span data-ttu-id="9dabc-228">Jei automatiškai arba neautomatiškai bandysite generuoti produkto variantus, kurių daugiau nei vienas turės tokį patį produkto varianto numerį, įvyks klaida.</span><span class="sxs-lookup"><span data-stu-id="9dabc-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="9dabc-229">Norėdami to išvengti, turite naudoti visas aktyvias produkto dimensijų grupės produkto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="9dabc-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="9dabc-230">Taip pat galite įtraukti numeraciją ir taip užtikrinti, kad produkto varianto numeriai bus unikalūs.</span><span class="sxs-lookup"><span data-stu-id="9dabc-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="9dabc-231">Konfigūravimas pagal apribojimus</span><span class="sxs-lookup"><span data-stu-id="9dabc-231">Constraint-based configurations</span></span>

<span data-ttu-id="9dabc-232">Priklausomai nuo nomenklatūros, sistema gali bandyti konfigūracijai priskirti ne unikalų produkto varianto numerį.</span><span class="sxs-lookup"><span data-stu-id="9dabc-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="9dabc-233">Tokiu atveju sistema naudos konfigūracijos dimensijos numeraciją kaip produkto varianto numerį ir bus rodomas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="9dabc-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="9dabc-234">Siekiant to išvengti, į nomenklatūrą turėtumėte įtraukti pakankamai atributų ir taip užtikrinti, kad produkto variantų numeriai bus unikalūs.</span><span class="sxs-lookup"><span data-stu-id="9dabc-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="9dabc-235">Taip pat įsitikinkite, kad įjungta komponento parinktis **Naudoti pakartotinai**.</span><span class="sxs-lookup"><span data-stu-id="9dabc-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="9dabc-236">Konfigūravimas pagal dimensijas</span><span class="sxs-lookup"><span data-stu-id="9dabc-236">Dimension-based configurations</span></span>

<span data-ttu-id="9dabc-237">Į konfigūravimo procesą įtrauktas etapas, kurio metu sistema pasiūlys konfigūracijos reikšmę pagal nomenklatūrą.</span><span class="sxs-lookup"><span data-stu-id="9dabc-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="9dabc-238">Šio etapo metu galite neautomatiškai keisti konfigūracijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9dabc-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="9dabc-239">Kai įrašote konfigūraciją, sistema patikrins, ar konfigūracijos reikšmė yra unikali.</span><span class="sxs-lookup"><span data-stu-id="9dabc-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="9dabc-240">Jei įvesta vertė nėra unikali, bus rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="9dabc-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="9dabc-241">Turite įvesti unikalią konfigūracijos reikšmę, kad galėtumėte konfigūraciją įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9dabc-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9dabc-242">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9dabc-242">Additional resources</span></span>
--------

[<span data-ttu-id="9dabc-243">Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="9dabc-244">Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="9dabc-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

