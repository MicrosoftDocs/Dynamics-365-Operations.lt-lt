---
title: „Power BI“ turinys Išlaidų valdymas
description: Šiame straipsnyje aprašoma, kas įtraukta į išlaidų valdymo Power BI turinį.
author: JennySong-SH
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.industry: Manufacturing
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
ms.openlocfilehash: 11b414c8c352ac0a6307584ef14bcc13122f4573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267355"
---
# <a name="cost-management-power-bi-content"></a>„Power BI“ turinys Išlaidų valdymas

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūra

„Microsoft Power BI“ turinys **Išlaidų valdymas** yra skirtas atsargų apskaitininkams arba organizacijoje dirbantiems asmenims, kurie yra atsakingi už atsargų būsenos arba nebaigtos gamybos (NG) statusą ar tiems, kurie šiuo statusu domisi, arba yra atsakingi už standartinės savikainos analizavimą ar tuo domisi.

Šiame „Power BI“ turinyje pateikiamas kategorizuotas formatas, padedantis stebėti atsargų našumą ir vizualizuoti, kaip vyksta atsargų našumo savikaina. Galite gauti valdymo įžvalgų, pvz., apie apyvartos koeficientą, dienų skaičių, kai atsargų yra turima, tikslumą bei „ABC klasifikaciją“ jūsų pageidaujamu agreguotu lygiu (įmonė, prekė, prekių grupė ar svetainė). Pasiekiamą informaciją taip pat galima naudoti kaip išsamų finansinės ataskaitos papildinį.

„Power BI“ turinys yra sukuriamas remiantis **CostObjectStatementCacheMonthly** agreguoto matavimo vienetu, kurio lentelė **CostObjectStatementCache** yra naudojama kaip pirminis duomenų šaltinis. Šią lentelę valdo duomenų rinkinio talpyklos sistema. Pagal numatytuosius parametrus lentelė atnaujinama kas 24 valandas, bet jūs atnaujinimo dažnumą pakeisti arba įgalinti galite duomenų rinkinio talpyklos konfigūracijoje. Neautomatinius atnaujinimus galima paleisti darbo srityje **Išlaidų administravimas** arba **Išlaidų analizė**.

Kiekvieną kartą atnaujinus **CostObjectStatementCache** lentelę, prieš atnaujinant „Power BI“ vizualizacijų duomenis reikia atnaujinti **CostObjectStatementCacheMonthly** agreguoto matavimo vienetą.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

„Power BI“ turinys **Išlaidų valdymas** rodomas darbo srityse **Išlaidų administravimas** ir **Išlaidų analizė**.

Darbo srityje **Išlaidų administravimas** pateikiami toliau nurodyti skirtukai.

- **Apžvalga** – šiame skirtuke pateikiami programos duomenys.
- **Atsargų apskaitos būsena** – šiame skirtuke rodomas „Power BI“ turinys.
- **Gamybos apskaitos būsena** – šiame skirtuke rodomas „Power BI“ turinys.

Darbo srityje **Išlaidų analizė** pateikiami toliau nurodyti skirtukai.

- **Apžvalga** – šiame skirtuke pateikiami programos duomenys.
- **Atsargų apskaitos analizė** – šiame skirtuke rodomas „Power BI“ turinys.
- **Gamybos apskaitos analizė** – šiame skirtuke rodomas „Power BI“ turinys.
- **Standartinio išlaidų nuokrypio analizė** – šiame skirtuke rodomas „Power BI“ turinys.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtraukti ataskaitos puslapiai

„Power BI“ turinyje **Kaštų valdymas** pateikiamas ataskaitos puslapių, sudarytų iš metrikų rinkinio, rinkinys. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės 

Toliau pateiktose lentelėse pateikiama „Power BI“ turinio **Išlaidų valdymas** vizualizacijų apžvalga.

### <a name="inventory-accounting-status"></a>Atsargų apskaitos būsena

| Ataskaitų puslapis                               | Vizualizacija                                   |
|-------------------------------------------|-------------------------------------------------|
| Atsargų peržiūra                        | Pradinis balansas                               |
|                                           | Grynasis pokytis                                      |
|                                           | Grynasis pokytis %                                    |
|                                           | Pabaigos likutis                                  |
|                                           | Atsargų tikslumas                              |
|                                           | Atsargų apyvartos koeficientas                        |
|                                           | Turimų atsargų dienos                          |
|                                           | Laikotarpio aktyvus produktas                        |
|                                           | Laikotarpio aktyvūs išlaidų objektai                   |
|                                           | Balansas pagal prekių grupę                           |
|                                           | Balansas pagal teritoriją                                 |
|                                           | Išrašas pagal kategoriją                           |
|                                           | Grynasis pokytis pagal ketvirtį                           |
| Atsargų apžvalga pagal teritoriją ir prekių grupę | Atsargų tikslumas pagal teritoriją                      |
|                                           | Atsargų apyvartos koeficientas pagal teritoriją                |
|                                           | Atsargų pabaigos balansas pagal teritoriją                |
|                                           | Atsargų tikslumas pagal prekių grupę                |
|                                           | Atsargų apyvartos koeficientas pagal prekių grupę          |
|                                           | Atsargų pabaigos balansas pagal teritoriją ir prekių grupę |
| Inventorizacijos aprašas                       | Inventorizacijos aprašas                             |
| Atsargų išrašas pagal teritoriją               | Atsargų išrašas pagal teritoriją                     |
| Atsargų išrašas pagal produktų hierarchiją  | Inventorizacijos aprašas                             |
| Atsargų išrašas pagal produktų hierarchiją  | Atsargų išrašas pagal teritoriją                     |

### <a name="manufacturing-accounting-status"></a>Gamybos apskaitos būsena

| Ataskaitų puslapis                | Vizualizacija                       |
|----------------------------|-------------------------------------|
| NG apžvalga nuo metų pradžios           | Pradinis balansas                   |
|                            | Grynasis pokytis                          |
|                            | Grynasis pokytis %                        |
|                            | Pabaigos likutis                      |
|                            | NG apyvartos koeficientas                  |
|                            | Turimų NG dienos                    |
|                            | Laikotarpio aktyvus išlaidų objektas        |
|                            | Grynasis pokytis pagal išteklių grupę        |
|                            | Balansas pagal teritoriją                     |
|                            | Išrašas pagal kategoriją               |
|                            | Grynasis pokytis pagal ketvirtį               |
| nebaigtos gamybos išrašas              | Pradinis balansas                   |
|                            | Pabaigos likutis                      |
|                            | NG išrašas pagal kategoriją           |
| NG išrašas pagal teritoriją      | Pradinis balansas                   |
|                            | Pabaigos likutis                      |
|                            | NG išrašas pagal kategoriją ir teritoriją  |
| NG išrašas pagal hierarchiją | Pradinis balansas                   |
|                            | Pabaigos likutis                      |
|                            | NG išrašas pagal kategorijų ir hierarchiją |

### <a name="inventory-accounting-analysis"></a>Atsargų apskaitos analizė

| Ataskaitų puslapis        | Vizualizacija                                                                |
|--------------------|------------------------------------------------------------------------------|
| Atsargų informacija  | 10 geriausių išteklių pagal galutinį balansą                                           |
|                    | 10 geriausių išteklių pagal grynąjį pokyčio padidėjimą                                      |
|                    | 10 geriausių išteklių pagal grynąjį pokyčio sumažėjimą                                      |
|                    | 10 geriausių išteklių pagal atsargų apyvartos koeficientą                                 |
|                    | Ištekliai pagal mažą atsargų apyvartos koeficientą ir pabaigos balansą, viršijantį ribą |
|                    | 10 geriausių išteklių mažą tikslumą                                             |
| ABC klasifikacija | Atsargų pabaigos balansas                                                     |
|                    | Suvartota medžiaga                                                            |
|                    | Parduota (PPK)                                                                  |
| Atsargų tendencijos   | Atsargų pabaigos balansas                                                     |
|                    | Atsargų grynasis pokytis                                                         |
|                    | Atsargų apyvartos koeficientas                                                     |
|                    | Atsargų tikslumas                                                           |

### <a name="manufacturing-accounting-analysis"></a>Gamybos apskaitos analizė

| Ataskaitų puslapis | Vizualizacija      |
|-------------|--------------------|
| NG tendencijos  | NG pabaigos likutis |
|             | NG grynasis pokytis     |
|             | NG apyvartos koeficientas |

### <a name="std-cost-variance-analysis"></a>Standartinio išlaidų nuokrypio analizė

| Ataskaitų puslapis                             | Vizualizacija                                        |
|-----------------------------------------|------------------------------------------------------|
| Pirkimo kainos pokytis (standartinės išlaidos) nuo metų pradžios | Įsigijimų balansas                                     |
|                                         | Pirkimo kainų nuokrypis                              |
|                                         | Pirkimo kainų nuokrypio koeficientas                        |
|                                         | Nuokrypis pagal prekių grupę                               |
|                                         | Nuokrypis pagal teritoriją                                     |
|                                         | Pirkimo kaina pagal ketvirtį                            |
|                                         | Pirkimo kaina pagal ketvirtį ir prekių grupę             |
|                                         | 10 geriausių išteklių pagal nepageidaujamą pirkimo kainos koeficientą |
|                                         | 10 geriausių išteklių pagal pageidaujamą pirkimo kainos koeficientą   |
| Gamybos nuokrypis (standartinės išlaidos) nuo metų pradžios     | Pagaminto kiekio savikaina                                    |
|                                         | Gamybos nuokrypis                                  |
|                                         | Gamybos nuokrypio koeficientas                            |
|                                         | Nuokrypis pagal prekių grupę                               |
|                                         | Nuokrypis pagal teritoriją                                     |
|                                         | Gamybos nuokrypis pagal ketvirtį                       |
|                                         | Gamybos nuokrypis pagal ketvirtį ir nuokrypio tipą     |
|                                         | 10 geriausių išteklių pagal nepageidaujamą gamybos nuokrypį  |
|                                         | 10 geriausių išteklių pagal pageidaujamą gamybos nuokrypį    |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Programos duomenys naudojami ataskaitos puslapiams „Power BI“ turinyje **Išlaidų valdymas** užpildyti. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objekto parduotuvėje, kuri yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Toliau pateiktų objektų agreguoti matavimo vienetai yra naudojami kaip „Power BI“ turinio pagrindas.

| Objektas                          | Pagrindiniai agreguoti matavimo vienetai | Finansų ir operacijų duomenų šaltinis | Laukas               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Suma                     | CostObjectStatementCache               | Suma              |
| CostObjectStatementCacheMonthly | Kiekis                   | CostObjectStatementCache               | Kiekis                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Toliau pateikiamoje lentelėje nurodyti pagrindiniai apskaičiuoti „Power BI“ turinio matavimo vienetai.

| Mato vnt.                            | Skaičiavimas |
|------------------------------------|-------------|
| Pradinis balansas                  | Pradžios balansas = \[pabaigos balansas\] - \[grynasis pokytis\] |
| Pradžios balanso kiekis             | Pradžios balanso kiekis = \[pabaigos balanso kiekis\] - \[grynojo pokyčio kiekis\] |
| Pabaigos likutis                     | Galutinis balansas = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Pabaigos balanso kiekis                | Galutinio balansas kiekis = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Grynasis pokytis                         | Grynasis pokytis = SUM(\[AMOUNT\]) |
| Grynojo pokyčio kiekis                    | Grynojo pokyčio kiekis = SUM(\[QTY\]) |
| Atsargų apyvartos koeficientas pagal sumą | Atsargų apyvartos koeficientas pagal sumą = if(OR(\[vidutinis atsargų balansas\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[parduotų arba sunaudotų atsargų problemos\])/\[vidutinis atsargų balansas\]) |
| Vidutinis atsargų balansas          | Vidutinis atsargų balansas = ((\[galutinis balansas\]  +  \[pradžios balansas\]) / 2) |
| Turimų atsargų dienos             | Turimų atsargų dienos = 365 / CostObjectStatementEntries\[atsargų apyvartos koeficientas pagal sumą\] |
| Atsargų tikslumas                 | Atsargų tikslumas pagal sumą = IF(\[pabaigos balansas\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[pabaigos balansas\] \< 0), 0, 1), MAX(0, (\[pabaigos balansas\] - ABS(\[apskaičiuota atsargų suma\]))/\[pabaigos balansas\])) |

Tolesnės pagrindinės dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti didesnį detalumą ir gauti gilesnių analitinių įžvalgų.


| Objektas                                                  | Atributų pavyzdžiai                          |
|---------------------------------------------------------|-------------------------------------------------|
| Produktai                                                | Produkto numeris, produkto pavadinimas, vienetas, prekių grupės |
| Kategorijų hierarchijos (priskirtos išlaidų valdymo vaidmeniui) | Kategorijų hierarchija, kategorijos lygis              |
| Juridiniai subjektai                                          | Juridinių subjektų pavadinimai                              |
| Finansiniai kalendoriai                                        | Finansinis kalendorius, metai, ketvirtis, laikotarpis, mėnuo   |
| Svetainė                                                    | ID, pavadinimas, adresas, valstybė, šalis               |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

