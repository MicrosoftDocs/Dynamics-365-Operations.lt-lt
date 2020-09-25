---
title: „Dynamics 365 Commerce” domenai
description: Šioje temoje aprašoma, kaip domenai valdomi „Microsoft Dynamics 365 Commerce”.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 84becee12363ca38951ff13073d87d1b1f14b616
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765006"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="452ba-103">„Dynamics 365 Commerce” domenai</span><span class="sxs-lookup"><span data-stu-id="452ba-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="452ba-104">Šioje temoje aprašoma, kaip domenai valdomi „Microsoft Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="452ba-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="452ba-105">Domenai yra interneto adresai, naudojami pereiti į „Dynamics 365 Commerce” svetaines žiniatinklio naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="452ba-106">Jūs kontroliuojate jūsų domeno valdymą su pasirinktu domenų vardų serverio (DNS) tiekėju.</span><span class="sxs-lookup"><span data-stu-id="452ba-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="452ba-107">Domenai nurodomi „Dynamics 365 Commerce” svetainių daryklėje, kad būtų galima koordinuoti, kaip svetainė bus pasiekiama publikavus.</span><span class="sxs-lookup"><span data-stu-id="452ba-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="452ba-108">Šioje temoje nagrinėjama, kaip domenai valdomi ir nurodomi „Commerce” svetainės kūrimo ir paleidimo ciklo metu.</span><span class="sxs-lookup"><span data-stu-id="452ba-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="452ba-109">Parengimas ir palaikomi pagrindinių kompiuterių vardai</span><span class="sxs-lookup"><span data-stu-id="452ba-109">Provisioning and supported host names</span></span>

<span data-ttu-id="452ba-110">Kuriant „e-Commerce” aplinką [„Microsoft Dynamics Lifecycle Services” (LCS)](https://lcs.dynamics.com/), „e-Commerce” parengimo ekrane rodomas laukas **Palaikomi pagrindinių kompiuterių vardai** naudojamas domenams, kurie bus susieti su įdiegta „Commerce” aplinka, įvesti.</span><span class="sxs-lookup"><span data-stu-id="452ba-110">When provisioning an e-Commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-Commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="452ba-111">Šie domenai bus kliento domenų vardų serverio (DNS) vardai, kur bus nuomojamos „e-Commerce” svetainės.</span><span class="sxs-lookup"><span data-stu-id="452ba-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-Commerce websites will be hosted.</span></span> <span data-ttu-id="452ba-112">Šio etapo metu įvedus domeną nepradedama nukreipti domeno srauto į „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="452ba-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="452ba-113">Domeno srautas bus nukreiptas į „Commerce” galinį punktą, tik kai atnaujinamas DNS CNAME įrašas, kad „Commerce” galinis punktas būtų naudojamas su domenu.</span><span class="sxs-lookup"><span data-stu-id="452ba-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="452ba-114">Kelis domenus galima įvesti į langelį **Palaikomi pagrindinių kompiuterių vardai** atskiriant juos kabliataškiais.</span><span class="sxs-lookup"><span data-stu-id="452ba-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="452ba-115">Toliau pateiktoje iliustracijoje parodytas LCS „e-Commerce” parengimo ekranas, kuriame paryškintas langelis **Palaikomi pagrindinių kompiuterių vardai**.</span><span class="sxs-lookup"><span data-stu-id="452ba-115">The following illustration shows the LCS e-Commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![LCS „e-Commerce” parengimo ekranas, kuriame paryškintas langelis **Palaikomi pagrindinių kompiuterių vardai**](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="452ba-117">Galite sukurti paslaugos užklausą, norėdami įtraukti papildomus domenus į aplinką, jei parengimas jau įvyko.</span><span class="sxs-lookup"><span data-stu-id="452ba-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="452ba-118">Norėdami sukurti paslaugos užklausą LCS, jūsų aplinkoje eikite į **Palaikymas \> Palaikymo problemos** ir pasirinkite **Pateikti incidentą**.</span><span class="sxs-lookup"><span data-stu-id="452ba-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="452ba-119">„Commerce” sugeneruoti URL</span><span class="sxs-lookup"><span data-stu-id="452ba-119">Commerce-generated URLs</span></span>

<span data-ttu-id="452ba-120">Rengiant „e-Commerce” aplinką, „Commerce” sugeneruos URL, kuris bus aplinkos darbo adresas.</span><span class="sxs-lookup"><span data-stu-id="452ba-120">When provisioning an e-Commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="452ba-121">Šis URL nurodomas „e-Commerce” svetainės saite, kuris rodomas LCS po to, kai aplinka sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="452ba-121">This URL is referenced in the e-Commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="452ba-122">„Commerce” sugeneruoto URL formatas yra `https://<e-Commerce tenant name>.commerce.dynamics.com`, kuriame „e-Commerce” nuomotojo pavadinimas yra LCS įvestas „Commerce” aplinkos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="452ba-122">A Commerce-generated URL is in the format `https://<e-Commerce tenant name>.commerce.dynamics.com`, where the e-Commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="452ba-123">Taip pat galite naudoti gamybos svetainės pagrindinių kompiuterių vardus smėlio dėžės aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="452ba-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="452ba-124">Ši parinktis puikiai tinka, kai kopijuojate svetainę iš smėlio dėžės aplinkos į gamybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="452ba-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="452ba-125">Svetainės sąranka</span><span class="sxs-lookup"><span data-stu-id="452ba-125">Site setup</span></span>

<span data-ttu-id="452ba-126">Kai parengta jūsų „e-Commerce” aplinka, turite nustatyti jūsų svetainę „Commerce” svetainių daryklėje ir susieti jūsų svetainę su darbo URL.</span><span class="sxs-lookup"><span data-stu-id="452ba-126">After your e-Commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="452ba-127">Pirmą kartą nustačius svetainę svetainių daryklėje, bus rodomas dialogo langas **Jūsų svetainės nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="452ba-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="452ba-128">Toliau pateiktoje iliustracijoje rodomas dialogo langas **Jūsų svetainės nustatymas** svetainei, kurios pavadinimas „numatytoji”, kai pirmą kartą pasiekiate svetainę svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![Dialogo langas **Jūsų svetainės nustatymas**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="452ba-130">Langelis **Pasirinkti domeną** leidžia susieti vieną iš palaikomų pagrindinių kompiuterių vardų, pateiktų jūsų svetainei LCS, su svetaine, esančia svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="452ba-131">Langelis **Kelias** gali būti paliktas tuščias arba galima įtraukti papildomą kelio eilutę, kuri bus rodoma jūsų darbo URL.</span><span class="sxs-lookup"><span data-stu-id="452ba-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="452ba-132">Jei langelis **Kelias** paliekamas tuščias, pagrindinis „Commerce” sugeneruotas URL susiejamas su svetaine, kuri nustatoma svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="452ba-133">Kiekvienos svetainės / domeno poros keliai turi būti unikalūs.</span><span class="sxs-lookup"><span data-stu-id="452ba-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="452ba-134">Pasirinkus svetainę ir domeną, tik viena aplinkos svetainė gali naudoti tuščią kelią arba būti susieta su unikalaus kelio eilute.</span><span class="sxs-lookup"><span data-stu-id="452ba-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="452ba-135">Bet kokia eilutė, įtraukta į lauką **Kelias** atliekant svetainės nustatymą, taps papildomu pagrindinio „Commerce” sugeneruoto URL, naudojamo svetainei pasiekti žiniatinklio naršyklėje, keliu.</span><span class="sxs-lookup"><span data-stu-id="452ba-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="452ba-136">Šis kelias dar žinomas kaip **Kelio atitikmuo**, kai įtraukiamas kanalas svetainės daryklės konfigūracijos skyriuje **Svetainės parametrai \> Kanalai**.</span><span class="sxs-lookup"><span data-stu-id="452ba-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="452ba-137">Pvz., jei svetainių daryklės „e-Commerce” nuomotojuje pavadinimu „xyz“ turite svetainę pavadinimu „fabrikam“ ir nustatėte svetainę tuščiu keliu, tada turėtumėte prieigą prie paskelbto svetainės turinio žiniatinklio naršyklėje eidami tiesiai į pagrindinį „Commerce” sugeneruotą URL.</span><span class="sxs-lookup"><span data-stu-id="452ba-137">For example, if you have a site in site builder called "fabrikam" in an e-Commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="452ba-138">Taip pat, jei tos pačios svetainės nustatymo metu įtraukėte „fabrikam” kelią, turėtumėte prieigą prie paskelbto svetainės turinio žiniatinklio naršyklėje naudodami toliau pateiktą URL.</span><span class="sxs-lookup"><span data-stu-id="452ba-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="452ba-139">Puslapiai ir URL</span><span class="sxs-lookup"><span data-stu-id="452ba-139">Pages and URLs</span></span>

<span data-ttu-id="452ba-140">Nustačius svetainę keliu, visi URL, susieti su svetainės daryklės puslapiais, bus sukurti pagal darbo URL („Commerce” sugeneruotą URL arba „Commerce” sugeneruotą URL ir kelią), skirtą svetainei.</span><span class="sxs-lookup"><span data-stu-id="452ba-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="452ba-141">Jei kursite naują URL svetainių daryklėje (**URL /> +Naujas**) pasirinkdami puslapį iš sąrašo, esančiame dialogo lange **Naujas URL** ir įvesdami to puslapio URL kelią, tas URL bus susietas su pasirinktu puslapiu.</span><span class="sxs-lookup"><span data-stu-id="452ba-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="452ba-142">URL kelio reikšmė tada pridedama prie svetainės darbo URL, kad būtų galima pasiekti puslapį, ir yra pažymėta kaip `./<URL path>` svetainių daryklės puslapio **URL** URL sąraše.</span><span class="sxs-lookup"><span data-stu-id="452ba-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="452ba-143">Toliau pateiktame paveikslėlyje parodytas dialogo langas **Naujas URL** svetainių daryklėje ir paryškintas pavyzdinis URL kelias.</span><span class="sxs-lookup"><span data-stu-id="452ba-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![Dialogo langas **Naujas URL** svetainių daryklėje](./media/Domains_PageSetup2a.png)

<span data-ttu-id="452ba-145">Toliau pateiktame paveikslėlyje parodytas puslapis **URL** svetainių daryklėje ir sąraše paryškintas pavyzdinis URL.</span><span class="sxs-lookup"><span data-stu-id="452ba-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![Vartotojo srauto vykdymo parinktis strategijos sraute](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="452ba-147">Domenai svetainių daryklėje</span><span class="sxs-lookup"><span data-stu-id="452ba-147">Domains in site builder</span></span>

<span data-ttu-id="452ba-148">Palaikomų pagrindinių kompiuterių vardų reikšmės gali būti susietos kaip domenas nustatant svetainę.</span><span class="sxs-lookup"><span data-stu-id="452ba-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="452ba-149">Renkantis palaikomą pagrindinio kompiuterio vardo reikšmę kaip domeną, pasirinktas domenas bus nurodytas svetainės daryklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="452ba-150">Šis domenas „Commerce” aplinkoje yra tik nuoroda, o to domeno tiesioginis srautas nebus perduotas į „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="452ba-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="452ba-151">Kai dirbate su svetainėmis svetainių daryklėje, jei turite dvi svetaines, nustatytas su dviem skirtingais domenais, galite pridėti atributą **?domain=** prie savo darbo URL, kad galėtumėte pasiekti publikuotą svetainės turinį naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="452ba-152">Pvz., aplinka „xyz” buvo parengta, o svetainių daryklėje sukurtos ir susietos dvi svetainės: viena su domenu `www.fabrikam.com` ir kita su domenu `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="452ba-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="452ba-153">Kiekviena svetainė buvo nustatyta naudojant tuščią kelią.</span><span class="sxs-lookup"><span data-stu-id="452ba-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="452ba-154">Tada šios dvi svetainės gali būti pasiekiamos žiniatinklio naršyklėje naudojant atributą **?domain=**, kaip pateikta toliau.</span><span class="sxs-lookup"><span data-stu-id="452ba-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="452ba-155">Kai domeno užklausos eilutė nenurodyta aplinkoje su keliais domenais, „Commerce” naudoja pirmą domeną, kurį nurodėte.</span><span class="sxs-lookup"><span data-stu-id="452ba-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="452ba-156">Pavyzdžiui, jei kelias „fabrikam” buvo pateiktas pirmiausiai svetainės nustatymo metu, URL `https://xyz.commerce.dynamics.com` gali būti naudojamas pasiekti publikuotos svetainės turinį `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="452ba-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="452ba-157">Srauto perdavimas gamybos metu</span><span class="sxs-lookup"><span data-stu-id="452ba-157">Traffic forwarding in production</span></span>

<span data-ttu-id="452ba-158">Galite imituoti kelis domenus naudodami domeno užklausos eilutės parametrus, esančius commerce.dynamics.com galiniame punkte.</span><span class="sxs-lookup"><span data-stu-id="452ba-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="452ba-159">Tačiau kai reikia įgyvendinti gamybos metu, turite persiųsti jūsų pasirinktinio domeno srautą į `<e-Commerce tenant name>.commerce.dynamics.com` galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="452ba-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-Commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="452ba-160">`<e-Commerce tenant name>.commerce.dynamics.com` galinis punktas nepalaiko pasirinktinio domeno saugiųjų jungčių lygmenų (SSL), todėl reikia nustatyti pasirinktinius domenus naudojant „Front Door Service“ arba turinio pristatymo tinklą (CDN).</span><span class="sxs-lookup"><span data-stu-id="452ba-160">The `<e-Commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="452ba-161">Norėdami nustatyti pasirinktinius domenus naudodami „Front Door Service“ arba CDN, turite dvi toliau pateiktas parinktis.</span><span class="sxs-lookup"><span data-stu-id="452ba-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="452ba-162">Nustatykite „Azure Front Door”, kad būtų galima valdyti sąsajos serverio srautą ir prisijungti prie savo „Commerce” aplinkos.</span><span class="sxs-lookup"><span data-stu-id="452ba-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="452ba-163">Tai suteikia galimybę labiau kontroliuoti domenus ir sertifikatus bei išsamesnes saugos strategijas.</span><span class="sxs-lookup"><span data-stu-id="452ba-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="452ba-164">Naudokite „Commerce” pateiktą „Azure Front Door” egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="452ba-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="452ba-165">Tam reikia koordinuoti veiksmus su „Dynamics 365 Commerce” komanda, kad būtų galima atlikti domeno tikrinimą ir gauti SSL sertifikatus savo gamybos domenui.</span><span class="sxs-lookup"><span data-stu-id="452ba-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="452ba-166">Informacijos apie tai, kaip nustatyti CDN paslaugą tiesiogiai, žr. [Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="452ba-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="452ba-167">Norėdami naudoti „Commerce” teikiamą „Azure Front Door” egzempliorių, turite sukurti paslaugos užklausą, kad gautumėte CDN nustatymo pagalbos iš „Commerce” supažindinimo komandos.</span><span class="sxs-lookup"><span data-stu-id="452ba-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="452ba-168">Jums reikės nurodyti jūsų įmonės pavadinimą, gamybos domeną, aplinkos ID ir gamybos „e-Commerce” nuomotojo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="452ba-168">You will need to provide your company name, the production domain, environment ID, and production e-Commerce tenant name.</span></span> 
- <span data-ttu-id="452ba-169">Jums reikės patvirtinti, ar tai esamas domenas (naudojamas šiuo metu aktyvioje svetainėje), ar naujas domenas.</span><span class="sxs-lookup"><span data-stu-id="452ba-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="452ba-170">Jei tai naujas domenas, domeno tikrinimas ir SSL sertifikatas gali būti pasiektas vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="452ba-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="452ba-171">Jei tai esamos svetainės domenas, yra kelių veiksmų procesas, kurio reikia norint nustatyti domeno tikrinimą ir SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="452ba-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="452ba-172">Šis procesas turi 7 darbo dienų aptarnavimo lygio sutartį (SLA), skirtą domenui, kad jis būtų įgyvendintas, nes procesas apima kelis nuoseklius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="452ba-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="452ba-173">Norėdami sukurti paslaugos užklausą LCS, jūsų aplinkoje eikite į **Palaikymas \> Palaikymo problemos** ir pasirinkite **Pateikti incidentą**.</span><span class="sxs-lookup"><span data-stu-id="452ba-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="452ba-174">Pasirinktiniai domenai su SSL palaikomi tik gamybos aplinkose.</span><span class="sxs-lookup"><span data-stu-id="452ba-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="452ba-175">Ne gamybos aplinkose, pvz., smėlio dėžės ir vartotojo priėmimo testavimo (UAT), naudokite „Commerce” sugeneruotą URL, kad pasiektumėte publikuotą turinį žiniatinklio naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="452ba-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="452ba-176">SSL sertifikato procesas</span><span class="sxs-lookup"><span data-stu-id="452ba-176">SSL certificate process</span></span>

<span data-ttu-id="452ba-177">Kai paslaugos užklausa pateikta, „Commerce” komanda su jumis derins toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="452ba-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="452ba-178">Jei domenai nauji, bus atlikti toliau pateikti veiksmai.</span><span class="sxs-lookup"><span data-stu-id="452ba-178">For new domains:</span></span>
- <span data-ttu-id="452ba-179">„Commerce” komanda nustatys „Azure Front Door” egzempliorių („Commerce” nuomojamą).</span><span class="sxs-lookup"><span data-stu-id="452ba-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="452ba-180">Tada „Commerce” komanda pateiks CNAME įrašą, kuris nurodys į jūsų pasirinktinį domeną.</span><span class="sxs-lookup"><span data-stu-id="452ba-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="452ba-181">Po to, kai CNAME įrašas bus atnaujintas, „Commerce” nuomojamas „Azure Front Door” egzempliorius galės patikrinti domeno savininką ir gauti SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="452ba-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="452ba-182">Jei domenai esami / aktyvūs, bus atlikti toliau pateikti veiksmai.</span><span class="sxs-lookup"><span data-stu-id="452ba-182">For existing/active domains:</span></span>
- <span data-ttu-id="452ba-183">„Commerce” komanda nurodys jums, kaip įtraukti `afdverify.<custom-domain>` CNAME įrašą, kad būtų galima jį pateikti jūsų domeno DNS teikėjui.</span><span class="sxs-lookup"><span data-stu-id="452ba-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="452ba-184">Baigus, „Commerce” komanda įtrauks domeną į „Azure Front Door” egzempliorių ir pateiks papildomų DNS TXT įrašų, kad jie būtų įtraukti į domeno DNS.</span><span class="sxs-lookup"><span data-stu-id="452ba-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="452ba-185">Užbaigus TXT įrašus, „Commerce” komanda užbaigs „Azure Front Door” naujinimus, skirtus domenui, kuris nustatys SSL sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="452ba-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="452ba-186">Viršūnės domenai</span><span class="sxs-lookup"><span data-stu-id="452ba-186">Apex domains</span></span>

<span data-ttu-id="452ba-187">„Commerce” teikiamas „Azure Front Door” egzempliorius nepalaiko viršūnės domenų (šakninių domenų, kuriuose nėra antrinių domenų).</span><span class="sxs-lookup"><span data-stu-id="452ba-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="452ba-188">Viršūnės domenams išspręsti reikalingas IP adresas, o „Commerce Azure Front Door” egzempliorius egzistuoja tik su virtualiaisiais galiniais punktais.</span><span class="sxs-lookup"><span data-stu-id="452ba-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="452ba-189">Norėdami naudoti viršūnės domeną, turite dvi toliau pateiktas parinktis.</span><span class="sxs-lookup"><span data-stu-id="452ba-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="452ba-190">**1 parinktis** – naudokite jūsų DNS teikėją, kad nukreiptumėte viršūnės domeną į „www” domeną.</span><span class="sxs-lookup"><span data-stu-id="452ba-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="452ba-191">Pvz., fabrikam.com nukreipia į `www.fabrikam.com`, o `www.fabrikam.com` yra CNAME įrašas, nurodantis į „Commerce” nuomojamą „Azure Front Door” egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="452ba-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="452ba-192">**2 parinktis** – nustatykite CDN / „Front Door” egzempliorių, kad būtų galima nuomoti viršūnės domeną.</span><span class="sxs-lookup"><span data-stu-id="452ba-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="452ba-193">Jei naudojate „Azure Front Door”, taip pat turite nustatyti „Azure” DNS toje pačioje prenumeratoje.</span><span class="sxs-lookup"><span data-stu-id="452ba-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="452ba-194">Viršūnės domenas, nuomojamas „Azure” DNS, gali nukreipti į jūsų „Azure Front Door” kaip į pseudonimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="452ba-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="452ba-195">Tai yra vienintelis sprendimas, nes viršūnės domenai visada turi nukreipti į IP adresą.</span><span class="sxs-lookup"><span data-stu-id="452ba-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="452ba-196">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="452ba-196">Additional resources</span></span>

  [<span data-ttu-id="452ba-197">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="452ba-197">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="452ba-198">Interneto parduotuvės kanalo integravimas</span><span class="sxs-lookup"><span data-stu-id="452ba-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="452ba-199">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="452ba-199">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="452ba-200">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="452ba-200">Associate an online site with a channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="452ba-201">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="452ba-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="452ba-202">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="452ba-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="452ba-203">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="452ba-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="452ba-204">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="452ba-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="452ba-205">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="452ba-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="452ba-206">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="452ba-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="452ba-207">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="452ba-207">Enable location-based store detection</span></span>](enable-store-detection.md)
