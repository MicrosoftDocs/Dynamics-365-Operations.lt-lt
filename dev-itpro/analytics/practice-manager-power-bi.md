---
title: "„Power BI“ turinys Praktikos vadovas"
description: "Šioje temoje paaiškinama, kas įtraukta į „Power BI“ turinį Praktikos vadovas. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>„Power BI“ turinys Praktikos vadovas

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kas įtraukta į „Microsoft Power BI“ turinį **Praktikos vadovas**. Joje paaiškinama, kaip pasiekti „Power BI“ ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, kurie naudojami turiniui kurti.

## <a name="overview"></a>Apžvalga

„Power BI“ turinys **Praktikos vadovas** sukurtas praktikos vadovams ir projektų vadovams. Jame pateikiamos pagrindinės metrikos, susijusios su organizacijos vykdomais projektais. Ataskaitų srityje pateikiama projektų ir susijusių klientų apžvalga. Ataskaitos lygio filtrą galima naudoti norint teikti konkrečių juridinių subjektų ataskaitas. Šis „Power BI“ turinys gauna duomenis iš „Microsoft Dynamics 365 for Operations“ projektų apskaitos sujungtų matavimo vienetų.

„Power BI“ **Praktikos vadovas** apima penkis ataskaitų puslapius: vieną peržiūros puslapį ir keturis puslapius, kuriuose pateikiama informacija apie projektų išlaidas, įplaukas, gautos vertės valdymą ir valandų metrikas, paskirstytas įvairiose dimensijose.

Visos turinio sumos rodomos sistemos valiuta. Sistemos valiutą galite nustatyti puslapyje **Sistemos parametrai**.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

„Power BI“turinį **Praktikos vadovas** galite rasti bendrai naudojamo turto bibliotekoje „Microsoft Dynamics Lifecycle Services“ (LCS). Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie „Dynamics 365 for Operations“ duomenų, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).

Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos

Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Praktikos vadovas** ataskaitų puslapyje.

| Ataskaitų puslapis                                          | Metrika               |
|------------------------------------------------------|-----------------------------------------------|
| Ataskaitų sritis  | Sukurti projektai<br>Įvertinti projektai<br>Apdorojami projektai<br>Projektų skaičius pagal etapą<br>Projektų skaičius pagal miestą<br>Faktinės įplaukos pagal klientą<br>Biudžeto bruto marža pagal projektą<br>Gautos vertės valdymo apžvalga |
| Savikaina                                                 | Faktinės ir biudžeto išlaidos pagal mėnesį<br>Faktinės ir biudžeto išlaidos pagal metus<br>Faktinės ir biudžeto išlaidos pagal kategoriją<br>Faktinės išlaidos pagal operacijos tipą       |
| Įplaukos                                              | Faktinės įplaukos pagal mėnesį<br>Faktinės įplaukos pagal pašto kodą<br>Faktinės ir biudžeto įplaukos pagal kategoriją<br>Faktinės įplaukos pagal kliento pramonės šaką        |
| EVM                                                  | Išlaidų ir planavimo efektyvumo indeksas pagal projektą                 |
| Valandos                                                | Faktinės apmokėtinos išnaudotos valandos, faktinės apmokėtinos neefektyvios valandos ir biudžeto valandos<br>Faktinės apmokėtinos išnaudotos valandos ir faktinės apmokėtinos neefektyvios valandos pagal projektą<br>Faktinės apmokėtinos išnaudotos valandos ir faktinės apmokėtinos neefektyvios valandos pagal išteklių<br>Faktinių apmokėtinų valandų tarifas pagal projektą<br>Faktinių apmokėtinų valandų tarifas pagal išteklių |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Taip pat galite naudoti funkciją Eksportuoti pagrindinius duomenis, norėdami eksportuoti vizualiai apibendrintus pagrindinius duomenis.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

„Dynamics 365 for Operations“ duomenys naudojami „Power BI“ turinio **Praktikos vadovas** ataskaitų puslapiams užpildyti. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objekto parduotuvėje, kuri yra „Microsoft SQL“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. temoje [„Power BI‟ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Tolesniuose skyriuose paaiškinami kiekviename objekte naudojami sujungti matavimo vienetai.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Objektas: ProjectAccountingCube_ActualHourUtilization
**Duomenų šaltinis**: ProjEmplTrans

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Faktinių apmokėtinų išnaudotų valandų suma |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Visas faktinio neefektyvumo tarifas             |

### <a name="entity-projectaccountingcubeactuals"></a>Objektas: ProjectAccountingCube_Actuals
**Duomenų šaltinis**: ProjTransPosting

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Visų operacijų užregistruotų įplaukų suma |   
| ActualCost   |                             Sum(ActualCost)           |    Visų operacijų tipų užregistruotų išlaidų suma    |

### <a name="entity-projectaccountingcubecustomer"></a>Objektas: ProjectAccountingCube_Customer
**Duomenų šaltinis**: CustTable

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Projektų skaičius        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Galimų projektų skaičius    |


### <a name="entity-projectaccountingcubeforecasts"></a>Objektas: ProjectAccountingCube_Forecasts
**Duomenų šaltinis**: ProjTransBudget

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Visų operacijų tipų prognozuojamų išlaidų suma     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Prognozuojamų sukauptų įplaukų / įplaukų, kurių SF išrašyta, suma         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Skirtumas tarp visų prognozuojamų įplaukų sumos ir visų prognozuojamų išlaidų sumos

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Objektas: ProjectAccountingCube_ProjectPlanCostsView
**Duomenų šaltinis**: projektas

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Visų projekto operacijų tipų su suplanuotomis užduotimis numatoma bendroji savikaina |

### <a name="entity-projectaccountingcubeprojects"></a>Objektas: ProjectAccountingCube_Projects
**Duomenų šaltinis**: projektas

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Išlaidų efektyvumo indeksas  |ProjectAccountingCube_Projects[gauta vertė] / ProjectAccountingCube_Projects[atliktų užduočių faktinių išlaidų suma] |     Viso gautos vertės, padalytos iš visų faktinių išlaidų, skaičiavimas|
|  Planavimo efektyvumo indeksas |ProjectAccountingCube_Projects[gauta vertė] / ProjectAccountingCube_Projects[atliktų užduočių suplanuotų išlaidų suma]|Viso gautos vertės, padalytos iš visų suplanuotų išlaidų, skaičiavimas |
|Atlikto darbo procentinė dalis |Atlikto darbo procentinė dalis = ProjectAccountingCube_Projects[atliktų užduočių faktinių išlaidų suma] / (ProjectAccountingCube_Projects[atliktų užduočių faktinių išlaidų suma] + ProjectAccountingCube_Projects[projekto suplanuotų išlaidų suma] – ProjectAccountingCube_Projects[atliktų užduočių suplanuotų išlaidų suma])|Visas atlikto darbo procentas pagal atliktų užduočių faktinių išlaidų sumą ir projekto suplanuotas išlaidas|
|Projekto faktinių apmokėtinų valandų tarifas|ProjectAccountingCube_Projects[projekto faktinių apmokėtinų išnaudotų valandų suma] / (ProjectAccountingCube_Projects[projekto faktinių apmokėtinų išnaudotų valandų suma] + ProjectAccountingCube_Projects[projekto faktinių apmokėtinų neefektyvių valandų suma])|Faktinės apmokėtinos valandos pagal išnaudotas + neefektyvias valandas|
|Gauta vertė|ProjectAccountingCube_Projects[projekto suplanuotų išlaidų suma] * ProjectAccountingCube_Projects[atlikto darbo procentas]|Suplanuotų išlaidų suma, padauginta iš atlikto darbo procento|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Objektas: ProjectAccountingCube_TotalEstimatedCosts 
**Duomenų šaltinis**: ProjTable

| Pagrindiniai sujungti matavimo vienetai                | Laukas                                | aprašymas                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Visų projekto operacijų tipų su atliktomis užduotimis numatoma bendroji savikaina|

## <a name="additional-resources"></a>Papildomi ištekliai

Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

- [Duomenų objektai](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [„Power BI‟ integravimo su darbo sritimis konfigūravimas](configure-power-bi-integration.md)

