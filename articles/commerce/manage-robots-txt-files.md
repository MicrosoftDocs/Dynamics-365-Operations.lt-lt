---
title: „Robots.txt” failų tvarkymas
description: Šioje temoje aprašoma, kaip tvarkyti „robots.txt“ failus sprendime „Microsoft Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f7a779d69bf49d3416de3e92d4414cfabf358eb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983628"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="5bc8a-103">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5bc8a-104">Šioje temoje aprašoma, kaip tvarkyti „robots.txt“ failus sprendime „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5bc8a-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="5bc8a-105">Overview</span></span>

<span data-ttu-id="5bc8a-106">Išimčių standartas robotams, arba „robots.txt“, yra standartas, kurį tinklapis naudoja bendrauti su interneto robotais.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="5bc8a-107">Juo nurodoma interneto robotams apie svetainės dalis, kurių robotas neturėtų pasiekti.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="5bc8a-108">Robotai dažnai naudojami ieškos moduliams indeksuojant svetaines.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="5bc8a-109">Norėdami pašalinti robotus iš serverio, galite sukurti failą serveryje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="5bc8a-110">Šiame faile nurodote robotų prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="5bc8a-111">Failas turi būti prieinama per HTTP vietinio URL **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="5bc8a-112">Failas „robots.txt“ padeda ieškos moduliui indeksuoti jūsų svetainės turinį.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="5bc8a-113">Naudodami „Dynamics 365 Commerce“ galite nusiųsti savo domeno failą „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="5bc8a-114">Kiekvienam „Commerce“ aplinkos domenui galite nusiųsti vieną failą „robots.txt“ ir susieti jį su tuo domenu.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="5bc8a-115">Norėdami sužinoti daugiau informacijos apie failą „robots.txt“, apsilankykite [Interneto robotų puslapiai](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="5bc8a-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="5bc8a-116">Failo „robots.txt“ nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-116">Upload a robots.txt file</span></span>

<span data-ttu-id="5bc8a-117">Sukūrę ir redagavę savo „robots.txt“ failą pagal [robotų išimčių standartą](https://www.robotstxt.org/orig.html), įsitikinkite, kad failas yra pasiekiamas kompiuteryje, kuriame naudosite „Commerce“ kūrimo įrankius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="5bc8a-118">Failas turi būti pavadintas **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="5bc8a-119">Siekdami geriausių rezultatų, jis turi būti formatu, kuris yra nurodytas standarte.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="5bc8a-120">Kiekvienas „Commerce“ klientas yra atsakingas už failo „robots.txt“ turinio patvirtinimą ir palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="5bc8a-121">Norėdami nusiųsti failą „robots.txt“, turite būti prisijungę prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="5bc8a-122">Norėdami nusiųsti failą „robots.txt“ į „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5bc8a-123">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5bc8a-124">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5bc8a-125">Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5bc8a-126">Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5bc8a-127">Pasirinkite **Valdyti**, kad nusiųstumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5bc8a-128">Dešinėje esančiame meniu pasirinkite mygtuką **Nusiųsti** (aukštyn nukreipta rodyklė) šalia domeno, susieto su failu „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5bc8a-129">Rodomas failo naršyklės dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5bc8a-130">Dialogo lange naršykite ir pasirinkite failą „robots.txt“, kurį norite nusiųsti į susietą domeną, ir pasirinkite **Atidaryti**, kad užbaigtumėte nusiuntimą.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="5bc8a-131">Įkėlimo metu „Commerce“ patikrina, ar failas yra tekstinis, bet nepatikrina failo turinio.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="5bc8a-132">Failo „robots.txt“ atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-132">Download a robots.txt file</span></span>

<span data-ttu-id="5bc8a-133">Norėdami atsisiųsti failą „robots.txt“ iš „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5bc8a-134">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5bc8a-135">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5bc8a-136">Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5bc8a-137">Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5bc8a-138">Pasirinkite **Valdyti**, kad atsisiųstumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5bc8a-139">Dešinėje esančiame meniu pasirinkite mygtuką **Atsisiųsti** (žemyn nukreipta rodyklė) šalia domeno, susieto su failu „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5bc8a-140">Rodomas failo naršyklės dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5bc8a-141">Dialogo lange eikite į norimą vietą vietiniame diske, patvirtinkite arba įveskite failo vardą, tada pasirinkite **Įrašyti**, kad užbaigtumėte atsisiuntimą.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="5bc8a-142">Ši procedūra gali būti naudojama atsisiųsti tik „robots.txt“ failų, kurie anksčiau buvo nusiųsti per „Commerce“ kūrimo įrankius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="5bc8a-143">Failo „robots.txt“ naikinimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-143">Delete a robots.txt file</span></span>

<span data-ttu-id="5bc8a-144">Norėdami naikinti failą „robots.txt“ iš „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5bc8a-145">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5bc8a-146">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5bc8a-147">Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5bc8a-148">Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5bc8a-149">Pasirinkite **Valdyti**, kad naikintumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5bc8a-150">Dešinėje esančiame meniu pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį šalia domeno, susieto su failu „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5bc8a-151">Atsiranda failų naršyklės langas.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-151">A file browser window appears.</span></span>
6. <span data-ttu-id="5bc8a-152">Failų naršyklės lange naršykite ir pasirinkite failą „robots.txt“, kurį norite naikinti domene, ir pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="5bc8a-153">Pasirodys įspėjimo pranešimo langas.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-153">A warning message box appears.</span></span>
7. <span data-ttu-id="5bc8a-154">Pranešimo lauke pasirinkite **Naikinti**, kad patvirtintumėte failo „robots.txt“ naikinimą.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="5bc8a-155">Ši procedūra gali būti naudojama naikinti tik „robots.txt“ failus, kurie anksčiau buvo nusiųsti per „Commerce“ kūrimo įrankius.</span><span class="sxs-lookup"><span data-stu-id="5bc8a-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bc8a-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5bc8a-156">Additional resources</span></span>

[<span data-ttu-id="5bc8a-157">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5bc8a-158">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5bc8a-159">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5bc8a-160">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="5bc8a-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5bc8a-161">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="5bc8a-162">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="5bc8a-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="5bc8a-163">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="5bc8a-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5bc8a-164">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="5bc8a-165">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5bc8a-166">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="5bc8a-166">Enable location-based store detection</span></span>](enable-store-detection.md)
