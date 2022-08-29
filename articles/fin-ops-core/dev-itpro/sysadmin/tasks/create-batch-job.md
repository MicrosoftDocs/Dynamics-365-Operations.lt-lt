---
title: Sukurkite paketinę užduotį
description: Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292457"
---
# <a name="create-a-batch-job"></a>Sukurkite paketinę užduotį

[!include [banner](../../includes/banner.md)]

Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė. Paketinės užduotys yra vykdomos naudojant užduotį sukūrusio naudotojo saugos kredencialus. Norėdami sukurti paketinę užduotį, naudokite nurodytą procedūrą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-the-batch-job"></a>Kurti paketinę užduotį
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.
2. Pasirinkite **Nauja**.
3. Užduoties **aprašymo** lauke įveskite paketinės užduoties aprašymą.
4. Lauke Suplanuota **pradžios data/ laikas** įveskite datą ir laiką, kada turėtų būti vykdoma paketinė užduotis.
5. Pasirinkite **Įrašyti**.

## <a name="create-a-recurrence"></a>Kurti pasikartojimą
1. Veiksmų srityje pasirinkite Paketinė **užduotis**.
2. Pasirinkite **Pasikartojimas**. Naudokite šias parinktis, kad norėdami įvesti pasikartojimo diapazoną ir šabloną.  
3. Pasirinkite **Gerai**.

## <a name="add-alerts"></a>Įtraukti įspėjimų
1. Veiksmų srityje pasirinkite Paketinė **užduotis**.
2. Pasirinkite **įspėjimus**. Nurodykite, ar norite, kad būtų siunčiami įspėjimo pranešimai, kai paketinė užduotis yra baigta, atšaukta arba kai iškyla klaida. Tada nurodykite, ar norite, kad įspėjimai būtų rodomi kaip iššokantieji pranešimai.   
3. Pasirinkite **Gerai**.

## <a name="add-a-task-to-a-batch-job"></a>Užduoties įtraukimas į paketinę užduotį
1.  Puslapyje Paketinės **užduotys** pasirinkite Peržiūrėti **užduotis**.
2.  Norėdami **sukurti užduotį, pasirinkite Ctrl+N**.
3.  Įvesti paketinės užduoties aprašymą.
4.  Lauke Įmonė **pasirinkite** įmonės duomenų bazę, kurioje turėtų būti vykdoma užduotis.
5.  Klasės pavadinimo **lauke** pasirinkite procesą, kurį turi paleisti užduotis. 
6.  Jei reikia, pasirinkite užduoties paketų grupę.

    Klientų užduotys turi būti priskirtos paketų grupei. Jos automatiškai priskiriamos numatytai paketų grupei (dar žinomai kaip Tuščio paketo grupė).

7.  Norėdami **įrašyti užduotį pasirinkite Ctrl+S**.
8.  Norėdami atlikti pasirinktą užduotį, priklausančią nuo kitos užduoties užduoties, **pasirinkite** Yra sąlygų tinklelis, tada kiekvienai sąlygai, kurią norite nustatyti, atlikite šiuos veiksmus:

    1. Norėdami **sukurti sąlygą, pasirinkite Ctrl+N**.
    2. Pasirinkite pirminės užduoties užduoties ID.
    3. Pasirinkite būseną, kurią pirminė užduotis turi pasiekti prieš tai, kol galės būti paleista priklausoma užduotis.
    4. Norėdami **įrašyti sąlygą pasirinkite Ctrl+S**.

    Jei apibrėžsite daugiau nei vieną sąlygą, *ir* jei visos sąlygos turi būti įvykdytos prieš tai, kol priklausoma užduotis galės būti paleista, pasirinkite sąlygos **tipą Visi**. Jei priklausoma užduotis gali būti vykdoma *,* kai visos sąlygos yra įvykdytos, pasirinkite sąlygos tipą **Bet kuris**.

9.  Pasirinkite, kaip turi būti apdorojamos užduočių klaidos. Norėdami nepaisyti konkrečios užduoties trikties, **skirtuke** Bendra pasirinkite **parinktį Nepaisyti užduoties trikties** tai užduočiai. Jei pažymėta ši pasirinktis, užduoties triktis nesutrikdo užduoties. Taip pat galite naudoti **lauką** Maksimalus kartojamas laikas, norėdami nurodyti užduoties kartotų skaičių, prieš tai, kai ji laikoma nepavykusi. Geriausia būtų nustatyti ne **daugiau** **kaip 5** lauko Maksimalus pašalinė vertė.

    Daugiau informacijos apie paketinį ret apdorojimą ieškokite Enable [batch retries](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Paketinės užduoties būsenos koregavimas
1. Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.
2. Pasirinkite atitinkamą paketinę užduotį.
3. Veiksmų srityje pasirinkite paketinės užduoties **elementą> keisti > būseną**.
4. Pasirinkite atitinkamą būseną:
    - **Sulaikyti**: nustatykite paketinę užduotį kaip **sulaikytą**, kad užduotis būtų sulaikyta paketinių užduočių planuoklėje. Prilygsta *sustabdymui*.
    - **Laukiama**: nustatykite paketinę užduotį kaip **laukiančią**, kad jį būtų eilėje, kol ją paims paketinių užduočių planuoklę. Prilygsta *vykdymui*.
5. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
