---
title: Gamybos užsakymų skelbimą baigtais
description: Ši procedūra nurodo, kaip gamybos užsakymą paskelbti kaip baigtą.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: def39fa86103bc69d1c88dde8d0660945c1de82e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210553"
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

