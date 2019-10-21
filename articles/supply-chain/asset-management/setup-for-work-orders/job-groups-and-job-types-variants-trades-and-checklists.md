---
title: Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai
description: Šioje temoje aprašomos modulio Turto valdymas priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6cb53322b9bdaaa06c6040d8244b7e2ea05336ca
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249614"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių pardavimas ir prižiūrimo turto kontroliniai sąrašai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kiekvienam turto vienetui priskiriamas turto tipas. Pagal turto tipus nustatomi galimų turto priežiūros užduočių tipai (ir priežiūros užduotys). Kurdami darbo užsakymą, privalote pasirinkti priežiūros užduoties tipą. Galite pasirinkti tik tuos priežiūros užduočių tipus, kurie yra susiję su turtui priskirto turto tipo sąranka.

Turto ir priežiūros užduočių tipų bei jų sąsajų su darbo užsakymais grafinė apžvalga pateikiama skyriuje [Turtas ir darbo užsakymai](../overview/functional-locations-and-objects.md).

Priežiūros užduočių tipų variantus galima nustatyti pasirinkus priežiūros užduoties tipą. Priežiūros užduočių tipų variantai – tai skirtingos užduoties tipo versijos, pavyzdžiui, gali skirtis dydis (maža, vidutinė arba didelė), laikotarpis (atliekama kartą per savaitę, kartą per dvi savaites, kartą per mėnesį arba kartą per tris mėnesius) ir konfigūracija (žemo lygio, lanksti arba didelio efektyvumo).

Priežiūros užduočių pardavime pateikiama informacija apie profesionalų paslaugų, pavyzdžiui, mechanikos, elektros ir hidraulikos srityse, pardavimą. Pasirinkus priežiūros užduoties pardavimą, galima nustatyti kompetencijos reikalavimus. Visus priežiūros užduočių pardavimo atvejus galima taikyti visiems priežiūros užduočių tipams. Kuriant darbo užsakymą, pasirinkti priežiūros užduoties tipo variantą ir (arba) priežiūros užduoties pardavimą neprivaloma.

Galima sukurti visų priežiūros užduočių tipų sąrankos variantus. Pavyzdžiui, jei yra priežiūros užduoties tipas, pavadintas **Paslauga**, galite sukurti tokius šio priežiūros užduoties tipo variantus: **Sunkvežimiai 30 000 km**, **Automobiliai 30 000 km** ir **Furgonai 30 000 km**.

Priežiūros užduočių tipų kategorijos naudojamos priežiūros užduočių grupėms kurti apžvalgos tikslais. Galimi priežiūros užduočių tipų kategorijų pavyzdžiai: **Kalibravimas**, **Patikrinimas**, **Kapitalinis remontas** ir **Naudojimasis prietaisais**.

Prižiūrimo turto kontrolinių sąrašų šablonai ir prižiūrimo turto kontrolinių sąrašų kintamieji naudojami prižiūrimo turto kontroliniams sąrašams parengti. Prižiūrimo turto kontroliniai sąrašai nustatomi pagal priežiūros užduočių tipus ir naudojami darbo užsakymuose.

Pirma nustatote reikiamas priežiūros užduočių tipų kategorijas, priežiūros užduočių tipų variantus ir priežiūros užduočių pardavimą. Paskui sukuriate priežiūros užduočių tipus. Galiausiai puslapyje **Priežiūros užduočių tipų numatytosios reikšmės** sukuriate visus priežiūros užduočių tipų variantus, kurių reikia jūsų įrangai. Šiame puslapyje taip pat galite nustatyti prognozes, prižiūrimo turto kontrolinius sąrašus ir priežiūros užduočių tipų derinio įrankius.

> [!NOTE]
> Priežiūros užduoties tipas gali būti susijęs tik su viena priežiūros užduoties tipo kategorija.

## <a name="create-a-maintenance-job-type-category"></a>Priežiūros užduoties tipo kategorijos kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Priežiūros užduočių tipų kategorijos**.
2. Pasirinkite **Naujas**.
3. Lauke **Priežiūros užduoties tipo kategorija** įveskite priežiūros užduoties tipo kategorijos ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.

    Susiejus priežiūros užduočių tipų kategorijas su priežiūros užduočių tipais, lauke **Užduočių tipai** rodomas priežiūros užduočių tipų, susijusių su šia priežiūros užduoties tipo kategorija, skaičius.

![1 pav.](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Priežiūros užduoties tipo varianto kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Priežiūros užduočių tipų variantai**.
2. Pasirinkite **Naujas**.
3. Lauke **Priežiūros užduoties tipo variantas** įveskite priežiūros užduoties tipo varianto ID.
4. Lauke **Aprašas** įveskite aprašą.
5. FastTab **Priežiūros užduočių tipai** pasirinkite **Įtraukti**, kad įtrauktumėte priežiūros užduoties tipą.
6. Lauke **Priežiūros užduoties tipas** pasirinkite priežiūros užduoties tipą.
7. Pakartokite 5–6 veiksmus, kas įtrauktumėte daugiau priežiūros užduočių tipų į priežiūros užduoties tipo variantą.

    FastTab **Išsami informacija** esančiame lauke **Užduočių tipai** rodomas priežiūros užduočių tipų, įtrauktų į šį priežiūros užduoties tipo variantą, skaičius.

![2 paveikslėlis](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Priežiūros užduočių pardavimo kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Priežiūros užduočių pardavimas**.
2. Pasirinkite **Naujas**.
3. Lauke **Pardavimas** įveskite priežiūros užduoties pardavimo ID.
4. Lauke **Aprašas** įveskite aprašą.
5. FastTab **Įgūdžiai** pasirinkite **Įtraukti**, kad įtrauktumėte naują įgūdį, kuris turėtų būti susijęs su priežiūros užduoties pardavimu.
6. Lauke **Įgūdis** pasirinkite įgūdį.
7. Lauke **Lygis** pasirinkite įgūdžių lygį.
8. Pakartokite 5–7 veiksmus, jei norite įtraukti daugiau įgūdžių į priežiūros užduoties pardavimą.

    FastTab **Išsami informacija** esančiame lauke **Įgūdžiai** rodomas įgūdžių, įtrauktų į šį priežiūros užduoties pardavimą, skaičius.

9. FastTab **Sertifikatai** pasirinkite **Įtraukti**, kad įtrauktumėte sertifikatą į priežiūros užduoties pardavimą.
10. Lauke **Sertifikato tipas** pasirinkite sertifikatą.
11. Pakartokite 9–10 veiksmus, jei norite įtraukti daugiau sertifikatų į priežiūros užduoties pardavimą.

    FastTab **Išsami informacija** esančiame lauke **Sertifikatai** rodomas sertifikatų, įtrauktų į šį priežiūros užduoties pardavimą, skaičius.

![3 paveikslėlis](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Prižiūrimo turto kontrolinio sąrašo kintamojo kūrimas

Kai kuriate prižiūrimo turto kontrolinio sąrašo eilutes priežiūros užduoties tipo numatytojoje reikšmėje, turite pasirinkti prižiūrimo turto kontrolinio sąrašo tipą. **Kintamasis** yra vienas iš prižiūrimo turto kontrolinio sąrašo tipų. Jis naudojamas apibrėžiant prižiūrimo turto kontrolinio sąrašo eilutės, kuri yra susijusi su darbo užsakymo eilute, galimą rezultatą kaip intervalą. Pasirinkus kintamąjį, galima nustatyti iš anksto apibrėžtus rezultatus neatliekant tikslaus matavimo.

**1 pavyzdys.** Galite matuoti alyvos lygį, nustatę tris reikšmes: **Per aukštas lygis**, **Per žemas lygis** ir **Tinkamas lygis**. Apibrėžiate, kad kiekvienos reikšmės rezultatas **Pavyko**, **Nepavyko** arba jo **Nėra**.

**2 pavyzdys.** Apžiūrite įrangą ir įvertinate dėvėjimąsi.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Prižiūrimo turto kontroliniai sąrašai** \> **Prižiūrimo turto kontrolinių sąrašų kintamieji**.
2. Pasirinkite **Naujas**.
3. Lauke **Kintamasis** įveskite prižiūrimo turto kontrolinio sąrašo kintamojo ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.
5. FastTab **Bendra** pasirinkite **Įtraukti**, kad įtrauktumėte kintamojo eilutę.

    Lauke **Eilutės numeris** automatiškai pagal eilės tvarką įvedamas eilutės numeris. Įtraukę visas eilutes, jei reikia, galite pakeisti jų numerius. Pasirinkus eilutę ir paskui paspaudus klavišą **Rodyklė žemyn**, į kitą eilutę automatiškai įterpiamas kitas sekos numeris.

6. Lauke **Reikšmė** įveskite reikšmės aprašą.
7. Lauke **Rezultatas** pasirinkite eilutės rezultatą.

![4 paveikslėlis](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Prižiūrimo turto kontrolinio sąrašo šablono kūrimas

Prižiūrimo turto kontrolinių sąrašų šablonus galima naudoti kaip dažnų užduočių, kuriuos darbuotojas turi atlikti, norėdamas tinkamai užpildyti darbo užsakymą, rinkinius. Šablonai kuriami pagal prižiūrimo turto kontrolinio sąrašo eilutes priežiūros užduoties tipo numatytojoje reikšmėje. Šablonai gali būti naudojami keliose priežiūros užduoties tipo numatytosiose eilutėse. Todėl dažnai atliekamų prižiūrimo turto kontrolinių sąrašų užduočių rinkinį lengva naudoti pakartotinai. Į prižiūrimo turto kontrolinių sąrašų šablonus įtraukiamos, pavyzdžiui, bendros saugos instrukcijos ir prekių ir sąlygų, kurias reikia patikrinti konkretaus siurblio arba panašaus modelio konvejerio juostos atveju, sąrašas.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Prižiūrimo turto kontroliniai sąrašai** \> **Prižiūrimo turto kontrolinių sąrašų šablonai**.
2. Pasirinkite **Naujas**.

    Šablono ID automatiškai įterpiamas į lauką **Prižiūrimo turto kontrolinio sąrašo šablonas**.

3. Lauke **Pavadinimas** įveskite prižiūrimo turto kontrolinio sąrašo šablono pavadinimą.
4. FastTab **Prižiūrimo turto kontrolinio sąrašo eilutės** pasirinkite **Įtraukti**, kad įtrauktumėte šablono eilutę.

    Lauke **Eilutės numeris** automatiškai pagal eilės tvarką įvedamas eilutės numeris. Įtraukę visas eilutes, jei reikia, galite pakeisti jų numerius. Pasirinkus eilutę ir paskui paspaudus klavišą **Rodyklė žemyn**, į kitą eilutę automatiškai įterpiamas kitas sekos numeris.

5. Lauke **Tipas** pasirinkite prižiūrimo turto kontrolinio sąrašo eilutės tipą. Laukai, susiję su kiekvienu prižiūrimo turto kontrolinio sąrašo tipu, rodomi FastTab **Eilutės informacija**. Galimos šios vertės:

    - **Tekstas** – eilutėje yra teksto, kuriame aprašomi atliktini veiksmai. Naudokite šį prižiūrimo turto kontrolinio sąrašo tipą, jei norite, kad darbuotojas ką nors patikrintų arba apžiūrėtų, bet nesitikite konkretaus (išmatuojamo) rezultato. Pasirinkę šį tipą, lauke **Pavadinimas** įveskite pavadinimą arba antraštę. Lauke **Instrukcijos** įveskite atliktinų veiksmų aprašą. Jei tam tikras prižiūrimo turto kontrolinio sąrašo veiksmas yra privalomas, parinktyje **Privaloma** pasirinkite **Taip**.
    - **Antraštė** – eilutė naudojama kaip po antrašte pateikiamų prižiūrimo turto kontrolinio sąrašo eilučių grupės antraštė. Šis tipas yra naudingas, jei įtraukėte keletą prižiūrimo turto kontrolinio sąrašo eilučių, kurias galima suskirstyti į konkrečias sritis. Antraštės pateikia apžvalgą darbuotojui, kuris pildys prižiūrimo turto kontrolinį sąrašą, kuriame yra daug prižiūrimo turto kontrolinio sąrašo eilučių. Pasirinkę šį tipą, lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.
    - **Šablonas** – ši eilutė naudojama, norint įtraukti esamą šabloną. Pasirinkę šį tipą, lauke **Pavadinimas** įveskite šablono pavadinimą. Lauke **Šablonas** pasirinkite šabloną.
    - **Kintamasis** – eilutė naudojama apibrėžiant galimą rezultatą kaip intervalą. Informacijos apie tai, kaip nustatyti prižiūrimo turto kontrolinio sąrašo kintamuosius, ieškokite skyriuje [Prižiūrimo turto kontrolinio sąrašo kintamojo kūrimas](#create-a-maintenance-checklist-variable). Pasirinkę šį tipą, lauke **Pavadinimas** įveskite aprašomąjį kintamojo pavadinimą. Lauke **Kintamasis** pasirinkite kintamąjį. Lauke **Instrukcijos** įveskite atliktinų veiksmų aprašą. Jei tam tikras prižiūrimo turto kontrolinio sąrašo veiksmas yra privalomas, parinktyje **Privaloma** pasirinkite **Taip**.
    - **Matavimas** – eilutė naudojama registruojant konkretų matavimo rezultatą. Galite nustatyti matavimą, susijusį su iš anksto nustatytu skaitikliu. Pasirinkę šį tipą, lauke **Pavadinimas** įveskite šablono pavadinimą. Jei šis prižiūrimo turto kontrolinio sąrašo veiksmas yra privalomas, parinktyje **Privaloma** pasirinkite **Taip**. Jei norite naudoti matavimo eilutę skaitikliui registruoti, lauke **Skaitiklis** pasirinkite skaitiklį. Susijęs laukas **Vienetas** atnaujinamas automatiškai. Jei pasirinkote skaitiklį, lauke **Reikšmė** pasirinkite naujinimo metodą. Laukuose **Min. reikšmė** ir **Maks. reikšmė** įveskite leistiną reikšmių intervalą. Lauke **Instrukcijos** įveskite atliktinų veiksmų aprašą.

        > [!NOTE]
        > Visos tipo **Matavimas** eilutės, kuriose nėra skaitiklio sąrankos, laikomos nepriklausomomis matavimo registracijomis, kurioms modulyje Turto valdymas nepriskirti automatiškai atliekami tolesni veiksmai. Taip pat jei pasirinkto skaitiklio tipo nėra su darbo užsakymu susijusiame turte, prižiūrimo turto kontrolinis sąrašas laikomas nepriklausomu matavimu. Skaitiklio reikšmę galima keisti keletą kartų. Ji neregistruojama, kol [darbo užsakymo ciklo būsena](work-order-lifecycle-states.md) nepasikeis į būseną, kurioje parinktyje **Proceso prižiūrimo turto kontrolinis sąrašas** nustatyta **Taip**.

    „FastTab“ **Išsami informacija** esančiame lauke **Patikrinimai** rodomas bendras kontrolinio sąrašo eilučių skaičius šablone. Į šį skaičių įeina visų esamų šablonų įdėtosios eilutės, panaudotos šablone. 

![5 paveikslėlis](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Priežiūros užduoties tipo kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Priežiūros užduočių tipai**.
2. Pasirinkite **Naujas**.
3. Lauke **Priežiūros užduoties tipas** įveskite priežiūros užduoties tipo ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.

    FastTab **Išsami informacija** rodoma šio priežiūros užduoties tipo priežiūros užduočių tipų variantų, įgūdžių, sertifikatų, paskui vykdomų užduočių ir turto tipų skaičiaus apžvalga. Lauke **Sąrankos eilutės** rodomas šio priežiūros užduoties tipo priežiūros užduočių tipų numatytųjų eilučių skaičius. Lauke **Turtas** rodomas aktyviųjų išteklių, kuriuose šiuo metu naudojamas šis priežiūros užduoties tipas, skaičius.

5. FastTab **Bendra** esančiame lauke **Priežiūros užduoties tipo kategorija** pasirinkite priežiūros užduoties tipo kategoriją.
6. Parinktyje **Prižiūrimo turto prastovos veiklos** nustatykite **Taip**, jei pagal priežiūros užduoties tipą prieš atliekant užduotį įrangą reikia sustabdyti priežiūros tikslu.
7. FastTab **Aprašas** įveskite priežiūros užduoties tipo aprašą.
8. FastTab **Priežiūros užduoties tipo variantai** galite įtraukti priežiūros užduoties tipo variantų.
9. FastTab **Reikalingi įgūdžiai** ir **Reikalingi sertifikatai** į priežiūros užduoties tipą galite įtraukti įgūdžių ir sertifikatų reikalavimų.
10. Jei vėliau reikia atlikti tam tikrą priežiūros užduoties tipą, įtraukite jį, pasirinkę FastTab **Paskui vykdomos užduotys**. Taip pat galite nustatyti priežiūros užduoties tipo variantą ir pardavimą, susijusius su priežiūros užduoties tipu. Jei paskui atliekama užduotis turėtų prasidėti praėjus tam tikram dienų skaičiui arba tam tikrą dienų skaičių iki prasidedant šio priežiūros užduoties tipo užduočiai, dienų skaičių įveskite lauke **Atidėjimas dienomis**. Teigiami skaičiai reiškia dienas, praėjusias nuo atitinkamos užduoties pradžios, o neigiami skaičiai reiškia dienas iki prasidedant planuojamai atitinkamai užduočiai. Pavyzdžiui, jei įvesite **5**, paskui atliekama užduotis prasidės po penkių dienų nuo užduoties, susijusios su priežiūros užduoties tipu, pradžios. Jei įvesite **–3**, paskui atliekama užduotis prasidės prieš tris dienas iki užduoties, susijusios su priežiūros užduoties tipu, planuojamos pradžios.

    > [!NOTE]
    > Jei įtrauksite daugiau kaip vieną priežiūros užduoties tipo eilutę, eilučių seka parodo tvarką, kuria jas reikėtų vykdyti. Seka pasideda sąrašo viršuje.

11. FastTab **Turto tipai** į priežiūros užduoties tipą galite įtraukti turto tipų.

![6 paveikslėlis](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Priežiūros užduočių tipų numatytųjų eilučių ir susijusių prognozių, prižiūrimo turto kontrolinių sąrašų, įrankių, aprašo ir priedų kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Priežiūros užduočių tipų numatytosios reikšmės**.

    arba,

    Pasirinkite **Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Priežiūros užduočių tipai**, pasirinkite priežiūros užduoties tipą, paskui pasirinkite **Priežiūros užduočių tipų numatytosios reikšmės**.

2. Pasirinkite **Naujas**.
3. Laukuose **Funkcinė vieta**, **Turto tipas**, **Gamintojas**, **Modelis** ir **Turtas** pasirinkite tinkamas reikšmes, atsižvelgdami į tai, kiek konkreti turėtų būti priežiūros užduoties tipo numatytoji reikšmė.
4. Lauke **Priežiūros užduoties tipas** pasirinkite priežiūros užduoties tipą, jei jis nebuvo pasirinktas automatiškai.
5. Laukuose **Priežiūros užduoties tipo variantas** ir **Pardavimas** pasirinkite reikiamą priežiūros užduoties tipo variantą ir priežiūros užduoties pardavimą.
6. Pasirinkite **Prognozė**.
7. Puslapyje **Priežiūros užduoties tipo numatytoji prognozė** galite prognozuoti valandas, prekes ir išlaidas. Atitinkamuose skirtukuose pasirinkite **Įtraukti**, tada pasirinkite elementus, kad sukurtumėte reikiamas priežiūros užduoties tipo prognozes.
8. Skirtuke **Prekės prognozė** galite pasirinkti atsargų dimensijas, rodytinas prekės eilutėje. Pasirinkite **Atsargos** \> **Dimensijos**, pasirinkite rodytinas dimensijas, parinktyje **Įrašyti sąranką** nustatykite **Taip**, tada pasirinkite **Gerai**.
9. Skirtuke **Prekės prognozė** pasirinkite **Kur naudota prekė**, jei norite pamatyti, kur pasirinktoje eilutėje esanti prekė naudojama modulyje Turto valdymas turto, priežiūros užduoties tipo numatytosios reikšmės, atsarginių dalių ir darbo užsakymų atžvilgiu. 

    FastTab **Priežiūros prognozių sumos** rodoma prognozių sumų apžvalga. Į šią apžvalgą įtrauktas bendras valandų ir sukurtų prognozių eilučių skaičius.

    > [!NOTE]
    > Norėdami nukopijuoti kito priežiūros užduoties tipo prognozės sąranką, pasirinkite **Kopijuoti prognozę**, paskui pasirinkite priežiūros užduoties tipą, kurio sąranką norite nukopijuoti.

11. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.
12. Uždarę puslapį **Priežiūros užduoties tipo numatytoji prognozė**, grįšite į puslapį **Priežiūros užduočių tipų numatytosios reikšmės**.
13. Pasirinkite **Prižiūrimo turto kontrolinis sąrašas**.
14. Puslapyje **Priežiūros užduočių tipų numatytųjų reikšmių kontrolinis sąrašas** į pasirinktą priežiūros užduoties tipo numatytąją reikšmę galite įtraukti prižiūrimo turto kontrolinio sąrašo eilučių. FastTab **Prižiūrimo turto patikrinimo eilutės** pasirinkite **Nauja**, kad įtrauktumėte prižiūrimo turto kontrolinio sąrašo eilutę.

    Eilučių numeriai automatiškai įvedamos į lauką **Eilutės numeris**, taip nurodant prižiūrimo turto kontrolinio sąrašo eilučių seką. Eilučių numerius galite redaguoti pagal savo poreikius. Sukūrę pirmą prižiūrimo turto kontrolinio sąrašo eilutę, pasirinkite eilutę, tada paspauskite klavišą **Rodyklė žemyn**, kad įtrauktumėte eilutę po pasirinkta eilute. Taip pat galite pasirinkti prižiūrimo turto kontrolinio sąrašo eilutę ir paskui pasirinkti **Nauja**. Šiuo atveju nauja eilutė įtraukiama virš pasirinktos prižiūrimo turto kontrolinio sąrašo eilutės.

15. Lauke **Tipas** pasirinkite eilutės tipą, paskui įtraukite informaciją, susijusią su prižiūrimo turto kontrolinio sąrašo eilute. Galimų tipų ir susijusių laukų aprašas pateikiamas skyriuje [Prižiūrimo turto kontrolinio sąrašo šablono kūrimas](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Norėdami nukopijuoti kito priežiūros užduoties tipo prižiūrimo turto kontrolinio sąrašo sąranką, pasirinkite **Kopijuoti prižiūrimo turto kontrolinį sąrašą**, paskui pasirinkite priežiūros užduoties tipą, kurio sąranką norite nukopijuoti.
    >
    > Sukurti šabloną pagal esamą prižiūrimo turto kontrolinį sąrašą tikrai paprasta. Vėliau galėsite pakartotinai naudoti šabloną keliuose prižiūrimo turto kontroliniuose sąrašuose. Naujas šablonas bus aktyviojo prižiūrimo turto kontrolinio sąrašo kopija. Pasirinkite **Kurti šabloną**, paskui įveskite šablono pavadinimą. Norėdami pakeisti esamą prižiūrimo turto kontrolinį sąrašą viena eilute, kurioje yra nuoroda į naują šabloną, parinktyje **Pakeisti** nustatykite **Taip**. Šablono turinį galite peržiūrėti išsamios informacijos puslapyje **Prižiūrimo turto kontrolinio sąrašo šablonai**.

16. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.
17. Grįžkite į puslapį **Priežiūros užduočių tipų numatytosios reikšmės**.
18. Pasirinkite **Įrankiai**.
19. Puslapyje **Priežiūros užduočių tipų numatytieji įrankiai** galite įtraukti priežiūros užduoties tipo įrankius (išteklius). Pasirinkite **Naujas**, tada lauke **Išteklius** pasirinkite įrankį.

    > [!NOTE]
    > Norėdami nukopijuoti kito priežiūros užduoties tipo įrankio sąranką, pasirinkite **Kopijuoti įrankius**, paskui pasirinkite priežiūros užduoties tipą, kurio sąranką norite nukopijuoti.

20. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.
21. Grįžkite į puslapį **Priežiūros užduočių tipų numatytosios reikšmės**.
22. Pasirinkite **Darbo aprašas**.
23. Puslapyje **Darbo aprašas** pasirinkite **Redaguoti**, paskui pagal poreikį įtraukite aprašą, susijusį su pasirinkta priežiūros užduoties tipo numatytąja reikšme.
24. Pasirinkite **Įrašyti**, kad įrašytumėte aprašą.

    Jei čia įtrauksite darbo aprašą, jis pakeis priežiūros užduoties tipo aprašą, nustatytą puslapyje **Priežiūros užduočių tipai**. Jei čia neįtrauksite darbo aprašo, bus naudojamas nustatytas priežiūros užduoties tipo aprašas. Aprašai automatiškai perkeliami į darbo užsakymus, kuriuose naudojami priežiūros užduoties tipas arba priežiūros užduoties tipo numatytoji reikšmė.

25. Grįžkite į puslapį **Priežiūros užduočių tipų numatytosios reikšmės**.
26. Norėdami nustatyti pasirinktos priežiūros užduoties tipo numatytosios eilutės priedus, pasirinkite **Pridėti dokumentus**. Priedai, nustatyti priežiūros užduoties tipo numatytojoje eilutėje, automatiškai įtraukiami į darbo užsakymo eilutes, kuriose naudojama minėta priežiūros užduoties tipo numatytoji eilutė.
27. Pasirinkite **Naujas**, tada pasirinkite dokumento tipą.
28. Nusiųskite dokumentą arba failą.
29. Nustatykite laukus puslapyje **Priedai**. Nustatant priedus naudojama standartinė dokumentų sąrankos funkcija.
30. Pasirinkite **Įrašyti**, kad įrašytumėte priedą.

    > [!NOTE]
    > Priežiūros užduoties tipo numatytosios eilutės priedai spausdinami kartu su darbo užsakymo ataskaita, tik jei priedų dokumentų tipai pasirinkti skirtuke **Dokumentų tipai** puslapyje **Turto valdymo parametrai** (**Turto valdymas** \> **Sąranka** \> **Turto valdymo parametrai**). Priedai gali būti, pavyzdžiui, gairės, kuriose paaiškinama, kaip atlikti tam tikrą užduotį, arba iš anksto nustatytas prižiūrimo turto kontrolinis sąrašas (jei nenaudojate priežiūros užduočių tipų numatytųjų eilučių prižiūrimo turto kontrolinio sąrašo funkcijos).

    Puslapyje **Priežiūros užduočių tipų numatytosios reikšmės** kiekvienoje eilutėje rodomas prognozuojamų valandų skaičius ir prekių, išlaidų, prižiūrimo turto kontrolinių sąrašų ir įrankių sukurtų eilučių skaičius. Lauke **Turtas** rodomas aktyviųjų išteklių, susijusių su priežiūros užduoties tipo numatytąja eilute, skaičius.

31. Norėdami nukopijuoti priežiūros užduoties tipo numatytąją reikšmę į kitos priežiūros užduoties tipo numatytąją reikšmę, pasirinkite priežiūros užduoties tipo numatytąją eilutę, į kurią norite nukopijuoti kitą sąranką, pasirinkite **Kopijuoti sąranką**, paskui pasirinkite priežiūros užduoties tipo numatytąją reikšmę, kurią norite nukopijuoti.
32. Norėdami peržiūrėti turto, priežiūros planų arba priežiūros ciklų, kuriuose šiuo metu naudojama priežiūros užduoties tipo numatytoji eilutė, sąrašą, pasirinkite eilutę, tada pasirinkite **Naudoja**.

![7 paveikslėlis](media/07-setup-for-work-orders.png)

Kai sistema pasirenka galimą priežiūros užduoties tipo numatytąją reikšmę, kuri turėtų būti naudojama darbo užsakymo eilutėje, pasirinkimą lemia turtas ir susijusio turto tipo sąranka. Modulyje Turto valdymas ieškant galimų atitikčių peržiūrimi visi priežiūros užduočių tipų numatytieji įrašai, susiję su priežiūros užduoties tipu, kuris yra susijęs su turto tipu. Visada pirmiausia tikrinami konkrečiausi deriniai. Kitaip tariant, siekiant nustatyti konkrečiausią derinį, modulyje Turto valdymas pirmiausia ieškoma galimo lauko **Pardavimas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipo variantas** atitikties. Jei atitikties nerandama, tikrinama, ar yra lauko **Priežiūros užduoties tipas** atitikties ir t. t. (**Pardavimas**, paskui **Priežiūros užduoties tipo variantas**, paskui **Priežiūros užduoties tipas**, paskui **Turtas**, paskui **Modelis**, paskui **Gamintojas**, paskui **Turto tipas**). Jeigu atitikties nerandama, naudojamas numatytasis įrašas, kuriame pasirinktas tik priežiūros užduoties tipas.

Projekto veiklos ID automatiškai susiejamas su kiekviena sukurta priežiūros užduoties tipo numatytąja eilute. Projekto veikla sukuriama prognozės projekte, pasirinktame lauke **Priežiūros prognozės projektas** skirtuke **Turtas** puslapyje **Turto valdymo parametrai**. Projekto veiklos tikslas yra valdyti valandų, prekių ir išlaidų prognozes, susijusias su darbo užsakymais. Priežiūros užduočių tipų prognozės automatiškai perkeliamos į darbo užsakymo eilutę ir kopijuojamos iš prognozės projekto į sukurtą darbo užsakymo eilutės darbo užsakymo projektą. Projekto veiklos tikslas yra valdyti prognozes, susijusias su darbo užsakymais.

Galite nustatyti paketinę užduotį, siekdami reguliariai naujinti priežiūros užduoties tipo numatytąsias nuorodas, arba galite paleisti užduotį rankiniu būdu. Norėdami sukurti paketinę užduotį arba paleisti naujinimą rankiniu būdu, pasirinkite **Turto valdymas** \> **Periodinis** \> **Prevencinė priežiūra** \> **Naujinti priežiūros užduoties tipo numatytąsias nuorodas**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Priežiūros užduočių tipų, susijusių su turtu, apžvalga

Sukūrę reikiamus priežiūros užduočių tipų numatytuosius derinius, puslapyje **Visas turtas** matysite esamos priežiūros užduoties tipo numatytosios reikšmės, susijusios su konkrečiu turtu, apžvalgą. Apžvalgoje rodomi visi priežiūros užduočių tipų numatytųjų reikšmių deriniai, kurie gali būti naudojami pasirinkto turto tipo atžvilgiu. Šie deriniai apima derinius, kuriose yra skirtingų priežiūros užduočių tipų variantų ir priežiūros užduočių pardavimų.

1. Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas** arba **Aktyvus turtas**.
2. Sąraše pasirinkite turto, kurio priežiūros užduočių tipų derinių apžvalgą norite pamatyti.
3. Veiksmų srities skirtuko **Bendra** grupėje **Susijusi informacija** pasirinkite **Priežiūros užduočių tipai**.

    Kairiojoje puslapio **Turto priežiūros užduočių tipai** srityje rodomas visų priežiūros užduočių tipų derinių, susijusių su pasirinktu turtu, sąrašas.

4. Pasirinkę priežiūros užduočių tipų derinį, pamatysite susijusią prižiūrimo turto kontrolinių sąrašų, prognozių ir įrankių sąranką. Skyriuje **Išsami informacija** FastTab **Priežiūros užduočių tipų numatytosios reikšmės** rodomas susijusių prižiūrimo turto kontrolinių sąrašų, prognozuojamų valandų, prekių ir t. t., kurie yra susiję su pasirinktu priežiūros užduočių tipų deriniu, skaičius.
5. Norėdami peržiūrėti išsamią informaciją apie pasirinktą priežiūros užduoties tipą, pasirinkite **Priežiūros užduočių tipai**.

![8 paveikslėlis](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Priežiūros užduočių tipų prognozių automatinis naujinimas

Modulyje Turto valdymas galima automatiškai naujinti priežiūros užduočių tipų prognozių dėl valandos kainų, prekių kainų ir išlaidų informaciją, kuri buvo atnaujinta kituose moduliuose. Taip užtikrinsite, kad priežiūros užduočių tipų prognozėse visada naudojamos aktualiausios savikainos.

1. Pasirinkite **Turto valdymas** \> **Periodinis** \> **Prognozė** \> **Naujinti priežiūros užduoties tipo prognozę**.
2. Dialogo lango **Naujinti priežiūros užduoties tipo prognozę** FastTab **Įtrauktini įrašai** pagal poreikį galite pasirinkti konkrečių priežiūros užduočių tipų parametrus. Pasirinkite **Filtras**, tada pasirinkite **Pasirinkti**, kad pasirinktumėte parametrus.
3. FastTab **Vykdyti fone** pagal poreikį galite nustatyti automatinio naujinimo paketinę užduotį.
4. Pasirinkus **Gerai**, pradedamas prognozės naujinimas.
