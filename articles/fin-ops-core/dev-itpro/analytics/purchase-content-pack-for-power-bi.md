---
title: „Power BI“ turinys Pirkimo išlaidų analizė
description: Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5914abaafab509e278d7a85441928feddb0b5164
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093447"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>„Power BI“ turinys Pirkimo išlaidų analizė

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti sekti pirkimo išlaidas. Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.

- Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)
- Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)

Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą. Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai. Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas. Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos. Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** \> **Užklausos ir ataskaitos** \> **Pirkimo našumo analizė** \> **Pirkimo ir išlaidų analizė**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
„Power BI“ turinyje **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės 

Toliau pateikiamuose skyriuose apžvelgiamos vizualizacijos.

### <a name="purchase-by-vendor-report-page"></a>Pirkimo pagal tiekėjo ataskaitą puslapis
**Diagramos**
- 10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)
- Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)
- Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)
- Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)

**Išklotinės**
- Iš viso pirkimų
- YOY pirkimo augimas
- Bendras # tiekėjų skaičius
- Bendras # aktyvių tiekėjų skaičius

**Pavyzdys**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Pirkimo pagal produkto ataskaitą puslapis

**Diagramos**
- Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)
- Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)
- 10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)

**Išklotinės**
- Iš viso # produktų</li>
- Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų
- Produktų, sudarančių 80 % pirkimo, skaičius

**Pavyzdys**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Pirkimo pagal laikotarpio ataskaitą puslapis
Šiame puslapyje pateikiami pirkimai šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.

**Diagramos** 
- Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)
- Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)
- Bendras pirkimo YOY augimas (stulpelinė diagrama)
- Įsigijimo išrašas (matrica)

**Išklotinės**
- YOY pirkimo augimas
- YOY pirkimo augimas %

**Pavyzdys**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Pirkimo pagal vietos ataskaitą puslapis

**Diagramos**
- Pirkimas pagal miestą
- Pirkimo YOY augimas %
- Pirkimas pagal šalį

**Pavyzdys**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Pirkimo išlaidų analizės pagal laiką ataskaitos puslapis

**Diagramos** 
- Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)
- Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)

**Pavyzdys**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Pirkimo išlaidų analizės pagal tiekėją ataskaitos puslapis

**Diagramos** 
- 10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)
- 10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs
- 10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs

**Pavyzdys** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Duomenų modelis ir objektai
Tolesniais duomenimis pildomi „Power BI“ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys. Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus. Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje [Power BI integravimas su objektų saugykla](power-bi-integration-entity-store.md). Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.

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
