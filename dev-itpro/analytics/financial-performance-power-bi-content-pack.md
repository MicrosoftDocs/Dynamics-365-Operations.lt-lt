---
title: "Finansinės veiklos „Power BI“ turinys"
description: "Šioje temoje aprašomas „Microsoft Dynamics 365 for Operations“ finansinės veiklos turinio paketas, skirtas „Microsoft Power BI“. Joje aprašomos į turinio paketą įtrauktos ataskaitų sritys ir ataskaitos bei pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9cd1d7e5b7b1fd892034dcca0a0c141363104a45
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Finansinės veiklos „Power BI“ turinys

[!include[banner](../includes/banner.md)]


Šioje temoje aprašomas „Microsoft Dynamics 365 for Operations“ finansinės veiklos turinio paketas, skirtas „Microsoft Power BI“. Joje aprašomos į turinio paketą įtrauktos ataskaitų sritys ir ataskaitos bei pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketo
--------------------------

Galima rinktis iš dviejų finansinės veiklos turinio paketo versijų. Vieną versiją galimą gauti iš „Microsoft Dynamics Lifecycle Services“ (LCS), o kitą – iš PowerBI.com.

-   **Versija, kurią galima gauti iš LCS.** Finansinės veiklos turinio paketo versija, kurią galima gauti iš LCS, palaiko 1611 „Microsoft Dynamics 365 for Operations“ versiją. Turinio paketą galite rasti LCS bendrai naudojamo turto bibliotekoje. Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie „Microsoft Dynamics 365 for Operations“ duomenų, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).
-   **Versija, kurią galima gauti iš PowerBI.com.** Finansinės veiklos turinio paketo versija, kurią galima gauti iš PowerBI.com, palaiko 7.0 ir 7.0.1 „Microsoft Dynamics AX“ versijas. Daugiau informacijos apie tai, kaip prijungti ir nusiųsti „Dynamics 365 for Operations“ duomenis, žr. [Prieiga prie 0„Power BI“ turinio naudojant PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Pagrindinių sąskaitų sąranka
Kadangi organizacijos nori, jog įsipareigojimai ir įplaukų sumos ataskaitose būtų rodomos kaip teigiamos sumos, svarbu nustatyti pagrindines sąskaitas „Dynamics 365 for Operations“. Tam, kad šios pagrindinės sąskaitos būtų rodomos kaip teigiamos sumos, turi būti nustatytas pagrindinės sąskaitos tipas **Įsipareigojimas** arba **Įplaukos**. Kai naudojami šie sąskaitų tipai, ataskaitas teikiant per „Microsoft Power BI“ ženklai pakeičiami ir rodomos teigiamos sumos.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos ataskaitų sritys ir ataskaitos
Prijungus turinio paketą prie „Dynamics 365 for Operations“ duomenų, ataskaitų srityje ir ataskaitose rodomi jūsų finansiniai duomenys. Jei niekada nenaudojote „Power BI“, daugiau apie tai galite sužinoti temoje [„Power BI“ mokymosi vedlio puslapis](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Ataskaitų srityje pateikiamos apibendrintos esamomis ataskaitomis pagrįstų duomenų plytelės. Kiekvienoje plytelėje pateikiama apibendrinta šių metų informacija apie visas įmones organizacijoje. Toliau pateikiamos kai kurios plytelės.

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

Kiekviena plytelė yra pagrindžiama papildoma ataskaita. Šiose ataskaitose yra diagramos ir lentelės, kurios teikia daugiau informacijos. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                      | Ataskaitoje pateikiama informacija                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grynųjų pinigų analizė               | Grynieji pinigai pagal juridinį subjektą, grynieji pinigai pagal ketvirtį, visa grynųjų pinigų suma ir grynieji pinigai pagal sąskaitą **Pastaba.** Ataskaitoje **Grynieji pinigai pagal ketvirtį** į bendrą pirmo ketvirčio sumą neįtraukiami pradžios balansai. Joje rodoma naujų operacijų, užregistruotų kiekvieną ketvirtį, bendra suma.                                                                                |
| Dabartinio koeficiento analizė      | Dabartinis koeficientas pagal juridinį subjektą, dabartinis koeficientas pagal ketvirtį ir trumpalaikio turto bei trumpalaikių įsipareigojimų balansai                                                                                                                                                                                                                              |
| Sparčiojo koeficiento analizė        | Spartusis koeficientas pagal juridinį subjektą, spartusis koeficientas pagal ketvirtį ir grynųjų pinigų, gautinų sumų bei trumpalaikių įsipareigojimų balansai                                                                                                                                                                                                                      |
| Parduotų prekių savikainos analizė | Parduotų prekių savikaina (PPK) pagal juridinį subjektą, PPK šiais metais ir praėjusiais metais pagal ketvirtį, PPK ir pardavimas pagal juridinį subjektą, bendroji PPK bei PPK ir pardavimo procentas                                                                                                                                                                                   |
| Apyvartinio kapitalo analizė    | Apyvartinis kapitalas pagal juridinį subjektą, apyvartinis kapitalas pagal ketvirtį, trumpalaikis turtas, trumpalaikiai įsipareigojimai ir visas apyvartinis kapitalas                                                                                                                                                                                                                   |
| Turto ir skolos analizė     | Bendro turto grąža ir skola, palyginti su bendru turtu, pagal juridinį subjektą, skola, palyginti su bendru turtu, ir bendro turto grąža ketvirtį iki dienos, turtas ir įsipareigojimai                                                                                                                                                                                     |
| Pelno maržos analizė      | Faktinė ir biudžeto pelno marža pagal juridinį subjektą, pelno žymėjimas pagal ketvirtį, pelno maržos procentas ir pelno marža                                                                                                                                                                                                                       |
| Grynųjų pinigų analizė         | Faktinės ir biudžeto grynosios pajamos pagal juridinį subjektą, grynosios pajamos šiais metais ir praėjusiais metais bei išlaidos ir grynųjų pinigų procentas                                                                                                                                                                                                                       |
| Pajamų analizė           | Faktinės ir biudžeto pajamos prieš palūkanas ir mokesčius (EBIT) pagal juridinį subjektą, EBIT šiais metais ir praėjusiais metais, išlaidos ir įplaukų procentas, faktinės bei biudžeto išlaidos ir įplaukos                                                                                                                                                          |
| Įplaukų analizė            | Bendrosios įplaukos, faktinės ir biudžeto bendrosios įplaukos pagal juridinį subjektą, bendrosios įplaukos šiais metais ir praėjusiais metais, įplaukų biudžeto nuokrypis pagal juridinį subjektą ir bendrosios įplaukos šį laikotarpį ir paskutinįjį laikotarpį                                                                                                                                                 |
| Išlaidų analizė            | Bendrosios išlaidos, faktinės ir biudžeto bendrosios išlaidos pagal juridinį subjektą, faktinės ir biudžeto bendrosios išlaidos pagal ketvirtį, bendrosios išlaidos pagal sąskaitos kategoriją ir veiklos išlaidų koeficientas                                                                                                                                                                 |
| Įplaukų, kurioms išrašyta sąskaita, analizė     | Bendrosios gautinos sumos, bendrosios gautinos sumos pagal juridinį subjektą, bendrosios gautinos sumos pagal ketvirtį ir gautinų sumų sąskaitų balansai **Pastaba.** Į ataskaitas neįtraukti gautinų sumų DK sąskaitų pradžios balansai. Jose rodoma naujų operacijų, užregistruotų gautinose sumose, bendra suma. |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Duomenys, naudojami finansinės veiklos turinio paketo ataskaitų sritims ir ataskaitoms užpildyti, yra „Dynamics 365 for Operations“ duomenys. Toliau pateikti objektai buvo naudojami kaip turinio paketo pagrindas. **Duomenų objektų sujungimas**

-   **GeneralLedgerActivities** – šis įrašas sujungia DK balansus pagal sąskaitos kategoriją.
-   **BudgetActivities** – šis įrašas sujungia biudžeto balansus pagal sąskaitos kategoriją.

**Duomenų objektai**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Didžiosios knygos
-   ChartofAccounts

Šie objektai buvo naudojami skaičiuojamiems matams duomenų modelyje sukurti. Skaičiuojami matai naudojami skaičiuojant pagrindinius efektyvumo indikatorius (KPI) ir ataskaitas, naudojamas turinio pakete. Pagal numatytuosius parametrus turinio paketas pastarųjų trejų metų duomenis sutelkia į vienerius būsimus metus. Norėdami ataskaitas ir ataskaitų sritį įtraukti papildomų skaičiavimų, galite modifikuoti [„Microsoft Excel“ darbaknygę](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Ši darbaknygė yra numatytasis duomenų modelis, kuris buvo naudojamas turinio paketui kurti. Atlikę keitimus, galite kurti organizacinį turinio paketą ir ataskaitų sritį, kuriuose yra jūsų įtraukta informacija.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)





