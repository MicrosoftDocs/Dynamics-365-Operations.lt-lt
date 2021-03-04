---
title: Trikčių šalinimo sandėlio papildymas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644878"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Trikčių šalinimo sandėlio papildymas

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Gaunu tolesnį klaidos pranešimą: „Darbas %1 negali būti atblokuotas dėl to, kad turi nepabaigtą papildymo darbą."

### <a name="issue-description"></a>Problemos aprašas

Paėmimo darbas blokuojamas dėl priklausančio papildymo darbo.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jums naudojant bangos poreikio papildymą, jei paėmimo vieta turi būti papildoma siekiant įgyvendinti šaltinio užsakymo poreikį, sistema sukuria papildymo darbą ir paėmimo darbą. Nepaisant to, ji blokuoja paėmimo darbą, kol bus užbaigtas papildymo darbas. Šis elgesys yra tyčinis, nes paėmimo vieta neturės pakankamai inventoriaus, nebent papildymo darbas bus užbaigtas. Užbaikite papildymo darbą ir tada apdorokite paėmimo darbą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]