---
title: „Inventory Visibility“ atsargų paskirstymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir naudoti atsargų paskirstymo funkciją, kuri leidžia atidėti skirtas atsargas ir užtikrinti, kad jūs galite vykdyti pelningiausią kanalą ar klientus.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: f79497a24a5b4dd501bb0d13d9eaca7e98672533
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306121"
---
# <a name="inventory-visibility-inventory-allocation"></a>„Inventory Visibility“ atsargų paskirstymas

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Verslo fonas ir paskirtis

Daugeliu atvejų gamintojai, mažmenininkai ir kiti tiekimo grandinės verslo savininkai turi iš anksto paskirstyti atsargas svarbiems pardavimo kanalams, vietų ar klientams ar konkretiems pardavimo įvykiams. Atsargų paskirstymas yra įprasta pardavimo veiklos planavimo proceso praktika, tai atliekama prieš įvykdant faktinę pardavimo veiklą ir sukūrus pardavimo užsakymą.

Pavyzdžiui, dviračio įmonė turi ribotas atsargas, galimas labai populiariausiai. Ši įmonė ir pardavimą internete, ir parduotuvėje. Kiekviename pardavimo kanale įmonė turi keletą svarbių įmonės partnerių (prekyviečių ir didelių mažmenininkų), kurie reikalauja, kad jiems būtų įrašyta konkreti galimų atsargų dalis. Todėl dviračio įmonė turi sugebėti suderinti atsargų paskirstymą kanaluose ir valdyti SAVO VIP partnerių lūkesčius. Geriausias būdas pasiekti abu tikslus yra naudoti atsargų paskirstymą, kad kiekvienas kanalas ir mažmenininkas galėtų gauti tam tikrus paskirstytus kiekius, kuriuos vėliau bus galima parduoti vartotojams.

Atsargų paskirstymas turi du pagrindinius verslo tikslus:

- **Atsargų apsauga (žiedinė)** – organizacijos nori iš anksto paskirstyti apribotas arba ribotas atsargas prioritetams nustatytiems kanalams, regionams, VIP klientams ir filialo įmonėms. Atsargų matomumo paskirstymo funkcijos tikslas yra apsaugoti paskirstytas atsargas, kad kiti paskirstymai, rezervavimai ar kiti pardavimo poreikiai nepaveiktų anksčiau paskirstytų atsargų.
- **Perteklinio pardavimo valdymas** – atsargų matomumo paskirstymo priemonė siekia apriboti anksčiau paskirstytus kiekius, kad gaunanti šalis (pvz., kanalas ar klientų grupė) nevartotų jų per daug, kai pradeda veikti faktinė pardavimo operacija, pagrįsta švelniu rezervavimu.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Paskirstymo aprašas atsargų matomumo paslaugoje

Nors atsargų matomumo paslaugos paskirstymo funkcija nenustato faktinių atsargų kiekių, ji nurodo turimus faktinių atsargų kiekius, *kad* būtų galima nustatyti pradinį turimų virtualiųjų telkinių kiekio paskirstymą. Atsargų paskirstymas pagal atsargų matomumą yra švelniai paskirstymas. Tai atliekama prieš įvykstant faktinėms pardavimo operacijoms ir nepriklauso nuo pardavimo užsakymų. Pavyzdžiui, galite paskirstyti atsargas svarbiausiems pardavimo kanalams arba stambiems įmonės mažmenininkams prieš galutiniams klientams apsilankant pardavimo kanale arba mažmeninės prekybos parduotuvėje, kad galėtų pirkti.

Skirtumas tarp atsargų paskirstymo ir atsargų soft [rezervavimo yra tas](inventory-visibility-reservations.md), kad švelniai rezervavimas paprastai susiejamas su faktinėmis pardavimo operacijomis (pardavimo užsakymo eilutės). Todėl jei norite naudoti paskirstymo ir soft rezervavimo priemones kartu, pirmiausia rekomenduojame atsargų paskirstymą atlikti, o tada iš dalies rezervuoti pagal paskirstytus kiekius. Daugiau informacijos rasite Naudojimo [kaip švelniai rezervavimas](#consume-to-soft-reserved).

Atsargų paskirstymo funkcija leidžia pardavimo planuotojams arba pagrindinių sąskaitų vadovams valdyti ir iš anksto paskirstyti svarbias paskirstymo grupių atsargas (pvz., kanalų, regionų ir klientų grupių). Taip pat ji palaiko suvartojimo pagal paskirstytus kiekius sekimą, koregavimą ir analizę, kad būtų galima papildyti arba perskirstyti laiku. Šis gebėjimas realiuoju laiku matyti matomumą paskirstymo, suvartojimo ir paskirstymo balanse, ypač svarbus greitos pardavimo arba akcijos įvykiams.

## <a name="terminology"></a>Terminologija

Šios sąlygos ir sampratos yra naudingos atsargų paskirstymo diskusijose:

- **Paskirstymo grupė** – grupė, kuri valdo paskirstymą, pvz., pardavimo kanalas, klientų grupė ar užsakymo tipas.
- **Paskirstymo grupės** vertė – kiekvienos paskirstymo grupės vertė. Pavyzdžiui, internetas *arba* *parduotuvė* gali būti pardavimo kanalo paskirstymo grupės vertė, *o VIP* *ar įprasta* – klientų paskirstymo grupės vertė.
- **Paskirstymo hierarchija** – A reiškia paskirstymo grupių jungtį hierarchiniu būdu. Pavyzdžiui, galite nurodyti kanalą kaip *1* hierarchijos lygį, *regioną* – 2 lygį, *o klientų grupę* – kaip 3 lygį. Paskirstant atsargas, reikia vadovautis paskirstymo hierarchijos seka, kai nurodote paskirstymo grupės vertę. Pavyzdžiui, jūs galite paskirstyti 200 raudonai *eilutėms* interneto kanalui, *Londono* regionui ir VIP *klientų* grupei.
- **Galima paskirstyti** – virtualusis *bendras telkinys*, nurodantis kiekį, kurį galima toliau paskirstyti. Apskaičiuotas matas, kurį galite laisvai nustatyti naudodami savo formulę. Jei naudojate ir soft reservation priemonę, rekomenduojame naudoti tą pačią formulę, norint apskaičiuoti turimas paskirstyti ir galimas rezervuoti.
- **Paskirstyta** – faktinis matas, rodantis paskirstytą paskirstymą, kurį gali suvartoti paskirstymo grupės.
- **Suvartota** – faktinis matas, nurodantis, kad kiekiai, suvartoti prieš pradinį paskirtą kiekį. Prie šio faktinio mato pridedami skaičiai, todėl automatiškai sumažinamas priskirtas faktinis matas.

Toliau pateikta iliustracija rodo atsargų paskirstymo verslo darbo eigą.

![Atsargų matomumo paskirstymo verslo darbo eiga.](media/inventory-visibility-allocation-flow.png "Atsargų matomumo paskirstymo verslo darbo eiga.")

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

Paskirstymo funkcijos konfigūravimo procesas turi du veiksmus:

- Nustatyti duomenų [šaltinį ir](inventory-visibility-configuration.md#data-source-configuration) jo [priemones](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Nustatykite paskirstymo grupės pavadinimą ir hierarchiją.

### <a name="predefined-data-source"></a>Iš anksto nustatytas duomenų šaltinis

Kai įgalinate paskirstymo priemonę ir iškiesite konfigūracijos atnaujinimo API, atsargų matomumas sukuria vieną iš anksto nustatytą duomenų šaltinį ir keletą pradinių priemonių.

Duomenų šaltinis pavadintas `@iv`.

Čia yra pradiniai faktiniai priemonės:

- `@iv`
  - `@allocated`
  - `@cumulative_allocated`
  - `@consumed`
  - `@cumulative_consumed`

Štai pradinių apskaičiuotų priemonių:

- `@iv`
  - `@iv.@available_to_allocate` = `??`– – `??``@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Įtraukti kitus faktinius matus į prieinamą paskirstyti apskaičiuotą matą

Norėdami naudoti paskirstymą, turite nustatyti skaičiuojamąjį matą, kurį galima paskirstyti (`@iv.@available_to_allocate`). Pavyzdžiui, turite duomenų `fno``onordered` šaltinį ir matą, `pos``inbound` duomenų šaltinį ir matą, taip pat norite atlikti turimos sumos ir `fno.onordered` kiekio paskirstymą `pos.inbound`. Šiuo atveju turėtų `@iv.@available_to_allocate` būti formulėje `pos.inbound``fno.onordered`. Čia pateikiamas pavyzdys:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

> [!NOTE]
> Duomenų šaltinis yra `@iv` iš anksto nustatytas duomenų šaltinis, o su prefiksu `@iv` apibrėžti faktiniai duomenys yra `@` iš anksto nustatyti duomenys. Šios priemonės yra iš anksto nustatyta paskirstymo funkcijos konfigūracija, todėl nekeiskite jų ar nenaikykite jų arba, tikėtina, kad įvyksta netikėtos klaidos naudojant paskirstymo funkciją.
>
> Galite pridėti naujų faktinių matų prie iš anksto apskaičiuoto matavimo `@iv.@available_to_allocate`, tačiau jo pavadinimo keisti negalima.

### <a name="change-the-allocation-group-name"></a>Paskirstymo grupės pavadinimo keitimas

Galima nustatyti daugiausiai aštuonis paskirstymo grupių pavadinimus. Grupėse yra hierarchija.

Nustatote grupių pavadinimus atsargų **matomumo energijos programos konfigūracijos** puslapyje. Norėdami atidaryti šį puslapį, savo aplinkoje Microsoft Dataverse atidarykite programą Atsargų matomumas ir pasirinkite Konfigūracijos **\> paskirstymas**.

Pvz., \[`channel``customerGroup` jei naudojate keturis grupių pavadinimus ir nustatote juos kaip, `region``orderType`\], šie pavadinimai tinkami su paskirstymu susijusioms užklausoms, kai iškiesite konfigūracijos atnaujinimo API.

### <a name="allocation-using-tips"></a>Paskirstymas naudojant patarimus

- Kiekvienam produktui paskirstymo funkcija turi naudoti tame *pačiame* dimensijų lygyje pagal produktų indeksų hierarchiją, kurią nustatėte produktų indeksų [hierarchijos konfigūracijoje](inventory-visibility-configuration.md#index-configuration). Pavyzdžiui, tarkime, kad jūsų indeksų hierarchija \[`Site` yra, `Location``Color`, . `Size`\] Jei dimensijų lygyje \[`Site` tam tikrą kiekį priskiriate vienam produktui, `Location``Color`\] kitą kartą, kai norite paskirstyti šį produktą, taip pat turėtumėte paskirstyti tame pačiame lygyje, \[`Site`,`Location``Color`\]. Jei naudojate lygį \[`Site`, (`Location` arba `Color`) `Size`\]\[`Site`, `Location`\] duomenys bus nesuderinami.
- Paskirstymo grupės pavadinimo keitimas neturės įtakos paslaugai įrašytims duomenims.
- Paskirstymas turi būti daromas, kai turimo produkto kiekis yra teigiamas.
- Norėdami paskirstyti produktus iš aukšto paskirstymo *lygio* grupės į pogrupį, naudokite `Reallocate` API. Pavyzdžiui, \[`channel` turite paskirstymo grupės hierarchiją,, `customerGroup``region`, `orderType`\] ir \[norite tam tikrą produktą paskirstyti iš paskirstymo grupės tinkle, VIP\] į subskirstyti \[grupę tinkle, VIP, EU\], `Reallocate` naudoti API kiekiui perkelti. Jei naudojate `Allocate` API, kiekis bus paskirstytas iš virtualiojo bendrojo telkinio.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a> Paskirstymo API naudojimas

Šiuo metu atidaromos penkios paskirstymo API:

- REGISTRUOTI / API / aplinką / paskirstymą{environmentId} / paskirstymą
- Registruoti / API / aplinką /{environmentId} paskirstymą / nepaskirstyti
- REGISTRUOTI / API / aplinką /{environmentId} paskirstymą / perskirstyti
- REGISTRUOTI / API / aplinką /{environmentId} paskirstymą / naudoti
- REGISTRUOTI / API / aplinką / paskirstymą{environmentId} / užklausą

#### <a name="allocate"></a>Paskirstyti

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
    "id": "???",
    "productId": "Bike",
    "groups": {
        "channel": "Online",
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

#### <a name="unallocate"></a>Nepaskirstyti

`Unallocate` Naudokite API operacijai `Allocate` atšaukti. Neigiamas kiekis operacijoje neleistinas `Allocate`. Kūno yra `Unallocate` identiškas .`Allocate`

#### <a name="reallocate"></a>Perskirstyti

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
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Online",
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

#### <a name="consume"></a>Naudoti

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
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
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

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Naudoti kaip švelniai rezervavimą

API `Consume` taip pat gali naudoti paskirstytą kiekį kaip soft rezervavimą. Tokiu atveju operacija sumažins `Consume` paskirstytą kiekį ir tada šį kiekį iš anksto rezervuos. Norėdami naudoti šį būdą, turite naudoti atsargų matomumo [funkciją](inventory-visibility-reservations.md) švelniai rezervavimo funkcija.

Pvz., nustatėte soft rezervavimo modifikatorių (matą) kaip `iv.softreserved`. Naudojama ši formulė, kurią naudojant galima rezervuoti apskaičiuojamasis matas:

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
        "channel": "Online",
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

#### <a name="query"></a>Užklausa

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
        "channel": "Online",
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
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
