---
title: Sandėlio atsargų skaičiavimas
description: Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0909625f31d15fe6b1387ff9ab7fd5d9a9135f4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836458"
---
# <a name="count-inventory-in-a-warehouse"></a>Sandėlio atsargų skaičiavimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje. Procedūra taikoma „pagrindinio sandėliavimo“ funkcijai, kuri galima Atsargų valdymo modulyje, o ne sandėliavimo funkcijai, kuri galima Sandėlio valdymo modulyje. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Jei naudojate savo duomenis, įsitikinkite, kad nustatėte produktus ir teritorijas ir kad sukūrėte atsargų žurnalo pavadinimą, skirtą skaičiavimo žurnalams. Atsargų inventorizaciją paprastai atlieka sandėlio darbuotojas.


## <a name="create-an-inventory-counting-journal"></a>Kurti atsargų inventorizacijos žurnalą
1. Valdymo skiltyje pasirinkite **Naršymo sritis > Moduliai > Atsargų valdymas > Žurnalo įrašai > Prekės skaičiavimas > Skaičiavimas**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** paspauskite išplečiamąjį mygtuką, kad pasirinktumėte atsargų inventorizacijos žurnalo pavadinimą, kurį norite naudoti. Kai kurie kiti laukai bus užpildyti atsižvelgiant į pasirinkto atsargų inventorizacijos žurnalo pavadinimo nustatymą.  
4. Lauke **Darbuotojas** spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
5. Iš sąrašo **Pasirinkti** naudotiną darbuotoją.
6. Pasirinkite **Gerai**.

## <a name="create-journal-lines"></a>Kurti žurnalo eilutes
1. Pasirinkite **Naujas**.
2. Lauke **Prekės numeris** pasirinkite norimą įrašą išplečiamajame sąraše. Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite **A0001**.  
3. Lauke **Puslapis** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite teritoriją **2**.
4. Lauke **Sandėlis** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite sandėlį **24**.  
5. Skirtuke **Location** iš išplečiamojo sąrašo pasirinkite norimą įrašą. Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite vietą **BULK-001**.  
6. Lauke Suskaičiuota įveskite skaičių. Jei įvesite apskaičiuotą numerį, kuris skiriasi nuo lauke **Turimos atsargos**rodomo skaičiaus, laukas **Kiekis** bus atnaujintas ir rodys neatitikimą.  
7. Pasirinkite **Įrašyti**.

## <a name="post-the-inventory-counting-journal"></a>Užregistruoti atsargų inventorizacijos žurnalą
1. Pasirinkite **Registruoti**. Kai registruojate atsargų inventorizacijos žurnalą, jei apskaičiuota suma skiriasi nuo sumos, kuri pateikta lauke **Turimos atsargos**, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamas atsargų lygis ir vertė bei sugeneruojamos DK operacijos.
2. Pasirinkite **Gerai**.

## <a name="view-inventory-transactions"></a>Peržiūrėti atsargų operacijas
1. Pasirinkite **Atsargos**.
2. Pasirinkite **Operacijos**. Čia galite pamatyti visas susijusias operacijas, kurios bus sukurtos registruojant atsargų inventorizacijos žurnalą.   

