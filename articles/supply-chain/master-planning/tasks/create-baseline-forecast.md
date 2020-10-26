---
title: Kurti pagrindinę prognozę
description: Gamybos planuotojas gali sukurti pagrindinę prognozę naudodamas laiko serijos prognozės modelius arba nukopijuodamas praeities poreikį.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a1d8fd665ec40efede0a3db8b0c59ac89751a64
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987195"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="ca6d7-103">Kurti pagrindinę prognozę</span><span class="sxs-lookup"><span data-stu-id="ca6d7-103">Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca6d7-104">Gamybos planuotojas gali sukurti pagrindinę prognozę naudodamas laiko serijos prognozės modelius arba nukopijuodamas praeities poreikį.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="ca6d7-105">Šioje procedūroje parodoma, kaip sukurti pagrindinę visų produktų prognozę, naudojant vieną prekių paskirstymo raktą nukopijavus praeities poreikį.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="ca6d7-106">Prekių paskirstymo rakto nustatymas</span><span class="sxs-lookup"><span data-stu-id="ca6d7-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="ca6d7-107">Pasirinkite Bendrasis planavimas > Nustatymas > Bendros įmonių planavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="ca6d7-108">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ca6d7-109">Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="ca6d7-110">Poreikio prognozė vykdoma per visus juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="ca6d7-111">Todėl jums reikės visas įmones, kurioms norite generuoti prognozes, įtraukti į vieną bendrą įmonių planavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="ca6d7-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ca6d7-113">Spustelėkite „Prekių paskirstymo raktai“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="ca6d7-114">Pasirinkite visus prekių paskirstymo raktus, kuriems norite kurti prognozes.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="ca6d7-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ca6d7-116">Pasirinkite D_Aloc prekių paskirstymo raktą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="ca6d7-117">Spustelėti >.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-117">Click >.</span></span>
7. <span data-ttu-id="ca6d7-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-118">Close the page.</span></span>
8. <span data-ttu-id="ca6d7-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="ca6d7-120">Nustatyti poreikio prognozės parametrus</span><span class="sxs-lookup"><span data-stu-id="ca6d7-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="ca6d7-121">Pasirinkite Bendrasis planavimas > Nustatymas > Poreikio prognozė > Poreikio prognozės parametrai.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="ca6d7-122">Išplėskite skirtuką Prognozės algoritmo parametrai.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="ca6d7-123">Lauke „Prognozės generavimo strategija“ pasirinkite „Kopijuoti praeities poreikį".</span><span class="sxs-lookup"><span data-stu-id="ca6d7-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="ca6d7-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="ca6d7-125">Kurti pagrindinę prognozę</span><span class="sxs-lookup"><span data-stu-id="ca6d7-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="ca6d7-126">Pasirinkite Bendrasis planavimas > Prognozė > Poreikio prognozė > Generuoti pagrindinę statistinę prognozę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="ca6d7-127">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="ca6d7-128">Jei turite pardavimo užsakymų, prasidedančių 2015 m. sausio 1 d., įveskite šią datą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="ca6d7-129">Jei neturite, įveskite anksčiausią pardavimo užsakymų datą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="ca6d7-130">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="ca6d7-131">Įveskite paskutinę savo pardavimo užsakymų datą, pavyzdžiui, „2015-03-31‟.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="ca6d7-132">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="ca6d7-133">Įveskite „2015-04-01‟.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="ca6d7-134">Ši data bus automatiškai skaičiuojama kaip kito prognozės segmento pradžios data.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="ca6d7-135">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="ca6d7-136">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-136">Click Filter.</span></span>
7. <span data-ttu-id="ca6d7-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ca6d7-138">Pažymėkite eilutę, kur laukas = bendra įmonių planavimo grupė.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="ca6d7-139">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="ca6d7-140">Įveskite bendrą įmonių planavimo grupę, pvz., 10, kurią naudojote pirmojoje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="ca6d7-141">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ca6d7-142">Pasirinkite eilutę, kur laukas = prekių paskirstymo raktas.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="ca6d7-143">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="ca6d7-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-144">Click OK.</span></span>
12. <span data-ttu-id="ca6d7-145">Išplėskite skyrių „Išplėstiniai parametrai“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="ca6d7-146">Lauke „Prognozės segmentas“ pasirinkite „Mėnesis“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="ca6d7-147">Lauke „Prognozės laikotarpis“ įveskite „3“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="ca6d7-148">Lauke „Blokavimo laiko ribos“ įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="ca6d7-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="ca6d7-150">Vizualizuoti poreikio prognozę</span><span class="sxs-lookup"><span data-stu-id="ca6d7-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="ca6d7-151">Pasirinkite Bendrasis planavimas > Prognozė > Poreikio prognozė > Pakoreguota poreikio prognozė.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="ca6d7-152">Bendrojo rodinio lentelėje pasirinkite 1 eilutėje 2 stulpelyje esantį langelį.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="ca6d7-153">Tai – antras mėnuo, kuriam sukūrėte prognozę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="ca6d7-154">Nustatykite „QtyCell“ reikšmę „400“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="ca6d7-155">Langelyje įveskite kitą numerį nei buvo prognozuotas, pvz., 400.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="ca6d7-156">Pakoregavote prognozę rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="ca6d7-157">Atlikdami kitą veiksmą atkreipkite dėmesį į grafinę indikaciją.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="ca6d7-158">Spustelėkite „Prognozės eilutės informacija“.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="ca6d7-159">Šiame puslapyje galite matyti tikslumo reikšmes, praeities poreikį ir prognozę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="ca6d7-160">Taip pat galite keisti ir prognozę.</span><span class="sxs-lookup"><span data-stu-id="ca6d7-160">You can make changes to the forecast as well.</span></span>  

