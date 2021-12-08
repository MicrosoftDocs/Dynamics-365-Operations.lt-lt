---
title: Pakeitus pirkimo užsakymo pristatymo adresą, pristatymo pavadinimas nėra sinchronizuojamas
description: Jums pakeitus pristatymo adresą pirkimo užsakymo antraštėje, pristatymo pavadinimas nėra sinchronizuojamas
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477060"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Pakeitus pirkimo užsakymo pristatymo adresą, pristatymo pavadinimas nėra sinchronizuojamas

## <a name="symptoms"></a>Požymiai

Pirkimo užsakymo antraštėje esantis adresas atnaujinamas į adresą, kuris nėra pristatymo adresas. Nors adresas yra atnaujinamas pirkimo užsakyme, pristatymo pavadinimas nėra atnaujinamas pagal atnaujintą adresą.

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. Pasirinktas adresas turi būti klasifikuojamas kaip pristatymo adresas. Kitu atveju pristatymo pavadinimas nėra atnaujinamas pagal pasirinktą adresą.