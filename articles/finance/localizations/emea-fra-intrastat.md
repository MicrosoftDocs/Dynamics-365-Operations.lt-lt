---
title: Prancūzijos „Intrastat”
description: Šioje temoje pateikiama informacija apie „Intrastat” deklaraciją Prancūzijoje.
author: andosip
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: d38169d73caf93a0f81e832293916c9e54855a1848fe6ab409a670a4bf707b7c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713141"
---
# <a name="french-intrastat"></a>Prancūzijos „Intrastat”

[!include[banner](../includes/banner.md)]

Prancūzijos įmonės, kurios yra užregistruotos pridėtiniam vertės mokesčiui (PVM) ir kuriuos prekiauja su kitomis Europos Sąjungos (ES) šalimis, turi deklaruoti prekes ir paslaugas, atvykstančias į Prancūziją ir išvykstančias iš Prancūzijos. „Declaration d'exchanges de biens” (Prekių prekybos deklaracija arba DEB) yra ES pardavimų sąrašo ir „Intrastat” ataskaitos derinys. Šią ataskaitą turite pateikti kas mėnesį visiems ES vidaus prekių pardavimams.

Galite generuoti DEB ataskaitą vienu iš dviejų elektroninio teksto failo formatų: „SAISUNIC 330” arba „INTRACOM” formatu.

Toliau pateiktoje lentelėje rodomi laukai, įtraukti į Prancūzijos „Intrastat” deklaraciją „SAISUNIC 330” formatu.

| **Laukas**                   | **Ataskaitos lygis**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (supaprastintas)** | **1 (pilnas)** |
| Nuorodos laikotarpis         | X                  | X            |
| Deklaracijos numeris       | X                  | X            |
| Eilutės numeris                 | X                  | X            |
| Šalies ISO kodas (FR)       | X                  | X            |
| Papildomas kodas          | X                  | X            |
| Sirenos numeris                | X                  | X            |
| Kliento PVM kodas        | X                  | X            |
| Krypties Kodas              | X                  | X            |
| Operacijos tipas            | X                  | X            |
| Įsipareigojimo Lygis            | X                  | X            |
| Prekės Kodas              |                    | X            |
| Nacionalinis NGP                |                    | X            |
| Apskritis (Padalinys)         |                    | X            |
| Operacijos Pobūdis       |                    | X            |
| Kilmės Šalis      |                    | X            |
| Kilmės šalis – Importavimai |                    | X            |
| Galutinė paskirties vieta – Eksportavimai |                    | X            |
| Sąskaitos faktūros reikšmė               | X                  | X            |
| Statistinė Vertė           |                    | X            |
| Grynasis Svoris                  |                    | X            |
| Papildomi Vienetai            |                    | X            |
| Transportavimo Kodas              |                    | X            |

Toliau pateiktoje lentelėje rodomi laukai, įtraukti į Prancūzijos „Intrastat” deklaraciją „INTRACOM” formatu.

| **Laukas**                   | **Ataskaitos lygis**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (supaprastintas)** | **1 (pilnas)** |
| Kodas                        | X                  | X            |
| Deklaracijos numeris       | X                  | X            |
| Eilutės numeris              | X                  | X            |
| Sirena                       | X                  | X            |
| Apskritis (Padalinys)         |                    | X            |
| Transportavimo Kodas              |                    | X            |
| Kilmės Šalis           |                    | X            |
| Operacijos Pobūdis       |                    | X            |
| Sąskaitos faktūros reikšmė               | X                  | X            |
| Pristatymo Būdai           |                    | X            |
| Operacijos tipas            | X                  | X            |
| Įsipareigojimo Lygis            | X                  | X            |
| Prekės Kodas              |                    | X            |
| Nacionalinis NGP                |                    | X            |
| Grynasis Svoris                  |                    | X            |
| Statistinė Vertė           |                    | X            |
| Papildomi Vienetai            |                    | X            |
| Kilmės šalis – Importavimai |                    | X            |
| Galutinė paskirties vieta – Eksportavimai |                    | X            |
| Kliento PVM kodas        | X                  | X            |
| Papildomas kodas          | X                  | X            |
| Nuorodos laikotarpis         | X                  | X            |

### <a name="set-up-intrastat"></a>„Intrastat” nustatymas

1.  [„Microsoft Dynamics Lifecycle Services” (LCS)](https://lcs.dynamics.com/Logon/Index) bendrai naudojamo turto bibliotekoje atsisiųskite naujausias šių Elektroninių ataskaitų (ER) konfigūracijų versijas „Intrastat” deklaracijai:

-   Intrastat modelis

-   Intrastat ataskaita

-   Intrastat INTRACOM (FR)

-   Intrastat SAISUNIC (FR)

Norėdami daugiau informacijos žr. [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  „Dynamics 365 Finance” eikite į **Mokesčiai** &gt; **Nustatymas** &gt; **Užsienio prekyba** &gt; **Užsienio prekybos parametrai** ir atlikite šiuos veiksmus:

    1.  Skirtuko **„Intrastat”** „FastTab” **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **„Intrastat” INTRACOM (FR)** arba **„Intrastat” SAISUNIC (FR)**.

    2.  **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.

    3.  „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** pasirinkite **„Intrastat”**.

    4.  „FastTab” **Bendra** lauke **Operacijos kodas** pasirinkite kodą, kuris naudojamas prekių perkėlimams.

    5.  Lauke **Kredito pažyma** pasirinkite kodą, kuris naudojamas prekių grąžinimams.

    6.  Lauke **Įsipareigojimo lygis eksportui** įveskite eksportavimo ataskaitos išsamumo lygį. Nuo lygio, kurį pasirenkate, priklauso ataskaitoje rodomos eilutės. Daugiau informacijos ieškokite lentelėse, esančiose šios temos pradžioje.

3.  Eikite į **Organizacijos administravimas** &gt; **Organizacijos** &gt; **Juridiniai subjektai**, pasirinkite savo įmonę ir tada atlikite šiuos veiksmus:

    1.  „FastTab” **Registracijos numeriai** lauke **NAF kodas** įveskite savo NAF kodą. Daugiau informacijos rasite [FR-00003 NAF kodai ir „Siret” numeriai](tasks/fr-00003-naf-codes-siret-numbers.md).

    2.  „FastTab” **Užsienio prekyba ir logistika** skyriuje **„Intrastat”** nustatykite **Neapmokestinamo PVM numerio eksportavimas** ir **Neapmokestinamo PVM numerio importavimas** laukus.

    3.  FastTab **Mokesčių registracija** lauke **Mokesčių mokėtojo kodas** įveskite savo įmonės mokesčių mokėtojo kodą.

4.  Norėdami nurodyti NAF kodus ir neapmokestinimo numerius klientams, eikite į **Gaunamos sumos** &gt; **Klientai** &gt; **Visi klientai** ir atlikite šiuos veiksmus:

    1.  Pasirinkite klientą.

    2.  „FastTab” **Sąskaita faktūra ir pristatymas** skyriaus **PVM** lauke **Neapmokestinimo numeris** įveskite kliento neapmokestinimo numerį.

    3.  „FastTab” **Pardavimų demografiniai duomenys** lauke **Prancūzų Siret** įveskite įmonės Siret numerį.

    4.  Lauke **NAF kodas** įveskite įmonės NAF kodą.

    5.  Pakartokite šiuos veiksmus kitiems klientams.

5.  Norėdami nurodyti NAF kodus ir neapmokestinimo numerius tiekėjams, eikite į **Mokėtinos sumos** &gt; **Tiekėjai** &gt; **Visi tiekėjai** ir atlikite šiuos veiksmus:

    1.  Pasirinkite tiekėją.

    2.  „FastTab” **Sąskaita faktūra ir pristatymas** skyriaus **PVM** lauke **Neapmokestinimo numeris** įveskite tiekėjo neapmokestinimo numerį.

    3.  „FastTab” **Pirkimų demografiniai duomenys** lauke **Prancūzų Siret** įveskite įmonės Siret numerį.

    4.  Lauke **NAF kodas** įveskite įmonės NAF kodą.

    5.  Pakartokite šiuos veiksmus kitiems tiekėjams.

6.  Eikite į **Mokesčiai** &gt; **Nustatymas** &gt; **Užsienio prekyba** &gt; **„Intrastat” glaudinimas** ir pasirinkite laukus, kurie turi būti lyginami apibendrinant „Intrastat” informaciją. Prancūzijos „Intrastat” pasirinkite **Statistikos procedūra**, **Pradinė būsena**, **Kilmės šalis/regionas**, **Pristatymo sąlygos**, **Transportavimas**, **Pataisymas**, **Šalis/regionas**, **Kilmės/paskirties vietos apskritis**, **Kryptis**, **Siuntėjo šalis/regionas**, **Siuntėjo būsena**, **Būsena**, **Operacijos kodas** ir **Prekė**.

7.  Eikite į **Sandėlio valdymas** &gt; **Nustatymas** &gt; **Sandėlis** &gt; **Sandėliai**, pasirinkite sandėlį, o tada atlikite šiuos veiksmus:

    1.  „FastTab” **Adresai** pasirinkite **Įtraukti** arba **Redaguoti**.

    2.  Dialogo lango lauke **Miestas** pasirinkite sandėlio miestą. Jūsų DEB ataskaitoje miesto būsena bus naudojama kaip rajonas.

### <a name="ngp-codes"></a>NGP kodai

DEB ataskaitoje produktų kodifikavimą sudaro toliau pateikti elementai:

1.  Aštuonių skaitmenų CN8 kodas, nurodantis ES tarifą ir statistinę nomenklatūrą.

2.  Jei taikoma, vieno skaitmens „Nomenclature Générale des Produits” (NGP) nacionalinis prekės kodas.

2021 metais NGP taikomas tik trims produktų tipams:

-   Kai kuriems produktams iš karvių, avių ir ožkų

-   Karinei įrangai

-   Prancūzijos vynams

Privalote nustatyti NGP kodus ir priskirti juos susijusiems produktams. Tada **„NGP”** laukas yra automatiškai nustatomas **„Intrastat” žurnalo** puslapyje.

#### <a name="set-up-an-ngp-code"></a>Nustatykite NGP kodą

1.  Eikite į **Mokesčiai** &gt; **Nustatymas** &gt; **Užsienio prekyba** &gt; **NGP kodai**.

2.  Veiksmų srityje pasirinkite **Nauja** tam, kad sukurtumėte NGP kodą.

3.  Lauke **„NGP”** įveskite vieno skaitmens kodą.

4.  Lauke **Aprašas** įveskite kodo aprašą.

#### <a name="assign-an-ngp-code-to-a-product"></a>Priskirkite NGP kodą produktui

1.  Eikite į **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Patvirtinti produktai**.

2.  Tinklelyje pasirinkite produktą.

3.  „FastTab” **Užsienio prekyba** skyriaus **„Intrastat”** lauke **„NGP”** pasirinkite atitinkamą NGP kodą.

## <a name="intrastat-journal"></a>„Intrastat” žurnalas

Eikite į **Mokesčiai** &gt; **Deklaracijos** &gt; **Užsienio** **prekyba** &gt; **„Intrastat”**, kad valdytumėte savo operacijas, taikomas užsienio prekybas su ES šalimis. Daugiau informacijos rasite [„Intrastat” apžvalga](emea-intrastat.md).

**„NGP”** stulpelis yra būdingas tik Prancūzijai. Jame rodomas produkto NGP kodas. Jei NGP netaikomas produktui, rodomas **„0”** (nulis). Jūs galite koreguoti NGP kodą. Pasirinkite operaciją, o tada, skirtuko **Bendra** skyriaus **Kodai** lauke **„NGP”** pasirinkite reikiamą NGP kodą.

### <a name="intrastat-transfer"></a>„Intrastat” perkėlimas

Veiksmų srities puslapyje **„Intrastat”** galite pasirinkti **Perkelti**, kad informacija apie ES vidaus prekybą būtų automatiškai perkelta iš jūsų pardavimo užsakymų, laisvos formos SF, pirkimo užsakymų, tiekėjo SF, tiekėjo produktų gavimo kvitų, projekto SF ir perkėlimo užsakymų. Bus perkelti tik dokumentai, kurių paskirties šalis ar regionas (išsiuntimams) arba siuntimas (įsigijimams) yra ES šalis.

Kadangi DEB ataskaita yra ES pardavimų sąrašo ir „Intrastat” ataskaitos derinys, joje taip pat yra *trišalės* operacijos, kuriose tiesioginis pristatymas atliekamas iš vienos ES šalies (A šalies) į kitą ES šalį (C šalį), o Prancūzijos juridinis subjektas (B šalis) yra trišalio sandorio viduryje.

### <a name="generate-a-deb-intrastat-report"></a>DEB „Intrastat” ataskaitos generavimas

1.  Eikite į **Mokesčiai** &gt; **Deklaracijos** &gt; **Užsienio prekyba** &gt; **„Intrastat”**.

2.  Veiksmų srityje pasirinkite **Išvestis** &gt; **Ataskaita**.

3.  Dialogo lange **„Intrastat” ataskaita** nustatykite toliau nurodytus laukus.

| Laukas            | Aprašas                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Nuo datos        | Pasirinkite ataskaitos pradžios datą.                                                                                               |
| Iki datos          | Pasirinkite ataskaitos pabaigos datą.                                                                                                 |
| Sugeneruoti failą    | Šią parinktį nustatykite į **Taip**, kad sugeneruotumėte .txt failą.                                                                                 |
| Failo vardas        | Įveskite savo „Intrastat” ataskaitos .txt failo pavadinimą.                                                                          |
| Generuoti ataskaitą  | Šią parinktį nustatykite į **Taip**, kad sugeneruotumėte .xml failą.                                                                                |
| Ataskaitos failo vardas | Įveskite reikiamą pavadinimą.                                                                                                            |
| Tik pataisymai | Šioje parinktyje nustatykite **Taip**, kad būtų pranešama tik apie pataisymus. Nustatykite **Ne**, kad būtų pranešama ir apie įprastas operacijas, ir apie pataisymus.         |
| Kryptis        | Pasirinkite **Įsigijimai** ataskaitai apie ES vidaus įsigijimus. Pasirinkite **Išsiuntimai** ataskaitai apie ES vidaus išsiuntimus. |

## <a name="example"></a>Pavyzdys

Toliau pateikiamas pavyzdys, kaip nustatyti ir dirbti su NGP kodais. Jis naudoja **„DEMF”** juridinį subjektą.

1.  [„Microsoft Dynamics Lifecycle Services” (LCS)](https://lcs.dynamics.com/Logon/Index) bendrai naudojamo turto bibliotekoje atsisiųskite naujausias šių ER konfigūracijų versijas „Intrastat” deklaracijos formatui:

-   Intrastat modelis

-   Intrastat ataskaita

-   Intrastat INTRACOM (FR)

2.  „Finance” nustatykite operacijos kodą:

    1.  Eikite į **Mokesčiai** &gt; **Nustatymas** &gt; **Užsienio prekyba** &gt; **Operacijos kodai**.

    2.  Veiksmų srityje pasirinkite **Naujas**.

    3.  Lauke **Operacijos kodas** įveskite **„11”**.

    4.  Lauke **Pavadinimas** įveskite **Pirkimas arba pardavimas**.

    5.  Veiksmų srityje pasirinkite **Įrašyti**.

3.  Norėdami nustatyti produktų hierarchiją:

    1.  Eikite į **Produkto informacijos valdymas** &gt; **Nustatymas** &gt; **Kategorijos ir atributai** &gt; **Kategorijų hierarchijos**.

    2.  Tinklelyje pasirinkite **„Intrastat”**. Tada veiksmų srities skirtuko **Kategorijų hierarchija** grupėje **Prižiūrėti** pasirinkite **Redaguoti**.

    3.  Veiksmų srityje pasirinkite **Naujas kategorijos mazgas**.

    4.  Lauke **Pavadinimas** įveskite **„Autres Libournais”**.

    5.  Lauke **Kodas** įveskite **„2204 21 42”**

    6.  Veiksmų srityje pasirinkite **Įrašyti**.

4.  Eikite į **Mokesčiai** &gt; **Nustatymas** &gt; **Užsienio prekyba** &gt; **Užsienio prekybos parametrai** ir atlikite šiuos veiksmus:

    1.  „FastTab” **Bendra** skirtuko **„Intrastat”** lauke **Operacijos kodas** pasirinkite **„11”**.

    2.  „FastTab” **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **„Intrastat” INTRACOM (FR)**.

    3.  **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.

    4.  „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** pasirinkite **„Intrastat”**.

5.  Norėdami nustatyti NGP kodą:

    1.  Eikite į **Mokesčiai** &gt; **Nustatymas** &gt; **Užsienio prekyba** &gt; **NGP kodai**.

    2.  Veiksmų srityje pasirinkite **Naujas**.

    3.  **NGP** laukelyje įveskite **8**.

    4.  Lauke **Aprašo pavadinimas** įveskite **„NGP 8”**.

    5.  Veiksmų srityje pasirinkite **Įrašyti**.

6.  Norėdami priskirti NGP kodą produktui:

    1.  Eikite į **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Patvirtinti produktai**.

    2.  Tinklelyje pasirinkite **„0001”**.

    3.  „FastTab“ **Užsienio prekyba** lauke **„NGP”** pasirinkite **„8”**.

    4.  Lauke **Prekė** pasirinkite **„2204 21 42”**.

    5.  Veiksmų srityje pasirinkite **Įrašyti**.

7.  Norėdami sukurti pardavimo užsakymą, kuriame būtų naujas produktas:

    1.  Eikite į **Gautinos sąskaitos** &gt; **Užsakymai** &gt; **Visi pardavimo užsakymai**.

    2.  Veiksmų srityje pasirinkite **Naujas**.

    3.  Dialogo lango **Kurti** **pardavimo** **užsakymą** skyriaus **Klientas** lauke **Kliento** **paskyra** pasirinkite **„100001”**.

    4.  Skyriaus **Adresas** lauke **Pristatymo adresas** pasirinkite pliuso ženklą (**„+”**), kad sukurtumėte adresą.

    5.  Dialogo lango **Naujas adresas** lauke **Aprašo pavadinimas** įveskite **Vokietija**.

    6.  Lauke **Šalis/regionas** pasirinkite **„DEU”**.

    7.  Pasirinkite **Gerai**.

    8.  Dialogo lange **Sukurti pardavimo užsakymą** pasirinkite **Gerai**.

    9.  „FastTab” **Pardavimo** **užsakymo eilutės** lauke **Prekės numeris** pasirinkite **„0001”**.

    10. Veiksmų srityje pasirinkite **Įrašyti**.

    11. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.

    12. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**. Tada pasirinkite **Gerai**, kad užregistruotumėte sąskaitą faktūrą.

8.  Norėdami sukurti DEB ataskaitą:

    1.  Eikite į **Mokesčiai** &gt; **Deklaracijos** &gt; **Užsienio prekyba** &gt; **„Intrastat”**:

    2.  Veiksmų srityje. pasirinkite **Perkelti**.

    3.  Dialogo lango **„Intrastat” (Perkelti)** skyriuje **Parametrai** nustatykite **Kliento sąskaitos faktūros** parinktį į **Taip**. Tada pasirinkite **Gerai**.

    4.  Rikiuoti operacijas pagal **Datos** lauką. Aukščiausia operacija yra gauta operacija. Laukas **„NGP”** nustatomas automatiškai.

    5.  Veiksmų srityje pasirinkite **Išvestis** &gt; **Ataskaita**.

    6.  Dialogo lango **„Intrastat” ataskaita**, esančio „FastTab” **Parametrai** skyriuje **Data** pasirinkite sukurto pardavimo užsakymo mėnesį.

    7.  Skyriuje **Eksportavimo parinktys** nustatykite parinktį **Generuoti failą** į **Taip**.

    8.  Lauke **Failo pavadinimas** įveskite reikiamą pavadinimą.

    9.  Pasirinkite **Gerai** ir peržiūrėkite ataskaitą.

