---
title: Konfigūruoti darbuotoją naudojant mobilųjį užduoties įrenginį
description: Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "327394"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigūruoti darbuotoją naudojant mobilųjį užduoties įrenginį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.


## <a name="assign-roles-to-user-account"></a>Priskirti vaidmenis vartotojo abonementui
1. Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.
2. Naudokite Spartųjį filtrą darbuotojo vardui filtruoti, kai vartotojo abonementas yra susietas su mašinų operatorius vaidmeniu. Demonstraciniuose duomenyse vardas yra Shannon.
3. Pažymėkite vartotojo abonemento įrašą.
4. Sąraše spustelėję nuorodą „Pavadinimas“ pasirinktoje eilutėje peržiūrėkite vartotojo abonemento informaciją.
5. Medyje pasirinkite 'vaidmenys \ mašinos operatorius'.
6. Uždarykite vartotojo abonemento informacijos puslapį.
7. Uždarykite puslapį.

## <a name="configure-worker-account"></a>Konfigūruokite darbuotojo abonementą.
1. Pasirinkite Personalas > Darbuotojai > Darbuotojai.
2. Naudokite Spartųjį filtrą darbuotojo vardui filtruoti, kai vartotojo abonementas yra susietas su mašinų operatorius vaidmeniu. Demonstraciniuose duomenyse vardas yra Shannon.
3. Pažymėkite vartotojo abonemento įrašą.
4. Sąraše spustelėję nuorodą „Pavadinimas“ pasirinktoje eilutėje peržiūrėkite vartotojo abonemento informaciją.
5. Spustelėkite skirtuką Užimtumas.
6. Išplėskite Laiko registravimo „FastTab“ ir registracijos terminaluose spustelėkite Aktyvinti.
7. Spustelėkite Suaktyvinti registravimo terminaluose.
8. Lauke Skaičiavimo grupė įveskite arba pasirinkite vertę.
9. Lauke Numatytoji skaičiavimo grupė įveskite arba pasirinkite vertę.
10. Lauke Patvirtinimo grupė įveskite arba pasirinkite vertę.
11. Lauke Standartinis profilis įveskite arba pasirinkite vertę.
12. Lauke Profilio grupė įveskite arba pasirinkite vertę.
13. Spustelėkite Gerai.
14. Spustelėję Redaguoti įveskite naujos laiko registracijos darbuotojo ženklo numerį.
15. Lauke Ženklo ID įveskite vertę.
16. Spustelėkite Įrašyti.
17. Naudokite nuorodą „SaveRecord“.
18. Uždarykite darbuotojo informacijos puslapį.
19. Uždarykite puslapį.

## <a name="assign-worker-to-device-group"></a>Priskirkite darbuotoją prie įrenginio grupės.
1. Pasirinkite Gamybos kontrolė > Nustatymas > Gamybos vykdymas > Konfigūruoti užduoties kortelę įrenginiams.
2. Spustelėkite Pridėti.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Spustelėkite GERAI.
5. Spustelėkite Redaguoti.
6. Lauke Gamybos vienetas galite nustatyti numatytąjį darbuotojo filtrą. Tai užtikrins, kad bus rodomos tik pasirinkto gamybos vieneto gamybos užduotys, kai darbuotojas prisiregistruoja prie įrenginio.
7. Uždarykite puslapį.

