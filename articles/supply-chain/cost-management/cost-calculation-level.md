---
title: Išlaidų skaičiavimo lygis
description: Šioje temoje aprašomas komplektavimo specifikacijų (KS) lygis, kuris pavadintas išlaidų skaičiavimo lygiu. Į šio KS lygio skaičiavimus neįtraukti gamybos ir paketiniai užsakymai.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251031"
---
# <a name="cost-calculation-level"></a>Išlaidų skaičiavimo lygis

Į komplektavimo specifikacijos (KS) lygio, vadinamo **Išlaidų skaičiavimo lygiu**, skaičiavimus neįtraukti gamybos užsakymai ir paketiniai užsakymai. Sistema naudoja šį lygį, kai atlieka išlaidų skaičiavimus įkainojimo versijose. Tokiuose procesuose, kaip perskaičiavimas ir atsargų uždarymas, sistema naudoja KS lygį **Įkainojimo lygis**.

Toliau pateiktas paprastas scenarijus parodo skirtumus tarp KS lygio **Išlaidų skaičiavimo lygis** ir KS lygio **Įkainojimo lygis**.

Turite tris produktus: A, B ir C. C produktas yra B produkto komponentas, o B produktas – A produkto komponentas.

- **Įkainojimo lygis** priskiria šiuos KS lygius:

    - **A produktas:** 0
    - **B produktas:** 1
    - **C produktas:** 2

- **Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:

    - **A produktas:** 0
    - **B produktas:** 1
    - **C produktas:** 2

Tada sukuriamas C produkto gamybos užsakymas, o A produktas įtraukiamas į gamybos užsakymo KS. Įvertinus užsakymą, KS lygiai atnaujinami, kaip nurodyta toliau:

- **Įkainojimo lygis** priskiria šiuos KS lygius:

    - **B produktas:** 1
    - **C produktas:** 2
    - **A produktas:** 3

- **Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:

    - **A produktas:** 0
    - **B produktas:** 1
    - **C produktas:** 2

Taip užtikrinama, kad gamybos užsakymo KS pakeitimai neturėtų įtakos būsimiems išlaidų skaičiavimams.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]