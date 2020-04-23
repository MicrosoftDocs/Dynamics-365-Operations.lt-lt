---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
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
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213520"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="b75fc-103">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="b75fc-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b75fc-104">„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, kuris įdiegtas „Microsoft"Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b75fc-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b75fc-105">Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="b75fc-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="b75fc-106">„Planning Optimization“ funkcija pagal numatytuosius parametrus nėra įjungta „Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="b75fc-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="b75fc-107">Todėl prieš ją įjungdami turite galimybę atlikti savo vertinimą.</span><span class="sxs-lookup"><span data-stu-id="b75fc-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="b75fc-108">Galiausiai, „Planning Optimization“ pakeis dabartinį įdiegtą „Supply Chain Management“ planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="b75fc-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="b75fc-109">Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus.</span><span class="sxs-lookup"><span data-stu-id="b75fc-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="b75fc-110">Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b75fc-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="b75fc-111">Licencijavimas</span><span class="sxs-lookup"><span data-stu-id="b75fc-111">Licensing</span></span>

<span data-ttu-id="b75fc-112">Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="b75fc-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="b75fc-113">Papildinio įdiegimas</span><span class="sxs-lookup"><span data-stu-id="b75fc-113">Install the add-in</span></span>

<span data-ttu-id="b75fc-114">Norėdami naudoti „Planning Optimization“, įdiekite „Planning Optimization“ papildinį, skirtą „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b75fc-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b75fc-115">Galite pasiekti papildinį savo LCS projekte ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="b75fc-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="b75fc-116">Planavimo optimizavimo reikalavimas yra su įgalintais LCS plačiai pasiekiama aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” versiją 10.0.7 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="b75fc-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="b75fc-117">Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="b75fc-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="b75fc-118">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="b75fc-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="b75fc-119">Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="b75fc-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="b75fc-120">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="b75fc-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="b75fc-121">Pasirinkite **Planning Optimization**.</span><span class="sxs-lookup"><span data-stu-id="b75fc-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="b75fc-122">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="b75fc-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="b75fc-123">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="b75fc-123">Select **Install**.</span></span>
1. <span data-ttu-id="b75fc-124">„FastTab“ **Aplinkos papildiniai** turėtumėte matyti, kad diegiamas planavimo optimizavimas.</span><span class="sxs-lookup"><span data-stu-id="b75fc-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="b75fc-125">Po kelių minučių būsena **Diegiama** turėtų pakisti į **Įdiegta** (jums gali prireikti atnaujinti puslapį).</span><span class="sxs-lookup"><span data-stu-id="b75fc-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="b75fc-126">Baigus diegti galite aktyvinti planavimo optimizavimą programoje „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b75fc-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="b75fc-127">„Planning Optimization“ integravimas</span><span class="sxs-lookup"><span data-stu-id="b75fc-127">Planning Optimization integration</span></span>

<span data-ttu-id="b75fc-128">Norėdami sukonfigūruoti, ar planavimo optimizavimo papildinys turi būti naudojamas bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b75fc-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="b75fc-129">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="b75fc-129">Connection status</span></span>

<span data-ttu-id="b75fc-130">Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną.</span><span class="sxs-lookup"><span data-stu-id="b75fc-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="b75fc-131">Lentelėje pateiktos galimės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="b75fc-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="b75fc-132">Ryšio būsena</span><span class="sxs-lookup"><span data-stu-id="b75fc-132">Connection status</span></span> | <span data-ttu-id="b75fc-133">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="b75fc-133">Description</span></span> | <span data-ttu-id="b75fc-134">Ar galima naudoti „Planning Optimization“?</span><span class="sxs-lookup"><span data-stu-id="b75fc-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="b75fc-135">Prisijungta</span><span class="sxs-lookup"><span data-stu-id="b75fc-135">Connected</span></span> | <span data-ttu-id="b75fc-136">Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b75fc-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="b75fc-137">Taip</span><span class="sxs-lookup"><span data-stu-id="b75fc-137">Yes</span></span> |
| <span data-ttu-id="b75fc-138">Įjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="b75fc-138">Enabling connection</span></span> | <span data-ttu-id="b75fc-139">Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="b75fc-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="b75fc-140">Ne</span><span class="sxs-lookup"><span data-stu-id="b75fc-140">No</span></span> |
| <span data-ttu-id="b75fc-141">Atsijungta</span><span class="sxs-lookup"><span data-stu-id="b75fc-141">Disconnected</span></span> | <span data-ttu-id="b75fc-142">Nėra ryšio su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="b75fc-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="b75fc-143">Ryšį galima įjungti iš LCS, kaip pirmiau aprašyta šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="b75fc-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="b75fc-144">Ne</span><span class="sxs-lookup"><span data-stu-id="b75fc-144">No</span></span> |
| <span data-ttu-id="b75fc-145">Išjungiamas ryšys</span><span class="sxs-lookup"><span data-stu-id="b75fc-145">Disabling connection</span></span> | <span data-ttu-id="b75fc-146">Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="b75fc-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="b75fc-147">Ne</span><span class="sxs-lookup"><span data-stu-id="b75fc-147">No</span></span> |
| <span data-ttu-id="b75fc-148">Gavimo būsena</span><span class="sxs-lookup"><span data-stu-id="b75fc-148">Getting status</span></span> | <span data-ttu-id="b75fc-149">Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos.</span><span class="sxs-lookup"><span data-stu-id="b75fc-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="b75fc-150">Ne</span><span class="sxs-lookup"><span data-stu-id="b75fc-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="b75fc-151">„Planning Optimization“ parinkties naudojimas</span><span class="sxs-lookup"><span data-stu-id="b75fc-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="b75fc-152">Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:</span><span class="sxs-lookup"><span data-stu-id="b75fc-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="b75fc-153">**Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="b75fc-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="b75fc-154">**Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.</span><span class="sxs-lookup"><span data-stu-id="b75fc-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b75fc-155">Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.</span><span class="sxs-lookup"><span data-stu-id="b75fc-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="b75fc-156">Integravimas su sąranka</span><span class="sxs-lookup"><span data-stu-id="b75fc-156">Integration with the setup</span></span>

<span data-ttu-id="b75fc-157">Jei „Planning Optimization“ peržiūra įjungta, bendrasis planavimas atliekamas naudojant „Planning Optimization“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="b75fc-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="b75fc-158">Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.</span><span class="sxs-lookup"><span data-stu-id="b75fc-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b75fc-159">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="b75fc-159">Related resources</span></span>

[<span data-ttu-id="b75fc-160">Peržiūros sąlygos ir nuostatos.</span><span class="sxs-lookup"><span data-stu-id="b75fc-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="b75fc-161">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b75fc-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="b75fc-162">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="b75fc-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b75fc-163">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="b75fc-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b75fc-164">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="b75fc-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="b75fc-165">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b75fc-165">Cancel a planning job</span></span>](cancel-planning-job.md)
