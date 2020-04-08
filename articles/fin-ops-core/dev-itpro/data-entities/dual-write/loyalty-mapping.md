---
title: Kliento lojalumo kortelės ir atlygio taškai
description: Šioje temoje aprašomas duomenų apie kliento lojalumo korteles ir atlygio taškų tarp „Finance and Operations“ programų ir „Common Data Service“ integravimas.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172974"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="b3019-103">Kliento lojalumo kortelės ir atlygio taškai</span><span class="sxs-lookup"><span data-stu-id="b3019-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b3019-104">Įmonės klasifikuoja klientus ir teikia modernias paslaugas, pagrįstas kliento pirkimo ir išlaidų modeliais.</span><span class="sxs-lookup"><span data-stu-id="b3019-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="b3019-105">„Microsoft Dynamics 365“ programų pakete „Dynamics 365 Commerce“ turi infrastruktūrą ir funkcijas, skirtas palengvinti tvarkyti klientų lojalumo korteles, atlygio taškus, lojalumu pagrįstą kainodarą ir atlygiu pagrįstą pirkimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="b3019-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="b3019-106">Kai duomenys apie klientų lojalumo korteles ir atlygio taškus „Commerce“ sinchronizuoti su „Common Data service“, šiuos duomenis galima naudoti modeliu grįstose programose „Dynamics 365“.</span><span class="sxs-lookup"><span data-stu-id="b3019-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="b3019-107">Pavyzdžiui, „Dynamics 365 Customer Service“ vartotojai gali naudoti duomenis, kad galėtų teikti tas pačias modernias paslaugas per pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="b3019-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="b3019-108">Šablonai</span><span class="sxs-lookup"><span data-stu-id="b3019-108">Templates</span></span>

| <span data-ttu-id="b3019-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="b3019-109">Finance and Operations apps</span></span> | <span data-ttu-id="b3019-110">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="b3019-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="b3019-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b3019-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="b3019-112">Lojalumo kortelė</span><span class="sxs-lookup"><span data-stu-id="b3019-112">Loyalty card</span></span>                | <span data-ttu-id="b3019-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="b3019-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="b3019-114">Šis šablonas sinchronizuoja informaciją apie klientų lojalumo korteles.</span><span class="sxs-lookup"><span data-stu-id="b3019-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="b3019-115">Atlygio taškai už lojalumą</span><span class="sxs-lookup"><span data-stu-id="b3019-115">Loyalty reward points</span></span>       | <span data-ttu-id="b3019-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="b3019-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="b3019-117">Šis šablonas sinchronizuoja informaciją apie klientų atlygio taškus.</span><span class="sxs-lookup"><span data-stu-id="b3019-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
