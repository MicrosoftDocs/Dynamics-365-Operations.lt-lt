---
title: "Automatizuotos darbo eigos užduoties konfigūravimas"
description: "Šioje temoje paaiškinama, kaip konfigūruoti automatizuotos užduoties ypatybes."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e8189f8d16e9b6dcbc339a23c1af5402c0316ce3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a>Automatizuotos darbo eigos užduoties konfigūravimas

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti automatizuotos užduoties ypatybes.

Norėdami darbo eigos rengyklėje konfigūruoti automatizuotą užduotį, dešiniuoju pelės mygtuku spustelėkite užduotį ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada naudokite šias procedūras, norėdami konfigūruoti automatizuotos užduoties ypatybes.

## <a name="name-the-task"></a>Užduoties pavadinimas
Norėdami įvesti automatizuotos užduoties pavadinimą, atlikite šiuos veiksmus.

1.  Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2.  Lauke **Pavadinimas** įveskite unikalų užduoties pavadinimą.

## <a name="specify-when-notifications-are-sent"></a>Nurodymas, kada siunčiami pranešimai
Galite siųsti pranešimus žmonėms, kai automatizuota užduotis buvo vykdoma arba atšaukta. Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.

1.  Kairiojoje srityje spustelėkite **Pranešimai**.
2.  Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.
    -   **Vykdymas** – pranešimai siunčiami užduotį vykdant.
    -   **Atšaukimas** – pranešimai siunčiami užduotį atšaukus.

3.  Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.
4.  Skirtuko **Pranešimo tekstas** teksto lauke įveskite pranešimo tekstą.
5.  Norėdami pranešimus pritaikyti, galite įterpti vietos rezervavimo ženklus. Pranešimą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.
    1.  Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.
    2.  Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3.  Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4.  Spustelėkite **Įterpti**.

6.  Norėdami įtraukti pranešimų vertimų, atlikite šiuos veiksmus.
    1.  Spustelėkite **Operacijos**.
    2.  Rodomame puslapyje spustelėkite **Pridėti**.
    3.  Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4.  Lauke **Išverstas tekstas** įveskite tekstą.
    5.  Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 5 veiksme.
    6.  Spustelėkite **Uždaryti**.

7.  Skirtuke **Gavėjas** nurodykite, kam pranešimai siunčiami. Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 8 veiksmą, atlikite papildomus tos parinkties veiksmus.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Parinktis</th>
    <th>Pranešimo gavėjai</th>
    <th>Papildomi veiksmai</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Dalyvis</td>
    <td>Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</td>
    <td><ol>
    <li>Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</li>
    <li>Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Darbo eigos vartotojas</td>
    <td>Dabartinėje darbo eigoje dalyvaujantys vartotojai</td>
    <td><ul>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Vartotojas</td>
    <td>Konkretūs „Microsoft Dynamics 365 for Finance and Operations‟ vartotojai</td>
    <td><ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Skirtukas <strong>Galimi vartotojai</strong> apima visus „Finance and Operations“ vartotojus. Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.





