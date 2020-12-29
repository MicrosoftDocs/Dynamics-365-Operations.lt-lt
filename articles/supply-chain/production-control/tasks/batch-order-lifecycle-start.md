---
title: Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo
description: Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e57cd9254185b73f544e8ff4f7658cf743b672f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433324"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo

[!include [banner](../../includes/banner.md)]

Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.

Nuo kūrimo, savikainos įvertinimo ir gamybos užduoties planavimo iki faktinio paketinio užsakymo paleidimo.



Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. 



Būtina šios procedūros vykdymo sąlyga su kitu duomenų rinkiniu yra patvirtintas produktas su aktyvia formule ir maršruto versija.


## <a name="create-a-batch-order"></a>Kurti paketinį užsakymą
1. Eikite į Visi gamybos užsakymai.
2. Spustelėkite Naujas paketinis užsakymas.
3. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
4. Spustelėkite Kurti.
5. Naudodami spartųjį filtrą filtruokite lauką Gamyba verte 'b'.

## <a name="view-production-formula-and-expected-co-products"></a>Peržiūrėti gamybos formulę ir numatomus sudėtinius produktus
1. Veiksmų srityje spustelėkite Gamybos užsakymas.
2. Spustelėkite Formulė.
3. Uždarykite puslapį.
4. Spustelėkite Sudėtiniai produktai.
5. Uždarykite puslapį.

## <a name="estimate-the-batch-order"></a>Įvertinti paketinį užsakymą
1. Spustelėkite Įvertinti.
2. Spustelėkite GERAI.
3. Veiksmų srityje spustelėkite Valdyti išlaidas.
4. Spustelėkite Peržiūrėti skaičiavimo informaciją.
5. Uždarykite puslapį.

## <a name="release-the-batch-order"></a>Patvirtinti paketinį užsakymą
1. Veiksmų srityje spustelėkite Gamybos užsakymas.
2. Spustelėkite Išleisti.
3. Spustelėkite GERAI.

## <a name="schedule-production-jobs"></a>Planuoti gamybos užduotis
1. Veiksmų srityje spustelėkite Grafikas.
2. Spustelėkite Planuoti užduotis.
3. Lauke Ribotas pajėgumas pasirinkite Ne.
4. Lauke Ribotos medžiagos pasirinkite Ne.
5. Spustelėkite Gerai.
6. Veiksmų srityje spustelėkite Gamybos užsakymas.
7. Spustelėkite Visos užduotys.
8. Uždarykite puslapį.

## <a name="start-the-batch-order"></a>Paleisti paketinį užsakymą
1. Spustelėkite Pradėti.
2. Spustelėkite skirtuką Bendra.
3. Lauke Registruoti išrinkimo dokumentą dabar pasirinkite Ne.
4. Spustelėkite GERAI.
5. Veiksmų srityje spustelėkite Peržiūrėti.
6. Spustelėkite Išrinkimo dokumentas.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Spustelėkite Technologinė kortelė.
11. Sąraše spustelėkite saitą pasirinktoje eilutėje.
12. Uždarykite puslapį.
13. Uždarykite puslapį.

