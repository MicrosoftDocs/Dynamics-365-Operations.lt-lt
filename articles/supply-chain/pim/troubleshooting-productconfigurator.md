---
title: Produkto konfigūratoriaus trikties šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto konfigūratoriumi.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
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
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d17d9f16f01a68da724751273b7d137a0f0f14de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248768"
---
# <a name="troubleshoot-the-product-configurator"></a>Produkto konfigūratoriaus trikties šalinimas

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto konfigūratoriumi.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Prekės tekstas yra užrašomas man konfigūruojant produktą prekybos užsakymo eilutėje.

### <a name="issue-description"></a>Problemos aprašas

Ši klaida įvyksta jums kuriant prekybos užsakymo eilutę konfigūruojamoje prekėje ir tuomet keičiant prekės tekstą. Jums konfigūruojant prekę ir tada pasirenktant **Gerai**, tekstas yra užrašomas standartiniu tekstu.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Tikimasi tokio elgesio. Teksto laukelis apima varianto pavadinimą, kuris užpildomas tik po to kai sukonfigūruojate eilutę. Dėl to, privalote keisti tekstą jums sukonfigūravus eilutę, o ne prieš tai.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Integruotojo savybės nėra tinkamai suapvalintos, kai produkto konfigūravimo modeliai yra skaičiuojami.

### <a name="issue-description"></a>Problemos aprašas

Ši problema atsitinka jums atliekant tolesnes veiksmų tvarkas:

1. Nustatykite tolesnius atributus gamybos konfigūravimo modelyje:

    - Įvestis (integruotojas)
    - Procentas (dešimtainis)
    - Rezultatas (integruotojas)

2. Sukurkite skaičiavimą, kuris turi tolesnes išraiškas:

    *Rezultatas* = *Įvestis* × *Procentas* ÷ 100

Tokiu atveju, integravimo rezultatas nėra visada tinkamai suapvalintas. Pavyzdžiui, įvestis yra 1 000, o procentas yra 2,40. Dėl to, tikitės integravimo rezultatų 24, nes 2,40 procentas 1 000 yra 24 (ar 24,00 dešimtaine forma). Vietoje to, rodomas rezultatas yra 23. Nepaisant to, kai procentas yra 2,39, skaičiavimas yra suapvalintas iki 24, o ne 23. Kai procentas yra 2,50, skaičiavimas yra suapvalintas iki 25 kaip tikėtasi.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši problema atsitinka dažnai, nes „Microsoft Solver Foundation“ pati programa turi skaičius naudodama frakcijas. Ankstesniame pavyzdyje, skaičiavimo rezultatas, kai 2,40 procentas yra rodomas kaip 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kai .NET rodo integruojamą vertę, ji grįš 23.

Šis elgesys nepasikeis, nes kiti scenarijai nuo jo priklauso. Ankstesniame pavyzdyje, galite ištaisyti problemą įvesdami papildomus dešimtainius atributus ir skaičiavimą.

Pavyzdžiui, galite nustatyti tolesnius atributus gamybos konfigūravimo modelyje:

- Įvestis (integruotojas)
- Procentas (dešimtainis)
- Dešimtainis rezultatas (dešimtainis)
- Rezultato integruotojas (integruotojas)

Tuomet galite įtraukti tolesnius apskaičiavimus:

- *Dešimtainis rezultatas* = *Įvestis* × *Procentas* ÷ 100
- *Rezultato integruotojas* = *Dešimtainis rezultatas*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]