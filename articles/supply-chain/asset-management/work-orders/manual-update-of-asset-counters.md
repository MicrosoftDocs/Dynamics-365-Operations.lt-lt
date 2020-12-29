---
title: Neautomatinis turto skaitiklių atnaujinimas
description: Šioje temoje aprašomas turto skaitiklių naujinimas rankiniu būdu skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433411"
---
# <a name="manual-update-of-asset-counters"></a>Neautomatinis turto skaitiklių atnaujinimas

[!include [banner](../../includes/banner.md)]



Skaitikliai naudojami norint sukurti turto registracijas, pvz., registracijas apie turto operacijos valandų skaičių arba pagaminamą kiekį.

Pasirenkamas skaitiklio tipas gali būti nustatytas perimti skaitiklio vertes. Kitaip tariant, puslapio **Skaitikliai** „FastTab” **Bendra** esanti parinktis **Perimti turto skaitiklio vertes** nustatyta į **Taip** (**Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai**). Tokiu atveju, kai sukuriate naują šio tipo skaitiklio eilutę, kiekvienas antrinis turtas, kuris naudoja tą patį skaitiklio tipą, automatiškai atnaujinamas.

Puslapyje **Visas turtas** galite turtui sukurti valandų ar dydžio skaitiklių registracijų, atsižvelgiant į jūsų turto rodmenis.

1. Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**.

2. Pasirinkite turtą, o tada veiksmų srityje, skirtuke **Turtas**, grupėje **Prevencinis**, pasirinkite **Skaitikliai**. Puslapyje **Turto skaitikliai** rodomas visų buvusių skaitiklių registracijų pasirinktam turtui sąrašas.

3. Pasirinkite **Naujas**, kad sukurtumėte registraciją. Turto ID automatiškai įvedamas lauke **Turtas**.

4. Lauke **Skaitiklis** pažymėkite susijusį skaitiklį. Galima pasirinkti tik susijusius su turto tipu, pasirinktu tam turtui, skaitiklius. Susijęs vienetas yra automatiškai įvedamas į lauką **Vienetas**.

5. Lauke **Registruota** pasirinkite skaitiklio registravimo datą ir laiką.

6. Lauke **Vertė** įveskite paskutinio skaitiklio registracijos numerį. Arba lauke **Agreguota vertė** įveskite bendrą skaitiklių skaičių.

Atkreipkite dėmesį į toliau nurodytus punktus.

- Jeigu įdiegėte turtui rankiniu būdu naują skaitiklį, turite užregistruoti pakeitimus turtui puslapyje **Turto skaitikliai**. Tada turite sukurti dvi registravimo eilutes, kuriose yra vienodos laiko žymos. Pirmoji eilutė turi būti skirta skaitikliui, kurį keičiate. Eilutėje, kuri susijusi su nauju skaitikliu, pažymėkite žymės langelį **Skaitiklio atkūrimas**. Lauke **Iš viso** bendras skaitiklių skaičius yra visų to skaitiklio tipo užregistruotų reikšmių bendra skaitiklių suma.

- Jei pasirinktas laukas **Skaitiklio atkūrimas**, naudojant priežiūros planą, kuriame yra intervalų tipas Pradėjus nuo... arba Pasiekus..., skaitiklis tebėra aktyvus naujoje skaitiklio eilutėje, nes sukuriate atskirą skaitiklio eilutę ir pradedate naujai numeruoti skaitiklius.

Toliau pateiktame paveikslėlyje parodytas puslapio **Turto skaitikliai** pavyzdys.

![1 pav.](media/11-work-orders.png)

Puslapyje **Turto skaitikliai** (**Turto valdymas** > **Užklausos** > **Turtas** > **Turto skaitikliai**) galite pagal poreikį tuo pačiu metu registruoti skaitiklius keliems ištekliams.

>[!NOTE]
>Galite nustatyti intervalą, kad nustatytumėte nuokrypius, kurie atsiranda rankiniu būdu registruojant skaitiklius. Taip pat galite nurodyti pranešimo, kuris rodomas, jei registruojant nukrypstama nuo nurodyto intervalo, tipą. Daugiau informacijos, kaip nustatyti skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).

