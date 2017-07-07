---
title: "Pirkimo išlaidų analizės „Power BI“ turinys"
description: "Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turiniui kurti."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: daba17aed7e6cc475a16d6100c5c99ee747ca048
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Pirkimo išlaidų analizės „Power BI“ turinys

[!include[banner](../includes/banner.md)]

Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**. Joje paaiškinama, kaip pasiekti „Power BI“ ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, kurie naudojami turiniui kurti.

## <a name="overview"></a>Apžvalga

„Power BI‟ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti stebėti pirkimo išlaidas. Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.

-   Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)
-   Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)

Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą. Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai. Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas. Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos. Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
Jei naudojate „Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimą su 2017 m. naujinimu, „Power BI‟ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** > **Užklausos ir ataskaitos** > **Pirkimo našumo analizė** > **Pirkimo ir išlaidų analizė**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
„Power BI‟ turinio pakete **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės Toliau pateikiamoje lentelėje apžvelgiamos vizualizacijos.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Ataskaitų puslapis</th>
<th>Diagramos</th>
<th>Išklotinės</th>
</tr>
</thead>
<tbody>
<tr class="odd">
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
<tr class="even">
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
<tr class="odd">
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
<tr class="even">
<td>Pirkimas pagal tiekėjo vietą</td>
<td><ul>
<li>Pirkimas pagal miestą</li>
<li>Pirkimo YOY augimas %</li>
<li>Pirkimas pagal šalį</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Pirkimo išlaidų analizė pagal laiką</td>
<td><ul>
<li>Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</li>
<li>Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
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

## <a name="extending-the-power-bi-content"></a>„Power BI“ turinio išplėtimas
Naudodami turinio paketus, kurie pateikiami „Microsoft Dynamics Lifecycle Services“ (LCS), žmonėms, kurie neprisijungia prie „Microsoft Dynamics 365“ galite pateikti didžiąją analizę. Galite keisti šiuos turinio paketus, kad į juos įtrauktumėte kitas ataskaitas arba vaizdinius, o po to paskelbti turinio paketus savo Power BI.com nuomotojui analizei. 

„Power BI“ turinį **Pirkimo išlaidų analizė** galite rasti LCS bibliotekoje Bendrai naudojamas turtas. Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md). Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).

Įsitikinkite, kad atsisiunčiate tą turinį **Pirkimo išlaidų analizė**, kuris taikomas jūsų naudojamai „Dynamics 365‟ versijai.

> [!NOTE]
> Jei naudojate „Microsoft Dynamics 365 for Operations‟ 1611 versiją, norint naudoti šį „Power BI‟ turinį būtina įdiegti KB 4011327. Prisijungę prie LCS, KB galite pasiekti adresu https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="data-model-and-entities"></a>Duomenų modelis ir objektai
Tolesniais duomenimis pildomi „Power BI‟ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. temoje [„Power BI‟ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys. Norint perkelti kubo agreguotus matavimo vienetus į objekto parduotuvę, reikia padaryti juos įdiegiamus. Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje ([„Power BI“ integravimo su objektų saugykla apžvalga](power-bi-integration-entity-store.md)). Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.

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

