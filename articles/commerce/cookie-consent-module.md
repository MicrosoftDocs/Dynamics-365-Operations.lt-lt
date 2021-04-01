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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 57c8876f1faf08ce965ccd796551996a8651e2eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213943"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="c5dcf-103">Sutikimo dėl slapukų modulis</span><span class="sxs-lookup"><span data-stu-id="c5dcf-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5dcf-104">Šioje temoje aprašomi sutikimo naudoti slapukus moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c5dcf-105">Sutikimo dėl slapukų modulis paragina svetainės vartotojus leisti naudoti slapukus bet kurioje funkcijoje ar modulyje, kurie naudoja naršyklės slapukus.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="c5dcf-106">Sutikimas reikalingas pirmą kartą, kai svetainės vartotojas naršo svetainę naujo naršyklės seanso metu.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="c5dcf-107">Gavus sutikimą pradedama sekti, o svetainės vartotojo daugiau nebus prašoma pateikti sutikimo.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="c5dcf-108">Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .</span><span class="sxs-lookup"><span data-stu-id="c5dcf-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="c5dcf-109">Jei svetainės vartotojo sutikimo naudoti slapukus negaunama, bet kokios funkcijos ir moduliai, naudojantys sutikimą dėl slapukų, puslapyje nebus atvaizduoti.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="c5dcf-110">Pavyzdžiui, pirkimo užbaigimo modulis, „Social Share” modulis ir pirmenybinės parduotuvės funkcija reikalauja sutikimo naudoti slapukus ir nebus atvaizduoti, jei svetainės vartotojo sutikimas nebus gaunamas.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="c5dcf-111">Sutikimo dėl slapukų modulį galima konfigūruoti puslapio antraštės fragmente, kad jį būtų galima taikyti įkeliant puslapį.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="c5dcf-112">Sutikimo dėl slapukų modulyje turi būti aiškus pranešimas, informuojantis svetainės vartotoją apie slapukų naudojimą svetainėje ir pateikiantis saitą su svetainės privatumo puslapiu.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="c5dcf-113">Toliau pateiktoje iliustracijoje pabrėžiamas sutikimo dėl slapukų pranešimo, kuriame yra saitas su svetainės privatumo strategijos puslapiu, rodomu svetainės puslapio antraštėje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="c5dcf-114">![Sutikimo dėl slapukų modulio pavyzdys](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="c5dcf-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="c5dcf-115">Sutikimo dėl slapukų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="c5dcf-115">Cookie consent module properties</span></span>

| <span data-ttu-id="c5dcf-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c5dcf-116">Property name</span></span>             | <span data-ttu-id="c5dcf-117">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="c5dcf-117">Value</span></span>                 | <span data-ttu-id="c5dcf-118">aprašymas</span><span class="sxs-lookup"><span data-stu-id="c5dcf-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c5dcf-119">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="c5dcf-119">Rich Text</span></span>                  | <span data-ttu-id="c5dcf-120">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="c5dcf-120">Rich Text</span></span> | <span data-ttu-id="c5dcf-121">Nurodo raiškiojo teksto pranešimą svetainės vartotojams, kad svetainė naudoja naršyklės slapukus ir kad vartotojai turėtų sutikti su slapukų naudojimu, norėdami, jog svetainė būtų visiškai funkcionali.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="c5dcf-122">Saitai</span><span class="sxs-lookup"><span data-stu-id="c5dcf-122">Links</span></span> | <span data-ttu-id="c5dcf-123">URL</span><span class="sxs-lookup"><span data-stu-id="c5dcf-123">URL</span></span> | <span data-ttu-id="c5dcf-124">Vienas ar daugiau saitų gali būti įtraukti į svetainės privatumo puslapį, aprašantį svetainėje naudojamų slapukų tipą.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="c5dcf-125">Sutikimo dėl slapukų modulio įtraukimas į svetainės puslapius</span><span class="sxs-lookup"><span data-stu-id="c5dcf-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="c5dcf-126">Norint įtraukti sutikimo dėl slapukų modulį į kelis svetainės puslapius, jį galima įtraukti į bendrai naudojamą puslapio antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="c5dcf-127">Po to, kai antraštės fragmentas bus įtrauktas į visus svetainės puslapius, sutikimo dėl slapukų pranešimas bus automatiškai vaizduojamas pirmą kartą, kai svetainės vartotojas pereis į bet kurį svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="c5dcf-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="c5dcf-128">Daugiau informacijos apie antraščių fragmentus ir modulius žr. [Antraštės modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="c5dcf-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5dcf-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c5dcf-129">Additional resources</span></span>

[<span data-ttu-id="c5dcf-130">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="c5dcf-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c5dcf-131">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="c5dcf-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="c5dcf-132">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="c5dcf-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]