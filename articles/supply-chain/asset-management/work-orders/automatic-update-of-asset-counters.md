---
title: Automatinis turto skaitiklių naujinimas
description: Šioje temoje aprašomas automatinis turto skaitiklių naujinimas turto valdyme.
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
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875805"
---
# <a name="automatic-update-of-asset-counters"></a>Automatinis turto skaitiklių naujinimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ankstesniame skyriuje aprašytas turto skaitiklių rankinis generavimas. Turto skaitiklių sąranka aprašyta [Skaitikliai](../setup-for-objects/counters.md).

Skaitiklio reikšmes taip pat galima automatiškai naujinti iš gamybos registracijų pagal gamybos valandas arba gamybos kiekį. Tai daroma **Naujinti turto skaitiklius**. Galite naujinti vieną arba kelis turtus į **Nuo datos** įvesdami vieną parametrą. Šis parametras nustato gamybos registracijų pradžios datą (valandas arba pagamintą kiekį) – pradžios datą, nuo kurios skaitiklio reikšmės turi būti naujintos.

Visas turtas, susijęs su ištekliais *ir* turi turto skaitiklius, kurie nustatyti, kad būtų naujinami pagal pagamintą kiekį arba gamybos valandas, bus įtrauktas į automatinį naujinimą, ir bus sukurta nauja skaitiklio reikšmė.

Naudojant gamybos kiekį, užregistruotas geras kiekis bei sugadintas kiekis yra įtraukiami į skaičių. Jei pagaminto kiekio registracijos vienetas skiriasi nuo skaitiklio vieneto, kiekis yra konvertuojamas į atitinkamą skaitiklio vienetą.

Kaip minėta pirmiau, automatiniai skaitikliai gali būti naujinami iš gamybos registracijų. Todėl turtas, kuriam norite automatiškai naujinti skaitiklius, turi būti susijęs su ištekliais (mašina). Aprašuose toliau pateikiama sąrankos ir gamybos užsakymų, kurie yra naudojami kaip turto automatinio skaitiklių naujinimo pagrindas modulyje **Turto valdymas**, apdorojimo apžvalga (modulyje **Gamybos valdymas**).

Kai pagamintas kiekis arba gamybos valandos užregistruojamos ištekliuje, galite naujinti susijusius turto skaitiklius.

1. Spustelėkite **Turto valdymas** > **Periodinis** > **Turtas** > **Naujinti turto skaitiklius**.

2. Lauke **Pradžios data** pažymėkite automatinio naujinimo pradžios datą.

>[!NOTE]
>Data šiame lauke yra vykdomo darbo data iš **Maršruto operacijos** (laukas **Gamybos valdymas** > **Užklausos ir ataskaitos** > **Gamyba** > **Maršruto operacijos** > **Fizinė data**).

3. Jei automatiniam naujinimui norite pažymėti konkretų turtą, turto tipą arba šaltinį, „FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir atlikite reikiamus pasirinkimus.

4. Jei reikia, galite nustatyti automatinio naujinimo paketinę užduotį FastTab **Vykdyti fone**.

![1 pav.](media/12-work-orders.png)

5. Spustelėkite **Gerai**. Kai automatinis turto skaitiklio naujinimas baigtas, galite matyti skaitiklio registracijas, susijusias su turtu **Turto skaitikliai** (mygtukas **Turto valdymas** > **Bendrieji dalykai** > **Turtas** > **Visas turtas** > pažymėti turtą> **Skaitikliai**).

**Turto skaitiklio suvestinė** galite peržiūrėti naujausias viso turto visų skaitiklių tipų registracijas. Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto sudėtinė reikšmė**. Rodinys labai panašus į **Turto skaitikliai**, tačiau **Turto sudėtinė reikšmė** negalite įtraukti arba redaguoti registracijų. Jis skirtas tik peržiūrai.

![2 paveikslėlis](media/13-work-orders.png)


- Tačiau skaitiklių tipams, kurie automatiškai atnaujinti, galima kurti rankines skaitiklio reikšmių registracijas. Daugiau informacijos žr. skyriuje „Turto skaitiklių rankinis naujinimas“.
- Galite nustatyti skaitiklius, susijusius su kitu skaitiklius. Tai reiškia, kad kai skaitiklis yra naujinamas, tuo pačiu metu naujinami susiję skaitikliai. Dėl susijusių skaitiklių sąrankos, žr. [Skaitikliai](../setup-for-objects/counters.md).
