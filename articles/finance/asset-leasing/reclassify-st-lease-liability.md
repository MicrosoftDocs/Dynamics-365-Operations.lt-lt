---
title: Trumpalaikės nuomos įsipareigojimo dalies perklasifikavimas
description: Šioje temoje paaiškinama, kaip sukurti mėnesio žurnalo įrašą, siekiant perklasifikuoti nuomos įsipareigojimo dalį kaip trumpalaikį.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 21cf81ce84d91d88a800cd250fca8fd5a9c876e66f506cd366b8d61ed480ea7e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720627"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Trumpalaikės nuomos įsipareigojimo dalies perklasifikavimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukurti mėnesio žurnalo įrašą, siekiant perklasifikuoti nuomos įsipareigojimo dalį kaip trumpalaikį. Kai paketiniame procese pasirinktas grafikas yra **Trumpalaikės nuomos įsipareigojimo perklasifikavimas**, sukuriamas žurnalo įrašas. Šis įrašas naudojamas dabartinei nuomos įsipareigojimo daliai užregistruoti paskutinę mėnesio dieną. Tuo pačiu metu, atšaukimo įrašas registruojamas kaip pirmą kito mėnesio dieną.

Trumpalaikė nuomos įsipareigojimo dalis rodoma įsipareigojimų amortizavimo grafike. Užregistravus žurnalo įrašą, stulpelis **Įsipareigojimo perklasifikavimo žurnalas sukurtas** tampa prieinamas, o žurnalo ID taip pat įrašomas į grafiką.

Norėdami sukurti ir užregistruoti trumpojo laikotarpio atsakomybės perklasifikavimo žurnalo įrašą, atlikite šiuos veiksmus.

1. Nueikite į **Turto nuoma \> Periodinė \> Paketinio žurnalo patvirtinimas**.
2. Dialogo lango **Paketinio žurnalo kūrimas** lauke **Pasirinkite grafiką** pasirinkite **Trumpalaikės nuomos įsipareigojimo perklasifikavimas**.
3. Lauke **Nuomos grupė** pasirinkite nuomos grupę. Arba lauke **Knygos ID** pasirinkite knygos ID.
4. Įjunkite parametrą **Registruoti**. Taip pat, jei įrašas turi būti sukurtas, bet neužregistruotas, šis parametras bus išjungtas.
5. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
