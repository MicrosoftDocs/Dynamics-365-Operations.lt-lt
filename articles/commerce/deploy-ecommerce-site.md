---
title: Naujo el. prekybos nuomotojo diegimas
description: Šioje temoje aprašoma, kaip įdiegti naują el. prekybos nuomininką naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).
author: psimolin
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d5cf2804c44e81ad135a3248d38c228148b530cc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096683"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="45a46-103">Naujo el. prekybos nuomotojo diegimas</span><span class="sxs-lookup"><span data-stu-id="45a46-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="45a46-104">Šioje temoje aprašoma, kaip įdiegti naują el. prekybos svetainę naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="45a46-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="45a46-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="45a46-105">Overview</span></span>

<span data-ttu-id="45a46-106">„Microsoft Dynamics“ „Lifecycle Services“ (LCS) yra debesiu pagrįsta bendradarbiavimo darbo sritis, kurią partneriai ir klientai gali naudoti savo projektams ir aplinkoms tvarkyti, peržiūrėti naujausią informaciją apie „Microsoft Dynamics“ produktus ir funkcijas bei kurti, sekti ir naršyti palaikymo incidentus.</span><span class="sxs-lookup"><span data-stu-id="45a46-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="45a46-107">El. prekybos valdymo funkcijos integruotos į LCS.</span><span class="sxs-lookup"><span data-stu-id="45a46-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="45a46-108">Norėdami sužinoti daugiau apie LCS, žr. [„Lifecycle Services“ vartotojo vadovą](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="45a46-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="45a46-109">Darbo pradžia</span><span class="sxs-lookup"><span data-stu-id="45a46-109">Get started</span></span>

<span data-ttu-id="45a46-110">Kad galėtumėte paleisti el. prekybą, turite paleisti projektą, aplinką ir „Retail Cloud Scale Unit“ (RCSU).</span><span class="sxs-lookup"><span data-stu-id="45a46-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="45a46-111">Norėdami atlikti LCS inicijavimą, turite turėti teises, skirtas projekto savininko arba aplinkos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="45a46-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="45a46-112">Palaikomos gamybos ir smėlio dėžės aplinkos topologijos.</span><span class="sxs-lookup"><span data-stu-id="45a46-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="45a46-113">Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="45a46-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="45a46-114">Daugiau informacijos apie RCSU, žr. [„Retail Cloud Scale Unit“ inicijavimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="45a46-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="45a46-115">El. prekybos inicijavimas</span><span class="sxs-lookup"><span data-stu-id="45a46-115">Initialize e-Commerce</span></span>

<span data-ttu-id="45a46-116">Naudokite šią procedūrą paleisti el. prekybos funkciją esamoje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="45a46-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="45a46-117">Prieš pradėdami įsitikinkite, kad turite tokią reikalingą informaciją:</span><span class="sxs-lookup"><span data-stu-id="45a46-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="45a46-118">RSCU, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="45a46-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="45a46-119">„Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama el. prekybos sistemos administratoriams.</span><span class="sxs-lookup"><span data-stu-id="45a46-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="45a46-120">„Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama įvertinimų ir apžvalgų moderatoriams.</span><span class="sxs-lookup"><span data-stu-id="45a46-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="45a46-121">Domenai, kurie bus susieti su aplinka.</span><span class="sxs-lookup"><span data-stu-id="45a46-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="45a46-122">Be to, galite rinkti tokią pasirinktinę informaciją:</span><span class="sxs-lookup"><span data-stu-id="45a46-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="45a46-123">„Azure AD“ verslo ir vartotojų (B2C) informaciją:</span><span class="sxs-lookup"><span data-stu-id="45a46-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="45a46-124">Nuomotojo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="45a46-124">Tenant Name.</span></span>
    - <span data-ttu-id="45a46-125">Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="45a46-125">Client ID.</span></span>
    - <span data-ttu-id="45a46-126">Prisijungimo pasirinktinis domenas.</span><span class="sxs-lookup"><span data-stu-id="45a46-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="45a46-127">Atsakymo URL.</span><span class="sxs-lookup"><span data-stu-id="45a46-127">Reply URL.</span></span>
    - <span data-ttu-id="45a46-128">Registracijos prisijungimo strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="45a46-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="45a46-129">Slaptažodžio nustatymo iš naujo strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="45a46-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="45a46-130">Redagagavimo profilio strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="45a46-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="45a46-131">Šią informaciją galima įtraukti vėliau, naudojant paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="45a46-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="45a46-132">Surinkę reikiamą informaciją, atlikite šiuos veiksmus, norėdami paleisti el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="45a46-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="45a46-133">Prisijunkite prie [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="45a46-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="45a46-134">Atidarykite projektą, kuriame yra aplinka, kurioje norima paleisti el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="45a46-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="45a46-135">Skyriuje **Aplinkos** pasirinkite aplinką.</span><span class="sxs-lookup"><span data-stu-id="45a46-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="45a46-136">Dalyje **Aplinkos funkcijos** pasirinkite saitą **„Retail“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="45a46-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="45a46-137">Skirtuke **El. prekyba** pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="45a46-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="45a46-138">Atsiranda dialogo langas, kuriame reikia įvesti informaciją, reikalingą kuriant.</span><span class="sxs-lookup"><span data-stu-id="45a46-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="45a46-139">Įveskite reikiamą informaciją ir pereikite prie tolesnio puslapio.</span><span class="sxs-lookup"><span data-stu-id="45a46-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="45a46-140">Kitame puslapyje įveskite reikiamą informaciją ir pateikite formą.</span><span class="sxs-lookup"><span data-stu-id="45a46-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="45a46-141">Jūs grąžinami į skirtuką **El. prekyba**, kur turėtumėte matyti, kad inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="45a46-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="45a46-142">Norėdami peržiūrėti inicijavimo būseną, **atnaujinkite** arba grįžkite į skirtuką **El. prekyba**.</span><span class="sxs-lookup"><span data-stu-id="45a46-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="45a46-143">Paleidus el. prekybą iš LCS, sistema sukuria keletą komponentų, kurie būtini el. prekybai ir susieja juos su aplinka.</span><span class="sxs-lookup"><span data-stu-id="45a46-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="45a46-144">Pasibaigus parengimui, skirtukas **El. prekyba** puslapyje **„Retail“ valdymas** atnaujinamas, kad atsispindėtų parengimą.</span><span class="sxs-lookup"><span data-stu-id="45a46-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="45a46-145">Puslapyje pateikiami naujausi tinkinimo diegimai ir bet kurių kitų vykdomų diegimų būsena.</span><span class="sxs-lookup"><span data-stu-id="45a46-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="45a46-146">Jame taip pat yra saitų į El. prekybos svetainę ir El. prekybos svetainių daryklę, kurioje kuriamos svetainės.</span><span class="sxs-lookup"><span data-stu-id="45a46-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="45a46-147">Prieiga prie svetainių daryklės</span><span class="sxs-lookup"><span data-stu-id="45a46-147">Access site builder</span></span>

<span data-ttu-id="45a46-148">Norėdami pasiekti svetainių daryklę, eikite į skirtuką **El. prekyba** LCS puslapyje **„Retail“ valdymas** ir pasirinkite saitą **El. prekybos svetainių valdymo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="45a46-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="45a46-149">Svetainių daryklės nukreipimo puslapyje rodomas nuomotojo lygio rodinys.</span><span class="sxs-lookup"><span data-stu-id="45a46-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="45a46-150">Šiame puslapyje galite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45a46-150">From this page, you can:</span></span>

- <span data-ttu-id="45a46-151">Modifikuoti nuomotojo lygio parametrus.</span><span class="sxs-lookup"><span data-stu-id="45a46-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="45a46-152">Pereiti į bet kurią sukurtą svetainę, kurią turite teisę peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="45a46-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="45a46-153">Naudotis peržiūros funkcijomis, pvz., priežiūra ir ataskaitų pateikimu.</span><span class="sxs-lookup"><span data-stu-id="45a46-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="45a46-154">Sukurkite naują svetainę.</span><span class="sxs-lookup"><span data-stu-id="45a46-154">Create a new site.</span></span> <span data-ttu-id="45a46-155">Daugiau informacijos apie tai, kaip sukurti naują svetainę, žr. [El. prekybos svetainės kūrimas](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="45a46-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="45a46-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="45a46-156">Additional resources</span></span>

[<span data-ttu-id="45a46-157">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="45a46-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="45a46-158">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="45a46-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="45a46-159">Interneto parduotuvės kanalo integravimas</span><span class="sxs-lookup"><span data-stu-id="45a46-159">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="45a46-160">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="45a46-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="45a46-161">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="45a46-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="45a46-162">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="45a46-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="45a46-163">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="45a46-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="45a46-164">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="45a46-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="45a46-165">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="45a46-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="45a46-166">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="45a46-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="45a46-167">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="45a46-167">Enable location-based store detection</span></span>](enable-store-detection.md)
