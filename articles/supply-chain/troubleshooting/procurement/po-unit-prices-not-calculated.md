---
title: Vienetų kainos pirkimo užsakymuose neskaičiuojamos pagal vienetų konvertavimą
description: Vienetų kainos pirkimo užsakymuose neskaičiuojamos pagal vienetų konvertavimą
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477087"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Vienetų kainos pirkimo užsakymuose neskaičiuojamos pagal vienetų konvertavimą

## <a name="symptoms"></a>Požymiai

Kai pirkimo užsakymo vienetas yra pakeičiamas, prekybos sutarčių kainos nėra perskaičiuojamos pagal vienetų konvertavimo apibrėžimus.

## <a name="cause"></a>Priežastis

Kainos visada gaunamos iš prekybos sutarčių (arba kitų sistemos kainos parametrų, tokių kaip pardavimo sutartys arba prekių kainos) ir yra nustatomos vienetui.

Jei vienetas pakeičiamas užsakymo eilutėje, sistema ieško naujo vieneto kainos ir pritaiko tą kainą. Jei nerandama vieneto kaina, sistema nepritaiko kainos. Vieneto konvertavimo negalima naudoti kainos perskaičiavimui į kitą vienetą. Teoriškai, vieno langelio dešimties vienetų kaina gali būti ne tokia pat kaip dešimt kartų didesnė kaina už vieno langelio kainą.

## <a name="workaround"></a>Apėjimo būdas

Vienas iš būdų, kaip išspręsti šią problemą, yra įsitikinti, kad yra prekybos sutarčių tiems vienetams, kuriuos tikitės panaudoti prekės užsakymo eilutėse.
