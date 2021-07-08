---
title: Gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetams
description: Ši tema aprašo, kaip dirbti su gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetais.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1e2006c0d9b9effe331a644aaaa9fa33ff2fb7c
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270540"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="c93fb-103">Gamybos vykdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams</span><span class="sxs-lookup"><span data-stu-id="c93fb-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]

> [!WARNING]
> <span data-ttu-id="c93fb-104">Šiuo metu gamybos vykdymo darbo krūvis yra prieinamas kaip peržiūros versija.</span><span class="sxs-lookup"><span data-stu-id="c93fb-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="c93fb-105">Kai kurios verslo funkcijos nėra visiškai palaikomos viešoje peržiūroje, kai darbo apkrovos skalės vienetai yra naudojami.</span><span class="sxs-lookup"><span data-stu-id="c93fb-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="c93fb-106">Vykstant gamybai, skalės vienetai suteikia šias galimybes:</span><span class="sxs-lookup"><span data-stu-id="c93fb-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="c93fb-107">Mašinos operatoriai ir parduotuvės aukšto vadovai gali prieiti prie operacijos gamybos plano.</span><span class="sxs-lookup"><span data-stu-id="c93fb-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="c93fb-108">Mašinos operatoriai gali vis atnaujintą planą diskretiškam vykdymui ir proceso gamybos darbams.</span><span class="sxs-lookup"><span data-stu-id="c93fb-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="c93fb-109">Parduotuvės aukšto vadovas gali keisti operacijos planą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="c93fb-110">Darbuotojai gali prieiti prie laiko ir lankymosi su laikrodžiu ir be jo veikiančiame krašte siekiant pataisyti darbuotojo užmokesčio skaičiuoklę.</span><span class="sxs-lookup"><span data-stu-id="c93fb-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="c93fb-111">Ši tema aprašo, kaip dirbti su gamybos vykdymo darbo apkrovos debesies ir krašto skalės vienetais.</span><span class="sxs-lookup"><span data-stu-id="c93fb-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="c93fb-112">Gamybos gyvavimo ciklas</span><span class="sxs-lookup"><span data-stu-id="c93fb-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="c93fb-113">Tolesnis paveikslėlis rodo gamybos gyvavimo ciklo padalijimą į tris etapus: *Planavimas*, *Vykdymas* ir *Užbaigimas*.</span><span class="sxs-lookup"><span data-stu-id="c93fb-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="c93fb-114">[![Gamybos vykdymo etapai, kai viena aplinka naudojama](media/mes-phases.png "Gamybos vykdymo etapai, kai viena aplinka naudojama")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="c93fb-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="c93fb-115">Etapas _Planavimas_ apima produkto sąvoką, planavimą, užsakymo sukūrimą ir planavimą ir išleidimą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="c93fb-116">Išleidimo žingsnis rodo perėjimą nuo _Planavimo_ etapo į _Vykdymo_ etapą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="c93fb-117">Kai gamybos užsakymas yra paleistas, gamybos užsakymo darbai bus matomi gamybos aukšte ir parengti vykdymui.</span><span class="sxs-lookup"><span data-stu-id="c93fb-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="c93fb-118">Kai gamybos darbas yra pažymėtas kaip baigtas, jis juda nuo _Vykdymo_ etapo prie _Užbaigimo_ etapo.</span><span class="sxs-lookup"><span data-stu-id="c93fb-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="c93fb-119">Etape _Užbaigti_ registracijos nuo *Vykdymo* etapo pereina pro patvirtinimo darbo eigą, kai jos yra apskaičiuojamos, patvirtinamos ir perduodamos.</span><span class="sxs-lookup"><span data-stu-id="c93fb-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="c93fb-120">Tuo metu, gamybos užsakymas yra užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="c93fb-120">At that point, the production order is completed.</span></span> <span data-ttu-id="c93fb-121">Dėl to, bazinis darbuotojo užmokestis yra sukuriamas.</span><span class="sxs-lookup"><span data-stu-id="c93fb-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="c93fb-122">Vykdymo etapo atskyrimas į keletą darbo apkrovų</span><span class="sxs-lookup"><span data-stu-id="c93fb-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="c93fb-123">Kaip rodo kitas paveikslėlis, kai skalės vienetai naudojami, _Vykdymo_ etapas yra paskirstomas kaip atskira darbo apkrova.</span><span class="sxs-lookup"><span data-stu-id="c93fb-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="c93fb-124">[![Gamybos vykdymo etapai, kai naudojami skalės vienetai](media/mes-phases-workloads.png "Gamybos vykdymo etapai, kai naudojami skalės vienetai")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="c93fb-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="c93fb-125">Modelis dabar eina nuo vieno elemento diegimo iki modelio, kuris yra pagrįstas centru ir skalės vienetais.</span><span class="sxs-lookup"><span data-stu-id="c93fb-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="c93fb-126">Etapai _Planavimas_ ir _Užbaigimas_ vyksta, kai ne su klientais susijusios operacijos vykdomos centre ir gamybos vykdymo darbo apkrova vykdoma skalės vienetuose.</span><span class="sxs-lookup"><span data-stu-id="c93fb-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="c93fb-127">Duomenys yra perduodami nesinchroniniu būdu tarp centro ir skalės vienetų.</span><span class="sxs-lookup"><span data-stu-id="c93fb-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="c93fb-128">Kai gamybos užsakymas išleidžiamas į centrą, visi duomenys yra būtini siekiant apdoroti gamybos darbus, kurie perduodami į skalės vienetą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="c93fb-129">Šie duomenys apima gamybos užsakymus, maršrutus, medžiagų aprašus ir gaminius.</span><span class="sxs-lookup"><span data-stu-id="c93fb-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="c93fb-130">Duomenys nėra susiję su gamybos užsakymu (tokiu kaip netiesioginės veiklos, nebuvimo kodai ir gamybos parametrai) yra taip pat perduodami iš centro į skalės vienetą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="c93fb-131">Kaip taisyklės, duomenys ateinantys iš centro ir perduodami į skalės vienetą negali būti sukruti ar naujinti tik centre.</span><span class="sxs-lookup"><span data-stu-id="c93fb-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="c93fb-132">Pavyzdžiui, naujas nebuvimo kodas ar netiesioginė veikla negali būti sukurta skalės vienete&mdash;jie gali būti panaudojami tik registravimui.</span><span class="sxs-lookup"><span data-stu-id="c93fb-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="c93fb-133">Registravimai atlikti skalės vienete vykdymo metu yra tada perduodami į centrą, kuriame laikas ir buvimo patvirtinimas, inventorius ir finansiniai naujiniai yra apdorojami.</span><span class="sxs-lookup"><span data-stu-id="c93fb-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="c93fb-134">Gamybos vykdymo užduotys, kurios gali vykti darbo apkrovose</span><span class="sxs-lookup"><span data-stu-id="c93fb-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="c93fb-135">Tolesnės gamybos vykdymo užduotys šiuo metu gali būti vykdomos darbo apkrovose, kai skalės vienetai naudojami:</span><span class="sxs-lookup"><span data-stu-id="c93fb-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="c93fb-136">Laiko suderinimas, prisijungimas ir laiko išderinimas ir nebuvimas</span><span class="sxs-lookup"><span data-stu-id="c93fb-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="c93fb-137">Pradėti užduotį</span><span class="sxs-lookup"><span data-stu-id="c93fb-137">Start job</span></span>
- <span data-ttu-id="c93fb-138">Pluoštiniai darbai</span><span class="sxs-lookup"><span data-stu-id="c93fb-138">Bundle jobs</span></span>
- <span data-ttu-id="c93fb-139">Pranešti apie eigą</span><span class="sxs-lookup"><span data-stu-id="c93fb-139">Report progress</span></span>
- <span data-ttu-id="c93fb-140">Pranešti apie atliekas</span><span class="sxs-lookup"><span data-stu-id="c93fb-140">Report scrap</span></span>
- <span data-ttu-id="c93fb-141">Netiesioginiai veiksmai</span><span class="sxs-lookup"><span data-stu-id="c93fb-141">Indirect activity</span></span>
- <span data-ttu-id="c93fb-142">Pertrauka</span><span class="sxs-lookup"><span data-stu-id="c93fb-142">Break</span></span>
- <span data-ttu-id="c93fb-143">Pranešti, kad baigta ir padėti (reikia, kad sandėlio vykdymo darbo krūvį paleistumėte ir savo skalės vienete, taip pat žr. ataskaitą kaip baigtą ir padėti [ant svarstyklių vieneto](#RAF))</span><span class="sxs-lookup"><span data-stu-id="c93fb-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="c93fb-144">Darbas su gamybos vykdymo darbo eigomis centre</span><span class="sxs-lookup"><span data-stu-id="c93fb-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="c93fb-145">Dažniausiai, procesai, kuriems reikia vykdyti gamybos darbo krūvius veikia automatiškai, kad palaikytų centrą ir skalės vienetus sinchroniniu būdu, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="c93fb-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="c93fb-146">Nepaisant to, jei susiduriate su sunkumais, galite rankiniu būdu paleisti neapdorotų registracijų tvarkymą, kuris gaunamas iš darbo krūvių ir (arba) tikrinti registracijos tvarkymo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="c93fb-147">Rankiniu būdu tvarkykite neapdorotas registracijas</span><span class="sxs-lookup"><span data-stu-id="c93fb-147">Manually process raw registrations</span></span>

<span data-ttu-id="c93fb-148">Palaidų vienetų darbas „Supply Chain Management“ veikia automatiniu būdu ir tvarko visas registracijas, gautas iš darbo krūvių.</span><span class="sxs-lookup"><span data-stu-id="c93fb-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="c93fb-149">Sukurtiems darbams reikia gamybos žurnalų ir žurnalų knygos įrašų, kai registracija yra apdorojama baigtam darbui darbo krūvyje.</span><span class="sxs-lookup"><span data-stu-id="c93fb-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="c93fb-150">Nepaisant to, kad darbas dažniausiai vyksta automatiniu būdu, galite vykdyti jį rankiniu būdu bet kuriuo metu prisijungę prie centro ir patekę į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Neapdorotų registracijų tvarkymas**.</span><span class="sxs-lookup"><span data-stu-id="c93fb-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="c93fb-151">Patikrinkite neapdorotos registracijos tvarkymo žurnalą</span><span class="sxs-lookup"><span data-stu-id="c93fb-151">Check the raw registration processing log</span></span>

<span data-ttu-id="c93fb-152">Norėdami peržiūrėti registracijos apdorojimo žurnalą, prisijunkite prie centro ir eikite į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Neapdorotų registracijų tvarkymo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="c93fb-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="c93fb-153">Puslapyje **Neapdorotų registracijų tvarkymo žurnalas** rodomos apdorotos žalios registracijos ir visų registracijų būsena.</span><span class="sxs-lookup"><span data-stu-id="c93fb-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="c93fb-154">![Žaliavų registracijos tvarkymo žurnalo puslapis](media/mes-processing-log.png "Žaliavų registracijos tvarkymo žurnalo puslapis")</span><span class="sxs-lookup"><span data-stu-id="c93fb-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="c93fb-155">Galite dirbti su bet kuria registracija sąraše pasirinkę ją ir tada pasirinkę vieną iš tolesnių mygtukų veiksmų juostoje:</span><span class="sxs-lookup"><span data-stu-id="c93fb-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="c93fb-156">**Tvarkyti** – Rankiniu būdu tvarkyti pasirinktą registraciją.</span><span class="sxs-lookup"><span data-stu-id="c93fb-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="c93fb-157">Šis veiksmas gali būti naudingas, jei _Tvarkyti žalias registracijas_ darbas nevyko arba jis nepavyko.</span><span class="sxs-lookup"><span data-stu-id="c93fb-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="c93fb-158">**Atšaukti** – Atšaukti pasirinktą registraciją.</span><span class="sxs-lookup"><span data-stu-id="c93fb-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="c93fb-159">Darbas su gamybos vykdymo darbo krūviais skalės vienete</span><span class="sxs-lookup"><span data-stu-id="c93fb-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="c93fb-160">Dažniausiai, procesai, kuriems reikia vykdyti gamybos darbo krūvius veikia automatiškai, kad palaikytų centrą ir skalės vienetus sinchroniniu būdu, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="c93fb-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="c93fb-161">Nepaisant to, jei turite problemų, galite patikrinti užsakymų istoriją, kurie buvo sutvarkyti skalės vienete ar rankiniu būdu vykdyti _Gamybos centro į skalės vienetą pranešimo tvarkytuvas_ darbą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="c93fb-162">Peržiūrėkite gamybos darbų istoriją, kurie buvo sutvarkyti skalės vienete</span><span class="sxs-lookup"><span data-stu-id="c93fb-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="c93fb-163">Norėdami peržiūrėti gamybos darbų istoriją, kurie buvo sutvarkyti skalės vienete, prisijunkite prie skalės vieneto mašinos ir eikite į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \> Gamybos darbų tvarkymo istorija**.</span><span class="sxs-lookup"><span data-stu-id="c93fb-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="c93fb-164">Puslapyje **Gamybos darbų tvarkymo istorija** rodoma gamybos užsakymų skalės vienete tvarkymo istorija.</span><span class="sxs-lookup"><span data-stu-id="c93fb-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="c93fb-165">Galite dirbti su bet kuriuo gamybos užsakymu sąraše pasirinkę ją ir tada pasirinkę vieną iš tolesnių mygtukų veiksmų juostoje:</span><span class="sxs-lookup"><span data-stu-id="c93fb-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="c93fb-166">**Tvarkyti** – Rankiniu būdu tvarkyti pasirinktą gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="c93fb-167">**Atšaukti** – Atšaukti pasirinktą gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="c93fb-168">Gamybos centras į skalės vieneto pranešimo tvarkytuvo darbą</span><span class="sxs-lookup"><span data-stu-id="c93fb-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="c93fb-169">_Gamybos centras į skalės vieneto pranešimo tvarkytuvą_ darbas tvarko duomenis iš centro į skalės vienetą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="c93fb-170">Šis darbas automatiniu būdu pradedamas, kai gamybos vykdymo darbo krūvis yra patalpintas.</span><span class="sxs-lookup"><span data-stu-id="c93fb-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="c93fb-171">Nepaisant to, galite vykdyti rankiniu būdu jį bet kuriuo metu patekę į **Gamybos valdymas \> Periodinės užduotys \> Galinio skyriaus darbo krūvio valdymas \>Gamybos centras į skalės vieneto pranešimo tvarkytuvą**.</span><span class="sxs-lookup"><span data-stu-id="c93fb-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="c93fb-172">Pranešti, kad baigta, ir padėti ant svarstyklių vieneto</span><span class="sxs-lookup"><span data-stu-id="c93fb-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="c93fb-173">Dabartiniame leidime sandėlio vykdymo darbo krūvis palaiko operacijas kaip baigtas ir padėjusias (baigtų produktų, sudėtinųjų ir tarpinių produktų) operacijas [ne gamybos vykdymo darbo krūvį](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="c93fb-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="c93fb-174">Todėl, norėdami šią funkciją naudoti prijungę prie svarstyklių vieneto, turite atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="c93fb-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="c93fb-175">Įdiekite sandėlio vykdymo darbo krūvį ir gamybos vykdymo darbo krūvį savo skalės vienete.</span><span class="sxs-lookup"><span data-stu-id="c93fb-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="c93fb-176">„Warehouse Management“ mobiliąją programą naudokite norėdami pranešti, kad baigta, ir apdoroti atidavimo darbą.</span><span class="sxs-lookup"><span data-stu-id="c93fb-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="c93fb-177">Gamybos laiko vykdymo sąsaja šiuo metu nepalaiko šių procesų.</span><span class="sxs-lookup"><span data-stu-id="c93fb-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
