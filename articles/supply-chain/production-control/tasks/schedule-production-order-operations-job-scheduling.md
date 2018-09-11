--- 
title: "Gamybos užsakymo planavimas, naudojant operacijų planavimą ir užduočių planavimą"
description: "Ši procedūra orientuota į gamybos užsakymo planavimą naudojant operacijų planavimą ir užduočių planavimą."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Gamybos užsakymo planavimas, naudojant operacijų planavimą ir užduočių planavimą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra orientuota į gamybos užsakymo planavimą naudojant operacijų planavimą ir užduočių planavimą. Užduotys nekuriamos naudojant operacijų planavimą, tačiau užduotys kuriamos naudojant užduočių planavimą. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta gamybos vadovui, gamybos planuotojui ar darbo laiko prižiūrėtojui, dirbančiam atskiros gamybos aplinkoje.


## <a name="create-a-production-order"></a>Kurti gamybos užsakymą
1. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
2. Spustelėkite Naujas gamybos užsakymas.
3. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Pasirinkite prekės numerį D0001.  
4. Spustelėkite Kurti.

## <a name="schedule-operations-for-the-production-order"></a>Gamybos užsakymo operacijų planavimas
1. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite ką tik sukurtą gamybos užsakymą. Jis turėtų būti sąrašo viršuje.      
2. Veiksmų srityje spustelėkite Grafikas.
3. Spustelėkite Planuoti operacijas.
4. Lauke Planavimo kryptis pasirinkite „Pirmyn nuo planavimo datos‟.
5. Lauke Planavimo data įveskite datą.
    * Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės. Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.  
6. Spustelėkite GERAI.
7. Sąraše pažymėkite pasirinktą eilutę.
    * Atminkite, kad būsena pasikeičia į Suplanuota.  
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite Visos užduotys.
    * Atminkite, kad nėra užduočių, sukurtų naudojant operacijų planavimą.  
10. Uždarykite puslapį.

## <a name="schedule-jobs-for-the-production-order"></a>Gamybos užsakymo užduočių planavimas
1. Veiksmų srityje spustelėkite Grafikas.
2. Spustelėkite Planuoti užduotis.
3. Lauke Planavimo kryptis pasirinkite „Pirmyn nuo planavimo datos‟.
4. Lauke Planavimo data įveskite datą.
    * Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės. Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.  
5. Spustelėkite GERAI.
6. Veiksmų srityje spustelėkite Gamybos užsakymas.
7. Spustelėkite Visos užduotys.
    * Atminkite, kad remiantis aktyviu maršrutu 5 užduotys sukuriamos naudojant užduočių planavimą.  


