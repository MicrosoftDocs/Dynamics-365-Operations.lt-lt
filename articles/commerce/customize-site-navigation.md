---
title: Svetainės naršymo tinkinimas
description: Šioje temoje aprašoma, kaip sukurti tinkintą interneto naršymo hierarchiją, kad būtų galima tvarkyti savo „Microsoft Dynamics 365 Commerce“ svetainėje naršomas prekes.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799354"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="0975b-103">Svetainės naršymo tinkinimas</span><span class="sxs-lookup"><span data-stu-id="0975b-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0975b-104">Šioje temoje aprašoma, kaip sukurti tinkintą interneto naršymo hierarchiją, kad būtų galima tvarkyti savo „Microsoft Dynamics 365 Commerce“ svetainėje naršomas prekes.</span><span class="sxs-lookup"><span data-stu-id="0975b-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="0975b-105">Internetinėse vitrinose paprastai klientai gali atrasti ir naršyti produktus, naršydami per produktų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="0975b-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="0975b-106">Šią galimybę paprastai teikiama skirtukais puslapio viršuje arba naršymo juosta kairėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="0975b-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="0975b-107">„Dynamics 365 Commerce“ galite kurti ir valdyti savo hierarchinę, kategorijų naršymo ir į įvairias kategorijas įtrauktų produktų, struktūrą.</span><span class="sxs-lookup"><span data-stu-id="0975b-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="0975b-108">Kanalo naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="0975b-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="0975b-109">Norėdami sukurti kanalo naršymo hierarchiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0975b-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="0975b-110">Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kategorijų ir produktų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="0975b-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="0975b-111">Pasirinkite **Kategorijų hierarchijos** ir pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="0975b-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="0975b-112">Pavadinkite hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="0975b-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0975b-113">Jūsų kuriama pagrindinė kategorija yra šakninis kategorijos mazgas.</span><span class="sxs-lookup"><span data-stu-id="0975b-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="0975b-114">Ji nebus rodoma jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="0975b-114">It won't be shown on your site.</span></span> <span data-ttu-id="0975b-115">Norėdami sukurti kategorijų hierarchiją, kurioje jūsų svetainėje rodomas vienas aukščiausio lygio mazgas, sukurkite ir pavadinkite kategoriją kaip šakninės kategorijos antrinį elementą.</span><span class="sxs-lookup"><span data-stu-id="0975b-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="0975b-116">Pasirinkite **Naujas kategorijos mazgas** ir pavadinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="0975b-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="0975b-117">Toliau kurkite pirmines ir antrines kategorijas, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="0975b-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="0975b-118">Dabar galite priskirti produktus kiekvienai kategorijai, kurią sukūrėte pagal aukščiausio lygio kategoriją.</span><span class="sxs-lookup"><span data-stu-id="0975b-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="0975b-119">Kategorijų tvarkos tinkinimas</span><span class="sxs-lookup"><span data-stu-id="0975b-119">Customize the order of categories</span></span>

<span data-ttu-id="0975b-120">Pagal numatytuosius parametrus, jūsų nustatytos kategorijos svetainėje bus rodomos abėcėlės tvarka.</span><span class="sxs-lookup"><span data-stu-id="0975b-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="0975b-121">Tačiau, taip pat galite tinkinti kategorijų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="0975b-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="0975b-122">Kategorijų hierarchijos tipo priskyrimas</span><span class="sxs-lookup"><span data-stu-id="0975b-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="0975b-123">Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kategorijų ir produktų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="0975b-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="0975b-124">Pasirinkite **Kategorijų hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="0975b-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="0975b-125">Veiksmų srities skirtuko **Kategorijų hierarchija** grupėje **Nustatyti** pasirinkite **Susieti hierarchijos tipą**.</span><span class="sxs-lookup"><span data-stu-id="0975b-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="0975b-126">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0975b-126">Select **New**.</span></span>
1. <span data-ttu-id="0975b-127">Lauke **Kategorijų hierarchijos tipas** pasirinkite **Kanalo naršymo hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="0975b-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="0975b-128">Lauke **Kategorijų hierarchija** pasirinkite kanalo naršymo hierarchiją, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="0975b-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="0975b-129">Naujų ar atnaujintų naršymo hierarchijų publikavimas</span><span class="sxs-lookup"><span data-stu-id="0975b-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="0975b-130">Norėdami, kad jūsų naršymo hierarchija būtų pasiekiama jūsų internetinėje vitrinoje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0975b-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="0975b-131">Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.</span><span class="sxs-lookup"><span data-stu-id="0975b-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="0975b-132">Kairėje esančiame medyje pasirinkite savo internetinę parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="0975b-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="0975b-133">Pasirinkite **Publikuoti kanalo naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="0975b-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="0975b-134">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="0975b-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="0975b-135">Sąraše raskite ir pasirinkite **Užduotis 1040**.</span><span class="sxs-lookup"><span data-stu-id="0975b-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="0975b-136">Pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="0975b-136">Select **Run now**.</span></span>
1. <span data-ttu-id="0975b-137">Pakartokite 5 ir 6 veiksmus, skirtus užduotims 1070 ir 1150.</span><span class="sxs-lookup"><span data-stu-id="0975b-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="0975b-138">Kategorijų rodymas jūsų svetainėje</span><span class="sxs-lookup"><span data-stu-id="0975b-138">Show categories on your site</span></span>

<span data-ttu-id="0975b-139">Norėdami savo kategorijų hierarchiją rodyti savo internetinėje vitrinoje, turite įtraukti naršymo meniu modulį į atitinkamas šablono ar fragmento vietas.</span><span class="sxs-lookup"><span data-stu-id="0975b-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="0975b-140">Tada naršymo meniu modulis rodys naršymo hierarchiją, jei savo naršymo hierarchiją publikavote kanale, su kuriuo yra susieta jūsų svetainė.</span><span class="sxs-lookup"><span data-stu-id="0975b-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="0975b-141">Naršymo meniu modulis, įtrauktas į modulių biblioteką, leidžia vartotojams pereiti tik į kategorijas, kurios neturi papildomų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="0975b-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="0975b-142">Jei jūsų klientai turėtų galėti pereiti į kategorijas, kurios turi subkategorijas, turite tinkinti naršymo meniu modulį.</span><span class="sxs-lookup"><span data-stu-id="0975b-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="0975b-143">Pasirinktinių naršymo parinkčių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="0975b-143">Add custom navigation options</span></span>

<span data-ttu-id="0975b-144">Naršymo meniu galite pridėti naršymo parinktis, kurios nepriklauso jūsų produktų kategorijų hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="0975b-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="0975b-145">Pavyzdžiui, produktų kategorijų sąrašo pabaigoje galite pridėti elementą **Susisiekite su mumis**, kuris nurodo kontaktinį puslapį, kurį sukūrėte savo svetainei.</span><span class="sxs-lookup"><span data-stu-id="0975b-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="0975b-146">Norėdami į naršymo meniu įtraukti pasirinktines naršymo parinktis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0975b-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="0975b-147">Norimame tinkinti šablone ar fragmente pasirinkite naršymo meniu modulį.</span><span class="sxs-lookup"><span data-stu-id="0975b-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="0975b-148">Ypatybių srityje, skirtuke **Duomenys**, pasirinkite **Įtraukti elementą**, kad sukurtumėte naują turinio valdymo sistemos (CMS) naršymo elementą.</span><span class="sxs-lookup"><span data-stu-id="0975b-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="0975b-149">Įveskite saito tekstą ir URL.</span><span class="sxs-lookup"><span data-stu-id="0975b-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="0975b-150">2 ir 3 veiksmus pakartokite, kad įtrauktumėte daugiau pasirinktinių naršymo parinkčių.</span><span class="sxs-lookup"><span data-stu-id="0975b-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="0975b-151">Baigę pasirinkite **Įrašyti**, kad įrašytumėte šabloną ar fragmentą, o tada pasirinkite **Baigti redagavimą**, kad įrašytumėte ir atrakintumėte.</span><span class="sxs-lookup"><span data-stu-id="0975b-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0975b-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0975b-152">Additional resources</span></span>

[<span data-ttu-id="0975b-153">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="0975b-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="0975b-154">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="0975b-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="0975b-155">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="0975b-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="0975b-156">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="0975b-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="0975b-157">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="0975b-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="0975b-158">Kurti puslapio URL</span><span class="sxs-lookup"><span data-stu-id="0975b-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="0975b-159">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="0975b-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
