---
title: Kurti ir tvarkyti atsargų blokavimą
description: Ši procedūra nurodo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 845d517ad10245df3b208874df61e235c199c7fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836411"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Kurti ir tvarkyti atsargų blokavimą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą. Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF naudodami rodomas pavyzdines reikšmes. Prieš pradedant šią procedūrą jums reikės turėti prekę su faktiškai turimomis atsargomis.


## <a name="create-an-inventory-blocking"></a>Sukurti atsargų blokavimą
1. Pasirinkite Atsargų valdymas > Periodinės užduotys > Atsargų blokavimas.
2. Spustelėkite Naujas.
3. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše pasirinkite norimą prekę. 
    * Pasirinkite prekės numerį su faktiškai turimomis atsargomis, kurias norite blokuoti. Jei naudojate USMF, galite pasirinkti prekę M9201.  
5. Lauke Kiekis įveskite skaičių.
    * Jei naudojate prekę M9201, turite pasirinkti mažiau nei 200.  
6. Perjunkite skyriaus „Atsargų matmenys“ išplėtimą.
7. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate prekę M9201, galite pasirinkti sandėlį 51.  
9. Spustelėkite Įrašyti.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Atnaujinti atsargų blokavimo sąlygas
1. Lauke Kiekis įveskite skaičių.
    * Atnaujinkite atsargų kiekio lauką, kad atitiktų norimą blokuoti kiekį.  
2. Lauke „Numatoma data“ įveskite datą.
    * Galite nurodyti, kada turėtų būti galima rezervuoti užblokuotas atsargas, priskirdami numatomą datą. Jei atsargų blokavimui parenkama parinktis „Numatomi gavimai“, kuri būna parenkama pagal numatytuosius nustatymus, kai blokavimą kuriate rankiniu būdu, ši data bus rodoma numatomoje operacijoje.  
3. Spustelėkite Įrašyti.

## <a name="remove-the-inventory-blocking"></a>Pašalinti atsargų blokavimą
1. Spustelėkite Naikinti.
2. Spustelėkite Taip.
3. Uždarykite puslapį.

