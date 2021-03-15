---
title: Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu
description: Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be1e818e8a97684248c9c0b9d43c39e631f855f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979268"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]