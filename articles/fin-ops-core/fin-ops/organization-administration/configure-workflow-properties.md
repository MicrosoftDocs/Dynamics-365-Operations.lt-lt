---
title: Darbo eigos ypatybių konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti įvairias darbo eigos ypatybes.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693287"
---
# <a name="configure-workflow-properties"></a>Darbo eigos ypatybių konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti įvairias darbo eigos ypatybes.

Norėdami konfigūruoti darbo eigos ypatybes, atidarykite darbo eigą darbo eigos rengyklėje. Spustelėkite lauką darbo eigos rengyklėje ir spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada galite naudoti šias procedūras norėdami konfigūruoti įvairias darbo eigos ypatybes.

## <a name="name-the-workflow"></a>Pavadinimo darbo eigai sukūrimas

Norėdami įvesti darbo eigos pavadinimą, atlikite šiuos veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pavadinimas** įveskite unikalų darbo eigos pavadinimą. Pavyzdžiui, jei kuriate pirkimo paraiškos darbo eigą kiekvienai šaliai / regionui, kuriame veikia jūsų verslas, pirkimo paraiškos darbo eigą galite pavadinti **Pirkimo paraiškos Danijoje** arba **Pirkimo paraiškos Ispanijoje**.

## <a name="specify-the-workflow-owner"></a>Darbo eigos savininko nustatymas

Darbo eigos savininkas yra asmuo, kuris valdo ir prižiūri darbo eigą. Norėdami nustatyti darbo eigos savininką, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Sąraše **Savininkas** pasirinkite darbo eigą valdysiančio asmens vardą.

## <a name="select-an-email-template"></a>El. laiško šablono pasirinkimas

Atlikite šiuos veiksmus, norėdami pasirinkti el. laiško šabloną, kuris naudojamas pranešimams apie darbo eigą generuoti.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Sąraše **Darbo eigos pranešimų el. laiško šablonas** pasirinkite šabloną.

## <a name="enter-instructions-for-users"></a>Instrukcijų vartotojams įvedimas

Galite pateikti instrukcijas vartotojams, kurie pateiks apdorotinus ir tvirtintinus dokumentus. Šie vartotojai taip pat nurodomi kaip *iniciatoriai*. Pavyzdžiui, jūs sukuriate pirkimo paraiškų darbo eigą ir įvedate instrukcijas. Tada tas instrukcijas gali peržiūrėti vartotojai, kurie pirkimo paraiškas įveda puslapyje **Pirkimo paraiškos**. Norėdamas peržiūrėti instrukcijas, iniciatorius turi spustelėti darbo eigos pranešimų juostoje esančią piktogramą. Norėdami vartotojams įvesti instrukcijas, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pateikimo instrukcijos** įveskite instrukcijas.
3. Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus. Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.

    1. Spustelėkite lauką **Pateikimo instrukcijos**, norėdami nurodyti, kur turėtų atsirasti vietos rezervavimo ženklas.
    2. Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3. Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4. Spustelėkite **Įterpti**.

4. Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Pridėti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus. Norėdami instrukcijų apie tai, kaip įvesti vietos rezervavimo ženklą, žr. 3 veiksmą.
    6. Spustelėkite **Uždaryti**.

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a>Nustatymas, kada naudojama ši darbo eiga naudojant aktyvinimo sąlygas

Galite sukurti kelias darbo eigas pagal tą patį darbo eigos tipą. Sukūrus kelias darbo eigas pagal tą patį tipą, jums reikia nurodyti, kada naudojamas kiekvienas šablonas naudojant aktyvinimo sąlygas. Jei aktyvinimo sąlygų nesilaikoma, naudojama numatytoji darbo eiga. Taip pat, jei darbo eigos tipui nustatyta tik viena darbo eigos konfigūracija, ta darbo eigos konfigūracija bus naudojama neatsižvelgiant į aktyvinimo sąlygas.

Pavyzdžiui, galite sukurti pirkimo paraiškos darbo eigą kiekvienai šaliai / regionui, kuriame veikia jūsų verslas, pavyzdžiui, Pirkimo paraiškos Danijoje ir Pirkimo paraiškos Ispanijoje, su toliau nurodytomis sąlygomis.

- Pirkimo paraiškos Danijoje naudojamos, kai: šalis / regionas = DK.
- Pirkimo paraiškos Ispanijoje naudojamos, kai: šalis / regionas = ES.

Norėdami nustatyti, kada turėtų būti naudojama jūsų konfigūruojama darbo eiga, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Aktyvinimas**.
2. Pasirinkite žymės langelį **Nustatyti darbo eigos vykdymo sąlygas**.
3. Spustelėkite **Įtraukti sąlygą**.
4. Įveskite sąlygą
5. Įveskite visas reikalingas papildomas sąlygas.
6. Apžvelkite darbo srautą su keletu paskirties įrašų tam, kad patikrintumėte, ar sąlyga tinkamai apima ir neįtraukia įrašų.

## <a name="specify-when-notifications-are-sent"></a>Nurodymas, kada siunčiami pranešimai

Kai dokumentas pateikiamas apdoroti, sukuriamas darbo eigos egzempliorius. Pranešimus vartotojams galima siųsti, kai dėl klaidos paleidžiami, pabaigiami, atšaukiami arba sustabdomi darbo eigos egzemplioriai (remiantis darbo eiga). Norėdami nustatyti, kada turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pranešimai**.
2. Pažymėkite žymės langelį kiekvienam įvykiui, kuriam įvykus turi būti suaktyvinti pranešimai.

    - **Pradėta** – pranešimai siunčiami, kai darbo eigos egzempliorius paleidžiamas.
    - **Sustabdyta** – pranešimai siunčiami, kai darbo eigos egzempliorius sustabdomas dėl klaidos.
    - **Baigta** – pranešimai siunčiami, kai darbo eigos egzempliorius pabaigiamas.
    - **Nepataisoma** – pranešimai siunčiami, kai darbo eigos egzempliorius sustabdomas dėl nepataisomos klaidos.
    - **Nutraukta** – pranešimai siunčiami, kai darbo eigos egzempliorius nutraukiamas.

3. Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.
4. Skirtuke **Pranešimo tekstas** įveskite pranešimo tekstą.
5. Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus. Tekstą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.

    1. Norėdami nurodyti, kur turėtų atsirasti vietos rezervavimo ženklas, spustelėkite lauką.
    2. Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3. Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4. Spustelėkite **Įterpti**.
    5. Bendras **Pranešimo teksto** rezervavimo ženklas, kurį reikia įtraukti, yra „Last Notes: %Workflow.Last note%“, kuris parodo visus komentarus iš ankstesniojo veiksmo.

6. Norėdami įtraukti teksto vertimų, atlikite šiuos veiksmus.

    1. Spustelėkite **Operacijos**.
    2. Rodomame puslapyje spustelėkite **Įtraukti**.
    3. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4. Lauke **Išverstas tekstas** įveskite tekstą.
    5. Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus. Norėdami instrukcijų apie tai, kaip įvesti vietos rezervavimo ženklą, žr. 5 veiksmą.
    6. Spustelėkite **Uždaryti**.

7. Skirtuke **Gavėjas** naudokite tolesnes parinktis, norėdami nurodyti, kas turėtų gauti pranešimus.

    <table>
    <thead>
    <tr>
    <th>Parinktis</th>
    <th>Pranešimai siunčiami šiems vartotojams</th>
    <th>Norėdami siųsti pranešimus, atlikite šiuos veiksmus</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalyvis</td>
    <td>Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</td>
    <td>
    <ol>
    <li>Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Dalyvis</strong>.</li>
    <li>Skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</li>
    <li>Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbo eigos vartotojas</td>
    <td>Vartotojai, kurie yra šios darbo eigos dalyviai</td>
    <td>
    <ol>
    <li>Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Darbo eigos vartotojas</strong>.</li>
    <li>Skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite šios darbo eigos dalyvį.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Vartotojas</td>
    <td>Konkretūs vartotojai</td>
    <td>
    <ol>
    <li>Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Vartotojas</strong>.</li>
    <li>Skirtuko <strong>Vartotojas</strong> sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus. Pasirinkite, kuriems bus siunčiami pranešimai, ir tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Komentarų apie atliktus darbo eigos pakeitimus įvedimas

Norėdami įvesti komentarų apie atliktus darbo eigos keitimus, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pastabos**.
2. Lauke **Įvesti komentarus apie darbo eigą** įveskite savo komentarus.
3. Peržiūrėkite savo komentarus. Įtraukę komentarus jų modifikuoti negalite.
4. Spustelėkite **Įtraukti**, norėdami komentarų įtraukti į sritį **Komentarų retrospektyva**.
