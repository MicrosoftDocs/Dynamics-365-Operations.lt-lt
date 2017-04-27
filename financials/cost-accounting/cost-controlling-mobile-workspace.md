---
title: "Mobilioji išlaidų valdymo darbo sritis, skirta programai „Microsoft Dynamics 365 for Operations“"
description: "Naudodami mobiliąją išlaidų valdymo darbo sritį, išlaidų centrų vadovai gali bet kada ir bet kur peržiūrėti išlaidų centro efektyvumą."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilioji išlaidų valdymo darbo sritis, skirta programai „Microsoft Dynamics 365 for Operations“

Naudodami mobiliąją išlaidų valdymo darbo sritį, išlaidų centrų vadovai gali bet kada ir bet kur peržiūrėti išlaidų centro efektyvumą. 

<a name="prerequisites"></a>Būtinieji komponentai
-------------

| Būtinoji sąlyga                                                         | aprašymas                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skaitykite apie „Microsoft Dynamics 365 for Operations“ mobiliąją platformą | [Mobilioji „Dynamics 365 for Operations“ platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Įsitikinkite, kad naudojate aplinką, kurioje yra „Microsoft Dynamics 365 for Operations“ 1611 versijos ir „Microsoft Dynamics for Operations“ 3 platformos naujinimas (2016 m. lapkričio mėn.). |
| Karštosios pataisos KB 3215650                                                    | Įdiegę karštąsias pataisas įjunksite „Microsoft Dynamics 365 for Operations“ pateikiamas darbo sritis.                                                                       |
| Mobilusis įrenginys, kuriame įdiegta programa „Dynamics 365 for Operations“ | Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite programą „Dynamics 365 for Operations“.                                                                                                      |

## <a name="introduction"></a>Įžanga
Mobilioji išlaidų valdymo darbo sritis suteikia esamo išlaidų centrų efektyvumo momentinį rodinį, palygindama faktines išlaidas ir biudžeto išlaidas. Galite detalizuoti atskirų išlaidų elementų būsenas.

### <a name="example"></a>Pavyzdys

Darbuotojas gauna pakvietimą į tarptautinę konferenciją. Organizacija turės padengti visas kelionės išlaidas. Darbuotojas klausia savo vadovo, ar jis gali dalyvauti konferencijoje. Vadovas greitai atidaro mobiliąją išlaidų valdymo darbo sritį savo mobiliajame telefone, kad peržiūrėtų biudžetą ir nuspręstų, ar darbuotojas gali dalyvauti konferencijoje.

### <a name="data-security"></a>Duomenų sauga

Duomenys išlaidų valdymo darbo srityje apsaugoti naudojant vartotojo kredencialus. Išlaidų centro vadovas gali peržiūrėti tik savo išlaidų centro duomenis. Prieigos lygio apsauga valdoma išlaidų apskaitos modulyje. Išlaidų buhalteriai nurodo mobiliosios išlaidų valdymo darbo srities konfigūraciją išlaidų apskaitos modulyje. Kai darbo sritis publikuojama programoje „Microsoft Dynamics 365 for Operations“, ją galima pasiekti „Dynamics 365 for Operations“ mobiliojoje programoje. Taip užtikrinama, kad visi išlaidų centrų vadovai organizacijoje duomenis peržiūri tuo pačiu formatu.

### <a name="actions-views-and-links"></a>Veiksmai, rodiniai ir saitai

Mobiliojoje išlaidų valdymo darbo srityje, skirtoje programai „Dynamics 365 for Operations“, pateikiami toliau nurodyti veiksmai, rodiniai ir saitai.

-   Veiksmai 
    -   Pasirinkite **Konfigūracijos**, kad pasirinktumėte maketą.
    -   Pasirinkite **Išlaidų objektai**, kad pasirinktumėte išlaidų centrus, kurių duomenis norite filtruoti. **Pastaba.** Sąrašas rodomas atsižvelgiant į išlaidų apskaitos modulyje suteiktą prieigą.

<!-- -->

-   Priklausomai nuo pasirinkimo dalyje **Veiksmai** ir nuo to, kas sukonfigūruota išlaidų apskaitos modulyje, galite peržiūrėti toliau nurodytą kortelių informaciją. Atkreipkite dėmesį, kad suma rodoma tuo pačiu formatu: Faktinė, Biudžeto, Nuokrypio ir Nuokrypio %. 
    -   Faktinė ir biudžeto sumos (dabartinis laikotarpis)
    -   Faktinė ir patikslinta biudžeto sumos (dabartinis laikotarpis)
    -   Faktinė ir biudžeto sumos (ankstesnis laikotarpis)
    -   Faktinė ir patikslinta biudžeto sumos (ankstesnis laikotarpis)
    -   Faktinė ir biudžeto sumos (nuo metų pradžios iki šios dienos)
    -   Faktinė ir patikslinta biudžeto sumos (nuo metų pradžios iki šios dienos)

<!-- -->

-   Saitai
    -   Dabartinio laikotarpio informacija.
    -   Ankstesnio laikotarpio informacija.
    -   Informacija nuo metų pradžios iki šiandien.

Kai pasirenkate vieną iš saitų, rodoma kortelė pagal išlaidų elementą. Suma kortelėse rodoma šiuo formatu: Faktinė, Biudžeto, Biudžeto nuokrypio, Biudžeto nuokrypio %, Patikslinta biudžeto, Patikslinta biudžeto nuokrypio ir Patikslinta biudžeto nuokrypio %.  [![cost-controlling](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Darbo pradžia
Norėdami pradėti naudoti mobiliąją išlaidų valdymo darbo sritį savo mobiliajame įrenginyje, atlikite šiuos veiksmus.

1.  Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite ir įdiekite programą „Microsoft Dynamics 365 for Operations“.
2.  Paleiskite programą savo mobiliajame įrenginyje.
3.  Įveskite savo „Dynamics 365“ URL.
4.  Įveskite įmonę, prie kurios norite prisijungti. Pavyzdžiui, įveskite **USMF**.
5.  Pirmą kartą prisijungus būsite paraginti įvesti savo „Microsoft Dynamics 365 for Operations“ paskyros vartotojo vardą ir slaptažodį. Įveskite savo kredencialus. Prisijungę matysite galimas savo įmonės darbo sritis.

Norėdami darbo sritis peržiūrėti savo mobiliojoje programoje, pirmiausia turite pageidaujamas sritis publikuoti programoje „Dynamics 365 for Operations“.

1.  Paleiskite „Dynamics 365 for Operations“.
2.  Pasirinkite **Sistemos administravimas** &gt; **Sąranka** &gt; **Sistemos parametrai**.
3.  Pasirinkite **Tvarkyti mobiliąją programą**.
4.  Pasirinkite darbo sritį **Išlaidų valdymas**, kad ją publikuotumėte mobiliojoje platformoje.
5.  Pasirinkite **Publikuoti darbo sritį**.
6.  Atnaujinkite įrenginio rodinį, kad matytumėte publikuojamas darbo sritis.

## <a name="view-the-performance-of-your-cost-center"></a>Išlaidų centro efektyvumo peržiūra
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Išlaidų valdymas**.
2.  Pasirinkite **Išlaidų objekto valdymas**.
3.  Spustelėkite **Veiksmai**.
4.  Spustelėkite **Pasirinkti konfigūraciją**, kad pasirinktumėte išlaidų valdymo maketą.
5.  Spustelėkite **Atlikta**.
6.  Spustelėkite **Veiksmai**.
7.  Spustelėkite **Pasirinkti išlaidų objektą**, kad pasirinktumėte išlaidų centrus, prie kurių turite prieigą.
8.  Spustelėkite **Atlikta**.
9.  Peržiūrėkite bendrą išlaidų centro efektyvumą.
10. Spustelėkite **Dabartinio laikotarpio informacija**.
11. Peržiūrėkite atskirų išlaidų elementų efektyvumą.
12. Taip pat galite ieškoti konkrečių išlaidų elementų.



