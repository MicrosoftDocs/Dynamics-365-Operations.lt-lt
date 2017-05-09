---
title: "Pranešti, kad gamybos užsakymai įvykdyti"
description: "Pranešti, kad baigta yra gamybos etapas. Šiame etape pranešama apie pabaigtą produktą ir jis perkeliamas iš gamybos užsakymo į atsargas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


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




