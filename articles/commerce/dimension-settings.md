---
title: Rodymo parametrų taikymas produktų dimensijoms
description: Šioje temoje apžvelgiami produkto dimensijų rodymo parametrai ir aprašoma, kaip juos taikyti „Microsoft Dynamics 365 Commerce” platformoje.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117237"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="4cefe-103">Rodymo parametrų taikymas produktų dimensijoms</span><span class="sxs-lookup"><span data-stu-id="4cefe-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4cefe-104">Šioje temoje apžvelgiami produkto dimensijų rodymo parametrai ir aprašoma, kaip juos taikyti „Microsoft Dynamics 365 Commerce” platformoje.</span><span class="sxs-lookup"><span data-stu-id="4cefe-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4cefe-105">„Dynamics 365 Commerce” palaiko dydžio, stiliaus ir spalvos dimensijas, kad būtų galima atskirti produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="4cefe-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="4cefe-106">Dimensijos įprastai rodomos kaip tekstinės reikšmės, pavyzdžiui, „Maža”, „Vidutinė” ir „Didelė” – dydžiams, o spalvoms – „Juoda” ir „Ruda”.</span><span class="sxs-lookup"><span data-stu-id="4cefe-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="4cefe-107">Tačiau, jei produktas palaiko daug variantų, gali būti sunku naršyti produkto variantus, nes reikia kelių pasirinkimų kiekvieno varianto vaizdui peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="4cefe-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="4cefe-108">Kad būtų lengviau naršyti produkto variantus, „Commerce” leidimo 10.0.20 versijoje galima naudoti vaizdus ir šešioliktainius („hex”) kodus, kad dimensijos būtų rodomos kaip pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="4cefe-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="4cefe-109">„Commerce“ svetainės kūrimo priemonėje dimensijų parametrai yra apibrėžiami **Svetainės parametrai \> Plėtiniai \> Dimensijų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="4cefe-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="4cefe-110">Šioje iliustracijoje pateikiamas dimensijos nustatymų pavyzdys svetainės kūrimo priemonėje.</span><span class="sxs-lookup"><span data-stu-id="4cefe-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Svetainės parametrų pavyzdys „Commerce“ svetainės kūrimo priemonėje](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="4cefe-112">Galimi du dimensijų parametrai:</span><span class="sxs-lookup"><span data-stu-id="4cefe-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="4cefe-113">**Dimensijos, rodytinos kaip vaizdas** – Nurodykite, kurios dimensijos turėtų būti rodomos kaip pavyzdžiai el. prekybos svetainės puslapiuose, pavyzdžiui, produkto informacijos puslapiuose (PDP) ir ieškos rezultatų sąrašo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="4cefe-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="4cefe-114">Bet koks spalvos, dydžio ir stiliaus dimensijų derinys gali būti rodomas kaip pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="4cefe-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="4cefe-115">Jei dimensija pasirinkta rodymui kaip pavyzdys, „Commerce” modulio generavimas ieškos galimos šešioliktainio kodo pavyzdžio konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="4cefe-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="4cefe-116">Jei nesukonfigūruotas šešioliktainis kodas, sistemos logika ieškos vaizdo URL pavyzdžio konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="4cefe-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="4cefe-117">Jei nesukonfigūruotas nei šešioliktainis kodas, nei vaizdo URL, bus rodomas tekstas.</span><span class="sxs-lookup"><span data-stu-id="4cefe-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="4cefe-118">Šioje iliustracijoje pateikiamas pavyzdys, kuriame PDP el. komercijos svetainėje apima spalvų ir dydžių pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="4cefe-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="4cefe-119">Šiame pavyzdyje šešioliktainis kodas konfigūruojamas spalvos dimensijai.</span><span class="sxs-lookup"><span data-stu-id="4cefe-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="4cefe-120">Todėl pavyzdžiai rodomi kaip spalvos.</span><span class="sxs-lookup"><span data-stu-id="4cefe-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="4cefe-121">Tačiau dydžio dimensijai nesukonfigūruojamas nei šešioliktainis kodas, nei vaizdo URL.</span><span class="sxs-lookup"><span data-stu-id="4cefe-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="4cefe-122">Todėl rodomas tekstas.</span><span class="sxs-lookup"><span data-stu-id="4cefe-122">Therefore, text is shown.</span></span>

    ![Spalvos dimensija rodoma kaip pavyzdys el. prekybos išsamios produkto informacijos puslapyje](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="4cefe-124">**Dimensijos, rodytinos produkto kortelėje** – Nurodykite, kurios dimensijos turėtų būti rodomos produkto kortelėse, rodomose sąrašuose ir sąrašo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="4cefe-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="4cefe-125">Kad dimensija galėtų būti rodoma produkto kortelėje, šis nustatymas turi būti įgalintas tai dimensijai.</span><span class="sxs-lookup"><span data-stu-id="4cefe-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="4cefe-126">Parametras **Dimensijos, rodytinos kaip vaizdas** taip pat turi būti įgalintas.</span><span class="sxs-lookup"><span data-stu-id="4cefe-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="4cefe-127">Pavyzdžių pasirinkimo veikimas produkto kortelėse yra optimizuotas spalvos dimensijai.</span><span class="sxs-lookup"><span data-stu-id="4cefe-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="4cefe-128">Norint tinkinti kitų dimensijų pavyzdžių pasirinkimo būdą, gali būti reikalingas rodinio plėtinys.</span><span class="sxs-lookup"><span data-stu-id="4cefe-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="4cefe-129">Šioje iliustracijoje pateikiamas pavyzdys, kuriame el. komercijos svetainės sąrašo puslapyje yra produktų kortelės, apimančios spalvų pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="4cefe-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Spalvos dimensija rodoma kaip pavyzdys el. prekybos sąrašo puslapyje](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="4cefe-131">Daugiau informacijos apie tai, kaip konfigūruoti produkto dimensijas, kad jos būtų rodomos kaip pavyzdžiai svetainės puslapiuose, rasite [Konfigūruoti produkto dimensijų reikšmes, kad jos būtų rodomos kaip pavyzdžiai](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="4cefe-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cefe-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4cefe-132">Additional resources</span></span>

[<span data-ttu-id="4cefe-133">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="4cefe-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4cefe-134">Ieškos rezultatų modulis</span><span class="sxs-lookup"><span data-stu-id="4cefe-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="4cefe-135">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="4cefe-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4cefe-136">Konfigūruoti produkto dimensijų reikšmes, kad jos būtų rodomos kaip pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="4cefe-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
