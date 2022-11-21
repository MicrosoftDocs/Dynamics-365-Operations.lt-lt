---
title: Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu
description: Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778549"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Įrašyti tiekėjo SF ir sugretinti su gautu kiekiu

[!include [banner](../../includes/banner.md)]

Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti. Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas. 

Mokėtinų **sumų parametrų puslapyje, įsitikinkite,** **kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą,** **·** **lauke Registruoti SF su nesutapimų nustatyta kaip Reikalauti patvirtinimo,** **o eilutės atitikimo strategijos laukas nustatytas** kaip Triaipus atitikimas.**·**

Šioje procedūroje naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Eikite į **Visi pirkimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Tiekėjo sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Lauke **Tiekėjo sąskaita** įveskite vertę.
5. Spustelėkite **Gerai**.
6. Spustelėkite **Pridėti eilutę**.
7. Lauke **Prekės numeris** įveskite vertę.
8. Veiksmų srityje spustelėkite **Pirkti**.
9. Spustelėkite **Patvirtinti**.

## <a name="post-a-product-receipt"></a>Registruoti produkto gavimo kvitą
1. Veiksmų srityje spustelėkite **Gauti**.
2. Spustelėkite **Produkto gavimo kvitas**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke **Produkto gavimo kvitas** įveskite vertę.
5. Spustelėkite **Gerai**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą
1. Veiksmų srityje spustelėkite **Sąskaita faktūra**.
2. Spustelėkite **Sąskaita faktūra**.
3. Lauke **Numeris** įveskite vertę.
4. Spustelėkite **Numatyt. iš: užsakyto kiekio**, kad atidarytumėte išplečiamąjį dialogo langą.
5. Lauke **Numatytasis eilučių kiekis** pasirinkite parinktį.
6. Spustelėkite **Gerai**.
7. Spustelėkite **Taip**.
8. Spustelėkite **Sugretinti produktų gavimo kvitus**.
9. Spustelėkite **Gerai**.
10. Veiksmų srityje spustelėkite **Peržiūrėti**.
11. Spustelėkite **Gretinimo informacija**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
