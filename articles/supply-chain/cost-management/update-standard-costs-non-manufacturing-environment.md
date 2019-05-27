---
title: Standartinių išlaidų atnaujinimas ne gamybos aplinkoje
description: Šiame straipsnyje patariama, kaip standartines išlaidas atnaujinti ne gamybos aplinkoje.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4fa545aa6903bd6f789dda20ab5755ffe9a12b88
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565675"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="a1d4d-103">Standartinių išlaidų atnaujinimas ne gamybos aplinkoje</span><span class="sxs-lookup"><span data-stu-id="a1d4d-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1d4d-104">Šiame straipsnyje patariama, kaip standartines išlaidas atnaujinti ne gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="a1d4d-105">Šios rekomendacijos taikomos, jei naudojate dviejų versijų standartinių išlaidų naujinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="a1d4d-106">Naudojant šį būdą, viena įkainojimo versija turi iš pradžių nustatytas standartines įšaldyto laikotarpio išlaidas, o antra įkainojimo versija turi papildančiuosius naujinimus.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="a1d4d-107">Kiekvienas naujinimas įvedamas kaip išlaidų įrašas antroje įkainojimo versijoje ir galiausiai jis suaktyvinamas.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="a1d4d-108">Alternatyvus būdas yra vienos versijos įkainojimas, naudojant iš pradžių apibrėžtų standartinių išlaidų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="a1d4d-109">Dviejų versijų būdui reikalingas antros įkainojimo versijos apibrėžimas.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="a1d4d-110">Toliau pateikti patarimai, kaip apibrėžti šią įkainojimo versiją.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="a1d4d-111">Priskirkite įkainojimo tipą **Standartinės išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="a1d4d-112">Priskirkite reikšmingą identifikatorių, kuris nurodo įkainojimo versijos turinį, pvz., **2016-NAUJINIMAI**.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="a1d4d-113">Įsitikinkite, kad turinyje yra išlaidų įrašai.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="a1d4d-114">Leiskite įvesti visų vietų išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="a1d4d-115">Jei nurodote vietą, galima įvesti tik tos vietos išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="a1d4d-116">Nurodykite atsarginį principą **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="a1d4d-117">Atsarginis principas taikomas tik pagamintų prekių išlaidų skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="a1d4d-118">Norėdami patikslinti, pakoreguoti arba atnaujinti standartines naujų prekių išlaidas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="a1d4d-119">Naudodami puslapį **Įkainojimo versijos** **nustatymas**, galite išlaidų duomenis leisti įvesti į antrą įkainojimo versiją.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="a1d4d-120">Nebūtina: neleiskite suaktyvinti laukiančių išlaidų, kad suaktyvinti būtų leista tik išsamiai ir tiksliai apibrėžus laukiančias išlaidas.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="a1d4d-121">Nebūtina: taip pat galite įvesti datą lauke **Pradžios data**.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="a1d4d-122">Bendra gairė – datą naudoti ketinant įgalinti papildančiuosius naujinimus.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="a1d4d-123">Taip pat įkainojimo versijos lauką **Pradžios data** galite palikti tuščią, o datą įvesti kiekvieno išlaidų įrašo lauke **Pradžios data**.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="a1d4d-124">Naudodami puslapį **Prekės kaina**, naujinimus galite įvesti kaip prekių išlaidų įrašus antrojoje įkainojimo versijoje.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="a1d4d-125">Naudodami ataskaitą **Prekių kainos** galite tikrinti prekių išlaidų įrašų antrojoje įkainojimo versijoje užbaigtumą ir tikslumą.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="a1d4d-126">Naudodami puslapį **Įkainojimo versijos tvarkymas**, galite pakeisti blokavimo vėliavėlę, kad leistumėte aktyvinti laukiančius išlaidų įrašus antrojoje įkainojimo versijoje.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="a1d4d-127">Naudodami puslapį **Aktyvinti kainas** (kurį galite atidaryti iš puslapio **Įkainojimo versijos tvarkymas**), galite aktyvinti laukiančius išlaidų įrašus antrojoje įkainojimo versijoje.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="a1d4d-128">Aktyvinti atskirų prekių laukiančių išlaidų įrašus taip pat galite puslapyje **Prekės kaina** spustelėdami mygtuką **Aktyvinti laukiančią kainą**.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="a1d4d-129">Kad nereikėtų papildomai tvarkyti duomenų, naudokite puslapį **Įkainojimo versijos nustatymas**, kad pakeistumėte blokavimo vėliavėles antrojoje įkainojimo versijoje.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="a1d4d-130">Blokavimo strategija apsaugos nuo naujų laukiančių išlaidų įvedimo ir laukiančių išlaidų aktyvinimo.</span><span class="sxs-lookup"><span data-stu-id="a1d4d-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>




