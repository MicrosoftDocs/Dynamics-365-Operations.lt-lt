---
title: Sunaudojimo ataskaitų kūrimas
description: Šioje temoje aiškinama, kaip kurti sunaudojimo ataskaitas turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: 3d978f8b991211e477dd8f766fe67432d9d493d0
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913100"
---
# <a name="create-consumption-reports"></a>Sunaudojimo ataskaitų kūrimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kai sukūrėte ir užregistravote sunaudojimo registracijas darbo užsakymuose turto valdyme, prieinamos dvi ataskaitos, kuriose rodoma sunaudojimo išsami informacija.


## <a name="asset-consumption-report"></a>Turto sunaudojimo ataskaita

Kai užregistravote sunaudojimą darbo užsakymuose, galite atsispausdinti turto sunaudojimo ataskaitą. Šioje ataskaitoje rodomos valandos, valandos kaštai, elemento kaštai ir užregistruotos turto išlaidos.

1. Spustelėkite **Turto valdymas** > **Ataskaitos** > **Turtas** > **Turto sunaudojimas**.

2. Dialogo lange **Turto sunaudojimas** pažymėkite parametrus ir išsamumo lygį, kurį norite matyti atitinkamuose perjungimo mygtukuose pažymėdami Taip ir įterpdami funkcinės vietos lygmenį skyriuje **Rodyti**.
    - Galite naudoti lauką **Lygiai**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti turto eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visas, skirtas funkcinei vietai, bus rodomos viršuje, todėl eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. Jei lauke **Lygiai** įrašysite skaičių „0“, matysite išsamų rezultatą, rodantį visą turtą visuose funkcinių vietų lygiuose, su kuriais jos yra susijusios. 
    - Perjungimo mygtuke **Viso antrinio turto suma** pažymėkite Taip, kad ataskaitoje matytumėte kiekvieno antrinio turto sumą.

3. Skyriuje **Datos** pažymėkite datos intervalą.

4. „FastTab“ **Paskirtis** pažymėkite, ar norite, kad ataskaita būtų rodoma ekrane, norite ją spausdinti ar įrašyti kaip failą arba el. laišką.

5. Jei reikia, galite pažymėti ne vieną konkretų turtą, kuris būtų rodomas ataskaitoje. „FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir įtraukite turtą, kurį norite įtraukti į ataskaitą.

6. Spustelėkite **Gerai**, kad sugeneruotumėte ataskaitą.


## <a name="work-order-consumption-report"></a>Darbo užsakymo sunaudojimo ataskaita

Kai užregistravote sunaudojimą darbo užsakymuose, galite atsispausdinti darbo užsakymo sunaudojimo ataskaitą. Šioje ataskaitoje rodomos valandos, valandos kaštai, elemento kaštai ir užregistruoti darbo užsakymai.

1. Spustelėkite **Turto valdymas** > **Ataskaitos** > **Darbo užsakymai** > **Darbo užsakymo sunaudojimas**.

2. Dialogo lange **Darbo užsakymo sunaudojimas** pažymėkite parametrus, kuriuos norite įtraukti į ataskaitą, skyriuje **Rodyti** atitinkamuose perjungimo mygtukuose pažymėdami Taip.

3. Skyriuje **Datos** pažymėkite datos intervalą.

4. „FastTab“ **Paskirtis** pažymėkite, ar norite, kad ataskaita būtų rodoma ekrane, norite ją spausdinti ar įrašyti kaip failą arba el. laišką.

5. Jei reikia, galite pažymėti konkrečius darbo užsakymus, kurie būtų rodomi ataskaitoje. „FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir įtraukite darbo užsakymus, kuriuos norite įtraukti į ataskaitą.

6. Spustelėkite **Gerai**, kad sugeneruotumėte ataskaitą.


>[!NOTE]
>Taip pat galite generuoti [darbo užsakymo ataskaitą](../work-orders/work-order-report.md), kurioje pateikta daugiau išsamios informacijos apie darbo užsakymą.

