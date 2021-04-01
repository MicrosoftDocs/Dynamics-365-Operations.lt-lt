---
title: Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija
description: Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e035c767474cba19c3a31eafdefb08b422b564ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209208"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="2dbd5-103">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="2dbd5-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2dbd5-104">Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="2dbd5-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="2dbd5-105">Overview</span></span>

<span data-ttu-id="2dbd5-106">Žiniatinklio analizė yra esminė priemonė, kai norima suprasti, kaip klientai elgiasi jūsų svetainėje, ir priimti sprendimus, kurie padės optimizuoti maksimalaus konvertavimo tikslą.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="2dbd5-107">Šiems tikslams pasiekti yra daug žiniatinklio analizės paketų, pvz., „Google Analytics“, „Clicky“, „Moz Analytics“ ir „KISSMetrics“.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="2dbd5-108">Didžiajai daliai tinklo analitikos paketų turėsite įtraukti kliento pusės scenarijaus kodą  **\<head\>** HTML elemente visiems jūsų svetainės puslapiams.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="2dbd5-109">Šioje temoje pateiktos instrukcijos taikomos ir kitoms pasirinktinėms kliento funkcijoms, kurių „Microsoft Dynamics 365 Commerce“ pati nesiūlo.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="2dbd5-110">Pakartotinai galimo naudoti fragmento sukūrimas scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="2dbd5-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="2dbd5-111">Fragmentas leidžia jums pakartotinai naudoti įdėtojo ar išorinio scenarijaus kodą visuose jūsų svetainės puslapiuose, neatsižvelgiant į jų naudojamą šabloną.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="2dbd5-112">Pakartotinai galimo naudoti fragmento sukūrimas įdėtojo scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="2dbd5-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="2dbd5-113">Norėdami svetainių daryklėje sukurti pakartotinai galimą naudoti fragmentą įdėtojo scenarijaus kodui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2dbd5-114">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2dbd5-115">Dialogo lange **Naujas fragmentas** pasirinkite **Linijinis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2dbd5-116">Dalyje **Fragmento pavadinimas** įveskite fragmento pavadinimą ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2dbd5-117">Sukurto fragmento dalyje pasirinkite modulį **Numatytasis įdėtasis scenarijaus**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="2dbd5-118">Dešinėje esančios ypatybių srities dalyje **Įdėtasis scenarijus** įveskite kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2dbd5-119">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2dbd5-120">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2dbd5-121">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="2dbd5-122">Pakartotinai galimo naudoti fragmento sukūrimas išorinio scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="2dbd5-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="2dbd5-123">Norėdami svetainių daryklėje sukurti pakartotinai galimą naudoti fragmentą išorinio scenarijaus kodui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2dbd5-124">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2dbd5-125">Dialogo lange **Naujas fragmentas** pasirinkite **Išorinis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2dbd5-126">Dalyje **Fragmento pavadinimas** įveskite fragmento pavadinimą ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2dbd5-127">Sukurto fragmento dalyje pasirinkite modulį **Numatytasis išorinis scenarijaus**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="2dbd5-128">Dešinėje esančios ypatybių srities dalyje **Scenarijaus šaltinis** pridėkite išorinį arba santykinį išorinio scenarijaus šaltinio URL.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2dbd5-129">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2dbd5-130">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2dbd5-131">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="2dbd5-132">Jei jūsų svetainei įjungta turinio saugos strategija (CSP), įsitikinkite, kad visi išoriniai URL įtraukti į CSP direktyvą **script-src** „Commerce” svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="2dbd5-133">- Norėdami gauti daugiau informacijos, žr. [turinio saugumo politikos valdymas (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="2dbd5-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="2dbd5-134">Fragmento, kuriame yra scenarijaus kodas, įtraukimas į šabloną</span><span class="sxs-lookup"><span data-stu-id="2dbd5-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="2dbd5-135">Norėdami svetainių daryklėje į šabloną įtraukti fragmentą, kuriame yra scenarijaus kodas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2dbd5-136">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2dbd5-137">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2dbd5-138">Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="2dbd5-139">Pasirinkite fragmentą, kurį sukūrėte savo scenarijaus kodui.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="2dbd5-140">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2dbd5-141">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="2dbd5-142">Išorinio scenarijaus arba įdėtojo scenarijaus įtraukimas tiesiai į šabloną</span><span class="sxs-lookup"><span data-stu-id="2dbd5-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="2dbd5-143">Jeigu norite įterpti įdėtąjį arba išorinį scenarijų tiesiai į vieno šablono valdomų puslapių rinkinį, jums nereikia iš pradžių kurti fragmento.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="2dbd5-144">Įdėtojo scenarijaus įtraukimas tiesiai į šabloną</span><span class="sxs-lookup"><span data-stu-id="2dbd5-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="2dbd5-145">Norėdami svetainių daryklėje įtraukti įdėtąjį scenarijų tiesiai į šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2dbd5-146">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2dbd5-147">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2dbd5-148">Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2dbd5-149">Dialogo lange **Įtraukti modulį** pasirinkite **Įdėtasis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2dbd5-150">Dešinėje esančios ypatybių srities dalyje **Įdėtasis scenarijus** įveskite kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2dbd5-151">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2dbd5-152">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2dbd5-153">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="2dbd5-154">Išorinio scenarijaus įtraukimas tiesiai į šabloną</span><span class="sxs-lookup"><span data-stu-id="2dbd5-154">Add an external script directly to a template</span></span>

<span data-ttu-id="2dbd5-155">Norėdami svetainių daryklėje įtraukti išorinį scenarijų tiesiai į šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2dbd5-156">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2dbd5-157">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2dbd5-158">Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2dbd5-159">Dialogo lange **Įtraukti modulį** pasirinkite **Išorinis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2dbd5-160">Dešinėje esančios ypatybių srities dalyje **Scenarijaus šaltinis** pridėkite išorinį arba santykinį išorinio scenarijaus šaltinio URL.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2dbd5-161">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2dbd5-162">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2dbd5-163">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dbd5-164">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2dbd5-164">Additional resources</span></span>

[<span data-ttu-id="2dbd5-165">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="2dbd5-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2dbd5-166">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="2dbd5-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2dbd5-167">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="2dbd5-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2dbd5-168">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="2dbd5-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2dbd5-169">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="2dbd5-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2dbd5-170">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="2dbd5-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2dbd5-171">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="2dbd5-171">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]