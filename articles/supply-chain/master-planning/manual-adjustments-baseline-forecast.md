---
title: "Neautomatiniai pagrindinės prognozės koregavimai"
description: "Šiame straipsnyje paaiškinama, kaip galima neautomatiškai koreguoti pagrindinę prognozę ir peržiūrėti prognozės informaciją."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 218374cdb6b5588648422d97c04fb60f26e47ac7
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="1dd7f-103">Neautomatiniai pagrindinės prognozės koregavimai</span><span class="sxs-lookup"><span data-stu-id="1dd7f-103">Make manual adjustments to the baseline forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1dd7f-104">Šiame straipsnyje paaiškinama, kaip galima neautomatiškai koreguoti pagrindinę prognozę ir peržiūrėti prognozės informaciją.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-104">This article explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="1dd7f-105">Svarbu, kad prieš atlikdami neautomatinius koregavimus suprastumėte kelias įvairių puslapių sąvokas.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="1dd7f-106">Tinklelis puslapyje Pakoreguota poreikio prognozė</span><span class="sxs-lookup"><span data-stu-id="1dd7f-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="1dd7f-107">Puslapyje **Pakoreguota poreikio prognozė** yra tinklelis, kurio struktūra nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="1dd7f-108">Pirmajame stulpelyje rodoma, kam prognozė generuojama: prekių paskirstymo raktams, prekėms, įmonėms ir t.t..</span><span class="sxs-lookup"><span data-stu-id="1dd7f-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="1dd7f-109">Puslapio paantraštėje pateikiamas dabartinių prognozės dimensijų, rodomų tinklelyje, aprašymas.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="1dd7f-110">Pavyzdžiui, jei puslapio paantraštė yra **Įmonė / Teritorija / Prekių paskirstymo raktas**, o viena iš tinklelio eilučių antraščių yra **USMF / 1 / D\_Alloc**, toje eilutėje rodoma prognozė, skirta USMF įmonei, 1 teritorijai ir prekių paskirstymo raktui **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="1dd7f-111">Kiti stulpeliai atspindi prognozės rinkinius, kuriems prognozė generuojama.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="1dd7f-112">Kiekviena stulpelio antraštė yra pirmoji stulpelyje rodomo prognozės rinkinio data.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="1dd7f-113">Langelių reikšmės nurodo to konkretaus prognozės rinkinio prognozę vienai prekei, prekių paskirstymo raktui ir t.t.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-deaggregation"></a><span data-ttu-id="1dd7f-114">Prognozės telkimas ir telkimo panaikinimas</span><span class="sxs-lookup"><span data-stu-id="1dd7f-114">Forecast aggregation and deaggregation</span></span>
<span data-ttu-id="1dd7f-115">Puslapio paantraštė nurodo prognozės telkimo lygį.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="1dd7f-116">Pavyzdžiui, jei puslapio paantraštė yra **Įmonė / Teritorija / Paskirstymo raktas / Prekės numeris / Spalva / Dydis / Konfigūracija / Stilius**, prognozės telkimo nėra ir prognozė rodoma prekės bei jos dimensijų lygyje.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="1dd7f-117">Norėdami keisti telkimą naudokite puslapį **Keisti prognozės dimensijas**, kurį galite atidaryti iš programų meniu.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="1dd7f-118">Norėdami modifikuoti prognozę, spustelėkite bet kurį galimą langelį ir įveskite pakoreguotą prognozės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="1dd7f-119">Pakeistas langelio reikšmė yra iš karto paryškinama siekiant nurodyti, kad rodoma prognozė nėra poreikio prognozės tarnybos sukurta prognozė, bet yra neautomatiškai pakoreguota.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="1dd7f-120">Pakeitus telkimą, kad puslapyje būtų rodoma daugiau apibendrintų duomenų, galima naudoti puslapį **Poreikio prognozės eilutės**, norint pamatyti atskiras prognozės eilutes, kurios sudaro agreguotą prognozę.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="1dd7f-121">Pvz., sugeneravote prognozę prekės lygiu, bet jūs žinote, kad dėl reklamos kampanijos arba kito panašaus įvykio šios prekės poreikis padidės visose teritorijose.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="1dd7f-122">Tokiu atveju puslapyje **Keisti prognozės dimensijas** galite telkimą nustatyti kaip **Įmonė / Prekių paskirstymo raktas / Prekė**.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="1dd7f-123">Tinklelyje **Pakoreguota poreikio prognozė** galite koreguoti visuotinę prekės prognozę visose teritorijose.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="1dd7f-124">Norėdami pamatyti keitimų visose teritorijose poveikį, atidarykite puslapį **Poreikio prognozės eilutės**.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="1dd7f-125">Šiame puslapyje matysite vieną prekės eilutę, skirtą kiekvienai teritorijai, pakoreguotam prognozės kiekiui ir pradiniam prognozės kiekiui.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="1dd7f-126">Atliekant prognozės kiekio koregavimą sudėtiniu lygiu, sistema naudoja svertinį paskirstymą koregavimams eilutėse, kurios kuria telkimą, proporcingai paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="1dd7f-127">Neautomatinius koregavimus taip pat galima atlikti puslapyje **Poreikio prognozės eilutės**, pakeičiant lauko **Bendras kiekis** reikšmę arba telkimo panaikinimo tinklelio dalies **Kiekis** langelius.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="1dd7f-128">Prognozės informacijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="1dd7f-128">Viewing details of the forecast</span></span>
<span data-ttu-id="1dd7f-129">Galite atidaryti puslapį **Poreikio prognozės informacija** ir peržiūrėti daugiau informacijos apie prognozę.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="1dd7f-130">Puslapyje **Poreikio prognozės informacija** toliau nurodyta informacija pateikiama lentelių ir grafiniu formatais.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="1dd7f-131">Praeities poreikis, kuriuo prognozė pagrįsta.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="1dd7f-132">Dabartinė prognozė, naudojama bendrajame planavime.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="1dd7f-133">Naujos poreikio prognozės reikšmės ir jų neautomatiškai pakoreguotos sumos.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="1dd7f-134">Prognozės reikšmių patikimumo intervalas.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="1dd7f-135">Prognozės modelis, kuris buvo naudojamas generuojant prognozę.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="1dd7f-136">Jei peržiūrite apibendrintus duomenis, matysite visų metodų, naudotų per visas telkimo serijas, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="1dd7f-137">Vidaus modelio tikslumas (MAPE).</span><span class="sxs-lookup"><span data-stu-id="1dd7f-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="1dd7f-138">Daugiau informacijos apie prognozės tikslumą žr. [Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="1dd7f-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="1dd7f-139">**Pastabos**</span><span class="sxs-lookup"><span data-stu-id="1dd7f-139">**Notes:**</span></span>

-   <span data-ttu-id="1dd7f-140">Patikimumo intervalas, kuris rodomas puslapio dalyje **Prognozė**, nurodo skirtumą tarp viršutinės ir apatinės patikimumo intervalo ribų.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="1dd7f-141">Norėdami peržiūrėti apatinės ir viršutinės ribų reikšmes, nuveskite žymeklį virš diagramos dalyje **Praeities poreikis ir prognozė grafiškai**.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="1dd7f-142">Jei naudojate „Finance and Operations“ poreikio prognozės „Microsoft Azure“ mašininio mokymo tarnybą, galite nurodyti generuojamos prognozės patikimumo lygio procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="1dd7f-143">Patikimumo intervalą sudaro reikšmės, kurios nurodo tinkamus poreikio prognozės įvertinimus.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="1dd7f-144">95 procentų patikimumo lygio procentas nurodo 5 % tikimybę, kad prognozės rezultatas nepateks į patikimumo intervalo diapazoną.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="1dd7f-145">Taip pat galite atlikti neautomatinius prognozės koregavimus puslapyje **Poreikio prognozės informacija**, pakeisdami reikšmes eilutėje **Prognozė**, kuri yra dalyje **Prognozė**.</span><span class="sxs-lookup"><span data-stu-id="1dd7f-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="see-also"></a><span data-ttu-id="1dd7f-146">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="1dd7f-146">See also</span></span>
--------

[<span data-ttu-id="1dd7f-147">Prognozės tikslumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="1dd7f-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="1dd7f-148">Pagrindinės statistinės prognozės generavimas</span><span class="sxs-lookup"><span data-stu-id="1dd7f-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



