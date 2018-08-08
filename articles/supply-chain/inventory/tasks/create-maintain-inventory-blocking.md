---
title: "Kurti ir tvarkyti atsargų blokavimą"
description: "Ši procedūra nurodo, kaip neleisti kitiems siunčiamiems šaltinio dokumentams rezervuoti faktiškai turimų atsargų naudojant atsargų blokavimą."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Kurti ir tvarkyti atsargų blokavimą

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

