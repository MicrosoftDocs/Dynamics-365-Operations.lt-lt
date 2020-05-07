---
title: Svetainės naršymo tinkinimas
description: Šioje temoje aprašoma, kaip sukurti tinkintą interneto naršymo hierarchiją, kad būtų galima tvarkyti savo „Microsoft Dynamics 365 Commerce“ svetainėje naršomas prekes.
author: bicyclingfool
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7696dcb5cdd99cd46b89ed1de1b03c16146e2d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269664"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="fc14a-103">Svetainės naršymo tinkinimas</span><span class="sxs-lookup"><span data-stu-id="fc14a-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fc14a-104">Šioje temoje aprašoma, kaip sukurti tinkintą interneto naršymo hierarchiją, kad būtų galima tvarkyti savo „Microsoft Dynamics 365 Commerce“ svetainėje naršomas prekes.</span><span class="sxs-lookup"><span data-stu-id="fc14a-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="fc14a-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="fc14a-105">Overview</span></span>

<span data-ttu-id="fc14a-106">Internetinėse vitrinose paprastai klientai gali atrasti ir naršyti produktus, naršydami per produktų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="fc14a-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="fc14a-107">Šią galimybę paprastai teikiama skirtukais puslapio viršuje arba naršymo juosta kairėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="fc14a-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="fc14a-108">„Dynamics 365 Commerce“ galite kurti ir valdyti savo hierarchinę, kategorijų naršymo ir į įvairias kategorijas įtrauktų produktų, struktūrą.</span><span class="sxs-lookup"><span data-stu-id="fc14a-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="fc14a-109">Kanalo naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="fc14a-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="fc14a-110">Norėdami sukurti kanalo naršymo hierarchiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fc14a-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="fc14a-111">Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kategorijų ir produktų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="fc14a-112">Pasirinkite **Kategorijų hierarchijos** ir pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="fc14a-113">Pavadinkite hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="fc14a-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fc14a-114">Jūsų kuriama pagrindinė kategorija yra šakninis kategorijos mazgas.</span><span class="sxs-lookup"><span data-stu-id="fc14a-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="fc14a-115">Ji nebus rodoma jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="fc14a-115">It won't be shown on your site.</span></span> <span data-ttu-id="fc14a-116">Norėdami sukurti kategorijų hierarchiją, kurioje jūsų svetainėje rodomas vienas aukščiausio lygio mazgas, sukurkite ir pavadinkite kategoriją kaip šakninės kategorijos antrinį elementą.</span><span class="sxs-lookup"><span data-stu-id="fc14a-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="fc14a-117">Pasirinkite **Naujas kategorijos mazgas** ir pavadinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="fc14a-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="fc14a-118">Toliau kurkite pirmines ir antrines kategorijas, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="fc14a-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="fc14a-119">Dabar galite priskirti produktus kiekvienai kategorijai, kurią sukūrėte pagal aukščiausio lygio kategoriją.</span><span class="sxs-lookup"><span data-stu-id="fc14a-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="fc14a-120">Kategorijų tvarkos tinkinimas</span><span class="sxs-lookup"><span data-stu-id="fc14a-120">Customize the order of categories</span></span>

<span data-ttu-id="fc14a-121">Pagal numatytuosius parametrus, jūsų nustatytos kategorijos svetainėje bus rodomos abėcėlės tvarka.</span><span class="sxs-lookup"><span data-stu-id="fc14a-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="fc14a-122">Tačiau, taip pat galite tinkinti kategorijų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="fc14a-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="fc14a-123">Kategorijų hierarchijos tipo priskyrimas</span><span class="sxs-lookup"><span data-stu-id="fc14a-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="fc14a-124">Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kategorijų ir produktų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="fc14a-125">Pasirinkite **Kategorijų hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="fc14a-126">Veiksmų srities skirtuko **Kategorijų hierarchija** grupėje **Nustatyti** pasirinkite **Susieti hierarchijos tipą**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="fc14a-127">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-127">Select **New**.</span></span>
1. <span data-ttu-id="fc14a-128">Lauke **Kategorijų hierarchijos tipas** pasirinkite **Kanalo naršymo hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="fc14a-129">Lauke **Kategorijų hierarchija** pasirinkite kanalo naršymo hierarchiją, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="fc14a-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="fc14a-130">Naujų ar atnaujintų naršymo hierarchijų publikavimas</span><span class="sxs-lookup"><span data-stu-id="fc14a-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="fc14a-131">Norėdami, kad jūsų naršymo hierarchija būtų pasiekiama jūsų internetinėje vitrinoje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fc14a-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="fc14a-132">Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="fc14a-133">Kairėje esančiame medyje pasirinkite savo internetinę parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="fc14a-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="fc14a-134">Pasirinkite **Publikuoti kanalo naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="fc14a-135">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="fc14a-136">Sąraše raskite ir pasirinkite **Užduotis 1040**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="fc14a-137">Pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="fc14a-137">Select **Run now**.</span></span>
1. <span data-ttu-id="fc14a-138">Pakartokite 5 ir 6 veiksmus, skirtus užduotims 1070 ir 1150.</span><span class="sxs-lookup"><span data-stu-id="fc14a-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="fc14a-139">Kategorijų rodymas jūsų svetainėje</span><span class="sxs-lookup"><span data-stu-id="fc14a-139">Show categories on your site</span></span>

<span data-ttu-id="fc14a-140">Norėdami savo kategorijų hierarchiją rodyti savo internetinėje vitrinoje, turite įtraukti naršymo meniu modulį į atitinkamas šablono ar fragmento vietas.</span><span class="sxs-lookup"><span data-stu-id="fc14a-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="fc14a-141">Tada naršymo meniu modulis rodys naršymo hierarchiją, jei savo naršymo hierarchiją publikavote kanale, su kuriuo yra susieta jūsų svetainė.</span><span class="sxs-lookup"><span data-stu-id="fc14a-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="fc14a-142">Naršymo meniu modulis, įtrauktas į parduotuvės darbo pradžios rinkinį, leidžia vartotojams pereiti tik į kategorijas, kurios neturi subkategorijų.</span><span class="sxs-lookup"><span data-stu-id="fc14a-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="fc14a-143">Jei jūsų klientai turėtų galėti pereiti į kategorijas, kurios turi subkategorijas, turite tinkinti naršymo meniu modulį.</span><span class="sxs-lookup"><span data-stu-id="fc14a-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="fc14a-144">Pasirinktinių naršymo parinkčių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="fc14a-144">Add custom navigation options</span></span>

<span data-ttu-id="fc14a-145">Naršymo meniu galite pridėti naršymo parinktis, kurios nepriklauso jūsų produktų kategorijų hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="fc14a-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="fc14a-146">Pavyzdžiui, produktų kategorijų sąrašo pabaigoje galite pridėti elementą **Susisiekite su mumis**, kuris nurodo kontaktinį puslapį, kurį sukūrėte savo svetainei.</span><span class="sxs-lookup"><span data-stu-id="fc14a-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="fc14a-147">Norėdami į naršymo meniu įtraukti pasirinktines naršymo parinktis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fc14a-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="fc14a-148">Norimame tinkinti šablone ar fragmente pasirinkite naršymo meniu modulį.</span><span class="sxs-lookup"><span data-stu-id="fc14a-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="fc14a-149">Ypatybių srityje, skirtuke **Duomenys**, pasirinkite **Įtraukti elementą**, kad sukurtumėte naują turinio valdymo sistemos (TVS) naršymo elementą.</span><span class="sxs-lookup"><span data-stu-id="fc14a-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="fc14a-150">Įveskite saito tekstą ir URL.</span><span class="sxs-lookup"><span data-stu-id="fc14a-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="fc14a-151">2 ir 3 veiksmus pakartokite, kad įtrauktumėte daugiau pasirinktinių naršymo parinkčių.</span><span class="sxs-lookup"><span data-stu-id="fc14a-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="fc14a-152">Baigę pasirinkite **Įrašyti**, kad įrašytumėte šabloną ar fragmentą, o tada pasirinkite **Baigti redagavimą**, kad įrašytumėte ir atrakintumėte.</span><span class="sxs-lookup"><span data-stu-id="fc14a-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc14a-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fc14a-153">Additional resources</span></span>

[<span data-ttu-id="fc14a-154">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="fc14a-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="fc14a-155">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="fc14a-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="fc14a-156">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="fc14a-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="fc14a-157">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="fc14a-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="fc14a-158">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="fc14a-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="fc14a-159">Kurti puslapio URL</span><span class="sxs-lookup"><span data-stu-id="fc14a-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="fc14a-160">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="fc14a-160">Work with publish groups</span></span>](publish-groups.md)
