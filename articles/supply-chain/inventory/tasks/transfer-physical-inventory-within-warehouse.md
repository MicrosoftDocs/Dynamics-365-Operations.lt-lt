---
title: Perkelti faktines atsargas sandėlyje
description: Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7715c8e7a56703993e8512af03f2ab8d6802a987
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916581"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Perkelti faktines atsargas sandėlyje

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą. Prieš pradedant atsargų perkėlimus, atsargų žurnalo pavadinimas turi būti nustatytas. Galite peržiūrėti šią procedūrą demonstracinių duomenų įmonės USMF naudodami rodomas pavyzdžio vertes, arba galite naudoti savo duomenis, esate nustatę produktus ir vietas. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="create-an-inventory-transfer-journal"></a>Kurkite atsargų perkėlimo žurnalą
1. **Naršymo srityje** eikite į **Atsargų valdymas > Žurnalo įrašai > Prekės > Perkėlimas**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
4. Spustelėkite **Gerai**. Yra galimybė kiekvienai žurnalo eilutei nurodyti dimensijas 'Nuo' ir 'Iki'. Tai būtina šiam žurnalo tipui. Galite perkelti elementus į vietas naudodami skirtingas taisykles. Šiame pavyzdyje perkelsime tame pačiame sandėlyje esantį elementą, iš vietos, kuri yra kontroliuojama pagal numerio lentelę į vietą, nekontroliuojamą pagal numerio lentelę.   

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
1. **Veiksmų sritis** spustelėkite **Registruoti**.
2. Spustelėkite **Gerai**.

## <a name="view-inventory-transactions"></a>Peržiūrėti atsargų operacijas
1. Spustelėkite **Atsargos**.
2. Spustelėkite **Operacijos**. Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.  

