--- 
title: "Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu"
description: "Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b0ba3a29514351a89cf83f1ce7a3e147626e721
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti. Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas. 

Puslapyje Mokėtinų sumų parametrai įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas Registruoti SF su nesutapimais nustatytas į Reikalauti patvirtinimo, o laukas Eilučių atitikimo strategija nustatytas į Tripusis atitikimas.

Šioje procedūroje naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Eikite į Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Lauke Tiekėjo sąskaita surinkite reikšmę.
5. Spustelėkite GERAI.
6. Spustelėkite Pridėti eilutę.
7. Lauke Prekės numeris surinkite reikšmę.
8. Veiksmų srityje spustelėkite Pirkti.
9. Spustelėkite Patvirtinti.

## <a name="post-a-product-receipt"></a>Registruoti produkto gavimo kvitą
1. Veiksmų srityje spustelėkite Gauti.
2. Spustelėkite Produkto gavimo kvitas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Produkto gavimo kvitas surinkite reikšmę.
5. Spustelėkite GERAI.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą
1. Veiksmų srityje spustelėkite Sąskaita faktūra.
2. Spustelėkite Sąskaita faktūra.
3. Lauke Numeris surinkite reikšmę.
4. Spustelėkite Numatyt. iš: užsakyto kiekio, kad atidarytumėte išplečiamąjį dialogo langą.
5. Lauke Numatytasis eilučių kiekis pasirinkite parinktį.
6. Spustelėkite GERAI.
7. Spustelėkite Taip.
8. Spustelėkite Sugretinti gavimo dokumentus.
9. Spustelėkite GERAI.
10. Veiksmų srityje spustelėkite Peržiūrėti.
11. Spustelėkite Gretinimo informacija.


