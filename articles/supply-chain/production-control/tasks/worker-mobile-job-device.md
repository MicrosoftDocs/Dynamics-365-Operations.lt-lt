---
title: Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį
description: Šiame straipsnyje paaiškinama, kaip darbuotojo vartotojo abonementui priskirti tinkamus vaidmenis ir įgalinti darbuotoją atlikti darbo laiko registracijas.
author: johanhoffmann
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f6f51a66d49cafd172ba123bf883fb41cdcb5c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844311"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip darbuotojo vartotojo abonementui priskirti tinkamus vaidmenis ir įgalinti darbuotoją atlikti darbo laiko registracijas.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Patikrinkite, ar darbuotojui priskirtas konkretus vaidmuo.

Pavyzdys: prieš sukonfigūruodami darbuotojo abonementą patikrinkite, ar vartotojui „SHANNON“ yra priskirtas mašinos operatoriaus vaidmuo.

1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.
2. Ieškokite vartojo naudodami spartųjį filtrą. Šiame pavyzdyje įveskite `shannon`.
3. Stulpelyje **Vartotojo ID** pasirinkite atsirandančios vartotojo paskyros saitą.
4. Medyje **Vartotojo vaidmenys** pasirinkite **Vaidmenys > Mašinų operatorius**.
5. Uždarykite puslapius **Vartotojo duomenys** ir **Vartotojai**, kad grįžtumėte į pradžios puslapį.

## <a name="configure-worker-account"></a>Konfigūruokite darbuotojo abonementą.
1. Eikite į **Naršymo sritis > Moduliai > Žmogiškieji ištekliai > Darbuotojai > Darbuotojai**.
2. Ieškokite vartojo naudodami spartųjį filtrą. Šiame pavyzdyje įveskite `shannon`.
3. Atsidariusiame vartotojo paskyros stulpelyje **Pavadinimas** pasirinkite saitą.
4. Pasirinkite skirtuką **Laiko registracija**.
5. Pasirinkite **Suaktyvinti registruojant terminalus**.
6. Šiuose laukuose pasirinkite vertes:  

    - **Skaičiavimo grupė**  
    - **Numatytoji skaičiavimo grupė**  
    - **Patvirtinimo grupė**  
    - **Standartinis šablonas**  
    - **Šablono grupė**  

7. Pasirinkite **Gerai**.
8. Spustelėję **Redaguoti** įveskite naujos laiko registracijos darbuotojo ženklo numerį. Lauke **Ženklo ID** įveskite reikšmę.
9. Pasirinkite **Įrašyti**.
10. Uždarykite puslapius **Darbuotojo informacija** ir **Darbuotojai**.

## <a name="assign-worker-to-device-group"></a>Priskirkite darbuotoją prie įrenginio grupės.
1. Eikite į **Gamybos kontrolė > Sąranka > Gamybos vykdymas > Konfigūruoti įrenginių užduoties kortelę**.
2. Pasirinkite **Įtraukti**.
3. Sąraše pasirinkite norimą vertinimo modelį. Šiame pavyzdyje pasirinkite **SHANNON**.
4. Pasirinkite **Gerai**.
5. Pasirinkite **Redaguoti**.
6. Lauke **Gamybos vienetas** galite nustatyti numatytąjį darbuotojo filtrą. Tai užtikrins, kad bus rodomos tik pasirinkto gamybos vieneto gamybos užduotys, kai darbuotojas prisiregistruoja prie įrenginio. Įvesti reikšmę.
7. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]