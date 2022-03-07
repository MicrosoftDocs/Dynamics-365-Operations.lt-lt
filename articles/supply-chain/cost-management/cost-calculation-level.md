---
title: Išlaidų skaičiavimo lygis
description: Šioje temoje aprašomas komplektavimo specifikacijų (KS) lygis, kuris pavadintas išlaidų skaičiavimo lygiu. Į šio KS lygio skaičiavimus neįtraukti gamybos ir paketiniai užsakymai.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 41f2550ff22b838aa5d85022582fd9715917fe462aa34dbfc833941f5ada3325
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717395"
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