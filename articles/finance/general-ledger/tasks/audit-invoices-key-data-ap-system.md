---
title: Mokėtinų sumų SF ir pagrindinių duomenų auditas
description: Šioje temoje aprašyta, kaip tikrinti mokėtinų sumų SF ir pagrindinius duomenis.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445876"
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

