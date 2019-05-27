---
title: Savikainos objektai
description: Šiame straipsnyje pateikiama informacija apie savikainos objektus ir paaiškinama, kaip kaupiamos savikainos ir kiekiai. Savikainos objektas yra objektas, kuriam kaupiamos išlaidos ir kiekiai. Savikainos objekto objektas gali būti produktas arba produkto variantas, pvz., stiliaus ir spalvos variantai.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275855f2fb4d32df91449d7ebb9ad9ba2bd3f36b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558554"
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
    -   Fakt. išlaidų suma
    -   Fin. išlaidų suma
    -   Koregavimai
-   Reikšmė **Kiekio** lauke yra tolesnių reikšmių suma.
    -   Gauta
    -   Išskaičiuota
    -   Užregistruotas kiekis
-   **Vidutinės vieneto savikainos** laukas yra apskaičiuotasis laukas. Reikšmė apskaičiuojama **Vertės** reikšmę padalijus iš **Kiekio** reikšmės.

**Pastaba.** Ankstesniems skaičiavimams parametras **Įtraukti fizinę vertę** įtakos neturi.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Produkto dimensijų grupė](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Saugojimo dimensijų grupė](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Sekimo dimensijų grupė](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Kas nauja ar pasikeitė](../../fin-and-ops/get-started/whats-new-changed.md)

[Savikainos įrašai](cost-entries.md)



