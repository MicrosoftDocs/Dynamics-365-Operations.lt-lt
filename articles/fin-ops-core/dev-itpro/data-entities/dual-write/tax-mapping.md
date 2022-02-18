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
ms.openlocfilehash: 532e6603b74ad0293d65684d2d6858ef31fbc496
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063192"
---
# <a name="integrated-tax"></a>Integruoti mokesčiai

[!include [banner](../../includes/banner.md)]



Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka. Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.

## <a name="templates"></a>Šablonai

Mokesčių duomenis sudaro lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.

| „Finance and Operations” programos | „Customer engagement“ programos | Aprašymas |
|-----------------------------|-----------------------------------|-------------|
[Prekės PVM grupė](mapping-reference.md#196) | msdyn_mokesčiųprekiųgrupės | |
[PVM rinkėjai](mapping-reference.md#193) | msdyn_mokesčiųinspekcijos | |
[Atleidimo nuo PVM kodo objekto CDS](mapping-reference.md#194) | msdyn_mokesčiųlengvatųkodai | |
[PVM grupės](mapping-reference.md#195) | msdyn_mokesčiųgrupės | |
[Didžiosios knygos PVM registravimo grupės V2](mapping-reference.md#197) | msdyn_mokesčiųregistravimogrupės | |
[Išskaitomų mokesčių kodai](mapping-reference.md#210) | msdyn_atidedamųmokesčiųkodai | |
[Išskaitomo mokesčio grupės](mapping-reference.md#211) | msdyn_atidedamųmokesčiųgrupės | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
