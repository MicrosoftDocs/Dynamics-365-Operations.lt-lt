---
title: Kategorijų užklausos iš tiekėjų
description: Šiame straipsnyje aprašoma, kaip tiekėjai gali prašyti įsigijimo kategorijų pagal savo sąskaitą. Taip pat aprašomas patvirtinimo procesas, kurį užbaigta įsigijimo agentų.
author: GalynaFedorova
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8deded1b7f908bcadf705cf992b2d97618bc28b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863889"
---
# <a name="category-requests-from-vendors"></a>Kategorijų užklausos iš tiekėjų

[!include [banner](../includes/banner.md)]

Kategorijos užklausos procesas leidžia tiekėjams susieti naujas įsigijimo kategorijas su jų sąskaita. Tada šias įsigijimo kategorijas galima naudoti susijusiuose įsigijimo ir pirkimo procesuose. (Išsamesnės informacijos žr. [Aprūpinimo katalogų peržiūra](procurement-catalogs.md).)

Kategorijos užklausas inicijuoja tiekėjai Tiekėjo **informacijos darbo** srityje. Tada jos bus pateiktos jūsų institucijai peržiūrėti ir patvirtinti. Patvirtintos kategorijos yra įtraukiami į tiekėjo sąskaitos įsigijimo kategorijų sąrašą.

## <a name="turn-the-category-requests-from-vendors-feature-on-or-off"></a>Įjungti arba išjungti kategorijų užklausas iš tiekėjų funkcijos

Kaip ir tiekimo grandinės valdymo versija 10.0.25 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali įjungti arba išjungti šią funkciją *ieškodami leisti tiekėjams taikyti įsigijimo kategorijoms*[naudojant tiekėjų bendradarbiavimo funkciją funkcijų valdymo darbo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.

Jei ši funkcija įjungta, vis dar galite rankiniu būdu įtraukti įsigijimo kategorijas į tiekėjų sąskaitas. Dėl išsamesnės informacijos, žr. [Konkrečių įsigijimo kategorijų tiekėjų tvirtinimas](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Tiekėjo bendradarbiavimo reikalavimai

Kad tiekėjas galėtų sąveikauti su kategorijos užklausomis, jis turi būti nustatytas tiekėjo bendradarbiavimo srityje.

Tiekėjas turi turėti bent vieną tiekėjo bendradarbiavimo vartotoją. Tik tiekėjų vartotojai, kuriems priklauso *tiekėjo administratoriaus (išorinis)* saugos vaidmuo, gali kurti ir pateikti kategorijos užklausas.

Daugiau informacijos žr. [Tiekėjo bendradarbiavimo nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Tiekėjo kategorijos užklausos darbo srauto nustatymas

Tiekėjo *kategorijos užklausos darbo eiga turi būti nustatyta įsigijimo ir gavimo darbo* eigose. Tiekėjai pateiks naujas kategorijos užklausas, kurias galėsite peržiūrėti ir patvirtinti. Pageidaujamos įsigijimo kategorijos bus pridėtos prie tiekėjo sąskaitos patvirtinus kategorijos užklausą.

Toliau pateikiamas pavyzdys, kaip nustatyti paprastą tiekėjo kategorijos užklausos darbo *eigą*, kurioje yra vienas tvirtintojas. Norėdami nustatyti tinkamą savo agentūros darbo eigos nustatymą, turite peržiūrėti vidinius procesus.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo darbo srautai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange pasirinkite Tiekėjo kategorijos užklausos darbo **eigą, kad atidarytumėte** darbo eigos rengyklę.
1. Prisiregistruokite prie darbo eigos rengyklės.
1. Veiksmų srityje pasirinkite **Ypatybės**.
1. Darbo **eigos** ypatybės puslapio pateikimo instrukcijų lauke įveskite **instrukcijos** tekstą. Instrukcijos bus matomos tiekėjams, kai jie pateikia kategorijos užklausą.
1. Uždarykite **Ypatybių** puslapį.
1. Nuvilkite **naują kategorijos užklausos darbo eigos elementą Patvirtinti į** rėmą.
1. Nuvilkite saitą iš darbo **eigos elemento Pradėti į Tvirtinti naują kategorijos užklausos darbo eigos** **elementą**.
1. Nuvilkite saitą iš darbo **eigos elemento Pradėti į Tvirtinti naują kategorijos užklausos** **Galutinės** darbo eigos elementui.
1. Dukart spustelėkite (arba du kartus spustelėkite) naujos **kategorijos užklausos darbo eigos elemento** patvirtinimas.
1. Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) **1 veiksmo** darbo eigos elementą, tada pasirinkite **Ypatybės**.
1. Darbo **eigos** elemento puslapio pateikimo instrukcijų lauke įveskite **Darbo elemento temos** tekstą. Šis tekstas bus rodomas kaip man priskirto darbo elementų puslapio **lauko** Tema **vertė**.
1. Lauke **Darbo elemento instrukcijos** įveskite instrukcijos tekstą. Kategorijos užklausos veiksmų srityje pasirinkus Darbo **eigą** instrukcijos bus matomos tvirtintojams.
1. Kairiojoje srityje pasirinkite **Priskyrimas**.
1. Skirtuke **Priskyrimo** tipas nustatykite Priskirti vartotojus šiam darbo eigos **elementui** *vartotojui*.
1. Skirtuko **Vartotojas** sąraše Galimi vartotojai **pasirinkite** tvirtintoją. Pavyzdžiui, įsigijimo skyriuje pasirinkite vartotoją.
1. Rinkitės dešinįjį rodyklės mygtuką (**\>**) norėdami perkelti patvirtinimo įrankį į **Pasirinktų vartotojų** sąrašą.
1. Uždarykite **Ypatybių** puslapį.
1. Pasirinkite **Įrašyti ir uždaryti**.
1. Lauke **Versijos pastabos** įveskite pastabas apie darbo eigą.
1. Norėdami įrašyti darbo eigą, pasirinkite **Gerai**.
1. Jei esate pasiruošę pradėti tikrinti darbo eigą, pasirinkite **Suaktyvinti naują** versiją. Priešingu atveju, **pasirinkite Neaktyvinti naujos** versijos.
1. Norėdami užbaigti darbo eigos nustatymus, pasirinkite **Gerai**.

> [!TIP]
> Jei jūsų institucijai nereikia patvirtinti kategorijos užklausų, turėtumėte konfigūruoti darbo eigą automatiniam patvirtinimui.

Dėl daugiau informacijos apie tai, kaip nustatyti darbo eigas, žr. [Darbo eigos sistemos apžvalga](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Kategorijos užklausos kūrimas ir pateikimo

Šiame skyriuje aprašoma, kaip tiekėjai gali naudoti tiekėjo informacijos darbo sritį kategorijų **užklausoms** kurti, redaguoti, peržiūrėti ir pateikti.

### <a name="start-a-new-request"></a>Pradėti naują užklausą

Norėdami pradėti naują kategorijos užklausą, atlikite šiuos veiksmus.

1. Tiekėjo **informacijos darbo** srityje pasirinkite kategorijos **užklausų išklotinę** vietą.
1. Veiksmų **srities puslapyje** Kategorijos užklausos pasirinkite Nauja **kategorijos** užklausa.
1. Naujos kategorijos užklausos dialogo lange suraskite kategoriją, dėl kurios norite taikyti, naršymą medyje ir (arba) naudodami filtrą sąrašo **viršuje**. Pažymėkite kiekvienos susijusios kategorijos žymės langelį.

    Atkreipkite dėmesį į toliau nurodytus punktus.

    - Kategorijos, šiuo metu aktyvios jūsų tiekėjo sąskaitoje, rodomos kaip pasirinktos ir jų pašalinti negalima.
    - Vienoje kategorijos užklausoje galite prašyti kelių įsigijimo kategorijų.

1. Pasirinkite **Gerai**, kad sukurtumėte užklausos šabloną.

    Nauja juodraščio užklausa dabar rodoma **kategorijos užklausų** puslapyje.

1. Atidaryti naują juodraščio užklausą, kad ją būtų galima peržiūrėti ir redaguoti, jei reikia.

    - Norėdami peržiūrėti kategorijų, kurios šiuo metu įtrauktos į užklausą, sąrašą, pasirinkite **pageidaujamų kategorijų** „FastTab".
    - Norėdami peržiūrėti aktyvias kategorijas, puslapio **dešinėje atidarykite** aktyvių kategorijų „FactBox".
    - Norėdami į užklausą įtraukti **kategoriją**, „FastTab" Pageidaujamos kategorijos įrankių **juostoje pasirinkite** Įtraukti.
    - Norėdami pašalinti kategoriją iš užklausos, pasirinkite kategoriją **pageidaujamose** kategorijose „FastTab", tada įrankių **juostoje** pasirinkite Pašalinti.
    - Norėdami prie užklausos pridėti dokumentą, **veiksmų** srityje pasirinkite Priedus. Pridėti dokumentai bus galimi tvirtintojams, kai jie peržiūrės kategorijos užklausą.
    - Norėdami pašalinti pridėtą dokumentą iš užklausos, **veiksmų** srityje pasirinkite Priedus. Pasirinkite pašalinamą dokumentą, o tada veiksmų srityje pasirinkite **Naikinti**.

1. Jei esate pasiruošę pateikti užklausą, veiksmų **srityje** pasirinkite Pateikti. Kitu atveju tiesiog uždarykite puslapį ir praleiskite likusius šios procedūros veiksmus. Tada galėsite vėliau grįžti į užklausą.
1. Perskaitykite visas pasirodančių pateikimo instrukcijas ir pasirinkite **Pateikti**.
1. Laukelyje **Komentarai**, įveskite visą papildomą informaciją, kurią reikia turėti apie produktą. Tada rinkitės **Pateikti** tam, kad užbaigtumėte užklausą.

### <a name="edit-a-draft-or-recalled-request"></a>Redaguoti juodraštį arba atšauktas užklausą

Norėdami redaguoti juodraštį arba atšaukti kategorijos užklausą, atlikite šiuos veiksmus.

1. Tiekėjo **informacijos darbo** srityje pasirinkite kategorijos **užklausų išklotinę** vietą.
1. Pasirinkite juodraštį arba atšaukite užklausą, kad jį atidarytumėte.
1. Jei reikia, redaguokite prašymą ir uždarykite jį arba pateikite, kaip aprašyta ankstesnėje procedūroje.

### <a name="submit-a-draft-or-recalled-request"></a>Pateikti juodraštį arba atšauktas užklausą

Norėdami pateikti juodraštį arba atšaukti kategorijos užklausą, atlikite šiuos veiksmus.

1. Tiekėjo **informacijos darbo** srityje pasirinkite kategorijos **užklausų išklotinę** vietą.
1. Pasirinkite juodraštį arba atšaukite užklausą, kurią norite pateikti.
1. Veiksmų srityje pasirinkite **Pateikti**.
1. Perskaitykite visas pasirodančių pateikimo instrukcijas ir pasirinkite **Pateikti**.
1. Laukelyje **Komentarai**, įveskite visą papildomą informaciją, kurią reikia turėti apie produktą. Tada rinkitės **Pateikti** tam, kad užbaigtumėte užklausą.

    Kategorijos užklausos būsena pakeičiama viena iš šių verčių:

    - _Laukiama peržiūros_ – užklausa peržiūrima darbo eigoje.
    - _Laukiama patvirtinimo_ – reikia patvirtinimo.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Atšaukti dar nepatvirt pateiktą užklausą

Norėdami atšaukti pateiktą, bet dar patvirtintą kategorijos užklausą, atlikite šiuos veiksmus.

1. Tiekėjo **informacijos darbo** srityje pasirinkite kategorijos **užklausų išklotinę** vietą.
1. Pasirinkite laukiančią užklausą, kurią norite atšaukti.
1. Veiksmų srityje pasirinkite **Atšaukti**.
1. Laukelyje **Įvesti komentarą**, įveskite visą papildomą informaciją, kurią reikia turėti apie produktą. Tada rinkitės **Pateikti** tam, kad užbaigtumėte užklausą.

    Užklausos kategorijos būsena pakeičiama į _Atšaukta_. Užklausa išlieka tokia, kol ją panaikinsite arba dar kartą pateikiate.

### <a name="delete-a-draft-or-recalled-request"></a>Naikinti juodraštį arba atšauktas užklausą

Norėdami naikinti juodraštį arba atšaukti kategorijos užklausą, atlikite šiuos veiksmus.

1. Tiekėjo **informacijos darbo** srityje pasirinkite kategorijos **užklausų išklotinę** vietą.
1. Pasirinkite juodraštį arba atšaukite užklausą, kurią norite naikinti.
1. Rinkitės **Naikinti** veiksmų juostoje.
1. Norėdami patvirtinti sunaikinimo operaciją, pasirinkite **Taip**.

### <a name="view-completed-requests"></a>Peržiūrėti baigtas užklausas

Norėdami peržiūrėti baigtas užklausas, atidarykite **tiekėjo informacijos darbo sritį ir pasirinkite kategorijos** užklausų **išklotinę** sritį. Baigtos kategorijos užklausos bus vienos iš šių būsenų:

- _Patvirtinta_ - Prašymas buvo patvirtintas. Norėdami peržiūrėti naujai įtrauktas kategorijas, grįžkite prie tiekėjo informacijos darbo srities, kairiojoje srityje atidarykite išplečiamąjį sąrašą Daugiau **informacijos** ir **pasirinkite** **Kategorijos**.
- Atmesta – užklausa buvo atmesta. Jei reikia, galite sukurti naują kategorijos užklausą.

## <a name="review-category-requests"></a>Peržiūrėti kategorijos užklausas

Šiame skyriuje paaiškinama, kaip patvirtinti, atmesti ir perduoti kategorijos užklausas, kurias pateikė tiekėjai, ir kaip peržiūrėti baigtas užklausas. Šie darbo eigos veiksmai skirti visai kategorijos užklausai.

### <a name="view-category-requests"></a>Peržiūrėti kategorijos užklausas

Norėdami peržiūrėti užklausas, atlikite šiuos veiksmus.

1. Eikite **į įsigijimo ir gavimo \> tiekėjams tiekėjo \> bendradarbiavimo užklausas \> kategorijos užklausas**.

    Rodomas **puslapis Kategorijos** užklausos. Numatytasis puslapio rodinys rodo kategorijos užklausas, kurių būsena yra *Laukiantis* veiksmas.

1. Norėdami peržiūrėti visas užklausas, *pasirinkite Visi lauke Rodyti* **užklausas**.
1. Atidaryti naują juodraščio užklausą, kad ją būtų galima peržiūrėti ir redaguoti, jei reikia.

    - Norėdami peržiūrėti kategorijų, kurios šiuo metu įtrauktos į užklausą, sąrašą, pasirinkite **pageidaujamų kategorijų** „FastTab".
    - Norėdami peržiūrėti aktyvias kategorijas, puslapio **dešinėje atidarykite** aktyvių kategorijų „FactBox".
    - Jei dokumentai buvo pateikti, **veiksmų** srities priedų (popieriaus įrašų) mygtukas rodo pridėtų dokumentų skaičių. Norėdami peržiūrėti pridėtus dokumentus, **pasirinkite** mygtuką Priedai. Tada pasirinkite dokumentą, kurį norite peržiūrėti ir **pasirinkite** Atidaryti, kad jį būtų galima peržiūrėti.
    - Norėdami prie užklausos pridėti dokumentą, **veiksmų** srityje pasirinkite Priedus. Pridėti dokumentai bus galimi tvirtintojams, kai jie peržiūrės kategorijos užklausą.
    - Norėdami pašalinti pridėtą dokumentą iš užklausos, **veiksmų** srityje pasirinkite Priedus. Pasirinkite pašalinamą dokumentą, o tada veiksmų srityje pasirinkite **Naikinti**.
    - Norėdami peržiūrėti darbo eigos istoriją, rinkitės **Darbo eiga** veiksmų juostoje. Darbo eigos pasirinktyse pasirinkite Daugiau **ir tada Darbo eigos** **retrospektyva**. Rodomas **darbo eigos** retrospektyvos puslapis.

### <a name="approve-a-pending-category-request"></a>Tvirtinti laukiamą kategorijos užklausą

Norėdami patvirtinti laukiančią kategorijos užklausą, atlikite šiuos veiksmus.

1. Eikite **į įsigijimo ir gavimo \> tiekėjams tiekėjo \> bendradarbiavimo užklausas \> kategorijos užklausas**.
1. Pasirinkti laukiančią patvirtinti užklausą.
1. Peržiūrėti kategorijos užklausą.
1. Pasirinktinai: **bendrajame** „FastTab" priežasties **kodo lauke pasirinkite priežasties** kodą. Tada lauke **Priežasties** komentaras įveskite komentarą apie priežasties kodą.
1. Veiksmų srityje pasirinkite **Darbo eiga**.
1. Darbo eigos pasirinktyse pasirinkite **Patvirtinti**.
1. Laukelyje **Komentaras**, įveskite visą papildomą informaciją, kurią reikia turėti apie produktą. Tada rinkitės **Tvirtinti** tam, kad užbaigtumėte užklausą.

    Kategorijos užklausos būsena pakeičiama į _Patvirtinta_, o įsigijimo kategorijos įtraukiami į tiekėjo sąskaitą.

### <a name="reject-a-pending-category-request"></a>Atmesti laukiamą kategorijos užklausą

Norėdami atmesti laukiančią kategorijos užklausą, atlikite šiuos veiksmus.

1. Eikite **į įsigijimo ir gavimo \> tiekėjams tiekėjo \> bendradarbiavimo užklausas \> kategorijos užklausas**.
1. Atmesti laukiančią patvirtinti užklausą.
1. Peržiūrėti kategorijos užklausą.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Pasirinktinai: **bendrajame** „FastTab" priežasties **kodo lauke pasirinkite priežasties** kodą. Tada lauke **Priežasties** komentaras įveskite komentarą apie priežasties kodą.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Darbo eiga**.
1. Darbo eigos pasirinktyse pasirinkite Daugiau **ir tada Darbo eigos** **Atmesti**.
1. Laukelyje **Komentaras**, įveskite visą papildomą informaciją, kurią reikia turėti apie produktą. Tada rinkitės **Atmesti** tam, kad užbaigtumėte užklausą.

    Užklausos kategorijos būsena pakeičiama į _Atmesta_. Šiuo metu tiekėjas gali sukurti naują kategorijos užklausą, kurios reikia.

### <a name="delegate-a-pending-category-request"></a>Perleisti laukiamą kategorijos užklausą

Norėdami perduoti laukiančią kategorijos užklausą kitam vartotojui, atlikite šiuos veiksmus.

1. Eikite **į įsigijimo ir gavimo \> tiekėjams tiekėjo \> bendradarbiavimo užklausas \> kategorijos užklausas**.
1. Pasirinkite laukiančią užklausą, kurią norite patvirtinti.
1. Veiksmų srityje pasirinkite **Darbo eiga**.
1. Darbo eigos pasirinktyse pasirinkite Daugiau **ir tada Darbo eigos** **Perduoti**.
1. Lauke **Vartotojas** pasirinkite vartotoją, kuriam priskirti kategorijos užklausą, kad ji būtų peržiūrėta.
1. Laukelyje **Komentaras**, įveskite visą papildomą informaciją, kurią reikia turėti apie produktą.
1. Rinkitės **Perduoti** norėdami užbaigti perdavimą. Dabar pasirinktas vartotojas gali peržiūrėti kategorijos užklausą.

### <a name="view-procurement-categories-for-a-vendor"></a>Peržiūrėti tiekėjo įsigijimo kategorijas

Norėdami peržiūrėti aprūpinimo kategorijas tiekėjui po kategorijos užklausos patvirtinimo, atlikite šiuos žingsnius.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**.
1. Puslapyje **Visi tiekėjai** pasirinkite tiekėją, kurio įsigijimo kategorijas norite peržiūrėti.
1. Veiksmų srityje atidarykite skirtuką **Bendri** ir grupėje **Nustatymas** pasirinkite **Kategorijos**.

    Rodomas **Kategorijos** Vieneto tekstai. **Įsigijimo** „FastTab" rodomos įsigijimo kategorijos, kurios buvo pridėtos pagal kategorijos užklausą.

1. Jei **reikia**, įsigijimo „FastTab" galite atlikti pakeitimus. Pavyzdžiui, galite nustatyti tiekėjo **kategorijos būsenos** lauką kaip _Pageidaujamą_.
