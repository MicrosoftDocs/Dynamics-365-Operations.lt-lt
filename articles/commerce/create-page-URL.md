---
title: Kurti puslapio URL
description: Šioje temoje aptariamos svetainės puslapio URL kūrimo pagrindinės koncepcijos ir procedūros.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 588cbedb077fab0663d3d62fc4a8b8ed915635b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414304"
---
# <a name="create-a-page-url"></a><span data-ttu-id="a2111-103">Kurti puslapio URL</span><span class="sxs-lookup"><span data-stu-id="a2111-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a2111-104">Šioje temoje aptariamos svetainės puslapio URL kūrimo pagrindinės koncepcijos ir procedūros.</span><span class="sxs-lookup"><span data-stu-id="a2111-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="a2111-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="a2111-105">Overview</span></span>

<span data-ttu-id="a2111-106">Visą arba absoliutųjį URL, kuris nurodo į jūsų svetainės puslapį, sudaro atskiros dalys.</span><span class="sxs-lookup"><span data-stu-id="a2111-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="a2111-107">Pavyzdžiui, URL `https://www.contoso.com/en-us/contactus` sudaro tolesnės dalys.</span><span class="sxs-lookup"><span data-stu-id="a2111-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="a2111-108">`https://www.contoso.com` – HTTP protokolas ir svetainės domenas.</span><span class="sxs-lookup"><span data-stu-id="a2111-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="a2111-109">`/en-us` – svetainės kalbos kelias.</span><span class="sxs-lookup"><span data-stu-id="a2111-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="a2111-110">`/contactus` – santykinis puslapio **Susisiekite su mumis** URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="a2111-111">Santykinis URL taip pat vadinamas *kintamaisiais URL duomenimis*.</span><span class="sxs-lookup"><span data-stu-id="a2111-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="a2111-112">Svetainės domeną ir pasirenkamą kalbos kelią nustatote nustatydami svetainę.</span><span class="sxs-lookup"><span data-stu-id="a2111-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="a2111-113">Daugiau domenų ir kalbos kelių į svetainę galite įtraukti svetainės parametrų dalyje esančiame internetinių parduotuvių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a2111-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="a2111-114">Kintamieji puslapio URL duomenys egzistuoja kaip atskiras objektas svetainės kūrimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="a2111-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="a2111-115">Puslapio URL sudaro dvi dalys: pavadinimas, nurodantis kintamuosius URL duomenis, ir puslapio, esančio jūsų arba išorinėje svetainėje, žymeklis.</span><span class="sxs-lookup"><span data-stu-id="a2111-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="a2111-116">Puslapio URL taip pat galima sukonfigūruoti taip, kad jis peradresauotų į kitą puslapį, esantį jūsų arba išorinėje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="a2111-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="a2111-117">Kurti puslapio URL</span><span class="sxs-lookup"><span data-stu-id="a2111-117">Create a page URL</span></span>

<span data-ttu-id="a2111-118">Toliau nurodyti du puslapių URL adresų kūrimo būdai.</span><span class="sxs-lookup"><span data-stu-id="a2111-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="a2111-119">Automatiškai, kai kuriate puslapį</span><span class="sxs-lookup"><span data-stu-id="a2111-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="a2111-120">Neautomatiškai, puslapyje **URL adresai**</span><span class="sxs-lookup"><span data-stu-id="a2111-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="a2111-121">Puslapio URL kūrimas kuriant puslapį</span><span class="sxs-lookup"><span data-stu-id="a2111-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="a2111-122">Jei kurdami naują puslapį lauke **URL** nurodote pavadinimą, puslapyje **URL adresai** automatiškai sukuriamas puslapio URL, nurodantis į tą puslapį.</span><span class="sxs-lookup"><span data-stu-id="a2111-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="a2111-123">Publikavus URL ir puslapį, į kurį jis nurodo, svetainės vartotojai (jūsų klientai) gali pasiekti puslapį, susietą su URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="a2111-124">Jei publikuojate URL nepublikuodami puslapio, į kurį jis nurodo, bandydami pasiekti puslapį svetainės vartotojai mato klaidą 404.</span><span class="sxs-lookup"><span data-stu-id="a2111-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="a2111-125">Jei publikuojate puslapį nepublikuodami URL, kuris į jį nurodo, naudojant URL puslapio pasiekti negalima.</span><span class="sxs-lookup"><span data-stu-id="a2111-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="a2111-126">Neautomatinis puslapio URL kūrimas</span><span class="sxs-lookup"><span data-stu-id="a2111-126">Manually create a page URL</span></span>

<span data-ttu-id="a2111-127">Kuriant naujus puslapius, nurodyti puslapio URL nereikia.</span><span class="sxs-lookup"><span data-stu-id="a2111-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="a2111-128">Jei URL lauką paliekate tuščią, puslapis sukuriamas nesusietos būsenos.</span><span class="sxs-lookup"><span data-stu-id="a2111-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="a2111-129">Šiuo atveju klientai puslapio negalės pasiekti, net jei jis publikuojamas.</span><span class="sxs-lookup"><span data-stu-id="a2111-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="a2111-130">Norėdami, kad puslapis būtų pasiekiamas, turite patys sukurti URL ir jį susieti su puslapiu.</span><span class="sxs-lookup"><span data-stu-id="a2111-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="a2111-131">Norėdami patys sukurti puslapio URL, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a2111-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="a2111-132">Puslapyje **URL adresai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a2111-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="a2111-133">Pasirinkite svetainės puslapį, kurį norite susieti su URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="a2111-134">Įveskite kintamuosius URL duomenis ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a2111-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="a2111-135">Šiuo metu URL yra juodraščio būsenos.</span><span class="sxs-lookup"><span data-stu-id="a2111-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="a2111-136">Kad svetainės vartotojai galėtų pasiekti susietą puslapį, jį reikia publikuoti.</span><span class="sxs-lookup"><span data-stu-id="a2111-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="a2111-137">Puslapio URL atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="a2111-137">Update a page URL</span></span>

<span data-ttu-id="a2111-138">Norėdami atnaujinti puslapio URL paskirties puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a2111-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="a2111-139">Puslapyje **URL adresai** pasirinkite atnaujintiną URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="a2111-140">Dešinėje esančioje ypatybių srityje pasirinkite prie paskirties puslapio esantį daugtaškio mygtuką (**...**).</span><span class="sxs-lookup"><span data-stu-id="a2111-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="a2111-141">Dialogo lange pasirinkite kitą puslapį, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a2111-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="a2111-142">URL įrašykite ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="a2111-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="a2111-143">Puslapio URL peradresavimas</span><span class="sxs-lookup"><span data-stu-id="a2111-143">Redirect a page URL</span></span>

<span data-ttu-id="a2111-144">Kartais galite norėti, kad, pageidavę konkretaus URL, jūsų klientai peržiūrėtų kitą puslapį.</span><span class="sxs-lookup"><span data-stu-id="a2111-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="a2111-145">Tokiais atvejais dažnai geriausia ir paprasčiausia yra pakeisti puslapį, į kurį nurodo puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="a2111-146">Tačiau galbūt naudodami HTTP 301 arba 3023 peradresavimą URL užklausas į kitą URL peradresuojate dėl pagrįstų priežasčių.</span><span class="sxs-lookup"><span data-stu-id="a2111-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="a2111-147">Norėdami URL peradresuoti į kitą URL, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a2111-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="a2111-148">Puslapyje **URL adresai** pasirinkite atnaujintiną URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="a2111-149">Dešinėje esančioje ypatybių srityje pasirinkite **Peradresuoti**.</span><span class="sxs-lookup"><span data-stu-id="a2111-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="a2111-150">Pasirinkite peradresavimo paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="a2111-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="a2111-151">Norėdami nurodyti į kitą svetainės puslapį, pasirinkite **Vidinis URL**, daugtaškio mygtuką (**...**) ir URL, į kurį norite peradresuoti.</span><span class="sxs-lookup"><span data-stu-id="a2111-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="a2111-152">Norėdami nukreipti į puslapį išorinėje svetainėje, pasirinkite **Išorinis URL** ir įveskite visą to puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="a2111-153">Būtinai įtraukite protokolą.</span><span class="sxs-lookup"><span data-stu-id="a2111-153">Be sure to include the protocol.</span></span> <span data-ttu-id="a2111-154">Pavyzdžiui, įveskite `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="a2111-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="a2111-155">Jei URL jau peradresuoja į vidinį URL, įvesti išorinį URL galėsite tik pasirinkę **Valyti pasirinkimą**.</span><span class="sxs-lookup"><span data-stu-id="a2111-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="a2111-156">Pasirinkite vieną iš tolesnių peradresavimo tipų.</span><span class="sxs-lookup"><span data-stu-id="a2111-156">Select a redirect type:</span></span>

    - <span data-ttu-id="a2111-157">**Peradresavimas visam laikui (301)** – pasirinkite šią parinktį, kai žinote, kad turinys perkeliamas visam laikui ir nebus grąžintas į ankstesnį URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="a2111-158">Ieškos moduliai peradresuojančio URL ieškos modulio optimizavimo (SEO) reikšmę priskirs peradresuojamam URL ir atnaujins savo įrašą, kad būtų rodomas naujasis URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="a2111-159">**Laikinas peradresavimas (302)** – pasirinkite šią parinktį, norėdami peradresuoti eismą neatnaujindami ieškos modulių.</span><span class="sxs-lookup"><span data-stu-id="a2111-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="a2111-160">Šis metodas paprastai naudojamas, jei turinys greitai grįš į ankstesnį URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="a2111-161">Kai būsite pasirengę vykdyti peradresavimą, įrašykite ir publikuokite URL.</span><span class="sxs-lookup"><span data-stu-id="a2111-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2111-162">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a2111-162">Additional resources</span></span>

[<span data-ttu-id="a2111-163">Svetainės naršymo tinkinimas</span><span class="sxs-lookup"><span data-stu-id="a2111-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="a2111-164">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="a2111-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="a2111-165">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a2111-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a2111-166">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="a2111-166">Add languages to your site</span></span>](add-languages-to-site.md)
