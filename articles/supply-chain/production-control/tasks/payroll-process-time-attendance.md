--- 
title: "Įgalinti laiko ir buvimo darbe algalapio procesą"
description: "Ši procedūra parodo, kaip įgalinti laiko ir buvimo darbe algalapio procesą."
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 16d8fc2120dfb7b356b238957019a29d05963f9a
ms.contentlocale: lt-lt
ms.lasthandoff: 02/06/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Įgalinti laiko ir buvimo darbe algalapio procesą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip įgalinti laiko ir buvimo darbe algalapio procesą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Kurti mokėjimo tipą su susijusiu darbo užmokesčio tarifu
1. Laikas ir buvimas darbe > Nustatymas > Algalapis > Mokėjimo tipai
2. Spustelėkite Naujas.
3. Lauke Mokėjimo tipas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite Tarifai.
    * Mokėjimo tipų koeficientai nustatomi tam tikriems laiko intervalams, o darbuotojams gali būti sukurti atskiri koeficientai. Ne visada būtina kurti laiko ir buvimo darbe mokėjimo tipų koeficientus. Ši informacija jau gali būti algalapių sistemoje, kuri naudojama atlyginimams generuoti.  
7. Spustelėkite Naujas.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Tarifas įveskite skaičių.
10. Spustelėkite Įrašyti.

## <a name="create-a-pay-agreement"></a>Mokėjimo sutarties kūrimas
1. Uždarykite puslapį.
2. Uždarykite puslapį.
3. Eikite į Mokėjimo sutartys.
    * Laikas ir buvimas darbe > Nustatymas > Mokėjimo sutartys  
4. Spustelėkite Naujas.
5. Lauke Mokėjimo sutartis surinkite reikšmę.
6. Lauke Aprašas įveskite reikšmę.
7. Spustelėkite Įrašyti.
8. Spustelėkite Sutarties eilutės.
9. Spustelėkite Naujas.
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke Profilio tipas įveskite arba pasirinkite reikšmę.
12. Lauke Mokėjimo tipas įveskite arba pasirinkite reikšmę.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Nustatyti laiko ir registracijos darbuotojo mokėjimo sutartį
1. Uždarykite puslapį.
2. Uždarykite puslapį.
3. Eikite į Laiko registracijos darbuotojai.
    * Laikas ir buvimas darbe > Nustatymas > Laiko registracijos darbuotojai  
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėkite skirtuką Užimtumas.
6. Išplėskite skyrių Laiko registracija.
7. Spustelėkite Redaguoti.
8. Lauke Mokėjimo sutartis įveskite arba pasirinkite reikšmę.


