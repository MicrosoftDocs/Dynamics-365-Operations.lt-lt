---
title: Krovinių ir siuntų planavimas naudojant krovinio planavimo darbo sritį
description: Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c37a98a3728cb1233a6e1207975a6b8f23f8120d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015923"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Krovinių ir siuntų planavimas naudojant krovinio planavimo darbo sritį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą. Būtina sąlyga – pirmiausia turime sukurti pardavimo užsakymą. Ši procedūra yra dalis transportavimo koordinatoriaus kasdienio darbo. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-sales-order"></a>Kurti pardavimo užsakymą
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento kodas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Pasirinkite sąskaitą **US-004**.
5. Pasirinkite **Gerai**.
6. Lauke **Prekės numeris** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Pasirinkti prekę: **A0001** **A0001** parengta naudoti transportavimo valdymui.  
8. Lauke **Puslapis** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą ir tada pasirinkite prekę.
9. Lauke **Kiekis** įveskite skaičių.
10. Lauke **Sandėlis** įveskite „24“ šiam pavyzdžiui. Šis sandėlis parengtas naudoti transportavimo valdymui ir patobulintam sandėlio valdymui.  
11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.

## <a name="create-a-new-load"></a>Sukurti naują krovinį
1. Eikite į **Valdymas skiltį > Moduliai > Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis**
2. Pasirinkite skirtuką **Pardavimo eilutės**. Dabar sukursite ką tik sukurto pardavimo užsakymo krūvį. Krovinius galima sudaryti remiantis pirkimo užsakymų, perkėlimo užsakymų ir pardavimo užsakymų sukuriama pasiūla ir paklausa.  
3. Veiksmų srityje spauskite **Tiekimas ir poreikis**.
4. Pasirinkite **Į naują krovinį**.
5. Lauke **Krovinio šablono ID** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Krovinio šablonas apibrėžia didžiausią viso krovinio svorį ir tūrį. Pvz., krovinio šablonas gali atitikti sunkvežimio ar konteinerio dydį. Pasirinkite prekę.
6. Pasirinkite **Gerai**.

## <a name="rate-and-route-the-load"></a>Nustatyti krovinio tarifą ir maršrutą
1. Pasirinkite **Tarifo ir maršruto planavimas**.
2. Pasirinkite **Tarifo ir maršruto darbo sritis**.
3. Pasirinkite **Tarifų parduotuvė**.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Pasirinkite **Priskirti**.
6. Uždarykite puslapį.

