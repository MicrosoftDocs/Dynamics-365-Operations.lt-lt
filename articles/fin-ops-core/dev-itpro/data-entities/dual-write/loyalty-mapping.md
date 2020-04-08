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
