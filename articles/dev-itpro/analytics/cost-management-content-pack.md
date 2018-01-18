---
title: "Išlaidų valdymo „Power BI“ turinys"
description: "Šioje temoje paaiškinama, kas įtraukta į išlaidų valdymo „Power BI“ turinį."
author: YuyuScheller
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: e0f9042b2647a484a70670d1d29e8036401b39f1
ms.contentlocale: lt-lt
ms.lasthandoff: 12/19/2017

---

# <a name="cost-management-power-bi-content"></a>Išlaidų valdymo „Power BI“ turinys

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kas įtraukta į išlaidų valdymo „Power BI“ turinį. 

# <a name="overview"></a>Peržiūra

**Kaštų apskaitos analizės** „Microsoft Power BI“ turinys skirtas išlaidų buhalteriams arba asmenims organizacijoje, kurie yra atsakingi už atsargas. **Išlaidų valdymo** „Power BI“turinys suteikia vadovams įžvalgų apie atsargas ir nebaigtos gamybos (NG) atsargas bei tai, kaip jose veikia išlaidų srautas. Informaciją taip pat galima naudoti kaip išsamų finansinės ataskaitos papildinį.

## <a name="key-measures"></a>Pagrindiniai matai

+ Pradinis balansas
+ Pabaigos likutis
+ Grynasis pokytis
+ Grynasis pokytis %
+ Skirstymas pagal terminus

## <a name="key-performance-indicators"></a>Pagrindiniai efektyvumo indikatoriai
+ Atsargų apyvarta
+ Atsargų tikslumas

CostAggregatedCostStatementEntryEntity pirminis duomenų šaltinis yra lentelė CostStatementCache. Šią lentelę valdo duomenų rinkinio talpyklos sistema. Pagal numatytuosius parametrus lentelė atnaujinama kas 24 valandas, bet jūs galite įjungti duomenų talpyklos konfigūracijos neautomatinius naujinimus. Tada galite atlikti neautomatinį naujinimą darbo srityje **Išlaidų valdymas** arba **Išlaidų analizė**. Paleidus CostStatementCache naujinį, turite atnaujinti „OData“ ryšį Power BI.com, kad svetainėje matytumėte atnaujintus duomenis. Nuokrypio (pirkimo, gamybos) matai šiame „Power BI“turinyje yra susiję tik su prekėmis, kurios vertinamos pagal standartinių išlaidų atsargų metodą. Gamybos nuokrypis apskaičiuojamas kaip skirtumas tarp aktyvios kainos ir realizuotos kainos. Gamybos nuokrypis apskaičiuojamas, kai gamybos užsakymo būsena būna **Baigtas**. Daugiau informacijos apie gamybos nuokrypių tipus ir tai, kaip kiekvienas tipas skaičiuojamas, žr. temoje [Apie baigto gamybos užsakymo nuokrypių analizę](https://technet.microsoft.com/en-us/library/gg242850.aspx)


## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
Į turinį įtrauktas ataskaitų puslapių rinkinys. Kiekvieną puslapį sudaro metrikų, pavaizduotų diagramomis, plytelėmis ir lentelėmis, rinkinys. Toliau pateiktoje lentelėje pateikiama **išlaidų valdymo** „Power BI“ turinio vizualizacijų apžvalga.

| Ataskaitų puslapis | Diagramos | Pareigos |
|---|---|---|
|Bendros atsargos (numatyta pagal dabartinį laikotarpį) |Tikslumas |Atsargų matai:<br>Atsargų pabaigos balansas<br>Atsargų grynasis pokytis<br>Atsargų grynasis pokytis %<br>|
| |Atsargų apyvarta | |
| |Atsargų pabaigos balansas pagal išteklių grupę | |
| |Atsargų grynasis pokytis pagal 1 lygio kategorijos pavadinimą ir 2 lygio kategorijos pavadinimą| |
| |Pirkimo nuokrypiai pagal išteklių grupę ir 3 lygio kategorijos pavadinimą | |
|Atsargos pagal teritoriją (numatyta pagal dabartinį laikotarpį) |Atsargų pabaigos balansas pagal teritorijos pavadinimą ir išteklių grupę | |
| |Atsargų apyvarta pagal teritorijos pavadinimą ir išteklių grupę | |
| |Atsargų pabaigos balansas pagal miestą ir išteklių grupę | |
|Atsargos pagal išteklių grupę (numatyta pagal dabartinį laikotarpį) |Atsargų matai | |
| |Atsargų tikslumas pagal sumą pagal išteklių grupę | |
| |Atsargų apyvarta pagal sumą pagal išteklių grupę | |
|Atsargų YOY (numatyta dabartiniai metai ir ankstesni metai) |Atsargų matai | |
| |Atsargų KPI<br>Atsargų apyvarta<br>Atsargų tikslumas | |
| |Atsargų pabaigos balansas pagal metus ir išteklių grupę | |
| |Pirkimo nuokrypiai pagal metus ir 3 lygio kategorijos pavadinimą | |
|Atsargų skirstymas pagal terminus (numatyta pagal dabartinius metus) |Atsargų skirstymas pagal terminus pagal ketvirtį ir išteklių grupę | |
| |Atsargų skirstymas pagal terminus pagal ketvirtį ir teritorijos pavadinimą | |
|Bendra NG (numatyta pagal dabartinį laikotarpį) |NG grynasis pokytis pagal 1 lygio kategorijos pavadinimą ir 2 lygio kategorijos pavadinimą |Nebaigtos gamybos NG matai<br>NG pabaigos likutis<br>NG grynasis pokytis<br>NG grynasis pokytis %<br> |
| |Gamybos nuokrypiai pagal išteklių grupę ir lygio kategorijos pavadinimą | |
| |NG grynasis pokytis pagal išteklių grupę | |
|NG pagal teritoriją (numatyta pagal dabartinį laikotarpį) |Nebaigtos gamybos NG matai | |
| |NG grynasis pokytis pagal teritorijos pavadinimą ir 2 lygio kategorijos pavadinimą | |
| |Gamybos nuokrypiai pagal išteklių grupę ir 3 lygio kategorijos pavadinimą | |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
„Finance and Operations“ duomenys naudojami **išlaidų valdymo** „Power BI“ turinio ataskaitų puslapiams užpildyti. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objekto parduotuvėje, kuri yra „Microsoft SQL“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. temoje [„Power BI‟ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md). Šie pagrindiniai sujungti matavimo vienetai naudojami kaip turinio pagrindas.

| Objektas            | Pagrindiniai sujungti matavimo vienetai | „Finance and Operations“ duomenų šaltinis | Laukas             | aprašymas                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Išrašo įrašai | Grynasis pokytis                | CostAggregatedCostStatementEntryEntity      | sum(\[Amount\])   | Suma apskaitos valiuta |
| Išrašo įrašai | Grynojo pokyčio kiekis       | CostAggregatedCostStatementEntryEntity      | sum(\[Quantity\]) |                                   |

Šioje lentelėje parodyta, kaip pagrindiniai sujungti matavimo vienetai naudojami kuriant kelis skaičiuojamus matus turinio duomenų rinkinyje.

| Mato vnt.                                 | Kaip matas apskaičiuojamas                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pradinis balansas                       | \[Ending balance\]-\[Net change\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Pradžios balanso kiekis              | \[Ending balance quantity\]-\[Net change quantity\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Pabaigos likutis                          | CALCULATE(SUM(\[Amount\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                           |
| Pabaigos balanso kiekis                 | CALCULATE(SUM(\[Quantity\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                         |
| Atsargų pradžios balansas             | CALCULATE(\[Beginning balance\], 'Statement entries'\[Statement Type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                      |
| Atsargų pabaigos balansas                | CALCULATE(\[Ending balance\], 'Statement entries'\[Statement Type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                         |
| Atsargų grynasis pokytis                    | CALCULATE(\[Net change\], 'Statement entries'\[Statement type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                             |
| Atsargų grynojo pokyčio kiekis           | CALCULATE(\[Net change quantity\], 'Statement entries'\[Statement type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                    |
| Atsargų grynasis pokytis %                  | IF(\[Inventory ending balance\] = 0, 0, \[Inventory net change\] / \[Inventory ending balance\])                                                                                                                                                                                                                                                                                                                                                                           |
| Atsargų apyvarta pagal sumą                | if(OR(\[Inventory average balance\] &lt;= 0, \[Inventory sold or consumed issues\] &gt;= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\])                                                                                                                                                                                                                                                                                                  |
| Vidutinis atsargų balansas               | (\[Inventory ending balance\] + \[Inventory beginning balance\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Parduotų arba sunaudotų atsargų problemos       | \[Inventory sold\] + \[Inventory consumed material cost\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Sunaudotų atsargų medžiagų išlaidos        | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Parduotos atsargos                          | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 2\_\] = "Sold")                                                                                                                                                                                                                                                                                                                                                                             |
| Atsargų tikslumas pagal sumą            | IF(\[Inventory ending balance\] &lt;= 0, IF(OR(\[Inventory counted amount\] &lt;&gt; 0, \[Inventory ending balance\] &lt; 0), 0, 1), MAX(0, (\[Inventory ending balance\] - ABS(\[Inventory counted amount\]))/\[Inventory ending balance\]))                                                                                                                                                                                                                              |
| Apskaičiuota atsargų suma                | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 3\_\] = "Counting")                                                                                                                                                                                                                                                                                                                                                                         |
| Atsargų skirstymas pagal terminus                         | if(ISBLANK(max('Fiscal calendars'\[Date\])), blank(), MAX(0, MIN(\[Inventory aging receipts quantity\], \[Inventory aging ending balance quantity\] - \[Inventory aging receipts quantity in the future\]))) \* \[Inventory avg unit cost\]                                                                                                                                                                                                                                |
| Atsargų skirstymo pagal terminus gavimo kiekis       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Inventory net change quantity\], 'Statement entries'\[Quantity\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\]))), CALCULATE(\[Inventory net change quantity\], 'Statement entries'\[Quantity\] &gt; 0)) |
| Atsargų skirstymo pagal terminus pabaigos balanso kiekis | \[Inventory ending balance quantity\] + CALCULATE(\[Inventory net change quantity\], FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; max('Fiscal calendars'\[Date\]) ))                                                                                                                                 |
| Atsargų skirstymo pagal terminus gavimas ateityje  | CALCULATE(\[Inventory net change\], 'Statement entries'\[Amount\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; MAX('Fiscal calendars'\[Date\])))                                                                                                                                             |
| Vidutinė atsargų vieneto savikaina                 | CALCULATE(\[Inventory ending balance\] / \[Inventory ending balance quantity\],ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]))                                                                                                                                                                                                                 |
| Pirkimo nuokrypiai                      | CALCULATE(SUM(\[Amount\]), 'Statement entries'\[Category name - level 2\_\] = "Procured", 'Statement entries'\[Statement type\] = "Variance")                                                                                                                                                                                                                                                                                                                              |
| NG pradžios balansas                   | CALCULATE(\[Beginning balance\], 'Statement entries'\[Statement Type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                            |
| NG pabaigos likutis                      | CALCULATE(\[Ending balance\], 'Statement entries'\[Statement Type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                               |
| NG grynasis pokytis                          | CALCULATE(\[Net change\], 'Statement entries'\[Statement type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                                   |
| NG grynasis pokytis %                        | IF(\[WIP ending balance\] = 0, 0, \[WIP net change\] / \[WIP ending balance\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Gamybos nuokrypiai                    | CALCULATE(SUM(\[Amount\]), 'Statement entries'\[Category name - level 2\_\] = "ManufacturedCost", 'Statement entries'\[Statement type\] = "Variance")                                                                                                                                                                                                                                                                                                                      |
| Kategorijos pavadinimas – 1 lygis                 | switch(\[Category name - level 1\_\], "None", "None", "NetSourcing", "Net sourcing", "NetUsage", "Net usage", "NetConversionCost", "Net conversion cost", "NetCostOfGoodsManufactured", "Net cost of goods manufactured", "BeginningBalance", "Beginning balance")                                                                                                                                                                                                         |
| Kategorijos pavadinimas – 2 lygis                 | switch(\[Category name - level 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Transferred", "Transferred", "Sold", "Sold", "ConsumedMaterialsCost", "Consumed material cost", "ConsumedManufacturingCost", "Consumed manufacturing cost", "ConsumedOutsourcingCost", "Consumed outsourcing cost", "ConsumedIndirectCost", "Consumed indirect cost", "ManufacturedCost", "Manufactured cost", "Variances", "Variances")                            |
| Kategorijos pavadinimas – 3 lygis                 | switch(\[Category name - level 3\_\], "None", "None", "Counting", "None", "ProductionPriceVariance", "Production price", "QuantityVariance", "Quantity", "SubstitutionVariance", "Substitution", "ScrapVariance", "Scrap", "LotSizeVariance", "Lot size", "RevaluationVariance", "Revaluation", "PurchasePriceVariance", "Purchase price", "CostChangeVariance", "Cost change", "RoundingVariance", "Rounding variance")                                                   |

Šios pagrindinės dimensijos naudojamos kaip filtrai sujungtiems matavimo vienetams skaidyti, siekiant didesnio detalumo ir gilesnių analitinių įžvalgų.

| Objektas           | Atributų pavyzdžiai                       |
|------------------|----------------------------------------------|
| Objektai         | ID, Pavadinimas                                     |
| Finansiniai kalendoriai | Kalendorius Mėnuo, Laikotarpis, Ketvirtis, Metai       |
| KPI tikslai        | Atsargų tikslumo tikslas, Atsargų apyvartos tikslas |
| Didžiosios knygos          | Valiuta, Pavadinimas, Aprašas                  |
| Vietos            | ID, Pavadinimas, Šalis, Miestas                      |






