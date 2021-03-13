---
title: Sunaudojimo ataskaitų kūrimas
description: Šioje temoje aiškinama, kaip kurti sunaudojimo ataskaitas turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e32924c71fd221caee4a7f413908120014ec8c5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022538"
---
# <a name="create-consumption-reports"></a>Sunaudojimo ataskaitų kūrimas

[!include [banner](../../includes/banner.md)]

 

Kai sukūrėte ir užregistravote sunaudojimo registracijas darbo užsakymuose turto valdyme, prieinamos dvi ataskaitos, kuriose rodoma sunaudojimo išsami informacija.


## <a name="asset-consumption-report"></a>Turto sunaudojimo ataskaita

Kai užregistravote sunaudojimą darbo užsakymuose, galite atsispausdinti turto sunaudojimo ataskaitą. Šioje ataskaitoje rodomos valandos, valandos kaštai, elemento kaštai ir užregistruotos turto išlaidos.

1. Spustelėkite **Turto valdymas** > **Ataskaitos** > **Turtas** > **Turto sunaudojimas**.

2. Dialogo lange **Turto sunaudojimas** pažymėkite parametrus ir išsamumo lygį, kurį norite matyti, atitinkamuose perjungimo mygtukuose pažymėdami **Taip** ir įterpdami funkcinės vietos lygmenį dalyje **Rodyti**.
    - Galite naudoti lauką **Lygiai**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti turto eilutėse. 
    
        Pavyzdžiui, jei lauke įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visas turtas, skirtas funkcinei vietai, bus rodomas viršuje, todėl eilutę galėsite įtraukti iš žemesniame lygmenyje esančių funkcinių vietų. 
        
        Jei lauke **Lygiai** įrašysite skaičių „0“, matysite išsamų rezultatą, rodant visą turtą visuose funkcinių vietų lygiuose, su kuriais jis yra susijęs. 
        
    - Perjungimo mygtuke **Viso antrinio turto suma** pažymėkite **Taip**, kad ataskaitoje matytumėte kiekvieno antrinio turto sumą.

3. Skyriuje **Datos** pažymėkite datos intervalą.

4. „FastTab“ **Paskirtis** pažymėkite, ar norite, kad ataskaita būtų rodoma ekrane, norite ją spausdinti ar įrašyti kaip failą arba el. laišką.

5. Jei reikia, galite pažymėti ne vieną konkretų turtą, kuris būtų rodomas ataskaitoje. „FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir įtraukite turtą, kurį norite įtraukti į ataskaitą.

6. Spustelėkite **Gerai**, kad sugeneruotumėte ataskaitą.


## <a name="work-order-consumption-report"></a>Darbo užsakymo sunaudojimo ataskaita

Kai užregistravote sunaudojimą darbo užsakymuose, galite atsispausdinti darbo užsakymo sunaudojimo ataskaitą. Šioje ataskaitoje rodomos valandos, valandos kaštai, elemento kaštai ir užregistruoti darbo užsakymai.

1. Spustelėkite **Turto valdymas** > **Ataskaitos** > **Darbo užsakymai** > **Darbo užsakymo sunaudojimas**.

2. Dialogo lange **Darbo užsakymo sunaudojimas** pažymėkite parametrus, kuriuos norite įtraukti į ataskaitą, dalyje **Rodyti** atitinkamuose perjungimo mygtukuose pasirinkdami **Taip**.

3. Skyriuje **Datos** pažymėkite datos intervalą.

4. „FastTab“ **Paskirtis** pažymėkite, ar norite, kad ataskaita būtų rodoma ekrane, norite ją spausdinti ar įrašyti kaip failą arba el. laišką.

5. Jei reikia, galite pažymėti konkrečius darbo užsakymus, kurie būtų rodomi ataskaitoje. „FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir įtraukite darbo užsakymus, kuriuos norite įtraukti į ataskaitą.

6. Spustelėkite **Gerai**, kad sugeneruotumėte ataskaitą.


>[!NOTE]
>Taip pat galite generuoti [darbo užsakymo ataskaitą](../work-orders/work-order-report.md), kurioje pateikta daugiau išsamios informacijos apie darbo užsakymą.

