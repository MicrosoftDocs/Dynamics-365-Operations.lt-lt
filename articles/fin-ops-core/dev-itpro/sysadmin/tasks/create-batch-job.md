---
title: Sukurkite paketinę užduotį
description: Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4903724adc9deaa40b6cd04c215273dd4b0522d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982531"
---
# <a name="create-a-batch-job"></a>Sukurkite paketinę užduotį

[!include [banner](../../includes/banner.md)]

Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė. Paketinės užduotys yra vykdomos naudojant užduotį sukūrusio naudotojo saugos kredencialus. Norėdami sukurti paketinę užduotį, naudokite nurodytą procedūrą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-the-batch-job"></a>Kurti paketinę užduotį
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.
2. Spustelėkite **Naujas**.
3. Lauke **Užduoties aprašas** įveskite reikšmę.
4. Lauke **Suplanuota pradžios data / laikas** įveskite datą ir laiką.
5. Spustelėkite **Įrašyti**.

## <a name="create-a-recurrence"></a>Kurti pasikartojimą
1. Veiksmų srityje spustelėkite **Paketinė užduotis**.
2. Spustelėkite **Pasikartojimas**. Naudokite šias parinktis, kad norėdami įvesti pasikartojimo diapazoną ir šabloną.  
3. Spustelėkite **Gerai**.

## <a name="add-alerts"></a>Įtraukti įspėjimų
1. Veiksmų srityje spustelėkite **Paketinė užduotis**.
2. Spustelėkite **Įspėjimai**. Nurodykite, ar norite, kad būtų siunčiami įspėjimo pranešimai, kai paketinė užduotis yra baigta, atšaukta arba kai iškyla klaida. Tada nurodykite, ar norite, kad įspėjimai būtų rodomi kaip iššokantieji pranešimai.   
3. Spustelėkite **Gerai**.

## <a name="adjust-batch-job-status"></a>Paketinės užduoties būsenos koregavimas
1. Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.
2. Pasirinkite atitinkamą paketinę užduotį.
3. Veiksmų srityje spustelėkite **Paketinė užduotis > Funkcijos > Keisti būseną**.
4. Pasirinkite atitinkamą būseną:
    - **Sulaikyti**: nustatykite paketinę užduotį kaip **sulaikytą**, kad užduotis būtų sulaikyta paketinių užduočių planuoklėje. Prilygsta *sustabdymui*.
    - **Laukiama**: nustatykite paketinę užduotį kaip **laukiančią**, kad jį būtų eilėje, kol ją paims paketinių užduočių planuoklę. Prilygsta *vykdymui*.
5. Spustelėkite **Gerai**.
