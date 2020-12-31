---
title: Kliento lojalumo kortelės ir atlygio taškai
description: Šioje temoje aprašomas duomenų apie kliento lojalumo korteles ir atlygio taškų integravimas atliekant dvigubą rašymą.
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
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683503"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="909d4-103">Kliento lojalumo kortelės ir atlygio taškai</span><span class="sxs-lookup"><span data-stu-id="909d4-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="909d4-104">Įmonės klasifikuoja klientus ir teikia modernias paslaugas, pagrįstas kliento pirkimo ir išlaidų modeliais.</span><span class="sxs-lookup"><span data-stu-id="909d4-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="909d4-105">Pavyzdžiui, „Dynamics 365 Commerce“ yra infrastruktūra ir funkcijos, skirtos palengvinti tvarkyti klientų lojalumo korteles, atlygio taškai, lojalumu pagrįsta kainodara ir atlygiu pagrįsta pirkimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="909d4-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="909d4-106">Kai duomenys apie klientų lojalumo korteles ir atlygio taškus „Commerce“ sinchronizuoti su „Dataverse“, šiuos duomenis galima naudoti „Customer Engagement“ programose.</span><span class="sxs-lookup"><span data-stu-id="909d4-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="909d4-107">Pavyzdžiui, „Dynamics 365 Customer Service“ vartotojai gali naudoti duomenis, kad galėtų teikti tas pačias modernias paslaugas per pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="909d4-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="909d4-108">Šablonai</span><span class="sxs-lookup"><span data-stu-id="909d4-108">Templates</span></span>

| <span data-ttu-id="909d4-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="909d4-109">Finance and Operations apps</span></span> | <span data-ttu-id="909d4-110">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="909d4-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="909d4-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="909d4-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="909d4-112">Lojalumo kortelė</span><span class="sxs-lookup"><span data-stu-id="909d4-112">Loyalty card</span></span>                | <span data-ttu-id="909d4-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="909d4-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="909d4-114">Šis šablonas sinchronizuoja informaciją apie klientų lojalumo korteles.</span><span class="sxs-lookup"><span data-stu-id="909d4-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="909d4-115">Atlygio taškai už lojalumą</span><span class="sxs-lookup"><span data-stu-id="909d4-115">Loyalty reward points</span></span>       | <span data-ttu-id="909d4-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="909d4-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="909d4-117">Šis šablonas sinchronizuoja informaciją apie klientų atlygio taškus.</span><span class="sxs-lookup"><span data-stu-id="909d4-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
