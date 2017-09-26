---
title: "Pranešti, kad gamybos užsakymai įvykdyti"
description: "Pranešti, kad baigta yra gamybos etapas. Šiame etape pranešama apie pabaigtą produktą ir jis perkeliamas iš gamybos užsakymo į atsargas."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 52607d645c6eaf4ff97d2c4bf8abc6ec1374fd7e
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="report-production-orders-as-finished"></a>Pranešti, kad gamybos užsakymai įvykdyti

[!include[banner](../includes/banner.md)]


Pranešti, kad baigta yra gamybos etapas. Šiame etape pranešama apie pabaigtą produktą ir jis perkeliamas iš gamybos užsakymo į atsargas.

Kai gamybos užsakymas paskelbiamas baigtu, pagamintų prekių kiekis atsargose yra atnaujinamas kaip turimas. Dalinius suplanuoto užsakymo kiekio kiekius galima paskelbti baigtais. Skelbiant kiekius baigtais taip pat galima apie klaidingus kiekius teikti ataskaitas su susieta klaidos priežastimi. Kai gamybos užsakymas tampa Paskelbtas baigtu, tai reiškia, kad daugiau apie gamybos užsakymo kiekį ataskaitos nebebus teikiamos.
Toliau pateiktos charakteristikos taip pat yra susietos su procesu **Skelbti baigtu**.
-   Galima nustatyti žaliavų ir laiko, proporcingų paskelbtam kiekiui (atgalinis suvartojimas), suvartojimą
-   Galima generuoti prekių, kurias galima naudoti sandėlio procesuose, atidėjimo darbą.
-   Galima nustatyti, kad DK sąskaitoms būtų teikiamos ataskaitos apie pagamintų prekių planuojamų arba standartinių išlaidų vertę.
-   Paskelbto kiekio kokybės užsakymą galima sukurti pagal kokybės susiejimo sąranką.

Kiekis skelbiamas išeigos vietoje. Tada sugeneruojamas sandėlio darbas kiekiui iš išeigos vietos į paskirties vietą, nustatytą atidėjimo darbo vietos nurodymu, perkelti.

-   Galima sukurti kokybės užsakymą, kai gamybos užsakymas yra paskelbtas baigtu, jei buvo nustatytas kokybės susiejimas.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Gamybos užsakymo nustatymas kaip paskelbto baigtu
Gamybos užsakymas gali būti nustatytas kaip **Skelbti baigtu** naudojant standartinę gamybos užsakymo atnaujinimo funkciją, technologinės ir užduoties kortelių žurnalus arba gamybos žurnalą **Skelbti baigtu**. Taip pat galina atnaujinti etapą į **Skelbti baigtu** naudojant užduoties kortelės terminalo ir užduoties kortelės įrenginio puslapius, kai paskelbiate paskutinę gamybos užsakymo užduotį. Galiausiai galite aktyvinti parinktį **Skelbti baigtu** kaip sandėlio kišeninio įrenginio sprendimo procesą.  




