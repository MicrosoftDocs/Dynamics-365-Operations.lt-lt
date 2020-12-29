---
title: Priežiūros prognozės
description: Šioje temoje aprašomos priežiūros prognozės modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2686dd6db032239e2a3aac03f3998cee055302f6
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434043"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="3d16d-103">Priežiūros prognozės</span><span class="sxs-lookup"><span data-stu-id="3d16d-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3d16d-104">Kai sukuriate darbo užsakymą, sukuriate darbo užsakymo užduotis su susijusiu turtu ir priežiūros užduočių tipais.</span><span class="sxs-lookup"><span data-stu-id="3d16d-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="3d16d-105">Kai pasirenkate priežiūros užduoties tipą, kuriame yra priežiūros prognozių, prognozės automatiškai nukopijuojamos į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3d16d-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="3d16d-106">Galbūt galėsite įtraukti prognozės eilutes į darbo užsakymą arba panaikinti jas iš darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="3d16d-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="3d16d-107">Darbo užsakymo ciklo būsenos sąranka, susijęs projekto tipas ir su projekto tipu susijusios etapo taisyklės nulemia tai, ar galite įtraukti arba redaguoti prognozės eilutes.</span><span class="sxs-lookup"><span data-stu-id="3d16d-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="3d16d-108">Daugiau informacijos apie darbo užsakymo ciklo būsenas ir susijusius projekto etapus žr. [Prognozės, darbo užsakymai ir projektai](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="3d16d-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="3d16d-109">Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3d16d-110">Sąraše pasirinkite darbo užsakymą, tada veiksmų srityje > skirtuke **Darbo užsakymas** > grupėje **Projektas**, pasirinkite **Prognozė**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="3d16d-111">Puslapyje **Darbo užsakymo priežiūros prognozė** rodomos priežiūros užduoties tipo, pasirinkto darbo užsakymo užduotyje, prognozės eilutės.</span><span class="sxs-lookup"><span data-stu-id="3d16d-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="3d16d-112">Valandų prognozės įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="3d16d-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="3d16d-113">Puslapyje **Darbo užsakymo priežiūros prognozė** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.</span><span class="sxs-lookup"><span data-stu-id="3d16d-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="3d16d-114">Norėdami sukurti naują eilutę, „FastTab” **Valandos** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="3d16d-115">Lauke **Kategorija** pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="3d16d-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="3d16d-116">Į lauką **Valandos** įterpkite prognozuojamų valandų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3d16d-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="3d16d-117">Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.</span><span class="sxs-lookup"><span data-stu-id="3d16d-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="3d16d-118">Prekių prognozės įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="3d16d-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="3d16d-119">Yra trys būdai, kaip įtraukti prekes į darbo užsakymo priežiūros prognozę.</span><span class="sxs-lookup"><span data-stu-id="3d16d-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="3d16d-120">Galite kurti į atsarginių dalių sąrašą arba turto KS neįtrauktų prekių (atsarginių dalių) eilutes, galite pasirinkti atsargines dalis iš patvirtinto atsarginių dalių sąrašo ir galite pasirinkti prekes iš turto KS.</span><span class="sxs-lookup"><span data-stu-id="3d16d-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="3d16d-121">Puslapyje **Darbo užsakymo priežiūros prognozė** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.</span><span class="sxs-lookup"><span data-stu-id="3d16d-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="3d16d-122">„FastTab” **Prekės**, naudodami tinkamą metodą, įtraukite prekes į priežiūros prognozę.</span><span class="sxs-lookup"><span data-stu-id="3d16d-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="3d16d-123">Norėdami įtraukti atsarginės dalies, neįtrauktos į atsarginių dalių sąrašą arba turto KS sąrašą, eilutę atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3d16d-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="3d16d-124">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-124">Select **Add**.</span></span>
2. <span data-ttu-id="3d16d-125">Lauke **Elemento numeris** pasirinkite elementą.</span><span class="sxs-lookup"><span data-stu-id="3d16d-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="3d16d-126">Lauke **Pardavimo kiekis** įveskite kiekį.</span><span class="sxs-lookup"><span data-stu-id="3d16d-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="3d16d-127">Lauke **Vienetas** pasirinkite kiekio matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="3d16d-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="3d16d-128">Laukuose **Savikaina** ir **Valiuta** įveskite tinkamas vertes.</span><span class="sxs-lookup"><span data-stu-id="3d16d-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="3d16d-129">Lauke **Eilutės ypatybė** pasirinkite eilutės ypatybę.</span><span class="sxs-lookup"><span data-stu-id="3d16d-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="3d16d-130">Jei norite pakeisti prekės eilutėse rodomų dimensijų sąrašą, pasirinkite **Atsargos** > **Rodyti dimensijas**, pasirinkite dimensijas, paskui nustatykite parinktį **Įrašyti sąranką** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="3d16d-131">Norėdami įtraukti atsarginę dalį iš patvirtintų atsarginių dalių sąrašo, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3d16d-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="3d16d-132">Pasirinkite **Įtraukti atsarginių dalių**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="3d16d-133">Pasirinkite atsarginę dalį ir pagal poreikį redaguokite susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="3d16d-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="3d16d-134">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-134">Select **OK**.</span></span>

<span data-ttu-id="3d16d-135">Norėdami įtraukti prekę iš turto KS, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3d16d-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="3d16d-136">Pasirinkite **Įtraukti KS prekių**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="3d16d-137">Pasirinkite prekę ir pagal poreikį redaguokite susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="3d16d-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="3d16d-138">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-138">Select **OK**.</span></span>

<span data-ttu-id="3d16d-139">Jei norite apžvelgti, kur naudojama prekė pasirinktoje eilutėje atsižvelgiant į turtą, priežiūros užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus turto valdyme, pasirinkite **Kur naudota prekė**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="3d16d-140">Daugiau informacijos apie šią apžvalgą žr. [Kur naudota prekė](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="3d16d-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="3d16d-141">Išlaidų prognozės įtraukimas į darbo užsakymą</span><span class="sxs-lookup"><span data-stu-id="3d16d-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="3d16d-142">Puslapyje **Darbo užsakymo priežiūros prognozė** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.</span><span class="sxs-lookup"><span data-stu-id="3d16d-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="3d16d-143">Norėdami sukurti eilutę, „FastTab” **Išlaidos** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="3d16d-144">Lauke **Kategorija** pasirinkite kategoriją.</span><span class="sxs-lookup"><span data-stu-id="3d16d-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="3d16d-145">Lauke **Kiekis** įveskite kiekį.</span><span class="sxs-lookup"><span data-stu-id="3d16d-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="3d16d-146">Laukuose **Savikaina**, **Pardavimo valiuta** ir **Pardavimo kaina** įveskite tinkamas vertes.</span><span class="sxs-lookup"><span data-stu-id="3d16d-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="3d16d-147">Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.</span><span class="sxs-lookup"><span data-stu-id="3d16d-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="3d16d-148">„FastTab” **Priežiūros prognozių sumos** rodoma pasirinktos darbo užsakymo užduoties ir darbo užsakymo kiekviename „FastTab” sukurtų eilučių skaičiaus apžvalga.</span><span class="sxs-lookup"><span data-stu-id="3d16d-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="3d16d-149">Taip pat rodoma darbo užsakymo užduoties ir darbo užsakymo prognozuojamų darbo valandų suma.</span><span class="sxs-lookup"><span data-stu-id="3d16d-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="3d16d-150">Toliau pateiktame paveikslėlyje parodytas puslapio **Darbo užsakymo priežiūros prognozė** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3d16d-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![1 pav.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="3d16d-152">Darbo užsakymo prognozių automatinis naujinimas</span><span class="sxs-lookup"><span data-stu-id="3d16d-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="3d16d-153">Turto valdyme galima automatiškai naujinti darbo užsakymų prognozių informaciją apie valandines išlaidas, prekių kainas ir išlaidas, jei ji buvo atnaujinta kituose „Microsoft Dynamics 365 for Finance and Operations“ moduliuose.</span><span class="sxs-lookup"><span data-stu-id="3d16d-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="3d16d-154">Ši galimybė padeda užtikrinti, kad darbo užsakymų prognozėse naudojamos aktualiausios savikainos.</span><span class="sxs-lookup"><span data-stu-id="3d16d-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="3d16d-155">Taip pat galima naujinti ir [priežiūros užduočių tipo prognozes](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="3d16d-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="3d16d-156">Pasirinkite **Turto valdymas** > **Periodinis** > **Prognozė** > **Naujinti darbo užsakymo prognozę**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="3d16d-157">Dialogo lange **Naujinti darbo užsakymo prognozę**, „FastTab” **Įtrauktini įrašai**, pagal poreikį galite pasirinkti parametrus, susijusius su konkrečiais darbo užsakymais arba darbo užsakymų užduotimis.</span><span class="sxs-lookup"><span data-stu-id="3d16d-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="3d16d-158">Norėdami atlikti reikiamus pasirinkimus, spustelėkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="3d16d-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="3d16d-159">FastTab **Vykdyti fone** pagal poreikį galite nustatyti automatinio naujinimo paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="3d16d-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="3d16d-160">Pasirinkus **Gerai**, pradedamas prognozės naujinimas.</span><span class="sxs-lookup"><span data-stu-id="3d16d-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="3d16d-161">Toliau pateiktame paveikslėlyje parodytas dialogo lango **Naujinti darbo užsakymo prognozę** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3d16d-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![2 pav.](media/07-work-orders.png)
