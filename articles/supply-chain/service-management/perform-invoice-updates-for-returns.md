---
title: SF naujinimas grąžinimams
description: Ši funkcija palaiko organizacijų, kurios pasirenka galimybę, kad grąžinimo užsakymai ir pardavimo užsakymai būtų išrašomi tuo pačiu metu ir to paties asmens, verslo procesus.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f999dec6639183015b1be9378dc4e8ea01c9a84
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670894"
---
# <a name="perform-invoice-updates-for-returns"></a>SF naujinimas grąžinimams 

[!include [banner](../includes/banner.md)]


Grąžinimo užsakymas yra pardavimo užsakymo, kuris pažymėtas kaip grąžintas užsakymas, tipas. Todėl grąžinimo užsakymams generuoti naudojamas sąrašo puslapis **Visi pardavimo užsakymai**, o ne forma **Grąžinimo užsakymai**. Ši funkcija palaiko organizacijų, kurios pasirenka galimybę, kad grąžinimo užsakymai ir pardavimo užsakymai būtų išrašomi tuo pačiu metu ir to paties asmens, verslo procesus.

Grąžintos prekės SF suma yra neigiama, todėl ji vadinama kredito nota.

Kai nustatote paketinio vykdymo SF atnaujinimą, pardavimo užsakymo, kurio tipas **Grąžintas užsakymas**, grąžinimo eilutės būsena turi būti **Gauta**. Tai rodo, kad užsakymo važtaraštis atnaujintas.

## <a name="post-an-invoice-for-a-return-order"></a>Grąžinimo užsakymo SF registravimas

1.  Spustelėkite **Gautinos sumos** \> **Bendros** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.

2.  Pasirinkite pardavimo užsakymą, kurio lauke **Užsakymo tipas** rodoma **Grąžintas užsakymas**.

3.  Veiksmų srities skirtuke **Sąskaita faktūra** esančioje grupėje **Generuoti** spustelėkite **Sąskaita faktūra**.

4.  Skirtuke **Parametrai** pasirinkite žymės langelį **Registravimas**.

5.  Peržiūrėkite formoje pateiktą informaciją ir visus reikiamus pakeitimus.

6.  Spustelėkite **Gerai**. Kredito nota užregistruota.

## <a name="see-also"></a>Taip pat žiūrėkite

[Važtaraščių naujinimas grąžinimams](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]