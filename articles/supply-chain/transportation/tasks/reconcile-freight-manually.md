--- 
title: "Transportavimo derinimas neautomatiniu būdu"
description: "Šioje procedūroje parodoma, kaip transportavimą derinti neautomatiniu būdu."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="reconcile-freight-manually"></a>Transportavimo derinimas neautomatiniu būdu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip transportavimą derinti neautomatiniu būdu. Paprastai tą daro transportavimo koordinatorius. Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.


## <a name="select-a-load-to-reconcile"></a>Derintinos apkrovos pasirinkimas
1. Pasirinkite Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis.
2. Išvalykite žymės langelį Slėpti išsiųstus ir gautus. 
3. Sąraše pasirinkite krovinį, kurio krovinio ID yra 00006.

## <a name="create-a-carrier-invoice"></a>Vežėjo SF kūrimas
    * Jei transportavimą derinate neautomatiniu būdu ir negaunate vežėjo SF automatiškai, galite kurti SF pagal transportavimo sąskaitą.  
1. Spustelėkite Susijusi informacija.
2. Spustelėkite Transportavimo sąskaitos informacija
3. Spustelėkite Generuoti krovinio atsiskaitymo SF.
4. Lauke Sąskaita faktūra surinkite reikšmę.
5. Spustelėkite GERAI.

## <a name="reconcile-the-invoice"></a>SF derinimas
    * Vežėjo SF ir transportavimo sąskaitos derinimas atliekamas kiekvienoje eilutėje.  
1. Spustelėkite Gretinti transportavimo sąskaitas ir SF.
2. Išplėskite skyrių SF informacija.
3. Išplėskite skyrių Nesugretinta transportavimo sąskaitos informacija.
4. Sąraše pažymėkite pasirinktą eilutę.
5. Spustelėkite Gretinti.
6. Išplėskite skyrių Sugretinta transportavimo sąskaitos informacija.

## <a name="submit-the-invoice-for-approval"></a>Pateikti SF patvirtinti
1. Spustelėkite Pateikti patvirtinti.
2. Uždarykite puslapį.
3. Išvalykite žymės langelį Slėpti patvirtintus. 
4. Spustelėkite Tiekėjo SF žurnalai.
5. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Nuorodų žurnalo numeris.
6. Spustelėkite Eilutės.


