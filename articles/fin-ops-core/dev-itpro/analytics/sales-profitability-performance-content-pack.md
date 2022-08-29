---
title: „Power BI“ turinys Pardavimo ir pelningumo našumas
description: Šiame straipsnyje aprašoma, kas įtraukta į pardavimo ir pelningumo našumo Power BI turinį.
author: Henrikan
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.form: SalesProfitabilityPerformancePowerBI
ms.openlocfilehash: 77271ad9f5a1d7c131e1d7750de280f0c70daaa4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274666"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>„Power BI“ turinys Pardavimo ir pelningumo našumas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kas įtraukta į pardavimo ir **pelningumo našumo** Microsoft Power BI turinį. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Pardavimo ir pelningumo našumas** buvo sukurtas tam, kad pardavimo vadovai galėtų stebėti pagrindines pardavimo metrikas – įplaukas, bendrąjį pelną ir pelno maržas. Jame naudojami pardavimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pardavimo skaičių rodinys, tiek klientų ir produktų pardavimo našumo analizė.

Ataskaitose perteikiama, kaip laikui bėgant kinta įplaukų ir pelno augimas. Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų klientų ir produktų tendencijas. Be to, diagramomis vienų su kitais lyginamos skirtingų produktų kategorijų ir klientų grupių įplaukos bei pelningumas. Todėl kategorijų ir regionų vadovai gali nustatyti atsiliekančiuosius ir pirmaujančiuosius. Galiausiai išsamioje ataskaitoje atskiro kliento įplaukos lyginamos su pelno marža. Todėl klientų vadovai turi duomenimis pagrįstas pagrindą, kurį naudodami gali savo pardavimo ir rinkodaros pastangas derinti pagal kiekvieno kliento profilį.

Naudodami turinį **Pardavimo ir pelningumo našumas** pardavimo vadovai pardavimo našumą gali analizuoti tolesniais būdais.

- Įplaukos, metinės iki datos (pagal klientų grupę ir atskirus klientus, pardavimo kategorijas, atskirus produktus ir regionus)
- Įplaukų pasikeitimas, metams bėgant (pagal klientų regionus ir pardavimo kategorijas)

Pelningumą galima analizuoti tolesniais būdais.

- bruto pelną ir pelno maržą (pagal klientų grupes ir produkto pardavimo kategorijas);
- bruto pelno pokytį, metams bėgant;
- kliento pelningumą (pagal įplaukas, lyginant su marža).

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Pardavimo ir pelningumo našumas** rodomas puslapyje **Pardavimo ir pelningumo našumas** (**Pardavimas ir rinkodara** \> **Užklausos ir ataskaitos** \> **Pardavimo efektyvumo analizė** \> **Pardavimo ir pelningumo našumas**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
„Power BI“ turinio pakete **Pardavimo ir pelningumo našumas** yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės Toliau pateiktoje lentelėje pateikiama turinio vizualizacijų apžvalga.

| Ataskaitų puslapis            | Diagramos                                     | Išklotinės                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Įplaukos pagal klientą    | 10 svarbiausių klientų pagal įplaukas                | Bendros įplaukos                                           |
|                        | Bendros įplaukos pagal kliento grupę            | Įplaukų augimas bėgant metams                                      |
|                        | Vidutinės kliento įplaukos pagal kliento grupę | Bruto marža                                            |
|                        | Įplaukos ir bruto pelnas pagal kliento grupę   |                                                         |
| Įplaukos pagal produktą     | Įplaukos ir bruto pelnas pagal pardavimo kategoriją   | Iš viso \# produktų                                    |
|                        | 10 svarbiausių produktų pagal įplaukas                 | Bendras skaičius aktyvių produktų ir procentais nuo bendros sumos |
|                        | Bendros įplaukos pagal pardavimo kategoriją            | Produktų, sudarančių 80 % įplaukų, skaičius           |
| Įplaukos pagal laikotarpį\*    | Įplaukos pagal mėnesį                           | Įplaukų augimas bėgant metams                                      |
|                        | Paskutinių įplaukų nuokrypis, bėgant metams             | Įplaukų augimas bėgant metams %                                    |
|                        | Bendras pardavimų nuokrypis pagal kliento regioną    |                                                         |
| Įplaukos pagal vietą    | Pardavimo įplaukos pagal miestą                      |                                                         |
|                        | Įplaukų augimas bėgant metams %                       |                                                         |
|                        | Pardavimo įplaukos pagal regioną                    |                                                         |
| Kliento pelningumas | Bruto marža, lyginant su įplaukomis, pagal klientą   | Bruto pelnas, bruto marža, įplaukų augimas bėgant metams          |
| Pelningumo analizė | Įplaukos ir bruto pelnas pagal mėnesį          |                                                         |
|                        | 15 svarbiausių klientų pagal bruto maržą           |                                                         |
|                        | Bruto pelnas pagal mėnesį, bėgant metams                 |                                                         |

\* įplaukos šiais ir praėjusiais metais ir augimas pagal pardavimo kategoriją.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Tolesniais duomenimis pildoma „Power BI“ turinio **Pardavimo ir pelningumo našumas** ataskaita. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Sujungti šio turinio matavimai yra sudedamųjų matavimų, Microsoft Dynamics AX kurie buvo galimi pardavimo kube 2012 ir 2012 Microsoft Dynamics AX R3, subgrupiniai matavimai. Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus. Išsamesnės informacijos žr. tinklaraščio įraše [„Power BI“ integravimas su objekto parduotuve programoje „Dynamics“](/archive/blogs/dynamicsaxbi/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update) pateiktą procedūrą, kaip perkelti agreguotus matavimo vienetus į kitą vietą objekto parduotuvėje.

Kaip turinio pagrindas naudojami šie pagrindiniai agreguoti objekto Sąskaitos faktūros eilutės matavimo vienetai.

| Objektas        | Pagrindiniai agreguoti matavimo vienetai                   | „Dynamics 365“ duomenų šaltinis | Laukas                                        | aprašymas                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| SF eilutės | Įplaukos                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Suma, išreikšta apskaitos valiuta.            |
|               | Parduotų prekių savikaina                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | Išlaidų sumos ir koregavimo suma.    |
|               | Komisinių eilutės suma – apskaitos valiuta | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Komisinių suma, išreikšta apskaitos valiuta. |

Tolesnėje lentelėje parodyti pagrindiniai agreguoti objekto Sąskaitos faktūros eilutės matavimo vienetai, kurie naudojami kuriant kelis apskaičiuojamus matus turinio duomenų rinkinyje.

| Mato vnt.           | Skaičiavimas                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bendrasis pelnas      | SUM(įplaukos – PPK – komisiniai – PVM (įtrauktas į kliento SF eilutės sumą))          |
| Bruto marža      | SUM(bruto pelnas / (įplaukos - PVM (įtrauktas į kliento SF eilutės sumą)))             |
| Praėjusių metų įplaukos | Praėjusių metų įplaukos = CALCULATE(SUM('SF eilutės'\[įplaukos\]), SAMEPERIODLASTYEAR(datos\[data\]) |

Toliau nurodytos pagrindinės pardavimo kubo dimensijos naudojamos kaip filtrai sujungtiems matavimams skaidyti, kad būtų galima pasiekti didesnio tikslumo ir gauti daugiau analitinių žinių.

| Objektas           | Atributų pavyzdžiai                               |
|------------------|------------------------------------------------------|
| Klientai        | Klientų grupės, klientų regionai, adresai, rinka |
| Produktai         | Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas       |
| Pardavimo kategorijos | Pardavimo kategorijų pavadinimai                                 |
| Juridiniai subjektai   | Juridinių subjektų pavadinimai                                   |
| Datos            | Datos                                                |

Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys. Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti. Taip pat galite pakeisti įmonės filtrą.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
