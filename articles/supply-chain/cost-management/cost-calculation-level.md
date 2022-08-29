---
title: Išlaidų skaičiavimo lygis
description: Šiame straipsnyje aprašomas komplektavimo specifikacijos (KS) lygis, pavadintas Išlaidų skaičiavimo lygis. Į šio KS lygio skaičiavimus neįtraukti gamybos ir paketiniai užsakymai.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334962"
---
# <a name="cost-calculation-level"></a>Išlaidų skaičiavimo lygis

[!include [banner](../includes/banner.md)]

Į komplektavimo specifikacijos (KS) lygio, vadinamo **Išlaidų skaičiavimo lygiu**, skaičiavimus neįtraukti gamybos užsakymai ir paketiniai užsakymai. Sistema naudoja šį lygį, kai atlieka išlaidų skaičiavimus įkainojimo versijose. Tokiuose procesuose, kaip perskaičiavimas ir atsargų uždarymas, sistema naudoja KS lygį **Įkainojimo lygis**.

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>Įjungti arba išjungti išlaidų skaičiavimo lygio funkciją

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai šią funkciją gali įjungti arba išjungti ieškodami išlaidų *skaičiavimo lygio funkcijos* funkcijų [valdymo darbo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

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