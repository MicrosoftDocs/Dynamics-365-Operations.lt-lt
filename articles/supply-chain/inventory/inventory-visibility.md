---
title: Inventoriaus matomumo papildinys
description: Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910430"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="0dbc5-103">Inventoriaus matomumo papildinys</span><span class="sxs-lookup"><span data-stu-id="0dbc5-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="0dbc5-104">Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mikropaslaugos, kurios įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="0dbc5-105">Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="0dbc5-106">Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="0dbc5-107">Inventoriaus matomumas yra mikrotarnyba, esanti „Microsoft Dataverse“, o tai reiškia, kad galite ją plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, atitinkančių jūsų verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="0dbc5-108">Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="0dbc5-109">Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="0dbc5-110">Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="0dbc5-111">Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="0dbc5-112">Įdiekite Inventoriaus matomumo papildinį</span><span class="sxs-lookup"><span data-stu-id="0dbc5-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="0dbc5-113">Jums reikia įdiegti jį naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0dbc5-114">LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="0dbc5-115">Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0dbc5-116">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="0dbc5-116">Prerequisites</span></span>

<span data-ttu-id="0dbc5-117">Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="0dbc5-118">Gaukite LCS diegimo projektą su mažiausiai viena patalpinta aplinka.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="0dbc5-119">Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) buvo patenkintos.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="0dbc5-120">Atsargų matomumui nereikia dvigubo rašymo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="0dbc5-121">Kreipkitės į atsargų matomumo komandą el. paštu [inventvisibilitysupp@microsoft.com ](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte šiuos tris reikalingus failus:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="0dbc5-122">`Inventory Visibility Integration.zip` (jei jūsų vykdoma „Supply Chain Management” versija yra ankstesnė nei 10.0.18 versija)</span><span class="sxs-lookup"><span data-stu-id="0dbc5-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="0dbc5-123">Vadovaukitės instrukcijomis, pateiktomis [Greitas pasirengimas darbui: Programos registravimas su „Microsoft” tapatybės platforma](/azure/active-directory/develop/quickstart-register-app), kad užregistruotumėte programą ir įtrauktumėte kliento slaptąjį raktą į AAD pagal jūsų „Azure” prenumeratą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="0dbc5-124">Programos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="0dbc5-125">Kliento slaptojo rakto įtraukimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="0dbc5-126">Tolesniuose veiksmuose bus naudojami **Programos (Kliento) ID**, **Kliento slaptasis raktas** ir **Nuomotojo ID**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="0dbc5-127">Šiuo metu palaikomos šalys ir regionai yra Kanada, Jungtinės Valstijos ir Europos Sąjunga (ES).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="0dbc5-128">Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="0dbc5-129">„Dataverse“ nustatymas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-129">Set up Dataverse</span></span>

<span data-ttu-id="0dbc5-130">Atlikite šiuos veiksmus, kad nustatytumėte „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="0dbc5-131">Prie savo nuomininko pridėkite aptarnavimo principą:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="0dbc5-132">Įdiekite „Azure AD“ „PowerShell“ v2 modulį, kaip aprašyta skyriuje [„Azure Active Directory“ „PowerShell for Graph“ diegimas](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="0dbc5-133">Paleiskite šią „PowerShell“ komandą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="0dbc5-134">Sukurkite programos naudotoją „Dataverse“ atsargų matomumui:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="0dbc5-135">Atidarykite savo „Dataverse“ aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="0dbc5-136">Eikite į **Išplėstiniai nustatymai \> Sistema \> Sauga \> Naudotojai** ir sukurkite programos naudotoją.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="0dbc5-137">Naudokite peržiūros meniu, kad puslapio rodinį pakeistumėte į **Programos naudotojai**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="0dbc5-138">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-138">Select **New**.</span></span> <span data-ttu-id="0dbc5-139">Programos ID nustatykite kaip *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="0dbc5-140">(Išsaugant keitimus objekto ID įkeliamas automatiškai.) Pavadinimą galima pritaikyti.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="0dbc5-141">Pavyzdžiui, jį galima pakeisti į *Atsargų matomumas*.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="0dbc5-142">Jums pabaigus, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="0dbc5-143">Pasirinkite **Priskirti vaidmenį**, tada pasirinkite **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="0dbc5-144">Jei yra vaidmuo pavadinimu **„Common Data Service“ naudotojas**, pasirinkite ir jį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="0dbc5-145">Daugiau informacijos žr. skyriuje [Programos naudotojo kūrimas](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="0dbc5-146">Jei jūsų „Dataverse” numatytoji kalba nėra **Anglų**:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="0dbc5-147">Eikite į **Išplėstiniai parametrai \> Administravimas \> Kalbos**,</span><span class="sxs-lookup"><span data-stu-id="0dbc5-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="0dbc5-148">Pasirinkite **Anglų (LanguageCode=1033)** ir pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="0dbc5-149">Importuokite failą `Inventory Visibility Dataverse Solution.zip`, kuriame yra su „Dataverse“ konfigūracija susiję objektai ir „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="0dbc5-150">Eikite į puslapį **Sprendimai**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="0dbc5-151">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-151">Select **Import**.</span></span>

1. <span data-ttu-id="0dbc5-152">Importuokite konfigūracijos atnaujinimo paleidiklio eigą:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="0dbc5-153">Eikite į puslapį „Microsoft Flow“.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="0dbc5-154">Patikrinkite, ar yra ryšys, pavadintas „*Dataverse“ (senesnis)*.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="0dbc5-155">(Jei ne, sukurkite jį.)</span><span class="sxs-lookup"><span data-stu-id="0dbc5-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="0dbc5-156">Importuokite failą `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="0dbc5-157">Jį importavus srityje **Mano srautai** bus rodomas paleidiklis.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="0dbc5-158">Inicijuokite šiuos keturis kintamuosius, atsižvelgdami į aplinkos informaciją:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="0dbc5-159">„Azure“ nuomininko ID</span><span class="sxs-lookup"><span data-stu-id="0dbc5-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="0dbc5-160">„Azure“ programos kliento ID</span><span class="sxs-lookup"><span data-stu-id="0dbc5-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="0dbc5-161">„Azure“ programos kliento raktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="0dbc5-162">Atsargų matomumo galinis punktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="0dbc5-163">Daugiau informacijos apie šį kintamąjį žr. toliau šioje temoje pateikiamame skyriuje [Atsargų matomumo integravimo nustatymas](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="0dbc5-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="0dbc5-164">![Konfigūracijos paleidiklis](media/configuration-trigger.png "Konfigūracijos paleidiklis")</span><span class="sxs-lookup"><span data-stu-id="0dbc5-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="0dbc5-165">Pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="0dbc5-166">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-166">Install the add-in</span></span>

<span data-ttu-id="0dbc5-167">Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="0dbc5-168">Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="0dbc5-169">Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="0dbc5-170">Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="0dbc5-171">Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai**, skyriuje **„Power Platform“ integravimas**, kuriame rasite „Dataverse“ aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="0dbc5-172">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="0dbc5-173">![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")</span><span class="sxs-lookup"><span data-stu-id="0dbc5-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="0dbc5-174">Rinkitės **Diegti naują papildinį** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="0dbc5-175">Esamų atvirų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="0dbc5-176">Sąraše pasirinkite **Atsargų matomumas**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="0dbc5-177">Įveskite šias vertes savo aplinkos laukeliuose:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="0dbc5-178">**AAD programos (kliento) ID**</span><span class="sxs-lookup"><span data-stu-id="0dbc5-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="0dbc5-179">**ĮTRAUKITE nuomotojo ID**</span><span class="sxs-lookup"><span data-stu-id="0dbc5-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="0dbc5-180">![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")</span><span class="sxs-lookup"><span data-stu-id="0dbc5-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="0dbc5-181">Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="0dbc5-182">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-182">Select **Install**.</span></span> <span data-ttu-id="0dbc5-183">Papildinio būsena bus rodoma kaip **diegiama**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="0dbc5-184">Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="0dbc5-185">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-185">Uninstall the add-in</span></span>

<span data-ttu-id="0dbc5-186">Norėdami išdiegti papildinį, pasirinkite **Išdiegti**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="0dbc5-187">Atnaujinus LCS inventoriaus matomumo papildinys bus panaikintas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="0dbc5-188">Atlikus išdiegimo procesą pašalinama papildinio registracija ir pradedamas darbas siekiant išvalyti visus verslo duomenis laikomus paslaugose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="0dbc5-189">Turimų atsargų duomenų iš „Supply Chain Management” naudojimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="0dbc5-190">Aplinkos matomumo integravimo paketo diegimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="0dbc5-191">Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="0dbc5-192">Tada įdiekite paketą LCS.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="0dbc5-193">Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="0dbc5-194">Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="0dbc5-195">Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="0dbc5-196">Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="0dbc5-197">Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="0dbc5-198">(Numatyta, kad jos yra įjungtos.)</span><span class="sxs-lookup"><span data-stu-id="0dbc5-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="0dbc5-199">Funkcijos aprašymas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-199">Feature description</span></span> | <span data-ttu-id="0dbc5-200">Kodo versija</span><span class="sxs-lookup"><span data-stu-id="0dbc5-200">Code version</span></span> | <span data-ttu-id="0dbc5-201">Klasės kaitaliojimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="0dbc5-202">Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="0dbc5-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="0dbc5-203">10.0.11</span></span> | <span data-ttu-id="0dbc5-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="0dbc5-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="0dbc5-205">Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="0dbc5-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="0dbc5-206">10.0.12</span></span> | <span data-ttu-id="0dbc5-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="0dbc5-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="0dbc5-208">Atsargų matomumo integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="0dbc5-209">„Supply Chain Management” atidarykite darbo sritį **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ir įjunkite funkciją **Atsargų matomumo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="0dbc5-210">Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų matomumo integravimo parametrai** ir įveskite aplinkos, kurioje paleidžiamas atsargų matomumas, URL.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="0dbc5-211">Raskite savo LCS aplinkos „Azure“ regioną, o tada įveskite URL.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="0dbc5-212">URL forma yra tokia:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="0dbc5-213">Pavyzdžiui, jei esate Europoje, jūsų aplinkos URL bus vienas iš šių:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="0dbc5-214">Šiuo metu naudojami nurodyti regionai.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="0dbc5-215">„Azure“ regionas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-215">Azure region</span></span> | <span data-ttu-id="0dbc5-216">Trumpas regiono pavadinimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="0dbc5-217">Rytų Australija</span><span class="sxs-lookup"><span data-stu-id="0dbc5-217">Australia east</span></span> | <span data-ttu-id="0dbc5-218">eau</span><span class="sxs-lookup"><span data-stu-id="0dbc5-218">eau</span></span> |
    | <span data-ttu-id="0dbc5-219">Pietryčių Australija</span><span class="sxs-lookup"><span data-stu-id="0dbc5-219">Australia southeast</span></span> | <span data-ttu-id="0dbc5-220">seau</span><span class="sxs-lookup"><span data-stu-id="0dbc5-220">seau</span></span> |
    | <span data-ttu-id="0dbc5-221">Centrinė Kanada</span><span class="sxs-lookup"><span data-stu-id="0dbc5-221">Canada central</span></span> | <span data-ttu-id="0dbc5-222">cca</span><span class="sxs-lookup"><span data-stu-id="0dbc5-222">cca</span></span> |
    | <span data-ttu-id="0dbc5-223">Rytų Kanada</span><span class="sxs-lookup"><span data-stu-id="0dbc5-223">Canada east</span></span> | <span data-ttu-id="0dbc5-224">eca</span><span class="sxs-lookup"><span data-stu-id="0dbc5-224">eca</span></span> |
    | <span data-ttu-id="0dbc5-225">Šiaurės Europa</span><span class="sxs-lookup"><span data-stu-id="0dbc5-225">North Europe</span></span> | <span data-ttu-id="0dbc5-226">neu</span><span class="sxs-lookup"><span data-stu-id="0dbc5-226">neu</span></span> |
    | <span data-ttu-id="0dbc5-227">Vakarų Europa</span><span class="sxs-lookup"><span data-stu-id="0dbc5-227">West Europe</span></span> | <span data-ttu-id="0dbc5-228">weu</span><span class="sxs-lookup"><span data-stu-id="0dbc5-228">weu</span></span> |
    | <span data-ttu-id="0dbc5-229">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="0dbc5-229">East US</span></span> | <span data-ttu-id="0dbc5-230">eus</span><span class="sxs-lookup"><span data-stu-id="0dbc5-230">eus</span></span> |
    | <span data-ttu-id="0dbc5-231">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="0dbc5-231">West US</span></span> | <span data-ttu-id="0dbc5-232">wus</span><span class="sxs-lookup"><span data-stu-id="0dbc5-232">wus</span></span> |

1. <span data-ttu-id="0dbc5-233">Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="0dbc5-234">Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="0dbc5-235">Vieša inventoriaus matomumo API</span><span class="sxs-lookup"><span data-stu-id="0dbc5-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="0dbc5-236">Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="0dbc5-237">Jis palaiko tris pagrindines sąveikos rūšis:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="0dbc5-238">Turimų atsargų pakeitimų į papildinio formą išorės sistemoje registravimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="0dbc5-239">Dabartinių turimų kiekių užklausos iš išorės sistemos</span><span class="sxs-lookup"><span data-stu-id="0dbc5-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="0dbc5-240">Automatinis sinchronizavimas su turimomis „Supply Chain Management“ atsargomis.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="0dbc5-241">Automatinis sinchronizavimas nėra viešosios API dalis.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="0dbc5-242">Vietoje to jis tvarkomas fone, aplinkoms, kuriose įjungtas atsargų matomumo priedas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="0dbc5-243">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-243">Authentication</span></span>

<span data-ttu-id="0dbc5-244">Platformos saugos atpažinimo ženklas naudojamas atsargų matomumo priedui iškviesti.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="0dbc5-245">Todėl turite sugeneruoti *„Azure Active Directory“ („Azure AD“) atpažinimo ženklą*, naudodami savo „Azure AD“ programą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="0dbc5-246">Tada turite naudoti „Azure AD“ atpažinimo ženklą, kad iš saugos tarnybos gautumėte *prieigos atpažinimo ženklą*.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="0dbc5-247">Gaukite saugos paslaugų žymą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="0dbc5-248">Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` jūsų „Supply Chain Management” programai.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="0dbc5-249">Iškvieskite „Azure Active Directory” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0dbc5-250">**„URL”** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="0dbc5-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="0dbc5-251">**Metodas** - `GET`</span><span class="sxs-lookup"><span data-stu-id="0dbc5-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="0dbc5-252">**Teksto turinys (formos duomenys)**:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="0dbc5-253">raktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-253">key</span></span> | <span data-ttu-id="0dbc5-254">vertė</span><span class="sxs-lookup"><span data-stu-id="0dbc5-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="0dbc5-255">„client_id”</span><span class="sxs-lookup"><span data-stu-id="0dbc5-255">client_id</span></span> | <span data-ttu-id="0dbc5-256">„${aadAppId}“</span><span class="sxs-lookup"><span data-stu-id="0dbc5-256">${aadAppId}</span></span> |
        | <span data-ttu-id="0dbc5-257">„client_secret”</span><span class="sxs-lookup"><span data-stu-id="0dbc5-257">client_secret</span></span> | <span data-ttu-id="0dbc5-258">„${aadAppSecret}“</span><span class="sxs-lookup"><span data-stu-id="0dbc5-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="0dbc5-259">„grant_type”</span><span class="sxs-lookup"><span data-stu-id="0dbc5-259">grant_type</span></span> | <span data-ttu-id="0dbc5-260">„client_credentials”</span><span class="sxs-lookup"><span data-stu-id="0dbc5-260">client_credentials</span></span> |
        | <span data-ttu-id="0dbc5-261">ištekliai</span><span class="sxs-lookup"><span data-stu-id="0dbc5-261">resource</span></span> | <span data-ttu-id="0dbc5-262">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="0dbc5-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="0dbc5-263">Turėtumėte gauti `aadToken` kaip atsakymą, panašų į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="0dbc5-264">Suformuluokite JSON užklausą, panašią į šią:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="0dbc5-265">Kur:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-265">Where:</span></span>
    - <span data-ttu-id="0dbc5-266">Reikšmė `client_assertion` turi būti `aadToken`, kurį gavote ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="0dbc5-267">Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="0dbc5-268">Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="0dbc5-269">Pateikite HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0dbc5-270">**„URL”** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="0dbc5-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="0dbc5-271">**Metodas** - `POST`</span><span class="sxs-lookup"><span data-stu-id="0dbc5-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="0dbc5-272">**HTTP antraštė** – įtraukite API versiją (raktas yra `Api-Version` ir reikšmė yra `1.0`)</span><span class="sxs-lookup"><span data-stu-id="0dbc5-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="0dbc5-273">**Teksto turinys** – įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="0dbc5-274">Gausite  `access_token` atsakyme.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="0dbc5-275">Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="0dbc5-276">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="0dbc5-277">Užklausos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0dbc5-277">Sample Request</span></span>

<span data-ttu-id="0dbc5-278">Jūsų nuorodai, čia yra http užklausos pavyzdys, jūs galite naudoti bet kokius įrankius ar kodavimo kalbą šiai užklausai išsiųsti, pavyzdžiui ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="0dbc5-279">Konfigūruoti Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="0dbc5-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="0dbc5-280">Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="0dbc5-281">Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="0dbc5-282">Jis iš esmės turi keturias dalis:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="0dbc5-283">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="0dbc5-284">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="0dbc5-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="0dbc5-285">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="0dbc5-286">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="0dbc5-287">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-287">Partitioning</span></span>

<span data-ttu-id="0dbc5-288">Dalijimas gali stipriai paveikti matomumo papildinio veikimą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="0dbc5-289">Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="0dbc5-290">Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="0dbc5-291">Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensija filtruose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="0dbc5-292">*Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="0dbc5-293">„Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="0dbc5-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="0dbc5-294">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="0dbc5-294">Dimension configurations</span></span>

<span data-ttu-id="0dbc5-295">Inventoriaus matomumas suteikia pagrindinių numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="0dbc5-296">Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="0dbc5-297">Dimensijos tipas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-297">Dimension type</span></span> | <span data-ttu-id="0dbc5-298">Dimensijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="0dbc5-299">Produktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="0dbc5-300">Produktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="0dbc5-301">Produktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="0dbc5-302">Produktas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="0dbc5-303">Sekimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="0dbc5-304">Sekimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="0dbc5-305">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="0dbc5-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="0dbc5-306">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="0dbc5-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="0dbc5-307">Inventoriaus būsena</span><span class="sxs-lookup"><span data-stu-id="0dbc5-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="0dbc5-308">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="0dbc5-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="0dbc5-309">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="0dbc5-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="0dbc5-310">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="0dbc5-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="0dbc5-311">Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="0dbc5-312">Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="0dbc5-313">Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="0dbc5-314">Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="0dbc5-315">Dėl integravimo inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinį* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="0dbc5-316">Tikslines nurodymas turi būti vienas iš:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="0dbc5-317">Numatyti Inventoriaus matomumo nurodymai</span><span class="sxs-lookup"><span data-stu-id="0dbc5-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="0dbc5-318">Pasirinktinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="0dbc5-318">Custom dimensions</span></span>

<span data-ttu-id="0dbc5-319">Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai dimensijose ir publikuoti įvykį su dimensijomis.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="0dbc5-320">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-320">Indexing</span></span>

<span data-ttu-id="0dbc5-321">Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="0dbc5-322">Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="0dbc5-323">Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="0dbc5-324">Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant įdiegti užtikrinant, kad atitiks jis jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="0dbc5-325">Pavyzdžiui, jei norite laukti produktų tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="0dbc5-326">Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="0dbc5-327">Kai kada norite tik laukti produkto bendrai.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="0dbc5-328">Turite du indeksus nustatytus kaip:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="0dbc5-329">Tuštinkite skliaustelius pagal produkto ID su dalijimu.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="0dbc5-330">Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="0dbc5-331">Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="0dbc5-332">Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="0dbc5-333">Galite padėti savo laukimo kriterijus pagal būtiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="0dbc5-334">Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="0dbc5-335">Šiuo metu iš lauko `filters` tik `ProductId` palaiko kelias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="0dbc5-336">Jei `ProductId` yra tuščias masyvas, bus pateiktos visų produktų užklausos.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="0dbc5-337">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-337">Custom measurement</span></span>

<span data-ttu-id="0dbc5-338">Numatytieji matavimo kiekiai yra siejami su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="0dbc5-339">Tačiau gali reikėti kiekio, kuris būtų pagamintas iš numatytųjų matavimų kombinacijos.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="0dbc5-340">Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimas užklausas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="0dbc5-341">Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="0dbc5-342">Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="0dbc5-343">Vartojimo sistema</span><span class="sxs-lookup"><span data-stu-id="0dbc5-343">Consumption system</span></span> | <span data-ttu-id="0dbc5-344">Skaičiuotos priemonės</span><span class="sxs-lookup"><span data-stu-id="0dbc5-344">Calculated measurers</span></span> | <span data-ttu-id="0dbc5-345">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="0dbc5-345">Data source</span></span> | <span data-ttu-id="0dbc5-346">Keitikas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-346">Modifier</span></span> | <span data-ttu-id="0dbc5-347">Keitiko apskaičiavimo tipas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="0dbc5-348">Priedas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="0dbc5-349">Priedas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="0dbc5-350">Atimtis</span><span class="sxs-lookup"><span data-stu-id="0dbc5-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="0dbc5-351">Priedas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="0dbc5-352">Atimtis</span><span class="sxs-lookup"><span data-stu-id="0dbc5-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="0dbc5-353">Priedas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="0dbc5-354">Priedas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="0dbc5-355">Atimtis</span><span class="sxs-lookup"><span data-stu-id="0dbc5-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="0dbc5-356">Atimtis</span><span class="sxs-lookup"><span data-stu-id="0dbc5-356">Subtraction</span></span> |

<span data-ttu-id="0dbc5-357">Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="0dbc5-358">Išvestis `MyCustomAvailableforReservation` paremta apskaičiavimo nustatymais tinkintuose matavimuose:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="0dbc5-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="0dbc5-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="0dbc5-360">Turimų keitimų publikavimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-360">Posting on-hand changes</span></span>

<span data-ttu-id="0dbc5-361">Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="0dbc5-362">Jo forma bus:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="0dbc5-363">Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="0dbc5-364">Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elemento duomenis su juo susietais.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="0dbc5-365">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="0dbc5-366">Publikavimo turimų keitimų laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="0dbc5-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="0dbc5-367">Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0dbc5-368">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0dbc5-369">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0dbc5-370">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="0dbc5-371">Publikavimo turimų keitimų laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="0dbc5-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="0dbc5-372">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0dbc5-373">Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reikšmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="0dbc5-374">JSON dokumento laukelio ypatybės</span><span class="sxs-lookup"><span data-stu-id="0dbc5-374">JSON document field properties</span></span>

<span data-ttu-id="0dbc5-375">Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="0dbc5-376">Lauko ID</span><span class="sxs-lookup"><span data-stu-id="0dbc5-376">Field ID</span></span> | <span data-ttu-id="0dbc5-377">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="0dbc5-378">Unikalus ID konkrečiam keitimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="0dbc5-379">Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="0dbc5-380">Organizacijos identifikatorius susietas su įvykiu.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="0dbc5-381">Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="0dbc5-382">Aptariamas produkto identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="0dbc5-383">Kiekis, pagal kurį turimi poreikiai keičiami.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="0dbc5-384">Jeigu, pavyzdžiui, 10 naujų riestainių buvo įtraukti į lentyną, vertė yra 10.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="0dbc5-385">Jei 3 riestainiai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="0dbc5-386">Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="0dbc5-387">Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="0dbc5-388">Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="0dbc5-389">Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimensijas savo eilėse.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="0dbc5-390">Dinaminis rakto maišas/verčių poros.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="0dbc5-391">Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="0dbc5-392">Esamas turimas laukimas</span><span class="sxs-lookup"><span data-stu-id="0dbc5-392">Querying current on-hand</span></span>

<span data-ttu-id="0dbc5-393">Laukimo galutinis taškas esamame turimame bus panašus URL:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="0dbc5-394">Jis bus laukiamas su HTTP `POST` metodu.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="0dbc5-395">Esamas turimas laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="0dbc5-395">Current on-hand query example 1</span></span>

<span data-ttu-id="0dbc5-396">Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0dbc5-397">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="0dbc5-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0dbc5-398">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0dbc5-399">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="0dbc5-400">Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="0dbc5-401">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="0dbc5-402">Esamas turimas laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="0dbc5-402">Current on-hand query example 2</span></span>

<span data-ttu-id="0dbc5-403">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0dbc5-404">Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reikšmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="0dbc5-405">Grįžtamojo rezultato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0dbc5-405">Example return result</span></span>

<span data-ttu-id="0dbc5-406">Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="0dbc5-407">Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.</span><span class="sxs-lookup"><span data-stu-id="0dbc5-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]