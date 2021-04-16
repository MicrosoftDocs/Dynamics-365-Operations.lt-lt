---
title: Registruoti prekės, kurios pagrindinio sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą
description: Ši procedūra nurodo, kaip reikia užregistruoti elementus naudojant prekių gavimo žurnalą, kai atsargų valdymo modulyje naudojate „pagrindinį sandėliavimą“.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 61ce76c5aac82ec95b7113066b47b85a9c944307
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830863"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Registruoti prekės, kurios pagrindinio sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip reikia užregistruoti elementus naudojant prekių gavimo žurnalą, kai atsargų valdymo modulyje naudojate „pagrindinį sandėliavimą“. Paprastai tai atlieka gavimo klerkas. Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF, naudodami rodomas pavyzdines reikšmes.  Jei nenaudojate USMF, prieš pradėdami šį vadovą turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute. Prekė eilutėje turi būti laikoma atsargose. Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje aktyvūs teritorija ir sandėlis.


## <a name="create-item-arrival-journal-header"></a>Kurti prekių gavimo žurnalo antraštę
1. Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekių gavimas > Prekių gavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
    * Jei naudojate USMF, galite surinkti WHS. Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinksite, turi turėti šias savybes: patikros rinkimo vieta turi būti nustatyta į „Ne“ ir karantino valdymas turi būti nustatytas į „Ne“.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]