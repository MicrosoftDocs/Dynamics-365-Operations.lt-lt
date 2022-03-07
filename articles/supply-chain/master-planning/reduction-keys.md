---
title: Prognozės mažinimo raktai
description: Šioje temoje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą. Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus. Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius.
author: ChristianRytt
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbed77fd1abc0e4ae26e2b9ddcc01d3f4a84889f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570830"
---
# <a name="forecast-reduction-keys"></a>Prognozės mažinimo raktai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie skirtingus metodus, kurie naudojami norint sumažinti prognozės poreikius. Joje pateikiami kiekvieno metodo rezultatų pavyzdžiai. Joje taip pat paaiškinama, kaip kurti, nustatyti ir naudoti prognozės mažinimo raktą. Kai kuriuose metoduose naudojamas mažinimo raktas siekiant sumažinti prognozės poreikius.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Naudojami prognozes poreikių mažinimo metodai

Kai įtraukiate prognozę į bendrąjį planą, galite pasirinkti, kaip mažinami prognozės poreikiai, kai faktinis poreikis yra įtrauktas. Atkreipkite dėmesį, kad bendrasis planavimas neapima buvusių prognozės poreikių, t. y. visų prognozės poreikių, kurių data yra ankstesnė nei šios dienos data.

Norėdami įtraukti prognozę į bendrąjį planą ir pasirinkti metodą, kuris naudojamas siekiant sumažinti prognozės poreikius, pasirinkite **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**. Lauke **Prognozės modelis** pasirinkite prognozės modelį. Lauke **Prognozes poreikių mažinimo metodas** pasirinkite metodą. Galimos toliau nurodytos parinktys.

- Nėra
- Procentai – mažinimo raktas
- Operacijos – mažinimo raktas
- Operacijos – dinaminis laikotarpis

Tolesniuose skyriuose pateikiama daugiau informacijos apie kiekvieną parinktį.

### <a name="none"></a>Nėra

Jei pasirinksite **Nėra**, prognozės poreikiai bendrojo planavimo metu nebus sumažinti. Tokiu atveju bendrasis planavimas sukuria suplanuotus užsakymus, kad būtų tenkinamas prognozuojamas poreikis (prognozės poreikiai). Šiuose suplanuotuose užsakymuose tvarkomas siūlomas kiekis, nepriklausomai nuo kitų poreikio tipų. Pvz., jei pateikiami pardavimo užsakymai, bendrasis planavimas sukuria papildomus suplanuotus užsakymus, kad tiektų pardavimo užsakymams skirtus produktus. Prognozės poreikių kiekis nėra sumažinamas.

### <a name="percent--reduction-key"></a>Procentai – mažinimo raktas

Jei pasirinksite **Procentas – mažinimo raktas**, prognozės poreikiai sumažinami pagal procentines dalis ir laiko laikotarpius, kurie nurodomi mažinimo raktu. Tokiu atveju bendrasis planavimas sukuria suplanuotus užsakymus, kurių kiekis apskaičiuojamas kaip prognozuojamas kiekis × kiekvieno laikotarpio mažinimo raktas. Jei kitų poreikio tipų, bendrasis planavimas taip pat sukuria suplanuotus užsakymus, kad tenkintų poreikį.

#### <a name="example-percent--reduction-key"></a>Pavyzdys: procentai – mažinimo raktas

Šiame pavyzdyje parodoma, kaip mažinimo raktas sumažina poreikio prognozės poreikius pagal procentines dalis ir laikotarpius, kuriuos nurodo mažinimo raktas.

Pavyzdžiui, į bendrąjį planą galite įtraukti toliau nurodytą poreikio prognozę.

| Mėnuo    | Poreikio prognozė |
|----------|-----------------|
| Sausio  | 1000           |
| Vasario | 1000           |
| Kovo    | 1000           |
| Balandžio    | 1000           |

Puslapyje **Mažinimo raktai** nustatykite toliau nurodytas eilutes.

| Keitimas | Vienetas  | Procentas |
|--------|-------|---------|
| 1      | Mėnuo | 100     |
| 2      | Mėnuo | 75      |
| 3      | Mėnuo | 50      |
| 4      | Mėnuo | 25      |

Priskirkite mažinimo raktą prekės draudimo grupei. Puslapio **Bendrieji planai** lauke **Prognozes poreikių mažinimo metodas** pasirinkite **Procentai – mažinimo raktas**.

Tokiu atveju, jei prognozės planavimą paleisite sausio 1 d., poreikio prognozės poreikiai bus naudojami atsižvelgiant į procentus, nustatytus puslapyje **Mažinimo raktai**. Toliau nurodyti poreikio kiekiai perkeliami į bendrąjį planą.

| Mėnuo                | Suplanuoto užsakymo kiekis | Skaičiavimas    |
|----------------------|------------------------|----------------|
| Sausio              | 0                      | = 0 % × 1000   |
| Vasario             | 250                    | = 25 % × 1000  |
| Kovo                | 500                    | = 50 % × 1000  |
| Balandžio                | 750                    | = 75 % × 1000  |
| Gegužė–gruodis | 1000                  | = 100 % × 1000 |

### <a name="transactions--reduction-key"></a>Operacijos – mažinimo raktas

Jei nustatote **metodą, naudojamą prognozės poreikio lauku sumažinti** iki *Operacijos - mažinimo rakto*, rognozės poreikiai yra sumažinami apibrėžtomis poreikio operacijomis, kurios atsiranda per laikotarpius, kuriuos nurodo mažinimo raktas.

Apibrėžtas poreikis apibrėžiamas lauke **Sumažinti prognozę pagal**, kuris yra **padengimo grupių** puslapyje. Jei lauke Sumažinti **prognozę nustatoma kaip** laukelį į *Užsakymai*, tik pardavimo užsakymo operacijos laikomos apibrėžtu poreikiu. Jei nustatėte jį *visoms operacijoms*, bet kokios ne vidinės įmonės išdavimo atsargų operacijos laikomos apibrėžtu poreikiu. **Įtraukti tarpininkaujančios įmonės užsakymas** – Nustatykite šią parinktį į *Taip* jei tarpininkaujančios įmonės užsakymai turi būti įtraukti, kai prognozė sumažinta.

Prognozės sumažinimas prasideda pirmu (anksčiausia) poreikio prognozės įrašu mažinimo rakto laikotarpiu. Jei apibrėžtų atsargų operacijų kiekis yra didesnis nei to paties mažinimo rakto laikotarpio poreikio prognozės eilučių kiekis, atsargų operacijų kiekio balansas bus naudojamas ankstesnio laikotarpio poreikio prognozės kiekiui sumažinti (jei yra nesudengta prognozė).

Jei ankstesniu mažinimo rakto laikotarpiu nelieka nesusumuotos prognozės, atsargų operacijų kiekio balansas bus naudojamas prognozės kiekiui sumažinti kitą mėnesį (jei yra nesudengta prognozė).

Mažinimo rakto eilučių lauko **Procentai** eikšmė nėra naudojama, kai laukas **Prognozės poreikius mažinti naudojamas metodas** yra nustatytas *Operacijos - mažinimo raktas*. Tik datos naudojamos mažinimo rakto laikotarpiui nurodyti.

> [!NOTE]
> Bet kuri prognozė, užregistruota šios dienos arba anksčiau, bus nepaisoma ir nebus naudojama suplanuotiems užsakymams kurti. Pvz., jei jūsų mėnesio poreikio prognozė sugeneruojama sausio 1 d., o jūs vykdote bendrąjį planavimą, į kurį įeina poreikio prognozė sausio 2 d., skaičiavimas nepaisys poreikio prognozės eilutės, kuri yra sausio mėn. 1 d.

#### <a name="example-transactions--reduction-key"></a>Pavyzdys: operacijos – mažinimo raktas

Šiame pavyzdyje parodoma, kaip faktiniai užsakymai, vykdomi per laikotarpius, kuriuos nurodo mažinimo raktas, sumažina poreikio prognozės poreikius.

Šiame pavyzdyje pasirinkite **Operacijos – mažinimo raktas** lauke **Prognozes poreikių mažinimo metodas**, kuris pateiktas puslapyje **Bendrieji planai**.

Sausio 1 d. yra toliau nurodyti pardavimo užsakymai.

| Mėnuo    | Užsakytų vienetų kiekis |
|----------|--------------------------|
| sausio  | 956                      |
| Vasaris | 1 176                    |
| Kovas    | 451                      |
| Balandis    | 119                      |

Jei naudojate tą pačią 1000 vienetų per mėnesį poreikio prognozę, kuri naudota ankstesniame pavyzdyje, į bendrąjį planą perkeliami toliau nurodyti poreikio kiekiai.

| Mėnuo                | Reikalingas vienetų kiekis |
|----------------------|---------------------------|
| sausio              | 44                        |
| Vasario             | 0                         |
| Kovo                | 549                       |
| Balandžio                | 881                       |
| Gegužė–gruodis | 1000                     |

### <a name="transactions--dynamic-period"></a>Operacijos – dinaminis laikotarpis

Jei pasirinksite **Operacijos – dinaminis laikotarpis**, prognozės poreikius sumažina faktinės užsakymų operacijos, vykstančios dinaminiu laikotarpiu. Dinaminis laikotarpis apima dabartinės prognozės datas ir baigiasi, kai prasideda kita prognozė. Tokiu atveju bendrasis planavimas sukuria suplanuotus užsakymus, kad būtų tenkinamas prognozuojamas poreikis (prognozės poreikiai). Tačiau, kai pateikiamos faktinės užsakymų operacijos, prognozės poreikiai sumažinami. Faktinės operacijos sunaudoja prognozuojamų poreikių dalį.

Naudojant šią parinktį, įvyksta toliau pateikti scenarijai.

- Mažinimo raktai nėra būtini arba naudojami. 
- Jei prognozė sumažinama iki galo, dabartinės prognozės poreikiai tampa 0 (nulis).
- Jei nėra ateities prognozės, mažinami poreikiai iš paskutinį kartą įvestos prognozės.
- Laiko ribos įtraukiamos skaičiuojant prognozės mažinimą.
- Teigiamos dienos įtraukiamos skaičiuojant prognozės mažinimą.
- Jei faktinės užsakymo operacijos yra didesnės nei prognozuoti poreikiai, likusios operacijos nėra perduodamos į kitą prognozės laikotarpį.

#### <a name="example-1-transactions--dynamic-period"></a>1 pavyzdys: operacijos – dinaminis laikotarpis

Čia pateiktas paprastas pavyzdys, kuris rodo, kaip veikia metodas **Operacijos – dinaminis laikotarpis**.

Pavyzdžiui, į bendrąjį planą galite įtraukti toliau nurodytą poreikio prognozę.

| Data       | Poreikio prognozė |
|------------|-----------------|
| Sausio 1  | 1000           |
| Vasario 1 | 1000             |

Taip pat galite kurti toliau nurodytus pardavimo užsakymus.

| Data        | Pardavimo užsakymo kiekis |
|-------------|----------------------|
| Sausio 15 d.  | 200                  |
| Vasario 15 | 400                  |

Tokiu atveju kuriami toliau nurodyti suplanuoti užsakymai.

| Poreikio prognozės data | Kiekis | Paaiškinimas                           |
|--------------------- |----------|---------------------------------------|
| Sausio 1            | 800      | Prognozės poreikiai (= 1000 – 200) |
| Sausio 15 d.           | 200      | Pardavimo užsakymų poreikiai             |
| Vasario 1           | 600      | Prognozės poreikiai (= 1000 – 400) |
| Vasario 15          | 400      | Pardavimo užsakymų poreikiai             |

#### <a name="example-2-transactions--dynamic-period"></a>2 pavyzdys: operacijos – dinaminis laikotarpis

Dažniausiai sistemos yra nustatomos taip, kad operacijos sumažintų poreikio prognozę per tam tikrus prognozės laikotarpius: savaites, mėnesius ir t. t. Šie laikotarpiai yra nustatomi mažinimo rakte. Tačiau laiko tarpas tarp dviejų poreikio prognozės eilučių taip pat gali *nurodyti* laikotarpį.

Šiame pavyzdyje sukurkite toliau nurodytų datų ir kiekių poreikio prognozę.

| Data       | Poreikio prognozė |
|------------|-----------------|
| Sausio 1  | 1000           |
| Sausio 5 d.  | 500             |
| Sausio 12 d. | 1000           |

Atkreipkite dėmesį, kad šioje prognozėje nėra aiškaus laikotarpio tarp prognozės datų. Tarp pirmos ir antros datų yra keturių dienų laikotarpis, o tarp antros ir trečios datų yra septynių dienų laikotarpis. Šie laikotarpiai yra dinaminiai laikotarpiai.

Taip pat galite kurti toliau nurodytas pardavimo užsakymų eilutes.

| Data                             | Pardavimo užsakymo kiekis |
|----------------------------------|----------------------|
| Ankstesnių metų gruodžio 15 d. | 500                  |
| Sausio 3 d.                        | 100                  |
| Sausio 10 d.                       | 200                  |

Tokiu atveju prognozė sumažinama toliau nurodytu būdu.

- Kadangi pirmas pardavimo užsakymas nepatenka į jokį laikotarpį, todėl jis nesumažins jokios prognozės.
- Kadangi antras pardavimo užsakymas yra tarp sausio 1 d. ir sausio 5 d., jis sumažins sausio 1 d. prognozę 100.
- Kadangi trečias pardavimo užsakymas yra tarp sausio 5 d. ir sausio 12 d., jis sumažins sausio 5 d. prognozę 200.

Todėl kuriami toliau nurodyti suplanuoti užsakymai.

| Poreikio prognozės data             | Kiekis | Paaiškinimas                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| Ankstesnių metų gruodžio 15 d. | 500      | Pardavimo užsakymų poreikiai                                            |
| Sausio 1                        | 900      | Prognozės poreikių laikotarpis nuo sausio 1 d. iki sausio 5 d. (= 1000 – 100) |
| Sausio 3 d.                        | 100      | Pardavimo užsakymų poreikiai                                            |
| Sausio 5 d.                        | 300      | Prognozės poreikių laikotarpis nuo sausio 5 d. iki sausio 10 d. (= 500 – 200)  |
| Sausio 12 d.                       | 1000    | Prognozės poreikių laikotarpis nuo sausio 12 d. iki pabaigos                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Prognozės mažinimo rakto kūrimas ir nustatymas

Prognozės mažinimo raktas naudojamas su prognozės poreikių mažinimo metoduose **Operacijos – mažinimo raktas** ir **Procentai – mažinimo raktas**. Atlikite toliau nurodytus veiksmus, kad sukurtumėte ir nustatytumėte mažinimo raktą.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Mažinimo raktai**.
2. Pasirinkite **Naujas**, kad sukurtumėte mažinimo raktą.
3. Lauke **Mažinimo raktas** įveskite prognozės mažinimo rakto unikalų identifikatorių. Tada lauke **Pavadinimas** įveskite pavadinimą. 
4. Nurodykite laikotarpius ir kiekvieno laikotarpio mažinimo rakto procentus.

    - Laukas **Įsigaliojimo data** nurodo laikotarpių kūrimo pradžios datą. Kai nustatytas parinkties **Naudoti galiojimo datą** parametras **Taip**, laikotarpiai prasideda įsigaliojimo dieną. Nustačius **Ne**, laikotarpiai prasideda bendrojo planavimo vykdymo dieną.
    - Nurodykite laikotarpius, per kuriuos turėtų būti sumažinta prognozė.
    - Tam tikrame laikotarpyje pateikite procentus, nurodančius, kiek turėtų būti sumažinti prognozės poreikiai. Sumažinti poreikiams galite įvesti teigiamas vertes, o padidinti poreikiams – neigiamas vertes.

## <a name="use-a-reduction-key"></a>Mažinimo rakto naudojimas

Prekės padengimo grupei turi būti priskirtas prognozės mažinimo raktas. Atlikite toliau nurodytus veiksmus, kad priskirtumėte mažinimo raktą prekės padengimo grupei.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**.
2. „FastTab“ **Kita** lauke **Mažinimo raktas** pasirinkite mažinimo raktą, kurį priskirsite padengimo grupei. Tada mažinimo raktas taikomas visoms prekėms, kurios priklauso padengimo grupei.
3. Jei norite naudoti mažinimo raktą, kad apskaičiuotumėte prognozės mažinimą bendrojo planavimo metu, šį parametrą turite nustatyti prognozės plane arba bendrajame plane. Atidarykite vieną iš toliau nurodytų vietų.

    - Bendrasis planavimas \> Sąranka \> Planai \> Prognozės planai
    - Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai

4. Puslapio **Prognozės planai** arba **Bendrieji planai** „FastTab“ **Bendra** lauke **Prognozes poreikių mažinimo metodas** pasirinkite **Procentai – mažinimo raktas** arba **Operacijos – mažinimo raktas**.

## <a name="reduce-a-forecast-by-transactions"></a>Prognozės mažinimas naudojant operacijas

Kai parinktį **Operacijos – mažinimo raktas** arba **Operacijos – dinaminis laikotarpis** pasirenkate kaip prognozės poreikių mažinimo metodą, galite nurodyti, kurios operacijos sumažina prognozę. Puslapio **Padengimo grupės** „FastTab“ konteinerio **Kita** lauke **Prognozę sumažina** pasirinkite **Visos operacijos**, jei visos operacijos turėtų mažinti prognozę, arba **Užsakymai**, jei tik pardavimo užsakymai turėtų mažinti prognozę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Bendrųjų planų apžvalga](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
