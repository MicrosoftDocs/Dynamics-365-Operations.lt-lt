---
title: robots.txt failų tvarkymas
description: Šioje temoje aprašoma, kaip tvarkyti „robots.txt“ failus sprendime „Microsoft Dynamics 365 Commerce“.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794240"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="314b5-103">robots.txt failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="314b5-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="314b5-104">Šioje temoje aprašoma, kaip tvarkyti „robots.txt“ failus sprendime „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="314b5-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="314b5-105">Išimčių standartas robotams, arba „robots.txt“, yra standartas, kurį tinklapis naudoja bendrauti su interneto robotais.</span><span class="sxs-lookup"><span data-stu-id="314b5-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="314b5-106">Juo nurodoma interneto robotams apie svetainės dalis, kurių robotas neturėtų pasiekti.</span><span class="sxs-lookup"><span data-stu-id="314b5-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="314b5-107">Robotai dažnai naudojami ieškos moduliams indeksuojant svetaines.</span><span class="sxs-lookup"><span data-stu-id="314b5-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="314b5-108">Norėdami pašalinti robotus iš serverio, galite sukurti failą serveryje.</span><span class="sxs-lookup"><span data-stu-id="314b5-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="314b5-109">Šiame faile nurodote robotų prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="314b5-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="314b5-110">Failas turi būti prieinama per HTTP vietinio URL **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="314b5-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="314b5-111">Failas „robots.txt“ padeda ieškos moduliui indeksuoti jūsų svetainės turinį.</span><span class="sxs-lookup"><span data-stu-id="314b5-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="314b5-112">Naudodami „Dynamics 365 Commerce“ galite nusiųsti savo domeno failą „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="314b5-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="314b5-113">Kiekvienam „Commerce“ aplinkos domenui galite nusiųsti vieną failą „robots.txt“ ir susieti jį su tuo domenu.</span><span class="sxs-lookup"><span data-stu-id="314b5-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="314b5-114">Norėdami sužinoti daugiau informacijos apie failą „robots.txt“, apsilankykite [Interneto robotų puslapiai](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="314b5-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="314b5-115">Failo „robots.txt“ nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="314b5-115">Upload a robots.txt file</span></span>

<span data-ttu-id="314b5-116">Sukūrę ir redagavę savo „robots.txt“ failą pagal [robotų išimčių standartą](https://www.robotstxt.org/orig.html), įsitikinkite, kad failas yra pasiekiamas kompiuteryje, kuriame naudosite „Commerce“ kūrimo įrankius.</span><span class="sxs-lookup"><span data-stu-id="314b5-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="314b5-117">Failas turi būti pavadintas **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="314b5-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="314b5-118">Siekdami geriausių rezultatų, jis turi būti formatu, kuris yra nurodytas standarte.</span><span class="sxs-lookup"><span data-stu-id="314b5-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="314b5-119">Kiekvienas „Commerce“ klientas yra atsakingas už failo „robots.txt“ turinio patvirtinimą ir palaikymą.</span><span class="sxs-lookup"><span data-stu-id="314b5-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="314b5-120">Norėdami nusiųsti failą „robots.txt“, turite būti prisijungę prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="314b5-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="314b5-121">Norėdami nusiųsti failą „robots.txt“ į „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="314b5-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="314b5-122">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="314b5-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="314b5-123">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="314b5-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="314b5-124">Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="314b5-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="314b5-125">Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.</span><span class="sxs-lookup"><span data-stu-id="314b5-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="314b5-126">Pasirinkite **Valdyti**, kad nusiųstumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="314b5-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="314b5-127">Dešinėje esančiame meniu pasirinkite mygtuką **Nusiųsti** (aukštyn nukreipta rodyklė) šalia domeno, susieto su failu „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="314b5-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="314b5-128">Rodomas failo naršyklės dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="314b5-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="314b5-129">Dialogo lange naršykite ir pasirinkite failą „robots.txt“, kurį norite nusiųsti į susietą domeną, ir pasirinkite **Atidaryti**, kad užbaigtumėte nusiuntimą.</span><span class="sxs-lookup"><span data-stu-id="314b5-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="314b5-130">Įkėlimo metu „Commerce“ patikrina, ar failas yra tekstinis, bet nepatikrina failo turinio.</span><span class="sxs-lookup"><span data-stu-id="314b5-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="314b5-131">Failo „robots.txt“ atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="314b5-131">Download a robots.txt file</span></span>

<span data-ttu-id="314b5-132">Norėdami atsisiųsti failą „robots.txt“ iš „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="314b5-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="314b5-133">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="314b5-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="314b5-134">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="314b5-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="314b5-135">Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="314b5-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="314b5-136">Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.</span><span class="sxs-lookup"><span data-stu-id="314b5-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="314b5-137">Pasirinkite **Valdyti**, kad atsisiųstumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="314b5-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="314b5-138">Dešinėje esančiame meniu pasirinkite mygtuką **Atsisiųsti** (žemyn nukreipta rodyklė) šalia domeno, susieto su failu „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="314b5-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="314b5-139">Rodomas failo naršyklės dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="314b5-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="314b5-140">Dialogo lange eikite į norimą vietą vietiniame diske, patvirtinkite arba įveskite failo vardą, tada pasirinkite **Įrašyti**, kad užbaigtumėte atsisiuntimą.</span><span class="sxs-lookup"><span data-stu-id="314b5-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="314b5-141">Ši procedūra gali būti naudojama atsisiųsti tik „robots.txt“ failų, kurie anksčiau buvo nusiųsti per „Commerce“ kūrimo įrankius.</span><span class="sxs-lookup"><span data-stu-id="314b5-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="314b5-142">Failo „robots.txt“ naikinimas</span><span class="sxs-lookup"><span data-stu-id="314b5-142">Delete a robots.txt file</span></span>

<span data-ttu-id="314b5-143">Norėdami naikinti failą „robots.txt“ iš „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="314b5-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="314b5-144">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="314b5-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="314b5-145">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="314b5-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="314b5-146">Dalyje **Nuomotojo parametrai** pasirinkite **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="314b5-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="314b5-147">Visų domenų, susietų su jūsų aplinka, sąrašas rodomas pagrindinėje lango dalyje.</span><span class="sxs-lookup"><span data-stu-id="314b5-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="314b5-148">Pasirinkite **Valdyti**, kad naikintumėte failą „robots.txt“, skirtą domenui jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="314b5-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="314b5-149">Dešinėje esančiame meniu pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį šalia domeno, susieto su failu „robots.txt“.</span><span class="sxs-lookup"><span data-stu-id="314b5-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="314b5-150">Atsiranda failų naršyklės langas.</span><span class="sxs-lookup"><span data-stu-id="314b5-150">A file browser window appears.</span></span>
6. <span data-ttu-id="314b5-151">Failų naršyklės lange naršykite ir pasirinkite failą „robots.txt“, kurį norite naikinti domene, ir pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="314b5-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="314b5-152">Pasirodys įspėjimo pranešimo langas.</span><span class="sxs-lookup"><span data-stu-id="314b5-152">A warning message box appears.</span></span>
7. <span data-ttu-id="314b5-153">Pranešimo lauke pasirinkite **Naikinti**, kad patvirtintumėte failo „robots.txt“ naikinimą.</span><span class="sxs-lookup"><span data-stu-id="314b5-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="314b5-154">Ši procedūra gali būti naudojama naikinti tik „robots.txt“ failus, kurie anksčiau buvo nusiųsti per „Commerce“ kūrimo įrankius.</span><span class="sxs-lookup"><span data-stu-id="314b5-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="314b5-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="314b5-155">Additional resources</span></span>

[<span data-ttu-id="314b5-156">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="314b5-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="314b5-157">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="314b5-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="314b5-158">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="314b5-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="314b5-159">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="314b5-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="314b5-160">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="314b5-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="314b5-161">„Commerce” B2C nuomotojo sąranka</span><span class="sxs-lookup"><span data-stu-id="314b5-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="314b5-162">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="314b5-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="314b5-163">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="314b5-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="314b5-164">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="314b5-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="314b5-165">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="314b5-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
