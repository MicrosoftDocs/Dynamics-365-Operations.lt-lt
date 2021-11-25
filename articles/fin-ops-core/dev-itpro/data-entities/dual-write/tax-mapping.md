---
title: Integruoti mokesčiai
description: Šioje temoje aprašomas mokesčių duomenų integravimas tarp „Finance and Operations“ ir „Dataverse“.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1e74bbbeba019ca48dd823b58251643e96edd0c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782215"
---
# <a name="integrated-tax"></a>Integruoti mokesčiai

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka. Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.

## <a name="templates"></a>Šablonai

Mokesčių duomenis sudaro lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.

| „Finance and Operations” programos | „Customer engagement“ programos | Aprašas |
|-----------------------------|-----------------------------------|-------------|
[Prekės PVM grupė](mapping-reference.md#196) | msdyn_mokesčiųprekiųgrupės | |
[PVM rinkėjai](mapping-reference.md#193) | msdyn_mokesčiųinspekcijos | |
[Atleidimo nuo PVM kodo objekto CDS](mapping-reference.md#194) | msdyn_mokesčiųlengvatųkodai | |
[PVM grupės](mapping-reference.md#195) | msdyn_mokesčiųgrupės | |
[Didžiosios knygos PVM registravimo grupės V2](mapping-reference.md#197) | msdyn_mokesčiųregistravimogrupės | |
[Išskaitomų mokesčių kodai](mapping-reference.md#210) | msdyn_atidedamųmokesčiųkodai | |
[Išskaitomo mokesčio grupės](mapping-reference.md#211) | msdyn_atidedamųmokesčiųgrupės | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
