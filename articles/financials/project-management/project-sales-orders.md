---
title: Projekto pardavimo užsakymai
description: Šioje temoje paaiškinama, kaip kurti pojektinius pardavimo užsakymus dirbant su laiko ir medžiagų projektais.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/12/2019
ms.locfileid: "976684"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Laiko ir medžiagų projektų pardavimo užsakymai

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Šioje temoje aprašoma, kaip sukurti projekto pardavimo užsakymą. Pardavimo užsakymus galima sukurti tik tiems projektams, kurių tipas **laikas ir medžiagos**.

Jei laiko ir medžiagų projekto sutartyje nurodyti keli lėšų skyrimo šaltiniai, puslapyje **Projektų valdymo ir apskaitos parametrai** būtina įjungti parametrą **Leisti projektų su keliais lėšų skyrimo šaltiniais pardavimo užsakymus**. 

> [!NOTE]
> - Projektų pardavimo užsakymai su keliais lėšų skyrimo šaltiniais palaikomi naudojant programos versiją 10.0.2 ir naujesnę versiją.
> - 2020 m. balandžio mėn. leidime parametras, skirtas įjungti projektų pardavimo užsakymų su keliais lėšų skyrimo šaltiniais palaikymą, bus panaikintas, taigi vėliau išleistose versijose funkcija bus visada įjungta.

Projektinius pardavimo užsakymus galite kurti dviem būdais.

- Eikite į patį projektą. Veiksmų srityje pasirinkite **Valdyti > Prekių užduotys > Pardavimo užsakymas**. Projekto informacijoje nurodomas numatytasis projekto pardavimo užsakymas. Jei projekto sutartyje nurodytas daugiau nei vienas lėšų skyrimo šaltinis, norėdami nustatyti pardavimo užsakymo klientą, turėsite pasirinkti lėšų skyrimo šaltinį. Jei yra tik vienas projekto lėšų skyrimo šaltinis, klientas nustatomas automatiškai.
- Eikite į sąrašo puslapį **Visi pardavimo užsakymai** ir sukurkite naują pardavimo užsakymą. Turite pasirinkti projektą, kuriam kuriamas pardavimo užsakymas. Pasirinkus projektą, klientas nustatomas pagal lėšų skyrimo šaltinį arba, jei projekto sutartyje nurodyti keli lėšų skyrimo šaltiniai, turėsite pasirinkti lėšų skyrimo šaltinį.

