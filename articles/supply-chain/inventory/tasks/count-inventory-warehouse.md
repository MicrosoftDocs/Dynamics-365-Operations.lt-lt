---
title: Skaičiuoti sandėlio atsargas
description: Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549919"
---
# <a name="count-inventory-in-a-warehouse"></a>Skaičiuoti sandėlio atsargas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje. Procedūra taikoma „pagrindinio sandėliavimo“ funkcijai, kuri galima Atsargų valdymo modulyje, o ne sandėliavimo funkcijai, kuri galima Sandėlio valdymo modulyje. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Jei naudojate savo duomenis, įsitikinkite, kad nustatėte produktus ir teritorijas ir kad sukūrėte atsargų žurnalo pavadinimą, skirtą skaičiavimo žurnalams. Atsargų inventorizaciją paprastai atlieka sandėlio darbuotojas.


## <a name="create-an-inventory-counting-journal"></a>Kurti atsargų inventorizacijos žurnalą
1. Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekės skaičiavimas > Skaičiavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite atsargų inventorizacijos žurnalo pavadinimą, kurį norite naudoti
    * Kai kurie kiti laukai bus užpildyti atsižvelgiant į pasirinkto atsargų inventorizacijos žurnalo pavadinimo nustatymą.  
5. Lauke Darbuotojas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
6. Iš sąrašo pasirinkite naudotiną darbuotoją.
7. Spustelėkite Pažymėti.
8. Spustelėkite GERAI.

## <a name="create-journal-lines"></a>Žurnalo eilučių kūrimas
1. Spustelėkite Naujas.
2. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite 'A0001'.  
4. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite teritoriją '2'.  
6. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite sandėlį '24'.  
8. Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite vietą 'BULK-001'.  
10. Lauke Suskaičiuota įveskite skaičių.
    * Jei įvesite apskaičiuotą numerį, kuris skiriasi nuo lauke Turimos atsargos rodomo skaičiaus, laukas Kiekis bus atnaujintas ir rodys neatitikimą.  
11. Spustelėkite Įrašyti.

## <a name="post-the-inventory-counting-journal"></a>Užregistruoti atsargų inventorizacijos žurnalą
1. Spustelėkite Registruoti.
    * Kai registruojate atsargų inventorizacijos žurnalą, jei apskaičiuota suma skiriasi nuo sumos, kuri pateikta lauke Turimos atsargos, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamas atsargų lygis ir vertė bei sugeneruojamos DK operacijos.  
2. Spustelėkite GERAI.

## <a name="view-inventory-transactions"></a>Peržiūrėti atsargų operacijas
1. Spustelėkite Atsargos.
2. Spustelėkite Operacijos.
    * Čia galite pamatyti visas susijusias operacijas, kurios bus sukurtos registruojant atsargų inventorizacijos žurnalą.   

