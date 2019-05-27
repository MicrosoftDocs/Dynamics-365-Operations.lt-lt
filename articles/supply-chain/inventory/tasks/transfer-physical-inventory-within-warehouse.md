---
title: Perkelti faktines atsargas sandėlyje
description: Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b3e91be8aeab10188b6d3925d44a9ec1106406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554189"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Perkelti faktines atsargas sandėlyje

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą. Prieš pradedant atsargų perkėlimus, atsargų žurnalo pavadinimas turi būti nustatytas. Galite peržiūrėti šią procedūrą demonstracinių duomenų įmonės USMF naudodami rodomas pavyzdžio vertes, arba galite naudoti savo duomenis, esate nustatę produktus ir vietas. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="create-an-inventory-transfer-journal"></a>Kurkite atsargų perkėlimo žurnalą
1. Eikite į Perkėlimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
4. Spustelėkite GERAI.
    * Yra galimybė kiekvienai žurnalo eilutei nurodyti dimensijas 'Nuo' ir 'Iki'. Tai būtina šiam žurnalo tipui. Galite perkelti elementus į vietas naudodami skirtingas taisykles. Šiame pavyzdyje perkelsime tame pačiame sandėlyje esantį elementą, iš vietos, kuri yra kontroliuojama pagal numerio lentelę į vietą, nekontroliuojamą pagal numerio lentelę.   

## <a name="create-journal-lines"></a>Žurnalo eilučių kūrimas
1. Spustelėkite Naujas.
2. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti 'A0001'.  
3. Lauke Iš teritorijos įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti '2'.  
4. Lauke Į teritoriją įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti '2'.  
5. Lauke Iš sandėlio įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti '24'.  
6. Lauke Į sandėlį įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti '24'.  
7. Lauke Iš vietos įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti 'FL-001'.  
8. Lauke Į vietą įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti 'BULK-001'.  
9. Lauke Kiekis įveskite skaičių.
10. Spustelėkite skirtuką Atsargų dimensijos.
11. Lauke Numerio lentelė įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti '24'.  
12. Spustelėkite Įrašyti.

## <a name="post-the-inventory-transfer-journal"></a>Registruokite atsargų perkėlimo žurnalą
1. Spustelėkite Registruoti.
2. Spustelėkite GERAI.

## <a name="view-inventory-transactions"></a>Peržiūrėti atsargų operacijas
1. Spustelėkite Atsargos.
2. Spustelėkite Operacijos.
    * Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.  

