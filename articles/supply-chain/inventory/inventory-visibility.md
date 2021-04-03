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
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574227"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="9a09c-103">Inventoriaus matomumo papildinys</span><span class="sxs-lookup"><span data-stu-id="9a09c-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="9a09c-104">Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mirkopaslaugos, kuriso įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="9a09c-105">Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="9a09c-106">Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="9a09c-107">Inventoriaus matomumas yra mikrotarnyba, esanti „Microsoft Dataverse“, o tai reiškia, kad galite ją plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, atitinkančių jūsų verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9a09c-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="9a09c-108">Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.</span><span class="sxs-lookup"><span data-stu-id="9a09c-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="9a09c-109">Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis.</span><span class="sxs-lookup"><span data-stu-id="9a09c-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="9a09c-110">Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.</span><span class="sxs-lookup"><span data-stu-id="9a09c-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="9a09c-111">Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).</span><span class="sxs-lookup"><span data-stu-id="9a09c-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="9a09c-112">Įdiekite Inventoriaus matomumo papildinį</span><span class="sxs-lookup"><span data-stu-id="9a09c-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="9a09c-113">Jums reikia įdiegtį jį naudjant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="9a09c-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9a09c-114">LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="9a09c-115">Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="9a09c-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9a09c-116">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="9a09c-116">Prerequisites</span></span>

<span data-ttu-id="9a09c-117">Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="9a09c-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="9a09c-118">Gaukite LCS implementavimo projektą su mažiausiai viena patalpinta aplinka.</span><span class="sxs-lookup"><span data-stu-id="9a09c-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="9a09c-119">Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) buvo patenkintos.</span><span class="sxs-lookup"><span data-stu-id="9a09c-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="9a09c-120">Atsargų matomumui nereikia dvigubo rašymo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="9a09c-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="9a09c-121">Kreipkitės į atsargų matomumo komandą el. paštu [inventvisibilitysupp@microsoft.com ](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte šiuos tris reikalingus failus:</span><span class="sxs-lookup"><span data-stu-id="9a09c-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="9a09c-122">`Inventory Visibility Integration.zip` (jei jūsų vykdoma „Supply Chain Management” versija yra ankstesnė nei 10.0.18 versija)</span><span class="sxs-lookup"><span data-stu-id="9a09c-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="9a09c-123">Šiuo metu palaikomos šalys ir regionai yra Kanada, Jungtinės Valstijos ir Europos Sąjunga (ES).</span><span class="sxs-lookup"><span data-stu-id="9a09c-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="9a09c-124">Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.</span><span class="sxs-lookup"><span data-stu-id="9a09c-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="9a09c-125">„Dataverse“ nustatymas</span><span class="sxs-lookup"><span data-stu-id="9a09c-125">Set up Dataverse</span></span>

<span data-ttu-id="9a09c-126">Atlikite šiuos veiksmus, kad nustatytumėte „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="9a09c-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="9a09c-127">Prie savo nuomininko pridėkite aptarnavimo principą:</span><span class="sxs-lookup"><span data-stu-id="9a09c-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="9a09c-128">Įdiekite „Azure AD“ „PowerShell“ v2 modulį, kaip aprašyta skyriuje [„Azure Active Directory“ „PowerShell for Graph“ diegimas](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="9a09c-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="9a09c-129">Paleiskite šią „PowerShell“ komandą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="9a09c-130">Sukurkite programos naudotoją „Dataverse“ atsargų matomumui:</span><span class="sxs-lookup"><span data-stu-id="9a09c-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="9a09c-131">Atidarykite savo „Dataverse“ aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="9a09c-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="9a09c-132">Eikite į **Išplėstiniai nustatymai \> Sistema \> Sauga \> Naudotojai** ir sukurkite programos naudotoją.</span><span class="sxs-lookup"><span data-stu-id="9a09c-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="9a09c-133">Naudokite peržiūros meniu, kad puslapio rodinį pakeistumėte į **Programos naudotojai**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="9a09c-134">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-134">Select **New**.</span></span> <span data-ttu-id="9a09c-135">Programos ID nustatykite kaip *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="9a09c-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="9a09c-136">(Išsaugant keitimus objekto ID įkeliamas automatiškai.) Pavadinimą galima pritaikyti.</span><span class="sxs-lookup"><span data-stu-id="9a09c-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="9a09c-137">Pavyzdžiui, jį galima pakeisti į *Atsargų matomumas*.</span><span class="sxs-lookup"><span data-stu-id="9a09c-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="9a09c-138">Jums pabaigus, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="9a09c-139">Pasirinkite **Priskirti vaidmenį**, tada pasirinkite **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="9a09c-140">Jei yra vaidmuo pavadinimu **„Common Data Service“ naudotojas**, pasirinkite ir jį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="9a09c-141">Daugiau informacijos žr. skyriuje [Programos naudotojo kūrimas](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="9a09c-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="9a09c-142">Importuokite failą `Inventory Visibility Dataverse Solution.zip`, kuriame yra su „Dataverse“ konfigūracija susiję objektai ir „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="9a09c-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="9a09c-143">Eikite į puslapį **Sprendimai**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="9a09c-144">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-144">Select **Import**.</span></span>

1. <span data-ttu-id="9a09c-145">Importuokite konfigūracijos atnaujinimo paleidiklio eigą:</span><span class="sxs-lookup"><span data-stu-id="9a09c-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="9a09c-146">Eikite į puslapį „Microsoft Flow“.</span><span class="sxs-lookup"><span data-stu-id="9a09c-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="9a09c-147">Patikrinkite, ar yra ryšys, pavadintas „*Dataverse“ (senesnis)*.</span><span class="sxs-lookup"><span data-stu-id="9a09c-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="9a09c-148">(Jei ne, sukurkite jį.)</span><span class="sxs-lookup"><span data-stu-id="9a09c-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="9a09c-149">Importuokite failą `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="9a09c-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="9a09c-150">Jį importavus srityje **Mano srautai** bus rodomas paleidiklis.</span><span class="sxs-lookup"><span data-stu-id="9a09c-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="9a09c-151">Inicijuokite šiuos keturis kintamuosius, atsižvelgdami į aplinkos informaciją:</span><span class="sxs-lookup"><span data-stu-id="9a09c-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="9a09c-152">„Azure“ nuomininko ID</span><span class="sxs-lookup"><span data-stu-id="9a09c-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="9a09c-153">„Azure“ programos kliento ID</span><span class="sxs-lookup"><span data-stu-id="9a09c-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="9a09c-154">„Azure“ programos kliento raktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="9a09c-155">Atsargų matomumo galinis punktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="9a09c-156">Daugiau informacijos apie šį kintamąjį žr. toliau šioje temoje pateikiamame skyriuje [Atsargų matomumo integravimo nustatymas](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="9a09c-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="9a09c-157">![Konfigūracijos paleidiklis](media/configuration-trigger.png "Konfigūracijos paleidiklis")</span><span class="sxs-lookup"><span data-stu-id="9a09c-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="9a09c-158">Pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="9a09c-159">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-159">Install the add-in</span></span>

<span data-ttu-id="9a09c-160">Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="9a09c-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="9a09c-161">Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.</span><span class="sxs-lookup"><span data-stu-id="9a09c-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="9a09c-162">Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.</span><span class="sxs-lookup"><span data-stu-id="9a09c-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="9a09c-163">Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="9a09c-164">Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai**, skyriuje **„Power Platform“ integravimas**, kuriame rasite „Dataverse“ aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="9a09c-165">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="9a09c-166">![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")</span><span class="sxs-lookup"><span data-stu-id="9a09c-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="9a09c-167">Rinkitės **Diegti naują papildinį** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="9a09c-168">Esamų atvirų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9a09c-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="9a09c-169">Sąraše pasirinkite **Atsargų matomumas**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="9a09c-170">Įveskite tolesnes vertes tolesniiuose savo aplinkos laukeliuose:</span><span class="sxs-lookup"><span data-stu-id="9a09c-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="9a09c-171">**AAD programos (kliento) ID**</span><span class="sxs-lookup"><span data-stu-id="9a09c-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="9a09c-172">**ĮTRAUKITE nuomotojo ID**</span><span class="sxs-lookup"><span data-stu-id="9a09c-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="9a09c-173">![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")</span><span class="sxs-lookup"><span data-stu-id="9a09c-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="9a09c-174">Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="9a09c-175">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-175">Select **Install**.</span></span> <span data-ttu-id="9a09c-176">Papildinio būsena bus rodoma kaip **diegiama**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="9a09c-177">Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="9a09c-178">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-178">Uninstall the add-in</span></span>

<span data-ttu-id="9a09c-179">Norėdami išdiegti papildinį, pasirinkite **Išdiegti**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="9a09c-180">Atnaujinus LCS inventoriaus matomumo papildinys bus panaikintas.</span><span class="sxs-lookup"><span data-stu-id="9a09c-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="9a09c-181">Atlikus išdiegimo procesą pašalinama papildinio registracija ir pradedamas darbas siekiant išvalyti visus verslo duomenis laikomus paslaugose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="9a09c-182">Turimų atsargų duomenų iš „Supply Chain Management” naudojimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="9a09c-183">Aplinkos matomumo integravimo paketo diegimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="9a09c-184">Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="9a09c-185">Tada įdiekite paketą LCS.</span><span class="sxs-lookup"><span data-stu-id="9a09c-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="9a09c-186">Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="9a09c-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="9a09c-187">Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="9a09c-188">Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją.</span><span class="sxs-lookup"><span data-stu-id="9a09c-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="9a09c-189">Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.</span><span class="sxs-lookup"><span data-stu-id="9a09c-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="9a09c-190">Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="9a09c-191">(Numatyta, kad jos yra įjungtos.)</span><span class="sxs-lookup"><span data-stu-id="9a09c-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="9a09c-192">Funkcijos aprašymas</span><span class="sxs-lookup"><span data-stu-id="9a09c-192">Feature description</span></span> | <span data-ttu-id="9a09c-193">Kodo versija</span><span class="sxs-lookup"><span data-stu-id="9a09c-193">Code version</span></span> | <span data-ttu-id="9a09c-194">Klasės kaitaliojimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="9a09c-195">Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="9a09c-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="9a09c-196">10.0.11</span></span> | <span data-ttu-id="9a09c-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="9a09c-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="9a09c-198">Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="9a09c-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="9a09c-199">10.0.12</span></span> | <span data-ttu-id="9a09c-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="9a09c-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="9a09c-201">Atsargų matomumo integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="9a09c-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="9a09c-202">„Supply Chain Management” atidarykite darbo sritį **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ir įjunkite funkciją **Atsargų matomumo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="9a09c-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="9a09c-203">Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų matomumo integravimo parametrai** ir įveskite aplinkos, kurioje paleidžiamas atsargų matomumas, URL.</span><span class="sxs-lookup"><span data-stu-id="9a09c-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="9a09c-204">Raskite savo LCS aplinkos „Azure“ regioną, o tada įveskite URL.</span><span class="sxs-lookup"><span data-stu-id="9a09c-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="9a09c-205">URL forma yra tokia:</span><span class="sxs-lookup"><span data-stu-id="9a09c-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="9a09c-206">Pavyzdžiui, jei esate Europoje, jūsų aplinkos URL bus vienas iš šių:</span><span class="sxs-lookup"><span data-stu-id="9a09c-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="9a09c-207">Šiuo metu naudojami nurodyti regionai.</span><span class="sxs-lookup"><span data-stu-id="9a09c-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="9a09c-208">„Azure“ regionas</span><span class="sxs-lookup"><span data-stu-id="9a09c-208">Azure region</span></span> | <span data-ttu-id="9a09c-209">Trumpas regiono pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="9a09c-210">Rytų Australija</span><span class="sxs-lookup"><span data-stu-id="9a09c-210">Australia east</span></span> | <span data-ttu-id="9a09c-211">eau</span><span class="sxs-lookup"><span data-stu-id="9a09c-211">eau</span></span> |
    | <span data-ttu-id="9a09c-212">Pietryčių Australija</span><span class="sxs-lookup"><span data-stu-id="9a09c-212">Australia southeast</span></span> | <span data-ttu-id="9a09c-213">seau</span><span class="sxs-lookup"><span data-stu-id="9a09c-213">seau</span></span> |
    | <span data-ttu-id="9a09c-214">Centrinė Kanada</span><span class="sxs-lookup"><span data-stu-id="9a09c-214">Canada central</span></span> | <span data-ttu-id="9a09c-215">cca</span><span class="sxs-lookup"><span data-stu-id="9a09c-215">cca</span></span> |
    | <span data-ttu-id="9a09c-216">Rytų Kanada</span><span class="sxs-lookup"><span data-stu-id="9a09c-216">Canada east</span></span> | <span data-ttu-id="9a09c-217">eca</span><span class="sxs-lookup"><span data-stu-id="9a09c-217">eca</span></span> |
    | <span data-ttu-id="9a09c-218">Šiaurės Europa</span><span class="sxs-lookup"><span data-stu-id="9a09c-218">North Europe</span></span> | <span data-ttu-id="9a09c-219">neu</span><span class="sxs-lookup"><span data-stu-id="9a09c-219">neu</span></span> |
    | <span data-ttu-id="9a09c-220">Vakarų Europa</span><span class="sxs-lookup"><span data-stu-id="9a09c-220">West Europe</span></span> | <span data-ttu-id="9a09c-221">weu</span><span class="sxs-lookup"><span data-stu-id="9a09c-221">weu</span></span> |
    | <span data-ttu-id="9a09c-222">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="9a09c-222">East US</span></span> | <span data-ttu-id="9a09c-223">eus</span><span class="sxs-lookup"><span data-stu-id="9a09c-223">eus</span></span> |
    | <span data-ttu-id="9a09c-224">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="9a09c-224">West US</span></span> | <span data-ttu-id="9a09c-225">wus</span><span class="sxs-lookup"><span data-stu-id="9a09c-225">wus</span></span> |

1. <span data-ttu-id="9a09c-226">Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="9a09c-227">Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="9a09c-228">Vieša inventoriaus matomumo API</span><span class="sxs-lookup"><span data-stu-id="9a09c-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="9a09c-229">Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus.</span><span class="sxs-lookup"><span data-stu-id="9a09c-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="9a09c-230">Jis palaiko tris pagrindines sąveikos rūšis:</span><span class="sxs-lookup"><span data-stu-id="9a09c-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="9a09c-231">Turimų atsargų pakeitimų į papildinio formą išorės sistemoje registravimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="9a09c-232">Dabartinių turimų kiekių užklausos iš išorės sistemos</span><span class="sxs-lookup"><span data-stu-id="9a09c-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="9a09c-233">Automatinis sinchronizavimas su turimomis „Supply Chain Management“ atsargomis.</span><span class="sxs-lookup"><span data-stu-id="9a09c-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="9a09c-234">Automatinis sinchronizavimas nėra viešosios API dalis.</span><span class="sxs-lookup"><span data-stu-id="9a09c-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="9a09c-235">Vietoje to jis tvarkomas fone, aplinkoms, kuriose įjungtas atsargų matomumo priedas.</span><span class="sxs-lookup"><span data-stu-id="9a09c-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="9a09c-236">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-236">Authentication</span></span>

<span data-ttu-id="9a09c-237">Platformos saugos atpažinimo ženklas naudojamas atsargų matomumo priedui iškviesti.</span><span class="sxs-lookup"><span data-stu-id="9a09c-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="9a09c-238">Todėl turite sugeneruoti *„Azure Active Directory“ („Azure AD“) atpažinimo ženklą*, naudodami savo „Azure AD“ programą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="9a09c-239">Tada turite naudoti „Azure AD“ atpažinimo ženklą, kad iš saugos tarnybos gautumėte *prieigos atpažinimo ženklą*.</span><span class="sxs-lookup"><span data-stu-id="9a09c-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="9a09c-240">Gaukite saugos paslaugų žymą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="9a09c-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="9a09c-241">Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` jūsų „Supply Chain Management” programai.</span><span class="sxs-lookup"><span data-stu-id="9a09c-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="9a09c-242">Iškvieskite „Azure Active Directory” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="9a09c-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="9a09c-243">**„URL”** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="9a09c-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="9a09c-244">**Metodas** - `GET`</span><span class="sxs-lookup"><span data-stu-id="9a09c-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="9a09c-245">**Teksto turinys (formos duomenys)**:</span><span class="sxs-lookup"><span data-stu-id="9a09c-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="9a09c-246">raktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-246">key</span></span> | <span data-ttu-id="9a09c-247">vertė</span><span class="sxs-lookup"><span data-stu-id="9a09c-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="9a09c-248">„client_id”</span><span class="sxs-lookup"><span data-stu-id="9a09c-248">client_id</span></span> | <span data-ttu-id="9a09c-249">„${aadAppId}“</span><span class="sxs-lookup"><span data-stu-id="9a09c-249">${aadAppId}</span></span> |
        | <span data-ttu-id="9a09c-250">„client_secret”</span><span class="sxs-lookup"><span data-stu-id="9a09c-250">client_secret</span></span> | <span data-ttu-id="9a09c-251">„${aadAppSecret}“</span><span class="sxs-lookup"><span data-stu-id="9a09c-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="9a09c-252">„grant_type”</span><span class="sxs-lookup"><span data-stu-id="9a09c-252">grant_type</span></span> | <span data-ttu-id="9a09c-253">„client_credentials”</span><span class="sxs-lookup"><span data-stu-id="9a09c-253">client_credentials</span></span> |
        | <span data-ttu-id="9a09c-254">ištekliai</span><span class="sxs-lookup"><span data-stu-id="9a09c-254">resource</span></span> | <span data-ttu-id="9a09c-255">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="9a09c-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="9a09c-256">Turėtumėte gauti `aadToken` kaip atsakymą, panašų į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="9a09c-257">Suformuluokite JSON užklausą, panašią į šią:</span><span class="sxs-lookup"><span data-stu-id="9a09c-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="9a09c-258">Kur:</span><span class="sxs-lookup"><span data-stu-id="9a09c-258">Where:</span></span>
    - <span data-ttu-id="9a09c-259">Reikšmė `client_assertion` turi būti `aadToken`, kurį gavote ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="9a09c-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="9a09c-260">Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="9a09c-261">Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="9a09c-262">Pateikite HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="9a09c-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="9a09c-263">**„URL”** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="9a09c-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="9a09c-264">**Metodas** - `POST`</span><span class="sxs-lookup"><span data-stu-id="9a09c-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="9a09c-265">**HTTP antraštė** – įtraukite API versiją (raktas yra `Api-Version` ir reikšmė yra `1.0`)</span><span class="sxs-lookup"><span data-stu-id="9a09c-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="9a09c-266">**Teksto turinys** – įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="9a09c-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="9a09c-267">Gausite  `access_token` atsakyme.</span><span class="sxs-lookup"><span data-stu-id="9a09c-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="9a09c-268">Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API.</span><span class="sxs-lookup"><span data-stu-id="9a09c-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="9a09c-269">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9a09c-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="9a09c-270">Konfigūruoti Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="9a09c-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="9a09c-271">Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="9a09c-272">Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos.</span><span class="sxs-lookup"><span data-stu-id="9a09c-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="9a09c-273">Jis iš esmės turi keturias dalis:</span><span class="sxs-lookup"><span data-stu-id="9a09c-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="9a09c-274">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="9a09c-275">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="9a09c-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="9a09c-276">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="9a09c-277">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="9a09c-278">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-278">Partitioning</span></span>

<span data-ttu-id="9a09c-279">Dalijimas gali stipriai paveikti matomumo papildinio veikimą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="9a09c-280">Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.</span><span class="sxs-lookup"><span data-stu-id="9a09c-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="9a09c-281">Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*.</span><span class="sxs-lookup"><span data-stu-id="9a09c-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="9a09c-282">Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensjia filtruose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="9a09c-283">*Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="9a09c-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="9a09c-284">„Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="9a09c-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="9a09c-285">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="9a09c-285">Dimension configurations</span></span>

<span data-ttu-id="9a09c-286">Inventoriaus matomumas suteikia pagrindinų numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.</span><span class="sxs-lookup"><span data-stu-id="9a09c-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="9a09c-287">Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="9a09c-288">Dimensijos tipas</span><span class="sxs-lookup"><span data-stu-id="9a09c-288">Dimension type</span></span> | <span data-ttu-id="9a09c-289">Dimensijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="9a09c-290">Produktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="9a09c-291">Produktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="9a09c-292">Produktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="9a09c-293">Produktas</span><span class="sxs-lookup"><span data-stu-id="9a09c-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="9a09c-294">Sekimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="9a09c-295">Sekimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="9a09c-296">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="9a09c-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="9a09c-297">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="9a09c-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="9a09c-298">Inventoriaus būsena</span><span class="sxs-lookup"><span data-stu-id="9a09c-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="9a09c-299">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="9a09c-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="9a09c-300">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="9a09c-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="9a09c-301">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="9a09c-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="9a09c-302">Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais.</span><span class="sxs-lookup"><span data-stu-id="9a09c-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="9a09c-303">Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="9a09c-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="9a09c-304">Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="9a09c-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="9a09c-305">Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="9a09c-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="9a09c-306">Dėl integravimo, inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinš* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="9a09c-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="9a09c-307">Tikslines nurodymas turi būti vienas iš:</span><span class="sxs-lookup"><span data-stu-id="9a09c-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="9a09c-308">Numatyti nurodymai Inventoriaus matomumo</span><span class="sxs-lookup"><span data-stu-id="9a09c-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="9a09c-309">Pasirinktinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="9a09c-309">Custom dimensions</span></span>

<span data-ttu-id="9a09c-310">Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai nurydmuose ir publikuoti įvykį su nurodymais.</span><span class="sxs-lookup"><span data-stu-id="9a09c-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="9a09c-311">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-311">Indexing</span></span>

<span data-ttu-id="9a09c-312">Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="9a09c-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="9a09c-313">Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.</span><span class="sxs-lookup"><span data-stu-id="9a09c-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="9a09c-314">Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių.</span><span class="sxs-lookup"><span data-stu-id="9a09c-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="9a09c-315">Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant implementuoti užtikrinant, kad atitiks jis jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="9a09c-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="9a09c-316">Pavyzdžiui, jei norite laukti produktų tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="9a09c-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="9a09c-317">Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="9a09c-318">Kai kada norite tik laukti produkto bendrai.</span><span class="sxs-lookup"><span data-stu-id="9a09c-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="9a09c-319">Turite du indeksus nustatytus kaip:</span><span class="sxs-lookup"><span data-stu-id="9a09c-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="9a09c-320">Tuštinkite skliaustelius pagal produkto ID su dalijimu.</span><span class="sxs-lookup"><span data-stu-id="9a09c-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="9a09c-321">Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="9a09c-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="9a09c-322">Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`.</span><span class="sxs-lookup"><span data-stu-id="9a09c-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="9a09c-323">Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="9a09c-324">Galite padėti savo laukimo kriterijus pagal būtiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="9a09c-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="9a09c-325">Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.</span><span class="sxs-lookup"><span data-stu-id="9a09c-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="9a09c-326">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-326">Custom measurement</span></span>

<span data-ttu-id="9a09c-327">Numatytieji matavimo kiekiai yra siejami su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="9a09c-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="9a09c-328">Tačiau gali reikėti kiekio, kuris būtų pagamintas iš numatytųjų matavimų kombinacijos.</span><span class="sxs-lookup"><span data-stu-id="9a09c-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="9a09c-329">Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimus laukimus.</span><span class="sxs-lookup"><span data-stu-id="9a09c-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="9a09c-330">Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.</span><span class="sxs-lookup"><span data-stu-id="9a09c-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="9a09c-331">Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.</span><span class="sxs-lookup"><span data-stu-id="9a09c-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="9a09c-332">Vartojimo sistema</span><span class="sxs-lookup"><span data-stu-id="9a09c-332">Consumption system</span></span> | <span data-ttu-id="9a09c-333">Skaičiuotos priemonės</span><span class="sxs-lookup"><span data-stu-id="9a09c-333">Calculated measurers</span></span> | <span data-ttu-id="9a09c-334">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="9a09c-334">Data source</span></span> | <span data-ttu-id="9a09c-335">Keitikas</span><span class="sxs-lookup"><span data-stu-id="9a09c-335">Modifier</span></span> | <span data-ttu-id="9a09c-336">Keitiko apskaičiavimo tipas</span><span class="sxs-lookup"><span data-stu-id="9a09c-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="9a09c-337">Priedas</span><span class="sxs-lookup"><span data-stu-id="9a09c-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="9a09c-338">Priedas</span><span class="sxs-lookup"><span data-stu-id="9a09c-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="9a09c-339">Atimtis</span><span class="sxs-lookup"><span data-stu-id="9a09c-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="9a09c-340">Priedas</span><span class="sxs-lookup"><span data-stu-id="9a09c-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="9a09c-341">Atimtis</span><span class="sxs-lookup"><span data-stu-id="9a09c-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="9a09c-342">Priedas</span><span class="sxs-lookup"><span data-stu-id="9a09c-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="9a09c-343">Priedas</span><span class="sxs-lookup"><span data-stu-id="9a09c-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="9a09c-344">Atimtis</span><span class="sxs-lookup"><span data-stu-id="9a09c-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="9a09c-345">Atimtis</span><span class="sxs-lookup"><span data-stu-id="9a09c-345">Subtraction</span></span> |

<span data-ttu-id="9a09c-346">Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.</span><span class="sxs-lookup"><span data-stu-id="9a09c-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="9a09c-347">Išvestis `MyCustomAvailableforReservation` praemta apskaičiavimo nustatymais tinkintuose matavimuose:</span><span class="sxs-lookup"><span data-stu-id="9a09c-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="9a09c-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="9a09c-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="9a09c-349">Turimų keitimų publikavimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-349">Posting on-hand changes</span></span>

<span data-ttu-id="9a09c-350">Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono.</span><span class="sxs-lookup"><span data-stu-id="9a09c-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="9a09c-351">Jo forma bus:</span><span class="sxs-lookup"><span data-stu-id="9a09c-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="9a09c-352">Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.</span><span class="sxs-lookup"><span data-stu-id="9a09c-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="9a09c-353">Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elementos duomenis su juo susietais.</span><span class="sxs-lookup"><span data-stu-id="9a09c-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="9a09c-354">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="9a09c-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="9a09c-355">Publikavimo turimų keitimų laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="9a09c-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="9a09c-356">Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="9a09c-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="9a09c-357">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="9a09c-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="9a09c-358">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="9a09c-359">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="9a09c-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="9a09c-360">Publikavimo turimų keitimų laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="9a09c-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="9a09c-361">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="9a09c-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="9a09c-362">Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reiškmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="9a09c-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="9a09c-363">JSON dokumento laukelip ypatybės</span><span class="sxs-lookup"><span data-stu-id="9a09c-363">JSON document field properties</span></span>

<span data-ttu-id="9a09c-364">Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="9a09c-365">Lauko ID</span><span class="sxs-lookup"><span data-stu-id="9a09c-365">Field ID</span></span> | <span data-ttu-id="9a09c-366">aprašymas</span><span class="sxs-lookup"><span data-stu-id="9a09c-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="9a09c-367">Unikalus ID konkrečiam keitimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="9a09c-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="9a09c-368">Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart.</span><span class="sxs-lookup"><span data-stu-id="9a09c-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="9a09c-369">Organizacijos identifikatorius susietas su įvykiu.</span><span class="sxs-lookup"><span data-stu-id="9a09c-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="9a09c-370">Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID.</span><span class="sxs-lookup"><span data-stu-id="9a09c-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="9a09c-371">Aptariamas produkto identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="9a09c-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="9a09c-372">Kiekis, pagal kurį turimi poreikiai keičiami.</span><span class="sxs-lookup"><span data-stu-id="9a09c-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="9a09c-373">Jei pavyzdžiui 10 naujų beigelių įtraukti į lentylą, vertė yra 10.</span><span class="sxs-lookup"><span data-stu-id="9a09c-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="9a09c-374">Jei 3 beigeliai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3.</span><span class="sxs-lookup"><span data-stu-id="9a09c-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="9a09c-375">Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje.</span><span class="sxs-lookup"><span data-stu-id="9a09c-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="9a09c-376">Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="9a09c-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="9a09c-377">Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="9a09c-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="9a09c-378">Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimenseijas savo eilėse.</span><span class="sxs-lookup"><span data-stu-id="9a09c-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="9a09c-379">Dinaminis rakto maišas/verčių poros.</span><span class="sxs-lookup"><span data-stu-id="9a09c-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="9a09c-380">Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="9a09c-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="9a09c-381">Esamas turimas laukimas</span><span class="sxs-lookup"><span data-stu-id="9a09c-381">Querying current on-hand</span></span>

<span data-ttu-id="9a09c-382">Laukimo galutinis taškas esamame turimame bus panašus URL:</span><span class="sxs-lookup"><span data-stu-id="9a09c-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="9a09c-383">Jis bus laukiamas su HTTP `POST` metodu.</span><span class="sxs-lookup"><span data-stu-id="9a09c-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="9a09c-384">Esamas turimas laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="9a09c-384">Current on-hand query example 1</span></span>

<span data-ttu-id="9a09c-385">Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="9a09c-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="9a09c-386">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="9a09c-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="9a09c-387">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="9a09c-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="9a09c-388">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="9a09c-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="9a09c-389">Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="9a09c-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="9a09c-390">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="9a09c-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="9a09c-391">Esamas turimas laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="9a09c-391">Current on-hand query example 2</span></span>

<span data-ttu-id="9a09c-392">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="9a09c-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="9a09c-393">Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reiškmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="9a09c-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="9a09c-394">Grįžtamojo rezultato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9a09c-394">Example return result</span></span>

<span data-ttu-id="9a09c-395">Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.</span><span class="sxs-lookup"><span data-stu-id="9a09c-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="9a09c-396">Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.</span><span class="sxs-lookup"><span data-stu-id="9a09c-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
