---
title: Kurti planą su apribojimais
description: Ši procedūra parodo, kaip sukurti planą, kuris atsižvelgia tiek į medžiagų, tiek į pajėgumų apribojimus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845308"
---
# <a name="generate-a-constrained-plan"></a>Kurti planą su apribojimais

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip sukurti planą, kuris atsižvelgia tiek į medžiagų, tiek į pajėgumų apribojimus. Planas užtikrina, kad gamyba neprasidėtų tol, kol bus turima medžiagų ir nebus perpildyti ištekliai. 

Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra yra skirta gamybos planuotojui.


## <a name="set-up-a-constrained-plan"></a>Nustatyti planą su apribojimais
1. Spustelėkite Bendrasis planavimas.
2. Spustelėkite Bendrieji planai.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pavyzdys: statinis planas  
4. Lauke Ribotas pajėgumas pasirinkite Taip.
5. Lauke Riboto pajėgumo laiko ribos įveskite „30‟.
6. Išplėskite dalį Laiko ribos dienomis.
7. Lauke Pajėgumas pasirinkite Taip.
8. Lauke Pajėgumo planavimo laiko ribos (dienomis) įveskite skaičių.
    * Pavyzdys: 60  
9. Lauke Apskaičiuoti atidėjimai pasirinkite Taip.
10. Lauke Apskaičiuotų atidėjimų laiko ribos (dienomis) įveskite skaičių.
    * Pavyzdys: 60  
11. Išplėskite dalį Apskaičiuoti atidėjimai.
12. Lauke Pridėti apskaičiuotą atidėjimą prie poreikio datos pasirinkite Taip.
13. Lauke Pridėti apskaičiuotą atidėjimą prie poreikio datos pasirinkite Taip.
14. Lauke Pridėti apskaičiuotą atidėjimą prie poreikio datos pasirinkite Taip.
15. Uždarykite puslapį.

## <a name="create-a-constrained-plan"></a>Kurti planą su apribojimais
1. Spustelėkite Vykdyti.
2. Lauke Bendrasis planas įveskite arba pasirinkite reikšmę.
    * Pasirinkite planą, kurio apribojimus nustatėte.  
3. Spustelėkite GERAI.
    * Tai gali užtrukti.  
4. Spustelėkite Suplanuoti užsakymai.

