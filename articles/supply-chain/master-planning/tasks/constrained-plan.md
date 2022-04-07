---
title: Plano su apribojimais kūrimas
description: Šioje temoje aiškinama, kaip sukurti planą, kuriame būtų atsižvelgta į medžiagos ir pajėgumo apribojimus.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8372f4e35b34ff66ef55c0961b867a1aff7a5e6
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468950"
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