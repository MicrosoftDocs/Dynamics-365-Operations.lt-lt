---
title: Atsargų kiekis neatnaujinamas dėl nepakankamų operacijų
description: Inventoriaus kiekis -1% negali būti naujinamas, nes nėra pakankamai inventoriaus operacijų prekei %2, kuri turi specialias dimensijas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477043"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Sistema negali atnaujinti atsargų kiekio dėl nepakankamų operacijų

## <a name="symptoms"></a>Požymiai

Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis. Gausite tolesnį klaidos pranešimą:

> Inventoriaus kiekis -%1 negali būti naujinamas dėl nepakankamų inventoriaus perlaidų prekei %2 su matmenimis Dydis=%3, Spalva=%4, Prieda=%5, Saitas=%6, Sandėlis=%7, Vieta=%8, Inventoriaus būsena=Prieinamas, Licensijos plokštelė=%9, Palaido kiekio numeris=%10 ataskaitos ID %11 partijos ID %12.

## <a name="resolution"></a>Sprendimas

Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį. Pavyzdžiui, šios perlaidos gali atverti kiekio užsakymus, inventoriaus blokavimo įrašus ar išvesties užsakymus.
