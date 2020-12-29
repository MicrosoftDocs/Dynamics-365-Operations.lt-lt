---
title: Konteinerio modulis
description: Šioje temoje aprašomi konteinerio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 9bb2c7d56184d009492b4aa839a3546160ad342f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414283"
---
# <a name="container-module"></a>Konteinerio modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi konteinerio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Konteinerio modulis yra modulis, kuriame yra kitų modulių. Pagrindinė konteinerio modulio paskirtis yra naudojant jam nustatytas ypatybes nustatyti jo turimų modulių išdėstymą. Pavyzdžiui, šie moduliai gali būti rodomi vienas šalia kito dviejų stulpelių, trijų stulpelių, keturių stulpelių arba šešių stulpelių makete. Jie taip pat gali būti ribojami pagal konteinerio plotį arba užpildyti ekraną. Į kiekvieną konteinerio modulį taip pat galima įtraukti antraštę.

Palaikomi trys konteinerio moduliai: konteineris, konteineris su 2 vietomis ir konteineris su 3 vietomis. Į šiuos konteinerius galima įdėti bet kokio tipo modulių. 

> [!NOTE] 
> Modulius rekomenduojame visada įdėti į konteinerio modulį, kad juos būtų galima apriboti pagal konteinerio plotį.

## <a name="examples-of-container-modules-in-e-commerce"></a>Konteinerio modulių pavyzdžiai el. prekyboje

- Svetainės autorius nori trijų stulpelių maketo, kuriame trys moduliai rodomi vienas šalia kito. Todėl svetainės autorius naudoja konteinerio su 3 vietomis tipo modulį.
- Svetainės autorius nori šešių stulpelių maketo, kuriame šeši moduliai rodomi vienas šalia kito. Todėl svetainės autorius naudoja konteinerį su šešiais stulpeliais.
- Svetainės autorius puslapyje nori įdėti modulį, tačiau nenori, kad jis užpildytų ekraną. Todėl svetainės autorius modulį įtraukia į konteinerio modulį ir konteinerio ypatybę **Plotis** nustato kaip **Priderinti prie konteinerio**.

Toliau pateiktame paveikslėlyje parodytas „Commerce“ svetainių daryklėje esančio konteinerio modulio, kuriame yra karuselės modulis, pavyzdys. Šiame pavyzdyje konteinerio modulio ypatybė **Plotis** nustatyta kaip **Užpildyti ekraną**.

![Konteinerio modulio pavyzdys](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Konteinerio modulio ypatybės

| Ypatybės pavadinimas     | Reikšmės | aprašymas |
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

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Konteinerio šablonas** ir pasirinkite **Gerai**.
1. Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite vaizdo įrašų leistuvo šabloną, kurį sukūrėte. Dalyje **Puslapio pavadinimas** įveskite **Konteinerio puslapis**, tada pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Konteinerio modulio ypatybių srityje ypatybę **Stulpelių skaičius** nustatykite kaip **1**, o ypatybę **Plotis** – kaip **Užpildyti konteinerį**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Turinio blokas**, tada pasirinkite **Gerai**.
1. Turinio bloko modulio ypatybių srityje sukonfigūruokite antraštę, vaizdą ir išdėstymą.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Turėtumėte matyti vieną ypatybių modulį, priderintą pire konteinerio modulio pločio.
1. Konteinerio modulio ypatybių srityje ypatybės **Stulpelių skaičius** reikšmę pakeiskite į **3**.
1. Pridėkite dar du turinio blokų modulius į konteinerio modulį ir sukonfigūruokite juos.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Dabar turėtumėte matyti tris turinio bloko modulius, rodomus vienas šalia kito.
1. Nustatę pageidaujamą maketą, pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, tada paskelbkite jį pasirinkdami **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Akordeono modulis](add-accordion.md)

[Skirtuko modulis](add-tab.md)

[Karuselės modulis](add-carousel.md)

[Teksto bloko modulis](add-content-rich-block.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
