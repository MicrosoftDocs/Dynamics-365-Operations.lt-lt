---
title: Produkto varianto matavimo vieneto konvertavimas
description: Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935104"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="a63d1-103">Produkto varianto matavimo vieneto konvertavimas</span><span class="sxs-lookup"><span data-stu-id="a63d1-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a63d1-104">Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="a63d1-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="a63d1-105">Joje pateikiamas nustatymo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a63d1-105">It includes an example of the setup.</span></span>

<span data-ttu-id="a63d1-106">Ši funkcija leidžia įmonėms nustatyti skirtingų vienetų konvertavimą tarp to paties produkto variantų.</span><span class="sxs-lookup"><span data-stu-id="a63d1-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="a63d1-107">Šioje temoje naudojamas toliau pateiktas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a63d1-107">The following example is used in this topic.</span></span> <span data-ttu-id="a63d1-108">Įmonė parduoda mažo, vidutinio, didelio ir labai didelio dydžio marškinėlius.</span><span class="sxs-lookup"><span data-stu-id="a63d1-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="a63d1-109">Marškinėliai apibrėžiami kaip produktas, o skirtingi dydžiai – kaip produkto variantai.</span><span class="sxs-lookup"><span data-stu-id="a63d1-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="a63d1-110">Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.</span><span class="sxs-lookup"><span data-stu-id="a63d1-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="a63d1-111">Įmonė nori sekti skirtingų variantų marškinėlius pagal vienetą **Vienetai**, tačiau pardavinėja marškinėlius pagal vienetą **Dėžės**.</span><span class="sxs-lookup"><span data-stu-id="a63d1-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="a63d1-112">Konvertavimo santykis tarp atsargų vieneto ir pardavimo vieneto yra 1 dėžė = 5 vienetai, išskyrus labai didelio dydžio variantą, kur santykis yra 1 dėžė = 4 vienetai.</span><span class="sxs-lookup"><span data-stu-id="a63d1-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="a63d1-113">Nustatyti produkto varianto vieneto konvertavimą</span><span class="sxs-lookup"><span data-stu-id="a63d1-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="a63d1-114">Produkto variantus galima kurti tik produktams, kurių **Produkto potipis**: **Bendrasis produktas**.</span><span class="sxs-lookup"><span data-stu-id="a63d1-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="a63d1-115">Daugiau informacijos žr. [Bendrojo produkto kūrimas](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="a63d1-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="a63d1-116">Funkcija neįgalinta produktams, kurie nustatyti esamo svorio procesams.</span><span class="sxs-lookup"><span data-stu-id="a63d1-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="a63d1-117">Sukūrus bendrąjį produktą su išleistų produktų variantais, galima nustatyti vieneto konvertavimą pagal variantus.</span><span class="sxs-lookup"><span data-stu-id="a63d1-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="a63d1-118">Galite rasti meniu elementą vieneto konvertavimo puslapiui atidaryti pagal toliau nurodytuose puslapiuose esantį produktą arba produkto variantą.</span><span class="sxs-lookup"><span data-stu-id="a63d1-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="a63d1-119">Puslapis **Produkto informacija**</span><span class="sxs-lookup"><span data-stu-id="a63d1-119">**Product details** page</span></span>
-   <span data-ttu-id="a63d1-120">Puslapis **Išleistų produktų informacija**</span><span class="sxs-lookup"><span data-stu-id="a63d1-120">**Released products details** page</span></span>
-   <span data-ttu-id="a63d1-121">Puslapis **Išleisto produkto variantai**</span><span class="sxs-lookup"><span data-stu-id="a63d1-121">**Released product variants** page</span></span>

<span data-ttu-id="a63d1-122">Atidarydami puslapį **Vieneto konvertavimas** pagal bendrąjį produktą arba išleisto produkto variantą, galite pasirinkti, ar norite nustatyti produkto arba produkto varianto vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="a63d1-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="a63d1-123">Tai atlikti galite pasirinkdami **Produkto variantas** arba **Produktas** lauke **Sukurti konvertavimą, skirtą**.</span><span class="sxs-lookup"><span data-stu-id="a63d1-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="a63d1-124">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="a63d1-124">Product variant</span></span>

<span data-ttu-id="a63d1-125">Pasirinkę **Produkto variantas**, galite pasirinkti, kuriam variantui norite nustatyti vieneto konvertavimą lauke **Produkto variantas**.</span><span class="sxs-lookup"><span data-stu-id="a63d1-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="a63d1-126">Produktas</span><span class="sxs-lookup"><span data-stu-id="a63d1-126">Product</span></span>

<span data-ttu-id="a63d1-127">Pasirinkę **Produktas**, galite nustatyti bendrojo produkto vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="a63d1-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="a63d1-128">Šis vieneto konvertavimas bus taikomas visiems produkto variantams, kurių vieneto konvertavimas neapibrėžtas.</span><span class="sxs-lookup"><span data-stu-id="a63d1-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="a63d1-129">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a63d1-129">Example</span></span>

<span data-ttu-id="a63d1-130">Bendrasis produktas **Marškinėliai** turi keturis išleistų produktų variantus: mažą, vidutinį, didelį ir labai didelį.</span><span class="sxs-lookup"><span data-stu-id="a63d1-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="a63d1-131">Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.</span><span class="sxs-lookup"><span data-stu-id="a63d1-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="a63d1-132">Pirmiausia atidarykite puslapį **Vieneto konvertavimas**, esantį **marškinėliams** skirtame išleisto produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a63d1-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="a63d1-133">Puslapyje **Vieneto konvertavimas** nustatykite išleisto produkto varianto Labai didelis vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="a63d1-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="a63d1-134">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="a63d1-134">**Field**</span></span>             | <span data-ttu-id="a63d1-135">**Parametras**</span><span class="sxs-lookup"><span data-stu-id="a63d1-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="a63d1-136">Sukurti konvertavimą, skirtą</span><span class="sxs-lookup"><span data-stu-id="a63d1-136">Create conversion for</span></span> | <span data-ttu-id="a63d1-137">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="a63d1-137">Product variant</span></span>         |
| <span data-ttu-id="a63d1-138">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="a63d1-138">Product variant</span></span>       | <span data-ttu-id="a63d1-139">Marškinėliai : : Labai didelis : :</span><span class="sxs-lookup"><span data-stu-id="a63d1-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="a63d1-140">Iš vieneto</span><span class="sxs-lookup"><span data-stu-id="a63d1-140">From unit</span></span>             | <span data-ttu-id="a63d1-141">Dėžės</span><span class="sxs-lookup"><span data-stu-id="a63d1-141">Boxes</span></span>                   |
| <span data-ttu-id="a63d1-142">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="a63d1-142">Factor</span></span>                | <span data-ttu-id="a63d1-143">4</span><span class="sxs-lookup"><span data-stu-id="a63d1-143">4</span></span>                       |
| <span data-ttu-id="a63d1-144">Į vienetą</span><span class="sxs-lookup"><span data-stu-id="a63d1-144">To Unit</span></span>               | <span data-ttu-id="a63d1-145">Dalys</span><span class="sxs-lookup"><span data-stu-id="a63d1-145">Pieces</span></span>                  |

<span data-ttu-id="a63d1-146">Išleisto produkto variantų Mažas, Vidutinis ir Didelis vieneto konvertavimas tarp vieneto dėžės ir vienetų yra toks pat, o tai reiškia, kad galite nustatyti šių bendrojo produkto variantų vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="a63d1-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="a63d1-147">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="a63d1-147">**Field**</span></span>             | <span data-ttu-id="a63d1-148">**Parametras**</span><span class="sxs-lookup"><span data-stu-id="a63d1-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="a63d1-149">Sukurti konvertavimą, skirtą</span><span class="sxs-lookup"><span data-stu-id="a63d1-149">Create conversion for</span></span> | <span data-ttu-id="a63d1-150">Produktas</span><span class="sxs-lookup"><span data-stu-id="a63d1-150">Product</span></span>     |
| <span data-ttu-id="a63d1-151">Produktas</span><span class="sxs-lookup"><span data-stu-id="a63d1-151">Product</span></span>               | <span data-ttu-id="a63d1-152">Marškinėliai</span><span class="sxs-lookup"><span data-stu-id="a63d1-152">T-Shirt</span></span>     |
| <span data-ttu-id="a63d1-153">Iš vieneto</span><span class="sxs-lookup"><span data-stu-id="a63d1-153">From unit</span></span>             | <span data-ttu-id="a63d1-154">Dėžės</span><span class="sxs-lookup"><span data-stu-id="a63d1-154">Boxes</span></span>       |
| <span data-ttu-id="a63d1-155">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="a63d1-155">Factor</span></span>                | <span data-ttu-id="a63d1-156">5</span><span class="sxs-lookup"><span data-stu-id="a63d1-156">5</span></span>           |
| <span data-ttu-id="a63d1-157">Į vienetą</span><span class="sxs-lookup"><span data-stu-id="a63d1-157">To Unit</span></span>               | <span data-ttu-id="a63d1-158">Dalys</span><span class="sxs-lookup"><span data-stu-id="a63d1-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="a63d1-159">Vieneto konvertavimo naujinimas naudojant „Excel“</span><span class="sxs-lookup"><span data-stu-id="a63d1-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="a63d1-160">Jei produktas turi daug produkto variantų su skirtingų vienetų konvertavimu, naudinga eksportuoti vienetų konvertavimą iš puslapio **Vienetų konvertavimas** į „Excel“ skaičiuoklę, atnaujinti konvertavimą ir tada jį publikuoti Tiekimo grandinės valdyme.</span><span class="sxs-lookup"><span data-stu-id="a63d1-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="a63d1-161">Parinktis eksportuoti į „Excel“ ir vėl publikuoti redagavimą Tiekimo grandinės valdyme įgalinama per meniu elementą **Atidaryti naudojant „Microsoft Office“**, esantį Veiksmų srities puslapyje **Vienetų konvertavimas**.</span><span class="sxs-lookup"><span data-stu-id="a63d1-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
