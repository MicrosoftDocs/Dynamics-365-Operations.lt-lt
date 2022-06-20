---
title: Mokėtinų sumų SF ir pagrindinių duomenų auditas
description: Šiame straipsnyje parodyta, kaip atlikti mokėtinų sumų SF ir pagrindinius duomenis.
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
ms.openlocfilehash: 76c45133091a86da773d7f63addd460abd92aae7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868361"
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
