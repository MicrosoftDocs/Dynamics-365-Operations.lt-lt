---
title: Turto klaidų analizė
description: Šioje temoje aiškinama turto gedimų analizė turto valdyme.
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
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918446"
---
# <a name="asset-fault-analysis"></a>Turto klaidų analizė

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Turto valdyme galite analizuoti turto gedimų registracijas, kad galėtumėte peržiūrėti bendrą konkrečiu laikotarpiu užregistruotų gedimų skaičių. Gedimų registracijas galima analizuoti skirtingais būdais, pavyzdžiui, pagal turtą, turto tipus, funkcines vietas, gedimo požymius ar gedimų tipus.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimo analizė**.

2. Dialoge lange **Turto gedimo analizės skaičiavimas** galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti turto gedimo eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos turto gedimo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, turto gedimo eilutes.

3. Jei norite apriboti iešką, „FastTab“ **Įtrauktini įrašai** galite pažymėti konkretų turtą, gedimų datas, gedimo priežastis ir gedimo šalinimo priemones.

4. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

5. Skirtuke **Turto gedimo analizė** veiksmų srities grupėse **Grupuoti pagal...** spustelėkite vieną ar kelis mygtukus, kad būtų rodoma lygio, kurį norite matyti, išsami informacija. Suaktyvinti mygtukai yra paryškinti. Suaktyvinkite arba deaktyvinkite mygtukus juos spustelėdami.

6. Spustelėkite **Naujinti skaičiavimus**, kad pasirinkimai būtų rodomi ekrane. 

>[!NOTE]
>Kiekvieną kartą, kai veiksmų srities grupėse **Grupuoti pagal...** suaktyvinate arba deaktyvinate mygtukus, pakeitę pasirinkimus spustelėkite mygtuką **Naujinti skaičiavimus**. Taip reikia, nes kai perskaičiuojama gedimo tikimybė, apdorojamas didelis kiekis duomenų.

Yra daug būdų, kaip analizuoti gedimų registracijas. Toliau penkiose ekrano kopijose pateikti pavyzdžiai, kaip pagal skirtingus duomenų pasirinkimus pateikiama skirtinga informacija. Pamatysite, kaip, analizuojant turto gedimų registracijas, pagal skirtingus pasirinkimus suteikiama daugiau įžvalgos ir informacijos.

Toliau pateiktoje ekrano kopijoje pažymėtas tik mygtukas **Požymis**.

- Gedimo registracijos atliktos pagal tris gedimo požymius: „Oro nuotėkis“, „Perdegęs saugiklis“ ir „Užstrigo įranga“.  
- Stulpelyje **Tikimybės %** visi procentai sumuojami iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta visomis **Požymis** registracijomis.

![1 pav.](media/06-controlling-and-reporting.png)


Toliau pateiktoje ekrano kopijoje įtraukti **Metai** ir **Mėnuo**, kad pamatytumėte, kaip galite peržiūrėti gedimų registracijas pagal pasirinktą laikotarpį.

- Dabar gedimo požymiai rodomi kaip registracijos pagal metus / mėnesį.  
- Stulpelyje **Tikimybės %**, jei įtraukiate visus kiekvieno mėnesio procentus, jie sumuojami iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis** registracijomis. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo požymį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo požymio registracijų skaičių.

![2 paveikslėlis](media/07-controlling-and-reporting.png)


- Turto ir turto tipo derinys naudojamas remiantis skaičiavimais, parodytais toliau pateiktose trijose ekrano kopijose, kurie didėja pagal išsamumo lygį.  
- Paprastai, veiksmų srities grupių **Grupuoti pagal datą**, **Grupuoti pagal turtą**, **Grupuoti pagal funkcinę vietą** mygtukai ir mygtukas **Gedimas** (gedimo ID) turi laikotarpius arba turto ryšius. Mygtukai **Požymis**, **Sritis**, **Tipas**, **Priežastis** ir **Šalinimo priemonė** yra kategorizacijos, naudojamos turto valdyme norint analizuoti turto gedimą ir nurodyti problemos sritis.  

Toliau pateiktoje ekrano kopijoje įtraukti **Turtas** ir **Turto tipas**, kad būtų rodoma daugiau informacijos apie gedimo registracijas.

- Dabar gedimo požymiai yra padalinti į derinius **Turtas** / **Turto tipas** / **Požymis**.  
- Stulpelyje **Tikimybė %**, jei įtraukiate visus derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis** registracijomis. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo požymį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo požymio registracijų skaičių.

![3 paveikslėlis](media/08-controlling-and-reporting.png)


Toliau pateiktose ekrano kopijoje **Sritis** įtraukta į **Požymis**, **Turtas** ir **Turto tipas**, kad būtų rodoma daugiau informacijos apie gedimo registracijas.

- Stulpelyje **Tikimybės %**, jei įtraukiate visus turto derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis** ir **Sritis** registracijomis. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo sritį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo srities registracijų skaičių.  

![4 paveikslėlis](media/09-controlling-and-reporting.png)


Toliau pateiktoje ekrano nuotraukoje buvo įtrauktas **Tipas** ir šiame pavyzdyje pateikiamas išsamiausias skaičiavimas.
 
- Stulpelyje **Tikimybės %**, jei įtraukiate visus turto derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis**, **Sritis** ir **Tipas** deriniu. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo tipą reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo tipo registracijų skaičių.

![5 paveikslėlis](media/10-controlling-and-reporting.png)


>[!NOTE]
>Norėdami peržiūrėti visas gedimų registracijas, sukurtas darbo užsakymuose ir priežiūros užklausose, spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimai**. Puslapyje **Turto gedimai** pažymėkite turto gedimo registraciją ir išplėskite sritį **Susijusi informacija**, kad matytumėte susijusio darbo užsakymo arba priežiūros užklausos informaciją.

