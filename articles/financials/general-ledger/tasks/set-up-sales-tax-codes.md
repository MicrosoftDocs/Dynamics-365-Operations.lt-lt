---
title: PVM kodų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti užsakymų sulaikymo kodus Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834835"
---
# <a name="set-up-sales-tax-codes"></a>PVM kodų nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje paaiškinama, kaip nustatyti užsakymų sulaikymo kodus Dynamics 365 for Finance and Operations. PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.

Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite **Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai**.
2. Pasirinkite **Naujas**.
3. Lauke **Sales tax code**surinkite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Pasirinkite **Settlement period**, kad nurodytumėte, kuriai PVM institucijai ir kuriais intervalais reikia pranešti apie šį PVM ir jį mokėti.
6. Pasirinkite **Ledger posting group**, kad nurodytumėte pagrindines sąskaitas, kuriose į DK registruoti PVM.
7. Išplėskite **Calculation** FastTab. „FastTab‟ Skaičiavimas yra keli laukai, kurie kontroliuoja, kaip bus apskaičiuojamos PVM sumos. Tinkamai užpildykite šiuos laukelius.  
8. Sąsajos viršutinėje dalyje esančioje **Veiksmų srityje** pasirinkite **PVM kodas**.
9. Pasirinkite **Reikšmės**.
10. Įveskite šio mokesčio kodo reikšmę stulpelyje **value**.
    - Jei „FastTab‟ **Calculation**, lauke Kilmė pasirinkta Suma pagal vienetą, kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.  Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.     
11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.
13. Pasirinkite **Įrašyti**.

