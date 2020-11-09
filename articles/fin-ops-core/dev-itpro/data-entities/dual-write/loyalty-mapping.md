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
# <a name="customer-loyalty-cards-and-reward-points"></a>Kliento lojalumo kortelės ir atlygio taškai

[!include [banner](../../includes/banner.md)]



Įmonės klasifikuoja klientus ir teikia modernias paslaugas, pagrįstas kliento pirkimo ir išlaidų modeliais. „Microsoft Dynamics 365“ programų pakete „Dynamics 365 Commerce“ turi infrastruktūrą ir funkcijas, skirtas palengvinti tvarkyti klientų lojalumo korteles, atlygio taškus, lojalumu pagrįstą kainodarą ir atlygiu pagrįstą pirkimo patirtį. Kai duomenys apie klientų lojalumo korteles ir atlygio taškus „Commerce“ sinchronizuoti su „Common Data service“, šiuos duomenis galima naudoti modeliu grįstose programose „Dynamics 365“. Pavyzdžiui, „Dynamics 365 Customer Service“ vartotojai gali naudoti duomenis, kad galėtų teikti tas pačias modernias paslaugas per pagalbos tarnybą.

## <a name="templates"></a>Šablonai

| „Finance and Operations” programėlės | Modeliu grįstos programos „Dynamics 365“ | aprašymas |
|-----------------------------|-----------------------------------|-------------|
| Lojalumo kortelė                | msdyn\_loyaltycards               | Šis šablonas sinchronizuoja informaciją apie klientų lojalumo korteles. |
| Atlygio taškai už lojalumą       | msdyn\_loyaltyrewardpoints        | Šis šablonas sinchronizuoja informaciją apie klientų atlygio taškus. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
