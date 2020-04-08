---
title: Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija
description: Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154091"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="b2f3f-103">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="b2f3f-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2f3f-104">Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="b2f3f-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="b2f3f-105">Overview</span></span>

<span data-ttu-id="b2f3f-106">Žiniatinklio analizė yra esminė priemonė, kai norima suprasti, kaip klientai elgiasi jūsų svetainėje, ir priimti sprendimus, kurie padės optimizuoti maksimalaus konvertavimo tikslą.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="b2f3f-107">Šiems tikslams pasiekti yra daug žiniatinklio analizės paketų, pvz., „Google Analytics“, „Clicky“, „Moz Analytics“ ir „KISSMetrics“.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="b2f3f-108">Naudojant daugumą žiniatinklio analizės paketų reikalaujama, kad visuose svetainės puslapiuose į HTML elementą **\<head\>** įtrauktumėte kliento scenarijaus kodą.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="b2f3f-109">Šioje temoje pateiktos instrukcijos taikomos ir kitoms pasirinktinėms kliento funkcijoms, kurių „Microsoft Dynamics 365 Commerce“ pati nesiūlo.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="b2f3f-110">Pakartotinai galimo naudoti puslapio fragmento sukūrimas scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="b2f3f-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="b2f3f-111">Puslapio fragmentas leidžia jums pakartotinai naudoti įdėtojo ar išorinio scenarijaus kodą visuose jūsų svetainės puslapiuose, neatsižvelgiant į jų naudojamą šabloną.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="b2f3f-112">Pakartotinai galimo naudoti puslapio fragmento sukūrimas įdėtojo scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="b2f3f-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="b2f3f-113">Norėdami svetainių daryklėje sukurti pakartotinai galimą naudoti puslapio fragmentą įdėtojo scenarijaus kodui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2f3f-114">Nueikite į **Puslapio fragmentai** ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="b2f3f-115">Dialogo lange **Naujas puslapio fragmentas** pasirinkite **Įdėtasis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="b2f3f-116">Dalyje **Puslapio fragmento pavadinimas** įveskite fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b2f3f-117">Sukurto puslapio fragmento dalyje pasirinkite modulį **Numatytasis įdėtasis scenarijaus**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="b2f3f-118">Dešinėje esančios ypatybių srities dalyje **Įdėtasis scenarijus** įveskite kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="b2f3f-119">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2f3f-120">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2f3f-121">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="b2f3f-122">Pakartotinai galimo naudoti puslapio fragmento sukūrimas išorinio scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="b2f3f-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="b2f3f-123">Norėdami svetainių daryklėje sukurti pakartotinai galimą naudoti puslapio fragmentą išorinio scenarijaus kodui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2f3f-124">Nueikite į **Puslapio fragmentai** ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="b2f3f-125">Dialogo lange **Naujas puslapio fragmentas** pasirinkite **Išorinis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="b2f3f-126">Dalyje **Puslapio fragmento pavadinimas** įveskite fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b2f3f-127">Sukurto puslapio fragmento dalyje pasirinkite modulį **Numatytasis išorinis scenarijaus**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="b2f3f-128">Dešinėje esančios ypatybių srities dalyje **Scenarijaus šaltinis** pridėkite išorinį arba santykinį išorinio scenarijaus šaltinio URL.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="b2f3f-129">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2f3f-130">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2f3f-131">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="b2f3f-132">Puslapio fragmento, kuriame yra scenarijaus kodas, įtraukimas į šabloną</span><span class="sxs-lookup"><span data-stu-id="b2f3f-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="b2f3f-133">Norėdami svetainių daryklėje į šabloną įtraukti puslapio fragmentą, kuriame yra scenarijaus kodas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2f3f-134">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b2f3f-135">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b2f3f-136">Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti puslapio fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="b2f3f-137">Pasirinkite fragmentą, kurį sukūrėte savo scenarijaus kodui.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="b2f3f-138">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2f3f-139">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="b2f3f-140">Išorinio scenarijaus arba įdėtojo scenarijaus įtraukimas tiesiai į šabloną</span><span class="sxs-lookup"><span data-stu-id="b2f3f-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="b2f3f-141">Jeigu norite įterpti įdėtąjį arba išorinį scenarijų tiesiai į vieno šablono valdomų puslapių rinkinį, jums nereikia iš pradžių kurti puslapio fragmento.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="b2f3f-142">Įdėtojo scenarijaus įtraukimas tiesiai į šabloną</span><span class="sxs-lookup"><span data-stu-id="b2f3f-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="b2f3f-143">Norėdami svetainių daryklėje įtraukti įdėtąjį scenarijų tiesiai į šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2f3f-144">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b2f3f-145">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b2f3f-146">Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b2f3f-147">Dialogo lange **Įtraukti modulį** pasirinkite **Įdėtasis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="b2f3f-148">Dešinėje esančios ypatybių srities dalyje **Įdėtasis scenarijus** įveskite kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="b2f3f-149">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2f3f-150">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2f3f-151">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="b2f3f-152">Išorinio scenarijaus įtraukimas tiesiai į šabloną</span><span class="sxs-lookup"><span data-stu-id="b2f3f-152">Add an external script directly to a template</span></span>

<span data-ttu-id="b2f3f-153">Norėdami svetainių daryklėje įtraukti išorinį scenarijų tiesiai į šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2f3f-154">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b2f3f-155">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b2f3f-156">Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b2f3f-157">Dialogo lange **Įtraukti modulį** pasirinkite **Išorinis scenarijus**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="b2f3f-158">Dešinėje esančios ypatybių srities dalyje **Scenarijaus šaltinis** pridėkite išorinį arba santykinį išorinio scenarijaus šaltinio URL.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="b2f3f-159">Tada konfigūruokite kitas parinktis, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2f3f-160">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2f3f-161">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="b2f3f-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2f3f-162">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b2f3f-162">Additional resources</span></span>

[<span data-ttu-id="b2f3f-163">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="b2f3f-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b2f3f-164">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="b2f3f-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b2f3f-165">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="b2f3f-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b2f3f-166">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="b2f3f-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b2f3f-167">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="b2f3f-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b2f3f-168">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="b2f3f-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b2f3f-169">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="b2f3f-169">Add languages to your site</span></span>](add-languages-to-site.md)
