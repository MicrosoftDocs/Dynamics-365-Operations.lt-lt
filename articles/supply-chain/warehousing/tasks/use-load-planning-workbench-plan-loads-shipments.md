---
title: Planuoti krovinius ir siuntas naudojant krovinio planavimo darbo sritį
description: Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "343908"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Planuoti krovinius ir siuntas naudojant krovinio planavimo darbo sritį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą. Būtina sąlyga – pirmiausia turime sukurti pardavimo užsakymą. Ši procedūra yra dalis transportavimo koordinatoriaus kasdienio darbo. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-sales-order"></a>Kurti pardavimo užsakymą
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Pasirinkite sąskaitą US-004.
5. Spustelėkite Gerai.
6. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Pasirinkite prekę A0001.
    * A0001 parengta naudoti transportavimo valdymui.  
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Kiekis įveskite skaičių.
10. Lauke „Sandėlis“ įveskite „24“.
    * Šiame pavyzdyje pasirinkite 24 sandėlį. Šis sandėlis parengtas naudoti transportavimo valdymui ir patobulintam sandėlio valdymui.  
11. Spustelėkite Įrašyti.
12. Uždarykite puslapį.

## <a name="create-a-new-load"></a>Sukurti naują krovinį
1. Pasirinkite Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis.
2. Spustelėkite skirtuką „Pardavimo eilutės“.
    * Dabar sudarysite krovinį pardavimo užsakymui, kurį ką tik sukūrėte. Krovinius galima sudaryti remiantis pirkimo užsakymų, perkėlimo užsakymų ir pardavimo užsakymų sukuriama pasiūla ir paklausa.  
3. Veiksmų srityje spustelėkite „Pasiūla ir paklausa“.
4. Spustelėkite „Į naują krovin“.
5. Lauke „Krovinio šablono ID“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Krovinio šablonas apibrėžia didžiausią viso krovinio svorį ir tūrį. Pvz., krovinio šablonas gali atitikti sunkvežimio ar konteinerio dydį.  
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite GERAI.

## <a name="rate-and-route-the-load"></a>Nustatyti krovinio tarifą ir maršrutą
1. Spustelėkite „Tarifo ir maršruto planavimas“.
2. Spustelėkite „Tarifo maršruto darbo sritis“.
3. Spustelėkite „Tarifo skyrius“.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Spustelėkite „Priskirti“.
6. Uždarykite puslapį.
7. Uždarykite puslapį.

