---
title: Kiekio mažinti negalima atšaukus pardavimo užsakymą
description: Kiekio mažinti negalima atšaukus pardavimo užsakymą.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230841"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Kiekio mažinti negalima atšaukus pardavimo užsakymą

Klaidos kodas: SYS138831

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Kiekio negalima sumažinti. Užsakytas atsargų operacijų kiekis per mažas, nes kiekį arba jo dalį nurodo išeigos užsakymas arba gamybos užsakymas arba jis yra pažymėtas pagal kitas operacijas.

## <a name="cause"></a>Priežastis

Jei darbas susietas su pardavimo užsakymu, negalite atšaukti pardavimo užsakymo, kol darbas nebus atšauktas. Šis reikalavimas taikomas, net jei darbas, susietas su pardavimo užsakymu, yra uždarytas.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

1. Atšaukti atidarytą darbą.
1. Panaikinkite krovinį.
1. Paimto kiekio sumažinimas.

### <a name="cancel-open-work"></a>Atšaukti atidarytą darbą

Norėdami atidaryti darbą, atlikite šiuos žingsnius.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Laukelyje **Darbo ID** nurodykite darbo ID, kurį norite atšaukti ir tai, kad dabar **Darbo būsenos** vertė *Atidaryta*, *Vykdoma*, *Atšaukta*, *Kombinuota* ar *Uždaryta*.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.

### <a name="delete-the-load"></a>Panaikinkite krovinį

Norėdami panaikinti krovinį, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Atidarykite reikalingą pardavimo užsakymą.
1. „FastTab“ **Pardavimo užsakymo eilutės** rinkitės **Sandėlis \> Darbo informacija**.
1. Puslapyje **Darbas** veiksmų juostoje, skirtuke **Darbas** grupėje **Darbas** rinkitės **Atšaukti darbą**.
1. Patvirtinkite, kad **Darbo būsena** nustatyta į *Atšaukta*.
1. Uždarykite puslapį **Darbas**.
1. Išsamios pardavimo užsakymo informacijos puslapio **pardavimo užsakymo eilučių** „FastTab“, pasirinkite **Sandėlio \> krovinio informacija**.
1. Rinkitės **Naikinti** veiksmų juostoje.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite naikinti krovinį.
1. Uždarykite puslapį **Krovinys**.

### <a name="reduce-the-picked-quantity"></a>Paimto kiekio sumažinimas

Kai visas darbas atšauktas, atlikite šiuos veiksmus, norėdami sumažinti paimtą kiekį.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Atidarykite reikalingą pardavimo užsakymą.
1. „FastTab“ **Pardavimo užsakymo eilutėse** , rinkitės **Naujinti eilutę \> Paėmimas** įrankių juostoje.
1. Puslapyje **Paimti** skyriuje **Operacijos** pasirinkite eilutę, kurioje **Problemos būsenos** laukelis yra nustatyta *Paimtas*.
1. Skyriuje **Operacijos** rinkitės **Įtraukti paėmimo eilutę** iš įrankių juostos.
1. Skyriuje **Paėmimo eilutės** rinkitės **Tvirtinti paėmimo eilutę** iš įrankių juostos.
1. Uždarykite puslapį **Paėmimas**.
1. Puslapio Pardavimo užsakymas veiksmų srities skirtuke **Prekybos užsakymas** skirtuke **Palaikyti** grupę rinkitės **Atšaukti**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti prekybos užsakymą.
