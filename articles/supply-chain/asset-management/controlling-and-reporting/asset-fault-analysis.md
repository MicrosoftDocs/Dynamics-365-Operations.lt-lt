---
title: Turto klaidų analizė
description: Šioje temoje aiškinama turto gedimų analizė turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f4d7b4a92486287027cba79c43ca5933cce42a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253859"
---
# <a name="asset-fault-analysis"></a>Turto klaidų analizė

[!include [banner](../../includes/banner.md)]

 

Turto valdyme galite analizuoti turto gedimų registracijas, kad galėtumėte peržiūrėti bendrą konkrečiu laikotarpiu užregistruotų gedimų skaičių. Gedimų registracijas galima analizuoti skirtingais būdais, pavyzdžiui, pagal turtą, turto tipus, funkcines vietas, gedimo požymius ar gedimų tipus.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimo analizė**.

2. Dialoge lange **Turto gedimo analizės skaičiavimas** galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti turto gedimo eilutėse. 

    Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos turto gedimo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. 
        
    Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, turto gedimo eilutes.

3. Jei norite apriboti iešką, „FastTab“ **Įtrauktini įrašai** galite pažymėti konkretų turtą, gedimų datas, gedimo priežastis ir gedimo šalinimo priemones.

4. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

5. Skirtuke **Turto gedimo analizė** spustelėkite vieną ar daugiau mygtukų **Grupuoti pagal**, kad būtų rodoma lygio, kurį norite matyti, išsami informacija. Suaktyvinti mygtukai yra paryškinti. Suaktyvinkite arba deaktyvinkite mygtukus juos spustelėdami.

6. Spustelėkite **Naujinti skaičiavimus**, kad pasirinkimai būtų rodomi ekrane. 

>[!NOTE]
>Kiekvieną kartą, kai aktyvindami arba deaktyvindami mygtuką **Grupuoti pagal**, nepamirškite spustelėti mygtuko **Naujinti skaičiavimus**. Taip reikia, nes kai perskaičiuojama gedimo tikimybė, apdorojamas didelis kiekis duomenų.

## <a name="examples"></a>Pavyzdžiai

Yra daug būdų, kaip analizuoti gedimų registracijas. Šiame skyriuje pateikti penki pavyzdžiai, kaip analizuojant turto gedimų registracijas skirtingai pasirinkus duomenis galima gauti daugiau informacijos.

### <a name="group-by-symptoms"></a>Grupuoti pagal požymius

Toliau pateiktoje ekrano kopijoje pažymėtas tik mygtukas **Požymis**.

- Gedimo registracijos atliktos pagal tris gedimo požymius: „Oro nuotėkis“, „Perdegęs saugiklis“ ir „Užstrigo įranga“.  
- Stulpelyje **Tikimybės %** visi procentai sumuojami iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta visomis **Požymis** registracijomis.

![1 pav.](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Grupuoti pagal požymius ir laikotarpį

Toliau pateiktoje ekrano kopijoje įtraukti **Metai** ir **Mėnuo**, kad pamatytumėte, kaip galite peržiūrėti gedimų registracijas pagal pasirinktą laikotarpį.

- Dabar gedimo požymiai rodomi kaip registracijos pagal metus / mėnesį.  
- Stulpelyje **Tikimybės %**, jei įtraukiate visus kiekvieno mėnesio procentus, jie sumuojami iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis** registracijomis. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo požymį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo požymio registracijų skaičių.

![2 pav.](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Grupuoti pagal kelis simptomus ir turtą

Turto ir turto tipo derinys naudojamas remiantis skaičiavimais, parodytais toliau pateiktose trijose ekrano kopijose, kurie didėja pagal išsamumo lygį.  

Paprastai, veiksmų srities grupių **Grupuoti pagal datą**, **Grupuoti pagal turtą**, **Grupuoti pagal funkcinę vietą** mygtukai ir mygtukas **Gedimas** (gedimo ID) turi laikotarpius arba turto ryšius. Mygtukai **Požymis**, **Sritis**, **Tipas**, **Priežastis** ir **Šalinimo priemonė** yra kategorizacijos, naudojamos turto valdyme norint analizuoti turto gedimą ir nurodyti problemos sritis.  

**Grupuoti pagal požymį, turtą ir turto tipą**

Toliau pateiktoje ekrano kopijoje įtraukti **Turtas** ir **Turto tipas**, kad būtų rodoma daugiau informacijos apie gedimo registracijas.

- Dabar gedimo požymiai yra padalinti į derinius **Turtas** / **Turto tipas** / **Požymis**.  
- Stulpelyje **Tikimybė %**, jei įtraukiate visus derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis** registracijomis. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo požymį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo požymio registracijų skaičių.

![3 pav.](media/08-controlling-and-reporting.png)

**Grupuoti pagal du požymius, turtą ir turto tipą**

Toliau pateiktose ekrano kopijoje **Sritis** įtraukta į **Požymis**, **Turtas** ir **Turto tipas**, kad būtų rodoma daugiau informacijos apie gedimo registracijas.

- Stulpelyje **Tikimybės %**, jei įtraukiate visus turto derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis** ir **Sritis** registracijomis. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo sritį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo srities registracijų skaičių.  

![4 pav.](media/09-controlling-and-reporting.png)

**Grupuoti pagal tris požymius, turtą ir turto tipą**

Toliau pateiktoje ekrano nuotraukoje buvo įtrauktas **Tipas** ir šiame pavyzdyje pateikiamas išsamiausias skaičiavimas.
 
- Stulpelyje **Tikimybės %**, jei įtraukiate visus turto derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %. Šioje gedimo analizėje tikimybė pagrįsta **Požymis**, **Sritis** ir **Tipas** deriniu. Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo tipą reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo tipo registracijų skaičių.

![5 paveikslėlis](media/10-controlling-and-reporting.png)


>[!NOTE]
>Norėdami peržiūrėti visas gedimų registracijas, sukurtas darbo užsakymuose ir priežiūros užklausose, spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimai**. Puslapyje **Turto gedimai** pažymėkite turto gedimo registraciją ir išplėskite sritį **Susijusi informacija**, kad matytumėte susijusio darbo užsakymo arba priežiūros užklausos informaciją.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]