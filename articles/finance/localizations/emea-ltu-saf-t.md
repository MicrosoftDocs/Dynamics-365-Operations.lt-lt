---
title: Lietuvai skirtas standartinis mokesčio audito failas (SAF-T)
description: Šioje temoje paaiškinama, kaip nustatyti ir sugeneruoti juridinių subjektų, kurių pagrindinis adresas yra Lietuvoje, standartinį audito failą (TAX-T).
author: liza-golub
ms.author: elgolu
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Lithuania
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d3d5da75faaa121fcafd0b6e120f1537b3d208e6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019514"
---
# <a name="standard-audit-file-for-tax-saf-t-for-lithuania"></a>Lietuvai skirtas standartinis mokesčio audito failas (SAF-T)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Pagal Lietuvos Respublika apskaitos įstatymo 16 straipsnį, Lietuvos įmonės pagal įstatymus turi pateikti ataskaitą standartiniu mokesčių (PST-T) formato audito failu. Šioje temoje aprašoma, kaip palaiko SAF-T reikalavimus ir paaiškinama, kaip pasiruošti finansams dirbti su „Microsoft Dynamics 365 Finance“ SAF-T ataskaita Lietuvai.

Daugiau informacijos rasite [SAF-T - VMI](https://www.vmi.lt/cms/web/guest/saf-t).

## <a name="setup"></a>Sąranka

Norėdami pradėti dirbti su **Lietuvos SAF-T** ataskaita, atlikite šiuos veiksmus.

1. Importuokite šias ar vėlesnes elektroninių ataskaitų (ER) konfigūracijų versijas iš visuotinės saugyklos.

    | ER kKonfigūracijos pavadinimas       | Tipas          | Versija | Aprašas |
    |-----------------------------|---------------|---------|-------------|
    | Standartinis audito failas (SAF-T) | Modelis         | 128     | Bendras duomenų modelis, skirtas skirtingoms audito ataskaitoms. |
    | SAF-T bendras modelio susiejimas | Modelio susiejimas | 128.251 | Modelio susiejimas, kuris suteikia bendrą duomenų šaltinio susiejimą. |
    | SAF-T formatas (LT)           | Formatuoti        | 128.198 | XML formatas, vaizduojantis SAF-T ataskaitą pagal Lietuvos reikalavimus. |

    ![ER konfigūracijos, skirtos Lietuvos SAF-T ataskaitos](media/lt-saf-t-ger-configurations.png)

    **SAF-T Bendroji modelio** susiejimo konfigūracija leidžia susieti bendruosius duomenų šaltinį toliau pateikiamais pagrindiniais duomenimis:

    - **Visuotinės DK paskyros** – Visuotinė DK.
    - **Klientai** – pirkėjai (klientai) ir kiti skolininkai (pateikti faile).
    - **Tiekėjai** – tiekėjai ir kiti kreditoriai (pateikiama faile).
    - **TaxTable** – mokesčių tipo lentelių duomenys. Nurodytos visos mokesčių tipo lentelės, naudojamos juridinio subjekto apskaitos sistemoje. Pavyzdžiai gali būti pridėtinės vertės mokestis (PVM), įmonės pajamų mokestis ir akcizo mokesčiai.
    - **UOM lentelė** – matavimo vienetų tipų lentelė.
    - **Analizės tipo lentelė** – analitinės apskaitos lentelių tipų duomenys. Šie duomenys naudojami išsamiai operacijos duomenų informacijai pateikti. Pavyzdžiai gali būti vieneto išlaidos, papildomos išlaidos, išlaidų centras arba projektas.
    - **Judėjimo tipo lentelė** – atsargų perkėlimo tipai.
    - **Produktai** – Produktai ir paslaugos.
    - **Fizinės atsargos** – atsargos (duomenys apie faile esančias atsargas).

    **SAF-T Bendroji modelio** susiejimo konfigūracija taip pat leidžia susieti bendruosius duomenų šaltinį toliau pateikiamais oepracijų duomenimis:

    - **Visuotinės DK įrašai** – Visuotinės DK įrašai.
    - **Pardavimo SF** – pradiniai pardavimo dokumentai.
    - **Pirkimo SF** – pirkimo ir įsigijimo apskaitos dokumentai.
    - **Mokėjimai** – mokėjimai.
    - **Prekių judėjimas** – informacija apie prekių judėjimą. Pavyzdžiui, perkėlimai apima prekių įrašymą, prekių nurašymą po to, kai jos parduodamos arba naudojamos gamyboje, ir baigtų produktų įrašymą, nustatytą nuostolį ir brokuotas prekes.
    - **Turto operacijos** – ekonominės operacijos arba ekonominės turto įvykiai (materialus, nematerialusis ir finansinis turtas).

    Būtinai importuokite naujausias konfigūracijų versijas. Versijos apraše paprastai yra „Microsoft“ žinių bazės (KB) straipsnio, kuriame paaiškinami konfigūracijos versijoje įgyvendinti pakeitimai, numeris.

    > [!IMPORTANT]
    > Importavę visas anksčiau pateiktoje ankstesnėje lentelėje nurodytas ER konfigūracijas, parinktyje **Numatytasis modelių susiejimui**, nustatykite **Taip** SAF-T bendrojo modelio žymėjimo **konfigūracijai**.
    >
    > ![Numatytoji modelio susiejimo pasirinktis, nustatyta kaip Taip, jei susiekite SAF-T bendrą modelio susiejimo konfigūraciją](media/lt-saf-t-default-model-mapping.png)

    Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti ER konfigūracijas iš „Microsoft" visuotinės saugyklos, žr. Atsisiųsti [ER konfigūracijas iš visuotinės](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md) saugyklos.

    Po to turite nustatyti IRT formato (LT) konfigūravimo **specialius programos** parametrus.
    
2. Elektroninėse ataskaitose atverkite **Konfigūravimų** puslapį. Konfigūracijos medyje, prie **Standartinio audito rinkmenos (SAF-T)** pasirinkite **SAF-T formatą (LT)**.
3. Rinkitės **Konfigūravimai** \> **Konkrečių programų parametrai** ir tada veiksmų juostoje rinkitės **Nustatymai**.
4. Rinkitės paskutinę konfigūravimo versiją sąraše kairėje.
5. Pateikti visų peržvalgos laukų susiejimą:

    - **StandardMainAccount_Lookup – apibrėžti įmonės naudojamų pagrindinių sąskaitų ir standartinių** Lietuvos pagrindinių sąskaitų susiejimą.
    - **ReportTaxCodes_LOOKUP – apibrėžti įmonės naudojamų prekybos mokesčių kodų** , naudojamų įmonės ir Lietuvos pagrindinių sąskaitų susiejimą.
    - **StandardAnalysisType_LOOKUP – apibrėžti įmonės naudojamų prekybos mokesčių dimensijų** , naudojamų įmonės ir Lietuvos standartinių analizės tipų.
    - **AddressType_LOOKUP – apibrėžti įmonės naudojamų adresų tipų susiejimą su adresų tipais, kurie naudojami** Lietuvos ataskaitoje SAF-T.

6. Kai baigiate peržvalgos laukų nustatymą, lauke Būsena **pasirinkite** **Baigta**. Įrašykite konfigūraciją.
7. Eikite į **Didžioji knyga** \> **nustatymas** \> **DK parametrai**.
8. Standartinio mokesčių "FastTab" audito failo standartinio audito failo **mokesčių** **(SAF-T) lauke** nustatykite SAF-T formatą.
9. Eikite į **Funkcijos valdymą** \> **Visi**.
10. Funkcijų sąraše raskite ir rinkitės šias funkcijas:

    - Užklausos duomenų šaltinio kūrimo laiko optimizavimas vykdant ER ataskaitas
    - Optimizuoti duomenų rinkinių atminties sąnaudas vykdant ER ataskaitas

11. Pasirinkite **Įjungti dabar**.

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
