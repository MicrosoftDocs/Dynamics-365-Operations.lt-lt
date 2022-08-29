---
title: Integruoti mokesčiai
description: Šiame straipsnyje aprašomas mokesčių duomenų integravimas tarp finansų ir operacijų bei Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288801"
---
# <a name="integrated-tax"></a>Integruoti mokesčiai

[!include [banner](../../includes/banner.md)]



Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka. Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.

## <a name="templates"></a>Šablonai

Mokesčių duomenis sudaro lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.

| „Finance and operations” programos | „Customer engagement“ programos | Aprašymas |
|-----------------------------|-----------------------------------|-------------|
[Prekės PVM grupė](mapping-reference.md#196) | msdyn_mokesčiųprekiųgrupės | |
[PVM rinkėjai](mapping-reference.md#193) | msdyn_mokesčiųinspekcijos | |
[Atleidimo nuo PVM kodo objekto CDS](mapping-reference.md#194) | msdyn_mokesčiųlengvatųkodai | |
[PVM grupės](mapping-reference.md#195) | msdyn_mokesčiųgrupės | |
[Didžiosios knygos PVM registravimo grupės V2](mapping-reference.md#197) | msdyn_mokesčiųregistravimogrupės | |
[Išskaitomų mokesčių kodai](mapping-reference.md#210) | msdyn_atidedamųmokesčiųkodai | |
[Išskaitomo mokesčio grupės](mapping-reference.md#211) | msdyn_atidedamųmokesčiųgrupės | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

