---
title: Turinio įtraukimo būdai
description: Šioje temoje pateikiama apžvalga ir parenkami saitai, kur ir kaip pradėti tvarkyti turinį, naudojant „Microsoft Dynamics 365 Commerce“ svetainės generatoriaus žiniatinklio kūrimo įrankių rinkinį.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e6794e528d9fa6066d7246e99a3307bb1bdc9c78
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797580"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="3a42b-103">Turinio įtraukimo būdai</span><span class="sxs-lookup"><span data-stu-id="3a42b-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3a42b-104">Šioje temoje pateikiama apžvalga ir saitai į dokumentus apie tai, kaip tvarkyti turinį, naudojant „Microsoft Dynamics 365 Commerce“ svetainės generatoriaus žiniatinklio kūrimo įrankių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="3a42b-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

<span data-ttu-id="3a42b-105">Yra daug būdų, kaip pakeisti svetainės išvaizdą, pojūtį ir turinį.</span><span class="sxs-lookup"><span data-stu-id="3a42b-105">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="3a42b-106">Atsižvelgiant į reikiamą tinkinimo lygį, daugelį šių pakeitimų gali įdiegti ne kūrėjai svetainės generatoriuje, žiniatinklio kūrimo įrankių rinkinyje, įtrauktame į „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="3a42b-106">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="3a42b-107">Svetainės generatorius leidžia kurti šablonus, pasirinkti temas ir pasirinkti ir generuoti modulius nerašant kodų.</span><span class="sxs-lookup"><span data-stu-id="3a42b-107">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="3a42b-108">Priešingai, norint sukurti naują temą arba modulį, reikia naudoti programavimo įgūdžius, nes būtina naudoti el. prekybos programinės įrangos kūrimo rinkinį (SDK) ir „Microsoft Dynamics Lifecycle Services“ (LCS) diegimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="3a42b-108">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="3a42b-109">Šios temos yra geras atspirties taškas pradėti suprasti, kaip įtraukti ir tvarkyti svetainės turinį.</span><span class="sxs-lookup"><span data-stu-id="3a42b-109">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="3a42b-110">Daugumoje temų dėmesys skiriamas toms svetainės sritims, kurioms nereikia programuotojo.</span><span class="sxs-lookup"><span data-stu-id="3a42b-110">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="3a42b-111">Kai kuriose aprašomi turinio redagavimo pagrindai, kitos skirtos svetainės administratorių užduotims.</span><span class="sxs-lookup"><span data-stu-id="3a42b-111">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="3a42b-112">Kiekvienoje iš šių temų bus nurodomos konkrečios užduotys, kurioms gali reikėti SDK darbo.</span><span class="sxs-lookup"><span data-stu-id="3a42b-112">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="3a42b-113">Kiekvienoje temoje laikoma, kad jau sukonfigūravote svetainę ir turite prieigą prie svetainės generatoriaus įrankių rinkinio.</span><span class="sxs-lookup"><span data-stu-id="3a42b-113">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="3a42b-114">Pasirinkite vieną iš šių temų, kad pradėtumėte.</span><span class="sxs-lookup"><span data-stu-id="3a42b-114">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="3a42b-115">Norėdami susipažinti su turinio valdymo terminologija, naudojama svetainės generatoriuje ir šiuose dokumentuose, žr. [Puslapio modelio žodynėlis](page-elements-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-115">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="3a42b-116">Norėdami suprasti, kaip veikia moduliai turinio valdymo darbo eigoje, žr. [Darbas su modeliais](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-116">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="3a42b-117">Norėdami esamame svetainės puslapyje pakeisti tekstą, vaizdus ar vaizdo įrašą, žr. [Darbas su moduliais](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-117">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="3a42b-118">Norėdami pamatyti, kaip fragmentai padeda efektyviau ir lanksčiau valdyti turinį, žr. [Darbas su fragmentais](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-118">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="3a42b-119">Norėdami užtikrinti sėkmingą žiniatinklio turinio autorių prekių ženklų kūrimo patirtį, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md) ir [Darbas su šablonais](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-119">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="3a42b-120">Norėdami pertvarkyti svetainės puslapio skyrius, žr. [Darbas su maketais](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-120">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="3a42b-121">Norėdami pakeisti svetainės puslapių šriftus, spalvas ir bendrą išvaizdą, žr. [Svetainės temos pasirinkimas](select-site-theme.md) arba [Darbas su CSS perrašymo failais](css-override-files.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-121">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="3a42b-122">Norėdami pertvarkyti arba pridėti naujų naršymo parinkčių, žr. [Svetainės naršymo tinkinimas](customize-site-navigation.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-122">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="3a42b-123">Norėdami sužinoti, kaip organizuoti, peržiūrėti ir publikuoti didelį kiekį lygiagrečių žiniatinklio turinio keitimų, žr. [Darbas su publikavimo grupėmis](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="3a42b-123">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a42b-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3a42b-124">Additional resources</span></span>

[<span data-ttu-id="3a42b-125">Turinio kūrimo puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="3a42b-125">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="3a42b-126">Puslapio modelio žodynas</span><span class="sxs-lookup"><span data-stu-id="3a42b-126">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="3a42b-127">Dokumentų būsenos ir vykdymo ciklas</span><span class="sxs-lookup"><span data-stu-id="3a42b-127">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="3a42b-128">Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="3a42b-128">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
