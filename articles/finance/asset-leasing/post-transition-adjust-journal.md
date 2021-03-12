---
title: Perkėlimo koregavimo žurnalo įrašų registravimas turto nuomoje
description: Šioje temoje aprašomos funkcijos, leidžiančios jums pereiti į nuomos portfelį pagal naujus nuomos apskaitos standartus, apskaitos standartų kodifikavimo temą Nr. 842 (ASC 842) ir tarptautinį finansinės atskaitomybės standartą Nr. 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969558"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Perkėlimo koregavimo žurnalo įrašų registravimas turto nuomoje

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, leidžiančios jums pereiti į nuomos portfelį su naujais nuomos apskaitos standartais: apskaitos standartų kodifikavimo tema Nr. 842 (ASC 842), kuri yra standartas bendrai priimtuose apskaitos principuose JAV (US GAAO)., ir tarptautiniu finansinės atskaitomybės standartu Nr. 16 (IFRS 16).

Norėdami gauti informacijos apie tai, kaip nustatyti perėjimo į naujus standartus knygą, žr. [Nuomos knygų nustatymas](set-up-lease-books.md).

Kuriant perėjimo derinimo žurnalo įrašą, generuojamas žurnalo įrašas. Šis įrašas atspindi nuomos balansų poveikį, kuris yra įrašomas pagal naujus standartus tą dieną. Atitinkama turto sąskaita debetuojama dėl tos datos balansinės vertės, o įsipareigojimo sąskaita kredituojama. Skirtumas yra arba debetuojamas, arba kredituojamas į nepaskirstytąjį pelną.

Norėdami užregistruoti perėjimo derinimą, laikydamasis naujų apskaitos standartų, atlikite šiuos veiksmus.

1. Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada – **Knygos**.
2. Knygoje pasirinkite **Mokėjimo grafikas**.
3. Dialogo lange **Mokėjimo grafikas** pasirinkite **Patvirtinti**. Tada uždarykite dialogo langą.
4. Pasirinkite **Perkėlimo koregavimas**.

    > [!NOTE]
    > Gali būti sukurtas tik nuomos knygų, priskirtų knygai, kurioje yra laukas **Perkėlimo knyga**, perkėlimo koregavimas. Jei lauko **Nuomos pradžia** vertė yra vėlesnė už perkėlimo datą, lauko **Perkėlimo koregavimas** vertė nebus atnaujinta.

5. Norėdami peržiūrėti žurnalo įrašą, pasirinkite **Turto nuomos žurnalai**.
6. Pasirinkite naują žurnalą ir pasirinkite **Registruoti**.
