---
title: Pagrindinis planavimas su paklausos prognozėmis
description: Ši tema aiškina, kaip įtraukti paklausos prognozes pagrindinio planavimo metu su „Planning Optimization“.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f322dd63cb2dee6a9048e6ed086dc075cc0e1b9
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474849"
---
# <a name="master-planning-with-demand-forecasts"></a>Pagrindinis planavimas su paklausos prognozėmis

[!include [banner](../../includes/banner.md)]

Galite naudoti paklausos prognozę kartu su „Planning Optimization“ siekiant apskaičiuoti tikėtiną paklausą jūsų pagrindiniame planavime. Galite rankiniu būdu sukurti paklauso prognozę, ją importuoti arba sukurti ją naudodami paklauso prognozės funkcijas „Microsoft Dynamics 365 Supply Chain Management“. Išsamesnės informacijos apie poreikio prognozes rasite [Poreikio prognozių apžvalga](../introduction-demand-forecasting.md).

> [!NOTE]
> Atskiras prognozės planavimas nepalaikomas su „Planning Optimization“. Dėl to, **Esamas prognozės planas** nustatymas puslapyje **Pagrindinio planavimo parametrai** neturi jokio poveikio jums naudojant „Planning Optimization“.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Nustatykite pagrindinį planą, kad apimtų poreikio prognozę

Norėdami konfigūruoti pagrindinį planą taip, kad jis įtrauktų paklausos prognozę, atlikite šiuos žingsnius.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Pasirinkite esamą planą ar sukurkite naują.
1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Prognozės modelis** – Pasirinkite taikomą prognozės modelį. Šis modelis bus laikomas galiojančiu, kai tiekimo siūlymas yra sukuriamas esamam pagrindiniam planui.
    - **Įtraukti paklausos prognozę** – Nustatykite šią parinktį į *Taip*, kad ji įtraukti paklausos prognozę esamame pagrindiniame plane. Jei nustatote *Ne*, paklausos prognozės perlaidos nebus įtrauktos į pagrindinį planą.
    - **Metodas naudojamas siekiant sumažinti prognozės reikalavimus** – Pasirinkite metodą, kuris turi būti naudojamas siekiant sumažinti prognozės reikalavimus. Dėl daugiau informacijos, žr. [Prognozės sumažinimo raktai](#reduction-keys) skyrių vėliau šioje skyriuje.

1. „FastTab“ **Laiko tvora dienomis** galite nustatyti tolesnius laukelius siekiant nustatyti laikotarpį, per kurį yra įtraukta paklausos prognozė:

    - **Prognozės planas** – Nustatykite parinktį į *Taip* tam, kad ji viršytų prognozės plano laikos tvarką, kurios ištakos yra atskiros apimties grupėse. Nustatykite ją į *Ne* tam, kad naudotumėte vertės atskiros apimties grupėms esamame pagrindiniame plane.
    - **Prognozės laiko laikotarpis** – Jei nustatote **Prognozės plano** parinktį į *Taip*, nurodykite dienų skaičių (nuo šiandienos), kuriam bus taikoma paklausos prognozė.

    > [!IMPORTANT]
    > Nustatymas **Prognozės planas** dar nėra palaikomas su „Planning Optimization“.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Nustatykite apimties grupė, kad ji apimtų poreikio prognozę

Norėdami konfigūruoti apimties grupę taip, kad ji įtrauktų paklausos prognozę, atlikite šiuos žingsnius.

1. Eikite į **Pagrindinis planavimas \> Nustatymas \> Planai \> Apimties grupės**.
1. Pasirinkite esamą apimties grupę ar sukurkite naują.
1. „FastTab“ **Kita**, nustatykite tolesnes vertes:

    - **Prognozės plano laiko tvora** – Įveskite dienų skaičių (nuo šiandienos), kuriam bus taikoma paklausos prognozė. Ši vertė gali būti viršijama naudojant **Prognozės plano** parinktį pagrindiniame plane, kaip aprašyta ankstesniame skyriuje.
    - **Sumažinimo raktas** – Pasirinkite taikomą sumažinimo raktą. Dėl daugiau informacijos, žr. [Sukurkite ir nustatykite prognozės sumažinimo raktą](#create-reduction-key) ir [Naudokite sumažinimo rakto](#use-reduction-key) skyrius toliau šioje temoje.
    - **Sumažinkite prognozę** – Pagrindiniams planams, kai **Metodas naudojamas siekiant sumažinti prognozės reikalavimus** laukelį, kuris nustatytas *Perlaidos - sumažinimo raktas* ar *Perlaidos - dinaminis laikotarpis*, nurodykite perlaidas, kurios turi sumažinti prognozę. Pasirinkite vieną iš šių reikšmių:

        - **Visos perlaidos** – Visos perlaidos turi sumažinti prognozę.
        - **Užsakymai** – Tik pardavimo užsakymai turi sumažinti prognozę.

        > [!NOTE]
        > Jei pasirenkate *Visos perlaidos*, perlaidos turinčios paklausą ir tiekimą tuose pačiuose inventoriaus dimensijose bus laikomos neutraliomis ir ignoruojamomis prognozės mažinimo metu. Pavyzdžiui, jei planavimo dimensija yra nustatyta tik į saitą, ne sandėlį, perlaidos užsakymas tarp saito 1, sandėlis 11 ir saito 1, sandėlis 13, bus ignoruojama ir nesumažins likusios paklausos prognozės.

    - **Įtraukti tarpininkaujančios įmonės užsakymas** – Nustatykite šią parinktį į *Taip* jei tarpininkaujančios įmonės užsakymai turi būti įtraukti, kai prognozė sumažinta. Kitu atveju, nustatykite į *Ne*.
    - **Įtraukite tinkintą prognozę paklauso prognozėje** – Nurodykite, ar tinkinta prognozė turi būti įtraukta į bendrą prognozę. Ši parinktis nustato, kaip esama paklausa sumažina prognozės paklausą. Galite naudoti ją siekiant užtikrinti, kad pagrindinis planavimas apimtų prekių tiekimą, kurios yra perkamos konkrečių klientų.

        - Nustatykite šią parinktį į *Taip* tam, kad įtrauktumėte kliento prognozę bendroje prognozėje. Šiuo atveju, reali kliento paklausa sumažina kliento prognozę ir bendrą prognozę. Pagrindinis planavimas sukuria suplanuotus užsakymus, kad jie padengtų bendrą prognozės kiekį.
        - Nustatykite šią parinktį į *Ne*, jei nenorite įtraukti kliento prognozės į bendrą prognozę. Šiuo atveju, reali kliento paklausa sumažina tik kliento prognozę ir bendrą prognozę. Pagrindinis planavimas sukuria suplanuotus užsakymus, kad jie padengtų tiek bendrą prognozės kiekį, tiek prognozę kiekvieno kliento kiekiui.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Prognozės mažinimo raktai

Šis skyrius pateikia informaciją apie skirtingus metodus, kurie yra naudojami siekiant sumažinti prognozės reikalavimus. Joje pateikiami kiekvieno metodo rezultatų pavyzdžiai. Joje taip pat paaiškinama, kaip kurti, nustatyti ir naudoti prognozės mažinimo raktą. Kai kuriuose metoduose naudojamas mažinimo raktas siekiant sumažinti prognozės poreikius.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Naudojami prognozes poreikių mažinimo metodai

Kai įtraukiate prognozę į bendrąjį planą, galite pasirinkti, kaip mažinami prognozės poreikiai, kai faktinis poreikis yra įtrauktas. Atkreipkite dėmesį, kad bendrasis planavimas neapima buvusių prognozės poreikių, t. y. visų prognozės poreikių, kurių data yra ankstesnė nei šios dienos data.

Norėdami įtraukti prognozę į bendrąjį planą ir pasirinkti metodą, kuris naudojamas siekiant sumažinti prognozės poreikius, pasirinkite **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**. Lauke **Prognozės modelis** pasirinkite prognozės modelį. Lauke **Prognozes poreikių mažinimo metodas** pasirinkite metodą. Galimos toliau nurodytos parinktys.

- Nėra
- Procentai – mažinimo raktas
- Perlaidos - sumažinimo raktas (dar nėra palaikomas su „Planning Optimization“).
- Operacijos – dinaminis laikotarpis

Tolesniuose skyriuose pateikiama daugiau informacijos apie kiekvieną parinktį.

#### <a name="none"></a>Nėra

Jei pasirinksite **Nėra**, prognozės poreikiai bendrojo planavimo metu nebus sumažinti. Tokiu atveju bendrasis planavimas sukuria suplanuotus užsakymus, kad būtų tenkinamas prognozuojamas poreikis (prognozės poreikiai). Šiuose suplanuotuose užsakymuose tvarkomas siūlomas kiekis, nepriklausomai nuo kitų poreikio tipų. Pvz., jei pateikiami pardavimo užsakymai, bendrasis planavimas sukuria papildomus suplanuotus užsakymus, kad tiektų pardavimo užsakymams skirtus produktus. Prognozės poreikių kiekis nėra sumažinamas.

#### <a name="percent--reduction-key"></a>Procentai – mažinimo raktas

Jei pasirinksite **Procentas – mažinimo raktas**, prognozės poreikiai sumažinami pagal procentines dalis ir laiko laikotarpius, kurie nurodomi mažinimo raktu. Tokiu atveju bendrasis planavimas sukuria suplanuotus užsakymus, kurių kiekis apskaičiuojamas kaip prognozuojamas kiekis × kiekvieno laikotarpio mažinimo raktas. Jei kitų poreikio tipų, bendrasis planavimas taip pat sukuria suplanuotus užsakymus, kad tenkintų poreikį.

##### <a name="example-percent--reduction-key"></a>Pavyzdys: procentai – mažinimo raktas

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

#### <a name="transactions--reduction-key"></a>Operacijos – mažinimo raktas

Jei nustatote **metodą, naudojamą prognozės poreikio lauku sumažinti** iki *Operacijos - mažinimo rakto*, rognozės poreikiai yra sumažinami apibrėžtomis poreikio operacijomis, kurios atsiranda per laikotarpius, kuriuos nurodo mažinimo raktas.

Apibrėžtas poreikis apibrėžiamas lauke **Sumažinti prognozę pagal**, kuris yra **padengimo grupių** puslapyje. Jei lauke Sumažinti **prognozę nustatoma kaip** laukelį į *Užsakymai*, tik pardavimo užsakymo operacijos laikomos apibrėžtu poreikiu. Jei nustatėte jį *visoms operacijoms*, bet kokios ne vidinės įmonės išdavimo atsargų operacijos laikomos apibrėžtu poreikiu. **Įtraukti tarpininkaujančios įmonės užsakymas** – Nustatykite šią parinktį į *Taip* jei tarpininkaujančios įmonės užsakymai turi būti įtraukti, kai prognozė sumažinta.

Prognozės sumažinimas prasideda pirmu (anksčiausia) poreikio prognozės įrašu mažinimo rakto laikotarpiu. Jei apibrėžtų atsargų operacijų kiekis yra didesnis nei to paties mažinimo rakto laikotarpio poreikio prognozės eilučių kiekis, atsargų operacijų kiekio balansas bus naudojamas ankstesnio laikotarpio poreikio prognozės kiekiui sumažinti (jei yra nesudengta prognozė).

Jei ankstesniu mažinimo rakto laikotarpiu nelieka nesusumuotos prognozės, atsargų operacijų kiekio balansas bus naudojamas prognozės kiekiui sumažinti kitą mėnesį (jei yra nesudengta prognozė).

Mažinimo rakto eilučių lauko **Procentai** eikšmė nėra naudojama, kai laukas **Prognozės poreikius mažinti naudojamas metodas** yra nustatytas *Operacijos - mažinimo raktas*. Tik datos naudojamos mažinimo rakto laikotarpiui nurodyti.

> [!NOTE]
> Bet kuri prognozė, užregistruota šios dienos arba anksčiau, bus nepaisoma ir nebus naudojama suplanuotiems užsakymams kurti. Pvz., jei jūsų mėnesio poreikio prognozė sugeneruojama sausio 1 d., o jūs vykdote bendrąjį planavimą, į kurį įeina poreikio prognozė sausio 2 d., skaičiavimas nepaisys poreikio prognozės eilutės, kuri yra sausio mėn. 1 d.

##### <a name="example-transactions--reduction-key"></a>Pavyzdys: operacijos – mažinimo raktas

Šiame pavyzdyje parodoma, kaip faktiniai užsakymai, vykdomi per laikotarpius, kuriuos nurodo mažinimo raktas, sumažina poreikio prognozės poreikius.

[![Faktiniai užsakymai ir prognozė prieš paleidus bendrąjį planavimą.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Šiame pavyzdyje pasirinkite *Operacijos – mažinimo raktas* lauke **Prognozes poreikių mažinimo metodas**, kuris pateiktas puslapyje **Bendrieji planai**.

Šios poreikio prognozės eilutės yra balandžio 1 d.

| Data     | Suplanuotas vienetų kiekis |
|----------|-----------------------------|
| balandžio mėn. 5 d.   | 100                         |
| balandžio mėn. 12 d.  | 100                         |
| balandžio mėn. 19 d.  | 100                         |
| balandžio mėn. 26 d.  | 100                         |
| gegužės mėn. 3 d.    | 100                         |
| gegužės mėn. 10 d.   | 100                         |
| gegužės mėn. 17 d.   | 100                         |

Šios pardavimo užsakymų eilutės yra balandžio mėnesį.

| Data     | Būtinas vienetų kiekis |
|----------|----------------------------|
| balandžio mėn. 27 d.  | 240                        |

[![Suplanuotas tiekimas, sugeneruotas pagal balandžio užsakymus.](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

Šie poreikio kiekiai perkeliami į bendrąjį planą, kai bendrasis planavimas vykdomas balandžio 1 d. Kaip matote, balandžio prognozės operacijos buvo sumažintos poreikio kiekiu (240) sekoje, pradedant nuo pirmos iš šių operacijų.

| Data     | Reikalingas vienetų kiekis |
|----------|---------------------------|
| balandžio mėn. 5 d.   | 0                         |
| balandžio mėn. 12 d.  | 0                         |
| balandžio mėn. 19 d.  | 60                        |
| balandžio mėn. 26 d.  | 100                       |
| balandžio mėn. 27 d.  | 240                       |
| gegužės mėn. 3 d.    | 100                       |
| gegužės mėn. 10 d.   | 100                       |
| gegužės mėn. 17 d.   | 100                       |

Dabar tarkime, kad nauji užsakymai buvo importuoti gegužės laikotarpiu.

Šios pardavimo užsakymų eilutės yra gegužės mėnesį.

| Data   | Būtinas vienetų kiekis |
|--------|----------------------------|
| gegužės mėn. 4 d.  | 80                         |
| gegužės mėn. 11 d. | 130                        |

[![Suplanuotas tiekimas, sugeneruotas pagal balandžio ir gegužės užsakymus.](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

Šie poreikio kiekiai perkeliami į bendrąjį planą, kai bendrasis planavimas vykdomas balandžio 1 d. Kaip matote, balandžio prognozės operacijos buvo sumažintos poreikio kiekiu (240) sekoje, pradedant nuo pirmos iš šių operacijų. Tačiau gegužės prognozės operacijos buvo sumažintos iš viso 210, pradedant nuo pirmos poreikio prognozės operacijos gegužės dieną. Tačiau išsaugomos bendrosios laikotarpio sumos (balandžio mėn. 400 d. ir gegužės 300 d.).

| Data     | Reikalingas vienetų kiekis |
|----------|---------------------------|
| balandžio mėn. 5 d.   | 0                         |
| balandžio mėn. 12 d.  | 0                         |
| balandžio mėn. 19 d.  | 60                        |
| balandžio mėn. 26 d.  | 100                       |
| balandžio mėn. 27 d.  | 240                       |
| gegužės mėn. 3 d.    | 0                         |
| gegužės mėn. 4 d.    | 80                        |
| gegužės mėn. 10 d.   | 0                         |
| gegužės mėn. 11 d.   | 130                       |
| gegužės mėn. 17 d.   | 90                        |

#### <a name="transactions--dynamic-period"></a>Operacijos – dinaminis laikotarpis

Jei pasirinksite **Operacijos – dinaminis laikotarpis**, prognozės poreikius sumažina faktinės užsakymų operacijos, vykstančios dinaminiu laikotarpiu. Dinaminis laikotarpis apima dabartinės prognozės datas ir baigiasi, kai prasideda kita prognozė. Tokiu atveju bendrasis planavimas sukuria suplanuotus užsakymus, kad būtų tenkinamas prognozuojamas poreikis (prognozės poreikiai). Tačiau, kai pateikiamos faktinės užsakymų operacijos, prognozės poreikiai sumažinami. Faktinės operacijos sunaudoja prognozuojamų poreikių dalį.

Naudojant šią parinktį, įvyksta toliau pateikti scenarijai.

- Mažinimo raktai nėra būtini arba naudojami. 
- Jei prognozė sumažinama iki galo, dabartinės prognozės poreikiai tampa 0 (nulis).
- Jei nėra ateities prognozės, mažinami poreikiai iš paskutinį kartą įvestos prognozės.
- Laiko ribos įtraukiamos skaičiuojant prognozės mažinimą.
- Teigiamos dienos įtraukiamos skaičiuojant prognozės mažinimą.
- Jei faktinės užsakymo operacijos yra didesnės nei prognozuoti poreikiai, likusios operacijos nėra perduodamos į kitą prognozės laikotarpį.

##### <a name="example-1-transactions--dynamic-period"></a>1 pavyzdys: operacijos – dinaminis laikotarpis

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

##### <a name="example-2-transactions--dynamic-period"></a>2 pavyzdys: operacijos – dinaminis laikotarpis

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Prognozės mažinimo rakto kūrimas ir nustatymas

Prognozės mažinimo raktas naudojamas su prognozės poreikių mažinimo metoduose **Operacijos – mažinimo raktas** ir **Procentai – mažinimo raktas**. Atlikite toliau nurodytus veiksmus, kad sukurtumėte ir nustatytumėte mažinimo raktą.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Mažinimo raktai**.
2. Pasirinkite **Naujas**, kad sukurtumėte mažinimo raktą.
3. Lauke **Mažinimo raktas** įveskite prognozės mažinimo rakto unikalų identifikatorių. Tada lauke **Pavadinimas** įveskite pavadinimą. 
4. Nurodykite laikotarpius ir kiekvieno laikotarpio mažinimo rakto procentus.

    - Laukas **Įsigaliojimo data** nurodo laikotarpių kūrimo pradžios datą. Kai nustatytas parinkties **Naudoti galiojimo datą** parametras **Taip**, laikotarpiai prasideda įsigaliojimo dieną. Nustačius **Ne**, laikotarpiai prasideda bendrojo planavimo vykdymo dieną.
    - Nurodykite laikotarpius, per kuriuos turėtų būti sumažinta prognozė.
    - Tam tikrame laikotarpyje pateikite procentus, nurodančius, kiek turėtų būti sumažinti prognozės poreikiai. Sumažinti poreikiams galite įvesti teigiamas vertes, o padidinti poreikiams – neigiamas vertes.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Mažinimo rakto naudojimas

Prekės padengimo grupei turi būti priskirtas prognozės mažinimo raktas. Atlikite toliau nurodytus veiksmus, kad priskirtumėte mažinimo raktą prekės padengimo grupei.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**.
2. „FastTab“ **Kita** lauke **Mažinimo raktas** pasirinkite mažinimo raktą, kurį priskirsite padengimo grupei. Tada mažinimo raktas taikomas visoms prekėms, kurios priklauso padengimo grupei.
3. Jei norite naudoti mažinimo raktą, kad apskaičiuotumėte prognozės mažinimą bendrojo planavimo metu, šį parametrą turite nustatyti prognozės plane arba bendrajame plane. Atidarykite vieną iš toliau nurodytų vietų.

    - **Bendrasis planavimas \> Nustatymas \> Planai \> Prognozės planai**
    - **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**

4. Puslapio **Prognozės planai** arba **Bendrieji planai** „FastTab“ **Bendra** lauke **Prognozes poreikių mažinimo metodas** pasirinkite **Procentai – mažinimo raktas** arba **Operacijos – mažinimo raktas**.

### <a name="reduce-a-forecast-by-transactions"></a>Prognozės mažinimas naudojant operacijas

Kai parinktį **Operacijos – mažinimo raktas** arba **Operacijos – dinaminis laikotarpis** pasirenkate kaip prognozės poreikių mažinimo metodą, galite nurodyti, kurios operacijos sumažina prognozę. Puslapio **Padengimo grupės** „FastTab“ konteinerio **Kita** lauke **Prognozę sumažina** pasirinkite **Visos operacijos**, jei visos operacijos turėtų mažinti prognozę, arba **Užsakymai**, jei tik pardavimo užsakymai turėtų mažinti prognozę.

## <a name="forecast-models-and-submodels"></a>Prognozės modeliai ir antriniai modeliai

Šiame skyriuje aprašoma, kaip kurti prognozės modelius ir kaip sujungti kelis prognozės modelius nustatant antrinius modelius.

*Prognozės modelis* įvardija ir identifikuoja konkrečią prognozę. Sukūrę prognozės modelį, prie jo galite pridėti prognozės eilutes. Norėdami įtraukti kelių prekių prognozės eilutes, naudokite puslapį **Poreikio prognozės eilutės**. Norėdami konkrečiai pasirinktai prekei pridėti prognozės eilutes, naudokite puslapį **Išleisti produktai**.

Prognozės modelis gali apimti prognozes iš kitų prognozės modelių. Norėdami pasiekti šį rezultatą, kitus prognozės modelius galite pridėti kaip pirminio prognozės modelio *antrinius modelius*. Kad jį galėtumėte pridėti kaip pirminio prognozės modelio antrinį modelį, turite sukurti kiekvieną atitinkamą modelį.

Gauta struktūra leidžia valdyti prognozes galingu būdu, nes ji leidžia sujungti (telkti) įvestį iš kelių atskirų prognozių. Todėl planavimo požiūriu yra nesunku suderinti modeliavimų prognozes. Pavyzdžiui, galite nustatyti modeliavimą, pagrįstą įprastos prognozės ir pavasario akcijos prognozės deriniu.

### <a name="submodel-levels"></a>Antrinio modelio lygiai

Antrinių modelių, kuriuos galima pridėti prie pirminio prognozės modelio, skaičius neribojamas. Tačiau struktūra gali būti tik vieno lygio. Kitaip tariant, prognozės modelis, kuris yra kito prognozės modelio antrinis modelis, negali turėti savo antrinio modelio. Kaip prie prognozės modelio pridedate antrinius modelius, sistema tikrina, ar tas prognozės modelis jau yra kito prognozės modelio antrinis modelis.

Jei bendrojo planavimo metu susiduriama su antriniu modeliu, kuris turi savo antrinius modelius, gausite klaidos pranešimą.

#### <a name="submodel-levels-example"></a>Antrinių modelių lygių pavyzdys

Prognozės A modelio prognozės B modelis yra antrinis modelis. Todėl B prognozės modelis negali turėti savo antrinių modelių. Jei prie B prognozės modelio bandysite pridėti antrinį modelį, gausite šį klaidos pranešimą: „B prognozės modelis yra A modelio antrinis modelis.“

### <a name="aggregating-forecasts-across-forecast-models"></a>Prognozių telkimas prognozių modeliuose

Tą pačią dieną įvykstančios prognozės eilutės telkiamos jų prognozės modelyje ir antriniuose modeliuose.

#### <a name="aggregation-example"></a>Telkimo pavyzdys

Prognozės A modelio prognozės B ir C modeliai yra antriniai modeliai.

- Prognozės A modelis apima 2 vienetų (vnt.) poreikio prognozę birželio 15 d.
- Prognozės B modelis apima 3 vnt. poreikio prognozę birželio 15 d.
- Prognozės C modelis apima 4 vnt. poreikio prognozę birželio 15 d.

Gauta poreikio prognozė bus vienas poreikis 9 vnt. (2 + 3 + 4) birželio 15 d.

> [!NOTE]
> Kiekvienas antrinis modelis naudoja savo, o ne pirminio prognozės modelio parametrus.

### <a name="create-a-forecast-model"></a>Prognozės modelio kūrimas

Norėdami kurti prognozės modelį, atlikite nurodytus veiksmus.

1. Eikite į **Bendrasis planavimas \> Nustatymas \> Poreikio prognozė \> Prognozės modeliai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujam prognozės modeliui nustatykite tokius laukelius:

    - **Modelis** – įveskite unikalų modelio identifikatorių.
    - **Pavadinimas** – įveskite modelį aprašantį pavadinimą.
    - **Sustabdyta** – paprastai šią parinktį reikėtų nustatyti kaip *Ne*. Nustatykite *Taip* tik jei norite uždrausti redaguoti visas modeliui priskirtas prognozės eilutes.

    > [!NOTE]
    > Laukelis **Įtraukti biudžeto srautų prognozes** ir laukeliai „FastTab“ skirtuke **Projektas** nėra susiję su bendruoju planavimu. Todėl šiame kontekste galite jų nepaisyti. Turite juos apsvarstyti tik kai dirbate su modulio **Projekto valdymas ir apskaita** prognozėmis.

### <a name="assign-submodels-to-a-forecast-model"></a>Prognozės modelio kaip antrinio modelio priskyrimas

Kad prognozės modeliui priskirtumėte produkto savininką, atlikite nurodytus veiksmus.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Prognozė \> Prognozės modeliai**.
1. Sąrašo srityje pasirinkite prognozės modelį, kuriam norite nustatyti antrinį modelį.
1. „FastTab“ skirtuke **Antrinis modelis** pasirinkite **Pridėti** ir prie tinklelio pridėkite eilutę.
1. Naujoje eilutėje nustatykite šiuos laukus:

    - **Antrinis modelis** – pasirinkite prognozės modelį, kurį norite pridėti kaip antrinį modelį. Šis prognozės modelis jau turi egzistuoti ir neturi turėti savo antrinių modelių.
    - **Pavadinimas** – antriniam modeliui įveskite aprašantį pavadinimą. Pavyzdžiui, šis pavadinimas gali nurodyti antrinio modelio ryšį su pirminiu prognozės modeliu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

