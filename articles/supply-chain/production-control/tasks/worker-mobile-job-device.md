---
title: Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį
description: Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.
author: ShylaThompson
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6e45ea8fdbe30436badd88d4972fda970755275
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835784"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Patikrinkite, ar darbuotojui priskirtas konkretus vaidmuo.

Pavyzdys: prieš sukonfigūruodami darbuotojo abonementą patikrinkite, ar vartotojui „SHANNON“ yra priskirtas mašinos operatoriaus vaidmuo.

1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.
2. Ieškokite vartojo naudodami spartųjį filtrą. Šiame pavyzdyje įveskite `shannon`.
3. Stulpelyje **Vartotojo ID** pasirinkite atsirandančios vartotojo paskyros saitą.
4. Medyje **User's roles** pasirinkit **Roles > Machine operator**.
5. Uždarykite puslapius **Vartotojo duomenys** ir **Vartotojai**, kad grįžtumėte į pradžios puslapį.

## <a name="configure-worker-account"></a>Konfigūruokite darbuotojo abonementą.
1. Eikite į **Naršymo sritis > Moduliai > Žmogiškieji ištekliai > Darbuotojai > Darbuotojai**.
2. Ieškokite vartojo naudodami spartųjį filtrą. Šiame pavyzdyje įveskite `shannon`.
3. Atsidariusiame vartotojo paskyros stulpelyje **Pavadinimas** pasirinkite saitą.
4. Pasirinkite skirtuką **Time registration**.
5. Pasirinkit **Activate on registration terminals**.
6. Šiuose laukuose pasirinkite vertes:  

    - **Skaičiavimo grupė**  
    - **Numatytoji skaičiavimo grupė**  
    - **Patvirtinimo grupė**  
    - **Standartinis šablonas**  
    - **Šablono grupė**  

7. Pasirinkite **Gerai**.
8. Spustelėję **Edit** įveskite naujos laiko registracijos darbuotojo ženklo numerį. Lauke **Badge ID** įveskite reikšmę.
9. Pasirinkite **Įrašyti**.
10. Uždarykite puslapius **Darbuotojo informacija** ir **Darbuotojai**.

## <a name="assign-worker-to-device-group"></a>Priskirkite darbuotoją prie įrenginio grupės.
1. Eikite į **Production control > Setup > Manufacturing execution > Configure job card for devices**.
2. Pasirinkite **Įtraukti**.
3. Sąraše pasirinkite norimą vertinimo modelį. Šiame pavyzdyje pasirinkite **SHANNON**.
4. Pasirinkite **Gerai**.
5. Pasirinkite **Redaguoti**.
6. Lauke **Production unit** galite nustatyti numatytąjį darbuotojo filtrą. Tai užtikrins, kad bus rodomos tik pasirinkto gamybos vieneto gamybos užduotys, kai darbuotojas prisiregistruoja prie įrenginio. Įvesti reikšmę.
7. Uždarykite puslapį.

