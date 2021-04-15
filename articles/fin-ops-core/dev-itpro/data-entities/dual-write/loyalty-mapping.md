---
title: Kliento lojalumo kortelės ir atlygio taškai
description: Šioje temoje aprašomas duomenų apie kliento lojalumo korteles ir atlygio taškų integravimas atliekant dvigubą rašymą.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747992"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="b61ca-103">Kliento lojalumo kortelės ir atlygio taškai</span><span class="sxs-lookup"><span data-stu-id="b61ca-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b61ca-104">Įmonės klasifikuoja klientus ir teikia modernias paslaugas, pagrįstas kliento pirkimo ir išlaidų modeliais.</span><span class="sxs-lookup"><span data-stu-id="b61ca-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="b61ca-105">Pavyzdžiui, „Dynamics 365 Commerce“ yra infrastruktūra ir funkcijos, skirtos palengvinti tvarkyti klientų lojalumo korteles, atlygio taškai, lojalumu pagrįsta kainodara ir atlygiu pagrįsta pirkimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="b61ca-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="b61ca-106">Kai duomenys apie klientų lojalumo korteles ir atlygio taškus „Commerce“ sinchronizuoti su „Dataverse“, šiuos duomenis galima naudoti „Customer Engagement“ programose.</span><span class="sxs-lookup"><span data-stu-id="b61ca-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="b61ca-107">Pavyzdžiui, „Dynamics 365 Customer Service“ vartotojai gali naudoti duomenis, kad galėtų teikti tas pačias modernias paslaugas per pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="b61ca-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="b61ca-108">Šablonai</span><span class="sxs-lookup"><span data-stu-id="b61ca-108">Templates</span></span>

| <span data-ttu-id="b61ca-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="b61ca-109">Finance and Operations apps</span></span> | <span data-ttu-id="b61ca-110">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="b61ca-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="b61ca-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b61ca-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="b61ca-112">Lojalumo kortelė</span><span class="sxs-lookup"><span data-stu-id="b61ca-112">Loyalty card</span></span>                | <span data-ttu-id="b61ca-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="b61ca-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="b61ca-114">Šis šablonas sinchronizuoja informaciją apie klientų lojalumo korteles.</span><span class="sxs-lookup"><span data-stu-id="b61ca-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="b61ca-115">Atlygio taškai už lojalumą</span><span class="sxs-lookup"><span data-stu-id="b61ca-115">Loyalty reward points</span></span>       | <span data-ttu-id="b61ca-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="b61ca-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="b61ca-117">Šis šablonas sinchronizuoja informaciją apie klientų atlygio taškus.</span><span class="sxs-lookup"><span data-stu-id="b61ca-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]