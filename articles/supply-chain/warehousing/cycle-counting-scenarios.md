---
title: Ciklo skaičiavimo pavyzdiniai scenarijai
description: Šiame straipsnyje pateikiamas scenarijų, kurie ištyrinėja "Microsoft" ciklų skaičiavimo priemones, rinkinys Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 91a18b6deade6d67fce6b90308671910a4196104
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335742"
---
# <a name="cycle-counting-example-scenarios"></a>Ciklo skaičiavimo pavyzdiniai scenarijai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamas scenarijų, kurie ištyrinėja "Microsoft" ciklų skaičiavimo priemones, rinkinys Dynamics 365 Supply Chain Management. Pirmiausia aprašomi jūsų esamos „Supply Chain Management” aplinkos reikalavimai. Tada paaiškinama, kaip konfigūruoti ciklo skaičiavimą ir aprašomi visi ciklo skaičiavimo etapai. Kai baigsite, turėtumėte gerai suprasti ciklo skaičiavimą, įskaitant valdomą ciklo skaičiavimą, aklą ciklo skaičiavimą, ciklo skaičiavimą vietoje, ciklo skaičiavimo ribines vertes ir ciklo skaičiavimo planus.

## <a name="prerequisites"></a>Būtinieji komponentai

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Kiekvienas scenarijus šiame straipsnyje nurodo vertes ir įrašus, įtrauktus į standartinius demonstracinius duomenis, kurie pateikiami tiekimo grandinės valdymui. Jei norite naudoti čia pateiktas reikšmes dirbdami pagal scenarijus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir nustatykite juridinį subjektą į **„USMF”** prieš pradėdami.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>„Warehouse Management Mobile App“ palaikymo įjungimas

Norint naudoti sandėlio valdymo mobiliąją programą, *jūsų sistemai reikia įjungti vartotojo parametrus, piktogramas* ir naujos sandėlio programos funkcijos veiksmų pavadinimus. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, *tada administratoriai gali įjungti arba išjungti šią funkciją ieškodami naujo sandėlio programos funkcijos vartotojo parametrų,*[piktogramų](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir veiksmų pavadinimų funkcijų funkcijų valdymo darbo srityje.

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Paruoškite demonstracinius duomenis scenarijams

Norėdami patvirtinti, kad visi demonstraciniai duomenys, reikalingi scenarijams, yra galimi USMF įmonėje jūsų sistemoje, atlikite šiuos veiksmus. Sukurkite trūkstamus įrašus ar vertes.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.
1. Sąrašo srityje pasirinkite **„Julia Funderburk”**.
1. „FastTab” **Vartotojai** pasirinkite eilutę, kuri turi toliau pateiktas vertes. Jei nei viena eilutė neturi šių verčių, sukurkite ją.

    - **Vartotojo ID:** *„61”*
    - **Vartotojo vardas:** *„WH61”*
    - **Nustatytasis sandėlis:** *61*
    - **Meniu pavadinimas:** *Pagrindinis*

1. „FastTab” **Darbas** nustatykite šias reikšmes *„61”* vartotojui, jei jos dar nėra nustatytos:

    - **Yra ciklų skaičiavimo prižiūrėtojas:** *Ne*
    - **Maksimali procentinė riba:** *0*
    - **Maksimali kiekio riba:** *0*
    - **Maksimali vertės riba:** *0*

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbas \> Darbo baseinai**.
1. Darbo telkiniai naudojami atskirti sandėlio darbui, atsižvelgiant į darbo tipą (šiuo atveju ciklo skaičiavimo darbas). Įsitikinkite, kad yra įrašas, turintis šiuos parametrus:

    - **Darbo telkinio ID:** *„CycleCount”*
    - **Aprašas:** *Ciklo skaičiavimas*

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sąrašo srityje pasirinkite įrašą, pavadintą *Ciklo skaičiavimas*. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį. Patvirtinkite arba nustatykite šias įrašo vertes:

    - **Meniu elemento pavadinimas:** *Ciklo skaičiavimas*
    - **Pavadinimas:** *Valdomas ciklo skaičiavimas*
    - **Režimas:** *Darbas*
    - **Naudoti esamą darbą:** *Taip*
    - **Sukūrė:** *Sukurta sistemos* (ši vertė nurodo, kad „Supply Chain Management” priskirs ciklo skaičiavimo darbo ID darbuotojui.)
    - **Rodyti atsargų būseną:** *Taip*

1. Veiksmų srityje pasirinkite **Ciklo skaičiavimas**.
1. Dialogo lange **Mobiliojo įrenginio ciklo skaičiavimas** patvirtinkite arba nustatykite šias vertes:

    - **Rodyti prekės numerį:** *Taip*
    - **Rodyti numerio lentelę:** *Taip*
    - **Bandymų skaičius:** *1*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Sąrašo srityje pasirinkite įrašą, pavadintą *Aklas ciklo skaičiavimas*. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį. Patvirtinkite arba nustatykite šias įrašo vertes:

    - **Meniu elemento pavadinimas:** *Aklas ciklo skaičiavimas*
    - **Pavadinimas:** *Aklas ciklo skaičiavimas*
    - **Režimas:** *Darbas*
    - **Naudoti esamą darbą:** *Taip*
    - **Sukūrė:** *Ciklo skaičiavimo grupavimas* (Ši reikšmė nurodo, kad darbuotojas gali grupuoti tam tikros vietos, zonos ar darbo telkinio ciklo skaičiavimo darbo ID.)

1. Veiksmų srityje pasirinkite **Ciklo skaičiavimas**.
1. Dialogo lange **Mobiliojo įrenginio ciklo skaičiavimas** patvirtinkite arba nustatykite šias vertes:

    - **Rodyti prekės numerį:** *Ne*
    - **Rodyti numerio lentelę:** *Ne*
    - **Bandymų skaičius:** *0*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Sąrašo srityje pasirinkite įrašą, pavadintą *Skaičiavimas vietoje*. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį. Patvirtinkite arba nustatykite šias įrašo vertes:

    - **Meniu elemento pavadinimas:** *Skaičiavimas vietoje*
    - **Pavadinimas:** *Skaičiavimas vietoje*
    - **Režimas:** *Darbas*
    - **Naudoti sukurtą darbą:** *Ne*
    - **Darbo kūrimo procesas:** *Ciklo skaičiavimas vietoje* Ši reikšmė nurodo,kad darbuotojas gali bet kada skaičiuoti prekes sandėlio vietoje nekurdamas ciklo skaičiavimo darbo. (Norėdamas atlikti ciklo skaičiavimą vietoje, darbuotojas įveda vietos ID.)

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Sąrašo srityje pasirinkite įrašą, pavadintą *Atsargos*. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį. Patvirtinkite, kad stulpelyje **Meniu struktūra** rodomi šie ciklo skaičiavimo meniu elementai:

    - Ciklo skaičiavimas
    - Aklas ciklo skaičiavimas
    - Skaičiavimas vietoje

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Skirtuke **Ciklo skaičiavimas** nustatykite tolesnes reikšmes:

    - **Numatytasis ciklo skaičiavimo koregavimo tipas:** *Ciklo skaičiavimas* (Šiame lauke nurodomas žurnalo tipas, registruojamas užbaigus ciklo skaičiavimą.)
    - **Numatytasis ciklo skaičiavimo darbo klasės ID:** *„CCount”* (Šis laukas nurodo darbo klasę, naudojamą skaičiuojant ciklus.)
    - **Numatytasis ciklo skaičiavimo darbo prioritetas:** *50* (Šiame lauke nustatomas prioritetas, bendras ciklo skaičiavimo darbui ir kitiems darbo sandėlyje tipais). (Įvesdami skaičių, mažesnį negu kitiems darbo tipams įvestą skaičių, didesnį prioritetą suteikiate ciklo skaičiavimo darbui.)

1. Eikite į **Sandėlio valdymas \> Sąranka \> Inventorius \> Koregavimo tipai**.
1. Puslapis **Koregavimo tipai** leidžia jums kurti kodus skirtingiems koregavimams, kurie gali atsirasti. Patvirtinkite, kad yra įrašas, turintis šiuos parametrus:

    - **Atsargų koregavimo tipas:** *Ciklo skaičiavimas*
    - **Aprašas:** *Ciklo skaičiavimas*
    - **Pavadinimas:** *„ICnt”*

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio sąranka \> Sandėliai**.
1. Sąrašo srityje pasirinkite *61* sandėlį. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį.
1. „FastTab” **Sandėlis** nustatykite tolesnes reikšmes:

    - **Naudokite sandėlio valdymo procesą:** *taip* (ši vertė įgalina sandėlį naudoti sandėlio valdymo procesus (WMS).)
    - **Leisti perkelti numerio lentelę atliekant ciklų skaičiavimą:** *Taip* (Ši vertė leidžia darbuotojams perkelti numerio lenteles ciklo skaičiavimo metu.)

## <a name="scenario-1-guided-cycle-counting"></a>1 scenarijus: Valdomas ciklo skaičiavimas

Prieš pradėdami vykdyti valdomą ciklo skaičiavimą, turite sukurti tam tikrą darbą. Šis darbas suteiks paskirtam asmeniui nurodymus visose sandėlio vietose, kad jis užbaigtų skaičiavimus, nustatytus darbe.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Ciklo skaičiavimo darbo kūrimas 1 scenarijui

Atlikite šiuos veiksmus, jei norite sukurti ciklo skaičiavimo darbą prekės vietai *„01A02R2S2B”* (BULK-06) *61* sandėlyje.

1. Eikite į **Sandėlio valdymas \> Ciklo skaičiavimas \> Ciklo skaičiavimo darbas pagal vietą**.
1. Dialogo lange **Kurti ciklo skaičiavimo darbą pagal vietą** nustatykite lauką **Darbo telkinio ID** į *CycleCount*.
1. „FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.
1. Užklausų rengyklės dialogo lango skirtuke **Diapazonas** atlikite šiuos veiksmus:

    - Eilutei, kurios **Lauko** laukas nustatytas į *Sandėlis*, nustatykite lauką **Kriterijai** į *61*.
    - Eilutei, kurios **Lauko** laukas nustatytas į *Vieta*, nustatykite lauką **Kriterijai** į *„01A02R2S2B”*.

1. Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.
1. Pasirinkite **GERAI**, kad uždarytumėte **Kurti ciklo skaičiavimo darbą pagal vietą** dialogo langą.

    Kai darbo kūrimo procesas bus baigtas, Veiksmų centre pasirodys pranešimas.

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Suraskite naujai sukurtą darbą nustatydami filtrą stulpelyje **Darbo telkinio ID**, kad rastumėte įrašus, kurių reikšmė yra *„CycleCount”*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Ciklo skaičiavimo darbo atlikimas 1 scenarijui

Sukūrę ciklo skaičiavimo darbą, jį atliekate suskaičiuodami prekes sandėlio vietoje ir tada mobiliuoju įrenginiu įvesdami rezultatus į „Supply Chain Management“. Atlikite šiuos veiksmus, jei norite atlikti ciklo skaičiavimo darbą „Warehouse Management Mobile App” programėlėje.

1. Prisiregistruokite prie sandėlio valdymo mobiliosios [programos kaip darbo vartotojas, kurį nustatėte anksčiau šiame straipsnyje skyriuje Paruošti demonstracinius](#prepare-demo-data) duomenis scenarijams. Kaip pavyzdį šiame straipsnyje, vartotojas yra pavadintas *"Vz." Funderburk* ir yra nustatytas sandėliui *61*. (USMF demonstraciniai duomenys turėtų leisti jums prisijungti kaip šio darbo vartotojui įvedant *61* kaip vartotojo ID ir *1* – kaip slaptažodį.)
1. Pagrindiniame meniu pasirinkite **Atsargos**.
1. Meniu **Atsargos** pasirinkite **Valdomas ciklo skaičiavimas**.
1. Pasirinkite lauką **Kiekis** ir dar kartą įveskite *9* naudodami skaičių klaviatūrą ir tada pasirinkite **GERAI** (varnelės mygtukas).
1. Sistema tikėjosi, kad įvesite 10 šios prekės, vietos ir numerio lentelės vienetų. Todėl jūs paprašomas perskaičiuoti. Pasirinkite lauką **Kiekis** ir dar kartą įveskite *9* naudodami skaičių klaviatūrą ir tada pasirinkite **GERAI** (varnelės mygtukas). Antruoju bandymu jūsų skaičiavimas bus priimtas.

    > [!NOTE]
    > Kai sistema aptiko skirtumą tarp numatomo turimo kiekio ir jūsų įvesto kiekio, sistema paprašė jūsų skaičiuoti antrą kartą, nes **Bandymų skaičius** yra nustatytas į *1* mobiliojo įrenginio meniu elementui **Valdomo ciklo skaičiavimas**. Jums buvo nurodytas tam tikras prekės numeris ir numerio lentelė, kadangi **Rodyti prekės numerį** ir **Rodyti numerio lentelė** parinktys yra nustatytos į *Taip* mobiliojo įrenginio meniu elementui.

1. Rinkitės **GERAI** (pažymėkite žymimą mygtuką).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Peržiūrėti 1 scenarijaus ciklo skaičiavimo skirtumus

Norėdami peržiūrėti ciklo skaičiavimo skirtumus, atlikite šiuos veiksmus.

1. Sugrįžkite į „Supply Chain Management“.
1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Raskite ir pasirinkite ciklo skaičiavimo darbą, kurį peržiūrėjote anksčiau. Pavyzdžiui, nustatykite filtrą stulpeliui **Darbo telkinio ID**, kad surastumėte įrašus, turinčius reikšmę *„CycleCount”*. Atkreipkite dėmesį, kad šio darbo laukas **Darbo būsena** dabar nustatytas kaip *Laukiantis peržiūros*.

    > [!NOTE]
    > Darbo vartotojo paskyrai, kurią naudojote skaičiavimo darbui atlikti, parinktis **Ciklo skaičiavimo prižiūrėtojas** yra nustatyta į *Ne*, o laukai **Didžiausia procento riba**, **Didžiausia kiekio riba** ir **Didžiausia reikšmės riba** nustatyti į *0* (nulis). Todėl visi skaičiavimo skirtumai, apie kuriuos praneša vartotojas, turi būti patvirtinti rankiniu būdu, o susijusio darbo laukas **Darbo būsena** nustatytas į *Laukiantis peržiūros*. Jei suskaičiuota vertė patenka į nuokrypio ribas (kaip nurodyta laukuose **Didžiausia procento riba** ar **Didžiausia kiekio riba** puslapyje **Darbo vartotojai**), arba, jei parinktis **Ciklo skaičiavimo prižiūrėtojas** vartotojui nustatyta į *Taip*, darbas būtų uždaromas automatiškai.

1. Veiksmų srities skirtuke **Darbas** pasirinkite **Ciklo skaičiavimas**.
1. Veiksmų srityje spustelėkite **Pridėti skaičiavimą**.

    Skirtumas užregistruojamas naudojant standartinį skaičiavimo žurnalą, taip pat sukuriamas naujas darbo užsakymas.

1. Veiksmų srities puslapyje **Ciklo skaičiavimo operacijos** pasirinkite **Išvestas darbas**, kad rastumėte darbą, sukurtą patvirtintam skirtumui.

## <a name="scenario-2-blind-cycle-counting"></a>2 scenarijus: Aklas ciklo skaičiavimas

Šiam scenarijui reikia, kad jūsų sistemoje jau būtų užbaigtas 1 scenarijus.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Ciklo skaičiavimo darbo kūrimas 2 scenarijui

Prieš pradėdami vykdyti aklą ciklo skaičiavimą, turite sukurti tam tikrą darbą. Atlikite šiuos veiksmus, jei norite sukurti ciklo skaičiavimo darbą prekės vietai *„01A02R2S2B”* (BULK-06) *61* sandėlyje.

1. Eikite į **Sandėlio valdymas \> Ciklo skaičiavimas \> Ciklo skaičiavimo darbas pagal prekę**.
1. Dialogo lange **Kurti ciklo skaičiavimo darbą pagal prekę** nustatykite lauką **Darbo telkinio ID** į *CycleCount*.
1. „FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.
1. Užklausų rengyklės dialogo lango skirtuke **Diapazonas** įtraukite tris eilutes su šiais nustatymais:

    - 1 eilutė:

        - **Lentelė:** *Prekės*
        - **Laukas:** *Prekės numeris*
        - **Kriterijai:** *L0101*

    - 2 eilutė:

        - **Lentelė:** *Atsargų dimensijos*
        - **Laukas:** *Sandėlis*
        - **Kriterijai:** *61*

    - 3 eilutė:

        - **Lentelė:** *Atsargų dimensijos*
        - **Laukas:** *Vieta*
        - **Kriterijai:** *01A02R2S2B*

1. Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.
1. Pasirinkite **GERAI**, kad uždarytumėte **Kurti ciklo skaičiavimo darbą pagal prekę** dialogo langą.

    Kai darbo kūrimo procesas bus baigtas, jūs gausite informacinį pranešimą.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Ciklo skaičiavimo darbo atlikimas 2 scenarijui

Sukūrę ciklo skaičiavimo darbą, atlikite šiuos veiksmus, jei norite atlikti darbą „Warehouse Management Mobile App” programėlėje.

1. Prisiregistruokite prie sandėlio valdymo mobiliosios [programos kaip darbo vartotojas, kurį nustatėte anksčiau šiame straipsnyje skyriuje Paruošti demonstracinius](#prepare-demo-data) duomenis scenarijams. Kaip pavyzdį šiame straipsnyje, vartotojas yra pavadintas *"Vz." Funderburk* ir yra nustatytas sandėliui *61*. (USMF demonstraciniai duomenys turėtų leisti jums prisijungti kaip šio darbo vartotojui įvedant *61* kaip vartotojo ID ir *1* – kaip slaptažodį.)
1. Pagrindiniame meniu pasirinkite **Atsargos**.
1. Meniu **Atsargos** pasirinkite **Aklas ciklo skaičiavimas**.
1. Pasirinkite lauką **Zonos ID**, įveskite *„BULK06”*, o tada pasirinkite **GERAI** (varnelės mygtukas).
1. Pasirinkite lauką **Prekė**, įveskite *„L0101”*, o tada pasirinkite **GERAI** (varnelės mygtukas).
1. Pasirinkite lauką **Numerio lentelė**, įveskite *„LP\_BULK\_06\_01”*, o tada pasirinkite **GERAI** (varnelės mygtukas).
1. Pasirinkite lauką **Kiekis**, įveskite *10*, o tada pasirinkite **GERAI** (varnelės mygtukas).

    > [!NOTE]
    > Nors sistema aptiko skirtumą tarp numatomo turimo kiekio ir jūsų nuskaityto kiekio, sistema neprašė jūsų skaičiuoti antrą kartą, nes **Bandymų skaičius** yra nustatytas į *0* (nulis) **Aklo ciklo skaičiavimo** mobiliojo įrenginio meniu elementui. Buvote paprašytas nuskaityti prekės numerį ir numerio lentelę, kadangi **Rodyti prekės numerį** ir **Rodyti numerio lentelė** parinktys yra nustatytos į *Ne* mobiliojo įrenginio meniu elementui.

1. Rinkitės **GERAI** (pažymėkite žymimą mygtuką).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Peržiūrėti 2 scenarijaus ciklo skaičiavimo skirtumus

Norėdami peržiūrėti ciklo skaičiavimo skirtumus, atlikite šiuos veiksmus.

1. Sugrįžkite į „Supply Chain Management“.
1. Eikite į **Sandėlio valdymas \> Bendra \> Darbas \> Peržiūros laukiantis ciklo skaičiavimo darbas**.
1. Veiksmų srities skirtuke **Darbas** pasirinkite **Ciklo skaičiavimas**.
1. Veiksmų srityje pasirinkite **Atmesti skaičiavimą**.

    Kadangi skaičiavimo skirtumas buvo atmestas, darbas yra uždaromas.

## <a name="scenario-3-spot-cycle-counting"></a>3 scenarijus: Ciklo skaičiavimas vietoje

Turimo kiekio įrašas rodo, kad yra turimas *„L0101”* prekės kiekis vietoje *„01A02R2S2B”*. Sandėlio darbuotojas yra *„01A02R2S1B”* vietoje. Nors ši vieta turėtų būti tuščia, ji yra pilna. Todėl sandėlio darbuotojas nedelsdamas atlieka šios vietos skaičiavimą vietoje.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Ciklo skaičiavimo darbo atlikimas 3 scenarijui

Atlikite šiuos veiksmus, jei norite atlikti ciklo skaičiavimo darbą „Warehouse Management Mobile App” programėlėje.

1. Prisiregistruokite prie sandėlio valdymo mobiliosios [programos kaip darbo vartotojas, kurį nustatėte anksčiau šiame straipsnyje skyriuje Paruošti demonstracinius](#prepare-demo-data) duomenis scenarijams. Kaip pavyzdį šiame straipsnyje, vartotojas yra pavadintas *"Vz." Funderburk* ir yra nustatytas sandėliui *61*. (USMF demonstraciniai duomenys turėtų leisti jums prisijungti kaip šio darbo vartotojui įvedant *61* kaip vartotojo ID ir *1* – kaip slaptažodį.)
1. Pagrindiniame meniu pasirinkite **Atsargos**.
1. Meniu **Atsargos** pasirinkite **Skaičiavimas vietoje**.
1. Pasirinkite lauką **Vieta**, įveskite *„01A02R2S1B”*, o tada pasirinkite **GERAI** (varnelės mygtukas).

    Sistema aptinka, kad vieta yra tuščia „Supply Chain Management”.

1. Pasirinkite **Įtraukti LP arba prekę**.
1. Pasirinkite lauką **Prekė**, įveskite *„L0101”*, o tada pasirinkite **GERAI** (varnelės mygtukas).
1. Pasirinkite lauką **Numerio lentelė**, įveskite *„LP\_BULK\_06\_01”*, o tada pasirinkite **GERAI** (varnelės mygtukas).
1. Pasirinkite lauką **Kiekis**, įveskite *9*, o tada pasirinkite **GERAI** (varnelės mygtukas).

    Kadangi sistema aptinka, kad nurodyta numerio lentelė jau yra galima kitoje „Supply Chain Management” vietoje, ši numerio lentelė bus perkelta į dabartinę vietą. Todėl sistema jūsų paprašys patvirtinti perkėlimą.

1. Rinkitės **GERAI** (pažymėkite žymimą mygtuką).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Peržiūrėti 3 scenarijaus ciklo skaičiavimo skirtumus

Norėdami peržiūrėti skaičiavimo rezultatus, atlikite šiuos veiksmus.

1. Sugrįžkite į „Supply Chain Management“.
1. Eikite į **Sandėlio valdymas \> Bendra \> Darbo išsami informacija**.
1. Pasirinkite žymės langelį **Rodyti uždarytus**, esantį tinklelio viršuje.
1. Nustatykite filtrą **Darbo užsakymo tipas** stulpeliui į *Atsargų perkėlimas*.

    Sistema automatiškai aptiko šį skaičiavimą kaip atsargų perkėlimą. Šis perkėlimas leidžiamas, nes parinktis **Leisti numerio lentelės perkėlimus ciklo skaičiavimo metu** yra nustatyta į *Taip* sandėliui *61* puslapyje **Sandėliai**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>4 scenarijus: Ciklo skaičiavimo ribinių verčių apibrėžimas

Vienas būdas sukurti ciklo skaičiavimo darbą yra naudoti ribines vertes. Ciklo skaičiavimo ribinė reikšmė rodo atsargų prekių kiekį arba procentinę ribą. Ciklo skaičiavimo darbas yra automatiškai sukuriamas pasiekus ribinę vertę.

Pavyzdžiui, vietoje, kurios ciklo skaičiavimo ribinė vertė yra 40, yra 60 prekių. Pardavimo užsakymo operacijos metu iš vietos paimamos 25 prekės ir padedamos laikino sandėliavimo vietoje. Kadangi naujasis prekių skaičius (35) yra mažesnis už ribinį kiekį, todėl vietos ciklo skaičiavimo darbas sukuriamas automatiškai.

Atlikite šiuos veiksmus, jei norite nustatyti ciklo skaičiavimo ribines vertes.

1. Pasirinkite **Sandėlio valdymas \> Nustatymai \> Ciklo skaičiavimas \> Ciklo skaičiavimo ribinės reikšmės**.
1. Veiksmų srityje pasirinkite **Nauja** ribinės vertės sukūrimui ir nustatykite jai šias vertes:

    - **Ciklo skaičiavimo ribinės reikšmės ID:** *„L0101”*
    - **Aprašas:** *Ribinė vertė L0101*
    - **Ribinis kiekis:** *2*
    - **Vienetas:** *ea*
    - **Pajėgumo ribinė vertė pagal procentinę dalį:** *0,00*
    - **Ciklo skaičiavimo ribinės vertės tipas:** *Kiekis*
    - **Apdoroti ciklo skaičių nedelsiant:** *Taip*
    - **Dienos tarp ciklo skaičiavimų:** *1*
    - **Darbo telkinio ID:** *„CycleCount”*

1. Veiksmų srityje pasirinkite **Pasirinkti prekes**.
1. Užklausų rengyklės dialogo lango skirtuke **Diapazonas** suraskite eilutę, kurioje **Lauko** laukas yra nustatytas į *Prekės numeris*. Nustatykite **Kriterijų** lauką tai eilutei į *„L0101”*.
1. Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.

    Dabar apibrėžėte prekės *„L0101”* ciklo skaičiavimo ribinę vertę.

Dabar bus sukurtas prekės *„L0101”* ciklo skaičiavimas bet kurioje vietoje, jei turimas kiekis yra mažesnis nei 2 ir, jei vietos paskutinio ciklo skaičiavimo data nėra šiandien.

## <a name="scenario-5-define-cycle-count-plans"></a>5 scenarijus: Ciklo skaičiavimo planų apibrėžimas

Ciklo skaičiavimo planai leidžia jums automatizuoti ciklo skaičiavimo darbo kūrimą. Galite nustatyti kiekvieną ciklo skaičiavimo planą su konkrečios prekės ir vietos užklausomis. Kai vykdoma paketinė užduotis, bus sukurtas visų vietų, kurios atitinka prekės ir vietos kriterijus, ciklo skaičiavimo darbas (iki didžiausio planui nurodyto skaičiavimų skaičiaus). Kai sukuriamas ciklo skaičiavimo darbas, skaičiavimo darbo eilutėje pateikiama informacija apie vietą, kurią reikia suskaičiuoti. Turimos atsargos, susietos su ta vieta, nėra užblokuojamos. Todėl jis galimas rezervavimui ir siunčiamam apdorojimui, net jei yra atidarytas skaičiavimo darbas.

Atlikite šiuos veiksmus, jei norite nustatyti ciklo skaičiavimo planą:

1. Pasirinkite **Sandėlio valdymas \> Nustatymai \> Ciklo skaičiavimas \> Ciklo skaičiavimo planai**.
1. Veiksmų srityje pasirinkite **Nauja**, norėdami įtraukti eilutę į tinklelį ir jai nustatykite toliau pateiktas reikšmes:

    - **Ciklo skaičiavimo plano ID:** *„BULK06”*
    - **Aprašas:** *Vietos skaičiavimas, skirtas „BULK06”*
    - **Darbo telkinio ID:** *„CycleCount”*
    - **Maksimalus ciklo skaičiavimų skaičius:** *10*
    - **Dienos tarp ciklo skaičiavimų:** *10*
    - **Tuščios vietos:** *Neįtraukti tuščių*
    - **Darbo šablonas** – Palikite šį lauką tuščią.

1. Veiksmų srityje pasirinkite **Pasirinkti vietas**.
1. Atsiranda standartinis užklausų rengyklės dialogo langas. Skirtuke **Diapazonas** įtraukite eilutę ir jai nustatykite šias vertes:

    - **Lentelė:** *Vietos*
    - **Laukas:** *Zonos ID*
    - **Kriterijai:** *BULK06*

1. Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.
1. Veiksmų srityje pasirinkite **Apdoroti ciklo skaičiavimo planą**.
1. Dialogo lango **Ciklo skaičiavimo planai** „FastTab” **Paleisti fone** nustatykite parinktį **Paketinis vykdymas** į *Taip*.
1. Pasirinkite **Pasikartojimas**.
1. Dialogo lange **Apibrėžti pasikartojimą** nustatykite paketinę užduotį taip, kad ji būtų paleidžiama nedelsiant kas minutę ir taip, kad nebūtų pabaigos datos.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Apibrėžti pasikartojimą**.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Ciklo skaičiavimo planai**.

    Pranešimas informuos, kad užduotis buvo įtraukta į paketų eilę.

1. Eikite į **Sandėlio valdymas \> Bendra \> Ciklo skaičiavimo planavimas**. Planas prasideda nedelsiant ir sukuria skaičiavimo darbą. Kadangi skaičiavimo darbas nėra užbaigtas, todėl laukas **Būsena** nustatomas į *Apdorojama*. Po vienos minutės, stulpelio **Visi ciklo skaičiavimai** vertė pasikeičia į *1*.

    > [!NOTE]
    > Ciklo skaičiavimo darbas nebus sukurtas, jei dienų skaičius nuo paskutinio ciklo skaičiavimo yra mažesnis nei jūsų nustatyta lauko **Dienos tarp ciklo skaičiavimų** reikšmė ciklo skaičiavimo planui. Pavyzdžiui, jei laukas **Dienos tarp ciklo skaičiavimų** nustatytas į *5*, ciklo skaičiavimo darbas bus kuriamas kas penkias dienas. Tačiau jei ciklo skaičiavimo darbas apdorojamas 3 dieną, kitas ciklo skaičiavimo darbas bus sukurtas po penkių dienų nuo paskutinio ciklo skaičiavimo – 8 dieną.

1. Veiksmų srityje pasirinkite **Darbas**, kad peržiūrėtumėte sukurtą skaičiavimo darbą.
