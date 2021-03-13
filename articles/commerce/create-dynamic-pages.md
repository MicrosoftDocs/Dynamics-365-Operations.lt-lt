---
title: Sukurti dinaminius e-komercijos puslapius pagal URL parameterus
description: Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ e-komercijos puslapį, kuris gali pateikti dinaminį turinį pagal URL parametrus.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098639"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="7cd5e-103">Sukurti dinaminius e-komercijos puslapius pagal URL parameterus</span><span class="sxs-lookup"><span data-stu-id="7cd5e-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7cd5e-104">Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ e-komercijos puslapį, kuris gali pateikti dinaminį turinį pagal URL parametrus.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="7cd5e-105">El. komercijos puslapis gali būti konfigūruotas siekiant talpinti kitą turinį pagal segmentą URL kelyje.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="7cd5e-106">Dėl to, puslapis yra žinomas kaip dinaminis puslapis.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="7cd5e-107">Segmentas yra naudojamas kaip parametras siekiant gauti puslapio turinį.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="7cd5e-108">Pavyzdžiui, puslapis pavadinimu **tinklaraščio\_rodinys** yra sukuriamas ir susiejamas su URL `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="7cd5e-109">Šis puslapis tuomet gali būti naudojamas siekiant rodyti kitą turinį pagal paskutinį segmentą URL kelyje.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="7cd5e-110">Pavyzdžiui, paskutinis segmentas URL `https://fabrikam.com/blog/article-1` yra **straipsnis-1**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="7cd5e-111">Atskiri kliento puslpiai, viršijantys dinaminį puslapį, gali būti taip pat siejami su segmentais URL kelyje.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="7cd5e-112">Pavyzdžiui, puslapis pavadinimu **tinklaraščio\_santrauka** yra sukuriamas ir susiejamas su URL `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="7cd5e-113">Kai URL yra reikalaujamas, **tinklaraštis\_santrauka** puslapis yra susiejamas su **/apie-šį-blogą** parametru ir grąžinamas vietoje **tinklaraštis\_rodinys** puslapio.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="7cd5e-114">Talpinimo, gavimo ir rodymo dinaminio puslapio funkcijos turinys yra įgyvendinamas naudojant tinkintą modulį.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="7cd5e-115">Dėl daugiau informacijos, žr. [Interneto kanalo plėtinys](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="7cd5e-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="7cd5e-116">Nustatykite dinaminį el. komercijos puslapį</span><span class="sxs-lookup"><span data-stu-id="7cd5e-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="7cd5e-117">Norėdami nustatyti dinaminį el. komercijos puslapį, privalote sukurti dinaminį puslapį, pagrindinį URL ir konfigūruoti maršrutą į dinaminį puslapį.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="7cd5e-118">Kurkite puslapį, kuris bus naudojamas dinaminiam turiniui</span><span class="sxs-lookup"><span data-stu-id="7cd5e-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="7cd5e-119">Norėdami sukurti puslapį, kuris bus naudojamas dinaminiam turiniui, atlikite veiksmus [Įtraukti naują saito puslapį](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="7cd5e-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="7cd5e-120">Jūsų sukurtam puslapiui reikės modulio įgyvendinimo, kuris naudoja paskutinį URL kelio segmentą siekiant gauti turinį iš išorės duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="7cd5e-121">Dėl daugiau informacijos apie tinkinto modulio kūrimą, žr. [Interneto kanalo plėtinys](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="7cd5e-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="7cd5e-122">Kurkite pagrindinį URL dinaminiam puslapiui</span><span class="sxs-lookup"><span data-stu-id="7cd5e-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="7cd5e-123">Norėdami kurti pagrindinį URL dinaminiam puslapiui „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7cd5e-124">Eikite į **URL** ir rinkitės **Naujas \> Naujas URL**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="7cd5e-125">Teksto laukelyje **Kurti naują URL** rinkitės **Vidinis puslapis**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="7cd5e-126">Skyriuje **URL kelias**, įveskite kelią, kuris bus naudojamas kaip dinaminio puslapio šaknis (šiuo atveju, **/tinklaraštis**).</span><span class="sxs-lookup"><span data-stu-id="7cd5e-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="7cd5e-127">Tada rinkitės **Kitas**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-127">Then select **Next**.</span></span>
1. <span data-ttu-id="7cd5e-128">Teksto laukelyje **Rinktis puslapį** rinkitės laukelį, puslapį, kurį sukūrėte, kad jis palaikytų dinaminį puslapį ir tada **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="7cd5e-129">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="7cd5e-130">Konfigūruokite maršrutą dinaminiam puslapiui</span><span class="sxs-lookup"><span data-stu-id="7cd5e-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="7cd5e-131">Norėdami konfigūruoti maršrutą į dinaminį puslapį „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7cd5e-132">Eikite į **Saito nustatymai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="7cd5e-133">Skyriuje **Parametrų URL keliai**, rinkitės **Įtraukti** ir tuomet įveskite URL kelią, kurį įvedėte kai sukūrėte URL (šiuo atveju, **/tinklaraštis**).</span><span class="sxs-lookup"><span data-stu-id="7cd5e-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="7cd5e-134">Rinkitės **įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-134">Select **Save and publish**.</span></span>

<span data-ttu-id="7cd5e-135">Po to, kai maršrutas sukonfigūruotas, visos užklausos URL keliui su parametrais grąžins puslapį, kuris yra susietas su tuo URL.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="7cd5e-136">Jei bet kokios užklausos turi papildomą segmentą, susietas puslapis bus grąžinamas, o puslapio turinys bus gaunamas naudojant segmentą kaip parametrą.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="7cd5e-137">Pavyzdžiui, `https://fabrikam.com/blog/article-1` grąžins **tinklaraščio\_santraukos** puslapį, o puslapio turinys bus gautas naudojant **/straipsnio-1** parametrą.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="7cd5e-138">Viršys URL su parametru su tinkintu puslapiu</span><span class="sxs-lookup"><span data-stu-id="7cd5e-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="7cd5e-139">Norėdami viršyti URL su parametrais su tinkintu puslapiu „Commerce“ saito kūrimo įrankiu, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7cd5e-140">Eikite į **URL** ir rinkitės **Naujas \> Naujas URL**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="7cd5e-141">Teksto laukelyje **Kurti naują URL** rinkitės **Vidinis puslapis**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="7cd5e-142">Skyriuje **URL kelias**, įveskite kelią, kuris įtraukia segmentą viršijiamą (šiuo atveju, **/tinklaraštis/apie-šį-tinklaraštį**).</span><span class="sxs-lookup"><span data-stu-id="7cd5e-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="7cd5e-143">Tada rinkitės **Kitas**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-143">Then select **Next**.</span></span>
1. <span data-ttu-id="7cd5e-144">Teksto laukelyje **Rinktis puslapį** rinkitės tinkintą puslapį ir tada **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="7cd5e-145">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-145">Select **Publish**.</span></span>
1. <span data-ttu-id="7cd5e-146">Jei tinkintas puslapis dar nebuvo publikuotas, eikite į **Puslapiai**, rinkitės tinkintą puslapį ir tada **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="7cd5e-147">Po tinkinto puslapio publikavimo, jis gali būti naudojamas vietoje dinaminio puslapio, kuris turi turinį su parametrais.</span><span class="sxs-lookup"><span data-stu-id="7cd5e-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cd5e-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7cd5e-148">Additional resources</span></span>

[<span data-ttu-id="7cd5e-149">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="7cd5e-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="7cd5e-150">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="7cd5e-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="7cd5e-151">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="7cd5e-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="7cd5e-152">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="7cd5e-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="7cd5e-153">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="7cd5e-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="7cd5e-154">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="7cd5e-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="7cd5e-155">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="7cd5e-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="7cd5e-156">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="7cd5e-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="7cd5e-157">Interneto kanalo išplečiamumas</span><span class="sxs-lookup"><span data-stu-id="7cd5e-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
