---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774011"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="8d07e-103">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="8d07e-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="8d07e-104">„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, kuris įdiegtas „Microsoft"Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="8d07e-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8d07e-105">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="8d07e-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="8d07e-106">„Planning Optimization“ funkcija pagal numatytuosius parametrus nėra įjungta „Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="8d07e-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="8d07e-107">Todėl prieš ją įjungdami turite galimybę atlikti savo vertinimą.</span><span class="sxs-lookup"><span data-stu-id="8d07e-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="8d07e-108">Galiausiai, „Planning Optimization“ pakeis dabartinį įdiegtą „Supply Chain Management“ planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="8d07e-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="8d07e-109">Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus.</span><span class="sxs-lookup"><span data-stu-id="8d07e-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="8d07e-110">Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8d07e-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="8d07e-111">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="8d07e-111">Licensing</span></span>

<span data-ttu-id="8d07e-112">Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="8d07e-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="8d07e-113">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="8d07e-113">Install the add-in</span></span>

<span data-ttu-id="8d07e-114">Norėdami naudoti „Planning Optimization“, įdiekite „Planning Optimization“ papildinį, skirtą „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="8d07e-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8d07e-115">Galite pasiekti papildinį savo LCS projekte ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="8d07e-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="8d07e-116">Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="8d07e-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="8d07e-117">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="8d07e-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="8d07e-118">Pasirinkite **Tvarkyti**arba slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="8d07e-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="8d07e-119">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="8d07e-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="8d07e-120">Pasirinkite **Planning Optimization**.</span><span class="sxs-lookup"><span data-stu-id="8d07e-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="8d07e-121">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="8d07e-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="8d07e-122">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="8d07e-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="8d07e-123">„Planning Optimization“ integravimas</span><span class="sxs-lookup"><span data-stu-id="8d07e-123">Planning Optimization integration</span></span>

<span data-ttu-id="8d07e-124">Norėdami sukonfigūruoti, ar „Planning Optimization“ papildinį reikia naudoti bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **„Planning Optimization“ integravimas** \> **Integravimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8d07e-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="8d07e-125">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="8d07e-125">Connection status</span></span>

<span data-ttu-id="8d07e-126">Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną.</span><span class="sxs-lookup"><span data-stu-id="8d07e-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="8d07e-127">Lentelėje pateiktos galimės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="8d07e-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="8d07e-128">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="8d07e-128">Connection status</span></span> | <span data-ttu-id="8d07e-129">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="8d07e-129">Description</span></span> | <span data-ttu-id="8d07e-130">Ar galima naudoti „Planning Optimization“?</span><span class="sxs-lookup"><span data-stu-id="8d07e-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="8d07e-131">Prisijungta</span><span class="sxs-lookup"><span data-stu-id="8d07e-131">Connected</span></span> | <span data-ttu-id="8d07e-132">Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="8d07e-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="8d07e-133">Taip</span><span class="sxs-lookup"><span data-stu-id="8d07e-133">Yes</span></span> |
| <span data-ttu-id="8d07e-134">Įjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="8d07e-134">Enabling connection</span></span> | <span data-ttu-id="8d07e-135">Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="8d07e-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="8d07e-136">Ne</span><span class="sxs-lookup"><span data-stu-id="8d07e-136">No</span></span> |
| <span data-ttu-id="8d07e-137">Atsijungta</span><span class="sxs-lookup"><span data-stu-id="8d07e-137">Disconnected</span></span> | <span data-ttu-id="8d07e-138">Nėra ryšio su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="8d07e-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="8d07e-139">Ryšį galima įjungti iš LCS, kaip pirmiau aprašyta šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="8d07e-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="8d07e-140">Ne</span><span class="sxs-lookup"><span data-stu-id="8d07e-140">No</span></span> |
| <span data-ttu-id="8d07e-141">Išjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="8d07e-141">Disabling connection</span></span> | <span data-ttu-id="8d07e-142">Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="8d07e-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="8d07e-143">Ne</span><span class="sxs-lookup"><span data-stu-id="8d07e-143">No</span></span> |
| <span data-ttu-id="8d07e-144">Gavimo būsena</span><span class="sxs-lookup"><span data-stu-id="8d07e-144">Getting status</span></span> | <span data-ttu-id="8d07e-145">Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos.</span><span class="sxs-lookup"><span data-stu-id="8d07e-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="8d07e-146">Ne</span><span class="sxs-lookup"><span data-stu-id="8d07e-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="8d07e-147">„Planning Optimization“ parinkties naudojimas</span><span class="sxs-lookup"><span data-stu-id="8d07e-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="8d07e-148">Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:</span><span class="sxs-lookup"><span data-stu-id="8d07e-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="8d07e-149">**Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="8d07e-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="8d07e-150">**Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="8d07e-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="8d07e-151">Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.</span><span class="sxs-lookup"><span data-stu-id="8d07e-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="8d07e-152">Integravimas su sąranka</span><span class="sxs-lookup"><span data-stu-id="8d07e-152">Integration with the setup</span></span>

<span data-ttu-id="8d07e-153">Jei „Planning Optimization“ peržiūra įjungta, bendrasis planavimas atliekamas naudojant „Planning Optimization“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="8d07e-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="8d07e-154">Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.</span><span class="sxs-lookup"><span data-stu-id="8d07e-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="8d07e-155">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="8d07e-155">Related resources</span></span>

[<span data-ttu-id="8d07e-156">Peržiūros sąlygos ir nuostatos.</span><span class="sxs-lookup"><span data-stu-id="8d07e-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="8d07e-157">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="8d07e-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="8d07e-158">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="8d07e-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="8d07e-159">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="8d07e-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="8d07e-160">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="8d07e-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="8d07e-161">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="8d07e-161">Cancel a planning job</span></span>](cancel-planning-job.md)
