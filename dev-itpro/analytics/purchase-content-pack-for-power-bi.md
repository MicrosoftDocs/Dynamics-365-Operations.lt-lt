---
title: "Pirkimą praleisti Power BI turinio analizė"
description: "Šioje temoje aprašoma, kas yra αtrauktas pirkimą praleisti analizės turinio paketą, skirtą &quot;Microsoft&quot; Power BI. Jis paaiškina, kaip pasiekti ataskaitas, kurios įtraukiamos į turinio paketą, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie yra naudojami kurti turinio paketas."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Pirkimą praleisti Power BI turinio analizė

Šioje temoje aprašoma, kas yra αtrauktas pirkimą praleisti analizės turinio paketą, skirtą "Microsoft" Power BI. Jis paaiškina, kaip pasiekti ataskaitas, kurios įtraukiamos į turinio paketą, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie yra naudojami kurti turinio paketas.

<a name="overview"></a>Apžvalga
--------

Pirkimą praleisti analizės turinio paketą, skirtą "Microsoft" Power BI buvo sukurta pirkimo vadovai ir vadybininkai, kurie yra atsakingi už biudžetų. Ji sukurta siekiant padėti joms užmesti akį į pirkimo išlaidų. Ji naudoja pirkimo sandorio duomenis iš Microsoft Dynamics 365 operacijoms ir skiria ir bendra Rodyti skaičių visos įmonės pirkimo ir pirkimo iš tiekėjo ir produkto išlaidų išklotinę. Ataskaitose pabrėžiama pasikeitimai pirkimo išlaidų per tam tikrą laiką. Todėl galima būtų jais įspėjimo vadovams apie teigiamus ir neigiamus išlaidų tendencijas atskirų tiekėjų. Diagramose pirkimo išlaidų skirtingų pirkimų kategorijas ir tiekėjų grupes. Kategorijos ir regiono vadybininkais gali būti naudinga naudoti šias diagramas, padėti nustatyti pokyčius išlaidų elgesys. Turinio paketas pirkimo vadovai ir vadybininkai, kurie yra atsakingi už biudžetų Panagrinėkime pirkimo išlaidų vienu iš šių būdų:

-   Metų pradžios pirkimo (pagal tiekėjų grupę ir atskirus tiekėjus, pirkimų kategorijos ir atskirų produktų ir tiekėjo vietą)
-   Metais per metus pirkimo kaitos (iš tiekėjų grupės ir pirkimų kategorija)

## <a name="accessing-the-content-pack"></a>Prieiga prie turinio paketas
Pirkimą praleisti analizės turinio paketas skelbiamas įgyvendinant turtu Microsoft Dynamics gyvavimo ciklo paslaugų (LCS) ir gali būti prieinama iš Microsoft Dynamics 365 operacijoms. Daugiau informacijos apie tai, kaip pasiekti ir atidaryti Power BI ataskaitų, rasite [LKD iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Rodikliai, kurie yra įtraukti į turinio paketas
Pirkimą praleisti turinio paketą sudaro ataskaitą, kuri susideda iš tam tikrų rodiklių analizė. Šių rodiklių yra ryškinamos diagramas, plytelės ir lenteles. Šioje lentelėje apžvelgiami vizualizacijos turinio paketas.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Ataskaitų puslapio</th>
<th>Diagramos</th>
<th>Plytelės</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pirkti iš tiekėjo</td>
<td><ul>
<li>10 geriausių pardavėjų iš pirkimo (sudėtinė Juostinė diagrama)</li>
<li>Iš viso pirkimus pagal tiekėją grupuoti / šalis / pavadinimas (skritulinę diagramą)</li>
<li>Pirkimus pagal tiekėją grupuoti / šalis / pavadinimas (stulpelinė diagrama)</li>
<li>Vidutinis pirkimus pagal tiekėją grupuoti / šalis / pavadinimas (stulpelinė diagrama)</li>
</ul></td>
<td><ul>
<li>Iš viso pirkimų</li>
<li>YOY pirkimo augimo</li>
<li>Iš viso # pardavėjai</li>
<li>Iš viso aktyvių pardavėjų #</li>
</ul></td>
</tr>
<tr class="even">
<td>Įsigyti produktą</td>
<td><ul>
<li>Pirkimų pagal pirkimų kategoriją / produkto pavadinimas (stulpelinė diagrama)</li>
<li>Iš viso pirkimo pagal viešųjų pirkimų kategoriją / produkto pavadinimas (skritulinę diagramą)</li>
<li>10 geriausių produktų pirkimo (sudėtinė Juostinė diagrama)</li>
</ul></td>
<td><ul>
<li>Iš viso # produktų</li>
<li>Aktyvus iš viso procentas visų # produktų</li>
<li>Produktus, kurie sudaro apie 80 % pirkimo numeris</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pirkimo laikotarpis *</td>
<td><ul>
<li>Pirkti pagal mėnesį / dieną (stulpelinė diagrama)</li>
<li>Kaupiamasis pirkimo YOY dispersija (krioklys diagramos)</li>
<li>Bendra pirkimo YOY augimo (stulpelinė diagrama)</li>
<li>Viešųjų pirkimų ataskaita (matrica)</li>
</ul></td>
<td><ul>
<li>YOY pirkimo augimo</li>
<li>YOY pirkimo augimo %</li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkti iš tiekėjo vietą</td>
<td><ul>
<li>Pirkti pagal miestą</li>
<li>Pirkimo YOY augimo %</li>
<li>Pirkti pagal šalis</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Pirkimą praleisti analizės metu</td>
<td><ul>
<li>Pirkimo einamaisiais metais pagal mėnesį / dieną (linijinė diagrama)</li>
<li>Pirkti einamųjų ir praėjusių metų (eilučių ir stulpelių diagrama)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Pirkimą praleisti analizė pagal tiekėją</td>
<td><ul>
<li>Top 10 tiekėjo pirkimo % pirkimo (piltuvas)</li>
<li>Į viršų 10 tiekėjai, padidėjusios išlaidos YOY</li>
<li>Į viršų 10 tiekėjai, sumažėjo išlaidų YOY</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Pirkimo šiemet ir pernai, ir augimo viešojo pirkimo kategorija

## <a name="data-model-and-entities"></a>Duomenų modelis ir subjektai
Dinamika 365 operacijoms pirkimo ataskaitoje naudojami duomenys praleisti analizės turinio paketas. Šie duomenys yra vaizduojamas kaip bendra matavimų, kurie yra pastatytas įmonės parduotuvėje, kuri yra "Microsoft" SQL duomenų bazę, kuri yra optimizuota Google analytics. Daugiau informacijos apie įmonės parduotuvėje, rasite, [Power BI integracija su įmonės parduotuvėje dinamikai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) dienoraštyje. Bendra matavimų šio turinio Pack yra sutrumpinti bendrą matavimų, kuriais galėjote naudotis pirkimo kubo Microsoft Dynamics AX 2012 ir Microsoft Dynamics 365 operacijų 2012 R3. Į sceną kubo bendra matavimų įmonės parduotuvėje, jūs turite padaryti juos išskleidimo. Norėdami gauti daugiau informacijos, žiūrėkite procedūrą, sustojimo bendra matavimų įmonės parduotuvėje, [Power BI integracija su įmonės parduotuvėje dinamikai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) dienoraštyje. Šiuos pagrindinius bendrus matavimus galima gauti tiesiogiai iš SF eilutes subjektas ir yra naudojami kaip pagrindas turinio pack.

| Objektas        | Bendra atliekami pagrindiniai matavimai | Duomenų šaltinis Dynamics 365 operacijoms | Laukas              | aprašymas                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| SF eilutės | Pirkimas                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Suma, išreikšta apskaitos valiuta |

Ši lentelė rodo pagrindinių matmenų, apskaičiuojami turinio paketas iš SF eilutes subjektas.

| Mato vnt.               | Skaičiavimas                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Pirkimo einamųjų metų | Pirkimo einamųjų metų = SUM ('SF eilutės'\[pirkti\])                                            |
| Pirkti pernai    | Pirkti pernai = apskaičiuoti (suma ("SF eilutės"\[pirkimo\]), SAMEPERIODLASTYEAR (datos\[data\])) |
| YOY pirkimo augimo   | YOY pirkti augimo = \[pirkti einamųjų metų\] - \[pirkti pernai\]                            |

Pagrindiniai matmenys turinio paketas yra naudojamas kaip filtrų tenka bendra matavimų, taip, kad jūs galite pasiekti daugiau detalumo ir gilesnių analitinių įžvalgų.

| Objektas                 | Atributų pavyzdžiai                                |
|------------------------|-------------------------------------------------------|
| Tiekėjai                | Tiekėjų grupių, tiekėjo šalis ar regionus, tiekėjo pavadinimas |
| Produktai               | Gaminio numeris, produkto pavadinimas, prekės grupės pavadinimas        |
| Įsigijimo kategorijos | Pirkimų kategorija, pirkimų kategorijų pavadinimai      |
| Juridiniai subjektai         | Juridinio subjekto pavadinimas                                     |
| Datos                  | Datos, metų poslinkis                                    |

Pagal numatytuosius nustatymus turinio paketas rodo duomenų einamaisiais kalendoriniais metais. Tačiau galite pakeisti datos filtras filtrai skyriuje ataskaita. Taip pat galite keisti įmonės filtras.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)



