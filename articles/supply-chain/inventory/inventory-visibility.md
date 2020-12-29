---
title: Inventoriaus matomumo papildinys
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625070"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="5387d-103">Inventoriaus matomumo papildinys</span><span class="sxs-lookup"><span data-stu-id="5387d-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5387d-104">Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mirkopaslaugos, kuriso įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.</span><span class="sxs-lookup"><span data-stu-id="5387d-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="5387d-105">Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą.</span><span class="sxs-lookup"><span data-stu-id="5387d-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="5387d-106">Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="5387d-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="5387d-107">Inventoriaus matomumas yra mikropaslaugos esančios „Common Data Service“, o tai reiškia, kad galite jas plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, kurios atitiktų jūsų verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="5387d-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="5387d-108">Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.</span><span class="sxs-lookup"><span data-stu-id="5387d-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="5387d-109">Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis.</span><span class="sxs-lookup"><span data-stu-id="5387d-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="5387d-110">Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.</span><span class="sxs-lookup"><span data-stu-id="5387d-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="5387d-111">Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).</span><span class="sxs-lookup"><span data-stu-id="5387d-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="5387d-112">Įdiekite Inventoriaus matomumo papildinį</span><span class="sxs-lookup"><span data-stu-id="5387d-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="5387d-113">Jums reikia įdiegtį jį naudjant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="5387d-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5387d-114">LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.</span><span class="sxs-lookup"><span data-stu-id="5387d-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="5387d-115">Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="5387d-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5387d-116">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="5387d-116">Prerequisites</span></span>

<span data-ttu-id="5387d-117">Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="5387d-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="5387d-118">Gaukite LCS implementavimo projektą su mažiausiai viena patalpinta aplinka.</span><span class="sxs-lookup"><span data-stu-id="5387d-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="5387d-119">Sukurkite beta raktus siūlydami LCS.</span><span class="sxs-lookup"><span data-stu-id="5387d-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="5387d-120">Įjunkite beta raktus siūlydami LCS savo vartotojui.</span><span class="sxs-lookup"><span data-stu-id="5387d-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="5387d-121">Susisiekite su „Microsoft Inventory Visibility“ produkto komanda ir pateikite aplinkos ID, kurioje norite talpinti papildinį.</span><span class="sxs-lookup"><span data-stu-id="5387d-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="5387d-122">Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.</span><span class="sxs-lookup"><span data-stu-id="5387d-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="5387d-123">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="5387d-123">Install the add-in</span></span>

<span data-ttu-id="5387d-124">Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="5387d-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="5387d-125">Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.</span><span class="sxs-lookup"><span data-stu-id="5387d-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="5387d-126">Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.</span><span class="sxs-lookup"><span data-stu-id="5387d-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="5387d-127">Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="5387d-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="5387d-128">Aplinkos puslapyje eikite žemyn, kol pamatysite **Aplinkos papildiniai** skyrių.</span><span class="sxs-lookup"><span data-stu-id="5387d-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="5387d-129">Jei skyrisu nematomas, įsitikinkite, kad būtinųjų sąlygų beta raktai yra visiškai sutvarkyti.</span><span class="sxs-lookup"><span data-stu-id="5387d-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="5387d-130">Skyriuje **Aplinkos papildiniai** rinkitės **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="5387d-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="5387d-131">![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")</span><span class="sxs-lookup"><span data-stu-id="5387d-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="5387d-132">Rinkitės **Diegti naują papildinį** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="5387d-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="5387d-133">Esamų atvirų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="5387d-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="5387d-134">Rinkitės **Inventoriaus paslaugos** iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="5387d-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="5387d-135">(Atsiminkite, kad tai gali būti išvardyta kaip **Inventoriaus matomumo papildinys „Dynamics 365 Supply Chain Management“**.)</span><span class="sxs-lookup"><span data-stu-id="5387d-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="5387d-136">Įveskite tolesnes vertes tolesniiuose savo aplinkos laukeliuose:</span><span class="sxs-lookup"><span data-stu-id="5387d-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="5387d-137">**ĮTRAUKITE programos ID**</span><span class="sxs-lookup"><span data-stu-id="5387d-137">**AAD application ID**</span></span>
    - <span data-ttu-id="5387d-138">**ĮTRAUKITE nuomotojo ID**</span><span class="sxs-lookup"><span data-stu-id="5387d-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="5387d-139">![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")</span><span class="sxs-lookup"><span data-stu-id="5387d-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="5387d-140">Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="5387d-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="5387d-141">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="5387d-141">Select **Install**.</span></span> <span data-ttu-id="5387d-142">Papildinio būsena bus rodoma kaip **diegiama**.</span><span class="sxs-lookup"><span data-stu-id="5387d-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="5387d-143">Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.</span><span class="sxs-lookup"><span data-stu-id="5387d-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="5387d-144">Gaukite saugos paslaugų žymą</span><span class="sxs-lookup"><span data-stu-id="5387d-144">Get a security service token</span></span>

<span data-ttu-id="5387d-145">Gaukite saugos paslaugų žymą atlikdami taip:</span><span class="sxs-lookup"><span data-stu-id="5387d-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="5387d-146">Gaukite savo `aadToken` ir skambinkite galutiniam taškui: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="5387d-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="5387d-147">Pakeiskite `client_assertion` tekste su savo `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="5387d-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="5387d-148">Pakeiskite kontekstą tekste su aplinka, kurioje norite talpinti papildinį.</span><span class="sxs-lookup"><span data-stu-id="5387d-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="5387d-149">Pakeiskite teksto tikslą tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="5387d-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="5387d-150">Tikslas MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="5387d-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="5387d-151">(Galite rasti „Azure Active Directory“ programos ID ir nuomotojo ID skirtą MCK `appsettings.mck.json`.)</span><span class="sxs-lookup"><span data-stu-id="5387d-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="5387d-152">Tikslas PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="5387d-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="5387d-153">(Galite rasti „Azure Active Directory“ programos ID ir nuomotojo ID skirtą PROD `appsettings.prod.json`.)</span><span class="sxs-lookup"><span data-stu-id="5387d-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="5387d-154">Rezultatas turi rodyti tolesnį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="5387d-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="5387d-155">Gausite  `access_token` atsakyme.</span><span class="sxs-lookup"><span data-stu-id="5387d-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="5387d-156">Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API.</span><span class="sxs-lookup"><span data-stu-id="5387d-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="5387d-157">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="5387d-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="5387d-158">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="5387d-158">Uninstall the add-in</span></span>

<span data-ttu-id="5387d-159">Norėdami išdiegti papildinį, pasirinkite **Išdiegti**.</span><span class="sxs-lookup"><span data-stu-id="5387d-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="5387d-160">Paleiskite iš naujo LCS ir inventoriaus matomumo papildinys bus panaikintas.</span><span class="sxs-lookup"><span data-stu-id="5387d-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="5387d-161">Išdiegimo procesas pašalins papildinio registraciją ir taip pat pradės darbą siekiant išvalyti visus verslo duomenis laikomus paslaugose.</span><span class="sxs-lookup"><span data-stu-id="5387d-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="5387d-162">Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="5387d-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="5387d-163">Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus.</span><span class="sxs-lookup"><span data-stu-id="5387d-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="5387d-164">Jis palaiko tris pagrindines sąveikos rūšis:</span><span class="sxs-lookup"><span data-stu-id="5387d-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="5387d-165">Publikavimas turimų pakeitimų į papildinio formą išorės sistemoje.</span><span class="sxs-lookup"><span data-stu-id="5387d-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="5387d-166">Laukimo turimi esami kiekiai iš išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="5387d-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="5387d-167">Automatinis sinchronizavimas su „Supply Chain Management“ turimu.</span><span class="sxs-lookup"><span data-stu-id="5387d-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="5387d-168">Automatinis sinchronizavimas nėra viešos API dalis, tačiau vietoje to tvarkomas kontekste aplinkose, kurios įjungia inventoriaus matomumo papildinius.</span><span class="sxs-lookup"><span data-stu-id="5387d-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="5387d-169">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="5387d-169">Authentication</span></span>

<span data-ttu-id="5387d-170">Platformos saugos žyma yra naudojama siekiant paskambinti inventoriaus matomumo papildiniui, todėl turite sukurti „Azure Active Directory“ žymą naudodami savo „Azure Active Directory“ programą.</span><span class="sxs-lookup"><span data-stu-id="5387d-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="5387d-171">Dėl daugiau informacijos apie tai, kaip gauti saugos žymą, žr. [Diegti inventoriaus matomumo papildinį](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="5387d-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="5387d-172">Konfigūruoti Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="5387d-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="5387d-173">Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="5387d-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="5387d-174">Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos.</span><span class="sxs-lookup"><span data-stu-id="5387d-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="5387d-175">Jis iš esmės turi keturias dalis:</span><span class="sxs-lookup"><span data-stu-id="5387d-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="5387d-176">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="5387d-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="5387d-177">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="5387d-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="5387d-178">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="5387d-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="5387d-179">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="5387d-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="5387d-180">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="5387d-180">Partitioning</span></span>

<span data-ttu-id="5387d-181">Dalijimas gali stipriai paveikti matomumo papildinio veikimą.</span><span class="sxs-lookup"><span data-stu-id="5387d-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="5387d-182">Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.</span><span class="sxs-lookup"><span data-stu-id="5387d-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="5387d-183">Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*.</span><span class="sxs-lookup"><span data-stu-id="5387d-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="5387d-184">Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensjia filtruose.</span><span class="sxs-lookup"><span data-stu-id="5387d-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="5387d-185">*Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="5387d-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="5387d-186">„Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="5387d-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="5387d-187">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="5387d-187">Dimension configurations</span></span>

<span data-ttu-id="5387d-188">Inventoriaus matomumas suteikia pagrindinų numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.</span><span class="sxs-lookup"><span data-stu-id="5387d-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="5387d-189">Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.</span><span class="sxs-lookup"><span data-stu-id="5387d-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="5387d-190">Dimensijos tipas</span><span class="sxs-lookup"><span data-stu-id="5387d-190">Dimension type</span></span> | <span data-ttu-id="5387d-191">Dimensijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="5387d-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="5387d-192">Produktas</span><span class="sxs-lookup"><span data-stu-id="5387d-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="5387d-193">Produktas</span><span class="sxs-lookup"><span data-stu-id="5387d-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="5387d-194">Produktas</span><span class="sxs-lookup"><span data-stu-id="5387d-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="5387d-195">Produktas</span><span class="sxs-lookup"><span data-stu-id="5387d-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="5387d-196">Sekimas</span><span class="sxs-lookup"><span data-stu-id="5387d-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="5387d-197">Sekimas</span><span class="sxs-lookup"><span data-stu-id="5387d-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="5387d-198">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="5387d-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="5387d-199">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="5387d-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="5387d-200">Inventoriaus būsena</span><span class="sxs-lookup"><span data-stu-id="5387d-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="5387d-201">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="5387d-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="5387d-202">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="5387d-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="5387d-203">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="5387d-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="5387d-204">Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais.</span><span class="sxs-lookup"><span data-stu-id="5387d-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="5387d-205">Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="5387d-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="5387d-206">Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="5387d-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="5387d-207">Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="5387d-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="5387d-208">Dėl integravimo, inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinš* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="5387d-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="5387d-209">Tikslines nurodymas turi būti vienas iš:</span><span class="sxs-lookup"><span data-stu-id="5387d-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="5387d-210">Numatyti nurodymai Inventoriaus matomumo</span><span class="sxs-lookup"><span data-stu-id="5387d-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="5387d-211">Pasirinktinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="5387d-211">Custom dimensions</span></span>

<span data-ttu-id="5387d-212">Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai nurydmuose ir publikuoti įvykį su nurodymais.</span><span class="sxs-lookup"><span data-stu-id="5387d-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="5387d-213">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="5387d-213">Indexing</span></span>

<span data-ttu-id="5387d-214">Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="5387d-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="5387d-215">Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.</span><span class="sxs-lookup"><span data-stu-id="5387d-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="5387d-216">Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių.</span><span class="sxs-lookup"><span data-stu-id="5387d-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="5387d-217">Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant implementuoti užtikrinant, kad atitiks jis jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="5387d-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="5387d-218">Pavyzdžiui, jei norite laukti produktų tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="5387d-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="5387d-219">Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.</span><span class="sxs-lookup"><span data-stu-id="5387d-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="5387d-220">Kai kada norite tik laukti produkto bendrai.</span><span class="sxs-lookup"><span data-stu-id="5387d-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="5387d-221">Turite du indeksus nustatytus kaip:</span><span class="sxs-lookup"><span data-stu-id="5387d-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="5387d-222">Tuštinkite skliaustelius pagal produkto ID su dalijimu.</span><span class="sxs-lookup"><span data-stu-id="5387d-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="5387d-223">Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="5387d-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="5387d-224">Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`.</span><span class="sxs-lookup"><span data-stu-id="5387d-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="5387d-225">Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.</span><span class="sxs-lookup"><span data-stu-id="5387d-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="5387d-226">Galite padėti savo laukimo kriterijus pagal būtiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="5387d-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="5387d-227">Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.</span><span class="sxs-lookup"><span data-stu-id="5387d-227">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="5387d-228">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="5387d-228">Custom measurement</span></span>

<span data-ttu-id="5387d-229">Numatytasis matavimo kiekiai yra susieti su „Supply Chain Management“, nepaisant to galite norėti turėti kiekį, kuris sudarytas iš numatytųjų priemonių derinių.</span><span class="sxs-lookup"><span data-stu-id="5387d-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="5387d-230">Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimus laukimus.</span><span class="sxs-lookup"><span data-stu-id="5387d-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="5387d-231">Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.</span><span class="sxs-lookup"><span data-stu-id="5387d-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="5387d-232">Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.</span><span class="sxs-lookup"><span data-stu-id="5387d-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="5387d-233">Vartojimo sistema</span><span class="sxs-lookup"><span data-stu-id="5387d-233">Consumption system</span></span> | <span data-ttu-id="5387d-234">Skaičiuotos priemonės</span><span class="sxs-lookup"><span data-stu-id="5387d-234">Calculated measurers</span></span> | <span data-ttu-id="5387d-235">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="5387d-235">Data source</span></span> | <span data-ttu-id="5387d-236">Keitikas</span><span class="sxs-lookup"><span data-stu-id="5387d-236">Modifier</span></span> | <span data-ttu-id="5387d-237">Keitiko apskaičiavimo tipas</span><span class="sxs-lookup"><span data-stu-id="5387d-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="5387d-238">Priedas</span><span class="sxs-lookup"><span data-stu-id="5387d-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="5387d-239">Priedas</span><span class="sxs-lookup"><span data-stu-id="5387d-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="5387d-240">Atimtis</span><span class="sxs-lookup"><span data-stu-id="5387d-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="5387d-241">Priedas</span><span class="sxs-lookup"><span data-stu-id="5387d-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="5387d-242">Atimtis</span><span class="sxs-lookup"><span data-stu-id="5387d-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="5387d-243">Priedas</span><span class="sxs-lookup"><span data-stu-id="5387d-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="5387d-244">Priedas</span><span class="sxs-lookup"><span data-stu-id="5387d-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="5387d-245">Atimtis</span><span class="sxs-lookup"><span data-stu-id="5387d-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="5387d-246">Atimtis</span><span class="sxs-lookup"><span data-stu-id="5387d-246">Subtraction</span></span> |

<span data-ttu-id="5387d-247">Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.</span><span class="sxs-lookup"><span data-stu-id="5387d-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="5387d-248">Išvestis `MyCustomAvailableforReservation` praemta apskaičiavimo nustatymais tinkintuose matavimuose:</span><span class="sxs-lookup"><span data-stu-id="5387d-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="5387d-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="5387d-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="5387d-250">Turimų keitimų publikavimas</span><span class="sxs-lookup"><span data-stu-id="5387d-250">Posting on-hand changes</span></span>

<span data-ttu-id="5387d-251">Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono.</span><span class="sxs-lookup"><span data-stu-id="5387d-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="5387d-252">Jo forma bus:</span><span class="sxs-lookup"><span data-stu-id="5387d-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="5387d-253">Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.</span><span class="sxs-lookup"><span data-stu-id="5387d-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="5387d-254">Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elementos duomenis su juo susietais.</span><span class="sxs-lookup"><span data-stu-id="5387d-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="5387d-255">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="5387d-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="5387d-256">Publikavimo turimų keitimų laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="5387d-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="5387d-257">Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="5387d-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="5387d-258">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="5387d-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="5387d-259">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="5387d-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="5387d-260">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="5387d-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="5387d-261">Publikavimo turimų keitimų laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="5387d-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="5387d-262">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="5387d-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="5387d-263">Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reiškmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="5387d-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="5387d-264">JSON dokumento laukelip ypatybės</span><span class="sxs-lookup"><span data-stu-id="5387d-264">JSON document field properties</span></span>

<span data-ttu-id="5387d-265">Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="5387d-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="5387d-266">Lauko ID</span><span class="sxs-lookup"><span data-stu-id="5387d-266">Field ID</span></span> | <span data-ttu-id="5387d-267">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5387d-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="5387d-268">Unikalus ID konkrečiam keitimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="5387d-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="5387d-269">Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart.</span><span class="sxs-lookup"><span data-stu-id="5387d-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="5387d-270">Organizacijos identifikatorius susietas su įvykiu.</span><span class="sxs-lookup"><span data-stu-id="5387d-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="5387d-271">Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID.</span><span class="sxs-lookup"><span data-stu-id="5387d-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="5387d-272">Aptariamas produkto identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="5387d-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="5387d-273">Kiekis, pagal kurį turimi poreikiai keičiami.</span><span class="sxs-lookup"><span data-stu-id="5387d-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="5387d-274">Jei pavyzdžiui 10 naujų beigelių įtraukti į lentylą, vertė yra 10.</span><span class="sxs-lookup"><span data-stu-id="5387d-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="5387d-275">Jei 3 beigeliai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3.</span><span class="sxs-lookup"><span data-stu-id="5387d-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="5387d-276">Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje.</span><span class="sxs-lookup"><span data-stu-id="5387d-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="5387d-277">Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="5387d-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="5387d-278">Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5387d-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="5387d-279">Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimenseijas savo eilėse.</span><span class="sxs-lookup"><span data-stu-id="5387d-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="5387d-280">Dinaminis rakto maišas/verčių poros.</span><span class="sxs-lookup"><span data-stu-id="5387d-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="5387d-281">Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="5387d-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="5387d-282">Esamas turimas laukimas</span><span class="sxs-lookup"><span data-stu-id="5387d-282">Querying current on-hand</span></span>

<span data-ttu-id="5387d-283">Laukimo galutinis taškas esamame turimame bus panašus URL:</span><span class="sxs-lookup"><span data-stu-id="5387d-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="5387d-284">Jis bus laukiamas su HTTP `POST` metodu.</span><span class="sxs-lookup"><span data-stu-id="5387d-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="5387d-285">Esamas turimas laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="5387d-285">Current on-hand query example 1</span></span>

<span data-ttu-id="5387d-286">Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="5387d-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="5387d-287">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="5387d-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="5387d-288">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="5387d-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="5387d-289">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="5387d-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="5387d-290">Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="5387d-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="5387d-291">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="5387d-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="5387d-292">Esamas turimas laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="5387d-292">Current on-hand query example 2</span></span>

<span data-ttu-id="5387d-293">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="5387d-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="5387d-294">Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reiškmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="5387d-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="5387d-295">Grįžtamojo rezultato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5387d-295">Example return result</span></span>

<span data-ttu-id="5387d-296">Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.</span><span class="sxs-lookup"><span data-stu-id="5387d-296">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="5387d-297">Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.</span><span class="sxs-lookup"><span data-stu-id="5387d-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
