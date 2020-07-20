---
title: Vietos numerio lentelės padėtis
description: Numerio lentelės vietos nustatymas leidžia matyti, kur numerio lentelė yra kelių padėklų vietoje, pvz., vietoje, kurioje naudojamas dvigubai gilių padėklų išdėstymas.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6810753c10d03999c38a6163687effd771076c15
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530057"
---
# <a name="location-license-plate-positioning"></a>Vietos numerio lentelės padėtis

[!include [banner](../includes/banner.md)]

Numerio lentelės vietos nustatymas leidžia matyti, kur numerio lentelė yra kelių padėklų vietoje, pvz., vietoje, kurioje naudojamas dvigubai gilių padėklų išdėstymas.

Funkcija prideda eilės numerį prie kiekvienos numerio lentelės, padėtos į saugojimo vietą. Šis eilės numeris naudojamas, kad būtų galima užsakyti numerių lenteles saugojimo vietoje. Todėl funkcija sumaniai palaiko scenarijus, kuriuose klientai naudoja gravitacinę išdėstymo sistemą ir turi žinoti, kad pasirenkant, kuriai numerio lentelė yra priekyje.

Šioje temoje parodytas scenarijus, kaip nustatyti ir naudoti funkciją.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Įjunkite Vietos numerio lentelės vietos nustatymo funkciją

Prieš naudojanti numerio lentelės vietos išdėstymą, funkcija turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Vietos numerio lentelės išdėstymas*

## <a name="example-scenario"></a>Pavyzdinis scenarijus

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti su šiuo scenarijumi naudojant čia rekomenduojamas vertes, turite dirbti su sistema, kurioje įdiegti duomenų pavyzdys. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

### <a name="set-up-the-feature-for-this-scenario"></a>Nustatykite funkciją šiam scenarijui

Užbaikite šias procedūras, kad nustatytumėte *Vietos numerio lentelės nustatymas* funkciją šioje temoje pristatytam scenarijui.

#### <a name="location-profiles"></a>Vietos šablonai

Funkcija turi būti įjungta kiekviename vietos, kurioje ji bus naudojama, profilyje.

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.
1. Vietų profilių sąraše, kairėje, pasirinkite **MASINIS-06**.
1. **Bendra** „FastTab” skirtuke dvi funkciją papildė dvi naujos parinktys. Nustatykite toliau nurodytas reikšmes.

    - **Įjungti numerio lentelės padėtį:** *Taip*

        Kai ši parinktis nustatyta į *Taip*, numerio lentelės pozicija bus išlaikyta vietos numerių lentelėse.

    - **Rodyti mobiliojo įrenginio LP padėtį:** *Taip*

        Kai parinktis nustatyta į *Taip*, numerio lentelės pozicija bus rodoma mobiliojo įrenginio vartotojams koreguojant ir skaičiuojant. Šią pasirinktį galima pakeisti tik tada, kai funkcija įjungta.

1. Pasirinkite **Įrašyti**.

#### <a name="location-directives"></a>Vietos nurodymai

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairiojoje srityje įsitikinkite, kad **Darbo užsakymo tipas** laukas nustatytas į *Pardavimų užsakymai*.
1. Vietų nurodymų sąraše pasirinkite **61 SO paimti užsakymą**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Eilutės** „FastTab” pasirinkite eilutę, kuri turi **Eilės numeris** *2* vertę.
1. **Vietos nurodymų veiksmai** „FastTab” skirtuke pasirinkite eilutę, kurios **Pavadinimas** vertė *Pasirinkti mažiau nei padėklą* (turi būti tik vienintelė eilutė), ir pakeiskite jos **Eilės numeris** vertę į *2*.
1. Pasirinkite į **Nauja** virš tinklelio pridėti eilutę naujam vietos nurodymo veiksmui.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Eilės numeris:** *1*
    - **Pavadinimas:** *Paėmimo pozicija 1*

1. Kol renkamasi nauja eilutė, virš tinklelio pasirinkite **Redaguoti užklausą**.
1. Užklausų rengyklėje pasirinkite **Sujungimai** skirtuką.
1. Išplėskite **Vietos** lentelę sujungimą, kad parodytų sujungimą prie **Atsargų dimensijos** lentelės.
1. Išplėskite **Atsargų dimensijos** lentelę sujungimą, kad parodytų sujungimą prie **Turimos atsargos** lentelės.
1. Pasirinkite **Atsargų dimensijos** ir pasirinkite **Pridėti lentelės sujungimą**.
1. Pasirodančiame lentelių sąraše **Ryšys** stulpelyje pasirinkite **Numerio lentelė (numerio lentelė)**. Tada pasirinkite **Pasirinkti**, kad į **Numerio lentelė** pridėtumėte **Atsargų dimensijos** lentelės sujungimą.
1. Kol **Numerio lentelė** vis dar pasirinkta, pasirinkite **Pridėti lentelės sujungimą**.
1. Pasirodančiame lentelių sąraše **Ryšys** stulpelyje pasirinkite **Vietos numerio lentelės nustatymas (numerio lentelė)**. Tada pasirinkite **Pasirinkti**, kad į **Vietos numerio lentelės nustatymas** pridėtumėte **Atsargų dimensijos** lentelės sujungimą.

    ![Lentelių sujungimai](media/LpTableJoin.png "Lentelių sujungimai")

1. Pasirinkite **Gerai**, kad patvirtintumėte atnaujintus sujungtas lenteles ir uždarytumėte užklausos rengyklę.
1. „FastTab“ skirtuke **Vietos nurodymų veiksmai** vėl pasirinkite **Redaguoti užklausą**, kad iš naujo atidarytumėte užklausos rengyklę.
1. Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Vietos numerio lentelės nustatymas*
    - **Išvestinė lentelė:** *Vietos numerio lentelės nustatymas*
    - **Laukas:** *LP pozicija*
    - **Kriterijai:** *1*

    ![Naujas diapazonas](media/LpPositionCriteria.png "Naujas diapazonas")

1. Pasirinkite **Gerai**, kad patvirtintumėte pakeitimus ir uždarytumėte užklausų rengyklę.

### <a name="set-up-sample-data-for-this-scenario"></a>Nustatykite duomenų pavyzdį šiam scenarijui

Šiam scenarijui vartotojas turi prisijungti prie sandėliavimo mobiliosios programėlės naudodamas darbuotoją, nustatytą sandėliui *61*, kad atliktų darbą. Vartotojas taip pat turi atlikti operacijas.

Kadangi *Vietos numerio lentelės nustatymas* funkcija prideda naują identifikatorių, skirtą numerių lentelių pozicijoms, vietoje, iš pradžių turite sukurti duomenų, kad šis scenarijus veiktų.

#### <a name="spot-count-the-first-location"></a>Vietoje skaičiavimo pirmoji vieta

1. Atverkite sandėliavimo mobiliąją programėlę, kad prisijungtumėte prie sandėlio *61*.
1. Eikite į **Atsargos \>Vietoje skaičiavimas**.
1. **Vietoje skaičiavimas** puslapyje nustatykite **Vietos** lauką į *01A01R1S1B*.
1. Pasirinkite **Gerai**.

    Puslapyje rodoma jūsų įvesta vieta. Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”

1. Pasirinkite **Atnaujinti**, kad pridėtumėte vietą.
1. **Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **Prekė** lauką ir įveskite vertę *A0001*.
1. Pasirinkite **Gerai**.
1. **Ciklo skaičius: pridėti naują LP arba prekę**puslapyje pasirinkite **LP** lauką ir įveskite vertę *LP1001* (arba kitą jūsų pasirinktą numerio lentelės numerį).

    **Ciklų skaičius: pridėti naują LP arba prekę** puslapis rodo **Numerio lentelės pozicija 1**.

1. Pasirinkite **Gerai**.

    Dabar turite nurodyti prekės kiekį, suskaičiuotą numerio lentelėje.

1. Nustatykite **Kiek.** lauką į *10*.
1. Pasirinkite **Gerai**.

    Puslapyje rodoma jūsų įvesta vieta. Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”

1. Pasirinkite **Atnaujinti**, kad pridėtumėte dar vieną skaičių vietoje.
1. **Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **Prekė** lauką ir įveskite vertę *A0002*.
1. Pasirinkite **Gerai**.
1. **Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **LP** lauką ir įveskite vertę *LP1002* (arba bet kokį kitą savo pasirinktą numerio lentelės numerį, tik jei jis skiriasi nuo anksčiau nurodyto numerio lentelės numerio).
1. Pakeiskite numerio lentelės padėtį nustatydami **LP pozicija** lauką į *2*.
1. Pasirinkite **Gerai**.
1. Nurodykite prekės kiekį, suskaičiuotą numerio lentelėje, nustatydami **Kiek.** lauką į *10*.
1. Pasirinkite **Gerai**.

    Puslapyje rodoma jūsų įvesta vieta. Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”

1. Pasirinkite **Gerai**.

Dabar darbas baigtas.

#### <a name="spot-count-the-second-location"></a>Vietoje skaičiavimo antroji vieta

1. **Vietoje skaičiavimas** puslapyje nustatykite **Vieta** lauką į *01A01R1S2B*.
1. Pasirinkite **Gerai**.

    Puslapyje rodoma jūsų įvesta vieta. Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”

1. Pasirinkite **Atnaujinti**, kad pridėtumėte vietą.
1. **Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **Prekė** lauką ir įveskite vertę *A0002*.
1. Pasirinkite **Gerai**.
1. **Ciklų skaičius: pridėti naują LP arba prekę** puslapyje pasirinkite **LP** lauką ir įveskite vertę *LP1003* (arba bet kokį kitą savo pasirinktą numerio lentelės numerį, tik jei jis skiriasi nuo numerio lentelių numerių, anksčiau nurodytų ankstesnėje procedūroje).

    **Ciklų skaičius: pridėti naują LP arba prekę** puslapis rodo **Numerio lentelės pozicija 1**.

1. Pasirinkite **Gerai**.
1. Nurodykite prekės kiekį, suskaičiuotą numerio lentelėje, nustatydami **Kiek.** lauką į *10*.
1. Pasirinkite **Gerai**.

    Puslapyje rodoma jūsų įvesta vieta. Taip pat rodomas šis pranešimas: „vieta baigta, pridėti naują LP arba prekę?”

1. Pasirinkite **Gerai**.

Dabar darbas baigtas.

#### <a name="work-details"></a>Darbo informacija

> [!NOTE]
> Vietų skaičiavimai iš mobiliosios programėlės sukuria ciklo skaičiavimo darbą „Microsoft Dynamics 365”. Darbui atlikti reikia, kad skaičiavimai būtų priimti prieš juos registruojant į atsargas.

1. Prisijunkite prie „Dynamics 365 Supply Chain Management“.
1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. **Apžvalga** skirtuke ieškokite eilučių, turinčių šias vertes:

    - **Darbo užsakymo tipas:** *Ciklo skaičiavimas*
    - **Sandėlis:** *61*
    - **Darbo būsena:** *Laukiama peržiūra*

    Šioms eilutėms buvo sukurti du darbo ID. Reikia priimti abiejų šių darbų ID skaičiavimus.

1. Tinklelyje pasirinkite pirmo darbo ID, skirtą *Ciklo skaičiavimas* darbo užsakymo tipui.
1. Veiksmų srityje skirtuke **Darbas**, **Bendra** grupėje, pasirinkite **Ciklo skaičiavimas**.

    Rodomos dvi eilutės, po vieną kiekvienai prekei ir numerio lentelei. **Suskaičiuotas kiekis** vertės **Vieta**, **Numerio lentelė** ir **Prekė** laukų vertės turi sutapti su jūsų mobiliajame įrenginyje sukurtais skaičiavimų įrašais. Jei kuris nors iš šių laukų nematomas, pasirinkite **Rodyti dimensijas** Veiksmų srityje, kad pridėtumėte į tinklelį.

1. Pasirinkite abi eilutes.
1. Veiksmų srityje spustelėkite **Pridėti skaičiavimą**.
1. Gaunate pranešimą „Registravimas – žurnalas”. Pasirinkite **Pranešimo išsami informacija**, kad peržiūrėtumėte užregistruotą žurnalo numerį.
1. Uždarykite pranešimo išsamią informaciją.
1. Atnaujinkite **Darbas** puslapį.

    Pirmas darbo ID buvo uždarytas ir nebebus rodomas.

    > [!TIP]
    > Norėdami peržiūrėti uždarytą darbą pasirinkite **Rodyti uždarytą** žymės langelį virš tinklelio.

    Dabar priimsite darbą, skirtą numerio lentelei, esantį *01A01R1S2B* vietoje.

1. **Apžvalga** skirtuke pasirinkite antrojo darbo ID, skirto *Ciklo skaičiavimas* darbo užsakymo tipui.
1. Veiksmų srityje skirtuke **Darbas**, **Bendra** grupėje, pasirinkite **Ciklo skaičiavimas**.

    Rodoma prekės ir numerio lentelės viena eilutė. **Suskaičiuotas kiekis** vertės **Vieta**, **Numerio lentelė** ir **Prekė** laukų vertės turi sutapti su jūsų mobiliajame įrenginyje sukurtais skaičiavimų įrašais.

1. Pasirinkite eilutę.
1. Veiksmų srityje spustelėkite **Pridėti skaičiavimą**.
1. Gaunate pranešimą „Registravimas – žurnalas”. Pasirinkite **Pranešimo išsami informacija**, kad peržiūrėtumėte užregistruotą žurnalo numerį.
1. Uždarykite pranešimo išsamią informaciją.
1. Atnaujinkite **Darbas** puslapį.

    Antras darbo ID buvo uždarytas ir nebebus rodomas.

    > [!TIP]
    > Norėdami peržiūrėti uždarytą darbą pasirinkite **Rodyti uždarytą** žymės langelį virš tinklelio.

#### <a name="on-hand-by-location"></a>Turimos atsargos pagal vietą

1. Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Turima pagal vietą**.
1. Nustatykite toliau nurodytas reikšmes.

    - **Vieta:** *6*
    - **Sandėlis:** *61*
    - **Atnaujinti keliose vietose:** *Taip*

1. Atkreipkite dėmesį, kad vieta *01A01R1S1B* turi dvi numerio lenteles:

    - **A0001**, kur **LP pozicija** laukas nustatytas į *1*
    - **A0002**, kur **LP pozicija** laukas nustatytas į *2*

1. Atkreipkite dėmesį, kad vieta *01A01R1S2B* turi vieną numerio lentelę:

    - **A0002**, kur **LP pozicija** laukas nustatytas į *1*

### <a name="sales-order-scenario"></a>Pardavimo užsakymo scenarijus

Dabar, kai *Vietos numerio lentelės nustatymas* funkcija nustatyta, o atsargos buvo parengtos, turite sukurti pardavimo užsakymą, kad būtų sugeneruotas paėmimo darbas, nukreipsiantis sandėlio darbuotoją paimti prekę *A0002* iš atsargų vietos, kurioje padėklo ID yra *1* pozicijoje.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-004*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai**.
1. Nauja eilutė pridėta į tinklelį, esantį **Pardavimo užsakymo eilutės** „FastTab”. Naujoje eilutėje nustatykite šias vertes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *1*

1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. **Rezervavimas** puslapyje, Veiksmų srityje, pasirinkite **Rezervuoti partiją**, kad užrezervuotumėte atsargas užsakymų eilutei.
1. Uždarykite **Rezervavimas** puslapį.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.

    Gausite informacinį pranešimą, nurodantį bangos ID ir siuntos ID, sukurtus šiam užsakymui.

1. **Pardavimo užsakymo eilutės** „FastTab” skirtuke, virš tinklelio esančiame meniu **Sandėlis**, pasirinkite **Darbo išsami informacija**.
1. **Darbas** puslapis pasirodo ir parodo pardavimų eilutei sukurtą darbą. Pasižymėkite rodomo darbo ID.

### <a name="sales-picking-scenario"></a>Pardavimo paėmimo scenarijus

1. Atverkite sandėliavimo mobiliąją programėlę ir prisijunkite prie sandėlio *61*.
1. Eikite į **Išsiųsti \> Pardavimų paėmimas**.
1. **Nuskaityti darbo ID / numerio lentelės ID** puslapyje pasirinkite **ID** lauką ir įveskite darbo ID iš pardavimo eilutės.
1. Atkreipkite dėmesį, kad paėmimo darbas nurodo jums paimti prekę *A0002* iš vietos *01A01R1S2B*. Gaunate šią instrukciją, nes prekė *A0002* yra numerio lentelėje, esančioje *1* padėtyje toje vietoje.

    ![1 pozicijos vieta](media/LocationLicensePlatePositioning.png "1 pozicijos vieta")

1. Įveskite vietai sukurtos numerio lentelės ID, tada vadovaukitės raginimais ir pasirinkite pardavimo užsakymą.
