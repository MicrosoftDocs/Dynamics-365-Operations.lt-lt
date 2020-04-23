---
title: Produkto varianto matavimo vieneto konvertavimas
description: Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204498"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="480e6-103">Produkto varianto matavimo vieneto konvertavimas</span><span class="sxs-lookup"><span data-stu-id="480e6-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="480e6-104">Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="480e6-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="480e6-105">Joje pateikiamas nustatymo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="480e6-105">It includes an example of the setup.</span></span>

<span data-ttu-id="480e6-106">Ši funkcija leidžia įmonėms nustatyti skirtingų vienetų konvertavimą tarp to paties produkto variantų.</span><span class="sxs-lookup"><span data-stu-id="480e6-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="480e6-107">Šioje temoje naudojamas toliau pateiktas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="480e6-107">The following example is used in this topic.</span></span> <span data-ttu-id="480e6-108">Įmonė parduoda mažo, vidutinio, didelio ir labai didelio dydžio marškinėlius.</span><span class="sxs-lookup"><span data-stu-id="480e6-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="480e6-109">Marškinėliai apibrėžiami kaip produktas, o skirtingi dydžiai – kaip produkto variantai.</span><span class="sxs-lookup"><span data-stu-id="480e6-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="480e6-110">Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.</span><span class="sxs-lookup"><span data-stu-id="480e6-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="480e6-111">Įmonė nori sekti skirtingų variantų marškinėlius pagal vienetą **Vienetai**, tačiau pardavinėja marškinėlius pagal vienetą **Dėžės**.</span><span class="sxs-lookup"><span data-stu-id="480e6-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="480e6-112">Konvertavimo santykis tarp atsargų vieneto ir pardavimo vieneto yra 1 dėžė = 5 vienetai, išskyrus labai didelio dydžio variantą, kur santykis yra 1 dėžė = 4 vienetai.</span><span class="sxs-lookup"><span data-stu-id="480e6-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="480e6-113">Nustatyti produkto varianto vieneto konvertavimą</span><span class="sxs-lookup"><span data-stu-id="480e6-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="480e6-114">Produkto variantus galima kurti tik produktams, kurių **Produkto potipis**: **Bendrasis produktas**.</span><span class="sxs-lookup"><span data-stu-id="480e6-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="480e6-115">Daugiau informacijos žr. [Bendrojo produkto kūrimas](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="480e6-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="480e6-116">Funkcija neįgalinta produktams, kurie nustatyti esamo svorio procesams.</span><span class="sxs-lookup"><span data-stu-id="480e6-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="480e6-117">Sukūrus bendrąjį produktą su išleistų produktų variantais, galima nustatyti vieneto konvertavimą pagal variantus.</span><span class="sxs-lookup"><span data-stu-id="480e6-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="480e6-118">Galite rasti meniu elementą vieneto konvertavimo puslapiui atidaryti pagal toliau nurodytuose puslapiuose esantį produktą arba produkto variantą.</span><span class="sxs-lookup"><span data-stu-id="480e6-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="480e6-119">Puslapis **Produkto informacija**</span><span class="sxs-lookup"><span data-stu-id="480e6-119">**Product details** page</span></span>
-   <span data-ttu-id="480e6-120">Puslapis **Išleistų produktų informacija**</span><span class="sxs-lookup"><span data-stu-id="480e6-120">**Released products details** page</span></span>
-   <span data-ttu-id="480e6-121">Puslapis **Išleisto produkto variantai**</span><span class="sxs-lookup"><span data-stu-id="480e6-121">**Released product variants** page</span></span>

<span data-ttu-id="480e6-122">Atidarydami puslapį **Vieneto konvertavimas** pagal bendrąjį produktą arba išleisto produkto variantą, galite pasirinkti, ar norite nustatyti produkto arba produkto varianto vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="480e6-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="480e6-123">Tai atlikti galite pasirinkdami **Produkto variantas** arba **Produktas** lauke **Sukurti konvertavimą, skirtą**.</span><span class="sxs-lookup"><span data-stu-id="480e6-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="480e6-124">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="480e6-124">Product variant</span></span>

<span data-ttu-id="480e6-125">Pasirinkę **Produkto variantas**, galite pasirinkti, kuriam variantui norite nustatyti vieneto konvertavimą lauke **Produkto variantas**.</span><span class="sxs-lookup"><span data-stu-id="480e6-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="480e6-126">Produktas</span><span class="sxs-lookup"><span data-stu-id="480e6-126">Product</span></span>

<span data-ttu-id="480e6-127">Pasirinkę **Produktas**, galite nustatyti bendrojo produkto vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="480e6-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="480e6-128">Šis vieneto konvertavimas bus taikomas visiems produkto variantams, kurių vieneto konvertavimas neapibrėžtas.</span><span class="sxs-lookup"><span data-stu-id="480e6-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="480e6-129">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="480e6-129">Example</span></span>

<span data-ttu-id="480e6-130">Bendrasis produktas **Marškinėliai** turi keturis išleistų produktų variantus: mažą, vidutinį, didelį ir labai didelį.</span><span class="sxs-lookup"><span data-stu-id="480e6-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="480e6-131">Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.</span><span class="sxs-lookup"><span data-stu-id="480e6-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="480e6-132">Pirmiausia atidarykite puslapį **Vieneto konvertavimas**, esantį **marškinėliams** skirtame išleisto produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="480e6-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="480e6-133">Puslapyje **Vieneto konvertavimas** nustatykite išleisto produkto varianto Labai didelis vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="480e6-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="480e6-134">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="480e6-134">**Field**</span></span>             | <span data-ttu-id="480e6-135">**Parametras**</span><span class="sxs-lookup"><span data-stu-id="480e6-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="480e6-136">Sukurti konvertavimą, skirtą</span><span class="sxs-lookup"><span data-stu-id="480e6-136">Create conversion for</span></span> | <span data-ttu-id="480e6-137">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="480e6-137">Product variant</span></span>         |
| <span data-ttu-id="480e6-138">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="480e6-138">Product variant</span></span>       | <span data-ttu-id="480e6-139">Marškinėliai : : Labai didelis : :</span><span class="sxs-lookup"><span data-stu-id="480e6-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="480e6-140">Iš vieneto</span><span class="sxs-lookup"><span data-stu-id="480e6-140">From unit</span></span>             | <span data-ttu-id="480e6-141">Dėžės</span><span class="sxs-lookup"><span data-stu-id="480e6-141">Boxes</span></span>                   |
| <span data-ttu-id="480e6-142">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="480e6-142">Factor</span></span>                | <span data-ttu-id="480e6-143">4</span><span class="sxs-lookup"><span data-stu-id="480e6-143">4</span></span>                       |
| <span data-ttu-id="480e6-144">Į vienetą</span><span class="sxs-lookup"><span data-stu-id="480e6-144">To Unit</span></span>               | <span data-ttu-id="480e6-145">Dalys</span><span class="sxs-lookup"><span data-stu-id="480e6-145">Pieces</span></span>                  |

<span data-ttu-id="480e6-146">Išleisto produkto variantų Mažas, Vidutinis ir Didelis vieneto konvertavimas tarp vieneto dėžės ir vienetų yra toks pat, o tai reiškia, kad galite nustatyti šių bendrojo produkto variantų vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="480e6-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="480e6-147">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="480e6-147">**Field**</span></span>             | <span data-ttu-id="480e6-148">**Parametras**</span><span class="sxs-lookup"><span data-stu-id="480e6-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="480e6-149">Sukurti konvertavimą, skirtą</span><span class="sxs-lookup"><span data-stu-id="480e6-149">Create conversion for</span></span> | <span data-ttu-id="480e6-150">Produktas</span><span class="sxs-lookup"><span data-stu-id="480e6-150">Product</span></span>     |
| <span data-ttu-id="480e6-151">Produktas</span><span class="sxs-lookup"><span data-stu-id="480e6-151">Product</span></span>               | <span data-ttu-id="480e6-152">Marškinėliai</span><span class="sxs-lookup"><span data-stu-id="480e6-152">T-Shirt</span></span>     |
| <span data-ttu-id="480e6-153">Iš vieneto</span><span class="sxs-lookup"><span data-stu-id="480e6-153">From unit</span></span>             | <span data-ttu-id="480e6-154">Dėžės</span><span class="sxs-lookup"><span data-stu-id="480e6-154">Boxes</span></span>       |
| <span data-ttu-id="480e6-155">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="480e6-155">Factor</span></span>                | <span data-ttu-id="480e6-156">5</span><span class="sxs-lookup"><span data-stu-id="480e6-156">5</span></span>           |
| <span data-ttu-id="480e6-157">Į vienetą</span><span class="sxs-lookup"><span data-stu-id="480e6-157">To Unit</span></span>               | <span data-ttu-id="480e6-158">Dalys</span><span class="sxs-lookup"><span data-stu-id="480e6-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="480e6-159">Vieneto konvertavimo naujinimas naudojant „Excel“</span><span class="sxs-lookup"><span data-stu-id="480e6-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="480e6-160">Jei produktas turi daug produkto variantų su skirtingų vienetų konvertavimu, naudinga eksportuoti vienetų konvertavimą iš puslapio **Vienetų konvertavimas** į „Excel“ skaičiuoklę, atnaujinti konvertavimą ir tada jį publikuoti Tiekimo grandinės valdyme.</span><span class="sxs-lookup"><span data-stu-id="480e6-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="480e6-161">Parinktis eksportuoti į „Excel“ ir vėl publikuoti redagavimą Tiekimo grandinės valdyme įgalinama per meniu elementą **Atidaryti naudojant „Microsoft Office“**, esantį Veiksmų srities puslapyje **Vienetų konvertavimas**.</span><span class="sxs-lookup"><span data-stu-id="480e6-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
