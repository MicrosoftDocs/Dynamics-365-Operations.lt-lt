---
title: Turto pristatymas
description: Šioje temoje pateikta turto valdyme naudojamo turto apžvalga.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b8e3aaa2b249d09b304242155d646483cbe971
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433409"
---
# <a name="introduction-to-assets"></a>Turto pristatymas

[!include [banner](../../includes/banner.md)]

 

Šioje temoje pateikta turto valdyme naudojamo turto apžvalga. *Turtas* yra bet kokios rūšies įranga, pvz., mašina ar įrenginio dalis, kurią reikia prižiūrėti, aptarnauti ar remontuoti.

Turtas automatiškai atnaujinamas naudojant susijusią informaciją. Pavyzdžiui, ši susijusi informacija gali būti apie naujus arba atnaujintus darbo užsakymus. Turtą galima kurti naudojant meniu elementą **Visas turtas** arba meniu elementą **Laukiantis turtas**. Šioje temoje paaiškinta, kaip kurti turtą naudojant meniu elementą **Visas turtas**. Informaciją apie turto kūrimą naudojant meniu elementą **Laukiantis turtas** žr. [Turto kūrimas pagal pirkimo užsakymus](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Visas turtas

Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**. Sąrašo puslapyje **Visas turtas** pateiktas visas turtas ir tam tikra su juo susijusi informacija. Norėdami peržiūrėti tik aktyvų turtą, pasirinkite **Aktyvus turtas**. Norėdami peržiūrėti tik turtą, įdiegtą funkcinėse vietose, su kuriomis esate susijęs kaip priežiūros darbuotojas, pasirinkite **Mano aktyvus turtas**. (Šis ryšys nustatomas puslapyje **Darbuotojai**. Daugiau informacijos žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)

Tinklelio rodinyje **Visas turtas** pasirinkite saitą, esantį stulpelyje **Turtas**, kad peržiūrėtumėte pasirinkto įrašo informaciją. Norėdami redaguoti įrašą, pasirinkite mygtuką **Redaguoti**. Informacijos rodinyje pateikta išsami su turtu susijusi informacija. Srities **Susijusi informacija** dešinėje pateikta papildoma su turtu susijusi informacija. Išplėskite sritį, kad būtų rodoma su pasirinktu turtu susijusi informacija.

Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose. Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.

| Mygtuko pavadinimas          | Aprašymas                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redagavimas                 | Redaguoti pasirinktą turtą.                                                                                                                                         |
| Naujos                  | Kurti naują turtą.                                                                                                                                                |
| Naikinti               | Naikinti pasirinktą turtą.                                                                                                                                       |
| Perkelti turtą           | Perkelti turtą į kitą turto struktūrą arba į kitą tos pačios turto struktūros vietą.                                                                                         |
| Pakeisti turtą        | Pakeisti vieną antrinį turtą turto hierarchijoje kitu turtu.                                                                                                  |
| Diegti turtą        | Diegti turtą funkcinėje vietoje.                                                                                                                          |
| Kopijuoti turtą           | Kopijuoti turto hierarchiją į kitą turtą.                                                                                                                          |
| Užklausos             | Atidaryti sąrašo puslapį **Aktyvios užklausos**, kuriame galima peržiūrėti pasirinktam turtui sukurtas priežiūros užklausas.                                                                         |
| Įvykių retrospektyva        | Peržiūrėti įvairių su turtu atliktų registracijų apžvalgą.                                                                                                         |
| Turto KS            | Peržiūrėti visų elementų (atsarginių dalių ir kitų elementų), naudojamų turtui, sąrašą.                                                                                  |
| Darbo užsakymai          | Atidaryti sąrašo puslapį **Aktyvūs darbo užsakymai**, kuriame galima peržiūrėti turto darbo užsakymus.                                                                                        |
| Kontrolinis sąrašas            | Peržiūrėti prižiūrimo turto kontrolinių sąrašų ir matavimų, kurie buvo užregistruoti turtui, apžvalgą.                                                                                                 |
| Prižiūrimo turto prastova | Kurti arba peržiūrėti prižiūrimo turto prastovų registracijas.                                                                                                       |
| Projekto operacijos | Peržiūrėti visas užregistruotas operacijas, susijusias su darbo užsakymais, sukurtais turtui.                                                                                       |
| Turto matai       | Kurti arba peržiūrėti turto matus.                                                                                                               |
| Priežiūros grafikas | Atidaryti sąrašo puslapį **Atidaryti priežiūros grafiką**, kuriame galima peržiūrėti su turtu susietus priežiūros planus, priežiūros užklausas ir priežiūros ciklus, taip pat tuos, kurie turi būseną **Sukurta**. |
| Atnaujinti turto būseną   | Atnaujinti turto ciklo būseną. Galima pasirinkti kelis turtus sąrašo puslapyje **Visas turtas**, tada tuo pačiu metu atnaujinti visų jų turto ciklo būseną.              |
| Ciklo būsenos žurnalas  | Atidaryti žurnalą, kuriame pateiktos pasirinkto turto ciklo būsenos.                                                                                                                 |
| Turto dokumentai      | Peržiūrėti dokumentų, pridėtų prie turto, sąrašą. Šie dokumentai nustatomi dalyje **Turto valdymas** \> **Sąranka** \> **Turto dokumentai**.                 |
| Atributai           | Kurti arba peržiūrėti turto atributus.                                                                                                                             |
| Vaizdas                | Pasirinkti turto vaizdą.                                                                                                                                   |
| Pagrindinis turtas        | Peržiūrėti pasirinkto turto pagrindinio turto retrospektyvą.                                                                                                                |
| Funkcinės vietos | Peržiūrėti pasirinkto turto funkcinės vietos retrospektyvą.                                                                                                          |
| Būklės vertinimas | Registruoti turto būklės vertinimo matus.                                                                                                         |
| Gedimai               | Atidaryti sąrašo puslapį **Turto gedimai**, kuriame galima peržiūrėti užregistruotus turto gedimus.                                                                                             |
| Išlaidų kontrolė         | Palyginti biudžeto išlaidas ir faktines turto išlaidas.                                                                                                              |
| Valandų kontrolė         | Palyginti prognozuojamas valandas ir faktines turto valandas.                                                                                                              |
| Turto KPI           | Apskaičiuoti ir peržiūrėti turto pagrindinius efektyvumo indikatorius (KPI).                                                                                              |
| Pareigų rūšys            | Peržiūrėti turto dabartinių numatytųjų užduoties tipų apžvalgą.                                                                                                            |
| Kritiškumo tipai    | Peržiūrėti arba atnaujinti turto kritiškumo tipus.                                                                                                                              |
| Atsarginės dalys          | Peržiūrėti patvirtintų ir alternatyvių atsarginių dalių, kurios gali būti naudojamos turtui, sąrašą.                                                                               |
| Turto naudojimas    | Spausdinti ataskaitą, kurioje rodomos turto naudojimo registracijos.                                                                                                |
| Turto gedimas          | Spausdinti ataskaitą, kurioje rodomos turto gedimų registracijos.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]