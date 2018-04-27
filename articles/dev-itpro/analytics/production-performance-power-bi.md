---
title: "„Power BI“ turinys Gamybos našumas"
description: "Šioje temoje aprašoma, kas įtraukta į „Power BI“ turinį Gamybos našumas. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d59a7aef90ecef0cd947b833f1cce1e2372f3033
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="production-performance-power-bi-content"></a>„Power BI“ turinys Gamybos našumas

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje aprašoma, kas įtraukta į „Microsoft Power BI“ turinį **Gamybos našumas**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Apžvalga

„Power BI‟ turinys **Gamybos našumas** skirtas gamybos vadovams ar organizacijos asmenims, atsakingiems už gamybos kontrolę.

Pasitelkę įtrauktas ataskaitas galite naudodami „Power BI‟ stebėti gamybos operacijų našumą vykdymo laiko, kokybės ir kaštų atžvilgiu. Ataskaitose naudojami operaciniai duomenys iš gamybos užsakymų ir paketinių užsakymų; jose pateikiamas tiek sujungtas visos įmonės gamybos metrikų rodinys, tiek pagal produktą ir išteklių paskirstytas metrikų rodinys.

„Power BI‟ turinys pažymi organizacijos gebėjimą gamybą baigti laiku ir visa apimtimi. Būsimas našumas numatomas pagal gamybos planus. Išsamiose ataskaitose pateikiama detalių įžvalgų apie produktų defektus, atsiradusius gamybos metu, bei išteklių ir operacijų defektų dažnį.

Naudodami šį „Power BI‟ turinį taip pat galite analizuoti gamybos nuokrypius. Gamybos nuokrypiai apskaičiuojami kaip įvertintų kaštų ir realizuotų kaštų skirtumas. Gamybos nuokrypiai skaičiuojami gamybos užsakymams ar paketiniams užsakymams pasiekus būseną **Baigtas**.

„Power BI‟ turinyje **Gamybos našumas** yra duomenų, kilusių iš gamybos užsakymų ir paketinių užsakymų. Ataskaitose nėra duomenų, susijusių su „kanban‟ gamyba.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Gamybos našumas** rodomas puslapyje **Gamybos našumas** (**Gamybos kontrolė** > **Užklausos ir ataskaitos** > **Gamybos našumo analizė** > **Gamybos našumas**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos

„Power BI‟ turinyje **Gamybos našumas** pateikiama keletas ataskaitų puslapių. Kiekvieną puslapį sudaro metrikų, pavaizduotų diagramomis, plytelėmis ir lentelėmis, rinkinys.

Toliau pateikiamoje lentelėje apžvelgiamos įtrauktos vizualizacijos.

| Ataskaitų puslapis                                | Diagramos                                               | Išklotinės |
|--------------------------------------------|------------------------------------------------------|-------|
| Gamybos našumas                     | <ul><li>Gamybos atvejų skaičius pagal datą</li><li>Gamybos atvejų skaičius pagal produktą ir prekių grupę</li><li>Suplanuotų gamybos atvejų skaičius pagal datą</li><li>Apatiniai 10 produktų pagal įvykdymą laiku ir visa apimtimi</li></ul> | <ul><li>Iš viso užsakymų</li><li>Įvykdyta laiku ir visa apimtimi (%)</li><li>Nebaigta (%)</li><li>Anksčiau termino (%)</li><li>Vėluoja (%)</li></ul> |
| Defektai pagal produktą                         | <ul><li>Defektų dažnis (ppm) pagal datą</li><li>Defektų dažnis (ppm) pagal produktą ir prekių grupę</li><li>Pagamintas kiekis pagal datą</li><li>Viršutiniai 10 produktų pagal defektų dažnį</li></ul> | <ul><li>Defektų dažnis (ppm)</li><li>Defektų kiekis</li><li>Bendras kiekis</li></ul> |
| Defektų tendencija pagal produktą                   | Defektų dažnis (ppm) pagal pagamintą kiekį | Defektų dažnis (ppm) |
| Defektai pagal išteklių                        | <ul><li>Defektų dažnis (ppm) pagal datą</li><li>Defektų dažnis (ppm) pagal išteklių ir teritoriją</li><li>Defektų dažnis (ppm) pagal operaciją</li><li>Viršutiniai 10 išteklių pagal defektų dažnį</li></ul> | Defektų kiekis |
| Defektų tendencija pagal išteklių                  | Defektų dažnis (ppm) pagal apdorotą kiekį | |
| Gamybos nuokrypiai įkainojant užduočių užsakymus | <ul><li>Gamybos nuokrypis pagal datą ir išlaidų grupės tipą</li><li>Gamybos nuokrypis pagal teritoriją ir išlaidų grupės tipą</li><li>Viršutiniai 10 produktų su nepalankiu gamybos nuokrypiu</li><li>Viršutiniai 10 nepalankių gamybos nuokrypių pagal išteklių</li></ul> | <ul><li>Realizuota savikaina</li><li>Gamybos nuokrypis</li><li>Gamybos nuokrypis (%)</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Tolesni duomenys naudojami „Power BI‟ turinio **Gamybos našumas** ataskaitų puslapiuose. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Norėdami daugiau sužinoti apie objektų saugyklą, žr. [„Power BI‟ integravimas su objektų saugykla](power-bi-integration-entity-store.md).

Tolesnėje lentelėje parodyti pagrindiniai agreguoti matavimo vienetai, naudojami kaip „Power BI‟ turinio pagrindas.

| Objektas                   | Pagrindiniai agreguoti matavimo vienetai  | „Finance and Operations“ duomenų šaltinis | Laukas              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Šioje lentelėje parodyta, kaip pagrindiniai sujungti matavimo vienetai naudojami kuriant kelis skaičiuojamus matus turinio duomenų rinkinyje.

| Mato vnt.                  | Kaip matas apskaičiuojamas |
|--------------------------|-------------------------------|
| Gamybos nuokrypis, %   | SUM('Production variance'[Production variance]) / SUM('Production variance'[Estimated cost]) |
| Visi suplanuoti užsakymai       | COUNTROWS('Planned production order') |
| Anksčiau                    | COUNTROWS(FILTER('Planned production order', 'Planned production order'[Scheduled end date] \< 'Planned production order'[Requirement date])) |
| Vėliau                     | COUNTROWS(FILTER('Planned production order', 'Planned production order'[Scheduled end date] \> 'Planned production order'[Requirement date])) |
| Laiku                  | COUNTROWS(FILTER('Planned production order', 'Planned production order'[Scheduled end date] = 'Planned production order'[Requirement date])) |
| Laiku (%)                | IF ( 'Planned production order'[On-time] \<\> 0, 'Planned production order'[On-time], IF ('Planned production order'[All planned orders] \<\> 0, 0, BLANK()) ) / 'Planned production order'[All planned orders] |
| Atlikta                | COUNTROWS(FILTER('Production order', 'Production order'[Is RAF'ed] = TRUE)) |
| Defektų dažnis (ppm)     | IF( 'Production order'[Total quantity] = 0, BLANK(), (SUM('Production order'[Defective quantity]) / 'Production order'[Total quantity]) \* 1000000) |
| Vėluojančios gamybos koeficientas  | 'Production order'[Late \#] / 'Production order'[Completed] |
| Anksčiau termino ir visa apimtimi          | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = TRUE && 'Production order'[Is early] = TRUE)) |
| Anksčiau termino \#                 | COUNTROWS(FILTER('Production order', 'Production order'[Is early] = TRUE)) |
| Anksčiau termino (%)                  | IFERROR( IF('Production order'[Early \#] \<\> 0, 'Production order'[Early \#], IF('Production order'[Total orders] = 0, BLANK(), 0)) / 'Production order'[Total orders], BLANK()) |
| Nebaigta               | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = FALSE && 'Production order'[Is RAF'ed] = TRUE)) |
| Nebaigta (%)             | IFERROR( IF('Production order'[Incomplete] \<\> 0, 'Production order'[Incomplete], IF('Production order'[Total orders] = 0, BLANK(), 0)) / 'Production order'[Total orders], BLANK()) |
| Vėluoja               | 'Production order'[Is RAF'ed] = TRUE && 'Production order'[Delayed value] = 1 |
| Anksčiau termino                 | 'Production order'[Is RAF'ed] = TRUE && 'Production order'[Days delayed] \< 0 |
| Visa apimtimi               | 'Production order'[Good quantity] \>= 'Production order'[Scheduled quantity] |
| Paskelbta kaip baigta                | 'Production order'[Production status value] = 5 \|\| 'Production order'[Production status value] = 7 |
| Vėluoja ir visa apimtimi           | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = TRUE && 'Production order'[Is delayed] = TRUE)) |
| Vėluoja \#                  | COUNTROWS(FILTER('Production order', 'Production order'[Is delayed] = TRUE)) |
| Vėluoja (%)                   | IFERROR( IF('Production order'[Late \#] \<\> 0, 'Production order'[Late \#], IF('Production order'[Total orders] = 0, BLANK(), 0)) / 'Production order'[Total orders], BLANK()) |
| Įvykdyta laiku ir visa apimtimi        | COUNTROWS(FILTER('Production order', 'Production order'[Is in full] = TRUE && 'Production order'[Is delayed] = FALSE && 'Production order'[Is early] = FALSE)) |
| Įvykdyta laiku ir visa apimtimi (%)      | IFERROR( IF('Production order'[On-time & in full] \<\> 0, 'Production order'[On-time & in full], IF('Production order'[Completed] = 0, BLANK(), 0)) / 'Production order'[Completed], BLANK()) |
| Iš viso užsakymų             | COUNTROWS('Production order') |
| Bendras kiekis           | SUM('Production order'[Good quantity]) + SUM('Production order'[Defective quantity]) |
| Defektų dažnis (ppm)        | IF( 'Route transactions'[Processed quantity] = 0, BLANK(), (SUM('Route transactions'[Defective quantity]) / 'Route transactions'[Processed quantity]) \* 1000000) |
| Defektų koeficientas (mišr.) (ppm) | IF( 'Route transactions'[Total mixed quantity] = 0, BLANK(), (SUM('Route transactions'[Defective quantity]) / 'Route transactions'[Total mixed quantity]) \* 1000000) |
| Apdorotas kiekis       | SUM('Route transactions'[Good quantity]) + SUM('Route transactions'[Defective quantity]) |
| Bendrasis mišrus kiekis     | SUM('Production order'[Good quantity]) + SUM('Route transactions'[Defective quantity]) |

Tolesnėje lentelėje parodytos pagrindinės dimensijos, naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti didesnio detalumo ir gauti gilesnių analitinių įžvalgų.

| Objektas                    | Atributų pavyzdžiai                                        |
|---------------------------|---------------------------------------------------------------|
| Data, kada paskelbta baigtu | Baigimo (RAF) datos, mėnesio ir metų poslinkis                 |
| Pabaigos data                | Pabaigos mėnesio poslinkis ir mėnuo                                  |
| Poreikio data          | Poreikio datos mėnesio poslinkis ir poreikio data            |
| Maršruto operacijos data    | Maršruto operacijos mėnesio poslinkis ir data                       |
| Vietos                     | Teritorijos ID, teritorijos pavadinimas, apskritis ir miestas                          |
| Objektai                  | ID ir pavadinimas                                                   |
| Ištekliai                 | Ištekliaus ID, ištekliaus pavadinimas, ištekliaus tipas ir išteklių grupė |
| Produktai                  | Produkto numeris, produkto pavadinimas, prekės ID ir prekių grupė         |



