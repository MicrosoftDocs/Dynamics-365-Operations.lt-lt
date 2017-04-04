---
title: Finansinio efektyvumo Power BI turinys
description: "Šioje temoje aprašoma &quot;Microsoft Dynamics 365 veiklos finansinių rezultatų turinio paketą, skirtą&quot; Microsoft &quot;Power BI&quot;. Aprašomas ataskaitų srities ir ataskaitų, kurie yra įtraukti į turinio pack, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinio paketas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Finansinio efektyvumo Power BI turinys

Šioje temoje aprašoma "Microsoft Dynamics 365 veiklos finansinių rezultatų turinio paketą, skirtą" Microsoft "Power BI". Aprašomas ataskaitų srities ir ataskaitų, kurie yra įtraukti į turinio pack, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinio paketas.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketas
--------------------------

Yra dvi versijos finansinių rezultatų turinio paketas. Viena versija yra prieinama iš Microsoft Dynamics gyvavimo ciklo paslaugų (LCS), ir kita yra iš PowerBI.com.

-   **Versija, kuri yra prieinama iš LKD:** The finansinių rezultatų turinio paketas, kurį galite atsisiųsti iš LKD palaiko Microsoft Dynamics 365 operacijų versija 1611. Kiekis pakuotėje rasite bendro naudojimo turto bibliotekoje LKD. Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie savo "Microsoft Dynamics 365" operacijų duomenų, rasite [LCS iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md).
-   **Versija, kuri yra prieinama iš PowerBI.com:** The finansinių rezultatų turinio paketą, kurį galite atsisiųsti iš PowerBI.com palaiko Microsoft Dynamics AX versijos 7.0 ir 7.0.1. Daugiau informacijos apie tai, kaip prisijungti ir įkelti savo dinamika 365 operacijų duomenis, rasite [turinio prieigos Power BI PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Pagrindinio abonemento nustatymas
Nes organizacijų įsipareigojimų ir pajamų sumos nurodomos kaip teigiamos sumos ataskaitose, pagrindinės sąskaitos dinamika 365 operacijoms nustatymas yra svarbus. Šie pagrindiniai sąskaitose nurodomos kaip teigiamos sumos, pagrindinės sąskaitos tipas turi būti nustatytas kaip **atsakomybę** ar **pajamos**. Kai naudojami šių abonementų tipų, per "Microsoft" Power BI ataskaitų bus pakeisti požymius ir kaip teigiamas sumas.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Ataskaitų sritis ir ataskaitas, kurios yra įtrauktos į turinio paketas
Prijungus turinio paketą prie „Dynamics 365 for Operations“ duomenų, ataskaitų srityje ir ataskaitose rodomi jūsų finansiniai duomenys. Jei niekada nenaudojote Power BI prieš, galite sužinoti daugiau apie tai apie su [vadovaujasi mokymosi puslapis, Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Ataskaitų srityje pateikiamos apibendrintos esamomis ataskaitomis pagrįstų duomenų plytelės. Kiekvienoje plytelėje pateikiama apibendrinta šių metų informacija apie visas įmones organizacijoje. Štai keletas plytelės:

-   Grynieji pinigai
-   Visos įplaukos šiais metais
-   Visos išlaidos šiais metais
-   Grynosios pajamos šiais metais
-   Spartusis koeficientas
-   Bendrosios išlaidos šiais metais pagal sąskaitos kategoriją
-   Dabartinis koeficientas
-   Skola, palyginus su visu turtu
-   Faktinės ir prognozuojamos įplaukos
-   Šių metų įplaukos, kurioms išrašyta sąskaita
-   Veiklos išlaidų koeficientas šiais metais
-   Pelno marža šiais metais
-   Faktinės ir biudžeto išlaidos – visos įmonės

Kiekviena plytelių remia patvirtinamuosius ataskaitą. Šiose ataskaitose yra diagramos ir lentelės, kurios teikia daugiau informacijos. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                      | Ataskaitoje pateikiama informacija                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grynųjų pinigų analizė               | Pinigų iš juridinio asmens, pinigų kvartalą, visų grynųjų pinigų ir pinigų iš sąskaitos **Pastaba:** ir **pinigų iš ketvirčio** ataskaita neapima pradžios likučiai viso pirmojo ketvirčio. Tai rodo naujos operacijos, kurios registruojamos kiekvieną ketvirtį.                                                                                |
| Dabartinio koeficiento analizė      | Dabartinis koeficientas pagal juridinį subjektą, dabartinis koeficientas pagal ketvirtį ir trumpalaikio turto bei trumpalaikių įsipareigojimų balansai                                                                                                                                                                                                                              |
| Sparčiojo koeficiento analizė        | Greitai santykis iš juridinio asmens, greitai santykis su kvartalo ir balansus už pinigus, sudaro gautinų sumų ir dabartinių įsipareigojimų                                                                                                                                                                                                                      |
| Parduotų prekių savikainos analizė | Parduotų prekių savikaina (PPK) pagal juridinį subjektą, PPK šiais metais ir praėjusiais metais pagal ketvirtį, PPK ir pardavimas pagal juridinį subjektą, bendroji PPK bei PPK ir pardavimo procentas                                                                                                                                                                                   |
| Apyvartinio kapitalo analizė    | Apyvartinis kapitalas pagal juridinį subjektą, apyvartinis kapitalas pagal ketvirtį, trumpalaikis turtas, trumpalaikiai įsipareigojimai ir visas apyvartinis kapitalas                                                                                                                                                                                                                   |
| Turto ir skolos analizė     | Bendro turto grąža ir skola, palyginti su bendru turtu, pagal juridinį subjektą, skola, palyginti su bendru turtu, ir bendro turto grąža ketvirtį iki dienos, turtas ir įsipareigojimai                                                                                                                                                                                     |
| Pelno maržos analizė      | Faktinė ir biudžeto pelno marža pagal juridinį subjektą, pelno žymėjimas pagal ketvirtį, pelno maržos procentas ir pelno marža                                                                                                                                                                                                                       |
| Grynųjų pinigų analizė         | Faktinės ir biudžeto grynosios pajamos pagal juridinį subjektą, grynosios pajamos šiais metais ir praėjusiais metais bei išlaidos ir grynųjų pinigų procentas                                                                                                                                                                                                                       |
| Pajamų analizė           | Faktinės ir biudžeto pajamos prieš palūkanas ir mokesčius (EBIT) pagal juridinį subjektą, EBIT šiais metais ir praėjusiais metais, išlaidos ir įplaukų procentas, faktinės bei biudžeto išlaidos ir įplaukos                                                                                                                                                          |
| Įplaukų analizė            | Bendrosios įplaukos, faktinės ir biudžeto bendrosios įplaukos pagal juridinį subjektą, bendrosios įplaukos šiais metais ir praėjusiais metais, įplaukų biudžeto nuokrypis pagal juridinį subjektą ir bendrosios įplaukos šį laikotarpį ir paskutinįjį laikotarpį                                                                                                                                                 |
| Išlaidų analizė            | Bendrosios išlaidos, faktinės ir biudžeto bendrosios išlaidos pagal juridinį subjektą, faktinės ir biudžeto bendrosios išlaidos pagal ketvirtį, bendrosios išlaidos pagal sąskaitos kategoriją ir veiklos išlaidų koeficientas                                                                                                                                                                 |
| Įplaukų, kurioms išrašyta sąskaita, analizė     | Iš viso gautinos sąskaitos, viso gautinos iš juridinio asmens, viso gautinos iš ketvirčio, o likučius gautinų sumų sąskaitoms **Pastaba:** ataskaitas ne įraukti pradžios balansus už sąskaitos gautinas DK sąskaitas. Jie rodo naują operacijų, kurios registruojamos sąskaitos gautinas suma. |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Prietaisų skydelyje ir finansinių rezultatų turinio paketą, apie juose esančius duomenis yra Dynamics 365 operacijų duomenis. Šie subjektai buvo remiamasi turinio paketą: **kaupti duomenų subjektų**

-   **GeneralLedgerActivities** – šios organizacijos kaupia DK likučiai iš sąskaitų kategoriją.
-   **BudgetActivities** – šios organizacijos kaupia biudžeto balansai iš sąskaitų kategoriją.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Didžiosios knygos
-   ChartofAccounts

Šių subjektų buvo naudojama siekiant sukurti apskaičiuojamieji matai duomenų modelio. Apskaičiuojamieji matai naudojami norint apskaičiuoti pagrindinius veiklos rodiklius (KPI) ir ataskaitų, kurias naudoja turinio paketas. Pagal numatytuosius parametrus turinio paketas pastarųjų trejų metų duomenis sutelkia į vienerius būsimus metus. Norėdami ataskaitas ir ataskaitų sritį įtraukti papildomų skaičiavimų, galite modifikuoti [„Microsoft Excel“ darbaknygę](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Ši darbaknygė yra numatytasis duomenų modelis, kuris buvo naudojamas turinio paketui kurti. Atlikę keitimus, galite kurti organizacinį turinio paketą ir ataskaitų sritį, kuriuose yra jūsų įtraukta informacija.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)



