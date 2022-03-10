---
title: Gamybos užsakymo planavimas naudojant operacijų ir užduočių planavimą
description: Šioje temoje aprašyta, kaip planuoti gamybos užsakymą naudojant operacijų ir užduočių planavimą.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91fe5aa398cd94e38beea017d6d60ecb44f17e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574382"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Gamybos užsakymo planavimas naudojant operacijų ir užduočių planavimą

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašyta, kaip planuoti gamybos užsakymą naudojant operacijų ir užduočių planavimą. Užduotys nekuriamos naudojant operacijų planavimą, tačiau užduotys kuriamos naudojant užduočių planavimą. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta gamybos vadovui, gamybos planuotojui ar darbo laiko prižiūrėtojui, dirbančiam atskiros gamybos aplinkoje.


## <a name="create-a-production-order"></a>Gamybos užsakymo kūrimas
1. Naršymo srityje eikite į **Moduliai > Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai**.
2. Pasirinkite **Naujas gamybos užsakymas**.
3. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę. Pasirinkite prekės numerį **D0001**.  
4. Pasirinkite **Kurti**.

## <a name="schedule-operations-for-the-production-order"></a>Gamybos užsakymo operacijų planavimas
1. Pažymėkite naujai sukurtą eilutę.      
2. Veiksmų srityje pasirinkite **Planavimas**.
3. Pasirinkite **Planuoti operacijas**.
4. Lauke **Planavimo kryptis** pasirinkite **Pirmyn nuo planavimo datos**.
5. Lauke **Planavimo data** įveskite datą. Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės. Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.  
6. Pasirinkite **Gerai**.
7. Sąraše pažymėkite pasirinktą eilutę. Atkreipkite dėmesį, kad būsena pakeičiama į **Suplanuotas**. 
8. Pasirinkite **Visos užduotys**. Atminkite, kad nėra užduočių, sukurtų naudojant operacijų planavimą.  
9. Uždarykite puslapį.

## <a name="schedule-jobs-for-the-production-order"></a>Gamybos užsakymo užduočių planavimas
1. Veiksmų srityje pasirinkite **Planavimas**.
2. Pasirinkite **Planuoti užduotis**.
3. Lauke **Planavimo kryptis** pasirinkite **Pirmyn nuo planavimo datos**.
4. Lauke **Planavimo data** įveskite datą. Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės. Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.  
5. Pasirinkite **Gerai**.
6. Veiksmų srityje pasirinkite **Gamybos užsakymas**.
7. Pasirinkite **Visos užduotys**. Atminkite, kad remiantis aktyviu maršrutu 5 užduotys sukuriamos naudojant užduočių planavimą.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]