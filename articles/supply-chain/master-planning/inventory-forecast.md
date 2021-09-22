---
title: Atsargų prognozės
description: Šioje temoje aprašomos tiekimo ir poreikio prognozės funkcijos, kurias galima naudoti kuriant atsargų prognozes programoje „Microsoft Dynamics 365 Supply Chain Management“.
author: crytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b9c82f28dcc7ebd223b2483ca257ba934024d755
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475089"
---
# <a name="inventory-forecasts"></a>Atsargų prognozės

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip peržiūrėti ir kurti atsargų prognozes. Galite kurti ir peržiūrėti prekių, prekių grupių, prekių paskirstymo raktų, klientų sąskaitų, klientų grupių, tiekėjų sąskaitų ir tiekėjų grupių tiekimo ir poreikio prognozės eilutes.

Kiekvienoje prognozės eilutėje galite pasirinkti naudojamą prognozės modelį. Tada galite nurodyti prekę arba prekių grupę bei kiekį arba operacijos sumą. Taip pat galite nustatyti prognozės kiekio paskirstymo tvarkaraštį.

Tiekimo ir poreikio prognozės eilutės sukuria to paties prekės ir modelio derinio atsargų prognozę. Ši atsargų prognozė pateikia balansą tarp tiekimo ir poreikio, kurie buvo įvesti tai pačiai prekei. Jos negalima redaguoti. Atsargų prognozė padeda atsargų valdymo komandai peržiūrėti numatomus turimų prekės atsargų pokyčius ateinant prognozuojamu laikotarpiu.

Įvedus Jūsų poreikį ir (ar) tiekimą, galite vykdyti prognozę ir planuoti skaičiavimo bendrus reikalavimus medžiagoms ir pajėgumams bei kurti suplanuotus užsakymus.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Prognozės eilučių rodymas ir įvesdami prognozės eilutes rankiniu būdu

Naudokite šią procedūrą, norėdami rankiniu būdu kurti produktų prognozės eilutes.

Prognozės eilutes galima kurti ir kitais būdais:

- [Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md).
- [Poreikio prognozių praeities duomenų importavimas](import-historical-data.md).
- [Kurti prognozę su „Microsoft Azure Machine Learning“ tinklo paslaugomis](demand-forecasting-setup.md).
- [Importuokite poreikio arba tiekimo prognozės eilutes naudodami duomenų valdymo sistemą (ForecastDemandForecastEntryStaging ir ForecastSupplyForecastEntryStaging) duomenų objektus](../../dev-itpro/data-entities/data-entities-data-packages.md).

Kaip rodo lentelė 1 veiksme, yra skirtingi būdai pasiekti naudojamus puslapius.

1. Priklausomai nuo objekto, kuriam norite sukurti prognozę, tipo ir prognozės, kurią norite sukurti, tipo, atidaryti tiekimo, poreikio arba atsargų prognozės puslapį, kaip aprašyta šioje lentelėje.

    | Objektas | Instrukcijos |
    |---|---|
    | Patvirtinti produktai | <ol><li>Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</li><li>Pasirinkite produktą, jei norite kurti prognozę.</li><li>Veiksmų juostoje **Plano** skirtuke, grupėje **Prognozė** rinktiės **Poreikio prognozę**, **Tiekimo prognozę**, ar **Atsargų prognozę**, priklausomai nuo prognozės tipo, su kuriuo norite dirbti.</li></ol> |
    | Patvirtinto produkto variantai | <ol><li>Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktų variantai**.</li><li>Pasirinkite variantą, jei norite kurti prognozę.</li><li>Veiksmų juostoje **Plano** skirtuke, grupėje **Prognozė** rinktiės **Poreikio prognozę**, **Tiekimo prognozę**, ar **Atsargų prognozę**, priklausomai nuo prognozės tipo, su kuriuo norite dirbti.</li></ol> |
    | Prekių grupės | <ol><li>Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių grupės**.</li><li>Pasirinkite prekės grupę, jei norite kurti prognozę.</li><li>Veiksmų juostoje rinkitės **Prognozė \> Poreikis**, **Prognozė \> Tiekimas**, ar **Prognozė \> Atsargų prognozė**, priklausomai nuo prognozės tipo, su kuriuo norite dirbti.</li></ol> |
    | Prekių paskirstymo raktai | <ol><li>Eikite į **Atsargų valdymas \> Nustatymas \> Prognozė**.</li><li>Pasirinkite prekės paskyrimo raktą, jei norite kurti prognozę.</li><li>Veiksmų srityje spustelėkite **Prašyti prognozės**.</li></ol> |
    | Klientai | <ol><li>Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Klientai**.</li><li>Pasirinkite klientą, jei norite kurti prognozę.</li><li>Veiksmų srityje spustelėkite **Nustatyti poreikio prognozę**.</li></ol> |
    | Klientų grupės | <ol><li>Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Klientų grupės**.</li><li>Pasirinkite klientų grupę, jei norite kurti prognozę.</li><li>Veiksmų srityje spustelėkite **Nustatyti poreikio prognozę**.</li></ol> |
    | Tiekėjai | <ol><li>Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Tiekėjai**.</li><li>Pasirinkite tiekėją, jei norite kurti prognozę.</li><li>Veiksmų srityje **Įrašas** pasirinkite atverti **Tiekimo prognozė** puslapį.</li></ol> |
    | Tiekėjų grupės | <ol><li>Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Tiekėjų grupės**.</li><li>Pasirinkite tiekėjų grupę, jei norite kurti prognozę.</li><li>Veiksmų srityje **Įrašas** pasirinkite atverti **Tiekimo prognozė** puslapį.</li></ol> | 
    | Visos eilutės | <ul><li>Eikite į **Bendrasisi planavimas \> prognozės \> poreikio prognozės eilutes** ar **Bendrasisi planavimas \> Prognozės \> Tiekimo prognozės eilutės**, priklausomai nuo prognozės tipo, su kuriuo norite dirbti.</li></ul> |

    Atsižvelgiant į pasirinkimą, rodomas puslapis **Tiekimo prognozė** ar **Poreikio prognozė**. Jame rodomos visos esamos įrašo, kurį pasirinkote prieš atidarę puslapį, prognozės eilutės.

1. Veiksmų juostoje rinkitės **Naujas** norėdami įtraukti prognozės eilutę į tinklelį viršutinėje puslapio dalyje.
1. Naujoje eilutėje lauke **Modelis** pasirinkite naudotiį prognozės modelį. Tada įveskite kitą reikiamą informaciją, pvz., prekę, prekių grupę, kliento ar tiekėjo kodą arba grupę, prekių kiekį arba bendrą operacijos sumą. Išsamios informacijos apie laukus, kurie galimi **tiekimo prognozės** ir **poreikio prognozės** puslapiuose, ieškokite vėlesniuose šios temos skyriuose.
1. Norėdami paskirstyti prognozę per laikotarpį, įrankių juostoje skirtuke **Peržiūra** ir rinkitės **Paskirstyte prognozę**.
1. Tinklelyje **Paskirstymas** peržiūrėkite laiko perspektyvą ir laiko intervalus, naudojamus prognozuojamiems kiekiams paskirstyti.

## <a name="supply-forecast-lines"></a>Tiekimo prognozės eilutės

Tiekimo prognozė leidžia sukurti prekių, kurias reikia nupirkti, planą. Jis nurodo įsigijimą ir užsakymų klerkus, ką jie turi užsakyti.

Galite įvesti tiekimo prognozę pagal prekę, prekių grupę, prekių paskirstymo raktą, tiekėją ir tiekėjų grupę. Informacijos apie visus būdus, kaip atidaryti **tiekimo prognozės** puslapį, žr. anksčiau šioje temoje skyriuje [Peržiūrėti ir rankiniu būdu įvesti](#manual-entry) prognozės eilutes.

Viršutinė **Tiekimo prognozės** puslapio dalis pateikia tiekimo prognozės eilučių tinklelį ir skirtukų rinkinį, kurį galite naudoti norėdami peržiūrėti ir nustatyti daugiau informacijos apie pasirinktą prognozės eilutę. Apatinėje puslapio dalyje pateikiamas **paskirstymo** tinklelis.

Toliau esančiuose poskyryje aprašomi visi kiekviename skirtuke galimi laukai ir visos komandos, galimos puslapio veiksmų srityje bei skirtuke Apžvalga esančioje **įrankių** juostoje.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Veiksmų srities komandos tiekimo prognozės puslapyje

Toliau pateiktoje lentelėje aprašomos komandos, esančios puslapio **Tiekimo prognozė** veiksmų srityje.

| Komanda | Aprašas |
|---|---|
| Įrašyti | Įrašykite dabartinius parametrus. |
| Redagavimas | Įgalinti nustatymus puslapyje, kad būtų galima redaguoti. |
| Nauja | Įtraukti prognozės eilutę į viršutinį tinklelį. |
| Panaikinti | Pašalinti pasirinktą prognozės eilutę iš viršutinio tinklelio. |
| Likučių prognozė | Peržiūrėti prognozės balansus, kurie buvo apskaičiuoti pasirinktų finansinių metų eilutės modelio ID. Balansai padalinti pagal laikotarpį (mėnesį). |
| Grynųjų pinigų srautų prognozės | Peržiūrėkite DK paskirstytas prognozės operacijas. Daugiau informacijos žr. [Pinigų srauto planavimas](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Atsargos \> Rodyti dimensijas | Pasirinkti atsargų dimensijas, kurios turėtų būti rodomos tinklelyje, **skirtuke** Peržiūra. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Tiekimo prognozės puslapio skirtuko Apžvalga įrankių juostos komandos

Toliau pateiktoje lentelėje aprašomos komandos, esančios įrankių juostoje **Peržiūra** puslapio skirtuke **Tiekimo prognozė**.

| Komanda | Aprašas |
|---|---|
| Paskirstyti prognozę | Jei naudojate paskirstymo metodą, sugeneruokite atskiras prognozės operacijos grafiko eilutes. Eilutės kiekis paskirstomas pagal datą (pagal pasirinktus laiko intervalus), viso laiko intervalo kiekį ir sumą. (Žr. [Skirti prognozę](#allocate-forecast) Atsargų atnaujinimo prognozės operacijos.) |
| Masinis naujinimas | Atidarykite **prognozės operacijų redagavimo** puslapį. (Žr. [Vėliau šioje temoje skyriuje](#bulk-update) Masinio atnaujinimo prognozės operacijos.) |
| Atsargų prognozė | Atidaryti atsargų **prognozės puslapio,** kuris filtruojamas pagal pasirinktą prekės / modelio derinį, rodinį. (Žr. [Vėliau šioje temoje skyriuje](#inventory-forecast) Atsargų atnaujinimo prognozės operacijos.) |
| Kurti prekės poreikį | Atidaryti dialogo langą, kuriame galite kurti prekių poreikius ir pardavimo užsakymą arba prekių žurnalo eilutes su projektu susijusioms prognozės operacijoms. Nors ši komanda galima ir tiekimo prognozės eilutėms, ir poreikio prognozės eilutėms, jos negalima naudoti tiekimo **prognozės puslapyje**. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Apžvalgos skirtukas tiekimo prognozės puslapyje.

Toliau pateikiamoje lentelėje aprašomi laukai **tiekimo** prognozės **puslapio skirtuke** Apžvalga.

| Laukas | Aprašas |
|---|---|
| **Modelis** | Prognozės modelis, su kuriuo susieta operacija. |
| **Data** | Operacijos pradžios data. |
| **Tiekėjo kodas** | Su operacija susijusi tiekėjo perlaida. |
| **Tiekėjų grupė** | Su operacija susijusi tiekėjo grupe. |
| **Prekės Nr.** | Prekės identifikatorius. |
| **Prekių grupė** | Prekės grupė, su kuria susijusi operacija. |
| **Prekių paskirstymo raktas** | Su prognoze susijęs prekių paskirstymo raktas. |
| **Svėrimo kiekis** | Prognozuojamas kiekis nurodytu esamo svorio vienetu. |
| **Svėrimo vnt.** | Pasirinkite pagavimo vienetą, kuriuo bus perkama prekė. Vertė automatiškai nuskaitoma iš prekės nustatymo. |
| **Kiekis** | Prognozuojamas kiekis nurodytu esamo pirkimo vienetu. |
| **Vienetas** | Pasirinkite vienetą, kuriuo bus perkama prekė. Vertė automatiškai nuskaitoma iš prekės nustatymo. Tačiau jį galima modifikuoti, jei nustatytas vienetų konvertavimas. |
| **Suma** | Bendra suma, atėmųus nuolaidų, dėl kurių prognozės operacija daro įtaką prognozei. |
| **Valiuta** | Operacijos metu naudotas prognozės kodas. Numatytoji valiuta automatiškai įveda,a bet galite pasirinkti kitą valiutą. |
| (Kitos dimensijos) | Papildomos dimensijos tinklelyje gali būti rodomos kaip stulpeliai. Norėdami pasirinkti papildomus rodomus matmenis, rinkitės **Rodyti matmenis** veiksmų srityje. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Apžvalgos bendras skirtukas tiekimo prognozės puslapyje.

Skirtuke **Bendra** rodoma daugiau informacijos apie eilutę, kurią šiuo metu pasirinkote **skirtuke** Peržiūra. Kai kuri informacija kartojama skirtuke **Peržiūra**. Toliau pateikiamoje lentelėje aprašomi unikalūs skirtuko **Bendra** laukai.

| Laukas | Aprašas |
|---|---|
| Ataskaita | Nustatykite šią parinktį į *Taip* tam, kad operacija būtų įtraukta į ataskaitas. |
| Komentarai | Įveskite visus komentarus apie prognozės perlaidą. |
| Aktyvi | Pažymėti šį langelį, kad operacija būtų įtraukta į biudžeto ataskaitas. |
| Įtraukti į grynųjų pinigų srautų prognozes | Pažymėkite šį langelį, kad prognozės operacijos būtų paskirtos į didžiąją knygą. Negalima modifikuoti ataskaitų operacijų šio žymės langelio nustatymo. |
| PVM grupė | Mokesčių grupė, naudojama nurodant prognozės operacijos mokesčius. |
| Prekės PVM grupė | Prekės mokesčių grupė, naudojama nurodant prognozės operacijos mokesčius. |
| Metodas | <p>Pasirinkite metodą, kuris naudojamas prognozės operacijai paskirstyti:</p><ul><li>**Joks** – paskirstymas nevykdomas.</li><li>**Laikotarpis** – prognozeikite tą patį kiekį kiekvienam laikotarpiui. Jei pasirinksite šią vertę, lauke Už nurodykite **kiekį**, o lauke Vienetas – **laiko** vienetą.</li><li>**Raktas** – prognozės kiekis paskirstomas pagal laikotarpių paskirstymo raktą, kurį nurodote lauke **Laikotarpio raktas**. Galite naudoti šį metodą, kai norite apgalvoti sezonų kaitą.</li></ol>|
| Per | <p>Įvesti intervalų, kuriais prognozė nusitęsia į ateitį, skaičių. Šis laukas galimas, tik jei lauke pasirinkote *Laikotarpis* laukelyje **Metodas**.</p><p>Pavyzdžiui, jei pasirinkote *Laikotarpis* laukelyje **Metodas** įveskite *1* lauke **pagal** ir rinkitės *Mėnesiai* lauke **Vienetas**. Lauke **Pabaiga** nurodote pabaigos datą, kuri prasitęsia metus į ateitį. Jei viena prognozės eilutė sukurta kiekvienam ateinančių metų mėnesiui, pagal prekę ir kiekį, kuri nurodyti antraštės eilutėje.</p> |
| Vienetas | Pasirinkite laiko intervalo vienetą: *dienos*, *mėnesiai* arba *metai*. Paskyrimas tuomet atitinka dienų skaičių ar metų skaičių, kurį nurodėte **Pagal** lauke.|
| Laikotarpio raktas | Nurodyti rakto paskyrimo laikotarpį. |
| Pabaigoje | Rodo pabaigos datą jums naudojant **Pagal** ir **Vieneto** laukus. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Prekės bendras skirtukas tiekimo prognozės puslapyje.

Skirtukas **Prekė** rodo daugiau informacijos apie prekę ir eilutę, kuri šiuo metu pasirinkta **Peržiūros** skirtuke.

Tinklelis, esantis skirtuko **Prekė** viršuje, pakartoja prekės informaciją, kuri taip pat rodoma **skirtuke** Peržiūra. Be to, joje yra laukas Vieneto kaina, kuriame rodoma **lauke** Vienetas nurodyto vienetų skaičiaus pirkimo **kaina**. Prekės kaina automatiškai gaunama iš prekės nustatymų, bet juos galite keisti.

Laukuose, esančiuose po tinkleliu, pateikiama daugiau prekės informacijos. Kai kuri informacija kartojama skirtuke **Peržiūra**. Toliau pateikiamoje lentelėje aprašomi laukeliai, kurie yra unikalūs **skirtuke** Prekė.

| Laukas | Aprašas |
|---|---|
| Kainos vienetas | Pardavimo vienetų, kuriems taikoma pirkimo kaina, skaičius. Vertė automatiškai gaunama iš prekių lentelės, tačiau jį galite modifikuoti. |
| Pirkimo išlaidos | Pirkimo kainos fiksuoti mokesčiai. Mokesčiai nepriklauso nuo kiekio. |
| Nuolaida procentais | Nuolaida kaip procentinė dalis. |
| Nuolaidos suma | Nuolaida, išreikšta kaip pardavimo vieneto suma. |
| Bendra suma | Suma, kai netaikoma jokia nuolaida. |
| Kiekis | Perlaidos kiekis, išreikštas prekės atsargų vienetais. |
| SubKS | Konkrečios KS komplektavimo specifikacijos (KS) numeris. |
| Maršrutas | Konkretaus maršruto numeris. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Finansinių dimensijų skirtukas tiekimo prognozės puslapyje.

Skirtuke **Finansinės dimensijos** rodomos visos eilutės, kuri šiuo metu pasirinkta skirtuke Peržiūra, finansinių **dimensijų** vertės.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Atsargų dimensijų skirtukas tiekimo prognozės puslapyje.

Skirtuke **Atsargų dimensijos** rodomos visos atsargų dimensijos eilutės, kuri šiuo metu pasirinkta skirtuke Peržiūra, finansinių **dimensijų** vertės.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Paskyrtimo tinklelis tiekimo prognozės puslapyje.

Jei naudojate prekių paskirstymo raktą arba jei įvedėte vieno ar kelių būsimų laikotarpių prekės prognozę, galite paskirstyti prognozę skirtuke **Peržiūra pasirinkdami** Paskirstyti prognozę. Kiekis **paskirstomas** taip, kaip nurodyta paskirstymo **tinklelio** eilutėse.

## <a name="demand-forecast-lines"></a>Poreikio prognozės eilutės

Poreikio prognozė leidžia įvesti arba sugeneruoti kliento poreikį. Tai padeda pardavimo ir rinkodaros tarnautojams informuoti bendrojo planavimo klerkas apie numatomą poreikį ateinant prognozės laikotarpiui.

Galite įvesti poreikio prognozę pagal prekę, prekių grupę, prekių paskirstymo raktą, klientą ir klientų grupę. Informacijos apie visus būdus, kaip atidaryti **poreikio prognozės** puslapį, žr. anksčiau šioje temoje skyriuje [Peržiūrėti ir rankiniu būdu įvesti](#manual-entry) prognozės eilutes.

Viršutinė **Poreikio prognozės** puslapio dalis pateikia poreikio prognozės eilučių tinklelį ir skirtukų rinkinį, kurį galite naudoti norėdami peržiūrėti ir nustatyti daugiau informacijos apie pasirinktą prognozės eilutę. Apatinėje puslapio dalyje pateikiamas **paskirstymo** tinklelis.

Toliau esančiuose poskyryje aprašomi visi kiekviename skirtuke galimi laukai ir visos komandos, galimos puslapio veiksmų srityje bei skirtuke Apžvalga esančioje **įrankių** juostoje.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Veiksmų srities komandos poreikio prognozės puslapyje

Toliau pateiktoje lentelėje aprašomos komandos, esančios puslapio **Poreikio prognozė** veiksmų srityje.

| Komanda | Aprašas |
|---|---|
| Įrašyti | Įrašykite dabartinius parametrus. |
| Redagavimas | Įgalinti nustatymus puslapyje, kad būtų galima redaguoti. |
| Nauja | Įtraukti prognozės eilutę į viršutinį tinklelį. |
| Panaikinti | Pašalinti pasirinktą prognozės eilutę iš viršutinio tinklelio. |
| Likučių prognozė | Peržiūrėti prognozės balansus, kurie buvo apskaičiuoti pasirinktų finansinių metų eilutės modelio ID. Balansai padalinti pagal laikotarpį (mėnesį). |
| Pinigų srautų prognozė | Peržiūrėkite DK privalomai paskirstytas prognozės operacijas. Daugiau informacijos žr. [Pinigų srauto planavimas](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Rodyti dimensijas | Pasirinkti atsargų dimensijas, kurios turėtų būti rodomos tinklelyje, **skirtuke** Peržiūra. |
| DK peržiūra | Peržiūrėti pasirinktos operacijos DK įrašus. |
| Perkelti pasiūlymo eilutes | Perkelti pasiūlymo eilutes į pasirinktą projektą. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Poreikio prognozės puslapio skirtuko Apžvalga įrankių juostos komandos

Toliau pateiktoje lentelėje aprašomos komandos, esančios įrankių juostoje **Peržiūra** puslapio skirtuke **Poreikio prognozė**.

| Komanda | Aprašas |
|---|---|
| Paskirstyti prognozę | Jei naudojate paskirstymo metodą, sugeneruokite atskiras prognozės operacijos grafiko eilutes. Eilutės kiekis paskirstomas pagal datą (pagal pasirinktus laiko intervalus), viso laiko intervalo kiekį ir sumą. (Žr. [Skirti prognozę](#allocate-forecast) Atsargų atnaujinimo prognozės operacijos.)|
| Masinis naujinimas | Atidarykite **prognozės operacijų redagavimo** puslapį. (Žr. [Vėliau šioje temoje skyriuje](#bulk-update) Masinio atnaujinimo prognozės operacijos.) |
| Atsargų prognozė | Atidaryti atsargų **prognozės puslapio,** kuris filtruojamas pagal pasirinktą prekės / modelio derinį, rodinį. (Žr. [Vėliau šioje temoje skyriuje](#inventory-forecast) Atsargų atnaujinimo prognozės operacijos.) |
| Kurti prekės poreikį | Atidaryti dialogo langą, kuriame galite kurti prekių poreikius ir pardavimo užsakymą arba prekių žurnalo eilutes su projektu susijusioms prognozės operacijoms. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Apžvalgos skirtukas Poreikio prognozės puslapyje.

Toliau pateikiamoje lentelėje aprašomi laukai **Poreikio** prognozės **puslapio skirtuke** Apžvalga.

| Laukas | Aprašas |
|---|---|
| **Užduoties pavadinimas** | Bendro apdorojimo, kuris buvo naudojamas prognozės eilutei sukurti, pavadinimas. |
| **Modelis** | Prognozės modelis, su kuriuo susieta operacija. |
| **Data** | Operacijos pradžios data. |
| **Kliento kodas** | Su perlaida susijusi kliento sąskaita. |
| **Klientų grupė** | Su kliento grupe susijusi kliento sąskaita. |
| **Prekės Nr.** | Prekės identifikatorius. |
| **Produkto pavadinimas** | Prekės aprašymas. |
| **Prekių paskirstymo raktas** | Prekių paskirstymo raktas, naudojamas paskirstant atsargų prognozes. |
| **Pardavimo kiekis** | Perlaidps kiekis, išreikštas nurodytu pardavimo vienetu pardavimo grupėje. |
| **Vienetas** | Vienetas, kuriuo parduodama prekė. |
| **Suma** | Bendra suma, atėmus nuolaidų, dėl kurių prognozės operacija daro įtaką prognozei. |
| **Pardavimo kaina** | Vienetų skaičiaus pardavimo kaina, nurodyta lauke **Kainos kiekis**. Vertė nuskaitoma iš prekių nustatymas, tačiau ją galite modifikuoti. |
| **Pardav. valiuta** | Operacijos metu naudotas prognozės kodas. Numatytoji valiuta automatiškai įveda,a bet galite pasirinkti kitą valiutą. |
| **Svėrimo kiekis** | Prognozuojamas kiekis nurodytu esamo svorio vienetu. |
| **Svėrimo vnt.** | Pasirinkite pagavimo vienetą, kuriuo bus parduodama prekė. Vertė automatiškai nuskaitoma iš prekės nustatymo. |
| (Kitos dimensijos) | Papildomos produkto, laikymo ir sekimo dimensijos gali būti rodomos tinklelyje kaip stulpeliai. Norėdami pasirinkti papildomus rodomus matmenis, rinkitės **Rodyti matmenis** veiksmų srityje. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Bendras skirtukas poreikio prognozės puslapyje.

Skirtuke **Bendra** rodoma daugiau informacijos apie eilutę, kurią šiuo metu pasirinkote **skirtuke** Peržiūra. Kai kuri informacija kartojama skirtuke **Peržiūra**. Toliau pateikiamoje lentelėje aprašomi unikalūs skirtuko **Bendra** laukai.

| Laukas | Aprašas |
|---|---|
| Poreikio prognozės sekos numeris | Unikalus poreikio prognozės eilutės numeris. Šis numeris generuojamas naudojant numeraciją, pasirinktą poreikio prognozėms **bendrojo planavimo parametrų** puslapyje. |
| Prekių grupė | Prekės grupė, su kuria susijusi operacija. |
| Ataskaita | Nustatykite šią parinktį į *Taip* tam, kad operacija būtų įtraukta į ataskaitas. |
| Komentarai | Įveskite visus komentarus apie prognozės perlaidą. |
| Aktyvi | Pažymėti šį langelį, kad operacija būtų įtraukta į biudžeto ataskaitas. Negalima modifikuoti ataskaitų operacijų šio žymės langelio nustatymo. |
| Įtraukti į grynųjų pinigų srautų prognozes | Pažymėkite šį langelį, kad prognozės operacijos būtų paskirtos į didžiąją knygą. Negalima modifikuoti ataskaitų operacijų šio žymės langelio nustatymo. Daugiau informacijos žr. [Pinigų srauto planavimas](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| PVM grupė | Mokesčių grupė, naudojama nurodant prognozės operacijos mokesčius. |
| Prekės PVM grupė | Prekės mokesčių grupė, naudojama nurodant prognozės operacijos mokesčius. |
| Metodas | <p>Pasirinkite metodą, kuris naudojamas prognozės operacijai paskirstyti:</p><ul><li>**Joks** – paskirstymas nevykdomas.</li><li>**Laikotarpis** – prognozeikite tą patį kiekį kiekvienam laikotarpiui. Jei pasirinksite šią vertę, lauke Už nurodykite **kiekį**, o lauke Vienetas – **laiko** vienetą.</li><li>**Raktas** – prognozės kiekis paskirstomas pagal laikotarpių paskirstymo raktą, kurį nurodote lauke **Laikotarpio raktas**. Galite naudoti šį metodą, kai norite apgalvoti sezonų kaitą.</li><ul>|
| Per | <p>Įvesti intervalų, kuriais prognozė nusitęsia į ateitį, skaičių. Šis laukas galimas, tik jei lauke pasirinkote *Laikotarpis* laukelyje **Metodas**.</p><p>Pavyzdžiui, jei pasirinkote *Laikotarpis* laukelyje **Metodas** įveskite *1* lauke **pagal** ir rinkitės *Mėnesiai* lauke **Vienetas**. Lauke **Pabaiga** nurodote pabaigos datą, kuri prasitęsia metus į ateitį. Jei viena prognozės eilutė sukurta kiekvienam ateinančių metų mėnesiui, pagal prekę ir kiekį, kuri nurodyti antraštės eilutėje. |
| Vienetas | Pasirinkite laiko intervalo vienetą: *dienos*, *mėnesiai* arba *metai*. Paskyrimas tuomet atitinka dienų skaičių ar metų skaičių, kurį nurodėte **Pagal** lauke.|
| Laikotarpio raktas | Nurodyti laikotarpio paskirstymo raktą, kuris naudojamas prognozei paskirstyti. Daugiau informacijos žr. [Biudžeto planavimo duomenų paskirstymas](../../finance/budgeting/budget-planning-data-allocation.md). |
| Pabaigoje | Rodo pabaigos datą jums naudojant **Pagal** ir **Vieneto** laukus. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Prekės bendras skirtukas poreikio prognozės puslapyje.

Skirtuke **Prekės** rodoma daugiau informacijos apie prekę, kurią šiuo metu pasirinkote **skirtuke** Peržiūra. Kai kuri informacija kartojama skirtuke **Peržiūra**. Toliau pateikiamoje lentelėje aprašomi unikalūs skirtuko **prekė** laukai.

| Laukas | Aprašas |
|---|---|
| Kainos vienetas | Pardavimo vienetų, kuriems taikoma pardavimo kaina, skaičius. Vertė automatiškai gaunama iš prekių lentelės, tačiau jį galite modifikuoti. |
| Pardavimo mokesčiai | Pardavimo kainos fiksuoti mokesčiai. Mokesčiai nepriklauso nuo kiekio. |
| Savikaina | Esamos prognozės operacijos išlaidos atsargų vienetui. Vertė nuskaitoma iš prekių lentelės, tačiau ją galite modifikuoti. |
| Nuolaida procentais | Nuolaida kaip procentinė dalis. |
| Nuolaidos suma | Nuolaida, išreikšta kaip pardavimo vieneto suma. |
| Bendra suma | Suma, kai netaikoma jokia nuolaida. |
| Atsargų kiekis | Perlaidos kiekis, išreikštas prekės atsargų vienetais. |
| Naudoti konkrečią KS | Konkrečios KS numeris. |
| Naudoti konkretų maršrutą | Konkretaus maršruto numeris. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Projekto bendras skirtukas poreikio prognozės puslapyje.

Skirtukas **Projektas** rodoma daugiau informacijos apie prekę, kurią šiuo metu pasirinkote **Peržiūra** skirtuke. Kai kuri informacija kartojama skirtuke **Peržiūra**, **Bendra** ar **Prekės** skirtuke. Toliau pateikiamoje lentelėje aprašomi unikalūs skirtuko **prekė** laukai.

| Laukas | Aprašas |
|---|---|
| Projekto data | Poreikio prognozės perlaidos data. |
| Projekto ID | Projekto identifikatorius, kurį nurodo dabartinė operacija. |
| Lėšų skyrimo šaltinis | Finansavimo šaltinis, su kuriuo susieta poreikio prognozė. |
| Veiklos numeris | Veikla, su kuria susieta poreikio prognozės perlaida. |
| Kategorija | Dabartinės operacijos kaštų kategorija. |
| Eilutės ypatybė | Operacijai priskirta būsena. |
| Operacijos ID | Poreikio prognozės operacijos sistemos identifikatorius. |
| Išlaidų suma | Poreikio prognozės kiekio data. |
| Vnt. kaina | Vieneto kaina. |
| Modifikavo | Paskutinis pasirinktą operaciją modifikavusio darbuotojo identifikatorius. |
| SF data | Įveskite numatomos sąskaitos datą. |
| Pašalinimo data | Peržiūrėkite arba modifikuokite pašalinimo datą. Kai sukuriama prognozė, pašalinimo data nustatoma kaip projekto pabaigos data. Jei projekto pabaigos datos nėra, bus taikoma projekto data. Šis laukas taikomas tik fiksuotos kainos ir projektams. |
| Išlaidų mokėjimo data | Įvesti numatytą pirkimo mokėjimo datą. |
| Pardavimo mokėjimo data | Įvesti numatytą pardavimo mokėjimo datą. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Finansinių dimensijų skirtukas poreikio prognozės puslapyje.

Skirtuke **Finansinės dimensijos** rodomos visos eilutės, kuri šiuo metu pasirinkta skirtuke Peržiūra, finansinių **dimensijų** vertės.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Atsargų dimensijų skirtukas poreikio prognozės puslapyje.

Skirtuke **Atsargų dimensijos** rodomos visos atsargų dimensijos eilutės, kuri šiuo metu pasirinkta skirtuke Peržiūra, finansinių **dimensijų** vertės.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Paskyrtimo tinklelis poreikio prognozės puslapyje.

Jei naudojate prekių paskirstymo raktą arba jei įvedėte vieno ar kelių būsimų laikotarpių prekės prognozę, galite paskirstyti prognozę skirtuke **Peržiūra pasirinkdami** Paskirstyti prognozę. Kiekis **paskirstomas** taip, kaip nurodyta paskirstymo **tinklelio** eilutėse. (Žr. [Skirti prognozę](#allocate-forecast) Atsargų atnaujinimo prognozės operacijos.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Atsargų prognozė

Tiekimo ir poreikio prognozės eilučių puslapiuose yra **atsargų prognozės** mygtukas kuris atidaro tos pačios **atsargų prognozės** puslapį, kuris filtruojamas tuo pačiu prekės ar modelio deriniu. Ši atsargų prognozė pateikia balansą tarp tiekimo ir poreikio, kurie buvo įvesti tai pačiai prekei. Jos negalima redaguoti. Atsargų prognozė padeda atsargų valdymo komandai peržiūrėti numatomus turimų prekės atsargų pokyčius ateinant prognozuojamu laikotarpiu.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Veiksmų srities komandos atsargų prognozės puslapyje

Toliau pateiktoje lentelėje aprašomos komandos, esančios puslapio **atsargų prognozė** veiksmų srityje.

| Operacija | Aprašas |
|---|---|
| Tiekimo prognozė | Atidaryti atsargų **tiekimo prognozę,** kuris filtruojamas pagal pasirinktą tą patį prekės / modelio / datos derinį, rodinį. |
| Poreikio prognozė | Atidaryti atsargų **poreikio prognozę,** kuris filtruojamas pagal pasirinktą tą patį prekės / modelio / datos derinį, rodinį. |
| Atsargos \> Rodyti dimensijas | Pasirinkti atsargų dimensijas, kurios turėtų būti rodomos tinklelyje, **skirtuke** Peržiūra tinklelyje. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Veiksmų srities komandos atsargų prognozės tinklelyje

Šioje lentelėje aprašomi laukeliai, esantys puslapio **Atsargų prognozės** tinklelyje.

| Laukas | Aprašas |
|---|---|
| **Modelis** | Prognozės modelis, su kuriuo susieta operacija. |
| **Prekės Nr.** | Prekės identifikatorius. |
| **Biudžeto data** | Poreikio prognozės perlaidos data. |
| **Prognozės tipas** | Operacijos šaltinis (*poreikio prognozė* arba *tiekimo prognozė*). |
| **Svėrimo kiekis** | Prognozuojamas kiekis nurodytu esamo svorio vienetu. |
| **Kiekis** | Kiekis, planuojamas kiekis atsargų vienetais. |
| **Sukauptas svėrimas** | Sukauptas prognozės kiekis esamo svorio vienetais, kai tai pačiai prekei buvo sukauptos kelios prognozės eilutės. |
| **SubKS** | Konkrečios KS numeris. |
| **Maršrutas** | Konkretaus maršruto numeris. |
| (Kitos dimensijos) | Papildomos dimensijos tinklelyje gali būti rodomos kaip stulpeliai. Norėdami pasirinkti papildomus rodomus matmenis, rinkitės **Atsargų \> Rodomi matmenys** veiksmų srityje. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Paskirstyti prognozę

Naudodami šią procedūrą galite apdoroti esamas prognozės operacijos eilutes. Kai paskirstote prognozę, kiekis paskirstomas taip, kaip nurodyta paskirstymo **tinklelio** eilutėse.

1. Priklausomai nuo objekto, kuriam norite sukurti prognozę, tipo ir prognozės, kurią norite sukurti, tipo, atidaryti tiekimo, poreikio arba [atsargų prognozės puslapį, kaip aprašyta šioje lentelėje](#manual-entry).
1. Tiekimo arba poreikio prognozės eilučių puslapyje pasirinkite prognozės eilutę, tada skirtuke Peržiūra pasirinkite **įrankių** juostoje **Paskirstyti prognozę**.
1. Dialogo lange **Paskirstyti prognozę** nustatykite laukus, kurie aprašyti šioje lentelėje. (Vertė, kurią pasirenkate lauke **Metodo** laukas nustato, kad kiti galimi laukai.)

    | Laukas | Aprašas |
    |---|---|
    | Metodas | <p>Pasirinkite metodą, kuris naudojamas prognozės operacijai paskirstyti:</p><ul><li>**Joks** – paskirstymas nevykdomas.</li><li>**Laikotarpis** – prognozeikite tą patį kiekį kiekvienam laikotarpiui. Jei pasirinksite šią vertę, lauke Už nurodykite **kiekį**, o lauke Vienetas – **laiko** vienetą.</li><li>**Raktas** – prognozės kiekis paskirstomas pagal laikotarpių paskirstymo raktą, kurį nurodote lauke **Laikotarpio raktas**. Galite naudoti šį metodą, kai norite apgalvoti sezonų keitimus.</li><ul>|
    | Per | <p>Įvesti intervalų, kuriais prognozė nusitęsia į ateitį, skaičių. Šis laukas galimas, tik jei lauke pasirinkote *Laikotarpis* laukelyje **Metodas**.</p><p>Pavyzdžiui, jei pasirinkote *Laikotarpis* laukelyje **Metodas** įveskite *1* lauke **pagal** ir rinkitės *Mėnesiai* lauke **Vienetas**. Tada, lauke **Pabaiga** nurodote pabaigos datą, kuri prasitęsia metus į ateitį. Jei viena prognozės eilutė sukurta kiekvienam ateinančių metų mėnesiui, pagal prekę ir kiekį, kuri nurodyti antraštės eilutėje. |
    | Vienetas | Pasirinkite laiko intervalo vienetą: *dienos*, *mėnesiai* arba *metai*. Paskyrimas tuomet atitinka dienų skaičių ar metų skaičių, kurį nurodėte **Pagal** lauke.|
    | Laikotarpio raktas | Nurodyti laikotarpio paskirstymo raktą, kuris naudojamas prognozei paskirstyti. Daugiau informacijos žr. [Biudžeto planavimo duomenų paskirstymas](../../finance/budgeting/budget-planning-data-allocation.md). |
    | Pabaigoje | Nurodykite pabaigos datą, kuri taikoma jūsų laukuose **Vienetui** ir **Vienetui**. |

1. Pasirinkite **Gerai** nustatymų patvirtinimui.
1. Galite peržiūrėti tos pačios **eilutės** rezultatus skirtuke Paskirstymas.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Masinio atnaujinimo prognozės operacijos

Naudodami šią procedūrą galite apdoroti esamas prognozės operacijos eilutes. Galite kopijuoti, redaguoti ir naikinti prognozės operacijos eilutes.

1. Tiekimo arba poreikio prognozės eilučių puslapyje pasirinkite **Masinis atnaujinimas**.
1. Dialogo lange pasirinkite **Filtruoti**.
1. Skirtuke **Intervalas** pasirinkite kriterijus, identifikuojančius šaltinio prognozės duomenis, kuriuos norite kopijuoti, modifikuoti arba naikinti. Duomenys gali būti prognozės modelis, prekės numeris ir kliento sąskaita.
1. Pasirinkite **OK** pasirinkimo patvirtinimui.

    Pasirinkę duomenis galite naudoti dialogo langą Redaguoti prognozės operacijas, kad nurodytumėte, kaip norite juos **kopijuoti, redaguoti arba** panaikinti.

    > [!NOTE]
    > Filtravimo veiksmas yra būtina sąlyga norint naudoti **masinio redagavimo** funkciją. Jei jį praleisite, programa pasirinks ir atnaujins **visas** prognozės eilutes. Dėl to galite netyčia dubliuoti arba pašalinti operacijas.

1. Valdymo **skyriuje** pasirinkite, ar norite kopijuoti, atnaujinti ar panaikinti pasirinktas prognozės operacijas.
1. Naudodami **Keitimai laukelyje** skurių, kuriuo keisite prognozės parametrus. Pažymėkite parametro žymės langelį ir rinkitės iš galimų parinkčių. Pavyzdžiui, pažymėkite žymės **langelį** Modelis, tada pasirinkite prognozės modelio numerį. Esamos prognozės eilutės kopijuojamos į pasirinktą prognozės modelį.
1. Naudokite skyrių **Laikotarpio keitimas**, kad perkeltumėte prognozės pradžios ir pabaigos datas į priekį ir atgal. Pažymėkite žymės langelį ir naudodami kiekio ir laikotarpio laukus nurodykite prognozės datų perkėlimo laikotarpį. Galite įvesti neigiamą kiekį, jei pradžios datą norite perkelti į priekį (tai yra, padaryti ją anksčiau).

    Pavyzdžiui, norėdami atidėti prognozės operacijos pradžios datą šešiais mėnesiais, pažymėkite žymės langelį, įveskite 6 kaip kiekį ir pasirinkite *Mėnesiai* kaip *laikotarpį*.

1. Naudodami **tinkamą laukelį** skyrių atnaujinkite faktinius prognozės duomenis. Lauke **Laukelis** pasirinkite kriterijų, kurį norite pakeisti. Lauke **Faktorius** įveskite daugybos koeficientą, kurį reikia taikyti pasirinktam kriterijui, arba įveskite sumos ar atimties konstantą. Pavyzdžiui, rinkitės *Kiekis* kaip kriterijų ir įveskite *1,5* kad prekės kiekis būtų padaugintos iš 1,5. Kitu atveju, įveskite konstantą *-25* ir sumažinsite prekės kiekį 25 vienetais.
1. Naudokite skyrių **Finansinės dimensijos**, norėdami atnaujinti prognozės eilučių finansines dimensijas. Pasirinkite finansines dimensijas, kurias norite keisti, tada įveskite vertę, kurią norite taikyti pasirinktoms dimensijoms.
1. Pasirinkite **Gerai** keitimo pritaikymui.

## <a name="use-forecasts-with-master-planning"></a>Prognozių naudojimas su bendruoju planavimu

Kai įvedate poreikio prognozę ir (arba) tiekimo prognozę, bendrojo planavimo metu galite įtraukti prognozes, kad būtų apskaičiuojamas numatomas poreikis ir (arba) tiekimas jūsų bendrojo planavimo vykdyme. Kai prognozės įtraukiamos į bendrąjį planavimą, apskaičiuojami bendrieji medžiagų ir pajėgumo reikalavimai bei sugeneruojami suplanuoti užsakymai.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Bendrojo plano nustatymas, kad jis apimtų atsargų prognozę

Norėdami nustatyti bendrąjį planą taip, kad jis apimtų atsargų prognozę, atlikite šiuos žingsnius.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Pasirinkite esamą planą ar sukurkite naują.
1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Prognozės modelis** – Pasirinkite taikomą prognozės modelį. Šis modelis bus laikomas galiojančiu, kai tiekimo siūlymas yra sukuriamas esamam pagrindiniam planui.
    - **Įtraukti tiekimo prognozę** – Nustatykite šią parinktį į *Taip*, kad įtrauktumėte tiekimo prognozę esamame bendrajame plane. Jei nustatote *Ne*, tiekimo prognozės operacijos nebus įtrauktos į pagrindinį planą.
    - **Įtraukti paklausos prognozę** – Nustatykite šią parinktį į *Taip*, kad ji įtraukti paklausos prognozę esamame pagrindiniame plane. Jei nustatote *Ne*, paklausos prognozės perlaidos nebus įtrauktos į pagrindinį planą.
    - **Metodas naudojamas siekiant sumažinti prognozės reikalavimus** – Pasirinkite metodą, kuris turi būti naudojamas siekiant sumažinti prognozės reikalavimus. Daugiau informacijos rasite [Prognozių mažinimo raktai](planning-optimization/demand-forecast.md#reduction-keys).

1. „FastTab“ **Laiko ribos dienomis** galite nustatyti tolesnius laukelius siekiant nustatyti laikotarpį, per kurį yra įtraukta prognozė:

    - **Prognozės planas** – Nustatykite parinktį į *Taip* tam, kad ji viršytų prognozės plano laikos tvarką, kurios ištakos yra atskiros apimties grupėse. Nustatykite ją į *Ne* tam, kad naudotumėte vertės atskiros apimties grupėms esamame pagrindiniame plane.
    - **Prognozės laiko laikotarpis** – Jei nustatote **Prognozės plano** parinktį į *Taip*, nurodykite dienų skaičių (nuo šiandienos), kuriam bus taikoma paklausos prognozė.

    > [!IMPORTANT]
    > Parinktis **Prognozės planas** dar nėra palaikomas su Planavimo optimizavimu.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Bendrojo plano, apimančio atsargų prognozę, vykdymas

Norėdami vykdyti bendrąjį planą, apimantį atsargų prognozę, atlikite šiuos žingsnius.

1. Eikite į **Bendrasis planavimas \> Darbo sritys \> Bendrasis planavimas**.
1. Lauke **Bendrasis planas** įveskite arba pasirinkite bendrąjį planą, kurį nustatėte ankstesnėje procedūroje.
1. Plytelėje **Bendrasis planavimas** pasirinkite **Vykdyti**.
1. Dialogo lange **Bendrasis planavimas** nustatykite parinktį **Sekti apdorojimo laiką** į *Taip*.
1. Lauke **Gijų skaičius** įveskite skaičių.
1. „FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.
1. Atsiranda standartinis užklausų rengyklės dialogo langas. Skirtuke **Diapazonas** pasirinkite eilutę, kurioje laukas **Laukas** yra nustatytas kaip *Elemento numeris*.
1. Lauke **Kriterijai** pasirinkite prekės numerį, kurį norite įtraukti į planą.
1. Pasirinkite **Gerai**.

Norėdami peržiūrėti apskaičiuotus poreikius, atidarykite **bruto poreikių** puslapį. Pavyzdžiui, veiksmų srities puslapio **Išleisti produktai** skirtuko **Planuoti** grupėje **Poreikiai** pasirinkite **Bendrasis poreikis**.

Norėdami peržiūrėti sugeneruotus suplanuotus užsakymus, eikite į **Bendrojo planavimo \> bendrus \> suplanuotus užsakymus**, ir pasirinkite reikiamą prognozės planą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Poreikio prognozavimo apžvalga](introduction-demand-forecasting.md)
- [Poreikio prognozavimo nustatymas](demand-forecasting-setup.md)
- [Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)
- [Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)
- [Pagrindinis planavimas su paklausos prognozėmis](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
