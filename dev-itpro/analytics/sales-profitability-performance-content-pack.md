---
title: "Pardavimų ir pelningumo efektyvumo Power BI turinys"
description: "Šioje temoje aprašoma, kas yra įskaičiuota į Dynamics 365 operacijų - pardavimų ir pelningumo veiklos turinio paketas, skirtas Microsoft Power BI. Jis paaiškina, kaip jas pasiekti turinio pakuotėje ir pateikia informaciją apie duomenų modelio ir subjektai, kurie yra naudojami kurti turinio paketas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Pardavimų ir pelningumo efektyvumo Power BI turinys

Šioje temoje aprašoma, kas yra įskaičiuota į Dynamics 365 operacijų - pardavimų ir pelningumo veiklos turinio paketas, skirtas Microsoft Power BI. Jis paaiškina, kaip jas pasiekti turinio pakuotėje ir pateikia informaciją apie duomenų modelio ir subjektai, kurie yra naudojami kurti turinio paketas.

<a name="overview"></a>Apžvalga
--------

Šis kiekis pakuotės buvo sukurta pardavimų vadybininkai stebėti pagrindinius pardavimo rodiklius pajamos, Bendrasis pelnas ir pelnas. Jis naudoja Dynamics 365 pardavimo operacijų duomenis operacijoms, o ir bendras vaizdas į visos įmonės pardavimų skaičių ir pardavimo efektyvumo analizę numato klientų bei produktų. Išryškinti pokyčius pajamų ir pelno augimą per tam tikrą laiką, ataskaitas galima įspėjimo vadovams apie teigiamas ir neigiamas tendencijas, individualių klientų ir produktų. Kategorijos ir regioniniai vadovai rasite tai naudinga turėti diagramas, palyginti pajamas ir pelningumą padidino skirtingų produktų kategorijų ir klientų grupių tarpusavyje išskirti atsilikusiems ir vadovai. Išsamią ataskaitą, kurioje vaizduojami atskiro pirkėjo pajamų ir pelno maržą siūlo sąskaitos valdytojų duomenys paremti Fondo pripratinti savo pardavimų ir rinkodaros pastangas į atitinkamus kiekvieno kliento profilį. Pardavimų ir pelningumo veiklos turinio paketas leidžia analizuoti pardavimo efektyvumo iš pardavimo vadybininkai:

-   Pajamos, metai iki datos (pagal klientų grupei ir atskiriems klientams, pardavimo kategorijas, ir atskirų produktų ir geografijos)
-   Pajamų pokytis, metų per metus (pagal kliento regionų ir pardavimo kategorijas)

Pelningumas gali būti analizuojami:

-   Bendrojo pelno ir pelno skirtumą (pagal klientų grupes ir produktų pardavimo kategorijos)
-   Bendrojo pelno pokytis, metų per metus
-   Klientų pelningumas (iš pajamų ir bendrojo pelno)

## <a name="accessing-the-content-pack"></a>Prieiga prie turinio paketas
Pardavimų ir pelningumo efektyvumo Power BI turinio paketas skelbiamas įgyvendinant turto gyvavimo ciklo paslaugų (LCS) ir gali būti pasiekiami iš Dynamics 365 operacijoms. Daugiau informacijos apie tai, kaip pasiekti ir paleisti Power BI ataskaitų, rasite [LKD iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Rodikliai kiekis pakuotėje
Turinio paketą sudaro ataskaitą, kuri susideda iš metrikos ryškinamos diagramas, plytelės ir lentelių rinkinys. Šioje lentelėje apžvelgiami turinio Pack vizualizaciją.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Ataskaitų puslapio**        | **Charts**                                 | **Plytelės**                                               |
| Įplaukos iš pirkėjų    | 10 populiariausių klientų iš pajamų                | Bendros įplaukos                                           |
|                        | Iš viso pajamų iš klientų grupės            | YOY pajamų augimo                                      |
|                        | Vidutinis kliento pajamas iš klientų grupės | Bruto marža                                            |
|                        | Pajamų ir bendrojo pelno iš klientų grupės   |                                                         |
| Pajamų pagal produktus     | Pajamų ir bendrojo pelno iš pardavimų kategorija   | Iš viso \#produktus                                    |
|                        | 10 geriausių produktų iš pajamų                 | Iš viso aktyvių produktų ir procentais nuo visos reikšmės |
|                        | Iš viso pajamų iš pardavimų kategorija            | Produktus, kurie sudaro apie 80 % pajamų skaičius           |
| Pajamos iš laikotarpio\*    | Pajamų pagal mėnesį                           | YOY pajamų augimo                                      |
|                        | Gale pajamų nuokrypis, YOY             | YOY pajamų augimo %                                    |
|                        | Bendra pardavimo nukrypimo iš klientų regionas    |                                                         |
| Pajamų pagal vietovę    | Pardavimo pajamos pagal miestą                      |                                                         |
|                        | YOY pajamų augimo %                       |                                                         |
|                        | Pardavimo pajamos pagal regionus                    |                                                         |
| Klientų pelningumas | Bendrasis pelningumas, palyginti su pajamų, klientas   | Bendrasis pelnas, Bendrasis pelningumas, YOY pajamų augimo          |
| Pelningumo analizė | Pajamų ir bendrojo pelno pagal mėnesį          |                                                         |
|                        | 15 geriausių klientai iš bendrojo pelno           |                                                         |
|                        | Bendrasis pelnas mėnesiu, YOY                 |                                                         |

\*Pajamos tai ir praėjusius metus, ir augimo pardavimo kategorijas.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Dinamika 365 operacijų duomenys yra naudojamas užpildyti ataskaitą pardavimų ir pelningumo veiklos turinio paketas. Tai is sudarė as bendra matavimų, kurie yra pastatytas įmonės parduotuvėje, kuri yra optimizuota Google analytics Microsoft SQL duomenų bazę. Skaityti daugiau apie tai blogas [Power BI integracija su įmonės parduotuvėje dinamikai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Bendra matavimų šio turinio Pack yra sutrumpinti bendrą matavimų, kuriais galėjote naudotis pardavimo kubui Dynamics AX 2012 ir AX 2012 R3. Į sceną kubo bendra matavimų subjektas parduotuvėje galite daryti išskleidimo. Norėdami gauti daugiau informacijos, žiūrėkite procedūrą, kaip į sceną į įmonės parduotuvę Dienoraštis bendra matavimų [Power BI integracija su įmonės parduotuvėje dinamikai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Šie pagrindiniai bendra matavimai SF eilutes subjektas yra remiamasi turinio paketas.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Bendra atliekami pagrindiniai matavimai**               | **Duomenų šaltinis Dynamics 365 operacijoms** | **Field**                                    | **Description**                          |
| SF eilutės | Įplaukos                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Suma, išreikšta apskaitos valiuta            |
|               | Parduotų prekių savikaina                           | InventTrans                                     | SUMA (CostAmountPosted + CostAmountAdjustment) | Savikainos suma + koregavimas                 |
|               | Komisija eilutės suma – numatytąja valiuta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisinių suma numatytąja valiuta |

Šioje lentelėje yra pagrindinė bendra matavimų SF eilutes subjekto, kurie naudojami sukurti keletą apskaičiuojamieji matai turinio paketo duomenų rinkinyje.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Perskaičiavus į**                                                                                |
| Bendrasis pelnas      | SUMA (pajamos – parduotų – Komisija – PVM (įtrauktos į kliento SF eilutės suma))          |
| Bruto marža      | SUMA (Bendrasis pelnas / (pajamų - PVM (įtrauktos į kliento SF eilutės suma)))             |
| Pajamų praėjusiais metais | Pajamos pernai = skaičiuoti (suma ("SF eilutės"\[pajamos\]), SAMEPERIODLASTYEAR (datos\[data\]) |

Šių pagrindinių matmenų – į **pardavimo kubui** yra naudojamas kaip filtrų Supjaustykite bendra matavimų siekti didesnio detalumo ir gilesnių analitinių įžvalgų.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Atributų pavyzdžiai**                           |
| Klientai        | Klientų grupes, klientų regionuose, adresas, pramonės |
| Produktai         | Gaminio numeris, produkto pavadinimas, prekės grupės pavadinimas       |
| Pardavimo kategorijos | Pardavimo kategorijų pavadinimai                                 |
| Juridiniai subjektai   | Juridinio asmens vardai                                   |
| Datos            | Datos                                                |

Pagal numatytuosius nustatymus turinio paketas rodo duomenų einamaisiais kalendoriniais metais, bet galite atidaryti ataskaitą filtrai skyrių ir pakeisti datos filtras. Taip pat galite keisti įmonės filtras.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)



