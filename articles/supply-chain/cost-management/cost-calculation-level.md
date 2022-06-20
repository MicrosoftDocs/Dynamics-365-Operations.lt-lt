---
title: Išlaidų skaičiavimo lygis
description: Šiame straipsnyje aprašomas komplektavimo specifikacijos (KS) lygis, pavadintas Išlaidų skaičiavimo lygis. Į šio KS lygio skaičiavimus neįtraukti gamybos ir paketiniai užsakymai.
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 647ef4b13b864cfdbb7905fe7a0d340e85f6c1e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850879"
---
# <a name="cost-calculation-level"></a>Išlaidų skaičiavimo lygis

[!include [banner](../includes/banner.md)]

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