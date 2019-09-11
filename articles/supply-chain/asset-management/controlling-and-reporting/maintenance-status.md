---
title: Priežiūros būsena
description: Šioje temoje aprašoma, kaip skaičiuoti priežiūros būseną skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918354"
---
# <a name="maintenance-status"></a>Priežiūros būsena

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Skiltyje Turto valdymas galite vykdyti skaičiavimus, norėdami matyti nurodyto laikotarpio naujų, aktyvių ir baigtų priežiūros užklausų, darbo užsakymų ir prižiūrimo turto prastovos veiklų apžvalgą. Tai pat galite matyti nurodyto laikotarpio baigtų sąlygų įvertinimų skaičių. Naudokite šį skaičiavimą peržiūrėti darbo krūvį, susijusį su gautinomis ir baigtomis priežiūros užklausomis ir darbo užsakymais.

## <a name="make-a-maintenance-status-calculation"></a>Vykdykite priežiūros būsenos skaičiavimą

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Priežiūros būsena**.

2. Dialogo lange **Apskaičiuoti būseną** pasirinkite laikotarpį, pagal kurį norite atlikti skaičiavimą, laukuose **Nuo datos** ir **Iki datos**.

3. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti priežiūros eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl būseną į eilutę galėsite įtraukti iš žemiau esančių funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, priežiūros eilutes.

4. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

5. Veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti veiksmų srities mygtukai yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

6. Nepamirškite spustelėti mygtuko **Naujinti**, kad skaičiavimai kiekvienąkart atsinaujintų, kai atliksite keitimus suaktyvindami arba išjungdami mygtukus **Grupuoti pagal...** arba atlikdami naujo laikotarpio skaičiavimą.

7. Spustelėkite **Būsena**, jei norite sukurti naują priežiūros būsenos skaičiavimą.

>[!NOTE]
>Skiltyje **Priežiūros būsena** rezultatai formuojami tik iš priežiūros užklausų ir darbo užsakymų, kurie turi faktinius pradžios datą ir laiką. Pabaigos data ir laikas gali būti tušti.

*1 pavyzdys:*

Toliau pateiktame paveikslėlyje yra suaktyvinti mygtukai **Metai** ir **Mėnuo**. Čia galite matyti bendrą mėnesinę darbo krūvio ir našumo, susijusio su priežiūros užklausomis ir darbo užsakymais, apžvalgą. 

![1 pav.](media/13-controlling-and-reporting.png)

*2 pavyzdys:*

Toliau pateiktame paveikslėlyje buvo įterpta informacija apie funkcines vietas. Dabar galite palyginti darbo krūvį ir našumą funkcinėse vietose, kuriose gali nurodyti geografines vietas, gamyklas arba darbo vietas. 

![2 paveikslėlis](media/14-controlling-and-reporting.png)

