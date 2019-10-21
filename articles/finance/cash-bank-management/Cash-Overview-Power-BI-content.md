---
title: „Power BI“ turinys Grynųjų pinigų apžvalga
description: Šioje temoje aprašomas „Power BI“ turinys Grynųjų pinigų apžvalga. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti.
author: saraschi2
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 553a4a5d25e126923576569b48414c46aab991ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179063"
---
# <a name="cash-overview-power-bi-content"></a>„Power BI“ turinys Grynųjų pinigų apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Grynųjų pinigų apžvalga**. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinį **Grynųjų pinigų apžvalga** sukūrė asmenys, kurie atsakingi už grynuosius pinigus savo organizacijoje. „Power BI“ turinys **Grynųjų pinigų apžvalga** suteikia galimybę matyti savo pinigų srautą. Taip pat pateikiama prognozė, kuri gali padėti priimti geresnius sprendimus ir pagerinti savo pinigų srauto būseną. Jūs galite analizuoti pinigus pagal juridinį subjektą, valiutą ir banko sąskaita, kad geriau suprastumėte perteklines ir trūkstamas sumas.

## <a name="setup-needed-to-view-power-bi-content"></a>Norint peržiūrėti „Power BI“ turinį reikia atlikti sąranką

Reikia atlikti toliau nurodytą sąranką, kad duomenys būtų rodomi **Grynųjų pinigų apžvalga** ir **Banko valdymas** „Power BI“ vaizdiniuose elementuose.

1. Eikite į **Sistemos administravimas > Sąranka > Sistemos parametrai** ir nustatykite **Sistemos valiuta** ir **Sistemos valiutos kursas**.
2. Norėdami nustatyti parinktis **Apskaitos valiuta** ir **Valiutos kurso tipas** eikite į **Didžioji knyga > Sąranka >DK**.
2. Nurodykite valiutos kursus tarp operacijos valiutų ir apskaitos valiutos, apskaitos valiutos ir sistemos valiutos, apskaitos valiutos ir banko valiutų. Norėdami tai padaryti, eikite į **Didžioji knyga > Valiutos > Valiutų kursai**.
3. Sukonfigūruokite ir vykdykite grynųjų pinigų srautų prognozavimą. Daugiau informacijos, kaip nustatyti grynųjų pinigų srautų prognozavimą, žr. <a href="https://docs.microsoft.com/dynamics365/unified-operations/financials/cash-bank-management/cash-flow-forecasting
">Grynųjų pinigų srautų prognozavimas</a>. 
4. Norėdami atnaujinti agreguotą matavimo vienetą **LedgerCovLiquidityMeasurement**, eikite į **Sistemos administravimas > Sąranka > Objektų saugykla**.

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

Toliau pateiktoje lentelėje nurodomi objektai, kuriais pagrįstas „Power BI“ turinys **Grynųjų pinigų apžvalga**.

| Objektas                                                                          | Turinys |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Įmonės, pagal kurias filtruojamos ataskaitos |
| LedgerCovLiquidityMeasurement\_Date                                             | Datos, pagal kurias filtruojamos ataskaitos |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Faktinis banko likutis palyginti su paskutiniu prognozuotu banko likučiu |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Prognozuotos operacijos informacija |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Grynųjų pinigų įplaukų, išmokų ir likučio suvestinė naudojant kiekvienos įmonės apskaitos valiutą |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Grynųjų pinigų įplaukų, išmokų ir likučio suvestinė naudojant visų įmonių sistemos valiutą |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Grynosios operacijos sumos ir valiutų likučio suvestinė naudojant operacijos valiutą |