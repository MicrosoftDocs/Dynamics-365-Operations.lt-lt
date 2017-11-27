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
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd84dde353972d2d259706dd9f8f3621cef04472
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="59597-103">Prognozės tikslumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="59597-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="59597-104">Šiame straipsnyje aprašomi prognozės tikslumo, kurį apskaičiuoja „Microsoft Dynamics 365 for Finance and Operations“, tipai ir paaiškinama, kaip galima peržiūrėti tikslumo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="59597-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="59597-105">„Finance and Operations“ apskaičiuoja toliau nurodytų tipų prognozės tikslumą.</span><span class="sxs-lookup"><span data-stu-id="59597-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="59597-106">Praeities prognozės tikslumas, bendrajame planavime naudojamą praeities prognozę palyginant su praeities poreikiu.</span><span class="sxs-lookup"><span data-stu-id="59597-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="59597-107">Norėdami peržiūrėti praeities prognozės tikslumo reikšmes (absoliučiąsias ir procentines), puslapyje **Poreikio prognozės informacija** spustelėkite **Rodyti tikslumą**.</span><span class="sxs-lookup"><span data-stu-id="59597-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="59597-108">Įvertintas prognozės modelio, naudojamo prognozėms generuoti, tikslumas.</span><span class="sxs-lookup"><span data-stu-id="59597-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="59597-109">Tikslumo procentą galite peržiūrėti puslapio **Poreikio prognozės informacija** dalyje **Modelio informacija – MAPE**.</span><span class="sxs-lookup"><span data-stu-id="59597-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="59597-110">**Pastaba:** jei naudojate „Finance and Operations“ poreikio prognozės „Microsoft Azure“ mašininio mokymo tarnybą, vidaus modelio tikslumo skaičiavimas yra pagrįstas bandymo duomenų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="59597-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="59597-111">Norėdami nurodyti bandymo duomenų rinkinio dydį, puslapyje **Poreikio prognozės parametrai** nustatykite parametrą **TEST\_SET\_SIZE\_PERCENT**.</span><span class="sxs-lookup"><span data-stu-id="59597-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="59597-112">Pavyzdžiui, jei nustatysite reikšmę **20**, vidaus modelio tikslumui apskaičiuoti bus naudojami paskutiniai 20 procentų praeities duomenų.</span><span class="sxs-lookup"><span data-stu-id="59597-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="59597-113">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="59597-113">See also</span></span>
--------

[<span data-ttu-id="59597-114">Pakoreguotos poreikio prognozės įgaliojimas</span><span class="sxs-lookup"><span data-stu-id="59597-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="59597-115">Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes</span><span class="sxs-lookup"><span data-stu-id="59597-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




