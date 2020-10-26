---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973481"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="3e56c-103">Darbo su planavimo optimizavimu pradžia</span><span class="sxs-lookup"><span data-stu-id="3e56c-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e56c-104">Kaip buvo [nurodyta anksčiau](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), numatoma, kad „Planning Optimization“ pakeis esamą integruotą bendrojo planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="3e56c-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="3e56c-105">Jei šiuo metu naudojate integruotą bendrojo planavimo mechanizmą, turite pradėti galvoti apie perėjimą prie „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="3e56c-106">Svarbu iš karto pradėti perėjimo procesą, nes tai gali turėti jūsų darbui, kai senesnė versija taps nebenaudojama.</span><span class="sxs-lookup"><span data-stu-id="3e56c-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="3e56c-107">Tam, kad išvengtumėte problemų, kai senesnė versija taps nebenaudojama, primygtinai rekomenduojame baigti perėjimą iki 2020 m. gruodžio 1 d.</span><span class="sxs-lookup"><span data-stu-id="3e56c-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="3e56c-108">„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, integruotame „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="3e56c-109">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="3e56c-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="3e56c-110">„Planning Optimization“ funkcija šiuo metu nėra įjungta „Dynamics Lifecycle Services“ (LCS) esant numatytiesiems parametrams, todėl jūs turite galimybę atlikti savo vertinimą prieš įjungiant funkciją.</span><span class="sxs-lookup"><span data-stu-id="3e56c-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="3e56c-111">Jums reikia prašyti išimties, kad galėtumėte nepereiti prie „Planning Optimization“, jei bendrojo planavimo procesas neapima gamybos (bendrojo planavimo sugeneruotų suplanuotų gamybos užsakymų) ir jums reikia 10.0.15 arba senesnės integruoto bendrojo planavimo mechanizmo versijos.</span><span class="sxs-lookup"><span data-stu-id="3e56c-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="3e56c-112">Pradedant nuo 10.0.16 versijos, bandant paleisti integruotą bendrąjį planavimą be suplanuotų gamybos užsakymų generavimo, bus rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="3e56c-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="3e56c-113">„Planning Optimization“ turi būti naudojama visiems naujiems įdiegimams, kurie negeneruoja suplanuotų gamybos užsakymų atliekant bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="3e56c-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="3e56c-114">Esamų aplinkų savininkai, leisdami integruotą bendrojo planavimo mechanizmą be suplanuotų gamybos užsakymų, gaus laiškus, kuriuose pateikiama informacija apie išimties procesą.</span><span class="sxs-lookup"><span data-stu-id="3e56c-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="3e56c-115">Rekomenduojame kartu su partneriu įvertinti ir planuoti perėjimą prie „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="3e56c-116">Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus.</span><span class="sxs-lookup"><span data-stu-id="3e56c-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="3e56c-117">Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3e56c-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="3e56c-118">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="3e56c-118">Availability</span></span>
<span data-ttu-id="3e56c-119">Šiuo metu planavimo optimizavimas pasiekiamas tolesniuose „Azure” regionuose: Jungtinės Valstijos, Kanada, Europa, Jungtinė Karalystė ir Australija.</span><span class="sxs-lookup"><span data-stu-id="3e56c-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="3e56c-120">Jei bandote įdiegti papildinį kitame geografiniame regione, LCS rodys pranešimą, nurodantį, kad šis regionas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="3e56c-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="3e56c-121">Turėkite omenyje, kad planavimo optimizavimas nepalaiko vietinių visuotinių „Dynamics 365 Supply Chain Management” diegimų.</span><span class="sxs-lookup"><span data-stu-id="3e56c-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="3e56c-122">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="3e56c-122">Licensing</span></span>

<span data-ttu-id="3e56c-123">Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="3e56c-124">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="3e56c-124">Install the add-in</span></span>

<span data-ttu-id="3e56c-125">Norėdami naudoti „Planning Optimization“, įdiekite „Planning Optimization“ papildinį, skirtą „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3e56c-126">Galite pasiekti papildinį savo LCS projekte ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="3e56c-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="3e56c-127">Planavimo optimizavimo reikalavimas yra su įgalintais LCS plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” versiją 10.0.7 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="3e56c-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="3e56c-128">Jei bandote įdiegti papildinį „OneBox” aplinkoje, diegimas nebus užbaigtas ir jį reikės atšaukti.</span><span class="sxs-lookup"><span data-stu-id="3e56c-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="3e56c-129">Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="3e56c-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="3e56c-130">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="3e56c-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="3e56c-131">Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="3e56c-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="3e56c-132">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="3e56c-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="3e56c-133">Pasirinkite **Planning Optimization**.</span><span class="sxs-lookup"><span data-stu-id="3e56c-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="3e56c-134">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="3e56c-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="3e56c-135">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="3e56c-135">Select **Install**.</span></span>
1. <span data-ttu-id="3e56c-136">„FastTab“ **Aplinkos papildiniai** turėtumėte matyti, kad diegiamas planavimo optimizavimas.</span><span class="sxs-lookup"><span data-stu-id="3e56c-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="3e56c-137">Po kelių minučių būsena **Diegiama** turėtų pakisti į **Įdiegta** (jums gali prireikti atnaujinti puslapį).</span><span class="sxs-lookup"><span data-stu-id="3e56c-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="3e56c-138">Baigus diegti galite aktyvinti planavimo optimizavimą programoje „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="3e56c-139">„Planning Optimization“ integravimas</span><span class="sxs-lookup"><span data-stu-id="3e56c-139">Planning Optimization integration</span></span>

<span data-ttu-id="3e56c-140">Norėdami sukonfigūruoti, ar planavimo optimizavimo papildinys turi būti naudojamas bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3e56c-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="3e56c-141">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="3e56c-141">Connection status</span></span>

<span data-ttu-id="3e56c-142">Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną.</span><span class="sxs-lookup"><span data-stu-id="3e56c-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="3e56c-143">Lentelėje pateiktos galimės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="3e56c-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="3e56c-144">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="3e56c-144">Connection status</span></span> | <span data-ttu-id="3e56c-145">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="3e56c-145">Description</span></span> | <span data-ttu-id="3e56c-146">Ar galima naudoti „Planning Optimization“?</span><span class="sxs-lookup"><span data-stu-id="3e56c-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="3e56c-147">Prisijungta</span><span class="sxs-lookup"><span data-stu-id="3e56c-147">Connected</span></span> | <span data-ttu-id="3e56c-148">Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="3e56c-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="3e56c-149">Taip</span><span class="sxs-lookup"><span data-stu-id="3e56c-149">Yes</span></span> |
| <span data-ttu-id="3e56c-150">Įjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="3e56c-150">Enabling connection</span></span> | <span data-ttu-id="3e56c-151">Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="3e56c-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="3e56c-152">Ne</span><span class="sxs-lookup"><span data-stu-id="3e56c-152">No</span></span> |
| <span data-ttu-id="3e56c-153">Atsijungta</span><span class="sxs-lookup"><span data-stu-id="3e56c-153">Disconnected</span></span> | <span data-ttu-id="3e56c-154">Nėra ryšio su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="3e56c-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="3e56c-155">Ryšį galima įjungti iš LCS, kaip pirmiau aprašyta šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="3e56c-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="3e56c-156">Ne</span><span class="sxs-lookup"><span data-stu-id="3e56c-156">No</span></span> |
| <span data-ttu-id="3e56c-157">Išjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="3e56c-157">Disabling connection</span></span> | <span data-ttu-id="3e56c-158">Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="3e56c-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="3e56c-159">Ne</span><span class="sxs-lookup"><span data-stu-id="3e56c-159">No</span></span> |
| <span data-ttu-id="3e56c-160">Gavimo būsena</span><span class="sxs-lookup"><span data-stu-id="3e56c-160">Getting status</span></span> | <span data-ttu-id="3e56c-161">Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos.</span><span class="sxs-lookup"><span data-stu-id="3e56c-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="3e56c-162">Ne</span><span class="sxs-lookup"><span data-stu-id="3e56c-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="3e56c-163">„Planning Optimization“ parinkties naudojimas</span><span class="sxs-lookup"><span data-stu-id="3e56c-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="3e56c-164">Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:</span><span class="sxs-lookup"><span data-stu-id="3e56c-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="3e56c-165">**Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="3e56c-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="3e56c-166">**Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="3e56c-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="3e56c-167">Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.</span><span class="sxs-lookup"><span data-stu-id="3e56c-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="3e56c-168">Integravimas su sąranka</span><span class="sxs-lookup"><span data-stu-id="3e56c-168">Integration with the setup</span></span>

<span data-ttu-id="3e56c-169">Jei „Planning Optimization“ peržiūra įjungta, bendrasis planavimas atliekamas naudojant „Planning Optimization“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="3e56c-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="3e56c-170">Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.</span><span class="sxs-lookup"><span data-stu-id="3e56c-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e56c-171">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3e56c-171">Additional resources</span></span>

[<span data-ttu-id="3e56c-172">Peržiūros sąlygos ir nuostatos.</span><span class="sxs-lookup"><span data-stu-id="3e56c-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="3e56c-173">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="3e56c-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="3e56c-174">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="3e56c-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="3e56c-175">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="3e56c-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="3e56c-176">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="3e56c-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="3e56c-177">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3e56c-177">Cancel a planning job</span></span>](cancel-planning-job.md)
