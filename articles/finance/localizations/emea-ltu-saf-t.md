---
title: Lietuvai skirtas standartinis mokesčio audito failas (SAF-T)
description: Šioje temoje paaiškinama, kaip nustatyti ir sugeneruoti juridinių subjektų, kurių pagrindinis adresas yra Lietuvoje, standartinį audito failą (TAX-T).
author: liza-golub
ms.author: elgolu
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Lithuania
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb4441f9bff3ad3ecb3fb89803b7b1ce29c93ca3cac37e851d52979ecb186d42
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770500"
---
# <a name="standard-audit-file-for-tax-saf-t-for-lithuania"></a>Lietuvai skirtas standartinis mokesčio audito failas (SAF-T)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Pagal Lietuvos Respublika apskaitos įstatymo 16 straipsnį, Lietuvos įmonės pagal įstatymus turi pateikti ataskaitą standartiniu mokesčių (PST-T) formato audito failu. Šioje temoje aprašoma, kaip palaiko SAF-T reikalavimus ir paaiškinama, kaip pasiruošti finansams dirbti su „Microsoft Dynamics 365 Finance“ SAF-T ataskaita Lietuvai.

Daugiau informacijos rasite [SAF-T - VMI](https://www.vmi.lt/evmi/en/home).

## <a name="setup"></a>Sąranka

Norėdami pradėti dirbti su **Lietuvos SAF-T** ataskaita, užbaikite šiuos veiksmus:

1. [Importuokite elektroninių ataskaitų konfigūracijas.](#import)
2. [Nustatykite **SAF-T formato (LT)** konfigūravimo specialius programos parametrus.](#application)
3. [Didžiosios knygos parametruose pasirinkite SAT-T formatą.](#satt)
4. [Funkcijų valdyme įjunkite funkcijas.](#features)
5. [Sukurkite savo įmonės kontaktinį asmenį.](#contact)

### <a name="import-electronic-reporting-configurations"></a><a name="import"></a>Elektroninių ataskaitų konfigūracijų importavimas

Importuokite šias ar vėlesnes elektroninių ataskaitų (ER) konfigūracijų versijas iš visuotinės saugyklos.

Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti ER konfigūracijas iš „Microsoft" visuotinės saugyklos, žr. Atsisiųsti [ER konfigūracijas iš visuotinės](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md) saugyklos.

| ER kKonfigūracijos pavadinimas       | Tipas          | Versija | Aprašas |
|-----------------------------|---------------|---------|-------------|
| Standartinis audito failas (SAF-T) | Modelis         | 128     | Bendras duomenų modelis, skirtas skirtingoms audito ataskaitoms. |
| SAF-T bendras modelio susiejimas | Modelio susiejimas | 128.251 | Modelio susiejimas, kuris suteikia bendrą duomenų šaltinio susiejimą. |
| SAF-T formatas (LT)           | Formatuoti        | 128.198 | XML formatas, vaizduojantis SAF-T ataskaitą pagal Lietuvos reikalavimus. |

![SAF-T bendroji modelių susiejimo konfigūracija Lietuvai.](media/lt-saf-t-ger-configurations.png)

**SAF-T Bendroji modelio** susiejimo konfigūracija leidžia susieti bendruosius duomenų šaltinį toliau pateikiamais pagrindiniais duomenimis:

- **Visuotinės DK paskyros** – Visuotinė DK.
- **Klientai** – Pirkėjai ir kiti mokėtojai.
- **Tiekėjai** – Tiekėjai ir kiti kreditoriai.
- **Mokesčių lentelė** – Mokesčių tipo lentelės, naudojamos juridinio subjekto apskaitos sistemoje. Pavyzdžiai gali būti pridėtinės vertės mokestis (PVM), įmonės pajamų mokestis ir akcizo mokesčiai.
- **UOM lentelė** – Matavimo vienetų lentelė.
- **Analizės tipo lentelė** – Analitinės apskaitos lentelių duomenys. Šie duomenys naudojami išsamiai operacijos duomenų informacijai pateikti. Pavyzdžiai gali būti vieneto išlaidos, papildomos išlaidos, išlaidų centras arba projektas.
- **Judėjimo tipo lentelė** – atsargų perkėlimo tipai.
- **Produktai** – Produktai ir paslaugos.
- **Fizinės atsargos** – Duomenys apie faile esančias atsargas.

**SAF-T Bendroji modelio** susiejimo konfigūracija taip pat leidžia susieti bendruosius duomenų šaltinį toliau pateikiamais oepracijų duomenimis:

- **Visuotinės DK įrašai** – Visuotinės DK įrašai.
- **Pardavimo SF** – pradiniai pardavimo dokumentai.
- **Pirkimo SF** – pirkimo ir įsigijimo apskaitos dokumentai.
- **Mokėjimai** – mokėjimai.
- **Prekių judėjimas** – informacija apie prekių judėjimą. Pavyzdžiui, perkėlimas įvyksta įrašant prekes, nurašant jas po to, kai jos parduotos ar panaudotos gamyboje, ir įrašant baigtus produktus, nustatytą nuostolį ir brokuotas prekes.
- **Turto operacijos** – Ekonominės operacijos arba materialaus ar nematerialaus ekonominio turto bei finansinio turto įvykiai.

Importuokite naujausias konfigūracijų versijas. Versijos apraše paprastai yra „Microsoft“ žinių bazės (KB) straipsnio, kuriame paaiškinami konfigūracijos versijoje įgyvendinti pakeitimai, numeris.

> [!IMPORTANT]
> Importavę visas anksčiau pateiktoje ankstesnėje lentelėje nurodytas ER konfigūracijas, parinktyje **Numatytasis modelių susiejimui**, nustatykite **Taip** SAF-T bendrojo modelio žymėjimo **konfigūracijai**.
>
> ![Numatytoji modelio susiejimo pasirinktis, nustatyta kaip Taip, jei susiekite SAF-T bendrą modelio susiejimo konfigūraciją.](media/lt-saf-t-default-model-mapping.png)

### <a name="set-up-application-specific-parameters-for-the-saf-t-format-lt-configuration"></a><a name="application"></a>Nustatykite SAF-T formato (LT) konfigūravimo specialius programos parametrus

1. Elektroninėse ataskaitose atverkite **Konfigūravimų** puslapį. 
2. Konfigūracijos medyje, prie **Standartinio audito rinkmenos (SAF-T)** pasirinkite **SAF-T formatą (LT)**.
3. Įsitikinkite, kad dirbate įmonėje, kuriai norite nustatyti konkrečios programos parametrus.
4. Rinkitės **Konfigūravimai** \> **Konkrečių programų parametrai** ir tada veiksmų juostoje rinkitės **Nustatymai**.
5. Kairėje esančiame sąraše pasirinkite paskutinę konfigūravimo versiją.
6. Pateikti visų peržvalgos laukų susiejimą:

    - **StandardAnalysisType_LOOKUP – apibrėžti įmonės naudojamų prekybos mokesčių dimensijų** , naudojamų įmonės ir Lietuvos standartinių analizės tipų. Pasirinkite reikšmę **„APA-100”** kaip paskutinę sąlygą sąraše. Stulpelis **Analizės ID** turi būti nustatytas kaip **\*Ne tuščias\***. Stulpelyje **Eilutė** patikrinkite, ar **„APA-100”** yra paskutinė lentelės sąlyga. Turi būti nustatyta bent viena eilutė, turinti **\*Ne tuščia\*** reikšmes.
    - **ReportTaxCodes_LOOKUP – apibrėžti įmonės naudojamų prekybos mokesčių kodų** , naudojamų įmonės ir Lietuvos pagrindinių sąskaitų susiejimą. Pasirinkite reikšmę **„PVM100”** kaip paskutinę sąlygą sąraše. Stulpelis **Mokesčių kodas** turi būti nustatytas kaip **\*Ne tuščias\***. Stulpelyje **Eilutė** patikrinkite, ar **„PVM100”** yra paskutinė lentelės sąlyga. Turi būti nustatyta bent viena eilutė, turinti **\*Ne tuščia\*** reikšmes.
    - **AddressType_LOOKUP – apibrėžti įmonės naudojamų adresų tipų susiejimą su adresų tipais, kurie naudojami** Lietuvos ataskaitoje SAF-T. Pasirinkite reikšmę **„KT”** kaip paskutinę sąlygą sąraše. Stulpelis **Tikslo pavadinimas** turi būti nustatytas kaip **\*Ne tuščias\***. Stulpelyje **Eilutė** patikrinkite, ar **„KT”** yra paskutinė lentelės sąlyga. Turi būti nustatyta bent viena eilutė, turinti **\*Ne tuščia\*** reikšmes.
    - **StandardMainAccount_Lookup – apibrėžti įmonės naudojamų pagrindinių sąskaitų ir standartinių** Lietuvos pagrindinių sąskaitų susiejimą. Pasirinkite reikšmę **„7”** kaip paskutinę sąlygą sąraše. Stulpelis **Analizės ID** turi būti nustatytas kaip **\*Ne tuščias\***. Stulpelyje **Eilutė** patikrinkite, ar **„7”** yra paskutinė lentelės sąlyga. Turi būti nustatyta bent viena eilutė, turinti **\*Ne tuščia\*** reikšmes.

6. Kai baigiate peržvalgos laukų nustatymą, lauke Būsena **pasirinkite** **Baigta**. Įrašykite konfigūraciją.

### <a name="select-the-sat-t-format-in-general-ledger-parameters"></a><a name="satt"></a>Didžiosios knygos parametruose pasirinkite SAT-T formatą

1. Eikite į **Didžioji knyga** \> **nustatymas** \> **DK parametrai**.
2. Standartinio mokesčių "FastTab" audito failo standartinio audito failo **mokesčių** **(SAF-T) lauke** nustatykite SAF-T formatą.

### <a name="turn-on-features-in-feature-management"></a><a name="features"></a>Funkcijų valdyme įjunkite funkcijas

1. Eikite į **Funkcijų valdymas** ir pasirinkite skirtuką **Visi**.
2. Funkcijų sąraše raskite ir rinkitės šias funkcijas:

    - Užklausos duomenų šaltinio kūrimo laiko optimizavimas vykdant ER ataskaitas
    - Optimizuoti duomenų rinkinių atminties sąnaudas vykdant ER ataskaitas

3. Pasirinkite **Įjungti dabar**.

### <a name="create-a-contact-person-for-your-company"></a><a name="contact"></a>Sukurkite savo įmonės kontaktinį asmenį

SAF-T ataskaitos **Įmonės** mazge turi būti kontakto informacija. Šis mazgas yra **Antraštės** mazge. Norėdami nustatyti kontaktinę informaciją, kuri bus pateikiama SAF-T, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara** \> **Ryšiai** \> **Kontaktai** \> **Visi kontaktai**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują savo juridinio subjekto kontaktą. Įsitikinkite, kad pasirinkote **Juridinis subjektas** lauke **Kontaktas**. 
3. Patikrinkite **Šalies ID** reikšmę, kad įsitikintumėte, jog pasirinkote juridinį subjektą, iš kurio SAF-T bus pateiktas.

![ER konfigūracijos, skirtos Lietuvos SAF-T ataskaitos.](media/lt-saf-t-contact-person.png)

## <a name="generate-the-saf-t-report"></a>SAF-T ataskaitos generavimas

- Norėdami generuoti SAF-T ataskaitą, eikite į DK užklausas ir ataskaitas apie standartinį mokesčių (PST-T) standartinį **audito** \> **failą** \> **mokesčiui** \> **(SAF-T)**.

Toliau pateikiamoje lentelėje aprašomi ataskaitos dialogo lango laukai.

| Lauko pavadinimas | Aprašas |
|------------|-------------|
| **SAF-T failo tipas** | <p>SAF-T palaiko šiuos failų tipus:</p><ul><li>**„F“** – visas SAF-T failas. Šio tipo SAF-T failą galima skaidyti pagal laikotarpį.</li><li>**DK** – DK įrašai. Šią SAF-T failo dalį galima skaidyti pagal objektus, laikotarpius ar dalis. </li><li>**„PI“** – pirkimo duomenys. Šią SAF-T failo dalį galima skaidyti pagal objektus, laikotarpius ar dalis.</li><li>**„PA“** – mokėjimo duomenys. Šią SAF-T failo dalį galima skaidyti pagal objektus, laikotarpius ar dalis.</li><li>**„SI“** – pardavimo duomenys. Šią SAF-T failo dalį galima skaidyti pagal objektus, laikotarpius ar dalis.</li><li>**„MG“** – prekių judėjimas. Šią SAF-T failo dalį galima skaidyti pagal objektus, laikotarpius ar dalis.</li><li>**„AS“** – ilgalaikio turto perkėlimas. Šią SAF-T failo dalį galima skaidyti pagal objektus, laikotarpius ar dalis.</li><ul> |
| **Ataskaitinis laikotarpis** nuo ir **ataskaitinis laikotarpis iki** | Apibrėžkite laikotarpio, už kurį reikalauja SAF-T, pradžios ir pabaigos datas. Pradžios data atsispindi **mazge Antraštė** \> **Atrankos kriterijai** \> **Atrankos pradžios data, o pabaigos data atsispindi mazge** **Antraštė** \> **Atrankos kriterijai** \> **Atrankos pabaigos data**. |
| **Data nuo** ir **Data iki** | Nurodykite laikotarpio, kurį ataskaita turi apimti, pradžios ir pabaigos datas. Pradžios data atsispindi **SAF-T** \> **Antraštė atrankos kirterijai** \> **Laikotarpio pradžia** mazge. Pabaigos data atsispindi **SAF-T** \> **Antraštė atrankos kirterijai** \> **Laikotarpio pabaigos** mazge. Vieno failo arba vienos failo dalies laikotarpis negali būti trumpesnis nei vienas mėnuo ir ilgesnis už ataskaitinį laikotarpį. |
| **Dalių skaičius** | Nurodykite dalių, kuriose bus generuojama SAF-T skaičius. Ši vertė atsispindi **Antraštė** \> **Dalių skaičiaus SAF-T mazgas**. |
| **Dalies numeris** | Nurodykite dalies, kuri kuriama dabar SAF-T, skaičių. Ši vertė atsispindi **Antraštė** \> **Dalies skaičius SAF-T mazgas**. |
| **Spausdinti nulinį balansą** | Šis žymės langelis turi įtakos duomenims, kurie pranešami **Pagrindiniai failai** \> **DK paskyros** mazge, kuris yra SAF-T. Pasirinkite šį žymės langelį, jei norite įtraukti visas pagrindines jūsų įmonės sąskaitas, net tas pagrindines sąskaitas, kurių balansas nurodytu laikotarpiu yra nulinis. Išvalykite žymės langelį, kad būtų įtrauktos tik tos pagrindinės sąskaitos, kurių balansas nėra lygus nuliui arba operacijos nurodytu laikotarpiu. |
| **Eksportuoti visus klientus** | Šis žymės langelis turi įtakos duomenims, kurie pranešami **Pagrindiniai failai** \> **Kliento** mazge, kuris yra SAF-T. Pasirinkite šį žymės langelį, jei norite įtraukti visus pagrindinius jūsų įmonės klientus, net tuos klientus, kurių balansas nurodytu laikotarpiu yra nulinis. Išvalykite žymės langelį, kad būtų įtraukti tik tie klientai, kurių balansas nėra lygus nuliui arba operacijos nurodytu laikotarpiu. |
| **Eksportuoti visus tiekėjus** | Šis žymės langelis turi įtakos duomenims, kurie pranešami **Pagrindiniai failai** \> **Tiekėjų** mazge, kuris yra SAF-T. Pasirinkite šį žymės langelį, jei norite įtraukti visus pagrindinius jūsų įmonės tiekėjus, net tuos tiekėjus, kurių balansas nurodytu laikotarpiu yra nulinis. Išvalykite žymės langelį, kad būtų įtraukti tik tie tiekėjai, kurių balansas nėra lygus nuliui arba operacijos nurodytu laikotarpiu. |
| **Eksportuoti visus analizės tipus** | Šis žymės langelis turi įtakos duomenims, kurie pranešami **Pagrindiniai failai** \> **Analizavimo tipo lentelės** mazge, kuris yra SAF-T. Pažymėti šį žymės langelį, norint įtraukti visas jūsų įmonės dimensijas. Išvalyti šį žymės langelį, kad būtų įtrauktos tik tos dimensijos, kurios naudojamos operacijose, kurios buvo įtrauktos per nurodytą laikotarpį. |
| **Eksportuoti visus produktus** | Šis žymės langelis turi įtakos duomenims, kurie pranešami **Pagrindiniai failai** \> **Produktų** mazge, kuris yra SAF-T. Pasirinkite šį žymės langelį, jei norite įtraukti visus pagrindinius jūsų įmonės produktus, net tuos produktus, kurių fizinės atsargos nurodytu laikotarpiu yra nulinės. Išvalykite žymės langelį, kad būtų įtrauktos tik tos pagrindiniai produktai, kurių fizinės atsargos nėra lygios nuliui arba operacijos nurodytu laikotarpiu. |
| **Eksportuoti visus PVM kodus** | Šis žymės langelis turi įtakos duomenims, kurie pranešami **Pagrindiniai failai** \> **Mokesčių lentelės** mazge, kuris yra SAF-T. Pažymėti šį žymės langelį, norint įtraukti visus jūsų įmonės mokesčių kodus. Išvalyti šį žymės langelį, kad būtų įtrauktos tik tie prekybos mokesčių kodai, kurie naudojami operacijose, kurios buvo įtrauktos per nurodytą laikotarpį. |

## <a name="saf-t-content"></a>SAF-T turinys

Pagal SAF-T techninėje dokumentacijoje, skirtingais IŠ SAF-T tipais yra skirtingas turinys, kaip parodyta pateiktoje lentelėje.

| SAF-T failo dalis        | Elementų grupė     | Pn. | GL | MG | SI | PI | PA | AS |
|------------------------|-----------------------|---|----|----|----|----|----|----|
| Antraštė                 |                       |   |    |    |    |    |    |    |
|                        | Antraštė                | X | X  | X  | X  | X  | X  | X  |
| Pagrindiniai failai           |                       |   |    |    |    |    |    |    |
|                        | DK sąskaitos | X | X  |    |    |    |    |    |
|                        | Klientai             | X | X  | X  | X  | X  | X  |    |
|                        | Tiekėjai             | X | X  | X  | X  | X  | X  | X  |
|                        | Mokesčių lentelė              | X | X  | X  | X  | X  |    |    |
|                        | UOM lentelė              | X |    | X  | X  | X  |    |    |
|                        | Analizės tipo lentelė     | X | X  |    | X  | X  | X  |    |
|                        | Judėjimo tipo lentelė     | X |    | X  |    |    |    |    |
|                        | Produktai              | X |    | X  | X  | X  |    |    |
|                        | Faktinės atsargos         | X |    | X  | X  | X  |    |    |
|                        | Turtas                | X |    |    |    |    |    | X  |
| Didžiosios knygos įrašai |                       |   |    |    |    |    |    |    |
|                        | DK įrašai  | X | X  |    |    |    |    |    |
| Šaltinio dokumentai       |                       |   |    |    |    |    |    |    |
|                        | Pardavimo SF        | X |    |    | X  |    |    |    |
|                        | Pirkimo SF      | X |    |    |    | X  |    |    |
|                        | Mokėjimai              | X |    |    |    |    | X  |    |
|                        | Prekių judėjimas       | X |    | X  |    |    |    |    |
|                        | Turto operacijos     | X |    |    |    |    |    | X  |
