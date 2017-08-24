--- 
title: "Pradėti gamybos užsakymą"
description: "Šioje procedūroje nurodoma, kaip paleisti gamybos užsakymą ceche."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: a88968072b28ab468af97a875bd76d4d6abecfde
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="start-a-production-order"></a>Pradėti gamybos užsakymą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje nurodoma, kaip paleisti gamybos užsakymą ceche. Šiame procese skelbiamos laiko ir medžiagų sąnaudos. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Tai yra penkta procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.


## <a name="start-a-production-order"></a>Pradėti gamybos užsakymą
1. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
    * Pasirinkite gamybos užsakymą, kurio būsena yra Išleistas.  
2. Veiksmų srityje spustelėkite Gamybos užsakymas.
3. Spustelėkite Pradėti.
    * Šiame puslapyje galite patvirtinti gamybos užsakymo pradžią.  
4. Spustelėkite skirtuką Bendra.
5. Lauke Šaltinio oper. Nr. įveskite „10“.
6. Lauke Automatinis maršruto suvartojimas pasirinkite „Visada“.
7. Spustelėkite žymės langelį Registruoti technologinę kortelę dabar.
8. Lauke Automatinis KS suvartojimas pasirinkite „Visada“.
9. Spustelėkite žymės langelį Registruoti išrinkimo dokumentą dabar.
10. Spustelėkite žymės langelį Spausdinti išrinkimo dokumentą.
11. Spustelėkite GERAI.
    * Tai yra atspausdintas išrinkimo dokumentas, kuriame nurodomos gamybos užsakymui naudojamos medžiagos.  
12. Uždarykite puslapį.

## <a name="validate-the-picking-list"></a>Išrinkimo dokumento tikrinimas
1. Veiksmų srityje spustelėkite Peržiūrėti.
2. Spustelėkite Išrinkimo dokumentas.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėkite Redaguoti.
6. Lauke Suvartojimas įveskite skaičių.
7. Spustelėkite Registruoti.
8. Spustelėkite GERAI.
    * Išrinkimo dokumento žurnale užregistruojamos gamybos užsakymui suvartotos medžiagos. Prieš užregistruodami žurnalą, jei yra skirtumas tarp įvertinto kiekio ir faktinio suvartoto kiekio, galite atlikti koregavimus.  
9. Spustelėkite skirtuką GridPanel.
10. Uždarykite puslapį.

## <a name="verify-the-route-card-journal"></a>Technologinės kortelės žurnalo tikrinimas
1. Veiksmų srityje spustelėkite Peržiūrėti.
2. Spustelėkite Technologinė kortelė.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėkite Redaguoti.
6. Lauke Valandos įveskite skaičių.
7. Spustelėkite Registruoti.
8. Spustelėkite GERAI.
    * Technologinės kortelės žurnale įrašomas atskiroms operacijoms skiriamas laikas. Taip pat gali būti nurodytas prekių ir klaidų kiekis.  


