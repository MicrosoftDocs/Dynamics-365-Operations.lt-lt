---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
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
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339883"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="0b76c-103">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="0b76c-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b76c-104">„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, kuris įdiegtas „Microsoft"Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0b76c-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0b76c-105">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="0b76c-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="0b76c-106">„Planning Optimization“ funkcija pagal numatytuosius parametrus nėra įjungta „Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="0b76c-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="0b76c-107">Todėl prieš ją įjungdami turite galimybę atlikti savo vertinimą.</span><span class="sxs-lookup"><span data-stu-id="0b76c-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="0b76c-108">Galiausiai, „Planning Optimization“ pakeis dabartinį įdiegtą „Supply Chain Management“ planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="0b76c-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="0b76c-109">Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus.</span><span class="sxs-lookup"><span data-stu-id="0b76c-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="0b76c-110">Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0b76c-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="0b76c-111">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="0b76c-111">Availability</span></span>
<span data-ttu-id="0b76c-112">Šiuo metu planavimo optimizavimas pasiekiamas tolesniuose „Azure” regionuose: Jungtinės Valstijos, Kanada, Europa, Jungtinė Karalystė ir Australija.</span><span class="sxs-lookup"><span data-stu-id="0b76c-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="0b76c-113">Jei bandote įdiegti papildinį kitame geografiniame regione, LCS rodys pranešimą, nurodantį, kad šis regionas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="0b76c-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="0b76c-114">Turėkite omenyje, kad planavimo optimizavimas nepalaiko vietinių visuotinių „Dynamics 365 Supply Chain Management” diegimų.</span><span class="sxs-lookup"><span data-stu-id="0b76c-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="0b76c-115">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="0b76c-115">Licensing</span></span>

<span data-ttu-id="0b76c-116">Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="0b76c-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="0b76c-117">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="0b76c-117">Install the add-in</span></span>

<span data-ttu-id="0b76c-118">Norėdami naudoti „Planning Optimization“, įdiekite „Planning Optimization“ papildinį, skirtą „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0b76c-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0b76c-119">Galite pasiekti papildinį savo LCS projekte ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="0b76c-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="0b76c-120">Planavimo optimizavimo reikalavimas yra su įgalintais LCS plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” versiją 10.0.7 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="0b76c-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="0b76c-121">Jei bandote įdiegti papildinį „OneBox” aplinkoje, diegimas nebus užbaigtas ir jį reikės atšaukti.</span><span class="sxs-lookup"><span data-stu-id="0b76c-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="0b76c-122">Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="0b76c-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="0b76c-123">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="0b76c-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="0b76c-124">Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="0b76c-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="0b76c-125">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="0b76c-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="0b76c-126">Pasirinkite **Planning Optimization**.</span><span class="sxs-lookup"><span data-stu-id="0b76c-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="0b76c-127">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="0b76c-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="0b76c-128">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="0b76c-128">Select **Install**.</span></span>
1. <span data-ttu-id="0b76c-129">„FastTab“ **Aplinkos papildiniai** turėtumėte matyti, kad diegiamas planavimo optimizavimas.</span><span class="sxs-lookup"><span data-stu-id="0b76c-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="0b76c-130">Po kelių minučių būsena **Diegiama** turėtų pakisti į **Įdiegta** (jums gali prireikti atnaujinti puslapį).</span><span class="sxs-lookup"><span data-stu-id="0b76c-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="0b76c-131">Baigus diegti galite aktyvinti planavimo optimizavimą programoje „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0b76c-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="0b76c-132">„Planning Optimization“ integravimas</span><span class="sxs-lookup"><span data-stu-id="0b76c-132">Planning Optimization integration</span></span>

<span data-ttu-id="0b76c-133">Norėdami sukonfigūruoti, ar planavimo optimizavimo papildinys turi būti naudojamas bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="0b76c-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="0b76c-134">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="0b76c-134">Connection status</span></span>

<span data-ttu-id="0b76c-135">Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną.</span><span class="sxs-lookup"><span data-stu-id="0b76c-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="0b76c-136">Lentelėje pateiktos galimės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0b76c-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="0b76c-137">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="0b76c-137">Connection status</span></span> | <span data-ttu-id="0b76c-138">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0b76c-138">Description</span></span> | <span data-ttu-id="0b76c-139">Ar galima naudoti „Planning Optimization“?</span><span class="sxs-lookup"><span data-stu-id="0b76c-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="0b76c-140">Prisijungta</span><span class="sxs-lookup"><span data-stu-id="0b76c-140">Connected</span></span> | <span data-ttu-id="0b76c-141">Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0b76c-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="0b76c-142">Taip</span><span class="sxs-lookup"><span data-stu-id="0b76c-142">Yes</span></span> |
| <span data-ttu-id="0b76c-143">Įjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="0b76c-143">Enabling connection</span></span> | <span data-ttu-id="0b76c-144">Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="0b76c-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="0b76c-145">Ne</span><span class="sxs-lookup"><span data-stu-id="0b76c-145">No</span></span> |
| <span data-ttu-id="0b76c-146">Atsijungta</span><span class="sxs-lookup"><span data-stu-id="0b76c-146">Disconnected</span></span> | <span data-ttu-id="0b76c-147">Nėra ryšio su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="0b76c-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="0b76c-148">Ryšį galima įjungti iš LCS, kaip pirmiau aprašyta šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="0b76c-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="0b76c-149">Ne</span><span class="sxs-lookup"><span data-stu-id="0b76c-149">No</span></span> |
| <span data-ttu-id="0b76c-150">Išjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="0b76c-150">Disabling connection</span></span> | <span data-ttu-id="0b76c-151">Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="0b76c-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="0b76c-152">Ne</span><span class="sxs-lookup"><span data-stu-id="0b76c-152">No</span></span> |
| <span data-ttu-id="0b76c-153">Gavimo būsena</span><span class="sxs-lookup"><span data-stu-id="0b76c-153">Getting status</span></span> | <span data-ttu-id="0b76c-154">Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos.</span><span class="sxs-lookup"><span data-stu-id="0b76c-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="0b76c-155">Ne</span><span class="sxs-lookup"><span data-stu-id="0b76c-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="0b76c-156">„Planning Optimization“ parinkties naudojimas</span><span class="sxs-lookup"><span data-stu-id="0b76c-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="0b76c-157">Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:</span><span class="sxs-lookup"><span data-stu-id="0b76c-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="0b76c-158">**Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="0b76c-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="0b76c-159">**Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="0b76c-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="0b76c-160">Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.</span><span class="sxs-lookup"><span data-stu-id="0b76c-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="0b76c-161">Integravimas su sąranka</span><span class="sxs-lookup"><span data-stu-id="0b76c-161">Integration with the setup</span></span>

<span data-ttu-id="0b76c-162">Jei „Planning Optimization“ peržiūra įjungta, bendrasis planavimas atliekamas naudojant „Planning Optimization“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="0b76c-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="0b76c-163">Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.</span><span class="sxs-lookup"><span data-stu-id="0b76c-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b76c-164">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0b76c-164">Additional resources</span></span>

[<span data-ttu-id="0b76c-165">Peržiūros sąlygos ir nuostatos.</span><span class="sxs-lookup"><span data-stu-id="0b76c-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="0b76c-166">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="0b76c-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0b76c-167">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="0b76c-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="0b76c-168">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="0b76c-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0b76c-169">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="0b76c-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="0b76c-170">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="0b76c-170">Cancel a planning job</span></span>](cancel-planning-job.md)
