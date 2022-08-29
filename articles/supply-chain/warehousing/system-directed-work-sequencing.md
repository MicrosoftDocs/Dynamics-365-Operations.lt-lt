---
title: Sistemos nurodyta darbo seka
description: Šiame straipsnyje pateikiama informacija apie sistemos nurodytos darbo sekos seką. Ši funkcija leidžia rūšiuoti ir filtruoti darbo užsakymus, kuriuos sistema pateikia vartotojams vykdyti. Tai naudinga scenarijuose, kuomet reikia nurodyti papildomus kriterijus prekių paėmimo proceso vykdymui.
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 1dab8d8bdace046f0f061713600fd1eab69e7c12
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335472"
---
# <a name="system-directed-work-sequencing"></a>Sistemos nurodyta darbo seka

[!include [banner](../includes/banner.md)]

Sistemos nurodyta darbo seka leidžia rūšiuoti ir filtruoti darbo užsakymus, kuriuos sistema pateikia vartotojams vykdyti. Tai naudinga scenarijuose, kai prekių paėmimo proceso vykdymui reikia nurodyti papildomus kriterijus, pvz., siuntimo laiką, prekių paėmimo zoną, vietos profilį arba įvairių kriterijų derinį.

Ši funkcija išplečia dabartinę sistemos nurodyto paėmimo funkciją įtraukdama sistemos nurodytą užklausos užsakymą, kuriame vartotojai gali nustatyti seką ir vieną ar daugiau užklausų, įvertinančių visus sukurtus darbo užsakymus. Užfiksuoti ir pristatyti bus tik tie darbo užsakymai, kurie atitinka kriterijus, nurodytus mobiliojo įrenginio meniu elemento nustatyme.

Todėl ši funkcija leidžia tolimesnį prekių paėmimo procesų optimizavimą, kadangi identifikuoja darbo užsakymus, atitinkančius nurodytus kriterijus, priskiria juos tinkamam mobiliojo įrenginio meniu elementui ir pateikia juos darbuotojui, atsižvelgiant į įgūdžius, surinkimo įrangą ar kitą reikalavimą.

> [!NOTE]
> Jei reikalingi įvairūs kriterijai, turi būti naudojami keli mobiliojo įrenginio meniu elementai.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Organizacijoje naudojamos sistemos nurodytos darbo eigos funkcijos įjungimas

Kad būtų galima naudoti sistemos nurodyta darbo seką, jūsų sistemoje reikia įjungti funkciją. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Organizacijoje naudojama sistemos nurodyta darbo seka*

## <a name="setup"></a>Sąranka

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Norėdami dirbti naudodami scenarijų, naudodami šiame straipsnyje pateiktas vertes, turite dirbti su sistema, kurioje įdiegti standartiniai [demonstraciniai](../../fin-ops-core/fin-ops/get-started/demo-data.md) duomenys. Taip pat, turite pasirinkti **USMF** juridinį subjektą. Scenarijus naudoja *51* sandėlio demonstracinius duomenis.

> [!IMPORTANT]
> Prieš išleisdami užsakymus į sandėlį, įsitikinkite, kad prekių paėmimo vietose pakanka atsargų visiems užsakymams.
>
> Numatytieji USMF duomenys turi palaikyti šį scenarijų. Jeigu nenaudojate demonstracinių duomenų, patikrinkite parametrą **Vietos nurodymas** sužinoti kurios prekių paėmimo vietos yra naudojamos pardavimo užsakymo prekių paėmimui atlikti. Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba bet kokį kitą srautą.

### <a name="set-up-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu nustatymas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Mobiliojo įrenginio meniu elementų sąraše pasirinkite **Prekių paėmimas – Sistema**. Reikalingas meniu elementas jau turi būti. 
1. Patikrinkite šiuos parametrus:

    - „FastTab“ skirtuke **Bendra** laukas **Nurodoma** turi būti nustatytas į *Sistemos nurodoma*.
    - „FastTab“ skirtukas **Darbo klasės** turi rodyti šiuos parametrus.

        | Darbo klasės ID | Darbo užsakymo tipas |
        |---|---|
        | Pardavimai | Pardavimo užsakymai |
        | Pardavimo užsakymų paėmimas | Pardavimo užsakymai |

1. Veiksmų srityje pasirinkite **Sistemos nurodytos darbo sekos užklausos**.
1. Pasirinkite **Redaguoti**.
1. Panaikinkite esamą eilutę ir patvirtinkite veiksmą pasirinkdami **Taip**.
1. Veiksmų srityje pasirinkite **Nauja** eilutei sukurti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Sekos numeris:** *1*
    - **Aprašymo laukas:** *Darbo kiekis yra mažesnis nei 20 ir Mažėjimo tvarka*

1. Pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Skirtuke **Sujungimas** išplėskite jungties hierarchiją lentelei **Darbo eilutės** rodyti.
1. Pasirinkite **Darbo eilučių** lentelės sujungimą.
1. Pasirinkite **Pridėti lentelės sujungimą**.
1. Atsiradusiame sąraše suraskite ir pasirinkite eilutę su šiais parametrais:

    - **Sujungimo režimas:** *n:1*
    - **Ryšys:** *Vietos (Vieta)*

1. Pasirinkite **Pasirinkti**.

    Vietos pridedamos į lentelės sujungimą.

1. Skirtuke **Rūšiavimas** pasirinkite **Pridėti** naujai eilutei pridėti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Darbo kiekis* (atsiradusiame pranešimo lauke pasirinkite **Taip** rūšiavimui į šį lauką įtraukti.)
    - **Ieškos kryptis:** *Mažėjanti*

1. Pasirinkite skirtuką **Diapazonas**.

    Jei į seką reikia įtraukti tik specifinius darbo kriterijus, juos galima nurodyti skirtuke **Diapazonas**. Šiame pavyzdyje jūs norite įterpti tik tą darbą, kurio kiekis yra mažesnis nei 20 EA (mažiausias matavimo vienetas).

    Atkreipkite dėmesį, kad kai kurios eilutės jau įtrauktos. Nepašalinkite šių eilučių.

1. Pasirinkite **Įtraukti** eilutei įtraukti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Atsargų darbo kiekis*
    - **Kriterijai:** *\<20* (mažiau nei 20)

1. Pasirinkite **Įtraukti** dar vienai eilutei įtraukti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Darbo eilutės*
    - **Išvestinė lentelė:** *Darbo eilutės*
    - **Laukas:** *Darbo tipas*
    - **Kriterijai:** *Paėmimas*

1. Pasirinkite **Įtraukti** dar vienai eilutei įtraukti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Vietos*
    - **Išvestinė lentelė:** *Vietos*
    - **Laukas:** *Vietos profilio ID*
    - **Kriterijai:** *!ETAPAS*

        > [!IMPORTANT]
        > Įsitikinkite, kad šauktukas (*!*) yra prieš *ETAPĄ*.

1. Pasirinkite **Gerai** norėdami išsaugoti ir uždaryti užklausą.
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį, kad sugrįžtumėte į **Mobiliojo įrenginio meniu elementų** puslapį.

> [!NOTE]
> Šis nustatymas nurodo kriterijus, kurie bus naudojami norint pateikti tinkamus darbus mobiliojo įrenginio meniu elementui. Jei prie užklausos pridėsite daugiau kriterijų eilučių, pirmiausia sistema naudos užklausos eilutę, kurios sekos numeris yra mažiausias. Kitaip tariant, visi tinkami darbai, kurių sekos numeris yra 1, bus pristatyti vartotojui pirmiausia, o tada pristatyti visi 2 sekos numerio darbai. Todėl, jei tam tikrą diapazoną ir rūšiavimą reikia naudoti kartu, jie turi būti nurodyti toje pačioje sistemos nurodytos darbo sekos užklausoje.
>
> Atliekant šį nustatymą bus užfiksuojamas bet koks darbas, kurio bent vienoje eilutėje yra kiekis mažesnis nei 20 EA. Todėl, jei darbas turi eilutę, kurioje kiekis yra lygus 20 EA arba didesnis, jis bus tinkamas, jei jame yra bent viena eilutė, kurioje kiekis yra mažesnis nei 20 AE.

### <a name="location-directives"></a>Vietos nurodymai

Jei naudojate numatytuosius „Contoso“ duomenis, vietos nurodymų užklausos veiksmui nereikalingi pakeitimai. Tačiau, siekiant užtikrinti, kad vietos nurodymuose bus užfiksuotos pardavimų užsakymų prekės, taikydami priemonę ne „Contoso“ aplinkoje, sukurkite naują vietos nurodymą. Norėdami patikrinti parodomosios aplinkos nustatymus, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Vietos direktyvos**.
1. Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.
1. Pasirinkite vietos nurodymą pavadinimu *51 paėmimas*.
1. „FastTab“ skirtuke **Vietos direktyvos veiksmai** pasirinkite eilutę **Paėmimo** veiksmui.
1. Pasirinkite **Redaguoti užklausą** virš tinklelio.
1. Peržiūrėti **Diapazono** užklausą.

    1. Suraskite eilutę, kurioje **Laukas** yra nustatytas *Vieta*.
    2. Įsitikinkite, kad laukas **Kriterijai** yra tuščias, t. y., nėra apribojimų.

## <a name="scenario"></a>Scenarijus

### <a name="create-sales-order-picking-work"></a>Pardavimo užsakymo paėmimo darbo užduoties sukūrimas

Prieš vykdant sistemos nurodytą paėmimą, reikia sukurti kai kuriuos siuntimo darbus. Šiame scenarijuje sukursite keturis pardavimo užsakymus, pagrįstus nurodytomis sistemos nurodytos darbo sekos užklausomis.

Jūs rezervuosite atsargų kiekį kiekvienam pardavimo užsakymui. Todėl kitiems užsakymams rezervuotų atsargų iš sandėlio paimti negalima, jei atsargų rezervavimas arba dalis atsargų rezervavimo nėra atšaukti.

Tada išleisite kiekvieną pardavimo užsakymą į sandėlį siuntimo darbui sukurti.

#### <a name="sales-order-1"></a>Pardavimo užsakymas 1

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Nauja** sukurti pardavimo užsakymą 1.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas** lauką **Kliento paskyra** nustatykite į *US–004*.
    - Skirtuke **Bendra** lauką **Sandėlis** nustatykite į *51*.

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą. Pasižymėkite pardavimo užsakymo numerį.
1. Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9200*
    - **Kiekis:** *20*

1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** atsargų rezervavimui.
1. Uždarykite **Rezervavimas** puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį** sandėlio darbo užduočiai sukurti.

    Gausite informacinius pranešimus apie sandėlio bangos ID ir siuntos ID, sukurtus šiam pardavimo užsakymui.

#### <a name="sales-order-2"></a>Pardavimo užsakymas 2

1. Veiksmų srityje pasirinkite **Nauja** pardavimo užsakymui 2 sukurti.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-007*
    - **Sandėlis:** *51*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą. Pasižymėkite pardavimo užsakymo numerį.
1. Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9200*
    - **Kiekis:** *5*

1. Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9201*
    - **Kiekis:** *1*

1. Rezervuoti abiejų eilučių atsargas.
1. Išleisti pardavimo užsakymus i sandėlį.

#### <a name="sales-order-3"></a>Pardavimo užsakymas 3

1. Veiksmų srityje pasirinkite **Nauja** sukurti pardavimo užsakymą 3.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-009*
    - **Sandėlis:** *51*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą. Pasižymėkite pardavimo užsakymo numerį.
1. Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9200*
    - **Kiekis:** *7*

1. Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9202*
    - **Kiekis:** *8*

1. Rezervuoti abiejų eilučių atsargas.
1. Išleisti pardavimo užsakymus i sandėlį.

#### <a name="sales-order-4"></a>Pardavimo užsakymas 4

1. Veiksmų srityje pasirinkite **Nauja** 4 pardavimo užsakymui sukurti.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-010*
    - **Sandėlis:** *51*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą. Pasižymėkite pardavimo užsakymo numerį.
1. Įtraukite eilutę į naują pardavimo užsakymą ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9200*
    - **Kiekis:** *25*

1. Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *M9202*
    - **Kiekis:** *10*

1. Rezervuoti abiejų eilučių atsargas.
1. Išleisti pardavimo užsakymus i sandėlį.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Gauti darbo ID sukurtiems darbams

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Filtruokite lauką **Sandėlis,** kad būtų rodomas tik *51* sandėlio darbas.
1. Turėtų būti sukurti keturi darbo ID. Pasižymėkite kiekvieno pardavimo užsakymo darbo ID.

    | Pardavimo užsakymo ID | Darbo ID | Darbo kiekis |
    |---|---|---|
    | Pardavimo užsakymas 1 | Darbo ID 1 | 20 EA |
    | Pardavimo užsakymas 2 | Darbo ID 2 | 6 EA (abiejų eilučių suma) |
    | Pardavimo užsakymas 3 | Darbo ID 3 | 15 EA (abiejų eilučių suma) |
    | Pardavimo užsakymas 4 | Darbo ID 4 | 35 EA (abiejų eilučių suma) |

Prieš paleisdami mobiliojo įrenginio srautą, įsitikinkite, kad sukurtas darbo statusas yra *Atviras* *51* sandėliui ir *Pardavimo užsakymo* darbo užsakymo tipui. Kitu atveju tikrinimo rezultatai gali skirtis, nes sistemos nurodytas paėmimas apims visą tinkamą darbą.

1. Eikite į **Sandėlio valdymas \>Darbas \> Siunčiama \> Atviri pardavimo darbai**.
1. Filtruokite tinklelio **Atviri pardavimo darbai** lauką **Sandėlis,** kad būtų rodomas tik *51* sandėlio darbas.
1. Patikrinkite, ar rodomi tik keturi anksčiau sukurti darbo ID.
1. Uždarykite puslapį **Darbas**.

### <a name="mobile-device-flow-execution"></a>Mobiliojo įrenginio srauto vykdymas

Atsižvelgiant į nustatymą, sistema naudos vartotojo darbą, kuris yra surūšiuotas iš didžiausio darbo eilutės kiekio į žemiausią. Kiekis kiekvienoje eilutėje bus mažesnis nei 20 AE.

Atminkite, kad atliekant ši nustatymą bus užfiksuojamas bet koks darbas, kurio bent vienoje eilutėje kiekis yra mažesnis nei 20 EA. Todėl, jei darbas turi kitą eilutę, kurioje kiekis yra lygus 20 EA ar daugiau kaip 20 EA, jis taip pat bus galiojantis.

#### <a name="mobile-app"></a>Mobilioji programa

1. Prisijunkite prie „Warehouse“ programėlės kaip vartotojas sandėlyje *51*.
1. Eikite į **Išsiųsti \> Pardavimų išrinkimo sistema**.

    Pateiktas darbo ID *4* išrinkimo veiksmas. Šis darbo ID yra pateikiamas pirmiausia dėl sistemos nurodytos užklausų sekos nustatymo, kuriame nurodėte, kad darbas turi būti nustatytas pagal darbo eilutės kiekį mažėjimo tvarka.

1. Užpildykite reikiamą išrinkimą ir uždarykite darbo ID.

    Tada pristatomas *3* darbo ID. Viena iš darbo eilučių yra sekoje, kuri pagrįsta darbo eilutės kiekiu.

1. Užpildykite išrinkimą ir uždarykite darbo ID.

    Tada pristatomas *2* darbo ID. Ši darbo išrinkimo eilutė yra sekoje.

1. Užpildykite išrinkimą ir uždarykite darbo ID.

    Jums nereikia pateikti jokio tolesnio darbo. Darbo ID *1* neatitinka šio mobiliojo įrenginio meniu elemento, nes užklausa nurodo, kad darbo antraštės bus nagrinėjamos tik tuo atveju, jei darbo eilutėse esantis kiekis yra mažesnis nei 20 AE.

## <a name="tips"></a>Patarimai

Sistemos nukreiptos darbo sekos užklausos yra *imtinai*. Svarbu, kad atsimintumėte šį faktą kai kuriems nustatymams. Pavyzdžiui, jūs norite, kad tam tikras meniu elementas būtų vykdomas tik tada, kai darbo vienetas yra *EA* ir užklausoje nurodote, kad apribojimas būtų taikomas tik skirtuke **Diapazonas**. Tokiu atveju visas darbas, kurio bent viena darbo eilutė turi darbo vienetą, nustatytą *EA,* bus perduodamas darbuotojui. Todėl šis darbas taip pat gali apimti darbą, kurio darbo eilučių darbo vienetas nėra *EA* (pvz., *dėžė* arba *padėklas)*. Užklausa neįtrauks tik darbo, kurio eilutė neturi darbo vieneto, nustatyto *EA*.

Todėl, šio scenarijaus pavyzdyje, darbo ID *4* taip pat buvo užfiksuotas naudojant užklausą. Sukūrus užklausą, buvo pridėtos dvi eilutės: viena 25 EA ir kita 10 EA. Šis darbas vis dar pateikiamas vartotojui, nes bent vienoje darbo eilutėje yra mažiau nei 20 EA.

Atsižvelgiant į scenarijų, šios problemos galima išvengti naudojant darbo pertraukas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]