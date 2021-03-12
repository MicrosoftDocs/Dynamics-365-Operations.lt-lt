---
title: „Dynamics 365 Supply Chain Management“ (Turto valdymas) integravimas su „Dynamics 365 Guides“
description: Šioje temoje paaiškinama, kaip integruoti „Microsoft Dynamics 365 Supply Chain Management“ modulį „Turto valdymas“ į „Dynamics 365 Guides“, kad kasdienėse paslaugose ir priežiūros darbo eigose būtų galima pasinaudoti mišriosios realybės vadovų teikiamomis galimybėmis.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: ae26012d236a44bfa0c8453bdc660671ddee82a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000289"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="9d838-103">„Dynamics 365 Supply Chain Management“ (Turto valdymas) integravimas su „Dynamics 365 Guides“</span><span class="sxs-lookup"><span data-stu-id="9d838-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="9d838-104">„Microsoft Dynamics 365 Supply Chain Management“ modulį **Turto valdymas** galite integruoti į „Dynamics 365 Guides“, kad kasdienėse paslaugose ir priežiūros darbo eigose galėtumėte pasinaudoti mišriosios realybės vadovų teikiamomis galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="9d838-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="9d838-105">Jei vadovas yra susietas su modulio „Turto valdymas“ darbo užsakymu, darbuotojas, kuris „Supply Chain Management“ („Dynamics 365“) mobilioje programoje atidaro darbo užsakymo prižiūrimo turto kontrolinį sąrašą, mato, kad vadovas yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="9d838-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="9d838-106">Tada darbuotojas gali rasti ir atidaryti vadovą „Dynamics 365 Guides HoloLens“ programoje.</span><span class="sxs-lookup"><span data-stu-id="9d838-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9d838-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="9d838-107">Prerequisites</span></span>

<span data-ttu-id="9d838-108">Norėdami pridėti vadovus modulio „Turto valdymas“ darbo užsakymų, turite atlikti toliau nurodytas būtinas užduotis.</span><span class="sxs-lookup"><span data-stu-id="9d838-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="9d838-109">[Sukonfigūruokite „Dynamics 365 Supply Chain Management“](../../fin-ops-core/fin-ops/index.md) 10.0.9 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="9d838-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="9d838-110">[„Supply Chain Management“ programoms įjunkite dvigubą rašymą](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="9d838-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="9d838-111">[Įjunkite testuojamą variantą](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** funkcijai.</span><span class="sxs-lookup"><span data-stu-id="9d838-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="9d838-112">(Gamybos aplinkose pirmiausia turite pateikti palaikymo bilietą, kad jūsų nuomotojas būtų įtrauktas į testuojamo varianto grupę.)</span><span class="sxs-lookup"><span data-stu-id="9d838-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="9d838-113">[Įjunkite toliau nurodytus konfigūracijos raktus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) puslapyje **Licencijos konfigūracija**:</span><span class="sxs-lookup"><span data-stu-id="9d838-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="9d838-114">Turto valdymas \> Turto valdymo mišrioji realybė</span><span class="sxs-lookup"><span data-stu-id="9d838-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="9d838-115">Mišrioji realybė \> Mišriosios realybės vadovas</span><span class="sxs-lookup"><span data-stu-id="9d838-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="9d838-116">[Sukonfigūruokite „Dynamics 365 Guides“](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 200.0.0.96 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="9d838-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="9d838-117">„Dynamics 365 Guides“ naudojimas su moduliu „Turto valdymas“</span><span class="sxs-lookup"><span data-stu-id="9d838-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="9d838-118">Vadovui susieti, modulyje „Turto valdymas“ naudojama prižiūrimo turto kontrolinio sąrašo eilutė.</span><span class="sxs-lookup"><span data-stu-id="9d838-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="9d838-119">Susiejimą galite sukurti naudodami prižiūrimo turto kontrolinio sąrašo šabloną, priežiūros užduoties tipą arba darbo užsakymą, nes visuose trijuose yra prižiūrimo turto kontrolinio sąrašo eilutės.</span><span class="sxs-lookup"><span data-stu-id="9d838-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="9d838-120">Naudodami šabloną galite sutaupyti laiko, nes šablonas gali būti susietas su visais priežiūros užduočių tipais, kuriuos jis naudoja.</span><span class="sxs-lookup"><span data-stu-id="9d838-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="9d838-121">Pavyzdžiui, vadovas, kuris yra susietas su priežiūros užduoties tipu, automatiškai susiejamas su visais darbo užsakymais, kurie nurodo tą užduoties tipą.</span><span class="sxs-lookup"><span data-stu-id="9d838-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="9d838-122">Kita vertus, tiesiogiai su darbo užsakymu susietas vadovas yra skirtas tik tam darbo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="9d838-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="9d838-123">Vadovo susiejimas su prižiūrimo turto kontrolinio sąrašo šablonu</span><span class="sxs-lookup"><span data-stu-id="9d838-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="9d838-124">Norėdami susieti vadovą su prižiūrimo turto kontrolinio sąrašo šablonu, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d838-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="9d838-125">Sukurkite vadovą naudodami „Dynamics 365 Guides“ kompiuterio ir „HoloLens“ programas.</span><span class="sxs-lookup"><span data-stu-id="9d838-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="9d838-126">Daugiau informacijos, kaip kurti vadovą, žr. tolesnėse temose.</span><span class="sxs-lookup"><span data-stu-id="9d838-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="9d838-127">Kompiuterio programos naudojimas vadovui kurti</span><span class="sxs-lookup"><span data-stu-id="9d838-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="9d838-128">„HoloLens“ programos naudojimas hologramoms uždėti</span><span class="sxs-lookup"><span data-stu-id="9d838-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="9d838-129">[Sukurkite prižiūrimo turto kontrolinio sąrašo šabloną](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template) programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="9d838-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="9d838-130">Susiekite vadovą, kurį sukūrėte prižiūrimo turto kontrolinio sąrašo eilutėje, naujame prižiūrimo turto kontrolinio sąrašo šablone.</span><span class="sxs-lookup"><span data-stu-id="9d838-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="9d838-131">„FastTab“ konteineryje **Prižiūrimo turto sąrašo eilutės** pasirinkite eilutę, su kuria norite susieti vadovą.</span><span class="sxs-lookup"><span data-stu-id="9d838-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="9d838-132">„FastTab“ konteineryje **Susieti vadovai** pasirinkite **Įtraukti vadovą**.</span><span class="sxs-lookup"><span data-stu-id="9d838-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="9d838-133">![Vadovo susiejimas su prižiūrimo turto kontrolinio sąrašo eilute](media/am-guides-integration-add-guide.png "Vadovo susiejimas su prižiūrimo turto kontrolinio sąrašo eilute")</span><span class="sxs-lookup"><span data-stu-id="9d838-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="9d838-134">Lauke **Pavadinimas** pasirinkite vadovą, tada – **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9d838-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="9d838-135">![Lauke Pavadinimas pasirinkite vadovą](media/am-guides-integration-select-guide.png "Lauke Pavadinimas pasirinkite vadovą")</span><span class="sxs-lookup"><span data-stu-id="9d838-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="9d838-136">Susiekite prižiūrimo turto kontrolinio sąrašo šabloną su užduoties tipu.</span><span class="sxs-lookup"><span data-stu-id="9d838-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="9d838-137">[Sukurkite priežiūros užduoties tipą ](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) arba pasirinkite esamą priežiūros užduoties tipą.</span><span class="sxs-lookup"><span data-stu-id="9d838-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="9d838-138">Veiksmų srityje pasirinkite **Priežiūros užduoties tipo numatytosios reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="9d838-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="9d838-139">![Mygtukas Priežiūros užduočių tipų numatytosios reikšmės](media/am-guides-integration-job-defaults.png "Mygtukas Priežiūros užduočių tipų numatytosios reikšmės")</span><span class="sxs-lookup"><span data-stu-id="9d838-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="9d838-140">Sukurkite eilutę ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9d838-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="9d838-141">![Kurti eilutę](media/am-guides-integration-add-line.png "Kurti eilutę")</span><span class="sxs-lookup"><span data-stu-id="9d838-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="9d838-142">Veiksmų srityje pasirinkite **Prižiūrimo turto kontrolinis sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="9d838-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="9d838-143">![Mygtukas Prižiūrimo turto kontrolinis sąrašas](media/am-guides-integration-maintenance-checklist.png "Mygtukas Prižiūrimo turto kontrolinis sąrašas")</span><span class="sxs-lookup"><span data-stu-id="9d838-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="9d838-144">„FastTab“ konteineryje **Prižiūrimo turto kontrolinio sąrašo eilutės** pridėkite eilutę, tada pakeiskite lauko **Tipas** reikšmę į **Šablonas**.</span><span class="sxs-lookup"><span data-stu-id="9d838-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="9d838-145">![Keisti lauko Tipas reikšmę](media/am-guides-integration-checklist-lines.png "Keisti lauko Tipas reikšmę")</span><span class="sxs-lookup"><span data-stu-id="9d838-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="9d838-146">„FastTab“ konteinerio **Išsami eilutės informacija** lauke **Šablonas** pasirinkite šabloną, su kuriuo susiejote vadovą, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9d838-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="9d838-147">![Pasirinkti šabloną](media/am-guides-integration-checklist-line-details.png "Pasirinkti šabloną")</span><span class="sxs-lookup"><span data-stu-id="9d838-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="9d838-148">[Sukurkite darbo užsakymą](work-orders/manually-created-workorders.md#create-work-order), tada pasirinkite priežiūros užduoties tipą, kuris naudoja prižiūrimo turto kontrolinio sąrašo šabloną, su kuriuo susiejote vadovą.</span><span class="sxs-lookup"><span data-stu-id="9d838-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="9d838-149">Vadovas automatiškai susiejamas su darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="9d838-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="9d838-150">![Pasirinkti priežiūros užduoties tipą](media/am-guides-integration-create-work-order.png "Pasirinkti priežiūros užduoties tipą")</span><span class="sxs-lookup"><span data-stu-id="9d838-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="9d838-151">Norėdami peržiūrėti vadovą, susietą su darbo užsakymu ir darbuotojais, atlikite toliau aprašytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d838-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="9d838-152">Norėdami pasiekti darbo užsakymą, atidarykite [Turto valdymo mobilioji darbo sritis](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="9d838-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="9d838-153">[Atidarykite darbo užsakymo prižiūrimo turto kontrolinį sąrašą](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).</span><span class="sxs-lookup"><span data-stu-id="9d838-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="9d838-154">Pasirinkite kontrolinio sąrašo eilutę, kad pamatytumėte susietą vadovą.</span><span class="sxs-lookup"><span data-stu-id="9d838-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="9d838-155">![Vadovas, susietas su kontrolinio sąrašo eilute](media/am-guides-integration-show-guide.png "Vadovas, susietas su kontrolinio sąrašo eilute")</span><span class="sxs-lookup"><span data-stu-id="9d838-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="9d838-156">Atidarykite vadovą „HoloLens“.</span><span class="sxs-lookup"><span data-stu-id="9d838-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="9d838-157">![Atidaryti vadovą „HoloLens“](media/am-guides-integration-hololens-select.png "Atidaryti vadovą „HoloLens“")</span><span class="sxs-lookup"><span data-stu-id="9d838-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="9d838-158">Vadovą taip pat galite tiesiogiai susieti darbo užsakymo arba užduoties tipo prižiūrimo turto kontroliniame sąraše.</span><span class="sxs-lookup"><span data-stu-id="9d838-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d838-159">Yra žinoma problema, kai susiejus prižiūrimo turto kontrolinio sąrašo šabloną su numatytuoju priežiūros užduoties tipu, su šablonu susietas vadovas nerodomas puslapio **Priežiūros užduočių tipų numatytosios reikšmės** „FastTab“ konteineryje **Susieti vadovai**.</span><span class="sxs-lookup"><span data-stu-id="9d838-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="9d838-160">Tačiau vadovas bus rodomas po to, kai tas užduoties tipas bus pritaikytas darbo užsakymui „FastTab“ konteineryje **Susieti vadovai**.</span><span class="sxs-lookup"><span data-stu-id="9d838-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d838-161">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="9d838-161">See also</span></span>

- [<span data-ttu-id="9d838-162">Dvigubo rašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="9d838-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="9d838-163">Išteklių valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="9d838-163">Asset management overview</span></span>](index.md)
