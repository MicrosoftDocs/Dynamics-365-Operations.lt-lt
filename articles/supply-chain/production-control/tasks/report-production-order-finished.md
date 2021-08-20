---
title: Gamybos užsakymų skelbimą baigtais
description: Ši procedūra nurodo, kaip gamybos užsakymą paskelbti kaip baigtą.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d7aceff33e126227c850b3bd087afb3e70b4254752c9c9240b8df0f5f681217
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781859"
---
# <a name="report-a-production-order-as-finished"></a>Gamybos užsakymų skelbimą baigtais

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]