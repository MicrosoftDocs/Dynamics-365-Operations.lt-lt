---
title: "„Power BI“ turinys Kredito ir mokėjimų priežiūros valdymas"
description: "Šioje temoje paaiškinama, kas įtraukta į „Power BI“ turinį Kredito ir mokėjimų priežiūros valdymas. Joje paaiškinama, kaip pasiekti „Power BI“ ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, kurie naudojami turiniui kurti."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6ce0b7b35264c05555d8b3a18e70484202a289d6
ms.openlocfilehash: 3832cabb11d67eda7afd7f3d5322c005b36dc1f5
ms.contentlocale: lt-lt
ms.lasthandoff: 03/07/2018

---

# <a name="credit-and-collections-management-power-bi-content"></a>„Power BI“ turinys Kredito ir mokėjimų priežiūros valdymas

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kas įtraukta į „Microsoft Power BI“ turinį **Kredito ir mokėjimų priežiūros valdymas**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Apžvalga

„Power BI‟ turinys **Kredito ir mokėjimų priežiūros valdymas** buvo sukurtas kredito ir mokėjimų priežiūros vadybininkams ir mokėjimų priežiūros darbuotojams. Jame pateikiamos pagrindinės kredito ir mokėjimų priežiūros metrikos, pavyzdžiui, neapmokėta suma, pradelstas likutis, kredito ekspozicija ir kredito limitą viršiję klientai. Jame naudojami operaciniai duomenys ir pateikiami sujungti visų įmonių kredito ir mokėjimų priežiūros duomenų rodiniai. Jame taip pat pateikiamas paskirstymas kiekvienai įmonei, klientų grupei ir klientui.

Šį „Power BI‟ turinį sudaro 10 puslapių ataskaita:

- dviejų puslapių peržiūra (vienas puslapis skirtas kredito peržiūrai, o kitas puslapis – mokėjimų peržiūrai)
- aštuoni išsamios informacijos puslapiai, kuriuose pateikiama informacija apie įvairiose dimensijose paskirstytas kredito ir mokėjimų priežiūros metrikas

Visos sumos rodomos sistemos valiuta. Sistemos valiutą galite nustatyti puslapyje **Sistemos parametrai**.

Pagal numatytuosius nustatymus rodomi šios įmonės kredito ir mokėjimų priežiūros duomenys. Norėdami pamatyti visų įmonių duomenis, vaidmeniui priskirkite pareigą **CustCollectionsBICrossCompany**.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Kreditų ir mokėjimų priežiūros valdymas** rodomas darbo srityje **Klientų kredito ir mokėjimų priežiūra**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos

„Power BI‟ turinio pakete **CustCollectionsBICrossCompany** yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės Toliau pateiktoje lentelėje pateikiama „Power BI“ turinio **CustCollectionsBICrossCompany** vizualizacijų apžvalga.

| Ataskaitų puslapis                 | Vizualizacija |
|-----------------------------|---------------|
| Mokėjimų priežiūros peržiūra        | <ul><li>Klientai, kurių terminas praėjęs</li><li>Klientai, viršijantys kredito limitą</li><li>DSO 30 dienų</li><li>Atviri atvejai</li><li>Dienų iki atvejo uždarymo vidurkis</li><li>Atvira veikla</li><li>Dienų iki veiklų uždarymo vidurkis</li><li>Atidarytos delspinigių pažymos</li><li>Atidaryti mokėjimų priežiūros laiškai</li><li>Kliento sulaikymas</li><li>Pardavimo sulaikymas</li><li>Suskirstyti pagal terminus balansai</li><li>Mokėjimų priežiūros būsenos sumos</li><li>Mokėjimų priežiūros kodo sumos</li><li>Nurašymas pagal priežastį</li><li>Skolos likutis pagal regioną</li><li>Numatyti mokėjimai</li></ul> |
| Kredito peržiūra             | <ul><li>Klientai, kurių terminas praėjęs</li><li>Kredito limitas ir skolos likutis</li><li>Klientai, viršijantys kredito limito tinklelį</li><li>Klientai, viršijantys kredito limitą, pagal įmonę</li><li>Išnaudotas kreditas ir bendras kredito limitas</li><li>Kredito limitas, palyginti su išnaudotu kreditu pagal regioną</li><li>Klientai pagal kredito vertinimą</li></ul> |
| Kredito limitas                | <ul><li>Kredito limitas</li><li>Informacija apie kredito limitą</li><li>Kiekvieno kliento kredito limitas</li><li>Kredito limitas pagal klientų grupę</li><li>Kredito limitas pagal kredito vertinimą pagal įmonę</li><li>Kredito limitas, palyginti su išnaudotu kreditu pagal regioną</li></ul> |
| Klientai, viršijantys kredito limitą | <ul><li>Klientai, viršijantys kredito limitą</li><li>Informacija apie klientus, viršijančius kredito limitą</li><li>Klientai, viršijantys kredito limitą, pagal įmonę</li><li>Klientas, viršijantis kredito limitą, pagal klientų grupę</li><li>Klientai, viršijantys kredito limitą, pagal regioną</li></ul> |
| Klientai, kurių terminas praėjęs          | <ul><li>Klientai, kurių terminas praėjęs</li><li>Informacija apie klientą, kurio terminas praėjęs</li><li>Kliento pradelsimai pagal įmonę</li><li>Klientas, pradelsęs terminą, pagal klientų grupę</li><li>Klientas, kurio terminas praėjęs, pagal regioną</li></ul> |
| Suskirstyti pagal terminus balansai               | <ul><li>Suskirstyti pagal terminus balansai</li><li>Informacija apie pagal terminus suskirstytus likučius</li><li>Suskirstyti pagal terminus balansai pagal įmonę</li><li>Suskirstyti pagal terminus balansai pagal klientų grupę</li></ul> |
| Numatyti mokėjimai           | <ul><li>Numatyti mokėjimai</li><li>Informacija apie numatytus mokėjimus</li><li>Numatyti mokėjimai pagal įmonę</li><li>Numatyti mokėjimai pagal klientų grupę</li><li>Numatyti mokėjimai pagal regioną</li></ul> |
| Nurašymai                  | <ul><li>Nurašymai pagal regioną</li><li>Nurašymų informacija</li><li>Nurašymai pagal pagrindinę sąskaitą</li><li>Nurašymai pagal įmonę</li><li>Nurašymai pagal klientų grupę</li><li>Nurašymai pagal regioną</li></ul> |
| Mokėjimų priežiūros būsena          | <ul><li>Užginčyta</li><li>Pažadas sumokėti sulaužytas</li><li>Pažadas sumokėti</li><li>Informacija apie mokėjimų priežiūros būseną</li><li>Mokėjimų priežiūros būsenos sumos</li><li>Atviri atvejai</li><li>Atvira veikla</li></ul> |
| Priminimo laiškai         | <ul><li>Priminimo laiško kodo sumos</li><li>Priminimo laiško kodo sumos informacija</li><li>Priminimo laiško suma pagal įmonę</li><li>Priminimo laiško suma pagal klientų grupę</li><li>Priminimo laiško suma pagal regioną</li></ul> |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Norėdami eksportuoti vizualiai apibendrintus pagrindinius duomenis, taip pat galite naudoti pagrindinių duomenų eksportavimo funkciją.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Tolesniais duomenimis pildoma „Power BI‟ turinio **Kredito ir mokėjimų priežiūros valdymas** ataskaita. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. temoje [„Power BI‟ integravimo su objekto parduotuve apžvalga](../../dev-itpro/analytics/power-bi-integration-entity-store.md).


|                   Objektas                    |      Pagrindiniai agreguoti matavimo vienetai      |             Duomenų šaltinis              |                           Laukas                            |                                    aprašymas                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  |            smmActivities             | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) |     Uždarytų veiklų skaičius ir vidutinis laikas, skirtas uždaryti tas veiklas.     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           Atvirų veiklų skaičius.                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             Pagal terminus suskirstytų likučių suma.                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           Pradelstos sumos.                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases, CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        Uždarytų atvejų skaičius ir vidutinis laikas, skirtas uždaryti tuos atvejus.        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              Atvirų atvejų skaičius.                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       Atvirų priminimo laiškų skaičius.                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     Užregistruotų priminimo laiškų likutis.                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                Operacijų, kurioms nustatyta priminimo būsena, likutis.                 |
|           CustCollectionsBICredit           | CreditExposed, AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed), Sum(AmountOverCreditLimit)       | Kredito ekspozicijos suma ir klientų viršijamos kredito limito sumos. |
|         CustCollectionsBICustOnHold         |               Užblokuota                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     Sulaikytų klientų skaičius.                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        30 dienų pardavimo neapmokėjimo laikas dienomis                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 Numatytų kitų metų mokėjimų suma.                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                Sukurtų delspinigių pažymų skaičius.                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 Bendras sulaikytų pardavimo užsakymų skaičius.                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                Nurašytų operacijų suma.                 |


