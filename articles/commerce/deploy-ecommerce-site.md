---
title: Talpinkite naują e-komercijos nuomotoją
description: Šiame skyriuje aprašoma, kaip talpinti naują „Dynamics 365 Commerce“ e-komercijos svetainę naudojant „Microsoft Dynamics  Lifecycle Services“ (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0fff5d47d6eb3e08288d17853fcd94f9eab843c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801954"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="653ec-103">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="653ec-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="653ec-104">Šiame skyriuje aprašoma, kaip talpinti naują „Dynamics 365 Commerce“ e-komercijos svetainę naudojant „Microsoft Dynamics  Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="653ec-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="653ec-105">„Microsoft Dynamics“ „Lifecycle Services“ (LCS) yra debesiu pagrįsta bendradarbiavimo darbo sritis, kurią partneriai ir klientai gali naudoti savo projektams ir aplinkoms tvarkyti, peržiūrėti naujausią informaciją apie „Microsoft Dynamics“ produktus ir funkcijas bei kurti, sekti ir naršyti palaikymo incidentus.</span><span class="sxs-lookup"><span data-stu-id="653ec-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="653ec-106">E-komercijos valdymo funkcijos yra integruotos į LCS.</span><span class="sxs-lookup"><span data-stu-id="653ec-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="653ec-107">Norėdami sužinoti daugiau apie LCS, žr. [„Lifecycle Services“ vartotojo vadovą](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="653ec-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="653ec-108">Pradėta</span><span class="sxs-lookup"><span data-stu-id="653ec-108">Get started</span></span>

<span data-ttu-id="653ec-109">Prieš tai kai pradėsite e-komerciją, turite pradėti projektą, aplinką ir Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="653ec-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="653ec-110">Norėdami atlikti LCS inicijavimą, turite turėti teises, skirtas projekto savininko arba aplinkos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="653ec-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="653ec-111">Palaikomos gamybos ir smėlio dėžės aplinkos topologijos.</span><span class="sxs-lookup"><span data-stu-id="653ec-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="653ec-112">Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="653ec-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="653ec-113">Daugiau informacijos apie RCSU, žr. [„Retail Cloud Scale Unit“ inicijavimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="653ec-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="653ec-114">Pradėkite e-komerciją</span><span class="sxs-lookup"><span data-stu-id="653ec-114">Initialize e-commerce</span></span>

<span data-ttu-id="653ec-115">Naudokite šią procedūrą siekiant pradėti e-komercijos funkciją esančioje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="653ec-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="653ec-116">Prieš pradėdami įsitikinkite, kad turite tokią reikalingą informaciją:</span><span class="sxs-lookup"><span data-stu-id="653ec-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="653ec-117">RSCU, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="653ec-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="653ec-118">„Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama e-komercijos sistemos administratorių.</span><span class="sxs-lookup"><span data-stu-id="653ec-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="653ec-119">„Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama įvertinimų ir apžvalgų moderatoriams.</span><span class="sxs-lookup"><span data-stu-id="653ec-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="653ec-120">Domenai, kurie bus susieti su aplinka.</span><span class="sxs-lookup"><span data-stu-id="653ec-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="653ec-121">Be to, galite rinkti tokią pasirinktinę informaciją:</span><span class="sxs-lookup"><span data-stu-id="653ec-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="653ec-122">„Azure AD“ verslo ir vartotojų (B2C) informaciją:</span><span class="sxs-lookup"><span data-stu-id="653ec-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="653ec-123">Nuomotojo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="653ec-123">Tenant Name.</span></span>
    - <span data-ttu-id="653ec-124">Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="653ec-124">Client ID.</span></span>
    - <span data-ttu-id="653ec-125">Prisijungimo pasirinktinis domenas.</span><span class="sxs-lookup"><span data-stu-id="653ec-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="653ec-126">Atsakymo URL.</span><span class="sxs-lookup"><span data-stu-id="653ec-126">Reply URL.</span></span>
    - <span data-ttu-id="653ec-127">Registracijos prisijungimo strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="653ec-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="653ec-128">Slaptažodžio nustatymo iš naujo strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="653ec-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="653ec-129">Redagavimo profilio strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="653ec-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="653ec-130">Šią informaciją galima įtraukti vėliau, naudojant paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="653ec-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="653ec-131">Jums surinkus reikiamą informaciją, atlikite šiuos žingsnius, kad pradėtumėte e-komerciją.</span><span class="sxs-lookup"><span data-stu-id="653ec-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="653ec-132">Prisijunkite prie [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="653ec-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="653ec-133">Atidarykite projektą, kuriame yra aplinka, kurioje norite pradėti e-komerciją.</span><span class="sxs-lookup"><span data-stu-id="653ec-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="653ec-134">Skyriuje **Aplinkos** pasirinkite aplinką.</span><span class="sxs-lookup"><span data-stu-id="653ec-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="653ec-135">Dalyje **Aplinkos funkcijos** pasirinkite saitą **„Retail“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="653ec-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="653ec-136">Skirtuke **El. prekyba** pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="653ec-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="653ec-137">Atsiranda dialogo langas, kuriame reikia įvesti informaciją, reikalingą kuriant.</span><span class="sxs-lookup"><span data-stu-id="653ec-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="653ec-138">Įveskite reikiamą informaciją ir pereikite prie tolesnio puslapio.</span><span class="sxs-lookup"><span data-stu-id="653ec-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="653ec-139">Kitame puslapyje įveskite reikiamą informaciją ir pateikite formą.</span><span class="sxs-lookup"><span data-stu-id="653ec-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="653ec-140">Jūs grąžinami į skirtuką **El. prekyba**, kur turėtumėte matyti, kad inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="653ec-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="653ec-141">Norėdami peržiūrėti inicijavimo būseną, **atnaujinkite** arba grįžkite į skirtuką **El. prekyba**.</span><span class="sxs-lookup"><span data-stu-id="653ec-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="653ec-142">Kai e-komercija yra pradėta iš LCS, sistemos suteikia keletą komponentų, kurie yra būtini e-komercijai ir susieja juos su aplinka.</span><span class="sxs-lookup"><span data-stu-id="653ec-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="653ec-143">Pasibaigus parengimui, skirtukas **El. prekyba** puslapyje **„Retail“ valdymas** atnaujinamas, kad atsispindėtų parengimą.</span><span class="sxs-lookup"><span data-stu-id="653ec-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="653ec-144">Puslapyje pateikiami naujausi tinkinimo diegimai ir bet kurių kitų vykdomų diegimų būsena.</span><span class="sxs-lookup"><span data-stu-id="653ec-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="653ec-145">Ji taip pat apima nuorodas į e-komercijos saitą ir komercijos saito kūrimo įrankį, kuriame saitai yra leidžiami.</span><span class="sxs-lookup"><span data-stu-id="653ec-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="653ec-146">Prieiga prie komercijos saito kūrimo įrankio</span><span class="sxs-lookup"><span data-stu-id="653ec-146">Access Commerce site builder</span></span>

<span data-ttu-id="653ec-147">Norėdami patekti į komercijos saito kūrimo įrankį, eikite į **e-komercijos** skirtuką  **Mažmeninis valdymas** puslapį LCS ir pasirinkite **e-komercijos saito valdymo įrankio** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="653ec-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="653ec-148">Svetainių daryklės nukreipimo puslapyje rodomas nuomotojo lygio rodinys.</span><span class="sxs-lookup"><span data-stu-id="653ec-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="653ec-149">Šiame puslapyje galite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="653ec-149">From this page, you can:</span></span>

- <span data-ttu-id="653ec-150">Modifikuoti nuomotojo lygio parametrus.</span><span class="sxs-lookup"><span data-stu-id="653ec-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="653ec-151">Pereiti į bet kurią sukurtą svetainę, kurią turite teisę peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="653ec-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="653ec-152">Naudotis peržiūros funkcijomis, pvz., priežiūra ir ataskaitų pateikimu.</span><span class="sxs-lookup"><span data-stu-id="653ec-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="653ec-153">Sukurkite naują svetainę.</span><span class="sxs-lookup"><span data-stu-id="653ec-153">Create a new site.</span></span> <span data-ttu-id="653ec-154">Dėl daugiau informacijos apie tai, kaip sukurti naują saitą, žr. [Sukurkite e-komercijos svetainę](create-ecommerce-site.md) .</span><span class="sxs-lookup"><span data-stu-id="653ec-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="653ec-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="653ec-155">Additional resources</span></span>

[<span data-ttu-id="653ec-156">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="653ec-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="653ec-157">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="653ec-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="653ec-158">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="653ec-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="653ec-159">robots.txt failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="653ec-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="653ec-160">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="653ec-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="653ec-161">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="653ec-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="653ec-162">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="653ec-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="653ec-163">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="653ec-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="653ec-164">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="653ec-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="653ec-165">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="653ec-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
