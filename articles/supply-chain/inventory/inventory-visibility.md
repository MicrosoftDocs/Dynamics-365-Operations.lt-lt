---
title: Inventoriaus matomumo papildinys
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114675"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="e8781-103">Inventoriaus matomumo papildinys</span><span class="sxs-lookup"><span data-stu-id="e8781-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="e8781-104">Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mirkopaslaugos, kuriso įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.</span><span class="sxs-lookup"><span data-stu-id="e8781-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="e8781-105">Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą.</span><span class="sxs-lookup"><span data-stu-id="e8781-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="e8781-106">Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="e8781-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="e8781-107">Inventoriaus matomumas yra mikrotarnyba, esanti „Microsoft Dataverse“, o tai reiškia, kad galite ją plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, atitinkančių jūsų verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e8781-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="e8781-108">Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.</span><span class="sxs-lookup"><span data-stu-id="e8781-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="e8781-109">Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis.</span><span class="sxs-lookup"><span data-stu-id="e8781-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="e8781-110">Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.</span><span class="sxs-lookup"><span data-stu-id="e8781-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="e8781-111">Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).</span><span class="sxs-lookup"><span data-stu-id="e8781-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="e8781-112">Įdiekite Inventoriaus matomumo papildinį</span><span class="sxs-lookup"><span data-stu-id="e8781-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="e8781-113">Jums reikia įdiegtį jį naudjant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="e8781-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e8781-114">LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.</span><span class="sxs-lookup"><span data-stu-id="e8781-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="e8781-115">Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="e8781-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e8781-116">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="e8781-116">Prerequisites</span></span>

<span data-ttu-id="e8781-117">Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="e8781-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="e8781-118">Gaukite LCS implementavimo projektą su mažiausiai viena patalpinta aplinka.</span><span class="sxs-lookup"><span data-stu-id="e8781-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="e8781-119">Sukurkite beta raktus siūlydami LCS.</span><span class="sxs-lookup"><span data-stu-id="e8781-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="e8781-120">Įjunkite beta raktus siūlydami LCS savo vartotojui.</span><span class="sxs-lookup"><span data-stu-id="e8781-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="e8781-121">Susisiekite su „Microsoft Inventory Visibility“ produkto komanda ir pateikite aplinkos ID, kurioje norite talpinti papildinį.</span><span class="sxs-lookup"><span data-stu-id="e8781-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="e8781-122">Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.</span><span class="sxs-lookup"><span data-stu-id="e8781-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="e8781-123">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="e8781-123">Install the add-in</span></span>

<span data-ttu-id="e8781-124">Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="e8781-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="e8781-125">Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.</span><span class="sxs-lookup"><span data-stu-id="e8781-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="e8781-126">Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.</span><span class="sxs-lookup"><span data-stu-id="e8781-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="e8781-127">Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="e8781-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="e8781-128">Aplinkos puslapyje eikite žemyn, kol pamatysite **Aplinkos papildiniai** skyrių.</span><span class="sxs-lookup"><span data-stu-id="e8781-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="e8781-129">Jei skyrisu nematomas, įsitikinkite, kad būtinųjų sąlygų beta raktai yra visiškai sutvarkyti.</span><span class="sxs-lookup"><span data-stu-id="e8781-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="e8781-130">Skyriuje **Aplinkos papildiniai** rinkitės **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="e8781-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="e8781-131">![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")</span><span class="sxs-lookup"><span data-stu-id="e8781-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="e8781-132">Rinkitės **Diegti naują papildinį** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="e8781-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="e8781-133">Esamų atvirų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e8781-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="e8781-134">Rinkitės **Inventoriaus paslaugos** iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="e8781-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="e8781-135">(Atsiminkite, kad tai gali būti išvardyta kaip **Inventoriaus matomumo papildinys „Dynamics 365 Supply Chain Management“**.)</span><span class="sxs-lookup"><span data-stu-id="e8781-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="e8781-136">Įveskite tolesnes vertes tolesniiuose savo aplinkos laukeliuose:</span><span class="sxs-lookup"><span data-stu-id="e8781-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="e8781-137">**ĮTRAUKITE programos ID**</span><span class="sxs-lookup"><span data-stu-id="e8781-137">**AAD application ID**</span></span>
    - <span data-ttu-id="e8781-138">**ĮTRAUKITE nuomotojo ID**</span><span class="sxs-lookup"><span data-stu-id="e8781-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="e8781-139">![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")</span><span class="sxs-lookup"><span data-stu-id="e8781-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="e8781-140">Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="e8781-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="e8781-141">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="e8781-141">Select **Install**.</span></span> <span data-ttu-id="e8781-142">Papildinio būsena bus rodoma kaip **diegiama**.</span><span class="sxs-lookup"><span data-stu-id="e8781-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="e8781-143">Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.</span><span class="sxs-lookup"><span data-stu-id="e8781-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="e8781-144">Gaukite saugos paslaugų žymą</span><span class="sxs-lookup"><span data-stu-id="e8781-144">Get a security service token</span></span>

<span data-ttu-id="e8781-145">Gaukite saugos paslaugų žymą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="e8781-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="e8781-146">Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` jūsų „Supply Chain Management” programai.</span><span class="sxs-lookup"><span data-stu-id="e8781-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="e8781-147">Iškvieskite „Azure Active Directory” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="e8781-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e8781-148">**„URL”** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="e8781-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="e8781-149">**Metodas** - `GET`</span><span class="sxs-lookup"><span data-stu-id="e8781-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="e8781-150">**Teksto turinys (formos duomenys)**:</span><span class="sxs-lookup"><span data-stu-id="e8781-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="e8781-151">raktas</span><span class="sxs-lookup"><span data-stu-id="e8781-151">key</span></span> | <span data-ttu-id="e8781-152">vertė</span><span class="sxs-lookup"><span data-stu-id="e8781-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="e8781-153">„client_id”</span><span class="sxs-lookup"><span data-stu-id="e8781-153">client_id</span></span> | <span data-ttu-id="e8781-154">„${aadAppId}“</span><span class="sxs-lookup"><span data-stu-id="e8781-154">${aadAppId}</span></span> |
        | <span data-ttu-id="e8781-155">„client_secret”</span><span class="sxs-lookup"><span data-stu-id="e8781-155">client_secret</span></span> | <span data-ttu-id="e8781-156">„${aadAppSecret}“</span><span class="sxs-lookup"><span data-stu-id="e8781-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="e8781-157">„grant_type”</span><span class="sxs-lookup"><span data-stu-id="e8781-157">grant_type</span></span> | <span data-ttu-id="e8781-158">„client_credentials”</span><span class="sxs-lookup"><span data-stu-id="e8781-158">client_credentials</span></span> |
        | <span data-ttu-id="e8781-159">ištekliai</span><span class="sxs-lookup"><span data-stu-id="e8781-159">resource</span></span> | <span data-ttu-id="e8781-160">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="e8781-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="e8781-161">Turėtumėte gauti `aadToken` kaip atsakymą, panašų į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="e8781-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="e8781-162">Suformuluokite JSON užklausą, panašią į šią:</span><span class="sxs-lookup"><span data-stu-id="e8781-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="e8781-163">Kur:</span><span class="sxs-lookup"><span data-stu-id="e8781-163">Where:</span></span>
    - <span data-ttu-id="e8781-164">Reikšmė `client_assertion` turi būti `aadToken`, kurį gavote ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="e8781-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="e8781-165">Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="e8781-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="e8781-166">Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="e8781-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="e8781-167">Pateikite HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="e8781-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e8781-168">**„URL”** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="e8781-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="e8781-169">**Metodas** - `POST`</span><span class="sxs-lookup"><span data-stu-id="e8781-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="e8781-170">**HTTP antraštė** – įtraukite API versiją (raktas yra `Api-Version` ir reikšmė yra `1.0`)</span><span class="sxs-lookup"><span data-stu-id="e8781-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="e8781-171">**Teksto turinys** – įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="e8781-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="e8781-172">Gausite  `access_token` atsakyme.</span><span class="sxs-lookup"><span data-stu-id="e8781-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="e8781-173">Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API.</span><span class="sxs-lookup"><span data-stu-id="e8781-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="e8781-174">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e8781-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="e8781-175">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="e8781-175">Uninstall the add-in</span></span>

<span data-ttu-id="e8781-176">Norėdami išdiegti papildinį, pasirinkite **Išdiegti**.</span><span class="sxs-lookup"><span data-stu-id="e8781-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="e8781-177">Paleiskite iš naujo LCS ir inventoriaus matomumo papildinys bus panaikintas.</span><span class="sxs-lookup"><span data-stu-id="e8781-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="e8781-178">Išdiegimo procesas pašalins papildinio registraciją ir taip pat pradės darbą siekiant išvalyti visus verslo duomenis laikomus paslaugose.</span><span class="sxs-lookup"><span data-stu-id="e8781-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="e8781-179">Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="e8781-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="e8781-180">Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus.</span><span class="sxs-lookup"><span data-stu-id="e8781-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="e8781-181">Jis palaiko tris pagrindines sąveikos rūšis:</span><span class="sxs-lookup"><span data-stu-id="e8781-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="e8781-182">Publikavimas turimų pakeitimų į papildinio formą išorės sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e8781-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="e8781-183">Laukimo turimi esami kiekiai iš išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="e8781-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="e8781-184">Automatinis sinchronizavimas su „Supply Chain Management“ turimu.</span><span class="sxs-lookup"><span data-stu-id="e8781-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="e8781-185">Automatinis sinchronizavimas nėra viešos API dalis, tačiau vietoje to tvarkomas kontekste aplinkose, kurios įjungia inventoriaus matomumo papildinius.</span><span class="sxs-lookup"><span data-stu-id="e8781-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="e8781-186">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="e8781-186">Authentication</span></span>

<span data-ttu-id="e8781-187">Platformos saugos žyma yra naudojama siekiant paskambinti inventoriaus matomumo papildiniui, todėl turite sukurti „Azure Active Directory“ žymą naudodami savo „Azure Active Directory“ programą.</span><span class="sxs-lookup"><span data-stu-id="e8781-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="e8781-188">Dėl daugiau informacijos apie tai, kaip gauti saugos žymą, žr. [Diegti inventoriaus matomumo papildinį](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="e8781-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="e8781-189">Konfigūruoti Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="e8781-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="e8781-190">Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="e8781-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="e8781-191">Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos.</span><span class="sxs-lookup"><span data-stu-id="e8781-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="e8781-192">Jis iš esmės turi keturias dalis:</span><span class="sxs-lookup"><span data-stu-id="e8781-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="e8781-193">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="e8781-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="e8781-194">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="e8781-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="e8781-195">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="e8781-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="e8781-196">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="e8781-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="e8781-197">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="e8781-197">Partitioning</span></span>

<span data-ttu-id="e8781-198">Dalijimas gali stipriai paveikti matomumo papildinio veikimą.</span><span class="sxs-lookup"><span data-stu-id="e8781-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="e8781-199">Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.</span><span class="sxs-lookup"><span data-stu-id="e8781-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="e8781-200">Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*.</span><span class="sxs-lookup"><span data-stu-id="e8781-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="e8781-201">Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensjia filtruose.</span><span class="sxs-lookup"><span data-stu-id="e8781-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="e8781-202">*Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="e8781-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="e8781-203">„Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="e8781-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="e8781-204">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="e8781-204">Dimension configurations</span></span>

<span data-ttu-id="e8781-205">Inventoriaus matomumas suteikia pagrindinų numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.</span><span class="sxs-lookup"><span data-stu-id="e8781-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="e8781-206">Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.</span><span class="sxs-lookup"><span data-stu-id="e8781-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="e8781-207">Dimensijos tipas</span><span class="sxs-lookup"><span data-stu-id="e8781-207">Dimension type</span></span> | <span data-ttu-id="e8781-208">Dimensijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e8781-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="e8781-209">Produktas</span><span class="sxs-lookup"><span data-stu-id="e8781-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="e8781-210">Produktas</span><span class="sxs-lookup"><span data-stu-id="e8781-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="e8781-211">Produktas</span><span class="sxs-lookup"><span data-stu-id="e8781-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="e8781-212">Produktas</span><span class="sxs-lookup"><span data-stu-id="e8781-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="e8781-213">Sekimas</span><span class="sxs-lookup"><span data-stu-id="e8781-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="e8781-214">Sekimas</span><span class="sxs-lookup"><span data-stu-id="e8781-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="e8781-215">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="e8781-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="e8781-216">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="e8781-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="e8781-217">Inventoriaus būsena</span><span class="sxs-lookup"><span data-stu-id="e8781-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="e8781-218">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="e8781-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="e8781-219">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="e8781-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="e8781-220">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="e8781-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="e8781-221">Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais.</span><span class="sxs-lookup"><span data-stu-id="e8781-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="e8781-222">Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="e8781-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="e8781-223">Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="e8781-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="e8781-224">Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="e8781-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="e8781-225">Dėl integravimo, inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinš* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="e8781-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="e8781-226">Tikslines nurodymas turi būti vienas iš:</span><span class="sxs-lookup"><span data-stu-id="e8781-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="e8781-227">Numatyti nurodymai Inventoriaus matomumo</span><span class="sxs-lookup"><span data-stu-id="e8781-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="e8781-228">Pasirinktinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="e8781-228">Custom dimensions</span></span>

<span data-ttu-id="e8781-229">Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai nurydmuose ir publikuoti įvykį su nurodymais.</span><span class="sxs-lookup"><span data-stu-id="e8781-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="e8781-230">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="e8781-230">Indexing</span></span>

<span data-ttu-id="e8781-231">Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="e8781-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="e8781-232">Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.</span><span class="sxs-lookup"><span data-stu-id="e8781-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="e8781-233">Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių.</span><span class="sxs-lookup"><span data-stu-id="e8781-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="e8781-234">Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant implementuoti užtikrinant, kad atitiks jis jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="e8781-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="e8781-235">Pavyzdžiui, jei norite laukti produktų tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="e8781-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="e8781-236">Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.</span><span class="sxs-lookup"><span data-stu-id="e8781-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="e8781-237">Kai kada norite tik laukti produkto bendrai.</span><span class="sxs-lookup"><span data-stu-id="e8781-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="e8781-238">Turite du indeksus nustatytus kaip:</span><span class="sxs-lookup"><span data-stu-id="e8781-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="e8781-239">Tuštinkite skliaustelius pagal produkto ID su dalijimu.</span><span class="sxs-lookup"><span data-stu-id="e8781-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="e8781-240">Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="e8781-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="e8781-241">Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`.</span><span class="sxs-lookup"><span data-stu-id="e8781-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="e8781-242">Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e8781-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="e8781-243">Galite padėti savo laukimo kriterijus pagal būtiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="e8781-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="e8781-244">Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.</span><span class="sxs-lookup"><span data-stu-id="e8781-244">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="e8781-245">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="e8781-245">Custom measurement</span></span>

<span data-ttu-id="e8781-246">Numatytasis matavimo kiekiai yra susieti su „Supply Chain Management“, nepaisant to galite norėti turėti kiekį, kuris sudarytas iš numatytųjų priemonių derinių.</span><span class="sxs-lookup"><span data-stu-id="e8781-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="e8781-247">Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimus laukimus.</span><span class="sxs-lookup"><span data-stu-id="e8781-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="e8781-248">Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.</span><span class="sxs-lookup"><span data-stu-id="e8781-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="e8781-249">Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.</span><span class="sxs-lookup"><span data-stu-id="e8781-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="e8781-250">Vartojimo sistema</span><span class="sxs-lookup"><span data-stu-id="e8781-250">Consumption system</span></span> | <span data-ttu-id="e8781-251">Skaičiuotos priemonės</span><span class="sxs-lookup"><span data-stu-id="e8781-251">Calculated measurers</span></span> | <span data-ttu-id="e8781-252">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="e8781-252">Data source</span></span> | <span data-ttu-id="e8781-253">Keitikas</span><span class="sxs-lookup"><span data-stu-id="e8781-253">Modifier</span></span> | <span data-ttu-id="e8781-254">Keitiko apskaičiavimo tipas</span><span class="sxs-lookup"><span data-stu-id="e8781-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="e8781-255">Priedas</span><span class="sxs-lookup"><span data-stu-id="e8781-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="e8781-256">Priedas</span><span class="sxs-lookup"><span data-stu-id="e8781-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="e8781-257">Atimtis</span><span class="sxs-lookup"><span data-stu-id="e8781-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="e8781-258">Priedas</span><span class="sxs-lookup"><span data-stu-id="e8781-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="e8781-259">Atimtis</span><span class="sxs-lookup"><span data-stu-id="e8781-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="e8781-260">Priedas</span><span class="sxs-lookup"><span data-stu-id="e8781-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="e8781-261">Priedas</span><span class="sxs-lookup"><span data-stu-id="e8781-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="e8781-262">Atimtis</span><span class="sxs-lookup"><span data-stu-id="e8781-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="e8781-263">Atimtis</span><span class="sxs-lookup"><span data-stu-id="e8781-263">Subtraction</span></span> |

<span data-ttu-id="e8781-264">Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.</span><span class="sxs-lookup"><span data-stu-id="e8781-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="e8781-265">Išvestis `MyCustomAvailableforReservation` praemta apskaičiavimo nustatymais tinkintuose matavimuose:</span><span class="sxs-lookup"><span data-stu-id="e8781-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="e8781-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="e8781-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="e8781-267">Turimų keitimų publikavimas</span><span class="sxs-lookup"><span data-stu-id="e8781-267">Posting on-hand changes</span></span>

<span data-ttu-id="e8781-268">Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono.</span><span class="sxs-lookup"><span data-stu-id="e8781-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="e8781-269">Jo forma bus:</span><span class="sxs-lookup"><span data-stu-id="e8781-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="e8781-270">Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.</span><span class="sxs-lookup"><span data-stu-id="e8781-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="e8781-271">Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elementos duomenis su juo susietais.</span><span class="sxs-lookup"><span data-stu-id="e8781-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="e8781-272">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="e8781-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="e8781-273">Publikavimo turimų keitimų laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="e8781-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="e8781-274">Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="e8781-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e8781-275">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="e8781-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e8781-276">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="e8781-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e8781-277">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="e8781-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="e8781-278">Publikavimo turimų keitimų laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="e8781-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="e8781-279">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="e8781-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e8781-280">Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reiškmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="e8781-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="e8781-281">JSON dokumento laukelip ypatybės</span><span class="sxs-lookup"><span data-stu-id="e8781-281">JSON document field properties</span></span>

<span data-ttu-id="e8781-282">Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="e8781-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="e8781-283">Lauko ID</span><span class="sxs-lookup"><span data-stu-id="e8781-283">Field ID</span></span> | <span data-ttu-id="e8781-284">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e8781-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="e8781-285">Unikalus ID konkrečiam keitimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="e8781-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="e8781-286">Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart.</span><span class="sxs-lookup"><span data-stu-id="e8781-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="e8781-287">Organizacijos identifikatorius susietas su įvykiu.</span><span class="sxs-lookup"><span data-stu-id="e8781-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="e8781-288">Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID.</span><span class="sxs-lookup"><span data-stu-id="e8781-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="e8781-289">Aptariamas produkto identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="e8781-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="e8781-290">Kiekis, pagal kurį turimi poreikiai keičiami.</span><span class="sxs-lookup"><span data-stu-id="e8781-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="e8781-291">Jei pavyzdžiui 10 naujų beigelių įtraukti į lentylą, vertė yra 10.</span><span class="sxs-lookup"><span data-stu-id="e8781-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="e8781-292">Jei 3 beigeliai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3.</span><span class="sxs-lookup"><span data-stu-id="e8781-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="e8781-293">Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje.</span><span class="sxs-lookup"><span data-stu-id="e8781-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="e8781-294">Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="e8781-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="e8781-295">Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e8781-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="e8781-296">Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimenseijas savo eilėse.</span><span class="sxs-lookup"><span data-stu-id="e8781-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="e8781-297">Dinaminis rakto maišas/verčių poros.</span><span class="sxs-lookup"><span data-stu-id="e8781-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="e8781-298">Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="e8781-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="e8781-299">Esamas turimas laukimas</span><span class="sxs-lookup"><span data-stu-id="e8781-299">Querying current on-hand</span></span>

<span data-ttu-id="e8781-300">Laukimo galutinis taškas esamame turimame bus panašus URL:</span><span class="sxs-lookup"><span data-stu-id="e8781-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="e8781-301">Jis bus laukiamas su HTTP `POST` metodu.</span><span class="sxs-lookup"><span data-stu-id="e8781-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="e8781-302">Esamas turimas laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="e8781-302">Current on-hand query example 1</span></span>

<span data-ttu-id="e8781-303">Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="e8781-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e8781-304">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="e8781-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e8781-305">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="e8781-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e8781-306">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="e8781-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="e8781-307">Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="e8781-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="e8781-308">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="e8781-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="e8781-309">Esamas turimas laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="e8781-309">Current on-hand query example 2</span></span>

<span data-ttu-id="e8781-310">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="e8781-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e8781-311">Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reiškmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="e8781-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="e8781-312">Grįžtamojo rezultato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e8781-312">Example return result</span></span>

<span data-ttu-id="e8781-313">Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.</span><span class="sxs-lookup"><span data-stu-id="e8781-313">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="e8781-314">Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.</span><span class="sxs-lookup"><span data-stu-id="e8781-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
