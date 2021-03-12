---
title: Sandėlio procesų kokybės valdymas
description: Šioje temoje pateikta informacija apie funkciją „Sandėlio procesų kokybės valdymas“. Ši priemonė išplečia kokybės valdymo galimybes ir leidžia vartotojams integruoti prekių pavyzdžių ėmimo valdiklius į sandėlio gavimo procesą, naudojant patobulintą sandėlio valdymą.
author: Henrikan
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: fd6b4b0c30a8a4cb36955e9b131c937c4db80772
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983730"
---
# <a name="quality-management-for-warehouse-processes"></a>Sandėlio procesų kokybės valdymas

Funkcija _Sandėlio procesų kokybės valdymas_ leidžia integruoti prekių pavyzdžių ėmimo valdiklius į sandėlio gavimo procesą, naudojant patobulintą sandėlio valdymą. Sandėlio darbas gali būti automatiškai sugeneruotas, kad būtų galima perkelti atsargas į kokybės kontrolės vietą pagal procentinę dalį arba fiksuotą kiekį, arba pagal kiekvieną *n*-tąją numerio lentelę. Atlikus kokybės užsakymą, darbas gali būti automatiškai sugeneruotas, kad būtų galima perkelti atsargas į kitą proceso vietą, atsižvelgiant į kokybės rezultatus.

Funkcija _Sandėlio procesų kokybės valdymas_ išplečia pagrindinės kokybės valdymo funkcijos galimybes. Ji suteikia galimybę kurti atsargų, siunčiamų į kokybės kontrolės vietą, kokybės užsakymus, nors kokybės užsakymai ne visada reikalingi. Todėl jis leidžia atlikti lengvą, sandėlio darbu pagrįstą kokybės kontrolės procesą.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Įjungti funkciją „Sandėlio procesų kokybės valdymas“

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Sandėlio procesų kokybės valdymas*

## <a name="key-benefits"></a>Pagrindiniai privalumai

Funkcija _Sandėlio procesų kokybės valdymas_ automatiškai sugeneruoja darbą kaip gavimo proceso dalį, kad būtų galima perkelti kokybės kontrolei reikiamą atsargų kiekį į kokybės kontrolės vietą. Jei gautas kiekis viršija kiekį, kuris reikalingas kokybės kontrolei (pagal prekių pavyzdžių ėmimo nustatymą), perviršis perkeliamas į gavimo vietą, kuri apibrėžta vietos nurodymo sąrankoje. Patikrinus kokybės užsakymą, darbas automatiškai sugeneruojamas taip, kad kokybės užsakymo kiekis būtų perkeltas į naują gavimo arba grąžinimo vietą, atsižvelgiant į tikrinimo rezultatą ir vietos nurodymo sąranką. Darbo, kuriame yra tik toks kiekis, kurį reikia perkelti į kokybės kontrolę ir iš jos, automatinis generavimas suteikia integruoto proceso patirtį.

> [!NOTE]
> Kai funkcija _Sandėlio procesų kokybės valdymas_ įjungta, vis tiek galite naudotis neautomatiniu procesu. Atliekant neautomatinį procesą, atsargų perkėlimas ir perkėlimas pagal šabloną yra naudojami tam, kad sandėlio darbuotojas suaktyvintų sandėlio darbo kūrimą, kad atsargos būtų perkeltos iš kokybės kontrolės vietos į naują vietą. Taip pat galite nustatyti gavimo vietos nurodymą, pagal kurį visos atsargos bus perkeltos iš gavimo vietos į kokybės kontrolės vietą, neatsižvelgiant į prekių pavyzdžių ėmimo nustatymą.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kokybės valdymas ir funkcija „Sandėlio procesų kokybės valdymas“

Kai funkcija _Sandėlio procesų kokybės valdymas_ įjungta, ji pakeičia pagrindinių sandėlio valdymo ir kokybės valdymo objektų nustatymą. Tolesnėje iliustracijoje pateikiama objektų, įgalinančių sandėlio procesų kokybės užsakymus, apžvalga. Skliaustuose esantis tekstas nurodo siūlomus veiksmus, kai kokybės valdymas buvo taikytas prieš įjungiant funkciją _Sandėlio procesų kokybės valdymas_.

![Kokybės valdymo objektai](media/quality-management-entity-diagram.png "Kokybės valdymo objektai")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Įgalinimo priemonės: tipai „Kokybės prekių pavyzdžių ėmimas“ ir „Kokybės užsakymo darbo užsakymas“

Funkcija _Sandėlio procesų kokybės valdymas_ pristato du darbo užsakymų tipus, kurie įgalina darbo kūrimo procesą.

- **Kokybės prekių pavyzdžių ėmimas** – šis darbo užsakymo tipas naudojamas kuriant darbą, kuris perkelia užregistruotas atsargas į kokybės kontrolę.
- **Kokybės užsakymas** – šis darbo užsakymo tipas naudojamas kuriant darbą, kuris perkelia atsargas iš kokybės kontrolės į naują vietą, atsižvelgiant į vietos nurodymo sąranką.

### <a name="work-classes-location-directives-and-work-templates"></a>Darbų klasės, vietų nurodymai ir darbų šablonai

Darbo užsakymų tipai _Kokybės prekių pavyzdžių ėmimas_ ir _Kokybės užsakymas_ naudojami vietų nurodymuose, darbų klasėse ir darbų šablonuose.

Prieš tai, kai sandėlio darbas gali būti automatiškai sugeneruotas, kad atsargos būtų perkeltos į kokybės kontrolę, turite atlikti toliau nurodytus veiksmus, kad nustatytumėte savo sistemą.

1. Sukurkite atskiras darbų klases darbo užsakymų tipams _Kokybės prekių pavyzdžių ėmimas_ ir _Kokybės užsakymas_. Taip užtikrinsite, kad pagal šiuos du darbo užsakymų tipus būtų galima automatiškai sukurti tinkamas darbo užduotis ir jas vykdyti naudojant „Warehousing“ programą.
1. Nustatykite kiekvieno darbo užsakymo tipo darbo šabloną.

    - Nustatykite darbo šabloną, kuris naudoja darbo užsakymo tipą _Kokybės prekių pavyzdžių ėmimas_, kad automatiškai perkeltų užregistruotas atsargas į kokybės kontrolės vietą.
    - Nustatykite darbo šabloną, kuris naudoja darbo užsakymo tipą _Kokybės užsakymas_, kad perkeltų atsargas iš kokybės kontrolės vietos po kokybės kontrolės užbaigimo.

1. Kiekvienam darbo užsakymo tipui nustatykite vietų nurodymus, taikančius tinkamas kokybės kontrolės vietas, į kurias turi būti perkeltos atsargos. Užbaigus kokybės kontrolę, darbo užsakymo tipo _Kokybės užsakymas_ vietos nurodymas užtikrina, kad bus pasirinkta nauja paskirties vieta, kad atsargas būtų galima perkelti iš kokybės kontrolės vietos.
1. Nustatykite atitinkamus mobiliojo įrenginio meniu elementus, kurie palaikys gautų atsargų perkėlimą į kokybės kontrolės vietą, o atsargų, kurios pereina kokybės kontrolę arba jos nepereina, perkėlimą iš kokybės kontrolės vietos į naują vietą.

Nuoseklų pavyzdį, kuriame parodyta, kaip atlikti šį nustatymą, rasite [pavyzdiniame scenarijuje](#example-scenario) šios temos pabaigoje.

## <a name="enable-a-warehouse-for-quality-management"></a>Sandėlio įgalinimas kokybės valdymui

Prieš tai, kai funkcija _Sandėlio procesų kokybės valdymas_ galės būti pritaikyta konkrečiam sandėliui, turite atlikti toliau nurodytus veiksmus, kad funkciją būtų galima naudoti tam sandėliui.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. Pasirinkite sandėlį, kad būtų galima įgalinti kokybės valdymą.
1. „FastTab“ konteineryje **Sandėlis** parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmę nustatykite kaip _Taip_. (Atkreipkite dėmesį, kad šią parinktį galima nustatyti kaip _Taip_ tik tiems sandėliams, kuriuose naudojami sandėlio valdymo procesai.)

Kai parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmė nustatyta kaip _Taip_, kokybės susiejimo nustatymas kontroliuoja, ar pasirinktam sandėliui iš tiesų taikoma funkcija _Sandėlio procesų kokybės valdymas_. Parinkties reikšmę į _Ne_ galite pakeisti bet kuriuo metu. Tokiu atveju funkcija nebebus taikoma sandėliui, neatsižvelgiant į kokybės susiejimo nustatymą.

## <a name="quality-control"></a>Kokybės kontrolė

Funkcija _Sandėlio procesų kokybės valdymas_ valdo kelis pagrindinius kokybės susiejimų ir prekių pavyzdžių ėmimo parametrus.

### <a name="quality-associations"></a>Kokybės susiejimai

Kiekvienas [kokybės susiejimo įrašas](enable-quality-management.md) apibrėžia bandymų rinkinį, priimtiną kokybės lygį (AQL) ir pavyzdžių ėmimo planą, kuris taikomas sugeneruotiems kokybės užsakymams. Norėdami nustatyti kokybės susiejimo įrašą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Kokybės susiejimai**.
1. Kurkite arba pasirinkite prekės ar grupės, su kuria dirbate, arba visų prekių kokybės susiejimo įrašą.
1. „FastTab“ konteineryje **Sąlygos** lauke **Taikomas sandėlio tipas** nustatykite vieną iš toliau nurodytų reikšmių.

    - **Tik sandėlio procesų kokybės valdymas** – suaktyvinkite funkciją _Sandėlio procesų kokybės valdymas_. Šią reikšmę galite pasirinkti tik tuo atveju, jei nuorodos tipas yra *Pirkimas* arba *Gamyba*.
    - **Visi** – išjunkite funkciją _Sandėlio procesų kokybės valdymas_. Pasirinkite šią reikšmę visiems nuorodų tipams, išskyrus *Pirkimas* ir *Gamyba*.

> [!NOTE]
> Funkcija _Sandėlio procesų kokybės valdymas_ veikia tik tada, jei šaltinio dokumento eilutėje nurodytai prekei naudojami patobulinti sandėlio valdymo procesai ir jei šaltinio dokumento eilutėje esančiam sandėliui parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmė yra nustatyta kaip _Taip_.

Kiekviena prekė yra užregistruota (arba paskelbta kaip baigta), todėl sistema nustato, kurie kokybės susiejimai jai taikomi.

Kai funkcija _Sandėlio procesų kokybės valdymas_ įjungta, taikomas sandėlio tipas logiškai įterpiamas į ketvirtąją kokybės susiejimo ieškos hierarchijos ieškos grupę. Tolesnėje lentelėje pateikiama loginis ieškos hierarchijos vaizdas.

| Ieškos grupė | aprašymas |
|---|---|
| 1 grupė | Kiekvienam kokybės susiejimui patikrinkite laukų **Nuorodos tipas**, **Įvykio tipą** ir **Vykdymo atitikmuo** reikšmes pagal prekę. Jei yra atitikmuo su šaltinio dokumento eilute, perkelkite į 2 grupę. |
| 2 grupė | Kiekvienam kokybės susiejimui patikrinkite lauko **Prekės kodas** reikšmę (_Lentelė_, _Grupė_ arba _Visi_) pagal prekę. Reikšmė _Lentelė_ yra labiau apibrėžta nei _Grupė_, o reikšmė _Grupė_ yra labiau apibrėžta nei _Visi_. Jei yra atitiktis su reikšme _Lentelė_ (konkreti prekė), perkelkite į 3 grupę. Jei atitikties su reikšme _Lentelė_ nėra, ieškokite atitikties reikšmei _Grupė_. Jeigu nėra atitikties reikšmei _Grupė_, taikoma _Visi_. Jei atitiktis yra, perkelkite į 3 grupę. |
| 3 grupė | Kiekvienam kokybės susiejimui patikrinkite laukų **Sąskaitos kodas** ir **Ištekliaus kodas** reikšmes pagal prekę. Pritaikyta logika panaši į logiką, kuri taikoma reikšmei **Prekės kodas**. |
| 4 grupė | Kiekvienam kokybės susiejimui patikrinkite lauko **Taikomas sandėlio tipas** reikšmę (_Tik sandėlio procesų kokybės valdymas_ arba _Visi_) pagal prekę. Jei šaltinio dokumente esančio sandėlio parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmė yra nustatyta kaip _Taip_, o šaltinio dokumento eilutėje nurodyta prekė yra nustatyta kaip _Naudoti sandėlio valdymo procesus_, abu susiejimai, kai yra atitiktis _Tik sandėlio procesų kokybės valdymas_, ir susiejimai, kai yra atitiktis _Visi_, taikomi lygiagrečiai, jei abu yra. Jei šaltinio dokumente esančiam sandėliui parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmė yra nustatyta kaip _Ne_, o šaltinio dokumento eilutėje nurodyta prekė nustatyta kaip _Naudoti sandėlio valdymo procesus_, bus taikomas tik kokybės valdymas. |

Pavyzdžiui, jūs nurodėte sandėlį, kur parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmė yra nustatyta kaip _Taip_, ir turite du kokybės susiejimus, kurie apibrėžti nuorodos tipui *Pirkimas*: vienas skirtas visoms prekėms ir vienas įvykio tipui *Registracija*. Vienintelis skirtumas tarp dviejų kokybės susiejimų yra lauko **Taikomas sandėlio tipas** reikšmė: vienam kokybės susiejimui ji nustatyta kaip _Visi_, o kitam – kaip _Tik sandėlio procesų kokybės valdymas_. Šiuo atveju abu kokybės susiejimai yra vienodai apibrėžti ir bus taikomi abu.

Kokybės susiejimų lauko **Bandymų grupė** reikšmė taip pat yra veiksnys. Šis laukas apibrėžia bandymo procedūrą, kuri turi būti taikoma. Jei lauko **Bandymų grupė** reikšmė yra tokia pati abiems susiejimams, bus sukurtas tik vienas kokybės užsakymas – kokybės susiejimui, kur lauko **Taikomas sandėlio tipas** reikšmė yra _Tik sandėlio procesų kokybės valdymas_. Jei abiejų susiejimų lauko **Bandymų grupė** reikšmė nėra vienoda, bus sukurti du kokybės užsakymai. Pirmasis kokybės užsakymas bus sukurtas kokybės susiejimui, kur lauko **Taikomas sandėlio tipas** reikšmė yra _Tik sandėlio procesų kokybės valdymas_. Antrasis kokybės užsakymas bus sukurtas kokybės susiejimui, kur lauko **Taikomas sandėlio tipas** reikšmė yra _Visi_.

> [!NOTE]
> Lauko _Tik sandėlio procesų kokybės valdymas_ reikšmė laikoma labiau apibrėžta už _Visi_, kai sutampa 1 ir 2 grupių kokybės susiejimų kriterijai ir bandymų grupė. Du kokybės užsakymai bus sukruti tik tada, kai bandymų grupės skirsis.

#### <a name="reference-types"></a>Nuorodų tipai

Kai lauko **Nuorodos tipas** reikšmė yra _Pirkimas_, o lauko **Taikomas sandėlio tipas** reikšmė yra _Tik sandėlio procesų kokybės valdymas_, lauko **Įvykio tipas**, esančio „FastTab“ konteineryje **Procesas**, reikšmė turi būti nustatyta kaip _Registracija_. _Registracija_ yra vienintelis palaikomas įvykio tipas nuorodos tipui _Pirkimas_, kai naudojate funkciją _Sandėlio procesų kokybės valdymas_.

#### <a name="quality-processing-policy"></a>Kokybės apdorojimo strategija

Funkcija _Sandėlio procesų kokybės valdymas_ leidžia sukurti darbą, pagrįstą tik prekių pavyzdžių ėmimu. Todėl ji sudaro galimybę lengvam procesui. Sukurto darbo atsargos priklauso nuo prekių pavyzdžių ėmimo, kuris yra susietas su kokybės susiejimu. Kai naudojamas lengvas procesas, darbuotojui pateikus kiekį į kokybės kontrolės vietą, kokybės padalinys gali neautomatiniu būdu sukurti kokybės užsakymą, jei jis yra reikalingas.

Laukas **Kokybės apdorojimo strategija**, esantis „FastTab“ konteineryje **Kokybės užsakymo procesas**, kontroliuoja, ar sukūrus darbą taip pat sukuriamas kokybės užsakymas, kad prekę būtų galima perkelti į kokybės kontrolės vietą. Šio lauko reikšmė gali būti nustatyta kaip _Kurti kokybės užsakymą_ arba _Kurti tik darbą_. Numatytoji reikšmė yra _Kurti kokybės užsakymą_.

> [!NOTE]
> Neatsižvelgiant į tai, ar kokybės užsakymus kuriate neautomatiniu ar automatiniu būdu, sistema automatiškai sugeneruoja darbą, kad kokybės užsakymą pažymėjus kaip patvirtintą, prekės būtų perkeltos iš kokybės kontrolės vietos.

Kokybės užsakymo darbo kūrimas nesusijęs su kokybės susiejimo nustatymu. Jei yra darbo šablonas, kurio lauko **Darbo užsakymo tipas** reikšmė yra *Kokybės užsakymas*, ir to darbo šablono užklausos kriterijai yra tenkinami, kokybės užsakymo tikrinimas suaktyvins kokybės užsakymo darbo kūrimą.

#### <a name="referenced-item-sampling"></a>Nurodytas prekių pavyzdžių ėmimas

Kiekvienas kokybės susiejimas turi nurodyti prekių pavyzdžių ėmimą. Prekių pavyzdžių ėmimas apibrėžia kiekį, kuris bus išsiųstas kokybės kontrolei. Jį galima nustatyti taip, kad jis būtų taikomas tik tokiam kokybės susiejimui, kur lauko **Taikomas sandėlio tipas** reikšmė yra _Tik sandėlio procesų kokybės valdymas_. Jei prekių pavyzdžių ėmimo lauko **Pavyzdžių ėmimo aprėptis** reikšmė yra _Krovinys_ arba _Siunta_, arba lauko **Kiekio specifikacija** reikšmė yra _Visa numerio lentelė_, prekių pavyzdžių ėmimą gali nurodyti tik tie kokybės susiejimai, kurių laiko **Taikomas sandėlio tipas** reikšmė yra _Tik sandėlio procesų kokybės valdymas_.

Jeigu nurodysite prekių pavyzdžių ėmimą, kuris naudoja taikomą sandėlio tipą _Tik sandėlio procesų kokybės valdymas_, gausite klaidą, jei bandysite jį nurodyti iš kokybės susiejimo, kuris nenaudoja funkcijos _Sandėlio procesų kokybės valdymas_.

> [!NOTE]
> Visišką blokavimą naudojantis prekių pavyzdžių ėmimas nepalaikomas kokybės susiejimuose, kur lauko **Taikomas sandėlio tipas** reikšmė yra nustatyta kaip _Tik sandėlio procesų kokybės valdymas_.

### <a name="item-sampling"></a>Prekės pavyzdžio ėmimas

Prekių pavyzdžių ėmimas kontroliuoja, kaip dažnai prekės siunčiamos kokybės kontrolei. Su funkcija _Sandėlio procesų kokybės valdymas_ pristatoma sąvoka _Pavyzdžių ėmimo aprėptis_. Sistema naudoja prekių pavyzdžių ėmimo aprėptį, kai vertina, ar reikia sukurti kokybės užsakymus ir (arba) kokybės prekių pavyzdžių ėmimo darbą bei kokybės užsakymo darbą, ir kaip tai padaryti.

Norėdami nustatyti prekių pavyzdžių ėmimą, eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Prekių pavyzdžių ėmimas** ir nustatykite lauko **Pavyzdžių ėmimo aprėptis** reikšmę kaip vieną iš toliau nurodytų reikšmių.

- **Užsakymas** – šaltinio dokumento eilutė bus pagrindu vertinant, ar kuriami kokybės užsakymai ir (arba) kokybės prekių pavyzdžių ėmimo darbas bei kokybės užsakymo darbas, ir kaip tai daroma. Ši reikšmė yra numatytoji, o kai ji pasirenkama, sistema veikia taip pat, kaip tada, funkcija _Sandėlio procesų kokybės valdymas_ nėra įjungta.
- **Krovinys** – kroviniai bus naudojami kaip pagrindas vertinant, ar kuriamas kokybės užsakymas ir (arba) darbas, ir kaip tai daroma. Ši reikšmė galima tik tada, kai įjungta funkcija _Sandėlio procesų kokybės valdymas_.
- **Siunta** – siuntos bus naudojamos kaip pagrindas vertinant, ar kuriamas kokybės užsakymas ir (arba) darbas, ir kaip tai daroma. Ši reikšmė galima tik tada, kai įjungta funkcija _Sandėlio procesų kokybės valdymas_.

> [!NOTE]
> Kai lauko **Pavyzdžių ėmimo aprėptis** reikšmė nustatyta kaip *Krovinys* arba *Siunta*, bus naudojami krovinio ir siuntų objektai, jei jie yra. Jei jų nėra, bus naudojamas užsakymo objektas.

Su funkcija _Sandėlio procesų kokybės valdymas_ taip pat pateikiama lauko **Kiekio specifikacija** reikšmė *Visa numerio lentelė*. Ši reikšmė palaiko kokybės užsakymo darbo ir kokybės prekių pavyzdžių ėmimo darbo kūrimą pagal numerių lenteles. Pasirinkus šią reikšmę, atliekami toliau nurodyti pakeitimai.

- „FastTab“ konteineryje **Procesas** atsiranda parinktis **Paskirstymas pagal prekę** ir laukas **Kiekvienai n-tajai numerio lentelei**.
- „FastTab“ konteineryje **Paimtų pavyzdžių kiekis** atsiranda laukas **Reikšmė**.
- Parinkčių **Pagal atnaujintą kiekį**, **Vieta** ir **Numerio lentelė** reikšmės yra nustatytos kaip *Taip,* ir nustatymų keisti negalima.

Pasirinktis **Paskirstymas pagal prekę** kontroliuoja, ar numerio lentelės skaičius vertinamas pagal prekę, ar pagal visas prekes pavyzdžių ėmimo aprėptyje. Produkto variantai yra laikomi ta pačia preke. Ši parinktis taip pat kontroliuoja, ar kiekvienos prekės numerio lentelių skaičius nustatomas iš naujo.

Lauko **Kiekvienai n-tajai numerio lentelei** reikšmė kontroliuoja, kaip dažnai kuriami kokybės užsakymai užregistruotų prekių skaičiaus atžvilgiu. Pavyzdžiui, reikšmė *3* į kokybės kontrolę siųs kas trečią prekę, pradedant nuo pirmosios prekės. Reikšmė turi būti didesnė už 0 (nulį).

Darbuotojai priima prekes naudodamiesi „Warehousing“ programa, o sistema patikrina, ar kokybės susiejimas yra nustatytas kiekvienai gaunamai prekei. Jei nustatyta kokybės asociacija, sistema naudoja prekių pavyzdžių ėmimo įrašą, sukonfigūruotą tam kokybės susiejimui, kad nustatytų, kaip bus kuriami kokybės užsakymai, kokybės prekių pavyzdžių ėmimo darbas ir pirkimo užsakymo darbas.

> [!NOTE]
> Kai gavimo registracija atliekama žiniatinklio kliente (naudojant mažos registracijos puslapį arba pirkimo užsakymo eilučių prekių gavimo žurnalą), nebus sukurtas joks kokybės prekių pavyzdžių ėmimo darbas arba pirkimo užsakymo darbas, neatsižvelgiant į nustatymą. Vietoj to, prekėms, kurios atitinka kokybės susiejimą, bus naudojamas nurodytas prekių pavyzdžių ėmimas, kad būtų kontroliuojamas tik kokybės užsakymų kūrimas.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Automatinio kokybės užsakymų generavimo pavyzdžiai

Toliau pateikiami pavyzdžiai rodo, kaip kokybės susiejimo ir susietų prekių pavyzdžių ėmimo nustatymas veikia kokybės užsakymų generavimą, kai lauko **Taikomas sandėlio tipas** reikšmė nustatyta kaip _Tik sandėlio procesų kokybės valdymas_.

Kai lauko **Kiekio specifikacija** reikšmė yra _Visa numerio lentelė_, laukas **Kiekvienai n-tajai numerio lentelei** kontroliuoja, kurioms numerio lentelėms yra sukurtas kokybės prekių pavyzdžių ėmimo darbas. Pirmoji numerio lentelė visuomet perduodama kokybės kontrolei, o tada šio lauko reikšmė nurodo, kad po tos numerio lentelės taip pat turi būti perduodama kiekviena *n*-toji numerio lentelė.

Lauko **Nuorodos tipas** reikšmė šiuose pavyzdžiuose yra _Pirkimas_, o lauko **Įvykio tipas** reikšmė yra *Registracija*.

| Pavyzdžių ėmimo aprėptis | Kiekio specifikacija | Pagal atnaujintą kiekį | Pagal saugojimo dimensiją | Pertraukti skaičių pagal prekę | N-ajai numerio lentelei | Rezultatas |
|---|---|---|---|---|---|---|
| Užsakymas | Visa numerio lentelė | Taip _(užrakinta / neredaguojama)_ | <p>Vieta: Taip</p><p>Numerio lentelė: Taip _(užrakinta / neredaguojama)_</p> | nr. | 3 | <p>**Užsakymo eilutės kiekis: 100 EA**</p><ol><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 20 EA</p><p>1 kokybės užsakymas, skirtas 20 EA</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 20 EA (padėjimas)</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 3 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 20 EA (padėjimas)</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 4 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 20 EA</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 5 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 20 EA (padėjimas)</p></li></ol> |
| Užsakymas | Fiksuotas kiekis = 1 | Taip | <p>Vieta: Taip</p><p>Numerio lentelė: Taip</p> | nr. | Netaikoma | <p>**Užsakymo eilutės kiekis: 100**</p><ol><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 1 EA</p><p>1 kokybės užsakymas, skirtas 1 EA</p><p>Pirkimo užsakymo darbas, skirtas 19 EA (padėjimas)</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 1 EA</p><p>1 kokybės užsakymas, skirtas 1 EA</p><p>Pirkimo užsakymo darbas, skirtas 19 (padėjimas)</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 3 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 1 EA</p><p>1 kokybės užsakymas, skirtas 1 EA</p><p>Pirkimo užsakymo darbas, skirtas 19 EA (padėjimas)</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 4 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 1 EA</p><p>1 kokybės užsakymas, skirtas 1 EA</p><p>Pirkimo užsakymo darbas, skirtas 19 EA (padėjimas)</p></li><li>Užregistruoti 20 EA gavimą „Warehousing“ programoje, 5 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 1 EA</p><p>1 kokybės užsakymas, skirtas 1 EA</p><p>Pirkimo užsakymo darbas, skirtas 19 EA (padėjimas)</p></li></ol> |
| Užsakymas | Procentai = 10 | nr. | <p>Vieta: Ne</p><p>Numerio lentelė: Ne</p> | nr. | Netaikoma | <p>**Užsakymo eilutės kiekis: 100 EA**</p><ol><li>Užregistruoti 50 EA gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 10 EA</p><p>1 kokybės užsakymas, skirtas 10 EA</p><p>Pirkimo užsakymo darbas, skirtas 40 EA (padėjimas)</p></li><li>Užregistruoti 50 EA gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 50 EA (padėjimas)</p></li></ol> |
| Apkrova | Procentai = 5 | Taip _(užrakinta / neredaguojama)_ | <p>Vieta: Ne</p><p>Numerio lentelė: Ne</p> | nr. | Netaikoma | <p>**Užsakymo eilutės kiekis: 500 EA**</p><p>**2 kroviniai: pirmasis krovinys 200 EA, antrasis krovinys 300 EA**</p><ol><li>Užregistruoti pirmojo 100 EA krovinio gavimą „Warehousing“ programoje<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 5 EA</p><p>1 kokybės užsakymas, skirtas 5 EA</p><p>Pirkimo užsakymo darbas, skirtas 95 EA (padėjimas)</p></li><li>Užregistruoti pirmojo 100 EA krovinio gavimą „Warehousing“ programoje<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 5 EA</p><p>1 kokybės užsakymas, skirtas 5 EA</p><p>Pirkimo užsakymo darbas, skirtas 95 EA (padėjimas)</p></li><li>Užregistruoti antrojo 300 EA krovinio gavimą „Warehousing“ programoje<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 15 EA</p><p>1 kokybės užsakymas, skirtas 15 EA</p><p>Pirkimo užsakymo darbas, skirtas 285 EA (padėjimas)</p></li></ol> |
| Užsakymas | Procentai = 10 | nr. | <p>Vieta: Taip</p><p>Numerio lentelė: Taip</p> | nr. | Netaikoma | <p>**Užsakymo eilutės kiekis: 100**</p><ol><li>Užregistruoti 50 EA gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 5 EA</p><p>1 kokybės užsakymas, skirtas 5 EA</p><p>Pirkimo užsakymo darbas, skirtas 45 EA (padėjimas)</p></li><li>Užregistruoti 50 EA gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 5 EA</p><p>1 kokybės užsakymas, skirtas 5 EA</p><p>Pirkimo užsakymo darbas, skirtas 45 (padėjimas)</p></li></ol> |
| Apkrova | Visa numerio lentelė | Taip _(užrakinta / neredaguojama)_ | <p>Vieta: Taip</p><p>Numerio lentelė: Taip _(užrakinta / neredaguojama)_</p> | nr. | 3 | <p>**Dvi prekės:**</p><ul><li>**A prekės užsakymo eilutės kiekis: 120 EA (4 padėklai)**</li><li>**B prekės užsakymo eilutės kiekis: 90 EA (3 padėklai)**</li></ul><p>**Vienas krovinys, dvi krovinio eilutės su kiekvieno užsakymo eilute**</p><ol><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 30 EA</p><p>1 kokybės užsakymas, skirtas 30 EA</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 3 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 4 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 30 EA</p><p>1 kokybės užsakymas, skirtas 30 EA</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 5 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 6 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 7 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 30 EA</p><p>1 kokybės užsakymas, skirtas 30 EA</p></li></ol> |
| Apkrova | Visa numerio lentelė | Taip _(užrakinta / neredaguojama)_ | <p>Vieta: Taip</p><p>Numerio lentelė: Taip _(užrakinta / neredaguojama)_</p> | Taip | 3 | <p>**Dvi prekės:**</p><ul><li>**A prekės užsakymo eilutės kiekis: 120 EA (4 padėklai)**</li><li>**B prekės užsakymo eilutės kiekis: 90 EA (3 padėklai)**</li></ul><p>**Vienas krovinys, dvi krovinio eilutės su kiekvieno užsakymo eilute**</p><ol><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 30 EA</p><p>1 kokybės užsakymas, skirtas 30 EA</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 3 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 4 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 30 EA</p><p>1 kokybės užsakymas, skirtas 30 EA</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 5 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 30 EA</p><p>1 kokybės užsakymas, skirtas 30 EA</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 6 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li><li>Užregistruoti prekės A, 30 EA, gavimą „Warehousing“ programoje, 7 numerio lentelė<p>Pirkimo užsakymo darbas, skirtas 30 EA (padėjimas)</p></li></ol> |
| Apkrova | Procentai = 10 | Taip _(užrakinta / neredaguojama)_ | <p>Vieta: Ne</p><p>Numerio lentelė: Ne</p> | nr. | Netaikoma | <p>**Užsakymo eilutės kiekis: 100 EA**</p><p>**Nėra sukurtų krovinių. Taikoma užsakymo aprėptis.**</p><ol><li>Užregistruoti 50 EA gavimą „Warehousing“ programoje, 1 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 5 EA</p><p>1 kokybės užsakymas, skirtas 5 EA</p><p>Pirkimo užsakymo darbas, skirtas 45 EA (padėjimas)</p></li><li>Užregistruoti 50 EA gavimą „Warehousing“ programoje, 2 numerio lentelė<p>Kokybės prekių pavyzdžių ėmimo darbas, skirtas 5 EA</p><p>1 kokybės užsakymas, skirtas 5 EA</p><p>Pirkimo užsakymo darbas, skirtas 45 EA (padėjimas)</p></li></ol> |

Kai darbuotojas patikrina vieną iš ankstesniame lentelėje pateiktų kokybės užsakymų, sistema automatiškai sugeneruoja kokybės užsakymo darbą, kad atsargos būtų perkeltos iš kokybės kontrolės vietos į vietą, nurodytą darbo užsakymo tipo _Kokybės užsakymas_ vietos nurodyme. Šiam tikslui galite nustatyti bet kurią vietą, pvz., grąžinimo arba saugojimo vietą, atsižvelgdami į kokybės užsakymo bandymo rezultatą. Šio nustatymo pavyzdį rasite [pavyzdiniame scenarijuje](#example-scenario) šios temos pabaigoje.

Galite iš naujo atidaryti jau patikrintą kokybės užsakymą, su sąlyga, kad kokybės užsakymo darbo, susijusio su atsargų perkėlimu iš kokybės kontrolės vietos, lauko **Darbo būsena** reikšmė nėra *Uždarytas* arba *Vykdomas*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Proceso įžvalgos, kai kartu veikia keli kokybės susiejimai

Tai pačiai šaltinio dokumento eilutei gali būti nustatytas ir pritaikytas daugiau nei vienas kokybės susiejimas, ir lauko **Taikomas sandėlio tipas** reikšmę kai kuriems iš tų kokybės susiejimų galima nustatyti kaip _Tik sandėlio procesų kokybės valdymas_, o kitiems – _Visi_.

Šiame pavyzdyje lauko **Nuorodos tipas** reikšmė yra _Pirkimas_.

1. Pirmasis kokybės susiejimas nustatomas taip:

    - **Taikomas sandėlio tipas:** *Tik sandėlio procesų kokybės valdymas*
    - **Prekės kodas:** *A0001*
    - **Sąskaitos kodas:** *Visi*
    - **Bandymų grupė:** *Priedas*
    - **Prekių pavyzdžių ėmimas:** *5 vnt.*

1. Antrasis kokybės susiejimas nustatomas taip:

    - **Taikomas sandėlio tipas:** *Visi*
    - **Prekės kodas:** *Visi*
    - **Sąskaitos kodas:** *Visi*
    - **Bandymų grupė:** *Priedas*
    - **Prekių pavyzdžių ėmimas:** *1 vnt.*

1. Trečiasis kokybės susiejimas nustatomas taip:

    - **Taikomas sandėlio tipas:** *Tik sandėlio procesų kokybės valdymas*
    - **Prekės kodas:** *Visi*
    - **Sąskaitos kodas:** *104*
    - **Bandymų grupė:** *Triktis*
    - **Prekių pavyzdžių ėmimas:** *Kas antra numerio lentelė* (Šis nustatymas reiškia, kad kokybės užsakymą sukurs pirma, trečia, penkta ir t.t. gautos numerio lentelės.)

1. Ketvirtasis kokybės susiejimas nustatomas taip:

    - **Taikomas sandėlio tipas:** *Visi*
    - **Prekės kodas:** *Visi*
    - **Sąskaitos kodas:** *Visi*
    - **Bandymų grupė:** *Triktis*
    - **Prekių pavyzdžių ėmimas:** *5 vnt.*

1. Penktasis kokybės susiejimas nustatomas taip:

    - **Taikomas sandėlio tipas:** *Visi*
    - **Prekės kodas:** *Visi*
    - **Sąskaitos kodas:** *Visi*
    - **Bandymų grupė:** *Kūgis*
    - **Prekių pavyzdžių ėmimas:** *10 %*

Dabar 104 tiekėjui sukurtas A0001 prekės pirkimo užsakymas kiekiui „10“. Tada pirkimo užsakymo eilutė, kurios kiekis yra 10, yra užregistruojama kaip gauta vienoje numerio lentelėje naudojant „Warehousing“ programą. Toliau parodytas rezultatas.

- Yra vienas kokybės užsakymas iš pirmojo bandymų grupės *Priedas* kokybės susiejimo. Kiekis yra 5. Nėra kokybės užsakymo iš antrojo kokybės susiejimo, nes pirmojo kokybės susiejimo kriterijai yra labiau apibrėžti, palyginti su bandymų grupe *Priedas*.
- Yra vienas kokybės užsakymas, skirtas trečiajam bandymų grupės *Triktis* kokybės susiejimui. Kiekis yra 10. Nėra kokybės užsakymo iš ketvirtojo kokybės susiejimo, nes pirmojo kokybės susiejimo kriterijai yra labiau apibrėžti, palyginti su bandymų grupe *Triktis*.
- Yra vienas kokybės užsakymas, skirtas penktajam bandymų grupės *Kūgis* kokybės susiejimui. Kiekis yra 1.

Kuriant vieną kokybės užsakymą kiekvienam iš trijų kokybės susiejimų, taip pat sukuriamas kokybės prekių pavyzdžių ėmimo darbas. Užregistruotas kiekis yra tik 10. Tačiau dėl prekių pavyzdžių ėmimo nustatymo, kokybės užsakymo kiekių, sukurtų taikomam sandėlio tipui *Tik sandėlio procesų kokybės valdymas*, suma yra 16, kuri viršija faktinį registruotą kiekį 10. Todėl darbas nebus sukurtas visiems kokybės užsakymo kiekiams (16), nes tik 10 galima faktiškai perkelti į kokybės kontrolės vietą. Prioritetas, naudojamas kuriant kokybės prekių pavyzdžių ėmimo darbą, yra toks pat, kaip kuriant kokybės užsakymą.

- **Pirmas kokybės užsakymas (kiekis = 5):** kokybės prekių pavyzdžių ėmimo darbas sukuriamas 5 prekėms. Kiekis 5 (10 – 5) dabar lieka tolesniam kokybės prekių pavyzdžių ėmimo darbo kūrimui.
- **Antrasis kokybės užsakymas (kiekis = 10):** kokybės prekių pavyzdžių ėmimo darbas sukuriamas 5 prekėms. Kiekis 0 (nulis) dabar lieka tolesniam kokybės prekių pavyzdžių ėmimo darbo kūrimui.
- **Trečiasis kokybės užsakymas (kiekis = 1):** kokybės prekių pavyzdžių ėmimo darbas nesukurtas.

Kuriant kokybės užsakymus, sukuriamas kiekio 10 atsargų blokavimas. Šis atsargų blokavimas nurodomas pagal kiekvieną iš trijų kokybės užsakymų. Kokybės užsakymo kiekių suma yra 16.

Kai kokybės užsakymai patikrinami, sistema bando sukurti kokybės užsakymo darbą kiekvienam patikrintam kokybės užsakymui. Kokybės užsakymo kiekių suma viršija faktiškai užblokuotą ir darbo kūrimui prieinamą kiekį, todėl kokybės užsakymo darbo negalima sukurti visiems kokybės užsakymo kiekiams, kaip parodyta čia. (Šiuo pavyzdžiu tęsiamas ankstesnis pavyzdys.)

1. **Patikrinkite antrąjį sukurtą kokybės užsakymą (kiekis = 10). Kokybės užsakymo darbas sukurtas kiekiui 4.**

    Kokybės užsakymo darbo kūrimą suaktyvina atsargų blokavimo kiekio pasikeitimas. Kokybės užsakymo kiekių suma buvo 16, todėl patikrinus kiekį 10, likę kokybės užsakymo kiekiai bus patikrinti kaip lygūs 6. Atsargų blokavimo kiekis sumažinamas nuo 10 iki 6. Sumažintas kiekis 4 yra priskiriamas kokybės užsakymo darbo kūrimui.

2. **Patikrinkite pirmąjį sukurtą kokybės užsakymą (kiekis = 5). Kokybės užsakymo darbas sukurtas kiekiui 5.**

    Kokybės užsakymo darbo kūrimą suaktyvina atsargų blokavimo kiekio pasikeitimas. Kokybės užsakymo kiekių suma buvo 6, todėl patikrinus kiekį 5, likę kokybės užsakymo kiekiai bus patikrinti kaip lygūs 1. Atsargų blokavimo kiekis sumažinamas nuo 6 iki 1. Sumažintas kiekis 5 yra priskiriamas kokybės užsakymo darbo kūrimui.

3. **Patikrinkite trečiąjį sukurtą kokybės užsakymą (kiekis = 1). Kokybės užsakymo darbas sukurtas kiekiui 1.**

    Kokybės užsakymo darbo kūrimą suaktyvina atsargų blokavimo kiekio pasikeitimas. Kokybės užsakymo kiekių suma buvo 1, todėl patikrinus kiekį 1, likę kokybės užsakymo kiekiai bus patikrinti kaip lygūs 0 (nuliui). Atsargų blokavimas pašalinamas (t. y., atsargų blokavimo kiekis sumažinamas nuo 1 iki 0). Sumažintas kiekis 1 yra priskiriamas kokybės užsakymo darbo kūrimui.

> [!NOTE]
> Kokybės užsakymo darbo kūrimas priklauso nuo atsargų blokavimo kiekio, nurodomo pagal vieną arba kelis kokybės užsakymus. Jei kokybės užsakymo kiekių suma viršija nurodytą atsargų blokavimo kiekį, užsakymas, kuriame patvirtinami kokybės užsakymai, lemia kokybės užsakymo darbo kūrimą.

## <a name="canceling-quality-item-sampling-work"></a>Kokybės prekių pavyzdžių ėmimo darbo atšaukimas

Galite atšaukti darbą, sukurtą kokybės prekių pavyzdžių ėmimui. Norėdami kontroliuoti, kas atsitinka atšaukus darbą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Skirtuko **Bendra** „FastTab“ konteineryje **Darbas** nustatykite vieną iš toliau nurodytų parinkties **Išregistruoti gavimą, kai darbas atšaukiamas** reikšmių.

    - **Taip** – kai atšaukiamas kokybės prekių pavyzdžių ėmimo darbas, susietas kokybės užsakymas panaikinamas, o atsargos išregistruojamos.
    - **Ne** – kai atšaukiamas kokybės prekių pavyzdžių ėmimo darbas, susietas kokybės užsakymas nepanaikinamas, o atsargos nėra išregistruojamos.

## <a name="cross-docking"></a>Prekių skirstymas

Jūs galite turėti kokybės susiejimo nustatymą, kuris sukuria prekių pavyzdžių ėmimo darbą. Tačiau, kai lygiagrečiai su kokybės susiejimu, kuris sukuria kokybės prekių pavyzdžių ėmimo darbą, vyksta prekių skirstymas, jei kiekio pakanka tik prekių skirstymui, sukuriamas tik prekių pavyzdžių ėmimo darbas. Tais atvejais, kai gavimo sandėliui parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmė yra nustatyta kaip _Taip_, o kokybės susiejimui lauko **Taikomas sandėlio tipas** reikšmė nustatyta kaip _Tik sandėlio procesų kokybės valdymas_, kokybės prekių pavyzdžių ėmimo darbo kūrimui taikomas pirmumas prieš prekių skirstymo darbo kūrimą. Jei kiekis viršija prekių skirstymo reikalavimus, sistema vis tiek kuria tik prekių pavyzdžių ėmimo darbą.

## <a name="destructive-testing"></a>Ardomieji bandymai

Galite apibrėžti bandymų grupę, kuri atlieka ardomąjį bandymą. Atliekant ardomąjį bandymą, daroma prielaida, kad, neatsižvelgiant į bandymo rezultatą, bandomos prekės kiekis bus sunaikintas kaip bandymo dalis. Taip, kaip funkcija _Sandėlio procesų kokybės valdymas_ palaiko ardomąjį bandymą, yra panašu į tai, kaip kokybės valdymas jį palaiko, kai funkcija neįjungta. Prieš tikrinant kokybės užsakymą, kokybės valdiklis turi nurodyti sunaikinto kiekio paėmimo vietą. Paėmimą galite užregistruoti iš kokybės užsakymo puslapio, veiksmų srityje pasirinkdami **Atsargos \> Paėmimas**. Užregistravus kokybės užsakymo kiekio paėmimą, galima atlikti tikrinimą.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

### <a name="prepare-the-scenario"></a>Scenarijaus paruošimas

Norėdami dirbti pagal šį scenarijų, turite parengti savo sistemą toliau aprašytu būdu.

- Įsitikinkite, kad sistemoje įdiegti demonstraciniai duomenys, ir pasirinkite juridinį subjektą **USMF**.
- [Funkcijų valdymo dalyje](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjunkite funkciją _Sandėlio procesų kokybės valdymas_.
- Konfigūruokite sandėlį 51, kad jis galėtų naudoti funkciją _Sandėlio procesų kokybės valdymas_, atlikdami toliau nurodytus veiksmus.

    1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
    1. Pasirinkite 51 sandėlį.
    1. „FastTab“ konteineryje **Sandėlis** parinkties **Įgalinti sandėlio procesų kokybės užsakymą** reikšmę nustatykite kaip *Taip*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Perkėlimo į kokybės kontrolę nustatymas – perkėlimas į kokybės kontrolės vietą

Dabar turite paruošti pagrindinį nustatymą, kuris įgalins jūsų sistemą palaikyti funkciją _Sandėlio procesų kokybės valdymas_, skirtą sandėliui 51. (Demonstraciniai duomenys apibrėžia kokybės valdymo vietą, pavadintą *QMS*. Ta vieta šiame scenarijuje yra nurodyta kelis kartus.) Jums reikės paruošti toliau nurodytus elementai, kaip aprašyta šio skyriaus poskirsniuose.

- Darbo klasė
- Darbo šablonas
- Vietos nurodymas
- Prekės pavyzdžio ėmimas
- Kokybės susiejimas
- Mobiliojo įrenginio meniu elementai

#### <a name="work-class-for-quality-in"></a>Perkėlimo į kokybės kontrolę darbo klasė

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.
1. Sukurkite darbo klasę ir nustatykite šias reikšmes:

    - **Darbo klasės ID:** _QualityIn_
    - **Aprašas:** _Kokybės prekių pavyzdžių ėmimas_
    - **Darbo užsakymo tipas:** _Kokybės prekių pavyzdžių ėmimas_

#### <a name="work-template"></a>Darbo šablonas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Nustatykite lauko **Darbo užsakymo tipas** reikšmę kaip _Kokybės prekių pavyzdžių ėmimas_.
1. Sukurkite darbo šabloną ir nustatykite šias reikšmes:

    - **Darbo šablonas:** _51 Kokybė_
    - **Darbo šablono aprašas:** _51 Kokybė_

1. Įtraukite į darbo šabloną eilutę ir nustatykite šias reikšmes:

    - **Darbo tipas:** _Paėmimas_
    - **Darbo klasės ID:** _QualityIn_

1. Įtraukite į darbo šabloną antrą eilutę ir nustatykite šias reikšmes:

    - **Darbo tipas:** _Padėjimas_
    - **Darbo klasės ID:** _QualityIn_

#### <a name="location-directive"></a>Vietos nurodymas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Nustatykite lauko **Darbo užsakymo tipas** reikšmę kaip _Kokybės prekių pavyzdžių ėmimas_.
1. Sukurkite vietos nurodymą ir nustatykite šias reikšmes:

    - **Pavadinimas:** _51 į kokybę_
    - **Darbo tipas:** _Padėjimas_
    - **Vieta:** 5
    - **Sandėlis:** _51_

1. Įtraukite vietos nurodymo eilutę ir nustatykite šias reikšmes:

    - **Pradinis kiekis:** _1_
    - **Galutinis kiekis:** _1000000_

1. Sukurkite vietos nurodymo veiksmą ir nustatykite šią reikšmę:

    - **Pavadinimas:** _Kokybė_

1. Norėdami sukurti naują vietos nurodymo veiksmą pasirinkite **Redaguoti užklausą** ir nurodykite įrašą **Diapazonas**, kuris turi tokias reikšmes:

    - **Lentelė:** *Vietos*
    - **Laukas:** _Vietos profilio ID_
    - **Kriterijai:** *QMS*

1. Pasirinkite **Gerai**, kad įrašytumėte užklausą, ir įrašykite naują vietos nurodymą.

Tada 51 sandėliui turite pakeisti esamų pirkimo užsakymo vietų nurodymų seką. Į parodomuosius duomenis įtraukti du vietų nurodymai, kurių lauko **Darbo užsakymo tipas** reikšmė yra _Pirkimas_: vienas pavadintas _51 QMS_, o kitas – _51 Tiesioginis PU_. Norėdami užtikrinti, kad 51 sandėliui būtų taikoma funkcija *Sandėlio procesų kokybės valdymas*, turite pasirūpinti, kad nebūtų taikomas vietos nurodymas _51 QMS_. Tačiau užuot panaikinę tą vietos nurodymą (nes galbūt norėsite jį naudoti ateityje), galite tiesiog pakeisti seką.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Lauko **Darbo užsakymo tipas** reikšmę nustatykite kaip _Pirkimo užsakymas_.
1. Sekos sąraše pasirinkite eilės numerį 5, skirtą vietos nurodymui _51 Tiesioginis PU_.
1. Perkelkite pažymėtą elementą seka aukštyn iki eilės numerio 4.
1. Patikrinkite, ar dabar vietos nurodymo _51 QMS_ eilės numeris yra ne mažesnis už 5.

#### <a name="item-sampling"></a>Prekės pavyzdžio ėmimas

Funkcija _Sandėlio procesų kokybės valdymas_ įtraukia kelias naujas prekių pavyzdžių ėmimo galimybes. Lauko **Pavyzdžių ėmimo aprėptis** reikšmė dabar gali būti _Užsakymas_, _Siunta_ arba _Krovinys_, o lauko **Paimtų pavyzdžių kiekis** reikšmė dabar gali būti _Visa numerio lentelė_.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Prekių pavyzdžių ėmimas**.
1. Sukurkite prekių pavyzdžių ėmimo įrašą ir nustatykite šias reikšmes:

    - **Prekių pavyzdžių ėmimas:** _3 LP_
    - **Aprašas:** _Kas trečia numerio lentelė_
    - **Pavyzdžių ėmimo aprėptis:** _Užsakymas_

1. „FastTab“ konteineryje **Paimtų pavyzdžių kiekis** lauko **Kiekio specifikacija** reikšmę nustatykite kaip _Visą numerio lentelė_.
1. „FastTab“ konteineryje **Procesas** lauko **Kiekvienai n-tajai numerio lentelei** reikšmę nustatykite kaip _3_.
1. Dalyje **Pagal saugojimo dimensiją** įgalinkite ir **Sandėlis**, ir **Atsargų būsena**.

#### <a name="quality-associations"></a>Kokybės susiejimai

Sukurkite kokybės susiejimą, kuris naudos naują prekių pavyzdžių ėmimą.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Kokybės susiejimai**.
1. Sukurkite kokybės susiejimo įrašą ir nustatykite šias reikšmes:

    - **Nuorodos tipas:** _Pirkimas_
    - **Prekės kodas:** _Lentelė_
    - **Prekė:** _M9201_
    - **Vieta:** _5_

1. „FastTab“ konteineryje **Procesas** lauko **Įvykio tipas** reikšmę nustatykite kaip *Registracija*.
1. „FastTab“ konteineryje **Sąlygos** lauko **Taikomas sandėlio tipas** reikšmę nustatykite kaip *Tik sandėlio procesų kokybės valdymas*.
1. „FastTab“ konteineryje **Kokybės užsakymo procesas** lauko **Kokybės apdorojimo strategija** reikšmę nustatykite kaip _Kurti kokybės užsakymą_.
1. „FastTab“ konteineryje **Specifikacijos** dešiniuoju pelės mygtuku spustelėkite lauką **Bandymų grupė**, tada pasirinkite **Peržiūrėti informaciją**, kad būtų atidarytas puslapis **Bandymų grupės**.
1. Puslapio **Bandymų grupės** viršutinio tinklelio skirtuke **Apžvalga** sukurkite bandymų grupę ir nustatykite šias reikšmes:

    - **Bandymų grupė:** _QMS_
    - **Aprašas:** _QMS bandymas_
    - **Priimtinas kiekis:** _100_
    - **Prekių pavyzdžių ėmimas:** _3 LP_ (pasirinkti)

1. Apatinio tinklelio skirtuke **Apžvalga** įtraukite vieno bandymo įrašą ir nustatykite šias reikšmes:

    - **Seka:** *1*
    - **Bandymas:** *Priedo matavimas*

1. Apatinio tinklelio skirtuke **Bandymas** nustatykite šias reikšmes:

    - **Bandymo kintamieji:** *Sėkminga / nesėkminga*
    - **Numatytasis rezultatas:** *Sėkminga*

1. Įrašykite naują bandymų grupę ir uždarykite puslapį **Bandymų grupės**.
1. Grįžę į puslapį **Kokybės susiejimai**, lauke **Bandymų grupė** pasirinkite **QMS**.
1. Įrašykite įrašą.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Perkėlimo į kokybės kontrolę mobiliojo įrenginio meniu elementai

Norėdami užbaigti nustatymą, kad prekė būtų perkeltos į kokybės kontrolės vietą, turite atlikti kokybės prekių pavyzdžių ėmimo darbą iš mobiliojo įrenginio meniu elemento.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite mobiliojo įrenginio meniu elementą **Pirkimo padėjimas**.
1. „FastTab“ konteineryje **Darbų klasės** įtraukite darbo klasės ID *QualityIn*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Suvestinė: jūsų nustatymas, pagal kurį prekės perkeliamos į kokybės kontrolę

Dabar apibrėžėte kokybės susiejimą, kuris naudoja funkciją *Sandėlio procesų kokybės valdymas*, kad būtų suaktyvintas kokybės užsakymo kūrimas. Nustatėte 51 sandėlio darbo ir vietos duomenis, kad užtikrintumėte, jog užregistravus prekės M9201 pirkimą bus sukurtas konkretus darbas. Šis nustatymas užtikrina, kad kas trečia užregistruota numerio lentelė būtų perkelta į kokybės vietą (_QMS_) ir kad numerio lentelių kiekiui bus sukurtas kokybės užsakymas. Visa kita bus perkelta į padėjimo, o ne kokybės kontrolės vietą.

### <a name="process-quality-management-work"></a>Procesų kokybės valdymo darbas

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Sukurkite pirkimo užsakymą ir nustatykite šias reikšmes:

    - **Nurodykite tiekėjo sąskaitą:** *104*
    - **Sandėlis:** *51*

1. Įtraukite pirkimo užsakymo eilutę ir nustatykite šias reikšmes:

    - **Prekė:** *M9201*
    - **Kiekis:** *20*
    - **Mat. vnt.:** *ea*
    - **Sandėlis:** *51*

1. Užsirašykite pirkimo užsakymo numerį, kad galėtumėte jį panaudoti vėliau.
1. Mobiliajame įrenginyje arba emuliatoriuje, kuriame veikia „Warehousing“ programa, prisijunkite prie 51 sandėlio įrašydami *51* į vartotojo ID vietą, o *1* – į slaptažodžo vietą.
1. Eikite į **Gaunamas \> Pirkimo gavimas** ir įveskite šias reikšmes:

    - **PONum:** ką tik sukurto pirkimo užsakymo numeris
    - **Kiekis:** *5*
    - **Vienetas:** *ea*

1. Tęskite, kad būtų gaunama pagal eilutę, po *5 ea* vienu metu, kol eilutė bus visiškai gauta. (Iš viso bus sukurtos keturios numerio lentelės.)
1. Atsijunkite nuo „Warehousing“ programos.
1. Grįžę į žiniatinklio klientą, eikite į **Įsigijimas ir šaltiniai \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Raskite ir atidarykite pirkimo užsakymą.
1. Dalyje **Pirkimo užsakymo eilutės** pasirinkite prekės numerio *M9201* eilutę, tada pasirinkite **Pirkimo užsakymo eilutės \> Darbo informacija**.
1. Atkreipkite dėmesį, kad antroji ir trečioji sukurtos darbo antraštės yra periodinis padėjimo darbas, o pirmoji ir ketvirtoji darbo antraštės yra kokybės prekių pavyzdžių ėmimo darbas. Šis rezultatas atitinka prekių pavyzdžių ėmimo nustatymą, kuris sukonfigūruotas taip, kad būtų imamas kas trečios numerio lentelės pavyzdys.

#### <a name="move-to-the-quality-control-location"></a>Perkėlimas į kokybės kontrolės vietą

Dabar perkelsite numerio lenteles į jų nurodytas vietas. Pirmoji ir ketvirtoji numerio lentelės pateks į kokybės kontrolės vietą, o antroji ir trečioji numerio lentelės pateks tiesiai į saugyklą.

1. Mobiliajame įrenginyje arba emuliatoriuje, kuriame veikia „Warehousing“ programa, prisijunkite prie 51 sandėlio įrašydami *51* į vartotojo ID vietą, o *1* – į slaptažodžo vietą.
1. Eikite į **Gaunamas \> Pirkimo padėjimas** ir padėkite kiekvieną numerio lentelę iš ankstesnės procedūros, kol uždarysite visą darbą.

#### <a name="summary-process-quality-management-work"></a>Suvestinė: Procesų kokybės valdymo darbas

Ką tik atlikote pirmosios ir ketvirtosios numerio lentelių kokybės prekių pavyzdžių ėmimo darbą, perkeldami jas į kokybės kontrolės vietą. Taip pat padėjote antrąją ir trečiąją numerio lenteles. Kitas veiksmas skirtas kokybės užsakymo bandymui ir kontrolei atlikti.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Perkėlimo iš kokybės kontrolės nustatymas – perkėlimas iš kokybės kontrolės vietos į saugyklą arba grąžinimas

Kai darbuotojai praneša kokybės užsakymo rezultatus, sistema automatiškai sugeneruoja darbą.

Dabar tęsite būtinąjį bazinį darbo klasės, darbo šablono ir vietos nurodymo nustatymą, kad būtų įgalintas sandėlio procesų kokybės valdymas ir kad būtų galima sukurti reikiamą darbą, pagal kurį kokybės užsakymo kiekis bus perkeltas iš kokybės kontrolės vietos perkelti į nurodytą sandėlio vietą.

#### <a name="work-class-for-quality-out"></a>Perkėlimo iš kokybės kontrolės darbo klasė

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.
1. Sukurkite darbo klasę ir nustatykite šias reikšmes:

    - **Darbo klasės ID:** *QualityOut*
    - **Aprašas:** *Perkėlimas iš kokybės kontrolės*
    - **Darbo užsakymo tipas:** *Kokybės užsakymas*

#### <a name="work-templates"></a>Darbo šablonai

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Pakeiskite lauko **Darbo užsakymo tipas** reikšmę į *Kokybės užsakymas*.
1. Sukurkite darbo šabloną ir nustatykite šias reikšmes:

    - **Darbo šablonas:** *51 iš kokybės*
    - **Darbo šablono aprašas:** *51 iš kokybės*

1. Įtraukite eilutę ir nustatykite šias reikšmes:

    - **Darbo tipas:** *Paėmimas*
    - **Darbo klasės ID:** **QualityOut**

1. Įtraukite antrą eilutę ir nustatykite šias reikšmes:

    - **Darbo tipas:** *Padėjimas*
    - **Darbo klasės ID:** *QualityOut*

#### <a name="location-directives"></a>Vietos nurodymai

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Pakeiskite lauko **Darbo užsakymo tipas** reikšmę į *Kokybės užsakymas*.
1. Sukurkite vietos nurodymą ir nustatykite šias reikšmes:

    - **Pavadinimas:** *51 sėkminga*
    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *5*
    - **Sandėlis:** *51*

1. Veiksmų srityje pasirinkite **Redaguoti užklausą**, kad atidarytumėte užklausos rengyklės dialogo langą.
1. Skirtuke **Diapazonas** nustatykite šias reikšmes:

    - **Lentelė:** *Kokybės užsakymai*
    - **Laukas:** *Būsena*
    - **Kriterijai:** *Sėkminga*

1. Pasirinkite **Gerai**, kad įrašytumėte užklausą ir uždarytumėte dialogo langą.
1. „FastTab“ konteineryje **Eilutės** įtraukite eilutę ir nustatykite šias reikšmes:

    - **Pradinis kiekis:** *1*
    - **Galutinis kiekis:** *1000000*

1. „FastTab“ konteineryje **Vietos nurodymo veiksmai**, įtraukite eilutę ir nustatykite šią reikšmę:

    - **Pavadinimas:** *Sėkminga*

1. „FastTab“ konteineryje **Vietos nurodymo veiksmai** pasirinkite **Redaguoti užklausą**, kad atidarytumėte užklausos rengyklės dialogo langą.
1. Skirtuke **Diapazonas** nustatykite šias reikšmes:

    - **Lentelė:** *Vietos*
    - **Laukas:** *Zonos ID*
    - **Kriterijai:** *Palaidas krovinys*

1. Pasirinkite **Gerai**, kad įrašytumėte užklausą ir uždarytumėte dialogo langą.
1. Veiksmų srityje pasirinkite **Įrašyti**, kad įrašytumėte naują vietos nurodymą.
1. Sukurkite antrąjį vietos nurodymą ir nustatykite šias reikšmes:

    - **Pavadinimas:** *51 nesėkminga*
    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *5*
    - **Sandėlis:** *51*

1. Veiksmų srityje pasirinkite **Redaguoti užklausą**, kad atidarytumėte užklausos rengyklės dialogo langą.
1. Skirtuke **Diapazonas** nustatykite šias reikšmes:

    - **Lentelė:** *Kokybės užsakymai*
    - **Laukas:** *Būsena*
    - **Kriterijai:** *Nesėkminga*

1. Pasirinkite **Gerai**, kad įrašytumėte užklausą ir uždarytumėte dialogo langą.
1. „FastTab“ konteineryje **Eilutės** įtraukite eilutę ir nustatykite šias reikšmes:

    - **Pradinis kiekis:** *1*
    - **Galutinis kiekis:** *1000000*

1. „FastTab“ konteineryje **Vietos nurodymo veiksmai**, įtraukite eilutę ir nustatykite šią reikšmę:

    - **Pavadinimas:** *Nesėkminga*

1. „FastTab“ konteineryje **Vietos nurodymo veiksmai** pasirinkite **Redaguoti užklausą**, kad atidarytumėte užklausos rengyklės dialogo langą.
1. Skirtuke **Diapazonas** nustatykite šias reikšmes:

    - **Lentelė:** *Vietos*
    - **Laukas:** *Zonos ID*
    - **Kriterijai:** *Grąžinimas*

1. Pasirinkite **Gerai**, kad įrašytumėte užklausą ir uždarytumėte dialogo langą.
1. Veiksmų srityje pasirinkite **Įrašyti**, kad įrašytumėte naują vietos nurodymą.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Perkėlimo iš kokybės kontrolės mobiliojo įrenginio meniu elementai

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite mobiliojo įrenginio meniu elementą **QMS padėjimas**.
1. „FastTab“ konteineryje **Darbų klasės** įtraukite darbo klasės ID *QualityPut*.

Dabar sandėlio darbuotojai galės pasirinkti kokybės užsakymo darbą naudodami meniu elementą **QMS padėjimas**. Prekes, kurių kokybės kontrolė buvo nesėkminga, galima padėti grąžinimo vietoje, o prekes, kurių kokybės kontrolė buvo sėkminga, galima perkelti į vietą „Bulk-001“.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Suvestinė: jūsų nustatymas, pagal kurį prekės perkeliamos iš kokybės kontrolės

Nustatėte 51 sandėlio darbo ir vietos duomenis, kad užtikrintumėte, jog atlikus kokybės užsakymus, darbas būtų sukurtas automatiškai. Šis nustatymas užtikrina, kad kiekviena kokybės kontroliuojama numerio lentelė būtų perkelta į palaidų krovinių vietą arba į grąžinimo vietą.

### <a name="process-quality-management-work"></a>Procesų kokybės valdymo darbas

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Pasirinkite pirmą užregistruotų kiekių kokybės užsakymą.
1. Pasirinkite **Tikrinti**. Bandymo būsena atnaujinama į *Nesėkminga*.
1. Eikite į **Sandėlio valdymas \> Visi darbai**.
1. Atidarykite ką tik sukurtą darbą ir atkreipkite dėmesį, kad lauko **Darbo užsakymo tipas** reikšmė yra *Kokybės užsakymas*. Darbas apima eilutę, kurioje padėjimo vieta yra *Grąžinimas*, o būsena – *Nesėkminga*. (Jei kokybės užsakymo būsena *Sėkminga*, vietoj to padėjimo vieta bus *Palaidas krovinys*.)
1. Grįžkite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Pasirinkite antrą užregistruotų prekių kokybės užsakymą.
1. Virš apatinio tinklelio pasirinkite **Rezultatai**. Atnaujinkite lauko **Rezultatų kiekis** reikšmę į *5*, ir patikrinkite, ar lauko **Bandymo rezultatas** reikšmė pasikeitė į varnelę.
1. Pasirinkite **Tikrinti** ir uždarykite puslapį.
1. Grįžę į puslapį **Kokybės užsakymai** pasirinkite **Tikrinti** ir atlikite tikrinimą. Būsena atnaujinama į *Sėkminga*.

    > [!NOTE]
    > Tikrinimo įvykis suaktyvina kokybės užsakymo darbo, skirto perkelti kiekį iš kokybės kontrolės vietos į naują vietą, kūrimą.

1. Eikite į **Sandėlio valdymas \> Visi darbai**.
1. Pasirinkite ką tik sukurtą darbą ir atkreipkite dėmesį, kad sukurta antra kokybės užsakymo darbo antraštė, kur padėjimo vieta yra *BULK-001*.
1. Mobiliajame įrenginyje arba emuliatoriuje, kuriame veikia „Warehousing“ programa, prisijunkite prie 51 sandėlio įrašydami *51* į vartotojo ID vietą, o *1* – į slaptažodžo vietą.
1. Eikite į **Kokybė \> Padėti iš QMS** ir apdorokite kiekvieną iš dviejų numerio lentelių, susijusių su abiem darbais, kad visi darbai būtų uždaryti.

> [!NOTE]
> Apsvarstykite galimybę įtraukti perkėlimo iš kokybės kontrolės įrašą į mobiliojo įrenginio meniu elementą, kai veiklos kodas *Rodyti atidarytą užduočių sąrašą*. Pavyzdžiui, demonstraciniuose duomenyse yra mobiliojo įrenginio meniu elementas, pavadintas **Darbų sąrašas**. Pirmiausia į vartotojo nukreiptą meniu elementą įtraukite darbo klasę *Kokybės užsakymas*, nes šiai darbo klasei reikia, kad darbas būtų rodomas darbų sąraše. Tada darbo klasę *Kokybės užsakymas* įtraukite į meniu elementą **Darbų sąrašas**. Tada vartotojai, turintys prieigą prie darbų sąrašo, galės paimti ir apdoroti darbą, kuris automatiškai sugeneruojamas atliekant kokybės užsakymo tikrinimą.
