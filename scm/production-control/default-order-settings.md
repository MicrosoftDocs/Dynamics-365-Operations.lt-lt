---
title: "Užsakymo numatytąsias dimensijas ir prekių dimensijų kombinacijoje"
description: "Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Numatytieji užsakymo parametrai naudojami kuriant pirkimo užsakymus, pardavimo užsakymus, perkėlimo užsakymus, atsargų žurnalus ir naudojant bendrąjį planavimą generuojant suplanuotus užsakymus. Numatytieji užsakymo parametrai gali būti pritaikyti prekei, vietai, produkto variantui arba produkto dimensijai."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 60abaa69debd891b2fe2dd98184c0dab50b0bf9f
ms.lasthandoff: 03/29/2017


---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Užsakymo numatytąsias dimensijas ir prekių dimensijų kombinacijoje

Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Numatytieji užsakymo parametrai naudojami kuriant pirkimo užsakymus, pardavimo užsakymus, perkėlimo užsakymus, atsargų žurnalus ir naudojant bendrąjį planavimą generuojant suplanuotus užsakymus. Numatytieji užsakymo parametrai gali būti pritaikyti prekei, vietai, produkto variantui arba produkto dimensijai.

Numatytuosius užsakymo parametrus galite nustatyti puslapyje **Numatytieji užsakymo parametrai**. Norėdami atidaryti šį puslapį, eikite į **produkto informacijos valdymo**&gt;**produktai**&gt;**išleisti produktai**&gt; pasirinkite išleido produktą &gt;ant, **planas** arba *** tvarkyti atsargų *** veiksmų sritį &gt;**nurodyti parametrai**&gt;**numatytieji parametrai tvarka**.

## <a name="default-order-settings"></a>Numatytieji užsakymo parametrai
Yra trijų tipų numatytieji užsakymo parametrai, skirti pirkimui, pardavimui ir atsargoms. Numatytieji pirkimo užsakymo parametrai naudojami kuriant:

-   Pirkimo užsakymo eilutės
-   Pirkimo sutarties eilutės
-   Pasiūlymo patvirtinimo eilutės
-   Pirkimo paraiškos eilutės
-   Konsignacijos papildymo eilutės
-   Suplanuoti pirkimo užsakymai

Numatytieji pardavimo užsakymo parametrai naudojami kuriant:

-   Pardavimo užsakymo eilutės
-   Pardavimo sutarties eilutės
-   Pardavimo pasiūlymo eilutės
-   Grąžinimo užsakymo eilutės ir prekės pakeitimo eilutės
-   Poreikio prognozės eilutės

Numatytieji pardavimo užsakymo parametrai taip pat taikomi kuriant:

-   Projekto prekių reikalavimai
-   Aptarnavimo užsakymo prekių poreikiai

Numatytieji atsargų užsakymo parametrai naudojami kuriant:

-   Atsargų žurnalai
-   Perkėlimo užsakymai
-   Suplanuoti perkėlimo užsakymai

Numatytieji atsargų užsakymo parametrai taip pat taikomi kuriant:

-   Sulaikymo užsakymai
-   Kokybės užsakymai
-   Gamybos užsakymai
-   KS eilutės
-   Suplanuoti gamybos užsakymai

## <a name="full-definition-of-a-released-product"></a>Visas išleisto produkto aprašas
Kurdami operaciją, turite nurodyti visiškai išleistas produkto apibrėžimas eilutės prieš Dynamics 365 operacijų bando nustatyti numatytąsias tvarka. Visas išleistas produkto apibrėžimas reiškia, kad prekės numerį ir visus aktyvaus produkto matmenys, pvz., konfigūracija, dydis, stilius ir spalva, nurodomi sandorio. Pavyzdžiui, jei rankiniu būdu kuriate išleisto produkto varianto pirkimo užsakymo eilutę, turite nurodyti visas reikiamas produkto dimensijas prieš tai, kai pagal numatytuosius parametrus užsakymo eilutėje bus rodoma vieta, sandėlis, kiekiai ir vykdymo laikas. 

Ne visi numatytieji užsakymo parametrai taikomi kuriant užsakymą arba žurnalo eilutes. Kiekius ir gamybos laikas rodys tik pagal numatytuosius nustatymus, jei reikia. Pvz., kai inventorizacijos žurnalo eilutę, tik vietai ir sandėliui bus rodomi pagal numatytuosius parametrus kai linija yra sukurta. Akivaizdžiai ne kiekis nustatomas kaip numatytasis ar kelis patikrinimus ir Minimum atliekami kuriant linija arba registravimo žurnalą. 

Kai sukuriamas užsakymas arba žurnalas, sistema visada bando rasti numatytąją vietą ir sandėlį. Pagal numatytuosius parametrus užsakymo parametruose vieta rodoma ne visada. Pavyzdžiui, kuriant pardavimo užsakymą arba pirkimo užsakymą užsakymo antraštėje nurodyta vieta automatiškai naudojama užsakymo eilutėse. Kuriant KS eilutės, naudojama KS antraštės svetainę. Po to, kai svetainė yra nustatyta, jis bus naudojamas rasti bet kurioje svetainėje specifine tvarka parametrus, tada galima kaip numatytąjį sandėlį. 

Numatytasis užsakymo tipas, pirkimo ir atsargų pristatymo laiką galima nepaisyti prekės padengimo taisyklės ant to **prekės padengimas** puslapis. Nors pagal nutylėjimą tvarka neleidžia atskirti gamybą ir perdavimą gamybos laikas, prekės padengimo taisyklės leidžia jį. Tačiau MRP prekės padengimo sąranką naudos tik tada, kai bus kuriami planuotos gamybos ir planuoto perkėlimo užsakymai, ir ji nebus taikoma rankiniu būdu kuriant gamybos ir perkėlimo užsakymus. 

## <a name="default-order-settings-rules"></a>Numatytųjų užsakymo parametrų taisyklės
Galite nurodyti bendruosius numatytuosius užsakymo parametrus ir neribotą skaičių numatytųjų užsakymo parametrų taisyklių, kurios taikomos tik esant tam tikroms sąlygoms, pavyzdžiui, vieta arba konkreti produkto dimensija arba produkto dimensijų kombinacija. Negalima nurodyti tik sandėliui taikomų užsakymo parametrų.

### <a name="rank-in-default-order-settings"></a>Rangas numatytuose užsakymo parametruose

Numatytieji užsakymo parametrai turi rangus. Kuo aukštesnis rangas, tuo svarbesnė taisyklė, o tai reiškia, kad ji turės pirmenybę ir bus naudojama pirmiau negu kitos taisyklės su žemesniais rangais. Bendrųjų numatytųjų užsakymo parametrų rangas nulis, kurio negalima keisti. Gali būti tik viena taisyklė, kurios rangas 0. Taisyklės gali turėti tą patį rangą, jei skiriasi dimensijos, kurioms jos taikomos. Tai naudinga modeliuojant vietai pritaikytus užsakymo parametrus. Sukūrus naują numatytųjų užsakymo parametrų taisyklę, užsakymo vertės, stabdymo žymė ir t. t. perimamos iš taisyklės, kurios rangas nulis, bet jų gali būti nepaisoma.

### <a name="default-order-settings-for-released-products"></a>Išleistiems produktams taikomi numatytieji užsakymo parametrai

Atskiriems išleistiems produktams galite nurodyti bendruosius užsakymo parametrus arba konkrečiai vietai taikomus užsakymo parametrus. Bendrųjų užsakymo parametrų rangas visada nulis. Jeigu vienu metu nustatote naujus pardavimo, pirkimo ir atsargų užsakymo parametrus, puslapyje **Numatytieji užsakymo parametrai ** rekomenduojame naudoti nuostatą **Informacijos rodinys**. Perjungti išsamios informacijos rodinį, pereikite prie to **funkcijos** veiksmų sritį &gt;**puslapis parinktys**&gt;**pakeisti vaizdą**&gt;**išsamios informacijos rodinį**.

### <a name="site-specific-order-settings"></a>Nuo vietos priklausomi užsakymo parametrai

Norėdami sukurti konkrečiai vietai pritaikytus užsakymo parametrus, spustelėkite **Naujas**. Į **išsamios informacijos rodinį**, užpildykite svetainės į **parametrai tinka**&gt;**svetainės** srityje. **Tinklelio rodinys** stulpelyje **Vieta** įveskite vietą. Naujai taisyklei bus automatiškai suteikta nauja reitingo reikšmė, didesnė už nulį. Galite sukurti tiek vietai pritaikytų taisyklių, kiek reikia, ir visoms vietai pritaikytoms taisyklėms galite priskirti tą patį reitingą, kad nurodytumėte, jog jos vienodai svarbios. 

Jei esate dalyje **Informacijos rodinys**, negalite peržiūrėti prekei sukurtų taisyklių. Perjunkite mygtuką **Rodyti / slėpti sąrašą**, kad pamatytumėte peržiūros informaciją. Sukūrus užsakymo eilutę bet kokio tipo ir ji turi ne išmatavo, Dynamics 365 operacijų paieškos taisyklės su ne svetainė, nurodyta parametru. Tai gali padėti nustatyti numatytosios svetainės užsakymo eilutėje. Tada ši vieta naudojama ieškant vietai pritaikytos taisyklės, kurioje gali būti nustatytas numatytasis sandėlis. Šis sandėlis taikomas užsakymo eilutei.

### <a name="specific-order-settings-for-product-dimension"></a>Produkto dimensijai pritaikyti užsakymo parametrai

Galite nurodyti bet kurios aktyvios produkto dimensijos arba aktyvių produkto dimensijų kombinacijos užsakymo parametrų taisykles. Jei produkto dimensijos laukas neužpildytas, tada taisyklė taikoma visoms produkto dimensijos vertėms. 

Atkreipkite dėmesį į toliau pateikiamą produkto pavyzdį.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Product name**                                    | Fotoelektrinis jutiklis                    |
| **Item number**                                     | XW56                                    |
| **Konfigūracija** (naudojama modeliuojant apšvietimo tipą) | C1 – matoma raudona šviesa, C2 – infraraudonųjų spindulių šviesa |
| **Stilius** (naudojamas modeliuojant inžinerijos peržiūrą)  | R1, R2, R3                              |

Pavyzdžiui, tarkime, kad produktas yra ne pagamintas, o įsigytas. Taip pat tarkime, kad konfigūracija C1 naudojama dažniausiai, todėl jos vykdymo laikas trumpesnis. 

Norėdami modeliuoti šį scenarijų, sukurkite toliau nurodytus numatytuosius užsakymo parametrus.

| Rangas | Svetainė | Konfigūravimas | Stilius | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Taip                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kai pirkimo užsakymo eilutė arba suplanuotas pirkimo užsakymas sukuriamas XW56, konfigūracijai C1, nepriklausomai nuo peržiūros ar eilutės buvimo vietos, vykdymo laikas bus 2. Tarkime, kad sustabdytos visos peržiūros, išskyrus R3.

Galite sukurti toliau nurodytus numatytuosius užsakymo parametrus.

| Rangas | Svetainė | Konfigūravimas | Stilius | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Taip                                  |                    | Taip                | Taip                               | Taip             |
| 20   |      |               | R1    | Taip                                  |                    | Taip                | Taip                               | Taip             |
| 10   |      | C1            |       | Taip                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Dviejų senų peržiūrų stabdymui skirtų taisyklių reitingas toks pats, o tai reiškia, kad jos yra vienodai svarbios. Abiejų jų reitingas aukštesnis negu konfigūracijos C1 taisyklės reitingas, o tai reiškia, kad jos svarbesnės negu konfigūracijos C1 taisyklė. 

Šiame pavyzdyje paaiškinama, kodėl reikalingas reitingas. Jei pirkimo užsakymas sukuriamas konfigūracijai C1 ir peržiūrai R2, kai nenurodytas reitingas, šios dvi R2 ir C1 nurodytos taisyklės būtų nevienareikšmiškos. Norėdama išspręsti dviprasmiškumo problemą „Dynamics 365 for Operations“ peržiūri taisykles pagal reitingą mažėjančia tvarka ir pritaiko pirmą taikytiną taisyklę. Dabartiniame pavyzdyje, kai pirkimo užsakymo eilutė sukuriama konfigūracijai C1 ir peržiūrai R2, vartotojas gaus įspėjantį pranešimą, kad prekė sulaikyta ir kad tai įvyko dėl peržiūros vertės. Jei konfigūracijos taisyklės reitingas aukštesnis negu peržiūros taisyklės reitingas, tada konfigūracijos C1 ir peržiūros R2 pirkimo užsakymo eilutė sukuriama sėkmingai ir vartotojas negaus pranešimo „prekė sulaikyta“. 

Atsižvelkite į toliau nurodytas numatytojo užsakymo parametro taisykles.

| Rangas | Svetainė | Konfigūravimas | Stilius | Numatytoji vieta | Numatytasis sandėlis | Pirkimas – nepaisyti numatytųjų saugojimo dimensijų | Pirkimo sandėlis |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Taip                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Sistema išanalizuoja taisyklių rinkinį du kartus, kad nustatytų vietą ir sandėlį. Sukūrus pirkimo užsakymo eilutės konfigūracijos C1, R2, stiliaus svetainės nustatomas remiantis rango 10 taisyklę. Tada sistema ieško svetainę 2 taisyklę, kad būtų galima nustatyti sandėlio. Randama 20 taisyklė ir, kadangi jos reitingas aukštesnis, pirkimo užsakymo eilutėje nurodomas sandėlis 22, o ne 21. 

Paprastai specialiųjų taisyklių ir svarbesnių negu kitos dimensijos dimensijų taisyklių reitingai būna aukštesni, o bendresnių taisyklių reitingai būna mažesni. 

Taisyklė, kurios reitingas nulis, naudojama kaip apsauginė sąlyga. Jei nėra kitų taisyklių, tada naudojami nulinės taisyklės numatytieji užsakymo parametrai. 

Kadangi labai svarbus reitingo skaičius, veiksmų srityje **Numatytieji užsakymo parametrai **pateikiamos funkcijos, kuriomis naudojantis galima perkelti taisyklę aukštyn arba žemyn ir iš naujo numeruoti taisykles, taip, kad jos būtų visada išdėstomos intervalais po 10. 

Išleistam produktui sukurtų taisyklių skaičius gali būti didelis. Norint geriau suprasti, ko nepaisoma vadovaujantis kiekviena taisykle ir kodėl kiekviena taisyklė reikalinga, rekomenduojame naudoti puslapyje** Numatytieji užsakymo parametrai** esantį **Tinklo rodinį**. Tinklelio rodinį galite įjungti eikite į į **funkcijos** veiksmų sritį &gt;**puslapis parinktys**&gt;**pakeisti vaizdą**&gt;**tinklelio rodinį**. Tinklelyje rodomų stulpelių skaičius gali būti gana svarbus, ypač pardavimo ir atsargų skirtukuose. Apriboti rodomas tinklelio stulpelių skaičių, grupių stulpelių gali būti paslėpti ar rodomas naudojant mygtukus ant to **numatytieji užsakymo parametrai**&gt;**stulpelių rodymo** meniu.

### <a name="specific-order-settings-for-released-product-variant"></a>Išleisto produkto variantui pritaikyti užsakymo parametrai

Jei numatytųjų užsakymo parametrų taisyklės sistema per daug sudėtinga, yra galimybė tiesiog nurodyti kiekvieno produkto varianto numatytuosius užsakymo parametrus. Toliau pateiktuose pavyzdžiuose parodoma, kaip tai atrodys konkretaus produkto atveju ir pirmiau aprašytais atvejais.

| Rangas | Svetainė | Konfigūravimas | Stilius | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Taip                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Taip                                  | 5                  | Taip                | Taip                               | Taip             |
| 10   |      | C2            | R1    | Taip                                  | 5                  | Taip                | Taip                               | Taip             |
| 10   |      | C1            | R3    | Taip                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Taip                                  | 2                  | Taip                | Taip                               | Taip             |
| 10   |      | C1            | R1    | Taip                                  | 2                  | Taip                | Taip                               | Taip             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Reitingas šiuo atveju nėra svarbus, todėl galite jį paslėpti. Šis sprendimas gali būti techninės priežiūros problemos priežastis. Tačiau, galbūt norėsite naudoti šią sąranką, jeigu svarstote integravimo su produkto naudojimo ciklo valdymo (PLM) sistemomis galimybę.


