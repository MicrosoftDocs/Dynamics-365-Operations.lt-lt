---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
manager: annbe
ms.date: 03/02/2020
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
ms.openlocfilehash: 23ac9d8844c2a8ae20bd316c40078319601a3a4d
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096730"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="7edbd-103">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7edbd-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).</span><span class="sxs-lookup"><span data-stu-id="7edbd-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="7edbd-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="7edbd-105">Overview</span></span>

<span data-ttu-id="7edbd-106">Programoje „Dynamics 365 Commerce“ nustatydami el. prekybos aplinką, galite sukonfigūruoti, kad ji veiktų su CDN tarnyba.</span><span class="sxs-lookup"><span data-stu-id="7edbd-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="7edbd-107">Jūsų pasirinktinį domeną galima įjungti konfigūruojant el. prekybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="7edbd-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="7edbd-108">Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas.</span><span class="sxs-lookup"><span data-stu-id="7edbd-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="7edbd-109">Konfigūruojant el. prekybos aplinką sugeneruojamas su aplinka susietas pagrindinio kompiuterio vardas.</span><span class="sxs-lookup"><span data-stu-id="7edbd-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="7edbd-110">Toliau nurodytas šio pagrindinio kompiuterio vardo formatas, kuriame *el. prekybos-nuomotojo-vardas* yra jūsų aplinkos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="7edbd-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="7edbd-111">&lt;el.prekybos-numotojo-vardas&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="7edbd-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="7edbd-112">Pagrindinio kompiuterio vardas arba galinis punktas, sugeneruotas konfigūruojant, palaiko tik \*.commerce.dynamics.com saugiųjų jungčių lygmens (SSL) sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="7edbd-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="7edbd-113">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="7edbd-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="7edbd-114">Todėl turite nutraukti pasirinktinių savo CDN domenų SSL, o srautą iš CDN persiųsti pagrindinio kompiuterio vardui arba galiniam punktui, kurį sugeneravo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="7edbd-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="7edbd-115">Be to, „Commerce“ *statika* („JavaScript“ arba pakopinių stilių sąrašo \[CSS\] failai) teikiama iš galinio punkto, kurį sugeneravo „Commerce“ (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="7edbd-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="7edbd-116">Statiką kaupti talpykloje galima, tik jei „Commerce“ sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas įdedamas už CDN.</span><span class="sxs-lookup"><span data-stu-id="7edbd-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="7edbd-117">SSL nustatymas</span><span class="sxs-lookup"><span data-stu-id="7edbd-117">Set up SSL</span></span>

<span data-ttu-id="7edbd-118">Norėdami padėti užtikrinti, kad būtų nustatytas SSL ir talpykloje kaupiama statika, turite sukonfigūruoti, kad jūsų CDN būtų susietas su pagrindinio kompiuterio vardu, kurį „Commerce“ sugeneravo jūsų aplinkai.</span><span class="sxs-lookup"><span data-stu-id="7edbd-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="7edbd-119">Taip pat turite talpykloje kaupti tik tolesnį statikos šabloną.</span><span class="sxs-lookup"><span data-stu-id="7edbd-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="7edbd-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="7edbd-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="7edbd-121">Sukonfigūravę savo „Commerce“ aplinką naudodami suteiktą pasirinktinį domeną arba pateikę pasirinktinį aplinkos domeną naudodami aptarnavimo užklausą, pasirinktinį domeną nukreipkite į „Commerce“ sugeneruotą pagrindinio kompiuterio vardą arba galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="7edbd-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="7edbd-122">Kaip buvo minėta anksčiau, sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas palaiko tik \*.commerce.dynamics.com SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="7edbd-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="7edbd-123">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="7edbd-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="7edbd-124">CDN tarnybos</span><span class="sxs-lookup"><span data-stu-id="7edbd-124">CDN services</span></span>

<span data-ttu-id="7edbd-125">Su „Commerce“ aplinka galima naudoti bet kurią CDN tarnybą.</span><span class="sxs-lookup"><span data-stu-id="7edbd-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="7edbd-126">Toliau pateikti du pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="7edbd-126">Here are two examples:</span></span>

- <span data-ttu-id="7edbd-127">**„Microsoft Azure Front Door Service“** – „Azure“ CDN sprendimas.</span><span class="sxs-lookup"><span data-stu-id="7edbd-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="7edbd-128">Norėdami apie „Azure Front Door Service“ gauti daugiau informacijos, žr. [„Azure Front Door Service“ dokumentaciją](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="7edbd-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="7edbd-129">**„Akamai Dynamic Site Accelerator“** – norėdami gauti daugiau informacijos, žr. [„Dynamic Site Accelerator“](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="7edbd-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="7edbd-130">CDN sąranka</span><span class="sxs-lookup"><span data-stu-id="7edbd-130">CDN setup</span></span>

<span data-ttu-id="7edbd-131">CDN sąrankos procesą sudaro tolesni bendrieji veiksmai.</span><span class="sxs-lookup"><span data-stu-id="7edbd-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="7edbd-132">Įtraukite sąsajos serverio pagrindinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="7edbd-132">Add a front-end host.</span></span>
1. <span data-ttu-id="7edbd-133">Sukonfigūruokite vidinio serverio telkinį.</span><span class="sxs-lookup"><span data-stu-id="7edbd-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="7edbd-134">Nustatykite maršruto parinkimo ir kaupimo talpykloje taisykles.</span><span class="sxs-lookup"><span data-stu-id="7edbd-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="7edbd-135">Sąsajos serverio pagrindinio kompiuterio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-135">Add a front-end host</span></span>

<span data-ttu-id="7edbd-136">Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“.</span><span class="sxs-lookup"><span data-stu-id="7edbd-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="7edbd-137">Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="7edbd-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="7edbd-138">Vidinio serverio telkinio sukonfigūravimas sprendime „Azure Front Door Service“</span><span class="sxs-lookup"><span data-stu-id="7edbd-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="7edbd-139">Norėdami sprendime „Azure Front Door Service“ sukonfigūruoti vidinio serverio telkinį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7edbd-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="7edbd-140">Į vidinio serverio telkinį įtraukite **&lt;el.prek-nuomotojo-vardas&gt;.commerce.dynamics.com** kaip pasirinktinį pagrindinį kompiuterį su tuščia vidinio serverio pagrindinio kompiuterio antrašte.</span><span class="sxs-lookup"><span data-stu-id="7edbd-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="7edbd-141">Dalies **Būklės patikros** lauke **Kelias** įveskite **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="7edbd-142">Lauke **Intervalas (sekundės)** įveskite **255**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="7edbd-143">Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7edbd-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="7edbd-144">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Vidinio serverio telkinio įtraukimas**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Vidinio serverio telkinio įtraukimas](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="7edbd-146">„Azure Front Door Service“ taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="7edbd-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="7edbd-147">Norėdami sprendime „Azure Front Door Service“ nustatyti maršruto parinkimo taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7edbd-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="7edbd-148">Įtraukite maršruto parinkimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7edbd-148">Add a routing rule.</span></span>
1. <span data-ttu-id="7edbd-149">Lauke **Pavadinimas** įveskite **numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="7edbd-150">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="7edbd-151">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="7edbd-152">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\***.</span><span class="sxs-lookup"><span data-stu-id="7edbd-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="7edbd-153">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="7edbd-154">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="7edbd-155">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="7edbd-156">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="7edbd-157">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="7edbd-158">Norėdami sprendime „Azure Front Door Service“ nustatyti kaupimo talpykloje taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7edbd-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="7edbd-159">Įtraukite kaupimo talpykloje taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7edbd-159">Add a caching rule.</span></span>
1. <span data-ttu-id="7edbd-160">Lauke **Pavadinimas** įveskite **statika**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="7edbd-161">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="7edbd-162">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="7edbd-163">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="7edbd-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="7edbd-164">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="7edbd-165">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="7edbd-166">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="7edbd-167">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="7edbd-168">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="7edbd-169">Lauke **Užklausos eilučių kaupimo talpykloje būdas** pasirinkite **Talpykloje kaupti kiekvieną unikalų URL**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="7edbd-170">Laukų grupėje **Dinaminis glaudinimas** pasirinkite parinktį **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="7edbd-171">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Taisyklės įtraukimas**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Taisyklės įtraukimas](./media/CDN_CachingRule.png)

<span data-ttu-id="7edbd-173">Įdiegę šią pradinę konfigūraciją, į „Azure Front Door Service“ konfigūraciją turite įtraukti savo pasirinktinį domeną.</span><span class="sxs-lookup"><span data-stu-id="7edbd-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="7edbd-174">Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).</span><span class="sxs-lookup"><span data-stu-id="7edbd-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="7edbd-175">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas CNAME konfigūravimas](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="7edbd-177">Jei jūsų naudosimas domenas jau aktyvus ir paleistas, kreipkitės į palaikymo tarnybą, kad šį domeną būtų galima naudoti su „Azure Front Door Service“ ir nustatyti testą.</span><span class="sxs-lookup"><span data-stu-id="7edbd-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="7edbd-178">Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="7edbd-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="7edbd-179">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="7edbd-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Pasirinktinio domeno HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="7edbd-181">Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.</span><span class="sxs-lookup"><span data-stu-id="7edbd-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7edbd-182">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7edbd-182">Additional resources</span></span>

[<span data-ttu-id="7edbd-183">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7edbd-184">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7edbd-185">Interneto parduotuvės kanalo integravimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-185">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="7edbd-186">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-186">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7edbd-187">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="7edbd-187">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7edbd-188">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="7edbd-188">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7edbd-189">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-189">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7edbd-190">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="7edbd-190">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7edbd-191">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="7edbd-191">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7edbd-192">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-192">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7edbd-193">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="7edbd-193">Enable location-based store detection</span></span>](enable-store-detection.md)
