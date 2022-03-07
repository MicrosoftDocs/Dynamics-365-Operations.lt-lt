---
title: Neautomatinių darbo eigos sprendimų konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti neautomatizuoto sprendimo ypatybes.
author: ChrisGarty
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d54c010c8fe0d8ca6cc8129948392fb56ef85283
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065660"
---
# <a name="configure-manual-decisions-in-a-workflow"></a>Neautomatinių darbo eigos sprendimų konfigūravimas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šioje temoje paaiškinama, kaip konfigūruoti neautomatizuoto sprendimo ypatybes.

Norėdami darbo eigos rengyklėje konfigūruoti neautomatizuotą sprendimą, dešiniuoju pelės mygtuku spustelėkite neautomatizuotą sprendimą ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada naudokite šias procedūras, norėdami konfigūruoti neautomatizuoto sprendimo ypatybes.

## <a name="name-the-decision"></a>Sprendimo pavadinimas

Norėdami įvesti neautomatizuoto sprendimo pavadinimą, atlikite šiuos veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pavadinimas** įveskite unikalų neautomatizuoto sprendimo pavadinimą.

## <a name="enter-a-subject-line-and-instructions"></a>Įveskite subjekto eilutę ir instrukcijas

Turite pateikti temos eilutę ir instrukcijas prie šio neautomatizuoto sprendimo priskirtiems vartotojams. Pavyzdžiui, jei konfigūruojate pirkimo paraiškų sprendimą, sprendimui priskirtas vartotojas matys temos eilutę ir instrukcijas puslapyje **Pirkimo paraiškos**. Temos eilutė rodoma puslapio pranešimo juostoje. Tada, norėdamas peržiūrėti instrukcijas, vartotojas gali spustelėti piktogramą pranešimų juostoje. Norėdami įvesti temos eilutę ir instrukcijas, atlikite šiuos veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Skirtuko **Instrukcijos** lauke **Darbo elemento tema** įveskite temos eilutę.
3. Norėdami personalizuoti temos eilutę, galite įterpti vietos rezervavimo ženklus. Temos eilutę rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.

    1. Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.
    2. Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3. Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4. Spustelėkite **Įterpti**.

4. Norėdami įtraukti temos eilutės vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Pridėti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 3 veiksme.
    6. Spustelėkite **Uždaryti**.

5. Lauke **Darbo elemento instrukcijos** įveskite instrukcijas.
6. Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus. Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.

    1. Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.
    2. Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3. Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4. Spustelėkite **Įterpti**.

7. Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Pridėti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 6 veiksme.
    6. Spustelėkite **Uždaryti**.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Nurodyti galimus sprendimo rezultatus

Paprastai, kai dokumentas priskiriamas sprendimų priėmėjui, sprendimų priėmėjui užduodamas klausimas. Atsakymas į šį klausimą paprastai yra **Taip** arba **Ne**, arba **Teisinga** arba **Klaidinga**. Atlikite šiuos veiksmus, norėdami nurodyti galimus neautomatizuoto sprendimo rezultatus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Skirtuko **Rezultatai** lauke **1 rezultatas** įveskite rezultato pavadinimą arba parinktį.
3. Norėdami įtraukti rezultato vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Pridėti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Spustelėkite **Uždaryti**.

4. Lauke **2 rezultatas** įveskite rezultato pavadinimą arba parinktį.
5. Norėdami įtraukti rezultato vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Pridėti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Spustelėkite **Uždaryti**.

## <a name="specify-when-notifications-are-sent"></a>Nurodymas, kada siunčiami pranešimai

Pranešimus žmonėms galima siųsti, kai sprendimas atliekamas, perduodamas arba perskiriamas. Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pranešimai**.
2. Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.

    - **\[1 pasirinkimas\]** – priskirtas vartotojas pasirinko **\[1 pasirinkimas\]**.
    - **\[2 pasirinkimas\]** – priskirtas vartotojas pasirinko **\[2 pasirinkimas\]**.
    - **Perduoti** – priskirtas vartotojas priskyrė sprendimą kitam vartotojui.
    - **Perskirti** – priskirtas vartotojas sprendimo nepriėmė per skirtąjį laiką.

3. Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.
4. Skirtuko **Pranešimo tekstas** teksto lauke įveskite pranešimo tekstą.
5. Norėdami pranešimus pritaikyti, galite įterpti vietos rezervavimo ženklus. Pranešimą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.

    1. Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.
    2. Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3. Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4. Spustelėkite **Įterpti**.

6. Norėdami įtraukti pranešimų vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Pridėti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 5 veiksme.
    6. Spustelėkite **Uždaryti**.

7. Skirtuke **Gavėjas** nurodykite, kam pranešimai siunčiami. Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 8 veiksmą, atlikite papildomus tos parinkties veiksmus.

    <table>
    <thead>
    <tr>
    <th>Parinktis</th>
    <th>Pranešimo gavėjai</th>
    <th>Papildomi veiksmai</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalyvis</td>
    <td>Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</li>
    <li>Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbo eigos vartotojas</td>
    <td>Dabartinės darbo eigos vartotojai</td>
    <td>
    <ul>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Vartotojas</td>
    <td>Konkretūs vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus. Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.

## <a name="assign-a-decision"></a>Sprendimo priskyrimas

Atlikite šiuos veiksmus, norėdami nurodyti, kam neautomatizuotas sprendimas turėtų būti priskirtas.

1. Kairiojoje srityje spustelėkite **Priskyrimas**.
2. Skirtuke **Priskyrimo tipas** pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 3 veiksmą, atlikite papildomus tos parinkties veiksmus.

    <table>
    <thead>
    <tr>
    <th>Parinktis</th>
    <th>Vartotojai, kuriems priskirtas sprendimas</th>
    <th>Papildomi veiksmai</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalyvis</td>
    <td>Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam norite priskirti sprendimą.</li>
    <li>Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam norite priskirti sprendimą.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarchija</td>
    <td>Konkrečios organizacijos hierarchijos vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite priskirti sprendimą.</li>
    <li>Sistema turi iš hierarchijos nuskaityti vartotojų vardus. Šie vardai nurodo vartotojus, kuriems galima priskirti sprendimą. Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką. <ol>
    <li>Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</li>
    <li>Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>. Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</li>
    </ol>
    </li>
    <li>Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams sprendimas turėtų būti priskirtas. <ul>
    <li><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – sprendimas priskiriamas visiems vartotojams diapazone.</li>
    <li><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – sprendimas priskiriamas tik paskutiniam vartotojui diapazone.</li>
    <li><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – sprendimas nepriskiriamas jokiems diapazono vartotojams, kurie atitinka tam tikrą sąlygą. Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbo eigos vartotojas</td>
    <td>Dabartinės darbo eigos vartotojai</td>
    <td>
    <ul>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Vartotojas</td>
    <td>Konkretūs vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus. Pasirinkite, kuriems vartotojams norite priskirti sprendimą, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek vartotojas turi laiko, skirto sprendimui priimti. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - **Valandos** – įveskite valandų, per kurias vartotojas turi priimti sprendimą, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Dienos** – įveskite dienų, per kurias vartotojas turi priimti sprendimą, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Savaitės** – įveskite savaičių, per kurias vartotojas turi priimti sprendimą, skaičių.
    - **Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių vartotojas turi priimti sprendimą. Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios mėnesio savaitės penktadienio.
    - **Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi priimti sprendimą. Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios gruodžio mėn. savaitės penktadienio.

    Jei per skirtąjį laiką vartotojas sprendimo nepriims, sprendimas bus laikomas vėluojančiu. Vėluojančiu laikomas sprendimas yra perskiriamas atsižvelgiant į parinktis, kurias pasirenkate puslapio srityje **Perskyrimas**.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Įvykių sprendimo vėlavimo atveju nurodymas

Jei per skirtąjį laiką vartotojas sprendimo nepriims, sprendimas bus laikomas vėluojančiu. Vėluojantį sprendimą galima perskirti arba automatiškai priskirti kitam vartotojui. Atlikite tolesnius veiksmus, kad perskirtumėte sprendimą, jei jis vėluoja.

1. Kairiojoje srityje spustelėkite **Perskyrimas**.
2. Pasirinkite žymės langelį **Naudoti perskyrimo maršrutą**, norėdami kurti perskyrimo maršrutą. Sistema automatiškai priskirs sprendimą perskyrimo sąraše pateiktiems vartotojams. Pavyzdžiui, tolesnėje lentelėje pateikiamas perskyrimo maršrutas.

    | Seka | Perskyrimo maršrutas            |
    |----------|----------------------------|
    | 1        | Priskirti: Donna           |
    | 2        | Priskirti: Erin            |
    | 3        | Galutinis veiksmas: \[1 pasirinkimas\] |

    Tokiu atveju, sistema priskirs vėluojantį sprendimą Donna. Jei Donna nepriims sprendimo per skirtąjį laiką, sistema priskirs sprendimą Erin. Jei Erin nepriims sprendimo per skirtąjį laiką, sistema kaip sprendimą pasirinks **\[1 pasirinkimas\]**.

3. Norėdami vartotoją įtraukti į perskyrimo maršrutą, spustelėkite **Įtraukti perskyrimą**. Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 4 veiksmą, atlikite papildomus tos parinkties veiksmus.

    <table>
    <thead>
    <tr>
    <th>Parinktis</th>
    <th>Vartotojai, kuriems perskiriamas sprendimas</th>
    <th>Papildomi veiksmai</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarchija</td>
    <td>Konkrečios organizacijos hierarchijos vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite perskirti sprendimą.</li>
    <li>Sistema turi iš hierarchijos nuskaityti vartotojų vardus. Šie vardai nurodo vartotojus, kuriems galima perskirti sprendimą. Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką. <ol>
    <li>Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</li>
    <li>Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>. Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</li>
    </ol>
    </li>
    <li>Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams sprendimas turėtų būti perskirtas. <ul>
    <li><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – sprendimas perskiriamas visiems vartotojams diapazone.</li>
    <li><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – sprendimas perskiriamas tik paskutiniam vartotojui diapazone.</li>
    <li><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – sprendimas neperskiriamas jokiems diapazono vartotojams, kurie atitinka tam tikrą sąlygą. Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbo eigos vartotojas</td>
    <td>Dabartinės darbo eigos vartotojai</td>
    <td>
    <ul>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Vartotojas</td>
    <td>Konkretūs vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus. Pasirinkite, kuriems vartotojams norite perskirti sprendimą, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek vartotojas turi laiko, skirto sprendimui priimti. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - **Valandos** – įveskite valandų, per kurias vartotojas turi priimti sprendimą, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Dienos** – įveskite dienų, per kurias vartotojas turi priimti sprendimą, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Savaitės** – įveskite savaičių, per kurias vartotojas turi priimti sprendimą, skaičių.
    - **Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių vartotojas turi priimti sprendimą. Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios mėnesio savaitės penktadienio.
    - **Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi priimti sprendimą. Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios gruodžio mėn. savaitės penktadienio.

5. Pakartokite 3 ir 4 veiksmus su kiekvienu vartotoju, kuris turėtų būti įtrauktas į perskyrimo maršrutą. Galite keisti vartotojų tvarką.
6. Jei perskyrimo maršrute esantys vartotojai per skirtąjį laiką nepriima sprendimo, sistema priims sprendimą. Norėdami nurodyti parinktį, kurią sistema pasirinks, pasirinkite eilutę **Veiksmas** ir tada skirtuke **Pabaigos veiksmas** pasirinkite parinktį.

## <a name="set-a-time-limit"></a>Laiko limito nustatymas

Jei sprendimas turi būti priimtas per tam tikrą laiką, atlikite šiuos veiksmus.

> [!NOTE]
> Šioje procedūroje pasirinktos parinktys gali perrašyti parinktis, kurias pasirinkote puslapio srityse **Priskyrimas** ir **Perskyrimas**.

1. Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.
2. Pasirinkite žymės langelį **Nustatyti darbo eigos elemento laiko limitą**.
3. Lauke **Trukmė** nurodykite, kada sprendimas turi būti priimtas. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - **Valandos** – įveskite valandų skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Dienos** – įveskite dienų skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Savaitės** – įveskite savaičių skaičių.
    - **Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių sprendimas turi būti priimtas. Pavyzdžiui, galbūt norite, kad sprendimas būtų priimtas iki trečios mėnesio savaitės penktadienio.
    - **Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių sprendimas turi būti priimtas. Pavyzdžiui, galbūt norite, kad sprendimas būtų priimtas iki trečios gruodžio mėn. savaitės penktadienio.

4. Jei viršijamas laiko limitas, sistema priims sprendimą. Sąraše **Veiksmas** pasirinkite parinktį, kurią sistema turi pasirinkti.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]