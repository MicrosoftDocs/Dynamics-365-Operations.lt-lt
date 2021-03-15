---
title: Paketo balansavimas
description: Šioje temoje aprašomas paketų balansavimo procesas.
author: johanhoffmann
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c1f52239b2050425c37a8130507e689b29205a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966560"
---
# <a name="batch-balancing"></a>Paketo balansavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip palaikomas paketų balansavimo procesas.

Norėdami gauti daugiau informacijos, peržiūrėkite [vaizdo įrašą apie paketo balansavimą](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

Vykdant paketų balansavimo procesą, gamybos pakete naudotinas ingredientų kiekis apskaičiuojamas pagal aktyviųjų ingredientų koncentraciją pasirinktuose produktų paketuose.

## <a name="products-that-have-an-active-ingredient"></a>Produktai su aktyviuoju ingredientu

Produktą galima apibrėžti pagal jame esančio aktyviojo ingrediento koncentraciją. Aktyvusis produkto ingredientas modeliuojamas naudojant konkretaus produkto paketo atributą, turintį minimalią reikšmę, maksimalią reikšmę ir tikslinį lygį.

Tikslinis paketo atributo lygis – tai įvertintas aktyviojo ingrediento procentas produkte. Minimali ir maksimali reikšmės – tai priimtinas nuokrypis nuo tikslinio lygio. Pavyzdžiui, jas galima naudoti kaip priimtiną paketų nuokrypį gaunant produktus.

Produktas gali turėti tik vieną aktyvųjį ingredientą. Norėdami nurodyti aktyvųjį produkto ingredientą, pirmiausia turite apibrėžti konkretaus produkto paketo atributą. Tada atributą reikia susieti kaip pagrindinį produkto atributą.

Produkto lygiu taip pat turite nurodyti, kaip turi būti įrašomas produkto paketo aktyviojo ingrediento lygis: kaip pirkimo gavimo proceso dalis ar kaip kokybės užsakymo proceso dalis.

Norint pagrindinį atributą susieti su produktu, reikia atlikti tolesnę sąranką.

- Produktas turi būti valdomas paketų. Norėdami produktą padaryti valdomą paketų, produktui, turinčiam aktyvią paketo dimensiją, turite priskirti sekimo dimensijų grupę.

- Ingredientų lygius rodantį atributą reikia apibrėžti kaip konkretaus produkto paketo atributą.

Norėdami peržiūrėti ir redaguoti faktinę paketo aktyviojo ingrediento vertę:
1. Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Sekimo dimensijos \> Paketai**.
1. Iš tinklelio pasirinkite paketo numerį.
1. Veiksmų srityje atidarykite skirtuką **Peržiūra** ir pasirinkite **Atsargų paketo atributai**.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Ingredientų tipai ir kaip jie sąveikauja vykstant paketų balansavimo procesui

Sukurtos formulės eilutės ingrediento tipas gali būti vienas iš tolesnių.

- None
- Aktyvu
- Kompensavimas
- Pildytojas

Likusioje šio skyriaus dalyje pateikiama pavyzdžių, rodančių, kaip veikia kiekvienas ingrediento tipas. Pavyzdžiai paremti tolesne formule, kurioje bendrasis paketo dydis yra 100 litrų.

| Sudedamosios dalies tipas | Prekės Nr. | Formulės eilutės kiekis | Vienetas |
|---|---|---|---|
| None | A | 20 | Litras |
| Aktyvios | Mlrd. | 30 | Litras |
| Kompensavimas | K | 10 | Litras |
| Pildytojas | D | 40 | Litras |

Toliau esančioje lentelėje pateikiama kiekvieno pavyzdžio rezultatų apžvalga.

| Prekės Nr. | Sudedamosios dalies tipas | Įvertintas kiekis | Subalansuotas kiekis | Aktyvus kiekis | Vienetas | Pagrindinė vertė |
|---|---|---|---|---|---|---|
| A | None | 20 | 20 | | Litras | |
| G | Aktyvu | 30 | 25,71 | 9,00 | Litras | 30.00 |
| K | Kompensavimas | 10 | 14.72 | | Litras | |
| D | Pildytojas | 40 | 39.57 | | Litras | |

### <a name="active-ingredients"></a>Aktyvieji ingredientai

Kai į formulės eilutę įtraukiamas produktas, turintis pagrindinį atributą, jis vadinamas formulės *aktyviuoju ingredientu*. Paketinius užsakymus su formulėmis, į kurias įtraukta aktyviųjų ingredientų, galima naudoti vykdant paketų balansavimo procesą. Vykdant paketų balansavimo procesą įvertinama, kiek kiekvieno formulės ingrediento reikia pagaminti produktą. Kiekiai įvertinami pagal aktyviųjų ingredientų koncentraciją pasirinktuose paketuose.

#### <a name="active-ingredient-example"></a>Aktyviojo ingrediento pavyzdys

Pagrindinis B ingrediento atributas yra X, o tikslinis lygis – 30, ir ingredientas įtrauktas į formulę, pagal kurią kiekvienam 100 litrų produkto reikia 30 litrų B ingrediento. Sukuriamas paketinis užsakymas, kurio dydis yra 100 litrų. Paketinis užsakymas pradedamas ir, vykstant paketų balansavimo procesui, vartotojas pasirenka B ingrediento paketą, kurio stiprumo lygis yra 35. Kadangi stiprumo lygis 35 yra didesnis nei tikslinis lygis 30, subalansuotas B ingrediento kiekis sumažinamas naudojant paketo stiprumo reikšmės ir tikslinio lygio santykį, kuris padauginamas iš įvertinto kiekio. Subalansuotas kiekis skaičiuojamas taip:

(30 ÷ 35) × 30 liters = 25,71 litro

### <a name="none-ingredients"></a>Jokių ingredientų

Paketų balansavimo procesą pritaikius tada, kai **Ingrediento tipas** yra *Joks*, paketinio užsakymo formulės eilutėje įvertintas kiekis ir subalansuotas kiekis sutampa.

#### <a name="none-ingredient-example"></a>Jokių ingredientų pavyzdys

A ingredientas priskiriamas tipo *Nėra* ingredientui ir įtraukiamas į baigto produkto formulę. Pagal formulę kiekvienam 100 litrų baigto produkto reikia 10 litrų A ingrediento. Kai paketiniam užsakymui reikia 200 litrų, tiek įvertintas, tiek subalansuotas A ingrediento kiekiai skaičiuojami kaip 20 litrų.

### <a name="compensating-ingredients"></a>Kompensuojamieji ingredientai

Kompensuojamasis ingredientas gali kompensuoti arba papildyti aktyviojo ingrediento produkte poveikį. Todėl sunaudojamo kompensuojamojo ingrediento kiekis priklauso nuo produkto stiprumo.

- **Priešingas poveikis** – jei aktyviojo ingrediento kiekis yra didesnis nei numatytas, kompensuojamojo ingrediento turite pridėti mažiau.

- **Kompensuojamasis poveikis** – jei aktyviojo ingrediento kiekis yra mažesnis nei numatytas, kompensuojamojo ingrediento turite pridėti daugiau.

Ryšys tarp aktyviojo ingrediento ir kompensuojamojo ingrediento nustatomas puslapyje **Kompensavimo principas**.

Norėdami nustatyti ryšius tarp ingredientų, atlikite tolesnius veiksmus.

1. Pasirinkite **Produkto informacijos valdymas \> KS ir formulės \> Formulės**.
1. Atidarykite formulės eilutę ir pasirinkite **Ingredientai** tam, kad atidarytumėte **Kompensuojamasis principas** puslapį.
1. Pasirinkite eilutę su kompensavimo principu, tada pasirinkite norimą kompensuoti aktyvųjį ingredientą.

Kompensavimo principo dalyje taip pat reikia įvesti teigiamą arba neigiamą kompensavimo koeficientą siekiant nurodyti kompensavimo kiekį ir ar principo poveikis turi būti priešingas, ar kompensuojamasis. Teigiamas koeficientas rodo kompensuojamąjį poveikį, o neigiamas koeficientas rodo priešingą poveikį.

#### <a name="compensating-ingredient-example"></a>Kompensuojamojo ingrediento pavyzdys

B ingredientas yra aktyvusis ingredientas, kurio pagrindinis atributas yra X, o tikslinis lygis – 30. Jis įtrauktas į formulę, pagal kurią kiekvienam 100 litrų produkto reikia 30 litrų B ingrediento. C ingredientas yra kompensuojamasis ingredientas ir į tą pačią formulę įtraukiamas kiekis „10“. Nustatomas kompensavimo principo kompensavimo koeficientas 1,10. Todėl subalansuotas kompensuojamojo ingrediento kiekis bus sumažintas aktyviojo ingrediento subalansuoto kiekio ir įvertinto reikiamo kiekio skirtumu, padaugintu iš 1,10.

Ingrediento tipo *Aktyvusis* pavyzdyje subalansuotas reikiamo aktyviojo ingrediento kiekis buvo apskaičiuotas kaip 25,71, o įvertintas reikiamas kiekis buvo apskaičiuotas kaip 30. Šiuo atveju subalansuotas kompensuojamojo ingrediento kiekis bus apskaičiuojamas taip, kaip nurodyta toliau.

1. Nustatomas skirtumas tarp įvertinto ir subalansuoto kiekio:  
    25,71 – 30 = –4,29

1. Rezultatas padauginamas iš kompensavimo koeficiento:  
    4,29 × 1,10 = –4,72

1. Įvertintas kompensuojamasis kiekis sumažinamas dydžiu –4,72 ir nustatomas subalansuotas kompensuojamasis kiekis:  
    10 – (–4,72) = 14,72

Kadangi 1,10 yra teigiamas kompensavimo koeficientas, šio kompensavimo principo poveikis yra kompensuojamasis. Šiuo atveju aktyvusis ingredientas yra stipresnis nei numatyta. Todėl reikia daugiau kompensuojamojo ingrediento.

### <a name="filler-ingredients"></a>Papildomi ingredientai

*Papildomas ingredientas* yra neutralus ingredientas, naudojamas norint pasiekti pageidaujamą baigto produkto išeigos kiekį. Papildomo kiekio koregavimas skaičiuojamas pagal aktyviojo ingrediento ir kompensuojamojo ingrediento nuokrypius, palyginti su standartiniu kiekiu.

#### <a name="filler-ingredient-example"></a>Papildomo ingrediento pavyzdys

Suformulavote produktą su A, B, C ir D ingredientais, kurio formulės dydis yra 100 litrų. Subalansuotą kiekį apskaičiavote visų tipų ingredientams, išskyrus tipo *Papildomas* ingredientą, naudojamą vienoje eilutėje.
Subalansuotas papildomo ingrediento kiekis apskaičiuojamas kaip skirtumas tarp paketo dydžio (100 litrų) ir A, B bei C ingredientų sumos:

100 – (20 + 25,71 + 14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Paketų balansavimo procesas

Paketų balansavimo procesas atliekamas puslapyje **Paketų balansavimas**.
Pasirinkite **Kaštų valdymas \> Paketiniai užsakymai**, o tada skirtuke **Procesas** pasirinkite **Partijų balansavimas**. Paketų balansavimo funkciją galima naudoti su paketiniais užsakymais, kurių būsena yra **Pradėtas**.

Apskritai, partijų balansavimo funkciją paketiniams užsakymams galima taikyti, jei formulėje yra bent viena formulės eilutė, kurioje **Ingrediento tipas** yra *Aktyvusis*. (Norėdami sužinoti apie šios taisyklės išimtį, žr. toliau šioje temoje pateiktą skyrių „Paketiniai užsakymai, kuriems paketų balansavimo funkcijos taikyti negalima“.)

Paketų balansavimo procesą galima išskaidyti į du antrinius procesus.

1. Balansuoti paketo sudedamąsias dalis
1. Formulės patvirtinimas ir išleidimas

### <a name="balance-batch-ingredients"></a>Balansuoti paketo sudedamąsias dalis

Vykdant procesą Paketų ingredientų balansavimas, gamybos pakete naudotinas ingredientų kiekis apskaičiuojamas pagal pasirinktus paketus su aktyviaisiais ingredientais. Paprastai apskaičiuoti galima, tik jei visiškai aprėpiami visi ingredientai. Negalite balansuoti tik tos paketo dalies, kurią pagaminti nustatytas paketinis užsakymas.

> [!NOTE]
> Negalite įrašyti skaičiavimo ir paketų balansavimo proceso baigti vėliau. Jei uždarote puslapį **Paketų balansavimas**, norėdami baigti procesą turite pakartoti skaičiavimą.

### <a name="confirm-and-release-the-formula"></a>Formulės patvirtinimas ir išleidimas

Kai ingredientų kiekiai apskaičiuoti, formulę galite patvirtinti ir išleisti. Išleidimo procesas skiriasi ir priklauso nuo to, ar su produktais galima vykdyti sandėlio valdymo procesus.

- Jei su produktu galima vykdyti sandėlio valdymo procesus, formulės eilutė į sandėlį išleidžiama pagal sandėlio valdymo procesų principus. Išleidžiami su subalansuotais kiekiais sutapantys formulės eilutės kiekiai ir jie išleidžiami tų konkrečių paketų, kuriuose pasirinkta naudoti aktyviuosius ingredientus.

    > [!NOTE]
    > Formulių eilutes į sandėlį galima išleisti tik vykdant paketų balansavimo procesą. Nors yra kitų parinkčių, kaip medžiagas gamybai išleisti į sandėlį, su formulių eilutėmis tų parinkčių naudoti negalima.

- Jei su produktu sandėlio valdymo procesų vykdyti negalima, jums tvirtinant ir išleidžiant formulę sukuriamas produkto išrinkimo dokumentas.

Vienoje formulėje galite sujungti produktus, su kuriais vykdyti sandėlio valdymo procesus galima, ir produktus, su kuriais sandėlio valdymo procesų vykdyti negalima. Kai šių dviejų tipų produktai įtraukti į vieną formulę, produktai, su kuriais galima vykdyti sandėlio valdymo procesus, išleidžiami į sandėlį. Jei su produktais sandėlio valdymo procesų vykdyti negalima, tvirtinant ir išleidžiant formulę sukuriamas jų išrinkimo dokumentas.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Paketiniai užsakymai, kuriems paketų balansavimo funkcijos taikyti negalima

Yra dvi išimtis taisyklei, kad paketiniams užsakymams galima taikyti paketų balansavimo funkciją, jei formulėje yra bent viena formulės eilutė, kurioje **Ingrediento tipas** yra *Aktyvusis*.

1. Jei formulėje yra produkto, su kuriuo galima vykdyti sandėlio valdymo procesus, aktyvusis ingredientas, tačiau rezervavimo hierarchijoje reikšmė „paketo numeris” yra žemiau reikšmės „vieta”, paketiniam užsakymui partijų balansavimo funkcijos taikyti negalima.
1. Jei formulės matavimo vienetas skiriasi nuo aktyviojo ingrediento atsargų matavimo vieneto, partijų balansavimas netaikomas paketo užsakymui.

Paketiniam užsakymui, kuriam negalima taikyti paketų balansavimo funkcijos, taikomas įprastas paketinių užsakymų apdorojimo ciklas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]