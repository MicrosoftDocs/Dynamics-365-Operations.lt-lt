---
title: Numatytieji dimensijų ir produkto variantų užsakymo parametrai
description: Numatytuose užsakymo parametruose nurodyta vieta ir sandėlis, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas.
author: johanhoffmann
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 106da56ed1de7d9e555cfdd63f19687d7e17599a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862575"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Numatytieji dimensijų ir produkto variantų užsakymų parametrai

[!include [banner](../includes/banner.md)]

Numatytuose „Dynamics 365 Supply Chain Management“ užsakymo parametruose nurodyta vieta ir sandėlis, iš kurių bus paimamos arba kuriuose bus laikomos prekės, minimalūs, maksimalūs, sudėtiniai ir standartiniai kiekiai, kurie bus naudojami prekiaujant arba valdant atsargas, vykdymo laikai, stabdymo vėliavėlė ir užsakymų vykdymo perspektyvos būdas. Numatytieji užsakymo parametrai naudojami kuriant pirkimo užsakymus, pardavimo užsakymus, perkėlimo užsakymus, atsargų žurnalus ir naudojant bendrąjį planavimą generuojant suplanuotus užsakymus. Numatytieji užsakymo parametrai gali būti pritaikyti prekei, vietai, produkto variantui arba produkto dimensijai.

Tam, kad nustatytumėte iš anksto nustatytus užsakymo nustatymus produktui, atlikite šiuos žingsnius.

1. Eikite į **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Patvirtinti produktai**.
1. Pasirinkite tinkamą produktą tinklelyje.
1. Veiksmų juostoje atlikite vieną iš šių žingsnių tam, kad atvertumėte **Nustatytųjų užsakymo nustatymų** puslapį pasirinktam produktui:

    - **Plano** skirtuke, **Užsakymo nustatymai** grupėje pasirinkite **Nustatytieji užsakymo nustatymai**.
    - **Valdyti atsargas** skirtuke, **Užsakymo nustatymai** grupėje pasirinkite **Nustatytieji užsakymo nustatymai**.

1. Konfigūruokite parametrus, kaip aprašyta likusioje šio straipsnio dalyje.

## <a name="default-order-settings"></a>Numatytieji užsakymo parametrai

Yra trijų tipų numatytieji užsakymo parametrai, skirti pirkimui, pardavimui ir atsargoms. Numatytieji pirkimo užsakymo parametrai naudojami kuriant:

- Pirkimo užsakymo eilutės
- Pirkimo sutarties eilutės
- Pasiūlymo patvirtinimo eilutės
- Pirkimo paraiškos eilutės
- Konsignacijos papildymo eilutės (palaikoma iš dalies, žr. pastabą)
- Suplanuoti pirkimo užsakymai

> [!NOTE]
> Naudojant konsignacijos papildymo užsakymo eilutes, vieninteliai taikomi puslapio **Numatytieji užsakymo parametrai** „FastTab” **Pirkimo užsakymas** parametrai yra laukas **Numatytoji teritorija**, laukas **Numatytasis sandėlis** ir žymės langelis **Sustabdyta**.

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

Jums sukūrus perlaidą, privalote nurodyti visą išleisto produkto linijoje sąvoką taip, kad „Supply Chain Management” galėtų bandyti atpažinti nustatytuosius užsakymo nustatymus. Viso išleisto produkto sąvoka, prekės numeris ir visos esančios produkto dimensijos, tokios kaip konfigūravimas, dydis, stilius, versija ir spalva yra nurodyti perlaidoje. Pavyzdžiui, jei rankiniu būdu sukuriate įsigijimo užsakymo eilutę išleistam produkto variantui, privalote nurodyti visas reikiamas produkto dimensijas prieš tai, kai vieta, sandėlis, kiekiai ir pagrindinis laikas pasirodys pagal nutylėjimą užsakymo eilutėje. 

Ne visi numatytieji užsakymo parametrai taikomi kuriant užsakymą arba žurnalo eilutes. Kiekiai ir vykdymo laikai bus rodomi tik pagal numatytuosius parametrus ir tik prireikus. Pavyzdžiui, skaičiuojant žurnalo eilutę, kai sukurta eilutė, pagal numatytuosius parametrus rodoma tik vieta ir sandėlis. Dėl šios priežasties, kuriant eilutę ar publikuojant žurnalą nėra iš anksto nustatyta jokių kiekių ar patikrinimų minimalioms ir maksimalioms vertėms. 

Kai sukuriamas užsakymas arba žurnalas, sistema visada bando rasti numatytąją vietą ir sandėlį. Pagal numatytuosius parametrus užsakymo parametruose vieta rodoma ne visada. Pavyzdžiui, kuriant pardavimo užsakymą arba pirkimo užsakymą užsakymo antraštėje nurodyta vieta automatiškai naudojama užsakymo eilutėse. Kuriant KS eilutę naudojama KS antraštėje nurodyta vieta. Po to, kai vieta nustatyta, ji bus naudojama surasti specifinius vietos užsakymo nustatymus, kurie vėliau bus naudojami kaip iš anksto nustatytieji sandėliui. 

Atsižvelgiant į puslapyje **Prekės padengimas** nurodytas prekės padengimo taisykles, numatytojo užsakymo tipo, pirkimo ir atsargų pristatymo laikų gali būti nepaisoma. Nors pagal numatytuosius užsakymo parametrus skirtumas tarp gamybos ir perkėlimo vykdymo laiko negalimas, prekės padengimo taisyklėse jis leidžiamas. Nepaisant to, elemento aprėpties nustatymas bus naudojamas tik pagrindiniam planavimui (MRP) kuriant suplanuotą produkciją ir persiuntimo užsakymus, ir nebus taikomi rankiniu būdu kuriant gamybos ir persiuntimo užsakymus. 

## <a name="default-order-settings-rules"></a>Numatytųjų užsakymo parametrų taisyklės

Galite nurodyti bendruosius numatytuosius užsakymo parametrus ir neribotą skaičių numatytųjų užsakymo parametrų taisyklių, kurios taikomos tik esant tam tikroms sąlygoms, pavyzdžiui, vieta arba konkreti produkto dimensija arba produkto dimensijų kombinacija. Galite nustatyti sandėlio specifinius užsakymo nustatymus.

### <a name="rank-in-default-order-settings"></a>Rangas numatytuose užsakymo parametruose

Numatytieji užsakymo parametrai turi rangus. Kuo aukštesnis rangas, tuo svarbesnė taisyklė, o tai reiškia, kad ji turės pirmenybę ir bus naudojama pirmiau negu kitos taisyklės su žemesniais rangais. Bendrųjų numatytųjų užsakymo parametrų rangas nulis, kurio negalima keisti. Gali būti tik viena taisyklė, kurios rangas 0. Taisyklės gali turėti tą patį rangą, jei skiriasi dimensijos, kurioms jos taikomos. Tai naudinga modeliuojant vietos specifinius užsakymo nustatymus. Sukūrus naują numatytųjų užsakymo parametrų taisyklę, užsakymo vertės, stabdymo žymės ir t. t. perimamos iš taisyklės, kurios rangas nulis, bet jų gali būti nepaisoma.

### <a name="default-order-settings-for-released-products"></a>Išleistiems produktams taikomi numatytieji užsakymo parametrai

Dėl atskirai leidžiamų produktų, galite nuspręsti bendrus užsakymo nustatymus ar vietos specifinius užsakymo nustatymus. Bendrųjų užsakymo parametrų rangas visada nulis. Jei nustatote naujus prekybos, įsigijimo ir inventoriaus užsakymo nustatymus vienu metu, rekomenduojame jums naudoti **Išsamios informacijos peržiūrą** **Nustatytieji užsakymo nustatymai** puslapyje. Tam, kad pakeistumėte išsamios informacijos peržiūrą, eikite į **Parinktys** &gt; **Puslapio parinktys** &gt; **Keisti peržiūrą** &gt; **Išsamios informacijos peržiūra**.

### <a name="site-specific-order-settings"></a>Nuo vietos priklausomi užsakymo parametrai

Tam, kad sukurtumėte vietos specifinius užsakymo nustatymus, pasirinkite **Naujas**. **Išsamios informacijos peržiūroje**, įveskite vietą **Vietos** laukelyje **Nustatymuose taikomuose** skyriui. **Tinklelio peržiūroje**, įveskite vietą **Vietos** stulpelyje. Nauja taisyklė automatiškai priskiriama naujo reitingo vertei, kuri yra didesnė nei 0 (nulis). Galite sukurti tiek vietos konkrečių taisyklių, kiek jums reikia. Tam, kad parodytumėte, jog jos yra vienodai svarbios, galite priskirti tą pačią reitingo vertę visoms su vieta susijusioms taisyklėms.

Jei esate dalyje **Informacijos rodinys**, negalite peržiūrėti prekei sukurtų taisyklių. Naudokite **Rodyti/slėpti sąrašą** mygtuką tam, kad peržiūrėtumėte informaciją. Sukūrus bet kokio tipo užsakymo eilutę, kurioje nėra nurodyta vieta, „Supply Chain Management“ ieško taisyklės, kurioje nenurodyta vieta. Tai padeda nustatyti iš anksto nustatytąją vietą užsakymo eilutėje. Ši vieta po to yra naudojama ieškoti nuo vietos priklausomų taisyklių, į kurias iš anksto nustatytas sandėlis gali būti nusiunčiamas. Šis sandėlis taikomas užsakymo eilutei.

### <a name="specific-order-settings-for-product-dimension"></a>Produkto dimensijai pritaikyti užsakymo parametrai

Galite nurodyti bet kurios aktyvios produkto dimensijos arba aktyvių produkto dimensijų kombinacijos užsakymo parametrų taisykles. Jei produkto dimensijos laukelis yra tuščias, tuomet taisyklė taikoma visoms produkto dimensijos vertėms. 

Atkreipkite dėmesį į toliau pateikiamą produkto pavyzdį.

| Produktas                                                | Reikšmė                                   |
|-----------------------------------------------------|-----------------------------------------|
| **Produkto pavadinimas**                                    | Fotoelektrinis jutiklis                    |
| **Prekės Nr.**                                     | XW56                                    |
| **Konfigūracija** (naudojama modeliuojant apšvietimo tipą) | C1 – matoma raudona šviesa, C2 – infraraudonųjų spindulių šviesa |
| **Versija** | V1, V2, V3                              |

Pavyzdžiui, tarkime, kad produktas yra ne pagamintas, o įsigytas. Taip pat tarkime, kad konfigūracija C1 naudojama dažniausiai, todėl jos vykdymo laikas trumpesnis. 

Norėdami modeliuoti šį scenarijų, sukurkite toliau nurodytus numatytuosius užsakymo parametrus.

| Rangas | Vieta | Konfigūravimas | Versija | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Taip                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kai prekybos užsakymo eilutė ar suplanuotas įsigijimo užsakymas yra sukuriamas XW56 prekei, konfigūravimui C1, nepriklausomai nuo versijos ar vietos, kurioje eilutė yra padėta, pagrindinis laikas bus nustatytas į 2. Manykime, kad visos versijos kartu su V3 yra sustabdytos.

Galite sukurti toliau nurodytus numatytuosius užsakymo parametrus.

| Rangas | Vieta | Konfigūravimas | Versija | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Taip                                  |                    | Taip                | Taip                               | Taip             |
| 20   |      |               | V1    | Taip                                  |                    | Taip                | Taip                               | Taip             |
| 10   |      | C1            |       | Taip                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Dvi senosios versijos sustabdymo taisyklės turi vienodą reitingą. Dėl to, jos yra vienodai svarbios. Kadangi abi šios taisyklės turi didesnį reitingą nei C1 konfigūravimo taisyklė, jos yra viršesnės nei C1 konfigūravimo taisyklė. 

Šiame pavyzdyje paaiškinama, kodėl reikalingas reitingas. Jei reitingas yra nenaudojamas, C1 konfigūravimui ir V2 versijai sukūrus įsigijimo užsakymą, abi taisyklės nustatytos V2 ir C1 bus dviprasmiškos. Norėdama išspręsti dviprasmiškumo problemą „Supply Chain Management“ peržiūri taisykles pagal reitingą mažėjančia tvarka ir pritaiko pirmą taikytiną taisyklę. Šiame pavyzdyje, kai prekybos užsakymo eilutė yra sukurta C1 konfigūravimui ir V2 versijai, vartotojas gaus perspėjantį pranešimą, kuris sako, kad prekė yra laikoma ir tai vyksta dėl versijos vertės. Jei konfigūravimo taisyklė turi didesnį reitingą nei versijos taisyklė, įsigijimo užsakymo eilutė bus sėkmingai sukurta C1 konfigūravimui ir V2 versijai bei vartotojas negaus „prekė laikoma“ pranešimo. 

Atsižvelkite į toliau nurodytas numatytojo užsakymo parametro taisykles.

| Rangas | Vieta | Konfigūravimas | Versija | Numatytoji teritorija | Numatytasis sandėlis | Pirkimas – nepaisyti numatytųjų saugojimo dimensijų | Pirkimo sandėlis |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Taip                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Sistema perkeičia taisyklių rinkinį du kartus tam, kad nustatytų vietą ir sandėlį. Kai įsigijimo užsakymo eilutė yra sukurta C1 konfigūravimui, V2 versijai, vieta nulemiama pagal taisyklę, turinčią 10 reitingą. Sistema tuomet ieško taisyklės vietai 2 tam, kad nustatytų sandėlį. Randama 20 taisyklė, nes ji turi didesnį reitingą, sandėlis įsigijimo užsakymo eilutėje bus 22, o ne 21.

Kaip bendros gairės, specialios taisyklės ir dimensijų taisyklės svarbesnės nei kitos dimensijos gauna aukštesnį lygmenį, o bendresnės taisyklės gauna žemesnįjį. 

Taisyklė, kurios reitingas nulis, naudojama kaip apsauginė sąlyga. Jei nėra kitų taisyklių, tada naudojami nulinės taisyklės numatytieji užsakymo parametrai. 

Kadangi lygmens numeris yra svarbus,**Nustatytieji užsakymo parametrai** veiksmų juostoje yra funkcijos leidžiančios judinti taisyklę aukštyn ar žemyn bei iš naujo sunumeruoti taisykles taip, kad jos visuomet didėtų po 10. 

Išleistam produktui sukurtų taisyklių skaičius gali būti didelis. Tam, kad geriau suprastumėte, ką kiekviena taisyklė viršija ir kam to reikia, rekomenduojame naudoti **Tinklelio peržiūrą** **Nustatytųjų užsakymo parametrų** puslapyje. Galite įjungti tinklelio peržiūrą eidami į **Parinktys** &gt; **Puslapio parinktys** &gt; **Keisti peržiūrą** &gt; **Tinklelio peržiūra**. Tinklelyje rodomų stulpelių skaičius gali būti gana svarbus, ypač pardavimo ir atsargų skirtukuose. Norint apriboti tinklelyje rodomų stulpelių skaičių, stulpelių grupes galima paslėpti arba rodyti naudojant meniu **Numatytieji užsakymo parametrai** &gt; **Stulpelio rodinys** mygtukus.

### <a name="specific-order-settings-for-released-product-variant"></a>Išleisto produkto variantui pritaikyti užsakymo parametrai

Jei taisyklės sistema nustatytiems užsakymo parametrams yra per didelė, tuomet esama parinkties, kuria galima nustatyti iš anksto nustatytuosius užsakymo parametrus kiekvienam produkto variantui. Toliau pateiktas pavyzdys rodo, kaip tai atrodo produktui ir prieš tai aprašytus atvejus.

| Rangas | Vieta | Konfigūravimas | Versija | Pirkimas – nepaisyti numatytųjų parametrų | Pirkimo vykdymo laikas | Pirkimas – sustabdytas | Pardavimas – nepaisyti numatytųjų parametrų | Pardavimas – sustabdytas |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Taip                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Taip                                  | 5                  | Taip                | Taip                               | Taip             |
| 10   |      | C2            | V1    | Taip                                  | 5                  | Taip                | Taip                               | Taip             |
| 10   |      | C1            | V3    | Taip                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Taip                                  | 2                  | Taip                | Taip                               | Taip             |
| 10   |      | C1            | V1    | Taip                                  | 2                  | Taip                | Taip                               | Taip             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Reitingas šiuo atveju nėra svarbus, todėl galite jį paslėpti. Šis sprendimas gali būti techninės priežiūros problemos priežastis. Nepaisant to, jums reikėtų apsvarstyti šio parametro naudojimą, jei galvojate apie produkto gyvavimo ciklo valdymo (PLM) sistemų integravimą.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Naudokite griežtą ar standartinį patvirtinimą iš anksto nustatytiems užsakymo kiekiams

Galite pasirinkti sistemos griežtumo lygį tvirtinant kiekius įvestus **Iš anksto nustatytiems užsakymo parametrams** produktui. Kai naudojate naują griežtą parinktį, **Standartinio užsakymo kiekis** visuomet turi būti keletas **Kelių** verčių prekybos užsakymuose, atsargose ir prekybos užsakymuose. Jei naudojate griežtą patvirtinimą, negalėsite įrašyti nustatytųjų užsakymo parametrų, kurie neatitinka šio reikalavimo (klaida bus rodoma pranešimo juostoje). 

Griežtas patvirtinimas taikomas **Standartiniam užsakymo kiekio** vertėms nurodytoms **Įsigijimo užsakymas**, **Inventorius** ir **Prekybos užsakymas** „FastTabs“ **Nustatytojo užsakymo parametro** puslapyje. Kiekvienas „FastTab“ turi savo **Daugelį** nustatymų, kurie yra naudojami patvirtinti **Standartinio užsakymo kiekio** vertę nurodytą tam „FastTab“.

### <a name="turn-the-strict-validation-option-on-or-off"></a>Įjungti arba išjungti griežtą tikrinimo parinktį

Norint naudoti griežtą tikrinimą *, jūsų sistemai turi* būti įjungta numatytojo užsakymo kiekių griežto tikrinimo funkcija. Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, [...](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*šią* funkciją galite įjungti arba išjungti nueidami į Funkcijų valdymą ir ieškodami numatytosios užsakymo kiekių funkcijos Griežtas tikrinimas.

### <a name="set-the-validation-option"></a>Nustatykite patvirtinimo parinktį

Patvirtinimo parinkties nustatymui:

1. Eikite į  **Produkto informacijos valdymas \> Nustatymai \> Produkto informacijos valdymo parametrai**.
1. **Bendra** skirtuke, nustatykite **Nustatytojo užsakymo kiekių tvirtinimas** į vieną iš šių verčių:
    - **Griežtas** - Pasirinkite šią parinktį siekiant užtikrinti, kad visos **Standartinio užsakymo kiekio** vertės bus dauginamos iš **Daugelio** verčių kiekvienam „FastTab“ (**Įsigijimo užsakymas**, **Inventorius** ir **Prekybos užsakymas**).
    - **Standartinis** - Pasirinkite šią parinktį tam, kad naudotumėte standartinį patvirtinimą (jis veikia tuo pačiu būdu, kai ši funkcija yra neįjungta).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]