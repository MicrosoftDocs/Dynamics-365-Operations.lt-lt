---
title: "Pirkimo išlaidų analizės „Power BI“ turinys"
description: "Šioje temoje paaiškinta, kas įtraukiama į pirkimo išlaidų analizės turinio paketą, skirtą „Microsoft Power BI“. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
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

# <a name="purchase-spend-analysis-power-bi-content"></a>Pirkimo išlaidų analizės „Power BI“ turinys

Šioje temoje paaiškinta, kas įtraukiama į pirkimo išlaidų analizės turinio paketą, skirtą „Microsoft Power BI“. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

<a name="overview"></a>Apžvalga
--------

„Microsoft Power BI“ skirtas pirkimo išlaidų analizės turinio paketas sukurtas pirkimo vadovams ir vadovams, kurie atsakingi už biudžetus. Jis sukurtas tam, kad padėtų jiems stebėti pirkimo išlaidas. Jame naudojami pirkimo operacijų duomenys iš „Microsoft Dynamics 365 for Operations“, pateikiamas ir sujungtas visos įmonės pirkimo skaičių rodinys, ir tiekėjo bei produkto pirkimo išlaidų paskirstymas. Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai. Todėl jas galima naudoti norint įspėti vadovus apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas. Diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos. Kategorijų ir regiono vadovams gali būti naudinga naudoti šias diagramas, kurios galėtų padėti nustatyti išlaidų elgesio pokyčius. Naudodami turinio paketą pirkimo vadovai ir vadovai, kurie atsakingi už biudžetus, gali išanalizuoti pirkimo išlaidas toliau nurodomais būdais.

-   Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)
-   Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)

## <a name="accessing-the-content-pack"></a>Prieiga prie turinio paketo
Pirkimo išlaidų analizės turinio paketas išleistas kaip „Microsoft Dynamics Lifecycle Services“ (LCS) diegimo išteklius ir yra pasiekiamas iš „Microsoft Dynamics 365 for Operations“. Išsamesnės informacijos apie tai, kaip pasiekti ir atidaryti „Power BI“ ataskaitas žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos metrikos
Pirkimo išlaidų analizės turinio pakete yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės Toliau pateiktoje lentelėje pateikiama turinio paketo vizualizacijų apžvalga.

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

## <a name="data-model-and-entities"></a>Duomenų modelis ir objektai
„Dynamics 365 for Operations“ duomenys naudojami pirkimo išlaidų analizės turinio pakete esančiai ataskaitai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objekto parduotuvėje, kuri yra „Microsoft SQL“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos apie objekto parduotuvę ieškokite tinklaraščio įraše [„Power BI“ integravimas su objekto parduotuve programoje „Dynamics“](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Agreguoti matavimo vienetai šiame turinio pakete yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Purchase Cube“ naudojant „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics 365 for Operations 2012 R3“, subrinkinys. Norint perkelti kubo agreguotus matavimo vienetus į objekto parduotuvę, reikia padaryti juos įdiegiamus. Išsamesnės informacijos žr. tinklaraščio įraše pateiktą procedūrą, kaip perkelti agreguotus matavimo vienetus į kitą vietą objekto parduotuvėje [„Power BI“ integravimas su objekto parduotuve programoje „Dynamics“](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Šiuos pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš sąskaitos faktūros eilučių objekto ir jie naudojami kaip turinio paketo pagrindas.

| Objektas        | Pagrindiniai agreguoti matavimo vienetai | „Dynamics 365 for Operations“ duomenų šaltinis | Laukas              | aprašymas                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| SF eilutės | Pirkimas                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Suma, išreikšta apskaitos valiuta |

Toliau pateiktoje lentelėje nurodomi pagrindiniai matavimo vienetai, kurie apskaičiuojami turinio pakete iš sąskaitos faktūros eilučių.

| Mato vnt.               | Skaičiavimas                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Pirkimas esamais metais | Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])                                            |
| Pirkimas pastaraisiais metais    | Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\])) |
| YOY pirkimo augimas   | YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]                            |

Šios pagrindinės turinio paketo dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams susegmentuoti, kad būtų galima pasiekti daugiau detalumo ir gilesnių analitinių įžvalgų.

| Objektas                 | Atributų pavyzdžiai                                |
|------------------------|-------------------------------------------------------|
| Tiekėjai                | Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas |
| Produktai               | Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas        |
| Įsigijimo kategorijos | Įsigijimo kategorija, įsigijimo kategorijų pavadinimai      |
| Juridiniai subjektai         | Juridinio subjekto pavadinimas                                     |
| Datos                  | Datos, metų poslinkis                                    |

Pagal numatytuosius parametrus turinio pakete rodomi esamų kalendorinių metų duomenys. Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti. Taip pat galite pakeisti įmonės filtrą.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)



