---
title: Įtraukti faktinę vertę
description: Puslapio Prekių modelių grupės „FastTab‟ skirtuko Atsargų modelis žymės langelis Įtraukti faktinę vertę naudojamas nurodyti, ar, skaičiuojant prekės einamąją vidutinę savikainą, atsižvelgiama į faktiškai atnaujintas operacijas.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6e70a40b15bf08d88958cbf3ee3e82ed63e7a48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433572"
---
# <a name="include-physical-value"></a>Įtraukti faktinę vertę

[!include [banner](../includes/banner.md)]

Puslapio Prekių modelių grupės „FastTab‟ skirtuko Atsargų modelis žymės langelis Įtraukti faktinę vertę naudojamas nurodyti, ar, skaičiuojant prekės einamąją vidutinę savikainą, atsižvelgiama į faktiškai atnaujintas operacijas.

Žymės langelyje **Įtraukti faktinę vertę** yra tolesnės reikšmės.

| Vertė    | Rezultatas                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Pasirinkta | Savikainai apskaičiuoti naudojamos tiek fiziškai, tiek finansiškai atnaujintos operacijos. |
| Apmokėta  | Skaičiuoti einamajai vidutinei savikainai naudojamos tik finansiškai atnaujintos operacijos.                                     |

Žymės langelio poveikis šiek tiek skiriasi – jis priklauso nuo jūsų naudojamo atsargų modelio.

-   Jei, naudodami atsargų modelį FIFO (pirmiausiai gaunama, pirmiausiai išduodama), LIFO (vėliausiai gaunama, pirmiausiai išduodama) arba LIFO data, pasirenkate žymės langelį **Įtraukti faktinę vertę**, uždarant atsargas taip pat pakoreguojamos faktiškai atnaujintos operacijos.
-   Jei, naudodami šiuos atsargų modelius, žymės langelio **Įtraukti faktinę vertę** nepasirenkante, uždarant atsargas sudengiamos tik finansiškai atnaujintos operacijos.
-   Kai naudojate svertinį vidurkį arba svertinio vidurkio datos atsargų modelį, atsargų uždarymas sudengia tik finansiškai atnaujintas operacijas, nesvarbu, ar pažymėjote žymės langelį **Įtraukti fizinę vertę**.

**1 pavyzdys** Pažymėjote žymės langelį **Įtraukti faktinę vertę** ir gaunate tolesnius pirkimo užsakymus.

-   Pirkimo užsakymas, kurį sudaro kiekis iš 2 už 10,00 JAV dol. savikainą, kurio važtaraštis buvo atnaujintas.
-   Pirkimo užsakymas, kurį sudaro kiekis iš 3 už 12,00 JAV dol. savikainą, kurio sąskaita buvo atnaujinta.

Šiuo atveju vidutinė vykdymo savikaina bus 11,20 JAV dol. = (2 x 10 + 3 x 12)/(2 + 3), nes fiziškai apdorotos operacijos ir finansiškai apdorotos operacijos naudojamos apskaičiuoti savikainą. 

**2 pavyzdys** Žymės langelio **Įtraukti faktinę vertę** nepažymėjote ir, nustatant prekes, savikaina yra 10,00 USD. 

-   Gaunate pirkimo užsakymą, kurio kiekis – 20, o savikaina – 12,00 USD, kurio važtaraštis atnaujintas.

Kai pardavimo užsakymas užregistruojamas, užregistruotoji savikaina yra 10,00 USD, nes į einamąją vidutinę savikainą neįtrauktos faktiškai užregistruotos operacijos. 

> [!NOTE]
> Palyginimui, jei šiam elementui pažymite žymės langelį **Įtraukti fizinę reikšmę**, kai pardavimo užsakymas yra paskelbtas, paskelbta savikaina bus 12,00 JAV dol.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]