---
title: Automatinis turto skaitiklių atnaujinimas
description: Šiame straipsnyje aprašomas automatinis turto valdymo turto skaitiklių atnaujinimas.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8ea84259eb8f12becdcf008ed9222a44b2626a0d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016223"
---
# <a name="automatic-update-of-asset-counters"></a>Automatinis turto skaitiklių atnaujinimas

[!include [banner](../../includes/banner.md)]

Informacijos apie turto skaitiklių registravimą neautomatiniu būdu žr. [Neautomatinis turto skaitiklių atnaujinimas](../work-orders/manual-update-of-asset-counters.md). Informacijos, kaip nustatyti turto skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).

Skaitiklio reikšmes taip pat galima automatiškai naujinti iš gamybos registracijų pagal gamybos valandas arba gamybos kiekį (t. y. pagamintą kiekį). Šis naujinimas atliekamas puslapyje **Naujinti turto skaitiklius**. Vieną arba kelis turtus galite atnaujinti nustatydami vieną parametrą **Pradžios data**. Šis parametras nurodo gamybos registracijų (gamybos valandų arba gamybos kiekių) pradžios datą. Kitaip tariant, jis nurodo datą, nuo kada reikia atnaujinti skaitiklio vertes.

Visas turtas, susijęs su ištekliumi *ir* turintis turto skaitiklius, kurie nustatyti, kad būtų naujinami pagal gamybos valandas ar arba gamybos kiekį, bus įtrauktas į automatinį naujinimą. Bus sukurtos naujos skaitiklio vertės.

Skaitikliams, kurie pagrįsti gamybos kiekiu, skaičius apima ir geros kokybės prekes, ir užregistruotus kiekius su klaidomis. Jei gamybos kiekio registravimui naudotas vienetas skiriasi nuo skaitiklio naudojamo vieneto, kiekis yra konvertuojamas, kad atitiktų skaitiklio vienetą.

Kaip minėta pirmiau, automatiniai skaitikliai gali būti naujinami iš gamybos registracijų. Todėl turtas, kuriam norite automatiškai naujinti skaitiklius, turi būti susijęs su ištekliais (mašina). Kai pagamintas kiekis arba gamybos valandos užregistruojamos ištekliuje, galite naujinti susijusius turto skaitiklius.

1. Pasirinkite **Turto valdymas** > **Periodinis** > **Turtas** > **Naujinti turto skaitiklius**.

2. Lauke **Pradžios data** pasirinkite automatinio naujinimo pradžios datą.

    >[!NOTE]
    >Data šiame lauke yra vykdomo darbo data iš **Maršruto operacijos** (laukas **Gamybos valdymas** > **Užklausos ir ataskaitos** > **Gamyba** > **Maršruto operacijos** > **Fizinė data**).

3. „FastTab“ **Įtrauktini įrašai** galite pasirinkti konkretų turtą,turto tipą ar išteklius automatiniam naujinimui. Pasirinkite **Filtras** ir atlikite reikiamus pasirinkimus.

4. FastTab **Vykdyti fone** pagal poreikį galite nustatyti automatinio naujinimo paketinę užduotį.

    Toliau pateiktame paveikslėlyje parodytas dialogo lango **Naujinti turto skaitiklius** pavyzdys.

    ![1 iliustracija.](media/12-work-orders.png)

5. Pasirinkite **Gerai**. 

Baigus automatinį turto skaitiklio naujinimą, puslapyje **Turto skaitikliai** galite peržiūrėti su turtu susijusias skaitiklio registracijas. Pasirinkite **Turto valdymo** > **turtas** > **Visas** turtas, pasirinkite turtą, tada veiksmų srityje, **skirtuke** Turtas, **grupėje** Prevencinė grupė, pasirinkite **Skaitikliai.**

Puslapyje **Turto sudėtinė reikšmė** galite peržiūrėti naujausias viso turto visų skaitiklių tipų registracijas. Pasirinkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto sudėtinė reikšmė**. Šis puslapis primena puslapį **Turto skaitikliai**, bet čia negalima pridėti arba redaguoti registracijų. Jis skirtas tik peržiūrai.

Toliau pateiktame paveikslėlyje parodytas puslapio **Turto sudėtinė reikšmė** pavyzdys.

![2 iliustracija.](media/13-work-orders.png)

Atkreipkite dėmesį į toliau nurodytus punktus.

- Tačiau skaitiklių tipams, kurie yra automatiškai atnaujinami, galite kurti rankines skaitiklio reikšmių registracijas. Daugiau informacijos žr. [Neautomatinis turto skaitiklių atnaujinimas](../work-orders/manual-update-of-asset-counters.md).

- Galite nustatyti skaitiklius, susietus su kitu skaitikliu. Šiuo atveju, atnaujinus skaitiklį, tuo pačiu metu automatiškai atnaujinami susiję skaitikliai. Daugiau informacijos, kaip nustatyti susijusius skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]