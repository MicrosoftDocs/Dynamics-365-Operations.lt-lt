---
title: Modifikuoti esamą svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ modifikuoti esamą svetainės puslapį.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803734"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="b6979-103">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="b6979-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6979-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ modifikuoti esamą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6979-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b6979-105">Kai reikia modifikuoti puslapį, pirmiausia jį atidarykite puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="b6979-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="b6979-106">Eikite į svetainę, kurioje yra jūsų puslapis, tada puslapių sąraše susiraskite norimą puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6979-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="b6979-107">Jei negalite rasti puslapio, galite naudoti kūrimo įrankio sudėtinės ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="b6979-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="b6979-108">Įveskite tikslų puslapio pavadinimą arba įveskite pirmas kelias jo raides, o tada – žvaigždutę (\*).</span><span class="sxs-lookup"><span data-stu-id="b6979-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="b6979-109">Atsiranda filtruotas puslapių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b6979-109">A filtered list of pages appears.</span></span> <span data-ttu-id="b6979-110">Galite naudoti šį sąrašą, norėdami rasti norimą puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6979-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="b6979-111">Radę teisingą puslapį, pasirinkite puslapio pavadinimą, kad puslapis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="b6979-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="b6979-112">Jei puslapis matomas puslapio inspektoriuje, galite pasirinkti **Redaguoti** ir išregistruoti puslapį prieš atidarydami jį puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="b6979-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="b6979-113">Tokiu būdu galite vienu metu patikrinti keletą puslapių.</span><span class="sxs-lookup"><span data-stu-id="b6979-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="b6979-114">Atidarę puslapį puslapio rengyklėje, turite įsitikinti, kad jis paimtas ir užrakintas.</span><span class="sxs-lookup"><span data-stu-id="b6979-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="b6979-115">Kūrimo įrankio komandų juosta yra dinamiška, kontekstinė ir galinti skirti būsenas.</span><span class="sxs-lookup"><span data-stu-id="b6979-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="b6979-116">Todėl joje rodomi tik veiksmai, kuriuos galite šiuo metu įvykdyti puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b6979-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="b6979-117">Pavyzdžiui, jei puslapis nepaimtas ir neužrakintas, komandų juostoje nerodomi mygtukai **Įrašyti** ir **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b6979-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="b6979-118">Taip pat puslapio būsena rodoma dešinėje lango pusėje.</span><span class="sxs-lookup"><span data-stu-id="b6979-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="b6979-119">Jei puslapis dar nepaimtas ir neužrakintas, pasirinkite komandų juostoje **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b6979-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="b6979-120">Komandų juosta pasikeičia, kad atsispindėtų nauja puslapio būsena.</span><span class="sxs-lookup"><span data-stu-id="b6979-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="b6979-121">Taip pat gausite pranešimą, kuriame teigiama, kad puslapis paimtas ir užrakintas.</span><span class="sxs-lookup"><span data-stu-id="b6979-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="b6979-122">Kitas veiksmas – atlikti faktinius keitimus.</span><span class="sxs-lookup"><span data-stu-id="b6979-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="b6979-123">Dažnai naudosite puslapio struktūros medį kairėje, norėdami rasti ir pasirinkti modulį, kurį norite keisti, o tada atliksite keitimus dešiniojoje ypatybių srityje.</span><span class="sxs-lookup"><span data-stu-id="b6979-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="b6979-124">Tačiau jūsų keitimai kartais gali apimti modelių ar fragmentų pridėjimą arba pašalinimą.</span><span class="sxs-lookup"><span data-stu-id="b6979-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="b6979-125">Norėdami įtraukti fragmentą ar modulį, naudokite puslapio struktūros medį, kad rastumėte atkarpą, į kurią norite įtraukti modulį arba fragmentą, ir tada pasirinkite daugtaškio mygtuką (**...**) tai atkarpai.</span><span class="sxs-lookup"><span data-stu-id="b6979-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="b6979-126">Pasirodys meniu, kuriame yra komandų, skirtų pridėti modulį ar fragmentą.</span><span class="sxs-lookup"><span data-stu-id="b6979-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="b6979-127">Norėdami pašalinti modulį arba fragmentą, suraskite ir pasirinkite jį puslapio struktūros medyje, pasirinkite daugtaškio mygtuką ir pasirinkite komandą, kad panaikintumėte modulį ar fragmentą.</span><span class="sxs-lookup"><span data-stu-id="b6979-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="b6979-128">Taip pat galite peržiūrėti ir redaguoti bet kurio modulio, kuris matomas puslapio daryklės peržiūroje, ypatybes, pasirinkdami jas tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="b6979-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="b6979-129">Atlikę keitimus ir peržiūrėję jų efektyvumą, turite puslapį įrašyti ir atrakinti, pasirinkdami komandų juostoje **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b6979-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="b6979-130">Norėdami nedelsiant publikuoti savo keitimus, komandų juostoje pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b6979-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="b6979-131">Naujausia įrašyta ir atrakinta puslapio versija, kurią modifikavote, yra publikuojama ir tampa pasiekiama išoriniams vartotojams, kurie mato jūsų svetainę.</span><span class="sxs-lookup"><span data-stu-id="b6979-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="b6979-132">Pavyzdys: Vaizdo įrašo keitimas pagrindiniame puslapyje</span><span class="sxs-lookup"><span data-stu-id="b6979-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="b6979-133">Šiame pavyzdyje parodyta, kaip modifikuoti pagrindinį puslapį, keičiant vaizdo įrašų leistuvo modulyje rodomą vaizdo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6979-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="b6979-134">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="b6979-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b6979-135">Kairėje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="b6979-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="b6979-136">Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="b6979-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="b6979-137">Komandų juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b6979-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="b6979-138">Puslapio struktūroje pasirinkite atkarpą **Pagrindinis**.</span><span class="sxs-lookup"><span data-stu-id="b6979-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="b6979-139">Atkarpoje **Pagrindinis** išplėskite visus nepastovius konteinerio modulius.</span><span class="sxs-lookup"><span data-stu-id="b6979-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="b6979-140">Suraskite ir pasirinkite vaizdo įrašų leistuvo modulį.</span><span class="sxs-lookup"><span data-stu-id="b6979-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="b6979-141">Dešiniojoje ypatybių srityje pasirinkite **vaizdo įrašo** ypatybę.</span><span class="sxs-lookup"><span data-stu-id="b6979-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="b6979-142">Atsiranda išteklių parinkiklis.</span><span class="sxs-lookup"><span data-stu-id="b6979-142">The asset picker appears.</span></span>
1. <span data-ttu-id="b6979-143">Išteklių parinkiklyje pasirinkite galimą vaizdo įrašo išteklių arba pasirinkite **įkelti naują išteklių**, kad įkeltumėte naują vaizdo įrašo išteklių.</span><span class="sxs-lookup"><span data-stu-id="b6979-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="b6979-144">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b6979-144">Select **OK**.</span></span>
1. <span data-ttu-id="b6979-145">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b6979-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b6979-146">Lauke **Komentarai** įveskite **Pakeisti vaizdo įrašą** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b6979-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="b6979-147">Norėdami peržiūrėti atnaujintą puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="b6979-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="b6979-148">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="b6979-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="b6979-149">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b6979-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6979-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b6979-150">Additional resources</span></span>

[<span data-ttu-id="b6979-151">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="b6979-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b6979-152">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="b6979-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b6979-153">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="b6979-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b6979-154">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="b6979-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b6979-155">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="b6979-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b6979-156">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="b6979-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="b6979-157">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="b6979-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="b6979-158">Sukurti dinaminius e-komercijos puslapius pagal URL parametrus</span><span class="sxs-lookup"><span data-stu-id="b6979-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
