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
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026740"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="16ebc-103">Kai prekių modelių grupės nukopijuojamos į kitą juridinį subjektą, trūksta lauko parametrų</span><span class="sxs-lookup"><span data-stu-id="16ebc-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="16ebc-104">KB numeris: 4612800</span><span class="sxs-lookup"><span data-stu-id="16ebc-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="16ebc-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="16ebc-105">Symptoms</span></span>

<span data-ttu-id="16ebc-106">Kai kopijuosite prekių modelių grupes į kitą juridinį subjektą (įmonę) naudodami *prekių modelių grupės atsargų* strategijos subjektą, paskirties juridiniame subjekte naujoje modelių grupėje trūksta kai kurių laukų parametrų (pvz., atsargų modelio ir aprašymo).</span><span class="sxs-lookup"><span data-stu-id="16ebc-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="16ebc-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="16ebc-107">Resolution</span></span>

<span data-ttu-id="16ebc-108">Norėdami sukurti visą prekės modelių grupės kopiją kitam juridiniam subjektui, taip pat turite pasirinkti ir prekių modelių grupės atsargų strategijas (`InventInventoryPolicyEntity`) ir išlaidų srauto prielaidos strategijas, kurios susietos su prekės modelių (`InventCostFlowAssumptionPolicyEntity`) grupe.</span><span class="sxs-lookup"><span data-stu-id="16ebc-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
