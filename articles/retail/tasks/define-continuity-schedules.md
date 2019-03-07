---
title: " Nustatyti tęstinumo grafikus"
description: Šioje temoje parodoma, kaip nustatyti tęstinumo programą (dar vadinamą pasikartojančiais užsakymais).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd70780927bb9aaa19c196705d6e8fa1c247ea66
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "330522"
---
# <a name="define-continuity-schedules"></a> Nustatyti tęstinumo grafikus

[!include[task guide banner](../includes/task-guide-banner.md)]

Šioje temoje parodoma, kaip nustatyti tęstinumo programą (dar vadinamą pasikartojančiais užsakymais). Šioje temoje naudojama demonstracinių duomenų įmonė USRT.


## <a name="create-continuity-program"></a>Tęstinumo programos kūrimas
1. Pasirinkite Mažmeninė prekyba ir prekyba > Tęstinumas > Tęstinumo programos.
2. Spustelėkite Naujas.
3. Lauke Grafiko ID įveskite tęstinumo grafiko ID.
4. Lauke Užsakymo pradžia pasirinkite Pirmasis įvykis.
    * Jei klientas pateikia naują užsakymą tęstinumo programai, yra dvi parinktys, kuris produktas bus siunčiamas: 1. Pirmas įvykis: bus siunčiamas pirmas tęstinumo programos produktas.  2. Dabartinis įvykis: bus siunčiamas pirmasis tęstinumo programos produktas. 2) Dabartinis įvykis: bus siunčiamas dabartinis produktas. Pavyzdys: praėjus trims mėnesiams nuo programos pradžios, klientas gaus trečiąjį programos produktą.  
5. Pasirinkite Taip, norite paraginti nurodyti užsakymo pradžios datą.
6. Spustelėkite Pridėti eilutę.
7. Lauke Prekės numeris įveskite pirmojo produkto (0013) prekės numerį.
8. Įveskite CP.
9. Įveskite datą, kada pirmąjį produktą bus galima užsisakyti.
10. Spustelėkite Pridėti eilutę.
11. Lauke Prekės numeris įveskite „0014“.
12. Išvalykite lauko Datų intervalo kodas reikšmę, kad jis būtų tuščias.
    * Atlikdami šią procedūrą, išvalykite datų intervalą. Galite nustatyti, kad datos reikšmė didėtų skaičiuojant nuo pirmosios prekės pradžios datos.  
13. Čia galite įvesti intervalą, kuriuo siunčiami produktai. Įveskite 30.
    * Jei programa trunka mėnesį, įveskite 30 dienų intervalą.  
14. Spustelėkite Pridėti eilutę.
15. Lauke Prekės numeris įveskite „0015“.
16. Įveskite Baigti.
17. Spustelėkite Įrašyti.

## <a name="assign-to-continuity-item"></a>Tęstinumo prekės priskyrimas
1. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
2. Pasirinkite prekę 0016.
    * Atlikdami šią procedūrą, pasirinkite prekės numerį 0016. Įprastai jūs sukursite patvirtintą produktą, kuriam taikoma papildoma tęstinumo verslo logika, kai jis pateikiamas skambučių centro pardavimo užsakyme.  
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite Redaguoti.
5. Išplėskite arba sutraukite skyrių Parduoti.
6. Čia galite įvesti tęstinumo programą, kurią ši prekė nurodo. Įveskite tvarkaraščio ID, kurį sukūrėte anksčiau.
    * Kai ši prekė parduodama skambučių centre, taikoma papildoma verslo logika iš pasirinktos tęstinumo programos.  
7. Spustelėkite Įrašyti.

