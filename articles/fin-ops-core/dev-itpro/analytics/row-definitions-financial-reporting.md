---
title: Finansinių ataskaitų dizaino įrankio eilučių aprašai
description: Eilutės aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo kiekvienos finansinės ataskaitos eilutės turinį.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom:
- "68873"
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.form: FinancialReports
ms.openlocfilehash: a60e66c372d85cc05219eaa17b7924aca5f3f337
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206325"
---
# <a name="row-definitions-in-financial-report-designer"></a>Finansinių ataskaitų dizaino įrankio eilučių aprašai

[!include [banner](../includes/banner.md)]

Eilutės aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo kiekvienos finansinės ataskaitos eilutės turinį. Eilutės aprašą galima derinti su stulpelių aprašais, ataskaitų medžio aprašais ir ataskaitų aprašais, taip sukuriant kūrimo blokų grupę, kurią gali naudoti kelios įmonės.

## <a name="create-a-row-definition"></a>Eilutės aprašo kūrimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Eilučių aprašai**.
2. Meniu **Failas** spustelėkite **Naujas**, tada spustelėkite **Eilutės aprašas**. Daugiau informacijos apie kiekvieno langelio turinį rasite dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Eilutės apibrėžimo atidarymas
1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Eilučių aprašai**.
2. Dukart spustelėkite norimo atidaryti eilutės apibrėžimo pavadinimą.
3. Norėdami peržiūrėti kūrimo blokus, susietus su eilutės apibrėžimu, dešiniuoju pelės klavišu spustelėkite eilutės apibrėžimą, tada pasirinkite **Susiejimai**.

## <a name="contents-of-a-row-definition"></a>Eilutės apibrėžimo turinys
Eilutės apraše gali būti iki 20 000 finansinės dimensijos eilučių ir jame gali būti pateikiama tolesnė informacija.

- Aprašomasis tekstas, suteikiantis ataskaitai reikšmę, kai sukuriamos skyriaus antraštės, eilutės ir tarpai, pavyzdžiui, **Grynieji pinigai** arba **Visos įplaukos**.
- Saitai su finansiniais duomenimis, kurie gali apimti dimensijų reikšmes į Microsoft Dynamics "365 Finance"

    > [!NOTE]
    > Galite nustatyti, kad kiekvieną kartą generuojant ataskaitą eilučių aprašas imtų duomenis iš finansinių dimensijų.

- Eilučių bendrosios sumos ir formulės, kurios pagrįstos susietais finansiniais duomenimis

Paprastai kiekvienoje eilutės apibrėžimo eilutėje yra vieno iš šių tipų informaciją:

- Saitai į finansinių dimensijų sistemą
- Bendrosios sumos arba skaičiavimai pagal duomenis
- Formatavimas

Informaciją įvesti į eilutės aprašą galima dviem būdais.

- Patiems įvesti eilutės informaciją į naują eilutės aprašą. Daugiau informacijos rasite dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).
- Naudojant ataskaitų dizaino įrankį gauti eilutės informaciją tiesiogiai iš finansinių dimensijų. Norėdami daugiau informacijos, žr. skyrių „Susijusios formulės / eilutės / vienetai“ dalyje [Eilutės apibrėžimo langelių keitimas](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Dimensijų įtraukimas į eilutės apibrėžimą
Dimensija yra duomenų ir reikšmių sankirta. Ataskaitų dizaino įrankyje galite grupuoti duomenis ir reikšmes. Tada galite išsamiau klasifikuoti ir analizuoti operacijas. Galite naudoti dialogo langą **Eilučių įterpimas iš dimensijų** ir vienu metu į eilutės apibrėžimą įtraukti kelias eilutes. Dialogo lange rodoma po vieną kiekvienos dimensijos stulpelį. Tolesnėje lentelėje nurodyta, kokią informaciją galite nurodyti kiekvienoje dimensijoje.

| Parinktis                | Prekės/Paslaugos pavadinimas |
|-----------------------|-------------|
| Dimensija             | Modelį, kuris identifikuoja į eilutės apibrėžimą norimą įtraukti dimensiją. Šiame modelyje kiekvienai dimensijų padėčiai yra po vieną ampersandą (&) arba skaičiaus ženklą (\#). Paprastai dimensijai Pagrindinė sąskaita naudojami visi konjunktūros ženklai, o kitoms dimensijoms naudojami visi skaičių ženklai. |
| Dimensijos diapazono pradžia | Pirmoji šios dimensijos vertė, įtrauktina į eilutės aprašą. |
| Dimensijos diapazono pabaiga   | Į eilutės apibrėžimą norima įtraukti paskutinė šios dimensijos reikšmė. |

Norėdami į eilutės aprašą įtraukti dimensijų, atlikite toliau nurodytus veiksmus.

1. Ataskaitų dizaino įrankyje spustelėkite **Eilučių aprašai**, tada atidarykite norimą keisti eilutės aprašą.
2. Meniu **Redaguoti** spustelėkite **Įterpti eilutes iš dimensijų**.
3. Eilutės **Dimensijos** dialogo lange **Įterpti eilutes iš dimensijų** pasirinkite į eilutės aprašą norimą perkelti dimensijos langelį, tada spustelėkite **Visi &&&**.
4. Norėdami apriboti eilutės aprašą iki kelių dimensijos reikšmių, langelyje **Dimensijos intervalo pradžia** įveskite pradžios dimensijos reikšmę, tada langelyje **Dimensijos intervalo pabaiga** įveskite pabaigos dimensijos reikšmę. Norėdami įtraukti visas pasirinktos dimensijos vertes palikite šiuos langelius tuščius.

    > [!NOTE]
    > Pakaitos simboliai (\* arba ?), esantys dimensijų intervaluose, gali nepateikti visų pageidaujamų rezultatų, atsižvelgiant į tai, kaip ERP duomenų bazė sugretina duomenis.

5. Lauke **Pradžios eilutės kodas** nurodykite pirmos dimensijos reikšmės eilutės kodą, kuris turėtų būti įtraukiamas į eilutės aprašą.
6. Lauke **Didinti kiekvieną eilutę** nurodykite tarpą tarp vienas paskui kitą einančių eilutės kodų.. Pvz., jei pirmos eilutės kodas yra 100, o padidinimo vertė yra 30, pirmų naujų eilučių kodai yra 100, 130, 160, 190 ir 220. Naudokite padidinimo vertę, kuria sukuriamas tarpas naujiems formatams ir formulių eilutėms įterpti.
7. Spustelėkite **GERAI**. Eilutės apraše kiekvienai pasirinktai dimensijos reikšmei įtraukiama viena eilutė.

## <a name="adjust-rounding-in-a-row-definition"></a>Koreguoti eilutės apibrėžimo apvalinimą
Jei turite balansą, kuriame sumos suapvalintos, bendrosios sumos į balansą gali nepatekti. Pavyzdžiui, taip gali atsitikti, jei balanso ataskaitoje naudojate apvalinimo parinktį, o ataskaitos apraše taip pat nurodomas apvalinimas. Norėdami subalansuoti balansų sumas, eilutės apraše galite naudoti parinktį **Apvalinimo koregavimas**. Apvalinimą galite išjungti arba modifikuoti ataskaitos aprašo skirtuke **Parametrai**. Toliau pateikiamoje lentelėje parodyta, kaip apvalinamos sumos. Šioje lentelėje įjungus apvalinimą eilučių 100 ir 200 sumos skiriasi.

| Eilutės kodas | Sumos be apvalinimo | Sumos su apvalinimu iki tūkstančių |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Bendroji suma    | 7,300                    | 8                                       |

Norėdami koreguoti balanso apvalinimą, atlikite toliau nurodytus veiksmus.

1. Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2. Meniu **Redaguoti** spustelėkite **Apvalinimo koregavimas**.
3. Dialogo lange **Apvalinimo koregavimai** įveskite šias reikšmes:

    - **Apvalinimo koregavimo eilutė** – eilutės, kuri bus pakoreguota norint subalansuoti balansą, kodas.
    - **Viso turto eilutė** – balanso eilutės, kurioje nurodytas bendras turtas, kodas.
    - **Visų įsipareigojimų ir kapitalo eilutė** – balanso eilutės, kurioje nurodyti visi įsipareigojimai ir kapitalas, kodas.
    - **Koregavimo sumos riba** – teigiamu sveikuoju skaičiumi išreikšta automatinių koregavimų riba. Ši suma palyginama su faktinės apvalinimo paklaidos absoliučiąja verte.

    > [!NOTE]
    > Eilučių kodai turi būti susieti su finansiniais duomenimis. Kitaip tariant, eilutės langelyje **Saitas su finansinėmis dimensijomis** turi būti nurodyta dimensijos vertė. **Nepateikite** nuorodos į aprašymo (**DESC**), apskaičiuotą (**CALC**) arba susumuotą (**TOT**) eilutę.

Dabar jūsų balanso sumos įjungus apvalinimą bus tolygiai subalansuotos.

> [!NOTE]
> Koregavimo limitas taikomas atsižvelgiant į parinktį **Apvalinimo tikslumas**, nustatomą ataskaitos aprašui. Pavyzdžiui, jei pasirenkate apvalinti savo ataskaitą iki tūkstančių ir lauke **Koregavimo sumos apribojimas** įvedate **2**, lauke **Apvalinimo koregavimo eilutė** nurodytą reikšmę padidinus arba sumažinus daugiau negu 2 000 rodomas įspėjantis pranešimas.

## <a name="format-row-and-column-text"></a>Eilutės ir stulpelio teksto formatavimas
Galite keisti savo ataskaitų išvaizdą pakeisdami šriftus ir formatuodami tekstą. Toliau nurodomuose skyriuose paaiškinama, kaip formatuoti ataskaitos eilučių ir stulpelių išvaizdą.

### <a name="manage-font-styles"></a>Tvarkyti šrifto stilius

Galite kurti ir modifikuoti ataskaitos šrifto stilius. Tada galite taikyti šiuos stilius dokumentui arba konkrečiai ataskaitos eilutei ar stulpeliui.

<table>
<tbody>
<tr>
<td><strong>Kurti šrifto stilių</strong></td>
<td>
<ol>
<li>Ataskaitos dizaino įrankio meniu <strong>Formatas </strong>spustelėkite <strong>Stiliai ir formatavimas</strong>.</li>
<li>Dialogo lange <strong>Stiliai ir formatavimas</strong> spustelėkite <strong>Nauja</strong>, tada įveskite unikalų naujojo stiliaus pavadinimą.</li>
<li>Pasirinkite šrifto parinktis, tada spustelėkite <strong>Gerai</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Šrifto stiliaus keitimas</strong></td>
<td>
<ol>
<li>Ataskaitos dizaino įrankio meniu <strong>Formatas </strong>spustelėkite <strong>Stiliai ir formatavimas</strong>.</li>
<li>Dialogo lange <strong>Stiliai ir formatavimas</strong> pasirinkite stilių, kurį norite keisti, tada spustelėkite <strong>Modifikuoti</strong>.</li>
<li>Pasirinkite šrifto parinktis, tada spustelėkite <strong>Gerai</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Taikyti šrifto stilių</strong></td>
<td>
<ol>
<li>Ataskaitų dizaino įrankio apraše, stulpelio apraše arba antraštėse ir poraštėse pasirinkite vieną ar kelis langelius.</li>
<li>Įrankių juostos sąraše <strong>Stilius</strong> pasirinkite šrifto stilių.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Formatuoti eilutės tekstą

Eilutės apraše nurodytas formatavimas perrašo stulpelio apraše ir ataskaitos apraše nurodytą formatavimą. Galite keisti teksto formatą, naudodami formatavimo įrankių juostos valdiklius. Šie valdikliai yra standartiniai „Microsoft Windows“ valdikliai.

1. Naudodami ataskaitų dizaino įrankį atidarykite norimą modifikuoti eilučių aprašą.
2. Pažymėkite norimus formatuoti langelius. Norėdami pažymėti kelis langelius, laikykite nuspaudę klavišą Ctrl ir pasirinkite langelį.
3. Norėdami taikyti, spustelėkite įrankių juostos formato mygtuką. Pavyzdžiui, norėdami įtraukti eilutę, pasirinkite eilutę, o tada spustelėkite **Padidinti įtrauką** ![Padidinti įtrauką.](media/indent.gif "Didinti įtrauką") įrankių juostoje.

### <a name="adjust-columns-while-you-design-reports"></a>Koreguoti stulpelius, kol kuriamos ataskaitos

Kad būtų lengviau peržiūrėti stulpelius, su kuriais dirbate eilutės apraše, galite koreguoti stulpelių plotį ir slėpti (sumažinti) arba rodyti stulpelius peržiūros srityje. Atlikti keitimai turi įtakos tik stulpelių vaizdui ekrane. Jie neturi įtakos ataskaitų stulpelių formatavimui.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Stulpelio pločio keitimas peržiūros srityje

1. Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2. Meniu **Formatas** pasirinkite **Stulpelio plotis**.
3. Dialogo lange **Stulpelio plotis** įveskite reikšmę ir tada spustelėkite **Gerai**. Stulpelio plotį pakeisti taip pat galite vilkdami stulpelio antraštės langelio dešiniąją kraštinę.

### <a name="hide-columns-in-the-view-pane"></a>Stulpelių slėpimas peržiūros rodinyje

1. Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2. Pasirinkite norimus minimizuoti stulpelius.
3. Spustelėkite dešinįjį pelės mygtuką, tada spustelėkite **Slėpti**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Visų paslėptų stulpelių rodymas peržiūros srityje

1. Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2. Dešiniuoju pelės mygtuku spustelėkite sumažintą stulpelį, kurį norite rodyti, tada spustelėkite **Nebeslėpti**.


## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
