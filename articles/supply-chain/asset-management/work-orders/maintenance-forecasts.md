---
title: Priežiūros prognozės
description: Šioje temoje aprašomos priežiūros prognozės modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875801"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="36cef-103">Priežiūros prognozės</span><span class="sxs-lookup"><span data-stu-id="36cef-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="36cef-104">Kai sukuriate darbo užsakymą, sukuriate darbo užsakymo užduotis su susijusiu turtu ir priežiūros užduočių tipais.</span><span class="sxs-lookup"><span data-stu-id="36cef-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="36cef-105">Kai pasirenkate priežiūros užduoties tipą, kuriame yra priežiūros prognozių, prognozės automatiškai nukopijuojamos į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="36cef-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="36cef-106">Galbūt turėsite galimybę įtraukti arba pašalinti darbo užsakymo prognozės eilutes.</span><span class="sxs-lookup"><span data-stu-id="36cef-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="36cef-107">Darbo užsakymo ciklo būsenos sąranka, susijęs projekto tipas ir su projekto tipu susijusios etapo taisyklės nulemia tai, ar galite įtraukti arba redaguoti prognozės eilutes.</span><span class="sxs-lookup"><span data-stu-id="36cef-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="36cef-108">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="36cef-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="36cef-109">Sąraše pasirinkite darbo užsakymą ir spustelėkite **Prognozė**.</span><span class="sxs-lookup"><span data-stu-id="36cef-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="36cef-110">Pasirinkus **Darbo užsakymo priežiūros prognozė**, rodomos priežiūros užduoties tipo, pasirinkto darbo užsakymo užduotyje, prognozės eilutės.</span><span class="sxs-lookup"><span data-stu-id="36cef-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="36cef-111">Valandų prognozės įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="36cef-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="36cef-112">Pažymėkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.</span><span class="sxs-lookup"><span data-stu-id="36cef-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="36cef-113">Norėdami sukurti naują eilutę, FastTab **Valandos** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="36cef-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="36cef-114">Lauke **Kategorija** pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="36cef-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="36cef-115">Į lauką **Valandos** įterpkite prognozuojamų valandų skaičių.</span><span class="sxs-lookup"><span data-stu-id="36cef-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="36cef-116">Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.</span><span class="sxs-lookup"><span data-stu-id="36cef-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="36cef-117">Prekių prognozės įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="36cef-117">Add items forecast to a work order</span></span>

<span data-ttu-id="36cef-118">Yra trys būdai įtraukti prekes į darbo užsakymo priežiūros prognozę: galite kurti į atsarginių dalių sąrašą arba turto KS neįtrauktų prekių (atsarginių dalių) eilutes, galite pasirinkti atsargines dalis iš patvirtinto atsarginių dalių sąrašo ir galite pasirinkti prekes iš turto KS.</span><span class="sxs-lookup"><span data-stu-id="36cef-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="36cef-119">Pažymėkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.</span><span class="sxs-lookup"><span data-stu-id="36cef-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="36cef-120">Pasirinkite FastTab **Prekės**.</span><span class="sxs-lookup"><span data-stu-id="36cef-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="36cef-121">Spustelėję **Įtraukti**, įtraukite naują atsarginės dalies, neįtrauktos į atsarginių dalių sąrašą arba turto KS sąrašą, eilutę.</span><span class="sxs-lookup"><span data-stu-id="36cef-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="36cef-122">Lauke **Prekės numeris** pasirinkite prekę.</span><span class="sxs-lookup"><span data-stu-id="36cef-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="36cef-123">Lauke **Pardavimo kiekis** įterpkite kiekį, o lauke **Vienetas** pasirinkite kiekio vienetą.</span><span class="sxs-lookup"><span data-stu-id="36cef-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="36cef-124">Į atitinkamus laukus įterpkite savikainą ir valiutą ir pasirinkite **Eilutės ypatybė**.</span><span class="sxs-lookup"><span data-stu-id="36cef-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="36cef-125">Jei norite pakeisti prekės eilutėse rodomų dimensijų sąrašą, spustelėkite **Atsargos** > **Rodyti dimensijas**, pasirinkite dimensijas, paskui perjungimo mygtuke **Įrašyti sąranką** pasirinkite „Taip”.</span><span class="sxs-lookup"><span data-stu-id="36cef-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="36cef-126">Jei į priežiūros prognozę norite įtraukti patvirtintą atsarginę dalį, spustelėkite **Įtraukti atsarginių dalių**, pasirinkite atsarginę dalį, jei reikia, pakoreguokite susijusią informaciją ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="36cef-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="36cef-127">Jei į prognozę norite įtraukti turto KS prekių, spustelėkite **Įtraukti KS prekių**, pasirinkite prekę, jei reikia, pakoreguokite susijusią informaciją ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="36cef-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="36cef-128">Spustelėkite **Kur naudota prekė**, jei norite pamatyti, kur pasirinktoje eilutėje esanti prekė naudojama modulyje Turto valdymas turto, priežiūros užduoties tipo numatytųjų reikšmių, atsarginių dalių ir darbo užsakymų atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="36cef-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="36cef-129">Išlaidų prognozės įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="36cef-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="36cef-130">Šioje temoje aiškinama, kaip įtraukti išlaidų prognozę į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="36cef-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="36cef-131">Formos kairėje pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.</span><span class="sxs-lookup"><span data-stu-id="36cef-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="36cef-132">Pasirinkite FastTab **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="36cef-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="36cef-133">Sukurkite naują eilutę, spustelėję **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="36cef-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="36cef-134">Lauke **Kategorija** pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="36cef-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="36cef-135">Lauke **Kiekis** įterpkite kiekį.</span><span class="sxs-lookup"><span data-stu-id="36cef-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="36cef-136">Į atitinkamus laukus įterpkite savikainą, pardavimo valiutą ir pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="36cef-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="36cef-137">Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.</span><span class="sxs-lookup"><span data-stu-id="36cef-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="36cef-138">FastTab **Priežiūros prognozių sumos** matote pasirinktos darbo užsakymo užduoties ir darbo užsakymo kiekviename skirtuke sukurtų eilučių skaičiaus apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="36cef-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="36cef-139">Taip pat matote darbo užsakymo užduoties ir darbo užsakymo prognozuojamų darbo valandų sumą.</span><span class="sxs-lookup"><span data-stu-id="36cef-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![1 pav.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="36cef-141">Darbo užsakymo prognozių automatinis naujinimas</span><span class="sxs-lookup"><span data-stu-id="36cef-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="36cef-142">Modulyje Turto valdymas galima automatiškai naujinti darbo užsakymų prognozių informaciją apie valandos kainas, prekių kainas ir išlaidas, kuri buvo atnaujinta kituose „Dynamics 365 for Finance and Operations“ moduliuose.</span><span class="sxs-lookup"><span data-stu-id="36cef-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="36cef-143">Tai daroma siekiant užtikrinti, kad darbo užsakymų prognozėse naudojamos aktualiausios savikainos.</span><span class="sxs-lookup"><span data-stu-id="36cef-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="36cef-144">Taip pat galima naujinti ir [priežiūros užduočių tipo prognozes](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="36cef-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="36cef-145">Spustelėkite **Turto valdymas** > **Periodinis** > **Prognozė** > **Naujinti darbo užsakymo prognozę**.</span><span class="sxs-lookup"><span data-stu-id="36cef-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="36cef-146">Išplečiamajame dialogo lange **Naujinti darbo užsakymo prognozę**, jei reikia, galite pasirinkti parametrus, susijusius su konkrečiais darbo užsakymais arba darbo užsakymų užduotimis.</span><span class="sxs-lookup"><span data-stu-id="36cef-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="36cef-147">Norėdami pasirinkti, spustelėkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="36cef-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="36cef-148">Jei reikia, galite nustatyti automatinio naujinimo paketinę užduotį FastTab **Vykdyti fone**.</span><span class="sxs-lookup"><span data-stu-id="36cef-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="36cef-149">Spustelėjus **Gerai**, pradedamas prognozės naujinimas.</span><span class="sxs-lookup"><span data-stu-id="36cef-149">Click **OK** to start the forecast update.</span></span>


![2 paveikslėlis](media/07-work-orders.png)

