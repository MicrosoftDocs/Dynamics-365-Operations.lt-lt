---
title: Savikainos objektai
description: Šiame straipsnyje pateikiama informacija apie savikainos objektus ir paaiškinama, kaip kaupiamos savikainos ir kiekiai. Savikainos objektas yra objektas, kuriam kaupiamos išlaidos ir kiekiai. Savikainos objekto objektas gali būti produktas arba produkto variantas, pvz., stiliaus ir spalvos variantai.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d27e2dcfd8f70c8d4b0f2ae1254f3c4fce63bb4d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572174"
---
# <a name="cost-objects"></a>Savikainos objektai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie savikainos objektus ir paaiškinama, kaip kaupiamos savikainos ir kiekiai. Savikainos objektas yra objektas, kuriam kaupiamos išlaidos ir kiekiai. Savikainos objekto objektas gali būti produktas arba produkto variantas, pvz., stiliaus ir spalvos variantai.  

## <a name="cost-objects"></a>Savikainos objektai

**Išlaidų objektų** puslapyje išvardyti visi registruoti produkto išlaidų objektai. Išlaidų objektai apibrėžiami pagal duomenis iš tolesnių šaltinių.

-   Produktas
-   Produkto dimensijų grupė
-   Saugojimo dimensijų grupė
-   Sekimo dimensijų grupė

**Pastaba.** Išlaidų objektas atitinka tik **Tiesioginės medžiagos** tipo išlaidų elementą. Išlaidų objektas ir atsargų objektas skiriasi tuo, kad išlaidų objektas apibrėžiamas pagal pasirinktas finansinių atsargų dimensijas. Pavyzdžiui, prekės konfigūracija yra tokia, kokia pateikta toliau.

-   **Teritorija:** fizinės atsargos = taip, finansinės atsargos = taip
-   **Sandėlis:** fizinės atsargos = taip, finansinės atsargos = ne
-   **Paketo Nr.:** fizinės atsargos = taip, finansinės atsargos = ne

Toliau pateikiamoje lentelėje parodyta, kas yra išlaidų objektas ir kas yra atsargų objektas.

| Objekto tipas      | Prekės numeris | Svetainė | Sandėlis | Paketo nr. |
|------------------|-------------|------|-----------|-----------|
| Išlaidų objektas      | x           | x    |           |           |
| Atsargų objektas | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Išlaidų ir kiekių kaupimas
-   Reikšmė **Vertės** lauke yra tolesnių reikšmių suma.
    -   Faktinių išlaidų suma
    -   Finansinių išlaidų suma
    -   Koregavimai
-   Reikšmė **Kiekio** lauke yra tolesnių reikšmių suma.
    -   Gauta
    -   Išskaičiuota
    -   Užregistruotas kiekis
-   **Vidutinės vieneto savikainos** laukas yra apskaičiuotasis laukas. Reikšmė apskaičiuojama **Vertės** reikšmę padalijus iš **Kiekio** reikšmės.

**Pastaba.** Ankstesniems skaičiavimams parametras **Įtraukti fizinę vertę** įtakos neturi.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produkto dimensijų grupė](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Saugojimo dimensijų grupė](/dynamicsax-2012//storage-dimension-groups-form)

[Sekimo dimensijų grupė](/dynamicsax-2012//tracking-dimension-groups-form)

[Kas nauja ar pasikeitė](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Savikainos įrašai](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]