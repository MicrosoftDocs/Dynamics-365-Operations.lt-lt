---
title: „Regression Suite Automation Tool“ mokymo programos nustatymas ir įdiegimas
description: Šiame straipsnyje aprašoma, kaip nustatyti ir įdiegti regresijos komplekto automatizavimo įrankį (RSAT).
author: tonyafehr
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: ced1300b268df9a6503ce1d33d74cae85ade3f20
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103157"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>„Regression Suite Automation Tool“ mokymo programos nustatymas ir įdiegimas

Šiame straipsnyje yra mokymo programa, kuri padeda gauti sąranką ir pradėti naudoti RSAT bei įrankius, susijusius su RSAT.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu.

## <a name="key-concepts"></a>Pagrindinės koncepcijos

- Supraskite diegimo ir būtinųjų komponentų sąranką, kurios reikia įvairioms programoms, palaikančioms „Regression suite automation tool“ (RSAT).
- Sužinokite, kaip užduočių įrašymo priemonės funkcija kartu su „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Microsoft Azure DevOps“ leidžia kurti, konfigūruoti, vykdyti, tirti ir pateikti testavimo atvejų ataskaitas.
- Įgalinkite funkcinius vartotojus įrašyti verslo užduotis naudojant užduočių įrašymo priemonę ir konvertuoti užduočių įrašus į automatinių testų paketą nereikalaujant rašyti pirminio kodo.

## <a name="before-you-begin"></a>Prieš pradedant

### <a name="prerequisites"></a>Būtinieji komponentai

- Norint paleisti šią mokymo programą reikia aplinkos, kurioje veiktų „Microsoft Dynamics 365 for Finance and Operations“ 10.0 (2019 m. balandžio mėn.) arba naujesnė versija. Klientai, naudojantys „Microsoft Dynamics 365 for Finance and Operations“, gali naudotis ir „Enterprise Edition 7.3“, „Platform Update 20“ (PU20) arba naujesnes versijas.
- Vartotojas turi turėti administratoriaus teises į šią aplinką.
- Turite turėti prieigą prie kliento nuomotojo LCS ir „Azure DevOps“ (anksčiau žinomos kaip „Microsoft Visual Studio Team Services“ \[VSTS\]).
- Vartotojas, kuris kuria ir valdo testavimo paketus, turi turėti „Azure DevOps“ testavimo planavimo arba testavimo vadovo licenciją. Šios licencijos irgi suteikia prieigą prie testavimo planų:
    - „Visual Studio Enterprise“ licencija
    - „Visual Studio Test Professional“ licencija
    - MSDN platformų prenumeratoriaus licencija
- RSAT turi turėti prieigą prie testavimo aplinkos per interneto naršyklę.
- Norėdami sugeneruoti ir redaguoti testavimo parametrus, turite būti įdiegę „Microsoft Excel“.

## <a name="configure-azure-devops"></a>Konfigūruoti „Azure DevOps“

### <a name="user-eligibility"></a>Vartotojo tinkamumas

Įsitikinkite, kad vartotojas yra sukurtas „Azure DevOps“ ir turi prenumeratos lygį, kuris suteikia prieigą prie „Azure“ testavimo planų. „Azure DevOps“ testavimo planų licencija reikalinga tik tada, kai vartotojas sukurs ir tvarkys testavimo atvejus (t. y. ne visi RSAT vartotojai turi turėti šią licenciją). Norėdami gauti informacijos apie licencijos reikalavimus, žr. [Licencijos reikalavimai](/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Naujo „Azure DevOps“ projekto kūrimas

RSAT naudoja „Azure DevOps“ testavimo atvejams ir testavimo paketui valdyti, ataskaitoms ir testavimo vykdymo rezultatų analizei.

> [!NOTE]
> Galite naudoti esamą „Azure DevOps“ projektą. Tačiau, jei jūsų esamas „Azure DevOps“ projektas nustatytas taip, kad jis būtų su pasirinktiniu šablonu, jums bus parodytas klaidos pranešimas VSTS sinchronizavimo triktis, kai sinchronizuojate testavimo atvejus iš verslo procesų modeliavimo įrankio (BPM) su „Azure DevOps“ (žr. skyrių [Sinchronizavimo iš BPM su „Azure DevOps“ testavimas](#test-the-synchronization-from-bpm-to-azure-devops)). Jei pasirinktiniam šablonui pritaikytos šios geriausios praktikos, galėsite sinchronizuoti testavimo atvejus su „Azure DevOps“. (Šie geriausios praktikos pavyzdžiai pateikti klaidos pranešime.)

- Nepanaikinkite jokių darbo elementų tipų ar netipinių laukų.
- Nepanaikinkite jokių darbo elemento tipo būsenų.
- Į darbo elemento tipą neįtraukite jokių privalomų laukų.

![Klaidos pranešimas, kuriame pateikiamas geriausios praktikos pavyzdžių sąrašas.](./media/setup_rsa_tool_02.png)

Kitu atveju pagal šią mokomąją programą rekomenduojame sukurti naują „Azure DevOps“ projektą. Norėdami gauti daugiau informacijos, žr. [Problemos, kylančios sinchronizuojant su BPM naudojant pasirinktinį „Azure DevOps“ (VSTS proceso šabloną](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/)).

1. Atidarykite „Azure DevOps“ URL (`https://dev.azure.com/<Azure DevOps Name>`).
2. Pasirinkite **Kurti projektą** viršutiniame dešiniajame „Azure DevOps“ puslapio kampe.

    ![Projekto kūrimo mygtukas.](./media/setup_rsa_tool_03.png)

3. Užpildykite šiuos laukus ir pasirinkite **Kurti**:

    - **Projekto pavadinimas**
    - **Versijų valdymas** – pasirinkite **Team Foundation Version Control**. Atkreipkite dėmesį, kad numatytoji parinktis **Git** nepalaikoma.
    - **Darbo elemento apdorojimas**

    ![Naujo projekto kūrimo dialogo langas.](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Asmeninės prieigos atpažinimo ženklo kūrimas

Šiojo mokymo programoje naudosite LCS verslo procesų modeliavimo įrankį (BPM) ir kursite testavimo atvejų biblioteką bei sinchronizuosite testavimo atvejus su „Azure DevOps“. Jums reikės asmeninės prieigos atpažinimo ženklo, kad galėtumėte sinchronizuoti BPM su „Azure DevOps“.

1. „Azure DevOps“ projekto puslapio viršutiniame dešiniajame kampe pasirinkite profilio piktogramą, tada pasirinkite **Sauga**.

    ![Saugos komanda.](./media/setup_rsa_tool_05.png)

2. Kairiojoje srityje, dalyje **Sauga**, pasirinkite **Asmeninės prieigos atpažinimo ženklai**. Tada pasirinkite **Naujas atpažinimo ženklas**.

    ![Naujo atpažinimo ženklo mygtukas, esantis vartotojo parametrų skirtuke Asmeninės prieigos atpažinimo ženklai.](./media/setup_rsa_tool_06.png)

3. Užpildykite šiuos laukus ir pasirinkite **Kurti**:

    - **Pavadinimas / vardas ir (arba) pavardė**
    - **Galiojimo laikas (UTC)** – pasirinkite **Pasirinktinis**, o tada naudokite datos parinkiklį, kad pasirinktumėte paskutinę galimą datą.
    - **Aprėptis** – pasirinkite parinktį **Visa prieiga**.

    ![Naujo asmeninės prieigos atpažinimo ženklo kūrimo dialogo langas.](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Pasižymėkite sukurtą asmeninės prieigos atpažinimo ženklą. Jums jo reikės vėliau nustačius RSAT konfigūraciją.

    ![Asmeninės prieigos atpažinimo ženklas.](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>LCS projekto konfigūravimas

Turite turėti „Lifecycle Services“ (LCS) projektą pagrindinei testavimo bibliotekai. LCS verslo procesų modeliavimo įrankis (BPM) naudojamas kaip pagrindinė jūsų testavimo atvejų biblioteka. BPM naudojamas testavimo bibliotekoms valdyti ir paskirstyti po LCS projektus. Pavyzdžiui, „Microsoft“ partnerio arba nepriklausomo programinės įrangos tiekėjo (ISV) kūrimo testavimo bibliotekos pateiks testavimo atvejus BPM bibliotekų forma. Naudojant BPM testavimo atvejai tvarkomi pagal verslo procesą. BPM nenustato vykdymo tvarkos ar teigiamų testavimo rezultatų dažnumo. Šios informacijos valdomos kaip Azure DevOps nurodyta toliau šiame straipsnyje.  

Savo LCS projektui galite naudoti esamą klientų įdiegimo arba partnerių projektą.

### <a name="update-the-lcs-language"></a>LCS kalbos naujinimas

> [!NOTE]
> Norint tinkamai parodyti verslo procesus vartotojo sąsajoje (UI) turi būti nustatyta LCS pageidaujama kalba **anglų (Jungtinės Valstijos)**.

1. Eikite į LCS diegimo projektą.
2. Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką **Parametrai** (krumpliaračio simbolis), o paskui pasirinkite **Kalbos nuostata**.

    ![Kalbos nuostatų atnaujinimas.](./media/setup_rsa_tool_09.png)

3. Lauke **Pageidaujama kalba** pasirinkite **anglų (Jungtinės Valstijos)**, tada pasirinkite **Įrašyti**.

    ![Vartotojo parametrų skirtukas Kalbos nuostata.](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS konfigūravimas, kad būtų galima prisijungti prie „Azure DevOps“ projekto

Jeigu anksčiau sukūrėte naują „Azure DevOps“ projektą, konfigūruokite LCS projektą, kad prie jo galėtumėte prisijungti. Arba jei jūsų LCS projektas jau prijungtas prie jūsų „Azure DevOps“ projekto, galite pereiti prie kito skyriaus.

1. Eikite į LCS diegimo projektą.
2. Pasirinkite mygtuką **Meniu**, tada pasirinkite **Projekto parametrai**.

    ![Komanda Projekto parametrai.](./media/setup_rsa_tool_11.png)

3. Kairiojoje srityje pasirinkite **Visual Studio Team Services**, tada pasirinkite **Nustatyti „Visual Studio Team Services“**.

    ![Skirtukas „Visual Studio Team Services“ projekto parametruose.](./media/setup_rsa_tool_12.png)

4. Lauke **Azure DevOps svetainės URL** įveskite „Azure DevOps“ svetainės URL. Lauke **Asmeninės prieigos atpažinimo ženklas** įveskite anksčiau sukurtą asmeninį prieigos atpažinimo ženklą.

    > [!NOTE]
    > Nors VSTS dabar žinoma kaip „Azure DevOps“, norėdami sujungti LCS su savo „Azure DevOps“ projektu, naudokite seną URL. Pavyzdžiui, šioje mokymo programoje „Azure DevOps“ naudojamas URL yra `https://dev.azure.com/D365FOFastTrack/`. Tačiau šioje iliustracijoje jis įvestas kaip `https://D365FOFastTrack.visualstudio.com/`.

    ![1 „Visual Studio Team Services“ nustatymo veiksmas.](./media/setup_rsa_tool_13.png)

5. Pasirinkite **Tęsti**.
6. Lauke **„Visual Studio Team Services“ projektas** pasirinktoje svetainėje pasirinkite VSTS projektą, kurį norite susieti su LCS projektu. Pagal numatytuosius parametrus lauko **Proceso šablonas** reikšmė yra **Agile**. Norėdami naudoti pasirinktinį šabloną, peržiūrėkite geriausios praktikos gaires, esančias skyriuje [Naujo „Azure DevOps“ projekto kūrimas](#create-a-new-azure-devops-project). Tada pasirinkite **Tęsti**.

    ![2 „Visual Studio Team Services“ nustatymo veiksmas.](./media/setup_rsa_tool_14.png)

7. Peržiūrėti parametrus ir pasirinkite **Įrašyti**.

    ![3 „Visual Studio Team Services“ nustatymo veiksmas.](./media/setup_rsa_tool_15.png)

8. Pasirinkite **Įgalioti**, kad leistumėte LCS pasiekti sukonfigūruotą „Azure DevOps“ svetainę jūsų vardu ir įjungti funkcijas, kurios integruoja su VSTS.

    ![Mygtukas Įgalioti.](./media/setup_rsa_tool_16.png)

9. Parodomas pranešimas: „Būsite nukreipti į vietinę svetainę, kad būtų galima įgalioti LCS prisijungti prie „Visual Studio Team Services“ jūsų vardu. Tęsti?“ Pasirinkite **Taip**.

    ![Pranešimo laukas.](./media/setup_rsa_tool_17.png)

10. Pasirinkite **Patvirtinti**.

    ![Prieigos įgaliojimas.](./media/setup_rsa_tool_18.png)

11. Jei esate įgaliotas kaip vartotojas, UI jus grąžins į LCS projekto parametrų puslapį.

    ![Įgaliotasis vartotojas.](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Naujos BPM bibliotekos kūrimas

1. Eikite į LCS diegimo projektą.
2. Pasirinkite mygtuką **Meniu**, tada pasirinkite **Verslo procesų modeliavimo įrankis**.

    ![Komanda Verslo procesų modeliavimo įrankis.](./media/setup_rsa_tool_20.png)

3. Pasirinkite **Nauja biblioteka**.

    ![Mygtukas Nauja biblioteka.](./media/setup_rsa_tool_21.png)

4. Lauke **Bibliotekos pavadinimas** įveskite pavadinimą ir pasirinkite **Kurti**. Šioje mokomojoje programoje pavadinkite BPM biblioteką **RSAT**.

    ![Naujos bibliotekos kūrimo dialogo langas.](./media/setup_rsa_tool_22.png)

5. Atidarykite naują **RSAT** BPM biblioteką.
6. Pasirinkite procesą **Pavyzdinis pagrindinio verslo procesas**, tada dešinėje pusėje pasirinkite **Redagavimo režimas**.

    ![Mygtukas Redagavimo režimas.](./media/setup_rsa_tool_23.png)

7. Pakeiskite abiejų laukų **Pavadinimas** ir **Aprašas** reikšmes, kad **sukurtumėte produktą**. Tada pasirinkite **Įrašyti**.

    ![Laukai Pavadinimas ir Aprašas.](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Aplinka

### <a name="version-requirement"></a>Versijos reikalavimas

Būtina turėti testavimo ar smėlio dėžės aplinką, kurioje veikia 10 versija. Klientai, naudojantys 7.3 versiją, gali naudotis ir „Platform Update 20“ arba naujesnes versijas.

> [!NOTE]
> RSAT turi turėti prieigą prie jūsų testavimo aplinkos per interneto naršyklę.

### <a name="user-criteria"></a>Vartotojo kriterijai

Vartotojas turi turėti administratoriaus teises į šią aplinką.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Žinyno parametrų, kad būtų galima prisijungti prie LCS, nustatymas

Šis veiksmas reikalingas, kad būtų galima prisijungti prie LCS, kad užduoties įrašus būtų galima įrašyti į atitinkamą BPM biblioteką, esančią LCS, naudojant klientą.

1. Atidarykite kliento programą.
2. Eikite į **Sistemos administravimas \> Sąranka \> Sistemos parametrai**.
3. Skirtuko **Žinynas** lauke **„Lifecycle Services“ žinyno konfigūracija** pasirinkite atitinkamą LCS projektą (šioje mokomojoje programoje **RSAT**).

    ![„Lifecycle Services“ žinyno konfigūracijos laukas, esantis žinyno skirtuke.](./media/setup_rsa_tool_25.png)

    BPM bibliotekos yra užpildomos pagal atitinkamą LCS projektą.

4. Pasirinkite **Įrašyti**.
5. Gali reikėti atnaujinti naršyklę, kad pamatytumėte atnaujintą žinyno turinį.

    ![Perspėjimas dėl naršyklės atnaujinimo.](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Užduočių įrašai

> [!NOTE]
> Įsitikinkite, kad visi jūsų užduočių įrašai prasideda pagrindinėje ataskaitų srityje. Atskirus įrašus saugokite trumpai ir sutelkti dėmesį į vieną verslo užduotį, pvz., pardavimo užsakymo kūrimo.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Užduoties įrašo kūrimas ir įrašymas į BPM biblioteką

Kurkite atitinkamus užduoties įrašus, kuriuos galite pridėti prie paprasto verslo proceso, sukurto naujoje BPM bibliotekoje.

1. Atidarykite kliento programą.
2. Pagrindinėje ataskaitų srityje pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirinkite **Užduočių įrašymo priemonė**.

    ![Užduočių įrašymo priemonės iš parametrų meniu pasirinkimas.](./media/setup_rsa_tool_27.png)

3. Pasirinkite **Kurti įrašą**.

    ![Mygtukas Kurti įrašą.](./media/setup_rsa_tool_28.png)

4. Užpildykite laukus **Įrašo pavadinimas** ir **Įrašo aprašas** ir pasirinkite **Pradėti**.

    ![Laukai Įrašo pavadinimas ir Įrašo aprašas.](./media/setup_rsa_tool_29.png)

5. Įrašykite produkto kūrimo veiksmus. Baigę pasirinkite **Stabdyti**, kad sustabdytumėte įrašą.

    ![Produkto kūrimo veiksmai.](./media/setup_rsa_tool_30.png)

6. Pasirinkite **Įrašyti į „Lifecycle Services“**.

    ![Užduoties įrašo išsaugojimas į „Lifecycle Services”.](./media/setup_rsa_tool_31.png)

    Bibliotekos informacija įkeliama iš LCS.

    ![Bibliotekos informacijos įkėlimas.](./media/setup_rsa_tool_32.png)

7. Pasirinkti BPM biblioteką, kurią reikia susieti su užduoties įrašu. Šioje mokomojoje programoje pasirinkite **RSAT** BPM biblioteką, kuri buvo sukurta anksčiau, ir verslo procesą **Kurti produktą**. Tada pasirinkite **Gerai**.

    ![Užduoties įrašo susiejimas su BPM biblioteka ir verslo procesu.](./media/setup_rsa_tool_33.png)

    Rodomas pranešimas „Įrašyta į „Lifecycle Services“.

    ![Pranešimas apie sėkmingą įrašymą į LCS.](./media/setup_rsa_tool_34.png)

8. Jei užduoties įrašą norite įrašyti vietoje, o tada nusiųsti jį į BPM per LCS, atlikite šiuos veiksmus:

    1. Baigę įrašyti, pasirinkite **Įrašyti į šį kompiuterį**.

        ![Įrašyti šiame kompiuteryje.](./media/setup_rsa_tool_35.png)

    2. Naršyklės pranešimų juostoje pasirinkite **Įrašyti** arba **Įrašyti kaip**, kad būtų įrašytas failas vietiniame kompiuteryje.

        ![Pranešimų juosta.](./media/setup_rsa_tool_36.png)

    3. Eikite į **RSAT** BPM biblioteką ir pasirinkite verslo procesą, į kurį įrašysite užduoties įrašą.
    4. Skirtuke **Peržiūra** pasirinkite **Nusiųsti**.

        ![Nusiuntimo mygtukas.](./media/setup_rsa_tool_37.png)

    5. Pasirinkite **Naršyti** ir pasirinkite. axtr failą, kurį įrašėte anksčiau. Tada pasirinkite **Nusiųsti**.

        ![.axtr failo pasirinkimas nusiųsti.](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Tikrinti sinchronizavimą iš BPM su „Azure DevOps“

Dabar, kai užduoties įrašas yra pridėtas prie verslo proceso, turite patikrinti, ar verslo procesą ir susietą užduoties įrašą galima sinchronizuoti su „Azure DevOps“ kaip funkciją ir testavimo atvejį (atitinkamai), naudojant VSTS sinchronizavimo funkciją LCS.

> [!NOTE]
> Atitinkamas „Azure DevOps“ sukurtas darbo elemento tipas gali skirtis; jis priklauso nuo proceso šablono, kurį pasirinkote konfigūruodami LCS projektą su „Azure DevOps“, kaip aprašyta skyriuje [Naujo „Azure DevOps“ projekto kūrimas](#create-a-new-azure-devops-project).

1. Eikite į BPM biblioteką ir atidarykite anksčiau sukurtą **RSAT** biblioteką.
2. Pasirinkite daugtaškio mygtuką (**...**) ir pasirinkite **VSTS sinchronizavimas**.

    ![VSTS sinchronizavimo komanda daugtaškio meniu.](./media/setup_rsa_tool_39.png)

    Kai bus baigtas VSTS sinchronizavimas, kairėje pusėje rodomas skirtukas **Reikalavimai**, kuriame yra ir atitinkamas „Azure DevOps“ darbo elementas.

    > [!NOTE]
    > Darbo elementas, sukurtas „Azure DevOps“, turės BPM bibliotekos pavadinimą kaip pavadinimo prefiksą.

    ![Skirtukas Reikalavimai.](./media/setup_rsa_tool_40.png)

3. Atnaujinkite puslapį.
4. Pasirinkite daugtaškio mygtuką (**...**). Matysite papildomą parinktį **Sinchronizuoti testavimo atvejus**. Pasirinkite šią parinktį.

    ![Testavimo atvejų sinchronizavimo komanda daugtaškio meniu.](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Jei atnaujinus puslapį parinkties **Sinchronizuoti testavimo atvejus** nėra, eikite į pagrindinį BPM puslapį ir pasirinkite visos bibliotekos parinktį **Sinchronizuoti testavimo atvejus**. Tokiu būdu galite efektyviai vykdyti visos bibliotekos sinchronizavimą.
    >
    > ![Visos bibliotekos testavimo atvejų sinchronizavimo pasirinkimas.](./media/setup_rsa_tool_42.png)

    Baigus sinchronizuoti testavimo atvejus, skirtuke **Reikalavimai** sukuriamas naujas testavimo atvejis.

    ![Naujas testavimo atvejis skirtuke Reikalavimai.](./media/setup_rsa_tool_43.png)

5. Eikite į savo „Azure DevOps“ projektą ir pasirinkite **Sritys \> Darbo elementai**.

    ![Darbo elementų komanda srityse.](./media/setup_rsa_tool_44.png)

6. Patikrinkite, ar yra darbo elementas ir testavimo atvejis, kuriuos sukūrėte per BPM sinchronizavimą.

    ![Darbo elementas ir testavimo atvejis.](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT konfigūravimas ir diegimas

RSAT galima įdiegti bet kuriame kompiuteryje, kuriame veikia „Windows 10“ ir kuris gali prisijungti prie aplinkos per interneto naršyklę („Internet Explorer“ arba „Google Chrome“).

> [!NOTE]
> Prieš diegiant naują įrankio versiją, rekomenduojame pašalinti ankstesnę jo versiją.

### <a name="install-an-authentication-certificate"></a>Autentifikavimo sertifikato diegimas

Norėdami įjungti autentifikavimą, turite sugeneruoti ir įdiegti sertifikatą tame pačiame kompiuteryje, kuriame veikia RSAT.

#### <a name="generate-a-certificate"></a>Sertifikato generavimas

1. Norėdami sugeneruoti sertifikato failą, atidarykite „Microsoft Windows PowerShell“ langą kaip administratorius ir vykdykite šią komandą.

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Atidarykite sertifikatų tvarkyklę dialogo lange **Vykdyti** įvesdami **certlm.msc** ir patvirtinkite, kad **D365 automatizuoto testavimo sertifikatas** sukurtas pagal **Asmeninis \> Sertifikatai**.

    > [!NOTE]
    > Būtinai įveskite **certlm.msc**, o ne **certmgr.msc**, nes sertifikatai saugomi vietiniame kompiuteryje.

    ![D365 automatizuotas testavimo sertifikato sertifikatas.](./media/setup_rsa_tool_46.png)

3. Spustelėkite dešiniuoju pelės mygtuku sertifikatą ir pasirinkite **Kopijuoti**.
4. Eikite į **Patikimos šakninės sertifikavimo tarnybos \> Sertifikatai**.

    ![Sertifikatų aplankas, esantis aplanke Patikimos šakninės sertifikavimo tarnybos.](./media/setup_rsa_tool_47.png)

5. Meniu **Veiksmas** pasirinkite **Įklijuoti**, kad nukopijuotumėte sertifikatą į vietą **Patikimos šakninės sertifikavimo tarnybos**.

    ![Meniu Veiksmas komanda Įklijuoti.](./media/setup_rsa_tool_48.png)

6. Norėdami gauti įdiegto sertifikato kontrolinį kodą tarpų ir specialiųjų simbolių, atidarykite „Windows PowerShell“ langą kaip administratorius ir vykdykite šias komandas.

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Įrašykite kontrolinį kodą, nes jums reikės jo vėliau, kai atnaujinsite programos objektų serverio (AOS) .wif failus ir nustatysite RSAT konfigūraciją.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>AOS kompiuterio konfigūravimas, kad būtų patikimas ryšys

> [!NOTE]
> Jei aplinka yra 2 arba aukštesnės pakopos aplinka, sertifikato nykščio atspaudas turi būti atnaujintas wif.config faile **visuose** aplinkos AOS kompiuteriuose.

1. Užmegzkite nuotolinio darbalaukio protokolo (RDP) ryšį su AOS kompiuteriu. Išsami prisijungimo informacija yra nurodyta LCS aplinkos informacijos puslapyje.
2. Atidarykite „Microsoft“ informacines interneto paslaugas (IIS) ir svetainių sąraše raskite **AOSService**.

    ![„AOSService” svetainių sąraše.](./media/setup_rsa_tool_49.png)

3. Dešiniuoju pelės mygtuku spustelėkite **Naršyti**, kad atidarytumėte aplanką **\<Drive\>: \\AosService\\WebRoot**. Raskite **wif.config** failą.

    ![Wif.config failas „WebRoot“ aplanke.](./media/setup_rsa_tool_50.png)

4. Atnaujinkite **wif.config** failą įtraukdami naują savo sertifikato tarnybos įrašą nurodydami sertifikato ir tarnybos pavadinimus, kaip parodyta šiame pavyzdyje.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Jei keli vartotojai naudoja tą pačią programą, kiekvienas vartotojas turi sugeneruoti atskirus nykščio atspaudus, o kiekvienas iš šių nykščio atspaudų turi būti įtrauktas į skiltį **\<keys\>**.

5. Jei yra daugiau nei vienas AOS kompiuteris, pakartokite 3–4 veiksmus su kiekvienu papildomu kompiuteriu.

    > [!NOTE]
    > Skirtingai nei senesnėse 2 pakopos aplinkose, naujos 2 pakopos aplinkos yra įdiegtos naudojant du AOS egzempliorius.

6. Vykdykite **iisreset** visuose AOS kompiuteriuose.

    > [!NOTE]
    > Jei neturite administratoriaus teisių vykdyti **iisreset** 1 pakopos kompiuteryje, LCS aplinkos informacijos puslapyje pasirinkite Prižiūrėti > Iš naujo paleisti tarnybas.

#### <a name="tier-2-environment"></a>2 ir aukštesnės pakopos aplinka

Jei naudojama 2 ar aukštesnės pakopos („Standard“ lygio priėmimo testavimo smėlio dėžė arba naujesnė) aplinka, patikrinkite arba nustatykite nurodytą registro parametrą kompiuteryje, kuriame įdiegta RSAT. Šis veiksmas būtinas, nes padeda išvengti autentifikavimo arba RSAT ryšio klaidų.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT įdiegimas

1. Eikite į <https://www.microsoft.com/download/details.aspx?id=57357> ir pasirinkite **Atsisiųsti**.
2. Pasirinkite visus failus, tada pasirinkite **Toliau**.

    ![Visų failų pasirinkimas.](./media/setup_rsa_tool_51.png)

3. Norėdami paleisti diegimo programą, du kartus spustelėkite. msi paketą. Tada, kai diegimas bus baigtas, pasirinkite **Baigti**.

    ![RSAT diegimo programos failas.](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>„Selenium“ ir naršyklių tvarkyklių įdiegimas

Jei naudojate senesnes RSAT versijas, turite įdiegti „Selenium“ ir naršyklių tvarkykles. Jums nebereikia diegti šių tvarkyklių, nes jos įdiegtos automatiškai.

1. Pirmą kartą atidarę RSAT, būsite paraginti automatiškai atsisiųsti ir įdiegti „Selenium“. Daugiau informacijos rasite skyriuje [RSAT konfigūravimas](#configure-rsat).
2. Kad galėtumėte vykdyti testavimo atvejį, būsite paraginti automatiškai atsisiųsti ir įdiegti naršyklės tvarkyklę, atitinkančią numatytąją naršyklę, kuri pasirenkama atliekant RSAT konfigūraciją. Daugiau informacijos rasite skyriuje [Testavimo atvejo įkėlimas ir vykdymas](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Darbo su RSAT“ pradžia

### <a name="create-a-test-plan-and-test-suites"></a>Testavimo plano ir testavimo paketų kūrimas

1. Eikite į „Azure DevOps“ projektą ir pasirinkti **Testavimo planai**.

    ![Komanda Testavimo planai.](./media/setup_rsa_tool_53.png)

2. Pasirinkite **Naujas testavimo planas**.

    ![Mygtukas Naujas testavimo planas.](./media/setup_rsa_tool_54.png)

3. Užpildykite lauką **Pavadinimas** ir pasirinkite **Kurti**. Šioje mokomojoje programoje pavadinkite testavimo planą **RSAT testavimo planas**.

    ![Naujo testavimo plano dialogo langas.](./media/setup_rsa_tool_55.png)

4. Pasirinkite pliuso ženklą (**+**), tada pasirinkite **Statinis paketas**, kad sukurtumėte statinį paketą pagal naują testavimo planą. Pavadinkite naują testavimo paketą **T01 – Make to Stock**.

    > [!NOTE]
    > Taip pat galite sukurti užklausa pagrįstą paketą, jei norite, kad naujieji testavimo atvejai būtų automatiškai įtraukiami iš BPM į RSAT testavimo paketą.

    ![Statinio paketo sukūrimas.](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Testavimo atvejų pridėjimas prie testavimo paketų

1. Pasirinkite **Įtraukti esamus** dešinėje pusėje, kad būtų įtraukti esami testavimo atvejai į testavimo paketą.

    ![Esamų įtraukimo mygtukas.](./media/setup_rsa_tool_57.png)

2. Puslapyje **Įtraukti testavimo atvejus į paketą** pasirinkite **Vykdyti užklausą** ir pasirinkite testavimo atvejį, kurį norite įtraukti į testavimo paketą. Šioje mokomojoje programoje pasirinkite **Kurti naują produktą** testavimo atvejį. Tada pasirinkite **Įtraukti testavimo atvejus** apatiniame dešiniajame puslapio kampe (šis mygtukas šioje iliustracijoje neparodytas).

    ![Mygtukas Vykdyti užklausą.](./media/setup_rsa_tool_58.png)

    Testavimo atvejis įtraukiamas į testavimo paketą **T01-Make to Stock**.

    ![Testavimo atvejis įtrauktas į testavimo paketą.](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Konfigūruoti RSAT

1. Atidarykite RSAT.

    ![RSAT piktograma.](./media/setup_rsa_tool_60.png)

2. Gaunate įspėjamąjį pranešimą, kuriame teigiama, kad „Regression Suite Automation Tool“ reikia „Selenium“; ar norite ją automatiškai atsisiųsti ir įdiegti dabar?“ Pasirinkite **Taip**.

    ![Įspėjimo pranešimas, kad „Regression Suite Automation Tool” reikia seleno.](./media/setup_rsa_tool_61.png)

3. Viršutiniame dešiniajame kampe pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirodžiusiame dialogo lange užpildykite šiuos laukus:

    - **Azure DevOps URL** – įveskite savo „Azure DevOps“ projekto URL, pvz., `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Prieigos atpažinimo ženklas** – įveskite prieigos atpažinimo ženklą, kuris leidžia įrankiui prisijungti prie „Azure DevOps“. Naudokite anksčiau sukurtu asmeninės prieigos atpažinimo ženklu. Norėdami gauti daugiau informacijos, žr. [Prieigos autentifikavimas naudojant asmeninės prieigos atpažinimo ženklus](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Projekto pavadinimas** – pasirinkite savo „Azure DevOps“ projekto pavadinimą.
    - **Testavimo planas** – pasirinkite „Azure DevOps“ testavimo planą, kuriame yra jūsų testavimo atvejų. Norėdami gauti daugiau informacijos, žr. [Testavimo planų ir testavimo paketų kūrimas](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Pasirinkę testavimo planą, pasirinkite **Tikrinti ryšį**, kad būtų galima tikrinti ryšį su „Azure DevOps“.
    - **Pagrindinio kompiuterio pavadinimas** – įveskite testavimo aplinkos pagrindinio kompiuterio pavadinimą, pvz., **\<myaos\>.cloudax.dynamics.com**. Neįtraukite **https://** arba **http://** prefikso.
    - **SOAP pagrindinio kompiuterio pavadinimas** – įveskite testavimo aplinkos SOAP pagrindinio kompiuterio pavadinimą. Paprastai SOAP pagrindinio kompiuterio pavadinimas yra toks pat kaip pagrindinio kompiuterio pavadinimas, bet jame yra **soap** sufiksas. Štai pavyzdys: **\<myaos\>soap.cloudax.dynamics.com**. Neįtraukite **https://** arba **http://** prefikso.

        > [!NOTE]
        > Norėdami rasti pagrindinio kompiuterio pavadinimą ir SOAP pagrindinio kompiuterio pavadinimą, atidarykite IIS tvarkyklę, dešiniuoju pelės mygtuku spustelėkite **Svetainės \> AOSService**, tada pasirinkite **Redaguoti susiejimus**. Stulpelyje **Pagrindinio kompiuterio pavadinimas** pateikiami pagrindinio kompiuterio pavadinimas ir SOAP pagrindinio kompiuterio pavadinimas (SOAP pagrindinio kompiuterio pavadinime yra sufiksas **soap** URL).

        ![Pagrindinio kompiuterio pavadinimas ir SOAP pagrindinio kompiuterio pavadinimas stulpelyje Pagrindinio kompiuterio pavadinimas.](./media/setup_rsa_tool_63.png)

    - **Administratoriaus vartotojo vardas** – įveskite testavimo aplinkos administratoriaus vartotojo el. pašto adresą.
    - **Kontrolinis kodas** – įveskite autentifikavimo sertifikato kontrolinį kodą, kaip pirmiau aprašyta šioje mokomojoje programoje.
    - **Darbo katalogas** – nurodykite aplanko, kuriame saugomi testavimo automatizavimo failai, pvz., „Excel“ testavimo duomenų failai, vietą. Pavyzdžiui, įveskite arba pasirinkite **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Jeigu aplanko pavadinime yra tarpų, vykdyti nepavyks, nes aplanko nepavyks rasti. Ši problema yra jau žinoma; ji nebeturi kilti naujausioje įrankio versijoje.

    - **Numatytoji naršyklė** – pasirinkite **Internet Explorer** arba **Google Chrome**. Įsitikinkite, kad įdiegtos tinkamos naršyklių tvarkyklės.
    - **Testavimo vykdymo skirtasis laikas** – nurodykite testavimo vykdymo laiką minutėmis. Pasibaigus skirtajam laikui, visi aktyvūs langai yra uždaromi, todėl laukiantys testavimo atvejai lieka neįvykdyti.
    - **Testavimo veiksmo skirtasis laikas** – šis laukas kontroliuoja „Finance and Operation“ aplinkos serverio užklausų skirtojo laiko periodą minutėmis. Paprastai turi užtekti numatytosios vertės (2 min.). Tačiau lėtesnių aplinkų atvejais galite pageidauti padidinti vertę, jei įvyksta su skirtuoju laiku susijusių klaidų.
    - **Įmonės pavadinimas** – įveskite įmonės pavadinimą, kuris bus naudojamas kaip numatytoji įmonė kuriant „Excel“ parametrų failus. Vėliau įmonę galite pakeisti redaguodami „Excel“ parametrų failą.

    ![Dialogo langas Parametrai.](./media/setup_rsa_tool_62.png)

4. Pasirinkite **Taikyti**, kad būtų pritaikyti ir įrašyti parametrai.

    Norėdami įrašyti savo dabartinius parametrus į kompiuteryje esantį konfigūracijos failą, pasirinkite **Įrašyti kaip**. Norėdami atkurti savo parametrus iš kompiuteryje esančio konfigūracijos failo, pasirinkite **Atidaryti**.

5. Pasirinkite **Uždaryti** norėdami uždaryti dialogo langą.

### <a name="load-and-run-test-cases"></a>Testavimo atvejų įkėlimas ir vykdymas

1. Pasirinkite **Įkelti**, kad būtų įkeltas **RSAT testavimo planas** iš „Azure DevOps“ projekto.

    ![Įkėlimo mygtukas.](./media/setup_rsa_tool_64.png)

2. Pasirinkite **Kurti naują produktą** testavimo atvejį iš testavimo paketo, tada pasirinkite **Naujas \> Generuoti testavimo vykdymo ir parametrų failus**.

    ![Komanda Generuoti testavimo vykdymo ir parametrų failus meniu Naujas.](./media/setup_rsa_tool_65.png)

    „Excel“ parametrų failas sukuriamas vietiniame aplanke, kurį nurodėte RSAT konfigūracijoje (pvz., **C:\\Temp\\RegressionTool**).

    ![„Excel“ parametrų failas sukurtas.](./media/setup_rsa_tool_66.png)

3. Jei norite įrašyti parametrų failus, pasirinkite **Nusiųsti**. Visų pasirinktų testavimo atvejų testavimo automatizavimo failai yra nusiunčiami į „Azure DevOps“ naudoti ateityje. (Tarp šitų failų yra „Excel“ testavimo parametrų failai.)

    Tokiu būdu galite pasirinkti **Įkelti** norėdami įkelti parametrų failus (ir automatizavimo failus) iš testavimo atvejo tiesiai iš „Azure DevOps“. Nereikia iš naujo sugeneruoti parametrų failų. Šis metodas bus svarbus vėliau, kai norėsite, kad parametrų failo pakeitimai būtų išlaikyti ir jie nebūtų perrašyti.

4. Norėdami patikrinti, ar automatizavimo failai ir parametrų failai yra įrašomi „Azure DevOps“, eikite į „Azure DevOps“ projektą, pasirinkite **Sritys \> Darbo elementai**, tada pasirinkite **Kurti naują produktą** testavimo atvejį. Skirtuke **Priedai** turite matyti keturis failus:

    - **.cs** – C\# automatizavimo failas
    - **.dll** – kompiliuotas automatizavimo failas kaip rinkinys
    - **.xlsx** – „Excel“ parametrų failas
    - **.xml** – įrašymo failas

    ![Failai skirtuke Priedai.](./media/setup_rsa_tool_67.png)

5. Pasirinkite norimą vykdyti testavimo atvejį ir pasirinkite **Vykdyti**.

    > [!NOTE]
    > Prieš vykdydami testavimo atvejus, jei naudojate „Internet Explorer“ kaip naršyklę, įsitikinkite, kad jūsų darbalaukio skiriamoji geba nustatyta kaip **100%** **„Windows“ ekrano parametrai \> Mastelis ir išdėstymas**. Jei negalite pakeisti šio parametro virtualiajame kompiuteryje (VM), jį pakeiskite kliente (nešiojamajame kompiuteryje), iš kurio bandote pasiekti VM. Tada skiriamosios gebos parametrus perims VM ekrano parametrai.

    ![Darbalaukio skiriamoji geba nustatyta kaip 100 %.](./media/setup_rsa_tool_68.png)

6. Jei sistemoje neįdiegta naršyklių tvarkyklių, gausite įspėjamąjį pranešimą, kuriame teigiama, kad „Šiai operacijai atlikti reikia \<browser name\> tvarkyklės. Ar norite automatiškai atsisiųsti ir įdiegti ją dabar?“ Pasirinkite **Taip**.

    ![Įspėjimo pranešimas, skirtas „Internet Explorer“.](./media/setup_rsa_tool_69.png)

    ![Įspėjimo pranešimas, skirtas „Chrome“.](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Jei naudojate „Chrome“ kaip naršyklę ir gaunate klaidos pranešimą, kuriame nurodoma, kad seansas nebuvo sukurtas, nes „Chrome“ versija netinkama, atsisiųskite naujausią „Chrome“ tvarkyklę iš <http://chromedriver.chromium.org/downloads> į **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** aplanką.

    ![Klaidos pranešimas, skirtas „Chrome“.](./media/setup_rsa_tool_71.png)

    Testavimo atvejis vykdomas ir laukas **Rezultatai** atnaujinamas.

    ![Atnaujintas rezultatų laukas.](./media/setup_rsa_tool_72.png)

    Jei vadovavotės šia mokomąja medžiaga, kaip parašyta, **Sukurti naują produktą** testavimo atvejo rezultatas bus neigiamas, nes produkto kūrimo užduoties įrašas įrašė produkto pavadinimą kaip užprogramuota vertė. Jei iš naujo įvykdysite tą patį testavimo atvejį, turėtumėte gauti klaidos pranešimą, nes produktas jau yra.

    ![Rezultatų lauko reikšmė Nepavyko.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Testavimo rezultatų peržiūra

1. Dukart spustelėkite nepavykusį testavimo atvejį.

    Gaunate klaidos pranešimą.

    ![Klaidos pranešimas.](./media/setup_rsa_tool_73.png)

2. Pasirinkite **Informacija**, kad būtų galima peržiūrėti visą klaidos pranešimą.

    ![Visas klaidos pranešimas.](./media/setup_rsa_tool_74.png)

3. Norėdami peržiūrėti išsamią klaidos pranešimo versiją „Azure DevOps“, pasirinkite **Atidaryti „Azure DevOps“**. „Azure DevOps“ galite peržiūrėti testavimo atvejo būseną ir išsamų klaidos pranešimą.

    ![Išsamus klaidos pranešimas, rodomas „Azure DevOps“.](./media/setup_rsa_tool_75.png)

4. Norėdami tiesiogiai „Azure DevOps“ projekte peržiūrėti testavimo rezultatus, eikite į **Testavimo planai \> Testavimo planai \> Vykdymai**. Du kartus spustelėkite testavimo vykdymą, kurio daugiau informacijos norite matyti.

    ![Testavimo vykdymų „Azure DevOps“ sąrašas.](./media/setup_rsa_tool_76.png)

5. Skirtuke **Vykdymo suvestinė** rodoma, kad testavimo atvejis nesėkmingas, bet faktinis klaidos pranešimas nepateikiamas. Norėdami peržiūrėti išsamų klaidos pranešimą, pasirinkite skirtuką **Testavimo rezultatai**.

    ![Skirtukas Vykdymo suvestinė.](./media/setup_rsa_tool_77.png)

    Skirtuke **Testavimo rezultatai** pateikiama testavimo atvejo informacija, taip pat rezultatas ir klaidos pranešimas.

    ![Skirtukas Testavimo rezultatai.](./media/setup_rsa_tool_78.png)

6. Du kartus spustelėkite reikiamą įrašą, kad peržiūrėtumėte išsamų klaidos pranešimą.

    ![Išsamus klaidos pranešimas.](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Visus klaidos pranešimus taip pat galima rasti vietoje **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Taip pat galite eksportuoti testavimo vykdymo rezultatus iš testavimo plano pasirinkdami **Eksportuoti**.

    ![Testavimo plano eksportavimas.](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>„Excel“ parametrų failo modifikavimas

1. Atidarykite RSAT.
2. Pasirinkite testavimo atvejį ir pasirinkite **Redaguoti**, norėdami atidaryti „Excel“ parametrų failą.

    Lape **EcoResProductCreate** atkreipkite dėmesį, kad lauko **Produkto numeris** vertė yra užprogramuota. Prieš dar kartą vykdydami testavimo atvejį, turite atnaujinti šį lauką nauju produkto numeriu.

3. Norėdami, kad būtų sugeneruotas unikalus kiekvieno vykdymo produkto numeris ir nereikėtų iš naujo atidaryti „Excel“ parametrų failo ir kiekvieną kartą patiems atnaujinti produkto numerio, naudokite šią „Excel“ formulę.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Be skirtuko **Bendra**, „Excel“ parametrų faile yra kiekvieno formos puslapio testavimo atvejų apsilankymų duomenų skirtukas.

    ![Laukas Produkto numeris.](./media/setup_rsa_tool_81.png)

4. Pasirinkite **Įrašyti** ir uždarykite „Excel“ darbaknygę.
5. Pasirinkite **Nusiųsti**, kad įrašytumėte „Excel“ parametrų failą į „Azure DevOps“.

    ![Sėkmingo nusiuntimo pranešimas.](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Norėdami vykdyti testavimo atvejus konkretaus vartotojo kontekste „Excel“ parametrų failo skirtuko **Bendra** lauke **Tikrinti vartotoją** įveskite vartotojo el. pašto ID. Naujausioje RSAT versijoje laukų išdėstymas, esantis „Excel“ parametrų faile, atnaujintas, bet koncepcija išlieka ta pati.
    >
    > ![Laukas Tikrinti vartotoją.](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Rezultatų tikrinimas

- Pasirinkite **Vykdyti**, kad iš naujo įvykdytumėte testavimo atvejį, ir patikrinkite, ar jo rezultatas teigiamas. Testavimo rezultatus galite peržiūrėti, kaip aprašyta skyriuje [Testavimo rezultatų peržiūra](#view-the-test-results).

    ![Rezultatų lauko reikšmė Pavyko.](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Testavimo atvejų sujungimas

Viena iš pagrindinių RSAT funkcijų – testavimo atvejų sujungimas (t. y. testavimo galimybė pereiti prie kitų testų). Testavimo atvejai vykdomi pagal „Azure DevOps“ testavimo plane nustatytą tvarką. (Šią tvarką taip pat galima atnaujinti patiems testavimo įrankyje.) Todėl, jei norite perkelti kintamuosius iš vieno testavimo atvejo į kitą, labai svarbu, kad testai eitų tinkama tvarka.

Šiame skyriuje sukursite įrašytą kintamąjį pirmame testavimo atvejyje, sukursite antrą testavimo atvejį ir perduosite įrašytą kintamąjį iš pirmo testavimo atvejo į antrą testavimo atvejį. Tada vykdysite testavimo atvejus kaip grandininį testavimo atvejį RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Esamo užduoties įrašo modifikavimas įrašytam kintamajam sukurti

1. Atidarykite kliento programą.
2. Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis), tada pasirinkite **Užduočių įrašymo priemonė**.
3. Pasirinkite **Redaguoti įrašą**.

    ![Mygtukas Redaguoti įrašą.](./media/setup_rsa_tool_85.png)

4. Pasirinkite **Atidaryti iš „Lifecycle Services“**.

    ![Mygtukas Atidaryti iš „Lifecycle Services“.](./media/setup_rsa_tool_86.png)

5. Pasirinkite **Pasirinkti „Lifecycle Services“ biblioteką**.

    ![Mygtukas Pasirinkti „Lifecycle Services“ biblioteką.](./media/setup_rsa_tool_87.png)

    BPM bibliotekos įkeliamos iš LCS.

    ![BPM bibliotekų įkėlimas.](./media/setup_rsa_tool_88.png)

6. Kai BPM bibliotekos įkeliamos iš LCS, pasirinkite **RSAT** BPM biblioteką ir **Kurti naują produktą** verslo procesą, su kuriuo susietas užduoties įrašas. Tada pasirinkite **Gerai**.

    ![BPM bibliotekos ir verslo proceso pasirinkimas.](./media/setup_rsa_tool_89.png)

7. Tinkamo užduoties įrašo pavadinimas įvedamas į lauką **Įrašo pavadinimas**. Pasirinkite **Paleisti**.

    ![Lauke Įrašo pavadinimas esantis užduoties įrašo pavadinimas.](./media/setup_rsa_tool_90.png)

8. Eikite į **Produkto informacijos valdymas \> Produktai** ir pasirinkite **Naujas**, kad būtų atidarytas puslapis, kuriame buvo įrašytas pradinis užduoties įrašas **Kurti produktą**.
9. Pasirinkite **Įterpti veiksmą**.

    > [!NOTE]
    > Naujas veiksmas įterpiamas **po** veiksmo, kurį pasirinkote srityje.

    ![Mygtukas Įterpti veiksmą.](./media/setup_rsa_tool_91.png)

10. Dešiniuoju pelės mygtuku spustelėkite lauką **Produkto numeris** ir pasirinkite **Užduočių įrašymo priemonė \> Kopijuoti**.

    ![Kopijavimo komanda.](./media/setup_rsa_tool_92.png)

11. Naujas veiksmas įtraukiamas į sritį. Pasižymėkite lauko **Produkto numeris** vertę, nes jos reikės vėliau.

    ![Naujas veiksmas įtrauktas.](./media/setup_rsa_tool_93.png)

12. Pasirinkite **Baigta redaguoti**.
13. Pasirinkite **Įrašyti į „Lifecycle Services“** ir susiekite naują užduoties įrašą su ta pačia BPM biblioteka ir verslo procesu, su kuriais susietas pradinis užduoties įrašas. Norėdami gauti daugiau informacijos, žr. skyrių [Užduoties įrašo kūrimas ir įrašymas į BPM biblioteką](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Eikite į BPM biblioteką ir pasirinkite **Sinchronizuoti testavimo atvejus**, kad būtų perrašytas užduoties įrašas, kuris yra pridėtas prie testavimo atvejo „Azure DevOps“, kaip aprašyta skyriuje [Tikrinti sinchronizavimą iš BPM su „Azure DevOps“](#test-the-synchronization-from-bpm-to-azure-devops).
15. Atidarykite RSAT ir pasirinkite **Įkelti**, kad iš naujo būtų įkelti visi testavimo paketo atvejai. Turite iš naujo sugeneruoti atitinkamo testavimo atvejo automatizavimo ir parametrų failus, pasirinkdami testavimo atvejį, o tada pasirinkdami **Naujas \> Generuoti testavimo vykdymo ir parametrų failus**, kaip aprašyta skyriuje [Testavimo atvejų įkėlimas ir vykdymas](#load-and-run-test-cases).

    > [!NOTE]
    > Jei „Excel“ parametrų failas buvo paliktas atidarytas, iš naujo sugeneruoti nepavyks. Todėl prieš generuodami naują „Excel“ parametrų failą įsitikinkite, kad „Excel“ parametrų failas yra uždarytas.

16. Pasirinkite **Redaguoti**, kad būtų atidarytas naujas „Excel“ parametrų failas. 9 eilutėje matysite naują įrašą **Įrašytas kintamasis**. Šis kintamasis **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** įrašomas užduoties įrašo XML faile ir gali būti naudojamas vėlesniuose testavimuose.

    ![Įrašyto kintamojo įrašas.](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Naujo testavimo atvejo kūrimas

1. Eikite į **RSAT** BPM biblioteką.
2. Pasirinkite procesą **Pavyzdinis pagalbos verslo procesas**, tada dešinėje pusėje pasirinkite **Redagavimo režimas**.
3. Pakeiskite abiejų laukų **Pavadinimas** ir **Aprašas** reikšmes, kad būtų **išleistas produktas**. Tada pasirinkite **Įrašyti**.

    ![Pavadinimas ir aprašas pakeisti, kad būtų išleistas produktas.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Naujo užduoties įrašo, kuriame būtų funkcija Tikrinti, kūrimas

- Sukurkite užduoties įrašą, kad būtų išleistas anksčiau USRT juridiniam subjektui sukurtas produktas. Norėdami gauti daugiau informacijos, žr. skyrių [Užduoties įrašo kūrimas ir įrašymas į BPM biblioteką](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Jei tai yra grandininiai testavimo atvejai, visada rekomenduojame rasti arba filtruoti įrašą, kurio jums reikia, *patiems įvedant lauko vertę*. Tokiu būdu įrankis gali nustatyti įrašą, kuriam turi būti atliktas veiksmas kitame testavimo atvejyje.

    ![Naujas užduoties įrašas, kuriame yra funkcija Tikrinti.](./media/setup_rsa_tool_96.png)

    Kaip rodo ankstesnė iliustracija, kai produktas randamas naudojant spartųjį filtrą, bet prieš jums pasirenkant **Išleisti produktus**, patikrinkite lauko **Produkto numeris** vertę, kad įsitikintumėte, jog produkto ID yra produkto ID, kuris buvo sukurtas anksčiau. Norėdami patikrinti vertę, dešiniuoju pelės mygtuku spustelėkite lauką **Produkto numeris**, tada pasirinkite **Užduočių įrašymo priemonė \> Tikrinti \> Dabartinė vertė**.

    ![Dabartinės vertės tikrinimas.](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Užduoties įrašo įrašymas BPM

1. Baigę užduoties įrašą, pasirinkite **Įrašyti į „Lifecycle Services“**.

    ![Baigtos užduoties įrašo išsaugojimas į „Lifecycle Services”.](./media/setup_rsa_tool_98.png)

2. Bibliotekos informacija įkeliama iš LCS.

    ![Bibliotekos informacijos įkėlimas iš LCS.](./media/setup_rsa_tool_99.png)

3. Pasirinkti BPM biblioteką, kurią reikia susieti su užduoties įrašu. Šioje mokomojoje programoje pasirinkite **RSAT** BPM biblioteką, kuri buvo sukurta anksčiau, ir verslo procesą **Išleisti produktą**. Tada pasirinkite **Gerai**.

#### <a name="sync-bpm-to-azure-devops"></a>BPM sinchronizavimas su „Azure DevOps“

1. Eikite į BPM biblioteką ir atidarykite **RSAT** biblioteką.
2. Pasirinkite **VSTS sinchronizavimas**, tada pasirinkite **Sinchronizuoti testavimo atvejus**. Norėdami gauti daugiau informacijos, žr. skyrių [Tikrinti sinchronizavimą iš BPM su „Azure DevOps“](#test-the-synchronization-from-bpm-to-azure-devops).

    Baigus sinchronizuoti, naujas verslo proceso **Išleisti produktą** darbo elementas ir atitinkamas testavimo atvejis rodomi „Azure DevOps“ **Sritys \> Darbo elementai**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Naujo testavimo atvejo įtraukimas į esamą testavimo paketą

1. Eikite į **Testavimo planai \> Testavimo planai** ir pasirinkite planą **RSAT testavimo planas**.
2. Pasirinkite **Įtraukti esamą**.
3. Puslapyje **Įtraukti testavimo atvejus į paketą** pasirinkite **Vykdyti užklausą**.
4. Pasirinkite naują testavimo atvejį, kuris buvo sukurtas **Išleisti produktą**, o tada apatiniame dešiniajame puslapio kampe pasirinkite **Įtraukti testavimo atvejus** (šis mygtukas šioje iliustracijoje neparodytas).

    ![Testavimo atvejų įtraukimo į paketą puslapis.](./media/setup_rsa_tool_100.png)

    Dabar testavimo pakete yra du testavimo atvejai.

    ![Du testavimo atvejai testavimo pakete.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Testavimo atvejų įkėlimas į RSAT

1. Atidarykite RSAT ir pasirinkite **Įkelti**.
2. Testavimo atvejai įkeliami, o jūs gausite įspėjimą, kad „Šis veiksmas perrašys „Excel“ testavimo duomenų failus ir vietiniai pakeitimai bus prarasti. Ar norite tęsti?“ Pasirinkite **Taip**, jei norite atnaujinti „Excel“ parametrų failus vietinėje sistemoje, o ne „Excel“ parametrų failus, nusiųstus į „Azure DevOps“.

    ![Šiuo veiksmu bus perrašyti „Excel” tikrinimo duomenų failai.](./media/setup_rsa_tool_102.png)

    Įkeliami abu testavimo atvejai kartu su pirmojo testavimo atveju „Excel“ parametrų failu. Kadangi paskutinio vykdymo metu pasirinkote **Nusiųsti**, parametrų failai yra ištraukiami iš „Azure DevOps“.

    ![Įkelti testavimo atvejai.](./media/setup_rsa_tool_103.png)

3. Pasirinkite tik antrą testavimo atvejį ir pasirinkite **Naujas \> Generuoti testavimo vykdymo ir parametrų failus**.

#### <a name="edit-the-excel-parameter-file"></a>„Excel“ parametrų failo redagavimas

1. Pasirinkite tik antrą testavimo atvejį ir pasirinkite **Redaguoti**, kad atidarytumėte atitinkamą „Excel“ parametrų failą.
2. Kopijuokite **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** įrašytą kintamąjį (žr. skyrių [Esamo užduoties įrašo modifikavimas įrašytam kintamajam sukurti](#modify-an-existing-task-recording-to-create-a-saved-variable)) iš pirmo testavimo atvejo į visus laukus, kur naudojamas produkto numeris. Šiuo atveju nukopijuojate kintamąjį į laukus **Produkto numeris** ir **Tikrinti produkto numerį**, esančius lape **EcoResProductListPage**.

    ![Laukai Produkto numeris ir Tikrinti produkto numerį.](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Kintamuosius galima perduoti iš vieno testo į kitą tik to paties testavimo vykdymo metu. Kintamųjų pavadinimai turi tiksliai sutapti.

3. Pasirinkite **Įrašyti** ir uždarykite „Excel“ darbaknygę.
4. Pasirinkite **Nusiųsti**, kad įrašytumėte keitimus, atliktus „Excel“ parametrų faile.

#### <a name="run-the-chained-test-cases"></a>Grandininių testavimo atvejų vykdymas

1. Pasirinkite abu testavimo atvejus ir pasirinkite **Vykdyti**.
2. Patikrinkite, ar abiejų testavimo atvejų rezultatai teigiami.

    ![Rezultatų laukas nustatytas kaip Sėkmingas abiejų testavimo atvejų.](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
