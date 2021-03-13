---
title: Darbo grafiko kūrimas bangos metu
description: Šioje temoje aprašoma, kaip nustatyti ir naudoti Darbo grafiko kūrimo bangos apdorojimo metodą.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078288"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="0d552-103">Darbo grafiko kūrimas bangos metu</span><span class="sxs-lookup"><span data-stu-id="0d552-103">Schedule work creation during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d552-104">Naudokite funkciją *Darbo grafiko kūrimas* kaip jūsų bangos apdorojimo proceso dalį, kad padidintumėte bangos apdorojimo našumą, sistemoje sukurdami darbą naudojant lygiagretųjį apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="0d552-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="0d552-105">Įgalinus funkciją, automatiškai sukuriamas suplanuotas darbas, kurį sistema galiausiai apdoros sukurti faktiniam darbui.</span><span class="sxs-lookup"><span data-stu-id="0d552-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="0d552-106">Jei bangos įkelties eilučių skaičius pasiekia iš anksto nustatytą ribinę vertę, sistema sukurs faktinį darbą greičiau, pritaikydama lygiagretųjį asinchroninį apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="0d552-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="0d552-107">Darbo grafiko kūrimo funkcijos įgalinimas</span><span class="sxs-lookup"><span data-stu-id="0d552-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="0d552-108">Funkcijos įjungimas funkcijų valdymo dalyje</span><span class="sxs-lookup"><span data-stu-id="0d552-108">Enable the feature in feature management</span></span>

<span data-ttu-id="0d552-109">Prieš jums naudojant *Darbo grafiko kūrimas* funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="0d552-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="0d552-110">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="0d552-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="0d552-111">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="0d552-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0d552-112">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="0d552-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0d552-113">**Funkcijos pavadinimas:** *Darbo grafiko kūrimas*</span><span class="sxs-lookup"><span data-stu-id="0d552-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="0d552-114">Prieš įgalinant *Darbo grafiko kūrimą*, turite įgalinti *Visos organizacijos darbo blokavimo* funkciją.</span><span class="sxs-lookup"><span data-stu-id="0d552-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="0d552-115">Paketinio bangų apdorojimo įjungimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="0d552-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="0d552-116">Norint pasinaudoti lygiagrečiu asinchroniniu metodu kurti sandėlio darbui, jūsų bangos procesas turi būti vykdomas pakete.</span><span class="sxs-lookup"><span data-stu-id="0d552-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="0d552-117">Norėdami tai nustatyti:</span><span class="sxs-lookup"><span data-stu-id="0d552-117">To set this up:</span></span>

1. <span data-ttu-id="0d552-118">Eikite į  **Sandėlio valdymas\> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="0d552-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="0d552-119">Skirtuke **Bendra** nustatykite **Apdoroti bangas pakete** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="0d552-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="0d552-120">Pasirinktinai galite pasirinkti paskirtą **Bangos apdorojimo paketų grupę** sustabdyti paketų eilės apdorojimo vykdymą tuo pačiu, kaip ir kitų procesų vykdymo, laiku.</span><span class="sxs-lookup"><span data-stu-id="0d552-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="0d552-121">Nustatykite **Laukti užrakto (ms)**, kuris taikomas, kai sistema vienu metu apdoroja kelias bangas.</span><span class="sxs-lookup"><span data-stu-id="0d552-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="0d552-122">Daugumai didesnių bangos procesų rekomenduojame vertę *60 000*.</span><span class="sxs-lookup"><span data-stu-id="0d552-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="0d552-123">Naujo bangos veiksmo metodo neautomatinis įjungimas esamiems bangos šablonams</span><span class="sxs-lookup"><span data-stu-id="0d552-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="0d552-124">Pradėkite sukurdami naują bangos veiksmo metodą ir įgalindami jį lygiagrečiam asinchroniniam užduoties apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="0d552-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="0d552-125">Eikite į **Sandėlio valdymas \>Sąranka \> Bangos \> Bangos apdorojimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="0d552-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="0d552-126">Pasirinkite  **Pakartotinio generavimo** metodą ir atkreipkite dėmesį, kad *„WHSScheduleWorkCreationWaveStepMethod”* buvo įtrauktas į bangos apdorojimo metodų, kuriuos galite naudoti jūsų siuntimo bangos šablonuose, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="0d552-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="0d552-127">Pasirinkite įrašą su **Metodo pavadinimu** *„WHSScheduleWorkCreationWaveStepMethod”* ir pasirinkite **Užduoties konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="0d552-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="0d552-128">Norėdami įtraukti naują eilutę į tinklelį, veiksmų srityje pasirinkite **Naujas** ir naudokite šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="0d552-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="0d552-129">**Sandėlis** – pasirinkite sandėlį, kurį naudosite darbo grafiko kūrimo apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="0d552-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="0d552-130">**Didžiausias paketinių užduočių skaičius** – nurodykite maksimalų paketinių užduočių skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d552-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="0d552-131">Daugeliu atvejų ši vertė turi būti diapazone 8‑16, tačiau patariame eksperimentuoti su optimaliu parametru, atsižvelgiant į jūsų scenarijus.</span><span class="sxs-lookup"><span data-stu-id="0d552-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="0d552-132">**Bangos apdorojimo paketų grupė** – pasirinkite paskirtą bangos apdorojimo paketų grupę, kad optimizuotumėte paketų darbo eilės apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="0d552-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="0d552-133">Dabar esate pasiruošę atnaujinti esamą bangos šabloną (arba sukurti naują) ir naudoti *Darbo grafiko kūrimo* bangos apdorojimo metodą.</span><span class="sxs-lookup"><span data-stu-id="0d552-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="0d552-134">Eikite į  **Sandėlio valdymas\>Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="0d552-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="0d552-135">Pasirinkite **Redaguoti** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="0d552-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="0d552-136">Sąrašo srityje pasirinkite bangos šabloną, kurį norite atnaujinti (jei testuojate naudodami demonstracinius duomenis, tada galite naudoti *24 siuntimo numatytuosius parametrus*).</span><span class="sxs-lookup"><span data-stu-id="0d552-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="0d552-137">Išplėskite „FastTab” **Metodai** ir pasirinkite eilutę, su **Pavadinimu** *Darbo grafiko kūrimas* tinklelyje **Likę metodai**.</span><span class="sxs-lookup"><span data-stu-id="0d552-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="0d552-138">Pasirinkite rodyklę, nukreiptą į stulpelį **Pasirinkti metodai** perkelti pasirinktai eilutei į tą stulpelį.</span><span class="sxs-lookup"><span data-stu-id="0d552-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="0d552-139">(Vienu metu galima pasirinkti tik vieną metodą, kuris naudoja *„WHSScheduleWorkCreationWaveStepMethod”* arba *„createWork”*, taigi, esama eilutė su **Metodo pavadinimu** *„createWork”* yra automatiškai perkeliama į **Likę metodai** tinklelį.)</span><span class="sxs-lookup"><span data-stu-id="0d552-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="0d552-140">Nustatykite bangos užduoties apdorojimo ribinės vertės duomenis</span><span class="sxs-lookup"><span data-stu-id="0d552-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="0d552-141">Sistema sukurs numatytuosius bangos užduoties apdorojimo ribinės vertės duomenis, kai pirmą kartą vykdomas bangos procesas naudojant bet kokį užduotimis pagrįstą apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="0d552-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="0d552-142">Duomenys yra naudojami valdymui, kai bangos apdorojimas bus vykdomas asinchroniškai ir bus pagrįstas užduotimis, o tai leidžia apdoroti ir kurti darbą lygiagrečiai.</span><span class="sxs-lookup"><span data-stu-id="0d552-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="0d552-143">Iš pradžių numatytieji duomenys naudos 15 ribinę vertę mažiausio krovinio eilučių skaičiaus („MINIMUMWAVELOADLINES”) atveju.</span><span class="sxs-lookup"><span data-stu-id="0d552-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="0d552-144">Tai reiškia, kad kai sistema apdoros bangą su daugiau nei 15 įkelties eilučių, ji naudos asinchroninį užduoties apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="0d552-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="0d552-145">Galite rankiniu būdu įterpti/atnaujinti šiuos duomenis **„WHSWaveTaskProcessingThresholdParameters”** lentelėje jūsų bandymo aplinkose, tačiau, jeigu jums reikia pakeisti šį parametrą gamybos aplinkoje, turite susisiekti su „Microsoft” palaikymo tarnyba ir paprašyti atnaujinimo.</span><span class="sxs-lookup"><span data-stu-id="0d552-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="0d552-146">Darbas su funkcija</span><span class="sxs-lookup"><span data-stu-id="0d552-146">Work with the feature</span></span>

<span data-ttu-id="0d552-147">Kai *Darbo grafiko kūrimo* funkcija yra įjungta, bangos apdorojimas sukurs suplanuotą darbą, kuris galiausiai bus panaudotas naujo darbo kūrimo procese.</span><span class="sxs-lookup"><span data-stu-id="0d552-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="0d552-148">Darbo kūrimo metu darbas bus užblokuotas, naudojant *Visos organizacijos darbo blokavimo* funkciją.</span><span class="sxs-lookup"><span data-stu-id="0d552-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="0d552-149">Šiose struktūrinėse schemose parodyta, kaip bangos apdorojimo metu sukuriamas suplanuotas darbas.</span><span class="sxs-lookup"><span data-stu-id="0d552-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Darbo grafiko kūrimas](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="0d552-151">Suplanuotas Darbas</span><span class="sxs-lookup"><span data-stu-id="0d552-151">Planned work</span></span>

<span data-ttu-id="0d552-152">Puslapyje **Suplanuoto darbo informacija** (**Sandėlio valdymas \> Darbas \> Suplanuoto darbo informacija**) rodoma informacija apie suplanuotą darbą, kuris iš pradžių yra sukuriamas bangos apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="0d552-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="0d552-153">Galimos šios **Apdorojimo būsenos** reikšmės:</span><span class="sxs-lookup"><span data-stu-id="0d552-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="0d552-154">**Eilėje** – laukiama, kada suplanuotas darbas bus panaudotas darbui sukurti.</span><span class="sxs-lookup"><span data-stu-id="0d552-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="0d552-155">**Užbaigta** – suplanuotas darbas buvo panaudotas darbui sukurti.</span><span class="sxs-lookup"><span data-stu-id="0d552-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="0d552-156">**Nepavyko** – bangos apdorojimas nepavyko.</span><span class="sxs-lookup"><span data-stu-id="0d552-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="0d552-157">Atkreipkite dėmesį, kad suplanuoto darbo būsena gali būti **Nepavyko** su susijusiu faktiniu darbu arba be jo.</span><span class="sxs-lookup"><span data-stu-id="0d552-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="0d552-158">Kai faktinio darbo kūrimo procesas nepavyksta, faktinio darbo būsena lieka *Atšaukta*.</span><span class="sxs-lookup"><span data-stu-id="0d552-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="0d552-159">Paketinė užduotis darbo kūrimo procesui</span><span class="sxs-lookup"><span data-stu-id="0d552-159">Batch job for the work creation process</span></span>

<span data-ttu-id="0d552-160">Norėdami peržiūrėti paketines užduotis bangų apdorojimui pasirinkite **Paketines užduotis** veiksmų srityje, **Visos bangos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="0d552-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="0d552-161">Čia galite peržiūrėti visą paketinės užduoties informaciją apie kiekvieną paketinės užduoties ID.</span><span class="sxs-lookup"><span data-stu-id="0d552-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>
