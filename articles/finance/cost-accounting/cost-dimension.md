---
title: Dimensijų kūrimas ir dimensijų narių importavimas
description: Kaštų apskaita yra nepriklausomas modulis, kurį norint naudoti reikalingi bendrieji duomenys iš kitų modulių.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a7db93e1877034051b6add4c11ddfe7cd7d17e0b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187917"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="15382-103">Dimensijų kūrimas ir dimensijų narių importavimas</span><span class="sxs-lookup"><span data-stu-id="15382-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15382-104">Kaštų apskaita yra nepriklausomas modulis, kurį norint naudoti reikalingi duomenys iš kitų modulių.</span><span class="sxs-lookup"><span data-stu-id="15382-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="15382-105">Šie duomenys yra suskirstyti į tolesnes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="15382-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="15382-106">Savikainos elementai</span><span class="sxs-lookup"><span data-stu-id="15382-106">Cost elements</span></span>
-  <span data-ttu-id="15382-107">Savikainos objektai</span><span class="sxs-lookup"><span data-stu-id="15382-107">Cost objects</span></span>
-  <span data-ttu-id="15382-108">Statistinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="15382-108">Statistical dimensions</span></span>

<span data-ttu-id="15382-109">**Savikainos elementas** sąskaitų plane atitinka su savikaina susijusį elementą.</span><span class="sxs-lookup"><span data-stu-id="15382-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="15382-110">**Savikainos objektas** atitinka bet kokio tipo finansinę dimensiją, pvz., produktus, išlaidų centrus ir projektus, kuriuos norite įvertinti, kuriems norite priskirti išlaidas ar kuriuos norite tiesiogiai matuoti.</span><span class="sxs-lookup"><span data-stu-id="15382-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="15382-111">Naudojant **statistinę dimensiją** ir jos narius, registruojami nepiniginiai įrašai.</span><span class="sxs-lookup"><span data-stu-id="15382-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="15382-112">Statistinių dimensijų narius galima naudoti kaip išlaidų paskirstymo ir priskyrimo paskirstymo pagrindą</span><span class="sxs-lookup"><span data-stu-id="15382-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="15382-113">Toliau pateiktoje diagramoje pavaizduotos modulyje Kaštų apskaita naudojamos dimensijos.</span><span class="sxs-lookup"><span data-stu-id="15382-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="15382-114">[![Savikainos apskaitos dimensijos](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="15382-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="15382-115">Į modulį Kaštų apskaita importavus duomenų, jį naudojant galima sukurti įvairių perspektyvų, vadovams suteikiančių įžvalgų visuose organizacijos lygiuose.</span><span class="sxs-lookup"><span data-stu-id="15382-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="15382-116">Tolesnėse temose pateikta informacijos apie dimensijų kūrimą ir dimensijų narių importavimą.</span><span class="sxs-lookup"><span data-stu-id="15382-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="15382-117">Savikainos elemento dimensijos</span><span class="sxs-lookup"><span data-stu-id="15382-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="15382-118">Savikainos elementų kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="15382-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="15382-119">Savikainos objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="15382-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="15382-120">Savikainos elementų kūrimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="15382-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="15382-121">Savikainos elemento dimensijos narių susiejimas į bendrą dimensijos narių rinkinį</span><span class="sxs-lookup"><span data-stu-id="15382-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="15382-122">Savikainos elemento dimensijos susiejimas (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="15382-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="15382-123">Statistinių dimensijų nariai ir statistinių priemonių teikimo įrankio šablonai</span><span class="sxs-lookup"><span data-stu-id="15382-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






