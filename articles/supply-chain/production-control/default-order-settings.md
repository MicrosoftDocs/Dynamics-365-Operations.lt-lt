---
title: Numatytieji dimensijų ir produkto variantų užsakymo parametrai
description: Numatytuose užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas.
author: t-benebo
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 13df8eb7873495847d994922be1acd77e57f8f23
ms.sourcegitcommit: dfe5916d982eaa879e2afef7440c30b1d0f4380a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/29/2020
ms.locfileid: "3637761"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Numatytieji dimensijų ir produkto variantų užsakymų parametrai

[!include [banner](../includes/banner.md)]

Numatytuose „Dynamics 365 Supply Chain Management“ užsakymo parametruose nurodyta vieta ir sandėlys, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Numatytieji užsakymo parametrai naudojami kuriant pirkimo užsakymus, pardavimo užsakymus, perkėlimo užsakymus, atsargų žurnalus ir naudojant bendrąjį planavimą generuojant suplanuotus užsakymus. Numatytieji užsakymo parametrai gali būti pritaikyti prekei, vietai, produkto variantui arba produkto dimensijai.

Numatytuosius užsakymo parametrus galite nustatyti puslapyje **Numatytieji užsakymo parametrai**. Šio puslapio atidarymui eikite į **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Išleisti produktai** &gt; **Pasirinkti išleistą produktą** &gt; skyriuje **Planas**. Galite taip pat eiti į **Inventoriaus valdymas** &gt; **Užsakymo nustatymai** &gt; **Grąžinti užsakymo nustatymus į gamyklinius**.

## <a name="default-order-settings"></a>Numatytieji užsakymo parametrai

Yra trijų tipų numatytieji užsakymo parametrai, skirti pirkimui, pardavimui ir atsargoms. Numatytieji pirkimo užsakymo parametrai naudojami kuriant:

- Pirkimo užsakymo eilutės
- Pirkimo sutarties eilutės
- Pasiūlymo patvirtinimo eilutės
- Pirkimo paraiškos eilutės
- Konsignacijos papildymo eilutės
- Suplanuoti pirkimo užsakymai

Numatytieji pardavimo užsakymo parametrai naudojami kuriant:

- Pardavimo užsakymo eilutės
- Pardavimo sutarties eilutės
- Pardavimo pasiūlymo eilutės
- Grąžinimo užsakymo eilutės ir prekės pakeitimo eilutės
- Poreikio prognozės eilutės

Numatytieji pardavimo užsakymo parametrai taip pat taikomi kuriant:

- Projekto prekių reikalavimai
- Aptarnavimo užsakymo prekių poreikiai

Numatytieji atsargų užsakymo parametrai naudojami kuriant:

- Atsargų žurnalai
- Perkėlimo užsakymai
- Suplanuoti perkėlimo užsakymai

Numatytieji atsargų užsakymo parametrai taip pat taikomi kuriant:

- Sulaikymo užsakymai
- Kokybės užsakymai
- Gamybos užsakymai
- KS eilutės
- Suplanuoti gamybos užsakymai

## <a name="full-definition-of-a-released-product"></a>Visas išleisto produkto aprašas

Kurdami operaciją eilutėje turite nurodyti visą išleisto produkto apibrėžimą, kad „Supply Chain Management“ pabandytų nustatyti numatytuosius užsakymo parametrus. Visas išleisto produkto apibrėžimas reiškia, kad prekės numeris ir visos aktyvios produkto dimensijos, pavyzdžiui, konfigūracija, dydis, stilius ir spalva yra nurodytos operacijoje. Pavyzdžiui, jei rankiniu būdu kuriate išleisto produkto varianto pirkimo užsakymo eilutę, turite nurodyti visas reikiamas produkto dimensijas prieš tai, kai pagal numatytuosius parametrus užsakymo eilutėje bus rodoma vieta, sandėlis, kiekiai ir vykdymo laikas. 

Ne visi numatytieji užsakymo parametrai taikomi kuriant užsakymą arba žurnalo eilutes. Kiekiai ir vykdymo laikai bus rodomi tik pagal numatytuosius parametrus ir tik prireikus. Pavyzdžiui, skaičiuojant žurnalo eilutę, kai sukurta eilutė, pagal numatytuosius parametrus rodoma tik vieta ir sandėlis. Dėl šios priežasties, kuriant eilutę ar publikuojant žurnalą nėra iš anksto nustatyta jokių kiekių ar patikrinimų minimalioms ir maksimalioms vertėms. 

Kai sukuriamas užsakymas arba žurnalas, sistema visada bando rasti numatytąją vietą ir sandėlį. Pagal numatytuosius parametrus užsakymo parametruose vieta rodoma ne visada. Pavyzdžiui, kuriant pardavimo užsakymą arba pirkimo užsakymą užsakymo antraštėje nurodyta vieta automatiškai naudojama užsakymo eilutėse. Kuriant KS eilutę naudojama KS antraštėje nurodyta vieta. Po to, kai vieta nustatyta, ji bus naudojama surasti specifinius vietos užsakymo nustatymus, kurie vėliau bus naudojami kaip iš anksto nustatytieji sandėliui. 

Atsižvelgiant į puslapyje **Prekės padengimas** nurodytas prekės padengimo taisykles, numatytojo užsakymo tipo, pirkimo ir atsargų pristatymo laikų gali būti nepaisoma. Nors pagal numatytuosius užsakymo parametrus skirtumas tarp gamybos ir perkėlimo vykdymo laiko negalimas, prekės padengimo taisyklėse jis leidžiamas. Nepaisant to, elemento aprėpties nustatymas bus naudojamas tik pagrindiniam planavimui (MRP) kuriant suplanuotą produkciją ir persiuntimo užsakymus, ir nebus taikomi rankiniu būdu kuriant gamybos ir persiuntimo užsakymus. 

## <a name="default-order-settings-rules"></a>Numatytųjų užsakymo parametrų taisyklės

Galite nurodyti bendruosius numatytuosius užsakymo parametrus ir neribotą skaičių numatytųjų užsakymo parametrų taisyklių, kurios taikomos tik esant tam tikroms sąlygoms, pavyzdžiui, vieta arba konkreti produkto dimensija arba produkto dimensijų kombinacija. Galite nustatyti sandėlio specifinius užsakymo nustatymus.

### <a name="rank-in-default-order-settings"></a>Rangas numatytuose užsakymo parametruose

Numatytieji užsakymo parametrai turi rangus. Kuo aukštesnis rangas, tuo svarbesnė taisyklė, o tai reiškia, kad ji turės pirmenybę ir bus naudojama pirmiau negu kitos taisyklės su žemesniais rangais. Bendrųjų numatytųjų užsakymo parametrų rangas nulis, kurio negalima keisti. Gali būti tik viena taisyklė, kurios rangas 0. Taisyklės gali turėti tą patį rangą, jei skiriasi dimensijos, kurioms jos taikomos. Tai naudinga modeliuojant vietos specifinius užsakymo nustatymus. Sukūrus naują numatytųjų užsakymo parametrų taisyklę, užsakymo vertės, stabdymo žymės ir t. t. perimamos iš taisyklės, kurios rangas nulis, bet jų gali būti nepaisoma.

### <a name="default-order-settings-for-released-products"></a>Išleistiems produktams taikomi numatytieji užsakymo parametrai

Dėl atskirai leidžiamų produktų, galite nuspresti bendrus užsakymo nustatymus ar vietos specifinius užsakymo nustatymus. Bendrųjų užsakymo parametrų rangas visada nulis. Jei nustatote naujus prekybos, įsigijimo ir inventoriaus užsakymo nustatymus vienu metu, rekomenduojame jums naudoti **Išsamios informacijso peržiūrą** **Nustatytieji užsakymo nustatymai** puslapyje. Tam, kad pakeistumėte išsamios informacijos peržiūrą, eikite į**Parinktys** &gt; **Puslapio parinktys** &gt; **Keisti peržiūrą** &gt; **Išsamios informacijos peržiūra**.

### <a name="site-specific-order-settings"></a>Nuo vietos priklausomi užsakymo parametrai

Tam, kad sukurtumėte vietos specifinius užsakymo nustatymus, pasirinkite **Naujas**. Dalies **Informacijos rodinys** lauke **Parametrai taikomi** &gt; **Vieta** įveskite vietą. **Tinklelio rodinys** stulpelyje **Vieta** įveskite vietą. Naujai taisyklei bus automatiškai suteikta nauja reitingo reikšmė, didesnė už nulį. Galite sukurti tiek nuo vietos priklausomų specialių taisyklių, kiek jums reikia ir tuomet priskirti nuo vietos priklausomas specialias taisykles vienam lygmeniui tam, kad sumodeliuotumėte vienodą jų svarbą. 

Jei esate dalyje **Informacijos rodinys**, negalite peržiūrėti prekei sukurtų taisyklių. Naudokite **Rodyti/slėpti sąrašą** mygtuką tam, kad peržiūrėtumėte informaciją. Sukūrus bet kokio tipo užsakymo eilutę, kurioje nėra nurodyta vieta, „Supply Chain Management“ ieško taisyklės, kurioje nenurodyta vieta. Tai padeda nustatyti iš anksto nustatytąją vietą užsakymo eilutėje. Ši vieta po to yra naudojama ieškoti nuo vietos priklausomų taisyklių, į kurias iš anksto nustatytas sandėlis gali būti nusiunčiamas. Šis sandėlis taikomas užsakymo eilutei.

### <a name="specific-order-settings-for-product-dimension"></a>Produkto dimensijai pritaikyti užsakymo parametrai

Galite nurodyti bet kurios aktyvios produkto dimensijos arba aktyvių produkto dimensijų kombinacijos užsakymo parametrų taisykles. Jei produkto dimensijos laukelis yra tuščias, tuomet taisyklė taikoma visoms produkto dimensijos vertėms. 

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

Šiame pavyzdyje paaiškinama, kodėl reikalingas reitingas. Jei pirkimo užsakymas sukuriamas konfigūracijai C1 ir peržiūrai R2, kai nenurodytas reitingas, šios dvi R2 ir C1 nurodytos taisyklės būtų nevienareikšmiškos. Norėdama išspręsti dviprasmiškumo problemą „Supply Chain Management“ peržiūri taisykles pagal reitingą mažėjančia tvarka ir pritaiko pirmą taikytiną taisyklę. Dabartiniame pavyzdyje, kai pirkimo užsakymo eilutė sukuriama konfigūracijai C1 ir peržiūrai R2, vartotojas gaus įspėjantį pranešimą, kad prekė sulaikyta ir kad tai įvyko dėl peržiūros vertės. Jei konfigūravimo taisyklė turėjo aukštesnį lygmenį nei patikrinimo taisyklė, tuomet įsigijimo užsakymo eilutės sukūrimas C1 konfigūravimui ir R2 patikrinimui bus įvykęs ir 'elementas laikomas' pranešimas naudotojui nebus rodomas. 

Atsižvelkite į toliau nurodytas numatytojo užsakymo parametro taisykles.

| Rangas | Svetainė | Konfigūravimas | Stilius | Numatytoji vieta | Numatytasis sandėlis | Pirkimas – nepaisyti numatytųjų saugojimo dimensijų | Pirkimo sandėlis |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Taip                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Sistema perkeičia taisyklių rinkinį du kartus tam, kad nustatytų vietą ir sandėlį. Sukūrus konfigūracijos C1, stiliaus R2 pirkimo užsakymo eilutę, vieta nustatoma pagal taisyklę, kurios reitingas 10. Tuomet sistema ieško taisyklės vietai 2 tam, kad nustatytų sandėlį. Randama 20 taisyklė ir, kadangi jos reitingas aukštesnis, pirkimo užsakymo eilutėje nurodomas sandėlis 22, o ne 21.

Kaip bendros gairės, specialios taisyklės ir dimensijų taisyklės svarbesnės nei kitos dimensijos gauna aukštesnį lygmenį, o bendresnės taisyklės gauna žemesnįjį. 

Taisyklė, kurios reitingas nulis, naudojama kaip apsauginė sąlyga. Jei nėra kitų taisyklių, tada naudojami nulinės taisyklės numatytieji užsakymo parametrai. 

Kadangi lygmens numeris yra svarbus,**Nustatytieji užsakymo paramtrai** veiksmų juostoje yra funkcijos leidžiančios judinti taisyklę aukštyn ar žemyn bei iš naujo sunumeruoti taisykles taip, kad jos visuomet didėtų po 10. 

Išleistam produktui sukurtų taisyklių skaičius gali būti didelis. Tam, kad geriau suprastumėte, ką kiekviena taisyklė viršija ir kam to reikia, rekomenduojame naudoti **Tinklelio peržiūrą** **Nustatytųjų užsakymo parametrų** puslapyje. Galite įjungti tinklelio peržiūrą eidami į **Parinktys** &gt; **Puslapio parinktys** &gt; **Keisti peržiūrą** &gt; **Tinklelio peržiūra**. Tinklelyje rodomų stulpelių skaičius gali būti gana svarbus, ypač pardavimo ir atsargų skirtukuose. Norint apriboti tinklelyje rodomų stulpelių skaičių, stulpelių grupes galima paslėpti arba rodyti naudojant meniu **Numatytieji užsakymo parametrai** &gt; **Stulpelio rodinys** mygtukus.

### <a name="specific-order-settings-for-released-product-variant"></a>Išleisto produkto variantui pritaikyti užsakymo parametrai

Jei taisyklės sistema nustatytiems užsakymo parametrams yra per didelė, tuomet esama parinkties, kuria galima nustatyti iš anksto nustatytuosius užsakymo parametrus kiekvienam produkto variantui. Toliau pateiktas pavyzdys rodo, kaip tai atrodo produktui ir prieš tai aprašytus atvejus.

| Rangas | Svetainė | Konfigūravimas | Stilius | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Taip                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Taip                                  | 5                  | Taip                | Taip                               | Taip             |
| 10   |      | C2            | R1    | Taip                                  | 5                  | Taip                | Taip                               | Taip             |
| 10   |      | C1            | R3    | Taip                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Taip                                  | 2                  | Taip                | Taip                               | Taip             |
| 10   |      | C1            | R1    | Taip                                  | 2                  | Taip                | Taip                               | Taip             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Reitingas šiuo atveju nėra svarbus, todėl galite jį paslėpti. Šis sprendimas gali būti techninės priežiūros problemos priežastis. Nepaisant to, jums reiketų apsvarstyti šio parametro naudojimą, jei galvojate apie produkto gyvavimo ciklos valdymo (PLM) sistemų integravimą.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Naudokite griežtą ar standartinį patvirtinimą iš anksto nustatytiems užsakymo kiekiams

Galite pasirinkti sistemos griežtumo lygį tvirtinant kiekius įvestus **Iš anksto nustatytiems užsakymo parametrams** produktui. Kai naudojate naują griežtą parinktį, **Standartinio užsakymo kiekis** visuomet turi būti keletos **Kelių** verčių prekybos užsakymuose, atsargose ir prekybos užsakymuose. Jei naudojate griežtą patvirtinimą, negalėsite įrašyti nustatytųjų užsakymo parametrų, kurie neatitinka šio reikalavimo (klaida bus rodoma pranešimo juostoje). 

Griežtas patvirtinimas taikomas **Standartiniam užsakymo kiekio** vertėms nurodytoms **Įsigijimo užsakyma**, **Inventorius** ir **Prekybos užsakym** „FastTabs“ **Nustatytojo užsakymo parametro** puslapyje. Kiekvienas „FastTab“ turi savo **Daugelį** nustatymų, kurie yra naudojami patvirtinti **Standartinio užsakymo kiekio** vertę nurodytą tam „FastTab“.

### <a name="enable-the-strict-validation-option"></a>Įjungti griežtą patvirtinimo parinktį

Prieš tai, kai galite naudoti griežtą patvirtinimo parinktį, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijas valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia. Čia funkcija yra nurodyta kaip:

- **Modulis** - *Produkto informacijos valdymas*
- **Funkcijos pavadinimas** - *Griežtas patvirtinimas dėl nustatytųjų užsakymo kiekio*

### <a name="set-the-validation-option"></a>Nustatykite patvirtinimo parinktį

Patvirtinimo parinkties nustatymui:

1. Eikite į  **Produkto informacijos valdymas \> Nustatymai \> Produkto informacijos valdymo parametrai**.
1. **Bendra** skirtuke, nustatykite**Nustatytojo užsakymo kiekių tvirtinimas** į vieną iš šių verčių:
    - **Griežtas** - Pasirinkite šią parinktį siekiant užtikrinti, kad visos **Standartinio užsakymo kiekio** vertės bus dauginamos iš **Daugelio** verčių kiekvienam „FastTab“ (**Įsigijimo užsakymas**, **Inventorius** ir **Prekybos užsakymas**).
    - **Standartinis** - Pasirinkite šią parinktį tam, kad naudotumėte standartinį patvirtinimą (jis veikia tuo pačiu būdu, kai ši funkcija yra neįjungta).
