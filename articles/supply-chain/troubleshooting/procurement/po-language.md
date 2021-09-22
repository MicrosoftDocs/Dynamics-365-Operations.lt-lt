---
title: Pirkimo užsakymai neatspindi juridinio subjekto kalbos nustatymų
description: Produkto pavadinimas pirkimo užsakyme rodomas sistemos kalba, o ne kalba, nustatyta juridiniam subjektui, kuriame buvo sukurtas pirkimo užsakymas
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477081"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Pirkimo užsakymai neatspindi juridinio subjekto kalbos nustatymų


## <a name="symptoms"></a>Požymiai

Produkto pavadinimas pirkimo užsakyme rodomas sistemos kalba, o ne kalba, nustatyta juridiniam subjektui, kuriame buvo sukurtas pirkimo užsakymas.

## <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Nustatykite sistemos kalbą į *EN-US* (JAV anglų kalba).
1. Įsitikinkite, kad egzistuoja produktas, kuriame *EN-US* ir *DE* (vokiečių) kalbos yra palaikomos produkto pavadinimo vertimams.
1. Pakeisti juridinio subjekto kalbą į *DE*.
1. Juridiniame subjekte, kuriame *DE* yra nustatyta kaip kalba, sukurkite pirkimo užsakymą, kuriame yra produktas.
1. Atkreipkite dėmesį, kad produkto pavadinimas vis dar rodomas JAV anglų kalba (sistemos kalba).

## <a name="resolution"></a>Sprendimas

Toks veikimo būdas yra numatytas. Pirkimo užsakymuose produktas visada rodomas sistemos kalba. Pirkimo užsakymo kalba yra naudojama, kai kuriamas patvirtinimo žurnalas.
