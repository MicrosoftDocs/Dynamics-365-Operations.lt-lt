---
title: Produkto varianto matavimo vieneto konvertavimas
description: Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844374"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="16e05-103">Produkto varianto matavimo vieneto konvertavimas</span><span class="sxs-lookup"><span data-stu-id="16e05-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="16e05-104">Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="16e05-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="16e05-105">Joje pateikiamas nustatymo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="16e05-105">It includes an example of the setup.</span></span>

<span data-ttu-id="16e05-106">Ši funkcija leidžia įmonėms nustatyti skirtingų vienetų konvertavimą tarp to paties produkto variantų.</span><span class="sxs-lookup"><span data-stu-id="16e05-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="16e05-107">Šioje temoje naudojamas toliau pateiktas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="16e05-107">The following example is used in this topic.</span></span> <span data-ttu-id="16e05-108">Įmonė parduoda mažo, vidutinio, didelio ir labai didelio dydžio marškinėlius.</span><span class="sxs-lookup"><span data-stu-id="16e05-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="16e05-109">Marškinėliai apibrėžiami kaip produktas, o skirtingi dydžiai – kaip produkto variantai.</span><span class="sxs-lookup"><span data-stu-id="16e05-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="16e05-110">Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.</span><span class="sxs-lookup"><span data-stu-id="16e05-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="16e05-111">Įmonė nori sekti skirtingų variantų marškinėlius pagal vienetą **Vienetai**, tačiau pardavinėja marškinėlius pagal vienetą **Dėžės**.</span><span class="sxs-lookup"><span data-stu-id="16e05-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="16e05-112">Konvertavimo santykis tarp atsargų vieneto ir pardavimo vieneto yra 1 dėžė = 5 vienetai, išskyrus labai didelio dydžio variantą, kur santykis yra 1 dėžė = 4 vienetai.</span><span class="sxs-lookup"><span data-stu-id="16e05-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="16e05-113">Sąranka</span><span class="sxs-lookup"><span data-stu-id="16e05-113">Setup</span></span>

<span data-ttu-id="16e05-114">Galite konfigūruoti parametrus naudodami funkciją, skirtą produktams, kurie įgalinti **visiems procesams**, arba tik produktui, kuris įgalintas **sandėlio procesams**, naudodami parinktį **Įgalinti matavimo vieneto konvertavimą**, esančią puslapyje **Produkto informacijos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="16e05-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="16e05-115">Nustatyti produkto varianto vieneto konvertavimą</span><span class="sxs-lookup"><span data-stu-id="16e05-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="16e05-116">Produkto variantus galima kurti tik produktams, kurių **Produkto potipis**: **Bendrasis produktas**.</span><span class="sxs-lookup"><span data-stu-id="16e05-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="16e05-117">Daugiau informacijos žr. [Bendrojo produkto kūrimas](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="16e05-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="16e05-118">Funkcija neįgalinta produktams, kurie nustatyti esamo svorio procesams.</span><span class="sxs-lookup"><span data-stu-id="16e05-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="16e05-119">Kuriant bendrąjį produktą, matavimo vieneto konvertavimas įgalinamas naudojant parinktį **Įgalinti matavimo vieneto konvertavimą**, esančią puslapyje **Produkto informacija**.</span><span class="sxs-lookup"><span data-stu-id="16e05-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="16e05-120">Sukūrus bendrąjį produktą su išleistų produktų variantais, galima nustatyti vieneto konvertavimą pagal variantus.</span><span class="sxs-lookup"><span data-stu-id="16e05-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="16e05-121">Galite rasti meniu elementą vieneto konvertavimo puslapiui atidaryti pagal toliau nurodytuose puslapiuose esantį produktą arba produkto variantą.</span><span class="sxs-lookup"><span data-stu-id="16e05-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="16e05-122">Puslapis **Produkto informacija**</span><span class="sxs-lookup"><span data-stu-id="16e05-122">**Product details** page</span></span>
-   <span data-ttu-id="16e05-123">Puslapis **Išleistų produktų informacija**</span><span class="sxs-lookup"><span data-stu-id="16e05-123">**Released products details** page</span></span>
-   <span data-ttu-id="16e05-124">Puslapis **Išleisto produkto variantai**</span><span class="sxs-lookup"><span data-stu-id="16e05-124">**Released product variants** page</span></span>

<span data-ttu-id="16e05-125">Atidarydami puslapį **Vieneto konvertavimas** pagal bendrąjį produktą arba išleisto produkto variantą, galite pasirinkti, ar norite nustatyti produkto arba produkto varianto vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="16e05-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="16e05-126">Tai atlikti galite pasirinkdami **Produkto variantas** arba **Produktas** lauke **Sukurti konvertavimą, skirtą**.</span><span class="sxs-lookup"><span data-stu-id="16e05-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="16e05-127">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="16e05-127">Product variant</span></span>

<span data-ttu-id="16e05-128">Pasirinkę **Produkto variantas**, galite pasirinkti, kuriam variantui norite nustatyti vieneto konvertavimą lauke **Produkto variantas**.</span><span class="sxs-lookup"><span data-stu-id="16e05-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="16e05-129">Produktas</span><span class="sxs-lookup"><span data-stu-id="16e05-129">Product</span></span>

<span data-ttu-id="16e05-130">Pasirinkę **Produktas**, galite nustatyti bendrojo produkto vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="16e05-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="16e05-131">Šis vieneto konvertavimas bus taikomas visiems produkto variantams, kurių vieneto konvertavimas neapibrėžtas.</span><span class="sxs-lookup"><span data-stu-id="16e05-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="16e05-132">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="16e05-132">Example</span></span>

<span data-ttu-id="16e05-133">Bendrasis produktas **Marškinėliai** turi keturis išleistų produktų variantus: mažą, vidutinį, didelį ir labai didelį.</span><span class="sxs-lookup"><span data-stu-id="16e05-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="16e05-134">Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.</span><span class="sxs-lookup"><span data-stu-id="16e05-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="16e05-135">Pirmiausia atidarykite puslapį **Vieneto konvertavimas**, esantį **marškinėliams** skirtame išleisto produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="16e05-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="16e05-136">Puslapyje **Vieneto konvertavimas** nustatykite išleisto produkto varianto Labai didelis vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="16e05-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="16e05-137">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="16e05-137">**Field**</span></span>             | <span data-ttu-id="16e05-138">**Parametras**</span><span class="sxs-lookup"><span data-stu-id="16e05-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="16e05-139">Sukurti konvertavimą, skirtą</span><span class="sxs-lookup"><span data-stu-id="16e05-139">Create conversion for</span></span> | <span data-ttu-id="16e05-140">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="16e05-140">Product variant</span></span>         |
| <span data-ttu-id="16e05-141">Produkto variantas</span><span class="sxs-lookup"><span data-stu-id="16e05-141">Product variant</span></span>       | <span data-ttu-id="16e05-142">Marškinėliai : : Labai didelis : :</span><span class="sxs-lookup"><span data-stu-id="16e05-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="16e05-143">Iš vieneto</span><span class="sxs-lookup"><span data-stu-id="16e05-143">From unit</span></span>             | <span data-ttu-id="16e05-144">Dėžės</span><span class="sxs-lookup"><span data-stu-id="16e05-144">Boxes</span></span>                   |
| <span data-ttu-id="16e05-145">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="16e05-145">Factor</span></span>                | <span data-ttu-id="16e05-146">4</span><span class="sxs-lookup"><span data-stu-id="16e05-146">4</span></span>                       |
| <span data-ttu-id="16e05-147">Į vienetą</span><span class="sxs-lookup"><span data-stu-id="16e05-147">To Unit</span></span>               | <span data-ttu-id="16e05-148">Dalys</span><span class="sxs-lookup"><span data-stu-id="16e05-148">Pieces</span></span>                  |

<span data-ttu-id="16e05-149">Išleisto produkto variantų Mažas, Vidutinis ir Didelis vieneto konvertavimas tarp vieneto dėžės ir vienetų yra toks pat, o tai reiškia, kad galite nustatyti šių bendrojo produkto variantų vieneto konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="16e05-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="16e05-150">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="16e05-150">**Field**</span></span>             | <span data-ttu-id="16e05-151">**Parametras**</span><span class="sxs-lookup"><span data-stu-id="16e05-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="16e05-152">Sukurti konvertavimą, skirtą</span><span class="sxs-lookup"><span data-stu-id="16e05-152">Create conversion for</span></span> | <span data-ttu-id="16e05-153">Produktas</span><span class="sxs-lookup"><span data-stu-id="16e05-153">Product</span></span>     |
| <span data-ttu-id="16e05-154">Produktas</span><span class="sxs-lookup"><span data-stu-id="16e05-154">Product</span></span>               | <span data-ttu-id="16e05-155">Marškinėliai</span><span class="sxs-lookup"><span data-stu-id="16e05-155">T-Shirt</span></span>     |
| <span data-ttu-id="16e05-156">Iš vieneto</span><span class="sxs-lookup"><span data-stu-id="16e05-156">From unit</span></span>             | <span data-ttu-id="16e05-157">Dėžės</span><span class="sxs-lookup"><span data-stu-id="16e05-157">Boxes</span></span>       |
| <span data-ttu-id="16e05-158">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="16e05-158">Factor</span></span>                | <span data-ttu-id="16e05-159">5</span><span class="sxs-lookup"><span data-stu-id="16e05-159">5</span></span>           |
| <span data-ttu-id="16e05-160">Į vienetą</span><span class="sxs-lookup"><span data-stu-id="16e05-160">To Unit</span></span>               | <span data-ttu-id="16e05-161">Dalys</span><span class="sxs-lookup"><span data-stu-id="16e05-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="16e05-162">Vieneto konvertavimo naujinimas naudojant „Excel“</span><span class="sxs-lookup"><span data-stu-id="16e05-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="16e05-163">Jei produktas turi daug produkto variantų su skirtingų vienetų konvertavimu, naudinga eksportuoti vieneto konvertavimą iš puslapio **Vieneto konvertavimas** į „Excel“ skaičiuoklę, atnaujinti konvertavimą ir tada juos publikuoti „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="16e05-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="16e05-164">Parinktis eksportuoti į „Excel“ ir vėl publikuoti „Finance and Operations“ redagavimą įgalinta per meniu elementą **Atidaryti naudojant „Microsoft Office“**, esantį veiksmų srities puslapyje **Vieneto konvertavimas**.</span><span class="sxs-lookup"><span data-stu-id="16e05-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
