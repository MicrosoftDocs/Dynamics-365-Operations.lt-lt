---
title: "Prognozės tikslumo stebėjimas"
description: "Šiame straipsnyje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 for Finance and Operations“, tipai ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2f9482a9906ad6c607d275769ac06b29b22c25d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="33b51-103">Prognozės tikslumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="33b51-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="33b51-104">Šiame straipsnyje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 for Finance and Operations“, tipai ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="33b51-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="33b51-105">„Finance and Operations“ apskaičiuoja toliau nurodytų tipų prognozės tikslumą.</span><span class="sxs-lookup"><span data-stu-id="33b51-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="33b51-106">Praeities prognozės tikslumas, bendrajame planavime naudojamą praeities prognozę palyginant su praeities poreikiu.</span><span class="sxs-lookup"><span data-stu-id="33b51-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="33b51-107">Norėdami peržiūrėti praeities prognozės tikslumo reikšmes (absoliučiąsias ir procentines), puslapyje **Poreikio prognozės informacija** spustelėkite **Rodyti tikslumą**.</span><span class="sxs-lookup"><span data-stu-id="33b51-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="33b51-108">Įvertintas prognozės modelio, naudojamo prognozėms generuoti, tikslumas.</span><span class="sxs-lookup"><span data-stu-id="33b51-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="33b51-109">Tikslumo procentą galite peržiūrėti puslapio **Poreikio prognozės informacija** dalyje **Modelio informacija – MAPE**.</span><span class="sxs-lookup"><span data-stu-id="33b51-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="33b51-110">**Pastaba:** jei naudojate „Finance and Operations“ poreikio prognozės „Microsoft Azure“ mašininio mokymo tarnybą, vidaus modelio tikslumo skaičiavimas yra pagrįstas bandymo duomenų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="33b51-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="33b51-111">Norėdami nurodyti bandymo duomenų rinkinio dydį, puslapyje **Poreikio prognozės parametrai** nustatykite parametrą **TEST\_SET\_SIZE\_PERCENT**.</span><span class="sxs-lookup"><span data-stu-id="33b51-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="33b51-112">Pavyzdžiui, jei nustatysite reikšmę **20**, vidaus modelio tikslumui apskaičiuoti bus naudojami paskutiniai 20 procentų praeities duomenų.</span><span class="sxs-lookup"><span data-stu-id="33b51-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="33b51-113">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="33b51-113">See also</span></span>
--------

[<span data-ttu-id="33b51-114">Pakoreguotos poreikio prognozės įgaliojimas</span><span class="sxs-lookup"><span data-stu-id="33b51-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="33b51-115">Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes</span><span class="sxs-lookup"><span data-stu-id="33b51-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




