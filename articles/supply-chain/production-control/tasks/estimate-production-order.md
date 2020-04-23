---
title: Įvertinti gamybos užsakymą
description: Šią procedūrą galite paleisti naudodami USMF demonstracinių duomenų įmonę arba savo duomenų rinkinį.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bbb541a09809c1f1bfada42094d840a2f6e7764
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207053"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="d7389-103">Įvertinti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="d7389-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7389-104">Šią procedūrą galite paleisti naudodami USMF demonstracinių duomenų įmonę arba savo duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="d7389-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="d7389-105">Abiem atvejais turite turėti atvirą gamybos užsakymą, kurio būsena yra Sukurta.</span><span class="sxs-lookup"><span data-stu-id="d7389-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="d7389-106">Tai yra antra procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.</span><span class="sxs-lookup"><span data-stu-id="d7389-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="d7389-107">Įvertinti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="d7389-107">Estimate a production order</span></span>
1. <span data-ttu-id="d7389-108">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="d7389-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="d7389-109">Pasirinkite užsakymą, kurio tinklelyje yra būsena Sukurta.</span><span class="sxs-lookup"><span data-stu-id="d7389-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="d7389-110">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="d7389-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="d7389-111">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="d7389-111">Click Estimate.</span></span>
    * <span data-ttu-id="d7389-112">Šiame etape skaičiuojama vieno gamybos užsakymo įvertinta savikaina.</span><span class="sxs-lookup"><span data-stu-id="d7389-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="d7389-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d7389-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="d7389-114">Skaičiavimo informacijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="d7389-114">View the calculation details</span></span>
1. <span data-ttu-id="d7389-115">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="d7389-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="d7389-116">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="d7389-116">Click View calculation details.</span></span>
    * <span data-ttu-id="d7389-117">Šiame puslapyje rodomas išlaidų paskirstymas.</span><span class="sxs-lookup"><span data-stu-id="d7389-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="d7389-118">Pavyzdžiui, pirmoje eilutėje galite peržiūrėti baigto produkto vieneto bendrąją savikainą.</span><span class="sxs-lookup"><span data-stu-id="d7389-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="d7389-119">Kitose eilutėse pateikiamos išlaidos pagal komplektavimo specifikaciją, gamybos maršrutą ir netiesiogines išlaidas.</span><span class="sxs-lookup"><span data-stu-id="d7389-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
