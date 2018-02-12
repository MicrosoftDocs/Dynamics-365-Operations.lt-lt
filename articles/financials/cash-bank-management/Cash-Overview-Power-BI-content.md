---
title: "„Power BI“ turinys Grynųjų pinigų apžvalga"
description: "Šioje temoje aprašomas „Power BI‟ turinys Grynųjų pinigų apžvalga. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti."
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 5d02a009ca988f91a212e467d4f9784248bbae76
ms.contentlocale: lt-lt
ms.lasthandoff: 12/19/2017

---

# <a name="cash-overview-power-bi-content"></a>„Power BI“ turinys Grynųjų pinigų apžvalga

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI‟ turinys **Grynųjų pinigų apžvalga**. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti.

## <a name="overview"></a>Apžvalga

„Power BI‟ turinį **Grynųjų pinigų apžvalga** sukūrė asmenys, kurie atsakingi už grynuosius pinigus savo organizacijoje. „Power BI‟ turinys **Grynųjų pinigų apžvalga** suteikia galimybę matyti savo pinigų srautą. Taip pat pateikiama prognozė, kuri gali padėti priimti geresnius sprendimus ir pagerinti savo pinigų srauto būseną. Jūs galite analizuoti pinigus pagal juridinį subjektą, valiutą ir banko sąskaita, kad geriau suprastumėte perteklines ir trūkstamas sumas.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

„Power BI“ turinio **Grynųjų pinigų apžvalga** ataskaitos rodomos darbo srityse **Grynųjų pinigų apžvalga** ir **Banko valdymas**.

Norėdami peržiūrėti grynųjų pinigų srautų prognozės ataskaitas ir duomenis, pirmiausia, naudodami srityje Grynųjų pinigų ir banko valdymas esančią funkciją **Grynųjų pinigų srautų prognozės skaičiavimas**, turite paleisti prognozės skaičiavimo procesą.  Šį veiksmą reikia atlikti kiekvienai į prognozę įtrauktai įmonei.  Tada turite atnaujinti puslapyje **Objektų saugykla** esančią priemonę LedgerCovLiquidityMeasurement agregatas.  

Demonstravimo tikslais, naudodami puslapyje **Duomenų generavimas** pateiktą demonstracinių duomenų modulį galite įtraukti grynųjų pinigų srautų prognozės demonstracinius duomenis.  Scenarijus įterps duomenis į grynųjų pinigų srautų prognozės lentelės, kad ataskaitoms reikalingą informaciją būtų galima greitai įvesti.  Šis modulis galimas tik tada, jei aplinkoje įdiegtas demonstracinių duomenų paketo modelis. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Grynųjų pinigų apžvalga** ataskaitų puslapyje.

| Ataskaita                                | Turinys |
|---------------------------------------|----------|
| Grynųjų pinigų apžvalga – visos įmonės         | <ul><li>Įplaukos ir išmokos sistemos valiuta</li><li>Prognozuojami valiutos likučiai</li><li>Banko likutis sistemos valiuta</li><li>Likutis pagal juridinį subjektą</li><li>Šiandienos faktinis ir prognozuojamas likutis banko sąskaitos valiuta</li></ul> |
| Grynųjų pinigų apžvalga – dabartinė įmonė       | <ul><li>Įplaukos ir išmokos apskaitos valiuta</li><li>Prognozuojami valiutos likučiai</li><li>Banko likutis apskaitos valiuta</li><li>Šiandienos faktinis ir prognozuojamas likutis banko sąskaitos valiuta</li></ul> |
| Grynųjų pinigų srauto prognozė – visos įmonės    | <ul><li>Įplaukos ir išmokos sistemos valiuta</li><li>Dienos prognozės suvestinė</li><li>Prognozės informacija</li></ul> |
| Grynųjų pinigų srautų prognozė – valiutos įmonė | <ul><li>Įplaukos ir išmokos apskaitos valiuta</li><li>Dienos prognozės suvestinė</li><li>Prognozės informacija</li></ul> |
| Valiutos prognozė                     | <ul><li>Prognozuojami valiutos likučiai</li><li>Dienos valiutos suvestinė</li><li>Prognozės informacija</li></ul> |
| Banko likučiai                         | <ul><li>Banko likutis sistemos valiuta</li><li>Likutis pagal juridinį subjektą</li><li>Šiandienos faktinis ir prognozuojamas likutis banko sąskaitos valiuta</li><li>Likutis pagal banko sąskaitą</li><li>Balansas pagal valiutą</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Toliau pateiktoje lentelėje nurodomi objektai, kuriais pagrįstas „Power BI‟ turinys **Grynųjų pinigų apžvalga**.

| Objektas                                                                          | Turinys |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Įmonės, pagal kurias filtruojamos ataskaitos |
| LedgerCovLiquidityMeasurement\_Date                                             | Datos, pagal kurias filtruojamos ataskaitos |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Faktinis banko likutis palyginti su paskutiniu prognozuotu banko likučiu |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Prognozuotos operacijos informacija |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Grynųjų pinigų įplaukų, išmokų ir likučio suvestinė naudojant kiekvienos įmonės apskaitos valiutą |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Grynųjų pinigų įplaukų, išmokų ir likučio suvestinė naudojant visų įmonių sistemos valiutą |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Grynosios operacijos sumos ir valiutų likučio suvestinė naudojant operacijos valiutą |



