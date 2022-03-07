---
title: Numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo
description: Numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477085"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo

## <a name="symptoms"></a>Požymiai

Jei naudojate mokėtojo kodą, kuris skiriasi nuo kliento kodo, numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo sukūrus pirkimo užsakymą.

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. Numatytosios mokesčių grupės vertės, mokėjimo nuolaidos ir kita kainos informacija yra paremtos kliento, o ne mokėtojo kodu.
