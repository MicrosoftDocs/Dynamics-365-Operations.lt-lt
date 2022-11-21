---
title: „Inventory Visibility“ atsargų paskirstymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir naudoti atsargų paskirstymo funkciją, kuri leidžia atidėti skirtas atsargas ir užtikrinti, kad jūs galite vykdyti pelningiausią kanalą ar klientus.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762678"
---
# <a name="inventory-visibility-inventory-allocation"></a>„Inventory Visibility“ atsargų paskirstymas

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Verslo fonas ir paskirtis

Organizacijos dažnai turi iš anksto paskirstyti savo atsargas svarbiausiems pardavimo kanalams, klientų grupėms, regionams ir akcijos įvykiams, siekiant užtikrinti, kad iš anksto nepaskirstytos atsargos būtų apsaugotos nuo bet kokio kito naudojimo ir būtų suvartojamos tik per pardavimo operacijas, susijusias su paskirstymu. Atsargų paskirstymas pagal atsargų matomumą yra pardavimo veiklos planavimo proceso komponentas ir atliekamas prieš įvykdant bet kokią faktinę pardavimo veiklą arba sukūrus pardavimo užsakymą.

Pavyzdžiui, įmonė, pavadinta "Contoso", gamina populiariausią. Deja, dėl to, kad naujausias tiekimo grandinės nutraukimas paveikė visas tos atsargos tranzitines atsargas, Contoso tik ribotas savo atsargas ir turi ja naudotis. "Contoso" veikia ir tinkle, ir parduotuvėse. Kiekviename pardavimo kanale įmonė turi keletą svarbių įmonės partnerių (prekyviečių ir didelių mažmenininkų), kurie reikalauja, kad jiems būtų įrašyta konkreti galimų atsargų dalis. Todėl dviračio įmonė turi sugebėti suderinti atsargų paskirstymą kanaluose ir valdyti SAVO VIP partnerių lūkesčius. Geriausias būdas pasiekti abu tikslus yra naudoti atsargų paskirstymą, kad kiekvienas kanalas ir mažmenininkas galėtų gauti tam tikrus paskirstytus kiekius, kuriuos vėliau bus galima parduoti vartotojams.

Atsargų paskirstymas turi du pagrindinius verslo tikslus:

- **Atsargų apsauga (žiedinis skambutis)** – organizacijos nori iš anksto perskirstyti apribotas arba ribotas atsargas prioritetams nustatytiems kanalams, regionams, VIP klientams ir filialų įmonėms. Atsargų matomumo paskirstymo funkcijos tikslas yra apsaugoti paskirstytas atsargas, kad kiti paskirstymai, rezervavimai ar kiti pardavimo poreikiai nepaveiktų anksčiau paskirstytų atsargų.
- **Perteklinio pardavimo valdymas** – atsargų matomumo paskirstymo priemonė siekia apriboti anksčiau paskirstytus kiekius, kad gaunanti šalis (pvz., kanalas ar klientų grupė) nevartotų jų per daug, kai pradeda veikti faktinė pardavimo operacija, pagrįsta švelniu rezervavimu.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Paskirstymo aprašas atsargų matomumo paslaugoje

### <a name="allocation-virtual-pool"></a>Paskirstymo virtualusis telkinys

Nors atsargų matomumo paskirstymo funkcija nenustato faktinių atsargų kiekių, ji nurodo turimus faktinių atsargų kiekius, *kad* būtų galima nustatyti pradinį turimų atsargų kiekį virtualiųjų telkinių kiekiui paskirstyti. Atsargų paskirstymas pagal atsargų matomumą yra švelniai paskirstymas. Tai atliekama prieš įvykstant faktinėms pardavimo operacijoms ir nepriklauso nuo pardavimo užsakymų. Pavyzdžiui, galite paskirstyti atsargas svarbiausiems pardavimo kanalams arba stambiems įmonės mažmenininkams prieš galutiniams klientams apsilankant pardavimo kanale arba mažmeninės prekybos parduotuvėje, kad galėtų pirkti.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Skirtumas tarp atsargų paskirstymo ir soft rezervavimo

[Paprastai švelniai rezervavimai](inventory-visibility-reservations.md) susiejami su faktinėmis pardavimo operacijomis (pardavimo užsakymo eilutės). Ir paskirstymą, ir švelniai rezervavimą galima naudoti nepriklausomai, tačiau jei norite juos naudoti kartu, po paskirstymo turi būti atliktas švelniai rezervavimas. Pirmiausia rekomenduojame atlikti atsargų paskirstymą, o tada iš dalies rezervuoti paskirstytus kiekius, kad būtų pasiektas beveik realiuoju laiku sunaudojimas pagal paskirstymą. Daugiau informacijos rasite Naudojimo [kaip švelniai rezervavimas](#consume-to-soft-reserved).

Atsargų paskirstymo funkcija leidžia pardavimo planuotojus arba raktų sąskaitų vadovus valdyti ir iš anksto paskirstyti svarbias paskirstymo grupių atsargas (pvz., kanalus, regionus ir klientų grupes). Taip pat ji palaiko suvartojimo pagal paskirstytus kiekius realiuoju laiku sekimą, koregavimą ir analizę, siekiant užtikrinti, kad būtų galima papildyti arba perskirstyti laiku. Šis gebėjimas realiuoju laiku matyti matomumą paskirstymo, suvartojimo ir paskirstymo balanse, ypač svarbus greitos pardavimo arba akcijos įvykiams.

## <a name="terminology"></a>Terminologija

Šios sąlygos ir sampratos yra naudingos atsargų paskirstymo diskusijose:

- **Paskirstymo grupė** – grupė, kuri valdo paskirstymą, pvz., pardavimo kanalas, klientų grupė ar užsakymo tipas.
- **Paskirstymo grupės** vertė – kiekvienos paskirstymo grupės vertė. Pavyzdžiui, internetas *arba* *parduotuvė* gali būti pardavimo kanalo paskirstymo grupės vertė, *o VIP* *ar įprasta* – klientų paskirstymo grupės vertė.
- **Paskirstymo hierarchija** – A reiškia paskirstymo grupių jungtį hierarchiniu būdu. Pavyzdžiui, galite nurodyti kanalą kaip *1* hierarchijos lygį, *regioną* – 2 lygį, *o klientų grupę* – kaip 3 lygį. Paskirstant atsargas, reikia vadovautis paskirstymo hierarchijos seka, kai nurodote paskirstymo grupės vertę. Pavyzdžiui, jūs galite paskirstyti 200 raudonai *eilutėms* interneto kanalui, *Londono* regionui ir VIP *klientų* grupei.
- **Galima paskirstyti** – virtualusis *bendras telkinys*, nurodantis kiekį, kurį galima toliau paskirstyti. Apskaičiuotas matas, kurį galite laisvai nustatyti naudodami savo formulę. Jei naudojate ir soft reservation priemonę, rekomenduojame naudoti tą pačią formulę, norint apskaičiuoti turimas paskirstyti ir galimas rezervuoti.
- **Paskirstyta** – faktinis matas, rodantis paskirstytą paskirstymą, kurį gali suvartoti paskirstymo grupės. Jis atimamas tuo pat metu, kai pridedamas suvartotas kiekis.
- **Suvartota** – faktinis matas, nurodantis, kad kiekiai, suvartoti prieš pradinį paskirtą kiekį. Prie šio faktinio mato pridedami skaičiai, todėl automatiškai sumažinamas priskirtas faktinis matas.

Toliau pateikta iliustracija rodo atsargų paskirstymo verslo darbo eigą.

![Atsargų matomumo paskirstymo verslo darbo eiga.](media/inventory-visibility-allocation-flow.png "Atsargų matomumo paskirstymo verslo darbo eiga.")

Toliau pateikta iliustracija rodo paskirstymo hierarchiją ir paskirstymo grupes. Virtualus *bendras telkinys*, kuris rodomas čia yra kiekis, kurį galima paskirstyti.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title=" Atsargų matomumo paskirstymo hierarchija" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>Nustatyti atsargų paskirstymą

Atsargų paskirstymo priemonę sudaro šie komponentai:

- Iš anksto nustatytas su paskirstymu susijęs duomenų šaltinis, faktiniai duomenys ir skaičiuojami duomenys.
- Pritaikomos paskirstymo grupės, kurių didžiausias leidžiamas aštuonių lygių skaičius.
- Paskirstymo programos programavimo sąsajų rinkinys (API):

    - paskirstyti
    - Perskirstyti
    - nepaskirstyti
    - Vartoti
    - Užklausos

Paskirstymo priemonės konfigūravimo procesas turi tris žingsnius:

- Įjunkite atsargų matomumo programos funkciją, nueikite į Konfigūracijos **funkcijų \> valdymas > Parametrų \> paskirstymas**.
- Nustatyti duomenų [šaltinį ir](inventory-visibility-configuration.md#data-source-configuration) jo [priemones](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Nustatykite paskirstymo grupės pavadinimą ir hierarchiją.

### <a name="predefined-data-source"></a>Iš anksto nustatytas duomenų šaltinis

Kai įgalinate paskirstymo priemonę ir iškiesite konfigūracijos atnaujinimo API, atsargų matomumas sukuria vieną iš anksto nustatytą duomenų šaltinį ir keletą pradinių priemonių.

Duomenų šaltinis pavadintas `@iv`. Jame įtrauktas numatytųjų fizinių priemonių rinkinys. Jas galite peržiūrėti naudodami atsargų matomumo programą, nueidami į **konfigūracijos \> duomenų šaltinį**. Turėtumėte matyti duomenų **šaltinį – @IV**. Išplėskite `@iv` duomenų šaltinį, kad būtų galima peržiūrėti pradinių faktinių priemonių sąrašą:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Norėdami peržiūrėti **pradinį apskaičiuotą** matą, pavadintą :, pasirinkite skirtuką Apskaičiuoti matai `@iv.@available_to_allocate`:

- `@iv`

    - `@iv.@available_to_allocate` = `??`– – `??``@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Įtraukti kitus faktinius matus į prieinamą paskirstyti apskaičiuotą matą

Norėdami naudoti paskirstymą, turite teisingai nustatyti formulę, kurią būtų galima priskirti skaičiuojamas matas (`@iv.@available_to_allocate`). Pavyzdžiui, `fno``onordered` turite duomenų šaltinį ir matą, `pos``inbound` duomenų šaltinį ir matą, `fno.onordered``pos.inbound` taip pat norite paskirstyti turimose atsargose sumą ir. Šiuo atveju turėtų `@iv.@available_to_allocate` būti formulėje `pos.inbound``fno.onordered`. Čia pateikiamas pavyzdys:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

> [!NOTE]
> Duomenų šaltinis yra `@iv` iš anksto nustatytas duomenų šaltinis, o su prefiksu `@iv` apibrėžti faktiniai duomenys yra `@` iš anksto nustatyti duomenys. Šios priemonės yra iš anksto nustatyta paskirstymo funkcijos konfigūracija, todėl nekeiskite jų ar nenaikykite jų arba, tikėtina, kad įvyksta netikėtos klaidos naudojant paskirstymo funkciją.
>
> Galite pridėti naujų faktinių matų prie iš anksto apskaičiuoto matavimo `@iv.@available_to_allocate`, tačiau jo pavadinimo keisti negalima.

### <a name="manage-allocation-groups"></a>Paskirstymo grupių valdymas

Galima nustatyti daugiausiai aštuonis paskirstymo grupių pavadinimus. Grupėse yra hierarchija. Norėdami peržiūrėti ir atnaujinti paskirstymo grupes, atlikite šiuos veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **konfigūracijos** puslapį, tada skirtuke **Paskirstymas** pasirinkite Redaguoti **konfigūraciją**. Numatyta, kad yra paskirstymo hierarchija, kuri turi keturis sluoksnius: `Channel` (viršutinis sluoksnis), `customerGroup` (antras sluoksnis),`Region` (trečias sluoksnis) ir `OrderType` (ketvirtas sluoksnis).
1. Esamą paskirstymo grupę galite pašalinti pasirinkdami **šalia jos esančią X**. Naujas paskirstymo grupes į hierarchiją galite įtraukti tiesiogiai į lauką įvesdami kiekvienos naujos grupės pavadinimą.

    > [!IMPORTANT]
    > Panaikinkite arba keisite paskirstymo hierarchijos susiejimą. Patarimų ieškokite Paskirstymo [naudojimo patarimai](#allocation-tips).

1. Baigę paskirstymo grupės ir hierarchijos parametrų konfigūravimą, įrašykite pakeitimus, **o tada viršutinėje dešinėje pasirinkite** Naujinti konfigūraciją. Sukonfigūruotų paskirstymo grupių vertės bus atnaujintos, kai sukursite paskirstymą naudodami vartotojo sąsają arba API SKELBIMĄ (/api<wbr>/environmentId<wbr>/\{\}<wbr>/allocation<wbr>/allocate). Informacija apie abu būdus pateikiama toliau šiame straipsnyje.

Jei naudojate keturis grupių pavadinimus ir \[`channel` nustatote juos kaip, `customerGroup``region`, `orderType`\] šie pavadinimai tinkami su paskirstymu susijusioms užklausoms, kai iškiesite konfigūracijos atnaujinimo API.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a> Paskirstymo naudojimo patarimai

- Kiekvienam produktui paskirstymo funkcija turi naudoti tame *pačiame* dimensijų lygyje pagal produktų indeksų hierarchiją, kurią nustatėte produktų indeksų [hierarchijos konfigūracijoje](inventory-visibility-configuration.md#index-configuration). Pavyzdžiui, tarkime, kad jūsų indeksų hierarchija \[`Site` yra, `Location``Color`, . `Size`\] Jei dimensijų lygyje \[`Site` tam tikrą kiekį priskiriate vienam produktui, `Location``Color`\] kitą kartą, kai norite paskirstyti šį produktą, taip pat turėtumėte paskirstyti tame pačiame lygyje, \[`Site`,`Location``Color`\]. Jei naudojate lygį \[`Site`, (`Location` arba `Color`) `Size`\]\[`Site`, `Location`\] duomenys bus nesuderinami.
- **Modifikuojant paskirstymo grupes ir hierarchiją:** jei sistemoje jau yra paskirstymo duomenų, esamos paskirstymo grupės arba paskirstymo grupės hierarchijos pamaina sugadins esamą paskirstymo grupių susiejimą. Todėl prieš atnaujindami savo naująją konfigūraciją būtinai išvalykite visus senus duomenis neautomatiniu būdu. Tačiau, kadangi naujų paskirstymo grupių pridėjimas prie žemiausios hierarchijos neturi įtakos esamiems susiejimams, duomenų išvalyti nereikia.
- Paskirstyti bus pavyko tik tada, jei produkto kiekis teigiamas `available_to_allocate`.
- Norėdami paskirstyti produktus iš aukšto paskirstymo *lygio* grupės į pogrupį, naudokite `Reallocate` API. Pavyzdžiui, \[`channel` turite paskirstymo grupės hierarchiją,, `customerGroup``region`, `orderType`\] ir \[norite tam tikrą produktą paskirstyti iš paskirstymo grupės tinkle, VIP\] į subskirstyti \[grupę tinkle, VIP, EU\], `Reallocate` naudoti API kiekiui perkelti. Jei naudojate `Allocate` API, kiekis bus paskirstytas iš virtualiojo bendrojo telkinio.
- Norėdami peržiūrėti bendrą produkto prieinamumą (bendrą telkinį), [norėdami](inventory-visibility-api.md#query-on-hand) prašyti atsargų sumos, kurią galima paskirstyti, naudokite turimų atsargų *API užklausą*. Remiantis šia informacija galite priimti paskirstymo sprendimus.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a> Naudoti paskirstymo API

Šiuo metu atidaromos penkios paskirstymo API:

- **REGISTRUOTI / API<wbr> / aplinkos<wbr>/\{environmentId\}<wbr> / paskirstymas<wbr> / paskirstymas** – šis API naudojamas pradiniam paskirstymui sukurti.
- **Registruoti / API<wbr> / aplinkos<wbr>/\{environmentId\}<wbr> / paskirstymas<wbr> / nepaskirstyti** – API naudojama paskirstyties kiekiams grąžinti arba pašalinti.
- **REGISTRUOTI / API<wbr> / aplinkos<wbr>/\{environmentId\}<wbr> / paskirstymas<wbr> / perskirstyti** – Ši API naudojama perkelti paskirstytą kiekį iš esamo paskirstymo į kitas paskirstymo grupes.
- **Registruoti /api<wbr>/aplinkos<wbr>/\{environmentId\}<wbr>/paskirstymą<wbr>/naudojimą** – api yra naudojama paskirstytam kiekiui atskaičiuoti (naudoti).
- **REGISTRUOTI / API<wbr> / aplinkos<wbr>/\{environmentId\}<wbr> / paskirstymas<wbr> / užklausą** – šis API naudojamas norint patikrinti esamus paskirstymo įrašus pagal paskirstymo grupes ir hierarchiją.

### <a name="allocate"></a>Paskirstyti

Iškviesti `Allocate` API, norint paskirstyti konkrečių dimensijų turiinį produktą. Tai yra užklausos kūno schema.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Pavyzdžiui, produkto Tarkime, 1 vieta, 11 *vieta,* raudona spalva, *kanalas internete,* *·* *klientų* grupė VIP *ir regionas* JAV norite priskirti 10 *kiekį*.*·* Norėdami atlikti tokį paskirstymą, galite iškviesti tokį turinio turinį.

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Kiekis visada turi būti didesnis nei 0 (nulis).

### <a name="unallocate"></a>Nepaskirstyti

`Unallocate` Naudokite API operacijai `Allocate` atšaukti. Neigiamas kiekis operacijoje neleistinas `Allocate`. Kūno yra `Unallocate` identiškas .`Allocate`

### <a name="reallocate"></a>Perskirstyti

Naudokite API, `Reallocate` norėdami perkelti kai kuriuos paskirstytus kiekius į kitą grupės derinį. Tai yra užklausos kūno schema.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Pavyzdžiui, \[galite perkelti dvi dalis, kurių dimensijų vieta = 1, vieta = 11, spalva =\]\[raudona iš paskirstymo grupės tinkle, VIP, JAV\]\[į paskirstymo grupę tinkle, VIP, EU\]`Reallocate`, kviečiant API ir pateikiant šį teksto tekstą.

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>Naudoti

`Consume` Naudokite API suvartojimo kiekiui registruoti prieš paskirstymą. Pavyzdžiui, galite naudoti šią API paskirstytam kiekiui perkelti į kai kuriuos tikrus priemones. Tai yra užklausos kūno schema.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Pvz., yra aštuoni paskirstyta dalis, \[kurios dimensijų vieta = 1, vieta = 11, spalva =\]\[raudona paskirstymo grupei Tinkle, VIP, JAV \]. Naudojama ši galima paskirstyti formulė:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

Aštuoni iš mato yra paskirstomi `pos.inbound` vienetai.

Dabar parduodamas trys atsiprašome, o jie paimti iš paskirstymo telkinio. Norėdami užregistruoti šį perkelti, galite skambinti, kuris turi toliau nurodytą užklausos instituciją.

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Po šio skambučio paskirstytas produkto kiekis bus sumažintas 3. Be to, atsargų matomumas sugeneruos turimų atsargų pakeitimo įvykį, kur `pos.inbound` = *-3*. Taip pat galite išlaikyti vertę taip `pos.inbound`, kaip yra, ir tiesiog sunaudoti paskirstytą kiekį. Tačiau šiuo atveju turite sukurti kitą fizinį matą, kad būtų išlaikomi sunaudoti kiekiai, arba naudoti iš anksto nustatytą matą `@iv.@consumed`.

Šioje užklausoje atkreipkite dėmesį, kad fizinis matas, kurį naudojate naudojimo užklausos dalyje, turi naudoti priešingą modifikatoriaus tipą (priedas ar atimtis), palyginus su modifikatoriaus tipu, naudojamu apskaičiuotame mate. Ir tai vartoti kūno, `iv.inbound` turi vertę `Subtraction`, o ne `Addition`.

Duomenų `fno` šaltinio negalima naudoti vartojimo lauke, nes visada teigsime, kad atsargų matomumas negali pakeisti jokių duomenų šaltinio `fno` duomenų. Duomenų srautas yra vien way, o tai reiškia, kad visi `fno` duomenų šaltinio kiekio pakeitimai turi būti gauti iš jūsų tiekimo grandinės valdymo aplinkos.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Naudoti kaip švelniai rezervavimą

API `Consume` taip pat gali naudoti paskirstytą kiekį kaip soft rezervavimą. Tokiu atveju operacija sumažins `Consume` paskirstytą kiekį ir tada šį kiekį iš anksto rezervuos. Norėdami naudoti šį būdą, turite naudoti atsargų matomumo [funkciją](inventory-visibility-reservations.md) švelniai rezervavimo funkcija.

Pvz., nustatote faktinio soft rezervavimo matą kaip `iv.softreserved`. Naudojama ši formulė, kurią naudojant galima rezervuoti apskaičiuojamasis matas:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– `iv.softreserved`

Norėdami naudoti šį nustatymą su paskirstymo priemone, įtraukite `@iv.@allocated`, kad `iv.available_to_reserve` formulę:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– – `iv.softreserved``@iv.@allocated`

Tada atnaujinkite `@iv.@available_to_allocate` į tą pačią vertę.

Kai norite naudoti 3 kiekį ir tiesiogiai rezervuoti šį kiekį, galite skambinti, kuriame yra ši užklausos tekstas.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Šiame prašyme atkreipkite dėmesį, kad `iv.softreserved` vertė yra `Addition` ne `Subtraction`.

### <a name="query"></a>Užklausa

`Query` Naudokite API, norėdami nuskaityti kai kurių produktų su paskirstymu susijusią informaciją. Norėdami susiaurinti rezultatus, galite naudoti dimensijų filtrus ir paskirstymo grupės filtrus. Dimensijos turi tiksliai atitikti tą, kurią norite nuskaityti, pvz., \[vieta = 1, vieta = 11 turės su vieta = 1\]\[susijusių rezultatų, vieta = 1, vieta = 11, spalva = raudona \].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Pavyzdžiui, naudokite vietą = \[1, vieta=11, spalva=raudona\] ir tuščias grupių laukas, kad gautumėte visus paskirstymo įrašus:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Naudokite \[svetainę=1, vieta=11, spalva=\]\[raudona ir grupės channel=Online, customerGroup=VIP, regionas=JAV\], norėdami gauti šios grupės paskirstymo įrašus:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Naudoti paskirstymo vartotojo sąsają

Galite rankiniu būdu valdyti paskirstymus naudodami vartotojo sąsają, atidarydami programą Atsargų matomumas ir nueidami prie veiklos **matomumo \> paskirstymo**. Iš ten galite atlikti bet kuriuos veiksmus, aprašytus toliau aprašytus poskyrius.

### <a name="create-an-allocation"></a>Paskirstymo kūrimas

Norėdami sukurti paskirstymą iš atsargų matomumo **programos** paskirstymo puslapio, atlikite šiuos veiksmus.

1. Pasirinkite **Paskirstyti**.
1. Nustatykite bazinių laukų, dimensijų ir tikslinių reikšmių paskirstymo grupes. (Kai pasirenkate surinkimo duomenų šaltinį lauke **Dimensijų** skyrius, pirmiausiai, naudoja išplečiamąjį sąrašą dimensijoms (pvz., `siteId`) nurodyti. Tada rodouose laukuose įveskite dimensijų vertes.)
1. Pasirinkite **pateikti**.

### <a name="consume-an-allocation"></a>Paskirstymo naudojimo

Pasirinkite **Naudoti** norint naudoti paskirstymą. Norėdami užtikrinti, kad naudojate tinkamoje paskirstymo grupėje ir hierarchijoje, įveskite tuos pačius organizacijos rinkinius ir dimensijos informaciją, kurią įvedėte kurdami paskirstymą.

### <a name="reallocate-an-allocation"></a>Iš dalies paskirstyti paskirstymą

Pasirinkti **Iš dalies perkelti** esamą paskirstytą kiekį iš vieno paskirstymo grupių rinkinio į kitą.

### <a name="query-existing-allocations"></a>Pateikti užklausą dėl esamų paskirstymų

Pasirinkite **Užklausa**, tada įveskite produkto, organizacijos, dimensijos ir paskirstymo grupės vertes, kad gautumėte esamų paskirstymų užklausų rezultatus.
