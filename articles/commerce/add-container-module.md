---
title: Konteinerio modulis
description: Šiame straipsnyje aprašomi konteinerio moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 58fa222dfef9e559da00fef448c572800651bd63
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272913"
---
# <a name="container-module"></a>Konteinerio modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi konteinerio moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Konteinerio modulis yra modulis, kuriame yra kitų modulių. Pagrindinė konteinerio modulio paskirtis yra naudojant jam nustatytas ypatybes nustatyti jo turimų modulių išdėstymą. Pavyzdžiui, šie moduliai gali būti rodomi vienas šalia kito dviejų stulpelių, trijų stulpelių, keturių stulpelių arba šešių stulpelių makete. Jie taip pat gali būti ribojami pagal konteinerio plotį arba užpildyti ekraną. Į kiekvieną konteinerio modulį taip pat galima įtraukti antraštę.

Palaikomi trys konteinerio moduliai: konteineris, konteineris su 2 vietomis ir konteineris su 3 vietomis. Į šiuos konteinerius galima įdėti bet kokio tipo modulių. 

> [!NOTE] 
> Modulius rekomenduojame visada įdėti į konteinerio modulį, kad juos būtų galima apriboti pagal konteinerio plotį.

## <a name="examples-of-container-modules-in-e-commerce"></a>Konteinerio modulių pavyzdžiai el. prekyboje

- Svetainės autorius nori trijų stulpelių maketo, kuriame trys moduliai rodomi vienas šalia kito. Todėl svetainės autorius naudoja konteinerio su 3 vietomis tipo modulį.
- Svetainės autorius nori šešių stulpelių maketo, kuriame šeši moduliai rodomi vienas šalia kito. Todėl svetainės autorius naudoja konteinerį su šešiais stulpeliais.
- Svetainės autorius puslapyje nori įdėti modulį, tačiau nenori, kad jis užpildytų ekraną. Todėl svetainės autorius modulį įtraukia į konteinerio modulį ir konteinerio ypatybę **Plotis** nustato kaip **Priderinti prie konteinerio**.

Toliau pateiktame paveikslėlyje parodytas „Commerce“ svetainių daryklėje esančio konteinerio modulio, kuriame yra karuselės modulis, pavyzdys. Šiame pavyzdyje konteinerio modulio ypatybė **Plotis** nustatyta kaip **Užpildyti ekraną**.

![Konteinerio modulio pavyzdys.](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Konteinerio modulio ypatybės

| Ypatybės pavadinimas     | Reikšmės | Aprašas |
|-------------------|--------|-------------|
| Antraštė           | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Galima nurodyti pasirenkamą konteinerio antraštę. Numatyta, kad naudojama antraštės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Plotis             | **Priderinti prie konteinerio** arba **Užpildyti ekraną** | Jei reikšmė nustatoma kaip **Priderinti prie konteinerio** (numatytoji reikšmė), konteineryje esantys moduliai ribojami pagal konteinerio plotį. Jei reikšmė nustatoma kaip **Užpildyti ekraną**, moduliai neribojami pagal konteinerio plotį, tačiau jie gali užpildyti ekraną. |
| Stulpelių skaičius | **1**, **2**, **3**, **4**, **6** arba **12** | Ši ypatybė nustato konteinerio stulpelių skaičių. Konteineryje gali būti iki 12 stulpelių. |

## <a name="container-with-2-slots"></a>Konteineris su 2 vietomis

Konteinerio su 2 vietomis tipas yra optimizuotas dviejų stulpelių maketui. Šio tipo konteineryje yra dvi vietos, kad jo moduliai galėtų būti vaizduojami vienas šalia kito.

Naudojant papildomus parametrus, maketą galima optimizuoti skirtingiems rodiniams (mobiliesiems įrenginiams, planšetiniams bei įprastiems kompiuteriams ir t. t.). Kiekviename rodinyje galima nustatyti kiekvieno stulpelio plotį. Galimi tolesni stulpelių pločio parametrai.

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
1. Dialogo lange **Naujas šablonas**, po Šablono **pavadinimas**, įveskite Konteinerio **šablonas** ir pasirinkite **Gerai**.
1. Teksto atminties **atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Numatytasis** puslapis, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį**, po Puslapio pavadinimas **įveskite** puslapį **Konteineris** ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite konteinerio **šabloną,** kurį sukūrėte, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Naujo puslapio **pagrindiniame** atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio modulio ypatybių srityje ypatybę **Stulpelių skaičius** nustatykite kaip **1**, o ypatybę **Plotis** – kaip **Užpildyti konteinerį**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite turinio bloko **modulį**, tada pasirinkite **Gerai**.
1. Turinio bloko modulio ypatybių srityje sukonfigūruokite antraštę, vaizdą ir išdėstymą.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Turėtumėte matyti vieną ypatybių modulį, priderintą prie konteinerio modulio pločio.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
