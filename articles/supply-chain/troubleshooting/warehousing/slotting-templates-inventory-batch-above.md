---
title: Turimos atsargos nelaikomos kaip paketinių užduočių prekės
description: Kai kuriuose laiko atminties atminties atminties šablonuose nenagrinėjamos dabar turimos atsargos, skirti pakete aukščiau esamoms prekėms. Poreikio užsakyme turi būti nurodytas paketas arba serijos numeris.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477092"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Laiko atminties atminties atminties šablonuose nenagrinėjamos dabar turimos atsargos, skirti pakete aukščiau esamoms prekėms

## <a name="symptoms"></a>Požymiai

Intervalo šablonai, turintys *Atsižvelgti į turimas atsargas* intervalo kriterijų, neatsižvelgia į dabartines turimas atsargas, skirtas *paketas aukščiau* prekėms. Jie atsižvelkite į jas tik tuo atveju, jei pardavimo užsakymo eilutėje nurodytas paketo numeris.

Tačiau, kai naudojate *paketas žemiau* prekes, laikoma, kad dabartinės turimos atsargos yra tikėtinos.

Daugiau informacijos rasite [Sandėlio intervalas](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Sprendimas

Intervalo šablono antraštę galima nurodyti *Užsakyta*, *Rezervuota* arba *Išleista* poreikio strategijoms. Poreikio strategijai *Užsakyta* taikomi tie patys rezervavimo hierarchijos reikalavimai, kurie taikomi ir rezervavimo arba išleidimo į sandėlio procesams. Todėl prekių, turinčių *paketas aukščiau* ir *serija žemiau* rezervavimo hierarchijas, poreikio užsakyme (pardavimo arba perkėlimo) turi būti nurodytas paketo arba serijos numeris.

Taip pat, galima naudoti poreikio strategiją *Rezervuota* pasirinkti paketo arba serijos numerį prieš generuojant sandėlio intervalo poreikį.
