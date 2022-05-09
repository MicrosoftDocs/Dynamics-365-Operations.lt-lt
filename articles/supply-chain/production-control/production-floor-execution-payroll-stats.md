---
title: Rodyti atostogų balansus gamybos laiko vykdymo sąsajoje
description: Šioje temoje pateikiamas pavyzdis scenarijus, kuris parodo, kaip nustatyti Microsoft Dynamics 365 Supply Chain Management, kad ji naudos algalapio statistiką, kad galėtų pateikti darbuotojams šių metų atostogų balanso peržiūrą.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: a97858c72b0be50609cee552bd0635e2d68ea478
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648169"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Rodyti atostogų balansus gamybos laiko vykdymo sąsajoje

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamas pavyzdis scenarijus, kuris parodo, kaip nustatyti Microsoft Dynamics 365 Supply Chain Management, kad ji naudos algalapio statistiką, kad kiekvienam darbuotojui būtų pateikta šių metų atostogų balanso apžvalga. Darbuotojai gamybos laiko vykdymo sąsajoje galės matyti **savo** atostogų balansą dialogo lange Mano diena.

Šis scenarijus naudoja Danijos švenčių įstatymą, kuriame atostogų metai vyksta nuo rugsėjo 1 d. iki rugpjūčio 31 d. Tokiu atveju jūsų įmonė pasamdė naują darbuotoją ir likusių šių atostogų metų laikotarpiui suteiks 10 atostogų dienų balansą.

## <a name="turn-on-the-required-features"></a>Reikiamų funkcijų įjungimas

Norėdami vykdyti šį scenarijų, funkcijų valdymo funkcijai *turite įgalinti gamybos laiko vykdymo sąsajos rodinį* "Mano [diena"](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Norėdami gauti informacijos apie tai, kaip įgalinti šią ir kitas gamybos laiko vykdymo sąsajos funkcijas, žr [. Konfigūruoti gamybos laiko vykdymo sąsają](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį subjektą prieš pradedant.

## <a name="create-a-new-pay-type"></a>Naujo mokėjimo tipo kūrimas

Pradėkite kurdami naują mokėjimo *tipą,* seksiantį darbuotojų uždirbtų atostogų dienas (dar vadinamą jų atostogų *balansu*). Paprastai mokėjimo tipai naudojami darbuotojų atlyginimui apskaičiuoti. Tačiau čia sukurtas mokėjimo tipas bus naudojamas balansui skaičiuoti.

1. Eikite į **laiko ir lankomumo nustatymo \>\> algalapio \> mokėjimo tipus**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Mokėjimo tipas:** *5151-1*
    - **Aprašas: darbuotojo** *atostogų dienų skaitiklis*
    - **Įtraukti į eksportą:** *Nr.*

## <a name="update-the-pay-agreement"></a>Atnaujinti mokėjimo sutartį

Šiame skyriuje galite redaguoti esamą mokėjimo sutartį įtraukdami naują mokėjimo tipą ir nustatydami taisykles, apibrėžiančios, *kaip* koreguojamas kiekvieno darbuotojo atostogų balansas užregistravimo atostogų dienomis.

1. Eikite į **Laiko ir lankomumo \> nustatymo \> algalapio \> mokėjimo sutartis**.
1. Pasirinkite mokėjimo sutartį, kurioje norite nustatyti atostogų strategiją. (Jei dirbate su standartiniais USMF pavyzdiniai duomenimis, yra tik viena mokėjimo sutartis, *Žmogus*.)
1. Įsitikinkite, kad pasirinkta mokėjimo sutartis galioja šią datą. Jei dirbate su standartiniais USMF pavyzdiniai duomenimis, **·** *man*. mokėjimo sutarties lauke Iki datos gali būti nustatyta praeities data. Pakeiskite vertę, kad ateityje ji būtų po du ar daugiau.
1. Veiksmų srityje pasirinkite sutarties **eilutes**.
1. Mokėjimo sutarties **eilučių puslapio** Apžvalgos **"FastTab"** įrankių juostoje nustatykite šias vertes:

    - Pirmame išplečiamajame sąraše pasirinkite **pirmadienį**.
    - Antrame išplečiamajame sąraše pasirinkite **Neatvykimas**.

1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje lauke **Mokėjimo tipas** nustatykite šiam scenarijui sukurtą mokėjimo tipą (*5151-1*). Palikite visų kitų laukų numatytąsias vertes.
1. Kol dar pasirenkama nauja eilutė, Bendrajame **FastTab** nustatykite šias vertes:

    - **Neatvykimo kodas:** *atostogos*
    - **Naudoti fiksuotą kiekį:** *Taip*
    - **Konstanta:** *-1*

1. Veiksmų srityje pasirinkite Kopijuoti **dieną**.
1. Dialogo lange **Kopijuoti** dieną nustatykite šias vertes:

    - **antradienis**, trečiadienis **,** ketvirtadienis **ir** penktadienis: **taip** *·*
    - **Perrašyti:** *Taip*
    - **Neatvykimas:** *taip*

1. Pasirinkite **Gerai**.

## <a name="create-a-payroll-statistic-group"></a>Algalapio statistikos grupės kūrimas

*Atlyginimų statistikos grupės* naudojamos laikotarpio darbuotojų registracijų statistikai nustatyti. Šiame scenarijuje naudosite algalapio statistikos grupę atostogų dienų, kurias darbuotojai uždirba atostogų laikotarpiu, skaičiui apskaičiuoti. Danijoje atostogų laikotarpis prasideda rugsėjo 1 d. – rugpjūčio 31 d.

1. Eikite į **laiko ir lankomumo nustatymo \>\> algalapio \> statistikos grupes**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Atlyginimų statistikos grupė:** *OI*
    - **Aprašas: atostogų** *balansas*
    - **Perkėlimas:** *ne*

1. Kol nauja eilutė vis dar pasirinkta, veiksmų **srityje** pasirinkite Nustatymas.
1. Norėdami į **tinklelį** įtraukti eilutę, nustatymo puslapyje veiksmų **srityje** pasirinkite Naujas.
1. Naujoje eilutėje nustatykite mokėjimo **tipo lauką** į *5151-1*.
1. Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku **) Laikotarpio kodo** lauką, tada pasirinkite **Peržiūrėti informaciją**. Dabar galite nustatyti laikotarpio kodą, kurį priskirsite šiam laukui vėliau.
1. Norėdami į **tinklelį** įtraukti eilutę, puslapio Laikotarpio tipai veiksmų **srityje** pasirinkite Naujas.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Laikotarpio tipai:** *Year*
    - **Aprašas:** *atostogos metais*
    - **Dažnis:** *metai*

1. Kol nauja eilutė vis dar pasirinkta, veiksmų **srityje pasirinkite** Generuoti laikotarpius.
1. Dialogo lange **Generuoti** laikotarpius nustatykite šias vertes:

    - **Nurodyti laikotarpio pradžios datą:** *2021 m. rugsėjo 1 d.*
    - **Laikotarpio ilgis:** *5*

1. Pasirinkite **Gerai**.
1. Norėdami grįžti **į puslapį** Atlyginimų statistikos grupės, **uždarykite laikotarpio tipų** puslapį.
1. Nustatyti laikotarpio **kodo lauką** kaip ką tik sukurtą laikotarpio tipą (*YearYear*).

## <a name="create-a-statistical-balance-setup"></a>Statistinio balanso nustatymo kūrimas

Šiame skyriuje sukuriate statistinio *balanso nustatymą*, susietą su algalapio statistikos grupe, kurią sukūrėte ankstesniame skyriuje. Vėliau šį statistinio balanso nustatymą susiesite su gamybos **laiko vykdymo** sąsajos rodiniu Mano diena. Tada **rodinyje** Mano diena bus galima peržiūrėti mokėjimo tipo, priskirto susietai algalapio statistikos grupei, atostogų balansus.

1. Eikite į **laiko ir lankomumo nustatymo \> algalapio \> statistinio \> balanso nustatymą**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Atlyginimų statistikos grupė:** *OI*
    - **Išorinis pavadinimas: atostogų** *balansas*
    - **Nukrypimas:** *ne*

## <a name="create-a-manual-premium"></a>Premijos kūrimas rankiniu būdu

*Neautomatiniai* priedai paprastai naudojami siekiant suteikti darbuotojams papildomą mokestį už papildomą darbą. Tokiu atveju sukursite neautomatinį premiją, kurią galėsite naudoti pradiniam kiekvieno darbuotojo atostogų balansui nustatyti.

1. Eikite į **Laiko ir lankomumo nustatymo \> algalapio \>\> rankiniu būdu premijas**.
1. Veiksmų srityje pasirinkite Naujas, kad **įtraukumėte** įrašą.
1. Naujame įraše nustatykite šias vertes:

    - **Priedai:** *OI*
    - **Aprašas:** *darbuotojų atostogų balanso koregavimai*
    - **Mokėjimo tipas:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Nustatyti pradinį darbuotojo atostogų balansą ir koreguoti jį viena diena

Algalapio administratoriai naudoja puslapį **Tvirtinti** norėdami peržiūrėti ir patvirtinti darbuotojų kasdienes registracijas. Tokiu atveju, turėsite atlikti administratoriaus vaidmenį, kad būtų galima nustatyti pradinį darbuotojo atostogų balansą ir užregistruoti darbuotojo atostogų dienas.

1. Eikite į **Laiko ir lankomumo \> peržiūra ir patvirtinkite \> Patvirtinti**.
1. Dialogo lange **Patvirtinti** nustatykite šiuos laukus:

    - **Patvirtinimo grupė** – pasirinkite patvirtinimo grupę, kuriai priklausote. (Jei dirbate su standartiniais USMF pavyzdiniai duomenimis, yra tik viena patvirtinimo grupė, *AdmMan*.)
    - **Peržiūrėti visą grupę, 1 dieną** – pasirinkite pasirinktį ir tada nustatykite lauką į esamą datą.

1. Pasirinkite **Gerai**.
1. Puslapyje **Patvirtinti** rodomas jūsų kriterijus atitinkančių įrašų sąrašas. Pasirinkite darbuotoją, kurį norite patvirtinti. Jei dirbate su standartiniais USMF pavyzdiniai duomenimis, pasirinkite darbuotojo *000496* (*Turi būti Portra*).
1. Suteikti pasirinktam darbuotojui 10 dienų atostogų:

    1. Kol darbuotojas vis dar pasirenkamas, veiksmų **srityje pasirinkite** Priedų eilutes.
    1. Priedų eilučių **puslapyje**, veiksmų srityje, pasirinkite Naujas, kad **įtraukumėte** eilutę į tinklelį.
    1. Naujoje eilutėje nustatykite šias vertes:

        - **Priedai:** *OI*
        - **Kiekis:** *10*

    1. Uždarykite **priedų eilučių** puslapį.

1. **Puslapyje Patvirtinti užregistruokite** faktą, kad darbuotojas šią dieną naudojo vieną iš atostogų dienų:

    1. Kol darbuotojas vis dar pasirenkamas, apatinėje puslapio dalyje, **skirtuke** Peržiūra, įrankių juostoje pasirinkite Naujas, **kad** į tinklelį įtraukumėte eilutę.
    1. Naujoje eilutėje nustatykite šias vertes:

        - **Žurnalo registracijos tipas: neatvykimas** *·*
        - **Nuoroda:** *atostogos*

    1. Viršutinėje puslapio dalyje įrankių juostoje pasirinkite Perkelti **,** norėdami pritaikyti atostogų balansą ir apskaičiuoti atskaitymą.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfigūruoti gamybos laiko vykdymo sąsają, kad joje būtų dialogo langas Mano diena

Šiame skyriuje, jūs įtraukiate mygtuką Mano **diena** į gamybos laiko vykdymo sąsają. Darbuotojai gali naudoti šį mygtuką, norėdami atidaryti dialogo **langą Mano** diena.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**.
1. Pasirinkite konfigūraciją, pvz., *Numatytoji*.
1. Veiksmų srityje pasirinkite skirtukus **Dizainas**.
1. **Skirtuko Dizainas puslapyje** sąrašo srityje pasirinkite Visos užduotys, *kad būtų* galima peržiūrėti to skirtuko parametrus. Dabar **pagrindiniame rodinio** lauke turi būti rodoma visų *užduočių vertė*.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Antrinės **įrankių juostos** "FastTab", stulpelyje **Galimi veiksmai**, pasirinkite **Mano diena**. Tada pasirinkite rodyklės dešinėn mygtuką, jei norite perkelti jį į stulpelį **Pasirinkti** veiksmai.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Patikrinkite savo balansą gamybos laiko vykdymo sąsajoje

Šiame skyriuje, jūs prisiregistruosite prie gamybos laiko vykdymo sąsajos kaip darbuotojas, kurio atostogų laiką nustatote anksčiau. Tada atidarysite dialogo **langą Mano diena**, kad galėsite peržiūrėti savo atostogų balansą.

1. Eikite į **Gamybos kontrolės \> nustatymas \> Gamybos vykdymas \> Gamybos laiko vykdymas**.
1. Jei jus paragins pasirinkti konfigūraciją, pasirinkite konfigūraciją, kurią nustatėte anksčiau šiame scenarijuje (*Numatytoji*).
1. Prisiregistruokite kaip vartotojas, kurį anksčiau nustatėte šiame scenarijuje. Jei dirbate su standartiniais USMF pavyzdiniai duomenimis, *turite turėti galimybę prisiregistruoti įvesdami 123* į **bado ID lauką**. Šis bado ID atitinka Jav Portra.
1. Pasirinkite **Mano diena kairiojoje** įrankių juostoje.
1. Tikrinti dialogo **lango balansų** skyrių. Šiame skyriuje dabar turi būti rodomas devynių atostogų dienų balansas.
