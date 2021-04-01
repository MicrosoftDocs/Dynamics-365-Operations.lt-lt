---
title: Perkelti faktines atsargas sandėlyje
description: Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b745308aca2503b31d7d24d7cac693bb803fc6ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244260"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Perkelti faktines atsargas sandėlyje

[!include [banner](../../includes/banner.md)]

Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą. Prieš pradedant atsargų perkėlimus, atsargų žurnalo pavadinimas turi būti nustatytas. Galite peržiūrėti šią procedūrą demonstracinių duomenų įmonės USMF naudodami rodomas pavyzdžio vertes, arba galite naudoti savo duomenis, esate nustatę produktus ir vietas. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="create-an-inventory-transfer-journal"></a>Kurkite atsargų perkėlimo žurnalą
1. **Naršymo srityje** eikite į **Atsargų valdymas > Žurnalo įrašai > Prekės > Perkėlimas**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
4. Spustelėkite **Gerai**. Yra galimybė kiekvienai žurnalo eilutei nurodyti dimensijas 'Nuo' ir 'Iki'. Tai būtina šiam žurnalo tipui. Galite perkelti elementus į vietas naudodami skirtingas taisykles. Šiame pavyzdyje perkelsime prekę į tą patį sandėlį iš numerio lentelės kontroliuojamos vietos į vietą, kurios nekontroliuoja numerio lentelė.   

## <a name="create-journal-lines"></a>Kurti žurnalo eilutes
1. „FastTab“ **Žurnalo eilutės** spustelėkite **Nauja**.
2. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti 'A0001'.  
3. Lauke **Vieta iš** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti '2'.  
4. Lauke **Vieta į** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti '2'.  
5. Lauke **Iš sandėlio** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti '24'.  
6. Lauke **Į sandėlį** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti '24'.  
7. Lauke **Iš vietos** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti 'FL-001'.  
8. Lauke **Į vietą** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti 'BULK-001'.  
9. Lauke **Kiekis** įveskite skaičių.
10. „fastTab“ **Eilutės informacija** spustelėkite skirtuką **Atsargų dimensijos**.
11. Lauko **Numerio lentelė** skiltyje **Iš atsargų dimensijų** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti '24'.  
12. Spustelėkite **Įrašyti**.

## <a name="post-the-inventory-transfer-journal"></a>Registruokite atsargų perkėlimo žurnalą
1. **Veiksmų srityje** spustelėkite **Registruoti**.
2. Spustelėkite **Gerai**.

## <a name="view-inventory-transactions"></a>Peržiūrėti atsargų operacijas
1. Spustelėkite **Atsargos**.
2. Spustelėkite **Operacijos**. Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]