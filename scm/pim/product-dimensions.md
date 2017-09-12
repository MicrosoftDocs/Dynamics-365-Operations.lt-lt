---
title: "Produktų dimensijos"
description: "Produktų dimensijos yra keturios – Spalva, Konfigūracija, Dydis ir Stilius. Produktų dimensijos jungiamos į dimensijų grupes, o dimensijų grupės priskiriamos bendriesiems produktams. Produktų dimensijų kombinacijomis nustatoma, kaip apibrėžiami produktų variantai."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 93dcf6cd8b2b3b906fca2494fbf5e47553e69e1b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="product-dimensions"></a><span data-ttu-id="a81bf-105">Produktų dimensijos</span><span class="sxs-lookup"><span data-stu-id="a81bf-105">Product dimensions</span></span>

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


<span data-ttu-id="a81bf-106">Produktų dimensijos yra keturios – Spalva, Konfigūracija, Dydis ir Stilius.</span><span class="sxs-lookup"><span data-stu-id="a81bf-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="a81bf-107">Produktų dimensijos jungiamos į dimensijų grupes, o dimensijų grupės priskiriamos bendriesiems produktams.</span><span class="sxs-lookup"><span data-stu-id="a81bf-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="a81bf-108">Produktų dimensijų kombinacijomis nustatoma, kaip apibrėžiami produktų variantai.</span><span class="sxs-lookup"><span data-stu-id="a81bf-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="a81bf-109">Produkto dimensijos – tai charakteristikos, naudojamos produkto variantui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a81bf-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="a81bf-110">Galite naudoti produkto dimensijų derinius produkto variantams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a81bf-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="a81bf-111">Norėdami sukurti produkto variantą, turite nustatyti bent vieną bendrojo produkto dimensiją.</span><span class="sxs-lookup"><span data-stu-id="a81bf-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="a81bf-112">Produkto variantai</span><span class="sxs-lookup"><span data-stu-id="a81bf-112">Product variants</span></span>
----------------

<span data-ttu-id="a81bf-113">Produkto variantai taip pat vadinami prekėmis.</span><span class="sxs-lookup"><span data-stu-id="a81bf-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="a81bf-114">Prekė – tai materialus produktas, kuris nėra apibūdinamas visiškai taip pat, kaip paslauga.</span><span class="sxs-lookup"><span data-stu-id="a81bf-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="a81bf-115">Taip pat galima nustatyti bendrąjį produktą naudojant tipą Paslauga.</span><span class="sxs-lookup"><span data-stu-id="a81bf-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="a81bf-116">Naudodami tipą Paslauga, galite nurodyti produkto variantus, kuriuose yra paslaugų.</span><span class="sxs-lookup"><span data-stu-id="a81bf-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="a81bf-117">Pavyzdžiui, galite nurodyti konsultacinio darbo bendrąjį produktą bei vyresniųjų ir jaunesniųjų konsultantų atliekamo darbo produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="a81bf-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="a81bf-118">Produktų dimensijos</span><span class="sxs-lookup"><span data-stu-id="a81bf-118">Product dimensions</span></span>
<span data-ttu-id="a81bf-119">Galimos šios produktų dimensijos: Konfigūracija, Spalva, Dydis ir Stilius.</span><span class="sxs-lookup"><span data-stu-id="a81bf-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="a81bf-120">Produkto variantas gali būti kuriamas pagal produkto dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="a81bf-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="a81bf-121">Produkto dimensijų vertes, pvz., Dydis, Spalva ir Stilius, galima sukurti puslapiuose **Dydis**, **Spalva** ir **Stilius**, kuriuos galima pasiekti iš šių vietų: **Produkto informacijos valdymas** &gt; **Sąranka** &gt; **Dimensijų ir variantų grupės** &gt; **Dydžiai / Spalvos / Stiliai**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="a81bf-122">Konfigūracijos dimensijos produkto dimensijų vertės paprastai kuriamos naudojant produkto konfigūratorių arba dimensijomis pagrįstą konfigūratorių.</span><span class="sxs-lookup"><span data-stu-id="a81bf-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="a81bf-123">Produkto dimensijos taip pat gali būti kuriamos ir tvarkomos puslapyje **Produktų dimensijos**, kurį galima pasiekti šiose vietose:</span><span class="sxs-lookup"><span data-stu-id="a81bf-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="a81bf-124">Spustelėkite **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Bendrieji produktai**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="a81bf-125">Dalyje **Veiksmų sritis** spustelėkite **Produktų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="a81bf-126">Spustelėkite **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Visi produktai ir bendrieji produktai**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="a81bf-127">Pasirinkite bendrąjį produktą.</span><span class="sxs-lookup"><span data-stu-id="a81bf-127">Select a product master.</span></span> <span data-ttu-id="a81bf-128">Dalyje **Veiksmų sritis** spustelėkite **Produktų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="a81bf-129">Spustelėkite **Produkto informacijos valdymas** &gt; **Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="a81bf-130">Pasirinkite bendrąjį produktą.</span><span class="sxs-lookup"><span data-stu-id="a81bf-130">Select a product master.</span></span> <span data-ttu-id="a81bf-131">Dalyje **Veiksmų sritis** spustelėkite **Produktas**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="a81bf-132">Grupėje **Bendrasis produktas** spustelėkite **Produktų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="a81bf-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="a81bf-133">Variantų, kuriuos galite sukurti prekei, kiekis ribojamas pagal galimų produkto dimensijų derinių kiekį.</span><span class="sxs-lookup"><span data-stu-id="a81bf-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>
| <span data-ttu-id="a81bf-134">**Patarimas**</span><span class="sxs-lookup"><span data-stu-id="a81bf-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a81bf-135">Pavyzdžiui, užsakymo eilutėje naudodami produktą, pasirinkę produkto dimensijas identifikuosite norimą naudoti produkto variantą.</span><span class="sxs-lookup"><span data-stu-id="a81bf-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="a81bf-136">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a81bf-136">Example</span></span>
<span data-ttu-id="a81bf-137">Įmonė parduoda džinsus.</span><span class="sxs-lookup"><span data-stu-id="a81bf-137">A company sells denim jeans.</span></span> <span data-ttu-id="a81bf-138">Prekei (džinsams) apibūdinti naudojamos produktų dimensijos Spalva ir Dydis.</span><span class="sxs-lookup"><span data-stu-id="a81bf-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="a81bf-139">Parduodami trijų skirtingų spalvų ir šešių skirtingų dydžių džinsai.</span><span class="sxs-lookup"><span data-stu-id="a81bf-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="a81bf-140">Spalvos: mėlyna, juoda, ruda Dydžiai: XS, S, M, L, XL, XXL Ne visi dydžiai galimi visų trijų spalvų.</span><span class="sxs-lookup"><span data-stu-id="a81bf-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="a81bf-141">Jei būtų galimi visi deriniai, būtų sukurta 18 skirtingų tipų džinsų.</span><span class="sxs-lookup"><span data-stu-id="a81bf-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="a81bf-142">Šiame pavyzdyje sukurti tik šie devyni produkto variantų deriniai.</span><span class="sxs-lookup"><span data-stu-id="a81bf-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="a81bf-143">Spalva</span><span class="sxs-lookup"><span data-stu-id="a81bf-143">Color</span></span> | <span data-ttu-id="a81bf-144">Dydis</span><span class="sxs-lookup"><span data-stu-id="a81bf-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="a81bf-145">Mėlyna</span><span class="sxs-lookup"><span data-stu-id="a81bf-145">Blue</span></span>  | <span data-ttu-id="a81bf-146">XS</span><span class="sxs-lookup"><span data-stu-id="a81bf-146">XS</span></span>   |
| <span data-ttu-id="a81bf-147">Mėlyna</span><span class="sxs-lookup"><span data-stu-id="a81bf-147">Blue</span></span>  | <span data-ttu-id="a81bf-148">Š.</span><span class="sxs-lookup"><span data-stu-id="a81bf-148">S</span></span>    |
| <span data-ttu-id="a81bf-149">Mėlyna</span><span class="sxs-lookup"><span data-stu-id="a81bf-149">Blue</span></span>  | <span data-ttu-id="a81bf-150">P</span><span class="sxs-lookup"><span data-stu-id="a81bf-150">M</span></span>    |
| <span data-ttu-id="a81bf-151">Juoda</span><span class="sxs-lookup"><span data-stu-id="a81bf-151">Black</span></span> | <span data-ttu-id="a81bf-152">P</span><span class="sxs-lookup"><span data-stu-id="a81bf-152">M</span></span>    |
| <span data-ttu-id="a81bf-153">Juoda</span><span class="sxs-lookup"><span data-stu-id="a81bf-153">Black</span></span> | <span data-ttu-id="a81bf-154">L</span><span class="sxs-lookup"><span data-stu-id="a81bf-154">L</span></span>    |
| <span data-ttu-id="a81bf-155">Juoda</span><span class="sxs-lookup"><span data-stu-id="a81bf-155">Black</span></span> | <span data-ttu-id="a81bf-156">XL</span><span class="sxs-lookup"><span data-stu-id="a81bf-156">XL</span></span>   |
| <span data-ttu-id="a81bf-157">Ruda</span><span class="sxs-lookup"><span data-stu-id="a81bf-157">Brown</span></span> | <span data-ttu-id="a81bf-158">L</span><span class="sxs-lookup"><span data-stu-id="a81bf-158">L</span></span>    |
| <span data-ttu-id="a81bf-159">Ruda</span><span class="sxs-lookup"><span data-stu-id="a81bf-159">Brown</span></span> | <span data-ttu-id="a81bf-160">XL</span><span class="sxs-lookup"><span data-stu-id="a81bf-160">XL</span></span>   |
| <span data-ttu-id="a81bf-161">Ruda</span><span class="sxs-lookup"><span data-stu-id="a81bf-161">Brown</span></span> | <span data-ttu-id="a81bf-162">XXL</span><span class="sxs-lookup"><span data-stu-id="a81bf-162">XXL</span></span>  |






