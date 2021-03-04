---
title: Kurti „kanban“ taisyklę naudojant „kanban“ eilutės įvykį
description: Šios procedūros metu „kanban“ taisyklė sukuriama naudojant „kanban“ eilutės įvykio parametrą, kad iš proceso veiklos būtų suaktyvintas atgalinis planavimas.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a6c4b7103874a6d955b21e99b8e219a039d4b55
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433315"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Kurti „kanban“ taisyklę naudojant „kanban“ eilutės įvykį

[!include [banner](../../includes/banner.md)]

Šios procedūros metu „kanban“ taisyklė sukuriama naudojant „kanban“ eilutės įvykio parametrą, kad iš proceso veiklos būtų suaktyvintas atgalinis planavimas. „Kanban“ taisyklę suaktyvina „kanban“ proceso veikla, kurios kiekvienas kiekis yra lygus arba didesnis už 25. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.


## <a name="create-a-kanban-rule"></a>„Kanban“ taisyklės kūrimas
1. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
2. Spustelėkite Naujas.
3. Lauke Papildymo strategija pasirinkite „Įvykis“.
    * Taip „kanban“ sugeneruojami tiesiogiai pagal poreikį. Ši parinktis naudojama siekiant nustatyti taisykles, apibrėžiančias gamybos pagal užsakymą scenarijų  
4. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Įveskite arba pasirinkite SpeakerAssemblyAndPolish. Pirmoji gamybos „kanban“ taisyklės veikla yra gamybos eigos proceso veikla. Kai pasirenkate veiklą, veiklos galiojimo datos nukopijuojamos į „kanban“ taisyklės galiojimo datas.  
5. Išplėskite skyrių Išsami informacija.
6. Lauke Produktas įveskite L0001.
7. Išplėskite skyrių Įvykiai.
8. Lauke „Kanban“ eilutės įvykis pasirinkite Automatinis.
    * Taip įvykio „kanban“ sugeneruojami pagal poreikį.  Laukas naudojamas norint konfigūruoti „kanban“ taisykles, papildančias medžiagą, kurios reikia taikomo proceso veiklai. Pasirinkus Automatinis, įvykio „kanban“ sukuriami pagal poreikį. Šį parametrą rekomenduojama naudoti, jei gamybą planuojate vykdyti tą pačią dieną.  
9. Nustatykite pasirinkties Mažiausias įvykio kiekis reikšmę „25“.
    * Įvykio „kanban“ generuojami, kai poreikio kiekis yra lygus šio lauko reikšmei arba už ją didesnis. Tai naudinga norint vienoje mašinoje gaminti užsakymo kiekį, mažesnį nei šio lauko reikšmė, ir kitoje mašinoje gaminti užsakymo kiekį, didesnį nei šio lauko reikšmė.  
10. Spustelėkite Įrašyti.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Kurti pardavimo užsakymą ir suaktyvinti „kanban“ grandinę
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
    * Pasirinkite Kliento sąskaita US-003, Miškų didmeninė prekyba.  
4. Spustelėkite GERAI.
5. Lauke „Prekės numeris“ įveskite „L0001“.
    * L0001 yra prekė, kuriai sukūrėte „kanban“ taisyklę.  
6. Nustatykite kiekį – 27.
    * Kadangi skaičius 27 yra didesnis nei minimalus „kanban“ taisyklės kiekis 25, bus suaktyvinta įvykio „kanban“.  
7. Lauke Vieta įveskite „1“.
8. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
    * Pasirinkite 13 sandėlį.  
9. Spustelėkite Įrašyti.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Peržiūrėti „kanban“, kurį sugeneravo „kanban“ taisyklė
1. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Išplėskite skyrių „Kanbans“.
    * Atkreipkite dėmesį, kad kiekio 27 „kanban“ buvo sukurtas siekiant apdoroti veiklą pagal sukurtą „kanban“ taisyklę.  
    * Tai paskutinis veiksmas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]