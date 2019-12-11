---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb757672fffb56892837c066d552773908dd1ec1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696973"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="b3683-103">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="b3683-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b3683-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).</span><span class="sxs-lookup"><span data-stu-id="b3683-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="b3683-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="b3683-105">Overview</span></span>

<span data-ttu-id="b3683-106">Programoje „Dynamics 365 Commerce“ nustatydami el. prekybos aplinką, galite sukonfigūruoti, kad ji veiktų su CDN tarnyba.</span><span class="sxs-lookup"><span data-stu-id="b3683-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="b3683-107">Jūsų pasirinktinį domeną galima įjungti konfigūruojant el. prekybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="b3683-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="b3683-108">Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas.</span><span class="sxs-lookup"><span data-stu-id="b3683-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="b3683-109">Konfigūruojant el. prekybos aplinką sugeneruojamas su aplinka susietas pagrindinio kompiuterio vardas.</span><span class="sxs-lookup"><span data-stu-id="b3683-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="b3683-110">Toliau nurodytas šio pagrindinio kompiuterio vardo formatas, kuriame *el. prekybos-nuomotojo-vardas* yra jūsų aplinkos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="b3683-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="b3683-111">&lt;el.prekybos-numotojo-vardas&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="b3683-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="b3683-112">Pagrindinio kompiuterio vardas arba galinis punktas, sugeneruotas konfigūruojant, palaiko tik \*.commerce.dynamics.com saugiųjų jungčių lygmens (SSL) sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="b3683-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="b3683-113">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="b3683-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="b3683-114">Todėl turite nutraukti pasirinktinių savo CDN domenų SSL, o srautą iš CDN persiųsti pagrindinio kompiuterio vardui arba galiniam punktui, kurį sugeneravo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="b3683-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="b3683-115">Be to, „Commerce“ *statika* („JavaScript“ arba pakopinių stilių sąrašo \[CSS\] failai) teikiama iš galinio punkto, kurį sugeneravo „Commerce“ (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="b3683-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="b3683-116">Statiką kaupti talpykloje galima, tik jei „Commerce“ sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas įdedamas už CDN.</span><span class="sxs-lookup"><span data-stu-id="b3683-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="b3683-117">SSL nustatymas</span><span class="sxs-lookup"><span data-stu-id="b3683-117">Set up SSL</span></span>

<span data-ttu-id="b3683-118">Norėdami padėti užtikrinti, kad būtų nustatytas SSL ir talpykloje kaupiama statika, turite sukonfigūruoti, kad jūsų CDN būtų susietas su pagrindinio kompiuterio vardu, kurį „Commerce“ sugeneravo jūsų aplinkai.</span><span class="sxs-lookup"><span data-stu-id="b3683-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="b3683-119">Taip pat turite talpykloje kaupti tik tolesnį statikos šabloną.</span><span class="sxs-lookup"><span data-stu-id="b3683-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="b3683-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="b3683-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="b3683-121">Sukonfigūravę savo „Commerce“ aplinką naudodami suteiktą pasirinktinį domeną arba pateikę pasirinktinį aplinkos domeną naudodami aptarnavimo užklausą, pasirinktinį domeną nukreipkite į „Commerce“ sugeneruotą pagrindinio kompiuterio vardą arba galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="b3683-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="b3683-122">Kaip buvo minėta anksčiau, sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas palaiko tik \*.commerce.dynamics.com SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="b3683-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="b3683-123">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="b3683-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="b3683-124">CDN tarnybos</span><span class="sxs-lookup"><span data-stu-id="b3683-124">CDN services</span></span>

<span data-ttu-id="b3683-125">Su „Commerce“ aplinka galima naudoti bet kurią CDN tarnybą.</span><span class="sxs-lookup"><span data-stu-id="b3683-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="b3683-126">Toliau pateikti du pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="b3683-126">Here are two examples:</span></span>

- <span data-ttu-id="b3683-127">**„Microsoft Azure Front Door Service“** – „Azure“ CDN sprendimas.</span><span class="sxs-lookup"><span data-stu-id="b3683-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="b3683-128">Norėdami apie „Azure Front Door Service“ gauti daugiau informacijos, žr. [„Azure Front Door Service“ dokumentaciją](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="b3683-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="b3683-129">**„Akamai Dynamic Site Accelerator“** – norėdami gauti daugiau informacijos, žr. [„Dynamic Site Accelerator“](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="b3683-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="b3683-130">CDN sąranka</span><span class="sxs-lookup"><span data-stu-id="b3683-130">CDN setup</span></span>

<span data-ttu-id="b3683-131">CDN sąrankos procesą sudaro tolesni bendrieji veiksmai.</span><span class="sxs-lookup"><span data-stu-id="b3683-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="b3683-132">Įtraukite sąsajos serverio pagrindinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="b3683-132">Add a front-end host.</span></span>
1. <span data-ttu-id="b3683-133">Sukonfigūruokite vidinio serverio telkinį.</span><span class="sxs-lookup"><span data-stu-id="b3683-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="b3683-134">Nustatykite maršruto parinkimo ir kaupimo talpykloje taisykles.</span><span class="sxs-lookup"><span data-stu-id="b3683-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="b3683-135">Sąsajos serverio pagrindinio kompiuterio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="b3683-135">Add a front-end host</span></span>

<span data-ttu-id="b3683-136">Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“.</span><span class="sxs-lookup"><span data-stu-id="b3683-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="b3683-137">Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="b3683-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="b3683-138">Vidinio serverio telkinio sukonfigūravimas sprendime „Azure Front Door Service“</span><span class="sxs-lookup"><span data-stu-id="b3683-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="b3683-139">Norėdami sprendime „Azure Front Door Service“ sukonfigūruoti vidinio serverio telkinį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b3683-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="b3683-140">Į vidinio serverio telkinį įtraukite **&lt;el.prek-nuomotojo-vardas&gt;.commerce.dynamics.com** kaip pasirinktinį pagrindinį kompiuterį su tuščia vidinio serverio pagrindinio kompiuterio antrašte.</span><span class="sxs-lookup"><span data-stu-id="b3683-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="b3683-141">Dalies **Būklės patikros** lauke **Kelias** įveskite **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="b3683-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="b3683-142">Lauke **Intervalas (sekundės)** įveskite **255**.</span><span class="sxs-lookup"><span data-stu-id="b3683-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="b3683-143">Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b3683-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="b3683-144">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Vidinio serverio telkinio įtraukimas**.</span><span class="sxs-lookup"><span data-stu-id="b3683-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Vidinio serverio telkinio įtraukimas](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="b3683-146">„Azure Front Door Service“ taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="b3683-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="b3683-147">Norėdami sprendime „Azure Front Door Service“ nustatyti maršruto parinkimo taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b3683-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="b3683-148">Įtraukite maršruto parinkimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="b3683-148">Add a routing rule.</span></span>
1. <span data-ttu-id="b3683-149">Lauke **Pavadinimas** įveskite **numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="b3683-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="b3683-150">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="b3683-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="b3683-151">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="b3683-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="b3683-152">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\***.</span><span class="sxs-lookup"><span data-stu-id="b3683-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="b3683-153">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b3683-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="b3683-154">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="b3683-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="b3683-155">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="b3683-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="b3683-156">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="b3683-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="b3683-157">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="b3683-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="b3683-158">Norėdami sprendime „Azure Front Door Service“ nustatyti kaupimo talpykloje taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b3683-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="b3683-159">Įtraukite kaupimo talpykloje taisyklę.</span><span class="sxs-lookup"><span data-stu-id="b3683-159">Add a caching rule.</span></span>
1. <span data-ttu-id="b3683-160">Lauke **Pavadinimas** įveskite **statika**.</span><span class="sxs-lookup"><span data-stu-id="b3683-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="b3683-161">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="b3683-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="b3683-162">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="b3683-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="b3683-163">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="b3683-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="b3683-164">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="b3683-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="b3683-165">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="b3683-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="b3683-166">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="b3683-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="b3683-167">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="b3683-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="b3683-168">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="b3683-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="b3683-169">Lauke **Užklausos eilučių kaupimo talpykloje būdas** pasirinkite **Talpykloje kaupti kiekvieną unikalų URL**.</span><span class="sxs-lookup"><span data-stu-id="b3683-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="b3683-170">Laukų grupėje **Dinaminis glaudinimas** pasirinkite parinktį **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="b3683-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="b3683-171">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Taisyklės įtraukimas**.</span><span class="sxs-lookup"><span data-stu-id="b3683-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Taisyklės įtraukimas](./media/CDN_CachingRule.png)

<span data-ttu-id="b3683-173">Įdiegę šią pradinę konfigūraciją, į „Azure Front Door Service“ konfigūraciją turite įtraukti savo pasirinktinį domeną.</span><span class="sxs-lookup"><span data-stu-id="b3683-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="b3683-174">Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).</span><span class="sxs-lookup"><span data-stu-id="b3683-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="b3683-175">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="b3683-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas CNAME konfigūravimas](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="b3683-177">Jei jūsų naudosimas domenas jau aktyvus ir paleistas, kreipkitės į palaikymo tarnybą, kad šį domeną būtų galima naudoti su „Azure Front Door Service“ ir nustatyti testą.</span><span class="sxs-lookup"><span data-stu-id="b3683-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="b3683-178">Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="b3683-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="b3683-179">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="b3683-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Pasirinktinio domeno HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="b3683-181">Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.</span><span class="sxs-lookup"><span data-stu-id="b3683-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3683-182">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b3683-182">Additional resources</span></span>

[<span data-ttu-id="b3683-183">Interneto parduotuvės peržiūra</span><span class="sxs-lookup"><span data-stu-id="b3683-183">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="b3683-184">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="b3683-184">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b3683-185">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="b3683-185">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b3683-186">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="b3683-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b3683-187">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b3683-187">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b3683-188">Įgalinti parduotuvės nustatymą pagal vietą</span><span class="sxs-lookup"><span data-stu-id="b3683-188">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="b3683-189">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="b3683-189">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
