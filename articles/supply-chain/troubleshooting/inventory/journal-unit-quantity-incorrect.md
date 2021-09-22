---
title: Vienetas ir vienetų kiekis atsargų žurnale veikia netinkamai
description: Vienetas ir vienetų kiekis atsargų žurnale veikia netinkamai
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477073"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Vienetas ir vienetų kiekis atsargų žurnale veikia netinkamai

## <a name="symptoms"></a>Požymiai

Kai dirbate su atsargų žurnalo vienetais ir kiekiais atsargų žurnale, galite susidurti su viena ar abiem problemomis.

- Nematote vienetų arba vienetų kiekių atsargų žurnale, kol vienetų konvertavimas nustatytas išleistam produktui, ir negalite pakeisti vieneto atsargų žurnale.
- Matote **Kiekis** ir **Vienetas** laukus atsargų žurnale, bet nematote lauko **Vieneto kiekis**. Jei pakeisite vienetą, įvesite kiekį ir užregistruosite žurnalą, žurnale vis tiek bus rodomas pradinis to kiekio matavimo vienetas.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti šią problemą, vykdykite šiuos veiksmus.

1. Darbo eigoje **Funkcijų valdymas** įsitikinkite, kad funkcija *Matavimo vienetų ir vienetų kiekio naudojimas atsargų žurnaluose* yra įjungta. Ši funkcija prideda laukus **Vienetas** ir **Vieneto kiekis** į žurnalą.
1. Įjungus šią funkciją, naudokite laukus **Kiekis**, **Vieneto kiekis** ir **Vienetas** laukus tokiu būdu:

    - **Kiekis** – nurodykite kiekį, naudodami numatytąjį vienetą, nurodytą išleistam produktui. Tačiau numatytasis vienetas čia nerodomas. Jei konvertavimas nustatytas tarp numatytojo vieneto ir vieneto, pasirinkto lauke **Vienetas**, laukas **Kiekis** yra automatiškai atnaujinimas pagal pasirinkimus laukuose **Vieneto kiekis** ir **Vienetas**.
    - **Vieneto kiekis** – nurodykite kiekį naudodami kiekį, pasirinktą lauke **Vienetas**.
    - **Vienetas** – pasirinkite vienetą, kurį norite taikyti vertei lauke **Vieneto kiekis**.
