---
title: Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija
description: Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: a5f82426d87cd2e0faa0195a841899bb03f9df08
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697341"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="5f311-103">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="5f311-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5f311-104">Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="5f311-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="5f311-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="5f311-105">Overview</span></span>

<span data-ttu-id="5f311-106">Žiniatinklio analizė yra esminė priemonė, kai norima suprasti, kaip klientai elgiasi jūsų svetainėje, ir priimti sprendimus, kurie padės optimizuoti maksimalaus konvertavimo tikslą.</span><span class="sxs-lookup"><span data-stu-id="5f311-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="5f311-107">Šiems tikslams pasiekti yra daug žiniatinklio analizės paketų, pvz., „Google Analytics“, „Clicky“, „Moz Analytics“ ir „KISSMetrics“.</span><span class="sxs-lookup"><span data-stu-id="5f311-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="5f311-108">Naudojant daugumą žiniatinklio analizės paketų reikalaujama, kad visuose svetainės puslapiuose į HTML elementą **\<head\>** įtrauktumėte kliento scenarijaus kodą.</span><span class="sxs-lookup"><span data-stu-id="5f311-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="5f311-109">Šioje temoje pateiktos instrukcijos taikomos ir kitoms pasirinktinėms kliento funkcijoms, kurių „Microsoft Dynamics 365 Commerce“ pati nesiūlo.</span><span class="sxs-lookup"><span data-stu-id="5f311-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="5f311-110">Pakartotinai galimo naudoti fragmento sukūrimas scenarijaus kodui</span><span class="sxs-lookup"><span data-stu-id="5f311-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="5f311-111">Sukūrus scenarijaus kodo fragmentą, jį galima pakartotinai naudoti visuose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="5f311-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="5f311-112">Nueikite į **Fragmentai \> Naujas puslapio fragmentas**.</span><span class="sxs-lookup"><span data-stu-id="5f311-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="5f311-113">Pasirinkite **Išorinis scenarijus**, įveskite fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5f311-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="5f311-114">Fragmentų hierarchijoje pasirinkite ką tik sukurto fragmento antrinį modulį **scenarijaus injektorius**.</span><span class="sxs-lookup"><span data-stu-id="5f311-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="5f311-115">Dešinėje esančioje ypatybių srityje įtraukite kliento scenarijų ir pagal poreikį nustatykite kitas konfigūracijos parinktis.</span><span class="sxs-lookup"><span data-stu-id="5f311-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="5f311-116">Fragmento įtraukimas į šablonus</span><span class="sxs-lookup"><span data-stu-id="5f311-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="5f311-117">Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.</span><span class="sxs-lookup"><span data-stu-id="5f311-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="5f311-118">Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.</span><span class="sxs-lookup"><span data-stu-id="5f311-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="5f311-119">Pasirinkite prie vietos **HTML antraštė** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="5f311-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="5f311-120">Pasirinkite fragmentą, kurį sukūrėte savo scenarijaus kodui.</span><span class="sxs-lookup"><span data-stu-id="5f311-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="5f311-121">Šabloną įrašykite ir atrakinkite.</span><span class="sxs-lookup"><span data-stu-id="5f311-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="5f311-122">Baigę turite publikuoti fragmentą ir pagrindinį šabloną.</span><span class="sxs-lookup"><span data-stu-id="5f311-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="5f311-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5f311-123">Additional resources</span></span>

[<span data-ttu-id="5f311-124">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="5f311-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5f311-125">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="5f311-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5f311-126">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="5f311-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5f311-127">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="5f311-127">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5f311-128">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="5f311-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5f311-129">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="5f311-129">Add languages to your site</span></span>](add-languages-to-site.md)

