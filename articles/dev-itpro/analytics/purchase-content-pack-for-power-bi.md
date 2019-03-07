---
title: „Power BI“ turinys Pirkimo išlaidų analizė
description: Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turiniui kurti.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "313847"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>„Power BI“ turinys Pirkimo išlaidų analizė

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti stebėti pirkimo išlaidas. Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.

- Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)
- Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)

Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą. Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai. Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas. Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos. Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** \> **Užklausos ir ataskaitos** \> **Pirkimo našumo analizė** \> **Pirkimo ir išlaidų analizė**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
„Power BI“ turinyje **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės Toliau pateikiamoje lentelėje apžvelgiamos vizualizacijos.

<table>
<thead>
<tr>
<th>Ataskaitų puslapis</th>
<th>Diagramos</th>
<th>Išklotinės</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pirkimas pagal tiekėją</td>
<td><ul>
<li>10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)</li>
<li>Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)</li>
<li>Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</li>
<li>Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</li>
</ul></td>
<td><ul>
<li>Iš viso pirkimų</li>
<li>YOY pirkimo augimas</li>
<li>Bendras # tiekėjų skaičius</li>
<li>Bendras # aktyvių tiekėjų skaičius</li>
</ul></td>
</tr>
<tr>
<td>Pirkimas pagal produktą</td>
<td><ul>
<li>Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)</li>
<li>Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)</li>
<li>10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)</li>
</ul></td>
<td><ul>
<li>Iš viso # produktų</li>
<li>Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų</li>
<li>Produktų, sudarančių 80 % pirkimo, skaičius</li>
</ul></td>
</tr>
<tr>
<td>Pirkimas pagal laikotarpį*</td>
<td><ul>
<li>Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)</li>
<li>Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)</li>
<li>Bendras pirkimo YOY augimas (stulpelinė diagrama)</li>
<li>Įsigijimo išrašas (matrica)</li>
</ul></td>
<td><ul>
<li>YOY pirkimo augimas</li>
<li>YOY pirkimo augimas %</li>
</ul></td>
</tr>
<tr>
<td>Pirkimas pagal tiekėjo vietą</td>
<td><ul>
<li>Pirkimas pagal miestą</li>
<li>Pirkimo YOY augimas %</li>
<li>Pirkimas pagal šalį</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Pirkimo išlaidų analizė pagal laiką</td>
<td><ul>
<li>Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</li>
<li>Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Pirkimo išlaidų analizė pagal tiekėją</td>
<td><ul>
<li>10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)</li>
<li>10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs</li>
<li>10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Pirkimas šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.

## <a name="data-model-and-entities"></a>Duomenų modelis ir objektai
Tolesniais duomenimis pildomi „Power BI“ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. temoje [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys. Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus. Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje [„Power BI“ integravimo su objektų saugykla apžvalga](power-bi-integration-entity-store.md). Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.

| Objektas        | Pagrindiniai agreguoti matavimo vienetai | Duomenų šaltinis                                 | Laukas              | aprašymas                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| SF eilutės | Pirkimas                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Suma, išreikšta apskaitos valiuta. |

Toliau pateiktoje lentelėje nurodomi pagrindiniai turinyje naudojami matavimo vienetai, apskaičiuojami pagal objektą Sąskaitos faktūros eilutės.

| Mato vnt.               | Skaičiavimas                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Pirkimas esamais metais | Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])                                            |
| Pirkimas pastaraisiais metais    | Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\])) |
| YOY pirkimo augimas   | YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]                            |

Šios pagrindinės turinio dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti daugiau detalumo ir gauti gilesnių analitinių įžvalgų.

| Objektas                 | Atributų pavyzdžiai                                |
|------------------------|-------------------------------------------------------|
| Tiekėjai                | Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas |
| Produktai               | Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas        |
| Įsigijimo kategorijos | Įsigijimo kategorija, įsigijimo kategorijų pavadinimai      |
| Juridiniai subjektai         | Juridinio subjekto pavadinimas                                     |
| Datos                  | Datos, metų poslinkis                                    |

Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys. Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti. Taip pat galite pakeisti įmonės filtrą.
