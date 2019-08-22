---
title: Krovinių ir siuntų planavimas naudojant krovinio planavimo darbo sritį
description: Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
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
ms.openlocfilehash: c5e20eef8aa748bb64c6c14dd7e1d92ccf6592e0
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/10/2019
ms.locfileid: "1739070"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Krovinių ir siuntų planavimas naudojant krovinio planavimo darbo sritį

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
10. Lauke **Warehouse** įveskite „24“ šiam pavyzdžiui. Šis sandėlis parengtas naudoti transportavimo valdymui ir patobulintam sandėlio valdymui.  
11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.

## <a name="create-a-new-load"></a>Sukurti naują krovinį
1. Eikite į **Valdymas skiltį > Moduliai > Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis**
2. Pasirinkite skirtuką **Pardavimo eilutės**. Dabar sukursite ką tik sukurto pardavimo užsakymo krūvį. Krovinius galima sudaryti remiantis pirkimo užsakymų, perkėlimo užsakymų ir pardavimo užsakymų sukuriama pasiūla ir paklausa.  
3. Veiksmų srityje spauskite **Supply and demand**.
4. Pasirinkite **To new load**.
5. Lauke **Load template ID** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Krovinio šablonas apibrėžia didžiausią viso krovinio svorį ir tūrį. Pvz., krovinio šablonas gali atitikti sunkvežimio ar konteinerio dydį. Pasirinkite prekę.
6. Pasirinkite **Gerai**.

## <a name="rate-and-route-the-load"></a>Nustatyti krovinio tarifą ir maršrutą
1. Pasirinkite **Rating and routing**.
2. Pasirinkite **Rate route workbench**.
3. Pasirinkite **Tarifų parduotuvė**.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Pasirinkite **Priskirti**.
6. Uždarykite puslapį.

