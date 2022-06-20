---
title: Trumpalaikės nuomos įsipareigojimo dalies perklasifikavimas
description: Šiame straipsnyje paaiškinama, kaip sukurti mėnesio žurnalo įrašą, norint perklasifikuoti nuomos įsipareigojimų dalį kaip trumpalaikio laikotarpio.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c7c3f86aa5d24e9aeed89526a4b7317699e9a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886348"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Trumpalaikės nuomos įsipareigojimo dalies perklasifikavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukurti mėnesio žurnalo įrašą, norint perklasifikuoti nuomos įsipareigojimų dalį kaip trumpalaikio laikotarpio. Kai paketiniame procese pasirinktas grafikas yra **Trumpalaikės nuomos įsipareigojimo perklasifikavimas**, sukuriamas žurnalo įrašas. Šis įrašas naudojamas dabartinei nuomos įsipareigojimo daliai užregistruoti paskutinę mėnesio dieną. Tuo pačiu metu, atšaukimo įrašas registruojamas kaip pirmą kito mėnesio dieną.

Trumpalaikė nuomos įsipareigojimo dalis rodoma įsipareigojimų amortizavimo grafike. Užregistravus žurnalo įrašą, stulpelis **Įsipareigojimo perklasifikavimo žurnalas sukurtas** tampa prieinamas, o žurnalo ID taip pat įrašomas į grafiką.

Norėdami sukurti ir užregistruoti trumpojo laikotarpio atsakomybės perklasifikavimo žurnalo įrašą, atlikite šiuos veiksmus.

1. Nueikite į **Turto nuoma \> Periodinė \> Paketinio žurnalo patvirtinimas**.
2. Dialogo lango **Paketinio žurnalo kūrimas** lauke **Pasirinkite grafiką** pasirinkite **Trumpalaikės nuomos įsipareigojimo perklasifikavimas**.
3. Lauke **Nuomos grupė** pasirinkite nuomos grupę. Arba lauke **Knygos ID** pasirinkite knygos ID.
4. Įjunkite parametrą **Registruoti**. Taip pat, jei įrašas turi būti sukurtas, bet neužregistruotas, šis parametras bus išjungtas.
5. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
