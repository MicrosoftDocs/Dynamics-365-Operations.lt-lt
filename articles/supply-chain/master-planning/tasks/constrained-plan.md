---
title: Plano su apribojimais kūrimas
description: Šioje temoje aiškinama, kaip sukurti planą, kuriame būtų atsižvelgta į medžiagos ir pajėgumo apribojimus.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4af946a8dd4e5311bcb90386c88d5e7f205c4eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999861"
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

