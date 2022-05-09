---
title: Lygiavimo datos scenarijai
description: Šioje temoje pateikiami pavyzdžiai, kurie parodo, kaip veikia lygiavimo datos abonementinio sąskaitų pateikimo metu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e80797e8dd532bb4b2ef78422b459487430d83d6
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629714"
---
# <a name="alignment-date-scenarios"></a>Lygiavimo datos scenarijai

Šioje temoje pateikiami pavyzdžiai, kurie parodo, kaip veikia lygiavimo datos abonementinio sąskaitų pateikimo metu.

Šiuose pavyzdžiuose informacijos apie atsiskaitymo grafiką data yra 2019 m. spalio 31 d. Pirmoji eilutės atsiskaitymo informacija baigiasi 2019 m. spalio 31 d. ir yra atitinkamai pateikiama. Eilutė bus automatiškai atnaujinta naudojant lapkričio 11 d. atnaujinimo pradžios datą.

> [!NOTE]
> Metai tinka, nes dėl to lygiuotės data gali būti daugiau arba mažesnė už metus. Šiuose pavyzdžiuose pakartojimo metodas nustatytas kaip Mėnesinis **periodinio** **sutarties atsiskaitymo parametrų** puslapyje. Jei nustatyta kaip Kasdienis, kai **kurios dalinės sumos skirsis**.

## <a name="scenario-1-no-alignment"></a>1 scenarijus: nėra lygiuotės

Atsiskaitymo grafike nustatyti šie duomenys:

- **Pradžios data:** 2019 m. gegužės 1 d.
- **Pabaigos data:** 2024 m. gruodžio 31 d.
- **Suma:** $1,000

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 2020-04-30 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>2 scenarijus: sutrumpinta lygiuotė

Atsiskaitymo grafike nustatyti šie duomenys:

- **Pradžios data:** 2019 m. gegužės 1 d.
- **Pabaigos data:** 2024 m. gruodžio 31 d.
- **Suma:** $1,000
- **Lygiavimo data:** 2019 m. gruodžio 31 d.

Pirmoji atnaujinimo suma skirta mažiau nei vienais metais.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 2020-01-01 | 2020-12-31 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 2022-01-01 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>3 scenarijus: išplėstinė lygiuotė

Atsiskaitymo grafike nustatyti šie duomenys:

- **Pradžios data:** 2019 m. gegužės 1 d.
- **Pabaigos data:** 2024 m. gruodžio 31 d.
- **Suma:** $1,000
- **Lygiavimo data:** 2020 m. gruodžio 31 d.

Pirmoji atnaujinimo suma skirta daugiau nei vienais metais.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 2020-12-31 | | | 1.00 | | 1.00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 2022-01-01 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>4 scenarijus: lygiavimas su kitu pabaigos mėnesiu

Atsiskaitymo grafike nustatyti šie duomenys:

- **Pradžios data:** 2019 m. gegužės 1 d.
- **Pabaigos data:** 2024 m. spalio 31 d.
- **Suma:** $1,000
- **Lygiavimo data:** 2019 m. gruodžio 31 d.

> [!NOTE]
> Šis scenarijus nėra įprastas.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 2020-01-01 | 2020-12-31 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 2022-01-01 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>5 scenarijus: vienas dalinis metai

Atsiskaitymo grafike nustatyti šie duomenys:

- **Pradžios data:** 2019 m. gegužės 1 d.
- **Pabaigos data:** 2019 m. gruodžio 31 d.
- **Suma:** $1,000
- **Lygiavimo** data: 2019 m. gruodžio 31 d.

Šiame scenarijuje lygiuotės datos nereikia. Šis scenarijus įprastas automatiniam atnaujinimui.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>6 scenarijus: apskaičiuotos datos

Palaikymas ir atnaujinimas nustatytas su šiais duomenimis:

- **Nepaisyti pradžios datos:** Ne
- **Palaikymo ir atnaujinimo pradžios datos:** kito mėnesio pradžia
- **SF registravimo data:** 2019 m. birželio 22 d.
- **Lygiavimo data:** 2020 m. gruodžio 31 d.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1.00 | | 1.00 | 297.60 |
| 8/1/2019 | 2020-12-31 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>7 scenarijus: apskaičiuotos datos ir būsimas registravimas

Palaikymas ir atnaujinimas nustatytas su šiais duomenimis:

- **Nepaisyti pradžios datos:** Ne
- **Palaikymo ir atnaujinimo pradžios datos:** kito mėnesio pradžia
- **SF registravimo data:** 2019 m. birželio 22 d.
- **Lygiavimo data:** 2020 m. gruodžio 31 d.

Šiame scenarijuje lygiavimo data pakeičiama į 2021 m. gruodžio 31 d.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 8/1/2019 | 2020-12-31 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>8 scenarijus: neautomatinės datos ir keli metai

Palaikymas ir atnaujinimas nustatytas su šiais duomenimis:

- **Nepaisyti pradžios datos:** Taip
- **Atnaujinimo pradžios data:** 2020 m. liepos 1 d.
- **Atnaujinimo pabaigos data:** 2024 m. gruodžio 31 d.
- **Lygiuoimo data:** 2021 m. gruodžio 31 d.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 2022-01-01 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>9 scenarijus: neautomatinės datos, keli metai ir kitas pabaigos mėnuo

Palaikymas ir atnaujinimas nustatytas su šiais duomenimis:

- **Nepaisyti pradžios datos:** Taip
- **Atnaujinimo pradžios data:** 2020 m. liepos 1 d.
- **Atnaujinimo pabaigos data:** 2024 m. spalio 31 d.
- **Lygiuoimo data:** 2021 m. gruodžio 31 d.

| Atsiskaitymo pradžios data | Atsiskaitymo pabaigos data | Ankstesnis rodmuo | Dabartinis rodmuo | Įvestas kiekis | Nemokamas kiekis | Apmokėtinas kiekis | Vnt. kaina |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 2022-01-01 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>10 scenarijus: lygiavimas be paai kai

Palaikymas ir atnaujinimas nustatytas su šiais duomenimis:

- **Nepaisyti pradžios datos:** Ne
- **SF registravimo data:** 2019 m. birželio 22 d.
- **Lygiavimo data:** 2019 m. gruodžio 31 d.

Atnaujinimo pradžios ir lygiavimo datos yra koreguojamos taip, kad abi pradžios datos būtų po registravimo datos.

- **Atnaujinimo pradžios data:** 2020 m. sausio 1 d.
- **Atnaujinimo pabaigos data:** 2020 m. gruodžio 31 d.
