---
title: Negalima rezervuoti atsargų, nes yra 0,00
description: Gaunate klaidą, per kurią sistema negali rezervuoti, nes atsargose yra tik 0,00. Šią klaidą greičiausiai sukelia atviras darbas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477123"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Sistema negali rezervuoti dėl 0,00 prieinamo atsargoje

## <a name="symptoms"></a>Požymiai

Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis. Gausite tolesnį klaidos pranešimą:

> Fiziškai turima Saitas=%1, Sandėlis=%2, Inventoriaus būsena=Prieinama, Palaido kiekio numeris=%3, Savininkas=%4: %5 negalima rezervuoti, nes tik 0.00 yra prieinama inventoriuje.

## <a name="resolution"></a>Sprendimas

Šią klaidą greičiausiai sukelia atviras darbas. Pabaikite darbą arba gaukite nesukūrę darbo. Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį. Pavyzdžiui, šios perlaidos gali būti atviri kiekio užsakymai, inventoriaus blokavimo įrašai ar išvesties užsakymai.
