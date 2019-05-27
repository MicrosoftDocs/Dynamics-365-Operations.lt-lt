---
title: Įvertinti gamybos užsakymą
description: Šią procedūrą galite paleisti naudodami USMF demonstracinių duomenų įmonę arba savo duomenų rinkinį.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8274e390a177f51649f5cad70ef7ad5bd50a8830
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558485"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="092c7-103">Įvertinti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="092c7-103">Estimate a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="092c7-104">Šią procedūrą galite paleisti naudodami USMF demonstracinių duomenų įmonę arba savo duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="092c7-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="092c7-105">Abiem atvejais turite turėti atvirą gamybos užsakymą, kurio būsena yra Sukurta.</span><span class="sxs-lookup"><span data-stu-id="092c7-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="092c7-106">Tai yra antra procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.</span><span class="sxs-lookup"><span data-stu-id="092c7-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="092c7-107">Įvertinti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="092c7-107">Estimate a production order</span></span>
1. <span data-ttu-id="092c7-108">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="092c7-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="092c7-109">Pasirinkite užsakymą, kurio tinklelyje yra būsena Sukurta.</span><span class="sxs-lookup"><span data-stu-id="092c7-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="092c7-110">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="092c7-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="092c7-111">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="092c7-111">Click Estimate.</span></span>
    * <span data-ttu-id="092c7-112">Šiame etape skaičiuojama vieno gamybos užsakymo įvertinta savikaina.</span><span class="sxs-lookup"><span data-stu-id="092c7-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="092c7-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="092c7-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="092c7-114">Skaičiavimo informacijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="092c7-114">View the calculation details</span></span>
1. <span data-ttu-id="092c7-115">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="092c7-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="092c7-116">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="092c7-116">Click View calculation details.</span></span>
    * <span data-ttu-id="092c7-117">Šiame puslapyje rodomas išlaidų paskirstymas.</span><span class="sxs-lookup"><span data-stu-id="092c7-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="092c7-118">Pavyzdžiui, pirmoje eilutėje galite peržiūrėti baigto produkto vieneto bendrąją savikainą.</span><span class="sxs-lookup"><span data-stu-id="092c7-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="092c7-119">Kitose eilutėse pateikiamos išlaidos pagal komplektavimo specifikaciją, gamybos maršrutą ir netiesiogines išlaidas.</span><span class="sxs-lookup"><span data-stu-id="092c7-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
