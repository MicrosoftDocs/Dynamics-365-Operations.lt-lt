---
title: Kelių lygių turtas
description: Šioje temoje paaiškinama, kaip kurti ir naikinti kelių lygių turtą.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f38253317ed8f06318fc501511ca5263a614e20
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783457"
---
# <a name="multi-level-assets"></a>Kelių lygių turtas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip kurti ir naikinti kelių lygių turtą. Galite kurti turtą ir susijusį antrinį turtą hierarchinėje medžio struktūroje. Tokiu būdu galite parodyti turto ryšius ir priklausomybes. Priežiūros užduotys gali būti susijusios su visais medžio struktūros lygiais. Statistiniai duomenys taip pat gali būti kuriami atskiram lygiui arba visų antrinio turto lygių sumai.

Puslapyje **All Assets** (**Asset management** \> **Common** \> **Assets** \> **All assets**), **Asset** skiltyje nurodomi turto hierarchine tvarka. Stulpelyje **Pirminis** rodomas susijęs pirminis. Be to, jei turtas ir antrinis turtas jau sukurti, srities **Susijusi informacija** sekcijoje **Turto medis** turtas rodomas medžio struktūroje.

Daugiau informacijos apie turto kūrimą ieškokite skyriuje [Turto kūrimas](../objects/create-an-object.md). Norėdami sukurti antrinį turtą, FastTab **Bendra** esančiame lauke **Pirminis** pasirinkite pirminį turtą.

## <a name="copy-an-asset-or-asset-structure"></a>Turto arba turto struktūros kopijavimas

Jei jūsų įmonėje yra keletas panašių turto struktūrų, galite naudoti modulio Turto valdymas funkciją Kopijuoti, kad greitai jas sukurtumėte.

1. Pasirinkite **Asset management** \> **Common** \> **Assets** \> **All assets**.
2. Sąrašo puslapyje **Visas turtas** pasirinkite norimą kopijuoti turtą. Pavyzdžiui, jei norite nukopijuoti visą turto struktūrą, įskaitant antrinį turtą, pasirinkite pirminį turtą.
3. Pasirinkite **Kopijuoti turtą**. Sekcijos **Kopijuoti iš** lauke **Turtas** nustatytas turtas, kurį pasirinkote sąrašo puslapyje.
4. Sekcijos **Kopijuoti į** lauke **Turtas** įveskite naujo turto pavadinimą.
5. Jei kuriamas turtas turėtų būti esamos turto struktūros dalis, sekcijos **Pirminis turtas** lauke **Turtas** pasirinkite pirminį ID.
6. Pasirinkite **Gerai**. Nauja turto struktūra rodoma sąrašo puslapyje **All assets**. Visi turto atributai, priežiūros planai ir priežiūros etapai, kurie yra susiję su nukopijuotu turtu, perkeliami į naują turtą arba turto struktūrą.

Kai kopijuojate turto struktūrą, antrinio turto pavadinimas naujoje struktūroje yra toks pat, kaip ir nukopijuoto antrinio turto pavadinimas. Kopijavimo procedūrai pasibaigus, galite lengvai pakeisti turto pavadinimą ir kitus parametrus. Sąrašo puslapyje **Visas turtas** pasirinkite turtą ir spustelėkite mygtuką **Redaguoti**.

> [!NOTE]
> Kai kopijuojate turtą arba turto struktūrą, naujo turto ciklo būsena nustatoma iš naujo į būseną, kurią apibrėžėte kaip pradinę turto ciklo būseną. Funkcinė vieta nustatoma iš naujo į numatytąją funkcinę vietą.

## <a name="delete-an-asset-or-asset-structure"></a>Turto arba turto struktūros naikinimas

Jei yra su turtu susijusio antrinio turto, jį galite panaikinti tik tada, jei jokiame turte neužregistruota priežiūros užklausų, užduočių pagal darbo užsakymus, užregistruotų gedimų arba būklės vertinimų.

1. Sąrašo puslapyje **Visas turtas** pasirinkite norimą naikinti turtą.
2. Pasirinkite **Naikinti**.

> [!NOTE]
> Jei negalite panaikinti turto vadovaudamiesi šia procedūra, kitas naikinimo būdas yra nustatyti turto ciklo būseną šiuo tikslu. Pavyzdžiui, puslapyje **Turto ciklo būsenos** galite nustatyti ciklo būseną **Nurašytas** arba **Panaikintas**.