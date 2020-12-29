---
title: Prognozės tikslumo stebėjimas
description: Šioje temoje aprašomi prognozės tikslumo, kurį apskaičiuoja „Dynamics 365 Supply Chain Management“, tipai, ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60e5425e54f9e0093888f355a51064e7f0057976
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433822"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="67137-103">Prognozės tikslumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="67137-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67137-104">Šioje temoje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 Supply Chain Management“, tipai, ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="67137-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="67137-105">„Supply Chain Management“ apskaičiuoja toliau nurodytų tipų prognozės tikslumą.</span><span class="sxs-lookup"><span data-stu-id="67137-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="67137-106">Praeities prognozės tikslumas, bendrajame planavime naudojamą praeities prognozę palyginant su praeities poreikiu.</span><span class="sxs-lookup"><span data-stu-id="67137-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="67137-107">Norėdami peržiūrėti praeities prognozės tikslumo reikšmes (absoliučiąsias ir procentines), puslapyje **Poreikio prognozės informacija** spustelėkite **Rodyti tikslumą**.</span><span class="sxs-lookup"><span data-stu-id="67137-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="67137-108">Įvertintas prognozės modelio, naudojamo prognozėms generuoti, tikslumas.</span><span class="sxs-lookup"><span data-stu-id="67137-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="67137-109">Tikslumo procentą galite peržiūrėti puslapio **Poreikio prognozės informacija** dalyje **Modelio informacija – MAPE**.</span><span class="sxs-lookup"><span data-stu-id="67137-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="67137-110">Jei naudojate poreikio prognozės „Microsoft Azure“ mašininį mokymą, vidaus modelio tikslumo skaičiavimas yra pagrįstas bandymo duomenų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="67137-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="67137-111">Norėdami nurodyti bandymo duomenų rinkinio dydį, puslapyje **Poreikio prognozės parametrai** nustatykite parametrą **TEST\_SET\_SIZE\_PERCENT**.</span><span class="sxs-lookup"><span data-stu-id="67137-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="67137-112">Pavyzdžiui, jei nustatysite reikšmę **20**, vidaus modelio tikslumui apskaičiuoti bus naudojami paskutiniai 20 procentų praeities duomenų.</span><span class="sxs-lookup"><span data-stu-id="67137-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="67137-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="67137-113">Additional resources</span></span>
--------

[<span data-ttu-id="67137-114">Pakoreguotos prognozės įgaliojimas</span><span class="sxs-lookup"><span data-stu-id="67137-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="67137-115">Pašalinių reikšmių šalinimas iš praeities operacijų duomenų skaičiuojant poreikio prognozę</span><span class="sxs-lookup"><span data-stu-id="67137-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



