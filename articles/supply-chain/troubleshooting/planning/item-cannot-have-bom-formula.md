---
title: Prekė negali turėti KS arba formulės
description: Kai bandote patvirtinti užsakymą, prekės patikrinimo metu gaunate klaidos pranešimą. Jame teigiama, kad prekė negali turėti komplektavimo specifikacijos (KS) ar formulės.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730111"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Prekė negali turėti KS arba formulės

Klaidos kodas: PRO2614

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti užsakymą, prekės patikrinimo metu gaunate tokį klaidos pranešimą:

> Prekė negali turėti KS arba formulės

## <a name="resolution"></a>Sprendimas

Prekės, kurios turi komplektavimo specifikaciją (KS) arba formulę, privalo būti *Planavimo prekės*, *KS* arba *formulės* tipo. Norėdami pakeisti prekės tipą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite atitinkamą produktą.
1. „FastTab“ **Inžinierius** nustatykite lauką **Produkto tipas** į *Planavimo prekė*, *KS* arba *formulė*.
