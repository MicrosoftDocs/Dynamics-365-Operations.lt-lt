---
title: "Finansinių ataskaitų dizaino įrankio eilučių aprašai"
description: "Eilutės aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo kiekvienos finansinės ataskaitos eilutės turinį. Eilutės aprašą galima derinti su stulpelių aprašais, ataskaitų medžio aprašais ir ataskaitų aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 6d4697af6f7467f25a461fae4e9320402f83b0e3
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017

---

# <a name="row-definitions-in-financial-report-designer"></a>Finansinių ataskaitų dizaino įrankio eilučių aprašai

[!include[banner](../includes/banner.md)]


Eilutės aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo kiekvienos finansinės ataskaitos eilutės turinį. Eilutės aprašą galima derinti su stulpelių aprašais, ataskaitų medžio aprašais ir ataskaitų aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės.

<a name="create-a-row-definition"></a>Sukurti eilutės apibrėžimą
-----------------------

1.  Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Eilučių aprašai**.
2.  Meniu **Failas** spustelėkite **Naujas**, tada spustelėkite **Eilutės aprašas**. Daugiau informacijos apie kiekvieno langelio turinį rasite dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Eilutės apibrėžimo atidarymas
1.  Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Eilučių aprašai**.
2.  Dukart spustelėkite norimo atidaryti eilutės apibrėžimo pavadinimą.
3.  Norėdami peržiūrėti kūrimo blokus, susietus su eilutės apibrėžimu, dešiniuoju pelės klavišu spustelėkite eilutės apibrėžimą, tada pasirinkite **Susiejimai**.

## <a name="contents-of-a-row-definition"></a> Eilutės apibrėžimo turinys
Eilutės apraše gali būti iki 20 000 finansinės dimensijos eilučių ir jame gali būti pateikiama tolesnė informacija.

-   Aprašomasis tekstas, suteikiantis ataskaitai reikšmę, kai sukuriamos skyriaus antraštės, eilutės ir tarpai, pavyzdžiui, **Grynieji pinigai** arba **Visos įplaukos**.
-   Saitai į finansinius duomenis, kurie gali apimti dimensijų reikšmes sprendime „Microsoft Dynamics 365 for Finance and Operations“ **Pastaba:** galite nustatyti, kad eilutės apibrėžtis duomenis gautų iš finansinių dimensijų sistemos kaskart, kai generuojama ataskaita.
-   Eilučių bendrosios sumos ir formulės, kurios pagrįstos susietais finansiniais duomenimis

Paprastai kiekvienoje eilutės apibrėžimo eilutėje yra vieno iš šių tipų informaciją:

-   Saitai į finansinių dimensijų sistemą
-   Bendrosios sumos arba skaičiavimai pagal duomenis
-   Formatavimas

Informaciją įvesti į eilutės aprašą galima dviem būdais.

-   Patiems įvesti eilutės informaciją į naują eilutės aprašą. Daugiau informacijos rasite dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).
-   Naudojant ataskaitų dizaino įrankį gauti eilutės informaciją tiesiogiai iš finansinių dimensijų. Norėdami daugiau informacijos, žr. skyrių „Susijusios formulės / eilutės / vienetai“ dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a> Dimensijų įtraukimas į eilutės apibrėžimą
Dimensija yra duomenų ir reikšmių sankirta. Ataskaitų dizaino įrankyje galite grupuoti duomenis ir reikšmes. Tada galite išsamiau klasifikuoti ir analizuoti operacijas. Galite naudoti dialogo langą **Eilučių įterpimas iš dimensijų** ir vienu metu į eilutės apibrėžimą įtraukti kelias eilutes. Dialogo lange rodoma po vieną kiekvienos dimensijos stulpelį. Tolesnėje lentelėje nurodyta, kokią informaciją galite nurodyti kiekvienoje dimensijoje.

| Parinktis                | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensija             | Modelį, kuris identifikuoja į eilutės apibrėžimą norimą įtraukti dimensiją. Šiame modelyje kiekvienai dimensijų padėčiai yra po vieną ampersandą (&) arba skaičiaus ženklą (\#). Paprastai dimensijai Pagrindinė sąskaita naudojami visi konjunktūros ženklai, o kitoms dimensijoms naudojami visi skaičių ženklai. |
| Dimensijos intervalo pradžia | Į eilutės apibrėžimą norima įtraukti pirmoji šios dimensijos reikšmė.                                                                                                                                                                                                                 |
| Dimensijos intervalo pabaiga   | Į eilutės apibrėžimą norima įtraukti paskutinė šios dimensijos reikšmė.                                                                                                                                                                                                                  |

Norėdami į eilutės aprašą įtraukti dimensijų, atlikite toliau nurodytus veiksmus.

1.  Ataskaitų dizaino įrankyje spustelėkite **Eilučių aprašai**, tada atidarykite norimą keisti eilutės aprašą.
2.  Meniu **Redaguoti** spustelėkite **Įterpti eilutes iš dimensijų**.
3.  Eilutės **Dimensijos** dialogo lange **Įterpti eilutes iš dimensijų** pasirinkite į eilutės aprašą norimą perkelti dimensijos langelį, tada spustelėkite **Visi &&&**.
4.  Norėdami apriboti eilutės aprašą iki kelių dimensijos reikšmių, langelyje **Dimensijos intervalo pradžia** įveskite pradžios dimensijos reikšmę, tada langelyje **Dimensijos intervalo pabaiga** įveskite pabaigos dimensijos reikšmę. Norėdami įtraukti visas pasirinktos dimensijos reikšmes, palikite šiuos langelius tuščius. **Pastaba:** naudojant pakaitos simbolius (\* arba ?) dimensijos intervaluose gali būti gaunami ne visi norimi rezultatai, priklausomai nuo to, kaip ERP duomenų bazė sujungia duomenis.
5.  Lauke **Pradžios eilutės kodas** nurodykite pirmos dimensijos reikšmės eilutės kodą, kuris turėtų būti įtraukiamas į eilutės aprašą.
6.  Lauke **Didinti kiekvieną eilutę** nurodykite tarpą tarp vienas paskui kitą einančių eilutės kodų.. Pvz., jei pirmos eilutės kodas yra 100, o padidinimo vertė yra 30, pirmų naujų eilučių kodai yra 100, 130, 160, 190 ir 220. Naudokite padidinimo vertę, kuria sukuriamas tarpas naujiems formatams ir formulių eilutėms įterpti.
7.  Spustelėkite **GERAI**. Eilutės apraše kiekvienai pasirinktai dimensijos reikšmei įtraukiama viena eilutė.

## <a name="adjust-rounding-in-a-row-definition"></a>Koreguoti eilutės apibrėžimo apvalinimą
Jei turite balansą, kuriame sumos suapvalintos, bendrosios sumos į balansą gali nepatekti. Pavyzdžiui, taip gali atsitikti, jei balanso ataskaitoje naudojate apvalinimo parinktį, o ataskaitos apraše taip pat nurodomas apvalinimas. Norėdami subalansuoti balansų sumas, eilutės apraše galite naudoti parinktį **Apvalinimo koregavimas**. Apvalinimą galite išjungti arba modifikuoti ataskaitos aprašo skirtuke **Parametrai**. Toliau pateikiamoje lentelėje parodyta, kaip apvalinamos sumos. Šioje lentelėje įjungus apvalinimą eilučių 100 ir 200 sumos skiriasi.

| Eilutės kodas | Sumos be apvalinimo | Sumos su apvalinimu iki tūkstančių |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Bendroji suma    | 7,300                    | 8                                       |

Norėdami koreguoti balanso apvalinimą, atlikite toliau nurodytus veiksmus.

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Meniu **Redaguoti** spustelėkite **Apvalinimo koregavimas**.
3.  Dialogo lange **Apvalinimo koregavimai** įveskite šias reikšmes:
    -   **Apvalinimo koregavimo eilutė** – eilutės, kuri bus pakoreguota norint subalansuoti balansą, kodas.
    -   **Viso turto eilutė** – balanso eilutės, kurioje nurodytas bendras turtas, kodas.
    -   **Visų įsipareigojimų ir kapitalo eilutė** – balanso eilutės, kurioje nurodyti visi įsipareigojimai ir kapitalas, kodas.
    -   **Koregavimo sumos riba** – teigiamu sveikuoju skaičiumi išreikšta automatinių koregavimų riba. Ši suma lyginama su faktinio apvalinimo skirtumo absoliučiąja reikšme.

    **Pastaba:** šie eilutės kodai turi būti susieti su finansiniais duomenimis. Kitaip tariant, eilutės dimensijos reikšmė turi būti nurodyta langelyje **Saitas su finansinėmis dimensijomis**. **Nepateikite** nuorodos į aprašymo (**DESC**), apskaičiuotą (**CALC**) arba susumuotą (**TOT**) eilutę.

Dabar jūsų balanso sumos įjungus apvalinimą bus tolygiai subalansuotos. **Pastaba:** koregavimo riba taikoma atsižvelgiant į nurodytą ataskaitos aprašo pasirinktį **Apvalinimo tikslumas**. Pavyzdžiui, jei pasirenkate apvalinti savo ataskaitą iki tūkstančių ir lauke **Koregavimo sumos apribojimas** įvedate **2**, lauke **Apvalinimo koregavimo eilutė** nurodytą reikšmę padidinus arba sumažinus daugiau negu 2 000 rodomas įspėjantis pranešimas.

## <a name="format-row-and-column-text"></a>Eilutės ir stulpelio teksto formatavimas
Galite keisti savo ataskaitų išvaizdą pakeisdami šriftus ir formatuodami tekstą. Toliau nurodomuose skyriuose paaiškinama, kaip formatuoti ataskaitos eilučių ir stulpelių išvaizdą.

### <a name="manage-font-styles"></a>Tvarkyti šrifto stilius

Galite kurti ir modifikuoti ataskaitos šrifto stilius. Tada galite taikyti šiuos stilius dokumentui arba konkrečiai ataskaitos eilutei ar stulpeliui.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Kurti šrifto stilių</td>
<td><ol>
<li>Ataskaitos dizaino įrankio meniu <strong>Formatas </strong>spustelėkite <strong>Stiliai ir formatavimas</strong>.</li>
<li>Dialogo lange <strong>Stiliai ir formatavimas</strong> spustelėkite <strong>Naujas</strong>, tada įveskite unikalų naujo stiliaus pavadinimą.</li>
<li>Pasirinkite šriftą, tada spustelėkite <strong>Gerai</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Modifikuoti šrifto stilių</td>
<td><ol>
<li>Ataskaitos dizaino įrankio meniu <strong>Formatas </strong>spustelėkite <strong>Stiliai ir formatavimas</strong>.</li>
<li>Dialogo lange <strong>Stiliai ir formatavimas</strong> pasirinkite norimą modifikuoti stilių, tada spustelėkite <strong>Modifikuoti</strong>.</li>
<li>Pasirinkite šriftą, tada spustelėkite <strong>Gerai</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Taikyti šrifto stilių</td>
<td><ol>
<li>Ataskaitų dizaino įrankio apraše, stulpelio apraše arba antraštėse ir poraštėse pasirinkite vieną ar kelis langelius.</li>
<li>Įrankių juostos sąraše <strong>Stilius</strong> pasirinkite šrifto stilių.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Formatuoti eilutės tekstą

Eilutės apraše nurodytas formatavimas perrašo stulpelio apraše ir ataskaitos apraše nurodytą formatavimą. Galite keisti teksto formatą, naudodami formatavimo įrankių juostos valdiklius. Šie valdikliai yra standartiniai „Microsoft Windows“ valdikliai.

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Pažymėkite norimus formatuoti langelius. Norėdami pažymėti kelis langelius, laikykite nuspaudę klavišą Ctrl ir pasirinkite langelį.
3.  Norėdami taikyti, spustelėkite įrankių juostos formato mygtuką. Pvz., norėdami įtraukti eilutę, pasirinkite eilutę, tada įrankių juostoje spustelėkite **Padidinti įtrauką** ![Padidinti įtrauką](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Padidinti įtrauką").

### <a name="adjust-columns-while-you-design-reports"></a>Koreguoti stulpelius, kol kuriamos ataskaitos

Kad būtų lengviau peržiūrėti stulpelius, su kuriais dirbate eilutės apraše, galite koreguoti stulpelių plotį ir slėpti (sumažinti) arba rodyti stulpelius peržiūros srityje. Atlikti keitimai turi įtakos tik stulpelių vaizdui ekrane. Jie neturi įtakos ataskaitų stulpelių formatavimui.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Stulpelio pločio keitimas peržiūros srityje

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Meniu **Formatas** pasirinkite **Stulpelio plotis**.
3.  Dialogo lange **Stulpelio plotis** įveskite reikšmę ir tada spustelėkite **Gerai**. Stulpelio plotį pakeisti taip pat galite vilkdami stulpelio antraštės langelio dešiniąją kraštinę.

### <a name="hide-columns-in-the-view-pane"></a>Stulpelių slėpimas peržiūros rodinyje

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Pasirinkite norimą sumažinti stulpelį arba stulpelius.
3.  Spustelėkite dešinįjį pelės mygtuką, tada spustelėkite **Slėpti**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Visų paslėptų stulpelių rodymas peržiūros srityje

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Dešiniuoju pelės mygtuku spustelėkite sumažintą stulpelį, kurį norite rodyti, tada spustelėkite **Nebeslėpti**.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Finansinės ataskaitos](financial-reporting-intro.md)




