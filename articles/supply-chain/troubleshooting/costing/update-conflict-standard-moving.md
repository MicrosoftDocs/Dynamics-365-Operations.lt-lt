---
title: Atnaujinimo nesuderinamumas įvyksta, kai įprastas vertinimo metodas yra Standartinė savikaina arba Slankusis vidurkis
description: Atnaujinimo nesuderinamumas įvyksta, kai atsargų vertinimo metodas yra įprasta savikaina arba perkėlimo vidurkis
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477122"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Atnaujinimo nesuderinamumas įvyksta, kai atsargų vertinimo metodas yra įprasta savikaina arba perkėlimo vidurkis

## <a name="symptoms"></a>Požymiai

Kai lygiagrečiai registruojate dokumentus, pvz., atsargų žurnalus, pirkimų užsakymų ir pardavimų užsakymų sąskaitas faktūras, norėdami lengviau pritaikyti ir pasiekti geresnį našumą, galite gauti klaidos pranešimą apie įvykusį atnaujinimo nesuderinamumą ir kai kurie dokumentai gali būti nepaskelbti. Ši klaida gali įvykti, kai atsargų vertinimo metodas yra *Standartinė savikaina* arba *Slankusis vidurkis*. Abu šie metodai yra nuolatiniai įkainojimo metodai. Kitaip tariant, galutinės išlaidos nustatomos registravimo metu.

Jei naudojate *Slankusis vidurkis* metodą, klaidos pranešimas gali būti toks:

> Atsargų vertė xx.xx nėra numatyta atlikus proporcinį išlaidų skaičiavimą

Jei naudojate *Standartinė savikaina* metodą, klaidos pranešimas gali būti toks:

> Standartiniai kaštai neatitinka su finansine inventoriaus verte po naujinimo. Vertė = xx.xx, kiekis = yy.yy, standartinė savikaina = zz.zz

## <a name="workaround"></a>Apėjimo būdas

Kol „Microsoft” išleis problemos sprendimą, apsvarstykite galimybę naudoti toliau nurodytus problemos sprendimus, kad išvengtumėte arba sumažintumėte šias klaidas:

- Iš naujo paskelbkite neįvykdytus dokumentus.
- Kurkite dokumentus, turinčius mažiau eilučių.
- Venkite naudoti dešimtaines standartinėje kainoje. Bandykite apibrėžti standartinę savikainą, kad laukas **Kainos kiekis** nustatytas *1*. Jei reikia nurodyti **Kainos kiekis** vertę, didesnę nei *1*, pabandykite sumažinti dešimtainių skaičių vieneto standartinėje savikainoje. (Būtų geriausia, jei būtų mažiau nei du dešimtainiai skaičiai.) Pavyzdžiui, venkite apibrėžti standartinės savikainos nustatymus, pavyzdžiui,  **Kaina** = *10* ir **Kainos kiekis** = *3*, nes jie sukurs 3,333333 vieneto standartinę kainą (kai dešimtainio skaičiaus vertė kartojasi).
- Daugelyje dokumentuose venkite naudoti kelias eilutes, turinčias tą pačią produkto kombinaciją ir finansines atsargų dimensijas.
- Sumažinkite paralelizavimo laipsnį. (Šiuo atveju jūsų sistema gali tapti spartesnė, nes atsiranda mažiau atnaujinimo nesuderinamumų ir atsiranda pakartotinių bandymų.)
