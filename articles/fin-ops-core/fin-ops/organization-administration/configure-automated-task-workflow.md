---
title: Automatizuotų darbo eigos užduočių konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti automatizuotos užduoties ypatybes.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b63a9a99c442b0fbe971bc2e8f05fc8c09ec3087
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567491"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>Automatizuotų darbo eigos užduočių konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti automatizuotos užduoties ypatybes.

Norėdami darbo eigos rengyklėje konfigūruoti automatizuotą užduotį, dešiniuoju pelės mygtuku spustelėkite užduotį ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada naudokite šias procedūras, norėdami konfigūruoti automatizuotos užduoties ypatybes.

## <a name="name-the-task"></a>Užduoties pavadinimas

Norėdami įvesti automatizuotos užduoties pavadinimą, atlikite šiuos veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pavadinimas** įveskite unikalų užduoties pavadinimą.

## <a name="specify-when-notifications-are-sent"></a>Nurodymas, kada siunčiami pranešimai

Galite siųsti pranešimus žmonėms, kai automatizuota užduotis buvo vykdoma arba atšaukta. Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.

1. Kairiojoje srityje spustelėkite **Pranešimai**.
2. Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.

    - **Vykdymas** – pranešimai siunčiami užduotį vykdant.
    - **Atšaukimas** – pranešimai siunčiami užduotį atšaukus.

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
    <td>Dabartinėje darbo eigoje dalyvaujantys vartotojai</td>
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]