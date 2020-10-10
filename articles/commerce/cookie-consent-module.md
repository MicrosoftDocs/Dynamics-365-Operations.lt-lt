---
title: Sutikimo dėl slapukų modulis
description: Šioje temoje aprašomi sutikimo naudoti slapukus moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817287"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="60880-103">Sutikimo dėl slapukų modulis</span><span class="sxs-lookup"><span data-stu-id="60880-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60880-104">Šioje temoje aprašomi sutikimo naudoti slapukus moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="60880-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60880-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="60880-105">Overview</span></span>

<span data-ttu-id="60880-106">Sutikimo dėl slapukų modulis paragina svetainės vartotojus leisti naudoti slapukus bet kurioje funkcijoje ar modulyje, kurie naudoja naršyklės slapukus.</span><span class="sxs-lookup"><span data-stu-id="60880-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="60880-107">Sutikimas reikalingas pirmą kartą, kai svetainės vartotojas naršo svetainę naujo naršyklės seanso metu.</span><span class="sxs-lookup"><span data-stu-id="60880-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="60880-108">Gavus sutikimą pradedama sekti, o svetainės vartotojo daugiau nebus prašoma pateikti sutikimo.</span><span class="sxs-lookup"><span data-stu-id="60880-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="60880-109">Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .</span><span class="sxs-lookup"><span data-stu-id="60880-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="60880-110">Jei svetainės vartotojo sutikimo naudoti slapukus negaunama, bet kokios funkcijos ir moduliai, naudojantys sutikimą dėl slapukų, puslapyje nebus atvaizduoti.</span><span class="sxs-lookup"><span data-stu-id="60880-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="60880-111">Pavyzdžiui, pirkimo užbaigimo modulis, „Social Share” modulis ir pirmenybinės parduotuvės funkcija reikalauja sutikimo naudoti slapukus ir nebus atvaizduoti, jei svetainės vartotojo sutikimas nebus gaunamas.</span><span class="sxs-lookup"><span data-stu-id="60880-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="60880-112">Sutikimo dėl slapukų modulį galima konfigūruoti puslapio antraštės fragmente, kad jį būtų galima taikyti įkeliant puslapį.</span><span class="sxs-lookup"><span data-stu-id="60880-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="60880-113">Sutikimo dėl slapukų modulyje turi būti aiškus pranešimas, informuojantis svetainės vartotoją apie slapukų naudojimą svetainėje ir pateikiantis saitą su svetainės privatumo puslapiu.</span><span class="sxs-lookup"><span data-stu-id="60880-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="60880-114">Toliau pateiktoje iliustracijoje pabrėžiamas sutikimo dėl slapukų pranešimo, kuriame yra saitas su svetainės privatumo strategijos puslapiu, rodomu svetainės puslapio antraštėje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="60880-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="60880-115">![Sutikimo dėl slapukų modulio pavyzdys](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="60880-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="60880-116">Sutikimo dėl slapukų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="60880-116">Cookie consent module properties</span></span>

| <span data-ttu-id="60880-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="60880-117">Property name</span></span>             | <span data-ttu-id="60880-118">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="60880-118">Value</span></span>                 | <span data-ttu-id="60880-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="60880-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="60880-120">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="60880-120">Rich Text</span></span>                  | <span data-ttu-id="60880-121">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="60880-121">Rich Text</span></span> | <span data-ttu-id="60880-122">Nurodo raiškiojo teksto pranešimą svetainės vartotojams, kad svetainė naudoja naršyklės slapukus ir kad vartotojai turėtų sutikti su slapukų naudojimu, norėdami, jog svetainė būtų visiškai funkcionali.</span><span class="sxs-lookup"><span data-stu-id="60880-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="60880-123">Saitai</span><span class="sxs-lookup"><span data-stu-id="60880-123">Links</span></span> | <span data-ttu-id="60880-124">URL</span><span class="sxs-lookup"><span data-stu-id="60880-124">URL</span></span> | <span data-ttu-id="60880-125">Vienas ar daugiau saitų gali būti įtraukti į svetainės privatumo puslapį, aprašantį svetainėje naudojamų slapukų tipą.</span><span class="sxs-lookup"><span data-stu-id="60880-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="60880-126">Sutikimo dėl slapukų modulio įtraukimas į svetainės puslapius</span><span class="sxs-lookup"><span data-stu-id="60880-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="60880-127">Norint įtraukti sutikimo dėl slapukų modulį į kelis svetainės puslapius, jį galima įtraukti į bendrai naudojamą puslapio antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="60880-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="60880-128">Po to, kai antraštės fragmentas bus įtrauktas į visus svetainės puslapius, sutikimo dėl slapukų pranešimas bus automatiškai vaizduojamas pirmą kartą, kai svetainės vartotojas pereis į bet kurį svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="60880-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="60880-129">Daugiau informacijos apie antraščių fragmentus ir modulius žr. [Antraštės modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="60880-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60880-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="60880-130">Additional resources</span></span>

[<span data-ttu-id="60880-131">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="60880-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="60880-132">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="60880-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="60880-133">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="60880-133">Cookie compliance</span></span>](cookie-compliance.md)
