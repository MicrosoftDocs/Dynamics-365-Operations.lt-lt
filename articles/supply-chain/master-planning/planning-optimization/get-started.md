---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d12e1908e234c841fb705266b2255c6c5e2140e1
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103598"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="5d114-103">Darbo su planavimo optimizavimu pradžia</span><span class="sxs-lookup"><span data-stu-id="5d114-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d114-104">Kaip buvo [nurodyta anksčiau](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), numatoma, kad „Planning Optimization“ pakeis esamą integruotą bendrojo planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="5d114-104">As [previously announced](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="5d114-105">Jei šiuo metu naudojate integruotą bendrojo planavimo mechanizmą, turite pradėti galvoti apie perėjimą prie „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="5d114-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="5d114-106">Svarbu iš karto pradėti perėjimo procesą, nes tai gali turėti jūsų darbui, kai senesnė versija taps nebenaudojama.</span><span class="sxs-lookup"><span data-stu-id="5d114-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="5d114-107">Tam, kad išvengtumėte problemų, kai senesnė versija taps nebenaudojama, primygtinai rekomenduojame baigti perėjimą iki 2020 m. gruodžio 1 d.</span><span class="sxs-lookup"><span data-stu-id="5d114-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="5d114-108">„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, integruotame „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="5d114-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="5d114-109">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="5d114-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="5d114-110">„Planning Optimization“ funkcija šiuo metu nėra įjungta „Dynamics Lifecycle Services“ (LCS) esant numatytiesiems parametrams, todėl jūs turite galimybę atlikti savo vertinimą prieš įjungiant funkciją.</span><span class="sxs-lookup"><span data-stu-id="5d114-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="5d114-111">Jums reikia prašyti išimties, kad galėtumėte nepereiti prie „Planning Optimization“, jei bendrojo planavimo procesas neapima gamybos (bendrojo planavimo sugeneruotų suplanuotų gamybos užsakymų) ir jums reikia 10.0.15 arba senesnės integruoto bendrojo planavimo mechanizmo versijos.</span><span class="sxs-lookup"><span data-stu-id="5d114-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="5d114-112">Pradedant nuo 10.0.16 versijos, bandant paleisti integruotą bendrąjį planavimą be suplanuotų gamybos užsakymų generavimo, bus rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="5d114-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="5d114-113">„Planning Optimization“ turi būti naudojama visiems naujiems įdiegimams, kurie negeneruoja suplanuotų gamybos užsakymų atliekant bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="5d114-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="5d114-114">Esamų aplinkų savininkai, leisdami integruotą bendrojo planavimo mechanizmą be suplanuotų gamybos užsakymų, gaus laiškus, kuriuose pateikiama informacija apie išimties procesą.</span><span class="sxs-lookup"><span data-stu-id="5d114-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="5d114-115">Rekomenduojame kartu su partneriu įvertinti ir planuoti perėjimą prie „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="5d114-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="5d114-116">Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus.</span><span class="sxs-lookup"><span data-stu-id="5d114-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="5d114-117">Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5d114-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="5d114-118">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="5d114-118">Availability</span></span>

<span data-ttu-id="5d114-119">Šiuo metu planavimo optimizavimas pasiekiamas tolesniuose „Azure” regionuose: Jungtinėse Valstijose, Kanadoje, Europoje, Jungtinėje Karalystėje, Australijoje ir Azijos ir Ramiojo vandenyno.</span><span class="sxs-lookup"><span data-stu-id="5d114-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="5d114-120">Jei bandote įdiegti papildinį kitame geografiniame regione, LCS rodys pranešimą, nurodantį, kad šis regionas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="5d114-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="5d114-121">Turėkite omenyje, kad planavimo optimizavimas nepalaiko vietinių visuotinių „Dynamics 365 Supply Chain Management” diegimų.</span><span class="sxs-lookup"><span data-stu-id="5d114-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="5d114-122">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="5d114-122">Licensing</span></span>

<span data-ttu-id="5d114-123">Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="5d114-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="5d114-124">„Planning Optimization“ diegimas ir įgalinimas</span><span class="sxs-lookup"><span data-stu-id="5d114-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="5d114-125">Norėdami naudoti „Planning Optimization”, turite įsitikinti, kad sistemoje yra visos būtinosios sąlygos, tada įgalinti jos licencijos raktą ir įdiegti „Planning Optimization” priedą, skirtą „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="5d114-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5d114-126">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="5d114-126">Prerequisites</span></span>

<span data-ttu-id="5d114-127">Prieš diegiant „Planning Optimization” priedą, turi būti įgyvendintos šios būtinosios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="5d114-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="5d114-128">Privalote vykdyti „Supply Chain Management” su įgalinta LCS plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinčia „Dynamics 365 Supply Chain Management” 10.0.7 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="5d114-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="5d114-129">Jei bandote įdiegti papildinį „OneBox” aplinkoje, diegimas nebus užbaigtas ir jį reikės atšaukti.</span><span class="sxs-lookup"><span data-stu-id="5d114-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="5d114-130">Jūsų sistema turi būti nustatyta „Power Platform” integravimui.</span><span class="sxs-lookup"><span data-stu-id="5d114-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="5d114-131">Daugiau informacijos rasite [„Microsoft Power Platform” integravimas su „Finance and Operations” programomis](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5d114-131">For more information, see [Microsoft Power Platform integration with Finance and Operations apps](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="5d114-132">„Planning Optimization“ licencijos įgalinimas</span><span class="sxs-lookup"><span data-stu-id="5d114-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="5d114-133">Norėdami naudoti „Planning Optimization”, turite įgalinti jo konfigūracijos raktą.</span><span class="sxs-lookup"><span data-stu-id="5d114-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="5d114-134">Norėdami tai padaryti:</span><span class="sxs-lookup"><span data-stu-id="5d114-134">To do so:</span></span>

1. <span data-ttu-id="5d114-135">Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="5d114-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="5d114-136">Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="5d114-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="5d114-137">Skirtuke **Konfigūracijos raktai** pasirinkite žymės langelį **Planavimo optimizavimas**.</span><span class="sxs-lookup"><span data-stu-id="5d114-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="5d114-138">Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="5d114-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="5d114-139">„Planning Optimization“ priedo diegimas</span><span class="sxs-lookup"><span data-stu-id="5d114-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="5d114-140">Turite įdiegti papildinį savo LCS projekte ir tada įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="5d114-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="5d114-141">Norėdami įdiegti „Planning Optimization“ priedą:</span><span class="sxs-lookup"><span data-stu-id="5d114-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="5d114-142">Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="5d114-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="5d114-143">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="5d114-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="5d114-144">Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="5d114-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="5d114-145">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="5d114-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="5d114-146">Pasirinkite **Planavimo optimizavimas**.</span><span class="sxs-lookup"><span data-stu-id="5d114-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="5d114-147">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="5d114-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="5d114-148">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="5d114-148">Select **Install**.</span></span>
1. <span data-ttu-id="5d114-149">„FastTab“ **Aplinkos papildiniai** turėtumėte matyti, kad planavimo optimizavimas yra diegiamas.</span><span class="sxs-lookup"><span data-stu-id="5d114-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="5d114-150">Po kelių minučių būsena **Diegiama** turėtų pasikeisti į **Įdiegta** (jums gali prireikti atnaujinti puslapį).</span><span class="sxs-lookup"><span data-stu-id="5d114-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="5d114-151">Baigus diegti galite aktyvinti planavimo optimizavimą programoje „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="5d114-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="5d114-152">Pagrindinis „Planning Optimization“ papildinio diegimo tikslas yra susieti paslaugas ir aplinką.</span><span class="sxs-lookup"><span data-stu-id="5d114-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="5d114-153">Dėl to, privalote įdiegti papildinį atskirai kiekvienoje aplinkoje, kurioje naudosite „Planning Optimization“ nepriklausomai nuo bet kokio kodo perkelto tarp aplinkų.</span><span class="sxs-lookup"><span data-stu-id="5d114-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="5d114-154">„Planning Optimization” integravimas su jūsų sistema</span><span class="sxs-lookup"><span data-stu-id="5d114-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="5d114-155">Norėdami sukonfigūruoti, ar planavimo optimizavimo papildinys turi būti naudojamas bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5d114-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="5d114-156">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="5d114-156">Connection status</span></span>

<span data-ttu-id="5d114-157">Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną.</span><span class="sxs-lookup"><span data-stu-id="5d114-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="5d114-158">Lentelėje pateiktos galimės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="5d114-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="5d114-159">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="5d114-159">Connection status</span></span> | <span data-ttu-id="5d114-160">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="5d114-160">Description</span></span> | <span data-ttu-id="5d114-161">Ar galima naudoti „Planning Optimization“?</span><span class="sxs-lookup"><span data-stu-id="5d114-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="5d114-162">Prisijungta</span><span class="sxs-lookup"><span data-stu-id="5d114-162">Connected</span></span> | <span data-ttu-id="5d114-163">Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="5d114-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="5d114-164">Taip</span><span class="sxs-lookup"><span data-stu-id="5d114-164">Yes</span></span> |
| <span data-ttu-id="5d114-165">Įjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="5d114-165">Enabling connection</span></span> | <span data-ttu-id="5d114-166">Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="5d114-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5d114-167">Ne</span><span class="sxs-lookup"><span data-stu-id="5d114-167">No</span></span> |
| <span data-ttu-id="5d114-168">Atsijungta</span><span class="sxs-lookup"><span data-stu-id="5d114-168">Disconnected</span></span> | <span data-ttu-id="5d114-169">Nėra ryšio su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="5d114-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="5d114-170">Ryšį galima įjungti iš LCS, kaip pirmiau aprašyta šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="5d114-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="5d114-171">Ne</span><span class="sxs-lookup"><span data-stu-id="5d114-171">No</span></span> |
| <span data-ttu-id="5d114-172">Išjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="5d114-172">Disabling connection</span></span> | <span data-ttu-id="5d114-173">Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="5d114-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="5d114-174">Ne</span><span class="sxs-lookup"><span data-stu-id="5d114-174">No</span></span> |
| <span data-ttu-id="5d114-175">Gavimo būsena</span><span class="sxs-lookup"><span data-stu-id="5d114-175">Getting status</span></span> | <span data-ttu-id="5d114-176">Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos.</span><span class="sxs-lookup"><span data-stu-id="5d114-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="5d114-177">Ne</span><span class="sxs-lookup"><span data-stu-id="5d114-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="5d114-178">„Planning Optimization“ parinkties naudojimas</span><span class="sxs-lookup"><span data-stu-id="5d114-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="5d114-179">Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:</span><span class="sxs-lookup"><span data-stu-id="5d114-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="5d114-180">**Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="5d114-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="5d114-181">**Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="5d114-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="5d114-182">Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.</span><span class="sxs-lookup"><span data-stu-id="5d114-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="5d114-183">Integravimas su sąranka</span><span class="sxs-lookup"><span data-stu-id="5d114-183">Integration with the setup</span></span>

<span data-ttu-id="5d114-184">Jei „Planning Optimization“ yra įjungtas, pagrindinis planavimas yra atliekamas naudojant „Planning Optimization“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="5d114-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="5d114-185">Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5d114-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d114-186">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5d114-186">Additional resources</span></span>

[<span data-ttu-id="5d114-187">Peržiūros sąlygos ir nuostatos.</span><span class="sxs-lookup"><span data-stu-id="5d114-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="5d114-188">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="5d114-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5d114-189">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="5d114-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5d114-190">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="5d114-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5d114-191">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="5d114-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="5d114-192">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="5d114-192">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
