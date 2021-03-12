---
title: Bendrojo planavimo vykdymo stebėjimas
description: Šioje temoje paaiškinama, kaip gamybos planuotojas gali matyti, ar vyksta bendrasis planavimas.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cbe2c55ef9e3ed35db30ca927f3472c750c1db5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999811"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="e53e8-103">Bendrojo planavimo vykdymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="e53e8-104">Gantt diagramos naudojimas siekiant vizualizuoti bendrojo planavimo eigą</span><span class="sxs-lookup"><span data-stu-id="e53e8-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="e53e8-105">Puslapyje **Peržiūrėti bendrojo planavimo eigą** galite peržiūrėti istorinius bendrojo planavimo vykdymus kaip Gantt diagramą.</span><span class="sxs-lookup"><span data-stu-id="e53e8-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="e53e8-106">Ši funkcija gali padėti jums suprasti įvairių bendrojo planavimo etapų laiką.</span><span class="sxs-lookup"><span data-stu-id="e53e8-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="e53e8-107">Dėl dabartinės aktyvios planavimo užduoties, puslapį **Peržiūrėti pagrindinio planavimo eigą** galima naudoti norint sekti eigą ir peržiūrėti apskaičiuotą likusį laiką.</span><span class="sxs-lookup"><span data-stu-id="e53e8-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="e53e8-108">Pagrindinio plano eigos vizualizacijos funkcijos įjungimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="e53e8-109">Norėdami naudoti šią funkciją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e53e8-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="e53e8-110">Darbo srityje **Funkcijos valdymas** skirtuke **Naujas** iš sąrašo pasirinkite **Pagrindinio planavimo eigos vizualizavimas**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="e53e8-111">Jei funkcija neatsiranda skirtuke **Naujas**, žiūrėkite skirtukus **Neįjungta** ir **Visi**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="e53e8-112">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-112">Select **Enable now**.</span></span> <span data-ttu-id="e53e8-113">Arba pasirinkite **Grafikas** ir pasirinkite laiką, kada norite, kad funkcija būtų įjungta.</span><span class="sxs-lookup"><span data-stu-id="e53e8-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="e53e8-114">Puslapyje **Bendrojo planavimo eiga** puslapyje gali būti rodomos istorinės planavimo užduotys ir aktyvios planavimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="e53e8-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="e53e8-115">Norint peržiūrėti istorines planavimo užduotis, galimos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="e53e8-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="e53e8-116">Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**, tada veiksmų skyde pasirinkite **Istorija**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="e53e8-117">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**</span><span class="sxs-lookup"><span data-stu-id="e53e8-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="e53e8-118">Eikite į **Bendrasis planavimas\> Darbo sritys \> Bendrasis planavimas**, bendrajame planavime spustelėkite **Istorija**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="e53e8-119">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**</span><span class="sxs-lookup"><span data-stu-id="e53e8-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e53e8-120">Norint peržiūrėti aktyvias planavimo užduotis, galimos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="e53e8-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="e53e8-121">Eikite į **Bendrasis planavimas \> Darbo sritys \> Bendrasis planavimas**, veiksmų skyde pasirinkite **Nebaigta planavimo eiga**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="e53e8-122">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="e53e8-123">Eikite į **Bendrasis planavimas\> Darbo sritys \> Bendrasis planavimas**, bendrajame planavime spustelėkite **Peržiūrėti eigą**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="e53e8-124">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**</span><span class="sxs-lookup"><span data-stu-id="e53e8-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e53e8-125">Atkreipkite dėmesį, kad aktyvias užduotis galite peržiūrėti, tik kai vykdoma planavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="e53e8-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="e53e8-126">Bendrojo planavimo užduoties analizavimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-126">Analyze a master planning job</span></span>

<span data-ttu-id="e53e8-127">Gantt diagramoje galite išplėsti kiekvieną iš šių planavimo eigų, norėdami peržiūrėti papildomą informaciją apie skirtą laiką:</span><span class="sxs-lookup"><span data-stu-id="e53e8-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="e53e8-128">Inicijuojama</span><span class="sxs-lookup"><span data-stu-id="e53e8-128">Initializing</span></span>
- <span data-ttu-id="e53e8-129">Naikinami ir įterpiami duomenys</span><span class="sxs-lookup"><span data-stu-id="e53e8-129">Deleting and inserting data</span></span>
- <span data-ttu-id="e53e8-130">Padengimo planavimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-130">Coverage planning</span></span>
- <span data-ttu-id="e53e8-131">Delsos</span><span class="sxs-lookup"><span data-stu-id="e53e8-131">Delays</span></span>
- <span data-ttu-id="e53e8-132">Veiksmų pranešimai</span><span class="sxs-lookup"><span data-stu-id="e53e8-132">Action messages</span></span>
- <span data-ttu-id="e53e8-133">Užbaigimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-133">Finalization</span></span>
- <span data-ttu-id="e53e8-134">Automatinis patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-134">Auto-firming</span></span>

<span data-ttu-id="e53e8-135">Gantt diagrama yra naudingas įrankis, jei norite peržiūrėti veiksmų pranešimų naudojimo poveikį.</span><span class="sxs-lookup"><span data-stu-id="e53e8-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="e53e8-136">Gantt diagramos naršymas</span><span class="sxs-lookup"><span data-stu-id="e53e8-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="e53e8-137">Norėdami išplėsti pasirinktą grupę ir rodyti išsamią informaciją, medžio rodinyje pasirinkite pliuso ženklą (**+**).</span><span class="sxs-lookup"><span data-stu-id="e53e8-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="e53e8-138">Norėdami sutraukti pažymėtą grupę, medžio rodinyje pasirinkite minuso ženklą (**–**).</span><span class="sxs-lookup"><span data-stu-id="e53e8-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="e53e8-139">Naršymui galite naudoti klaviatūrą.</span><span class="sxs-lookup"><span data-stu-id="e53e8-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="e53e8-140">Klavišais **Rodyklės į viršų** ir **Rodyklė į apačią** galite judėti tarp eilučių.</span><span class="sxs-lookup"><span data-stu-id="e53e8-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="e53e8-141">Naudokite klavišus **Rodyklė į dešinę** ir **Rodyklė į kairę**, kad išplėstumėte ir sutrauktumėte grupes.</span><span class="sxs-lookup"><span data-stu-id="e53e8-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="e53e8-142">Norėdami atidaryti arba uždaryti visus Gantt diagramos lygius, pasirinkite **Išplėsti viską** arba **Sutraukti viską**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="e53e8-143">Norėdami peržiūrėti susijusį vykdymo laiką, užveskite žymeklį virš užduoties.</span><span class="sxs-lookup"><span data-stu-id="e53e8-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="e53e8-144">(Užduotys yra žemiausias lygis Gantt diagramoje.)</span><span class="sxs-lookup"><span data-stu-id="e53e8-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="e53e8-145">Papildomo pagrindinio planavimo vykdymo peržiūrėjimas norint palyginti užduotis</span><span class="sxs-lookup"><span data-stu-id="e53e8-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="e53e8-146">Pasirinkus bendrojo planavimo užduotį lauke **Rodyti papildomą bendrąjį planavimą**, Gantt diagramoje galite peržiūrėti papildomo bendrojo planavimo vykdymą ir palyginti dvi užduotis.</span><span class="sxs-lookup"><span data-stu-id="e53e8-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="e53e8-147">KS lygio rodymas</span><span class="sxs-lookup"><span data-stu-id="e53e8-147">BOM-level display</span></span>

<span data-ttu-id="e53e8-148">Komplektavimo specifikacijų (KS) lygiai rodomi skirtingų padengimų planavimui, vėlavimams, veiksmams ir patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="e53e8-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="e53e8-149">**Padengimo planavimas** – KS lygiai rodomi kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="e53e8-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e53e8-150">Jie apskaičiuojami iš viršaus į apačią.</span><span class="sxs-lookup"><span data-stu-id="e53e8-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="e53e8-151">**Pavyzdys:** KS lygis 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e53e8-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e53e8-152">**Vėlavimai** – KS lygiai rodomi kaip padengimo planavimo KS lygiai, padauginti iš –1.</span><span class="sxs-lookup"><span data-stu-id="e53e8-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="e53e8-153">(Kitaip tariant, jie turi neigiamą ženklą.)</span><span class="sxs-lookup"><span data-stu-id="e53e8-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="e53e8-154">**Pavyzdys:** KS lygis –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="e53e8-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="e53e8-155">**Veiksmo pranešimas** – KS lygiai rodomi kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="e53e8-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e53e8-156">Jie apskaičiuojami iš viršaus į apačią.</span><span class="sxs-lookup"><span data-stu-id="e53e8-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="e53e8-157">**Pavyzdys:** KS lygis 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e53e8-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e53e8-158">**Automatinis patvirtinimas** – KS lygiai rodomi kaip 999 minus padengimo planavimo KS lygis.</span><span class="sxs-lookup"><span data-stu-id="e53e8-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="e53e8-159">**Pavyzdys:** KS lygis 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="e53e8-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="e53e8-160">Šioje lentelėje apibendrinama elgsena.</span><span class="sxs-lookup"><span data-stu-id="e53e8-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="e53e8-161">Rodomas KS lygis</span><span class="sxs-lookup"><span data-stu-id="e53e8-161">BOM level that is shown</span></span> | <span data-ttu-id="e53e8-162">Galutinė prekė</span><span class="sxs-lookup"><span data-stu-id="e53e8-162">End item</span></span> | <span data-ttu-id="e53e8-163">Subkomponentas</span><span class="sxs-lookup"><span data-stu-id="e53e8-163">Subcomponent</span></span> | <span data-ttu-id="e53e8-164">Žaliavos</span><span class="sxs-lookup"><span data-stu-id="e53e8-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="e53e8-165">Padengimo planavimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-165">Coverage planning</span></span> | <span data-ttu-id="e53e8-166">0</span><span class="sxs-lookup"><span data-stu-id="e53e8-166">0</span></span> | <span data-ttu-id="e53e8-167">1</span><span class="sxs-lookup"><span data-stu-id="e53e8-167">1</span></span> | <span data-ttu-id="e53e8-168">2</span><span class="sxs-lookup"><span data-stu-id="e53e8-168">2</span></span> |
| <span data-ttu-id="e53e8-169">Delsos</span><span class="sxs-lookup"><span data-stu-id="e53e8-169">Delays</span></span> | <span data-ttu-id="e53e8-170">0</span><span class="sxs-lookup"><span data-stu-id="e53e8-170">0</span></span> | <span data-ttu-id="e53e8-171">–1</span><span class="sxs-lookup"><span data-stu-id="e53e8-171">–1</span></span> | <span data-ttu-id="e53e8-172">–2</span><span class="sxs-lookup"><span data-stu-id="e53e8-172">–2</span></span> |
| <span data-ttu-id="e53e8-173">Veiksmo pranešimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-173">Action message</span></span> | <span data-ttu-id="e53e8-174">0</span><span class="sxs-lookup"><span data-stu-id="e53e8-174">0</span></span> | <span data-ttu-id="e53e8-175">1</span><span class="sxs-lookup"><span data-stu-id="e53e8-175">1</span></span> | <span data-ttu-id="e53e8-176">2</span><span class="sxs-lookup"><span data-stu-id="e53e8-176">2</span></span> |
| <span data-ttu-id="e53e8-177">Automatinis patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-177">Auto-firming</span></span> | <span data-ttu-id="e53e8-178">999</span><span class="sxs-lookup"><span data-stu-id="e53e8-178">999</span></span> | <span data-ttu-id="e53e8-179">998</span><span class="sxs-lookup"><span data-stu-id="e53e8-179">998</span></span> | <span data-ttu-id="e53e8-180">997</span><span class="sxs-lookup"><span data-stu-id="e53e8-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="e53e8-181">Eigos vizualizavimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-181">Visualize progress</span></span>

<span data-ttu-id="e53e8-182">Jei peržiūrite bendrojo planavimo užduotį, kuri šiuo metu vykdoma, eiga rodoma spalvotai Gantt diagramoje.</span><span class="sxs-lookup"><span data-stu-id="e53e8-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="e53e8-183">Toliau nurodytos spalvos taikomos mėlynai temai.</span><span class="sxs-lookup"><span data-stu-id="e53e8-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="e53e8-184">Kitose spalvų temose spalvos skirsis.</span><span class="sxs-lookup"><span data-stu-id="e53e8-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="e53e8-185">**Tamsiai mėlyna** – baigtos planavimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="e53e8-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="e53e8-186">**Oranžinė** – šiuo metu vykdoma užduotis.</span><span class="sxs-lookup"><span data-stu-id="e53e8-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="e53e8-187">**Žydra** – likusių užduočių įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="e53e8-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="e53e8-188">Spalva rodoma tik žemiausiame Gantt diagramos lygyje.</span><span class="sxs-lookup"><span data-stu-id="e53e8-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="e53e8-189">Norėdami peržiūrėti visas užduotis pagrindinio planavimo užduotyje, pasirinkite **Išplėsti viską** .</span><span class="sxs-lookup"><span data-stu-id="e53e8-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="e53e8-190">Likusių užduočių įvertinimas paremtas istorinėmis bendrojo planavimo užduotimis.</span><span class="sxs-lookup"><span data-stu-id="e53e8-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="e53e8-191">Pagrindinio planavimo vykdymas ir vykdymo eigos stebėjimas</span><span class="sxs-lookup"><span data-stu-id="e53e8-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="e53e8-192">Numatytoje ataskaitų srityje pasirinkite **Pagrindinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="e53e8-193">Lauke **Planas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e53e8-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="e53e8-194">Pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-194">Select **Run**.</span></span>
1. <span data-ttu-id="e53e8-195">Parinktį **Stebėti vykdymo laiką** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="e53e8-196">Lauke **Gijų skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e53e8-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="e53e8-197">„FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="e53e8-198">Tinklelyje pasirinkite eilutę, kurioje laukas **Laukas** yra nustatytas kaip **Elemento numeris.**</span><span class="sxs-lookup"><span data-stu-id="e53e8-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="e53e8-199">Lauke **Kriterijai** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e53e8-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="e53e8-200">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e53e8-200">Select **OK**.</span></span>
