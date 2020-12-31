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
# <a name="customer-loyalty-cards-and-reward-points"></a>Kliento lojalumo kortelės ir atlygio taškai

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Įmonės klasifikuoja klientus ir teikia modernias paslaugas, pagrįstas kliento pirkimo ir išlaidų modeliais. Pavyzdžiui, „Dynamics 365 Commerce“ yra infrastruktūra ir funkcijos, skirtos palengvinti tvarkyti klientų lojalumo korteles, atlygio taškai, lojalumu pagrįsta kainodara ir atlygiu pagrįsta pirkimo patirtis. Kai duomenys apie klientų lojalumo korteles ir atlygio taškus „Commerce“ sinchronizuoti su „Dataverse“, šiuos duomenis galima naudoti „Customer Engagement“ programose. Pavyzdžiui, „Dynamics 365 Customer Service“ vartotojai gali naudoti duomenis, kad galėtų teikti tas pačias modernias paslaugas per pagalbos tarnybą.

## <a name="templates"></a>Šablonai

| „Finance and Operations” programėlės | Modeliu grįstos programos „Dynamics 365“ | aprašymas |
|-----------------------------|-----------------------------------|-------------|
| Lojalumo kortelė                | msdyn\_loyaltycards               | Šis šablonas sinchronizuoja informaciją apie klientų lojalumo korteles. |
| Atlygio taškai už lojalumą       | msdyn\_loyaltyrewardpoints        | Šis šablonas sinchronizuoja informaciją apie klientų atlygio taškus. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
