---
title: Pradėti gamybos užsakymą
description: Šioje procedūroje nurodoma, kaip paleisti gamybos užsakymą ceche.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be1c389bc4193ef080dbeb1639b69acf466ef0de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831871"
---
# <a name="start-a-production-order"></a>Pradėti gamybos užsakymą

[!include [banner](../../includes/banner.md)]

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]