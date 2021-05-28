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
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017011"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="ed477-103">Inventoriaus matomumo papildinys</span><span class="sxs-lookup"><span data-stu-id="ed477-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="ed477-104">Inventoriaus matomumo papildinys yra nepriklausomos ir labai išdidinamos mikropaslaugos, kurios įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą.</span><span class="sxs-lookup"><span data-stu-id="ed477-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="ed477-105">Visa informacija susijusi su turimu inventoriumi yra eksportuojama į paslaugas esančias šalia realaus laiko per žemo lygio SQL integravimą.</span><span class="sxs-lookup"><span data-stu-id="ed477-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="ed477-106">Išorės sistemos prieiga prie paslaugų per RESTful API, kurios leidžia laukti turimos informacijos pagal turimą dimensijų rinkinį ir gauti esamų turimų padėčių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ed477-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="ed477-107">Inventoriaus matomumas yra mikrotarnyba, esanti „Microsoft Dataverse“, o tai reiškia, kad galite ją plėsti kurdami „Power Apps“ ir taikydami „Power BI“ norėdami tinkintų funkcijų, atitinkančių jūsų verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="ed477-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="ed477-108">Taip pat galima pagerinti indeksavimą inventoriaus užklausoms.</span><span class="sxs-lookup"><span data-stu-id="ed477-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="ed477-109">Inventoriaus matomumas suteikia konfigūravimo parinktis, kurios leidžia jį integruoti su keliomis trečiųjų šalių sistemomis.</span><span class="sxs-lookup"><span data-stu-id="ed477-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="ed477-110">Jis palaiko standartizuotą inventoriaus dimensiją, tinkintą plėtinį ir standartizuotus ir konfigūruojamus skaičiuojamus kiekius.</span><span class="sxs-lookup"><span data-stu-id="ed477-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="ed477-111">Ši tema aprašo, kaip įdiegti ir konfigūruoti inventoriaus matomumo papildinį „Dynamics 365 Supply Chain Management“ ir kaip naudoti jo programavimo sąsają (API).</span><span class="sxs-lookup"><span data-stu-id="ed477-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="ed477-112">Įdiekite Inventoriaus matomumo papildinį</span><span class="sxs-lookup"><span data-stu-id="ed477-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="ed477-113">Jums reikia įdiegti jį naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="ed477-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ed477-114">LCS yra bendradarbiavimo portalas suteikiantis aplinką ir reguliariai naujinamų paslaugų rinkinį, kuris padeda jums valdyti programos gyvavimo ciklą jūsų „Dynamics 365 Finance and Operations“ programose.</span><span class="sxs-lookup"><span data-stu-id="ed477-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="ed477-115">Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="ed477-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="ed477-116">Atsargų matomumo išankstinės sąlygos</span><span class="sxs-lookup"><span data-stu-id="ed477-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="ed477-117">Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="ed477-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="ed477-118">Gaukite LCS diegimo projektą su mažiausiai viena patalpinta aplinka.</span><span class="sxs-lookup"><span data-stu-id="ed477-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="ed477-119">Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) buvo patenkintos.</span><span class="sxs-lookup"><span data-stu-id="ed477-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="ed477-120">Atsargų matomumui nereikia dvigubo rašymo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="ed477-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="ed477-121">Kreipkitės į atsargų matomumo komandą el. paštu [inventvisibilitysupp@microsoft.com ](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte šiuos tris reikalingus failus:</span><span class="sxs-lookup"><span data-stu-id="ed477-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="ed477-122">`Inventory Visibility Integration.zip` (jei jūsų vykdoma „Supply Chain Management” versija yra ankstesnė nei 10.0.18 versija)</span><span class="sxs-lookup"><span data-stu-id="ed477-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="ed477-123">Kitu atveju, kreipkitės į atsargų matomumo komandą el. paštu [inventvisibilitysupp@microsoft.com ](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo „Package Deployer“.</span><span class="sxs-lookup"><span data-stu-id="ed477-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="ed477-124">Šiuos paketus gali naudoti oficialus „Package Deployer“ įrankis.</span><span class="sxs-lookup"><span data-stu-id="ed477-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="ed477-125">`InventoryServiceApplication.PackageDeployer.zip` (šiame pakete yra visi paketo pakeitimai `InventoryServiceBase` ir papildomi vartotojo sąsajos programos komponentai)</span><span class="sxs-lookup"><span data-stu-id="ed477-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="ed477-126">Vadovaukitės instrukcijomis, pateiktomis [Greitas pasirengimas darbui: Programos registravimas su „Microsoft” tapatybės platforma](/azure/active-directory/develop/quickstart-register-app), kad užregistruotumėte programą ir įtrauktumėte kliento slaptąjį raktą į AAD pagal jūsų „Azure” prenumeratą.</span><span class="sxs-lookup"><span data-stu-id="ed477-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="ed477-127">Programos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="ed477-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="ed477-128">Kliento slaptojo rakto įtraukimas</span><span class="sxs-lookup"><span data-stu-id="ed477-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="ed477-129">Tolesniuose veiksmuose bus naudojami **Programos (Kliento) ID** ir **Kliento slaptasis raktas** ir **Nuomotojo ID**.</span><span class="sxs-lookup"><span data-stu-id="ed477-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ed477-130">Šiuo metu palaikomos šalys ir regionai yra Kanada, Jungtinės Valstijos ir Europos Sąjunga (ES).</span><span class="sxs-lookup"><span data-stu-id="ed477-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="ed477-131">Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda.</span><span class="sxs-lookup"><span data-stu-id="ed477-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="ed477-132">„Dataverse“ nustatymas</span><span class="sxs-lookup"><span data-stu-id="ed477-132">Set up Dataverse</span></span>

<span data-ttu-id="ed477-133">Norėdami nustatyti naudoti su atsargų matomumu, pirmiausia turite paruošti būtinąsias sąlygas ir nuspręsti, ar nustatyti „Package Deployer“ įrankį, ar rankiniu būdu importuodami sprendimus (abiejų „Dataverse“ daryti „Dataverse“ nereikia).</span><span class="sxs-lookup"><span data-stu-id="ed477-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="ed477-134">Tada, įdiekite Inventoriaus matomumo papildinį.</span><span class="sxs-lookup"><span data-stu-id="ed477-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="ed477-135">Toliau pateikti poskyriai aprašo, kaip užbaigti visas šias užduotis.</span><span class="sxs-lookup"><span data-stu-id="ed477-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="ed477-136">Paruošti „Dataverse“ būtinąsias sąlygas</span><span class="sxs-lookup"><span data-stu-id="ed477-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="ed477-137">Prieš pradėdami „Dataverse“ nustatyti, pridėkite aptarnavimo principą savo nuomininkui, atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="ed477-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="ed477-138">Įdiekite „Azure AD“ „PowerShell“ v2 modulį, kaip aprašyta skyriuje [„Azure Active Directory“ „PowerShell for Graph“ diegimas](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="ed477-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="ed477-139">Paleiskite šią „PowerShell“ komandą:</span><span class="sxs-lookup"><span data-stu-id="ed477-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="ed477-140">Nustatyti „Dataverse“ naudojant „Package Deployer“ įrankį</span><span class="sxs-lookup"><span data-stu-id="ed477-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="ed477-141">Jei turite būtinųjų komponentų, naudokite šią procedūrą, jei norite nustatyti „Dataverse“ naudodami „Package Deployer“ įrankį.</span><span class="sxs-lookup"><span data-stu-id="ed477-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="ed477-142">Daugiau informacijos apie tai, kaip importuoti sprendimus neautomatiniu būdu, rasite kitame skyriuje (neduokite abiejų).</span><span class="sxs-lookup"><span data-stu-id="ed477-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="ed477-143">Įdiekite programavimo įrankius, kaip aprašyta [atsisiuntimo „NuGet“ įrankiuose](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span><span class="sxs-lookup"><span data-stu-id="ed477-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="ed477-144">Atsižvelgdami į savo verslo poreikius, pasirinkite `InventoryServiceBase` pakuotę arba `InventoryServiceApplication` pakuotę.</span><span class="sxs-lookup"><span data-stu-id="ed477-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="ed477-145">Importuoti sprendimus:</span><span class="sxs-lookup"><span data-stu-id="ed477-145">Import the solutions:</span></span>
    1. <span data-ttu-id="ed477-146">`InventoryServiceBase` paketui:</span><span class="sxs-lookup"><span data-stu-id="ed477-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="ed477-147">Išpakuokite `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="ed477-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="ed477-148">Rasti `InventoryServiceBase` aplanką, `[Content_Types].xml` failą, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` failą, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` failą ir `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` failą.</span><span class="sxs-lookup"><span data-stu-id="ed477-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="ed477-149">Nukopijuokite kiekvieną iš šių aplankų ir rinkmenų į `.\Tools\PackageDeployment` katalogą, kuris buvo sukurtas įdiegus programuotojo įrankius.</span><span class="sxs-lookup"><span data-stu-id="ed477-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="ed477-150">`InventoryServiceApplication` paketui:</span><span class="sxs-lookup"><span data-stu-id="ed477-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="ed477-151">Išpakuokite `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="ed477-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="ed477-152">Rasti `InventoryServiceApplication` aplanką, `[Content_Types].xml` failą, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` failą, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` failą ir `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` failą.</span><span class="sxs-lookup"><span data-stu-id="ed477-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="ed477-153">Nukopijuokite kiekvieną iš šių aplankų ir rinkmenų į `.\Tools\PackageDeployment` katalogą, kuris buvo sukurtas įdiegus programuotojo įrankius.</span><span class="sxs-lookup"><span data-stu-id="ed477-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="ed477-154">Vykdyti `.\Tools\PackageDeployment\PackageDeployer.exe`.</span><span class="sxs-lookup"><span data-stu-id="ed477-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="ed477-155">Norėdami importuoti sprendimus vykdykite ekrane pateiktas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="ed477-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="ed477-156">Priskirkite saugos vaidmenis programos vartotojui.</span><span class="sxs-lookup"><span data-stu-id="ed477-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="ed477-157">Atidarykite savo „Dataverse“ aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="ed477-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="ed477-158">Eikite į **išplėstinių parametrų \> sistemos \> saugos \> vartotojus** ir raskite vartotoją **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="ed477-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="ed477-159">Pasirinkite **Priskirti vaidmenį**, tada pasirinkite **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="ed477-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="ed477-160">Jei yra vaidmuo pavadinimu **„Common Data Service“ naudotojas**, pasirinkite jį taip pat.</span><span class="sxs-lookup"><span data-stu-id="ed477-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="ed477-161">Neautomatiniu būdu „Dataverse“ nustatyti importuojant sprendimus</span><span class="sxs-lookup"><span data-stu-id="ed477-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="ed477-162">Jei turite būtinųjų komponentų, naudokite šią procedūrą, jei norite nustatyti „Dataverse“ rankiniu būdu importuojant sprendimus.</span><span class="sxs-lookup"><span data-stu-id="ed477-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="ed477-163">Norėdami gauti daugiau informacijos, kaip naudoti „Package Deployer“ įrankį, žr. ankstesniame skyriuje (ne atlikite abu).</span><span class="sxs-lookup"><span data-stu-id="ed477-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="ed477-164">Sukurkite programos naudotoją „Dataverse“ atsargų matomumui:</span><span class="sxs-lookup"><span data-stu-id="ed477-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="ed477-165">Atidarykite savo „Dataverse“ aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="ed477-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="ed477-166">Eikite į **Išplėstiniai nustatymai \> Sistema \> Sauga \> Naudotojai** ir sukurkite programos naudotoją.</span><span class="sxs-lookup"><span data-stu-id="ed477-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="ed477-167">Naudokite peržiūros meniu, kad puslapio rodinį pakeistumėte į **Programos naudotojai**.</span><span class="sxs-lookup"><span data-stu-id="ed477-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="ed477-168">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ed477-168">Select **New**.</span></span> <span data-ttu-id="ed477-169">Programos ID nustatykite kaip *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="ed477-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="ed477-170">(Išsaugant keitimus objekto ID įkeliamas automatiškai.) Pavadinimą galima pritaikyti.</span><span class="sxs-lookup"><span data-stu-id="ed477-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="ed477-171">Pavyzdžiui, jį galima pakeisti į *Atsargų matomumas*.</span><span class="sxs-lookup"><span data-stu-id="ed477-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="ed477-172">Jums pabaigus, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ed477-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="ed477-173">Pasirinkite **Priskirti vaidmenį**, tada pasirinkite **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="ed477-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="ed477-174">Jei yra vaidmuo pavadinimu **„Common Data Service“ naudotojas**, pasirinkite ir jį.</span><span class="sxs-lookup"><span data-stu-id="ed477-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="ed477-175">Daugiau informacijos žr. skyriuje [Programos naudotojo kūrimas](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="ed477-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="ed477-176">Jei jūsų „Dataverse” numatytoji kalba nėra **Anglų**:</span><span class="sxs-lookup"><span data-stu-id="ed477-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="ed477-177">Eikite į **Išplėstiniai parametrai \> Administravimas \> Kalbos**,</span><span class="sxs-lookup"><span data-stu-id="ed477-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="ed477-178">Pasirinkite **Anglų (LanguageCode=1033)** ir pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="ed477-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="ed477-179">Importuokite failą `Inventory Visibility Dataverse Solution.zip`, kuriame yra su „Dataverse“ konfigūracija susiję objektai ir „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="ed477-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="ed477-180">Eikite į puslapį **Sprendimai**.</span><span class="sxs-lookup"><span data-stu-id="ed477-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="ed477-181">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="ed477-181">Select **Import**.</span></span>

1. <span data-ttu-id="ed477-182">Importuokite konfigūracijos atnaujinimo paleidiklio eigą:</span><span class="sxs-lookup"><span data-stu-id="ed477-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="ed477-183">Eikite į puslapį „Microsoft Flow“.</span><span class="sxs-lookup"><span data-stu-id="ed477-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="ed477-184">Patikrinkite, ar yra ryšys, pavadintas „*Dataverse“ (senesnis)*.</span><span class="sxs-lookup"><span data-stu-id="ed477-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="ed477-185">(Jei ne, sukurkite jį.)</span><span class="sxs-lookup"><span data-stu-id="ed477-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="ed477-186">Importuokite failą `Inventory Visibility Configuration Trigger.zip`.</span><span class="sxs-lookup"><span data-stu-id="ed477-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="ed477-187">Jį importavus srityje **Mano srautai** bus rodomas paleidiklis.</span><span class="sxs-lookup"><span data-stu-id="ed477-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="ed477-188">Inicijuokite šiuos keturis kintamuosius, atsižvelgdami į aplinkos informaciją:</span><span class="sxs-lookup"><span data-stu-id="ed477-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="ed477-189">„Azure“ nuomininko ID</span><span class="sxs-lookup"><span data-stu-id="ed477-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="ed477-190">„Azure“ programos kliento ID</span><span class="sxs-lookup"><span data-stu-id="ed477-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="ed477-191">„Azure“ programos kliento raktas</span><span class="sxs-lookup"><span data-stu-id="ed477-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="ed477-192">Atsargų matomumo galinis punktas</span><span class="sxs-lookup"><span data-stu-id="ed477-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="ed477-193">Daugiau informacijos apie šį kintamąjį žr. toliau šioje temoje pateikiamame skyriuje [Atsargų matomumo integravimo nustatymas](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="ed477-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="ed477-194">![Konfigūracijos paleidiklis](media/configuration-trigger.png "Konfigūracijos paleidiklis")</span><span class="sxs-lookup"><span data-stu-id="ed477-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="ed477-195">Pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="ed477-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="ed477-196">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="ed477-196">Install the add-in</span></span>

<span data-ttu-id="ed477-197">Norėdami įdiegti inventoriaus matomumo papildinį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="ed477-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="ed477-198">Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/Logon/Index) portalo.</span><span class="sxs-lookup"><span data-stu-id="ed477-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="ed477-199">Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.</span><span class="sxs-lookup"><span data-stu-id="ed477-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="ed477-200">Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="ed477-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="ed477-201">Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai**, skyriuje **„Power Platform“ integravimas**, kuriame rasite „Dataverse“ aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ed477-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="ed477-202">Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="ed477-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="ed477-203">![Aplinkos puslapis LCS](media/inventory-visibility-environment.png "Aplinkos puslapis LCS")</span><span class="sxs-lookup"><span data-stu-id="ed477-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="ed477-204">Rinkitės **Diegti naują papildinį** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="ed477-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="ed477-205">Esamų atvirų papildinių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ed477-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="ed477-206">Sąraše pasirinkite **Atsargų matomumas**.</span><span class="sxs-lookup"><span data-stu-id="ed477-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="ed477-207">Įveskite šias vertes savo aplinkos laukeliuose:</span><span class="sxs-lookup"><span data-stu-id="ed477-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="ed477-208">**AAD programos (kliento) ID**</span><span class="sxs-lookup"><span data-stu-id="ed477-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="ed477-209">**ĮTRAUKITE nuomotojo ID**</span><span class="sxs-lookup"><span data-stu-id="ed477-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="ed477-210">![Įtraukite į nustatymų puslapį](media/inventory-visibility-setup.png "Papildinio nustatymus puslapis")</span><span class="sxs-lookup"><span data-stu-id="ed477-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="ed477-211">Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="ed477-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="ed477-212">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="ed477-212">Select **Install**.</span></span> <span data-ttu-id="ed477-213">Papildinio būsena bus rodoma kaip **diegiama**.</span><span class="sxs-lookup"><span data-stu-id="ed477-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="ed477-214">Kai pasibaigs, paleiskite iš naujo puslapį, kad matytumėte būsenos keitimą į **Diegta**.</span><span class="sxs-lookup"><span data-stu-id="ed477-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="ed477-215">Papildinio šalinimas</span><span class="sxs-lookup"><span data-stu-id="ed477-215">Uninstall the add-in</span></span>

<span data-ttu-id="ed477-216">Norėdami išdiegti papildinį, pasirinkite **Išdiegti**.</span><span class="sxs-lookup"><span data-stu-id="ed477-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="ed477-217">Atnaujinus LCS inventoriaus matomumo papildinys bus panaikintas.</span><span class="sxs-lookup"><span data-stu-id="ed477-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="ed477-218">Atlikus išdiegimo procesą pašalinama papildinio registracija ir pradedamas darbas siekiant išvalyti visus verslo duomenis laikomus paslaugose.</span><span class="sxs-lookup"><span data-stu-id="ed477-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="ed477-219">Turimų atsargų duomenų iš „Supply Chain Management” naudojimas</span><span class="sxs-lookup"><span data-stu-id="ed477-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="ed477-220">Aplinkos matomumo integravimo paketo diegimas</span><span class="sxs-lookup"><span data-stu-id="ed477-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="ed477-221">Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą.</span><span class="sxs-lookup"><span data-stu-id="ed477-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="ed477-222">Tada įdiekite paketą LCS.</span><span class="sxs-lookup"><span data-stu-id="ed477-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="ed477-223">Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="ed477-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="ed477-224">Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ed477-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="ed477-225">Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją.</span><span class="sxs-lookup"><span data-stu-id="ed477-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="ed477-226">Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.</span><span class="sxs-lookup"><span data-stu-id="ed477-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="ed477-227">Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ed477-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="ed477-228">(Numatyta, kad jos yra įjungtos.)</span><span class="sxs-lookup"><span data-stu-id="ed477-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="ed477-229">Funkcijos aprašymas</span><span class="sxs-lookup"><span data-stu-id="ed477-229">Feature description</span></span> | <span data-ttu-id="ed477-230">Kodo versija</span><span class="sxs-lookup"><span data-stu-id="ed477-230">Code version</span></span> | <span data-ttu-id="ed477-231">Klasės kaitaliojimas</span><span class="sxs-lookup"><span data-stu-id="ed477-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="ed477-232">Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="ed477-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="ed477-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="ed477-233">10.0.11</span></span> | <span data-ttu-id="ed477-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="ed477-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="ed477-235">Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="ed477-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="ed477-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="ed477-236">10.0.12</span></span> | <span data-ttu-id="ed477-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="ed477-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="ed477-238">Atsargų matomumo integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ed477-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="ed477-239">„Supply Chain Management” atidarykite darbo sritį **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ir įjunkite funkciją **Atsargų matomumo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="ed477-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="ed477-240">Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų matomumo integravimo parametrai** ir įveskite aplinkos, kurioje paleidžiamas atsargų matomumas, URL.</span><span class="sxs-lookup"><span data-stu-id="ed477-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="ed477-241">Raskite savo LCS aplinkos „Azure“ regioną, o tada įveskite URL.</span><span class="sxs-lookup"><span data-stu-id="ed477-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="ed477-242">URL forma yra tokia:</span><span class="sxs-lookup"><span data-stu-id="ed477-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="ed477-243">Pavyzdžiui, jei esate Europoje, jūsų aplinkos URL bus vienas iš šių:</span><span class="sxs-lookup"><span data-stu-id="ed477-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="ed477-244">Šiuo metu naudojami nurodyti regionai.</span><span class="sxs-lookup"><span data-stu-id="ed477-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="ed477-245">„Azure“ regionas</span><span class="sxs-lookup"><span data-stu-id="ed477-245">Azure region</span></span> | <span data-ttu-id="ed477-246">Trumpas regiono pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ed477-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="ed477-247">Rytų Australija</span><span class="sxs-lookup"><span data-stu-id="ed477-247">Australia east</span></span> | <span data-ttu-id="ed477-248">eau</span><span class="sxs-lookup"><span data-stu-id="ed477-248">eau</span></span> |
    | <span data-ttu-id="ed477-249">Pietryčių Australija</span><span class="sxs-lookup"><span data-stu-id="ed477-249">Australia southeast</span></span> | <span data-ttu-id="ed477-250">seau</span><span class="sxs-lookup"><span data-stu-id="ed477-250">seau</span></span> |
    | <span data-ttu-id="ed477-251">Centrinė Kanada</span><span class="sxs-lookup"><span data-stu-id="ed477-251">Canada central</span></span> | <span data-ttu-id="ed477-252">cca</span><span class="sxs-lookup"><span data-stu-id="ed477-252">cca</span></span> |
    | <span data-ttu-id="ed477-253">Rytų Kanada</span><span class="sxs-lookup"><span data-stu-id="ed477-253">Canada east</span></span> | <span data-ttu-id="ed477-254">eca</span><span class="sxs-lookup"><span data-stu-id="ed477-254">eca</span></span> |
    | <span data-ttu-id="ed477-255">Šiaurės Europa</span><span class="sxs-lookup"><span data-stu-id="ed477-255">North Europe</span></span> | <span data-ttu-id="ed477-256">neu</span><span class="sxs-lookup"><span data-stu-id="ed477-256">neu</span></span> |
    | <span data-ttu-id="ed477-257">Vakarų Europa</span><span class="sxs-lookup"><span data-stu-id="ed477-257">West Europe</span></span> | <span data-ttu-id="ed477-258">weu</span><span class="sxs-lookup"><span data-stu-id="ed477-258">weu</span></span> |
    | <span data-ttu-id="ed477-259">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="ed477-259">East US</span></span> | <span data-ttu-id="ed477-260">eus</span><span class="sxs-lookup"><span data-stu-id="ed477-260">eus</span></span> |
    | <span data-ttu-id="ed477-261">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="ed477-261">West US</span></span> | <span data-ttu-id="ed477-262">wus</span><span class="sxs-lookup"><span data-stu-id="ed477-262">wus</span></span> |

1. <span data-ttu-id="ed477-263">Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį.</span><span class="sxs-lookup"><span data-stu-id="ed477-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="ed477-264">Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.</span><span class="sxs-lookup"><span data-stu-id="ed477-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="ed477-265">Vieša inventoriaus matomumo API</span><span class="sxs-lookup"><span data-stu-id="ed477-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="ed477-266">Vieša REST API inventoriaus matomumo papildinio nustatymuose nurodo kai kuriuos integravimo galutinius taškus.</span><span class="sxs-lookup"><span data-stu-id="ed477-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="ed477-267">Jis palaiko tris pagrindines sąveikos rūšis:</span><span class="sxs-lookup"><span data-stu-id="ed477-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="ed477-268">Turimų atsargų pakeitimų į papildinio formą išorės sistemoje registravimas</span><span class="sxs-lookup"><span data-stu-id="ed477-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="ed477-269">Dabartinių turimų kiekių užklausos iš išorės sistemos</span><span class="sxs-lookup"><span data-stu-id="ed477-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="ed477-270">Automatinis sinchronizavimas su turimomis „Supply Chain Management“ atsargomis.</span><span class="sxs-lookup"><span data-stu-id="ed477-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="ed477-271">Automatinis sinchronizavimas nėra viešosios API dalis.</span><span class="sxs-lookup"><span data-stu-id="ed477-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="ed477-272">Vietoje to jis tvarkomas fone, aplinkoms, kuriose įjungtas atsargų matomumo priedas.</span><span class="sxs-lookup"><span data-stu-id="ed477-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="ed477-273">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="ed477-273">Authentication</span></span>

<span data-ttu-id="ed477-274">Platformos saugos atpažinimo ženklas naudojamas atsargų matomumo priedui iškviesti.</span><span class="sxs-lookup"><span data-stu-id="ed477-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="ed477-275">Todėl turite sugeneruoti *„Azure Active Directory“ („Azure AD“) atpažinimo ženklą*, naudodami savo „Azure AD“ programą.</span><span class="sxs-lookup"><span data-stu-id="ed477-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="ed477-276">Tada turite naudoti „Azure AD“ atpažinimo ženklą, kad iš saugos tarnybos gautumėte *prieigos atpažinimo ženklą*.</span><span class="sxs-lookup"><span data-stu-id="ed477-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="ed477-277">Gaukite saugos paslaugų žymą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="ed477-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="ed477-278">Prisijunkite prie „Azure” portalo ir naudokite jį rasti `clientId` ir `clientSecret` jūsų „Supply Chain Management” programai.</span><span class="sxs-lookup"><span data-stu-id="ed477-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="ed477-279">Iškvieskite „Azure Active Directory” atpažinimo ženklą (`aadToken`) pateikdami HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="ed477-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="ed477-280">**„URL”** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="ed477-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="ed477-281">**Metodas** - `GET`</span><span class="sxs-lookup"><span data-stu-id="ed477-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="ed477-282">**Teksto turinys (formos duomenys)**:</span><span class="sxs-lookup"><span data-stu-id="ed477-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="ed477-283">raktas</span><span class="sxs-lookup"><span data-stu-id="ed477-283">key</span></span> | <span data-ttu-id="ed477-284">vertė</span><span class="sxs-lookup"><span data-stu-id="ed477-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="ed477-285">„client_id”</span><span class="sxs-lookup"><span data-stu-id="ed477-285">client_id</span></span> | <span data-ttu-id="ed477-286">„${aadAppId}“</span><span class="sxs-lookup"><span data-stu-id="ed477-286">${aadAppId}</span></span> |
        | <span data-ttu-id="ed477-287">„client_secret”</span><span class="sxs-lookup"><span data-stu-id="ed477-287">client_secret</span></span> | <span data-ttu-id="ed477-288">„${aadAppSecret}“</span><span class="sxs-lookup"><span data-stu-id="ed477-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="ed477-289">„grant_type”</span><span class="sxs-lookup"><span data-stu-id="ed477-289">grant_type</span></span> | <span data-ttu-id="ed477-290">„client_credentials”</span><span class="sxs-lookup"><span data-stu-id="ed477-290">client_credentials</span></span> |
        | <span data-ttu-id="ed477-291">ištekliai</span><span class="sxs-lookup"><span data-stu-id="ed477-291">resource</span></span> | <span data-ttu-id="ed477-292">„0cdb527f-a8d1-4bf8-9436-b352c68682b2“</span><span class="sxs-lookup"><span data-stu-id="ed477-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="ed477-293">Turėtumėte gauti `aadToken` kaip atsakymą, panašų į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="ed477-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="ed477-294">Suformuluokite JSON užklausą, panašią į šią:</span><span class="sxs-lookup"><span data-stu-id="ed477-294">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="ed477-295">Kur:</span><span class="sxs-lookup"><span data-stu-id="ed477-295">Where:</span></span>
    - <span data-ttu-id="ed477-296">Reikšmė `client_assertion` turi būti `aadToken`, kurį gavote ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="ed477-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="ed477-297">Reikšmė `context` turi būti aplinkos ID, kuriame norite diegti papildinį.</span><span class="sxs-lookup"><span data-stu-id="ed477-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="ed477-298">Nustatykite visas kitas reikšmes, kaip parodyta pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="ed477-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="ed477-299">Pateikite HTTP užklausą su šiomis ypatybes:</span><span class="sxs-lookup"><span data-stu-id="ed477-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="ed477-300">**„URL”** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="ed477-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="ed477-301">**Metodas** - `POST`</span><span class="sxs-lookup"><span data-stu-id="ed477-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="ed477-302">**HTTP antraštė** – įtraukite API versiją (raktas yra `Api-Version` ir reikšmė yra `1.0`)</span><span class="sxs-lookup"><span data-stu-id="ed477-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="ed477-303">**Teksto turinys** – įtraukite JSON užklausą, kurią sukūrėte ankstesniu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="ed477-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="ed477-304">Gausite  `access_token` atsakyme.</span><span class="sxs-lookup"><span data-stu-id="ed477-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="ed477-305">Dėl to jums reikia geresnės žymos siekiant iškviesti inventoriaus papildinio API.</span><span class="sxs-lookup"><span data-stu-id="ed477-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="ed477-306">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ed477-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="ed477-307">Užklausos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ed477-307">Sample Request</span></span>

<span data-ttu-id="ed477-308">Jūsų nuorodai, čia yra http užklausos pavyzdys, jūs galite naudoti bet kokius įrankius ar kodavimo kalbą šiai užklausai išsiųsti, pavyzdžiui ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="ed477-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

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

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="ed477-309">Konfigūruoti Inventoriaus matomumo vieša API</span><span class="sxs-lookup"><span data-stu-id="ed477-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="ed477-310">Prieš naudodami paslaugas, turite užbaigti konfigūravimus aprašytus tolesniuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="ed477-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="ed477-311">Konfigūravimas gali skirtis priklausomai nuo jūsų aplinkos išsamios informacijos.</span><span class="sxs-lookup"><span data-stu-id="ed477-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="ed477-312">Jis iš esmės turi keturias dalis:</span><span class="sxs-lookup"><span data-stu-id="ed477-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="ed477-313">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="ed477-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="ed477-314">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="ed477-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="ed477-315">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="ed477-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="ed477-316">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="ed477-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="ed477-317">Dalijimas</span><span class="sxs-lookup"><span data-stu-id="ed477-317">Partitioning</span></span>

<span data-ttu-id="ed477-318">Dalijimas gali stipriai paveikti matomumo papildinio veikimą.</span><span class="sxs-lookup"><span data-stu-id="ed477-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="ed477-319">Gera mintis būtų nustatyti schemą, kuri leidžia mažoms duomenų grupėms veikti vis dar leidžiant svarbias duomenų užklausa.</span><span class="sxs-lookup"><span data-stu-id="ed477-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="ed477-320">Visuomet `organizationId` (`dataAreaId` „Supply Chain Management“) bus dalijimo dalis ir pagal nutylėjimą papildinys nustatytas į dimensijų dalijimą kaip *Saitas + Vieta*.</span><span class="sxs-lookup"><span data-stu-id="ed477-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="ed477-321">Tai reiškia, kad paslaugos turi būti visuomet laukiamos su šia dimensija filtruose.</span><span class="sxs-lookup"><span data-stu-id="ed477-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="ed477-322">*Saitas* ir *Vieta* yra dvi pagrindinės dimensijos inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="ed477-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="ed477-323">„Supply Chain Management“ dimensijos yra vadinamos *Saitas* (`InventSiteId`) ir *Sandėlis* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="ed477-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="ed477-324">Dimensijos konfigūravimai</span><span class="sxs-lookup"><span data-stu-id="ed477-324">Dimension configurations</span></span>

<span data-ttu-id="ed477-325">Inventoriaus matomumas suteikia pagrindinių numatytų dimensijų sąrašą siekiant integruoti kelis sistemos išteklius.</span><span class="sxs-lookup"><span data-stu-id="ed477-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="ed477-326">Tolesnė lentelė pateikia inventoriaus dimensijas, kurios bus numatytieji vardai inventoriaus papildinyje.</span><span class="sxs-lookup"><span data-stu-id="ed477-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="ed477-327">Dimensijos tipas</span><span class="sxs-lookup"><span data-stu-id="ed477-327">Dimension type</span></span> | <span data-ttu-id="ed477-328">Dimensijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ed477-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="ed477-329">Produktas</span><span class="sxs-lookup"><span data-stu-id="ed477-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="ed477-330">Produktas</span><span class="sxs-lookup"><span data-stu-id="ed477-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="ed477-331">Produktas</span><span class="sxs-lookup"><span data-stu-id="ed477-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="ed477-332">Produktas</span><span class="sxs-lookup"><span data-stu-id="ed477-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="ed477-333">Sekimas</span><span class="sxs-lookup"><span data-stu-id="ed477-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="ed477-334">Sekimas</span><span class="sxs-lookup"><span data-stu-id="ed477-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="ed477-335">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="ed477-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="ed477-336">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="ed477-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="ed477-337">Inventoriaus būsena</span><span class="sxs-lookup"><span data-stu-id="ed477-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="ed477-338">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="ed477-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="ed477-339">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="ed477-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="ed477-340">Sandėliui konkretus</span><span class="sxs-lookup"><span data-stu-id="ed477-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="ed477-341">Dimensijos tipas įrašytas ankstesnėje lentelėje tik nuorodų tikslais.</span><span class="sxs-lookup"><span data-stu-id="ed477-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="ed477-342">Jums nereikia nustatyti dimensijos tipo inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="ed477-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="ed477-343">Jei tinkinta dimensija yra ir jai reikia patekti į eigą į numatytąją vertę, kai suvartojama inventoriaus matomume, ją galite konfigūruoti **TInkinta dimensija** pavadinime inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="ed477-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="ed477-344">Išorės sistemos prieiga prie „Inventory Visibility“ per RESTful API, kurios leidžia turėti informaciją pagal suteiktus laukiančius dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="ed477-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="ed477-345">Dėl integravimo inventoriaus matomumas jums leidžia konfigūruoti *išorės kanalo duomenų šaltinį* ir šaltinio nurodymą *tikslinis nurodymas* inventoriaus matomume.</span><span class="sxs-lookup"><span data-stu-id="ed477-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="ed477-346">Tikslines nurodymas turi būti vienas iš:</span><span class="sxs-lookup"><span data-stu-id="ed477-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="ed477-347">Numatyti Inventoriaus matomumo nurodymai</span><span class="sxs-lookup"><span data-stu-id="ed477-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="ed477-348">Pasirinktinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="ed477-348">Custom dimensions</span></span>

<span data-ttu-id="ed477-349">Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai dimensijose ir publikuoti įvykį su dimensijomis.</span><span class="sxs-lookup"><span data-stu-id="ed477-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="ed477-350">Indeksavimas</span><span class="sxs-lookup"><span data-stu-id="ed477-350">Indexing</span></span>

<span data-ttu-id="ed477-351">Didžiąją laiko dalį, inventoriaus turima užklausa nebus tik aukščiausia „bendra“ reikšmė, bet galite matyti rezultatus apibendrintus pagal inventoriaus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="ed477-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="ed477-352">Inventoriaus matomumas suteikia lankstumo ir leidžia jums nustatyti indeksavimą, kurie paremti nurodymu ir jų deriniu.</span><span class="sxs-lookup"><span data-stu-id="ed477-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="ed477-353">Šiuo metu galite konfigūruoti indeksu iki daugiausiai penkių.</span><span class="sxs-lookup"><span data-stu-id="ed477-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="ed477-354">Turite atsargiai apgalvoti, kurie nurodymai ar derinys bus naudojamas siekiant įdiegti užtikrinant, kad atitiks jis jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="ed477-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="ed477-355">Pavyzdžiui, jei norite laukti produktų tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="ed477-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="ed477-356">Laukti bendrintų produktų turimų *Spalva* ir *Dydis* nurodymuose.</span><span class="sxs-lookup"><span data-stu-id="ed477-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="ed477-357">Kai kada norite tik laukti produkto bendrai.</span><span class="sxs-lookup"><span data-stu-id="ed477-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="ed477-358">Turite du indeksus nustatytus kaip:</span><span class="sxs-lookup"><span data-stu-id="ed477-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="ed477-359">Tuštinkite skliaustelius pagal produkto ID su dalijimu.</span><span class="sxs-lookup"><span data-stu-id="ed477-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="ed477-360">Indeksavimas nustato, kaip galite grupuoti savo rezultatus pagal `groupBy` laukimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="ed477-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="ed477-361">Tokiu atveju, jei nenustatėte jokių `groupBy` verčių, gausite bendrus `productid`.</span><span class="sxs-lookup"><span data-stu-id="ed477-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="ed477-362">Kitaip, jei nustatėte `groupBy` kaip `groupBy=ColorId&groupBy=SizeId`, gausite padaugintas eilutes grąžintas pagal kitą spalvą ir dydžio derinius sistemoje.</span><span class="sxs-lookup"><span data-stu-id="ed477-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="ed477-363">Galite padėti savo laukimo kriterijus pagal būtiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="ed477-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="ed477-364">Čia yra pavyzdys laukimui gaminiui su spalvos ir dydžio deriniu.</span><span class="sxs-lookup"><span data-stu-id="ed477-364">Here is a sample query on the product with color and size combination.</span></span>

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

<span data-ttu-id="ed477-365">Šiuo metu iš lauko `filters` tik `ProductId` palaiko kelias reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ed477-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="ed477-366">Jei `ProductId` yra tuščias masyvas, bus pateiktos visų produktų užklausos.</span><span class="sxs-lookup"><span data-stu-id="ed477-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="ed477-367">Tinkintas matavimas</span><span class="sxs-lookup"><span data-stu-id="ed477-367">Custom measurement</span></span>

<span data-ttu-id="ed477-368">Numatytieji matavimo kiekiai yra siejami su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="ed477-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="ed477-369">Tačiau gali reikėti kiekio, kuris būtų pagamintas iš numatytųjų matavimų kombinacijos.</span><span class="sxs-lookup"><span data-stu-id="ed477-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="ed477-370">Tam, turite turėti tinkintų kiekių konfigūravimą, kuris bus įtrauktas į išvesties turimas užklausas.</span><span class="sxs-lookup"><span data-stu-id="ed477-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="ed477-371">Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.</span><span class="sxs-lookup"><span data-stu-id="ed477-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="ed477-372">Pavyzdžiui, tolesnė laukimo sąlygas, ji konfigūruos tinkintų priemonių kiekį kaip `MyCustomAvailableforReservation` tam, kad būtų suvartota vartojimo sistemos.</span><span class="sxs-lookup"><span data-stu-id="ed477-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="ed477-373">Vartojimo sistema</span><span class="sxs-lookup"><span data-stu-id="ed477-373">Consumption system</span></span> | <span data-ttu-id="ed477-374">Skaičiuotos priemonės</span><span class="sxs-lookup"><span data-stu-id="ed477-374">Calculated measurers</span></span> | <span data-ttu-id="ed477-375">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="ed477-375">Data source</span></span> | <span data-ttu-id="ed477-376">Keitikas</span><span class="sxs-lookup"><span data-stu-id="ed477-376">Modifier</span></span> | <span data-ttu-id="ed477-377">Keitiko apskaičiavimo tipas</span><span class="sxs-lookup"><span data-stu-id="ed477-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="ed477-378">Priedas</span><span class="sxs-lookup"><span data-stu-id="ed477-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="ed477-379">Priedas</span><span class="sxs-lookup"><span data-stu-id="ed477-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="ed477-380">Atimtis</span><span class="sxs-lookup"><span data-stu-id="ed477-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="ed477-381">Priedas</span><span class="sxs-lookup"><span data-stu-id="ed477-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="ed477-382">Atimtis</span><span class="sxs-lookup"><span data-stu-id="ed477-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="ed477-383">Priedas</span><span class="sxs-lookup"><span data-stu-id="ed477-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="ed477-384">Priedas</span><span class="sxs-lookup"><span data-stu-id="ed477-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="ed477-385">Atimtis</span><span class="sxs-lookup"><span data-stu-id="ed477-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="ed477-386">Atimtis</span><span class="sxs-lookup"><span data-stu-id="ed477-386">Subtraction</span></span> |

<span data-ttu-id="ed477-387">Su tuo, laukimas tinkinto matavimo kiekyje grįš į tolesnę išvestį.</span><span class="sxs-lookup"><span data-stu-id="ed477-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="ed477-388">Išvestis `MyCustomAvailableforReservation` paremta apskaičiavimo nustatymais tinkintuose matavimuose:</span><span class="sxs-lookup"><span data-stu-id="ed477-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="ed477-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="ed477-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="ed477-390">Turimų keitimų publikavimas</span><span class="sxs-lookup"><span data-stu-id="ed477-390">Posting on-hand changes</span></span>

<span data-ttu-id="ed477-391">Tikslus URL, į kurį bus publikuojamas įvykis bus publikuojamas priklausomai nuo geografinio regiono.</span><span class="sxs-lookup"><span data-stu-id="ed477-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="ed477-392">Jo forma bus:</span><span class="sxs-lookup"><span data-stu-id="ed477-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="ed477-393">Kai jis autentifikuotas, šis URL gali būti naudojamas kartu su HTTP `POST` metodu, kad siųstumėte turimus keitimo įvykius į paslaugas.</span><span class="sxs-lookup"><span data-stu-id="ed477-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="ed477-394">Konkreti antraštė naudojamas siekiant pranešti su „Dynamics 365“ paslaugomis per HTTP užklausas nustatant aplinkos ID „Supply Chain Management“ elemento duomenis su juo susietais.</span><span class="sxs-lookup"><span data-stu-id="ed477-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="ed477-395">Pvz.:</span><span class="sxs-lookup"><span data-stu-id="ed477-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="ed477-396">Publikavimo turimų keitimų laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="ed477-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="ed477-397">Šis pavyzdys rodo scenarijų, kai jau nustatėte dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="ed477-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="ed477-398">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="ed477-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="ed477-399">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="ed477-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="ed477-400">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="ed477-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="ed477-401">Publikavimo turimų keitimų laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="ed477-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="ed477-402">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="ed477-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="ed477-403">Visos dimensijos turi būti pagrindinės, kai  `dimensionDataSource` laukelis yra nulio reikšmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="ed477-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="ed477-404">JSON dokumento laukelio ypatybės</span><span class="sxs-lookup"><span data-stu-id="ed477-404">JSON document field properties</span></span>

<span data-ttu-id="ed477-405">Laukeliai iš JSON užklausų pavyzdžių, pateikti anksčiau turi ypatybes išvardytas tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="ed477-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="ed477-406">Lauko ID</span><span class="sxs-lookup"><span data-stu-id="ed477-406">Field ID</span></span> | <span data-ttu-id="ed477-407">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ed477-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="ed477-408">Unikalus ID konkrečiam keitimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="ed477-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="ed477-409">Šis ID naudojamas siekiant užtikrinti, kad jei komunikacija su paslaugomis nepavyksta publikavimo metu, pakartotinis pateikimo įvykis nevyks tame pačiame taške sistemai skaičiuojant dukart.</span><span class="sxs-lookup"><span data-stu-id="ed477-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="ed477-410">Organizacijos identifikatorius susietas su įvykiu.</span><span class="sxs-lookup"><span data-stu-id="ed477-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="ed477-411">Tai patalpina „Supply Chain Management“ organizacijas ar duomenų srities ID.</span><span class="sxs-lookup"><span data-stu-id="ed477-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="ed477-412">Aptariamas produkto identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="ed477-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="ed477-413">Kiekis, pagal kurį turimi poreikiai keičiami.</span><span class="sxs-lookup"><span data-stu-id="ed477-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="ed477-414">Jeigu, pavyzdžiui, 10 naujų riestainių buvo įtraukti į lentyną, vertė yra 10.</span><span class="sxs-lookup"><span data-stu-id="ed477-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="ed477-415">Jei 3 riestainiai buvo pašalinti nuo lentynos ar parduoti, ši vertė bus -3.</span><span class="sxs-lookup"><span data-stu-id="ed477-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="ed477-416">Duomenų šaltinio dimensijų naudojimas publikavimo keitimo įvykyje ir eilėje.</span><span class="sxs-lookup"><span data-stu-id="ed477-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="ed477-417">Jei nurodėte duomenų šaltinį, galite naudoti tinkintas dimensijas iš konkretaus duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="ed477-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="ed477-418">Su dimensijos konfigūravimu, inventoriaus matomumas gali žymėti tinkintas dimensijas į bendras nustatytas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="ed477-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="ed477-419">Jei `dimensionDataSource` nenurodyta, galite tik naudoti bendras numatytąsias dimensijas savo eilėse.</span><span class="sxs-lookup"><span data-stu-id="ed477-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="ed477-420">Dinaminis rakto maišas/verčių poros.</span><span class="sxs-lookup"><span data-stu-id="ed477-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="ed477-421">Jos nustatys keletą dimensijų „Supply Chain Management“, tačiau galite taip pat įtraukti tinkintas dimensijas (tokias kaip *Šaltinis*), kurios nustatys, ar įvykis ateina iš „Supply Chain Management“ ar išorės sistemos.</span><span class="sxs-lookup"><span data-stu-id="ed477-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="ed477-422">Esamas turimas laukimas</span><span class="sxs-lookup"><span data-stu-id="ed477-422">Querying current on-hand</span></span>

<span data-ttu-id="ed477-423">Laukimo galutinis taškas esamame turimame bus panašus URL:</span><span class="sxs-lookup"><span data-stu-id="ed477-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="ed477-424">Jis bus laukiamas su HTTP `POST` metodu.</span><span class="sxs-lookup"><span data-stu-id="ed477-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="ed477-425">Esamas turimas laukimo pavyzdys 1</span><span class="sxs-lookup"><span data-stu-id="ed477-425">Current on-hand query example 1</span></span>

<span data-ttu-id="ed477-426">Šis pavyzdys rodo scenarijų, kai jau turite baigtą dimensijos konfigūravimą „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="ed477-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="ed477-427">Naudokite tolesnę užklausą norėdami konfigūruoti dimensijos žemėlapį „Power Apps“:</span><span class="sxs-lookup"><span data-stu-id="ed477-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="ed477-428">Atsiminkite, kad galite nustatyti `dimensionDataSource` ir naudoti tinkintas dimensijas savo užklausose.</span><span class="sxs-lookup"><span data-stu-id="ed477-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="ed477-429">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="ed477-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="ed477-430">Galite nustatyti `DimensionDataSource` esančius `filters` ir nurodyti tinkintas dimensijas tiek `filters` , tiek ir `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="ed477-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="ed477-431">Sistema automatiškai pavers tinkintas dimensijas į pagrindines.</span><span class="sxs-lookup"><span data-stu-id="ed477-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="ed477-432">Esamas turimas laukimo pavyzdys 2</span><span class="sxs-lookup"><span data-stu-id="ed477-432">Current on-hand query example 2</span></span>

<span data-ttu-id="ed477-433">Pavyzdys rodo scenarijų, kuriame jokie žemėlapiai nenustatyti dimensijos konfigūravimui „Power Apps“, todėl publikavimas taip pat turi naudoti pagrindinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="ed477-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="ed477-434">Visos dimensijos turi būti pagrindinės, kai `dimensionDataSource` laukelis skyriuje `filters` yra nulio reikšmės, tuščias ar balta erdvė.</span><span class="sxs-lookup"><span data-stu-id="ed477-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="ed477-435">Grįžtamojo rezultato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ed477-435">Example return result</span></span>

<span data-ttu-id="ed477-436">Laukimas rodomas ankstesniuose pavyzdžiuose gali grįžti kaip rezultatas.</span><span class="sxs-lookup"><span data-stu-id="ed477-436">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="ed477-437">Pastebėkite, kad kiekių laukeliai yra struktūruoti kaip priemonių žodynas ir su jomis susijusios vertės.</span><span class="sxs-lookup"><span data-stu-id="ed477-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
