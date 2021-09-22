---
title: Skaičiuojant produkto konfigūracijos modelį neteisingai suapvalinti integers
description: Integruotojo rezultatai nėra visada tinkamai suapvalinti, kai produkto konfigūravimo modeliai yra skaičiuojami. Išspręskite problemą naudodami pridėtą dešimtainį atributą ir skaičiavimą.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477111"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Integruotojų savybės nėra tinkamai suapvalintos, kai produkto konfigūravimo modeliai yra skaičiuojami.

## <a name="symptoms"></a>Požymiai

Ši problema atsitinka jums atliekant tolesnes veiksmų tvarkas:

1. Nustatykite šiuos atributus gamybos konfigūravimo modelyje:

    - Įvestis (integruotojas)
    - Procentas (dešimtainis)
    - Rezultatas (integruotojas)

2. Sukurkite skaičiavimą, kuris turi tolesnes išraiškas:

    *Rezultatas* = *Įvestis* × *Procentas* ÷ 100

Tokiu atveju, integravimo rezultatas nėra visada tinkamai suapvalintas. Pavyzdžiui, jei įvestis yra 1000, o procentas yra 2,40, jūs tikitės, kad sveikojo skaičiaus vertė bus 24, nes 2,40 procentų (1000) yra 24 (arba 24,00 dešimtainė forma). Vietoje to, rodomas rezultatas yra 23. Nepaisant to, kai procentas yra 2,39, skaičiavimas yra suapvalintas iki 24, o ne 23. Kai procentas yra 2,50, skaičiavimas yra suapvalintas iki 25 kaip tikėtasi.

## <a name="cause"></a>Priežastis

Ši problema atsitinka dažnai, nes „Microsoft Solver Foundation“ pati programa turi skaičius naudodama frakcijas. Ankstesniame pavyzdyje, skaičiavimo rezultatas, kai 2,40 procentas yra rodomas kaip 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kai .NET rodo integruojamą vertę, ji grįš 23.

## <a name="resolution"></a>Sprendimas

Šis elgesys nepasikeis, nes kiti scenarijai nuo jo priklauso. Ankstesniame pavyzdyje, galite ištaisyti problemą įvesdami papildomus dešimtainius atributus ir skaičiavimai.

Pavyzdžiui, galite nustatyti tolesnius atributus gamybos konfigūravimo modelyje:

- Įvestis (integruotojas)
- Procentas (dešimtainis)
- Dešimtainis rezultatas (dešimtainis)
- Rezultato integruotojas (integruotojas)

Tuomet galite įtraukti tolesnius apskaičiavimus:

- *Dešimtainis rezultatas* = *Įvestis* × *Procentas* ÷ 100
- *Rezultato integruotojas* = *Dešimtainis rezultatas*
