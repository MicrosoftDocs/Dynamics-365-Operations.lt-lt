---
title: Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį
description: Šioje temoje aprašomas baigtų produktų užbaigimo gamybos užsakyme procesas į atsargas, kai vieta valdoma pagal numerio lentelę.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995147"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="48ac8-103">Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį</span><span class="sxs-lookup"><span data-stu-id="48ac8-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="48ac8-104">Procesas, vadinamas Paskelbimu, kad baigta, gamybos užsakyme baigia baigtus produktus į atsargas.</span><span class="sxs-lookup"><span data-stu-id="48ac8-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="48ac8-105">Jei baigtas produktas yra įgalintas taikant pažangius sandėlio procesus, produktas paskelbiamas baigtu į vietą, vadinamą gamybos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="48ac8-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="48ac8-106">Norėdami gauti informacijos apie gamybos išeigos vietos nustatymą, žr. [Gamybos išeigos vieta](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="48ac8-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="48ac8-107">Norėdami atlikti šią užduotį, turite pasirinkti esamą numerio lentelės numerį.</span><span class="sxs-lookup"><span data-stu-id="48ac8-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="48ac8-108">Jei nustatyta, kad gamybos išeigos vieta būtų sekama pagal numerio lentelę, tuomet, kai gamybos išeigos vieta paskelbiama baigta, turi būti įtrauktas numerio lentelės numeris.</span><span class="sxs-lookup"><span data-stu-id="48ac8-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="48ac8-109">Laukas **Numerio lentelė** matomas raginime **Pranešti apie eigą** puslapyje **Užduoties kortelės įrenginys**.</span><span class="sxs-lookup"><span data-stu-id="48ac8-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="48ac8-110">Šis laukas matomas tik raginime **Pranešti apie eigą**, kai pranešama apie paskutinę gamybos užsakymo operaciją.</span><span class="sxs-lookup"><span data-stu-id="48ac8-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="48ac8-111">Laukas rodomas tik tuo atveju, jei sandėlio valdymo procesuose yra įjungtas gamybos užsakymo elementas.</span><span class="sxs-lookup"><span data-stu-id="48ac8-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
