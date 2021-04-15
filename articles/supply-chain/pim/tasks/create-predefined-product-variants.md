---
title: Iš anksto apibrėžtų produkto variantų kūrimas
description: Šia procedūra apžvelgiamas bendrojo produkto variantų kūrimas naudojant produkto dimensijų kombinacijas.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8340d295ffd072c95d9b174507ef4203131c8165
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809355"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="f0b58-103">Iš anksto apibrėžtų produkto variantų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f0b58-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0b58-104">Šia procedūra apžvelgiamas bendrojo produkto variantų kūrimas naudojant produkto dimensijų kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="f0b58-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="f0b58-105">Kuriant šią procedūrą naudojama demonstracinė įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="f0b58-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="f0b58-106">Kurti bendrąjį produktą</span><span class="sxs-lookup"><span data-stu-id="f0b58-106">Create a product master</span></span>
1. <span data-ttu-id="f0b58-107">Pasirinkite Produkto informacijos valdymas > Produktai > Bendrieji produktai.</span><span class="sxs-lookup"><span data-stu-id="f0b58-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="f0b58-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0b58-108">Click New.</span></span>
3. <span data-ttu-id="f0b58-109">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f0b58-110">Įvesti produkto numerį rankiniu būdu reikia tik jei produkto numerio lauke numerių seka nenustatyta.</span><span class="sxs-lookup"><span data-stu-id="f0b58-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="f0b58-111">Kitaip tariant, jei lauko numeracija nustatyta, veiksmą praleiskite.</span><span class="sxs-lookup"><span data-stu-id="f0b58-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="f0b58-112">Lauke Produkto pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="f0b58-113">Lauke Produkto dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0b58-114">Pasirinkite produkto dimensijų grupę SizeCol (Dydis ir Spalva).</span><span class="sxs-lookup"><span data-stu-id="f0b58-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="f0b58-115">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f0b58-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="f0b58-116">Produkto dimensijų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="f0b58-116">Add product dimensions</span></span>
1. <span data-ttu-id="f0b58-117">Spustelėkite Produkto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="f0b58-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="f0b58-118">Šiame pavyzdyje parodyta, kaip rankiniu būdu įvesti produkto dimensijų.</span><span class="sxs-lookup"><span data-stu-id="f0b58-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="f0b58-119">Taip pat galite pasirinkti dydžių, spalvų ar stilių grupę, kurioje yra jūsų norimos naudoti produkto dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="f0b58-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="f0b58-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0b58-120">Click New.</span></span>
3. <span data-ttu-id="f0b58-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f0b58-122">Lauke Dydis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="f0b58-123">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="f0b58-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0b58-124">Click New.</span></span>
7. <span data-ttu-id="f0b58-125">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f0b58-126">Lauke Dydis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="f0b58-127">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="f0b58-128">Spustelėkite skirtuką Spalvos.</span><span class="sxs-lookup"><span data-stu-id="f0b58-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="f0b58-129">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0b58-129">Click New.</span></span>
12. <span data-ttu-id="f0b58-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f0b58-131">Lauke Spalva įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="f0b58-132">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="f0b58-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0b58-133">Click New.</span></span>
16. <span data-ttu-id="f0b58-134">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="f0b58-135">Lauke Spalva įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="f0b58-136">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0b58-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="f0b58-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f0b58-137">Click Save.</span></span>
20. <span data-ttu-id="f0b58-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f0b58-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="f0b58-139">Produkto variantų generavimas</span><span class="sxs-lookup"><span data-stu-id="f0b58-139">Generate product variants</span></span>
1. <span data-ttu-id="f0b58-140">Spustelėkite Produkto variantai.</span><span class="sxs-lookup"><span data-stu-id="f0b58-140">Click Product variants.</span></span>
2. <span data-ttu-id="f0b58-141">Spustelėkite Variantų pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="f0b58-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="f0b58-142">Spustelėkite Žymėti viską.</span><span class="sxs-lookup"><span data-stu-id="f0b58-142">Click Select all.</span></span>
    * <span data-ttu-id="f0b58-143">Šiame pavyzdyje pasirinkti visi galimi variantai.</span><span class="sxs-lookup"><span data-stu-id="f0b58-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="f0b58-144">Jei kurti variantams bus naudojamas tik galimų produkto dimensijų kombinacijų subrinkinys, galite pasirinkti atskirus įrašus.</span><span class="sxs-lookup"><span data-stu-id="f0b58-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="f0b58-145">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="f0b58-145">Click Create.</span></span>
    * <span data-ttu-id="f0b58-146">Visų savo variantų aprašus galite generuoti pagal produkto dimensijų reikšmių kombinaciją.</span><span class="sxs-lookup"><span data-stu-id="f0b58-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="f0b58-147">Aprašai nėra privalomi.</span><span class="sxs-lookup"><span data-stu-id="f0b58-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="f0b58-148">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f0b58-148">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]