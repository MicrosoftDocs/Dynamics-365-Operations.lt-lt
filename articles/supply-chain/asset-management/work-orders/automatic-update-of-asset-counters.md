---
title: Automatinis turto skaitiklių naujinimas
description: Šioje temoje aprašomas automatinis turto skaitiklių naujinimas turto valdyme.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3e8619439545cf3ea42f84a6dd7ee6ffdf1026e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021935"
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

    ![1 pav.](media/12-work-orders.png)

5. Pasirinkite **Gerai**. 

Baigus automatinį turto skaitiklio naujinimą, puslapyje **Turto skaitikliai** galite peržiūrėti su turtu susijusias skaitiklio registracijas. Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**, pasirinkite turtą, o tada veiksmų srityje, skirtuke **Turtas**, grupėje **Profilaktinė** pasirinkite **Skaitikliai**.

Puslapyje **Turto sudėtinė reikšmė** galite peržiūrėti naujausias viso turto visų skaitiklių tipų registracijas. Pasirinkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto sudėtinė reikšmė**. Šis puslapis primena puslapį **Turto skaitikliai**, bet čia negalima pridėti arba redaguoti registracijų. Jis skirtas tik peržiūrai.

Toliau pateiktame paveikslėlyje parodytas puslapio **Turto sudėtinė reikšmė** pavyzdys.

![2 pav.](media/13-work-orders.png)

Atkreipkite dėmesį į toliau nurodytus punktus.

- Tačiau skaitiklių tipams, kurie yra automatiškai atnaujinami, galite kurti rankines skaitiklio reikšmių registracijas. Daugiau informacijos žr. [Neautomatinis turto skaitiklių atnaujinimas](../work-orders/manual-update-of-asset-counters.md).

- Galite nustatyti skaitiklius, susietus su kitu skaitikliu. Šiuo atveju, atnaujinus skaitiklį, tuo pačiu metu automatiškai atnaujinami susiję skaitikliai. Daugiau informacijos, kaip nustatyti susijusius skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]