---
title: Iš anksto apibrėžtų produkto variantų kūrimas
description: Šia procedūra apžvelgiamas bendrojo produkto variantų kūrimas naudojant produkto dimensijų kombinacijas.
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938207"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="ceab0-103">Iš anksto apibrėžti produkto variantai</span><span class="sxs-lookup"><span data-stu-id="ceab0-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="ceab0-104">Scenarijaus pavyzdys: Iš anksto apibrėžtų produkto variantų kūrimas</span><span class="sxs-lookup"><span data-stu-id="ceab0-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="ceab0-105">Šia procedūra apžvelgiamas bendrojo produkto variantų kūrimas naudojant produkto dimensijų kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="ceab0-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ceab0-106">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="ceab0-106">Make demo data available</span></span>

<span data-ttu-id="ceab0-107">Šio scenarijaus įgyvendinimui naudojant siūlomas vertes, privalote turėti įdiegtus demo duomenis ir pasirinkti *USMF* juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="ceab0-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="ceab0-108">1 žingsnis: Bendrojo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="ceab0-108">Step 1: Create a product master</span></span>

<span data-ttu-id="ceab0-109">Norėdami kurti bendrąjį produktą:</span><span class="sxs-lookup"><span data-stu-id="ceab0-109">To create a product master:</span></span>

1. <span data-ttu-id="ceab0-110">Eikite į **Produkto informacijos valdymas > Produktai > Bendrieji produktai**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="ceab0-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-111">Select **New**.</span></span>
1. <span data-ttu-id="ceab0-112">Jei **lauke** Produkto numeris dar nerodyti numerio, įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="ceab0-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="ceab0-113">Šį veiksmą atlikti reikia tik jei nenustatyta produktų numeracija šiame lauke.</span><span class="sxs-lookup"><span data-stu-id="ceab0-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="ceab0-114">Laukelyje **Produkto pavadinimas** įveskite produkto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ceab0-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="ceab0-115">Produkto **dimensijų grupės** lauke pasirinkite produkto dimensijų grupę *SizeCol* (Dydis ir spalva).</span><span class="sxs-lookup"><span data-stu-id="ceab0-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="ceab0-116">Norėdami **sukurti ir atidaryti naują bendrąjį** produktą, pasirinkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="ceab0-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="ceab0-117">2 žingsnis: Produkto dimensijų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="ceab0-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="ceab0-118">Šiame pavyzdyje parodyta, kaip rankiniu būdu įvesti produkto dimensijų.</span><span class="sxs-lookup"><span data-stu-id="ceab0-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="ceab0-119">Taip pat galite pasirinkti dydžių, spalvų ar stilių grupę, kurioje yra jūsų norimos naudoti produkto dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ceab0-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="ceab0-120">Norėdami įtraukti produkto dimensijas:</span><span class="sxs-lookup"><span data-stu-id="ceab0-120">To add product dimensions:</span></span>

1. <span data-ttu-id="ceab0-121">Kai naujas bendrasis produktas vis dar atidarytas, **veiksmų srityje pasirinkite Produkto** dimensijos.</span><span class="sxs-lookup"><span data-stu-id="ceab0-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="ceab0-122">Atidarykite **skirtuką Dydis ir** įrankių **juostoje** pasirinkite Naujas, kad įtraukumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="ceab0-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="ceab0-123">Naujoje eilutėje nustatykite šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="ceab0-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="ceab0-124">**Dydis:** Pasirinkti dydžio vertę.</span><span class="sxs-lookup"><span data-stu-id="ceab0-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="ceab0-125">**Pavadinimas** Įveskite pavadinimą dydžiui.</span><span class="sxs-lookup"><span data-stu-id="ceab0-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="ceab0-126">Įrankių **juostoje** pasirinkite Naujas ir į tinklelį įtraukite antrą dydį, naudodami naują **dydį** ir **pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="ceab0-127">Atidarykite **Spalvos** įrankių **juostoje** pasirinkite Naujas, kad įtraukumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="ceab0-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="ceab0-128">Naujoje eilutėje nustatykite šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="ceab0-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="ceab0-129">**Spalva:** pasirinkite spalvos vertę.</span><span class="sxs-lookup"><span data-stu-id="ceab0-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="ceab0-130">**Pavadinimas** Įveskite pavadinimą spalvai.</span><span class="sxs-lookup"><span data-stu-id="ceab0-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="ceab0-131">Įrankių **juostoje** pasirinkite Naujas ir į tinklelį įtraukite antrą dydį, naudodami naują **Spalva** ir **pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="ceab0-132">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-132">Select **Save**.</span></span>
1. <span data-ttu-id="ceab0-133">Norėdami grįžti į savo naują bendrąjį produktą, uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ceab0-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="ceab0-134">3 žingsnis: Produkto variantų generavimas</span><span class="sxs-lookup"><span data-stu-id="ceab0-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="ceab0-135">Šiame skyriuje aprašoma, kaip generuoti produktų variantus, *kai neįgalinta* variantų pasiūlymų puslapio patobulinimų funkcija.</span><span class="sxs-lookup"><span data-stu-id="ceab0-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="ceab0-136">Informacijos apie tai, kaip generuoti produkto variantus, kai ši funkcija yra pasiekiama, rasite kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="ceab0-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="ceab0-137">Norėdami kurti produkto variantus:</span><span class="sxs-lookup"><span data-stu-id="ceab0-137">To generate product variants:</span></span>

1. <span data-ttu-id="ceab0-138">Kai naujas bendrasis produktas vis dar atidarytas, **veiksmų srityje pasirinkite Produkto** variantus.</span><span class="sxs-lookup"><span data-stu-id="ceab0-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="ceab0-139">Rinkitės **Varianto siūlymus** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="ceab0-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="ceab0-140">Sistema sugeneruoja sąrašą su visomis galimais dydžių ir spalvų deriniais, kuriuos nustatote produktui.</span><span class="sxs-lookup"><span data-stu-id="ceab0-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="ceab0-141">Pasirinkite **Žymėti viską įrankių** juostoje.</span><span class="sxs-lookup"><span data-stu-id="ceab0-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="ceab0-142">Šiame pavyzdyje pasirinkite visus galimus variantus.</span><span class="sxs-lookup"><span data-stu-id="ceab0-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="ceab0-143">Jei norite naudoti tik galimų produkto dimensijų derinių subrinkinį, pasirinkite tik reikiamus žymės langelius.</span><span class="sxs-lookup"><span data-stu-id="ceab0-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="ceab0-144">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-144">Select **Create**.</span></span>
1. <span data-ttu-id="ceab0-145">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="ceab0-146">Patobulinti variantų pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="ceab0-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="ceab0-147">Variantų pasiūlymų puslapio patobulinimų funkcija pagerina variantų pasiūlymų puslapį, kad adresuoti našumo ir tinkamumo naudoti problemas įmonėse, kurios turi daug *produkto* dimensijų **derinių**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="ceab0-148">Patobulintas produkto dimensijų reikšmių pasirinkimo procesas, kurio variantų pasiūlymus būtų galima atlikti greičiau ir paprasčiau identifikuoti bei pateikti atitinkamą produkto variantų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ceab0-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="ceab0-149">Šią priemonę pridėjo šie patobulinimai:</span><span class="sxs-lookup"><span data-stu-id="ceab0-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="ceab0-150">**Atidėtas variantų pasiūlymų generavimas: variantų pasiūlymų puslapyje, kai pirmą kartą** jį **atidarote**, nebėra pasiūlymų.</span><span class="sxs-lookup"><span data-stu-id="ceab0-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="ceab0-151">Todėl turite tiesiogiai pasirinkti, kurių verčių jums reikia, tada pasirinkti **mygtuką** Siūlyti, kad būtų generuojamos kombinacijos.</span><span class="sxs-lookup"><span data-stu-id="ceab0-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="ceab0-152">Taip procesas bus matomas ir interaktyviau.</span><span class="sxs-lookup"><span data-stu-id="ceab0-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="ceab0-153">**Dimensijų verčių pasirinkimas: kai turite daug dimensijų verčių, paprastai jus domina generuoti variantų pasiūlymus, kuriuose yra tik keletas iš jų (pvz., pristatant naują spalvų arba stilių** rinkinį).</span><span class="sxs-lookup"><span data-stu-id="ceab0-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="ceab0-154">Naudodami patobulintą dizainą, galite pasirinkti dimensijų vertes, kurioms norite generuoti produkto variantų pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="ceab0-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="ceab0-155">Tai labai padidina siūlomų variantų tinkamumą ir pagerina sistemos našumą ir vartotojo produktyvumą.</span><span class="sxs-lookup"><span data-stu-id="ceab0-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="ceab0-156">Variantų pasiūlymų puslapio patobulinimų funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="ceab0-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="ceab0-157">Norėdami naudoti *Varianto siūlymo puslapio gerinimų* funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="ceab0-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="ceab0-158">Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="ceab0-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ceab0-159">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="ceab0-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ceab0-160">**Modulis:** *Produkto informacijos valdymas*</span><span class="sxs-lookup"><span data-stu-id="ceab0-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="ceab0-161">**Funkcijos pavadinimas:** *Variantų pasiūlymų puslapio patobulinimai*</span><span class="sxs-lookup"><span data-stu-id="ceab0-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="ceab0-162">Dirbti su patobulintais variantų pasiūlymais</span><span class="sxs-lookup"><span data-stu-id="ceab0-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="ceab0-163">Norėdami kurti produkto varianto siūlymus, *kai neįgalinta* variantų pasiūlymų puslapio patobulinimų funkcija:</span><span class="sxs-lookup"><span data-stu-id="ceab0-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="ceab0-164">Atidaryti arba sukurti bendrąjį produktą ir įtraukti į jį reikiamas produkto dimensijas, kaip aprašyta ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="ceab0-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="ceab0-165">Kai naujas bendrasis produktas vis dar atidarytas, **veiksmų srityje pasirinkite Produkto** variantus.</span><span class="sxs-lookup"><span data-stu-id="ceab0-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="ceab0-166">Rinkitės **Varianto siūlymus** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="ceab0-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="ceab0-167">Pasirinkite vertes, kurias norite naudoti visose dimensijose.</span><span class="sxs-lookup"><span data-stu-id="ceab0-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="ceab0-168">Viršutinėje įrankių juostoje pasirinkite **Siūlyti**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="ceab0-169">Sistema sugeneruoja sąrašą su visomis galimais dydžių ir spalvų deriniais, kuriuos pasirenkate produktui.</span><span class="sxs-lookup"><span data-stu-id="ceab0-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="ceab0-170">Siūlomų variantų „FastTab" pažymėkite kiekvieno norimo naudoti produkto dimensijų derinio žymės langelį arba įrankių juostoje pasirinkite Žymėti viską, kad juos **visas** **pasirinktumėte**.</span><span class="sxs-lookup"><span data-stu-id="ceab0-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="ceab0-171">Pasirinkite **Kurti**, jei norite įtraukti variantus į dabartinį bendrąjį produktą.</span><span class="sxs-lookup"><span data-stu-id="ceab0-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
