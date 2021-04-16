---
title: „Power BI“ turinys Praktikos vadovas
description: Šioje temoje paaiškinama, kas įtraukta į „Power BI“ turinį Praktikos vadovas.
author: KimANelson
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 77079a8013cb98acc5f36787ca10706c361736d3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753095"
---
# <a name="practice-manager-power-bi-content"></a>„Power BI“ turinys Praktikos vadovas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kas įtraukta į „Microsoft Power BI“ turinį **Praktikos vadovas**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Praktikos vadovas** sukurtas praktikos vadovams ir projektų vadovams. Jame pateikiamos pagrindinės metrikos, susijusios su organizacijos vykdomais projektais. Ataskaitų srityje pateikiama projektų ir susijusių klientų apžvalga. Ataskaitos lygio filtrą galima naudoti norint teikti konkrečių juridinių subjektų ataskaitas. Šis „Power BI“ turinys duomenis gauna iš projektų apskaitos sujungtų matavimo vienetų.

„Power BI“ turinys **Praktikos vadovas** apima penkis ataskaitų puslapius: vieną peržiūros puslapį ir keturis puslapius, kuriuose pateikiama informacija apie projektų išlaidas, įplaukas, gautos vertės valdymą ir valandų metrikas, suskirstytas įvairiose dimensijose.

Visos turinio sumos rodomos sistemos valiuta. Sistemos valiutą galite nustatyti puslapyje **Sistemos parametrai**.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

„Power BI“ turinys **Praktikos vadovas** rodomas darbo srityje **Projektų valdymas**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos

Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Praktikos vadovas** ataskaitų puslapyje.

| Ataskaitų puslapis       | Metrika |
|-------------------|---------|
| Projektų apžvalga | <ul><li>Sukurti projektai</li><li>Įvertinti projektai</li><li>Apdorojami projektai</li><li>Faktinės įplaukos pagal klientą</li><li>Biudžeto bruto marža pagal projektą</li><li>Gautos vertės valdymo apžvalga</li></ul> |
| Savikaina              | <ul><li>Faktinės ir biudžeto išlaidos pagal mėnesį</li><li>Faktinės ir biudžeto išlaidos pagal metus</li><li>Faktinės ir biudžeto išlaidos pagal kategoriją</li><li>Faktinės išlaidos pagal operacijos tipą</li></ul> |
| Įplaukos           | <ul><li>Faktinės įplaukos pagal mėnesį</li><li>Faktinės įplaukos pagal pašto kodą</li><li>Faktinės ir biudžeto įplaukos pagal kategoriją</li><li>Faktinės įplaukos pagal kliento pramonės šaką</li></ul> |
| EVM               | Išlaidų ir planavimo efektyvumo indeksas pagal projektą |
| Valandos             | <ul><li>Faktinių apmokėtinų išnaudotų valandų, faktinių apmokėtinų neefektyvių valandų ir biudžeto valandų palyginimas</li><li>Faktinių apmokėtinų išnaudotų valandų ir faktinių apmokėtinų neefektyvių valandų palyginimas pagal projektą</li><li>Faktinių apmokėtinų išnaudotų valandų ir faktinių apmokėtinų neefektyvių valandų palyginimas pagal išteklių</li><li>Faktinių apmokėtinų valandų tarifas pagal projektą</li><li>Faktinių apmokėtinų valandų tarifas pagal išteklių</li></ul> |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Taip pat galite naudoti funkciją Eksportuoti pagrindinius duomenis, norėdami eksportuoti vizualiai apibendrintus pagrindinius duomenis.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Tolesniais duomenimis pildomi „Power BI“ turinio **Praktikos vadovas** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Tolesniuose skyriuose aprašyti kiekviename objekte naudojami sujungti matavimo vienetai.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Objektas: ProjectAccountingCube\_ActualHourUtilization
**Duomenų šaltinis:** ProjEmplTrans

| Pagrindiniai sujungti matavimo vienetai      | Laukas                              | aprašymas |
|--------------------------------|------------------------------------|-------------|
| Faktinės apmokėtinos išnaudotos valandos | Sum(ActualUtilizationBillableRate) | Faktinių apmokėtinų išnaudotų valandų suma. |
| Faktinės apmokėtinos neefektyvios valandos   | Sum(ActualBurdenBillableRate)      | Visas faktinio neefektyvumo tarifas. |

### <a name="entity-projectaccountingcube_actuals"></a>Objektas: ProjectAccountingCube\_Actuals
**Duomenų šaltinis:** ProjTransPosting

| Pagrindiniai sujungti matavimo vienetai | Laukas              | aprašymas |
|---------------------------|--------------------|-------------|
| Faktinės įplaukos            | Sum(ActualRevenue) | Visų operacijų užregistruotų įplaukų suma. |
| Faktinės išlaidos               | Sum(ActualCost)    | Visų operacijų tipų užregistruotų išlaidų suma. |

### <a name="entity-projectaccountingcube_customer"></a>Objektas: ProjectAccountingCube\_Customer
**Duomenų šaltinis:** CustTable

| Pagrindiniai sujungti matavimo vienetai | Laukas                                             | aprašymas |
|---------------------------|---------------------------------------------------|-------------|
| Projektų skaičius        | COUNTA(ProjectAccountingCube\_Projects\[PROJECTS\]) | Galimų projektų skaičius. |

### <a name="entity-projectaccountingcube_forecasts"></a>Objektas: ProjectAccountingCube\_Forecasts
**Duomenų šaltinis:** ProjTransBudget

| Pagrindiniai sujungti matavimo vienetai | Laukas                  | aprašymas |
|---------------------------|------------------------|-------------|
| Biudžeto išlaidos               | Sum(BudgetCost)        | Visų operacijų tipų prognozuojamų išlaidų suma. |
| Biudžeto įplaukos            | Sum(BudgetRevenue)     | Prognozuojamų sukauptų įplaukų / įplaukų, kurių sąskaita faktūra išrašyta, suma. |
| Biudžeto bruto marža       | Sum(BudgetGrossMargin) | Skirtumas tarp visų prognozuojamų įplaukų sumos ir visų prognozuojamų išlaidų sumos. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Objektas: ProjectAccountingCube\_ProjectPlanCostsView
**Duomenų šaltinis:** projektas

| Pagrindiniai sujungti matavimo vienetai | Laukas                    | aprašymas |
|---------------------------|--------------------------|-------------|
| Suplanuotos išlaidos              | Sum(SumOfTotalCostPrice) | Visų projekto operacijų tipų su suplanuotomis užduotimis numatoma bendroji savikaina. |

### <a name="entity-projectaccountingcube_projects"></a>Objektas: ProjectAccountingCube\_Projects
**Duomenų šaltinis:** projektas

| Pagrindiniai sujungti matavimo vienetai    | Laukas | aprašymas |
|------------------------------|-------|-------------|
| Išlaidų efektyvumo indeksas       | ProjectAccountingCube\_Projects\[Earned value\] ÷ ProjectAccountingCube\_Projects\[atliktų užduočių faktinių išlaidų suma\] | Viso gautos vertės, padalytos iš visų faktinių išlaidų, skaičiavimas. |
| Planavimo efektyvumo indeksas   | ProjectAccountingCube\_Projects\[Earned value\] ÷ ProjectAccountingCube\_Projects\[atliktų užduočių suplanuotų išlaidų suma\] | Viso gautos vertės, padalytos iš visų planuojamų išlaidų, skaičiavimas. |
| Atlikto darbo procentinė dalis | Atlikto darbo procentinė dalis = ProjectAccountingCube\_Projects\[atliktų užduočių faktinių išlaidų suma\] ÷ (ProjectAccountingCube\_Projects\[atliktų užduočių faktinių išlaidų suma\] + ProjectAccountingCube\_Projects\[projekto suplanuotų išlaidų suma\] – ProjectAccountingCube\_Projects\[atliktų užduočių suplanuotų išlaidų suma\]) | Visas atlikto darbo procentas pagal atliktų užduočių faktinių išlaidų sumą ir projekto suplanuotas išlaidas. |
| Faktinių apmokėtinų valandų koeficientas  | ProjectAccountingCube\_Projects\[projekto faktinių apmokėtinų išnaudotų valandų suma\] ÷ (ProjectAccountingCube\_Projects\[projekto faktinių apmokėtinų išnaudotų valandų suma\] + ProjectAccountingCube\_Projects\[projekto faktinių apmokėtinų neefektyvių valandų suma\]) | Faktinių apmokėtinų valandų suma, remiantis išnaudotomis valandomis ir neefektyviomis valandomis. |
| Gauta vertė                 | ProjectAccountingCube\_Projects\[projekto suplanuotų išlaidų suma\] × ProjectAccountingCube\_Projects\[atlikto darbo procentas\] | Suplanuotų išlaidų suma, padauginta iš atlikto darbo procento. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Objektas: ProjectAccountingCube\_TotalEstimatedCosts 
**Duomenų šaltinis:** ProjTable

| Pagrindiniai sujungti matavimo vienetai       | Laukas               | aprašymas |
|---------------------------------|---------------------|-------------|
| Užbaigtos veiklos suplanuotos išlaidos | Sum(TotalCostPrice) | Visų projekto operacijų tipų su užbaigtomis užduotimis numatoma bendroji savikaina. |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]