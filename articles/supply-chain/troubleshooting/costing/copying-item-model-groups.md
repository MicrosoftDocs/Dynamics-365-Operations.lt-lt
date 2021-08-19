---
title: Kai prekių modelių grupės nukopijuojamos į kitą juridinį subjektą, trūksta lauko parametrų
description: Kai prekių modelių grupės nukopijuojamos į kitą juridinį subjektą, trūksta laukelio nustatymų.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738848"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Kai prekių modelių grupės nukopijuojamos į kitą juridinį subjektą, trūksta lauko parametrų

KB numeris: 4612800

## <a name="symptoms"></a>Požymiai

Kai kopijuosite prekių modelių grupes į kitą juridinį subjektą (įmonę) naudodami *prekių modelių grupės atsargų* strategijos subjektą, paskirties juridiniame subjekte naujoje modelių grupėje trūksta kai kurių laukų parametrų (pvz., atsargų modelio ir aprašymo).

## <a name="resolution"></a>Skiriamoji geba

Norėdami sukurti visą prekės modelių grupės kopiją kitam juridiniam subjektui, taip pat turite pasirinkti ir prekių modelių grupės atsargų strategijas (`InventInventoryPolicyEntity`) ir išlaidų srauto prielaidos strategijas, kurios susietos su prekės modelių (`InventCostFlowAssumptionPolicyEntity`) grupe.
