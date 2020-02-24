---
title: Modifikuoti esamą svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ modifikuoti esamą svetainės puslapį.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c393fc143214c2c7c7ddad9a77e273e1e53e34ac
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003446"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="8c76d-103">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="8c76d-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8c76d-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ modifikuoti esamą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="8c76d-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8c76d-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="8c76d-105">Overview</span></span>

<span data-ttu-id="8c76d-106">Kai reikia modifikuoti puslapį, pirmausia jį atidarykite puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="8c76d-107">Eikite į svetainę, kurioje yra jūsų puslapis, tada puslapių sąraše susiraskite norimą puslapį.</span><span class="sxs-lookup"><span data-stu-id="8c76d-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="8c76d-108">Jei negalite rasti puslapio, galite naudoti kūrimo įrankio sudėtinės ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="8c76d-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="8c76d-109">Įveskite tikslų puslapio pavadinimą arba įveskite pirmas kelias jo raides, o tada – žvaigždutę (\*).</span><span class="sxs-lookup"><span data-stu-id="8c76d-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="8c76d-110">Atsiranda filtruotas puslapių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="8c76d-110">A filtered list of pages appears.</span></span> <span data-ttu-id="8c76d-111">Galite naudoti šį sąrašą, norėdami rasti norimą puslapį.</span><span class="sxs-lookup"><span data-stu-id="8c76d-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="8c76d-112">Radę teisingą puslapį, pasirinkite puslapio pavadinimą, kad puslapis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="8c76d-113">Jei puslapis matomas puslapio inspektoriuje, galite jį pasirinkti ir patikrinti prieš atidarydami jį puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="8c76d-114">Tokiu būdu galite vienu metu patikrinti keletą puslapių.</span><span class="sxs-lookup"><span data-stu-id="8c76d-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="8c76d-115">Atidarę puslapį puslapio rengyklėje, turite įsitikinti, kad jis paimtas ir užrakintas.</span><span class="sxs-lookup"><span data-stu-id="8c76d-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="8c76d-116">Kūrimo įrankio komandų juosta yra dinamiška, kontekstinė ir galinti skirti būsenas.</span><span class="sxs-lookup"><span data-stu-id="8c76d-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="8c76d-117">Todėl joje rodomi tik veiksmai, kuriuos galite šiuo metu įvykdyti puslapyje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="8c76d-118">Pavyzdžiui, jei puslapis nepaimtas ir neužrakintas, komandų juostoje nerodomi mygtukai **Įrašyti** ir **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="8c76d-119">Taip pat puslapio būsena rodoma dešinėje lango pusėje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="8c76d-120">Jei puslapis dar nepaimtas ir neužrakintas, pasirinkite komandų juostoje **Paimti ir užrakinti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="8c76d-121">Komandų juosta pasikeičia, kad atsispindėtų nauja puslapio būsena.</span><span class="sxs-lookup"><span data-stu-id="8c76d-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="8c76d-122">Taip pat gausite pranešimą, kuriame teigiama, kad puslapis paimtas ir užrakintas.</span><span class="sxs-lookup"><span data-stu-id="8c76d-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="8c76d-123">Kitas veiksmas – atlikti faktinius keitimus.</span><span class="sxs-lookup"><span data-stu-id="8c76d-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="8c76d-124">Dažnai naudosite puslapio struktūros medį kairėje, norėdami rasti ir pasirinkti modulį, kurį norite keisti, o tada atliksite keitimus dešiniojoje ypatybių srityje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="8c76d-125">Tačiau jūsų keitimai kartais gali apimti modelių ar fragmentų pridėjimą arba pašalinimą.</span><span class="sxs-lookup"><span data-stu-id="8c76d-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="8c76d-126">Norėdami įtraukti fragmentą ar modulį, naudokite puslapio struktūros medį, kad rastumėte atkarpą, į kurią norite įtraukti modulį arba fragmentą, ir tada pasirinkite daugtaškio mygtuką (**...**) tai atkarpai.</span><span class="sxs-lookup"><span data-stu-id="8c76d-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="8c76d-127">Pasirodys meniu, kuriame yra komandų, skirtų pridėti modulį ar fragmentą.</span><span class="sxs-lookup"><span data-stu-id="8c76d-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="8c76d-128">Norėdami pašalinti modulį arba fragmentą, suraskite ir pasirinkite jį puslapio struktūros medyje, pasirinkite daugtaškio mygtuką ir pasirinkite komandą, kad panaikintumėte modulį ar fragmentą.</span><span class="sxs-lookup"><span data-stu-id="8c76d-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="8c76d-129">Taip pat galite peržiūrėti ir redaguoti bet kurio modulio, kuris matomas „ką matote, tą ir gaunate“ (WYSIWYG) peržiūoje, ypatybes, pasirinkdami jas tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="8c76d-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="8c76d-130">Atlikę keitimus ir peržiūrėję jų efektyvumą, turite puslapį įrašyti ir atrakinti, pasirinkdami komandų juostoje **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="8c76d-131">Norėdami nedelsiant publikuoti savo keitimus, komandų juostoje pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="8c76d-132">Naujausia įrašyta ir atrakinta puslapio versija, kurią modifikavote, yra publikuojama ir tampa pasiekiama išoriniams vartotojams, kurie mato jūsų svetainę.</span><span class="sxs-lookup"><span data-stu-id="8c76d-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="8c76d-133">Pavyzdys: Vaizdo įrašo keitimas pagrindiniame puslapyje</span><span class="sxs-lookup"><span data-stu-id="8c76d-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="8c76d-134">Šiame pavyzdyje parodyta, kaip modifikuoti pagrindinį puslapį, keičiant vaizdo įrašų leistuvo modulyje rodomą vaizdo įrašą.</span><span class="sxs-lookup"><span data-stu-id="8c76d-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="8c76d-135">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="8c76d-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8c76d-136">Kairėje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="8c76d-137">Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="8c76d-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="8c76d-138">Komandų juostoje pasirinkite **Paimti ir užrakinti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="8c76d-139">Puslapio struktūroje pasirinkite atkarpą **Pagrindinis**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="8c76d-140">Atkarpoje **Pagrindinis** išplėskite visus nepastovius konteinerio modulius.</span><span class="sxs-lookup"><span data-stu-id="8c76d-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="8c76d-141">Suraskite ir pasirinkite vaizdo įrašų leistuvo modulį.</span><span class="sxs-lookup"><span data-stu-id="8c76d-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="8c76d-142">Dešiniojoje ypatybių srityje pasirinkite **vaizdo įrašo** ypatybę.</span><span class="sxs-lookup"><span data-stu-id="8c76d-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="8c76d-143">Atsiranda išteklių parinkiklis.</span><span class="sxs-lookup"><span data-stu-id="8c76d-143">The asset picker appears.</span></span>
1. <span data-ttu-id="8c76d-144">Išteklių parinkiklyje pasirinkite galimą vaizdo įrašo išteklių arba pasirinkite **įkelti naują išteklių**, kad įkeltumėte naują vaizdo įrašo išteklių.</span><span class="sxs-lookup"><span data-stu-id="8c76d-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="8c76d-145">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-145">Select **OK**.</span></span>
1. <span data-ttu-id="8c76d-146">Pasirinkite **Įrašyti**, tada – **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="8c76d-147">Lauke **Komentarai** įveskite **Pakeisti vaizdo įrašą** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="8c76d-148">Norėdami peržiūrėti atnaujintą puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="8c76d-149">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="8c76d-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="8c76d-150">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="8c76d-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c76d-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8c76d-151">Additional resources</span></span>

[<span data-ttu-id="8c76d-152">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="8c76d-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="8c76d-153">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="8c76d-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8c76d-154">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="8c76d-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="8c76d-155">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="8c76d-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8c76d-156">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="8c76d-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="8c76d-157">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="8c76d-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="8c76d-158">Puslapio turinio pritaikymo neįgaliesiems patikra</span><span class="sxs-lookup"><span data-stu-id="8c76d-158">Verify page content accessibility</span></span>](verify-accessibility.md)
