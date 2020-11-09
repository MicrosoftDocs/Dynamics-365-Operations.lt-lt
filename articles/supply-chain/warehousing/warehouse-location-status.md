---
title: Sandėlio vietos būsena
description: Šioje temoje pateikiama sandėlio vietos būsenos funkcijos apžvalga.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 31216c24f54f22ec928eb143d4a913aabcd50cf8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016015"
---
# <a name="warehouse-location-status"></a>Sandėlio vietos būsena

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ apima kelis vietos laukus, kurie suteikia lankstumo darbui su vietomis ir jų priežiūrai. Galite į vietos nurodymo užklausą įterpti vietos būsenas, kad būtų lengviau kontroliuoti sandėlio eigą.

Šie keturi puslapiai **Vietos** seka informaciją apie dabartinę vietos būseną. Šie laukai leidžia sandėlio vadovams peržiūrėti sandėlio vietų būseną. Jie taip pat leidžia išplėstas ataskaitas ir filtravimą.

- **Prekės numeris** – Prekė, kuri šiuo metu yra vietoje. Jeigu vietoje yra kelios prekės, šis laukas yra tuščias.
- **Paskutinė veiklos data ir laikas** – Paskutinės sandėlio operacijos, atliktos su vieta, laiko žyma.
- **Skirstymo pagal terminus data** – Vietos atsargų įvežimo į sandėlį data. Ši vertė apskaičiuojama pagal numerio lentelės skirstymo pagal terminus datą. Ji yra tiksli vietoms, kurių numerio lentelė yra sekamos, tačiau ji gali būti netiksli vietoms, kurių numerio lentelės nėra sekamos.
- **Vietos būsena** – Vietos būsena. Yra keturios galimos reikšmės yra:

    - **Nenustatyta** – Vietos profilis negali susekti būsenos. Todėl dabartinė būsena yra nežinoma.
    - **Tuščia** – Vietoje nėra atsargų.
    - **Paėmimas** – Siuntimo operacijos buvo atliktos pagal vietą, nes ji paskutinį kartą buvo tuščia.
    - **Laikymas** – Gavimo operacijos buvo atliktos pagal vietą, nes ji paskutinį kartą buvo tuščia.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Sandėlio vietos funkcijos įjungimas

Norėdami naudoti *Sandėlio vietos funkcijos* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Sandėlio vietos būsena*

## <a name="set-up-warehouse-location-status"></a>Nustatyti sandėlio vietos būseną

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Paruošti pavyzdinius duomenis, reikalingus pavyzdžio scenarijui

Prieš pradėdami dirbti pagal scenarijų, turite suaktyvinti pavyzdžio duomenis ir nustatyti šią funkciją, kaip aprašyta šiame skyriuje. Norėdami užbaigti pavyzdžio scenarijų, turite naudoti arba „Warehousing“ programą, arba naršykle pagrįstą emuliatorių. Čia pateikiami veiksmai naudoja „Warehousing“ programą. Veiksmai, skirti naršyklei pagrįstam emuliatoriui yra panašūs.

#### <a name="use-the-usmf-legal-entity"></a>Naudokite USMF juridinį subjektą

Norėdami dirbti pagal pavyzdžio scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

#### <a name="set-up-location-profiles"></a>Nustatyti vietų šablonus

Pavyzdiniame scenarijuje reikia paruošti du vietos šablonus.

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.
1. Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.
1. Pasirinkite **KROVINYS-06** profilį.
1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Įgalinti prekę vietoje** – Šią parinktį nustatykite kaip _Taip_.
    - **Įgalinti vietos veiklos datą ir laiką:** Nustatykite šią pasirinktį _taip_.
    - **Įgalinti vietos būseną** – Šią parinktį nustatykite kaip _Taip_.

    Šios pasirinktys kontroliuoja, ar nuorodos laukai vietoje yra aktyvūs.

1. Pakartokite 3-4 veiksmus, skirtus **PAĖMIMAS-06** profiliui.

> [!NOTE]
> Kai vietos šablono parametrai ( **Įgalinti prekę vietoje** , **Įgalinti vietos veiklą** , **Įgalinti vietos būseną** ) nustatyti į *Taip* , sistema iš karto atnaujina atitinkamas vietas, vykdydama užduotį *Sandėlio vietos būsenos nuolatinis tikrinimas*.

### <a name="scenario"></a>Scenarijus

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lango **Sukurti pirkimo užsakymą** „FastTab“ skirtuko **Tiekėjas** lauke **Tiekėjo paskyra** pasirinkite *104*.
1. „FastTab“ **Bendra** lauke **Sandėlis** pasirinkite *61*.
1. Pasirinkite **Gerai**.
1. Jūsų naujas pirkimo užsakymas (PU) yra atidarytas. Jis apima naują tuščią eilutę **Pirkimo užsakymo eilučių** tinklelyje. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** _A0002_
    - **Kiekis:** _5_

1. Dalyje Veiksmų sritis, skirtuko **Pirkimas** grupėje **Veiksmai** pasirinkite **Patvirtinti** pirkimo užsakymų patvirtinimui.
1. Mobiliajame įrenginyje eikite į **Gaunami \> Gautas pirkimas**.
1. Pasirinkite lauką **PU numeris** , įveskite ir patvirtinkite PU numerį.
1. Pasirinkite lauką **PREKĖ** įveskite prekės numerį *A0002* ir jį patvirtinkite.
1. Puslapyje **Kiekis** įveskite kiekį *5* ir patvirtinkite.

    Įvesti kiekį galima vienu iš šių būdų:

    - Pasirinkite pliuso ( **+** ) arba minuso ( **–** ) ženklo mygtuką norėdami pridėti arba atimti skaitinę reikšmę.
    - Pasirinkite tuščią lauką tarp pliuso ( **+** ) ir minuso ( **–** ) ženklų mygtukų, kad būtų galima atidaryti skaičių klaviatūrą.

1. Patvirtinkite prekės numerio *A0002* ir kiekio *5* pasirinkimą. Puslapio apačioje atsiranda pranešimas "Baigtas darbas".
1. Pasirinkite meniu mygtuką (kartais vadinamą Hamburger arba Hamburger mygtuku) viršutiniame dešiniajame kampe, tada pasirinkite **Atšaukti,** kad išeitumėte iš **Gauto pirkimo** ir grįžtumėte į **Gaunami** meniu.
1. Pirkimo užsakymo puslapyje pasirinkite **Darbo informaciją** virš **Pirkimo užsakymo eilučių** tinklelio.
1. Skirtuke **Bendra** atkreipkite dėmesį į **Darbo ID** ir **Tikslinės numerio lentelės ID** vertes, kurios buvo sukurtos.
1. Skyriuje **Eilutės** atkreipkite dėmesį į **Vietos** reikšmes *Paėmimo* ir *Padėjimo* darbų tipams.
1. Mobiliajame įrenginyje eikite į **Gavimas \> Gautas padėjimas**.
1. Pasirinkite lauką **ID** , įveskite ir patvirtinkite darbo ID.
1. Patvirtinkite dar kartą, kad užbaigtumėte *Paėmimo* užklausą.
1. Paspauskite viršutiniame dešiniajame puslapio kampe esantį meniu mygtuką, o paskui pasirinkite **Atlikta** *Paėmimo* darbui užbaigti.
1. Pasižymėkite padėjimo vietą ir patvirtinkite. Puslapio apačioje atsiranda pranešimas "Baigtas darbas".
1. Viršutiniame dešiniajame kampe pasirinkite meniu mygtuką, tada pasirinkite **Atšaukti,** jei norite išeiti iš **Pirkimo padėjimo** ir grįžti į **Gavimo** meniu.
1. Pasirinkite **Grįžti** norėdami sugrįžti į pagrindinį meniu.
1. „Dynamics 365 Supply Chain Management“ eikite į **Sandėlio tvarkymas \> Nustatymas \> Sandėlis  \> Vietos**.
1. Filtruoti **Vietą** ir įvesti padėjimo vietą iš pirkimo užsakymo darbo. Turėtumėte matyti šiuos rezultatus:

    - Stulpelyje **Vietos būsena** pateikiama *Saugyklos* reikšmė, nes paskutinė šios vietos operacija buvo padėjimas.
    - Stulpelyje **Prekės numeris** pateikiama reikšmė *A0002* , nes ta prekė buvo gauta ir įvesta į vietą.
    - Stulpelyje **Paskutinės veiklos data ir laikas** pateikiama datos ir laiko, kada darbas buvo baigtas vietoje, laiko žyma.

1. Mobiliajame įrenginyje eikite į **Kokybė \> Perkėlimas**.
1. Pasirinkite lauką **Vieta / LP** ir įveskite vietą, kurią pasižymėjote ankstesniuose veiksmuose.
1. Patvirtinkite rodomą informaciją. Pasižymėkite sugeneruotą numerio lentelės numerį.
1. Ekrane **Informacija** pasirinkite lauką **Vieta / LP** ir įveskite *06A07R2S1B* kaip vietą, į kurią norite perkelti prekę.
1. Ekrane **Informacija** patvirtinkite **LP** vertę (tikslinio numerio lentelės ID), kuri sugeneruojama automatiškai. Puslapio apačioje atsiranda pranešimas "Baigtas darbas".
1. Viršutiniame dešiniajame kampe pasirinkite meniu mygtuką, tada pasirinkite **Atšaukti,** jei norite išeiti iš **Perkėlimas** ir sugrįžti į **Kokybės valdymas** meniu.
1. Pasirinkite **Grįžti** norėdami sugrįžti į pagrindinį meniu.
1. „Dynamics 365 Supply Chain Management“ eikite į **Sandėlio tvarkymas \> Nustatymas \> Sandėlis  \> Vietos**.
1. Atnaujinkite **Vietos** puslapį ir iš naujo peržiūrėkite pradinę padėjimo vietą. Atkreipkite dėmesį, kad **Vietos būsenos** laukas dabar nustatytas kaip *Tuščias* , o **Prekės numerio** stulpelis yra tuščias.
1. Peržiūrėkite vietos *06A07R2S1B* įrašą ir atkreipkite dėmesį, kad **Būsenos** reikšmė buvo pakeista į *Saugyklą* ir laukai **Prekės numeris** ir **Paskutinės veiklos data ir laikas** atsinaujino.
1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lang **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite *US-002*.
1. Lauke **Sandėlis** pasirinkite *61*.
1. Pasirinkite **Gerai**.
1. Jūsų naujas pirkimo užsakymas yra atidarytas. Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** tinklelyje. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** _A0002_
    - **Kiekis:** _1_

1. „FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.
1. Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** užsakymo eilutės rezervavimui. Tada spustelėkite **Uždarymo** mygtuką ( **X** ) viršutiniame dešiniajame kampe puslapiui uždarykite.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. **Pardavimo užsakymo eilutės** skirtuke, virš tinklelio esančiame meniu **Sandėlis** pasirinkite **Darbo išsami informacija**.
1. Nukopijuokite **Darbo ID** vertę, kuri buvo sukurta.
1. Mobiliajame įrenginyje eikite į **Siuntimas \> Pardavimų išrinkimas**.
1. Pasirinkite lauką **ID** , įveskite ir patvirtinkite anksčiau nukopijuotą darbo ID.
1. Puslapyje **Pardavimo užsakymai: Paėmimas** laukas **LOC** pasiūlo paėmimo vietą kaip padėjimo vietą, kuri buvo sukurta anksčiau. Pasižymėkite vietą.
1. Pasirinkite lauką **Vieta** , įveskite ir patvirtinkite vietą.
1. Pasirinkite **LP** lauką, įveskite ir patvirtinkite numerio lentelės numerį, kurį pasižymėjote perkėlimo veiklos vykdymo metu.
1. Pasirinkite lauką **Prekė** įveskite prekės numerį *A0002* ir jį patvirtinkite.
1. Puslapyje **Kiekis** įveskite kiekį *1* ir jį patvirtinkite.

    Įvesti kiekį galima vienu iš šių būdų:

    - Pasirinkite pliuso ( **+** ) arba minuso ( **–** ) ženklo mygtuką norėdami pridėti arba atimti skaitinę reikšmę.
    - Pasirinkite tuščią lauką tarp pliuso ( **+** ) ir minuso ( **–** ) ženklų mygtukų, kad būtų galima atidaryti skaičių klaviatūrą.

1. Pasirinkite lauką **Tikslinės LP** , įveskite vartotojo nustatytą tikslinės numerio lentelės ID ir patvirtinkite.
1. Patvirtinkite dar kartą, kad užbaigtumėte paėmimo darbą. Puslapio apačioje atsiranda pranešimas "Baigtas darbas".
1. Viršutiniame dešiniajame kampe pasirinkite meniu mygtuką, tada pasirinkite **Atšaukti** paėmimo užduočiai atšauti ir sugrįžti į **Siuntimas** meniu.
1. „Dynamics 365 Supply Chain Management“ eikite į **Sandėlio tvarkymas \> Nustatymas \> Sandėlis  \> Vietos**.
1. Filtruoti **Vietą** ir įvesti paėmimo vietą iš pardavimo užsakymo darbo.
1. Atkreipkite dėmesį, kad laukas **Vietos būsena** vietai, iš kurios paimtas pardavimo užsakymo darbas, dabar nustatytas kaip *Paėmimas* , o **Paskutinės veiklos datos ir laiko** laukas buvo atnaujintas.

> [!NOTE]
> Vietos laukus atnaujina tik sandėlio operacijos. Jei atsargas perkeliate naudodami žurnalą ar kitus ne WHS procesus, laukai nebus atnaujinti.
