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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998019"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="37c35-103">Kliento lojalumo kortelės ir atlygio taškai</span><span class="sxs-lookup"><span data-stu-id="37c35-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="37c35-104">Įmonės klasifikuoja klientus ir teikia modernias paslaugas, pagrįstas kliento pirkimo ir išlaidų modeliais.</span><span class="sxs-lookup"><span data-stu-id="37c35-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="37c35-105">„Microsoft Dynamics 365“ programų pakete „Dynamics 365 Commerce“ turi infrastruktūrą ir funkcijas, skirtas palengvinti tvarkyti klientų lojalumo korteles, atlygio taškus, lojalumu pagrįstą kainodarą ir atlygiu pagrįstą pirkimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="37c35-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="37c35-106">Kai duomenys apie klientų lojalumo korteles ir atlygio taškus „Commerce“ sinchronizuoti su „Common Data service“, šiuos duomenis galima naudoti modeliu grįstose programose „Dynamics 365“.</span><span class="sxs-lookup"><span data-stu-id="37c35-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="37c35-107">Pavyzdžiui, „Dynamics 365 Customer Service“ vartotojai gali naudoti duomenis, kad galėtų teikti tas pačias modernias paslaugas per pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="37c35-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="37c35-108">Šablonai</span><span class="sxs-lookup"><span data-stu-id="37c35-108">Templates</span></span>

| <span data-ttu-id="37c35-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="37c35-109">Finance and Operations apps</span></span> | <span data-ttu-id="37c35-110">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="37c35-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="37c35-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="37c35-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="37c35-112">Lojalumo kortelė</span><span class="sxs-lookup"><span data-stu-id="37c35-112">Loyalty card</span></span>                | <span data-ttu-id="37c35-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="37c35-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="37c35-114">Šis šablonas sinchronizuoja informaciją apie klientų lojalumo korteles.</span><span class="sxs-lookup"><span data-stu-id="37c35-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="37c35-115">Atlygio taškai už lojalumą</span><span class="sxs-lookup"><span data-stu-id="37c35-115">Loyalty reward points</span></span>       | <span data-ttu-id="37c35-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="37c35-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="37c35-117">Šis šablonas sinchronizuoja informaciją apie klientų atlygio taškus.</span><span class="sxs-lookup"><span data-stu-id="37c35-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
