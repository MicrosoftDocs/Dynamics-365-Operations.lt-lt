---
title: Turinio įtraukimo būdai
description: Šioje temoje pateikiama apžvalga ir parenkami saitai, kur ir kaip pradėti tvarkyti turinį, naudojant „Microsoft Dynamics 365 Commerce“ svetainės generatoriaus žiniatinklio kūrimo įrankių rinkinį.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eb0b1c3f77bb71ba04c9110ed25fb80c2f2e61f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208068"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="c417c-103">Turinio įtraukimo būdai</span><span class="sxs-lookup"><span data-stu-id="c417c-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c417c-104">Šioje temoje pateikiama apžvalga ir saitai į dokumentus apie tai, kaip tvarkyti turinį, naudojant „Microsoft Dynamics 365 Commerce“ svetainės generatoriaus žiniatinklio kūrimo įrankių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="c417c-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

## <a name="overview"></a><span data-ttu-id="c417c-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="c417c-105">Overview</span></span>

<span data-ttu-id="c417c-106">Yra daug būdų, kaip pakeisti svetainės išvaizdą, pojūtį ir turinį.</span><span class="sxs-lookup"><span data-stu-id="c417c-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="c417c-107">Atsižvelgiant į reikiamą tinkinimo lygį, daugelį šių pakeitimų gali įdiegti ne kūrėjai svetainės generatoriuje, žiniatinklio kūrimo įrankių rinkinyje, įtrauktame į „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c417c-107">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="c417c-108">Svetainės generatorius leidžia kurti šablonus, pasirinkti temas ir pasirinkti ir generuoti modulius nerašant kodų.</span><span class="sxs-lookup"><span data-stu-id="c417c-108">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="c417c-109">Priešingai, norint sukurti naują temą arba modulį, reikia naudoti programavimo įgūdžius, nes būtina naudoti el. prekybos programinės įrangos kūrimo rinkinį (SDK) ir „Microsoft Dynamics Lifecycle Services“ (LCS) diegimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="c417c-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="c417c-110">Šios temos yra geras atspirties taškas pradėti suprasti, kaip įtraukti ir tvarkyti svetainės turinį.</span><span class="sxs-lookup"><span data-stu-id="c417c-110">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="c417c-111">Daugumoje temų dėmesys skiriamas toms svetainės sritims, kurioms nereikia programuotojo.</span><span class="sxs-lookup"><span data-stu-id="c417c-111">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="c417c-112">Kai kuriose aprašomi turinio redagavimo pagrindai, kitos skirtos svetainės administratorių užduotims.</span><span class="sxs-lookup"><span data-stu-id="c417c-112">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="c417c-113">Kiekvienoje iš šių temų bus nurodomos konkrečios užduotys, kurioms gali reikėti SDK darbo.</span><span class="sxs-lookup"><span data-stu-id="c417c-113">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="c417c-114">Kiekvienoje temoje laikoma, kad jau sukonfigūravote svetainę ir turite prieigą prie svetainės generatoriaus įrankių rinkinio.</span><span class="sxs-lookup"><span data-stu-id="c417c-114">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="c417c-115">Pasirinkite vieną iš šių temų, kad pradėtumėte.</span><span class="sxs-lookup"><span data-stu-id="c417c-115">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="c417c-116">Norėdami susipažinti su turinio valdymo terminologija, naudojama svetainės generatoriuje ir šiuose dokumentuose, žr. [Puslapio modelio žodynėlis](page-elements-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-116">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="c417c-117">Norėdami suprasti, kaip veikia moduliai turinio valdymo darbo eigoje, žr. [Darbas su modeliais](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-117">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="c417c-118">Norėdami esamame svetainės puslapyje pakeisti tekstą, vaizdus ar vaizdo įrašą, žr. [Darbas su moduliais](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-118">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="c417c-119">Norėdami pamatyti, kaip fragmentai padeda efektyviau ir lanksčiau valdyti turinį, žr. [Darbas su fragmentais](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-119">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="c417c-120">Norėdami užtikrinti sėkmingą žiniatinklio turinio autorių prekių ženklų kūrimo patirtį, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md) ir [Darbas su šablonais](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-120">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="c417c-121">Norėdami pertvarkyti svetainės puslapio skyrius, žr. [Darbas su maketais](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-121">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="c417c-122">Norėdami pakeisti svetainės puslapių šriftus, spalvas ir bendrą išvaizdą, žr. [Svetainės temos pasirinkimas](select-site-theme.md) arba [Darbas su CSS perrašymo failais](css-override-files.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-122">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="c417c-123">Norėdami pertvarkyti arba pridėti naujų naršymo parinkčių, žr. [Svetainės naršymo tinkinimas](customize-site-navigation.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-123">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="c417c-124">Norėdami sužinoti, kaip organizuoti, peržiūrėti ir publikuoti didelį kiekį lygiagrečių žiniatinklio turinio keitimų, žr. [Darbas su publikavimo grupėmis](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c417c-124">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c417c-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c417c-125">Additional resources</span></span>

[<span data-ttu-id="c417c-126">Turinio kūrimo puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="c417c-126">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="c417c-127">Puslapio modelio žodynas</span><span class="sxs-lookup"><span data-stu-id="c417c-127">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="c417c-128">Dokumentų būsenos ir vykdymo ciklas</span><span class="sxs-lookup"><span data-stu-id="c417c-128">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="c417c-129">Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="c417c-129">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]