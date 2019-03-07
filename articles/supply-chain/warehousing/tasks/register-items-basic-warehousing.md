---
title: Registruoti prekės, kurios pagrindinio sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą
description: Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c53a38eb6afdf8d3cc1a316c8da5e84549ab60d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "361434"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Registruoti prekės, kurios pagrindinio sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟. Paprastai tai atlieka gavimo klerkas. Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF, naudodami rodomas pavyzdines reikšmes.  Jei nenaudojate USMF, prieš pradėdami šį vadovą turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute. Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų. Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje aktyvūs teritorija ir sandėlis.


## <a name="create-item-arrival-journal-header"></a>Kurti prekių gavimo žurnalo antraštę
1. Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekių gavimas > Prekių gavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
    * Jei naudojate USMF, galite surinkti WHS. Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinkote, turi turėti toliau nurodytas ypatybes: Tikrinti paėmimo vietą turi būti nustatyta į Ne ir Sulaikymo valdymas turi būti nustatyta į Ne.  
4. Lauke Važtaraštis surinkite reikšmę.
    * Tai yra važtaraščio ID iš tiekėjo išduoto važtaraščio. Pridėkite unikalų numerį.  
5. Lauke Numeris pasirinkite pirkimo užsakymą.
6. Spustelėkite GERAI.

## <a name="add-lines-to-item-arrival-journal"></a>Į prekių gavimo žurnalą pridėti eilučių
1. Spustelėkite Funkcijos.
2. Spustelėkite Kurti eilutes.
    * Į šį žurnalą eilutes galima įvesti rankiniu būdu arba sukurti automatiškai. Bus parodyta, kaip sukurti automatiškai.  
3. Pažymėkite arba atžymėkite žymės langelį Inicijuoti kiekį.
    * Kiekis žurnalo eilutėse bus inicijuojamas su kiekiu, neužregistruotu pirkimo užsakymo eilutėje.  
4. Spustelėkite GERAI.

## <a name="post-the-journal"></a>Registruoti žurnalą
1. Spustelėkite Registruoti.
2. Spustelėkite GERAI.

## <a name="generate-the-product-receipt"></a>Generuoti produkto gavimo kvitą
1. Spustelėkite Funkcijos.
2. Spustelėkite Produkto gavimo kvitas.
3. Spustelėkite GERAI.

