---
title: Papildomo krovinio kūrimas bangos metu
description: Šioje temoje pateikiama informacija apie papildomo bangos krovinio kūrimą, kuris automatiškai priskiria siuntas esamoms bangoms vykdant bangą. Todėl galite sukurti prasmingus krovinius, kurie vaizduoja sunkvežimius, nenaudodami krovinio planavimo darbo srities.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 7f51b3d65c8dd1e11296956c37ef9dfe568e5ec2
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654203"
---
# <a name="advanced-load-building-during-wave"></a>Papildomo krovinio kūrimas bangos metu

[!include [banner](../includes/banner.md)]

Papildomas bangos krovinio kūrimas automatiškai priskiria siuntas esamoms bangoms vykdant bangą. Todėl galite sukurti prasmingus krovinius, kurie vaizduoja sunkvežimius, nenaudodami krovinio planavimo darbo srities. Ši galimybė naudinga įmonėms, kurios nori naudoti krovinio koncepciją sekti ir planuoti krovinių siuntimą sunkvežimyje/priekaboje, bet kurios nenori rankiniu būdu sukurti tų krovinių kiekvieną dieną.

Apdorojant bangą, sistema paprastai sukuria naują kiekvienos siuntos krovinį, kuriam nepriskirtas joks krovinys. Tačiau įjungus papildomo bangos krovinio kūrimą, sistema priskiria kiekvieną nepriskirtą siuntą esamam kroviniui (jei atitinkamas krovinys yra) ir nauji kroviniai sukuriami pagal poreikį. Papildomo bangos krovinio kūrimas automatiškai sukuria naujus krovinius, pagrįstus jūsų nustatytais kriterijais.

Norėdami naudoti šią funkciją, turite nustatyti sistemą taip:

- Sukurkite *bangos šablonai*, kuriuose yra naujas **kurtiKrovinius** metodas. Šis metodas padaro prieinamą papildomą bangos krovinių kūrimą bangoms, naudojančioms tuos šablonus.
- Nustatykite *įkelti kūrimo šablonus šablonus*, kurių kiekvienas yra susijęs su konkrečiu bangos šablonu ir metodu. Paleiskite kūrimo šablonų valdiklį, kuris įkelia (esamas arba naujas) krovinio eilutes, esančias bangoje arba pridėtas. Galite sujungti arba atskirti siuntas, remiantis kriterijais, pvz., krovinio šablonu, įranga ir kitomis lauko vertėmis krovinio eilutėje.
- Nustatykite *įkelti mišrias grupes*, kad valdytumėte, kurios prekės turėtų ir neturėtų būti sujungtos į vieną krovinį. Taip pat nurodote, ar dėl apribojimo turi atsirasti įspėjimas arba klaida, ir ar turi būti įvertintas krovinio šablono tūrio matavimo apribojimas.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Įjunkite papildomo bangos krovinio kūrimą savo sistemoje

Prieš jums naudojantis papildomo bangos krovinio kūrimo funkcija, įjunkite dvi funkcijas savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų šių funkcijų būseną ir jas įjungtų, jei būtina. Darbo srityje **Funkcijų valdymas** funkcijos išvardintos šia tvarka:

- Bangos krovinio kūrimo funkcija:

    - **Modulis:** *sandėlio valdymas*
    - **Funkcijos pavadinimas:** *Bangos krovinio kūrimo funkcija*

- Organizacijos bangos žingsnio kodas:

    - **Modulis:** *sandėlio valdymas*
    - **Funkcijos pavadinimas:** *Organizacijos bangos žingsnio kodas*

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti su parodomąja versija, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Taip pat galite naudoti šią parodomąją versiją kaip vedlį, kaip naudotis funkcija dirbant gamybos sistemoje. Tačiau tokiu atveju, Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Įsitikinkite, kad scenarijaus sąrankoje yra pakankamai galimų atsargų

Jei dirbate su **USMF** parodomosios versijos duomenimis, pirmiausia turite įsitikinti, kad jūsų sistema nustatyta taip, kad kiekvienoje atitinkamoje vietoje yra pakankamai atsargų. Šia parodomąja versija numanoma, kad šių atsargų yra *62* sandėlyje:

- **Prekė A0001:** 10 vnt.
- **Prekė A0002:** 10 vnt.
- **Prekė M9200:** 10 EA

Prekė **M9200** turi būti pridėta sandėlyje. Norėdami pridėti prekių atsargas, atlikite toliau esančiuose poskyriuose nurodytas procedūras.

#### <a name="create-a-new-license-plate-id"></a>Naujos numerio lentelės ID kūrimas

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Sandėlis** \> **Numerių lentelės**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujojoje eilutėje **Numerio lentelė** lauke įveskite *LP6203*.
1. Pasirinkite **Įrašyti**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Prekės M9200, esančios 6 svetainėje, įprastinės kainos nustatymas

1. Eikite į **Produkto informacijos valdymas** \> **Produktai** \> **Patvirtinti produktai**.
1. Ieškoti **M9200**.
1. Pasirinkite prekės eilutę, tada Veiksmų srityje, **Tvarkyti kainas** skirtuke **Nustatyti** grupėje pasirinkite **Prekės kaina**.
1. **Prekės kaina** puslapyje pasirinkite **Laukiamos kainos** skirtuką.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Įkainojimo tipas:** *Numatoma kaina*
    - **Kainos tipas:** *Savikaina*
    - **Versija:** *10*
    - **Vieta:** *6*
    - **Kaina:** *1,60*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Aktyvinti numatomą (-as) kainą (-as)**.
1. Pasirinkite **Aktyvios kainos** skirtuką, kad patikrintumėte, kad nauja savikaina *6* pridėta svetainėje.

#### <a name="create-inventory-in-warehouse-62"></a>Atsargų kūrimas sandėlyje Nr. 62

1. Eikite į **Atsargų valdymas** \> **Žurnalo įrašai** \> **Prekės** \> **Atsargų koregavimas**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lango **Sukurti atsargų žurnalą** esančiame **Apžvalga** „FastTab” skirtuke **Sandėlis** lauke įveskite *62*. Priimkite numatytąsias vertes visuose kituose laukuose.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. **Atsargų koregavimas** puslapis atvertas. **Žurnalo eilutės** „FastTab” skirtuke pasirinkite **Nauja**, kad pridėtumėte naują eilutę.
1. Naujoje eilutėje nustatykite šias reikšmes: Priimkite numatytąsias vertes visuose kituose laukuose.

    - **Prekės numeris:** *M9200*
    - **Vieta:** *masinis-003*
    - **Kiekis:** Pakeiskite vertę į *10*.

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Tikrinti**, kad patikrintumėte, ar nėra klaidų.
1. Dialogo lange **Tikrinti žurnalą** pasirinkite **Gerai**, kad pradėtumėte patikrinimą. Kai čekis baigiamas, gaunamas pranešimas.
1. Veiksmų srityje pasirinkite **Registruoti**, kad atliktumėte atsargų koregavimą.
1. Dialogo lange **Registruoti žurnalą** pasirinkite **Gerai**, kad pradėtumėte registravimą. Kai registravimas baigiamas, gaunamas pranešimas.

## <a name="set-up-advanced-wave-load-building"></a>Nustatykite papildomo bangos krovinio kūrimą

### <a name="regenerate-wave-process-methods"></a>Iš naujo generuokite bangos procesų metodus

Gali tekti iš naujo sugeneruoti savo bangos procesų metodus, kad padarytumėte prieinamą krovinio kūrimo metodą (**kurtiKrovinius**).

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Bangos** \> **Bangos procesų metodai**.
2. Patikrinkite, ar **kurtiKrovinius** yra sąraše. Jei nėra, pasirinkite **Iš naujo generuoti metodus** Veiksmų srityje, kad pridėtumėte.

### <a name="set-up-wave-templates"></a>Bangų šablonų nustatymas

Norėdami pasinaudoti papildomo bangos krovinio kūrimo privalumais, turite įtraukti **kurtiKrovinius** metodą kiekviename atitinkame [bangos šablone](tasks/configure-wave-processing.md).

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Bangos** \> **Bangų šablonai**.
1. Pasirinkite bangos šabloną.

    Jei dirbate su **USMF** parodomąja versija, pasirinkite **62 siuntos numatytasis nustatymas** šabloną.

1. Veiksmų srityje pasirinkite **Redaguoti**, kad pakeistumėte puslapio režimą į redagavimo.
1. **Metodai** „FastTab” skirtuke **Likusieji metodai** tinklelyje pasirinkite **kurtiKrovinius** metodą.
1. Pasirinkite dešinės rodyklės mygtuką, kad perkeltumėte **kurtiKrovinius** metodą į **Pasirinkti metodai** tinklelį.
1. Norėdami priskirti **Bangos žingsnio kodas** vertę, skirtą **kurtiKrovinius** metodą, pirmiausia, sukurkite kodą **Bangų žingsnių kodai** puslapyje. Galite naudoti bet kokią norimą vertę, bet būtinai ją pasižymėkite, nes vėliau jums jos prireiks. Atlikite šiuos veiksmus, kad sukurtumėte **WSC2112** kodą:

    1. **kurtiKrovinius** metodo eilutėje dešiniuoju pelės mygtuku spustelėkite rodyklę žemyn, esančią **Bangos žingsnio kodas** lauke, tada pasirinkite **Peržiūrėti išsamią informaciją**.
    1. **Bangų žingsnių kodai** puslapyje, esančiame Veiksmų srityje, pasirinkite **Naujas**.
    1. **Bangos žingsnio kodas** lauke įveskite *WSC2112*.
    1. **Bangos žingsnio aprašas** lauke įveskite *WSC2112*.
    1. **Bangos žingsnio tipas** lauke pasirinkite *Krovinio kūrimas*.

1. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
1. **kurtiKrovinius** metodo eilutėje, esančioje **Bangos žingsnio kodas** lauke pasirinkite ką tik sukurtą kodą (**WSC2112**).
1. Veiksmų srityje pasirinkite **Įrašyti**.

> [!NOTE]
> Bangų žingsnių kodai yra kodai, kuriuos vartotojai gali nustatyti ir naudoti konkretiems bangos metodų egzemplioriams susieti su atitinkamais šablonais. Yra papildymo, krovimo į konteinerius, etikečių spausdinimo, krovinio kūrimo ir rūšiavimo šablonų.
>
> Kai bangos veiksmo kodai nenaudojami, vartotojai turi įvesti laisvos formos tekstą, kad galėtų nurodyti konkretų bangos metodo egzemplioriaus šabloną. Laisvos formos tekste dažnai būna klaidų, nes vartotojai turi įsitikinti, kad jų pridėtas bangos žingsnio tekstas konkrečiame bangos žingsnio metode bangos šablone atitinka bangos žingsnio tekstą tikslinio šablono bangos žingsnio tekstą.
>
> Konkretaus bangos veiksmo tipo bangos veiksmo kodai nustatomi atskirame puslapyje. Kiekvieno bangos žingsnio metodo egzemplioriaus bangos šablone, kuriam būtinas bangos žingsnio kodas, bangos veiksmo kodas turi būti pasirinktas išplečiamajame sąraše. Pasirinkus išplečiamajame meniu, pakeičiamas laisvos formos teksto įrašas ir sumažinamas žmogaus padarytos klaidos pavojus ir poveikis. Sąrankos kodai naudojami norint susieti bangos veiksmo metodą bangos šablone su metodo tiksliniu šablonu.

### <a name="set-up-load-mix-groups"></a>Krovinio mišrių grupių nustatymas

Įkelkite mišrių grupių nustatymo taisykles prekių tipams, kurie gali būti sujungti viename krovinyje. Galite nustatyti tiek krovinių mišrių grupių,  kiek jums reikia. Tačiau norėdami naudoti papildomą bangos krovinio kūrimą, turite turėti bent vieną. Atlikite šiuos veiksmus, kad sukurtumėte krovinio mišrią grupę.

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Krovinys** \> **Krovinio mišrios grupės**.
1. Veiksmų srityje pasirinkite **Nauja**, kad sukurtumėte krovinio grupę.
1. **Krovinio mišrios grupės ID** lauke įveskite naujos grupės pavadinimą.

    Jei dirbate su **USMF** parodomosios versijos duomenimis, nustatykite šias vertes:

    - **Krovinio mišinio grupės ID:** *TV*
    - **Aprašas:** *TV*

1. Veiksmų srityje pasirinkite **Įrašyti**, kad **Krovinio mišrios grupės kriterijai** „FastTab” skirtukas taptų prieinamas.
1. **Skirtuko mišrios grupės kriterijai** „FastTab” pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite norimas vertes kiekviename lauke. Šios vertės apibrėžia prekių grupes, kurios svarstoma įtraukti į krovinio kombinaciją.

    Jei dirbate su **USMF** parodomosios versijos duomenimis, pasirinkite *TV ir vaizdo įrašas* lauke **Prekės grupė**.

1. Veiksmų srityje pasirinkite **Įrašyti**, kad **Krovinio mišrios grupės apribojimai** „FastTab” skirtukas taptų prieinamas.
1. **Mišrios grupės apribojimai** „FastTab” skirtuke pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite norimas vertes kiekviename lauke.

    Jei dirbate su **USMF** parodomosios versijos duomenimis, nustatykite šias vertes:

    - **Prekės grupė:** *AutomobilioAudio*
    - **Krovinio kūrimo veiksmas:** *Riboti* (Ši vertė neleis priskirti prekių, priklausančių **AutomobilioAudio** prekių grupei, tam pačiam kroviniui kaip prekių, priklausančių **TV ir Vaizdo įrašas** prekių grupei.)

1. Toliau dirbkite su taisyklėmis, kol pridėsite visus kriterijus ir apribojimus, kurių reikia krovinio mišriajai grupei.

Jei dirbate su **USMF** parodomosios versijos duomenimis, dabar baigėte šią sąranką.

### <a name="set-up-load-build-templates"></a>Krovinio kūrimo šablonų nustatymas

Galite nustatyti tiek krovinių kūrimo šablonų, kiek būtina. Tačiau norėdami naudoti papildomą bangos krovinio kūrimą, turite turėti bent vieną. Norėdami sukurti krovinio kūrimo šabloną, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Krovinys** \> **Bangos krovinio kūrimo šablonai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes.

    | Laukas | aprašymas | USMF parodomosios versijos duomenų vertė |
    |---|---|---|
    | Sekos numeris | Tvarka, pagal kurią šablonas bus įvertintas. | *1* |
    | Krovinio kūrimo šablono pavadinimas | Įveskite krovinio kūrimo šablono unikalų identifikatorių. Turite įvesti sukurto ar anksčiau šioje sąrankoje atnaujinto šablono pavadinimą. | *62 siuntos numatytasis nustatymas* |
    | Bangos veiksmo kodas | Įveskite bangos žingsnio kodą, kad susietumėte šabloną su bangos metodu. Turite įvesti kodą, kurį pasirinkote **kurtiKrovinius** metodui, kai anksčiau šioje sąrankoje nustatėte bangos šabloną. | *WSC2112* |
    | Krovinio šablono ID | Pasirinkite krovinio šabloną, kuris bus naudojamas kuriant naujus krovinius ir kuriuos reikia suderinti priskiriant prie esamų krovinių. Krovinio šablonas apibrėžia maksimalų leidžiamą viso krovinio svorį ir tūrį. | *Esamas krovinio šablonas* |
    | Įranga | Įranga, kurią reikia suderinti priskiriant esamus krovinius ir įvedant naujus sukurtus krovinius. | Palikite šį lauką tuščią. |
    | Krovinio rinkinio grupės ID | Pasirinkite krovinio mišrią grupę naudojimui, jei prekę galima įtraukti į krovinį. Mišri grupė nustato taisykles prekių tipams, kurias gali būti sujungtos į vieną krovinį. Turite pasirinkti vieną iš anksčiau šioje sąrankoje sukurtų mišrių grupių. | *TV* |
    | Naudoti atvirus krovinius | Pasirinkite, ar esami atviri kroviniai turėtų būti pridėti. Galimos toliau nurodytos parinktys.<ul><li>**Nėra** – nepridėti atvirų krovinių prie esamų krovinių.</li><li>**Bet koks** – pridėti atvirus krovinius prie esamų krovinių, galiojančių eilutėje.</li><li>**Priskirta** – pridėti atvirus krovinius prie krovinio, priskirto bangai.</li></ul> | *Bet kuris (-i)* |
    | Kurti krovinius | Nurodykite, ar nauji kroviniai turėtų būti sukurti, jei egzistuojantys kroviniai neatitinka kriterijų. | Pasirinkta (= *Taip*) |
    | Leisti siuntos eilutės padalijimą | Nurodykite, ar viena krovinio eilutė gali būti padalinta keliems kroviniams, jei pilna linija viršija didžiausią krovinio šablono pajėgumą. | Apmokėta (= *Ne*) |
    | Patvirtinti tūrio metriką | Nurodykite, ar krovinio kūrimo režimas turėtų patikrinti svorį ir tūrį kiekvienos eilutės pridėjimo metu, kad būtų užtikrinta, jog laikomasi krovinio šablonui taikomų tūrio matavimų ribojimų. | Apmokėta (= *Ne*) |

1. Veiksmų srityje pasirinkite **Įrašyti**, kad padarytumėte **Redaguoti užklausą** parinktį prieinamą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**, kad atidarytumėte dialogo langą užklausai redaguoti.
1. Dialogo lango **Rūšiavimas** skirtuke pasirinkite **Pridėti**, kad pridėtumėte eilutę į tinklelį.
1. Naujojoje eilutėje nurodykite norimas naudoti rūšiavimo taisykles. Pavyzdžiui, nustatykite šias vertes rūšiuoti paieškos rezultatus didėjančia tvarka pagal užsakymo numerį:

    - **Lentelė:** *Krovinio išsami informacija*
    - **Išvestinė lentelė:** *Krovinio išsami informacija*
    - **Laukas:** *Užsakymo numeris*
    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **Gerai**, kad išsaugotumėte savo pakeitimus ir uždarykite dialogo langą.
1. **Skelti pagal** „FastTab” skirtuke, nustatykite taisykles, kad valdytumėte, kaip jūsų kroviniai yra perskeliami. Paprastai galite skelti pasirinktinius laukus, kurie buvo išplėstiniai į krovinio eilutę, pvz., **Maršrutas**, **Ekskursija** arba **Leisti**. Pavyzdžiui, norėdami sukurti vieną krovinio už užsakymą numerį, pasirinkite **Skelti pagal** eilutės žymės laukelį, turintį šias vertes:

    - **Nuorodos lentelės pavadinimas:** *Išsami krovinio informacija*
    - **Nuorodos lauko pavadinimas:** *Užsakymo numeris*

## <a name="scenario"></a>Scenarijus

Šis scenarijus nurodo, kaip anksčiau šioje temoje aprašyti parametrai veikia sandėlio operacijas, kol apdorojamas pardavimo užsakymas. Šis scenarijus naudoja **USMF** parodomosios versijos duomenis su kitomis parodomosios versijos vertėmis, pateiktomis tose sąrankos instrukcijose.

### <a name="create-sales-orders"></a>Pardavimo užsakymų kūrimas

1. Eikite į **Pardavimas ir rinkodara** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad atidarytumėte dialogo langą **Sukurti pardavimų užsakymą**.
1. Dialogo lange nustatykite šias vertes:

    - **Klientas** „FastTab” skirtuke nustatykite **Kliento paskyra** lauką į *US–007*.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Jūsų naujas pirkimo užsakymas yra atidarytas. Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje. Naujoje eilutėje nustatykite **Prekės numeris** lauką į *A0001* ir **Kiekis** lauką į  *1*.
1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. **Rezervacija** puslapyje, esančiame Veiksmų srityje, pasirinkite **Rezervuoti partiją**.
1. Pasirinkite **Uždaryti** mygtuką (**X**) viršutiniame dešiniajame puslapio kampe, kad grįžtumėte į pardavimų užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**. Sistema sukuria siuntą ir prideda ją į naują krovinį, nes nei viename esančiame krovinyje nėra krovinio eilučių, turinčių tokį užsakymo numerį.

    Gausite informacinius pranešimus, kuriuose pateikta informacija apie darbą, bangą ir siuntą, sukurtą šiam užsakymui.

1. Norėdami patvirtinti krovinį, siuntą ir išsamią darbo informaciją pardavimo eilutėje, pasirinkite eilutę, tada **Sandėlis** meniu virš tinklelio, pasirinkite **Išsami krovinio informacija**, **Išsami siuntimo informacija** arba **Išsami darbo informacija**.
1. Ką tik sukurtame pardavimo užsakyme **Pardavimo užsakymo eilutės** „FastTab” pasirinkite **Pridėti eilutę**, kad pridėtumėte kitą eilutę.
1. Naujoje eilutėje nustatykite **Prekės numeris** lauką į *A0002* ir **Kiekis** lauką į  *1*.
1. Pakartokite nuo 6 iki 9 eilutes, kad užrezervuotumėte eilutę ir ją išleistumėte į sandėlį. Sistema sukuria **Nauja** siuntą naujai jūsų pridėtai eilutei. Tačiau, kadangi naudojate papildomo bangos krovinio kūrimą, sistema prideda tą siuntą ir krovinio eilutę į esamą bangą. Jei nenaudotumėte papildomo bangos krovinio kūrimo, sistema sukurtų naują siuntos krovinį.
1. Ką tik sukurtame pardavimo užsakyme **Pardavimo užsakymo eilutės** „FastTab” pasirinkite **Pridėti eilutę**, kad pridėtumėte kitą eilutę.
1. Naujoje eilutėje nustatykite **Prekės numeris** lauką į *M9200* ir **Kiekis** lauką į  *1*.
1. Pakartokite nuo 6 iki 9 eilutes, kad užrezervuotumėte eilutę ir ją išleistumėte į sandėlį. Kaip ir anksčiau, sistema sukuria **Nauja** siuntą naujai jūsų pridėtai eilutei. Tačiau, kadangi prekė yra iš **AutomobilioAudio** prekių grupės, ji **neperleidžia jūsų krovinio mišriai grupei nustatytų apribojimų**. Todėl jis **pridedamas į naują krovinį**. Jei nebūtumėte nurodę krovinio mišrios grupės krovinio kūrimo šablone, ši siunta būtų buvusi pridėta pirmame krovinyje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]