---
title: "„Power BI“ turinys Praktikos vadovas"
description: "Šioje temoje paaiškinama, kas įtraukta į „Power BI“ turinį Praktikos vadovas. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turiniui kurti."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: lt-lt
ms.lasthandoff: 06/20/2017

---

# <a name="practice-manager-power-bi-content"></a>„Power BI“ turinys Praktikos vadovas

[!include[banner](../includes/banner.md)]

Šioje temoje paaiškinama, kas įtraukta į „Microsoft Power BI“ turinį **Praktikos vadovas**. Joje paaiškinama, kaip pasiekti „Power BI“ ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, kurie naudojami turiniui kurti.

## <a name="overview"></a>Apžvalga

„Power BI“ turinys **Praktikos vadovas** sukurtas praktikos vadovams ir projektų vadovams. Jame pateikiamos pagrindinės metrikos, susijusios su organizacijos vykdomais projektais. Ataskaitų srityje pateikiama projektų ir susijusių klientų apžvalga. Ataskaitos lygio filtrą galima naudoti norint teikti konkrečių juridinių subjektų ataskaitas. Šis „Power BI“ turinys duomenis gauna iš projektų apskaitos sujungtų matavimo vienetų.

„Power BI“ turinys **Praktikos vadovas** apima penkis ataskaitų puslapius: vieną peržiūros puslapį ir keturis puslapius, kuriuose pateikiama informacija apie projektų išlaidas, įplaukas, gautos vertės valdymą ir valandų metrikas, suskirstytas įvairiose dimensijose.

Visos turinio sumos rodomos sistemos valiuta. Sistemos valiutą galite nustatyti puslapyje **Sistemos parametrai**.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition‟ 2017 m. liepos mėn. naujinimą, „Power BI‟ turinys **Praktikos vadovas** rodomas darbo srityje **Projektų valdymas**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos

Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Praktikos vadovas** ataskaitų puslapyje.

| Ataskaitų puslapis       | Metrika |
|-------------------|---------|
| Projektų apžvalga | <ul><li>Sukurti projektai</li><li>Įvertinti projektai</li><li>Apdorojami projektai</li><li>Projektų skaičius pagal etapą</li><li>Projektų skaičius pagal miestą</li><li>Faktinės įplaukos pagal klientą</li><li>Biudžeto bruto marža pagal projektą</li><li>Gautos vertės valdymo apžvalga</li></ul> |
| Savikaina              | <ul><li>Faktinės ir biudžeto išlaidos pagal mėnesį</li><li>Faktinės ir biudžeto išlaidos pagal metus</li><li>Faktinės ir biudžeto išlaidos pagal kategoriją</li><li>Faktinės išlaidos pagal operacijos tipą</li></ul> |
| Įplaukos           | <ul><li>Faktinės įplaukos pagal mėnesį</li><li>Faktinės įplaukos pagal pašto kodą</li><li>Faktinės ir biudžeto įplaukos pagal kategoriją</li><li>Faktinės įplaukos pagal kliento pramonės šaką</li></ul> |
| EVM               | Išlaidų ir planavimo efektyvumo indeksas pagal projektą |
| Valandos             | <ul><li>Faktinių apmokėtinų išnaudotų valandų, faktinių apmokėtinų neefektyvių valandų ir biudžeto valandų palyginimas</li><li>Faktinių apmokėtinų išnaudotų valandų ir faktinių apmokėtinų neefektyvių valandų palyginimas pagal projektą</li><li>Faktinių apmokėtinų išnaudotų valandų ir faktinių apmokėtinų neefektyvių valandų palyginimas pagal išteklių</li><li>Faktinių apmokėtinų valandų tarifas pagal projektą</li><li>Faktinių apmokėtinų valandų tarifas pagal išteklių</li></ul> |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Taip pat galite naudoti funkciją Eksportuoti pagrindinius duomenis, norėdami eksportuoti vizualiai apibendrintus pagrindinius duomenis.

## <a name="extending-the-power-bi-content"></a>„Power BI“ turinio išplėtimas
Naudodami turinio paketus, kurie pateikiami „Microsoft Dynamics Lifecycle Services“ (LCS), žmonėms, kurie neprisijungia prie „Microsoft Dynamics 365“ galite pateikti didžiąją analizę. Galite keisti šiuos turinio paketus, kad į juos įtrauktumėte kitas ataskaitas arba vaizdinius, tada paskelbti juos savo Power BI.com nuomotojui analizei. 

„Power BI“ turinį **Praktikos vadovas** galite rasti LCS bibliotekoje Bendrai naudojamas turtas. Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md). Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).

Būtinai atsisiųskite turinį **Praktikos vadovas**, kuris taikomas jūsų naudojamai „Dynamics 365‟ versijai.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Tolesniais duomenimis pildomi „Power BI‟ turinio **Praktikos vadovas** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. temoje [„Power BI‟ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Tolesniuose skyriuose aprašyti kiekviename objekte naudojami sujungti matavimo vienetai.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Objektas: ProjectAccountingCube_ActualHourUtilization
**Duomenų šaltinis:** ProjEmplTrans

| Pagrindiniai sujungti matavimo vienetai      | Laukas                              | aprašymas | 
|--------------------------------|------------------------------------|-------------|
| Faktinės apmokėtinos išnaudotos valandos | Sum(ActualUtilizationBillableRate) | Faktinių apmokėtinų išnaudotų valandų suma. |
| Faktinės apmokėtinos neefektyvios valandos   | Sum(ActualBurdenBillableRate)      | Visas faktinio neefektyvumo tarifas. |

### <a name="entity-projectaccountingcubeactuals"></a>Objektas: ProjectAccountingCube_Actuals
**Duomenų šaltinis:** ProjTransPosting

| Pagrindiniai sujungti matavimo vienetai | Laukas              | aprašymas | 
|---------------------------|--------------------|-------------|
| Faktinės įplaukos            | Sum(ActualRevenue) | Visų operacijų užregistruotų įplaukų suma. |   
| Faktinės išlaidos               | Sum(ActualCost)    | Visų operacijų tipų užregistruotų išlaidų suma. |

### <a name="entity-projectaccountingcubecustomer"></a>Objektas: ProjectAccountingCube_Customer
**Duomenų šaltinis:** CustTable

| Pagrindiniai sujungti matavimo vienetai | Laukas                                            | aprašymas | 
|---------------------------|--------------------------------------------------|-------------|
| Projektų skaičius        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Galimų projektų skaičius. |


### <a name="entity-projectaccountingcubeforecasts"></a>Objektas: ProjectAccountingCube_Forecasts
**Duomenų šaltinis:** ProjTransBudget

| Pagrindiniai sujungti matavimo vienetai | Laukas                  | aprašymas | 
|---------------------------|------------------------|-------------|
| Biudžeto išlaidos               | Sum(BudgetCost)        | Visų operacijų tipų prognozuojamų išlaidų suma. |
| Biudžeto įplaukos            | Sum(BudgetRevenue)     | Prognozuojamų sukauptų įplaukų / įplaukų, kurių sąskaita faktūra išrašyta, suma.  |
| Biudžeto bruto marža       | Sum(BudgetGrossMargin) | Skirtumas tarp visų prognozuojamų įplaukų sumos ir visų prognozuojamų išlaidų sumos. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Objektas: ProjectAccountingCube_ProjectPlanCostsView
**Duomenų šaltinis:** projektas

| Pagrindiniai sujungti matavimo vienetai | Laukas                    | aprašymas | 
|---------------------------|--------------------------|-------------|
| Suplanuotos išlaidos              | Sum(SumOfTotalCostPrice) | Visų projekto operacijų tipų su suplanuotomis užduotimis numatoma bendroji savikaina. |

### <a name="entity-projectaccountingcubeprojects"></a>Objektas: ProjectAccountingCube_Projects
**Duomenų šaltinis:** projektas

| Pagrindiniai sujungti matavimo vienetai    | Laukas | aprašymas | 
|------------------------------|-------|-------------|
| Išlaidų efektyvumo indeksas       | ProjectAccountingCube_Projects[gauta vertė] / ProjectAccountingCube_Projects[atliktų užduočių faktinių išlaidų suma] | Viso gautos vertės, padalytos iš visų faktinių išlaidų, skaičiavimas. |
| Planavimo efektyvumo indeksas   | ProjectAccountingCube_Projects[gauta vertė] / ProjectAccountingCube_Projects[atliktų užduočių suplanuotų išlaidų suma] | Viso gautos vertės, padalytos iš visų planuojamų išlaidų, skaičiavimas. |
| Atlikto darbo procentinė dalis | Atlikto darbo procentinė dalis = ProjectAccountingCube_Projects[atliktų užduočių faktinių išlaidų suma] / (ProjectAccountingCube_Projects[atliktų užduočių faktinių išlaidų suma] + ProjectAccountingCube_Projects[projekto suplanuotų išlaidų suma] – ProjectAccountingCube_Projects[atliktų užduočių suplanuotų išlaidų suma]) | Visas atlikto darbo procentas pagal atliktų užduočių faktinių išlaidų sumą ir projekto suplanuotas išlaidas. |
| Faktinių apmokėtinų valandų koeficientas  | ProjectAccountingCube_Projects[projekto faktinių apmokėtinų išnaudotų valandų suma] / (ProjectAccountingCube_Projects[projekto faktinių apmokėtinų išnaudotų valandų suma] + ProjectAccountingCube_Projects[projekto faktinių apmokėtinų neefektyvių valandų suma]) | Faktinių apmokėtinų valandų suma, remiantis išnaudotomis valandomis ir neefektyviomis valandomis. |
| Gauta vertė                 | ProjectAccountingCube_Projects[projekto suplanuotų išlaidų suma] * ProjectAccountingCube_Projects[atlikto darbo procentas] | Suplanuotų išlaidų suma, padauginta iš atlikto darbo procento. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Objektas: ProjectAccountingCube_TotalEstimatedCosts 
**Duomenų šaltinis:** ProjTable

| Pagrindiniai sujungti matavimo vienetai       | Laukas               | aprašymas | 
|---------------------------------|---------------------|-------------|
| Užbaigtos veiklos suplanuotos išlaidos | Sum(TotalCostPrice) | Visų projekto operacijų tipų su užbaigtomis užduotimis numatoma bendroji savikaina. |

