---
title: Trikčių šalinimo sandėlio papildymas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828087"
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