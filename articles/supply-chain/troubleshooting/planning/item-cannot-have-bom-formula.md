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
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294137"
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
