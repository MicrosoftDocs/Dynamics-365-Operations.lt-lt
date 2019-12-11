---
title: Darbas su moduliais
description: Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 06a26e5dfd35bf229e67ed27213210d0da726bdf
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698078"
---
# <a name="work-with-modules"></a><span data-ttu-id="23827-103">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="23827-103">Work with modules</span></span>

<span data-ttu-id="23827-104">Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="23827-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="23827-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="23827-105">Overview</span></span>

<span data-ttu-id="23827-106">Moduliai yra loginiai kūrimo blokai, kurie sudaro puslapio struktūrą, o jų paskirtis ir taikymo sritys yra įvairios.</span><span class="sxs-lookup"><span data-stu-id="23827-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="23827-107">Kai kurie moduliai yra aukšto lygio konteineriai, o jų vienintelė paskirtis – laikyti ir organizuoti kitus modulius (antrinius modulius).</span><span class="sxs-lookup"><span data-stu-id="23827-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="23827-108">Kitų modulių, pvz., paprasto vaizdų išdėstymo modulio, paskirtis yra labai konkreti.</span><span class="sxs-lookup"><span data-stu-id="23827-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="23827-109">Kiti moduliai, pvz., karuselės modulis, patenka tarp šių dviejų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="23827-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="23827-110">Pagal numatytuosius nustatymus jūsų „Dynamics 365 Commerce“ svetainėje yra darbo pradžios rinkinio modulių biblioteka, kuri leidžia įgyvendinti pagrindinius el. prekybos scenarijus.</span><span class="sxs-lookup"><span data-stu-id="23827-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="23827-111">Tiesiog naudodami šiuos modulius greičiausiai galėsite sukurti visapusišką el. prekybos svetainę.</span><span class="sxs-lookup"><span data-stu-id="23827-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="23827-112">Tačiau galbūt norėsite šiuos modulius tinkinti arba kurti naujus pasirinktinius modulius konkretiems poreikiams.</span><span class="sxs-lookup"><span data-stu-id="23827-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="23827-113">Jei norite kurti pasirinktinius modulius, galite naudoti modulių kūrimo programinės įrangos kūrimo rinkinį (SDK), kuris padės sukurti pasirinktinių modulių biblioteką.</span><span class="sxs-lookup"><span data-stu-id="23827-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="23827-114">Konteinerio moduliai ir vietos</span><span class="sxs-lookup"><span data-stu-id="23827-114">Container modules and slots</span></span>

<span data-ttu-id="23827-115">Kaip minėta anksčiau, kai kurie moduliai yra skirti laikyti antrinius modulius.</span><span class="sxs-lookup"><span data-stu-id="23827-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="23827-116">Šie moduliai vadinami *konteineriais* ir leidžia naudoti įdėtųjų modulių hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="23827-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="23827-117">Konteinerio moduliai apima *vietas*.</span><span class="sxs-lookup"><span data-stu-id="23827-117">Container modules include *slots*.</span></span> <span data-ttu-id="23827-118">Vietos naudojamos antrinių modulių maketui ir paskirčiai konteineryje tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="23827-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="23827-119">Pavyzdys – pagrindinis puslapio konteinerio modulis (bet kurio puslapio aukščiausio lygio modulis), kuriame nustatytos kelios svarbios vietos.</span><span class="sxs-lookup"><span data-stu-id="23827-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="23827-120">Antraštės vieta</span><span class="sxs-lookup"><span data-stu-id="23827-120">A header slot</span></span>
- <span data-ttu-id="23827-121">Pagrindinės dalies vieta</span><span class="sxs-lookup"><span data-stu-id="23827-121">A body slot</span></span>
- <span data-ttu-id="23827-122">Poraštės vieta</span><span class="sxs-lookup"><span data-stu-id="23827-122">A footer slot</span></span>

<span data-ttu-id="23827-123">Modulio kūrėjas apibrėžia šias vietas ir nustato, kuriuos antrinius modulius ir kiek antrinių modulių galima tiesiogiai įdėti jų viduje.</span><span class="sxs-lookup"><span data-stu-id="23827-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="23827-124">Pavyzdžiui, antraštės vieta gali palaikyti tik vieną tipo **Antraštės modulis** modulį, o pagrindinės dalies vieta gali palaikyti neribotą skaičių bet kokio tipo modulių (išskyrus kitus puslapio konteinerio modulius).</span><span class="sxs-lookup"><span data-stu-id="23827-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="23827-125">Naudodami kūrimo įrankius puslapių autoriai neprivalo iš anksto žinoti, kuriuos modulius galima įdėti į kiekvieną vietą arba kurių modulių įdėti negalima.</span><span class="sxs-lookup"><span data-stu-id="23827-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="23827-126">Kai puslapių autoriai pasirenka vietą ir bando pasirinkti modulį, kurį nori į šią vietą įtraukti, jie matys modulio tipų, kurie toje vietoje palaikomi, filtruotą rodinį.</span><span class="sxs-lookup"><span data-stu-id="23827-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="23827-127">Turinio moduliai</span><span class="sxs-lookup"><span data-stu-id="23827-127">Content modules</span></span>

<span data-ttu-id="23827-128">Turinio moduliuose yra turinio ir medijos elementų, pvz., teksto (pvz., antraščių, pastraipų ir saitų) arba turto nuorodų (pavyzdžiui, vaizdų, vaizdo įrašų ir PDF failų).</span><span class="sxs-lookup"><span data-stu-id="23827-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="23827-129">Įprastų turinio modulių tipų pavyzdžiai – **Pagrindinė reklaminė juosta**, **Ypatybė** ir **Reklaminė juosta**.</span><span class="sxs-lookup"><span data-stu-id="23827-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="23827-130">Šių trijų tipų moduliuose gali būti teksto arba medijos, ir jiems nereikia jokių antrinių modulių, kad kokią nors informaciją būtų galima padaryti matoma puslapyje.</span><span class="sxs-lookup"><span data-stu-id="23827-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="23827-131">Dauguma įprastų, kasdienių puslapių ir turinio kūrimo užduočių apima turinio modulius, visų pirma todėl, kad šie moduliai apibrėžia faktinį turinį, kuris generuojamas jų pirminio konteinerio moduliuose.</span><span class="sxs-lookup"><span data-stu-id="23827-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="23827-132">Yra daug turinio modulių ir jie paprastai yra paskutinės dalys, kurias įtrauksite į puslapio įdėtųjų modulių hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="23827-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="23827-133">Toliau pateiktoje iliustracijoje parodyta, kaip moduliai yra įdėti į pirminio konteinerio modulio vietas.</span><span class="sxs-lookup"><span data-stu-id="23827-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Modulių įdėjimas](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="23827-135">Modulių įtraukimas arba pašalinimas</span><span class="sxs-lookup"><span data-stu-id="23827-135">Add or remove modules</span></span>

<span data-ttu-id="23827-136">Tolesnėse procedūrose aprašoma, kaip įtraukti modulių arba juos pašalinti</span><span class="sxs-lookup"><span data-stu-id="23827-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="23827-137">Modulio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="23827-137">Add a module</span></span>

<span data-ttu-id="23827-138">Norėdami modulį įtraukti į vietą arba konteinerį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="23827-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="23827-139">Struktūros srityje kairėje pasirinkite konteinerį arba vietą, į kuriuos galima įtraukti antrinį modulį.</span><span class="sxs-lookup"><span data-stu-id="23827-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23827-140">Modulių dizaino įrankyje nustatytas modulių, kuriuos galima įtraukti į konkrečią modulio vietą, tipų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="23827-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="23827-141">Tada šablonų autoriai gali patikslinti leidžiamų modulių parinktis, kad būtų užtikrintas visų puslapių, kurie kuriami naudojant konkretų šabloną, nuoseklus ieškos modulio optimizavimas (SEO) ir kūrimo efektyvumas.</span><span class="sxs-lookup"><span data-stu-id="23827-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="23827-142">Pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="23827-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="23827-143">Rodomas dialogo langas **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="23827-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="23827-144">Šis dialogo langas automatiškai filtruojamas taip, kad jame būtų rodomi tik tie moduliai, kurie palaikomi pasirinktame konteineryje arba vietoje.</span><span class="sxs-lookup"><span data-stu-id="23827-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="23827-145">Modulių sąrašas nustatomas pagal puslapio šabloną arba konteinerio modulio aprašą.</span><span class="sxs-lookup"><span data-stu-id="23827-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23827-146">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti modulį** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="23827-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="23827-147">Dialogo lange raskite ir pasirinkite modulį, kurį norite įtraukti į puslapį.</span><span class="sxs-lookup"><span data-stu-id="23827-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="23827-148">**Ypatybės** ir **Pagrindinės reklaminės juostos** modulių tipai yra tinkami pradedantiesiems.</span><span class="sxs-lookup"><span data-stu-id="23827-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="23827-149">Pasirinkite **Gerai**, kad pasirinktą modulį įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="23827-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="23827-150">Modulio šalinimas</span><span class="sxs-lookup"><span data-stu-id="23827-150">Remove a module</span></span>

<span data-ttu-id="23827-151">Norėdami modulį pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="23827-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="23827-152">Struktūros srityje kairėje šalia modulio, kurį norite pašalinti, pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite šiukšliadėžės mygtuką.</span><span class="sxs-lookup"><span data-stu-id="23827-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="23827-153">Kai būsite paraginti patvirtinti, kad norite pašalinti modulį, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="23827-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="23827-154">Modulių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="23827-154">Configure modules</span></span>

<span data-ttu-id="23827-155">Tolesnėse procedūrose aprašoma, kaip konfigūruoti turinio ir konteinerio modulius.</span><span class="sxs-lookup"><span data-stu-id="23827-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="23827-156">Turinio modulio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="23827-156">Configure a content module</span></span>

<span data-ttu-id="23827-157">Norėdami konfigūruoti turinio modulį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="23827-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="23827-158">Kairėje pusėje esančioje struktūros srityje pasirinkite turinio modulio tipą (pvz, **Ypatybė**, **Pagrindinė reklaminė juosta** arba **Reklaminė juosta**).</span><span class="sxs-lookup"><span data-stu-id="23827-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="23827-159">Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.</span><span class="sxs-lookup"><span data-stu-id="23827-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="23827-160">Jei ypatybių srityje yra skyrius **Duomenų konfigūracija**, jį spustelėkite, kad išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="23827-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="23827-161">Priešingu atveju pereikite į 5 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="23827-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="23827-162">Jei rodomas mygtukas **Įtraukti duomenų šaltinį**, jį spustelėkite ir pasirinkite turinio elementus, kuriuos norite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="23827-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="23827-163">Įveskite visų būtinų arba pageidaujamų modulio valdiklių parametrus.</span><span class="sxs-lookup"><span data-stu-id="23827-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="23827-164">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="23827-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="23827-165">Konteinerio modulio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="23827-165">Configure a container module</span></span>

<span data-ttu-id="23827-166">Norėdami konfigūruoti konteinerio modulį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="23827-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="23827-167">Savo puslapyje pasirinkite konteinerio modulį (pavyzdžiui, karuselės arba nepastovaus konteinerio modulį).</span><span class="sxs-lookup"><span data-stu-id="23827-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="23827-168">Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.</span><span class="sxs-lookup"><span data-stu-id="23827-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="23827-169">Struktūros srityje kairėje šalia konteinerio arba bet kokių konteineryje esančių vietų pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="23827-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="23827-170">Tada į pasirinktą konteinerį įtraukite antrinių modulių.</span><span class="sxs-lookup"><span data-stu-id="23827-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="23827-171">Norėdami gauti daugiau informacijos, žr. pirmiau šioje temoje aprašytą procedūrą [Modulio įtraukimas](#add-a-module).</span><span class="sxs-lookup"><span data-stu-id="23827-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="23827-172">Jei pirminiame konteineryje yra keli tos pačios kilmės antriniai moduliai, galite pakeisti jų rodymo pirminiame konteineryje tvarką.</span><span class="sxs-lookup"><span data-stu-id="23827-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="23827-173">Pasirinkite modulio daugtaškio mygtuką, tada naudokite rodyklės aukštyn arba rodyklės žemyn mygtukus.</span><span class="sxs-lookup"><span data-stu-id="23827-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23827-174">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="23827-174">Additional resources</span></span>

[<span data-ttu-id="23827-175">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="23827-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="23827-176">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="23827-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="23827-177">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="23827-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="23827-178">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="23827-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="23827-179">Konteinerio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="23827-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="23827-180">Turinio išdėstymo modulių įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="23827-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

