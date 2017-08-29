--- 
title: "Gamybos užsakymų skelbimą baigtais"
description: "Ši procedūra nurodo, kaip gamybos užsakymą paskelbti kaip baigtą."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff651be006b4bbe205aa9937bd7927e37a83a558
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="report-a-production-order-as-finished"></a>Gamybos užsakymų skelbimą baigtais

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip gamybos užsakymą paskelbti kaip baigtą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Tai yra šešta procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.


## <a name="report-a-production-order-as-finished"></a>Gamybos užsakymų skelbimą baigtais
1. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
    * Pasirinkite gamybos užsakymą, kurio būsena yra Pradėta.  
2. Veiksmų srityje spustelėkite Gamybos užsakymas.
3. Spustelėkite Paskelbti baigtu.
    * Šiame puslapyje galite patvirtinti baigto produkto kiekį, kurį norite paskelbti kaip baigtą.  
4. Spustelėkite skirtuką Bendra.
5. Nustatykite Prekių kiekį į '18'.
6. Nustatykite Klaidų kiekį į '2'.
7. Lauke Klaidos priežastis pasirinkite 'Medžiaga'.
8. Pažymėkite arba išvalykite žymės langelį Galutinė užduotis.
9. Pažymėkite arba išvalykite žymės langelį Leisti klaidą.
10. Spustelėkite GERAI.

## <a name="verify-the-report-as-finished-journal"></a>Patikrinti žurnalą Skelbti baigtu
1. Veiksmų srityje spustelėkite Peržiūrėti.
2. Spustelėkite Paskelbta baigtu.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Žurnalas Skelbti baigtu užregistruotas. Jei norite koreguoti žurnalą, galite rankiniu būdu sukurti naują žurnalą, kuriame galite atlikti keitimus.  


