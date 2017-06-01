---
title: "Pardavimo ir pelningumo našumo „Power BI“ turinys"
description: "Šioje temoje paaiškinta, kas įtraukiama į „Microsoft Dynamics 365 for Operations“ pardavimo ir pelningumo našumo turinio paketą, skirtą „Microsoft Power BI“. Jame paaiškinta, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 357f7071d801b13518c83170f8d0e7946dd9dede
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Pardavimo ir pelningumo našumo „Power BI“ turinys

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinta, kas įtraukiama į „Microsoft Dynamics 365 for Operations“ pardavimo ir pelningumo našumo turinio paketą, skirtą „Microsoft Power BI“. Jame paaiškinta, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

<a name="overview"></a>Apžvalga
--------

Šis turinio paketas sukurtas pardavimo vadovams, pagrindinėms pardavimo įplaukų, bruto pelno ir pelno maržos metrikoms stebėti. Jame naudojami pardavimo operacijų duomenys iš „Dynamics 365 for Operations“, pateikiamas ir sujungtas visos įmonės pardavimo skaičių rodinys, ir klientų, ir produktų pardavimo našumo paskirstymas. Pabrėžiant įplaukų ir pelno pakitimus per tam tikrą laikotarpį, ataskaitas galima naudoti, norint įspėti vadovus apie teigiamas ir neigiamas atskirų klientų ir produktų tendencijas. Kategorijų ir regionų vadovams bus naudinga turėti diagramas, tarpusavyje lyginančias įvairių produktų kategorijų ir klientų grupių įplaukas ir pelną, išryškinančias atsiliekančius ir pirmaujančius. Išsamioje ataskaitoje, atskiro kliento įplaukas lyginant su pelno marža, vadovams pateikia duomenimis pagrįstą pagrindą, norint suderinti jų pardavimo ir rinkodaros pastangas su atitinkamu kiekvieno kliento šablonu. Pardavimo ir pelningumo našumo turinio paketas pardavimo vadovams leidžia analizuoti pardavimo našumą pagal:

-   Įplaukos, metinės iki datos (pagal klientų grupę ir atskirus klientus, pardavimo kategorijas, atskirus produktus ir regionus)
-   Įplaukų pasikeitimas, metams bėgant (pagal klientų regionus ir pardavimo kategorijas)

Pelningumą galima analizuoti pagal:

-   bruto pelną ir pelno maržą (pagal klientų grupes ir produkto pardavimo kategorijas);
-   bruto pelno pokytį, metams bėgant;
-   kliento pelningumą (pagal įplaukas, lyginant su marža).

## <a name="accessing-the-content-pack"></a>Prieiga prie turinio paketo
Pardavimo ir pelningumo našumo turinio paketas „Power BI“ išleistas kaip „Lifecycle Services“ (LCS) diegimo išteklius ir yra pasiekiamas iš „Dynamics 365 for Operations“. Išsamesnės informacijos apie tai, kaip pasiekti ir paleisti „Power BI“ ataskaitas žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).
**Pastaba:** KB 4011327 yra būtinoji šio „Power BI“ turinio sąlyga. Prisijungę prie „Lifecycle Services“ galite pasiekti KB čia: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>Į turinio paketą įtrauktos metrikos
Turinio pakete yra ataskaita, sudaryta iš metrikų, pavaizduotų diagramomis, išklotinėmis ir lentelėmis, rinkinio. Toliau pateiktoje lentelėje pateikiama turinio paketo vizualizacijų apžvalga.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Ataskaitų puslapis**        | **Diagramos**                                 | **Išklotinės**                                               |
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
„Dynamics 365 for Operations“ duomenys naudojami ataskaitai užpildyti pardavimo ir pelningumo našumo turinio pakete. Tai pateikiama agreguotais matavimo vienetais, paskirstytais objekto parduotuvėje, kuri yra „Microsoft SQL“ analizei atlikti optimizuota duomenų bazė. Daugiau apie tai skaitykite tinklaraštyje [„Power BI“ integravimas su objekto parduotuve programoje „Dynamics“](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Agreguoti matavimo vienetai šiame turinio pakete yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Sales Cube in Dynamics AX 2012“ ir AX 2012 R3, subrinkinys. Norint perkelti kubo agreguotus matavimo vienetus į objekto parduotuvę, reikia padaryti juos įdiegiamus. Išsamesnės informacijos žr. tinklaraštyje pateiktą procedūrą, kaip perkelti agreguotus matavimo vienetus į objekto parduotuvę [„Power BI“ integravimas su objekto parduotuve programoje „Dynamics“](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Šie pagrindiniai agreguoti matavimo vienetai iš sąskaitos faktūros eilučių objekto naudojami kaip turinio paketo pagrindas.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Objektas**    | **Pagrindiniai agreguoti matavimo vienetai**               | **„Dynamics 365 for Operations“ duomenų šaltinis** | **Laukas**                                    | **Aprašas**                          |
| SF eilutės | Įplaukos                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Suma, išreikšta apskaitos valiuta            |
|               | Parduotų prekių savikaina                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Išlaidų suma + koregavimas                 |
|               | Komisinių eilutės suma – apskaitos valiuta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisinių eilutės suma apskaitos valiuta |

Šioje lentelėje parodyti pagrindiniai agreguotų matavimo vienetų iš sąskaitos faktūros eilučių objekto, kurie naudojami kuriant kelis apskaičiuojamus kriterijus turinio paketo duomenų rinkinyje.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Matas**       | **Apskaičiuota kaip**                                                                                |
| Bendrasis pelnas      | SUM(įplaukos – PPK – komisiniai – PVM (įtrauktas į kliento SF eilutės sumą))          |
| Bruto marža      | SUM(bruto pelnas / (įplaukos - PVM (įtrauktas į kliento SF eilutės sumą)))             |
| Praėjusių metų įplaukos | Praėjusių metų įplaukos = CALCULATE(SUM('SF eilutės'\[įplaukos\]), SAMEPERIODLASTYEAR(datos\[data\]) |

Šios pagrindinės dimensijos **Pardavimo kubas** naudojamos kaip filtrai agreguotiems matavimo vienetams susegmentuoti, siekiant didesnio detalumo ir gilesnių analitinių įžvalgų.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Objektas**       | **Atributų pavyzdžiai**                           |
| Klientai        | Klientų grupės, klientų regionai, adresai, rinka |
| Produktai         | Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas       |
| Pardavimo kategorijos | Pardavimo kategorijų pavadinimai                                 |
| Juridiniai subjektai   | Juridinių subjektų pavadinimai                                   |
| Datos            | Datos                                                |

Pagal numatytuosius nustatymus, turinio paketas rodo šių kalendorinių metų duomenis, tačiau galite atidaryti ataskaitos filtrų skyrių ir keisti datos filtrą. Taip pat galite pakeisti įmonės filtrą.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)





