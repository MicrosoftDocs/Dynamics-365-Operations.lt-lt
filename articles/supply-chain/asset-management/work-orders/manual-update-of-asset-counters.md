---
title: Neautomatinis turto skaitiklių atnaujinimas
description: Šioje temoje aprašomas turto skaitiklių naujinimas rankiniu būdu skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875800"
---
# <a name="manual-update-of-asset-counters"></a>Neautomatinis turto skaitiklių atnaujinimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Skaitikliai naudojami kuriant turto registracijas, pvz., operacijos valandų skaičių arba pagamintų kiekių skaičių.

Jei skaitikliui parinktas skaitiklio tipas nustatytas perimti skaitiklio reikšmes (**Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai** > **Bendra** „FastTab“ > **Perimti turto skaitiklio vertes** perjungiklis nustatytas į Taip), tada, kai kursite to tipo naują skaitiklio eilutę, kiekvienas antrinis turtas, naudojantis tą patį skaitiklio tipą, automatiškai naujinamas.

Skiltyje **Visas turtas** galite turtui sukurti valandų ar dydžio skaitiklių registracijų, atsižvelgiant į jūsų turto rodmenis.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Turtas** > **Visas turtas**.

2. Sąraše pasirinkite turtą ir spustelėkite **Skaitikliai**. Formoje **Turto skaitikliai** galite matyti visų buvusių skaitiklių registracijų pasirinktam turtui sąrašą.

3. Spustelėkite **Naujas**, kad sukurtumėte naują registraciją. Turto ID įterpiamas automatiškai.

4. Lauke **Skaitiklis** pažymėkite susijusį skaitiklį. Tik skaitikliai, susiję su turto tipu, pasirinktu tam turtui, yra pasiekiami. Susijęs vienetas yra automatiškai įterpiamas į lauką **Vienetas**.

5. Skaitiklio registracijai nurodykite datą ir laiką.

6. Lauke **Reikšmė** įterpkite paskutinio skaitiklio registracijos numerį arba, į lauką **Agreguota reikšmė** įterpkite bendrą skaitiklių numerį.

- Jeigu įdiegėte turtui rankiniu būdu naują skaitiklį, turite užregistruoti pakeitimus turtui skiltyje **Turto skaitikliai**. Po to, turite sukurti dvi registravimo eilutes, kurių laiko žymės sutampa, ir eilutėje, kurioje yra naujas skaitiklis, pasirinkti žymės langelį **Skaitiklio atkūrimas**. Kai sukuriate dvi registravimo eilutes, pirmoje eilutėje turi būti skaitiklis, kurį keičiate. Lauke **Iš viso** bendras skaitiklių skaičius yra visų to skaitiklio tipo užregistruotų reikšmių bendra skaitiklių suma.  
- Jei pasirinktas laukas **Skaitiklio atkūrimas**, naudojant priežiūros planą, kuriame yra intervalų tipas Pradėjus nuo... arba Pasiekus..., skaitiklis tebėra aktyvus naujoje skaitiklio eilutėje, nes sukuriate atskirą skaitiklio eilutę ir pradedate naujai numeruoti skaitiklius.

![1 pav.](media/11-work-orders.png)


Jei jums reikia registruoti skaitiklį keliems ištekliams, tai galite atlikti pasirinkus **Turto valdymas** > **Užklausos** > **Turtas** > **Turto skaitikliai.**

>[!NOTE]
>Galite nustatyti intervalą, kad būtų apibrėžti nuokrypiai, kurie atsiranda rankiniu būdu registruojant skaitiklius, ir pranešimo tipas, kuris turi būti rodomas, jei registruojant nukrypstama nuo nurodyto intervalo. Dėl skaitiklių sąrankos žr. temoje [Skaitikliai](../setup-for-objects/counters.md).
