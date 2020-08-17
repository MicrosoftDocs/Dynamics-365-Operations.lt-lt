---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646044"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="102db-103">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="102db-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="102db-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).</span><span class="sxs-lookup"><span data-stu-id="102db-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="102db-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="102db-105">Overview</span></span>

<span data-ttu-id="102db-106">Programoje „Dynamics 365 Commerce“ nustatydami el. prekybos aplinką, galite sukonfigūruoti, kad ji veiktų su CDN tarnyba.</span><span class="sxs-lookup"><span data-stu-id="102db-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="102db-107">Jūsų pasirinktinį domeną galima įjungti konfigūruojant el. prekybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="102db-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="102db-108">Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas.</span><span class="sxs-lookup"><span data-stu-id="102db-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="102db-109">Konfigūruojant el. prekybos aplinką sugeneruojamas su aplinka susietas pagrindinio kompiuterio vardas.</span><span class="sxs-lookup"><span data-stu-id="102db-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="102db-110">Pagrindinio kompiuterio pavadinimas yra šio formato, kuriame \<*e-commerce-tenant-name*\> yra jūsų aplinkos pavadinimas:</span><span class="sxs-lookup"><span data-stu-id="102db-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="102db-111">&lt;el.prekybos-numotojo-vardas&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="102db-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="102db-112">Pagrindinio kompiuterio vardas arba galinis punktas, sugeneruotas konfigūruojant, palaiko tik \*.commerce.dynamics.com saugiųjų jungčių lygmens (SSL) sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="102db-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="102db-113">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="102db-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="102db-114">Todėl turite nutraukti pasirinktinių savo CDN domenų SSL, o srautą iš CDN persiųsti pagrindinio kompiuterio vardui arba galiniam punktui, kurį sugeneravo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="102db-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="102db-115">Be to, „Commerce“ *statika* („JavaScript“ arba pakopinių stilių sąrašo \[CSS\] failai) teikiama iš galinio punkto, kurį sugeneravo „Commerce“ (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="102db-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="102db-116">Statiką kaupti talpykloje galima, tik jei „Commerce“ sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas įdedamas už CDN.</span><span class="sxs-lookup"><span data-stu-id="102db-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="102db-117">SSL nustatymas</span><span class="sxs-lookup"><span data-stu-id="102db-117">Set up SSL</span></span>

<span data-ttu-id="102db-118">Norėdami padėti užtikrinti, kad būtų nustatytas SSL ir talpykloje kaupiama statika, turite sukonfigūruoti, kad jūsų CDN būtų susietas su pagrindinio kompiuterio vardu, kurį „Commerce“ sugeneravo jūsų aplinkai.</span><span class="sxs-lookup"><span data-stu-id="102db-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="102db-119">Taip pat turite talpykloje kaupti tik tolesnį statikos šabloną.</span><span class="sxs-lookup"><span data-stu-id="102db-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="102db-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="102db-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="102db-121">Sukonfigūravę savo „Commerce“ aplinką naudodami suteiktą pasirinktinį domeną arba pateikę pasirinktinį aplinkos domeną naudodami aptarnavimo užklausą, pasirinktinį domeną nukreipkite į „Commerce“ sugeneruotą pagrindinio kompiuterio vardą arba galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="102db-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="102db-122">Kaip buvo minėta anksčiau, sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas palaiko tik \*.commerce.dynamics.com SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="102db-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="102db-123">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="102db-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="102db-124">CDN tarnybos</span><span class="sxs-lookup"><span data-stu-id="102db-124">CDN services</span></span>

<span data-ttu-id="102db-125">Su „Commerce“ aplinka galima naudoti bet kurią CDN tarnybą.</span><span class="sxs-lookup"><span data-stu-id="102db-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="102db-126">Toliau pateikti du pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="102db-126">Here are two examples:</span></span>

- <span data-ttu-id="102db-127">**„Microsoft Azure Front Door Service“** – „Azure“ CDN sprendimas.</span><span class="sxs-lookup"><span data-stu-id="102db-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="102db-128">Norėdami apie „Azure Front Door Service“ gauti daugiau informacijos, žr. [„Azure Front Door Service“ dokumentaciją](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="102db-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="102db-129">**„Akamai Dynamic Site Accelerator“** – norėdami gauti daugiau informacijos, žr. [„Dynamic Site Accelerator“](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="102db-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="102db-130">CDN sąranka</span><span class="sxs-lookup"><span data-stu-id="102db-130">CDN setup</span></span>

<span data-ttu-id="102db-131">CDN sąrankos procesą sudaro tolesni bendrieji veiksmai.</span><span class="sxs-lookup"><span data-stu-id="102db-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="102db-132">Įtraukite sąsajos serverio pagrindinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="102db-132">Add a front-end host.</span></span>
1. <span data-ttu-id="102db-133">Konfigūruoti vidinio serverio baseiną.</span><span class="sxs-lookup"><span data-stu-id="102db-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="102db-134">Nustatykite maršruto parinkimo ir kaupimo talpykloje taisykles.</span><span class="sxs-lookup"><span data-stu-id="102db-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="102db-135">Sąsajos serverio pagrindinio kompiuterio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="102db-135">Add a front-end host</span></span>

<span data-ttu-id="102db-136">Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“.</span><span class="sxs-lookup"><span data-stu-id="102db-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="102db-137">Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="102db-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="102db-138">Konfigūruoti vidinio serverio baseiną „Azure Front Door Service“</span><span class="sxs-lookup"><span data-stu-id="102db-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="102db-139">Vidinio serverio baseino „Azure Front Door Service“ konfigūravimui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="102db-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="102db-140">Įtraukti **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** vidinio serverio baseiną, kaip tinkintą pagrindinį kompiuterį, kuris turi tuščią vidinio serverio pagrindinio kompiuterio antraštę.</span><span class="sxs-lookup"><span data-stu-id="102db-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="102db-141">Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="102db-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="102db-142">Toliau pateiktas paveikslėlis rodo **Įtraukti serverį** teksto langelį „Azure Front Door Service“ su serverio pagrindinio kompiuterio įvestu pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="102db-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Dialogo langas Vidinio serverio telkinio įtraukimas](./media/CDN_BackendPool.png)

<span data-ttu-id="102db-144">Toliau pateiktas paveikslėlis rodo **Įtraukti serverio baseiną** teksto langelį „Azure Front Door Service“ nustatytosios apkrovos balansavimo vertėmis.</span><span class="sxs-lookup"><span data-stu-id="102db-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Įtraukti serverio baseino teksto laukelio tęsinį](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="102db-146">„Azure Front Door Service“ taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="102db-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="102db-147">Norėdami sprendime „Azure Front Door Service“ nustatyti maršruto parinkimo taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="102db-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="102db-148">Įtraukite maršruto parinkimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="102db-148">Add a routing rule.</span></span>
1. <span data-ttu-id="102db-149">Lauke **Pavadinimas** įveskite **numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="102db-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="102db-150">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="102db-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="102db-151">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="102db-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="102db-152">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\***.</span><span class="sxs-lookup"><span data-stu-id="102db-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="102db-153">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="102db-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="102db-154">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="102db-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="102db-155">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="102db-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="102db-156">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="102db-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="102db-157">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="102db-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="102db-158">Norėdami sprendime „Azure Front Door Service“ nustatyti kaupimo talpykloje taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="102db-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="102db-159">Įtraukite kaupimo talpykloje taisyklę.</span><span class="sxs-lookup"><span data-stu-id="102db-159">Add a caching rule.</span></span>
1. <span data-ttu-id="102db-160">Lauke **Pavadinimas** įveskite **statika**.</span><span class="sxs-lookup"><span data-stu-id="102db-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="102db-161">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="102db-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="102db-162">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="102db-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="102db-163">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="102db-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="102db-164">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="102db-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="102db-165">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="102db-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="102db-166">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="102db-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="102db-167">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="102db-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="102db-168">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="102db-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="102db-169">Lauke **Užklausos eilučių kaupimo talpykloje būdas** pasirinkite **Talpykloje kaupti kiekvieną unikalų URL**.</span><span class="sxs-lookup"><span data-stu-id="102db-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="102db-170">Laukų grupėje **Dinaminis glaudinimas** pasirinkite parinktį **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="102db-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="102db-171">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Taisyklės įtraukimas**.</span><span class="sxs-lookup"><span data-stu-id="102db-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Taisyklės įtraukimas](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="102db-173">Jei jūsų naudojamas domenas jau yra veikiantis ir paleistas, sukurkite paramos bilietą **Parama** dreną [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com/) tam, kad gautumėte pagalbą tolesniems savo veiksmams.</span><span class="sxs-lookup"><span data-stu-id="102db-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="102db-174">Dėl išsamesnės informacijos, žr.  [Gauti pagalbą „Finance and Operations“ programoms arba „Lifecycle Services (LCS)“](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="102db-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="102db-175">Jei jūsų domenas yra naujas ir nėra iš anksto egzistuojantis gyvas domenas, galite įtraukti savo tinkintą domeną į „Azure Front Doore Service“ kongirūravimą.</span><span class="sxs-lookup"><span data-stu-id="102db-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="102db-176">Tai leis žiniatinklio srautui vesti jūsų svetainę pro „Azure Front Door“ pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="102db-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="102db-177">Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).</span><span class="sxs-lookup"><span data-stu-id="102db-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="102db-178">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="102db-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas CNAME konfigūravimas](./media/CNAME_Configuration.png)

<span data-ttu-id="102db-180">Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="102db-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="102db-181">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="102db-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Pasirinktinio domeno HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="102db-183">Dėl išsamių instrukcijų apie kliento domeno įraukimą į savo „Azure Front Door“, žr. [Įtraukti tinkintą domentą į savo „Front Door“](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="102db-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="102db-184">Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.</span><span class="sxs-lookup"><span data-stu-id="102db-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="102db-185">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="102db-185">Additional resources</span></span>

[<span data-ttu-id="102db-186">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="102db-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="102db-187">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="102db-187">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="102db-188">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="102db-188">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="102db-189">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="102db-189">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="102db-190">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="102db-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="102db-191">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="102db-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="102db-192">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="102db-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="102db-193">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="102db-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="102db-194">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="102db-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="102db-195">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="102db-195">Enable location-based store detection</span></span>](enable-store-detection.md)
