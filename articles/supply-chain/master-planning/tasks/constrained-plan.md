---
title: Plano su apribojimais kūrimas
description: Šioje temoje aiškinama, kaip sukurti planą, kuriame būtų atsižvelgta į medžiagos ir pajėgumo apribojimus.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e36396ce12ec51d9c093fbf7c72051f7501d84900ec62d6f3ebd8f36296636e3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744111"
---
# <a name="generate-a-constrained-plan"></a>Plano su apribojimais kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sukurti planą, kuriame būtų atsižvelgta į medžiagos ir pajėgumo apribojimus. Planas užtikrina, kad gamyba neprasidėtų tol, kol bus turima medžiagų ir nebus perpildyti ištekliai. 

Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra yra skirta gamybos planuotojui.


## <a name="set-up-a-constrained-plan"></a>Nustatyti planą su apribojimais
1. Pagrindiniame puslapyje pažymėkite darbo sritį **Pagrindinis planavimas**.
2. Darbo srities dešinėje pusėje saitų sąraše pažymėkite **Pagrindiniai planai**.
3. Sąraše raskite ir pasirinkite norimą įrašą. Pavyzdys: **StaticPlan**  
4. Pasirinkite **Taip** lauke **Ribotas pajėgumas**.
5. Lauke **Riboto pajėgumo laiko riba** įveskite `30`.
6. Išplėskite skyrių **Laiko riba dienomis**.
7. Pasirinkite **Taip** lauke **Pajėgumas**.
8. Lauke **Pajėgumo planavimo laiko riba (dienomis)** įveskite skaičių. Pavyzdys: `60`  
9. Pasirinkite **Taip** lauke **Apskaičiuotos delsos**.
10. Lauke **Apskaičiuotų delsų laiko riba (dienomis)** įveskite skaičių. Pavyzdys: `60` 
11. Išplėskite skyrių **Apskaičiuotos delsos**.
12. Visuose laukuose **Įtraukti apskaičiuotą delsą į reikalavimo datą** pažymėkite **Taip**.
13. Uždarykite puslapį.

## <a name="create-a-constrained-plan"></a>Kurti planą su apribojimais
1. Pasirinkite **Vykdyti**.
2. Lauke **Pagrindinis planas** įveskite arba pasirinkite planą, kuriam nustatėte apribojimus.  
3. Pasirinkite **Gerai**.
4. Pažymėkite **Suplanuoti užsakymai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]