---
title: Darbo grafiko kūrimas bangos metu
description: Šioje temoje aprašoma, kaip nustatyti ir naudoti Darbo grafiko kūrimo bangos apdorojimo metodą.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078288"
---
# <a name="schedule-work-creation-during-wave"></a>Darbo grafiko kūrimas bangos metu

[!include [banner](../includes/banner.md)]

Naudokite funkciją *Darbo grafiko kūrimas* kaip jūsų bangos apdorojimo proceso dalį, kad padidintumėte bangos apdorojimo našumą, sistemoje sukurdami darbą naudojant lygiagretųjį apdorojimą.

Įgalinus funkciją, automatiškai sukuriamas suplanuotas darbas, kurį sistema galiausiai apdoros sukurti faktiniam darbui. Jei bangos įkelties eilučių skaičius pasiekia iš anksto nustatytą ribinę vertę, sistema sukurs faktinį darbą greičiau, pritaikydama lygiagretųjį asinchroninį apdorojimą.

## <a name="enable-the-schedule-work-creation-feature"></a>Darbo grafiko kūrimo funkcijos įgalinimas

### <a name="enable-the-feature-in-feature-management"></a>Funkcijos įjungimas funkcijų valdymo dalyje

Prieš jums naudojant *Darbo grafiko kūrimas* funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Darbo grafiko kūrimas*

> [!NOTE]
> Prieš įgalinant *Darbo grafiko kūrimą*, turite įgalinti *Visos organizacijos darbo blokavimo* funkciją.

### <a name="manually-enable-batch-processing-of-waves"></a>Paketinio bangų apdorojimo įjungimas rankiniu būdu

Norint pasinaudoti lygiagrečiu asinchroniniu metodu kurti sandėlio darbui, jūsų bangos procesas turi būti vykdomas pakete. Norėdami tai nustatyti:

1. Eikite į  **Sandėlio valdymas\> Sąranka \> Sandėlio valdymo parametrai**.

1. Skirtuke **Bendra** nustatykite **Apdoroti bangas pakete** į *Taip*. Pasirinktinai galite pasirinkti paskirtą **Bangos apdorojimo paketų grupę** sustabdyti paketų eilės apdorojimo vykdymą tuo pačiu, kaip ir kitų procesų vykdymo, laiku.

1. Nustatykite **Laukti užrakto (ms)**, kuris taikomas, kai sistema vienu metu apdoroja kelias bangas. Daugumai didesnių bangos procesų rekomenduojame vertę *60 000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Naujo bangos veiksmo metodo neautomatinis įjungimas esamiems bangos šablonams

Pradėkite sukurdami naują bangos veiksmo metodą ir įgalindami jį lygiagrečiam asinchroniniam užduoties apdorojimui.

1. Eikite į **Sandėlio valdymas \>Sąranka \> Bangos \> Bangos apdorojimo metodai**.

1. Pasirinkite  **Pakartotinio generavimo** metodą ir atkreipkite dėmesį, kad *„WHSScheduleWorkCreationWaveStepMethod”* buvo įtrauktas į bangos apdorojimo metodų, kuriuos galite naudoti jūsų siuntimo bangos šablonuose, sąrašą.

1. Pasirinkite įrašą su **Metodo pavadinimu** *„WHSScheduleWorkCreationWaveStepMethod”* ir pasirinkite **Užduoties konfigūraciją**.

1. Norėdami įtraukti naują eilutę į tinklelį, veiksmų srityje pasirinkite **Naujas** ir naudokite šiuos parametrus:

    - **Sandėlis** – pasirinkite sandėlį, kurį naudosite darbo grafiko kūrimo apdorojimui.

    - **Didžiausias paketinių užduočių skaičius** – nurodykite maksimalų paketinių užduočių skaičių. Daugeliu atvejų ši vertė turi būti diapazone 8‑16, tačiau patariame eksperimentuoti su optimaliu parametru, atsižvelgiant į jūsų scenarijus.

    - **Bangos apdorojimo paketų grupė** – pasirinkite paskirtą bangos apdorojimo paketų grupę, kad optimizuotumėte paketų darbo eilės apdorojimą.

Dabar esate pasiruošę atnaujinti esamą bangos šabloną (arba sukurti naują) ir naudoti *Darbo grafiko kūrimo* bangos apdorojimo metodą.

1. Eikite į  **Sandėlio valdymas\>Nustatymas \> Bangos \> Bangų šablonai**.

1. Pasirinkite **Redaguoti** veiksmų srityje.

1. Sąrašo srityje pasirinkite bangos šabloną, kurį norite atnaujinti (jei testuojate naudodami demonstracinius duomenis, tada galite naudoti *24 siuntimo numatytuosius parametrus*).

1. Išplėskite „FastTab” **Metodai** ir pasirinkite eilutę, su **Pavadinimu** *Darbo grafiko kūrimas* tinklelyje **Likę metodai**.

1. Pasirinkite rodyklę, nukreiptą į stulpelį **Pasirinkti metodai** perkelti pasirinktai eilutei į tą stulpelį. (Vienu metu galima pasirinkti tik vieną metodą, kuris naudoja *„WHSScheduleWorkCreationWaveStepMethod”* arba *„createWork”*, taigi, esama eilutė su **Metodo pavadinimu** *„createWork”* yra automatiškai perkeliama į **Likę metodai** tinklelį.)

## <a name="set-wave-task-processing-threshold-data"></a>Nustatykite bangos užduoties apdorojimo ribinės vertės duomenis

Sistema sukurs numatytuosius bangos užduoties apdorojimo ribinės vertės duomenis, kai pirmą kartą vykdomas bangos procesas naudojant bet kokį užduotimis pagrįstą apdorojimą. Duomenys yra naudojami valdymui, kai bangos apdorojimas bus vykdomas asinchroniškai ir bus pagrįstas užduotimis, o tai leidžia apdoroti ir kurti darbą lygiagrečiai.

Iš pradžių numatytieji duomenys naudos 15 ribinę vertę mažiausio krovinio eilučių skaičiaus („MINIMUMWAVELOADLINES”) atveju. Tai reiškia, kad kai sistema apdoros bangą su daugiau nei 15 įkelties eilučių, ji naudos asinchroninį užduoties apdorojimą. Galite rankiniu būdu įterpti/atnaujinti šiuos duomenis **„WHSWaveTaskProcessingThresholdParameters”** lentelėje jūsų bandymo aplinkose, tačiau, jeigu jums reikia pakeisti šį parametrą gamybos aplinkoje, turite susisiekti su „Microsoft” palaikymo tarnyba ir paprašyti atnaujinimo.

## <a name="work-with-the-feature"></a>Darbas su funkcija

Kai *Darbo grafiko kūrimo* funkcija yra įjungta, bangos apdorojimas sukurs suplanuotą darbą, kuris galiausiai bus panaudotas naujo darbo kūrimo procese. Darbo kūrimo metu darbas bus užblokuotas, naudojant *Visos organizacijos darbo blokavimo* funkciją.

Šiose struktūrinėse schemose parodyta, kaip bangos apdorojimo metu sukuriamas suplanuotas darbas.

![Darbo grafiko kūrimas](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Suplanuotas Darbas

Puslapyje **Suplanuoto darbo informacija** (**Sandėlio valdymas \> Darbas \> Suplanuoto darbo informacija**) rodoma informacija apie suplanuotą darbą, kuris iš pradžių yra sukuriamas bangos apdorojimo metu. Galimos šios **Apdorojimo būsenos** reikšmės:

- **Eilėje** – laukiama, kada suplanuotas darbas bus panaudotas darbui sukurti.
- **Užbaigta** – suplanuotas darbas buvo panaudotas darbui sukurti.
- **Nepavyko** – bangos apdorojimas nepavyko. Atkreipkite dėmesį, kad suplanuoto darbo būsena gali būti **Nepavyko** su susijusiu faktiniu darbu arba be jo. Kai faktinio darbo kūrimo procesas nepavyksta, faktinio darbo būsena lieka *Atšaukta*.

### <a name="batch-job-for-the-work-creation-process"></a>Paketinė užduotis darbo kūrimo procesui

Norėdami peržiūrėti paketines užduotis bangų apdorojimui pasirinkite **Paketines užduotis** veiksmų srityje, **Visos bangos** puslapyje.

Čia galite peržiūrėti visą paketinės užduoties informaciją apie kiekvieną paketinės užduoties ID.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]