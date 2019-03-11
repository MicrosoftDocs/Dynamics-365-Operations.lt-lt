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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "322265"
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

