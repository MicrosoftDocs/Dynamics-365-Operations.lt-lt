---
title: Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį
description: Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89b75936ea9c0f25f82175a1871088da8fd74ad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980936"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.

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