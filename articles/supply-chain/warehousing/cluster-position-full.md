---
title: Klasterio padėtis pilna
description: Šioje temoje pateikiama informacija apie funkciją Klasterio padėtis pilna. Ši funkcija suteikia alternatyvą griežtesniam darbo paskirstymo taisyklių vykdymui, kai naudojamas klasterio paėmimas, nes ji leidžia didesnę konteinerių ar krepšių tūrinių apribojimų paklaidos ribą.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a23168b550bfa2bb6a51c8df5d0a558431c23ebb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574262"
---
# <a name="cluster-position-full"></a>Klasterio padėtis pilna

[!include [banner](../includes/banner.md)]

Funkcija *Klasterio padėtis pilna* suteikia alternatyvą griežtesniam darbo paskirstymo taisyklių vykdymui, kai naudojamas klasterio paėmimas, nes ji leidžia didesnę konteinerių ar krepšių tūrinių apribojimų paklaidos ribą. Įprastu atveju ne visos darbo užsakymo prekės telpa į pasirinktą konteinerį. Sandėlio darbuotojai, vykdantys klasterio paėmimą, tokiu atveju turi mažai pasirinkimų: jie turi pakeisti konteinerio dydį į didesnį arba dirbti su prižiūrėtoju, kad sugalvotų kitą sprendimo būdą.

Ši funkcija teikia galimybę vykdyti mygtuką **Pilnas** viename iš klasterio darbo vienetų. Senesnėse versijose ši parinktis buvo pasiekiama įprastų užsakymų paėmimui, o ne klasterių paėmimui. Tačiau ši funkcija skiriasi nuo standartinio mygtuko **Pilnas** tuo, kad ji atšaukia likusį darbą. Ji nesiūlo vartotojui įtraukti kitos dėžės į tą patį klasterį ir automatiškai nesukuria naujo darbo.

## <a name="turn-on-the-cluster-position-full-feature"></a>Funkcijos Klasterio padėtis pilna įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Klasterio padėtis pilna*

## <a name="setup"></a>Sąranka

Šiame skyriuje pateikiamos gairės ir pavyzdys, rodantis, kaip nustatyti ir naudoti funkciją *Klasterio padėtis pilna*.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Tam, kad dirbtumėte su [pavyzdiniu scenarijumi](#example-scenario) naudodami pavyzdinius įrašus ir vertes nurodytas čia, turite būti sistemoje, kurioje standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yra įdiegti. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Taip pat galite naudoti pavyzdinį scenarijų kaip darbo su šia funkcija gamybos sistemoje instrukcijas. Tačiau tokiu atveju turite pakeisti čia aprašytus parametrus jūsų pačių reikšmėmis.

### <a name="cluster-profiles"></a>Klasterio šablonai

Turite nurodyti, ar klasterių ID sugeneruojami automatiškai, kiek padėčių naudojama, kai klasteriai skaidomi, ir kaip nustatoma paėmimo darbų seka bei vykdomas jų tikrinimas.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Klasterio šablonai**.
1. Sąrašo srityje pažymėkite įrašą **Kurti klasterį**.
1. „FastTab” **Bendra** patikrinkite toliau pateiktas reikšmes.

    - **Generuoti klasterio ID:** *Taip*
    - **Aktyvinti padėtis:** *Taip*
    - **Padėčių skaičius:** *2*
    - **Padėties pavadinimas:** *Skaitinis*
    - **Skaidyti klasterį:** *Dėti*
    - **Rūšiavimo patikros tipas:** *Padėties nuskaitymas*

1. „FastTab” **Klasterio rūšiavimas**. Tinklelis turėtų būti tuščias (t. y., jame turi nebūti jokių eilučių).

### <a name="work-templates"></a>Darbo šablonai

Turite nurodyti, kaip kuriamas klasterio paėmimo darbas.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Puslapio viršuje nustatykite lauką **Darbo užsakymo tipas** į *Pardavimo užsakymai*.
1. Įsitikinkite, kad išvardyti toliau pateikti demonstracinių duomenų darbo šablonai. Jei jų nėra, negalėsite užbaigti scenarijaus.

    - 61 SO surinkimo vieta
    - 61 SO klasterio paėmimas

### <a name="location-directives"></a>Vietos nurodymai

Turite nurodyti, iš kur prekės yra paimamos ir kur jos padedamos.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Sąrašo antraštėje nustatykite lauką **Darbo užsakymo tipas** į *Pardavimo užsakymai*.
1. Įsitikinkite, kad išvardytos toliau pateiktos demonstracinių duomenų pardavimų užsakymų direktyvos. Jei jų nėra, negalėsite užbaigti scenarijaus.

    - 61 klasterio paėmimas
    - 61 SO paėmimo užsakymas

### <a name="mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementai

Turite sukonfigūruoti mobiliojo įrenginio meniu elementą, kad galėtumėte naudoti esamą darbą, kurį nukreipė klasterio paėmimas. Klasterio paėmimo mobiliojo įrenginio meniu elemento parametras **Leisti darbo skaidymą** turi būti įjungtas ir turi būti įtraukta darbo klasė *SO paėmimas*.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sąrašo srityje pažymėkite įrašą **Klasterio paėmimo kūrimas**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Nukreipė:** *Klasterio paėmimas*
    - **Generuoti numerio lentelę:** *Taip*
    - **Leisti darbo skaidymą:** *Taip*
    - **Klasterio profilio ID:** *Kurti klasterį*

    Priimkite numatytąsias vertes visuose kituose laukuose.

1. „FastTab” **Darbo klasės** įtraukite dvi toliau pateiktas eilutes, kaip nurodyta.

    - 1 eilutė (dažniausiai pateikiama demonstraciniuose duomenyse):

        - **Darbo klasės ID:** *Pardavimai* 
        - **Darbo užsakymo tipas:** *Pardavimų užsakymai*

    - 2 eilutė (tikriausiai nepateikiama demonstraciniuose duomenyse):

        - **Darbo klasės ID:** *SO paėmimas*
        - **Darbo užsakymo tipas:** *Pardavimų užsakymai*

1. Veiksmų srityje eikite į **Darbo patvirtinimo sąranka**.
1. Pasirinkite **Redaguoti**.
1. Tinklelio eilutėje įveskite toliau nurodytas reikšmes.
    - **Darbo tipas** - *Paėmimas*
    - **Produkto patvirtinimas** - *Pasirinkti žymės langelį*

1. Veiksmų srityje pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-picking-work"></a>Paėmimo darbo kūrimas

Prieš pradedant klasterio paėmimą, turite sukurti siuntimo darbą. Anksčiau sukurtame klasterio profilyje nurodytos dvi klasterio padėtys. Todėl turi būti sukurti bent du pardavimų užsakymo paėmimo darbo ID. Pagal šį scenarijų operacijos įvyks *61* sandėlyje ir bus naudojamos prekės *L0101* ir *T0100*. Demonstraciniuose duomenyse turi būti pakankamai šių prekių turimų atsargų. Įsitikinkite, kad turite pakankamai atsargų operacijoms atlikti.

### <a name="create-sales-order-1"></a>1 pardavimo užsakymo kūrimas

1. Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Norėdami sukurti 1 pardavimo užsakymą, pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-010*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai**.
1. Naujas pardavimo užsakymas yra atidarytas. **Prekybos užsakymai** „FastTab“, įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Prekės numeris:** *T0100*
    - **Kiekis:** *5*

1. „FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.
1. „FastTab” **Pardavimo užsakymo eilutės** įtraukite antrą eilutę, kurioje yra toliau pateikti parametrai.

    - **Prekės numeris:** *L0101*
    - **Kiekis:** *20*

1. „FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.
1. Kiekvienai eilutei, kurią įtraukėte, atlikite toliau pateiktus veiksmus siekiant rezervuoti atsargas.

    1. Pasirinkite eilutę rezervavimui.
    2. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
    3. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.
    4. Uždarykite **Rezervavimas** puslapį.

1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Kai išleidimas bus atliktas, gausite informacinį pranešimą, kuriame bus rodomi sukurti bangos ir krovinio ID.

### <a name="create-sales-order-2"></a>Pardavimo užsakymo 2 sukūrimas

1. Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Norėdami sukurti 2 pardavimo užsakymą, pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-011*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai**.
1. Naujas pardavimo užsakymas yra atidarytas. **Prekybos užsakymai** „FastTab“, įtraukite eilutę, kuri turi šiuos nustatymus:

    - **Prekės numeris:** *L0101*
    - **Kiekis:** *20*

1. „FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.
1. „FastTab” **Pardavimo užsakymo eilutės** įtraukite antrą eilutę, kurioje yra toliau pateikti parametrai.

    - **Prekės numeris:** *T0100*
    - **Kiekis:** *2*

1. „FastTab” **Eilutės informacija** skirtuke **Pristatymas** nustatykite lauką **Patvirtinta siuntimo data** į šiandienos datą.
1. Kiekvienai eilutei, kurią įtraukėte, atlikite toliau pateiktus veiksmus siekiant rezervuoti atsargas.

    1. Pasirinkite eilutę rezervavimui.
    2. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
    3. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.
    4. Uždarykite **Rezervavimas** puslapį.

1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Kai išleidimas bus atliktas, gausite informacinį pranešimą, kuriame bus rodomi sukurti bangos ir krovinio ID.

### <a name="get-work-ids-and-license-plate-numbers"></a>Darbo ID ir numerio lentelių gavimas

Turėjo būti sukurti du darbo ID, kurių kiekviename yra dvi paėmimo eilutės. Norėdami rasti darbo ID ir numerio lenteles, atlikite toliau pateiktus veiksmus.

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Tinklelyje **Apžvalga** ieškokite dviejų pardavimo užsakymų, kuriuos sukūrėte, stulpelio **Užsakymo numeris**. Pasižymėkite kiekvieno pardavimo užsakymo atitinkamą darbo ID.
1. Pasirinkite kiekvieno pardavimo užsakymo eilutę, kad tinklelyje **Eilutės** būtų rodoma susijusi informacija. Pasižymėkite kiekvienos prekės vietą, kur ji bus paimta.
1. Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.
1. Veiksmų srityje pasirinkite **Dimensijos**, kad būtų atidarytas dialogo langas **Dimensijų rodymas**.
1. Patikrinkite, ar pažymėti žymės langeliai **Numerio lentelė**, **Sandėlis** ir **Prekės numeris**, tada pasirinkite **Gerai**.
1. Srityje **Filtras**, nustatykite toliau nurodytus filtrus.

    - **Prekės numeris** – **vienas iš dviejų** – *L0101* arba *T100*
    - **Sandėlis** – **prasideda** – *61*

1. Pasižymėkite rodomas **numerio lentelės** reikšmes.

## <a name="example-scenario"></a><a name="example-scenario"></a>Pavyzdinis scenarijus

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Mobiliojo įrenginio srauto vykdymas – produkto darbo patvirtinimo sąranka

1. Prisijunkite prie sandėlio mobiliųjų įrenginių programėlė kaip vartotojas sandėlyje *61*.
1. Eikite į **Siuntimas \> Klasterio paėmimo kūrimas**.

    Atidaromas puslapis **UŽDUOTIS. Darbo priskyrimas klasteriui**.

1. Įveskite 1 pardavimo užsakymo ID, kad priskirtumėte jį 1 klasterio padėčiai.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Įveskite 2 pardavimo užsakymo ID, kad priskirtumėte jį 2 klasterio padėčiai.
1. Pasirinkite **Gerai** (varnelės simbolis).

    Atidaromas puslapis **UŽDUOTIS. Klasterio paėmimo kūrimas. Paėmimas** ir rodoma *Prekė L0101 2 PL*.

Kadangi klasterio profilyje padėčių skaičius nustatytas į 2, sistema automatiškai nukreipia į pirmą konsoliduotąjį paėmimą: du prekės *L0101* padėklai (PL).

Bet kuriuo toliau pateiktų veiksmų metu galite pasirinkti skirtuką **Išsami informacija**, norėdami peržiūrėti informaciją apie užduotį, pvz., paėmimo vietą.

1. Nustatykite lauką **PREKĖ** į *L0101*. Tai patvirtina prekės numerį, reikalingą šiam meniu elementui (tai sukonfigūravote anksčiau, pasirinkę **Darbo patvirtinimo sąranka** puslapyje **Mobiliojo įrenginio meniu elementas**, kurdami šį meniu elementą).
1. Įveskite numerio lentelės numerį, susietą su preke, jos paėmimo vietoje. Pasiimsite du padėklus.
1. Nustatykite lauką **LP** į *LP\_PAĖMIMAS\_01*.
1. Pasirinkite **Gerai** (varnelės simbolis).

    Atidaromas puslapis **UŽDUOTIS. Rūšiavimas. Klasterio paėmimo kūrimas**. Jame rūšiuosite du paimamus padėklus į paėmimo padėtį. Ši padėtis gali būti krepšys ar konteineris, naudojamas atskirti paimamas atsargas pagal pardavimo užsakymą.

1. Peržiūrėkite rodomą prekės (*L0101*) ir kiekio (*20* vnt.) išsamią informaciją, kuri bus rūšiuojama į 1 padėtį (1 pardavimo užsakymo).
1. Nustatykite lauką **PADĖTIES PAVADINIMAS** į *1*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Peržiūrėkite rodomą prekės (*L0101*) ir kiekio (*20* vnt.) išsamią informaciją, kuri bus rūšiuojama į 2 padėtį (2 pardavimo užsakymo).
1. Nustatykite lauką **PADĖTIES PAVADINIMAS** į *2*.
1. Pasirinkite **Gerai** (varnelės simbolis).

    Atidaromas puslapis **UŽDUOTIS. Klasterio paėmimo kūrimas. Paėmimas** ir rodoma *Prekė T0100 7 vnt*.

Pagal šį scenarijų 1 padėtis negali priimti viso prekių, kurias reikia paimti siekiant atlikti 1 pardavimo užsakymą, kiekio. Padėtis turi būti pažymėta kaip pilna. Pagal šį scenarijų atliksite antros prekės paėmimą dalimis. Antra prekė bus paimta dalimis pagal 1 padėtį ir bus sukurtas naujas darbas, kad būtų paimtas likęs kiekis ir atliktas užsakymas.

1. Pasirinkite mygtuką Meniu (kartais vadinamą mėsainiu arba mėsainio mygtuku) ir tada pasirinkite **Padėtis pilna**.
1. Nurodykite pilną padėtį ir pasirinkite *1*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Įveskite paėmimo kiekį, kurį galima paimti su 1 padėtimi. Sistema gali nustatyti, kuris prekės numeris paimamas.
1. Įveskite *2*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Patvirtinkite prekės numerį, kad užbaigtumėte likusios prekės paėmimą su 2 padėtimi.
1. Nustatykite lauką **PREKĖ** į *T0100*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Įveskite numerio lentelę, iš kur prekė paimama, nustatydami lauką **LP** į *LPREPL04*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Peržiūrėkite rodomą prekės (*T0100*) ir kiekio (*2* vnt.) išsamią informaciją, kuri bus rūšiuojama į 2 padėtį (2 pardavimo užsakymo).
1. Nustatykite lauką **PADĖTIES PAVADINIMAS** į *2*.
1. Pasirinkite **Gerai** (varnelės simbolis).
1. Peržiūrėkite rodomą prekės (*T0100*) ir kiekio (*2* vnt.) išsamią informaciją, kuri bus rūšiuojama į 1 padėtį (1 pardavimo užsakymo).
1. Nustatykite lauką **PADĖTIES PAVADINIMAS** į *1*.
1. Pasirinkite **Gerai** (varnelės simbolis).

    Atidaromas puslapis **UŽDUOTIS. Klasterio paėmimo kūrimas. Padėjimas**.

Pagal šį scenarijų klasterio paėmimas užbaigiamas ir vartotojas nukreipiamas padėti paimamas 1 padėties ir 2 padėties prekes į surinkimo vietą *STAGE01*.

1. Peržiūrėkite puslapio informaciją. Rodoma, kad bendras kiekis, kuris yra *44*, bus padėtas į surinkimo vietą.
1. Pasirinkite **Gerai** (varnelės simbolis).

    Bus pateiktas pranešimas „Klasteris užbaigtas”.

Dabar galite naudoti meniu elementą **Pardavimo paėmimas**, norėdami paimti likusį kiekį. Tada galite naudoti meniu elementą **Pardavimo krovimas**, norėdami perkelti prekes iš surinkimo vietos į krovimo rampą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]