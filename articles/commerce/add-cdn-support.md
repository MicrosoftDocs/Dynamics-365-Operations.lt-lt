---
title: Turinio pristatymo tinklo (CDN) palaikymo įtraukimas
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936835"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="e55a7-103">Turinio pateikimo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e55a7-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e55a7-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ aplinką įtraukti turinio pristatymo tinklą (CDN).</span><span class="sxs-lookup"><span data-stu-id="e55a7-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="e55a7-105">Jums nustatant e-komercijos aplinką „Dynamics 365 Commerce“, galite konfigūruoti ją darbui su jūsų CDN paslaugomis.</span><span class="sxs-lookup"><span data-stu-id="e55a7-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="e55a7-106">Jūsų tinkintas domenas gali būti įjungtas jūsų e-komercijos aplinkos suteikimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="e55a7-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="e55a7-107">Jį taip pat galite nustatyti naudodami aptarnavimo užklausą, kai konfigūravimo procesas baigtas.</span><span class="sxs-lookup"><span data-stu-id="e55a7-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="e55a7-108">E-komercijos aplinkos suteikimo procesas sukuria šeimininko pavadinimą, susijusį su aplinka.</span><span class="sxs-lookup"><span data-stu-id="e55a7-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="e55a7-109">Pagrindinio kompiuterio pavadinimas yra šio formato, kuriame \<*e-commerce-tenant-name*\> yra jūsų aplinkos pavadinimas:</span><span class="sxs-lookup"><span data-stu-id="e55a7-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="e55a7-110">&lt;el.prekybos-numotojo-vardas&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="e55a7-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="e55a7-111">Pagrindinio kompiuterio vardas arba galinis punktas, sugeneruotas konfigūruojant, palaiko tik \*.commerce.dynamics.com saugiųjų jungčių lygmens (SSL) sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="e55a7-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="e55a7-112">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="e55a7-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="e55a7-113">Todėl turite nutraukti pasirinktinių savo CDN domenų SSL, o srautą iš CDN persiųsti pagrindinio kompiuterio vardui arba galiniam punktui, kurį sugeneravo „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e55a7-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="e55a7-114">Be to, „Commerce“ *statika* („JavaScript“ arba pakopinių stilių sąrašo \[CSS\] failai) teikiama iš galinio punkto, kurį sugeneravo „Commerce“ (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="e55a7-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="e55a7-115">Statiką kaupti talpykloje galima, tik jei „Commerce“ sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas įdedamas už CDN.</span><span class="sxs-lookup"><span data-stu-id="e55a7-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="e55a7-116">Nustatyti SSL</span><span class="sxs-lookup"><span data-stu-id="e55a7-116">Set up SSL</span></span>

<span data-ttu-id="e55a7-117">Sukonfigūravę savo „Commerce“ aplinką naudodami suteiktą pasirinktinį domeną arba pateikę pasirinktinį aplinkos domeną naudodami aptarnavimo užklausą, pasirinktinį domeną, turite bendradarbiauti su „Commerce“ parengimo komanda planuodami DNS pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="e55a7-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="e55a7-118">Kaip buvo minėta anksčiau, sugeneruotas pagrindinio kompiuterio vardas arba galinis punktas palaiko tik \*.commerce.dynamics.com SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="e55a7-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="e55a7-119">Jis nepalaiko pasirinktinių domenų SSL.</span><span class="sxs-lookup"><span data-stu-id="e55a7-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="e55a7-120">CDN tarnybos</span><span class="sxs-lookup"><span data-stu-id="e55a7-120">CDN services</span></span>

<span data-ttu-id="e55a7-121">Su „Commerce“ aplinka galima naudoti bet kurią CDN tarnybą.</span><span class="sxs-lookup"><span data-stu-id="e55a7-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="e55a7-122">Toliau pateikti du pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="e55a7-122">Here are two examples:</span></span>

- <span data-ttu-id="e55a7-123">**„Microsoft Azure Front Door Service“** – „Azure“ CDN sprendimas.</span><span class="sxs-lookup"><span data-stu-id="e55a7-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="e55a7-124">Norėdami apie „Azure Front Door Service“ gauti daugiau informacijos, žr. [„Azure Front Door Service“ dokumentaciją](/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="e55a7-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="e55a7-125">**„Akamai Dynamic Site Accelerator“** – norėdami gauti daugiau informacijos, žr. [„Dynamic Site Accelerator“](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="e55a7-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="e55a7-126">CDN sąranka</span><span class="sxs-lookup"><span data-stu-id="e55a7-126">CDN setup</span></span>

<span data-ttu-id="e55a7-127">CDN sąrankos procesą sudaro tolesni bendrieji veiksmai.</span><span class="sxs-lookup"><span data-stu-id="e55a7-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="e55a7-128">Sąsajos serverio pagrindinio kompiuterio įtraukimas.</span><span class="sxs-lookup"><span data-stu-id="e55a7-128">Add a front-end host.</span></span>
1. <span data-ttu-id="e55a7-129">Vidinio serverio baseino konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="e55a7-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="e55a7-130">Maršruto parinkimo taisyklių nustatymas.</span><span class="sxs-lookup"><span data-stu-id="e55a7-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="e55a7-131">Sąsajos serverio pagrindinio kompiuterio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e55a7-131">Add a front-end host</span></span>

<span data-ttu-id="e55a7-132">Galima naudoti bet kurią CDN tarnybą, tačiau šios temos pavyzdyje naudojama „Azure Front Door Service“.</span><span class="sxs-lookup"><span data-stu-id="e55a7-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="e55a7-133">Norėdami gauti informacijos apie tai, kaip nustatyti „Azure Front Door Service“, žr. [Greitas pasirengimas darbui: „Front Door“ profilio sukūrimas plačiai pasiekiamai visuotinei žiniatinklio programai](/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="e55a7-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="e55a7-134">Konfigūruoti vidinio serverio baseiną „Azure Front Door Service“</span><span class="sxs-lookup"><span data-stu-id="e55a7-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="e55a7-135">Vidinio serverio baseino „Azure Front Door Service“ konfigūravimui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="e55a7-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e55a7-136">Įtraukite **&lt;ecom-nuomotojo-pavadinimas&gt;.commerce.dynamics.com** į vidinį telkinį kaip pasirinktinę pagrindinę svetainę, turinčią vidinę pagrindinę antraštę **&lt;ecom-nuomotojo-pavadinimas&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="e55a7-137">Dalyje **Apkrovos išlyginimas** palikite numatytąsias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e55a7-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="e55a7-138">Išjunkite vidinio telkinio sveikatos patikrinimus.</span><span class="sxs-lookup"><span data-stu-id="e55a7-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="e55a7-139">Toliau pateiktas paveikslėlis rodo **Įtraukti serverį** teksto langelį „Azure Front Door Service“ su serverio pagrindinio kompiuterio įvestu pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="e55a7-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Dialogo langas Vidinio serverio telkinio įtraukimas](./media/CDN_BackendPool.png)

<span data-ttu-id="e55a7-141">Toliau pateiktas paveikslėlis rodo **Įtraukti serverio baseiną** teksto langelį „Azure Front Door Service“ nustatytosios apkrovos balansavimo vertėmis.</span><span class="sxs-lookup"><span data-stu-id="e55a7-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Įtraukti serverio baseino teksto laukelio tęsinį](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="e55a7-143">Įsitikinkite, kad išjungėte **Sveikatos tikrinimo duomenis** nustatydami savo „Azure Front Door Service”, skirtą „Commerce”.</span><span class="sxs-lookup"><span data-stu-id="e55a7-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="e55a7-144">„Azure Front Door Service“ taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="e55a7-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="e55a7-145">Norėdami sprendime „Azure Front Door Service“ nustatyti maršruto parinkimo taisyklę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e55a7-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e55a7-146">Įtraukite maršruto parinkimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="e55a7-146">Add a routing rule.</span></span>
1. <span data-ttu-id="e55a7-147">Lauke **Pavadinimas** įveskite **numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="e55a7-148">Lauke **Pripažįstamas protokolas** pasirinkite **HTTP ir HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="e55a7-149">Lauke **Sąsajos serverio pagrindiniai kompiuteriai** įveskite **dynamics-el.prek-nuomotojo-vardas.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="e55a7-150">Viršutiniame dalies **Gretintini šablonai** lauke įveskite **/\***.</span><span class="sxs-lookup"><span data-stu-id="e55a7-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="e55a7-151">Dalyje **Išsami maršruto informacija** parinktį **Maršruto tipas** nustatykite kaip **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="e55a7-152">Lauke **Vidinio serverio telkinys** pasirinkite **el.prek-vidinisserveris**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="e55a7-153">Laukų grupėje **Persiuntimo protokolas** pasirinkite parinktį **Gretinimo užklausa**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="e55a7-154">Parinktį **URL perrašymas** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="e55a7-155">Parinktį **Kaupimas talpykloje** nustatykite kaip **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="e55a7-156">Jei jūsų naudojamas domenas jau yra veikiantis ir paleistas, sukurkite paramos bilietą **Parama** dreną [„Microsoft Dynamics Lifecycle Services“](https://lcs.dynamics.com/) tam, kad gautumėte pagalbą tolesniems savo veiksmams.</span><span class="sxs-lookup"><span data-stu-id="e55a7-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="e55a7-157">Dėl išsamesnės informacijos, žr.  [Gauti pagalbą „Finance and Operations“ programoms arba „Lifecycle Services (LCS)“](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="e55a7-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="e55a7-158">Jei jūsų domenas yra naujas ir nėra iš anksto egzistuojantis gyvas domenas, galite įtraukti savo tinkintą domeną į „Azure Front Doore Service“ kongirūravimą.</span><span class="sxs-lookup"><span data-stu-id="e55a7-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="e55a7-159">Tai leis žiniatinklio srautui vesti jūsų svetainę pro „Azure Front Door“ pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="e55a7-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="e55a7-160">Norėdami įtraukti pasirinktinį domeną (pavyzdžiui, `www.fabrikam.com`), turite sukonfigūruoti domeno kanoninį vardą (CNAME).</span><span class="sxs-lookup"><span data-stu-id="e55a7-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="e55a7-161">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **CNAME konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas CNAME konfigūravimas](./media/CNAME_Configuration.png)

<span data-ttu-id="e55a7-163">Sertifikatą valdyti galite naudodami „Azure Front Door Service“ arba galite naudoti nuosavą pasirinktinio domeno sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="e55a7-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="e55a7-164">Toliau pateiktoje iliustracijoje parodytas „Azure Front Door Service“ dialogo langas **Pasirinktinio domeno HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="e55a7-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialogo langas Pasirinktinio domeno HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="e55a7-166">Dėl išsamių instrukcijų apie kliento domeno įraukimą į savo „Azure Front Door“, žr. [Įtraukti tinkintą domentą į savo „Front Door“](/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="e55a7-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="e55a7-167">Dabar jūsų CDN turėtų būti tinkamai sukonfigūruotas, kad jį būtų galima naudoti su jūsų „Commerce“ svetaine.</span><span class="sxs-lookup"><span data-stu-id="e55a7-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e55a7-168">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e55a7-168">Additional resources</span></span>

[<span data-ttu-id="e55a7-169">Turinio pristatymo tinklo diegimo parinktys</span><span class="sxs-lookup"><span data-stu-id="e55a7-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]