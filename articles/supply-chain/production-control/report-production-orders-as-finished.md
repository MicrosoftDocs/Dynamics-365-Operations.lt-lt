---
title: Pranešti, kad gamybos užsakymai įvykdyti
description: Pranešti, kad baigta yra gamybos etapas. Šiame etape pranešama apie pabaigtą produktą ir jis perkeliamas iš gamybos užsakymo į atsargas.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61c12ee3a831abcb46af18645eba55fe100c99c9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "315825"
---
# <a name="report-production-orders-as-finished"></a><span data-ttu-id="0c92c-104">Pranešti, kad gamybos užsakymai įvykdyti</span><span class="sxs-lookup"><span data-stu-id="0c92c-104">Report production orders as finished</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c92c-105">Pranešti, kad baigta yra gamybos etapas.</span><span class="sxs-lookup"><span data-stu-id="0c92c-105">Report as finished is a production stage.</span></span> <span data-ttu-id="0c92c-106">Šiame etape pranešama apie pabaigtą produktą ir jis perkeliamas iš gamybos užsakymo į atsargas.</span><span class="sxs-lookup"><span data-stu-id="0c92c-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="0c92c-107">Kai gamybos užsakymas paskelbiamas baigtu, pagamintų prekių kiekis atsargose yra atnaujinamas kaip turimas.</span><span class="sxs-lookup"><span data-stu-id="0c92c-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="0c92c-108">Dalinius suplanuoto užsakymo kiekio kiekius galima paskelbti baigtais.</span><span class="sxs-lookup"><span data-stu-id="0c92c-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="0c92c-109">Skelbiant kiekius baigtais taip pat galima apie klaidingus kiekius teikti ataskaitas su susieta klaidos priežastimi.</span><span class="sxs-lookup"><span data-stu-id="0c92c-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="0c92c-110">Kai gamybos užsakymas tampa Paskelbtas baigtu, tai reiškia, kad daugiau apie gamybos užsakymo kiekį ataskaitos nebebus teikiamos.</span><span class="sxs-lookup"><span data-stu-id="0c92c-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="0c92c-111">Toliau pateiktos charakteristikos taip pat yra susietos su procesu **Skelbti baigtu**.</span><span class="sxs-lookup"><span data-stu-id="0c92c-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="0c92c-112">Galima nustatyti žaliavų ir laiko, proporcingų paskelbtam kiekiui (atgalinis suvartojimas), suvartojimą</span><span class="sxs-lookup"><span data-stu-id="0c92c-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="0c92c-113">Galima generuoti prekių, kurias galima naudoti sandėlio procesuose, atidėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="0c92c-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="0c92c-114">Galima nustatyti, kad DK sąskaitoms būtų teikiamos ataskaitos apie pagamintų prekių planuojamų arba standartinių išlaidų vertę.</span><span class="sxs-lookup"><span data-stu-id="0c92c-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="0c92c-115">Paskelbto kiekio kokybės užsakymą galima sukurti pagal kokybės susiejimo sąranką.</span><span class="sxs-lookup"><span data-stu-id="0c92c-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="0c92c-116">Kiekis skelbiamas išeigos vietoje.</span><span class="sxs-lookup"><span data-stu-id="0c92c-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="0c92c-117">Tada sugeneruojamas sandėlio darbas kiekiui iš išeigos vietos į paskirties vietą, nustatytą atidėjimo darbo vietos nurodymu, perkelti.</span><span class="sxs-lookup"><span data-stu-id="0c92c-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="0c92c-118">Galima sukurti kokybės užsakymą, kai gamybos užsakymas yra paskelbtas baigtu, jei buvo nustatytas kokybės susiejimas.</span><span class="sxs-lookup"><span data-stu-id="0c92c-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="0c92c-119">Gamybos užsakymo nustatymas kaip paskelbto baigtu</span><span class="sxs-lookup"><span data-stu-id="0c92c-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="0c92c-120">Gamybos užsakymas gali būti nustatytas kaip **Skelbti baigtu** naudojant standartinę gamybos užsakymo atnaujinimo funkciją, technologinės ir užduoties kortelių žurnalus arba gamybos žurnalą **Skelbti baigtu**.</span><span class="sxs-lookup"><span data-stu-id="0c92c-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="0c92c-121">Taip pat galina atnaujinti etapą į **Skelbti baigtu** naudojant užduoties kortelės terminalo ir užduoties kortelės įrenginio puslapius, kai paskelbiate paskutinę gamybos užsakymo užduotį.</span><span class="sxs-lookup"><span data-stu-id="0c92c-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="0c92c-122">Galiausiai galite aktyvinti parinktį **Skelbti baigtu** kaip sandėlio kišeninio įrenginio sprendimo procesą.</span><span class="sxs-lookup"><span data-stu-id="0c92c-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  



