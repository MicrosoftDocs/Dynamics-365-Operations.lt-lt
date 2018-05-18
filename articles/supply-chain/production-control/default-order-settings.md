---
title: "Numatytieji dimensijų ir produkto variantų užsakymo parametrai"
description: "Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: d0e8d1ac8b775f9c728d6bfa6ba219dd889bf8a2
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Numatytieji dimensijų ir produkto variantų užsakymų parametrai

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Numatytuose „Microsoft Dynamics 365 for Finance and Operations“ užsakymo parametruose nurodyta vieta ir sandėlis, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Numatytieji užsakymo parametrai naudojami kuriant pirkimo užsakymus, pardavimo užsakymus, perkėlimo užsakymus, atsargų žurnalus ir naudojant bendrąjį planavimą generuojant suplanuotus užsakymus. Numatytieji užsakymo parametrai gali būti pritaikyti prekei, vietai, produkto variantui arba produkto dimensijai.

Numatytuosius užsakymo parametrus galite nustatyti puslapyje **Numatytieji užsakymo parametrai**. Norėdami atidaryti šį puslapį, eikite į **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Išleisti produktai** &gt; **Pasirinkti išleistą produktą** &gt; veiksmų srityje **Planas** arba **Valdyti atsargas** &gt; **Užsakymo parametrai** &gt; **Numatytieji užsakymo parametrai**.

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
Kurdami operaciją eilutėje turite nurodyti visą išleisto produkto apibrėžimą prieš tai, kai „Finance and Operations“ pabandys nustatyti numatytuosius užsakymo parametrus. Visas išleisto produkto apibrėžimas reiškia, kad prekės numeris ir visos aktyvios produkto dimensijos, pavyzdžiui, konfigūracija, dydis, stilius ir spalva yra nurodytos operacijoje. Pavyzdžiui, jei rankiniu būdu kuriate išleisto produkto varianto pirkimo užsakymo eilutę, turite nurodyti visas reikiamas produkto dimensijas prieš tai, kai pagal numatytuosius parametrus užsakymo eilutėje bus rodoma vieta, sandėlis, kiekiai ir vykdymo laikas. 

Ne visi numatytieji užsakymo parametrai taikomi kuriant užsakymą arba žurnalo eilutes. Kiekiai ir vykdymo laikai bus rodomi tik pagal numatytuosius parametrus ir tik prireikus. Pavyzdžiui, skaičiuojant žurnalo eilutę, kai sukurta eilutė, pagal numatytuosius parametrus rodoma tik vieta ir sandėlis. Žinoma, kuriant eilutę arba registruojant žurnalą nenustatomos jokios numatytosios kiekio reikšmės ir neatliekami jokie kartotinių ir minimalių reikšmių patikrinimai. 

Kai sukuriamas užsakymas arba žurnalas, sistema visada bando rasti numatytąją vietą ir sandėlį. Pagal numatytuosius parametrus užsakymo parametruose vieta rodoma ne visada. Pavyzdžiui, kuriant pardavimo užsakymą arba pirkimo užsakymą užsakymo antraštėje nurodyta vieta automatiškai naudojama užsakymo eilutėse. Kuriant KS eilutę naudojama KS antraštėje nurodyta vieta. Nustačius vietą ji naudojama norint rasti visus konkrečios vietos užsakymo parametrus, kuriuos galima naudoti kaip numatytuosius sandėlio parametrus. 

Atsižvelgiant į puslapyje **Prekės padengimas** nurodytas prekės padengimo taisykles, numatytojo užsakymo tipo, pirkimo ir atsargų pristatymo laikų gali būti nepaisoma. Nors pagal numatytuosius užsakymo parametrus skirtumas tarp gamybos ir perkėlimo vykdymo laiko negalimas, prekės padengimo taisyklėse jis leidžiamas. Tačiau MRP prekės padengimo sąranką naudos tik tada, kai bus kuriami planuotos gamybos ir planuoto perkėlimo užsakymai, ir ji nebus taikoma rankiniu būdu kuriant gamybos ir perkėlimo užsakymus. 

## <a name="default-order-settings-rules"></a>Numatytųjų užsakymo parametrų taisyklės
Galite nurodyti bendruosius numatytuosius užsakymo parametrus ir neribotą skaičių numatytųjų užsakymo parametrų taisyklių, kurios taikomos tik esant tam tikroms sąlygoms, pavyzdžiui, vieta arba konkreti produkto dimensija arba produkto dimensijų kombinacija. Negalima nurodyti tik sandėliui taikomų užsakymo parametrų.

### <a name="rank-in-default-order-settings"></a>Rangas numatytuose užsakymo parametruose

Numatytieji užsakymo parametrai turi rangus. Kuo aukštesnis rangas, tuo svarbesnė taisyklė, o tai reiškia, kad ji turės pirmenybę ir bus naudojama pirmiau negu kitos taisyklės su žemesniais rangais. Bendrųjų numatytųjų užsakymo parametrų rangas nulis, kurio negalima keisti. Gali būti tik viena taisyklė, kurios rangas 0. Taisyklės gali turėti tą patį rangą, jei skiriasi dimensijos, kurioms jos taikomos. Tai naudinga modeliuojant vietai pritaikytus užsakymo parametrus. Sukūrus naują numatytųjų užsakymo parametrų taisyklę, užsakymo vertės, stabdymo žymės ir t. t. perimamos iš taisyklės, kurios rangas nulis, bet jų gali būti nepaisoma.

### <a name="default-order-settings-for-released-products"></a>Išleistiems produktams taikomi numatytieji užsakymo parametrai

Atskiriems išleistiems produktams galite nurodyti bendruosius užsakymo parametrus arba konkrečiai vietai taikomus užsakymo parametrus. Bendrųjų užsakymo parametrų rangas visada nulis. Jeigu vienu metu nustatote naujus pardavimo, pirkimo ir atsargų užsakymo parametrus, puslapyje **Numatytieji užsakymo parametrai** rekomenduojame naudoti nuostatą **Informacijos rodinys**. Norėdami perjungti informacijos rodinį, pasirinkite **Parinktys** Veiksmų sritis &gt; **Puslapio parinktys** &gt; **Keisti rodinį** &gt; **Informacijos rodinys**.

### <a name="site-specific-order-settings"></a>Nuo vietos priklausomi užsakymo parametrai

Norėdami sukurti konkrečiai vietai pritaikytus užsakymo parametrus, spustelėkite **Naujas**. Dalies **Informacijos rodinys** lauke **Parametrai taikomi** &gt; **Vieta** įveskite vietą. **Tinklelio rodinys** stulpelyje **Vieta** įveskite vietą. Naujai taisyklei bus automatiškai suteikta nauja reitingo reikšmė, didesnė už nulį. Galite sukurti tiek vietai pritaikytų taisyklių, kiek reikia, ir visoms vietai pritaikytoms taisyklėms galite priskirti tą patį reitingą, kad nurodytumėte, jog jos vienodai svarbios. 

Jei esate dalyje **Informacijos rodinys**, negalite peržiūrėti prekei sukurtų taisyklių. Perjunkite mygtuką **Rodyti / slėpti sąrašą**, kad pamatytumėte peržiūros informaciją. Sukūrus bet kokio tipo užsakymo eilutę, kurioje nėra nurodyta vieta, „Finance and Operations“ ieško taisyklės, kurioje nenurodyta vieta. Tai gali padėti nustatyti numatytąją užsakymo eilutės vietą. Tada ši vieta naudojama ieškant vietai pritaikytos taisyklės, kurioje gali būti nustatytas numatytasis sandėlis. Šis sandėlis taikomas užsakymo eilutei.

### <a name="specific-order-settings-for-product-dimension"></a>Produkto dimensijai pritaikyti užsakymo parametrai

Galite nurodyti bet kurios aktyvios produkto dimensijos arba aktyvių produkto dimensijų kombinacijos užsakymo parametrų taisykles. Jei produkto dimensijos laukas neužpildytas, tada taisyklė taikoma visoms produkto dimensijos vertėms. 

Atkreipkite dėmesį į toliau pateikiamą produkto pavyzdį.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Produkto pavadinimas**                                    | Fotoelektrinis jutiklis                    |
| **Prekės Nr.**                                     | XW56                                    |
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

Šiame pavyzdyje paaiškinama, kodėl reikalingas reitingas. Jei pirkimo užsakymas sukuriamas konfigūracijai C1 ir peržiūrai R2, kai nenurodytas reitingas, šios dvi R2 ir C1 nurodytos taisyklės būtų nevienareikšmiškos. Norėdama išspręsti dviprasmiškumo problemą „Finance and Operations“ peržiūri taisykles pagal reitingą mažėjančia tvarka ir pritaiko pirmą taikytiną taisyklę. Dabartiniame pavyzdyje, kai pirkimo užsakymo eilutė sukuriama konfigūracijai C1 ir peržiūrai R2, vartotojas gaus įspėjantį pranešimą, kad prekė sulaikyta ir kad tai įvyko dėl peržiūros vertės. Jei konfigūracijos taisyklės reitingas aukštesnis negu peržiūros taisyklės reitingas, tada konfigūracijos C1 ir peržiūros R2 pirkimo užsakymo eilutė sukuriama sėkmingai ir vartotojas negaus pranešimo „prekė sulaikyta“. 

Atsižvelkite į toliau nurodytas numatytojo užsakymo parametro taisykles.

| Rangas | Svetainė | Konfigūravimas | Stilius | Numatytoji vieta | Numatytasis sandėlis | Pirkimas – nepaisyti numatytųjų saugojimo dimensijų | Pirkimo sandėlis |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Taip                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Sistema išanalizuoja taisyklių rinkinį du kartus, kad nustatytų vietą ir sandėlį. Sukūrus konfigūracijos C1, stiliaus R2 pirkimo užsakymo eilutę, vieta nustatoma pagal taisyklę, kurios reitingas 10. Tada sistema ieško 2 vietos taisyklės, kad nustatytų sandėlį. Randama 20 taisyklė ir, kadangi jos reitingas aukštesnis, pirkimo užsakymo eilutėje nurodomas sandėlis 22, o ne 21. 

Paprastai specialiųjų taisyklių ir svarbesnių negu kitos dimensijos dimensijų taisyklių reitingai būna aukštesni, o bendresnių taisyklių reitingai būna mažesni. 

Taisyklė, kurios reitingas nulis, naudojama kaip apsauginė sąlyga. Jei nėra kitų taisyklių, tada naudojami nulinės taisyklės numatytieji užsakymo parametrai. 

Kadangi labai svarbus reitingo skaičius, veiksmų srityje **Numatytieji užsakymo parametrai** pateikiamos funkcijos, kuriomis naudojantis galima perkelti taisyklę aukštyn arba žemyn ir iš naujo numeruoti taisykles, taip, kad jos būtų visada išdėstomos intervalais po 10. 

Išleistam produktui sukurtų taisyklių skaičius gali būti didelis. Norint geriau suprasti, ko nepaisoma vadovaujantis kiekviena taisykle ir kodėl kiekviena taisyklė reikalinga, rekomenduojame naudoti puslapyje **Numatytieji užsakymo parametrai** esantį **Tinklo rodinį**. Tinklelį galite įgalinti pasirinkdami **Parinktys** Veiksmų sritis &gt; **Puslapio parinktys** &gt; **Pakeisti rodinį** &gt; **Tinklo rodinys**. Tinklelyje rodomų stulpelių skaičius gali būti gana svarbus, ypač pardavimo ir atsargų skirtukuose. Norint apriboti tinklelyje rodomų stulpelių skaičių, stulpelių grupes galima paslėpti arba rodyti naudojant meniu **Numatytieji užsakymo parametrai** &gt; **Stulpelio rodinys** mygtukus.

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




