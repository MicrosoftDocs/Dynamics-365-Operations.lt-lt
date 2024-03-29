---
title: Darbo eigos patvirtinimo procesų konfigūravimas
description: Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.
author: ChrisGarty
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a4e131b2afa65152d8e9d41b8405895d997250
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070807"
---
# <a name="configure-approval-processes-in-a-workflow"></a>Darbo eigos patvirtinimo procesų konfigūravimas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.

Norėdami darbo eigos rengyklėje konfigūruoti patvirtinimo procesą, dešiniuoju pelės mygtuku spustelėkite patvirtinimo elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.

## <a name="name-the-approval-process"></a>Patvirtinimo proceso pavadinimas

Atlikite šiuos veiksmus, jei norite įvesti patvirtinimo proceso pavadinimą.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pavadinimas** įveskite unikalų patvirtinimo proceso pavadinimą.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Nurodymas, kada sistema automatiškai atlieka veiksmą su dokumentu

Galite konfigūruoti sistemą, kad ji galėtų automatiškai vykdyti tam tikras sąlygas atitinkantį dokumentą. Pvz., sistema gali patvirtinti išlaidų ataskaitas, kurių bendrosios sumos yra mažesnės nei 100 USD. Atlikite šiuos veiksmus, norėdami nurodyti, kada sistema turi atlikti veiksmą su dokumentu.

1. Kairiojoje srityje spustelėkite **Automatiniai veiksmai**.
2. Pažymėkite žymės langelį **Įjungti automatinius veiksmus**.
3. Spustelėkite **Įtraukti sąlygą**.
4. Įveskite sąlygą
5. Jei reikia, įveskite papildomas sąlygas.
6. Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.

    1. Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.
    2. Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.
    3. Spustelėkite **Išbandyti**. Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.
    4. Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.

7. Sąraše **Automatinio užbaigimo veiksmas** pasirinkite veiksmą, kurį su dokumentu turi atlikti sistema.

## <a name="specify-when-notifications-are-sent"></a>Nurodymas, kada siunčiami pranešimai

Pranešimus žmonėms galima siųsti, kai dokumentas yra patvirtintas, atmestas, perduotas ar perskirtas arba kai reikalaujama keitimo. Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pranešimai**.
2. Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.

    - **Perduoti** – kai dokumentas priskiriamas tvirtinti kitam vartotojui.
    - **Perskirti** – kai priskirtas vartotojas per paskirtą laiką neatliko jokių veiksmų su dokumentu.
    - **Patvirtinti** – kai dokumentas buvo patvirtintas.
    - **Atmesti** – kai dokumentas buvo atmestas.
    - **Reikalauti keitimo** – kai priskirtas vartotojas reikalauja keisti pateiktą dokumentą.

3. Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.
4. Spustelėkite skirtuką **Pranešimo tekstas**.
5. Teksto lauke įveskite pranešimo tekstą.
6. Norėdami tekstą personalizuoti, galite įterpti vietos rezervavimo ženklus, kurie bus pakeičiami atitinkamais duomenimis, kai jie bus pateikiami vartotojams. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.

    1. Spustelėkite teksto lauką vietoje, kurioje turėtų atsirasti vietos rezervavimo ženklas.
    2. Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3. Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4. Spustelėkite **Įterpti**.

7. Norėdami įtraukti pranešimų vertimų, spustelėkite **Vertimai**. Rodomoje formoje atlikite šiuos veiksmus.

    1. Spustelėkite **Įtraukti**.
    2. Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    3. Teksto lauke **Išverstas tekstas** įveskite tekstą.
    4. Norėdami personalizuoti tekstą, įterpkite vietos rezervavimo ženklų.
    5. Spustelėkite **Uždaryti**.

8. Spustelėkite skirtuką **Gavėjas**.
9. Nurodykite, kam siunčiami pranešimai. Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 10 veiksmą, atlikite papildomus tos parinkties veiksmus.

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
    <td><strong>Dalyvis</strong></td>
    <td>Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Dalyvis</strong> spustelėkite skirtuką <strong>Pagal vaidmenį</strong>.</li>
    <li>Sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens, kuriam bus siunčiami pranešimai, grupę.</li>
    <li>Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Darbo eigos vartotojas</strong></td>
    <td>Dabartinėje darbo eigoje dalyvaujantys vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, spustelėkite skirtuką <strong>Darbo eigos vartotojas</strong>.</li>
    <li>Sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Vartotojas</strong></td>
    <td>Konkretūs vartotojai</td>
    <td>
    <ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Pakartokite veiksmus 3–9 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.

## <a name="specify-a-final-approver"></a>Galutinio tvirtintojo nurodymas

Galite nurodyti galutinį scenarijų, kuriuose tvirtintojas yra asmuo, pateikęs dokumentą patvirtinimui, ir naudojamas „Neleisti tvirtinti pateikėjui“, tvirtintoją. Norėdami nurodyti galutinį tvirtintoją, atlikite šiuos veiksmus.

1. Darbo eigos rengyklėje dešiniuoju pelės mygtuku spustelėkite patvirtinimo elementą, tada pasirinkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.
2. Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.
3. Pažymėkite žymės langelį **Naudoti galutinį tvirtintoją**.
4. Sąraše pasirinkite vartotoją, kuris bus galutinis tvirtintojas.

## <a name="set-a-time-limit"></a>Laiko limito nustatymas

Jei patvirtinimo procesas turi būti baigtas per tam tikrą laiką, atlikite šiuos veiksmus.

> [!NOTE]
> Parinktys, kurias pasirinkote atlikdami šiuos veiksmus, gali perrašyti parinktis, kurias pasirinkote kiekvieno patvirtinimo veiksmo srityse **Priskyrimas** ir **Perskyrimas**.

1. Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.
2. Pasirinkite žymės langelį **Nustatyti darbo eigos** **elemento laiko limitą**.
3. Lauke **Trukmė** nurodykite, kada patvirtinimo procesas turi būti baigtas. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - **Valandos** – įveskite valandų, per kurias patvirtinimo procesas turi būti baigtas, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Dienos** – įveskite dienų, per kurias patvirtinimo procesas turi būti baigtas, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    - **Savaitės** – įveskite savaičių, per kurias patvirtinimo procesas turi būti baigtas, skaičių.
    - **Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių patvirtinimo procesas turi būti baigtas. Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas trečios mėnesio savaitės penktadienį.
    - **Metai** – pasirinkite savaitę ir mėnesį, iki kurių patvirtinimo procesas turi būti baigtas. Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas iki trečios gruodžio savaitės penktadienio.

4. Jei viršijamas laiko limitas, sistema atliks veiksmą su dokumentu. Sąraše **Veiksmas** pasirinkite veiksmą, kurį turi atlikti sistema.

## <a name="specify-which-actions-are-available-to-the-user"></a>Nurodymas, kuriuos veiksmus vartotojas gali atlikti

Vartotojas turi vykdyti dokumentą, kai dokumentas yra priskirtas vartotojui patvirtinti. Atlikite šiuos veiksmus, norėdami nurodyti, kuriuos veiksmus vartotojas gali atlikti su pateiktu dokumentu.

1. Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.
2. Jei norite, kad vartotojas galėtų tvirtinti dokumentą, pažymėkite žymės langelį **Patvirtinti**.
3. Jei norite, kad vartotojas galėtų atmesti dokumentą, pažymėkite žymės langelį **Atmesti**.
4. Jei norite, kad vartotojai galėtų reikalauti dokumento keitimų, pažymėkite žymės langelį **Reikalauti keitimo**.
5. Jei norite, kad vartotojas galėtų perduoti dokumentą kitam vartotojui, pažymėkite žymės langelį **Perduoti**.

> [!NOTE]
> Žymės langelio **Įjungti veiksmus iš darbų sąrašo įmonės portale** naudoti nebegalima.

## <a name="configure-the-approval-steps"></a>Patvirtinimo veiksmų konfigūravimas

Patvirtinimo procesą sudaro patvirtinimo veiksmai. Atlikite šią procedūrą, norėdami įtraukti veiksmų į patvirtinimo procesą ir veiksmus sukonfigūruoti.

1. Darbo eigos rengyklėje dukart spustelėkite patvirtinimo procesą. Darbo eigos rengyklėje rodomi patvirtinimo proceso veiksmai.
2. Norėdami įtraukti patvirtinimo veiksmą, vilkite veiksmą iš srities **Darbo eigos elementai** į drobę.
3. Norėdami konfigūruoti patvirtinimo veiksmą, žr. [Patvirtinimo veiksmų konfigūravimas darbo eigoje](configure-approval-step-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]