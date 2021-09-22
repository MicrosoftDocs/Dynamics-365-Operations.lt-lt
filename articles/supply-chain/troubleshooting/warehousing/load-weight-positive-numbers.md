---
title: Krovinio svorį gali sudaryti tik teigiami skaičiai
description: Apdorodami darbą tarp vietų, galite gauti klaidą dėl krovinio svorio ir jūsų atnaujinimo atšaukimo. Atlikite šiuos veiksmus, kad ištaisytumėte klaidą.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477080"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Krovinio svorio klaida ir atnaujinimas atšauktas apdorojant darbą tarp vietų

## <a name="symptoms"></a>Požymiai

Jei yra atviras darbas jums tvarkant darbą iš paketų vietų į parengimo vietas arba iš parengimo vietų į dokų vietas, galite gauti tokį klaidos pranešimą:

> Laukelis 'Krovinio svoris'(=-%1) gali turėti tik teigiamus skaičius. Atnaujinimas atšauktas.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti šią problemą, eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenų bazė \> Nuoseklumos tikrinimas** ir vykdykite procesą **Sandėlio krovinio svorio nuoseklumo tikrinimas**.
