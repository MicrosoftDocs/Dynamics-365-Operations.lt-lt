---
title: Įkelti ir aptarnauti statinius failus
description: Šioje temoje paaiškina, kaip įkelti statinį failą į „Microsoft Dynamics 365 Commerce“ vietos kūrimo įrankį ir kaip sukurti tinkintą URL ir failo pavadinimą, kurį galima naudoti prašant to failo.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594985"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="2de77-103">Įkelti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="2de77-103">Upload and serve static files</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2de77-104">Šioje temoje paaiškina, kaip įkelti statinį failą į „Microsoft Dynamics 365 Commerce“ vietos kūrimo įrankį ir kaip sukurti tinkintą URL ir failo pavadinimą, kurį galima naudoti prašant to failo.</span><span class="sxs-lookup"><span data-stu-id="2de77-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="2de77-105">Kai kurios trečiųjų šalių jungtys reikalauja, kad failas būtų patalpintas ir aptarnautas e-komercijos saite.</span><span class="sxs-lookup"><span data-stu-id="2de77-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="2de77-106">Šios jungtys tikisi, kad failas bus grąžintas pagal užklausas į konkretų atšaukimo URL kelią ir failo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2de77-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="2de77-107">Dėl to, šioje temoje paaiškinta, kaip įkelti ir aptarnauti statinį failą, kuris turi vartotojo nustatytą URL ir failo pavadinimą „Dynamics 365 Commerce“ e-komercijos saite.</span><span class="sxs-lookup"><span data-stu-id="2de77-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="2de77-108">Sukurkite saito URL, kuris grąžina statinį failą</span><span class="sxs-lookup"><span data-stu-id="2de77-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="2de77-109">Siekiant sukurti saito URL, kuris grąžina statinį failą „Commerce“ vietos kūrimo įtaise, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="2de77-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2de77-110">Eikite į savo vietos medijos biblioteką ir įkelkite failą, kuris turi būti aptarnaujamas pagal užklausas į jūsų nustatytą URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="2de77-111">Jei jau įkėlėte failą, galite praleisti šį žingsnį.</span><span class="sxs-lookup"><span data-stu-id="2de77-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="2de77-112">Eikite į **URL** savo saite.</span><span class="sxs-lookup"><span data-stu-id="2de77-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="2de77-113">Pasirinkite **Naujas \> Naujas URL**.</span><span class="sxs-lookup"><span data-stu-id="2de77-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="2de77-114">Teksto laukelyje **Naujas URL** rinkitės **Medijos bibliotekos turinys**.</span><span class="sxs-lookup"><span data-stu-id="2de77-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="2de77-115">Laukelyje **URL kelias** įveskite URL kelią.</span><span class="sxs-lookup"><span data-stu-id="2de77-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="2de77-116">Įtraukti failo pavadinimą kelyje.</span><span class="sxs-lookup"><span data-stu-id="2de77-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="2de77-117">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="2de77-117">Select **Next**.</span></span> <span data-ttu-id="2de77-118">Medijos biblioteka yra atverta ir rodo visą medijos turinį pagal **Dokumento** tipą, kuris buvo įkeltas.</span><span class="sxs-lookup"><span data-stu-id="2de77-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="2de77-119">Pasirinkite failą, kuris turi būti rodomas užklausoms tame URL, kurį nustatėte žingsnyje 5.</span><span class="sxs-lookup"><span data-stu-id="2de77-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="2de77-120">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2de77-120">Select **Save**.</span></span>

<span data-ttu-id="2de77-121">Dabar URL, kurį sukūrėte yra šablono būsenoje.</span><span class="sxs-lookup"><span data-stu-id="2de77-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="2de77-122">Failas, į kurį veda URL, nebebus grąžinamas iki jums publikuojant URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="2de77-123">Prieš jums publikuojant URL, galite patvirtinti, kad būtų grąžinami tinkami duomenys.</span><span class="sxs-lookup"><span data-stu-id="2de77-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="2de77-124">Patvirtinti ir publikuoti URL</span><span class="sxs-lookup"><span data-stu-id="2de77-124">Validate and publish a URL</span></span>

<span data-ttu-id="2de77-125">Siekiant patvirtinti URL prieš jo publikavimą, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="2de77-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="2de77-126">Eikite į **URL** savo saite ir pasirinkite rodomą URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="2de77-127">Ypatybių juostoje dešinėje, po **Redaguoti** mygtuką, pasirinkite tinkamą URL nuorodą.</span><span class="sxs-lookup"><span data-stu-id="2de77-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="2de77-128">Naujame atvertame naršyklės lange turėtumėte matyti 404 klaidą.</span><span class="sxs-lookup"><span data-stu-id="2de77-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="2de77-129">Prikabinkite **?peržiūra=progrese** užklausos eilutę į URL (pavyzdžiui, `https://yoursite.com/callback.html?preview=inprogress`) ir iš naujo įkelkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2de77-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="2de77-130">Failas, kurį įkėlėte į medijos biblioteką turi grįžti į atsakymą.</span><span class="sxs-lookup"><span data-stu-id="2de77-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="2de77-131">Jums patvirtinus URL, galite jį publikuoti.</span><span class="sxs-lookup"><span data-stu-id="2de77-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="2de77-132">Eikite į **URL** savo saite ir pasirinkite rodomą URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="2de77-133">Pasirinkite **Publikuoti** komandos juostoje.</span><span class="sxs-lookup"><span data-stu-id="2de77-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="2de77-134">Naujinkite failą, į kurį veda URL</span><span class="sxs-lookup"><span data-stu-id="2de77-134">Update the file that a URL points to</span></span>

<span data-ttu-id="2de77-135">Po URL publikavimo, galite naujinti jį taip, kad jis rodytų į kitą failą.</span><span class="sxs-lookup"><span data-stu-id="2de77-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="2de77-136">Kitu atveju, galite naujinti URL taip, kad jis vestų į kitą išteklių tipą kaip aprašyta kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="2de77-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="2de77-137">Pavyzdžiui, galite nurodyti URL į vidaus puslapį ar nukreipimą.</span><span class="sxs-lookup"><span data-stu-id="2de77-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="2de77-138">Norėdami naujinti failą, į kurį rodo URL, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="2de77-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="2de77-139">Eikite į **URL** savo saite ir pasirinkite rodomą naujinama URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="2de77-140">Ypatybių juostoje dešinėje rinkitės **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2de77-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="2de77-141">Skyriuje **URL priskyrimas**, rinkitės **Žingsnis 2** laukelį ir tada rinkitės naują dokumentą iš medijos bibliotekos.</span><span class="sxs-lookup"><span data-stu-id="2de77-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="2de77-142">Pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="2de77-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="2de77-143">Naujinkite turinio tipą, į kurį veda URL</span><span class="sxs-lookup"><span data-stu-id="2de77-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="2de77-144">Galite taip pat naujinti URL taip, kad jis rodytų į kitą turinio tipą (išteklius), tokius kaip vidinį puslapį ar nukreipimą.</span><span class="sxs-lookup"><span data-stu-id="2de77-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="2de77-145">Norėdami naujinti turinio tipą, į kurį rodo URL, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="2de77-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="2de77-146">Eikite į **URL** savo saite ir pasirinkite rodomą naujinama URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="2de77-147">Ypatybių juostoje dešinėje rinkitės **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2de77-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="2de77-148">Skyriuje **URL priskyrimas**, **Žingsnis 1**, pasirinkite kitą turinio tipą.</span><span class="sxs-lookup"><span data-stu-id="2de77-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="2de77-149">Pasirinkite **Žingsnio 2** laukelį ir tada pasirinkite naują turinį.</span><span class="sxs-lookup"><span data-stu-id="2de77-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="2de77-150">Pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="2de77-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="2de77-151">Keiskite URL kelią</span><span class="sxs-lookup"><span data-stu-id="2de77-151">Change the URL path</span></span>

<span data-ttu-id="2de77-152">Sukūrus URL, jo kelio keisti nebepavyks.</span><span class="sxs-lookup"><span data-stu-id="2de77-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="2de77-153">Jei privaltoe keisti URL kelią, kuris reikalingas failui ar kito tipo ištekliams, turite sukurti naują URL, sudaryti jo žemėlapį į esantį failą ar kitą resursą ir tada nebepublikuoti bei panaikinti seną URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="2de77-154">Norėdami keisti URL kelią, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="2de77-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="2de77-155">Norėdami sukurti naują URL ir sudaryti jo žemėlapį į esantį failą ar kitą resursą, laikykitės šių instrukcijų [Sukurti saito URL, kuris grąžina statinį failą](#create-a-site-url-that-returns-a-static-file) skyrių anksčiau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="2de77-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="2de77-156">Pasirinkite naują URL ir rinkitės **Publikuoti** komandos juostoje.</span><span class="sxs-lookup"><span data-stu-id="2de77-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="2de77-157">Naujas URL yra publikuotas.</span><span class="sxs-lookup"><span data-stu-id="2de77-157">The new URL is published.</span></span>
1. <span data-ttu-id="2de77-158">Norėdami nepublikuoti seno URL, pasirinkte jį ir tada rinkitės **Nepublikuoti** komandų juostoje.</span><span class="sxs-lookup"><span data-stu-id="2de77-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="2de77-159">Dabar jei norite, galite panaikinti seną URL.</span><span class="sxs-lookup"><span data-stu-id="2de77-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2de77-160">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2de77-160">Additional resources</span></span>

[<span data-ttu-id="2de77-161">Skaitmeninio turto valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="2de77-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="2de77-162">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="2de77-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="2de77-163">Vaizdo įrašų įkėlimas</span><span class="sxs-lookup"><span data-stu-id="2de77-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="2de77-164">Kitų nei vaizdo ir vaizdo įrašų failų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="2de77-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="2de77-165">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="2de77-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="2de77-166">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="2de77-166">Customize image focal points</span></span>](dam-custom-focal-point.md)