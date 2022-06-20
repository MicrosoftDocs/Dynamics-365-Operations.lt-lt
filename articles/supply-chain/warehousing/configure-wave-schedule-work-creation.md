---
title: Darbo grafiko kūrimas bangos metu
description: Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti darbo planavimo darbo kūrimo bangos apdorojimo metodą.
author: Mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8b4505d66c37134bc8f672b38d195f4f677df9bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852076"
---
# <a name="schedule-work-creation-during-wave"></a>Darbo grafiko kūrimas bangos metu

[!include [banner](../../includes/banner.md)]

Naudokite funkciją *Darbo grafiko kūrimas* kaip jūsų bangos apdorojimo proceso dalį, kad padidintumėte bangos apdorojimo našumą, sistemoje sukurdami darbą naudojant lygiagretųjį apdorojimą.

Įgalinus funkciją, automatiškai sukuriamas suplanuotas darbas, kurį sistema galiausiai apdoros sukurti faktiniam darbui. Jei bangos įkelties eilučių skaičius pasiekia iš anksto nustatytą ribinę vertę, sistema sukurs faktinį darbą greičiau, pritaikydama lygiagretųjį asinchroninį apdorojimą.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Suplanuoto darbo kūrimo funkcijų įjungimas funkcijų valdyme

Norint naudoti šiame straipsnyje aprašytas funkcijas, jos turi būti įjungti jūsų sistemai. Naudokite darbo sritį [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungti šias funkcijas pateikta tvarka:

1. **Visos organizacijos darbo blokavimas** – Reikalingas tiek rankiniam, tiek automatiniam suplanuoto darbo kūrimo konfigūravimui. (Kaip ir tiekimo grandinės valdymo versija 10.0.21, ši funkcija yra privaloma, todėl ji įjungta pagal numatytuosius nustatymus ir jos negalima išjungti dar kartą.)
1. **Suplanuoto darbo kūrimas** – Reikalingas tiek rankiniam, tiek automatiniam suplanuoto darbo kūrimo konfigūravimui.
1. **Visos organizacijos „Suplanuoto darbo kūrimo” bangos metodas** – Reikalingas automatiniam suplanuoto darbo kūrimo konfigūravimui. Jums šios funkcijos nereikia, jeigu naudosite tik neautomatinį konfigūravimą.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Suplanuoto darbo kūrimo automatinis konfigūravimas

Jeigu įgalinate *Visos organizacijos „Suplanuoto darbo kūrimo” bangos metodo* funkciją, jūsų sistemoje automatiškai atsiranda:

- Bangos metodas *Suplanuoto darbo kūrimas*(`WHSScheduleWorkCreationWaveStepMethod`) yra įtraukiamas ir sukonfigūruojamas veikti lygiagrečiai visuose juridiniuose subjektuose.
- Bangoms šablonams iš visų juridinių subjektų, kurių **Bangos šablono tipas** nustatytas į *Siuntimas* ir **Šablono būsena** nustatyta į *Tinkama*, bus pakeistas metodas *Darbo kūrimas* į metodą *Suplanuoto darbo kūrimas*. Tačiau bangos šablonai iš juridinių subjektų, kuriuose metodą *Darbo kūrimas* leidžiama kartoti, nebus modifikuoti.
- Metodo *Suplanuoto darbo kūrimas* užduočių konfigūracijos bus sukurtos visiems sandėliams iš visų juridinių subjektų, kuriuose įjungta **Naudoti sandėlio valdymo procesus** funkcija. Tai reiškia, kad pagal numatytuosius nustatymus, metodas *Suplanuoto darbo kūrimas* bus vykdomas lygiagrečiai. Esami sandėliai, kuriems funkciją **Naudoti sandėlio valdymo procesus** pakeičiate iš *Ne* į *Taip*, taip bus vykdys šį metodą lygiagrečiai pagal numatytuosius nustatymus.
- Visi juridiniai subjektai apdoros bangas paketais ir **Laukti užrakto (ms)** bus nustatyta į numatytąją reikšmę *60 000* ms, jeigu anksčiau ji buvo nustatyta *į 0* ms.
- Visi jūsų naujai sukurti bangos šablonams turės *Suplanuoto darbo kūrimo* metodą, o ne *Darbo kūrimo* metodą.

Taip pat, esamos užduočių ir bangų apdorojimo konfigūracijos bus išlaikytos visiems juridiniams subjektams, kurie jau yra sukonfigūruoti bangų apdorojimui paketais, ir visiems sandėliams, kurie jau yra sukonfigūruoti lygiagrečiam *Suplanuoto darbo kūrimo* metodo naudojimui.

Jei reikia, galite toliau pateiktu rankiniu būdu grąžinti bet kuriuos arba visus parametrus, sukurtus automatiniu būdu, kai įgalinote *Visos organizacijos suplanuoto darbo kūrimo bangos metodo* funkciją:

- Bangos šablonus rasite **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**. Pakeisti *Suplanuoto darbo kūrimo* metodą į *Darbo kūrimo*.
- Sandėlio parametrų eikite į Sandėlio **valdymo nustatymo \>\> sandėlio valdymo parametrus**. Skirtuke **Bangos apdorojimas** taikykite pageidaujamas funkcijų **Bangų apdorojimas paketais** ir **Laukite užrakto (ms)** reikšmes.
- Bangos metodus rasite **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**. Pasirinkite „`WHSScheduleWorkCreationWaveStepMethod`” ir veiksmų srityje pažymėkite **Užduoties konfigūracija**. Jeigu reikia, modifikuokite arba panaikinkite kiekvieno sandėlio paketinių užduočių skaičių ir priskirtą bangos grupę.

## <a name="manually-configure-scheduled-work-creation"></a>Suplanuoto darbo kūrimo konfigūravimas rankiniu būdu

Jeigu neįgalinote [*Visos organizacijos „Suplanuoto darbo kūrimo” bangos metodo* funkcijos](#Auto-enable-schedule-work-creation), tada galite naudoti šiame skyriuje pateiktas procedūras, skirtas sukonfigūruoti jums reikiamo suplanuoto darbo kūrimą.

### <a name="manually-enable-batch-processing-of-waves"></a>Paketinio bangų apdorojimo įjungimas rankiniu būdu

Norint pasinaudoti lygiagrečiu asinchroniniu metodu kurti sandėlio darbui, jūsų bangos procesas turi būti vykdomas pakete. Norėdami tai nustatyti:

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Skirtuke **Bendra** nustatykite **Apdoroti bangas pakete** į *Taip*. Pasirinktinai galite pasirinkti paskirtą **Bangos apdorojimo paketų grupę** sustabdyti paketų eilės apdorojimo vykdymą tuo pačiu, kaip ir kitų procesų vykdymo, laiku.
1. Nustatykite **Laukti užrakto (ms)**, kuris taikomas, kai sistema vienu metu apdoroja kelias bangas. Daugumai didesnių bangos procesų rekomenduojame vertę *60 000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Naujo bangos veiksmo metodo neautomatinis įjungimas esamiems bangos šablonams

Pradėkite sukurdami naują bangos veiksmo metodą ir įgalindami jį lygiagrečiam asinchroniniam užduoties apdorojimui.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.
1. Pasirinkite **iš naujo nustatymo** *metodą ir atkreipkite dėmesį, kad WHSScheduleWorkCreationWaveStepMethod* buvo įtrauktas į bangos proceso metodų, kuriuos galite naudoti siuntimo bangos šablonuose, sąrašą.
1. Pasirinkite įrašą su **Metodo pavadinimu** *„WHSScheduleWorkCreationWaveStepMethod”* ir pasirinkite **Užduoties konfigūraciją**.
1. Norėdami įtraukti naują eilutę į tinklelį, veiksmų srityje pasirinkite **Naujas** ir naudokite šiuos parametrus:

    - **Sandėlis** – pasirinkite sandėlį, kurį naudosite darbo grafiko kūrimo apdorojimui.
    - **Didžiausias paketinių užduočių skaičius** – nurodykite maksimalų paketinių užduočių skaičių. Daugeliu atvejų ši vertė turi būti diapazone 8‑16, tačiau patariame eksperimentuoti su optimaliu parametru, atsižvelgiant į jūsų scenarijus.
    - **Bangos apdorojimo paketų grupė** – pasirinkite paskirtą bangos apdorojimo paketų grupę, kad optimizuotumėte paketų darbo eilės apdorojimą.

Dabar esate pasiruošę atnaujinti esamą bangos šabloną (arba sukurti naują) ir naudoti *Darbo grafiko kūrimo* bangos apdorojimo metodą.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Pasirinkite **Redaguoti** veiksmų srityje.
1. Sąrašo srityje pasirinkite bangos šabloną, kurį norite atnaujinti (jei testuojate naudodami demonstracinius duomenis, tada galite naudoti *24 siuntimo numatytuosius parametrus*).
1. Išplėskite „FastTab” **Metodai** ir pasirinkite eilutę, su **Pavadinimu** *Darbo grafiko kūrimas* tinklelyje **Likę metodai**.
1. Pasirinkite rodyklę, nukreiptą į stulpelį **Pasirinkti metodai** perkelti pasirinktai eilutei į tą stulpelį. (Vienu metu galima pasirinkti tik vieną metodą, kuris naudoja „`WHSScheduleWorkCreationWaveStepMethod`” arba „`createWork`”, taigi, esama eilutė su **Metodo pavadinimu** „`createWork`” yra automatiškai perkeliama į tinklelį **Likę metodai**.)

## <a name="set-wave-task-processing-threshold-data"></a>Nustatykite bangos užduoties apdorojimo ribinės vertės duomenis

Sistema sukurs numatytuosius bangos užduoties apdorojimo ribinės vertės duomenis, kai pirmą kartą vykdomas bangos procesas naudojant bet kokį užduotimis pagrįstą apdorojimą. Duomenys yra naudojami valdymui, kai bangos apdorojimas bus vykdomas asinchroniškai ir bus pagrįstas užduotimis, o tai leidžia apdoroti ir kurti darbą lygiagrečiai.

Iš pradžių numatytieji duomenys naudos 15 kaip ribinę mažiausio krovinio eilučių skaičiaus („`MINIMUMWAVELOADLINES`”) vertę. Tai reiškia, kad kai sistema apdoros bangą su daugiau nei 15 įkelties eilučių, ji naudos asinchroninį užduoties apdorojimą. Galite rankiniu būdu įterpti arba atnaujinti šiuos duomenis „`WHSWaveTaskProcessingThresholdParameters`” lentelėje savo testavimo aplinkose. Jeigu jums reikia pakeisti šį parametrą gamybos aplinkoje, turite kreiptis į „Microsoft“ palaikymo tarnybą ir pateikti užklausą naujinimui.

## <a name="work-with-the-scheduled-work-creation"></a>Darbas su Suplanuoto darbo kūrimo funkcija

Išsamesnės informacijos apie tai, kaip dirbti su Suplanuoto darbo kūrimo funkciją, rasite [Bangos kūrimas ir apdorojimas](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
