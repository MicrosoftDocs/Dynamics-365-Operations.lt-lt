---
title: Remonto valdymas
description: Sistematiškai grupuokite problemas – tai padės rasti sprendimus, sėkmingai panaudotus anksčiau.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d45732ff35069a64b37b6c53d9e22adf9a9a46d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975613"
---
# <a name="repair-management"></a>Remonto valdymas       

[!include [banner](../includes/banner.md)]


Remonto valdymo tikslais problemas galite grupuoti sistematiškai. Tai padės rasti sprendimus, sėkmingai panaudotus anksčiau.

Galite nustatyti požymių, diagnozės ir sprendimo parametrus. Visus juos bus galima pritaikyti vėliau, kai prireiks taisyti panašią prekę. Taip pat galite nustatyti remonto etapus, kurie gali sekti remonto eigą.

## <a name="setting-up-repair-management"></a>Remonto valdymo nustatymas

Toliau pateiktose nustatymo formose Įveskite informaciją, kuri bus naudojama nurodant remonto požymius, diagnozę ir sprendimą.

1.  Spustelėkite **Aptarnavimo valdymas** \> **Nustatymas** \> **Remontas** \> **Sąlygos**.

2.  Spustelėkite **Aptarnavimo valdymas** \> **Nustatymas** \> **Remontas** \> **Požymių sritys**.

3.  Spustelėkite **Aptarnavimo valdymas** \> **Nustatymas** \> **Remontas** \> **Diagnozės sritys**.

4.  Spustelėkite **Aptarnavimo valdymas** \> **Nustatymas** \> **Remontas** \> **Sprendimai**.

5.  Spustelėkite **Aptarnavimo valdymas** \> **Nustatymas** \> **Remontas** \> **Remonto etapai**.

## <a name="symptoms-and-conditions"></a>Požymiai ir sąlygos

Požymiai yra tai, kaip klientas apibūdina problemą. Požymiai apima kliento pastebėjimus, leidžiančius manyti, jog reikalingas remontas.

Jūs galite nustatyti požymių sritis, požymių kodus ir sąlygas. Požymių sritis nurodo trikčių sritį, o požymio kodas nurodo trikties požymį. Sąlyga aprašo situaciją arba aplinką, kurioje iškilo problema.

**Pavyzdys**

Kompiuteris atvežamas taisyti, nes po ilgo naudojimo įvyksta jo kietojo disko triktis. Kietojo disko triktis sukelia mėlyno ekrano klaidą. Technikas, kuris gauna kompiuterį, įveda šiuos požymius ir sąlygas:

1.  Požymių sritis yra kietasis diskas

2.  Požymio kodas yra mėlyno ekrano klaida

3.  Sąlyga – kietojo disko triktis įvyksta po ilgo naudojimo

## <a name="diagnosis-and-resolutions"></a>Diagnozė ir sprendimai

Diagnozės ir sprendimo laukai yra išrašai iš remonto veiksmų. Tai yra žingsniai, kurios technikas atliko spręsdamas problemą.

Diagnozės sritis apima veiksmą, kurį reikia atlikti siekiant išspręsti problemą. Diagnozės kodas yra tai, kaip buvo dorojamasi su problema, o sprendimas galėtų būti tai, kad prekė buvo taisoma, pakeista kita arba užsakymas buvo atšauktas kliento. Pavyzdžiui, jei kompiuteris yra taisomas, diagnozės sritis galėtų būti „defektą turinti prekė“, diagnozės kodas galėtų būti „įdiegta nauja vaizdo plokštė“, o sprendimas galėtų būti „pakeista“.

## <a name="repair-stages"></a>Remonto etapai

Remonto etapai nurodo remonto proceso eigą. Remonto etapas turi išsiregistravimo parametrą **Baigta**, kuris nurodo, kad remonto eilutė buvo užbaigta, taip pat baigimo datą ir įrašymo laiką.

## <a name="applying-repair-management"></a>Remonto valdymo taikymas

Jei norite taikyti remonto valdymą prekei, aptarnavimo užsakyme prekė turi būti nustatyta su aptarnavimo objekto ryšiu. Iš aptarnavimo užsakymo galite sukurti remonto eilutę, kurioje būtų pateikta informacija apie dabartinį triktį. Remonto eilutėje nurodomas remontuojamas aptarnavimo objektas ir informacija apie požymius, diagnozę ir vykdymą. Jūs taip pat galite sukurti pastabą remonto eilutei.

Remonto eilutes galite kurti kiekvienam remonto proceso žingsniui.

## <a name="create-a-repair-line-on-a-service-order"></a>Aptarnavimo užsakymo remonto eilutės kūrimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.

2.  Pasirinkite aptarnavimo užsakymą su aptarnavimo objektu, kuriam reikia remonto.

3.  Spustelėkite **Remontas** \> **Remonto eilutės**, kad atidarytumėte formą **Remonto eilutės**.

4.  Paspauskite Ctrl+N, kad sukurtumėte naują eilutę.

5.  Pasirinkite aptarnavimo objektą. Jūs galite pasirinkti bet kurį aptarnavimo objektą, kuris aptarnavimo užsakyme buvo nustatytas su objekto ryšiu.

6.  Remonto eilutėje pasirinkite bet kuriuos reikiamus iš anksto nustatytus požymius, diagnozes ir vykdymo vertes, tada spustelėję skirtuką **Pastaba** remonto eilutėje sukurkite pastabą (jei reikia).

7.  Norėdami išsaugoti naują remonto eilutę, paspauskite CTRL+S. Formos **Remonto eilutės** skirtuke **Bendra** esančiame lauke **Sukūrimo data ir laikas** atnaujinamas įrašymo laikas.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Remonto eigos sekimas ir problemos sprendimas

Galite nustatyti, kad remonto eilutės remonto etapuose būtų sekama remonto eiga.

Pašalinus problemą, remonto eilutę galima uždaryti. Nustatykite remonto etapą su įjungta ypatybe **Baigta**. Esama data ir laikas yra užregistruojami eilutėje kaip baigimo laikas.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Pašalinto trikčio remonto eilutės uždarymas

1.  Atidarykite formą **Remonto eilutės**. Sukurkite remonto eilutę atlikdami ankstesnėje šios temos dalyje nurodytą procedūrą.

2.  Pasirinkite norimą uždaryti remonto eilutę, kurioje pateiktas trikčio remontas.

3.  Lauke **Remonto etapas** pasirinkite etapą su įjungta ypatybe **Baigta**.

  


