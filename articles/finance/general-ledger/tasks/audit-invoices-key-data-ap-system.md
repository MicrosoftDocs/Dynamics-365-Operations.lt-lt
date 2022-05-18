---
title: Mokėtinų sumų SF ir pagrindinių duomenų auditas
description: Šioje temoje aprašyta, kaip tikrinti mokėtinų sumų SF ir pagrindinius duomenis.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb8799f8baf7b6ed775c73a1624abe794e692a3
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711526"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Mokėtinų sumų SF ir pagrindinių duomenų auditas

[!include [banner](../../includes/banner.md)]

Gavę sąskaitą faktūrą iš tiekėjo už prekes ir paslaugas, pateiktas pirkimo užsakyme, atsižvelgiant į verslo procesus, gali reikėti, kad prekės ar paslaugos būtų gautos prieš pateikiant sąskaitą faktūrą apmokėti. Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas. 

Puslapyje **Mokėtinų sumų parametrai** įsitikinkite, kad pasirinkta parinktis Įgalinti SF gretinimo tikrinimą, laukas **Registruoti SF su nesutapimais** nustatytas į **Reikalauti patvirtinimo**, o laukas **Eilučių atitikimo strategija** nustatytas į **Tripusis atitikimas**.

Šioje procedūroje naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Eikite į **Visi pirkimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Tiekėjo sąskaita** įveskite vertę.
4. Spustelėkite **Gerai**.
5. Spustelėkite **Pridėti eilutę**.
6. Lauke **Prekės numeris** įveskite vertę.
7. Veiksmų srityje spustelėkite **Pirkti**.
8. Spustelėkite **Patvirtinti**.

## <a name="post-a-product-receipt"></a>Registruoti produkto gavimo kvitą
1. Veiksmų srityje spustelėkite **Gauti**.
2. Spustelėkite **Produkto gavimo kvitas**.
3. Lauke **Produkto gavimo kvitas** įveskite vertę.
4. Spustelėkite **Gerai**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Įrašyti bei gretinti tiekėjo SF ir produkto gavimo kvitą
1. Veiksmų srityje spustelėkite **Sąskaita faktūra > Sąskaita faktūra**.
2. Lauke **Numeris** įveskite vertę.
3. Spustelėkite **Numatyt. iš: užsakyto kiekio**, kad atidarytumėte išplečiamąjį dialogo langą.
4. Lauke **Numatytasis eilučių kiekis** pasirinkite parinktį.
5. Spustelėkite **Gerai**.
6. Spustelėkite **Taip**.
7. Spustelėkite **Sugretinti produktų gavimo kvitus**.
8. Spustelėkite **Gerai**.
9. Veiksmų srityje spustelėkite **Peržiūrėti**.
10. Spustelėkite **Gretinimo informacija**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
