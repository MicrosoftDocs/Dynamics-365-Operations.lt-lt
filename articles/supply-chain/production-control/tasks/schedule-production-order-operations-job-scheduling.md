---
title: Gamybos užsakymo planavimas, naudojant operacijų planavimą ir užduočių planavimą
description: Ši procedūra orientuota į gamybos užsakymo planavimą naudojant operacijų planavimą ir užduočių planavimą.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4932cfa472c34a16249b226aa4a07b8e5f528053
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838492"
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

