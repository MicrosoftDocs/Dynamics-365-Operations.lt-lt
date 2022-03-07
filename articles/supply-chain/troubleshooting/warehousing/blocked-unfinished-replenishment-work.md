---
title: Paėmimo darbas užblokuotas, nes nebaigtas papildymo darbas
description: Paėmimo darbas gali būti blokuojamas dėl priklausančio papildymo darbo. Užbaikite papildymo darbą ir tada apdorokite paėmimo darbą.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477138"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Paėmimo darbas negali būti atrakintas dėl nepabaigto papildymo darbo

## <a name="symptoms"></a>Požymiai

Naudojant bangos paklausos papildymą, paėmimo darbas gali būti užblokuotas dėl priklausomo papildymo darbo. Jei Jums naudojant bangos poreikio papildymą, jei paėmimo vieta turi būti papildoma siekiant įgyvendinti šaltinio užsakymo poreikį, sistema sukuria papildymo darbą ir paėmimo darbą. Tačiau jis neleidžia paimti darbo, kol papildymo darbas nėra baigtas, ir jūs gaunate tokį klaidos pranešimą:

> Negalima atblokuoti darbo %1, nes jame yra nebaigtas papildymo darbas.

## <a name="resolution"></a>Sprendimas

Šis elgesys yra tyčinis, nes paėmimo vieta neturės pakankamai inventoriaus, nebent papildymo darbas bus užbaigtas. Užbaikite papildymo darbą ir tada apdorokite paėmimo darbą.
