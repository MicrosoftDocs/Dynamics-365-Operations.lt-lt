---
title: "Darbo eigos patvirtinimo veiksmo konfigūravimas"
description: "Šioje temoje paaiškinama, kaip konfigūruoti patvirtinimo veiksmo ypatybes."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1924562f866ecdbb6fa6d3d0a9dc7627387f2d6a
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="configure-an-approval-step-in-a-workflow"></a>Darbo eigos patvirtinimo veiksmo konfigūravimas

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip konfigūruoti patvirtinimo veiksmo ypatybes.

Norėdami darbo eigos rengyklėje konfigūruoti patvirtinimo veiksmą, dešiniuoju pelės mygtuku spustelėkite patvirtinimo veiksmą ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**. Tada naudokite šias procedūras, norėdami konfigūruoti patvirtinimo veiksmo ypatybes.

## <a name="name-the-step"></a>Veiksmo pavadinimas
Norėdami įvesti patvirtinimo veiksmo pavadinimą, atlikite šiuos veiksmus.

1.  Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2.  Lauke **Pavadinimas** įveskite unikalų patvirtinimo veiksmo pavadinimą.

## <a name="enter-a-subject-line-and-instructions"></a>Įveskite subjekto eilutę ir instrukcijas
Turite pateikti temos eilutę ir instrukcijas prie šio patvirtinimo veiksmo priskirtiems vartotojams. Pavyzdžiui, jei konfigūruojate pirkimo paraiškų patvirtinimo veiksmą, veiksmui priskirtas vartotojas matys temos eilutę ir instrukcijas puslapyje **Pirkimo paraiškos**. Temos eilutė rodoma puslapio pranešimo juostoje. Tada, norėdamas peržiūrėti instrukcijas, vartotojas gali spustelėti piktogramą pranešimų juostoje. Norėdami įvesti temos eilutę ir instrukcijas, atlikite šiuos veiksmus.

1.  Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2.  Lauke **Darbo elemento tema** įveskite temos eilutę.
3.  Norėdami personalizuoti temos eilutę, galite įterpti vietos rezervavimo ženklus. Temos eilutę rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.
    1.  Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.
    2.  Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3.  Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4.  Spustelėkite **Įterpti**.

4.  Norėdami įtraukti temos eilutės vertimų, atlikite šiuos veiksmus.
    1.  Spustelėkite **Operacijos**.
    2.  Rodomame puslapyje spustelėkite **Pridėti**.
    3.  Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4.  Lauke **Išverstas tekstas** įveskite tekstą.
    5.  Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 3 veiksme.
    6.  Spustelėkite **Uždaryti**.

5.  Lauke **Darbo elemento instrukcijos** įveskite instrukcijas.
6.  Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus. Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis. Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.
    1.  Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.
    2.  Spustelėkite **Įterpti vietos rezervavimo ženklą**.
    3.  Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.
    4.  Spustelėkite **Įterpti**.

7.  Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.
    1.  Spustelėkite **Operacijos**.
    2.  Rodomame puslapyje spustelėkite **Pridėti**.
    3.  Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.
    4.  Lauke **Išverstas tekstas** įveskite tekstą.
    5.  Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 6 veiksme.
    6.  Spustelėkite **Uždaryti**.

## <a name="assign-the-approval-step"></a>Patvirtinimo veiksmo priskyrimas
Atlikite šiuos veiksmus, kad nurodytumėte, kam patvirtinimo veiksmas turėtų būti priskirtas.

1.  Kairiojoje srityje spustelėkite **Priskyrimas**.
2.  Skirtuke **Priskyrimo tipas** pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 3 veiksmą, atlikite papildomus tos parinkties veiksmus.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Parinktis</th>
    <th>Vartotojai, kuriems priskirtas patvirtinimo veiksmas</th>
    <th>Papildomi veiksmai</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Dalyvis</td>
    <td>Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</td>
    <td><ol>
    <li>Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam norite priskirti veiksmą.</li>
    <li>Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam norite priskirti veiksmą.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarchija</td>
    <td>Konkrečios organizacijos hierarchijos vartotojai</td>
    <td><ol>
    <li>Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite priskirti veiksmą.</li>
    <li>Sistema turi iš hierarchijos nuskaityti vartotojų vardus. Šie vardai nurodo vartotojus, kuriems galima priskirti veiksmą. Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką. <ol>
    <li>Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</li>
    <li>Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>. Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</li>
    </ol></li>
    <li>Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams veiksmas turėtų būti priskirtas. <ul>
    <li><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – veiksmas priskiriamas visiems vartotojams diapazone.</li>
    <li><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – veiksmas priskiriamas tik paskutiniam vartotojui diapazone.</li>
    <li><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – veiksmas nepriskiriamas jokiems diapazono vartotojams, kurie atitinka tam tikrą sąlygą. Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Darbo eigos vartotojas</td>
    <td>Dabartinės darbo eigos vartotojai</td>
    <td><ul>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Vartotojas</td>
    <td>Konkretūs „Microsoft Dynamics 365 for Operations“ vartotojai</td>
    <td><ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Skirtukas <strong>Galimi vartotojai</strong> apima visus „Dynamics 365 for Operations“ vartotojus. Pasirinkite, kuriems vartotojams norite priskirti veiksmą, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek laiko vartotojas turi imtis veiksmų arba reaguoti į dokumentus, kurie yra patvirtinimo veiksme. Pasirinkite vieną iš toliau pateiktų pasirinkčių:
    -   **Valandos** – įveskite valandų, per kurias vartotojas turi reaguoti, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    -   **Dienos** – įveskite dienų, per kurias vartotojas turi reaguoti, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    -   **Savaitės** – įveskite savaičių, per kurias vartotojas turi reaguoti, skaičių.
    -   **Mėnesiai** – pasirinkite dieną ir savaitę, iki kurios vartotojas turi reaguoti. Pavyzdžiui, galbūt norite, kad vartotojas atsakytų iki trečiosios mėnesio savaitės penktadienio.
    -   **Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi reaguoti. Pavyzdžiui, galbūt norite, kad vartotojas atsakytų iki trečiosios gruodžio mėn. savaitės penktadienio.

    Jei per skirtąjį laiką vartotojas nesiims veiksmų su dokumentu, dokumentas laikomas vėluojančiu. Vėluojančiu laikomas dokumentas yra perskiriamas atsižvelgiant į parinktis, kurias pasirenkate puslapio srityje **Perskyrimas**.
4.  Jei patvirtinimo veiksmą priskiriate keliems vartotojams arba vartotojų grupei, skirtuke **Baigimo strategija** pasirinkite vieną iš tolesnių parinkčių.
    -   **Vienas tvirtintojas** – koks bus atliekamas veiksmas su dokumentu, sprendžia pirmasis turintis reaguoti asmuo. Pvz., Sam pateikė 15 000 JAV dolerių išlaidų ataskaitą. Šiuo metu išlaidų ataskaita yra priskirta Sue, Jo ir Bill. Jei Sue yra pirmasis asmuo, kuris turi reaguoti į dokumentą, veiksmas, kurį ji atlieka, bus taikomas dokumentui. Jei Sue dokumentą atmeta, jis atmetamas ir grąžinamas Sam. Jei Sue dokumentą patvirtina, jis siunčiamas Ann tvirtinti. ![Darbo eiga su patvirtinimo procesu](./media/workflow_multipleusersinstep.gif)
    -   **Tvirtintojų dauguma** – koks bus atliekamas veiksmas su dokumentu, lemia tvirtintojų dauguma. Pvz., Sam pateikė 15 000 JAV dolerių išlaidų ataskaitą. Šiuo metu išlaidų ataskaita yra priskirta Sue, Jo ir Bill. Jei Sue ir Jo yra pirmieji du tvirtintojai, kurie reaguoja, jų atliekami veiksmai bus taikomi dokumentui.
        -   Jei Sue patvirtina dokumentą, o Jo jį atmeta, dokumentas yra atmetamas ir siunčiamas atgal Sam.
        -   Jei tiek Sue, tiek Jo dokumentą patvirtina, jis siunčiamas Ann patvirtinti.
    -   **Tvirtintojų procentas** – koks bus atliekamas veiksmas su dokumentu, lemia tam tikras tvirtintojų procentas. Pvz., Sam pateikė 15 000 JAV dolerių išlaidų ataskaitą. Šiuo metu išlaidų ataskaita yra priskirta Sue, Jo ir Bill, o jūs kaip procentą įvedėte **50**. Jei Sue ir Jo pirmieji du Tvirtintojai, kurie reaguoja, jų atliekami veiksmai bus taikomi dokumentui, nes jie sudaro reikiamus 50 procentų tvirtintojų.
        -   Jei Sue patvirtina dokumentą, o Jo jį atmeta, dokumentas yra atmetamas ir siunčiamas atgal Sam.
        -   Jei tiek Sue, tiek Jo dokumentą patvirtina, jis siunčiamas Ann patvirtinti.
    -   **Visi tvirtintojai** – visi tvirtintojai turi patvirtinti dokumentą. Kitu atveju darbo eigos tęsti negalima. Pvz., Sam pateikė 15 000 JAV dolerių išlaidų ataskaitą. Šiuo metu išlaidų ataskaita yra priskirta Sue, Jo ir Bill. Jei Sue ir Joe dokumentą patvirtina, o Bill jį atmeta, dokumentas yra atmetamas ir siunčiamas atgal Sam. Jei Sue, Jo ir Bill visi dokumentą patvirtina, jis siunčiamas Ann patvirtinti.

## <a name="specify-when-the-approval-step-is-required"></a>Nurodymas, kada būtinas patvirtinimo veiksmas
Galite nurodyti, kada būtinas patvirtinimo veiksmas. Patvirtinimo veiksmas gali būti reikalingas visada arba tik jei patenkinamos konkrečios sąlygos.

### <a name="the-approval-step-is-always-required"></a>Patvirtinimo veiksmas reikalingas visada

Jei patvirtinimo veiksmas reikalingas visada, atlikite šiuos veiksmus.

1.  Kairiojoje srityje spustelėkite **Sąlyga**.
2.  Pasirinkite pasirinktį **Visada vykdyti šį veiksmą**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Patvirtinimo veiksmas reikalingas tam tikromis aplinkybėmis

Patvirtinimo veiksmas, kurį konfigūruojate, gali būti reikalingas tik jei patenkinamos konkrečios sąlygos. Pavyzdžiui, jei konfigūruojate pirkimo paraiškos darbo eigos patvirtinimo veiksmą, galite norėti, kad patvirtinimo veiksmas būtų vykdomas tik tada, kai pirkimo paraiškos suma yra didesnė kaip 10 000 JAV dolerių. Atlikite tolesnius veiksmus, norėdami nurodyti, kada reikalingas patvirtinimo veiksmas.

1.  Kairiojoje srityje spustelėkite **Sąlyga**.
2.  Pasirinkite pasirinktį **Vykdyti šį veiksmą tik tada, kai įvykdytos nurodytos sąlygos**.
3.  Įveskite sąlygą
4.  Įveskite visas reikalingas papildomas sąlygas.
5.  Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.
    1.  Spustelėkite **Išbandyti**.
    2.  Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą.
    3.  Spustelėkite **Išbandyti**. Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.
    4.  Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Nurodymas, kokie veiksmai turi būti vykdomi, kai dokumentas yra vėluojantis
Jei per skirtąjį laiką vartotojas nesiims veiksmų su dokumentu, dokumentas laikomas vėluojančiu. Vėluojantį dokumentą galima perskirti arba automatiškai priskirti kitam vartotojui patvirtinti. Atlikite tolesnius veiksmus, kad perskirtumėte dokumentą, jei jis vėluoja.

1.  Kairiojoje srityje spustelėkite **Perskyrimas**.
2.  Pasirinkite žymės langelį **Naudoti perskyrimo maršrutą**, norėdami kurti perskyrimo maršrutą. Sistema automatiškai priskirs dokumentą perskyrimo sąraše pateiktiems vartotojams. Pavyzdžiui, tolesnėje lentelėje pateikiamas perskyrimo maršrutas.
    | Seka | Perskyrimo maršrutas      |
    |----------|----------------------|
    | 1        | Priskirti: Donna     |
    | 2        | Priskirti: Erin      |
    | 3        | Galutinis veiksmas: atmesti |

    Tokiu atveju, sistema priskirs vėluojantį dokumentą Donna. Jei Donna per skirtąjį laiką nesureaguos, sistema priskirs dokumentą Erin. Jei Erin per skirtąjį laiką nesureaguos, sistema dokumentą atmes.
3.  Norėdami vartotoją įtraukti į perskyrimo maršrutą, spustelėkite **Įtraukti perskyrimą**. Skirtuke **Priskyrimo tipas** pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 4 veiksmą, atlikite papildomus tos parinkties veiksmus.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Parinktis</th>
    <th>Vartotojai, kuriems perskiriamas dokumentas</th>
    <th>Papildomi veiksmai</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarchija</td>
    <td>Konkrečios organizacijos hierarchijos vartotojai</td>
    <td><ol>
    <li>Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite perskirti dokumentą.</li>
    <li>Sistema turi iš hierarchijos nuskaityti vartotojų vardus. Šie vardai nurodo vartotojus, kuriems galima perskirti dokumentą. Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką. <ol>
    <li>Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</li>
    <li>Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>. Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</li>
    </ol></li>
    <li>Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams dokumentas turėtų būti perskirtas. <ul>
    <li><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – dokumentas perskiriamas visiems vartotojams diapazone.</li>
    <li><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – dokumentas perskiriamas tik paskutiniam vartotojui diapazone.</li>
    <li><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – dokumentas neperskiriamas jokiems diapazono vartotojams, kurie atitinka tam tikrą sąlygą. Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Darbo eigos vartotojas</td>
    <td>Dabartinės darbo eigos vartotojai</td>
    <td><ul>
    <li>Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Vartotojas</td>
    <td>Konkretūs „Dynamics 365 for Operations“ vartotojai</td>
    <td><ol>
    <li>Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</li>
    <li>Skirtukas <strong>Galimi vartotojai</strong> apima visus „Dynamics 365 for Operations“ vartotojus. Pasirinkite, kuriems vartotojams norite perskirti dokumentą, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek laiko vartotojas turi imtis veiksmų arba reaguoti į dokumentus. Pasirinkite vieną iš toliau pateiktų pasirinkčių:
    -   **Valandos** – įveskite valandų, per kurias vartotojas turi reaguoti, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    -   **Dienos** – įveskite dienų, per kurias vartotojas turi reaguoti, skaičių. Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.
    -   **Savaitės** – įveskite savaičių, per kurias vartotojas turi reaguoti, skaičių.
    -   **Mėnesiai** – pasirinkite dieną ir savaitę, iki kurios vartotojas turi reaguoti. Pavyzdžiui, galbūt norite, kad vartotojas atsakytų iki trečiosios mėnesio savaitės penktadienio.
    -   **Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi reaguoti. Pavyzdžiui, galbūt norite, kad vartotojas atsakytų iki trečiosios gruodžio mėn. savaitės penktadienio.

5.  Pakartokite 3 ir 4 veiksmus su kiekvienu vartotoju, kuris turėtų būti įtrauktas į perskyrimo maršrutą. Galite keisti vartotojų tvarką.
6.  Jei perskyrimo maršrute esantys vartotojai per skirtąjį laiką nesureaguoja, sistema atliks veiksmą su dokumentu automatiškai. Norėdami nurodyti veiksmą, kurį sistema atliks, pasirinkite eilutę **Veiksmas** ir tada skirtuke **Pabaigos veiksmas** pasirinkite veiksmą.





