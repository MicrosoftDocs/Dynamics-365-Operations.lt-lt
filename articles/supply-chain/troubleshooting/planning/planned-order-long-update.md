---
title: Suplanuoti užsakymai užtrunka ilgai, kai yra naujinami
description: Naujinant reikalavimo kiekį ir (arba) pristatymo datą suplanuotame užsakyme, dažniausiai užtrunka mažiausiai 30 sekundžių, kad vienas užsakymas įrašytų naujinimą
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477105"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Suplanuoti užsakymai užtrunka ilgai, kai yra naujinami

## <a name="symptoms"></a>Požymiai

Naujinant reikalavimo kiekį ir (arba) pristatymo datą suplanuotame užsakyme, dažniausiai užtrunka mažiausiai 30 sekundžių, kad vienas užsakymas įrašytų naujinimą.

## <a name="resolution"></a>Sprendimas

Ši žinoma problema su įtaisytuoju pagrindinio planavimo varikliu. Jį sukelia jį remiantis automatinis sprogimas per BOM struktūrą redagavimo metu. Ši problema pažymėta „Planning Optimization“, kurioje planavimo įrankis gali būti naujinti ir tvirtinti atitinkamus užsakymus ir kai norima, paskatinti planavimo vykdymą siekiant atnaujinti suplanuotus užsakymus po ja esančiai BOM struktūrai.

Vienas būdas skirtas pagerinti vykdymą su inkorporuotu pagrindinio planavimo varikliu yra tokia:

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Pasirinkite kelią.
1. Išplėskite **Laiko tvora dienomis** „FastTab“.
1. Nustatykite **Sprogimą** į *Taip* ir nustatykite tolesnio laukelio nustatymą į 0 (taip).

> [!NOTE]
> Toks bus ribojimas sprogimų laikotarpiui, kurie įvyko per šį pagrindinį planavimą ir vienos dienos metu.
