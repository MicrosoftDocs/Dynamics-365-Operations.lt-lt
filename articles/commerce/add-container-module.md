---
title: Konteinerio modulis
description: Šioje temoje aprašomi konteinerio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697065"
---
# <a name="container-module"></a>Konteinerio modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi konteinerio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Konteinerio modulis yra modulis, kuriame yra kitų modulių. Tai yra bendriausias konteineris, naudojamas programoje „Dynamics 365 Commerce“. Pagrindinė konteinerio modulio paskirtis yra naudojant jam nustatytas ypatybes nustatyti viduje esančių modulių išdėstymą. Pavyzdžiui, šie moduliai gali būti rodomi vienas šalia kito dviejų stulpelių, trijų stulpelių, keturių stulpelių arba šešių stulpelių makete. Jie taip pat gali būti ribojami pagal konteinerio plotį arba užpildyti ekraną. Į kiekvieną konteinerio modulį taip pat galima įtraukti antraštę.

Konteinerio modulių yra trys standartiniai tipai: konteineris, konteineris su 2 vietomis ir konteineris su 3 vietomis. Į šiuos konteinerius galima įdėti bet kokio tipo modulių. Konteinerio modulių taip pat yra specialių tipų, pvz., karuselės, raiškiojo turinio bloko, turinio išdėstymo, krepšelio, pirkimo užbaigimo, pirkimo langelio, antraštės ir poraštės. Šie konteineriai turi konkrečią paskirtį ir į juos galima įdėti tik konkrečių palaikomų tipų modulių.

Modulius rekomenduojame įdėti į konteinerį, kad juos būtų galima apriboti pagal konteinerio plotį.

## <a name="examples-of-container-modules-in-e-commerce"></a>Konteinerio modulių pavyzdžiai el. prekyboje

- Svetainės autorius nori trijų stulpelių maketo, kuriame trys moduliai rodomi vienas šalia kito. Todėl svetainės autorius naudoja konteinerio su 3 vietomis tipo modulį.
- Svetainės autorius nori šešių stulpelių maketo, kuriame šeši moduliai rodomi vienas šalia kito. Todėl svetainės autorius naudoja konteinerį su šešiais stulpeliais.
- Svetainės autorius puslapyje nori įdėti modulį, tačiau nenori, kad jis užpildytų ekraną. Todėl svetainės autorius modulį įtraukia į konteinerio modulį ir konteinerio ypatybę **Plotis** nustato kaip **Priderinti prie konteinerio**.

## <a name="container-module-properties"></a>Konteinerio modulio ypatybės

| Ypatybės pavadinimas     | Reikšmės | Aprašymas |
|-------------------|--------|-------------|
| Antraštė           | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Galima nurodyti pasirenkamą konteinerio antraštę. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Plotis             | **Priderinti prie konteinerio** arba **Užpildyti ekraną** | Jei reikšmė nustatoma kaip **Priderinti prie konteinerio** (numatytoji reikšmė), konteineryje esantys moduliai ribojami pagal konteinerio plotį. Jei reikšmė nustatoma kaip **Užpildyti ekraną**, moduliai neribojami pagal konteinerio plotį, tačiau jie gali užpildyti ekraną. |
| Stulpelių skaičius | **1**, **2**, **3**, **4**, **6** arba **12** | Ši ypatybė nustato konteinerio stulpelių skaičių. Konteineryje gali būti iki 12 stulpelių. |

## <a name="container-with-2-slots"></a>Konteineris su 2 vietomis

Konteinerio su 2 vietomis tipas yra optimizuotas dviejų stulpelių maketui. Šio tipo konteineryje yra dvi vietos, kad jo moduliai galėtų būti vaizduojami vienas šalia kito.

Naudojant papildomus parametrus, maketą galima optimizuoti skirtingiems rodiniams (mobiliesiems įrenginiams, planšetiniams bei įprastiesms kompiuteriams ir t. t.). Kiekviename rodinyje galima nustatyti kiekvieno stulpelio plotį. Galimi tolesni stulpelių pločio parametrai.

- **75 % / 25 %** – pirmojo modulio stulpelių plotis yra 75 procentai, o antrojo – 25 procentai. Taip pat galima naudoti parinktį **25 % / 75 %**.
- **50 % / 50 %** – abiejų modulių stulpelių plotis yra vienodas.
- **67 % / 33 %** – pirmojo modulio stulpelių plotis yra 67 procentai, o antrojo – 33 procentai. Taip pat galima naudoti parinktį **33 % / 67 %**.
- **100 %** – abiejų modulių stulpelių plotis neribojamas. Todėl moduliai yra vertikaliai sudėti į šūsnį viename stulpelyje. Nors šis vieno stulpelio maketas neatitinka konteinerio su 2 vietomis tipo paskirties, kai kuriems rodiniams (pavyzdžiui, itin mažiems rodiniams, pvz., mobiliųjų įrenginių) jis gali būti labiau tinkamas.

### <a name="container-with-2-slots-properties"></a>Konteinerio su 2 vietomis ypatybės

| Ypatybės pavadinimas                   | Reikšmės | Aprašymas |
|---------------------------------|--------|-------------|
| Antraštė                         | Antraštės tekstas ir antraštės žymė | Galima nurodyti pasirenkamą konteinerio antraštę. |
| Itin mažo rodinio konfigūracija | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** arba **100 %** | Ši ypatybė nustato itin mažų rodinių maketą. |
| Mažo rodinio konfigūracija   | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** arba **100 %** | Ši ypatybė nustato mažų rodinių, pvz., mobiliųjų įrenginių, maketą. |
| Vidutinio rodinio konfigūracija  | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** arba **100 %** | Ši ypatybė nustato vidutinių rodinių, pvz., planšetinių kompiuterių, maketą. |
| Didelio rodinio konfigūracija   | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** arba **100 %** | Ši ypatybė nustato didelių rodinių, pvz., kompiuterių, maketą. |

## <a name="container-with-3-slots"></a>Konteineris su 3 vietomis

Konteinerio su 3 vietų moduliais tipas yra optimizuotas trijų stulpelių maketui.

Naudojant papildomus parametrus, galima optimizuoti skirtingų rodinių maketą. Kiekviename rodinyje galima nustatyti kiekvieno stulpelio plotį. Galimi tolesni stulpelių pločio parametrai.

- **33 % / 33 % / 33 %** – visų trijų modulių stulpelių plotis yra vienodas.
- **50 % / 25 % / 25 %** – pirmojo modulio stulpelių plotis yra 50 procentų, o kiekvieno iš likusių dviejų modulių – 25 procentai. Taip pat galima naudoti parinktis **25 % / 50 % / 25 %** ir **25 % / 25 % / 50 %**.
- **16 % / 16 % / 67 %** – kiekvieno iš pirmų dviejų modulių stulpelių plotis yra 16 procentų, o trečiojo modulio – 67 procentai. Taip pat galima naudoti parinktis **16 % / 67 % / 16 %** ir **67 % / 16 % / 16 %**.

### <a name="container-with-3-slots-properties"></a>Konteinerio su 3 vietomis ypatybės

| Ypatybės pavadinimas                   | Reikšmės | Aprašymas |
|---------------------------------|--------|-------------|
| Antraštė                         | Antraštės tekstas ir antraštės žymė | Į konteinerį galima įtraukti pasirenkamą antraštę. |
| Itin mažo rodinio konfigūracija | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** arba **67 % / 16 % / 16 %** | Ši ypatybė nustato itin mažų rodinių maketą. |
| Mažo rodinio konfigūracija   | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** arba **67 % / 16 % / 16 %** | Ši ypatybė nustato mažų rodinių, pvz., mobiliųjų įrenginių, maketą. |
| Vidutinio rodinio konfigūracija  | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** arba **67 % / 16 % / 16 %** | Ši ypatybė nustato vidutinių rodinių, pvz., planšetinių kompiuterių, maketą. |
| Didelio rodinio konfigūracija   | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** arba **67 % / 16 % / 16 %** | Ši ypatybė nustato didelių rodinių, pvz., kompiuterių, maketą. |

## <a name="add-a-container-module-to-a-page"></a>Konteinerio modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti konteinerio leistuvo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite puslapio šabloną, pavadintą **konteinerio šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.
1. Konteinerio modulyje įtraukite ypatybių modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą konteinerio šabloną, sukurkite puslapį, pavadintą **konteinerio puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.
1. Konteinerio modulio ypatybių srityje ypatybę **Stulpelių skaičius** nustatykite kaip **1**, o ypatybę **Plotis** – kaip **Priderinti prie konteinerio**.
1. Konteinerio modulyje įtraukite ypatybių modulį.
1. Ypatybių modulio ypatybių srityje sukonfigūruokite antraštę.
1. Puslapį įrašykite ir peržiūrėkite. Turėtumėte matyti vieną ypatybių modulį, priderintą pire konteinerio modulio pločio.
1. Konteinerio modulio ypatybių srityje ypatybės **Stulpelių skaičius** reikšmę pakeiskite į **3**.
1. Į konteinerio modulį įtraukite dar du ypatybių modulius.
1. Puslapį įrašykite ir peržiūrėkite. Dabar turėtumėte matyti tris ypatybių modulius, rodomus vienas šalia kito.
1. Pasiekę norimą maketą, puslapį įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)