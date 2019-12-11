---
title: Naujo el. prekybos nuomotojo diegimas
description: Šioje temoje aprašoma, kaip įdiegti naują el. prekybos nuomininką naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697456"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="9731f-103">Naujo el. prekybos nuomotojo diegimas</span><span class="sxs-lookup"><span data-stu-id="9731f-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9731f-104">Šioje temoje aprašoma, kaip įdiegti naują el. prekybos svetainę naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="9731f-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="9731f-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9731f-105">Overview</span></span>
    
<span data-ttu-id="9731f-106">„Microsoft Dynamics“ „Lifecycle Services“ (LCS) yra debesiu pagrįsta bendradarbiavimo darbo sritis, kurią partneriai ir klientai gali naudoti savo projektams ir aplinkoms tvarkyti, peržiūrėti naujausią informaciją apie „Microsoft Dynamics“ produktus ir funkcijas bei kurti, sekti ir naršyti palaikymo incidentus.</span><span class="sxs-lookup"><span data-stu-id="9731f-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="9731f-107">El. prekybos valdymo funkcijos integruotos į LCS.</span><span class="sxs-lookup"><span data-stu-id="9731f-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="9731f-108">Norėdami sužinoti daugiau apie LCS, žr. [„Lifecycle Services“ vartotojo vadovą](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="9731f-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="9731f-109">Darbo pradžia</span><span class="sxs-lookup"><span data-stu-id="9731f-109">Get started</span></span>

<span data-ttu-id="9731f-110">Kad galėtumėte paleisti el. prekybą, turite paleisti projektą, aplinką ir „Retail Cloud Scale Unit“ (RCSU).</span><span class="sxs-lookup"><span data-stu-id="9731f-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="9731f-111">Norėdami atlikti LCS inicijavimą, turite turėti teises, skirtas projekto savininko arba aplinkos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="9731f-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="9731f-112">Palaikomos gamybos ir smėlio dėžės aplinkos topologijos.</span><span class="sxs-lookup"><span data-stu-id="9731f-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="9731f-113">Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="9731f-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="9731f-114">Daugiau informacijos apie RCSU, žr. [„Retail Cloud Scale Unit“ inicijavimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9731f-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="9731f-115">El. prekybos inicijavimas</span><span class="sxs-lookup"><span data-stu-id="9731f-115">Initialize e-Commerce</span></span>

<span data-ttu-id="9731f-116">Naudokite šią procedūrą paleisti el. prekybos funkciją esamoje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="9731f-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="9731f-117">Prieš pradėdami įsitikinkite, kad turite tokią reikalingą informaciją:</span><span class="sxs-lookup"><span data-stu-id="9731f-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="9731f-118">RSCU, kuris bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="9731f-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="9731f-119">„Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama el. prekybos sistemos administratoriams.</span><span class="sxs-lookup"><span data-stu-id="9731f-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="9731f-120">„Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama įvertinimų ir apžvalgų moderatoriams.</span><span class="sxs-lookup"><span data-stu-id="9731f-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="9731f-121">Domenai, kurie bus susieti su aplinka.</span><span class="sxs-lookup"><span data-stu-id="9731f-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="9731f-122">Be to, galite rinkti tokią pasirinktinę informaciją:</span><span class="sxs-lookup"><span data-stu-id="9731f-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="9731f-123">„Azure AD“ verslo ir vartotojų (B2C) informaciją:</span><span class="sxs-lookup"><span data-stu-id="9731f-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="9731f-124">Nuomotojo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="9731f-124">Tenant Name.</span></span>
    - <span data-ttu-id="9731f-125">Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="9731f-125">Client ID.</span></span>
    - <span data-ttu-id="9731f-126">Prisijungimo pasirinktinis domenas.</span><span class="sxs-lookup"><span data-stu-id="9731f-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="9731f-127">Atsakymo URL.</span><span class="sxs-lookup"><span data-stu-id="9731f-127">Reply URL.</span></span>
    - <span data-ttu-id="9731f-128">Registracijos prisijungimo strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="9731f-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="9731f-129">Slaptažodžio nustatymo iš naujo strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="9731f-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="9731f-130">Redagagavimo profilio strategijos ID.</span><span class="sxs-lookup"><span data-stu-id="9731f-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="9731f-131">Šią informaciją galima įtraukti vėliau, naudojant paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="9731f-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="9731f-132">Surinkę reikiamą informaciją, atlikite šiuos veiksmus, norėdami paleisti el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="9731f-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="9731f-133">Prisijunkite prie [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9731f-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="9731f-134">Atidarykite projektą, kuriame yra aplinka, kurioje norima paleisti el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="9731f-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="9731f-135">Skyriuje **Aplinkos** pasirinkite aplinką.</span><span class="sxs-lookup"><span data-stu-id="9731f-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="9731f-136">Dalyje **Aplinkos funkcijos** pasirinkite saitą **„Retail“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="9731f-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="9731f-137">Skirtuke **El. prekyba** pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="9731f-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="9731f-138">Atsiranda dialogo langas, kuriame reikia įvesti informaciją, reikalingą kuriant.</span><span class="sxs-lookup"><span data-stu-id="9731f-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="9731f-139">Įveskite reikiamą informaciją ir pereikite prie tolesnio puslapio.</span><span class="sxs-lookup"><span data-stu-id="9731f-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="9731f-140">Kitame puslapyje įveskite reikiamą informaciją ir pateikite formą.</span><span class="sxs-lookup"><span data-stu-id="9731f-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="9731f-141">Jūs grąžinami į skirtuką **El. prekyba**, kur turėtumėte matyti, kad inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="9731f-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="9731f-142">Norėdami peržiūrėti inicijavimo būseną, **atnaujinkite** arba grįžkite į skirtuką **El. prekyba**.</span><span class="sxs-lookup"><span data-stu-id="9731f-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="9731f-143">Paleidus el. prekybą iš LCS, sistema sukuria keletą komponentų, kurie būtini el. prekybai ir susieja juos su aplinka.</span><span class="sxs-lookup"><span data-stu-id="9731f-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="9731f-144">Baigus parengimą, skirtukas **El. prekyba** puslapyje **„Retail“ valdymas** atnaujinamas, kad atsispindėtų parengimą.</span><span class="sxs-lookup"><span data-stu-id="9731f-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="9731f-145">Puslapyje pateikiami naujausi tinkinimo diegimai ir bet kurių kitų vykdomų diegimų būsena.</span><span class="sxs-lookup"><span data-stu-id="9731f-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="9731f-146">Jame taip pat yra saitų į el. prekybos svetainę ir el. prekybos svetainių valdymo įrankį (kūrimo įrankį).</span><span class="sxs-lookup"><span data-stu-id="9731f-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="9731f-147">Prieiga prie kūrimo aplinkos</span><span class="sxs-lookup"><span data-stu-id="9731f-147">Access the authoring environment</span></span>

<span data-ttu-id="9731f-148">Norėdami pasiekti kūrimo aplinką, eikite į skirtuką **El. prekyba** puslapyje **„Retail“ valdymas**.</span><span class="sxs-lookup"><span data-stu-id="9731f-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="9731f-149">Ten rasite saitus į savo el. prekybos svetainę ir svetainės valdymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="9731f-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9731f-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9731f-150">Additional resources</span></span>

[<span data-ttu-id="9731f-151">Interneto parduotuvės peržiūra</span><span class="sxs-lookup"><span data-stu-id="9731f-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="9731f-152">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="9731f-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9731f-153">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="9731f-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9731f-154">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9731f-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9731f-155">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="9731f-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9731f-156">Įgalinti parduotuvės nustatymą pagal vietą</span><span class="sxs-lookup"><span data-stu-id="9731f-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="9731f-157">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="9731f-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
