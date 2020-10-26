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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 045b82af6f65b22e1c683f8de47a6df282711e6a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978135"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="9267e-103">Bendrojo planavimo vykdymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="9267e-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="9267e-104">Gantt diagramos naudojimas siekiant vizualizuoti bendrojo planavimo eigą</span><span class="sxs-lookup"><span data-stu-id="9267e-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="9267e-105">Puslapyje **Peržiūrėti bendrojo planavimo eigą** galite peržiūrėti istorinius bendrojo planavimo vykdymus kaip Gantt diagramą.</span><span class="sxs-lookup"><span data-stu-id="9267e-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="9267e-106">Ši funkcija gali padėti jums suprasti įvairių bendrojo planavimo etapų laiką.</span><span class="sxs-lookup"><span data-stu-id="9267e-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="9267e-107">Dėl dabartinės aktyvios planavimo užduoties, puslapį **Peržiūrėti pagrindinio planavimo eigą** galima naudoti norint sekti eigą ir peržiūrėti apskaičiuotą likusį laiką.</span><span class="sxs-lookup"><span data-stu-id="9267e-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="9267e-108">Pagrindinio plano eigos vizualizacijos funkcijos įjungimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="9267e-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="9267e-109">Norėdami naudoti šią funkciją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9267e-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="9267e-110">Darbo srityje **Funkcijos valdymas** skirtuke **Naujas** iš sąrašo pasirinkite **Pagrindinio planavimo eigos vizualizavimas**.</span><span class="sxs-lookup"><span data-stu-id="9267e-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="9267e-111">Jei funkcija neatsiranda skirtuke **Naujas**, žiūrėkite skirtukus **Neįjungta** ir **Visi**.</span><span class="sxs-lookup"><span data-stu-id="9267e-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="9267e-112">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="9267e-112">Select **Enable now**.</span></span> <span data-ttu-id="9267e-113">Arba pasirinkite **Grafikas**ir pasirinkite laiką, kada norite, kad funkcija būtų įjungta.</span><span class="sxs-lookup"><span data-stu-id="9267e-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="9267e-114">Puslapyje **Bendrojo planavimo eiga** puslapyje gali būti rodomos istorinės planavimo užduotys ir aktyvios planavimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="9267e-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="9267e-115">Norint peržiūrėti istorines planavimo užduotis, galimos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="9267e-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="9267e-116">Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**, tada veiksmų skyde pasirinkite **Istorija**.</span><span class="sxs-lookup"><span data-stu-id="9267e-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="9267e-117">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**</span><span class="sxs-lookup"><span data-stu-id="9267e-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="9267e-118">Eikite į **Bendrasis planavimas\> Darbo sritys \> Bendrasis planavimas**, bendrajame planavime spustelėkite **Istorija**.</span><span class="sxs-lookup"><span data-stu-id="9267e-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="9267e-119">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**</span><span class="sxs-lookup"><span data-stu-id="9267e-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="9267e-120">Norint peržiūrėti aktyvias planavimo užduotis, galimos dvi parinktys.</span><span class="sxs-lookup"><span data-stu-id="9267e-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="9267e-121">Eikite į **Bendrasis planavimas \> Darbo sritys \> Bendrasis planavimas**, veiksmų skyde pasirinkite **Nebaigta planavimo eiga**.</span><span class="sxs-lookup"><span data-stu-id="9267e-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="9267e-122">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**.</span><span class="sxs-lookup"><span data-stu-id="9267e-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="9267e-123">Eikite į **Bendrasis planavimas\> Darbo sritys \> Bendrasis planavimas**, bendrajame planavime spustelėkite **Peržiūrėti eigą**.</span><span class="sxs-lookup"><span data-stu-id="9267e-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="9267e-124">Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**</span><span class="sxs-lookup"><span data-stu-id="9267e-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="9267e-125">Atkreipkite dėmesį, kad aktyvias užduotis galite peržiūrėti, tik kai vykdoma planavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="9267e-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="9267e-126">Bendrojo planavimo užduoties analizavimas</span><span class="sxs-lookup"><span data-stu-id="9267e-126">Analyze a master planning job</span></span>

<span data-ttu-id="9267e-127">Gantt diagramoje galite išplėsti kiekvieną iš šių planavimo eigų, norėdami peržiūrėti papildomą informaciją apie skirtą laiką:</span><span class="sxs-lookup"><span data-stu-id="9267e-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="9267e-128">Inicijuojama</span><span class="sxs-lookup"><span data-stu-id="9267e-128">Initializing</span></span>
- <span data-ttu-id="9267e-129">Naikinami ir įterpiami duomenys</span><span class="sxs-lookup"><span data-stu-id="9267e-129">Deleting and inserting data</span></span>
- <span data-ttu-id="9267e-130">Padengimo planavimas</span><span class="sxs-lookup"><span data-stu-id="9267e-130">Coverage planning</span></span>
- <span data-ttu-id="9267e-131">Delsos</span><span class="sxs-lookup"><span data-stu-id="9267e-131">Delays</span></span>
- <span data-ttu-id="9267e-132">Veiksmų pranešimai</span><span class="sxs-lookup"><span data-stu-id="9267e-132">Action messages</span></span>
- <span data-ttu-id="9267e-133">Užbaigimas</span><span class="sxs-lookup"><span data-stu-id="9267e-133">Finalization</span></span>
- <span data-ttu-id="9267e-134">Automatinis patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="9267e-134">Auto-firming</span></span>

<span data-ttu-id="9267e-135">Gantt diagrama yra naudingas įrankis, jei norite peržiūrėti veiksmų pranešimų naudojimo poveikį.</span><span class="sxs-lookup"><span data-stu-id="9267e-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="9267e-136">Gantt diagramos naršymas</span><span class="sxs-lookup"><span data-stu-id="9267e-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="9267e-137">Norėdami išplėsti pasirinktą grupę ir rodyti išsamią informaciją, medžio rodinyje pasirinkite pliuso ženklą (**+**).</span><span class="sxs-lookup"><span data-stu-id="9267e-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="9267e-138">Norėdami sutraukti pažymėtą grupę, medžio rodinyje pasirinkite minuso ženklą (**–**).</span><span class="sxs-lookup"><span data-stu-id="9267e-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="9267e-139">Naršymui galite naudoti klaviatūrą.</span><span class="sxs-lookup"><span data-stu-id="9267e-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="9267e-140">Klavišais **Rodyklės į viršų** ir **Rodyklė į apačią** galite judėti tarp eilučių.</span><span class="sxs-lookup"><span data-stu-id="9267e-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="9267e-141">Naudokite klavišus **Rodyklė į dešinę** ir **Rodyklė į kairę**, kad išplėstumėte ir sutrauktumėte grupes.</span><span class="sxs-lookup"><span data-stu-id="9267e-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="9267e-142">Norėdami atidaryti arba uždaryti visus Gantt diagramos lygius, pasirinkite **Išplėsti viską** arba **Sutraukti viską**.</span><span class="sxs-lookup"><span data-stu-id="9267e-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="9267e-143">Norėdami peržiūrėti susijusį vykdymo laiką, užveskite žymeklį virš užduoties.</span><span class="sxs-lookup"><span data-stu-id="9267e-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="9267e-144">(Užduotys yra žemiausias lygis Gantt diagramoje.)</span><span class="sxs-lookup"><span data-stu-id="9267e-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="9267e-145">Papildomo pagrindinio planavimo vykdymo peržiūrėjimas norint palyginti užduotis</span><span class="sxs-lookup"><span data-stu-id="9267e-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="9267e-146">Pasirinkus bendrojo planavimo užduotį lauke **Rodyti papildomą bendrąjį planavimą**, Gantt diagramoje galite peržiūrėti papildomo bendrojo planavimo vykdymą ir palyginti dvi užduotis.</span><span class="sxs-lookup"><span data-stu-id="9267e-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="9267e-147">KS lygio rodymas</span><span class="sxs-lookup"><span data-stu-id="9267e-147">BOM-level display</span></span>

<span data-ttu-id="9267e-148">Komplektavimo specifikacijų (KS) lygiai rodomi skirtingų padengimų planavimui, vėlavimams, veiksmams ir patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="9267e-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="9267e-149">**Padengimo planavimas** – KS lygiai rodomi kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="9267e-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="9267e-150">Jie apskaičiuojami iš viršaus į apačią.</span><span class="sxs-lookup"><span data-stu-id="9267e-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="9267e-151">**Pavyzdys:** KS lygis 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="9267e-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="9267e-152">**Vėlavimai** – KS lygiai rodomi kaip padengimo planavimo KS lygiai, padauginti iš –1.</span><span class="sxs-lookup"><span data-stu-id="9267e-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="9267e-153">(Kitaip tariant, jie turi neigiamą ženklą.)</span><span class="sxs-lookup"><span data-stu-id="9267e-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="9267e-154">**Pavyzdys:** KS lygis –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="9267e-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="9267e-155">**Veiksmo pranešimas** – KS lygiai rodomi kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="9267e-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="9267e-156">Jie apskaičiuojami iš viršaus į apačią.</span><span class="sxs-lookup"><span data-stu-id="9267e-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="9267e-157">**Pavyzdys:** KS lygis 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="9267e-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="9267e-158">**Automatinis patvirtinimas** – KS lygiai rodomi kaip 999 minus padengimo planavimo KS lygis.</span><span class="sxs-lookup"><span data-stu-id="9267e-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="9267e-159">**Pavyzdys:** KS lygis 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="9267e-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="9267e-160">Šioje lentelėje apibendrinama elgsena.</span><span class="sxs-lookup"><span data-stu-id="9267e-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="9267e-161">Rodomas KS lygis</span><span class="sxs-lookup"><span data-stu-id="9267e-161">BOM level that is shown</span></span> | <span data-ttu-id="9267e-162">Galutinė prekė</span><span class="sxs-lookup"><span data-stu-id="9267e-162">End item</span></span> | <span data-ttu-id="9267e-163">Subkomponentas</span><span class="sxs-lookup"><span data-stu-id="9267e-163">Subcomponent</span></span> | <span data-ttu-id="9267e-164">Žaliavos</span><span class="sxs-lookup"><span data-stu-id="9267e-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="9267e-165">Padengimo planavimas</span><span class="sxs-lookup"><span data-stu-id="9267e-165">Coverage planning</span></span> | <span data-ttu-id="9267e-166">0</span><span class="sxs-lookup"><span data-stu-id="9267e-166">0</span></span> | <span data-ttu-id="9267e-167">1</span><span class="sxs-lookup"><span data-stu-id="9267e-167">1</span></span> | <span data-ttu-id="9267e-168">2</span><span class="sxs-lookup"><span data-stu-id="9267e-168">2</span></span> |
| <span data-ttu-id="9267e-169">Delsos</span><span class="sxs-lookup"><span data-stu-id="9267e-169">Delays</span></span> | <span data-ttu-id="9267e-170">0</span><span class="sxs-lookup"><span data-stu-id="9267e-170">0</span></span> | <span data-ttu-id="9267e-171">–1</span><span class="sxs-lookup"><span data-stu-id="9267e-171">–1</span></span> | <span data-ttu-id="9267e-172">–2</span><span class="sxs-lookup"><span data-stu-id="9267e-172">–2</span></span> |
| <span data-ttu-id="9267e-173">Veiksmo pranešimas</span><span class="sxs-lookup"><span data-stu-id="9267e-173">Action message</span></span> | <span data-ttu-id="9267e-174">0</span><span class="sxs-lookup"><span data-stu-id="9267e-174">0</span></span> | <span data-ttu-id="9267e-175">1</span><span class="sxs-lookup"><span data-stu-id="9267e-175">1</span></span> | <span data-ttu-id="9267e-176">2</span><span class="sxs-lookup"><span data-stu-id="9267e-176">2</span></span> |
| <span data-ttu-id="9267e-177">Automatinis patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="9267e-177">Auto-firming</span></span> | <span data-ttu-id="9267e-178">999</span><span class="sxs-lookup"><span data-stu-id="9267e-178">999</span></span> | <span data-ttu-id="9267e-179">998</span><span class="sxs-lookup"><span data-stu-id="9267e-179">998</span></span> | <span data-ttu-id="9267e-180">997</span><span class="sxs-lookup"><span data-stu-id="9267e-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="9267e-181">Eigos vizualizavimas</span><span class="sxs-lookup"><span data-stu-id="9267e-181">Visualize progress</span></span>

<span data-ttu-id="9267e-182">Jei peržiūrite bendrojo planavimo užduotį, kuri šiuo metu vykdoma, eiga rodoma spalvotai Gantt diagramoje.</span><span class="sxs-lookup"><span data-stu-id="9267e-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="9267e-183">Toliau nurodytos spalvos taikomos mėlynai temai.</span><span class="sxs-lookup"><span data-stu-id="9267e-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="9267e-184">Kitose spalvų temose spalvos skirsis.</span><span class="sxs-lookup"><span data-stu-id="9267e-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="9267e-185">**Tamsiai mėlyna** – baigtos planavimo užduotys.</span><span class="sxs-lookup"><span data-stu-id="9267e-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="9267e-186">**Oranžinė** – šiuo metu vykdoma užduotis.</span><span class="sxs-lookup"><span data-stu-id="9267e-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="9267e-187">**Žydra** – likusių užduočių įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="9267e-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="9267e-188">Spalva rodoma tik žemiausiame Gantt diagramos lygyje.</span><span class="sxs-lookup"><span data-stu-id="9267e-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="9267e-189">Norėdami peržiūrėti visas užduotis pagrindinio planavimo užduotyje, pasirinkite **Išplėsti viską** .</span><span class="sxs-lookup"><span data-stu-id="9267e-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="9267e-190">Likusių užduočių įvertinimas paremtas istorinėmis bendrojo planavimo užduotimis.</span><span class="sxs-lookup"><span data-stu-id="9267e-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="9267e-191">Pagrindinio planavimo vykdymas ir vykdymo eigos stebėjimas</span><span class="sxs-lookup"><span data-stu-id="9267e-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="9267e-192">Numatytoje ataskaitų srityje pasirinkite **Pagrindinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="9267e-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="9267e-193">Lauke **Planas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9267e-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="9267e-194">Pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="9267e-194">Select **Run**.</span></span>
1. <span data-ttu-id="9267e-195">Parinktį **Stebėti vykdymo laiką** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9267e-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="9267e-196">Lauke **Gijų skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9267e-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="9267e-197">„FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="9267e-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="9267e-198">Tinklelyje pasirinkite eilutę, kurioje laukas **Laukas** yra nustatytas kaip **Elemento numeris.**</span><span class="sxs-lookup"><span data-stu-id="9267e-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="9267e-199">Lauke **Kriterijai** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9267e-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="9267e-200">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9267e-200">Select **OK**.</span></span>
